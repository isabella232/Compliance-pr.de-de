---
title: Überwachung der Sicherheit (Übersicht)
description: Informationen zur Sicherheitsüberwachung in Microsoft 365
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
ms.openlocfilehash: 95762cef8c7287c7a028554efd18ad0098b49198
ms.sourcegitcommit: 01938022a292c07e98041dc6ae1312a1b8c617db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "58260750"
---
# <a name="security-monitoring-overview"></a>Überwachung der Sicherheit (Übersicht)

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Was ist die Microsoft-Strategie für die Überwachung der Sicherheit?

Microsoft nimmt an einer kontinuierlichen Sicherheitsüberwachung seiner Systeme teil, um Bedrohungen für Microsoft-Onlinedienste zu erkennen und darauf zu reagieren. Unsere wichtigsten Grundsätze für die Sicherheitsüberwachung und -warnung sind:

- Robustheit: Signale und Logik zum Erkennen verschiedener Angriffsverhalten
- Genauigkeit: aussagekräftige Warnungen, um Ablenkungen durch Rauschen zu vermeiden
- Geschwindigkeit: Möglichkeit, Angreifer schnell genug abzufangen, um sie zu stoppen

Automatisierungs-, Skalierungs- und cloudbasierte Lösungen sind die Schlüsselpfeiler unserer Überwachungs- und Reaktionsstrategie. Damit wir Angriffe im Umfang einiger Microsoft-Onlinedienste effektiv verhindern können, müssen unsere Überwachungssysteme nahezu in Echtzeit automatisch hochgenaue Warnungen auslösen. Wenn ein Problem erkannt wird, benötigen wir auch die Möglichkeit, das Risiko im großen Maßstab zu mindern. Wir können uns nicht darauf verlassen, dass unser Team Probleme computerweise manuell behebt. Um Risiken in großem Umfang zu mindern, verwenden wir cloudbasierte Tools, um automatisch Gegenmaßnahmen anzuwenden und Technikern Tools zur Verfügung zu stellen, mit denen genehmigte Maßnahmen schnell in der gesamten Umgebung angewendet werden können.

## <a name="how-do-microsoft-online-services-perform-security-monitoring"></a>Wie führen Microsoft-Onlinedienste eine Sicherheitsüberwachung durch?

Microsoft-Onlinedienste verwenden die zentrale Protokollierung, um Protokollereignisse für Aktivitäten zu sammeln und zu analysieren, die auf einen Sicherheitsvorfall hinweisen können. Tools für die zentralisierte Protokollierung aggregieren Protokolle aller Systemkomponenten, einschließlich Ereignisprotokolle, Anwendungsprotokolle, Zugriffssteuerungsprotokolle und netzwerkbasierten Angriffserkennungssysteme. Zusätzlich zur Serverprotokollierung und Daten auf Anwendungsebene ist die Kerninfrastruktur mit angepassten Sicherheits-Agents ausgestattet, die detaillierte Telemetrie generieren und hostbasierte Angriffserkennung bereitstellen. Wir nutzen diese Telemetrie für Überwachung und Forensik.

Die erfassten Protokollierungs- und Telemetriedaten ermöglichen 24/7-Sicherheitswarnungen. Unser Warnungssystem analysiert Protokolldaten, während sie hochgeladen werden, und erzeugt fast in Echtzeit Warnungen. Dies umfasst regelbasierte und fortgeschrittene Warnungen basierend auf Modellen für maschinelles Lernen. Unsere Überwachungslogik geht über generische Angriffsszenarien hinaus und enthält ein tiefgreifendes Wissen über die Dienstarchitektur und den Betrieb. Wir analysieren Daten zur Sicherheitsüberwachung, um unsere Modelle kontinuierlich zu verbessern, um neue Arten von Angriffen zu erkennen und die Genauigkeit unserer Sicherheitsüberwachung zu verbessern.

## <a name="how-do-microsoft-online-services-respond-to-security-monitoring-alerts"></a>Wie reagieren Microsoft-Onlinedienste auf Warnungen zur Sicherheitsüberwachung?

Wenn Sicherheitsereignisse, die Warnungen auslösen, reaktionsfähige Maßnahmen erfordern oder forensische Nachweise im gesamten Dienst weiter untersuchen müssen, ermöglichen unsere cloudbasierten Tools eine schnelle Reaktion in der gesamten Umgebung. Zu diesen Tools zählen vollständig automatisierte, intelligente Agents, die mit Sicherheitsmaßnahmen auf erkannte Bedrohungen reagieren. In vielen Fällen werden mit diesen Agenten automatische Gegenmaßnahmen zur Minimierung von Sicherheitsentdeckungen im erforderlichen Umfang bereitgestellt. Wenn diese Antwort nicht möglich ist, benachrichtigt das Sicherheitsüberwachungssystem automatisch die entsprechenden Bereitschaftstechniker, die mit einer Reihe von Tools ausgestattet sind, mit denen sie in Echtzeit reagieren können, um erkannte Bedrohungen im großen Maßstab zu mindern. Potenzielle Vorfälle werden an das entsprechende Microsoft-Sicherheitsteam eskaliert und mithilfe des Prozesses zur Reaktion auf Sicherheitsvorfälle behoben.

## <a name="how-do-microsoft-online-services-monitor-system-availability"></a>Wie überwachen Microsoft-Onlinedienste die Systemverfügbarkeit?

Microsoft überwacht seine Systeme aktiv auf Indikatoren für Ressourcenüberlastung und anormale Nutzung. Die Ressourcenüberwachung wird durch Dienstredundanzen ergänzt, um unerwartete Ausfallzeiten zu vermeiden und Kunden zuverlässigen Zugriff auf Produkte und Dienste zu bieten. Microsoft Online Service Health-Probleme werden Kunden über das Service Health Dashboard (SHD) umgehend mitgeteilt.

Azure- und Dynamics 365-Onlinedienste nutzen mehrere Infrastrukturdienste, um ihre Sicherheits- und Integritätsverfügbarkeit zu überwachen. Die Implementierung von STX-Tests (Synthetic Transaction) ermöglicht Es Azure und Dynamics-Diensten, die Verfügbarkeit ihrer Dienste zu überprüfen. Das STX-Framework wurde entwickelt, um das automatisierte Testen von Komponenten in ausgeführten Diensten zu unterstützen, und wird auf Warnungen bei Live-Websitefehlern getestet. Darüber hinaus hat der Azure Security Monitoring (ASM)-Dienst zentralisierte synthetische Testverfahren implementiert, um zu überprüfen, ob Sicherheitswarnungen in neuen und ausgeführten Diensten erwartungsgemäß funktionieren.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Sicherheitsüberwachung.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------|:--------|:------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Verfügbarkeitsüberwachung und Kapazitätsplanung | 2. Dezember 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Verfügbarkeitsüberwachung und Kapazitätsplanung <br> A.16.1: Verwaltung von Vorfällen und Verbesserungen der Informationssicherheit | 2. Dezember 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | Chat-1: Vorfallverwaltungsframework <br> Chat-2: Konfiguration der Vorfallerkennung <br> CHAT-3: Verfahren für die Vorfallverwaltung <br> CHAT-4: Vorfall nach der Analyse <br> VM-1: Protokollierung und Sammlung von Sicherheitsereignissen <br> VM-12: Überwachung der Verfügbarkeit von Azure-Diensten <br> VM-4: Untersuchung bösartiger Ereignisse <br> VM-6: Überwachung von Sicherheitsrisiken | 31. März 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | Chat-1: Vorfallverwaltungsframework <br> Chat-2: Konfiguration der Vorfallerkennung <br> CHAT-3: Verfahren für die Vorfallverwaltung <br> CHAT-4: Vorfall nach der Analyse <br> PI-2: Überprüfung der SLA-Leistung des Azure-Portals <br> VM-1: Protokollierung und Sammlung von Sicherheitsereignissen <br> VM-12: Überwachung der Verfügbarkeit von Azure-Diensten <br> VM-4: Untersuchung bösartiger Ereignisse <br> VM-6: Überwachung von Sicherheitsrisiken | 31. März 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------|:--------|:------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2: Kontoverwaltung <br> AC-17: Remotezugriff <br> AU-7: Audit-Reduzierung und Berichterstellung <br> SI-4: Überwachung des Informationssystems <br> SI-7: Software, Firmware und Informationsintegrität <br> | 24. September 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Verfügbarkeitsüberwachung und Kapazitätsplanung | 20. April 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Änderungsüberwachung <br> CA-26: Berichterstellung über Sicherheitsvorfälle <br> CA-29: Bereitschaftstechniker <br> CA-48: Rechenzentrumsprotokollierung | 24. Dezember 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Änderungsüberwachung <br> CA-26: Berichterstellung über Sicherheitsvorfälle <br> CA-29: Bereitschaftstechniker <br> CA-30: Verfügbarkeitsüberwachung <br> CA-48: Rechenzentrumsprotokollierung | 24. Dezember 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Melden von Vorfällen <br> CUEC-10: Serviceverträge | 24. Dezember 2020 |

## <a name="resources"></a>Ressourcen

- [Hinter den Kulissen: Sicherung der Infrastruktur beim Einbringen des Microsoft 365-Diensts](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
