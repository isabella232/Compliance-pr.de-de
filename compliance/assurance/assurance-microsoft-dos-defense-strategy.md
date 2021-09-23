---
title: Microsoft Denial-of-Service-Verteidigungsstrategie
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
ms.openlocfilehash: ba0d0bbea11000144d7091455c6ee204f2c17037
ms.sourcegitcommit: 856111c112a30160950fdd0ce94369aff7e176dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "59489372"
---
# <a name="microsoft-denial-of-service-defense-strategy"></a>Microsoft Denial-of-Service-Verteidigungsstrategie

## <a name="denial-of-service-defense-strategy"></a>Strategie für den Schutz vor Denial of Service-Angriffen

Die Strategie von Microsoft zum Schutz vor netzwerkbasierten verteilten Denial-of-Service (DDoS)-Angriffen ist aufgrund einer großen globalen Präsenz einzigartig, sodass Microsoft Strategien und Techniken nutzen kann, die für die meisten anderen Organisationen nicht verfügbar sind. Darüber hinaus trägt Microsoft zu einem umfassenden Threat Intelligence-Netzwerk bei, das Microsoft-Partner und die umfassendere Internetsicherheitscommunity umfasst, und nutzt dieses gesammelte Wissen. Diese Intelligenz verbessert zusammen mit Informationen, die von Onlinediensten und der globalen Kundenbasis von Microsoft gesammelt werden, kontinuierlich das Microsoft DDoS-Abwehrsystem, das alle Ressourcen von Microsoft-Onlinediensten schützt.

Der Grundpfeiler der DDoS-Strategie von Microsoft ist die globale Präsenz. Microsoft setzt sich mit Internetanbietern, Peeringanbietern (öffentlich und privat) und privaten Unternehmen auf der ganzen Welt zusammen. Durch dieses Engagement erhält Microsoft eine erhebliche Internetpräsenz und ermöglicht es Microsoft, Angriffe über einen großen Oberflächenbereich hinweg aufzufangen.

Da die Edgekapazität von Microsoft im Laufe der Zeit weiter wächst, hat sich die Bedeutung von Angriffen auf einzelne Ränder erheblich verringert. Aufgrund dieser Verringerung hat Microsoft die Erkennungs- und Risikominderungskomponenten seines DDoS-Verhinderungssystems getrennt. Microsoft stellt mehrstufige Erkennungssysteme in regionalen Rechenzentren bereit, um Angriffe zu erkennen, die näher an ihren Sättigungspunkten sind, während gleichzeitig die globale Risikominderung an den Edgeknoten beibehalten wird. Mit dieser Strategie wird sichergestellt, dass Microsoft-Dienste mehrere gleichzeitige Angriffe verarbeiten können.

Eine der effektivsten und kostengünstigsten Schutzmaßnahmen von Microsoft gegen DDoS-Angriffe ist die Reduzierung der Angriffsflächen für Dienste. Unerwünschter Datenverkehr wird am Netzwerkrand verworfen, anstatt die Daten inline zu analysieren, zu verarbeiten und zu scrubbieren.

An der Schnittstelle mit dem öffentlichen Netzwerk verwendet Microsoft spezielle Sicherheitsgeräte für Firewall-, Netzwerkadressübersetzungs- und IP-Filterfunktionen. Microsoft verwendet auch das globale ECMP-Routing (Equal-Cost Multi-Path). Das globale ECMP-Routing ist ein Netzwerkframework, um sicherzustellen, dass es mehrere globale Pfade gibt, um einen Dienst zu erreichen. Bei mehreren Pfaden zu jedem Dienst sind DDoS-Angriffe auf den Bereich beschränkt, aus dem der Angriff stammt. Andere Regionen sollten von dem Angriff nicht betroffen sein, da Endbenutzer andere Pfade verwenden würden, um den Dienst in diesen Regionen zu erreichen. Microsoft hat auch interne DDoS-Korrelations- und Erkennungssysteme entwickelt, die Flussdaten, Leistungsmetriken und andere Informationen verwenden, um DDoS-Angriffe schnell zu erkennen.

Um Clouddienste weiter zu schützen, verwendet Microsoft Azure DDoS Protection, ein DDoS-Abwehrsystem, das in die kontinuierlichen Überwachungs- und Penetrationstests von Microsoft Azure integriert ist. Azure DDoS Protection dient nicht nur dazu, externe Angriffe zu verhindern, sondern auch Angriffe von anderen Azure-Mandanten. Azure verwendet standardmäßige Erkennungs- und Risikominderungstechniken wie SYN-Cookies, Ratenbegrenzungen und Verbindungsgrenzwerte zum Schutz vor DDoS-Angriffen. Zur Unterstützung automatisierter Schutzmaßnahmen identifiziert ein arbeitslastübergreifendes DDoS-Vorfallreaktionsteam die Rollen und Verantwortlichkeiten in allen Teams, die Kriterien für Eskalationen und die Protokolle für die Behandlung von Sicherheitsvorfällen in den betroffenen Teams.

Die meisten DDoS-Angriffe, die gegen Ziele gestartet werden, befinden sich auf der Netzwerk- (L3) und Transportebene (L4) des OSI-Modells [(Open Systems Interconnection).](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Angriffe, die auf die L3- und L4-Ebene gerichtet sind, sind darauf ausgelegt, eine Netzwerkschnittstelle oder einen Dienst mit Angriffsverkehr zu überlasten, um Ressourcen zu überlasten und die Möglichkeit zu verweigern, auf legitimen Datenverkehr zu reagieren. Um sich vor L3- und L4-Angriffen zu schützen, verwenden die DDoS-Lösungen von Microsoft Datenverkehrssamplingdaten von Rechenzentrumsroutern, um die Infrastruktur und die Kundenziele zu schützen. Datenverkehrssamplingdaten werden von einem Netzwerküberwachungsdienst analysiert, um Angriffe zu erkennen. Wenn ein Angriff erkannt wird, treten automatisierte Abwehrmechanismen ein, um den Angriff zu mindern und sicherzustellen, dass der Angriffsverkehr, der auf einen Kunden gerichtet ist, nicht zu Sicherheitsschäden oder einer verringerten Netzwerkqualität für andere Kunden führt.

Microsoft verfolgt auch einen anstößigen Ansatz für die DDoS-Verteidigung. Botnets sind eine häufige Quelle von Befehl und Kontrolle für DDoS-Angriffe, um Angriffe zu verstärken und die Anonymität aufrechtzuerhalten. Der Schwerpunkt der Microsoft DigitalEntstegungseinheit (DCU) liegt auf der Identifizierung, Untersuchung und Unterbrechung der Verteilungs- und Kommunikationsinfrastruktur von Schadsoftware, um den Umfang und die Auswirkungen von Botnets zu verringern.

## <a name="application-level-defenses"></a>Schutzmechanismen auf Anwendungsebene

Die Clouddienste von Microsoft wurden absichtlich entwickelt, um hohe Lasten zu unterstützen, die zum Schutz vor DDoS-Angriffen auf Anwendungsebene beitragen. Die skalierte Architektur von Microsoft verteilt Dienste über mehrere globale Rechenzentren mit regionaler Isolation und workloadspezifischen Drosselungsfunktionen für relevante Workloads.

Das Land oder die Region jedes Kunden, das bzw. die der Administrator des Kunden während der anfänglichen Konfiguration der Dienste identifiziert, bestimmt den primären Speicherort für die Daten dieses Kunden. Kundendaten werden zwischen redundanten Rechenzentren gemäß einer Primären/Sicherungsstrategie repliziert. Ein primäres Rechenzentrum hostet die Anwendungssoftware zusammen mit allen primären Kundendaten, die auf der Software ausgeführt werden. Ein Sicherungsdatencenter bietet automatisches Failover. Wenn das primäre Rechenzentrum aus irgendeinem Grund nicht mehr funktioniert, werden Anforderungen an die Kopie der Software und Kundendaten im Sicherungsdatencenter umgeleitet. Kundendaten können jederzeit entweder im primären oder im Sicherungsdatencenter verarbeitet werden. Durch die Verteilung von Daten über mehrere Rechenzentren wird die betroffene Fläche für den Fall reduziert, dass ein Rechenzentrum angegriffen wird. Darüber hinaus können die Dienste im betroffenen Rechenzentrum schnell an das sekundäre Rechenzentrum umgeleitet werden, um die Verfügbarkeit während eines Angriffs aufrechtzuerhalten, und an das primäre Rechenzentrum umgeleitet werden, sobald ein Angriff abgemildert wurde.

Als weitere Gegenmaßnahme gegen DDoS-Angriffe umfassen einzelne Workloads integrierte Features, die die Ressourcenauslastung verwalten. Beispielsweise sind die Drosselungsmechanismen in Exchange Online und SharePoint Online Teil eines mehrstufigen Ansatzes zum Schutz vor DDoS-Angriffen.

Azure SQL-Datenbank verfügt über eine zusätzliche Sicherheitsebene in Form eines Gatewaydiensts namens DoSGuard, der fehlgeschlagene Anmeldeversuche basierend auf der IP-Adresse verfolgt. Wenn der Schwellenwert für fehlgeschlagene Anmeldeversuche von derselben IP-Adresse erreicht wird, blockiert DoSGuard die Adresse für einen vordefinierten Zeitraum.

## <a name="resources"></a>Ressourcen

- [Übersicht über den Azure DDoS Protection Standard](/azure/ddos-protection/ddos-protection-overview)
- [Grundlegende bewährte Methoden für Azure DDoS Protection Standard](/azure/ddos-protection/fundamental-best-practices)
- [Komponenten einer DDoS-Antwortstrategie](/azure/ddos-protection/ddos-response-strategy)
