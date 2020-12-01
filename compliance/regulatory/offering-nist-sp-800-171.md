---
title: NIST SP 800-171
description: Microsoft-Cloud-Dienste entsprechen den NIST-SP 800-171-Richtlinien, um kontrollierte nicht klassifizierte Informationen (CUI) in nicht föderalen Informationssystemen zu schützen.
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
ms.openlocfilehash: 071bbbb24110b9d74aa75580d9a23628041455a6
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506966"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>Informationen zu NIST SP 800-171

Das US National Institute of Standards and Technology (NIST) fördert und unterhält Mess Standards und Richtlinien, die zum Schutz der Informations-und Informationssysteme von Bundesbehörden beitragen. Als Reaktion auf den Executive Order 13556 zum Verwalten von kontrollierten nicht klassifizierten Informationen (CUI) veröffentlicht er [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final), um *kontrollierte nicht klassifizierte Informationen in nicht föderalen Informationssystemen und Organisationen zu schützen*. Cui wird als digitale und physische Information definiert, die von einer Regierung (oder einer Entität in Ihrem Namen) erstellt wurde, die zwar nicht klassifiziert, aber noch vertraulich ist und Schutz erfordert.

NIST SP 800-171 wurde ursprünglich im Juni 2015 veröffentlicht und wurde seitdem mehrmals als Reaktion auf die Entwicklung von Bedrohungen aktualisiert. Sie enthält Richtlinien für die sichere Zugänglichkeit, Übertragung und Speicherung von Cui in nicht föderalen Informationssystemen und Organisationen. die Anforderungen fallen in vier Hauptkategorien:

- Steuerelemente und Prozesse für die Verwaltung und den Schutz
- Überwachung und Verwaltung von IT-Systemen
- Clear Practices and Procedures for End Users
- Implementierung technischer und physikalischer Sicherheitsmaßnahmen

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft und NIST SP 800-171

Akkreditierte Drittanbieter-Assessment-Organisationen, Kratos Secureinfo und Coalfire, die mit Microsoft zusammenarbeiten, um zu bestätigen, dass die in-Scope-Cloud-Dienste die Kriterien in NIST SP 800-171 erfüllen und *kontrollierte nicht klassifizierte Informationen (CUI) in nicht föderalen Informationssystemen und Organisationen schützen*, wenn Sie Cui verarbeiten. Die [Microsoft-Implementierung von FedRAMP](offering-fedramp.md) -Anforderungen stellt sicher, dass Microsoft-bezogene Cloud-Dienste die Anforderungen von NIST SP 800-171 mit den vorhandenen Systemen und Vorgehensweisen erfüllen oder übertreffen.

NIST SP 800-171-Anforderungen sind eine Teilmenge von NIST SP 800-53, dem Standard, den FedRAMP verwendet. Anhang D von NIST SP 800-171 stellt eine direkte Zuordnung seiner Cui-Sicherheitsanforderungen zu den relevanten Sicherheitskontrollen in NIST SP 800-53 dar, für die die in-Scope-Cloud-Dienste bereits im Rahmen des FedRAMP-Programms geprüft und autorisiert wurden.

Jede Entität, die die US-Regierung Cui verarbeitet oder speichert – Forschungseinrichtungen, Beratungsunternehmen, Fertigungsunternehmen – muss den strengen Anforderungen von NIST SP 800-171 entsprechen. Diese Bestätigung bedeutet, dass Microsoft-basierte Cloud-Dienste Kunden bei der Bereitstellung von Cui-Arbeitsauslastungen mit der Gewissheit unterstützen können, dass Microsoft die vollständige Compliance vorsieht. Beispielsweise erfüllen alle DoD-Auftragnehmer, die "abgedeckte Verteidigungsinformationen" mit in-Scope-Microsoft Cloud-Diensten in ihren Informationssystemen verarbeiten, speichern oder übertragen, die DFARS-Klauseln des US-Verteidigungsministeriums, die die Einhaltung der Sicherheitsanforderungen von NIST SP 800-171 erfordern.

## <a name="microsoft-in-scope-cloud-services"></a>Eingeschlossene Microsoft-Clouddienste

- [Azure-Regierung](https://aka.ms/AzureCompliance)
- [Dynamics 365 U.S. Government](https://aka.ms/d365-compliance-list)
- Intune
- [Office 365 US Government Community Cloud (gcc), Office 365 gcc High und DoD](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>Prüfungen, Berichte und Zertifikate

- [Azure Government Testat of Compliance with NIST SP 800-171](https://aka.ms/Azure-NIST-800-171)

## <a name="how-to-implement"></a>Implementierung

- [Azure Blueprint-Beispiele](https://docs.microsoft.com/azure/governance/blueprints/samples/): erhalten Sie Unterstützung für die Implementierung von Arbeitsauslastungen, die NIST-basierten Steuerelementen entsprechen.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Kann ich die Microsoft-Konformität mit NIST SP 800-171 für meine Organisation verwenden?**

Ja. Microsoft-Kunden können die überwachten Steuerelemente, die in den Berichten unabhängiger Drittanbieter-Assessment-Organisationen (3PAO) für FedRAMP-Standards beschrieben werden, als Teil ihrer eigenen FedRAMP-und NIST-Risikoanalyse-und Qualifizierungsmaßnahmen verwenden. Diese Berichte bestätigen die Effektivität der Steuerelemente, die von Microsoft in seinen in-Scope-Cloud-Diensten implementiert wurden. Kunden sind dafür verantwortlich sicherzustellen, dass Ihre Cui-Arbeitslasten den NIST-SP-800-171-Richtlinien entsprechen.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Verwenden Sie den Microsoft Compliance-Manager, um Ihr Risiko einzuschätzen

Der [Microsoft Compliance-Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) ist ein Feature im [Microsoft 365 Compliance Center](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center), mit dem Sie die Compliance-Position Ihres Unternehmens verstehen und Maßnahmen zur Risikominderung ergreifen können. Der Compliance Manager bietet eine Premium-Vorlage zum Erstellen einer Bewertung für diese Verordnung. Suchen Sie die Vorlage auf der Seite **Bewertungsvorlagen** im Compliance-Manager. Erfahren Sie, wie Sie [Bewertungen im Compliance-Manager erstellen](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Ressourcen

- [Microsoft DoD-Zertifizierung erfüllt NIST 800-171 Anforderungen](offering-DoD-DISA-L2-L4-L5.md)
- [NIST 800-171 Compliance beginnt mit der Cyber-Dokumentation](https://www.nist800171.com/)
- [FedRAMP-Autorisierungen für Microsoft Cloud Services](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [NIST 800-171 3,3 Audit und Verantwortlichkeit mit Office 365 gcc hoch](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft und das NIST-Cyber-Framework](offering-nist-csf.md)
- [Microsoft Government Cloud](https://www.microsoft.com/enterprise/government)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
