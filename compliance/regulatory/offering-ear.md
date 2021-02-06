---
title: US Export Administration Regulations (EAR)
description: Microsoft Cloud Services helfen Kunden, die den US Export Administration Regulations (EAR) unterliegen, ihre Complianceanforderungen zu erfüllen und das Exportkontrollrisiko zu verwalten.
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
ms.openlocfilehash: fbc8166770a3ad2539264bbf76319116a2c306a9
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120004"
---
# <a name="us-export-administration-regulations-ear"></a>US Export Administration Regulations (EAR)

## <a name="about-the-ear"></a>Informationen zum EAR

Das US Department of Commerce setzt die Export Administration Regulations (EAR) über das [Bis (Bureau of Industry and Security) durch.](https://www.bis.doc.gov/) Das EAR regelt und erlegt im Allgemeinen Kontrollen für den Export und den Wiederexport der meisten gewerblichen Waren, Software und Technologien auf, einschließlich "Dual-Use"-Elementen, die sowohl für kommerzielle als auch für verteidigungsorientierte Zwecke sowie für bestimmte Verteidigungselemente verwendet werden können.

Die Richtlinien für das Bis halten fest, dass der Kunde, nicht der Cloudanbieter, der "Exporteur" ist, wenn Daten oder Software in die Cloud hochgeladen oder zwischen Benutzerknoten übertragen werden, der "Exporteur" ist, der dafür verantwortlich ist, sicherzustellen, dass die Übertragung, Speicherung und der Zugriff auf diese Daten oder Software dem EAR entspricht.

[Gemäß der](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)BIS  bezieht sich der Export auf die Übertragung geschützter Technologie- oder technischer Daten an ein fremdes Ziel oder dessen Freigabe an eine fremde Person in den USA (auch als als "export" *bezeichnet).* Das EAR regelt allgemein:

- Exporte aus den USA.
- Exportiert oder übertragt Elemente aus den USA und bestimmte Fremde mit mehr als einem *de-1-Teil* des US-Ursprungsinhalts erneut.
- Übertragungen oder Offenlegungen an Personen aus anderen Ländern.

Elemente, die dem EAR unterliegen, finden Sie in der Commerce Control List (CCL), wo jedem Element eine eindeutige [#A0 (Export Control Classification Number, ECCN) zugewiesen ist.](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn) Elemente, die nicht im CCL aufgeführt sind, sind als EAR99 gekennzeichnet, und die meisten kommerziellen #A0 benötigen keine Lizenz, um exportiert zu werden. Je nach Ziel, Endbenutzer oder Endnutzung des Elements ist jedoch auch für ein EAR99-Element möglicherweise eine BIS-Exportlizenz erforderlich.

In [](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)der endgültigen Regel, die im Juni 2016 veröffentlicht wurde, wurde klargestellt, dass die Lizenzierungsanforderungen für EAR auch nicht für die Übertragung und Speicherung nicht klassifizierter technischer Daten und Software gelten, wenn sie mit FIPS 140-2-validierten Kryptografiemodulen end-to-end verschlüsselt wurden und nicht absichtlich in einem vom Ausland oder in der Russischen Föderation gespeicherten Land gespeichert wurden.

## <a name="microsoft-and-the-ear"></a>Microsoft und das EAR

Microsoft-Technologien, -Produkte und -Dienste unterliegen den US Export Administration Regulations (EAR). Während es keine Compliancezertifizierung für DAS EAR gibt, bieten Microsoft Azure, Microsoft Azure Government und Microsoft Office 365 Government (GCCHigh- und DoD-Umgebungen) wichtige Features und Tools, mit denen berechtigte Kunden, die der EAR unterliegen, Exportsteuerungsrisiken verwalten und ihre Complianceanforderungen erfüllen können.

Das US Commerce Department, das die EAR erzwingt, hat die Position übernommen, dass Kunden, nicht Clouddienstanbieter wie Microsoft, als Exporteur ihrer eigenen Kundendaten angesehen werden. Während die meisten Kundendaten nicht als "Technologie" oder "technische Daten" betrachtet werden, die den EXPORTkontrollen von EAR unterliegen, sind die microsoft-basierten Clouddienste so strukturiert, dass Kunden die potenziellen Exportsteuerungsrisiken, mit der sie verbunden sind, verwalten und erheblich mindern können. Microsoft empfiehlt im Allgemeinen, aber nicht ausschließlich, die Verwendung seiner Government Cloud Services für berechtigte Kunden. Bei entsprechender Planung können Kunden die folgenden Tools und ihre eigenen internen Verfahren verwenden, um die vollständige Einhaltung der US-Exportkontrollen sicherzustellen.

- **Steuerelemente für den Datenspeicherort.** Kunden haben Einblick in den Speicherort ihrer Daten und Haben Zugriff auf robuste Tools, um den Speicher einzuschränken. Sie können daher sicherstellen, dass ihre Daten in den Vereinigten Staaten gespeichert werden, und die Übertragung kontrollierter Technologie oder technischer Daten außerhalb der VEREINIGTEn Staaten minimieren. Darüber hinaus werden Kundendaten nicht an einem nicht konformen Speicherort gespeichert, was mit den Vorschriften von EAR im Einklang steht, wo Daten "absichtlich gespeichert" werden: In keinem der 25 Gruppen-D:5-Länder oder der Russischen Föderation befindet sich kein Azure-Rechenzentrum.
- **End-to-End-Verschlüsselung.** Durch die Nutzung der End-to-End-Verschlüsselung für physische Speicherstandorte, die im EAR angegeben sind, bieten die microsoft-basierten Clouddienste Verschlüsselungsfeatures, die vor Exportsteuerungsrisiken schützen können. Sie bieten Kunden außerdem eine [Vielzahl](https://aka.ms/Azure-Encryption-Overview) von Optionen zum Verschlüsseln von Daten bei der Übertragung und im Ruhestand sowie die Flexibilität, zwischen Verschlüsselungsoptionen zu wählen.
- **Tools und Protokolle, um nicht autorisierten als Export eingestuften Zutritt zu verhindern.** Die Verwendung der Verschlüsselung trägt auch zum Schutz vor einem potenziellen als exportierend eingestuften (oder als erneuten Export eingestuften) #A0 bei, da selbst wenn ein Nicht-US-Benutzer Zugriff auf verschlüsselte Daten hat, nichts aufgedeckt wird, wenn er die Daten während der Verschlüsselung nicht lesen oder verstehen kann. daher gibt es keine "Freigabe" der kontrollierten Daten.

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft Cloud Services im Leistungsumfang

- [Azure und Azure Government](https://aka.ms/AzureCompliance)
- [Office 365 Government (GCC-High und DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>Implementierung

Übersicht über die US-Exportkontrollen und Anleitungen für Kunden, die ihre Verpflichtungen im Rahmen des EAR bewerten.

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Was muss ich tun, um Exportkontrollen bei Verwendung von Microsoft Cloud Services zu erfüllen?**

Wenn daten auf einen Cloudserver wie die Microsoft Cloud hochgeladen werden, gilt der Kunde, der die Daten besitzt , nicht der Clouddienstanbieter, unter dem EAR als Exporteur. Aus diesem Grund muss der Besitzer der Daten – d. h. der Microsoft-Kunde – sorgfältig abschätzen, wie die Nutzung der Microsoft Cloud die Exportsteuerelemente der USA inplizieren kann, und bestimmen, ob die Daten, die sie dort verwenden oder speichern möchten, möglicherweise den EAR-Kontrollen unterliegen und wenn ja, welche Steuerelemente gelten. Erfahren Sie mehr darüber, [wie Azure-](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) und [Office 365-Clouddienste](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) Kunden dabei helfen können, ihre vollständige Compliance mit den US-Exportsteuerelementen sicherzustellen.

**Unterliegen Microsoft-Technologien, -Produkte und -Dienste dem EAR?**

Die meisten Technologien, Produkte und Dienste von Microsoft:

- Unterliegen nicht dem EAR und sind daher nicht in der Liste der Handelssteuerelemente enthalten und verfügen nicht über ECCN;
- Oder sie sind EAR99- oder 5D992-Massenmarkt-berechtigt für die Selbstklassifizierung durch Microsoft und können ohne Lizenz als NlR (No License Required, NLR) in länder ohne Lizenz exportiert werden.

Allerdings wurde einigen Microsoft-Produkten eine ECCN zugewiesen, für die möglicherweise eine Lizenz erforderlich ist. Wenden Sie sich an den EAR oder rechtsberater, um den geeigneten Lizenztyp und die für Exportzwecke berechtigten Länder zu ermitteln.

**Was ist der Unterschied zwischen dem EAR und dem International Traffic in Arms Regulations (ITAR)?**

Die wichtigsten Exportkontrollen in den USA mit der umfassendsten Anwendung sind die EAR, die vom US Department of Commerce verwaltet werden. Das EAR gilt für Dual-Use-Elemente, die sowohl kommerzielle als auch für kommerzielle Anwendungen haben, sowie für Elemente mit rein kommerziellen Anwendungen.

In den USA gibt es auch separate und speziellere Exportkontrollbestimmungen, z. B. die ITAR, die die sensibelsten Elemente und Technologien regelt. Sie werden vom #A0 verwaltet und stellen Kontrollen für den Export, den temporären Import, den erneuten Export und die Übertragung vieler Verteidigungs-, Verteidigungs- und Intelligenceelemente (auch als "Verteidigungsartikel" bezeichnet) fest, einschließlich verwandter technischer Daten.

## <a name="resources"></a>Ressourcen

- [Exportieren von Microsoft-Produkten: Übersicht](https://www.microsoft.com/exporting/overview.aspx)
- [Exportieren von Microsoft-Produkten: Häufig gestellte Fragen](https://www.microsoft.com/exporting/faq.aspx)
- [Exportieren von Microsoft-Produkten: Produkts lookup](https://www.microsoft.com/exporting/exporting-information.aspx)
- [Exporteinschränkungen für Kryptografie](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft und FIPS 140-2](offering-fips-140-2.md)
- [Microsoft und ITAR](offering-itar.md)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
