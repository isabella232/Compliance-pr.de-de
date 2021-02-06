---
title: Unveränderlichkeit von Daten in Microsoft 365
description: Erfahren Sie, wie Microsoft 365 Daten in auf discoverabler Form beibewahrt, um rechtliche Vorschriften, interne Governanceanforderungen und Risiken für Rechtsstreitigkeiten zu erfüllen.
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
ms.openlocfilehash: da465b850a9216dd64f8e4d9e6450c6a17f7b26d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120664"
---
# <a name="data-immutability-in-microsoft-365"></a>Unveränderlichkeit von Daten in Microsoft 365

Die Einhaltung gesetzlicher Vorschriften, interne Steuerungsanforderungen oder Risiken bei Rechtsstreitigkeiten erfordern, dass Organisationen E-Mails und zugehörige Daten in einer aufsentlichen Form beibehalten. Alle Daten im System müssen auf discoverable sein, und keines davon kann zerstört oder geändert werden. Der Branchenstandardbegriff dafür ist "Unveränderlichkeit".

Herkömmliche Methoden zur Unveränderlichkeit funktionierten in der Regel, indem E-Mail-Nachrichten an einen separaten, schreibgeschützten Speicherort verschieben. Solche Systeme dienen zwar dazu, Postfachelemente für die Ermittlung zu erhalten, sie wirken sich jedoch häufig auf die Benutzerfreundlichkeit aus, indem beibehaltene Elemente aus dem benutzerdefinierten täglichen Workflow entfernt werden. Für IT-Experten erfordert dieser Unveränderlichkeitsansatz die Bereitstellung und fortlaufende Wartung einer separaten Server- und Speicherinfrastruktur. Die Ermittlung erfolgt mit Tools außerhalb des E-Mail-Systems und umfasst die zugehörigen Bereitstellungs- und Wartungskosten.

Durch die Features der In-Place-Aufbewahrungs- und Aufbewahrungsrichtlinie für die Archivierung in Microsoft 365 und seinen Diensten können Sie viele Klassen eingehender, interner und ausgehender Daten beibehalten und beibehalten. Dies umfasst Folgendes:

- Ein- und ausgehende E-Mail-Kommunikation
- Bücher und Datensätze, die in E-Mail-Form oder in freigegebenen Online-Dokumenten enthalten sind
- Besprechungsanfragen
- Faxe
- Chatnachrichten
- Während Onlinebesprechungen freigegebene Dokumente
- Voicemails

Darüber hinaus hat Microsoft Add-On-Features entwickelt, um die Archivierung von Daten aus anderen Quellen durch die Integration in Drittanbieterlösungen zur Datenerfassung und -verwaltung zu ermöglichen. [](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) Nachdem Drittanbieterdaten importiert wurden, können Sie Microsoft 365-Compliancefeatures auf die Daten anwenden, einschließlich:

- [Aufbewahrung für eventuelle Rechtsstreitigkeiten](/microsoft-365/compliance/create-a-litigation-hold)
- [In-Situ-eDiscovery und -Speicher](/microsoft-365/compliance/manage-legal-investigations)
- [Compliance-Suche](/microsoft-365/compliance/search-for-content)
- [In-Situ-Archivierung](/microsoft-365/compliance/enable-archive-mailboxes)
- [Postfachüberwachung](/microsoft-365/compliance/enable-mailbox-auditing)
- [Aufbewahrungsrichtlinien](/microsoft-365/compliance/retention-policies)

Wenn für ein Postfach z. B. das Rechtsverfahren aktiviert ist, werden Drittanbieterdaten beibehalten. Sie können Drittanbieterdaten mithilfe In-Place eDiscovery- oder Compliancesuche durchsuchen. Oder Sie können Archivierungs- und Aufbewahrungsrichtlinien auf Drittanbieterdaten anwenden, genau wie bei Microsoft-Daten. Die Archivierung von Drittanbieterdaten in Microsoft 365 hilft Ihrer Organisation, die Behördlichen und behördlichen Richtlinien zu erfüllen.

Die Archivierung in Microsoft 365 bietet Eine Securities and Exchange Commission (SEC) Regel 17a-4-kompatiblen Speicher. Microsoft 365 bewahrt permanente Dateien aller Daten auf, die in einem nicht beschreibbaren, nicht auslöschbaren Format erfasst wurden, und verwendet aufbewahrungsrichtlinien und Aufbewahrungsrichtlinien, einschließlich Erhaltungssperre.

Insbesondere gilt:

- Alle Datensätze, die mithilfe der oben genannten Aufbewahrungsrichtlinien gespeichert werden, werden in einem dedizierten Speicherbereich aufbewahrt, der nicht dem normalen Benutzer zur Verfügung stehen soll. Nur autorisierte Benutzer können auf diese Datensätze zugreifen und diese durchsuchen, sie jedoch nicht ändern oder löschen.
- Metadaten für jedes Element enthalten einen Zeitstempel, der bei der Berechnung der Aufbewahrungsdauer verwendet wird. Zeitstempel werden angewendet, wenn ein neues Element empfangen oder erstellt wird und nicht geändert oder aus den Metadaten entfernt werden kann.
- Mit der Archivierung in Microsoft 365 können Benutzer unterschiedliche Aufbewahrungsrichtlinien und Aufbewahrungsaktionen kombinieren, um präzise Aufbewahrungsrichtlinien zu erstellen. Diese Richtlinien definieren den Typ oder Speicherort der aufbewahrten Elemente und die Dauer der Aufbewahrung.
- Mit dem Feature "Erhaltungssperre" können Benutzer auswählen, ob die Richtlinie zu einer restriktiven Richtlinie werden soll. Eine restriktive Richtlinie verhindert, dass jeder benutzer die Möglichkeit hat, die Aufbewahrungsrichtlinie zu entfernen, zu deaktivieren oder Änderungen vorzunehmen. Dies bedeutet, dass die Erhaltungssperre nach der Aktivierung nicht deaktiviert werden kann und kein Mechanismus vorhanden ist, mit dem daten von vorhandenen Verwahrern, die von den vorhandenen Aufbewahrungsrichtlinien erfasst wurden, während des Aufbewahrungszeitraums überschrieben, geändert, gelöscht oder gelöscht werden können. Darüber hinaus kann der durch die Erhaltungssperre festgelegte Aufbewahrungszeitraum nicht verkürzt oder verringert werden. Es kann jedoch verlängert werden, wenn die Aufbewahrung der gespeicherten Daten, wie oben erwähnt, gesetzlich vorgeschrieben ist. Die Erhaltungssperre stellt sicher, dass niemand, nicht einmal Administratoren oder Personen mit bestimmtem Kontrollzugriff, die Einstellungen ändern oder gespeicherte Daten überschreiben oder löschen kann. Dadurch wird die Archivierung in Microsoft 365 in Einklang mit den Anleitungen in version 2003 der SEC Rule 17a-4 gesetzt.

Informationen dazu, wie Ihnen Microsoft 365 bei der Erfüllung gesetzlicher Verpflichtungen hilft, [](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf) insbesondere in Bezug auf Die Anforderungen der Regel 17a-4, finden Sie im Whitepaper zu Exchange Online-Archivierung, SharePoint Online, OneDrive for Business und Skype for Business. Das Whitepaper enthält außerdem eine ausführliche Analyse der Microsoft 365-Archivierungsfunktionen und -funktionen für jede der Anforderungen gemäß DER SEC-Regel 17a-4 und veranschaulicht regulierten Kunden, wie sie mit der Microsoft 365-Archivierung diese Anforderungen erfüllen können.
