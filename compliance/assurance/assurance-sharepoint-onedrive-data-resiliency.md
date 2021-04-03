---
title: SharePoint- und OneDrive-Datenresilienz in Microsoft 365
description: Dieser Artikel bietet eine Übersicht über die Ausfallsicherheit von SharePoint- und OneDrive-Daten in Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: c267551f26b4dd96e3762b0edc2942a3cb22eb5c
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496761"
---
# <a name="sharepoint-and-onedrive-data-resiliency-in-microsoft-365"></a>SharePoint- und OneDrive-Datenresilienz in Microsoft 365

In Microsoft 365 baut OneDrive auf der #A0 auf. In diesem Artikel wird nur SharePoint verwendet, um auf beide Produkte zu verweisen. Der Inhalt dieses Artikels ist für Microsoft 365 relevant und gilt nicht für Verbraucherdienste.

Es gibt zwei primäre Ressourcen, aus deren Kerninhaltsspeicherung SharePoint besteht:

- **Metadaten:** Metadaten zu jeder Datei werden in Azure SQL gespeichert. Azure SQL bietet einen vollständigen Geschäftskontinuitätsartikel, den SharePoint verwendet, und Details werden weiter später in diesem Artikel behandelt.
- **Blobspeicher:** Benutzerinhalte, die in SharePoint hochgeladen werden, werden in Azure Storage gespeichert. SharePoint hat einen benutzerdefinierten Ausfallsicherheitsplan auf Der Azure Storage erstellt, um eine nahezu Echtzeitduplizierung von Benutzerinhalten und einem wirklich aktiven/aktiven System sicherzustellen.

Der vollständige Satz von Steuerelementen zur Sicherstellung der Datenresilienz wird in weiteren Abschnitten erläutert.

## <a name="blob-storage-resilience"></a>Ausfallsicherheit von Blobspeichern

SharePoint verfügt über eine benutzerdefinierte Lösung zum Speichern von Kundendaten in Azure Storage. Jede Datei wird gleichzeitig in eine primäre und eine sekundäre Rechenzentrumsregion geschrieben. Wenn schreibe in eine der Azure-Regionen fehlschlagen, wird die Datei gespeichert. Nachdem die Inhalte in Azure Storage geschrieben wurden, werden Prüfsummen separat mit Metadaten gespeichert und verwendet, um sicherzustellen, dass der zugesagte Schreibzugriff mit der ursprünglichen Datei identisch ist, die während aller zukünftigen Lesezugriffe an SharePoint gesendet wurde. Dieselbe Technik wird in allen Workflows verwendet, um die Weitergabe von Beschädigungen zu verhindern, die auftreten sollten. In jeder Region bietet Azure Locally Redundant Storage (LRS) ein hohes Maß an Zuverlässigkeit. Weitere Informationen finden Sie im [Azure Storage-Redundanzartikel.](/azure/storage/common/storage-redundancy-lrs)

SharePoint verwendet Append-Only Speicher. Durch diesen Prozess wird sichergestellt, dass Dateien nach einem anfänglichen Speichern nicht geändert oder beschädigt werden können, aber auch mithilfe der produktin-produktin-versioning können alle vorherigen Versionen des Dateiinhalts abgerufen werden.

![Ausfallsicherheit von Blobspeichern](../media/assurance-blob-storage-resiliency-diagram.png)

SharePoint-Umgebungen in beiden Rechenzentren können auf Speichercontainer in beiden Azure-Regionen zugreifen. Aus Leistungsgründen wird der Speichercontainer im gleichen lokalen Datencenter immer bevorzugt. Leseanforderungen, für die keine Ergebnisse innerhalb eines gewünschten Schwellenwerts angezeigt werden, verfügen jedoch über denselben Inhalt, der vom Remotedatencenter angefordert wird, um sicherzustellen, dass Daten immer verfügbar sind.

## <a name="metadata-resilience"></a>Ausfallsicherheit von Metadaten

SharePoint-Metadaten sind auch für den Zugriff auf Benutzerinhalte von entscheidender Bedeutung, da sie den Speicherort von und den Zugriffsschlüsseln auf die in Azure Storage gespeicherten Inhalte speichern. Diese Datenbanken werden in Azure SQL gespeichert, das über einen umfassenden [Business Continuity Plan verfügt.](/azure/sql-database/sql-database-business-continuity)

SharePoint verwendet das von Azure SQL bereitgestellte Replikationsmodell und hat eine proprietäre Automatisierungstechnologie entwickelt, um zu ermitteln, ob ein Failover erforderlich ist, und um den Vorgang bei Bedarf zu initiieren. Daher fällt es aus Azure SQL-Sicht in die Kategorie "Manuelles Datenbankfailover". Die neuesten Metriken für azure SQL Datenbankerholbarkeit finden Sie [hier](/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview#recover-a-database-to-the-existing-server).

![Ausfallsicherheit von Metadaten](../media/assurance-metadata-resiliency-diagram.png)

SharePoint verwendet das SQL von Azure SQL, um Point in Time Restores (PITR) für bis zu 14 Tage zu aktivieren. PITR wird in einem späteren [Abschnitt behandelt.](#deletion-backup-and-point-in-time-restore)

## <a name="automated-failover"></a>Automatisiertes Failover

SharePoint verwendet ein benutzerdefiniertes automatisiertes Failover, um die Auswirkungen auf die Benutzererfahrung zu minimieren, wenn ein standortspezifisches Ereignis auftritt. Die überwachungsgesteuerte Automatisierung, bei der ein Einzelner- oder Mehrkomponentenfehler über bestimmte Schwellenwerte hinaus erkannt wird, führt zu einer automatischen Umleitung der Aktivitäten aller Benutzer aus der problematischen Umgebung und zu einer heißen sekundären Umgebung. Ein Failover führt dazu, dass Metadaten und Computespeicher vollständig aus dem neuen Datencenter entfernt werden. Da der Blobspeicher immer vollständig aktiv/aktiv ausgeführt wird, ist für ein Failover keine Änderung erforderlich. Die Computeebene bevorzugt den nächstgelegenen Blobcontainer, verwendet jedoch jederzeit lokale und Remote-Blobspeicherorte, um die Verfügbarkeit sicherzustellen.

SharePoint verwendet den Azure-Front-Door-Dienst, um das interne Routing an das Microsoft-Netzwerk zu ermöglichen. Diese Konfiguration ermöglicht die Failoverumleitung unabhängig von DNS und reduziert die Auswirkungen der Zwischenspeicherung auf lokale Computer. Die meisten Failovervorgänge sind für Endbenutzer transparent. Bei einem Failover müssen Kunden keine Änderungen vornehmen, um den Zugriff auf den Dienst aufrecht zu erhalten.

## <a name="versioning-and-files-restore"></a>Versions- und Dateiwiederherstellung

Bei neu erstellten Dokumentbibliotheken hat SharePoint standardmäßig 500 Versionen für jede Datei und kann so konfiguriert werden, dass bei Bedarf weitere Versionen beibehalten werden. Die Benutzeroberfläche lässt nicht zu, dass ein Wert unter 100 Versionen festgelegt wird, aber es ist möglich, das System so zu setzen, dass weniger Versionen mit öffentlichen APIs gespeichert werden. Aus Zuverlässigkeitssicht wird ein Beliebiger Wert unter 100 nicht empfohlen und kann zu Benutzeraktivitäten führen, die unbeabsichtigte Datenverluste verursachen.

Weitere Informationen zur Versionsierung finden Sie unter [Versioning in SharePoint](/microsoft-365/community/versioning-basics-best-practices).

Die Wiederherstellung von Dateien ist die Möglichkeit, in jeder Dokumentbibliothek in SharePoint zu jeder Sekunde in den letzten 30 Tagen "zurück in die Zeit" zu wechseln. Dieser Prozess kann zum Wiederherstellen von Ransomware, Massenlöschungen, Beschädigungen oder einem anderen Ereignis verwendet werden. Dieses Feature verwendet Dateiversionen, sodass das Reduzieren von Standardversionen die Effektivität dieser Wiederherstellung verringern kann.

Die Dateiwiederherstellungsfunktion ist sowohl für [OneDrive](https://support.office.com/article/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15) als auch [für SharePoint dokumentiert.](https://support.office.com/article/Restore-a-document-library-317791c3-8bd0-4dfd-8254-3ca90883d39a)

## <a name="deletion-backup-and-point-in-time-restore"></a>Lösch-, Sicherungs- und Zeitwiederherstellung

Aus SharePoint gelöschte Benutzerinhalte werden durch den folgenden Löschvorgang durchlauft.

Gelöschte Elemente werden für einen bestimmten Zeitraum in Papierkörbe aufbewahrt. Für SharePoint beträgt die Aufbewahrungszeit 93 Tage. Sie beginnt, wenn Sie das Element vom ursprünglichen Speicherort löschen. Wenn Sie das Element aus dem Websitepapierkorb löschen, wird es in den Papierkorb [der Websitesammlung eingeteilt.](https://support.office.com/article/restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) Er bleibt für die restlichen 93 Tage dort und wird dann endgültig gelöscht. Weitere Informationen zur Verwendung des Papierkorbs finden Sie unter den folgenden Links:

- [Wiederherstellen von Elementen im Papierkorb](https://support.office.com/article/Restore-items-in-the-Recycle-Bin-of-a-SharePoint-site-6df466b6-55f2-4898-8d6e-c0dff851a0be)
- [Wiederherstellen gelöschter Elemente aus dem Papierkorb der Websitesammlung](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b).

Dieser Prozess ist der Standardlöschvorgang und berücksichtigt keine Aufbewahrungsrichtlinien oder Bezeichnungen. Weitere Informationen finden Sie [unter Learn about retention for SharePoint and OneDrive](/microsoft-365/compliance/retention-policies-sharepoint).

Nach Abschluss der 93-tägigen Recyclingpipeline erfolgt das Löschen unabhängig von Metadaten und Blob Storage. Metadaten werden sofort aus der Datenbank entfernt, wodurch der Inhalt unlesbar wird, es sei denn, die Metadaten werden aus der Sicherung wiederhergestellt. SharePoint verwaltet 14 Tage Sicherungskopien von Metadaten. Diese Sicherungen werden lokal in nahezu Echtzeit erstellt und dann in redundanten Azure Storage-Containern in einem 5-10-Minütigen Zeitplan [gespeichert.](/azure/sql-database/sql-database-automated-backups)

Beim Löschen von Blob Storage-Inhalten verwendet SharePoint das Feature zum soft delete für Azure Blob Storage, um vor versehentlichem oder böswilligem Löschen zu schützen. Mit diesem Feature haben wir insgesamt 14 Tage Zeit, Inhalte wiederherzustellen, bevor sie endgültig gelöscht werden.

>[!Note]
>Während Microsoft-Anwendungen Inhalte für den Standardprozess an den Papierkorb senden, stellt SharePoint APIs zur Verfügung, mit denen der Papierkorb übersprungen und ein sofortiges Löschen erzwungen werden kann. Überprüfen Sie Ihre Anwendungen, um sicherzustellen, dass dies aus Compliancegründen nur bei Bedarf erfolgt.

## <a name="integrity-checks"></a>Integritätsüberprüfungen

SharePoint verwendet verschiedene Methoden, um die Integrität von Blobs und Metadaten in allen Phasen des Datenlebenszyklus sicherzustellen:

- **In Metadaten gespeicherter** Dateihash: Hash der gesamten Datei wird mit Dateimetadaten gespeichert, um sicherzustellen, dass die Datenintegrität auf Dokumentebene während aller Vorgänge beibehalten wird
- **In Metadaten gespeicherter** Blobhash: Jedes Blobelement speichert einen Hash des verschlüsselten Inhalts, um beschädigungen im zugrunde liegenden #A0 zu schützen.
- Datenintegritätsauftrag: Alle 14 Tage wird jede Website auf Integrität überprüft, indem Elemente in der Datenbank aufgelistet und mit den aufgelisteten Blobs im Azure-Speicher abgegleicht werden. Der Auftrag meldet alle Blobverweise fehlender Speicher-Blobs und kann diese Blobs bei Bedarf über die [Soft-Delete-Funktion](/azure/storage/blobs/soft-delete-blob-overview) des Azure-Speichers abrufen.
