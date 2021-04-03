---
title: Verwaltung von Sicherheitsvorfällen unter Microsoft 365
description: Dieser Artikel enthält eine Übersicht über den Prozess zur Verwaltung von Sicherheitsvorfällen in Microsoft 365.
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
ms.openlocfilehash: a61a4406c4951c4d4584831cf58030545955fd35
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496782"
---
# <a name="microsoft-365-security-incident-management"></a>Verwaltung von Sicherheitsvorfällen unter Microsoft 365

Microsoft arbeitet kontinuierlich an der Bereitstellung von hochsicheren Diensten auf Unternehmensqualität für Microsoft 365-Kunden. In diesem Dokument wird beschrieben, wie Microsoft Sicherheitsvorfälle in Microsoft 365 behandelt. Ein Sicherheitsvorfall bezieht sich auf einen unrechtmäßigen Zugriff auf Kundendaten, die auf microsofts Geräten oder in Microsoft-Einrichtungen gespeichert sind, oder auf nicht autorisierten Zugriff auf solche Geräte oder Einrichtungen, die zum Verlust, zur Offenlegung oder Änderung von Kundendaten führen können. Microsofts Ziele bei der Reaktion auf Sicherheitsvorfälle sind der Schutz von Kundendaten und den Microsoft 365-Diensten.

Das Microsoft 365 Security-Team und die verschiedenen Dienstteams arbeiten gemeinsam und gehen bei Sicherheitsvorfällen den gleichen Ansatz ein:

- Vorbereitung
- Erkennung und Analyse
- Eindämmung
- Beseitigung
- Wiederherstellung
- Aktivitäten nach dem Vorfall

## <a name="microsoft-approach-to-security-incident-management"></a>Microsoft-Ansatz für die Verwaltung von Sicherheitsvorfällen

Microsofts Ansatz zur Verwaltung eines Sicherheitsvorfalls entspricht dem [National Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61. Microsoft verfügt über mehrere dedizierte Teams, die zusammenarbeiten, um Sicherheitsvorfälle zu verhindern, zu überwachen, zu erkennen und darauf zu reagieren.

|**Team/Bereich**|**Beschreibung**|
|:------------|:--------------|
| Microsoft Security Response Center | Identifiziert, überwacht, löst und reagiert auf Sicherheitsvorfälle und Sicherheitsrisiken von Microsoft Software. |
| Cyber Defense Operations Center | Das Cyber Defense Operations Center ist der physische Standort, an dem Sicherheitsreaktionsteams und Experten aus dem gesamten Unternehmen zusammenkommen, um Bedrohungen in Echtzeit zu schützen, zu erkennen und darauf zu reagieren. |
| Corporate, External, and Legal Affairs | Bietet rechtliche und rechtliche Hinweise für einen verdächtigen Sicherheitsvorfall. |
| Microsoft 365 Security Response Team | Partner mit Microsoft 365-Serviceteams, um den entsprechenden Prozess zur Verwaltung von Sicherheitsvorfällen zu erstellen und die Reaktion auf Sicherheitsvorfälle zu unterstützen. |
| Office 365 Trust | Enthält Anleitungen zu behördlichen Anforderungen, Compliance und Datenschutz. |
| Microsoft 365 Datacenter Security Team | Team, das sich in den verschiedenen Diensten auf gemeinsame Sicherheitstechnikinvestitionen konzentriert, um Risiken und Bedrohungen der Microsoft 365-Dienstarchitektur zu schützen, zu erkennen und darauf zu reagieren. |
| Serviceteams | Engineering teams for Microsoft 365 services, such as Exchange, SharePoint, and Microsoft Teams, that are responsible for security-related policies and decisions for each service. |
| Microsoft Threat Intelligence Center (MSTIC) | Bietet den aktuellen Stand der Technik in digitalen Sicherheitsbedrohungen gegen die Microsoft-Infrastruktur und -Ressourcen, unterstützt Partnerteams innerhalb von Microsoft bei der Priorisierung von Maßnahmenplänen für Maßnahmen zur Risikominderung und Verhinderung und erhöht den Schutz, indem sie die Überwachung/Erkennung von Vorfällen in Echtzeit übernehmen. |
| PartnerSicherheitsteams | Andere Partnersicherheitsteams in Microsoft, die wichtige Dienste bereitstellen oder für wichtige Abhängigkeiten in Microsoft 365 verantwortlich sind, z. B. das Azure Security Response-Team, Identity Security Response und Microsoft Corporate Security Response Teams. |
| Microsoft 365 Customer Experience Communications | Engineering team responsible for all customer communications about security and service incidents. |

## <a name="response-management-process"></a>Reaktionsverwaltungsprozess

Das Microsoft 365-Sicherheitsteam und die Dienstteams arbeiten zusammen und gehen denselben Ansatz für Sicherheitsvorfälle ein, der auf den Reaktionsverwaltungsphasen von NIST 800-61 basiert:

- **Vorbereitung**: Bezieht sich auf die organisatorische Vorbereitung, die erforderlich ist, um reagieren zu können, einschließlich Tools, Prozesse, Kompetenzen und Bereitschaft.
- **Erkennung &:** Bezieht sich auf die Aktivität, um einen Sicherheitsvorfall in einer Produktionsumgebung zu erkennen und alle Ereignisse zu analysieren, um die Echtheit des Sicherheitsvorfalls zu bestätigen.
- **Eindämmung, Auslöschung,** Wiederherstellung : Bezieht sich auf die erforderlichen und geeigneten Maßnahmen zur Eindämmung des Sicherheitsvorfalls basierend auf der Analyse in der vorherigen Phase. Möglicherweise ist in dieser Phase auch eine weitere Analyse erforderlich, um die vollständige Wiederherstellung nach dem Sicherheitsvorfall zu gewährleisten.
- **Aktivität nach dem Vorfall**: Bezieht sich auf die Post-Mortem-Analyse, die nach der Wiederherstellung eines Sicherheitsvorfalls durchgeführt wurde. Die während des Prozesses ausgeführten operativen Aktionen werden überprüft, um festzustellen, ob änderungen in den Vorbereitungs- oder Erkennungs- und Analysephasen vorgenommen werden müssen.

## <a name="federated-security-response-model"></a>Verbundsicherheitsantwortmodell

Zu den Microsoft 365-Diensten gehören die wichtigsten Microsoft Onlinedienste (Exchange, SharePoint und Microsoft Teams usw.) und andere Microsoft-Clouddienste, z. B. Azure Active Directory, die Microsoft Commerce Platform und msTIC. Diese Dienste werden von separaten Teams mit eigenen Sicherheitsabläufen betrieben. Andere Teams bei Microsoft sind auch mit verschiedenen Sicherheitsaspekten von Microsoft 365 beschäftigt. Aufgrund der Vielzahl von Teams, die an der Verwaltung von Sicherheitsvorgängen in allen verschiedenen Diensten von Microsoft 365 arbeiten, hat Microsoft ein Verbundsicherheitsreaktionsmodell implementiert.

In dieser Tabelle sind die Betriebsgrenzen zwischen den verschiedenen Microsoft 365-Sicherheitsbetriebsteams und den Microsoft 365-Dienstteams aufgeführt:

|**Aktivität**|**Microsoft 365 Security Team Operations**|**Microsoft 365 Service Team Operations**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Erkennung und Analyse | – Erkennungsanforderungen <br> - Sicherheitsüberwachung und -analyse <br> - Indikator für Kompromissfeger (IOC) <br> – Verletzungssuche <br> – 24 x 7 Sicherheitsvorsprung bei Anruf und Reaktion auf Vorfälle | – Erkennungsanforderungen <br> - Überwachen der Infrastrukturbereitstellung <br> - Dienstanalyse und -einblick <br> - Ereignis- und Warnungstriage <br> - 24 x 7 Service Engineering on-Call  |
| Eindämmung, Auslöschung, Wiederherstellung | – Vorfallreaktionsvorsprung <br> - Forensische Untersuchung <br> - Sicherheitsexpertise und -beratung <br> – Anleitung zur Wiederherstellung | - Besitzer von Sicherheitsvorfällen <br> – Service-Einblick und -kompetenz <br> – Ausführen von Eindämmung, Auslöschung und Wiederherstellung |
| Aktivitäten nach dem Vorfall | – Lead für die Analyse nach dem Vorfall <br> - Datensammlung und -archivierung <br> – Gelernte Lektionen und Fehleranforderungen <br> – Bericht über Vorfälle | - Dienstseitige Vorfallanalyse <br> – Priorisieren von Follow-up-Aktivitäten <br> – Investitionen in die Implementierungssicherheit <br> - Dienstsicherheitsbereitschaft |

## <a name="related-articles"></a>Verwandte Artikel

- [Vorbereitung der Sicherheitsvorfälle in Microsoft 365](assurance-sim-preparation.md)
- [Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365](assurance-sim-detection-analysis.md)
- [Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen in Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 Security Incident Management post-incident activity](assurance-sim-post-incident-activity.md)
