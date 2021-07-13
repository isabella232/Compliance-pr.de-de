---
title: Governance (Übersicht)
description: Erfahren Sie mehr über Compliance-Governance in Microsoft-Onlinediensten.
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
hideEdit: true
ms.openlocfilehash: bf17ec68648efbc5f149bad0671a4e035d27a307
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377472"
---
# <a name="governance-overview"></a>Governance (Übersicht)

## <a name="how-does-microsoft-provide-effective-security-governance-across-the-enterprise"></a>Wie bietet Microsoft eine effektive Sicherheitsgovernance im gesamten Unternehmen?

Microsoft ist sich bewusst, dass effektive Sicherheitsrichtlinien unternehmensweit konsistent implementiert werden müssen, um Microsoft-Informationssysteme und -Kunden zu schützen. Sicherheitsrichtlinien müssen außerdem Abweichungen bei Geschäftsfunktionen und Informationssystemen für eine universelle Anwendbarkeit berücksichtigen. Um diese Anforderungen zu erfüllen, implementiert Microsoft ein umfassendes Security Governance-Programm als Teil des Microsoft Policy Framework. Die Sicherheitsgovernance fällt unter die Microsoft-Sicherheitsrichtlinie (Microsoft Security Policy, MSP).

Der MSP organisiert die Sicherheitsrichtlinien, Standards und Anforderungen von Microsoft, sodass sie in allen Microsoft-Engineering-Gruppen und -Geschäftsbereichen implementiert werden können. Einzelne Unternehmenseinheiten sind für spezifische Implementierungen von Microsoft-Sicherheitsrichtlinien verantwortlich. Beispielsweise dokumentiert Microsoft 365 seine Sicherheitsimplementierungen in der Microsoft 365 Information Security Policy und im zugehörigen Microsoft 365 Control Framework. Azure und Dynamics 365 dokumentieren ihre Sicherheitsimplementierungen in den Standardvorgehensweisen (SOPs) und im Azure Control Framework. Diese Sicherheitsimplementierungen entsprechen den Zielen und Zielen des MSP.

Das Sicherheitsgovernance-Programm von Microsoft wird von verschiedenen regulatorischen und Compliance-Frameworks informiert und entspricht diesem. Sicherheitsanforderungen werden ständig weiterentwickelt, um neue Technologien, behördliche und Complianceanforderungen sowie Sicherheitsbedrohungen zu berücksichtigen. Aufgrund dieser Änderungen aktualisiert Microsoft regelmäßig unsere Sicherheitsrichtlinien und unterstützenden Dokumente, um Microsoft-Systeme und -Kunden zu schützen, unsere Verpflichtungen zu erfüllen und das Kundenvertrauen aufrechtzuerhalten.

## <a name="how-do-microsoft-online-services-implement-the-microsoft-security-policy-msp"></a>Wie implementieren Microsoft-Onlinedienste die Microsoft-Sicherheitsrichtlinie (MSP)?

Microsoft 365 dokumentiert Sicherheitsimplementierungen in den Microsoft 365-Richtlinien zur Informationssicherheit. Diese Richtlinie richtet sich nach der Microsoft-Sicherheitsrichtlinie und steuert das Microsoft 365-Informationssystem, einschließlich aller Microsoft 365-Umgebungen und aller Ressourcen, die mit der Sammlung, Verarbeitung, Wartung, Nutzung, Freigabe, Verbreitung und Entsorgung von Daten verbunden sind. Ebenso verwenden Azure und Dynamics 365 die Microsoft-Sicherheitsrichtlinie, um ihr Informationssystem zu steuern.

Die Informationssysteme umfassen die folgenden Komponenten, die durch die Microsoft 365 Information Security Policy (für Microsoft 365) und die Microsoft-Sicherheitsrichtlinie (für Azure und Dynamics 365) geregelt sind:

- Infrastruktur: Die physischen und Hardwarekomponenten von Azure, Dynamics 365 und Microsoft 365 Systemen (Einrichtungen, Geräte und Netzwerke)
- Software: Die Programme und Die Betriebssoftware von Azure, Dynamics 365 und Microsoft 365 Systemen (Systeme, Anwendungen und Dienstprogramme)
- Personen: Das Personal, das an dem Betrieb und der Verwendung von Azure-, Dynamics 365- und Microsoft 365-Systemen beteiligt ist (Entwickler, Operatoren, Benutzer und Vorgesetzte)
- Verfahren: Die programmierten und manuellen Verfahren für den Betrieb von Azure-, Dynamics 365- und Microsoft 365-Systemen
- Daten: Die von Azure, Dynamics 365 und Microsoft 365 Systemen generierten, gesammelten und verarbeiteten Informationen (Transaktionsdatenströme, Dateien, Datenbanken und Tabellen)

Die Microsoft 365-Richtlinien zur Informationssicherheit werden durch das Microsoft 365 Control Framework ergänzt. Im Microsoft 365 Control Framework werden die Mindestsicherheitsanforderungen für alle Microsoft 365 Dienste und Komponenten des Informationssystems beschrieben. Es verweist auch auf die rechtlichen und geschäftlichen Anforderungen hinter jedem Steuerelement. Das Framework umfasst Kontrollaktivitätsnamen, Beschreibungen und Anleitungen zur Sicherstellung effektiver Kontrollimplementierungen durch Serviceteams. Microsoft 365 verwendet das Steuerungsframework, um Kontrollimplementierungen für interne und externe Berichte nachzuverfolgen. Auf ähnliche Weise werden Azure und Dynamics 365-Datensatzsteuerungsimplementierungen im Azure Control Framework implementiert.

## <a name="how-do-online-services-limit-and-track-exceptions-to-established-policies-and-procedures"></a>Wie beschränken und verfolgen Onlinedienste Ausnahmen von etablierten Richtlinien und Verfahren?

Alle Ausnahmen von den Control Frameworks müssen eine berechtigte geschäftliche Begründung haben und von einer entsprechenden Governance-Entität innerhalb jedes Onlinedienstteams genehmigt werden. Abhängig vom Umfang der Ausnahme und des potenziellen Risikos, das sie darstellt, muss die Genehmigung für Ausnahmen möglicherweise bei der Unternehmensleitung eingeholt werden. Ausnahmen werden in einem Nachverfolgungstool verwaltet, in dem sie überprüft und für die weitere Relevanz genehmigt werden.

## <a name="how-do-online-services-keep-security-and-compliance-requirements-updated"></a>Wie halten Onlinedienste die Sicherheits- und Complianceanforderungen auf dem neuesten Stand?

Governance-, Risiko- und Compliance-Teams jedes Onlinediensts (GRC) arbeiten kontinuierlich an der Aufrechterhaltung des Kontrollframeworks. In mehreren Szenarien muss das GRC-Team möglicherweise das Kontrollframework aktualisieren, einschließlich Änderungen relevanter Vorschriften oder Gesetze, neue Bedrohungen, Penetrationstestergebnisse, Sicherheitsvorfälle, Audit-Feedback und neue Compliance-Anforderungen. Wenn eine Frameworkänderung erforderlich ist, identifiziert das Vertrauensteam die wichtigsten Beteiligten, die für die Genehmigung und Implementierung der Änderung verantwortlich sind, um sicherzustellen, dass sie machbar ist und keine unbeabsichtigten Probleme mit Onlinediensten verursacht. Sobald sich das GRC-Team und die relevanten Projektbeteiligten darauf einigen, was die Änderung erfordert, legen die für die Implementierung der Änderung verantwortlichen Workloads das Zieldatum für den Abschluss fest und arbeiten daran, die Änderung innerhalb ihrer jeweiligen Dienste zu implementieren. Nachdem die Implementierungsziele erreicht wurden, aktualisiert das Vertrauensteam das Steuerelementframework mit den neuen oder aktualisierten Steuerelementen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit Governance.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1: Einhaltung gesetzlicher und vertraglicher Anforderungen <br> A.18.2: Überprüfungen der Informationssicherheit | 2. Dezember 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1: Einhaltung gesetzlicher und vertraglicher Anforderungen <br> A.18.2: Überprüfungen der Informationssicherheit | 2. Dezember 2020 |
| [SOC 1](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fservicetrust.microsoft.com%2FViewPage%2FMSComplianceGuideV3%3Fcommand%3DDownload%26downloadType%3DDocument%26downloadId%3D66043614-5628-4e26-83be-057eb3bb026c%26tab%3D7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb%26docTab%3D7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%252F_SSAE_16_Reports&data=04%7C01%7Csostah%40microsoft.com%7Cb9591cf4bd214d42c4f408d93cd83520%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637607721602686385%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=B2xjy%2Bx70e8vI%2FKC2BCa4AyJt0OSMzAGuhwllHF4NGM%3D&reserved=0) | IS-1: Microsoft-Sicherheitsrichtlinie <br> IS-2: Microsoft-Sicherheitsrichtlinienüberprüfung <br> IS-3: Sicherheitsrollen und -zuständigkeiten | 31. März 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | C5-1: Standardvorgehensweisen <br> IS-1: Microsoft-Sicherheitsrichtlinie <br> IS-2: Microsoft-Sicherheitsrichtlinienüberprüfung <br> IS-3: Sicherheitsrollen und -zuständigkeiten <br> SOC2-14: Vertraulichkeits- und Geheimhaltungsverträge <br> SOC2-18: Gesetzliche, behördliche und vertragliche Anforderungen <br> SOC2-19: Funktionsübergreifendes Complianceprogramm <br> SOC2-20: ISMS-Programm | 31. März 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | Ca-2: Sicherheitsbewertungen <br> PL-2: Systemsicherheitsplan | 24. September 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1: Einhaltung gesetzlicher und vertraglicher Anforderungen <br> A.18.2: Überprüfungen der Informationssicherheit | 20. April 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-11: Richtlinienframeworkupdates <br> CA-17: Microsoft-Sicherheitsrichtlinie <br> CA-25: Control Framework-Updates | 24. Dezember 2020 |

## <a name="resources"></a>Ressourcen

- [Microsoft-Sicherheitsrichtlinie](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=bc35aefb-ec41-4a0e-bfc7-10aa5169ca88&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Microsoft-Sicherheitsprogrammrichtlinie](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=4b010ac5-2861-4d20-b8ff-db77875b43a9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)