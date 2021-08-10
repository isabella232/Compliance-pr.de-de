---
title: Securities and Exchange Commission (SEC) Rule 17a-4(f) United States
description: Ein unabhängiges Bewertungsunternehmen hat überprüft, dass Azure und Office 365 Finanzunternehmen dabei helfen können, DIE SEC-Regel 17a-4(f) für die Aufbewahrung von Datensätzen und unveränderliche Speicheranforderungen zu erfüllen.
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
ms.openlocfilehash: 2c866391c08b4a69db3cb54bdbfbe367007e32ce59207f0d42df0bb29cf98f9f
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54293402"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>Securities and Exchange Commission (SEC) Rule 17a-4(f) United States

## <a name="about-sec-rule-17a-4f"></a>Informationen zu SEC-Regel 17a-4(f)

Die [US Securities and Exchange Commission (SEC)](https://www.sec.gov/) ist eine unabhängige Agentur der US-Regierung und der primären Aufseher und Regulierungsbehörde der US-Amerikanischen Wertpapiermärkte. Sie verfügt über die Durchsetzungsbehörde über die Bundesgesetze, schlägt neue Wertpapierregeln vor und überwacht die Marktbestimmungen der Wertpapierbranche.

Die SEC definiert strenge und explizite Anforderungen für regulierte Entitäten, die entscheiden, Bücher und Aufzeichnungen auf elektronischen Speichermedien aufzubewahren. Es hat [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) und [17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) eingerichtet, um die Datensatzführung, einschließlich Aufbewahrungszeiträumen, für Wertpapierbroker-Händler zu regeln. Später [änderte](https://www.sec.gov/rules/interp/34-47806.htm) die SEC 17 CFR 240.17a-4 Absatz (f) und gibt zwei Interpretationsversionen aus, die ausdrücklich zulassen, dass Bücher und Datensätze auf elektronischen Speichermedien aufbewahrt werden, solange bestimmte Bedingungen erfüllt sind.

Ein elektronisches Speichersystem erfüllt diese Bedingungen, wenn es die Änderung oder Löschung von Datensätzen für den erforderlichen Aufbewahrungszeitraum verhindert. Aufbewahrungszeiträume variieren je nach Datensatztypen zwischen drei und sechs Jahren, wobei die sofortige Barrierefreiheit für die ersten beiden Jahre vorgeschrieben ist. Darüber hinaus erfordert eine der interpretativen Versionen, dass das Speichersystem Datensätze über den von der SEC festgelegten Aufbewahrungszeitraum hinaus aufbewahren kann, um Vorladungen, gesetzliche Aufbewahrungspflicht oder andere solche Anforderungen einzuhalten.

## <a name="microsoft-and-sec-rule-17a-4f"></a>Microsoft- und SEC-Regel 17a-4(f)

Finanzdienstleistungskunden, die eine der am stärksten regulierten Branchen der Welt darstellen, unterliegen komplexen Bestimmungen wie der Aufbewahrung von Finanztransaktionen und der damit verbundenen Kommunikation in einem nicht löschbaren und nicht veränderbaren Zustand. Zu den wichtigsten Bestimmungen zählt Regel 17a-4(f) der US Security and Exchange Commission (SEC), die strenge Anforderungen für regulierte Entitäten festlegt, die entscheiden, Bücher und Aufzeichnungen auf elektronischen Speichermedien aufzubewahren. Gespeicherte Datensätze müssen manipulationssicher sein, ohne dass sie bis nach dem festgelegten Aufbewahrungszeitraum geändert oder gelöscht werden können.

Microsoft Azure Unveränderliche Blob-Storage mit Richtliniensperre und Microsoft Office 365 mit Erhaltungssperre können Finanzinstituten helfen, die unveränderlichen Speicheranforderungen der SEC-Regel 17a-4(f) zu erfüllen.

Um die Compliance von Azure und Office 365 SEC-Regel 17a-4(f) zu bewerten, bewahre Microsoft ein unabhängiges Bewertungsunternehmen, das sich auf die Datensatzverwaltung und Informationsgovernance spezialisiert hat, Cohasset Associates. Im resultierenden Bericht für:

- **Azure**: [SEC 17a-4(f) Compliance Assessment: Microsoft Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports), Cohasset hat überprüft, dass [Azure Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) mit der Option "Richtliniensperre" verwendet wird, wenn es verwendet wird, um zeitbasierte Blobs in einem nicht löschbaren und nicht beschreibbaren (WORM)-Format beizubehalten, die unveränderlichen Speicheranforderungen der SEC-Regel zu erfüllen. Jedes Blob (Datensatz) ist vor Änderungen, Überschreibungen oder Löschungen geschützt, bis der erforderliche Aufbewahrungszeitraum abgelaufen ist und alle zugehörigen rechtlichen Haltebereiche freigegeben wurden. Softwareanbieter und Partner mit vertraulichen Workloads können sich jetzt auf Azure Immutable Blob Storage als Onestop-Shop-Cloudlösung für die Aufbewahrung von Datensätzen und unveränderlichen Speicher verlassen. Finanzinstitute können jetzt ihre eigenen Anwendungen erstellen, die diese Features nutzen und gleichzeitig konform bleiben.
- **Microsoft 365:** Für [SEC 17a-4(f)-Anforderungen](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) hat Cohasset überprüft, dass Microsoft 365 Archivierungsfunktionen umfasst, mit denen regulierte Kunden, einschließlich Broker-Händler, Daten auf eine Weise speichern können, die ihnen hilft, die SEC-Anforderungen für die Datensatzaufbewahrung zu erfüllen. Aufbewahrungsfunktionen in Microsoft 365 dabei helfen, eine vielzahl von Daten zu erhalten, einschließlich E-Mail, Voicemail, freigegebene Dokumente, Chatnachrichten und Daten von Drittanbietern. Insbesondere die Archivierung in Microsoft 365 ermöglicht Es Kunden, globale oder granulare Aufbewahrungsrichtlinien für Messaging festzulegen, um Daten für einen definierten Zeitraum und darüber hinaus in einem nicht umschreibbaren, nicht löschbaren Format zu speichern.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Zu Microsoft gehörende Cloudplattformen und -dienste

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Prüfungen, Berichte und Zertifikate

### <a name="azure--sec-rule-17"></a>Azure & SEC-Regel 17

[SEC 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment of Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC-Regel 17

[SEC 17a-4(f) Compliance Assessment: Microsoft Security & Compliance Center mit SharePoint, OneDrive, Teams, Exchange und Skype for Business](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=2dc92867-5f83-49d8-ad04-9e7295c9e40e&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>Implementierung

### <a name="financial-services-regulation"></a>Regulierung für Finanzdienstleistungen

Compliance-Karte der wichtigsten US-regulatorischen Prinzipien für Cloud Computing und Microsoft-Onlinedienste. [Weitere Informationen](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>Leitfaden zur Risikobewertung & Compliance

Erstellen Sie ein Governancemodell für die Risikobewertung von Microsoft-Clouddiensten und Benachrichtigungen der Regulierungsbehörden. [Weitere Informationen](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>Finanzielle Anwendungsfälle

Verwenden Sie Fallübersichten, Lernprogramme und andere Ressourcen, um Azure-Lösungen für Finanzdienstleistungen zu erstellen. [Weitere Informationen](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Verwenden von Microsoft Compliance-Manager zur Einschätzung des Risikos

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) ist eine Funktion im [Microsoft 365 Compliance Center](/microsoft-365/compliance/microsoft-365-compliance-center), die Ihnen hilft, die Compliance-Position Ihres Unternehmens zu verstehen und Maßnahmen zu ergreifen, um Risiken zu reduzieren. Compliance Manager bietet eine Premiumvorlage für die Erstellung einer Bewertung für diese Verordnung. Suchen Sie die Vorlage auf der Seite **Bewertungsvorlagen** im Compliance Manager. Erfahren Sie, wie Sie [Bewertungen im Compliance-Manager erstellen](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Ressourcen

- [Archivierung in Microsoft Office 365, Datenaufbewahrung und Regel 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
- [Compliance Microsoft Financial Services](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Compliance-Programm Microsoft Business Cloud Services und Finanzdienstleistungen](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Finanzdienstleister-Compliance in Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Azure Financial Services Cloud Risikobewertungstool](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365 Aufbewahrungsrichtlinien](/office365/securitycompliance/retention-policies)
- [Microsoft Financial Services Community](https://techcommunity.microsoft.com/t5/financial-services/ct-p/FinancialServices)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
