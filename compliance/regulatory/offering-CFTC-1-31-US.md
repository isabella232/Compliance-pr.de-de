---
title: Commodity Futures Trading Commission (CFTC) Rule 1.31(c-d) United States
description: Ein unabhängiges Bewertungsunternehmen hat überprüft, ob Azure und Office 365 Finanzunternehmen dabei helfen können, die Anforderungen der CFTC-Regel 1.31 für die Aufbewahrung von Datensätzen und unveränderliche Speicheranforderungen zu erfüllen.
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
ms.openlocfilehash: 474cd04d98dc91668e48d1999f4fbd91d81523ec
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121754"
---
# <a name="commodity-futures-trading-commission-cftc-rule-131c-d-united-states"></a>Commodity Futures Trading Commission (CFTC) Rule 1.31(c-d) United States

## <a name="about-cftc-rule-13c-d"></a>Informationen zu CFTC Rule 1.3(c-d)

The [Commodity Futures Trading Commission](https://www.cftc.gov/) (CFTC), an independent US federal agency, regulates the commodity futures and options markets and, more recently, the swaps market.  
  
Die langlebige CFTC-Regel 1.31 definiert die Aufbewahrungsanforderungen für Datensätze, die durch die SEC-Regel 17a-4(f) festgelegt wurden. Darüber hinaus wird festgelegt, dass elektronische Aufzeichnungen fünf Jahre lang aufbewahrt werden müssen und dass die Originale während der ersten beiden Jahre "leicht zugänglich" bleiben und während des gesamten Aufbewahrungszeitraums zur Überprüfung durch die Kommission oder das US Department of Sichten zur Verfügung stehen.  
  
Im Jahr 2017 überarbeitete [die CFTC](https://www.cftc.gov/sites/default/files/idc/groups/public/@lrfederalregister/documents/file/2017-11014a.pdf)ihre Regel, überarbeitete und modernisierte ihre Datensatzverordnung, um weniger präskriptive, prinzipienbasierte Standards zu übernehmen, die mehr Flexibilität bei der Aufbewahrung von Datensätzen bieten. Diese Überarbeitung macht die Regel technologieneutraler, sodass regulierte Entitäten die für ihr Unternehmen am besten geeignete Technologie auswählen können und gleichzeitig die Sicherheiten beibehalten, die "die Zuverlässigkeit des Datensatzprozesses sicherstellen". Die überarbeitete Regel entfernt die Anforderung, dass Organisationen die ursprünglichen Datensätze zwei Jahre lang verwalten, behält jedoch den Wartungszeitraum von fünf Jahren bei, wodurch Praktiken für Unternehmen, die sowohl durch die CFTC als auch durch die SEC reguliert werden, entfsprecht.

## <a name="microsoft-and-cftc-rule-131c-d"></a>Microsoft und CFTC Rule 1.31(c-d)

Finanzdienstleister, die eine der am stärksten regulierten Branchen der Welt darstellen, unterliegen komplexen Bestimmungen wie der Aufbewahrung von Finanztransaktionen und verwandter Kommunikation in einem nicht änderbaren und nicht änderbaren Zustand. Eine der am häufigsten festgelegten Bestimmungen ist Regel 1.31 der US Commodity Futures Trading Commission (CFTC), die strenge Anforderungen für regulierte Entitäten vorschreiben, die bücher und Datensätze auf elektronischen Speichermedien beibehalten. Gespeicherte Datensätze müssen manipulationssicher sein, ohne dass sie nach dem festgelegten Aufbewahrungszeitraum geändert oder gelöscht werden können. Microsoft Azure Immutable Blob Storage mit Richtliniensperre und Microsoft Office 365 mit Erhaltungssperre kann Finanzinstituten dabei helfen, die Speicheranforderungen der #A0 1.31(c-d) zu erfüllen.

### <a name="microsoft-azure"></a>Microsoft Azure

Um die #A0 mit #A1 1.31(c-d) zu bewerten, hat Microsoft ein unabhängiges Bewertungsunternehmen, das sich auf Datensatzverwaltung und Informationsverwaltung spezialisiert hat, Cohasset Associates, beibehalten. Im resultierenden Bericht hat [CFTC 1.31 (c)–(d) Compliance Assessment: Microsoft Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports), Cohasset überprüft, ob [Azure Immutable Blob Storage](/azure/storage/blobs/storage-blob-immutable-storage) mit der Richtliniensperrenoption, wenn es verwendet wird, um zeitbasierte Blobs in einem nicht löschbaren und nicht umschreibbaren Format (WORM) zu speichern, die prinzipienbasierten Anforderungen der #A0 erfüllt. Jedes Blob (Datensatz) ist vor Änderung, Überschreiben oder Löschen geschützt, bis der erforderliche Aufbewahrungszeitraum abgelaufen ist und alle zugehörigen gesetzlichen Aufbewahrungsfristen freigegeben wurden. Softwareanbieter und Partner mit vertraulichen Workloads können sich jetzt auf Azure Immutable Blob Storage als One-Stop-Shop-Cloudlösung für die Datensatzaufbewahrung verlassen. Finanzinstitute können jetzt ihre eigenen Anwendungen erstellen, die diese Features nutzen und gleichzeitig konform bleiben.

### <a name="microsoft-365"></a>Microsoft 365

Für [CFTC 1.31(c)-(d)-Anforderungen](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) hat Cohasset überprüft, dass Microsoft 365 Archivierungsfunktionen umfasst, mit denen regulierte Kunden, einschließlich Broker-Händlern, Daten auf eine Weise speichern können, die ihnen hilft, die #A0 für die Datensatzaufbewahrung zu erfüllen. Aufbewahrungsfeatures in Microsoft 365 helfen, eine vielzahl von Daten zu erhalten, einschließlich E-Mail, Voicemail, freigegebene Dokumente, Chatnachrichten und Drittanbieterdaten. Insbesondere die Archivierung in Microsoft 365 ermöglicht Kunden das Festlegen globaler oder differenzierter Aufbewahrungsrichtlinien für Messaging, um Daten für einen definierten Zeitraum und darüber hinaus in einem nicht umschreibbaren, nicht auslöschbaren Format zu speichern.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft Cloud Services im Leistungsumfang

- [Azure](https://aka.ms/AzureCompliance)
- [Office 365](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>Prüfungen, Berichte und Zertifikate

[Azure & CFTC Rule 1.31: SEC 17a-4(f) & CFTC 1.31(c-d) Compliance Assessment of Azure Storage

[Office 365 & CFTC Rule 1.31: Archiving in Office 365, data retention, and SEC Rule 17a-4 compliance

## <a name="how-to-implement"></a>Implementierung

- [Regulierung für Finanzdienstleistungen:](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)Compliancemap wichtiger us-rechtlicher Prinzipien für Cloud Computing und Microsoft-Onlinedienste.
- [Leitfaden für Risikobewertung und Compliance](https://aka.ms/RiskGovernanceGuide): Erstellen Sie ein Governance-Modell für die Risikobewertung von Microsoft-Clouddiensten und die Benachrichtigung der Aufsichtsbehörden.
- [Anwendungsfälle in der Finanzbranche](/azure/industry/financial/): Verwenden Sie Fallübersichten, Lernprogramme und andere Ressourcen, um Azure-Lösungen für Finanzdienstleistungen zu entwickeln.

## <a name="resources"></a>Ressourcen

- [Microsoft Compliance-Programm für Finanzdienstleiter](https://aka.ms/FSCP-Print)
- [Microsoft Clouddienste für Unternehmen und Finanzdienstleistungen](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
- [Finanzdienstleister-Compliance in Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft Office 365-Aufbewahrungsrichtlinien](/office365/securitycompliance/retention-policies)
- [Microsoft Financial Services Blog](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
