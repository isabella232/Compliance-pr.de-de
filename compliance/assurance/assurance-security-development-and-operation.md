---
title: Übersicht über die Sicherheitsentwicklung und den Sicherheitsbetrieb
description: Informationen zur Sicherheitsentwicklung und zum Sicherheitsbetrieb in Microsoft 365
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
ms.openlocfilehash: 062284cb1cb56602bbcc4ba683670bfeb98460db2569bd837eaf748feceaae7d
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292173"
---
# <a name="security-development-and-operations-overview"></a>Übersicht über die Sicherheitsentwicklung und den Sicherheitsbetrieb

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Wie implementiert Microsoft sichere Entwicklungspraktiken?

Der Security Development Lifecycle (SDL) von Microsoft ist ein Prozess zur Gewährleistung der Sicherheit, der sich auf die Entwicklung und den Betrieb sicherer Software konzentriert. Der SDL enthält detaillierte, messbare Sicherheitsanforderungen für Entwickler und Techniker bei Microsoft, um die Anzahl und den Schweregrad von Sicherheitsrisiken in unseren Produkten und Dienstleistungen zu reduzieren. Alle Microsoft-Softwareentwicklungsteams müssen die SDL-Anforderungen einhalten, und wir aktualisieren den SDL kontinuierlich, um der sich ändernden Bedrohungslandschaft, den bewährten Methoden der Branche und gesetzlichen Standards für die Compliance Rechnung zu tragen.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Wie verbessert Microsoft SDL die Anwendungssicherheit?

Der SDL-Prozess bei Microsoft kann in fünf Phasen der Entwicklung betrachtet werden: Anforderungen, Entwurf, Implementierung, Überprüfung und Freigabe. Es beginnt mit der Definition von Softwareanforderungen unter Berücksichtigung der Sicherheit. Um dieses Ziel zu erreichen, stellen wir sicherheitsrelevante Fragen dazu, was die Anwendung leisten muss. Muss die Anwendung vertrauliche Daten sammeln? Wird der Antrag vertrauliche oder wichtige Aufgaben erfüllen? Muss die Anwendung Eingaben aus nicht vertrauenswürdigen Quellen akzeptieren?

Sobald die relevanten Sicherheitsanforderungen identifiziert sind, entwerfen wir unsere Software so, dass sie Sicherheitsfunktionen enthält, die diese Anforderungen erfüllen. Unsere Entwickler implementieren SDL- und Designanforderungen in den Code, den wir durch manuelle Codeüberprüfung, automatisierte Sicherheitstools und Penetrationstests verifizieren. Schließlich werden neue Features und wesentliche Änderungen vor der Veröffentlichung von Code einer abschließenden Sicherheits- und Datenschutzprüfung unterzogen, um sicherzustellen, dass alle Anforderungen erfüllt sind.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Wie teste Microsoft Quellcode auf allgemeine Sicherheitsrisiken?

Um unsere Entwickler beim Implementieren von Sicherheitsanforderungen während der Codeentwicklung und nach der Veröffentlichung zu unterstützen, bietet Microsoft eine Reihe sicherer Entwicklungstools, mit denen der Quellcode automatisch auf Sicherheitslücken und -risiken überprüft werden kann. Microsoft definiert und veröffentlicht eine Liste der genehmigten Tools, die unsere Entwickler verwenden können, z. B. Compiler und Entwicklungsumgebungen, zusammen mit den integrierten Sicherheitsüberprüfungen, die automatisch in Microsoft-Buildpipelines ausgeführt werden. Unsere Entwickler verwenden die neuesten Versionen genehmigter Tools, um neue Sicherheitsfeatures nutzen zu können.

Bevor Code in einen Release Branch eingecheckt werden kann, erfordert der SDL eine manuelle Codeüberprüfung durch einen separaten Prüfer. Codeüberprüfer suchen nach Codierungsfehlern und überprüfen, ob Codeänderungen den SDL- und Konzeptanforderungen entsprechen, ob sie Funktions- und Sicherheitstests bestehen und zuverlässig funktionieren. Außerdem prüfen sie zugeordnete Dokumentationen, Konfigurationen und Abhängigkeiten, um sicherzustellen, dass die Codeänderungen ordnungsgemäß dokumentiert wurden und keine unbeabsichtigten Nebeneffekte zur Folge haben. Wenn ein Überprüfer während der Codeüberprüfung auf Probleme stößt, kann er die einreichende Person auffordern, den Code mit den vorgeschlagenen Änderungen und nach zusätzlichen Tests erneut einzureichen. Codeüberprüfer können die Übernahme des Codes auch gänzlich verhindern, wenn dieser den Anforderungen nicht entspricht. Nachdem der Code vom Prüfer als zufriedenstellend eingestuft wurde, stellt der Prüfer eine Genehmigung bereit, die erforderlich ist, bevor der Code mit der nächsten Bereitstellungsphase fortfahren kann.

Zusätzlich zu sicheren Entwicklungstools und manueller Codeüberprüfung setzt Microsoft SDL-Anforderungen mithilfe automatisierter Sicherheitstools durch. Viele dieser Tools sind in die Commitpipeline integriert und analysieren code automatisch auf Sicherheitsfehler, wenn er eingecheckt wird und neue Builds kompiliert werden. Beispiele hierfür sind statische Codeanalysen für häufige Sicherheitsfehler und Anmeldeinformationsscanner, die Code auf eingebettete geheime Schlüssel analysieren. Probleme, die von automatisierten Sicherheitstools entdeckt werden, müssen behoben werden, bevor neue Builds die Sicherheitsüberprüfung bestehen und für die Veröffentlichung genehmigt werden können.

## <a name="how-does-microsoft-manage-open-source-software"></a>Wie verwaltet Microsoft Open-Source-Software?

Microsoft hat eine allgemeine Strategie für die Verwaltung der Open Source-Sicherheit eingeführt, die Tools und Workflows verwendet, die für Folgendes entwickelt wurden:

- Verstehen, welche Open Source-Komponenten in unseren Produkten und Diensten verwendet werden.
- Erfassen, wo und wie diese Komponenten verwendet werden.
- Ermitteln, ob diese Komponenten Sicherheitsrisiken aufweisen.
- Bei ermittelten Sicherheitsrisiken, die sich auf diese Komponenten auswirken, angemessen zu reagieren.

Microsoft-Entwicklungsteams sind für die Sicherheit aller Open Source-Software, die in einem Produkt oder Dienst enthalten ist, verantwortlich. Um diese Sicherheit im großen Maßstab zu erreichen, hat Microsoft über CG wesentliche Funktionen in Engineering-Systeme integriert, die die Open Source-Erkennung, rechtliche Anforderungsworkflows und Warnungen für anfällige Komponenten automatisieren. Automatisierte CG-Tools überprüfen Builds bei Microsoft auf Open Source-Komponenten und zugehörige Sicherheitsrisiken oder rechtliche Verpflichtungen. Entdeckte Komponenten werden registriert und den zuständigen Teams für Business-und Security Reviews übermittelt. Diese Überprüfungen sind so ausgelegt, dass sie alle rechtlichen Verpflichtungen oder Sicherheitsrisiken auswerten, die mit Open Source-Komponenten verbunden sind, und diese beheben, bevor sie Komponenten für die Bereitstellung genehmigen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Sicherheitsentwicklung und dem Sicherheitsvorgang.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Steuerelemente für die Änderungsverwaltung <br> A.14.2: Sicherheit in Entwicklungs- und Supportprozessen | 2. Dezember 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Steuerelemente für die Änderungsverwaltung <br> A.14.2: Sicherheit in Entwicklungs- und Supportprozessen | 2. Dezember 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | SDL-1: Security Development Lifecycle (SDL)-Methodik <br> SDL-2: Anforderungen an die Sicherheitssteuerung, die in Versionen dokumentiert sind <br> SDL-4: Trennung von Test- und Produktionsumgebungen <br> SDL-6: Schadsoftwarescans bei Quellcodebuilds <br> SDL7: Halbjährliche SDL-Überprüfung | 31. März 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SA-3: Lebenszyklus der Systementwicklung | 24. September 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Steuerelemente für die Änderungsverwaltung <br> A.14.2: Sicherheit in Entwicklungs- und Supportprozessen | 20. April 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Risikomanagement <br> CA-18: Änderungsverwaltung <br> CA-19: Änderungsüberwachung <br> CA-21: Änderungstests <br> CA-38: Basiskonfigurationen <br> CA-46: Sicherheitsüberprüfung | 24. Dezember 2020 |

## <a name="resources"></a>Ressourcen

- [Sicherheitsentwicklungslebenszyklus von Microsoft](https://www.microsoft.com/securityengineering/sdl)
