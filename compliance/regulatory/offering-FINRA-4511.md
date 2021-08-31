---
title: Financial Industry Regulatory Authority (FINRA) Rule 4511(c) United States
description: Ein unabhängiges Bewertungsunternehmen hat überprüft, dass Azure und Office 365 Finanzunternehmen dabei helfen können, DIE FINRA-Regel 4511 für die Aufbewahrung von Datensätzen und unveränderliche Speicheranforderungen zu erfüllen.
keywords: Microsoft 365, Compliance, Angebote
ms.localizationpriority: medium
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
ms.openlocfilehash: addcf3852fda46989e75b18bd323d86aa1981d4e
ms.sourcegitcommit: 70efe7749db2c6dd4ae0faa8ac22da6e87109c79
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/30/2021
ms.locfileid: "58707144"
---
# <a name="financial-industry-regulatory-authority-finra-rule-4511c-united-states"></a>Financial Industry Regulatory Authority (FINRA) Rule 4511(c) United States

## <a name="about-finra-rule-4511"></a>Informationen zur FINRA-Regel 4511

Die [Financial Industry Regulatory Authority (FINRA)](https://www.finra.org/#/) ist die größte unabhängige Stelle für Wertpapierunternehmen mit Aufsicht über mehr als 4.500 Wertpapierunternehmen in den USA. Sie wurde vom US-Amerikanischen Industrieunternehmen autorisiert, "um die Amerikanischen Behörden zu schützen, indem sichergestellt wurde, dass die Broker-Händler-Branche fair und redlich arbeitet."

Im Jahr 2011 genehmigte die US Security and Exchange Commission (SEC) die FINRA-Einführung von SEC-Regeln zur Aufbewahrung von Büchern und Aufzeichnungen auf elektronischen Speichermedien. [FINRA-Regel 4511(c)](https://www.finra.org/sites/default/files/NoticeDocument/p123548.pdf) legt fest, dass "alle Bücher und Aufzeichnungen, die gemäß den FINRA-Regeln erstellt werden müssen, in einem Format und Medien aufbewahrt werden, die der SEA-Regel 17a-4 (Securities Exchange Act) entsprechen."

Darüber hinaus schreibt FINRA-Regel 4511(c) vor, dass Unternehmen diese Bücher und Aufzeichnungen, für die gemäß den geltenden FINRA- oder SEA-Regeln kein aufbewahrungszeitraum gilt, für einen Zeitraum von mindestens sechs Jahren aufbewahren müssen. Wenn sich die Bücher und Datensätze auf ein Konto beziehen, ist der Aufbewahrungszeitraum auf sechs Jahre nach dem Schließen des Kontos festgelegt. Andernfalls beträgt der Aufbewahrungszeitraum sechs Jahre, nachdem solche Bücher und Datensätze erstellt wurden.

## <a name="microsoft-and-finra-rule-4511c"></a>Microsoft und FINRA-Regel 4511(c)

Finanzdienstleistungskunden, die eine der am stärksten regulierten Branchen der Welt darstellen, unterliegen komplexen Bestimmungen wie der Aufbewahrung von Finanztransaktionen und der damit verbundenen Kommunikation in einem nicht löschbaren und nicht veränderbaren Zustand. Darunter ist Regel 4511 der Finanzaufsichtsbehörde (FINANCIAL Industry Regulatory Authority, FINRA), die strenge Anforderungen für regulierte Entitäten festlegt, die entscheiden, Bücher und Aufzeichnungen auf elektronischen Speichermedien aufzubewahren. Gespeicherte Datensätze müssen manipulationssicher sein, ohne dass sie bis nach dem festgelegten Aufbewahrungszeitraum geändert oder gelöscht werden können.

Microsoft Azure Unveränderliche Blob-Storage mit Richtliniensperre und Microsoft Office 365 mit Erhaltungssperre können Finanzinstituten helfen, die unveränderlichen Speicheranforderungen der FINRA-Regel 4511(c) zu erfüllen.

## <a name="microsoft-azure"></a>Microsoft Azure

Um die Compliance von Azure mit FINRA-Regel 4511(c) zu bewerten, bewahre Microsoft ein unabhängiges Bewertungsunternehmen, das sich auf datensatzverwaltung und Informationsgovernance spezialisiert hat, Cohasset Associates. Der resultierende Bericht [SEC 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment: Microsoft Azure Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)umfasst azure compliance with FINRA Rule 4511(c), die den Format- und Medienanforderungen der SEC-Regel 17a-4(f) entspricht.

Cohasset hat überprüft, dass [Azure Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) mit der Option "Richtliniensperre" verwendet wird, wenn es verwendet wird, um zeitbasierte Blobs in einem nicht löschbaren und nicht beschreibbaren (WORM)-Format beizubehalten, die relevanten FINRA-Speicheranforderungen erfüllt. Jedes Blob (Datensatz) ist vor Änderungen, Überschreibungen oder Löschungen geschützt, bis der erforderliche Aufbewahrungszeitraum abgelaufen ist und alle zugehörigen rechtlichen Haltebereiche freigegeben wurden.

Softwareanbieter und Partner mit vertraulichen Workloads können sich jetzt auf Azure Immutable Blob Storage als zentrale Cloudlösung für die Aufbewahrung von Datensätzen und unveränderlichen Speicher verlassen. Finanzinstitute können jetzt ihre eigenen Anwendungen erstellen, die diese Features nutzen und gleichzeitig konform bleiben.

## <a name="microsoft-365"></a>Microsoft 365

Für anforderungen der [FINRA-Regel 4511(c)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) hat Cohasset überprüft, dass Microsoft 365 Archivierungsfunktionen umfasst, mit denen regulierte Kunden, einschließlich Broker-Händler, Daten auf eine Weise speichern können, die ihnen hilft, die SEC-Anforderungen für die Datensatzaufbewahrung einzuhalten. Aufbewahrungsfunktionen in Microsoft 365 dabei helfen, eine vielzahl von Daten zu erhalten, einschließlich E-Mail, Voicemail, freigegebene Dokumente, Chatnachrichten und Daten von Drittanbietern. Insbesondere die Archivierung in Microsoft 365 ermöglicht Es Kunden, globale oder granulare Aufbewahrungsrichtlinien für Messaging festzulegen, um Daten für einen definierten Zeitraum und darüber hinaus in einem nicht umschreibbaren, nicht löschbaren Format zu speichern.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>In Microsoft eingeschlossene Cloudplattformen und -Dienste

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Prüfungen, Berichte und Zertifikate

### <a name="azure--finra-rule-4511c"></a>Azure & FINRA-Regel 4511(c)

- [SEC 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment of Azure Storage](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)

### <a name="office-365--finra-rule-4511c"></a>Office 365 & FINRA-Regel 4511(c)

[Archivierung in Office 365, Datenaufbewahrung und SEC-Regel 17a-4 Compliance](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)

## <a name="how-to-implement"></a>Implementierung

- **Regulierung für Finanzdienstleistungen:** Compliance-Karte wichtiger US-regulatorischer Prinzipien für Cloud Computing und Microsoft-Onlinedienste. [Weitere Informationen](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- **Leitfaden für Risikobewertung und Compliance**: Erstellen Sie ein Governance-Modell für die Risikobewertung von Microsoft Cloud Services und die Benachrichtigung der Aufsichtsbehörden. [Weitere Informationen](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- **Anwendungsfälle in der Finanzbranche**: Verwenden Sie Fallübersichten, Lernprogramme und andere Ressourcen, um Azure-Lösungen für Finanzdienstleistungen zu entwickeln. [Weitere Informationen](/azure/industry/financial/)

## <a name="resources"></a>Ressourcen

- [Microsoft Compliance-Programm für Finanzdienstleiter](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Microsoft Clouddienste für Unternehmen und Finanzdienstleistungen](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Finanzdienstleister-Compliance in Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Azure Financial Services Cloud Risikobewertungstool](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365 Aufbewahrungsrichtlinien](/office365/securitycompliance/retention-policies)
- [Microsoft Financial Services Blog](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
