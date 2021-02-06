---
title: Löschen von Microsoft 365 SharePoint Online-Daten
description: Erfahren Sie, wie das Löschen von Daten in SharePoint Online funktioniert, z. B. wo gelöschte Inhalte gespeichert werden und wie lange.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 89281b32dbc577f935224396fd358ed753348ea1
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120744"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>Löschen von SharePoint Online-Daten in Microsoft 365

SharePoint Online speichert Objekte als abstrahierten Code in Anwendungsdatenbanken. Wenn ein Benutzer eine Datei in SharePoint Online hochlädt, wird diese Datei zerlegt und in Anwendungscode übersetzt und in mehreren Tabellen über mehrere Datenbanken hinweg gespeichert. In SharePoint Online werden alle Inhalte, die ein Kunde hochlädt, in Blöcke aufgeteilt, verschlüsselt (möglicherweise mit mehreren AES 256-Bit-Schlüsseln) und über das Rechenzentrum verteilt. Einzelheiten zum Blockierungs- und Verschlüsselungsprozess finden Sie unter ["Verschlüsselung in der Microsoft Cloud".](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview) 

In SharePoint Online werden Elemente ab dem Zeitpunkt, an dem Sie sie von ihrem ursprünglichen Speicherort löschen, 93 Tage lang aufbewahrt. Sie bleiben die gesamte Zeit im Papierkorb der Website, es sei denn, jemand löscht sie dort oder leert diesen Papierkorb. In diesem Fall wechseln die Elemente in den Papierkorb der Websitesammlung, wo sie für die restlichen 93 Tage bleiben. Informationen zum Wiederherstellen gelöschter Elemente finden Sie unter "Wiederherstellen von Elementen im Papierkorb einer [SharePoint-Website"](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) und "Wiederherstellen gelöschter Elemente aus dem Papierkorb der [Websitesammlung".](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b) Die Aufbewahrungszeit für den Papierkorb kann in SharePoint Online nicht konfiguriert werden.

Wenn Sie eine Websitesammlung löschen, löschen Sie auch die Hierarchie der Websites in der Auflistung und den inhalten:

- Dokumente und Dokumentbibliotheken
- Listen und Listendaten
- Standortkonfigurationseinstellungen
- Rollen- und Sicherheitsinformationen im Zusammenhang mit der Website oder deren Unterwebsites
- Unterwebsites der Website auf oberster Ebene, deren Inhalte und Benutzerinformationen

Wenn Sie eine Websitesammlung versehentlich löschen, kann sie von einem globalen oder SharePoint-Administrator über das SharePoint Admin Center wiederhergestellt werden.

Gelöschte Websitesammlungen werden 93 Tage lang aufbewahrt. Nach 93 Tagen werden Websites sowie alle Inhalte und Einstellungen, einschließlich Listen, Bibliotheken, Seiten und Unterwebsites, dauerhaft gelöscht.

Das endgültige Löschen erfolgt, wenn ein Benutzer gelöschte Elemente aus dem Papierkorb der Websitesammlung löscht, wenn die Aufbewahrungs- und Sicherungszeiträume ablaufen oder wenn ein Administrator eine Websitesammlung mithilfe des [Cmdlets "Remove-SPODeletedSite"](/powershell/module/sharepoint-online/remove-spodeletedsite)endgültig löscht. Wenn ein Benutzer Inhalte endgültig aus SharePoint Online löscht (endgültig löscht oder löscht), werden auch alle Verschlüsselungsschlüssel für die gelöschten Blöcke gelöscht. Die Blöcke auf den Datenträgern, die zuvor die gelöschten Blöcke gespeichert haben, werden als nicht verwendet markiert und können wiederver verwendet werden.
