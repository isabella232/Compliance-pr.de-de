---
title: Übersicht über die Sicherheitsentwicklung und -vorgänge
description: Informationen zu Sicherheitsentwicklung und -vorgängen in Microsoft 365
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
hideEdit: true
ms.openlocfilehash: b63c73b54cb16389d071945a8fcf849f8b1d58a9
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497449"
---
# <a name="security-development-and-operations-overview"></a>Übersicht über die Sicherheitsentwicklung und -vorgänge

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Wie implementiert Microsoft sichere Entwicklungspraktiken?

Microsofts Security Development Lifecycle (SDL) ist ein Sicherheitssicherungsprozess, der sich auf die Entwicklung und den Betrieb sicherer Software konzentriert. Der SDL enthält detaillierte, messbare Sicherheitsanforderungen für Entwickler und Techniker bei Microsoft, um die Anzahl und den Schweregrad von Sicherheitsrisiken in unseren Produkten und Dienstleistungen zu reduzieren. Alle Microsoft-Softwareentwicklungsteams müssen den SDL-Anforderungen entsprechen, und wir aktualisieren den SDL kontinuierlich, um die sich ändernde Bedrohungslandschaft, bewährte Methoden in der Branche und gesetzliche Standards für die Compliance wider zuspiegeln.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Wie verbessert Microsoft SDL die Anwendungssicherheit?

Der SDL-Prozess bei Microsoft kann in fünf Phasen der Entwicklung gedacht werden: Anforderungen, Entwurf, Implementierung, Überprüfung und Veröffentlichung. Es beginnt mit der Definition von Softwareanforderungen unter Berücksichtigung der Sicherheit. Dazu stellen wir sicherheitsrelevante Fragen dazu, was die Anwendung leisten muss. Muss die Anwendung vertrauliche Daten sammeln? Wird der Antrag vertrauliche oder wichtige Aufgaben erfüllen? Muss die Anwendung Eingaben aus nicht vertrauenswürdigen Quellen akzeptieren?

Sobald die relevanten Sicherheitsanforderungen identifiziert sind, entwerfen wir unsere Software so, dass sie Sicherheitsfunktionen enthält, die diese Anforderungen erfüllen. Unsere Entwickler implementieren SDL- und Designanforderungen in den Code, den wir durch manuelle Codeüberprüfung, automatisierte Sicherheitstools und Penetrationstests verifizieren. Bevor Code veröffentlicht werden kann, werden neue Features und wesentliche Änderungen schließlich einer abschließenden Sicherheits- und Datenschutzüberprüfung unterzogen, um sicherzustellen, dass alle Anforderungen erfüllt sind.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Wie testiert Microsoft Quellcode auf häufige Sicherheitsrisiken?

Um unsere Entwickler beim Implementieren von Sicherheitsanforderungen während der Codeentwicklung und nach der Veröffentlichung zu unterstützen, bietet Microsoft eine Reihe sicherer Entwicklungstools, mit denen der Quellcode automatisch auf Sicherheitslücken und -risiken überprüft werden kann. Microsoft definiert und veröffentlicht eine Liste der genehmigten Tools für unsere Entwickler, z. B. Compiler und Entwicklungsumgebungen, zusammen mit den integrierten Sicherheitsüberprüfungen, die automatisch in #A0 ausgeführt werden. Unsere Entwickler verwenden die neuesten Versionen genehmigter Tools, um neue Sicherheitsfeatures nutzen zu können.

Bevor Code in einen Veröffentlichungszweig eingecheckt werden kann, erfordert SDL eine manuelle Codeüberprüfung durch einen separaten Prüfer. Codeüberprüfer suchen nach Codierungsfehlern und überprüfen, ob Codeänderungen den SDL- und Konzeptanforderungen entsprechen, ob sie Funktions- und Sicherheitstests bestehen und zuverlässig funktionieren. Außerdem prüfen sie zugeordnete Dokumentationen, Konfigurationen und Abhängigkeiten, um sicherzustellen, dass die Codeänderungen ordnungsgemäß dokumentiert wurden und keine unbeabsichtigten Nebeneffekte zur Folge haben. Wenn ein Überprüfer während der Codeüberprüfung auf Probleme stößt, kann er die einreichende Person auffordern, den Code mit den vorgeschlagenen Änderungen und nach zusätzlichen Tests erneut einzureichen. Codeüberprüfer können die Übernahme des Codes auch gänzlich verhindern, wenn dieser den Anforderungen nicht entspricht. Sobald der Code vom Prüfer als zufriedenstellend eingestuft wurde, stellt der Prüfer die Genehmigung vor, die erforderlich ist, bevor der Code mit der nächsten Bereitstellungsphase fortfahren kann.

Zusätzlich zu sicheren Entwicklungstools und einer manuellen Codeüberprüfung erzwingt Microsoft die SDL-Anforderungen mithilfe automatisierter Sicherheitstools. Viele dieser Tools sind in die Commitpipeline integrierte und analysieren code automatisch auf Sicherheitsfehler, wenn sie eingecheckt und neue Builds kompiliert werden. Beispiele hierfür sind statische Codeanalysen für häufige Sicherheitsfehler und Anmeldeinformationsscanner, die Code für eingebettete Geheimgeheimnisse analysieren. Probleme, die von automatisierten Sicherheitstools aufgedeckt werden, müssen behoben werden, bevor neue Builds die Sicherheitsüberprüfung bestehen und zur Veröffentlichung genehmigt werden können.

## <a name="how-does-microsoft-manage-open-source-software"></a>Wie verwaltet Microsoft Open-Source-Software?

Microsoft hat eine strategie auf hoher Ebene für die Verwaltung der Open-Source-Sicherheit entwickelt, die Tools und Workflows nutzt, die für:

- Verstehen, welche Open Source-Komponenten in unseren Produkten und Diensten verwendet werden.
- Erfassen, wo und wie diese Komponenten verwendet werden.
- Ermitteln, ob diese Komponenten Sicherheitsrisiken aufweisen.
- Bei ermittelten Sicherheitsrisiken, die sich auf diese Komponenten auswirken, angemessen zu reagieren.

Microsoft-Entwicklungsteams sind für die Sicherheit aller Open Source-Software, die in einem Produkt oder Dienst enthalten ist, verantwortlich. Um dies im großen Maße zu erreichen, hat Microsoft wichtige Funktionen über CG in Entwicklersysteme integriert. Diese automatisieren die Open Source-Erkennung, Arbeitsabläufe für gesetzliche Anforderungen und Warnmeldungen für Komponenten mit Sicherheitsrisiken. Automatisierte CG-Tools überprüfen Builds bei Microsoft auf Open-Source-Komponenten und zugehörige Sicherheitsrisiken oder rechtliche Verpflichtungen. Entdeckte Komponenten werden registriert und den zuständigen Teams für Business-und Security Reviews übermittelt. Diese Überprüfungen sind so ausgelegt, dass sie alle rechtlichen Verpflichtungen oder Sicherheitsrisiken auswerten, die mit Open Source-Komponenten verbunden sind, und diese beheben, bevor sie Komponenten für die Bereitstellung genehmigen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Sicherheitsentwicklung und -operation.

| **Externe Prüfungen** | **Section** | **Datum des letzten Berichts** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: Lebenszyklus der Systementwicklung | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Änderungsverwaltungssteuerelemente <br> A.14.2: Sicherheit bei Entwicklungs- und Supportprozessen | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Änderungsverwaltungssteuerelemente <br> A.14.2: Sicherheit bei Entwicklungs- und Supportprozessen | Februar 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Risikomanagement <br> CA-18: Änderungsverwaltung <br> CA-19: Änderungsüberwachung <br> CA-21: Änderungstests <br> CA-38: Basiskonfigurationen <br> CA-46: Sicherheitsüberprüfung | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Risikomanagement <br> CA-18: Änderungsverwaltung <br> CA-19: Änderungsüberwachung <br> CA-21: Änderungstests <br> CA-38: Basiskonfigurationen <br> CA-46: Sicherheitsüberprüfung | 24. Dezember 2020 |

## <a name="resources"></a>Ressourcen

- [Microsofts Sicherheitsentwicklungslebenszyklus](https://www.microsoft.com/securityengineering/sdl)
