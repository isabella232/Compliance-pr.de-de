---
title: Securities and Exchange Commission (SEC) Rule 17a-4(f) United States
description: Ein unabhängiges Bewertungsunternehmen hat überprüft, ob Azure und Office 365 Finanzunternehmen dabei helfen können, die Anforderungen der SEC-Regel 17a-4(f) zur Aufbewahrung von Datensätzen und unveränderlichen Speicheranforderungen zu erfüllen.
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
ms.openlocfilehash: f877bbec76cc0d760f2f908975b3818b88551829
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121204"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>Securities and Exchange Commission (SEC) Rule 17a-4(f) United States

## <a name="about-sec-rule-17a-4f"></a>Informationen zur SEC-Regel 17a-4(f)

Die [US Securities and Exchange Commission (SEC)](https://www.sec.gov/) ist eine unabhängige Agentur der US-Regierung und der primären Aufsicht und Regulierungsbehörde der US-Wertpapiermarkt. Sie führt die Durchsetzungsbehörde über bundesgesetzliche Wertpapiergesetze, führt neue Wertpapierregeln durch und beaufsichtigt die Marktbestimmungen der Wertpapierbranche.

Die SEC definiert strenge und explizite Anforderungen für regulierte Entitäten, die bücher und Datensätze auf elektronischen Speichermedien beibehalten. Sie hat [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) und [17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) eingerichtet, um die Aufzeichnung von Wertpapierbrokern, einschließlich Aufbewahrungszeiträumen, zu regeln. Später hat die [SEC](https://www.sec.gov/rules/interp/34-47806.htm) 17 CFR 240.17a-4 Absatz (f) geändert und zwei interpretative Veröffentlichungen ausstellen, um die Aufbewahrung von Büchern und Datensätzen auf elektronischen Speichermedien zu ermöglichen, solange bestimmte Bedingungen erfüllt sind.

Ein elektronisches Speichersystem erfüllt diese Bedingungen, wenn es die Änderung oder Löschung von Datensätzen für den erforderlichen Aufbewahrungszeitraum verhindert. Aufbewahrungszeiträume variieren je nach Datensatztyp zwischen drei und sechs Jahren, mit sofortiger Barrierefreiheit für die ersten beiden Jahre. Darüber hinaus erfordert eine der interpretationsfähigen Veröffentlichungen, dass das Speichersystem in der Lage ist, Datensätze über den vom SEC festgelegten Aufbewahrungszeitraum hinaus zu speichern, um Vorladungen, gesetzliche Aufbewahrungspflichten oder andere derartige Anforderungen zu erfüllen.

## <a name="microsoft-and-sec-rule-17a-4f"></a>Microsoft und sec Rule 17a-4(f)

Finanzdienstleister, die eine der am stärksten regulierten Branchen der Welt darstellen, unterliegen komplexen Bestimmungen wie der Aufbewahrung von Finanztransaktionen und verwandter Kommunikation in einem nicht änderbaren und nicht änderbaren Zustand. Zu den wichtigsten Bestimmungen gehört Regel 17a-4(f) der US Security and Exchange Commission (SEC), die strenge Anforderungen für regulierte Entitäten vorschreiben, die Bücher und Datensätze auf elektronischen Speichermedien beibehalten. Gespeicherte Datensätze müssen manipulationssicher sein, ohne dass sie nach dem festgelegten Aufbewahrungszeitraum geändert oder gelöscht werden können.

Microsoft Azure Immutable Blob Storage mit Richtliniensperre und Microsoft Office 365 mit Erhaltungssperre kann Finanzinstituten dabei helfen, die unveränderlichen Speicheranforderungen der SEC-Regel 17a-4(f) zu erfüllen.

Zur Bewertung der Compliance von Azure und Office 365 mit der SEC-Regel 17a-4(f) hat Microsoft ein unabhängiges Bewertungsunternehmen, cohasset Associates, beibehalten, das sich auf Datensatzverwaltung und Informationsverwaltung spezialisiert hat. Im resultierenden Bericht für:

- **Azure**: [SEC 17a-4(f) Compliance-Bewertung: Microsoft Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports), Cohasset hat überprüft, ob Azure [Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) mit der Richtliniensperrenoption, wenn es verwendet wird, um zeitbasierte Blobs in einem nicht beschreibbaren und nicht beschreibbaren (WORM)-Format zu speichern, den unveränderlichen Speicheranforderungen der SEC-Regel entspricht. Jedes Blob (Datensatz) ist vor Änderung, Überschreiben oder Löschen geschützt, bis der erforderliche Aufbewahrungszeitraum abgelaufen ist und alle zugehörigen gesetzlichen Aufbewahrungsaufbewahrungen freigegeben wurden. Softwareanbieter und Partner mit vertraulichen Workloads können sich jetzt auf Azure Immutable Blob Storage als Eine-Top-Shop-Cloudlösung für die Datensatzaufbewahrung und den unveränderlichen Speicher verlassen. Finanzinstitute können jetzt ihre eigenen Anwendungen erstellen, die diese Features nutzen und gleichzeitig konform bleiben.
- **Microsoft 365**: Für sec [17a-4(f)-Anforderungen](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) hat Cohasset überprüft, dass Microsoft 365 Archivierungsfeatures umfasst, mit denen regulierte Kunden, einschließlich Brokerhändlern, Daten so speichern können, dass sie die Anforderungen der SEC für die Datensatzaufbewahrung erfüllen können. Aufbewahrungsfeatures in Microsoft 365 helfen, eine vielzahl von Daten zu erhalten, einschließlich E-Mail, Voicemail, freigegebene Dokumente, Chatnachrichten und Drittanbieterdaten. Insbesondere mit der Archivierung in Microsoft 365 können Kunden globale oder differenzierte Aufbewahrungsrichtlinien für Messaging festlegen, um Daten für einen definierten Zeitraum und darüber hinaus in einem nicht umschreibbaren, nicht auslöschbaren Format zu speichern.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft Cloud Services im Leistungsumfang

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Prüfungen, Berichte und Zertifikate

### <a name="azure--sec-rule-17"></a>Azure & SEC Rule 17

[SEC 17a-4(f) & CFTC 1.31 (c-d) & von Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC Rule 17

[SEC 17a-4(f) Compliance-Bewertung: Microsoft Security & Compliance Center mit SharePoint, OneDrive, Teams, Exchange und Skype for Business](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>Implementierung

### <a name="financial-services-regulation"></a>Regulierung für Finanzdienstleistungen

Compliancezuordnung wichtiger us-rechtlicher Prinzipien für Cloud Computing und Microsoft-Onlinedienste. [Weitere Informationen](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>Leitfaden zur Risikobewertung & Compliance

Erstellen sie ein Steuerungsmodell für die Risikobewertung von Microsoft Cloud Services und eine Benachrichtigung der Regulierungsbehörde. [Weitere Informationen](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>Finanzielle Verwendungsfälle

Verwenden Sie Fallübersichten, Lernprogramme und andere Ressourcen zum Erstellen von Azure-Lösungen für Finanzdienstleistungen. [Weitere Informationen](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Verwenden Sie den Microsoft Compliance Manager, um Ihr Risiko einzuschätzen

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) ist eine Funktion im [Microsoft 365 Compliance Center, die Ihnen](/microsoft-365/compliance/microsoft-365-compliance-center) hilft, die Compliance-Position Ihres Unternehmens zu verstehen und Maßnahmen zu ergreifen, um Risiken zu reduzieren. Compliance Manager bietet eine Premiumvorlage für die Erstellung einer Bewertung für diese Verordnung. Suchen Sie die Vorlage auf der Seite **Bewertungsvorlagen** im Compliance Manager. Erfahren Sie, wie Sie [Bewertungen in Compliance Manager erstellen](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Ressourcen

- [Archivierung in Microsoft Office 365, Datenaufbewahrung und Regel 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
- [Compliance Microsoft Financial Services](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Complianceprogramm Microsoft Business Cloud Services und Finanzdienstleistungen](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Finanzdienstleister-Compliance in Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Azure Financial Services Cloud Risikobewertungstool](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365-Aufbewahrungsrichtlinien](/office365/securitycompliance/retention-policies)
- [Microsoft Financial Services Community](https://techcommunity.microsoft.com/t5/financial-services/ct-p/FinancialServices)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
