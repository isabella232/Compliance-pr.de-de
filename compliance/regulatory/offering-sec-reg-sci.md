---
title: Securities and Exchange Commission – Regulation Systems Compliance and Integrity (SCI)
description: Die SCI-Regeln gelten für SCI-Entitäten, die self-regulatory organizations (SROs) wie Aktien- und Optionsaustausche, registrierte Clearingstellen und alternative Handelspartner (ATSs) umfassen.
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
ms.openlocfilehash: 06537749b60f40ab87211aa6efa65e8e88ed691b
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087534"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>Securities and Exchange Commission: Regulation Systems Compliance and Integrity (SCI)

## <a name="about-regulation-sci"></a>Informationen zur Verordnung SCI

Die US Securities and Exchange Commission (SEC) ist eine unabhängige Agentur der US-Regierung und der primären Aufseher und Regulierungsbehörde der US-Amerikanischen Wertpapiermärkte. Sie verfügt über die Durchsetzungsbehörde über die Bundesgesetze, schlägt neue Wertpapierregeln vor und überwacht die Marktbestimmungen der Wertpapierbranche.

Im November 2014 hat die SEC [Regulation Systems Compliance and Integrity (SCI)](https://www.sec.gov/rules/final/2014/34-73639.pdf) (und Form SCI für die Meldung von SCI-Ereignissen) eingeführt, um die Technologieinfrastruktur in den US-Wertpapiermärkten zu stärken. Die Verordnung dient dazu, die Häufigkeit von Systemausfällen zu verringern, die Resilienz zu verbessern, wenn solche Vorfälle auftreten, und die SEC-Aufsicht über die Wertpapiermarkttechnologie und die Durchsetzung ihrer Vorschriften zu erhöhen.

Die SCI-Regeln gelten für SCI-Entitäten, die self-regulatory organizations (SROs) wie Aktien- und Optionsaustausche, registrierte Clearingstellen und alternative Handelspartner (ATSs) umfassen. Die Regeln regeln in erster Linie die Systeme, die wichtige Wertpapiermarktfunktionen direkt unterstützen: Handel, Freigabe und Abrechnung, Auftragsweiterleitung, Marktdaten, Marktvorschriften und Marktüberwachung.

## <a name="microsoft-and-sec-regulation-sci"></a>Microsoft- und SEC-Verordnung SCI

Die US Securities and Exchange Commission (SEC) hat die Sci-Verordnung angenommen, um die Technologieinfrastruktur der Finanzorganisationen zu stärken, die die US-Amerikanischen Wertpapiermärkte betreiben und unterstützen. Unter SEC-Aufsicht sind die Anforderungen darauf ausgelegt, sicherzustellen, dass diese Systeme eine hohe Verfügbarkeit, hohe Resilienz und geringe Latenz (große Anzahl von Nachrichten mit geringer Verzögerung) aufweisen.

Um Kunden von US-Finanzdienstleistungen zu unterstützen, die diese Verordnung einhalten müssen, hat Microsoft den [Microsoft Azure Sec Regulation Systems Compliance and Integrity Cloud Implementation Guide](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)veröffentlicht. Die Anleitung in diesem Dokument:

- Bietet eine Übersicht über die gesamten Azure-Funktionen, die hohe Resilienz, hohe Verfügbarkeit und niedrige Latenz unterstützen.
- Macht deutlich, welche Kontrollbereiche und regulatorischen Aspekte Azure behandelt. Diese Punkt-für-Punkt-Zuordnung von Azure-Features und -Diensten zu SCI-Anforderungen misst die Azure-Compliance mit dem gesetzlichen Rahmen. Es hilft Kunden auch zu verstehen, wo sie sicherheitsbezogene Verantwortlichkeiten auf Azure übertragen können, die sie beim Betrieb vor Ort in vollem Besitz hatten. Diese Funktionen werden durch die Zusagen unterstützt, die Microsoft in Azure SLAs macht.
- Gibt jede SCI-Anforderung der Verordnung an, die in der Verantwortung des Kunden liegt, und bietet Azure-Dokumentationen und -Dienste, die ihnen dabei helfen, diese Zuständigkeiten zu erfüllen.

Dieses Dokument enthält eine ausführliche Checkliste kritischer Sci-Fokusbereiche der Verordnung. Diese Checkliste hilft Finanzorganisationen zu verstehen, wie sie Azure einführen können, um ihren Regulierungsbehörden, Kunden und Führungskräften zu gewährleisten, dass sie die geltenden behördlichen Anforderungen einhalten können.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft-Clouddienste im Leistungsumfang

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>Implementierung

- [Sci-Implementierungsleitfaden](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)für die Verordnung: Karten Azure-Funktionen gegen die Verordnung und details zur gemeinsamen Verantwortung für die Compliance.
- [Entwerfen zuverlässiger Azure-Anwendungen:](/azure/architecture/resiliency/)Eine kurze Übersicht über die Erstellung von Zuverlässigkeit in jedem Schritt des Azure-Anwendungsentwurfs.
- [Entwerfen hochverfügbarer Anwendungen:](/azure/storage/common/storage-designing-ha-apps-with-ragrs)Wie Entwickler sicherstellen können, dass ihre Azure Storage Anwendungen hoch verfügbar sind.
- [Leitfaden für Risikobewertung und Compliance](https://aka.ms/RiskGovernanceGuide): Erstellen Sie ein Governance-Modell für die Risikobewertung von Microsoft Cloud Services und die Benachrichtigung der Aufsichtsbehörden.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Was bedeutet gemeinsame Verantwortung bei der Verwendung der Cloudtechnologie?**

Wenn Computerumgebungen von lokalen Rechenzentren auf die in der Cloud übertragen werden, verschiebt sich auch die Verantwortung für die Sicherheit – der Cloud-Dienstanbieter (CSP) und der Kunde teilen diese Verantwortung nun. Für jede Anwendung und Lösung hängt der Umfang dieser Verantwortung auf den Kunden und der CSP vom Azure-Modell ab, das ein Kunde bereitstellt – IaaS, SaaS oder PaaS. Der Kunde muss wissen, in welchem Maß er für die Implementierung der erforderlichen Sicherheitskontrollen verantwortlich ist. Microsoft bietet jedoch Anleitungen, um Kunden bei der Navigation in dieser komplexen Dynamischen zu unterstützen. Weitere Informationen finden Sie unter ["Gemeinsame Verantwortlichkeiten für Cloud Computing".](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91)

**Welche Finanzinstitute können Azure nutzen, um die Sci-Anforderungen der Verordnung zu erfüllen?**

Finanzorganisationen oder SCI-Entitäten, die dieser Verordnung unterliegen, können Azure bereitstellen. Die SEC gibt an, dass ihre Verordnung für "Selbstaufsichtsbehörden (Self-Regulatory Organizations, SROs) gilt, einschließlich Aktien- und Optionsaustauschen, registrierter Clearingstellen, FINRA und MSRB, alternativer Handelspartner (ATSs), die NMS- und Nicht-NMS-Aktien handeln, die die angegebenen Volumenschwellenwerte überschreiten, Händler konsolidierter Marktdaten (Planverarbeiter) und bestimmte ausgenommene Clearingstellen."

## <a name="resources"></a>Ressourcen

- [Antworten der SEC auf häufig gestellte Fragen zur Verordnung SCI](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [Geschäftskontinuität und Notfallwiederherstellung (BCDR): Gekoppelte Azure-Regionen](/azure/best-practices-availability-paired-regions)
- [Compliance-Karte der regulatorischen Prinzipien von Cloud Computing und Microsoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Microsoft Cloud Financial Services Compliance Program](https://aka.ms/FSCP-Print)
- [Financial Services Compliance in Azure](https://aka.ms/FinServ-Compliance-Azure)
- [Microsoft Financial Services](https://aka.ms/FinServ-Compliance)
- [Microsoft und SEC-Regel 17a-4](offering-SEC-17a-4.md)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
