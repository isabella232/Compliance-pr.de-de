---
title: Verwaltung von Sicherheitsvorfällen (Übersicht)
description: Informationen zum Vorfallmanagement in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 203adce9b4c7167315abbbfbebce0efdd604fefe
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159013"
---
# <a name="incident-management-overview"></a>Verwaltung von Sicherheitsvorfällen (Übersicht)

## <a name="what-is-a-security-incident"></a>Was ist ein Sicherheitsvorfall?

Microsoft definiert einen Sicherheitsvorfall in seinen Onlinediensten als eine bestätigte Sicherheitsverletzung, die zur versehentlichen oder unrechtmäßigen Zerstörung, zum Verlust, zur Änderung, zur unberechtigten Offenlegung von oder zum unberechtigten Zugriff auf Kundendaten oder personenbezogene Daten während der Verarbeitung durch Microsoft führt. Beispielsweise würden nicht autorisierter Zugriff auf die Microsoft-Onlinedienstinfrastruktur und die Exfiltration von Kundendaten einen Sicherheitsvorfall darstellen, während Complianceereignisse, die sich nicht auf die Vertraulichkeit, Integrität oder Verfügbarkeit von Diensten oder Kundendaten auswirken, nicht als Sicherheitsvorfälle betrachtet werden.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Wie reagiert Microsoft auf Sicherheitsvorfälle?

Wenn es einen Sicherheitsvorfall gibt, ist Microsoft bestrebt, schnell und effektiv zu reagieren, um Microsoft-Dienste und Kundendaten zu schützen. Microsoft verwendet eine Strategie zur Reaktion auf Vorfälle, um Sicherheitsbedrohungen schnell und effizient zu untersuchen, einzudämmen und zu entfernen.

Microsoft-Clouddienste werden kontinuierlich auf Anzeichen von Kompromittierung überwacht. Zusätzlich zur automatisierten Sicherheitsüberwachung und -warnung erhalten alle Mitarbeiter jährliche Schulungen, um Anzeichen potenzieller Sicherheitsvorfälle zu erkennen und zu melden. Verdächtige Aktivitäten, die von Mitarbeitern, Kunden oder Sicherheitsüberwachungstools erkannt werden, werden zur Untersuchung an dienstspezifische Sicherheitsteams eskaliert. Alle Service-Operations-Teams, einschließlich dienstspezifischer Sicherheitsteams, führen eine umfassende Bereitschaftsdienstrotation durch, um sicherzustellen, dass Ressourcen für die Reaktion auf Vorfälle 24 x 7 x 365 zur Verfügung stehen. Unsere Bereitschaftsdienstrotationen ermöglichen Es Microsoft, jederzeit oder in großem Umfang eine effektive Reaktion auf Vorfälle zu ermöglichen, einschließlich weit verbreiteter oder gleichzeitiger Ereignisse.

Wenn verdächtige Aktivitäten erkannt und eskaliert werden, initiieren dienstspezifische Sicherheitsteams einen Prozess der **Analyse, Eindämmung, Beseitigung und Wiederherstellung.** Diese Teams koordinieren die Analyse des potenziellen Vorfalls, um seinen Umfang zu ermitteln, einschließlich der Auswirkungen auf Kunden oder Kundendaten. Basierend auf dieser Analyse arbeiten dienstspezifische Sicherheitsteams mit betroffenen Serviceteams an der Entwicklung eines Plans, um die Bedrohung einzudämmen und die Auswirkungen des Vorfalls zu minimieren, die Bedrohung aus der Umgebung zu beseitigen und vollständig in einen bekannten sicheren Zustand zurückzuverfolgen. Relevante Serviceteams implementieren den Plan mit Unterstützung von servicespezifischen Security Response-Teams, um sicherzustellen, dass die Bedrohung erfolgreich beseitigt wird und betroffene Dienste einer vollständigen Wiederherstellung unterzogen werden.

Nachdem ein Vorfall behoben wurde, implementieren Serviceteams alle aus dem Vorfall gewonnenen Erkenntnisse, um ähnliche Vorfälle in Zukunft besser zu verhindern, zu erkennen und darauf zu reagieren. Ausgewählte Sicherheitsvorfälle, insbesondere solche, die auswirkungen auf den Kunden haben oder zu einer Datenschutzverletzung führen, werden einer vollständigen Nachträglichkeit von Vorfällen unterzogen. Die nachträgliche Analyse dient zur Ermittlung von technischen Fehlern, Verfahrensfehlern, manuellen Fehlern und anderen Prozessmängeln, die möglicherweise zu dem Vorfall beigetragen haben oder während der Vorfallreaktion erkannt wurden. Verbesserungen, die während der nachträglichen Analyse identifiziert wurden, werden mithilfe der Koordination von servicespezifischen Sicherheitsreaktionsteams implementiert, um zukünftige Vorfälle zu verhindern und die Erkennungs- und Reaktionsfunktionen zu verbessern.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>Wie und wann werden Kunden über Sicherheits- oder Datenschutzvorfälle informiert?

Wenn Microsoft auf einen Sicherheitsverstoß im Zusammenhang mit unbefugtem Verlust, offenlegung oder Änderung von Kundendaten aufmerksam wird, benachrichtigt Microsoft betroffene Kunden innerhalb von 72 Stunden, wie im Datenschutznachtrag (Data Protection Addendum, DPA) der Online services Terms (OST) beschrieben. Die Verpflichtung zur Benachrichtigung auf der Zeitachse beginnt mit dem Eintreten der offiziellen Deklaration des Sicherheitsvorfalls. Wenn ein Sicherheitsvorfall gemeldet wird, erfolgt die Benachrichtigung so schnell wie möglich und ohne unangemessene Verzögerung.

Benachrichtigungen enthalten eine Beschreibung der Art der Verletzung, ungefähre Auswirkungen auf die Benutzer und Maßnahmen zur Risikominderung (sofern zutreffend). Wenn die Untersuchung von Microsoft zum Zeitpunkt der ersten Benachrichtigung nicht abgeschlossen ist, gibt die Benachrichtigung auch die nächsten Schritte und Zeitpläne für die nachfolgende Kommunikation an.

Wenn ein Kunde auf einen Vorfall aufmerksam wird, der sich auf Microsoft auswirken könnte, einschließlich, aber nicht beschränkt auf eine Datenschutzverletzung, ist der Kunde dafür verantwortlich, Microsoft umgehend über den Vorfall gemäß der Definition in der Datenschutzbehörde zu informieren.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Vorfallverwaltung.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Verwaltung von Vorfällen und Verbesserungen der Informationssicherheit | 2. Dezember 2021 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Verwaltung von Vorfällen und Verbesserungen der Informationssicherheit | 2. Dezember 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Benachrichtigung über eine Datenschutzverletzung im Zusammenhang mit personenbezogenen Informationen  | 2. Dezember 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | Chat-1: Vorfallverwaltungsframework <br> CHAT-2: Erkennungsmechanismen und Warnungen <br> Chat-3: Ausführung der Reaktion auf Vorfälle <br> CHAT-4: Post-Mortems für Vorfälle <br> Chat-6: Vorfallreaktionstests <br> OA-7: Zugriff durch Bereitschaftstechniker | 31. März 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CCM-9: Forensische Verfahren <br> CUEC: Melden von Vorfällen <br> Chat-1: Vorfallverwaltungsframework <br> CHAT-2: Erkennungsmechanismen und Warnungen <br> Chat-3: Ausführung der Reaktion auf Vorfälle <br> CHAT-4: Post-Mortems für Vorfälle <br> Chat-6: Vorfallreaktionstests <br> OA-7: Zugriff durch Bereitschaftstechniker <br> SOC2-6: Kundensupport-Website <br> SOC2-9: Dienstdashboards | 31. März 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | IR-4: Behandlung von Sicherheitsvorfällen <br> IR-6: Vorfallberichterstattung <br> IR-8: Plan zur Reaktion auf Vorfälle | 24. September 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Verwaltung von Vorfällen und Verbesserungen der Informationssicherheit | 20. April 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Benachrichtigung über eine Datenschutzverletzung im Zusammenhang mit personenbezogenen Informationen  | 20. April 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26: Berichterstellung über Sicherheitsvorfälle <br> CA-47: Reaktion auf Vorfälle | 24. Dezember 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12: Vereinbarungen zum Servicelevel (SERVICE Level Agreements, SLAs) <br> CA-13: Handbücher zur Behandlung von Sicherheitsvorfällen <br> CA-15: Dienststatusbenachrichtigungen  <br>  <br> CA-26: Berichterstellung über Sicherheitsvorfälle <br> CA-29: Bereitschaftstechniker <br> CA-47: Reaktion auf Vorfälle | 24. Dezember 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Melden von Vorfällen  | 24. Dezember 2020  |

## <a name="resources"></a>Ressourcen

- [Onlinedienstbedingungen (Online Services Terms, OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [Datenschutz-Nachtrag](https://www.microsoft.com/licensing/product-licensing/products)
- [Implementierungsleitfaden für Microsoft Cloud Incident Management für Azure und Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 – Bewertung der Sicherheitsrisiken von Drittanbietern für Office 365 – 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
