---
title: Securities and Exchange Commission – Regulation Systems Compliance and Integrity (SCI)
description: Die Regeln für den Informationsaustausch gelten für SCI-Entitäten, zu denen solche selbstaufsichtsbehörden Organisationen (Self-Regulatory Organizations, SROs) gehören, z. B. Aktien- und Optionswechsel, registrierte Clearingstellen und alternative Handelssysteme (ATSs).
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
ms.openlocfilehash: 049f0516598209411b0c5ca47eea39140762fd3d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50119874"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>Securities and Exchange Commission: Regulation Systems Compliance and Integrity (SCI)

## <a name="about-regulation-sci"></a>Informationen zur Regulation SCI

Die US Securities and Exchange Commission (SEC) ist eine unabhängige Agentur der US-Regierung und der primären Aufsicht und Regulierungsbehörde der US-Wertpapiermarkt. Sie führt die Durchsetzungsbehörde über bundesgesetzliche Wertpapiergesetze, führt neue Wertpapierregeln durch und beaufsichtigt die Marktbestimmungen der Wertpapierbranche.

Im November 2014 hat die SEC die [Regulation Systems Compliance and Integrity (SCI)](https://www.sec.gov/rules/final/2014/34-73639.pdf) (und Form SCI zum Melden von SCI-Ereignissen) angenommen, um die Technologieinfrastruktur auf den US-Amerikanischen Wertpapiermärkten zu stärken. Die Verordnung dient dazu, die Häufigkeit von Systemausfällen zu verringern, die Ausfallsicherheit zu verbessern, wenn solche Vorfälle auftreten, und die Aufsicht der SEC über die Technologie des Wertpapiermarkts und die Durchsetzung ihrer Vorschriften zu erhöhen.

Die Regeln für den Informationsaustausch gelten für SCI-Entitäten, zu denen solche selbstaufsichtsbehörden Organisationen (Self-Regulatory Organizations, SROs) gehören, z. B. Aktien- und Optionswechsel, registrierte Clearingstellen und alternative Handelssysteme (ATSs). Die Regeln regeln in erster Linie die Systeme, die wichtige Funktionen des Wertpapiermarkts direkt unterstützen: Handel, Freigabe und Abrechnung, Auftragsrouting, Marktdaten, Marktbestimmungen und Marktüberwachung.

## <a name="microsoft-and-sec-regulation-sci"></a>Microsoft und SEC Regulation SCI

Die US Securities and Exchange Commission (SEC) hat die Verordnung SCI zur Verstärkung der Technologieinfrastruktur der Finanzorganisationen angenommen, die die us-amerikanischen Wertpapiermarkt betreiben und unterstützen. Unter aufsicht der SEC sind die Anforderungen so konzipiert, dass diese Systeme über hohe Verfügbarkeit, hohe Resilienz und geringe Latenz (große Anzahl von Nachrichten mit geringer Verzögerung) verfügen.

Microsoft hat den Microsoft Azure SEC Regulation Systems Compliance [and Integrity Cloud Implementation Guide](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)veröffentlicht, um Kunden von FINANZDIENSTLEISTUNGEN in den USA zu unterstützen, die diese Verordnung einhalten müssen. Die Anleitungen in diesem Dokument:

- Bietet eine Übersicht über die gesamten Azure-Funktionen, die eine hohe Ausfallsicherheit, hohe Verfügbarkeit und geringe Latenz unterstützen.
- Macht klar, auf welche Kontrollbereiche und regulatorischen Aspekte Azure zugreift. Diese Punkt-für-Punkt-Zuordnung von Azure-Features und -Diensten zu SCI-Anforderungen misst die Compliance von Azure im Einklang mit dem regulatorischen Framework. Es hilft Kunden auch zu verstehen, wo sie Sicherheitsaufgaben auf Azure übertragen können, die sie bei der lokalen Nutzung vollständig hatten. Diese Funktionen werden durch die Zusagen von Microsoft in Azure SLAs unterstützt.
- Gibt jede Anforderung an, die der Kunde erfüllen muss, und bietet Azure-Dokumentationen und -Dienste an, die ihm dabei helfen, diese Verantwortlichkeiten zu erfüllen.

Dieses Dokument enthält eine sorgfältige Checkliste wichtiger Sci-Focus-Bereiche der Verordnung. Diese Prüfliste hilft Finanzorganisationen zu verstehen, wie sie Azure übernehmen können, um ihren Regulierungsbehörden, Kunden und Führungskräften zu gewährleisten, dass sie die geltenden behördlichen Anforderungen einhalten können.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft Cloud Services im Leistungsumfang

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>Implementierung

- [Leitfaden zur Sci-Compliance-Implementierung:](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)Ordnet die Funktionen von Azure der Verordnung zu und gibt Details zur gemeinsamen Verantwortung für die Einhaltung von Vorschriften an.
- [Entwerfen zuverlässiger Azure-Anwendungen:](/azure/architecture/resiliency/)Eine kurze Übersicht darüber, wie Sie Zuverlässigkeit in jeden Schritt des Azure-Anwendungsentwurfs einplanen.
- [Entwerfen von Hochverf](/azure/storage/common/storage-designing-ha-apps-with-ragrs)hrungsanwendungen: Wie Entwickler sicherstellen können, dass ihre Azure -Speicheranwendungen hoch verfügbar sind.
- [Leitfaden für Risikobewertung und Compliance](https://aka.ms/RiskGovernanceGuide): Erstellen Sie ein Governance-Modell für die Risikobewertung von Microsoft-Clouddiensten und die Benachrichtigung der Aufsichtsbehörden.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Was bedeutet gemeinsame Verantwortung bei der Verwendung von Cloudtechnologie?**

Wenn Computerumgebungen von lokalen Rechenzentren in die Cloud umziehen, verschiebt sich auch die Verantwortung für die Sicherheit– clouddienstanbieter (Cloud Services Provider, CSP) und Kunden teilen sich diese Verantwortung nun. Für jede Anwendung und Lösung hängt der Teil dieser Verantwortung auf den Kunden und wie viel auf dem CSP vom #A0 ab, das ein Kunde bereitgestellt – IaaS, SaaS oder PaaS. Der Kunde muss wissen, in welchem Maß er für die Implementierung der erforderlichen Sicherheitskontrollen zur Rechenschaft gezogen wird. Microsoft bietet jedoch Anleitungen, mit deren Hilfe Kunden durch diese komplexe Dynamische navigieren können. Weitere Informationen finden Sie unter ["Gemeinsame Verantwortlichkeiten für Cloud Computing".](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91)

**Welche Finanzinstitute können Azure nutzen, um die Anforderungen der Sci-In-Verordnung zu erfüllen?**

Finanzorganisationen oder SCI-Entitäten, die dieser Verordnung unterliegen, können Azure bereitstellen. Die SEC gibt an, dass ihre Verordnung für "selbstaufsichtliche Organisationen (Self-Regulatory Organizations, SROs) gilt, einschließlich Aktien- und Optionsaustausch, registrierter Clearingstellen, FINRA und MSRB, alternativer Handelssysteme (ATSs), die NMS- und Nicht-NMS-Aktien handeln, die die angegebenen Volumenschwellenwerte überschreiten, Disseminatoren konsolidierter Marktdaten (Planverarbeiter) und bestimmte ausgenommene Clearingstellen."

## <a name="resources"></a>Ressourcen

- [Antworten der SEC auf häufig gestellte Fragen zur Vorschrift SCI](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [Geschäftskontinuität und Notfallwiederherstellung (BCDR): Azure Paired Regions](/azure/best-practices-availability-paired-regions)
- [Compliance Map of Cloud Computing Regulatory Principles and Microsoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Microsoft Cloud Financial Services Compliance Program](https://aka.ms/FSCP-Print)
- [Financial Services Compliance in Azure](https://aka.ms/FinServ-Compliance-Azure)
- [Microsoft Financial Services](https://aka.ms/FinServ-Compliance)
- [Microsoft und sec Rule 17a-4](offering-SEC-17a-4.md)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
