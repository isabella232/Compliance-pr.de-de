---
title: Unveränderbarkeit von Daten in Microsoft 365
description: Erfahren Sie, wie Microsoft 365 Daten in auffindbarer Form aufbewahrt, um die Einhaltung gesetzlicher Vorschriften, interne Governanceanforderungen und Rechtsstreitigkeiten zu beheben.
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e17685c7d927ab8188abe1ef4dae4d2cdf0f3764
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482118"
---
# <a name="data-immutability-in-microsoft-365"></a>Unveränderbarkeit von Daten in Microsoft 365

Die Einhaltung gesetzlicher Vorschriften, interne Governanceanforderungen oder Rechtsstreitigkeiten erfordern, dass Organisationen E-Mails und zugehörige Daten in einer auffindbaren Form aufbewahren. Alle Daten im System müssen auffindbar sein, und keine davon kann zerstört oder geändert werden. Der branchenübliche Begriff hierfür lautet "Unveränderlichkeit".

Herkömmliche Methoden zur Unveränderlichkeit funktionierten in der Regel, indem E-Mail-Nachrichten an einen separaten, schreibgeschützten Speicherort verschoben wurden. Solche Systeme dienen zwar dazu, Postfachelemente für die Ermittlung zu erhalten, wirken sich jedoch häufig auf die Benutzererfahrung aus, indem beibehaltene Elemente aus dem täglichen Workflow entfernt werden. Für IT-Experten erfordert dieser Unveränderlichkeitsansatz die Bereitstellung und fortlaufende Wartung eines separaten Servers und einer separaten Speicherinfrastruktur. Die Ermittlung erfolgt mit Tools außerhalb des E-Mail-Systems und umfasst die zugehörigen Bereitstellungs- und Wartungskosten.

Durch die Funktionen der in-situ-Aufbewahrungs- und Aufbewahrungsrichtlinie für die Archivierung in Microsoft 365 und deren Diensten können Sie viele Klassen von eingehenden, internen und ausgehenden Daten beibehalten und aufbewahren. Dies umfasst Folgendes:

- Ein- und ausgehende E-Mail-Kommunikation
- Bücher und Datensätze, die in E-Mail-Form oder in freigegebenen Online-Dokumenten enthalten sind
- Besprechungsanfragen
- Faxe
- Chatnachrichten
- Während Onlinebesprechungen freigegebene Dokumente
- Voicemails

Darüber hinaus hat Microsoft Add-On-Features entwickelt, um die [Archivierung von Daten](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) aus anderen Quellen durch die Integration in Drittanbieterlösungen zur Datenerfassung und -verwaltung zu ermöglichen. Nachdem Drittanbieterdaten importiert wurden, können Sie Microsoft 365 Compliancefeatures auf die Daten anwenden, einschließlich:

- [Aufbewahrung für eventuelle Rechtsstreitigkeiten](/microsoft-365/compliance/create-a-litigation-hold)
- [In-Situ-eDiscovery und -Speicher](/microsoft-365/compliance/manage-legal-investigations)
- [Compliance-Suche](/microsoft-365/compliance/search-for-content)
- [In-Situ-Archivierung](/microsoft-365/compliance/enable-archive-mailboxes)
- [Postfachüberwachung](/microsoft-365/compliance/enable-mailbox-auditing)
- [Aufbewahrungsrichtlinien](/microsoft-365/compliance/retention-policies)

Wenn z. B. ein Postfach in die Beweissicherung für juristische Zwecke versetzt wird, werden Daten von Drittanbietern beibehalten. Sie können Daten von Drittanbietern mithilfe In-Place eDiscovery oder Compliance-Suche durchsuchen. Oder Sie können Archivierungs- und Aufbewahrungsrichtlinien auf Drittanbieterdaten anwenden, genau wie bei Microsoft-Daten. Die Archivierung von Daten von Drittanbietern in Microsoft 365 hilft Ihrer Organisation, die Einhaltung von Regierungsrichtlinien und behördlichen Richtlinien zu unterstützen.

Die Archivierung in Microsoft 365 bietet speicherkonforme Speicher der Securities and Exchange Commission (SEC) Rule 17a-4. Microsoft 365 permanente Dateien aller Daten, die in einem nicht umschreibbaren, nicht löschbaren Format gesammelt werden, mithilfe von in-situ-Aufbewahrungsrichtlinien und Erhaltungsrichtlinien, einschließlich Erhaltungssperre, aufbewahrt.

Insbesondere gilt:

- Alle Mithilfe der oben genannten Aufbewahrungsrichtlinien gespeicherten Datensätze werden in einem dedizierten Speicherbereich außerhalb der Bereinigung des normalen Benutzers aufbewahrt. Nur autorisierte Benutzer können auf diese Datensätze zugreifen und diese durchsuchen, jedoch nicht ändern oder löschen.
- Metadaten für jedes Element enthalten einen Zeitstempel, der bei der Berechnung der Aufbewahrungsdauer verwendet wird. Zeitstempel werden angewendet, wenn ein neues Element empfangen oder erstellt wird und nicht geändert oder aus den Metadaten entfernt werden kann.
- Die Archivierung in Microsoft 365 ermöglicht Benutzern, verschiedene Aufbewahrungsrichtlinien und Aufbewahrungsaktionen zu kombinieren, um granulare Aufbewahrungsrichtlinien zu erstellen. Diese Richtlinien definieren den Typ oder Speicherort der aufbewahrten Elemente und die Dauer der Aufbewahrung.
- Mit dem Feature "Erhaltungssperre" können Benutzer auswählen, ob die Richtlinie zu einer restriktiven Richtlinie werden soll. Eine restriktive Richtlinie verhindert, dass jemand die Möglichkeit hat, die Aufbewahrungsrichtlinie zu entfernen, zu deaktivieren oder Änderungen daran vorzunehmen. Dies bedeutet, dass die Erhaltungssperre nicht deaktiviert werden kann und kein Mechanismus vorhanden ist, unter dem Daten von vorhandenen Verwahrern, die von den vorhandenen Aufbewahrungsrichtlinien erfasst wurden, während des Aufbewahrungszeitraums überschrieben, geändert, gelöscht oder gelöscht werden können. Darüber hinaus kann der durch die Erhaltungssperre festgelegte Aufbewahrungszeitraum nicht verkürzt oder verringert werden. Sie kann jedoch verlängert werden, wenn eine gesetzliche Anforderung besteht, die Aufbewahrung der gespeicherten Daten fortzusetzen, wie oben erwähnt. Die Erhaltungssperre stellt sicher, dass niemand, nicht einmal Administratoren oder Personen mit bestimmtem Kontrollzugriff, die Einstellungen ändern oder gespeicherte Daten überschreiben oder löschen kann, wodurch die Archivierung in Microsoft 365 gemäß den Anweisungen in der 2003-Version der SEC-Regel 17a-4 erfolgt.

Informationen dazu, wie Microsoft 365 Ihnen dabei hilft, behördliche Verpflichtungen zu erfüllen, insbesondere im Hinblick auf die Anforderungen von Regel 17a-4, finden Sie im [Whitepaper](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf) zu Exchange Online-Archivierung, SharePoint Online, OneDrive for Business und Skype for Business. Das Whitepaper bietet außerdem eine ausführliche Analyse der Microsoft 365 Archivierungsfunktionen und -funktionen im Vergleich zu den anforderungen gemäß SEC-Regel 17a-4 und veranschaulicht regulierten Kunden, wie Microsoft 365 Archivierung es ihnen ermöglichen kann, diese Anforderungen zu erfüllen.
