---
title: US DoE 10 CFR Part 810
description: Kunden, die den Exportkontrollanforderungen von US DoE 10 CFR Part 810 unterliegen, können Azure Government verwenden.
keywords: Microsoft 365, Compliance, Angebote
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 1a16495f5cfe3e293910ebe84e6af566aea17621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087544"
---
# <a name="us-doe-10-cfr-part-810"></a>US DoE 10 CFR Part 810

## <a name="microsoft-and-doe-10-cfr-part-810"></a>Microsoft und DoE 10 CFR Teil 810

Microsoft Azure Behörden können Kunden, die den Exportkontrollanforderungen des US Department of Energy (DoE) 10 CFR Part 810 unterliegen, durch zwei Autorisierungen unterstützen:

- Die vom Joint Authorization Board (JAB) ausgestellte FedRAMP High Interim Authorization to Operate (P-ATO)
- Die Vorläufigen Genehmigungen der Stufe 4 und 5 des Verteidigungsministeriums (Department of Defense, DoD) Defense Information Systems Agency

FedRAMP bietet einen geeigneten Basisplan, um zu gewährleisten, dass Azure Government Kerninfrastruktur- und Virtualisierungstechnologien und -dienste wie Compute, Speicher und Netzwerk bereitstellt, die mit strengen NIST-Kontrollen konzipiert sind. Diese tragen dazu bei, die Anforderungen an die Trennung von Kundendaten zu erfüllen und sichere Verbindungen mit den lokalen Umgebungen von Kunden zu ermöglichen.

Darüber hinaus ist Azure Government eine COMMUNITY-Cloud der US-Regierung, die physisch von der Azure-Cloud getrennt ist. Es bietet zusätzliche Zusicherungen zu bestimmten Anforderungen der US-Regierung im Hinblick auf hintergrundbezogene Überprüfungen, einschließlich bestimmter Kontrollen, die den Zugriff auf Informationen und Systeme auf überprüfte US-Bürger unter Azure-Betriebspersonal einschränken.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft-Clouddienste im Leistungsumfang

- [Azure Government](https://aka.ms/AzureCompliance)
- Intune

## <a name="how-to-implement"></a>Implementierung

- [NERC CIP Standards & Cloud Computing:](https://aka.ms/AzureNERC)Leitfaden für Stromunternehmen und registrierte Entitäten, die Workloads in Azure oder Azure Government bereitstellen.

## <a name="about-doe-10-cfr-part-810"></a>Informationen zu DoE 10 CFR Part 810

Die Exportkontrollregel [10 CFR Teil 810](https://www.govinfo.gov/content/pkg/FR-2015-02-23/pdf/2015-03479.pdf) des US-Energieministeriums (DoE) regelt den Export von nicht klassifizierter Technologie und Unterstützung. Dadurch wird sichergestellt, dass aus den VEREINIGTEn Staaten exportierte Technologien nur für Zwecke verwendet werden. Der überarbeitete Teil 810 (endgültige Regel) wurde im März 2015 wirksam und wird von der [Nationalen Sicherheitsverwaltung](https://www.energy.gov/nnsa/national-nuclear-security-administration)verwaltet. In Abschnitt 810.6 ist festgelegt, dass eine spezifische DoE-Autorisierung sowohl für Unterstützung und Übertragung sensibler Atomtechnologie erforderlich ist, die "allgemein autorisiert" sind, als auch für Solche, die eine spezifische Autorisierung erfordern (z. B. bei Unterstützung bei sensiblen Technologien wie Anreicherung und Schwer wasserintensiver Produktion).

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Gelten die 10 CFR Part 110-Bestimmungen der US-Amerikanischen Aufsichtsaufsichtsbehörde für Azure Government?**

Nein Die [US Regulatory Regulatory Commission](https://www.nrc.gov/) (NRC) regelt den Export und [Import](https://www.nrc.gov/about-nrc/ip/export-import.html) von Einrichtungen und zugehörigen Geräten und Materialien unter [10 CFR Teil 110.](https://www.nrc.gov/reading-rm/doc-collections/cfr/part110/) Die NRC regelt keine Technologie und Unterstützung im Zusammenhang mit diesen Elementen, die der DoE-Gerichtsbarkeit unterliegen. Daher würden NRC 10 CFR Part 110-Bestimmungen nicht für Azure Government gelten.

**Wie kann ich nachweisen, dass ich DoE 10 CFR Part 810 erfüllt?**

Wenn Ihre Organisation Daten in Azure Government bereitstellt, können Sie sich auf die Azure Government FedRAMP High P-ATO als Nachweis dafür verlassen, dass Sie Daten auf angemessen eingeschränkte Weise behandeln. Sie sind jedoch dafür verantwortlich, die DoE-Autorisierung für Ihre eigenen Systeme zu erhalten, einschließlich der Verwendung von Clouddiensten.

**Was sind meine Zuständigkeiten für die Klassifizierung von Daten, die in Azure Government bereitgestellt werden?**

Kunden, die Daten in Azure Government bereitstellen, sind für ihren eigenen Sicherheitsklassifizierungsprozess verantwortlich. Für Kundendaten, die DoE-Exportkontrollen unterliegen, wird das Klassifizierungssystem durch die Unclassified Controlled Atomic Information (UCNI)-Kontrollen ergänzt, die durch Abschnitt 148 des [US Atomic Energy Act](https://www.epa.gov/laws-regulations/summary-atomic-energy-act)eingerichtet wurden.

## <a name="resources"></a>Ressourcen

- [Azure Cloud Services- und US-Exportsteuerelemente](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- [Microsoft und FedRAMP](offering-fedramp.md)
- [Microsoft und DoD](offering-dod-disa-l2-l4-l5.md)
- [Microsoft Government Cloud](https://www.microsoft.com/enterprise/government)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
