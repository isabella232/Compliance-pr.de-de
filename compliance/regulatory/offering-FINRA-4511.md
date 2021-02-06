---
title: Financial Industry Regulatory Authority (FINRA) Rule 4511(c) United States
description: Ein unabhängiges Bewertungsunternehmen hat überprüft, ob Azure und Office 365 Finanzunternehmen dabei helfen können, die Anforderungen an die FINRA-Regel 4511-Datensatzaufbewahrung und unveränderliche Speicherung zu erfüllen.
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
ms.openlocfilehash: f4a26a88ca742178d894b5e46d0372d91babba66
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120844"
---
# <a name="financial-industry-regulatory-authority-finra-rule-4511c-united-states"></a>Financial Industry Regulatory Authority (FINRA) Rule 4511(c) United States

## <a name="about-finra-rule-4511"></a>Informationen zu FINRA Rule 4511

Die [Financial Industry Regulatory Authority (FINRA)](https://www.finra.org/#/) ist die größte unabhängige Stelle, die Wertpapierunternehmen mit der Aufsicht über mehr als 4.500 Brokerunternehmen in den USA beaufsichtigung. Sie wurde vom US-Amerikanischen Kongress autorisiert, "um die amerikanischen Investoren zu schützen, indem sie dafür sorgt, dass die Broker-Händler-Branche fair und ehrlich arbeitet".

Im Jahr 2011 genehmigte die US Security and Exchange Commission (SEC) die FINRA-Einführung von SEC-Regeln, die die Aufbewahrung von Büchern und Datensätzen auf elektronischen Speichermedien regeln. [Die #A0 4511(c)](https://www.finra.org/sites/default/files/NoticeDocument/p123548.pdf) gibt an, dass "alle Bücher und Aufzeichnungen, die gemäß den #A1 vorgenommen werden müssen, in einem Format und in einem Medium aufbewahrt werden, das der SEA (Securities Exchange Act)-Regel 17a-4 entspricht".

Außerdem schreibt die #A0 4511(c) vor, dass Unternehmen die Bücher und Datensätze, für die gemäß den geltenden FINRA- oder #A1 kein festgelegter Aufbewahrungszeitraum festgelegt ist, mindestens sechs Jahre lang beibehalten müssen. Wenn sich die Bücher und Datensätze auf ein Konto bezieht, ist der Aufbewahrungszeitraum auf sechs Jahre nach Kontoschließung vererbbar. Andernfalls beträgt der Aufbewahrungszeitraum sechs Jahre, nachdem solche Bücher und Datensätze erstellt wurden.

## <a name="microsoft-and-finra-rule-4511c"></a>Microsoft und #A0 4511(c)

Finanzdienstleister, die eine der am stärksten regulierten Branchen der Welt darstellen, unterliegen komplexen Bestimmungen wie der Aufbewahrung von Finanztransaktionen und verwandter Kommunikation in einem nicht änderbaren und nicht änderbaren Zustand. Dazu gehört Regel 4511 der Financial Industry Regulatory Authority (FINRA), die strenge Anforderungen für regulierte Entitäten vor sieht, die bücher und Datensätze auf elektronischen Speichermedien beibehalten. Gespeicherte Datensätze müssen manipulationssicher sein, ohne dass sie nach dem festgelegten Aufbewahrungszeitraum geändert oder gelöscht werden können.

Microsoft Azure Immutable Blob Storage mit Richtliniensperre und Microsoft Office 365 mit Erhaltungssperre kann Finanzinstituten dabei helfen, die unveränderlichen Speicheranforderungen der #A0 4511(c) zu erfüllen.

## <a name="microsoft-azure"></a>Microsoft Azure

Um die #A0 mit der #A1 4511(c) zu bewerten, hat Microsoft ein unabhängiges Bewertungsunternehmen, das sich auf Datensatzverwaltung und Informationssteuerung spezialisiert hat, Cohasset Associates, beibehalten. Der resultierende Bericht, [SEC 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment: Microsoft Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports), umfasst die & mit der FINRA-Regel 4511(c), die auf das Format und die Medienanforderungen der #A1 17a-4(f) zurück stellt.

Cohasset hat überprüft, dass [Azure Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) mit der Richtliniensperrenoption, wenn es zum Beibehalten zeitbasierter Blobs in einem nicht löschbaren und nicht umschreibbaren (WORM)-Format verwendet wird, die relevanten FINRA-Speicheranforderungen erfüllt. Jedes Blob (Datensatz) ist vor Änderung, Überschreiben oder Löschen geschützt, bis der erforderliche Aufbewahrungszeitraum abgelaufen ist und alle zugehörigen gesetzlichen Aufbewahrungsaufbewahrungen freigegeben wurden.

Softwareanbieter und Partner mit vertraulichen Workloads können sich jetzt auf Azure Immutable Blob Storage als One-Stop-Shop-Cloudlösung für die Datensatzaufbewahrung und den unveränderlichen Speicher verlassen. Finanzinstitute können jetzt ihre eigenen Anwendungen erstellen, die diese Features nutzen und gleichzeitig konform bleiben.

## <a name="microsoft-365"></a>Microsoft 365

Für [#A0 4511(c)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) hat Cohasset überprüft, dass Microsoft 365 Archivierungsfeatures enthält, mit denen regulierte Kunden, einschließlich Broker-Händlern, Daten so speichern können, dass sie die #A1 für die Datensatzaufbewahrung einhalten können. Aufbewahrungsfeatures in Microsoft 365 helfen, eine vielzahl von Daten zu erhalten, einschließlich E-Mail, Voicemail, freigegebene Dokumente, Chatnachrichten und Drittanbieterdaten. Insbesondere mit der Archivierung in Microsoft 365 können Kunden globale oder differenzierte Aufbewahrungsrichtlinien für Messaging festlegen, um Daten für einen definierten Zeitraum und darüber hinaus in einem nicht umschreibbaren, nicht auslöschbaren Format zu speichern.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft Cloud Services im Leistungsumfang

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Prüfungen, Berichte und Zertifikate

### <a name="azure--finra-rule-4511c"></a>Azure & FINRA Rule 4511(c)

[SEC 17a-4(f) & CFTC 1.31 (c-d) & von Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--finra-rule-4511c"></a>Office 365 & FINRA Rule 4511(c)

[Archivierung in Office 365, Datenaufbewahrung und Einhaltung der SecS-Regel 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)

## <a name="how-to-implement"></a>Implementierung

- **Regulierung für Finanzdienstleistungen:** Compliancemap wichtiger us-rechtlicher Prinzipien für Cloud Computing und Microsoft-Onlinedienste. [Weitere Informationen](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- **Leitfaden für Risikobewertung und Compliance**: Erstellen Sie ein Governance-Modell für die Risikobewertung von Microsoft-Clouddiensten und die Benachrichtigung der Aufsichtsbehörden. [Weitere Informationen](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- **Anwendungsfälle in der Finanzbranche**: Verwenden Sie Fallübersichten, Lernprogramme und andere Ressourcen, um Azure-Lösungen für Finanzdienstleistungen zu entwickeln. [Weitere Informationen](/azure/industry/financial/)

## <a name="resources"></a>Ressourcen

- [Microsoft Compliance-Programm für Finanzdienstleiter](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Microsoft Clouddienste für Unternehmen und Finanzdienstleistungen](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Finanzdienstleister-Compliance in Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Azure Financial Services Cloud Risikobewertungstool](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365-Aufbewahrungsrichtlinien](/office365/securitycompliance/retention-policies)
- [Microsoft Financial Services Blog](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
