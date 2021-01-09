---
title: Verwaltung von Sicherheitsvorfällen (Übersicht)
description: Erfahren Sie mehr über das Vorfallmanagement in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 24ecad99115705f293f765edb84345dad8ff8c93
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787314"
---
# <a name="incident-management-overview"></a>Verwaltung von Sicherheitsvorfällen (Übersicht)

## <a name="what-is-a-security-incident"></a>Was ist ein Sicherheitsvorfall?

Microsoft definiert einen Sicherheitsvorfall in seinen Onlinediensten als eine bestätigte Sicherheitsverletzung, die zur versehentlichen oder unrechtmäßigen Zerstörung, zum Verlust, zur Änderung, zur unberechtigten Offenlegung von oder zum unberechtigten Zugriff auf Kundendaten oder personenbezogene Daten während der Verarbeitung durch Microsoft führt. Beispielsweise würden ein nicht autorisierter Zugriff auf die Microsoft 365-Infrastruktur und die Exfiltration von Kundendaten einen Sicherheitsvorfall darstellen, während Complianceereignisse, die sich nicht auf die Vertraulichkeit, Integrität oder Verfügbarkeit von Diensten oder Kundendaten auswirken, nicht als Sicherheitsvorfälle betrachtet werden.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Wie reagiert Microsoft auf Sicherheitsvorfälle?

Bei jedem Sicherheitsvorfall ist Microsoft bestrebt, schnell und effektiv zu reagieren, um die Dienste und Kundendaten von Microsoft zu schützen. Microsoft setzt eine Strategie zur Reaktion auf Sicherheitsvorfälle ein, die darauf ausgelegt ist, Sicherheitsbedrohungen schnell und effizient zu untersuchen, eindämmung und zu entfernen.

Microsoft Cloud Services werden kontinuierlich auf Anzeichen von Kompromissen überwacht. Zusätzlich zur automatisierten Sicherheitsüberwachung und -warnung erhalten alle Mitarbeiter jährliche Schulungen, um Anzeichen potenzieller Sicherheitsvorfälle zu erkennen und zu melden. Verdächtige Aktivitäten, die von Mitarbeitern, Kunden oder Sicherheitsüberwachungstools erkannt werden, werden zur Untersuchung an servicespezifische Sicherheitsreaktionsteams eskaliert. Alle Servicebetriebsteams, einschließlich servicespezifischer Sicherheitsreaktionsteams, behalten eine tiefgehende On-Call-Rotation bei, um sicherzustellen, dass Ressourcen für die Reaktion auf Vorfälle rund um die Uhr verfügbar sind. Unsere On-Call-Drehungen ermöglichen Es Microsoft, eine effektive Reaktion auf Vorfälle zu jedem Beliebigen Zeitpunkt oder Umfang, einschließlich weit verbreiteter oder gleichzeitiger Ereignisse, zu ermöglichen.

Wenn verdächtige Aktivitäten erkannt und eskaliert werden, initiieren dienstspezifische Sicherheitsreaktionsteams einen Analyse-, Eindämmungs-, Beseitigungs- **und Wiederherstellungsprozess.** Diese Teams koordinieren die Analyse des potenziellen Vorfalls, um seinen Umfang zu bestimmen, einschließlich aller Auswirkungen auf Kunden oder Kundendaten. Basierend auf dieser Analyse arbeiten dienstspezifische Sicherheitsreaktionsteams mit den betroffenen Serviceteams zusammen, um einen Plan zu entwickeln, der die Bedrohung eindähmt und die Auswirkungen des Vorfalls minimiert, die Bedrohung aus der Umgebung entfernt und die vollständige Wiederherstellung in einen bekannten sicheren Zustand vor sich geht. Relevante Serviceteams implementieren den Plan mit Unterstützung von servicespezifischen Security Response-Teams, um sicherzustellen, dass die Bedrohung erfolgreich beseitigt und die betroffenen Dienste einer vollständigen Wiederherstellung unterzogen werden.

Nachdem ein Vorfall behoben wurde, implementieren Serviceteams alle aus dem Vorfall gewonnenen Erkenntnisse, um ähnliche Vorfälle in Zukunft besser zu verhindern, zu erkennen und darauf zu reagieren. Ausgewählte Sicherheitsvorfälle, insbesondere solche, die auswirkungen auf Kunden haben oder zu einer Datenschutzverletzung führen, werden einer vollständigen nachträglichen Analyse des Vorfalls unterzogen. Die nachträgliche Analyse dient zur Ermittlung von technischen Fehlern, Verfahrensfehlern, manuellen Fehlern und anderen Prozessmängeln, die möglicherweise zu dem Vorfall beigetragen haben oder während der Vorfallreaktion erkannt wurden. Während der nachträglichen Analyse identifizierte Verbesserungen werden mit der Koordination von servicespezifischen Sicherheitsreaktionsteams implementiert, um zukünftige Vorfälle zu verhindern und die Erkennungs- und Reaktionsfunktionen zu verbessern.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>Wie und wann werden Kunden über Sicherheits- oder Datenschutzvorfälle benachrichtigt?

Wenn Microsoft von einer Sicherheitsverletzung im Zusammenhang mit unbefugtem Verlust, Offenlegung oder Änderung von Kundendaten kenntnist, benachrichtigt Microsoft betroffene Kunden innerhalb von 72 Stunden, wie im Datenschutz-Add-In (DPA) der Onlinedienstbedingungen beschrieben. Die Verpflichtung zur Benachrichtigung auf der Zeitachse beginnt mit dem Eintreten der offiziellen Deklaration des Sicherheitsvorfalls. Wenn ein Sicherheitsvorfall gemeldet wird, erfolgt die Benachrichtigung so schnell wie möglich und ohne unangemessene Verzögerung.

Benachrichtigungen umfassen eine Beschreibung der Art der Verletzung, ungefähre Auswirkungen auf den Benutzer und Maßnahmen zur Risikominderung (falls zutreffend). Wenn die Untersuchung von Microsoft zum Zeitpunkt der ersten Benachrichtigung nicht abgeschlossen ist, enthält die Benachrichtigung auch die nächsten Schritte und Zeitpläne für die nachfolgende Kommunikation.

Wenn ein Kunde auf einen Vorfall aufmerksam wird, der Auswirkungen auf Microsoft haben könnte, einschließlich, aber nicht beschränkt auf eine Datenschutzverletzung, ist der Kunde dafür verantwortlich, Microsoft umgehend über den Vorfall gemäß der Definition in der Datenschutz-Datenschutzverletzung zu informieren.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Bestimmungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf Einhaltung externer Bestimmungen und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Vorfallverwaltung.

| **Externe Überwachungen** | **Section** | **Datum des letzten Berichts** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IR-4: Behandlung von Vorfällen <br> IR-6: Vorfallberichterstattung <br> IR-8: Plan zur Reaktion auf Vorfälle | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Verwaltung von Vorfällen und Verbesserungen der Informationssicherheit | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Verwaltung von Vorfällen und Verbesserungen der Informationssicherheit | Februar 22, 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Benachrichtigung über eine Datenschutzverletzung im Zusammenhang mit personenbezogenen Informationen  | Februar 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26: Melden von Sicherheitsvorfällen <br> CA-47: Reaktion auf Vorfälle | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12: Vereinbarungen zum Servicelevel (Service Level Agreements, SLAs) <br> CA-13: Handbücher zur Reaktion auf Vorfälle <br> CA-15: Benachrichtigungen zum Dienstzustand  <br>  <br> CA-26: Melden von Sicherheitsvorfällen <br> CA-29: On-Call-Techniker <br> CA-47: Reaktion auf Vorfälle | 24. Dezember 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Melden von Vorfällen  | 24. Dezember 2020  |

## <a name="resources"></a>Ressourcen

- [Onlinedienstbedingungen (Online Services Terms, OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [Datenschutzergänzung (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Implementierungsleitfavorfälle für microsoft Cloud Incident Management für Azure und Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 – Sicherheitsrisikobewertung von Drittanbietern von Office 365 – 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
