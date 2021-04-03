---
title: Microsoft 365 Denial-of-Service-Verteidigungsstrategie
description: In diesem Artikel finden Sie eine Übersicht über die Microsoft-Verteidigungsstrategie für Denial-of-Service(DoS)-Angriffe.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
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
ms.openlocfilehash: 5776b3eb6c0b79b5f272d6e24dd8680967ca2eb4
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496954"
---
# <a name="microsoft-365-denial-of-service-defense-strategy"></a>Microsoft 365 Denial-of-Service-Verteidigungsstrategie

## <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Wichtige Grundsätze zum Schutz vor Denial-of-Service-Angriffen

Beim Schutz vor netzwerkbasierten Denial-of-Service(DoS)-Angriffen gibt es drei Kernprinzipien: Aufnahme, Erkennung und Schadensminderung. Die Aufnahme erfolgt vor der Erkennung, und die Erkennung muss erfolgen, bevor die Gegenmaßnahmen beginnen können. Wenn selbst ein kleiner DoS-Angriff nicht aufgefangen werden kann, werden dienste nicht lange genug überdauern, damit der Angriff erkannt wird. Durch erkennen eines Angriffs, bevor das System überlastet ist, können Verteidiger einen Reaktionsplan implementieren.

Die folgende Formel hilft bei der Ungefährung der Auswirkungen eines DoS-Angriffs:

  **Maximale Kapazität (in Byte/s) / Zuwachsrate (in Byte/s) = Zeit bis Auswirkung (in Sec)**

Wenn die Zeit bis zur Erkennung länger ist als die Zeit bis zu den Auswirkungen, wird der DoS-Angriff wahrscheinlich erfolgreich sein. Wenn die Zeit bis zur Erkennung kürzer ist als die Zeit bis zu den Auswirkungen, sollten die angegriffenen Dienste online bleiben und zugänglich bleiben, wenn Gegenmaßnahmenstrategien erfolgreich sind.

Daher gibt es zwei primäre Strategien für die Verteidigung gegen DoS-Angriffe:

- Erhöhen der Kapazität, um die Obergrenze der maximalen Kapazität anzurufen (was wiederum mehr Zeit zum Erkennen eines Angriffs bietet); oder
- Verringern Sie die Zeit zum Erkennen eines Angriffs.

Ein Sicherheitsvorteil der Verwendung von Microsoft Cloud Services besteht in der kostengünstigen Bereitstellung eines starken Netzwerkschutzes für Cloudkunden durch umfangreiche Microsoft-Dienste. Auch im großen Maßstab muss ein Gleichgewicht zwischen Aufnahme, Erkennung und Risikominderung besteht. Um dieses Gleichgewicht zu finden, untersucht Microsoft die Zuwachsraten, um zu schätzen, wie viel Microsoft-Dienste aufnehmen müssen.

## <a name="denial-of-service-defense-strategy"></a>Strategie für den Schutz vor Denial of Service-Angriffen

Die Strategie von Microsoft, sich gegen netzwerkbasierte DoS-Angriffe zu verteidigen, ist aufgrund unseres Umfangs und unserer globalen Präsenz einzigartig. Mit dieser Skalierung kann Microsoft Strategien und Techniken nutzen, die für die meisten anderen Organisationen nicht verfügbar sind. Der Eckpfeiler unserer DoS-Strategie ist unsere globale Präsenz. Microsoft ist mit Internetanbietern, Peeringanbietern (öffentlich und privat) und privaten Unternehmen auf der ganzen Welt verbunden. Dieses Engagement bietet Microsoft eine erhebliche Internetpräsenz und ermöglicht Es Microsoft, Angriffe über eine große Fläche hinweg zu absorbieren.

Da die Edgekapazität von Microsoft im Laufe der Zeit gewachsen ist, hat sich die Bedeutung von Angriffen auf einzelne Kanten erheblich verringert. Aufgrund dieser Verringerung hat Microsoft die Erkennungs- und Risikominderungskomponenten seines DoS-Präventionssystems getrennt. Microsoft stellt mehrstufige Erkennungssysteme in regionalen Rechenzentren zur Erkennung von Angriffen näher an ihren Sättigungspunkten bei gleichzeitiger Aufrechterhaltung der globalen Gegenmaßnahmen an den Edgeknoten zur Verfügung. Diese Strategie stellt sicher, dass Microsoft-Dienste mehrere gleichzeitige Angriffe verarbeiten können.

Eine der effektivsten und kostengünstigsten Abwehrangriffe von Microsoft gegen DoS-Angriffe ist die Reduzierung der Angriffsoberflächen von Dienstangriffen. Unerwünschter Datenverkehr wird am Netzwerkrand verworfen, anstatt die Daten inline zu analysieren, zu verarbeiten und zu bereinigungen.

An der Schnittstelle mit dem öffentlichen Netzwerk verwendet Microsoft spezielle Sicherheitsgeräte für Firewall-, Netzwerkadressenübersetzungs- und IP-Filterfunktionen. Microsoft verwendet auch globales ecmp-Routing (Equal-Cost Multi-Path). Das globale ECMP-Routing ist ein Netzwerkframework, um sicherzustellen, dass mehrere globale Pfade zum Erreichen eines Diensts zur Verfügung stehen. Bei mehreren Pfaden zu jedem Dienst sind DoS-Angriffe auf die Region beschränkt, aus der der Angriff stammt. Andere Regionen sollten von dem Angriff nicht betroffen sein, da Endbenutzer andere Pfade verwenden würden, um den Dienst in diesen Regionen zu erreichen. Microsoft hat auch interne DoS-Korrelations- und Erkennungssysteme entwickelt, die Flussdaten, Leistungsmetriken und andere Informationen verwenden, um DoS-Angriffe schnell zu erkennen.

Zum weiteren Schutz unserer Clouddienste verwendet Microsoft 365 ein verteiltes Denial-of-Service(DDoS)-Schutzsystem, das in die kontinuierlichen Überwachungs- und Penetrationstests von Microsoft Azure integrierte. Das Azure DDoS-Abwehrsystem ist nicht nur für externe Angriffe ausgelegt, sondern auch für Angriffe anderer Azure-Mandanten. Azure verwendet standardmäßige Erkennungs- und Risikominderungstechniken, z. B. SYN-Cookies, Geschwindigkeitsbegrenzungen und Verbindungsgrenzen zum Schutz vor DDoS-Angriffen. Zur Unterstützung unserer automatisierten Schutzmaßnahmen identifiziert ein arbeitslastübergreifendes DoS-Vorfallreaktionsteam die Rollen und Verantwortlichkeiten in allen Teams, die Kriterien für Eskalationen und die Protokolle für die Behandlung von Vorfällen in den betroffenen Teams.

Die meisten gegen Ziele gestarteten DoS-Angriffe befinden sich auf den Ebenen Netzwerk (L3) und Transport (L4) des [Open Systems Interconnection](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) (OSI)-Modells. Angriffe auf die L3- und L4-Ebenen sollen eine Netzwerkschnittstelle oder einen Dienst mit Angriffsdatenverkehr überfluten, um Ressourcen zu überfordern und die Möglichkeit zu verweigern, auf legitimen Datenverkehr zu reagieren. Um sich vor L3- und L4-Angriffen zu schützen, verwenden die DoS-Lösungen von Microsoft Datenverkehrs-Samplingdaten von Datencenterroutern, um die Infrastruktur und die Kundenziele zu schützen. Datenverkehrsstichprobedaten werden von einem Netzwerküberwachungsdienst analysiert, um Angriffe zu erkennen. Wenn ein Angriff erkannt wird, treten automatisierte Abwehrmechanismen ein, um den Angriff zu mildern und sicherzustellen, dass der angriffsverkehr, der auf einen Kunden gerichtet ist, keine Kollateralschäden oder eine verringerte Netzwerkqualität für andere Kunden zur Folge hat.

## <a name="application-level-defenses"></a>Verteidigung auf Anwendungsebene

Microsoft Engineering Teams befolgen die strengen Standards von [Microsoft Operational Security Assurance,](https://www.microsoft.com/SDL/OperationalSecurityAssurance) um Kundendaten zu schützen. Die Clouddienste von Microsoft wurden absichtlich so entwickelt, dass sie hohe Lasten unterstützen, was den Schutz vor DoS-Angriffen auf Anwendungsebene unterstützt. Die skalierte Architektur von Microsoft 365 verteilt Dienste über mehrere globale Rechenzentren mit regionaler Isolation und arbeitslastenspezifischen Einschränkungsfeatures für relevante Workloads.

Das Land oder die Region jedes Kunden, das der Administrator des Kunden während der erst eingerichteten Dienste identifiziert, bestimmt den primären Speicherort für die Daten dieses Kunden. Kundendaten werden zwischen redundanten Rechenzentren gemäß einer primären/Sicherungsstrategie repliziert. Ein primäres Datencenter hostet die Anwendungssoftware zusammen mit allen primären Kundendaten, die auf der Software ausgeführt werden. Ein Sicherungsdatencenter bietet automatisches Failover. Wenn das primäre Datencenter aus irgendeinem Grund nicht mehr funktioniert, werden Anforderungen an die Kopie der Software und kundendaten im Sicherungsdatencenter umgeleitet. Kundendaten können jederzeit im primären oder im Sicherungsdatencenter verarbeitet werden. Durch die Verteilung von Daten über mehrere Rechenzentren wird die betroffene Oberfläche reduziert, falls ein Datencenter angegriffen wird. Darüber hinaus können die Dienste im betroffenen Datencenter schnell an das sekundäre Datencenter umgeleitet werden, um die Verfügbarkeit während eines Angriffs zu gewährleisten und zurück zum primären Datencenter umgeleitet werden, sobald ein Angriff abgemildert wurde.

Als weitere Gegenmaßnahmen gegen DoS-Angriffe umfassen einzelne Arbeitsauslastungen integrierte Features, die die Ressourcenauslastung verwalten. Beispielsweise sind die Drosselungsmechanismen in Exchange Online und SharePoint Online Teil eines mehrschichtigen Ansatzes zum Schutz vor DoS-Angriffen.
