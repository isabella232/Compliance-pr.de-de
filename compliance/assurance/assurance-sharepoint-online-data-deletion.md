---
title: Microsoft 365 SharePoint Löschen von Onlinedaten
description: Erfahren Sie, wie das Löschen von Daten in SharePoint Online funktioniert, z. B. wo und wie lange gelöschte Inhalte gespeichert werden.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 3545a6e5746553e59603fbf68432ee4705a21f3f
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159585"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>SharePoint Löschen von Onlinedaten in Microsoft 365

SharePoint Online speichert Objekte als abstrahierten Code in Anwendungsdatenbanken. Wenn ein Benutzer eine Datei in SharePoint Online hochlädt, wird diese Datei zerlegt und in Anwendungscode übersetzt und in mehreren Tabellen über mehrere Datenbanken hinweg gespeichert. In SharePoint Online werden alle Inhalte, die ein Kunde hochlädt, in Blöcke aufgeteilt, verschlüsselt (möglicherweise mit mehreren AES 256-Bit-Schlüsseln) und über das Rechenzentrum verteilt. Spezifische Informationen zum Blockierungs- und Verschlüsselungsprozess finden Sie unter ["Verschlüsselung in der Microsoft Cloud".](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview) 

In SharePoint Online werden Elemente ab dem Zeitpunkt, an dem Sie sie von ihrem ursprünglichen Speicherort löschen, 93 Tage lang aufbewahrt. Sie verbleiben die gesamte Zeit im Papierkorb der Website, es sei denn, jemand löscht sie dort oder leert diesen Papierkorb. In diesem Fall werden die Elemente in den Papierkorb der Websitesammlung verschoben, wo sie für den Rest der 93 Tage verbleiben. Informationen zum Wiederherstellen gelöschter Elemente finden Sie unter [Wiederherstellen von Elementen im Papierkorb einer SharePoint Website](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) und [Wiederherstellen gelöschter Elemente aus dem Papierkorb der Websitesammlung.](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b) Die Aufbewahrungszeit des Papierkorbs kann in SharePoint Online nicht konfiguriert werden.

Wenn Sie eine Websitesammlung löschen, löschen Sie auch die Hierarchie der Websites in der Sammlung und alle darin enthaltenen Inhalte:

- Dokumente und Dokumentbibliotheken
- Listen und Listendaten
- Standortkonfigurationseinstellungen
- Rollen- und Sicherheitsinformationen im Zusammenhang mit der Website oder deren Unterwebsites
- Unterwebsites der Website auf oberster Ebene, deren Inhalte und Benutzerinformationen

Wenn Sie versehentlich eine Websitesammlung löschen, kann sie von einem globalen oder SharePoint-Administrator über das SharePoint Admin Center wiederhergestellt werden.

Gelöschte Websitesammlungen werden 93 Tage lang aufbewahrt. Nach 93 Tagen werden Websites sowie alle Inhalte und Einstellungen, einschließlich Listen, Bibliotheken, Seiten und Unterwebsites, dauerhaft gelöscht.

Das endgültige Löschen erfolgt, wenn ein Benutzer gelöschte Elemente aus dem Papierkorb der Websitesammlung löscht, wenn die Aufbewahrungs- und Sicherungszeiträume ablaufen oder wenn ein Administrator eine Websitesammlung mithilfe des [Cmdlets "Remove-SPODeletedSite"](/powershell/module/sharepoint-online/remove-spodeletedsite)endgültig löscht. Wenn ein Benutzer Inhalte aus SharePoint Online endgültig löscht (endgültig löscht oder löscht), werden auch alle Verschlüsselungsschlüssel für die gelöschten Blöcke gelöscht. Die Blöcke auf den Datenträgern, auf denen zuvor die gelöschten Blöcke gespeichert wurden, werden als nicht verwendet markiert und stehen zur Wiederverwendung zur Verfügung.
