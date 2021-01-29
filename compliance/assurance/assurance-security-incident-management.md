---
title: Verwaltung von Sicherheitsvorfällen in Microsoft 365
description: Dieser Artikel bietet eine Übersicht über den Prozess zur Verwaltung von Sicherheitsvorfällen in Microsoft 365.
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
ms.openlocfilehash: 9a76a258edf77708786cf19b160c4c5ee7af7ee6
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040358"
---
# <a name="microsoft-365-security-incident-management"></a>Verwaltung von Sicherheitsvorfällen in Microsoft 365

Microsoft arbeitet kontinuierlich daran, microsoft 365-Kunden äußerst sichere Dienste auf Unternehmensqualität anzubieten. In diesem Dokument wird beschrieben, wie Microsoft Sicherheitsvorfälle in Microsoft 365 behandelt. Ein Sicherheitsvorfall bezieht sich auf jeglichen unrechtmäßigen Zugriff auf Kundendaten, die auf Geräten von Microsoft oder in Einrichtungen von Microsoft gespeichert sind, oder auf nicht autorisierten Zugriff auf solche Geräte oder Einrichtungen, die zu Verlust, Offenlegung oder Änderung von Kundendaten führen können. Die Ziele von Microsoft bei der Reaktion auf Sicherheitsvorfälle sind der Schutz von Kundendaten und den Microsoft 365-Diensten.

Das Microsoft 365 -Sicherheitsteam und die verschiedenen Serviceteams arbeiten gemeinsam und gehen denselben Ansatz für Sicherheitsvorfälle ein:

- Vorbereitung
- Erkennung und Analyse
- Eindämmung
- Beseitigung
- Wiederherstellung
- Aktivitäten nach dem Vorfall

## <a name="microsoft-approach-to-security-incident-management"></a>Ansatz von Microsoft für die Verwaltung von Sicherheitsvorfällen

Der Ansatz von Microsoft zur Verwaltung eines Sicherheitsvorfalls entspricht dem [National Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61. Microsoft verfügt über mehrere dedizierte Teams, die zusammenarbeiten, um Sicherheitsvorfälle zu verhindern, zu überwachen, zu erkennen und darauf zu reagieren.

|**Team/Bereich**|**Beschreibung**|
|:------------|:--------------|
| Microsoft Security Response Center | Identifiziert, überwacht, löst und reagiert auf Sicherheitsvorfälle und Microsoft-Softwaresicherheitsrisiken. |
| Cyber Defense Operations Center | Das Cyber Defense Operations Center ist der physische Standort, an dem Sicherheitsteams und Experten aus dem gesamten Unternehmen zusammenkommen, um Bedrohungen in Echtzeit zu schützen, zu erkennen und darauf zu reagieren. |
| Unternehmens-, Externe und Rechtsfragen | Bietet rechtliche und behördliche Ratschläge für einen verdächtigen Sicherheitsvorfall. |
| Microsoft 365 Security Response Team | Arbeiten Sie mit Microsoft 365-Serviceteams zusammen, um den geeigneten Prozess zur Verwaltung von Sicherheitsvorfällen zu erstellen und die Reaktion auf Sicherheitsvorfälle zu unterstützen. |
| Office 365 Trust | Enthält Anleitungen zu behördlichen Anforderungen, Compliance und Datenschutz. |
| Microsoft 365 Datacenter Security Team | Team, das sich in den verschiedenen Diensten auf gemeinsame Sicherheitstechnikinvestitionen konzentriert, um Risiken und Bedrohungen der Microsoft 365-Dienstarchitektur zu schützen, zu erkennen und darauf zu reagieren. |
| Serviceteams | Entwicklungsteams für Microsoft 365-Dienste wie Exchange, SharePoint und Microsoft Teams, die für sicherheitsbezogene Richtlinien und Entscheidungen für jeden Dienst verantwortlich sind. |
| Microsoft Threat Intelligence Center (MSTIC) | Bietet den aktuellen Stand der Technik in digitalen Sicherheitsbedrohungen gegen die Infrastruktur und Ressourcen von Microsoft, hilft Partnerteams innerhalb von Microsoft bei der Priorisierung von Maßnahmenplänen für Risikominderung und Verhinderung und erhöht den Schutz durch die Einführung nahezu echtzeitnaher Vorfallüberwachung/-erkennung. |
| Partnersicherheitsteams | Andere Partnersicherheitsteams innerhalb von Microsoft, die wichtige Dienste bereitstellen oder für wichtige Abhängigkeiten in Microsoft 365 verantwortlich sind, z. B. das Azure Security Response-Team, Identity Security Response und Microsoft Corporate Security Response Teams. |
| Microsoft 365 Customer Experience Communications | Entwicklungsteam, das für die gesamte Kundenkommunikation über Sicherheits- und Dienstvorfälle verantwortlich ist. |

## <a name="response-management-process"></a>Reaktionsverwaltungsprozess

Das Microsoft 365 -Sicherheitsteam und die Serviceteams arbeiten zusammen an einem Ansatz für Sicherheitsvorfälle, der auf den Phasen der NIST 800-61-Reaktionsverwaltung basiert:

- **Vorbereitung:** Bezieht sich auf die Vorbereitung der Organisation, die erforderlich ist, um reagieren zu können, einschließlich Tools, Prozesse, Kompetenzen und Bereitschaft.
- **Erkennung &:** Bezieht sich auf die Aktivität, um einen Sicherheitsvorfall in einer Produktionsumgebung zu erkennen und alle Ereignisse zu analysieren, um die Echtheit des Sicherheitsvorfalls zu bestätigen.
- **Eindämmung, Beseitigung,** Wiederherstellung: Bezieht sich auf die erforderlichen und geeigneten Maßnahmen, die zur Eindämmung des Sicherheitsvorfalls auf der Grundlage der in der vorherigen Phase durchgeführten Analyse ergriffen wurden. In dieser Phase kann auch eine weitere Analyse erforderlich sein, um die vollständige Wiederherstellung nach dem Sicherheitsvorfall zu gewährleisten.
- **Aktivitäten nach dem Vorfall:** Bezieht sich auf die nachträgliche Analyse, die nach der Wiederherstellung eines Sicherheitsvorfalls durchgeführt wurde. Die während des Prozesses ausgeführten operativen Aktionen werden überprüft, um festzustellen, ob in den Vorbereitungs- oder Erkennungs- und Analysephasen Änderungen vorgenommen werden müssen.

## <a name="federated-security-response-model"></a>Reaktionsmodell für die Verbundsicherheit

Microsoft 365-Dienste umfassen grundlegende Microsoft Onlinedienste (Exchange, SharePoint und Microsoft Teams usw.) und andere Microsoft-Clouddienste, wie Azure Active Directory, die Microsoft Commerce Platform und MSTIC. Diese Dienste werden von separaten Teams mit eigenen Sicherheitsprozessen betrieben. Andere Teams bei Microsoft sind auch an verschiedenen Sicherheitsaspekten von Microsoft 365 beschäftigt. Aufgrund der Vielzahl von Teams, die an der Verwaltung von Sicherheitsvorgängen in allen verschiedenen Diensten von Microsoft 365 arbeiten, hat Microsoft ein Verbundmodell für die Sicherheitsreaktion implementiert.

Diese Tabelle enthält die betriebsbereiten Grenzen zwischen den verschiedenen Microsoft 365-Sicherheitsteams und den Microsoft 365-Serviceteams:

|**Aktivität**|**Microsoft 365 Security Team Operations**|**Microsoft 365 Service Team Operations**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Erkennung und Analyse | – Erkennungsanforderungen <br> - Sicherheitsüberwachung und -analyse <br> – IOC(Indicator of Compromise)-Aufrrungen <br> – Suche nach Sicherheitsverletzungen <br> - 24 x 7-Sicherheitsvorsprung bei Anruf und Reaktion auf Sicherheitsvorfälle | – Erkennungsanforderungen <br> – Überwachen der Infrastrukturbereitstellung <br> – Dienstanalyse und Einblick <br> – Ereignis- und Warnungstriage <br> - 24 x 7 Service Engineering on-call  |
| Eindämmung, Beseitigung, Wiederherstellung | – Vorfallreaktionsleiter <br> – Forensische Untersuchung <br> - Sicherheitskenntnisse und -beratungs <br> - Anleitung zur Wiederherstellung | – Besitzer des Sicherheitsvorfalls <br> – Einblick und Fachwissen des Diensts <br> – Eindämmung, Beseitigung und Wiederherstellung ausführen |
| Aktivitäten nach dem Vorfall | – Leiter der Analyse nach einem Vorfall <br> – Datensammlung und Archivierung <br> – Gelernte Lektionen und Fehleranforderungen <br> – Vorfallberichterstattung | – Dienstseitige Vorfallanalyse <br> – Priorisieren von Aktivitäten nach dem Folgen <br> – Investitionen in die Implementierungssicherheit <br> - Dienstsicherheitsbereitschaft |

## <a name="related-articles"></a>Verwandte Artikel

- [Vorbereitung der Verwaltung von Sicherheitsvorfällen in Microsoft 365](assurance-sim-preparation.md)
- [Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365](assurance-sim-detection-analysis.md)
- [Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen in Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365-Sicherheitsvorfallverwaltung nach einem Vorfall](assurance-sim-post-incident-activity.md)
