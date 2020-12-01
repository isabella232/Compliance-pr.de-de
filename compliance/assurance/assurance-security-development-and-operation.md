---
title: Übersicht über die Sicherheitsentwicklung und-Vorgänge
description: Informationen zu Sicherheitsentwicklung und-Vorgängen in Microsoft 365
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
ms.openlocfilehash: 7c6752b84470eebbdb6ad78c212361156dea957b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506826"
---
# <a name="security-development-and-operations-overview"></a>Übersicht über die Sicherheitsentwicklung und-Vorgänge

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Wie implementiert Microsoft sichere Entwicklungsmethoden?

Der Security Development Lifecycle (SDL) von Microsoft ist ein Sicherheits Assurance-Prozess, der sich mit der Entwicklung und dem Betrieb sicherer Software befasst. Der SDL enthält detaillierte, messbare Sicherheitsanforderungen für Entwickler und Techniker bei Microsoft, um die Anzahl und den Schweregrad von Sicherheitsrisiken in unseren Produkten und Dienstleistungen zu reduzieren. Alle Microsoft-Softwareentwicklungsteams müssen den SDL-Anforderungen entsprechen, und der SDL wird ständig aktualisiert, um die sich ändernde Bedrohungslandschaft, die bewährten bewährten Methoden und die regulatorischen Standards für Compliance widerzuspiegeln.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Wie verbessert Microsoft SDL die Anwendungssicherheit?

Der SDL-Prozess bei Microsoft kann im Hinblick auf fünf Entwicklungsphasen gedacht werden: Anforderungen, Entwurf, Implementierung, Überprüfung und Veröffentlichung. Es beginnt mit der Definition von Softwareanforderungen unter Berücksichtigung der Sicherheit. Dazu stellen wir sicherheitsrelevante Fragen dazu, was die Anwendung leisten muss. Muss die Anwendung vertrauliche Daten sammeln? Wird der Antrag vertrauliche oder wichtige Aufgaben erfüllen? Muss die Anwendung Eingaben aus nicht vertrauenswürdigen Quellen akzeptieren?

Sobald die relevanten Sicherheitsanforderungen identifiziert sind, entwerfen wir unsere Software so, dass sie Sicherheitsfunktionen enthält, die diese Anforderungen erfüllen. Unsere Entwickler implementieren SDL- und Designanforderungen in den Code, den wir durch manuelle Codeüberprüfung, automatisierte Sicherheitstools und Penetrationstests verifizieren. Bevor Code freigegeben werden kann, werden neue Features und wesentliche Änderungen der endgültigen Sicherheit und der Datenschutz Überprüfung unterzogen, um sicherzustellen, dass alle Anforderungen erfüllt werden.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Wie testet Microsoft den Quellcode auf häufige Schwachstellen?

Um unsere Entwickler beim Implementieren von Sicherheitsanforderungen während der Codeentwicklung und nach der Veröffentlichung zu unterstützen, bietet Microsoft eine Reihe sicherer Entwicklungstools, mit denen der Quellcode automatisch auf Sicherheitslücken und -risiken überprüft werden kann. Microsoft definiert und veröffentlicht eine Liste der genehmigten Tools, die für unsere Entwickler verwendet werden sollen, wie Compiler und Entwicklungsumgebungen, zusammen mit den integrierten Sicherheitsüberprüfungen, die automatisch in Microsoft Build-Pipelines ausgeführt werden. Unsere Entwickler verwenden die neuesten Versionen genehmigter Tools, um neue Sicherheitsfeatures nutzen zu können.

Bevor Code in eine Versions Verzweigung eingecheckt werden kann, erfordert der SDL eine manuelle Codeüberprüfung durch einen separaten Prüfer. Codeüberprüfer suchen nach Codierungsfehlern und überprüfen, ob Codeänderungen den SDL- und Konzeptanforderungen entsprechen, ob sie Funktions- und Sicherheitstests bestehen und zuverlässig funktionieren. Außerdem prüfen sie zugeordnete Dokumentationen, Konfigurationen und Abhängigkeiten, um sicherzustellen, dass die Codeänderungen ordnungsgemäß dokumentiert wurden und keine unbeabsichtigten Nebeneffekte zur Folge haben. Wenn ein Überprüfer während der Codeüberprüfung auf Probleme stößt, kann er die einreichende Person auffordern, den Code mit den vorgeschlagenen Änderungen und nach zusätzlichen Tests erneut einzureichen. Codeüberprüfer können die Übernahme des Codes auch gänzlich verhindern, wenn dieser den Anforderungen nicht entspricht. Nachdem der Code vom Prüfer als zufrieden stellend eingestuft wurde, stellt der Prüfer eine Genehmigung bereit, die erforderlich ist, bevor der Code zur nächsten Bereitstellungsphase übergehen kann.

Zusätzlich zu den sicheren Entwicklungstools und der manuellen Codeüberprüfung erzwingt Microsoft SDL-Anforderungen mithilfe von automatisierten Sicherheitstools. Viele dieser Tools sind in die Commit-Pipeline integriert und analysieren Code automatisch bei der eincheckung und beim Kompilieren neuer Builds auf Sicherheitsmängel. Beispiele hierfür sind statische Codeanalysen für allgemeine Sicherheitsmängel und Anmelde Informations Scanner, die Code für eingebettete Schlüssel analysieren. Probleme, die durch automatisierte Sicherheitstools aufgedeckt werden, müssen behoben werden, bevor neue Builds die Sicherheitsüberprüfung übergeben und zur Veröffentlichung genehmigt werden können.

## <a name="how-does-microsoft-manage-open-source-software"></a>Wie verwaltet Microsoft Open-Source-Software?

Microsoft hat eine allgemeine Strategie für die Verwaltung der Open-Source-Sicherheit angenommen, die Tools und Workflows nutzt, die für folgende Zwecke entwickelt wurden:

- Verstehen, welche Open Source-Komponenten in unseren Produkten und Diensten verwendet werden.
- Erfassen, wo und wie diese Komponenten verwendet werden.
- Ermitteln, ob diese Komponenten Sicherheitsrisiken aufweisen.
- Bei ermittelten Sicherheitsrisiken, die sich auf diese Komponenten auswirken, angemessen zu reagieren.

Microsoft-Entwicklungsteams sind für die Sicherheit aller Open Source-Software, die in einem Produkt oder Dienst enthalten ist, verantwortlich. Um dies im großen Maße zu erreichen, hat Microsoft wichtige Funktionen über CG in Entwicklersysteme integriert. Diese automatisieren die Open Source-Erkennung, Arbeitsabläufe für gesetzliche Anforderungen und Warnmeldungen für Komponenten mit Sicherheitsrisiken. Automated CG Tools Scan baut bei Microsoft für Open-Source-Komponenten und zugehörige Sicherheitsrisiken oder rechtliche Verpflichtungen auf. Entdeckte Komponenten werden registriert und den zuständigen Teams für Business-und Security Reviews übermittelt. Diese Überprüfungen sind so ausgelegt, dass sie alle rechtlichen Verpflichtungen oder Sicherheitsrisiken auswerten, die mit Open Source-Komponenten verbunden sind, und diese beheben, bevor sie Komponenten für die Bereitstellung genehmigen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Verordnungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Bestimmungen und Zertifizierungen überprüft. In der folgenden Tabelle erhalten Sie Informationen zur Validierung von Steuerelementen im Zusammenhang mit der Sicherheitsentwicklung und dem Betrieb.

| **Externe Überprüfungen** | **Section** | **Letztes Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | Sa-3: System Entwicklungslebenszyklus | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.2: Änderungs Verwaltungssteuerelemente <br> A. 14.2: Sicherheit in Entwicklungs-und Supportprozessen | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.2: Änderungs Verwaltungssteuerelemente <br> A. 14.2: Sicherheit in Entwicklungs-und Supportprozessen | Februar 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03: Risikomanagement <br> CA-18: Change Management <br> CA-19: Änderungsüberwachung <br> CA-21: Änderungs Tests <br> CA-38: Baseline-Konfigurationen <br> CA-46: Sicherheitsüberprüfung | 30. September 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03: Risikomanagement <br> CA-18: Change Management <br> CA-19: Änderungsüberwachung <br> CA-21: Änderungs Tests <br> CA-38: Baseline-Konfigurationen <br> CA-46: Sicherheitsüberprüfung | 30. September 2019 |

## <a name="resources"></a>Ressourcen

- [Microsoft-Sicherheitsentwicklungszyklus](https://www.microsoft.com/securityengineering/sdl)
