---
title: NIST SP 800-171
description: Microsoft Cloud Services entsprechen den NIST SP 800-171-Richtlinien zum Schutz von kontrollierten nicht klassifizierten Informationen (CuI) in nicht föderierten Informationssystemen.
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
ms.openlocfilehash: da5e2621969ff9cd4ce2778fa7f075522454aef7
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121114"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>Informationen zu NIST SP 800-171

Das US National Institute of Standards and Technology (NIST) fördert und verwaltet Messstandards und Richtlinien zum Schutz der Informations- und Informationssysteme von Bundesstellen. Als Reaktion auf die Executive Order 13556 zum Verwalten von kontrollierten nicht klassifizierten Informationen (Controlled Unclassified Information, CUI) veröffentlichte sie [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final), *Protecting Controlled Unclassified Information In Nonfederal Information Systems and Organizations*. CUI ist als digitale und physische Informationen definiert, die von einer Regierung (oder einer Entität in ihrem Namen) erstellt werden, die zwar nicht klassifiziert ist, aber dennoch vertraulich ist und Schutz erfordert.

NIST SP 800-171 wurde ursprünglich im Juni 2015 veröffentlicht und seitdem mehrmals als Reaktion auf sich entwickelnde Cyberbedrohungen aktualisiert. Es enthält Richtlinien dazu, wie kui sicher auf nicht föderale Informationssysteme und Organisationen zugegriffen, übertragen und gespeichert werden soll; Die Anforderungen sind in vier Hauptkategorien unterteilt:

- Steuerelemente und Prozesse zum Verwalten und Schützen
- Überwachung und Verwaltung von IT-Systemen
- Klare Methoden und Verfahren für Endbenutzer
- Implementierung von technischen und physischen Sicherheitsmaßnahmen

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft und NIST SP 800-171

Die akkreditierten Bewertungsorganisationen Kratos Secureinfo und Coalfire von Drittanbietern, die mit Microsoft zusammenarbeiten, um zu bestätigen, dass ihre im Umfang basierten Clouddienste die Kriterien in NIST SP 800-171, *Protecting Controlled Unclassified Information (CUI) in* nicht föderalen Informationssystemen und Organisationen, erfüllen, wenn sie CUI verarbeiten. Die Implementierung von [FedRAMP-Anforderungen](offering-fedramp.md) durch Microsoft hilft sicherzustellen, dass microsoft-basierte Clouddienste die Anforderungen von NIST SP 800-171 mit den bereits vorhandenen Systemen und Methoden erfüllen oder überschreiten.

NIST SP 800-171-Anforderungen sind eine Teilmenge von NIST SP 800-53, dem von FedRAMP verwendeten Standard. Anhang D von NIST SP 800-171 enthält eine direkte Zuordnung der CUI-Sicherheitsanforderungen zu den relevanten Sicherheitskontrollen in NIST SP 800-53, für die die im Umfang basierten Clouddienste bereits im Rahmen des FedRAMP-Programms bewertet und autorisiert wurden.

Jede Organisation, die CUI der US-Regierung verarbeitet oder speichert – Forschungseinrichtungen, Beratungsunternehmen, Auftragnehmer im Fertigungsunternehmen – muss die strengen Anforderungen von NIST SP 800-171 erfüllen. Dieser Nachweis bedeutet, dass microsoft-basierte Clouddienste Kunden, die die Bereitstellung von KUI-Workloads in vollem Umfang bereitstellen, mit der Gewissheit aufnehmen können, dass Microsoft die compliancekonform ist. Beispielsweise erfüllen alle DoD-Vertragsnehmer, die "abgedeckte Verteidigungsinformationen" mithilfe von bereichsbasierten Microsoft Cloud Services in ihren Informationssystemen verarbeiten, speichern oder übertragen, die DFARS-Klauseln des US-Verteidigungsministeriums, die die Einhaltung der Sicherheitsanforderungen von NIST SP 800-171 erfordern.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft Cloud Services im Leistungsumfang

- [Azure Government](https://aka.ms/AzureCompliance)
- [Azure Commercial](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)
- [Dynamics 365 U.S. Government](https://aka.ms/d365-compliance-list)
- Intune
- [Office 365 U.S. Government Community Cloud (GCC), Office 365 GCC High und DoD](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>Prüfungen, Berichte und Zertifikate

- [Azure Government Attestation of Compliance mit NIST SP 800-171](https://aka.ms/Azure-NIST-800-171)

## <a name="how-to-implement"></a>Implementierung

- [Azure Blueprint-Beispiele:](/azure/governance/blueprints/samples/)Erhalten Sie Unterstützung für die Implementierung von Workloads, die NIST-basierten Steuerelementen entsprechen.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Kann ich die Microsoft Compliance mit NIST SP 800-171 für meine Organisation verwenden?**

Ja. Kunden von Microsoft können die in den Berichten von unabhängigen Bewertungsorganisationen von Drittanbietern (3PAO) beschriebenen überwachten Kontrollen zu den FedRAMP-Standards im Rahmen ihrer eigenen FedRAMP- und NIST-Risikoanalyse- und Qualifizierungsbemühungen verwenden. Diese Berichte belegen die Effektivität der Steuerelemente, die Microsoft in seinen in-Scope-Cloud-Diensten implementiert hat. Kunden sind dafür verantwortlich sicherzustellen, dass ihre CUI-Workloads den NIST SP 800-171-Richtlinien entsprechen.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Verwenden Sie den Microsoft Compliance Manager, um Ihr Risiko einzuschätzen

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) ist eine Funktion im [Microsoft 365 Compliance Center, die Ihnen](/microsoft-365/compliance/microsoft-365-compliance-center) hilft, die Compliance-Position Ihres Unternehmens zu verstehen und Maßnahmen zu ergreifen, um Risiken zu reduzieren. Compliance Manager bietet eine Premiumvorlage für die Erstellung einer Bewertung für diese Verordnung. Suchen Sie die Vorlage auf der Seite **Bewertungsvorlagen** im Compliance Manager. Erfahren Sie, wie Sie [Bewertungen in Compliance Manager erstellen](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Ressourcen

- [Microsoft -DoD-Zertifizierung erfüllt NIST 800-171-Anforderungen](offering-DoD-DISA-L2-L4-L5.md)
- [NIST 800-171 Compliance beginnt mit der Cybersicherheitsdokumentation](https://www.nist800171.com/)
- [Microsoft Cloud Services – FedRAMP-Autorisierungen](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [NIST 800-171 3.3 Audit and Accountability with Office 365 GCC High](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft und das NIST Cybersecurity Framework](offering-nist-csf.md)
- [Microsoft Government Cloud](https://www.microsoft.com/enterprise/government)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
