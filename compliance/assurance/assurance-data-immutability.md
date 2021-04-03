---
title: Unveränderlichkeit von Daten in Microsoft 365
description: Erfahren Sie, wie Microsoft 365 Daten in auf lesbarer Form erhält, um rechtliche Compliance, interne Steuerungsanforderungen und Prozessrisiken zu erfüllen.
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2e86cdfe082ec35fd7fd111a13a4def6f1b01806
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497627"
---
# <a name="data-immutability-in-microsoft-365"></a>Unveränderlichkeit von Daten in Microsoft 365

Behördliche Compliance, interne Steuerungsanforderungen oder Rechtsstreitigkeiten erfordern, dass Organisationen E-Mails und zugeordnete Daten in einer auffingbaren Form beibehalten. Alle Daten im System müssen ermittelt werden können, und keine daten kann zerstört oder geändert werden. Der Branchenstandardbegriff dafür ist "Unveränderlichkeit".

Herkömmliche Methoden zur Unveränderlichkeit funktionierten in der Regel durch Verschieben von E-Mail-Nachrichten an einen separaten, schreibgeschützten Speicherort. Solche Systeme dienen zwar zum Beibehalten von Postfachelementen für die Ermittlung, wirken sich jedoch häufig auf die Benutzerfreundlichkeit aus, indem beibehaltene Elemente aus dem üblichen täglichen Workflow entfernt werden. Für IT-Experten erfordert dieser Unveränderlichkeitsansatz die Bereitstellung und laufende Wartung einer separaten Server- und Speicherinfrastruktur. Die Ermittlung erfolgt mit Tools außerhalb des E-Mail-Systems und umfasst die zugehörigen Bereitstellungs- und Wartungskosten.

Durch die Features der archivierungsinternen Aufbewahrungs- und Aufbewahrungsrichtlinie in Microsoft 365 und seinen Diensten können Sie viele Klassen eingehender, interner und ausgehender Daten beibehalten und beibehalten. Dies umfasst Folgendes:

- Ein- und ausgehende E-Mail-Kommunikation
- Bücher und Datensätze, die in E-Mail-Form oder in freigegebenen Online-Dokumenten enthalten sind
- Besprechungsanfragen
- Faxe
- Chatnachrichten
- Während Onlinebesprechungen freigegebene Dokumente
- Voicemails

Darüber hinaus hat Microsoft Add-On-Features entwickelt, um die Archivierung von Daten aus anderen Quellen durch die Integration in Drittanbieterlösungen für die Datenerfassung und -verwaltung zu ermöglichen. [](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) Nachdem Daten von Drittanbietern importiert wurden, können Sie Microsoft 365-Compliancefeatures auf die Daten anwenden, einschließlich:

- [Aufbewahrung für eventuelle Rechtsstreitigkeiten](/microsoft-365/compliance/create-a-litigation-hold)
- [In-Situ-eDiscovery und -Speicher](/microsoft-365/compliance/manage-legal-investigations)
- [Compliance-Suche](/microsoft-365/compliance/search-for-content)
- [In-Situ-Archivierung](/microsoft-365/compliance/enable-archive-mailboxes)
- [Postfachüberwachung](/microsoft-365/compliance/enable-mailbox-auditing)
- [Aufbewahrungsrichtlinien](/microsoft-365/compliance/retention-policies)

Wenn z. B. ein Postfach in das Prozesssicherungsverfahren einbehalten wird, werden Daten von Drittanbietern beibehalten. Sie können Daten von Drittanbietern mithilfe In-Place eDiscovery- oder Compliancesuche durchsuchen. Oder Sie können Archivierungs- und Aufbewahrungsrichtlinien auf Daten von Drittanbietern anwenden, genau wie bei Microsoft-Daten. Die Archivierung von Drittanbieterdaten in Microsoft 365 hilft Ihrer Organisation, die Richtlinien von Behörden und Behörden zu erfüllen.

Die Archivierung in Microsoft 365 bietet Securities and Exchange Commission (SEC) Regel 17a-4-kompatiblen Speicher. Microsoft 365 bewahrt permanente Dateien aller Daten auf, die in einem nicht umschreibbaren, nicht löschbaren Format mithilfe von Aufbewahrungsrichtlinien und Aufbewahrungsrichtlinien gespeichert werden, einschließlich der Erhaltungssperre.

Insbesondere gilt:

- Alle Datensätze, die mithilfe der oben genannten Aufbewahrungsrichtlinien gespeichert werden, werden in einem dedizierten Speicherbereich aufbewahrt, der nicht dem normalen Benutzer zur Verfügung stehen soll. Nur autorisierte Benutzer können auf diese Datensätze zugreifen und diese durchsuchen, können sie jedoch nicht ändern oder löschen.
- Metadaten für jedes Element enthalten einen Zeitstempel, der bei der Berechnung der Aufbewahrungsdauer verwendet wird. Zeitstempel werden angewendet, wenn ein neues Element empfangen oder erstellt wird und nicht geändert oder aus den Metadaten entfernt werden kann.
- Durch die Archivierung in Microsoft 365 können Benutzer unterschiedliche Aufbewahrungsrichtlinien kombinieren und Aktionen durchführen, um präzise Aufbewahrungsrichtlinien zu erstellen. Diese Richtlinien definieren den Typ oder Speicherort der beibehaltenen Elemente und die Dauer der Aufbewahrung.
- Mit dem Feature "Erhaltungssperre" können Benutzer auswählen, ob die Richtlinie zu einer restriktiven Richtlinie gemacht werden soll. Eine restriktive Richtlinie verhindert, dass jeder Benutzer die Möglichkeit hat, die Aufbewahrungsrichtlinie zu entfernen, zu deaktivieren oder änderungen vorzunehmen. Dies bedeutet, dass nach aktivierung der Erhaltungssperre nicht deaktiviert werden kann und kein Mechanismus vorhanden ist, unter dem daten von vorhandenen Verwahrern, die von den geltenden Aufbewahrungsrichtlinien gesammelt wurden, während des Aufbewahrungszeitraums überschrieben, geändert, gelöscht oder gelöscht werden können. Darüber hinaus kann der von der Erhaltungssperre festgelegte Haltezeitraum nicht verkürzt oder verringert werden. Es kann jedoch verlängert werden, wenn eine gesetzliche Anforderung besteht, die Aufbewahrung der gespeicherten Daten wie oben erwähnt fortzufahren. Die Erhaltungssperre stellt sicher, dass niemand, nicht einmal Administratoren oder Personen mit bestimmtem Steuerelementzugriff, die Einstellungen ändern oder gespeicherte Daten überschreiben oder löschen kann, was die Archivierung in Microsoft 365 im Einklang mit den Anweisungen in der 2003 Release of SEC Rule 17a-4 enthält.

Informationen dazu, wie Microsoft 365 Ihnen bei der Erfüllung gesetzlicher Verpflichtungen hilft, [](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf) insbesondere in Bezug auf Regel 17a-4-Anforderungen, finden Sie im Whitepaper zu Exchange Online-Archivierung, SharePoint Online, OneDrive for Business und Skype for Business. Das Whitepaper enthält außerdem eine eingehende Analyse der Archivierungsfeatures und -funktionen von Microsoft 365 gemäß den anforderungen gemäß SEC Rule 17a-4 und veranschaulicht regulierten Kunden, wie die Microsoft 365-Archivierung diese Anforderungen erfüllen kann.
