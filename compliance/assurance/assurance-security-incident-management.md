---
title: Microsoft-Sicherheitsvorfallverwaltung
description: Dieser Artikel bietet eine Übersicht über den Prozess zur Verwaltung von Sicherheitsvorfällen in Microsoft-Onlinediensten.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: cb9d27f02ec53c98e2f00d3106f8e4be8798d78f
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947138"
---
# <a name="microsoft-security-incident-management"></a>Microsoft-Sicherheitsvorfallverwaltung

Microsoft arbeitet kontinuierlich an der Bereitstellung streng sicherer Dienste auf Unternehmensniveau für Microsoft-Kunden. Sicherheitsvorfälle sind jedoch eine zwangsläufige Realität, die sorgfältig und schnell verwaltet werden muss. Dieses Dokument bietet eine Übersicht darüber, wie Microsoft Sicherheitsvorfälle mithilfe bewährter Methoden und Technologien behandelt, um ihre potenziellen Auswirkungen zu minimieren. Ein Sicherheitsvorfall bezieht sich auf jeden unrechtmäßigen Zugriff auf Kundendaten, die auf Geräten von Microsoft oder in Einrichtungen von Microsoft gespeichert sind, oder auf unbefugten Zugriff auf solche Geräte oder Einrichtungen, die zu Verlust, Offenlegung oder Änderung von Kundendaten führen können. Die Ziele von Microsoft bei der Reaktion auf Sicherheitsvorfälle sind der Schutz von Kundendaten und Microsoft-Onlinediensten.

Microsoft Online Services-Sicherheitsteams und die verschiedenen Serviceteams arbeiten gemeinsam und verfolgen den gleichen Ansatz für Sicherheitsvorfälle:

- Vorbereitung
- Erkennung und Analyse
- Eindämmung, Beseitigung und Wiederherstellung
- Aktivitäten nach einem Vorfall

## <a name="microsoft-approach-to-security-incident-management"></a>Microsoft-Ansatz für die Verwaltung von Sicherheitsvorfällen

Der Ansatz von Microsoft zur Verwaltung eines Sicherheitsvorfalls entspricht dem [National Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61. Microsoft verfügt über mehrere dedizierte Teams, die zusammenarbeiten, um Sicherheitsvorfälle zu verhindern, zu überwachen, zu erkennen und darauf zu reagieren.

|**Team/Bereich**|**Beschreibung**|
|:------------|:--------------|
| Microsoft Security Response Center | Identifiziert, überwacht, löst und reagiert auf Sicherheitsvorfälle und Microsoft-Softwaresicherheitsrisiken. |
| Cyber Defense Operations Center | Das Cyber Defense Operations Center ist der physische Standort, der Sicherheitsteams und Experten aus dem gesamten Unternehmen zusammenführt, um Bedrohungen in Echtzeit zu schützen, zu erkennen und darauf zu reagieren. |
| Unternehmens-, Externe und Rechtsbeziehungen | Bietet rechtliche und behördliche Hinweise für einen verdächtigen Sicherheitsvorfall. |
| Microsoft Datacenter Security Team | Team, das sich auf die verschiedenen Dienste konzentriert und sich auf allgemeine Sicherheits-Engineering-Investitionen konzentriert, um Risiken und Bedrohungen der Dienstarchitektur zu schützen, zu erkennen und darauf zu reagieren. |
| Microsoft Security Response Teams | Unabhängige Azure, Dynamics 365 und Microsoft 365 Sicherheitsteams, die mit Serviceteams zusammenarbeiten, um den geeigneten Prozess zum Verwalten von Sicherheitsvorfällen zu erstellen und die Reaktion auf Sicherheitsvorfälle zu fördern. |
| Microsoft Governance-, Risiko- und Compliance-Teams (GRC) | Bereitstellen von Anleitungen zu gesetzlichen Anforderungen, Compliance und Datenschutz. |
| Serviceteams | Entwicklungsteams für Azure, Dynamics 365 Microsoft 365, die für sicherheitsbezogene Richtlinien und Entscheidungen für jeden Dienst verantwortlich sind. |
| Azure-Betriebsmanager | Überwacht die Untersuchung und Lösung von Azure-bezogenen Sicherheits- und Datenschutzvorfällen. |
| Microsoft Threat Intelligence Center (MSTIC) | Bietet den aktuellen Stand der Technik bei digitalen Sicherheitsbedrohungen für Microsoft-Infrastruktur und -Ressourcen, hilft Partnerteams innerhalb von Microsoft bei der Priorisierung von Maßnahmenplänen zur Risikominderung und -verhinderung und erhöht den Schutz durch nahezu Echtzeit-Vorfallüberwachung/-erkennung. |
| Teams für die Kundenerfahrungskommunikation | Entwicklungsteams, die für die gesamte Kundenkommunikation zu Sicherheits- und Dienstvorfällen verantwortlich sind. Separate Teams sind Azure, Dynamics 365 und Microsoft 365 zugeordnet. |

## <a name="response-management-process"></a>Reaktionsverwaltungsprozess

Sicherheitsteams und Serviceteams von Microsoft Online Services arbeiten zusammen und verfolgen den gleichen Ansatz für Sicherheitsvorfälle, der auf den NIST 800-61-Reaktionsverwaltungsphasen basiert:

- **Vorbereitung:** Bezieht sich auf die organisatorische Vorbereitung, die erforderlich ist, um reagieren zu können, einschließlich Tools, Prozessen, Kompetenzen und Bereitschaft.
- **Erkennung & Analyse:** Bezieht sich auf die Aktivität, um einen Sicherheitsvorfall in einer Produktionsumgebung zu erkennen und alle Ereignisse zu analysieren, um die Echtheit des Sicherheitsvorfalls zu bestätigen.
- **Eindämmung, Beseitigung, Wiederherstellung:** Bezieht sich auf die erforderlichen und geeigneten Maßnahmen, um den Sicherheitsvorfall basierend auf der in der vorherigen Phase durchgeführten Analyse einzudämmen. In dieser Phase kann auch eine weitere Analyse erforderlich sein, um die vollständige Wiederherstellung nach dem Sicherheitsvorfall zu gewährleisten.
- **Aktivität nach dem Vorfall:** Bezieht sich auf die nachträgliche Analyse, die nach der Wiederherstellung eines Sicherheitsvorfalls durchgeführt wurde. Die während des Prozesses durchgeführten betrieblichen Aktionen werden überprüft, um festzustellen, ob Änderungen in den Vorbereitungs- oder Erkennungs- und Analysephasen vorgenommen werden müssen.

![Phasen der Verwaltung von Sicherheitsvorfällen.](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>Antwortmodell für Verbundsicherheit

Microsoft-Onlinedienste bestehen aus wichtigen Microsoft-Produkten, einschließlich Azure, Dynamics 365 und Microsoft 365. Jeder dieser Dienste wird von separaten Teams mit eigenen Sicherheitsprozessen betrieben. Andere Teams bei Microsoft, z. B. MSTIC, sind auch an verschiedenen Sicherheitsaspekten von Microsoft-Onlinediensten beteiligt. Aufgrund der Vielzahl von Teams, die an der Verwaltung von Sicherheitsvorgängen in allen verschiedenen Diensten von Microsoft-Onlinediensten arbeiten, hat Microsoft ein Verbundsicherheitsreaktionsmodell implementiert.

Diese Tabelle enthält die betriebsbereiten Grenzen zwischen den verschiedenen Microsoft Online Service Security Operations Teams und den Microsoft Service Teams:

|**Aktivität**|**Microsoft Security Team Operations**|**Microsoft Service Team Operations**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Erkennung und Analyse | – Erkennungsanforderungen <br> – Sicherheitsüberwachung und -analyse <br> - Indikator für Kompromittierungen (Indicator of compromise, IOC) – Sweeps <br> – Suche nach Sicherheitsverletzungen <br> - 24 x 7 Lead für Sicherheit bei Anrufen und Reaktion auf Vorfälle | – Erkennungsanforderungen <br> – Überwachen der Infrastrukturbereitstellung <br> – Dienstanalyse und Einblicke <br> – Ereignis- und Warnungstriage <br> - 24 x 7 Service Engineering on-Call  |
| Eindämmung, Beseitigung, Wiederherstellung | – Lead für die Reaktion auf Vorfälle <br> – Forensische Untersuchung <br> – Sicherheitskenntnisse und Beratung <br> - Anleitung zur Wiederherstellung | – Besitzer von Sicherheitsvorfällen <br> – Einblick und Expertise des Diensts <br> – Ausführung von Eindämmung, Beseitigung und Wiederherstellung |
| Aktivitäten nach dem Vorfall | – Lead für die Analyse nach dem Vorfall <br> – Datensammlung und Archivierung <br> – Erkenntnisse und Fehleranforderungen <br> – Vorfallberichterstattung | – Dienstseitige Vorfallanalyse <br> – Priorisieren von Nachverfolgungsaktivitäten <br> – Implementierung von Sicherheitsinvestitionen <br> – Bereitschaft zur Dienstsicherheit |

## <a name="related-articles"></a>Verwandte Artikel

- [Microsoft Security Incident Management: Vorbereitung](assurance-sim-preparation.md)
- [Microsoft Security Incident Management: Erkennung und Analyse](assurance-sim-detection-analysis.md)
- [Microsoft Security Incident Management: Eindämmung, Beseitigung und Wiederherstellung](assurance-sim-containment-eradication-recovery.md)
- [Microsoft-Sicherheitsvorfallverwaltung: Aktivitäten nach dem Vorfall](assurance-sim-post-incident-activity.md)
