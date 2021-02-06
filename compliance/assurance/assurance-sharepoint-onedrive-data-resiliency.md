---
title: 'SharePoint- und #A0 in Microsoft 365'
description: Dieser Artikel bietet eine Übersicht über die Datenresilienz von SharePoint und OneDrive in Microsoft 365.
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
ms.openlocfilehash: 26281e076ea2500a0a4071233b88c2a1f23fe9c5
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120454"
---
# <a name="sharepoint-and-onedrive-data-resiliency-in-microsoft-365"></a>SharePoint- und #A0 in Microsoft 365

In Microsoft 365 baut OneDrive auf der #A0 auf. In diesem Artikel wird nur SharePoint verwendet, um auf beide Produkte zu verweisen. Der Inhalt dieses Artikels ist für Microsoft 365 relevant und gilt nicht für Verbraucherdienste.

Es gibt zwei primäre Ressourcen, aus deren Kerninhaltsspeicherung SharePoint besteht:

- **Metadaten:** Metadaten zu jeder Datei werden in Azure SQL gespeichert. Azure SQL bietet eine vollständige Geschäftskontinuitätsgeschichte, die SharePoint verwendet, und Details werden weiter später in diesem Artikel behandelt.
- **Blobspeicher:** Benutzerinhalte, die in SharePoint hochgeladen werden, werden in Azure Storage gespeichert. SharePoint hat einen benutzerdefinierten Ausfallsicherheitsplan auf der Oberseite von Azure Storage erstellt, um eine nahezu Echtzeitduplizierung von Benutzerinhalten und ein wirklich aktives/aktives System sicherzustellen.

Der vollständige Satz von Steuerelementen zur Sicherstellung der Datenresilienz wird in weiteren Abschnitten erläutert.

## <a name="blob-storage-resilience"></a>Blobspeicherresilienz

SharePoint verfügt über eine benutzerdefinierte Lösung zum Speichern von Kundendaten in Azure Storage. Jede Datei wird gleichzeitig in eine primäre und eine sekundäre Rechenzentrumsregion geschrieben. Wenn schreibe in eine der Azure Regionen fehlschlagen, wird die Datei gespeichert. Nachdem die Inhalte in Azure Storage geschrieben wurden, werden Prüfsummen separat mit Metadaten gespeichert und verwendet, um sicherzustellen, dass der geschriebene Schreibzugriff mit der ursprünglichen Datei identisch ist, die während aller zukünftigen Lesezugriffe an SharePoint gesendet wird. Dieselbe Technik wird in allen Workflows verwendet, um die Weitergabe von Beschädigungen zu verhindern, die auftreten sollten. Innerhalb jeder Region bietet Azure Locally Redundant Storage (LRS) ein hohes Maß an Zuverlässigkeit. Weitere Informationen finden Sie im Artikel zur Azure Storage-Redundanz. [](/azure/storage/common/storage-redundancy-lrs)

SharePoint verwendet Append-Only Speicher. Dadurch wird sichergestellt, dass Dateien nach dem ersten Speichern nicht geändert oder beschädigt werden können, aber auch mithilfe der Produktversionsfreigabe kann jede frühere Version des Dateiinhalts abgerufen werden.

SharePoint-Umgebungen in beiden Rechenzentren können auf Speichercontainer in beiden Regionen von Azure zugreifen. Aus Leistungsgründen wird der Speichercontainer im gleichen lokalen Datencenter immer bevorzugt. Leseanforderungen, die keine Ergebnisse innerhalb eines gewünschten Schwellenwerts sehen, verfügen jedoch über denselben Inhalt, der vom Remotedatencenter angefordert wird, um sicherzustellen, dass Daten immer verfügbar sind.

## <a name="metadata-resilience"></a>Metadatenresilienz

SharePoint-Metadaten sind auch wichtig für den Zugriff auf Benutzerinhalte, da sie den Speicherort von und den Zugriffsschlüssel auf die in Azure Storage gespeicherten Inhalte speichern. Diese Datenbanken werden in Azure SQL gespeichert, das einen umfassenden [Geschäftskontinuitätsplan hat.](/azure/sql-database/sql-database-business-continuity)

SharePoint verwendet das von Azure SQL bereitgestellte Replikationsmodell und hat eine proprietäre Automatisierungstechnologie entwickelt, um zu bestimmen, dass ein Failover erforderlich ist, und um den Vorgang bei Bedarf zu initiieren. Daher fällt sie aus Azure-Sicht in die Kategorie "Manuelles Datenbankfailover", SQL ist. Die neuesten Metriken für die Wiederherstellung SQL Azure-Datenbanken sind [hier verfügbar.](/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview#recover-a-database-to-the-existing-server)

SharePoint verwendet das SQL von Azure, um Point in Time Restores (PITR) für bis zu 14 Tage zu aktivieren. PITR wird in einem späteren [Abschnitt behandelt.](#deletion-backup-and-point-in-time-restore)

## <a name="automated-failover"></a>Automatisiertes Failover

SharePoint verwendet ein benutzerdefiniertes automatisiertes Failover, um die Auswirkungen auf die Kundenerfahrung zu minimieren, wenn ein standortspezifisches Ereignis auftritt. Die überwachungsgesteuerte Automatisierung, die einen Einzelnen- oder Mehrkomponentenfehler über bestimmte Schwellenwerte hinaus erkennt, führt zu einer automatischen Umleitung aller Benutzeraktivitäten aus der problematischen Umgebung und zu einer warmen sekundären Umgebung. Ein Failover führt dazu, dass Metadaten und Computespeicher vollständig aus dem neuen Rechenzentrum bedient werden. Da der Blobspeicher immer vollständig aktiv/aktiv ausgeführt wird, ist für ein Failover keine Änderung erforderlich. Die Computeebene bevorzugt den nächstgelegenen BLOB-Container, verwendet jedoch jederzeit lokale und Remote-BLOB-Speicherspeicherorte, um die Verfügbarkeit sicherzustellen.

SharePoint verwendet den Azure Front Door-Dienst, um internes Routing an das Microsoft-Netzwerk zu ermöglichen. Diese Konfiguration ermöglicht die Failoverumleitung unabhängig von DNS und reduziert die Auswirkungen des Zwischenspeicherns auf lokale Computer. Die meisten Failovervorgänge sind für Endbenutzer transparent. Bei einem Failover müssen Kunden keine Änderungen vornehmen, um den Zugriff auf den Dienst zu erhalten.

## <a name="versioning-and-files-restore"></a>Versions- und Dateiwiederherstellung

Bei neu erstellten Dokumentbibliotheken verwendet SharePoint standardmäßig 500 Versionen für jede Datei und kann so konfiguriert werden, dass bei Bedarf weitere Versionen beibehalten werden. Die Benutzeroberfläche lässt nicht zu, dass ein Wert von weniger als 100 Versionen festgelegt wird, aber es ist möglich, das System so zu gestalten, dass weniger Versionen mit öffentlichen APIs gespeichert werden. Aus Zuverlässigkeitssicht wird jeder Wert unter 100 nicht empfohlen und kann zu Benutzeraktivitäten führen, die zu versehentlichen Datenverlusten führen.

Weitere Informationen zur Versionsfreigabe finden Sie unter [Versionsinformationen in SharePoint.](/microsoft-365/community/versioning-basics-best-practices)

Die Wiederherstellung von Dateien ist die Möglichkeit, in jeder Dokumentbibliothek in SharePoint zu jeder Sekunde in den letzten 30 Tagen zurück in die Zeit zu wechseln. Dieser Prozess kann verwendet werden, um nach Ransomware, Massenlöschvorgängen, Beschädigungen oder einem anderen Ereignis wiederhergestellt zu werden. Dieses Feature verwendet Dateiversionen, sodass das Reduzieren von Standardversionen die Effektivität dieser Wiederherstellung verringern kann.

Die Dateiwiederherstellungsfunktion ist für [OneDrive](https://support.office.com/article/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15) und [SharePoint dokumentiert.](https://support.office.com/article/Restore-a-document-library-317791c3-8bd0-4dfd-8254-3ca90883d39a)

## <a name="deletion-backup-and-point-in-time-restore"></a>Lösch-, Sicherungs- und Zeitpunktwiederherstellung

Benutzerinhalte, die aus SharePoint gelöscht wurden, werden durch den folgenden Löschvorgang durchf?en.

Gelöschte Elemente werden für einen bestimmten Zeitraum in Papierkörbe aufbewahrt. Für SharePoint beträgt die Aufbewahrungszeit 93 Tage. Sie beginnt, wenn Sie das Element am ursprünglichen Speicherort löschen. Wenn Sie das Element aus dem Papierkorb der Website löschen, wird es in den Papierkorb [der Websitesammlung eingeteilt.](https://support.office.com/article/restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b) Sie bleibt für die restlichen 93 Tage dort und wird dann endgültig gelöscht. Weitere Informationen zur Verwendung des Papierkorbs finden Sie unter den folgenden Links:

- [Wiederherstellen von Elementen im Papierkorb](https://support.office.com/article/Restore-items-in-the-Recycle-Bin-of-a-SharePoint-site-6df466b6-55f2-4898-8d6e-c0dff851a0be)
- [Wiederherstellen gelöschter Elemente aus dem Papierkorb der Websitesammlung.](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b)

Dieser Vorgang ist der Standardmäßige Löschvorgang und berücksichtigt keine Aufbewahrungsrichtlinien oder Bezeichnungen. Weitere Informationen finden Sie unter [Informationen zur Aufbewahrung für SharePoint und OneDrive](/microsoft-365/compliance/retention-policies-sharepoint).

Nach Abschluss der 93-tägigen Recyclepipeline erfolgt der Löschvorgang unabhängig für Metadaten und blob-Speicher. Metadaten werden sofort aus der Datenbank entfernt, wodurch der Inhalt unlesbar wird, es sei denn, die Metadaten werden aus der Sicherung wiederhergestellt. SharePoint verwaltet 14 Tage dauernde Sicherungen von Metadaten. Diese Sicherungen werden nahezu in Echtzeit lokal erstellt und dann in [](/azure/sql-database/sql-database-automated-backups) redundanten Azure Storage-Containern in einem 5-10-minütigen Zeitplan in der Dokumentation zum Zeitpunkt dieser Veröffentlichung gespeichert.

Beim Löschen von Blob Storage-Inhalten verwendet SharePoint das Soft Delete-Feature für Azure Blob Storage, um vor versehentlichem oder böswilligem Löschen zu schützen. Bei Verwendung dieses Features haben wir insgesamt 14 Tage Zeit, Inhalte wiederherzustellen, bevor sie endgültig gelöscht werden.

>[!Note]
>Während microsoft-Anwendungen Inhalte für den Standardprozess an den Papierkorb senden, stellt SharePoint APIs zur Verfügung, mit denen der Papierkorb übersprungen und ein sofortiges Löschen erzwungen werden kann. Überprüfen Sie Ihre Anwendungen, um sicherzustellen, dass dies nur bei Bedarf aus Compliancegründen erfolgt.

## <a name="integrity-checks"></a>Integritätsüberprüfungen

SharePoint verwendet verschiedene Methoden, um die Integrität von BLOBS und Metadaten in allen Phasen des Datenlebenszyklus sicherzustellen:

- **In Metadaten gespeicherter** Dateihash: Hash der gesamten Datei wird mit Dateimetadaten gespeichert, um sicherzustellen, dass die Datenintegrität auf Dokumentebene während aller Vorgänge beibehalten wird
- **#A0 in Metadaten gespeichert:** Jedes #A1 speichert einen Hash des verschlüsselten Inhalts, um sich vor Beschädigungen im zugrunde liegenden #A2 zu schützen.
- Datenintegritätsauftrag: Alle 14 Tage wird jede Website auf Integrität überprüft, indem Elemente in der Datenbank aufgelistet und mit den aufgelisteten Blobs im Azure Storage abgegleich werden. Der Auftrag meldet alle BLOB-Verweise auf fehlende Speicher-BLOBs und kann diese BLOBs bei Bedarf über das [Azure Storage Soft-Delete-Feature](/azure/storage/blobs/soft-delete-blob-overview) abrufen.
