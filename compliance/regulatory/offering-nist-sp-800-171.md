---
title: NIST SP 800-171
description: Microsoft Cloud Services entsprechen den NIST SP 800-171-Richtlinien zum Schutz kontrollierter nicht klassifizierter Informationen (NIST SP 800-171) in nichtfederalen Informationssystemen.
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
ms.openlocfilehash: 19b312d1b9f31683d775049010d390710554df01
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385665"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>Informationen zu NIST SP 800-171

Das US National Institute of Standards and Technology (NIST) fördert und verwaltet Messstandards und Richtlinien zum Schutz der Informations- und Informationssysteme von Bundesbehörden. Als Reaktion auf die Executive Order 13556 zur Verwaltung kontrollierter nicht klassifizierter Informationen (NIST SP 800-171) zum *Schutz von kontrollierten nicht klassifizierten Informationen in nichtfederalen Informationssystemen und Organisationen* wurde [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final)veröffentlicht. CUI ist als digitale und physische Informationen definiert, die von einer Regierung (oder einer Entität in ihrem Auftrag) erstellt werden, die zwar nicht klassifiziert, aber dennoch vertraulich ist und Schutz erfordert.

NIST SP 800-171 wurde ursprünglich im Juni 2015 veröffentlicht und wurde seitdem als Reaktion auf sich entwickelnde Cyberbedrohungen mehrmals aktualisiert. Es enthält Richtlinien dazu, wie auf CUI sicher zugegriffen, übertragen und in nichtfederischen Informationssystemen und Organisationen gespeichert werden sollte; Die Anforderungen lassen sich in vier Hauptkategorien unterteilen:

- Steuerelemente und Prozesse zum Verwalten und Schützen
- Überwachung und Verwaltung von IT-Systemen
- Klare Methoden und Verfahren für Endbenutzer
- Implementierung technischer und physischer Sicherheitsmaßnahmen

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft und NIST SP 800-171

Akkreditierte Drittanbieterbewertungsorganisationen, Kratos Secureinfo und Coalfire, haben sich mit Microsoft zusammengehörig, um zu bestätigen, dass die zugehörigen Clouddienste die Kriterien in NIST SP 800-171, *Protecting Controlled Unclassified Information (CUI) in nonfederal Information Systems and Organizations,* erfüllen, wenn sie CUI verarbeiten. Die [Microsoft-Implementierung der FedRAMP-Anforderungen](offering-fedramp.md) trägt dazu bei, sicherzustellen, dass die microsoft-in-Scope-Clouddienste die Anforderungen von NIST SP 800-171 mithilfe der bereits eingerichteten Systeme und Praktiken erfüllen oder überschreiten.

NIST SP 800-171-Anforderungen sind eine Teilmenge von NIST SP 800-53, dem von FedRAMP verwendeten Standard. Anhang D von NIST SP 800-171 enthält eine direkte Zuordnung der CUI-Sicherheitsanforderungen zu den relevanten Sicherheitskontrollen in NIST SP 800-53, für die die im Umfang enthaltenen Clouddienste bereits im Rahmen des FedRAMP-Programms bewertet und autorisiert wurden.

Jede Entität, die CUI der US-Regierung verarbeitet oder speichert – Forschungseinrichtungen, Beratungsunternehmen, Auftragnehmer der Fertigung , muss die strengen Anforderungen von NIST SP 800-171 erfüllen. Dieser Nachweis bedeutet, dass Microsoft-Clouddienste im Umfang Kunden, die CUI-Workloads bereitstellen möchten, mit der Gewissheit erfüllen können, dass Microsoft die vollständige Compliance erfüllt. Beispielsweise erfüllen alle DoD-Vertragsnehmer, die "erfasste Verteidigungsinformationen" mithilfe von Microsoft Cloud Services in ihren Informationssystemen verarbeiten, speichern oder übertragen, die DFARS-Klauseln des US-Verteidigungsministeriums, die die Einhaltung der Sicherheitsanforderungen von NIST SP 800-171 erfordern.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft-cloudbasierte Plattformen &-Dienste

- Azure Commercial, Azure Government
- Dynamics 365 U.S. Government
- Intune
- Office 365 US-Government Community Cloud (GCC), Office 365 GCC High und DoD

## <a name="azure-dynamics-365-and-nist-sp-800-171"></a>Azure, Dynamics 365 und NIST SP 800-171

Weitere Informationen zu Azure, Dynamics 365 und anderen Onlinediensten finden Sie im [Azure NIST SP 800-171-Angebot.](/azure/compliance/offerings/offering-nist-800-171)

## <a name="office-365-and-nist-sp-800-171"></a>Office 365 und NIST SP 800-171

### <a name="office-365-cloud-environments"></a>Office 365 Cloudumgebungen

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 Anwendbarkeit und In-Scope-Dienste

Verwenden Sie die folgende Tabelle, um die Anwendbarkeit für Ihre Office 365 Dienste und Abonnements zu ermitteln:

| **Anwendbarkeit** | **In-Scope-Dienste** |
|:------------------|:----------------------|
| **GCC** | Activity Feed Service, Bing Services, Delve, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |
| **GCC High** | Activity Feed Service, Bing Services, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, 
SharePoint Online, Skype for Business, Windows Ink |
| **DoD** | Activity Feed Service, Bing Services, Exchange Online, Intelligent Services, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, Microsoft Teams, SharePoint Online, Skype for Business, Windows Ink |

### <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Kann ich die Microsoft-Compliance mit NIST SP 800-171 für meine Organisation verwenden?**

Ja. Microsoft-Kunden können die in den Berichten von unabhängigen Drittanbieterbewertungsorganisationen (3PAO) beschriebenen auditierten Kontrollen zu FedRAMP-Standards als Teil ihrer eigenen FedRAMP- und NIST-Risikobewertungen und Qualifizierungsaktivitäten verwenden. Diese Berichte belegen die Effektivität der Kontrollen, die Microsoft in seinen cloudbezogenen Diensten implementiert hat. Kunden sind dafür verantwortlich, sicherzustellen, dass ihre CUI-Workloads den NIST SP 800-171-Richtlinien entsprechen.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Verwenden von Microsoft Compliance-Manager zur Einschätzung des Risikos

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) ist eine Funktion im [Microsoft 365 Compliance Center](/microsoft-365/compliance/microsoft-365-compliance-center), die Ihnen hilft, die Compliance-Position Ihres Unternehmens zu verstehen und Maßnahmen zu ergreifen, um Risiken zu reduzieren. Compliance Manager bietet eine Premiumvorlage für die Erstellung einer Bewertung für diese Verordnung. Suchen Sie die Vorlage auf der Seite **Bewertungsvorlagen** im Compliance Manager. Erfahren Sie, wie Sie [Bewertungen im Compliance-Manager erstellen](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Ressourcen

- [Microsoft DoD-Zertifizierung erfüllt NIST 800-171-Anforderungen](offering-DoD-DISA-L2-L4-L5.md)
- [NIST 800-171 Compliance beginnt mit der Cybersicherheitsdokumentation](https://www.nist800171.com/)
- [FedRAMP-Autorisierungen für Microsoft Cloud Services](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [NIST 800-171 3.3 Audit and Accountability with Office 365 GCC High](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft und das NIST Cybersecurity Framework](offering-nist-csf.md)
- [Microsoft Government Cloud](https://www.microsoft.com/enterprise/government)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
