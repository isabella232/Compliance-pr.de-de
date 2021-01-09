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
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 8a538ee055d10b002ea7efcc7d39ce20658df12b
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787354"
---
# <a name="security-monitoring-overview"></a>Überwachung der Sicherheit (Übersicht)

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Wie sieht die Strategie von Microsoft für die Überwachung der Sicherheit aus?

Microsoft 365 setzt sich für die kontinuierliche Sicherheitsüberwachung seiner Systeme ein, um Bedrohungen für Microsoft 365-Dienste zu erkennen und darauf zu reagieren. Unsere wichtigsten Grundsätze für die Sicherheitsüberwachung und -benachrichtigung sind:

- Robustheit: Signale und Logik zum Erkennen einer Vielzahl von Angriffsverhalten
- Genauigkeit: aussagekräftige Warnungen zur Vermeidung von Ablenkungen durch Rauschgeräusche
- Geschwindigkeit: Möglichkeit, Angreifer schnell genug zu fangen, um sie zu stoppen

Automatisierungs-, Skalierungs- und cloudbasierte Lösungen sind die Schlüsselpfeiler unserer Überwachungs- und Reaktionsstrategie. Damit wir Angriffe im Rahmen einiger Microsoft 365-Basisdienste effektiv erfassen und stoppen können, müssen unsere Überwachungssysteme fast in Echtzeit automatisch hochgenaue Benachrichtigungen auslösen. Wenn ein Problem erkannt wird, benötigen wir die Möglichkeit, das Risiko im großen Maßstab zu mindern. Wir können uns nicht darauf verlassen, dass unser Team Probleme Computer für Computer manuell beheben kann. Um Risiken erforderlichen Umfang zu minimieren, verwenden wir cloudbasierte Tools, um automatisch Gegenmaßnahmen anzuwenden und Entwicklern Werkzeuge zur Verfügung zu stellen, mit denen bewährte Minimierungsmaßnahmen in der gesamten Umgebung schnell angewendet werden können.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Wie führt Microsoft 365 eine Sicherheitsüberwachung aus?

Microsoft 365 verwendet die zentralisierte Protokollierung, um Protokollereignisse für Aktivitäten zu sammeln und zu analysieren, die auf einen Sicherheitsvorfall hinweisen können. Tools für die zentralisierte Protokollierung aggregieren Protokolle aller Systemkomponenten, einschließlich Ereignisprotokolle, Anwendungsprotokolle, Zugriffssteuerungsprotokolle und netzwerkbasierten Angriffserkennungssysteme. Zusätzlich zur Serverprotokollierung und Daten auf Anwendungsebene ist die Kerninfrastruktur unseres Dienstes mit kundenspezifischen Sicherheits-Agents ausgestattet, die detaillierte Telemetrie erzeugen und hostbasierte Angriffserkennung bieten. Wir nutzen diese Telemetrie für Überwachung und Forensik.

Die erfassten Protokollierungs- und Telemetriedaten ermöglichen 24/7-Sicherheitswarnungen. Unser Warnungssystem analysiert Protokolldaten, während sie hochgeladen werden, und erzeugt fast in Echtzeit Warnungen. Dies umfasst regelbasierte und fortgeschrittene Warnungen basierend auf Modellen für maschinelles Lernen. Unsere Überwachungslogik geht über generische Angriffsszenarien hinaus und enthält ein tiefgreifendes Wissen über die Dienstarchitektur und den Betrieb. Wir verwenden Sicherheitsüberwachungsdaten, um unsere Modelle kontinuierlich zu verbessern und neue Arten von Angriffen zu erkennen sowie die Genauigkeit unserer Sicherheitsüberwachung zu verbessern.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Wie reagiert Microsoft 365 auf Sicherheitsüberwachungswarnungen?

Wenn wir eine Aktion als Reaktion auf eine Warnung oder zur weiteren Untersuchung forensischer Nachweise während des gesamten Diensts ergreifen müssen, lassen sich mit unseren cloudbasierten Tools in der gesamten Umgebung schnell reagieren. Zu diesen Tools zählen vollständig automatisierte, intelligente Agents, die mit Sicherheitsmaßnahmen auf erkannte Bedrohungen reagieren. In vielen Fällen werden mit diesen Agenten automatische Gegenmaßnahmen zur Minimierung von Sicherheitsentdeckungen im erforderlichen Umfang bereitgestellt. Wenn dies nicht möglich ist, warnt das Sicherheitsuberwachungssystem automatisch die entsprechenden Techniker, die mit einer Reihe von Werkzeugen ausgerüstet sind, die es Ihnen ermöglichen, in Echtzeit zu agieren, um erkannte Bedrohungen im erforderlichen Umfang zu minimieren. Potenzielle Vorfälle, die an das Microsoft 365 Security Response-Team eskaliert wurden, werden mithilfe des Prozesses zur Reaktion auf Sicherheitsvorfälle behoben.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Wie überwacht Microsoft 365 die Systemverfügbarkeit?

Microsoft 365 überwacht seine Systeme aktiv auf Indikatoren für eine zu hohe Ressourcenauslastung und anormale Nutzung. Die Ressourcenüberwachung wird durch Dienstredundanzen ergänzt, um unerwartete Ausfallzeiten zu vermeiden und Kunden zuverlässigen Zugriff auf Produkte und Dienste zu bieten. Dienstinte health issues are communicated promptly to customers through the Service Health Dashboard (SHD).

## <a name="related-external-regulations--certifications"></a>Verwandte externe Bestimmungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf Einhaltung externer Bestimmungen und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Sicherheitsüberwachung.

| **Externe Überwachungen** | **Section** | **Datum des letzten Berichts** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Kontoverwaltung <br> AC-17: Remotezugriff <br> AU-7: Reduzierung der Überwachung und Berichterstellung <br> SI-4: Überwachung des Informationssystems <br> SI-7: Software, Firmware und Informationsintegrität <br> | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Verfügbarkeitsüberwachung und Kapazitätsplanung | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Verfügbarkeitsüberwachung und Kapazitätsplanung <br> A.16.1: Verwaltung von Vorfällen und Verbesserungen der Informationssicherheit | Februar 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Änderungsüberwachung <br> CA-26: Melden von Sicherheitsvorfällen <br> CA-29: On-Call-Techniker <br> CA-48: Datencenterprotokollierung | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Änderungsüberwachung <br> CA-26: Melden von Sicherheitsvorfällen <br> CA-29: On-Call-Techniker <br> CA-30: Verfügbarkeitsüberwachung <br> CA-48: Datencenterprotokollierung | 24. Dezember 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: Melden von Vorfällen <br> CUEC-10: Serviceverträge | 24. Dezember 2020 |

## <a name="resources"></a>Ressourcen

- [Hinter den Kulissen: Sicherung der Infrastruktur beim Einbringen des Microsoft 365-Diensts](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
