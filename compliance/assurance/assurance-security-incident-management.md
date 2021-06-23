---
title: Verwaltung von Sicherheitsvorfällen unter Microsoft 365
description: Dieser Artikel bietet eine Übersicht über den Prozess der Verwaltung von Sicherheitsvorfällen in Microsoft 365.
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
- MS-Compliance0
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 5f3123d4b4ef853357c0b98f1b6973cc8ba4d1e8
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088887"
---
# <a name="microsoft-365-security-incident-management"></a>Verwaltung von Sicherheitsvorfällen unter Microsoft 365

Microsoft arbeitet kontinuierlich daran, für Microsoft 365 Kunden äußerst sichere Dienste auf Unternehmensniveau bereitzustellen. In diesem Dokument wird beschrieben, wie Microsoft Sicherheitsvorfälle in Microsoft 365 behandelt. Ein Sicherheitsvorfall bezieht sich auf jeden unrechtmäßigen Zugriff auf Kundendaten, die auf Geräten von Microsoft oder in Einrichtungen von Microsoft gespeichert sind, oder auf unbefugten Zugriff auf solche Geräte oder Einrichtungen, die zu Verlust, Offenlegung oder Änderung von Kundendaten führen können. Die Ziele von Microsoft bei der Reaktion auf Sicherheitsvorfälle sind der Schutz von Kundendaten und der Microsoft 365-Dienste.

Das Microsoft 365 Security-Team und die verschiedenen Serviceteams arbeiten gemeinsam und verfolgen den gleichen Ansatz für Sicherheitsvorfälle:

- Vorbereitung
- Erkennung und Analyse
- Eindämmung
- Beseitigung
- Wiederherstellung
- Aktivitäten nach einem Vorfall

## <a name="microsoft-approach-to-security-incident-management"></a>Microsoft-Ansatz für die Verwaltung von Sicherheitsvorfällen

Der Ansatz von Microsoft zur Verwaltung eines Sicherheitsvorfalls entspricht dem [National Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61. Microsoft verfügt über mehrere dedizierte Teams, die zusammenarbeiten, um Sicherheitsvorfälle zu verhindern, zu überwachen, zu erkennen und darauf zu reagieren.

|**Team/Bereich**|**Beschreibung**|
|:------------|:--------------|
| Microsoft Security Response Center | Identifiziert, überwacht, löst und reagiert auf Sicherheitsvorfälle und Microsoft-Softwaresicherheitsrisiken. |
| Cyber Defense Operations Center | Das Cyber Defense Operations Center ist der physische Standort, der Sicherheitsteams und Experten aus dem gesamten Unternehmen zusammenführt, um Bedrohungen in Echtzeit zu schützen, zu erkennen und darauf zu reagieren. |
| Unternehmens-, Außen- und Rechtsbeziehungen | Bietet rechtliche und behördliche Hinweise für einen verdächtigen Sicherheitsvorfall. |
| Microsoft 365 Security Response Team | Arbeitet mit Microsoft 365 Serviceteams zusammen, um den geeigneten Prozess zur Verwaltung von Sicherheitsvorfällen zu erstellen und die Reaktion auf Sicherheitsvorfälle zu fördern. |
| Office 365 Vertrauen | Enthält Anleitungen zu gesetzlichen Anforderungen, Compliance und Datenschutz. |
| Microsoft 365 Datacenter Security Team | Team, das sich auf die verschiedenen Dienste konzentriert und sich auf allgemeine Sicherheits-Engineering-Investitionen konzentriert, um Risiken und Bedrohungen Microsoft 365 Dienstarchitektur zu schützen, zu erkennen und darauf zu reagieren. |
| Serviceteams | Entwicklungsteams für Microsoft 365 Dienste wie Exchange, SharePoint und Microsoft Teams, die für sicherheitsbezogene Richtlinien und Entscheidungen für jeden Dienst verantwortlich sind. |
| Microsoft Threat Intelligence Center (MSTIC) | Bietet den aktuellen Stand der Technik bei digitalen Sicherheitsbedrohungen für Microsoft-Infrastruktur und -Ressourcen, hilft Partnerteams innerhalb von Microsoft bei der Priorisierung von Maßnahmenplänen zur Risikominderung und -verhinderung und erhöht den Schutz durch nahezu Echtzeit-Vorfallüberwachung/-erkennung. |
| Partnersicherheitsteams | Andere Partnersicherheitsteams innerhalb von Microsoft, die wichtige Dienste bereitstellen oder für wichtige Abhängigkeiten in Microsoft 365 verantwortlich sind, z. B. das Azure Security Response-Team, Identity Security Response und Microsoft Corporate Security Response-Teams. |
| Microsoft 365 Kundenerfahrungskommunikation | Das Entwicklungsteam ist für die gesamte Kundenkommunikation zu Sicherheits- und Dienstvorfällen verantwortlich. |

## <a name="response-management-process"></a>Reaktionsverwaltungsprozess

Das Microsoft 365 Security-Team und die Serviceteams arbeiten zusammen und verfolgen den gleichen Ansatz für Sicherheitsvorfälle, der auf den NIST 800-61-Reaktionsverwaltungsphasen basiert:

- **Vorbereitung:** Bezieht sich auf die organisatorische Vorbereitung, die erforderlich ist, um reagieren zu können, einschließlich Tools, Prozessen, Kompetenzen und Bereitschaft.
- **Erkennung & Analyse:** Bezieht sich auf die Aktivität, um einen Sicherheitsvorfall in einer Produktionsumgebung zu erkennen und alle Ereignisse zu analysieren, um die Echtheit des Sicherheitsvorfalls zu bestätigen.
- **Eindämmung, Beseitigung, Wiederherstellung:** Bezieht sich auf die erforderlichen und geeigneten Maßnahmen, um den Sicherheitsvorfall basierend auf der in der vorherigen Phase durchgeführten Analyse einzudämmen. In dieser Phase kann auch eine weitere Analyse erforderlich sein, um die vollständige Wiederherstellung nach dem Sicherheitsvorfall zu gewährleisten.
- **Aktivität nach dem Vorfall:** Bezieht sich auf die nachträgliche Analyse, die nach der Wiederherstellung eines Sicherheitsvorfalls durchgeführt wurde. Die während des Prozesses durchgeführten operativen Aktionen werden überprüft, um festzustellen, ob Änderungen in den Vorbereitungs- oder Erkennungs- und Analysephasen vorgenommen werden müssen.

![Phasen der Verwaltung von Sicherheitsvorfällen](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>Antwortmodell für Verbundsicherheit

Microsoft 365 Dienste umfassen wichtige Microsoft-Onlinedienste (Exchange, SharePoint und Microsoft Teams usw.) und andere Microsoft-Clouddienste wie Azure Active Directory, die Microsoft Commerce-Plattform und MSTIC. Diese Dienste werden von separaten Teams mit eigenen Sicherheitsprozessen betrieben. Andere Teams bei Microsoft befassen sich auch mit verschiedenen Sicherheitsaspekten von Microsoft 365. Aufgrund der Vielzahl von Teams, die an der Verwaltung des Sicherheitsbetriebs in allen verschiedenen Diensten arbeiten, aus denen Microsoft 365 besteht, hat Microsoft ein Verbundsicherheitsreaktionsmodell implementiert.

Diese Tabelle enthält die Betriebsgrenzen zwischen den verschiedenen Sicherheitsteams für Microsoft 365 und den Microsoft 365 Serviceteams:

|**Aktivität**|**Microsoft 365 Sicherheitsteamvorgänge**|**Microsoft 365 Serviceteamvorgänge**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Erkennung und Analyse | – Erkennungsanforderungen <br> – Sicherheitsüberwachung und -analyse <br> – Indikator für Kompromittierungen (Indicator of compromise, IOC) <br> – Suche nach Sicherheitsverletzungen <br> - 24 x 7 Lead für Sicherheit bei Anrufen und Reaktion auf Vorfälle | – Erkennungsanforderungen <br> – Überwachen der Infrastrukturbereitstellung <br> – Dienstanalyse und Einblicke <br> – Ereignis- und Warnungstriage <br> - 24 x 7 Service Engineering on-Call  |
| Eindämmung, Beseitigung, Wiederherstellung | – Lead für die Reaktion auf Vorfälle <br> – Forensische Untersuchung <br> – Sicherheitskenntnisse und Beratung <br> - Anleitung zur Wiederherstellung | – Besitzer von Sicherheitsvorfällen <br> – Einblick und Expertise des Diensts <br> – Ausführung von Eindämmung, Beseitigung und Wiederherstellung |
| Aktivitäten nach dem Vorfall | – Lead für die Analyse nach dem Vorfall <br> – Datensammlung und Archivierung <br> – Erkenntnisse und Fehleranforderungen <br> – Vorfallberichterstattung | – Dienstseitige Vorfallanalyse <br> – Priorisieren von Nachverfolgungsaktivitäten <br> – Implementierung von Sicherheitsinvestitionen <br> – Bereitschaft zur Dienstsicherheit |

## <a name="related-articles"></a>Verwandte Artikel

- [Vorbereitung des Microsoft 365 Sicherheitsvorfallmanagements](assurance-sim-preparation.md)
- [Microsoft 365 Erkennung und Analyse von Sicherheitsvorfällen](assurance-sim-detection-analysis.md)
- [Microsoft 365 Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 Aktivitäten zur Verwaltung von Sicherheitsvorfällen nach einem Vorfall](assurance-sim-post-incident-activity.md)
