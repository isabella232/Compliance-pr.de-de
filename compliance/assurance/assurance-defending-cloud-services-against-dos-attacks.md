---
title: Schutz von Microsoft 365-Clouddiensten vor Denial-of-Service-Angriffen
description: In diesem Artikel erfahren Sie, wie Microsoft seine Clouddienste vor Denial-of-Service-Angriffen (Denial-of-Service, DoS) schützen kann.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: e632c1524d5cc8c21aec9dab3d95d285a3b8801e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120574"
---
# <a name="defending-microsoft-365-cloud-services-against-denial-of-service-attacks"></a>Schutz von Microsoft 365-Clouddiensten vor Denial-of-Service-Angriffen

Die Rechenzentren von Microsoft sind durch eine tief gehende Sicherheit geschützt, die Umkreis-Fencing, Videokameras, Sicherheitspersonal und sichere Eingänge umfasst, die biometrische, Smartcard- und mehrstufige Authentifizierung verwenden. Die tief gehende Sicherheit wird über jeden Bereich der Einrichtung und jede physische Servereinheit fortgesetzt. Die [Microsoft Cloud Infrastructure and Operations Group](https://www.microsoft.com/cloud-platform/global-datacenters) stellt die Kerninfrastruktur und grundlegende Technologien für unsere Clouddienste zur Verfügung. Unsere Rechenzentren entsprechen den Branchenstandards für physische Sicherheit und Zuverlässigkeit und werden von Mitarbeitern des Betriebs von Microsoft verwaltet, überwacht und verwaltet.

Um unsere Clouddienste weiter zu schützen, bietet Microsoft ein DDoS-Abwehrsystem, das Teil der kontinuierlichen Überwachung und Penetrationstests von Microsoft Azure ist. Das Azure DDoS-Abwehrsystem ist nicht nur so konzipiert, dass Angriffe von außen, sondern auch von anderen Azure-Mandanten unterstützt werden. Azure verwendet standardmäßige Erkennungs- und Risikominderungstechniken wie SYN-Cookies, Die Geschwindigkeitsbegrenzung und Verbindungslimits zum Schutz vor DDoS-Angriffen.

Die Clouddienste von Microsoft unterliegen der Bedrohung durch Angriffe aus mehreren Quellen. Um die verschiedenen Bedrohungen von DoS abzuwehren und vor diesen zu schützen, wurde ein hoch skalierbares und dynamisches Azure-basiertes Bedrohungserkennungs- und Risikominderungssystem entwickelt und implementiert, das das Hauptziel hat, die zugrunde liegende Infrastruktur vor DoS-Angriffen zu schützen und Dienstunterbrechungen für Kunden von Clouddiensten zu verhindern. Das Azure DoS-Risikominderungssystem schützt eingehenden, ausgehenden und Region-zu-Region-Datenverkehr.

Die meisten DoS-Angriffe, die gegen Ziele auf der Netzwerkebene (L3) und der Transportebene (L4) des [Open Systems Interconnection](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) (OSI)-Modells gestartet werden. Angriffe auf die L3- und die L4-Schicht sind darauf ausgelegt, eine Netzwerkschnittstelle oder einen Dienst mit Angriffsverkehr zu überfluten, um Ressourcen zu überfordern und die Möglichkeit zu verweigern, auf legitimen Datenverkehr zu reagieren. Insbesondere versuchen L3- und L4-Angriffe, entweder die Kapazität von Netzwerkverbindungen, Geräten oder Diensten zu sättigung oder die CPUs von Servern oder virtuellen Computern zu überfordern, die eine Anwendung unterstützen.

Um sich vor L3- und L4-Angriffen zu schützen, hat Microsoft eine Lösung entwickelt, entwickelt und bereitgestellt, die speziell auf den Schutz der Infrastruktur und der Kundenziele ausgerichtet ist, die durch den Schutz dieser Ebenen in Angriff gesetzt werden. Durch den Schutz der Infrastruktur wird sichergestellt, dass Angriffsverkehr, der für einen Kunden vorgesehen ist, keine Sicherheitsbeschädigungen oder eine verringerte Netzwerkqualität für andere Kunden zur Folge hat. Die Lösung verwendet Datenverkehrs-Samplingdaten von Datencenterroutern. Diese Daten werden von einem Netzwerküberwachungsdienst analysiert, um Angriffe zu erkennen. Wenn ein Angriff erkannt wird, treten automatisierte Abwehrmechanismen ein.

## <a name="application-level-defenses"></a>Application-Level Abwehren
Microsoft Engineering Teams folgen den strengen Standards von [Microsoft Operational Security Assurance,](https://www.microsoft.com/SDL/OperationalSecurityAssurance) um Kundendaten zu schützen. Die Clouddienste von Microsoft sind absichtlich so aufgebaut, dass sie eine sehr hohe Last unterstützen sowie um DoS-Angriffe auf Anwendungsebene zu schützen und abzuschwächen. Wir haben eine skalierte Architektur implementiert, bei der Dienste über mehrere globale Rechenzentren mit regionalen Isolations- und Einschränkungsfeatures in einigen der Workloads verteilt sind.

Das Land oder die Region jedes Kunden, das der Administrator des Kunden bei der Ersteinrichtung der Dienste identifiziert, bestimmt den primären Speicherort für die Daten dieses Kunden. Kundendaten werden gemäß einer primären/Sicherungsstrategie zwischen redundanten Rechenzentren repliziert. Ein primäres Datencenter hostet die Anwendungssoftware zusammen mit allen primären Kundendaten, die auf der Software ausgeführt werden. Ein Sicherungsdatencenter bietet ein automatisches Failover. Wenn das primäre Datencenter aus irgendeinem Grund nicht mehr funktioniert, werden Anforderungen an die Kopie der Software und kundendaten im Sicherungsdatencenter umgeleitet. Kundendaten können jederzeit im primären oder im Sicherungsdatencenter verarbeitet werden. Durch die Verteilung von Daten über mehrere Rechenzentren wird die betroffene Oberfläche reduziert, falls ein Rechenzentrum angegriffen wird. Darüber hinaus können die Dienste im betroffenen Datencenter als einer der Wiederherstellungsmechanismen schnell zum sekundären Datencenter umgeleitet werden und umgekehrt (zurück zum primären Datencenter, nachdem der Dienst wiederhergestellt wurde).

Einzelne Workloads umfassen integrierte Features zur Verwaltung der Ressourcenauslastung. Beispielsweise sind die Drosselungsmechanismen in Exchange Online und SharePoint Online Teil eines mehrschichtigen Ansatzes zum Schutz vor DoS-Angriffen. Die Einschränkung für Exchange Online-Benutzer basiert auf dem Vom Endbenutzer verbrauchten Ressourcen, unabhängig davon, ob sich die Ressourcen in Active Directory, im Exchange Online-Informationsspeicher oder an anderer Stelle befinden. Jedem Client wird ein Budget zugewiesen, um die von einem Benutzer verbrauchten Ressourcen zu begrenzen. Die Einschränkung von Exchange Online für Benutzeraktivitäten und Systemkomponenten basiert auf der [Verwaltung der Arbeitsauslastung.](https://technet.microsoft.com/library/jj150503(v=exchg.150).aspx) Eine Exchange Online-Arbeitsauslastung ist ein Exchange Online-Feature, -Protokoll oder -Dienst, das explizit für die Exchange Online-Systemressourcenverwaltung definiert wurde. Jede Exchange Online-Arbeitsauslastung erfordert Systemressourcen wie CPU, Postfachdatenbankvorgänge oder Active Directory-Anforderungen, um Benutzeranforderungen oder Hintergrundarbeiten durchzuführen. Beispiele für Exchange Online-Workloads sind Outlook im Web, Exchange ActiveSync, Postfachmigration und Postfach-Assistenten. Mandantenadministratoren können Einschränkungseinstellungen für die Verwaltung der Arbeitsauslastung von Exchange für Benutzer mit der Exchange-Verwaltungsshell verwalten. Es gibt verschiedene Arten von Drosselung, die in Exchange Online implementiert wurden, darunter PowerShell, Exchange-Webdienste, POP und IMAP, Exchange ActiveSync, Verbindungen mit mobilen Geräten, Empfänger und vieles mehr. Während Administratoren von lokalen Exchange-Bereitstellungen Einschränkungsrichtlinien konfigurieren können, können Administratoren keine Einschränkungsrichtlinien für Exchange Online konfigurieren.

Der häufigste Auslöser für die Drosselung in SharePoint Online ist Client-Side Object Model (CSOM)-Code, der zu viele Aktionen mit zu hoher Häufigkeit ausführt. Mit CSOM können viele Aktionen mit einer einzigen Anforderung ausgeführt werden, die Verwendungsgrenzwerte überschreiten und Benutzereinschränkungen verursachen kann.

Unabhängig von der Aktivität, die zu einer Drosselung führen kann, drosselt SharePoint Online alle weiteren Anforderungen von diesem Benutzerkonto, wenn ein Benutzer die Nutzungsgrenzwerte überschreitet, in der Regel für einen kurzen Zeitraum. Während eine Benutzerdrosselung wirksam ist, werden alle Aktionen dieses Benutzers gemäß den folgenden Kriterien bis zum Ablauf der Drosselung gedrosselt:
- Bei Anforderungen, die vom Benutzer direkt in einem Browser ausgeführt werden, leitet SharePoint Online zu einer Einschränkungsinformationsseite um, und die Anforderungen führen zu einem Fehler.
- Für alle anderen Anforderungen, einschließlich CSOM-Aufrufen, gibt SharePoint Online den #A0 429 ("zu viele Anforderungen") zurück, und die Anforderungen führen zu einem Fehler.

Wenn der beleidende Prozess weiterhin die Verwendungsgrenzwerte überschreitet, blockiert SharePoint Online den Prozess möglicherweise vollständig und gibt den Statuscode 503 des HTTP zurück ("Dienst nicht verfügbar").

## <a name="vulnerability-and-penetration-testing"></a>Sicherheitsrisiko- und Penetrationstests
Microsoft verwendet [](https://www.microsoft.com/trustcenter/security/threatmanagement) viele Sicherheitstechnologien [](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) und -methoden, um seine Cloudinfrastruktur und lokale Netzwerke vor modernen, komplexen Bedrohungen zu schützen, einschließlich der Verwendung von Antischadwarekomponenten und -diensten für Clouddienste, virtuelle Computer (VMs) und andere Systeme. Advanced Threat Analytics, das normale Nutzungsmuster für Netzwerke, Systeme und Benutzer überwacht und maschinelles Lernen verwendet, um jegliches Verhalten zu kennzeichnen, das nicht den üblichen und regelmäßigen Penetrationstests unterlag.

Neben unseren eigenen Penetrationstests und dem Angebot eines [Microsoft Cloud Unified Penetration Testing-Programms](https://technet.microsoft.com/mt784683)für unsere Kunden sind wir auch mit Sicherheitsexperten von Drittanbietern beschäftigt, die regelmäßige Sicherheitsrisikobewertungen und Penetrationstests für unsere Clouddienste durchführen. Wir stellen die Berichte aus diesen Sicherheitsrisikobewertungen von Drittanbietern zum Download über die [Service Trust-](https://aka.ms/STP) und die [Service Assurance-Portale](https://aka.ms/ServiceAssurance) zur Verfügung.
