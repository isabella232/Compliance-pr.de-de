---
title: Denial-of-Service-Verteidigungsstrategie in Microsoft 365
description: In diesem Artikel finden Sie eine Übersicht über die Microsoft-Verteidigungsstrategie für Denial-of-Service (DoS)-Angriffe.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 56888f704d3cc5da5e820e3cb80a3d10cbb1ef95
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481877"
---
# <a name="microsoft-365-denial-of-service-defense-strategy"></a>Denial-of-Service-Verteidigungsstrategie in Microsoft 365

## <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Wichtige Grundsätze zum Schutz vor Denial-of-Service-Angriffen

Es gibt drei Grundprinzipien beim Schutz vor netzwerkbasierten Denial-of-Service (DoS)-Angriffen: Reduzierung, Erkennung und Risikominderung. Die Risikominderung erfolgt vor der Erkennung, und die Erkennung muss erfolgen, bevor mit der Risikominderung begonnen werden kann. Wenn selbst ein kleiner DoS-Angriff nicht aufgefangen werden kann, werden Dienste nicht lange genug bestehen, damit der Angriff erkannt wird. Indem sie einen Angriff erkennen, bevor das System überlastet ist, können Verteidiger einen Reaktionsplan implementieren.

Die folgende Formel hilft, die Zeit für die Auswirkungen eines DoS-Angriffs anzunähern:

  **Maximum Capacity (in bytes/sec) / Growth Rate (in bytes/sec) = Time to Impact (in sec)**

Wenn die Zeit bis zur Erkennung länger als die Zeit bis zur Auswirkung ist, ist der DoS-Angriff wahrscheinlich erfolgreich. Wenn die Zeit bis zur Erkennung kürzer als die Zeit bis zu den Auswirkungen ist, sollten die angegriffenen Dienste online bleiben und bei erfolgreicher Risikominderungsstrategie zugänglich bleiben.

Daher gibt es zwei primäre Strategien zum Schutz vor DoS-Angriffen:

- Erhöhen Sie die Kapazität, um die Obergrenze der maximalen Kapazität zu erhöhen (was wiederum mehr Zeit zum Erkennen eines Angriffs bietet); Oder
- Verringern Sie die Zeit zum Erkennen eines Angriffs.

Ein Sicherheitsvorteil der Verwendung von Microsoft Cloud Services ist, wie großmaßstäblich Microsoft-Dienste Cloudkunden einen starken Netzwerkschutz auf kostengünstige Weise bieten. Auch in großem Umfang muss ein Gleichgewicht zwischen Dermandierung, Erkennung und Risikominderung vorhanden sein. Um dieses Gleichgewicht zu finden, greift Microsoft die Wachstumsraten an, um zu schätzen, wie viel Microsoft-Dienste auffangen müssen.

## <a name="denial-of-service-defense-strategy"></a>Strategie für den Schutz vor Denial of Service-Angriffen

Die Strategie von Microsoft zum Schutz vor netzwerkbasierten DoS-Angriffen ist aufgrund unseres Umfangs und unserer globalen Präsenz einzigartig. Mit dieser Skalierung kann Microsoft Strategien und Techniken nutzen, die für die meisten anderen Organisationen nicht verfügbar sind. Der Grundpfeiler unserer DoS-Strategie ist unsere globale Präsenz. Microsoft setzt sich mit Internetanbietern, Peeringanbietern (öffentlich und privat) und privaten Unternehmen auf der ganzen Welt zusammen. Durch dieses Engagement erhält Microsoft eine erhebliche Internetpräsenz und ermöglicht es Microsoft, Angriffe über einen großen Oberflächenbereich hinweg aufzufangen.

Da die Edgekapazität von Microsoft im Laufe der Zeit weiter wächst, hat sich die Bedeutung von Angriffen auf einzelne Ränder erheblich verringert. Aufgrund dieser Verringerung hat Microsoft die Erkennungs- und Risikominderungskomponenten seines DoS-Präventionssystems getrennt. Microsoft stellt mehrstufige Erkennungssysteme in regionalen Rechenzentren bereit, um Angriffe zu erkennen, die näher an ihren Sättigungspunkten sind, während die globale Risikominderung an den Edgeknoten beibehalten wird. Mit dieser Strategie wird sichergestellt, dass Microsoft-Dienste mehrere gleichzeitige Angriffe verarbeiten können.

Eine der effektivsten und kostengünstigsten Schutzmaßnahmen von Microsoft gegen DoS-Angriffe ist die Reduzierung der Angriffsflächen für Dienste. Unerwünschter Datenverkehr wird am Netzwerkrand verworfen, anstatt die Daten inline zu analysieren, zu verarbeiten und zu scrubbieren.

An der Schnittstelle mit dem öffentlichen Netzwerk verwendet Microsoft spezielle Sicherheitsgeräte für Firewall-, Netzwerkadressübersetzungs- und IP-Filterfunktionen. Microsoft verwendet auch das globale ECMP-Routing (Equal-Cost Multi-Path). Das globale ECMP-Routing ist ein Netzwerkframework, um sicherzustellen, dass es mehrere globale Pfade gibt, um einen Dienst zu erreichen. Bei mehreren Pfaden zu jedem Dienst sind DoS-Angriffe auf die Region beschränkt, aus der der Angriff stammt. Andere Regionen sollten von dem Angriff nicht betroffen sein, da Endbenutzer andere Pfade verwenden würden, um den Dienst in diesen Regionen zu erreichen. Microsoft hat auch interne DoS-Korrelations- und Erkennungssysteme entwickelt, die Flussdaten, Leistungsmetriken und andere Informationen verwenden, um DoS-Angriffe schnell zu erkennen.

Um unsere Clouddienste weiter zu schützen, verwendet Microsoft 365 ein verteiltes Denial-of-Service (DDoS)-Abwehrsystem, das in die kontinuierlichen Überwachungs- und Penetrationstests von Microsoft Azure integriert ist. Das Azure DDoS-Abwehrsystem ist nicht nur darauf ausgelegt, externe Angriffe, sondern auch Angriffe von anderen Azure-Mandanten zu verhindern. Azure verwendet standardmäßige Erkennungs- und Risikominderungstechniken wie SYN-Cookies, Ratenbegrenzungen und Verbindungsgrenzwerte zum Schutz vor DDoS-Angriffen. Zur Unterstützung unserer automatisierten Schutzmaßnahmen identifiziert ein arbeitslastübergreifendes DoS-Team für die Reaktion auf Vorfälle die Rollen und Verantwortlichkeiten in allen Teams, die Kriterien für Eskalationen und die Protokolle für die Behandlung von Sicherheitsvorfällen in den betroffenen Teams.

Die meisten DoS-Angriffe, die gegen Ziele gestartet werden, befinden sich auf der Netzwerk- (L3) und Transportebene (L4) des OsI-Modells [(Open Systems Interconnection).](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Angriffe, die auf die L3- und L4-Ebene gerichtet sind, sind darauf ausgelegt, eine Netzwerkschnittstelle oder einen Dienst mit Angriffsverkehr zu überlasten, um Ressourcen zu überlasten und die Möglichkeit zu verweigern, auf legitimen Datenverkehr zu reagieren. Um sich vor L3- und L4-Angriffen zu schützen, verwenden die DoS-Lösungen von Microsoft Datenverkehrssamplingdaten von Rechenzentrumsroutern, um die Infrastruktur und Die Kundenziele zu schützen. Datenverkehrssamplingdaten werden von einem Netzwerküberwachungsdienst analysiert, um Angriffe zu erkennen. Wenn ein Angriff erkannt wird, treten automatisierte Abwehrmechanismen ein, um den Angriff zu mindern und sicherzustellen, dass der Angriffsverkehr, der auf einen Kunden gerichtet ist, nicht zu Sicherheitsschäden oder einer verringerten Netzwerkqualität für andere Kunden führt.

## <a name="application-level-defenses"></a>Schutzmechanismen auf Anwendungsebene

Microsoft-Entwicklungsteams folgen den strengen Standards von [Microsoft Operational Security Assurance,](https://www.microsoft.com/SDL/OperationalSecurityAssurance) um Kundendaten zu schützen. Die Clouddienste von Microsoft sind absichtlich so aufgebaut, dass sie hohe Lasten unterstützen, was zum Schutz vor DoS-Angriffen auf Anwendungsebene beiträgt. Die skalierte Architektur Microsoft 365 verteilt Dienste über mehrere globale Rechenzentren mit regionaler Isolation und workloadspezifischen Drosselungsfunktionen für relevante Workloads.

Das Land oder die Region jedes Kunden, das bzw. die der Administrator des Kunden bei der Ersteinrichtung der Dienste identifiziert, bestimmt den primären Speicherort für die Daten dieses Kunden. Kundendaten werden zwischen redundanten Rechenzentren gemäß einer Primären/Sicherungsstrategie repliziert. Ein primäres Rechenzentrum hostet die Anwendungssoftware zusammen mit allen primären Kundendaten, die auf der Software ausgeführt werden. Ein Sicherungsdatencenter bietet automatisches Failover. Wenn das primäre Rechenzentrum aus irgendeinem Grund nicht mehr funktioniert, werden Anforderungen an die Kopie der Software und Kundendaten im Sicherungsdatencenter umgeleitet. Kundendaten können jederzeit entweder im primären oder im Sicherungsdatencenter verarbeitet werden. Durch die Verteilung von Daten über mehrere Rechenzentren wird die betroffene Fläche für den Fall reduziert, dass ein Rechenzentrum angegriffen wird. Darüber hinaus können die Dienste im betroffenen Rechenzentrum schnell an das sekundäre Rechenzentrum umgeleitet werden, um die Verfügbarkeit während eines Angriffs aufrechtzuerhalten, und an das primäre Rechenzentrum umgeleitet werden, sobald ein Angriff abgemildert wurde.

Als weitere Gegenmaßnahme gegen DoS-Angriffe umfassen einzelne Workloads integrierte Features, mit denen die Ressourcennutzung verwaltet wird. Beispielsweise sind die Drosselungsmechanismen in Exchange Online und SharePoint Online Teil eines mehrstufigen Ansatzes zum Schutz vor DoS-Angriffen.
