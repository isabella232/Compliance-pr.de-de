---
title: US Export Administration Regulations (EAR)
description: Microsoft Cloud Services helfen Kunden, die den US Export Administration Regulations (EAR) unterliegen, ihre Compliance-Anforderungen zu erfüllen und das Exportkontrollrisiko zu verwalten.
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
ms.openlocfilehash: 859067495b6811b2264ab3a379f305d428771bce
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159093"
---
# <a name="us-export-administration-regulations-ear"></a>US Export Administration Regulations (EAR)

## <a name="about-the-ear"></a>Informationen zum EAR

Das US-Handelsministerium setzt die Export Administration Regulations (EAR) über das [Bureau of Industry and Security (BIS)](https://www.bis.doc.gov/)durch. Das EAR steuert und erzwingt im Wesentlichen Kontrollen für den Export und den Wiederexport der meisten kommerziellen Waren, Software und Technologien, einschließlich "Dual-Use"-Elemente, die sowohl für kommerzielle als auch für behördliche Zwecke und bestimmte Verteidigungselemente verwendet werden können.

Der BIS-Leitfaden sieht vor, dass beim Hochladen von Daten oder Software in die Cloud oder übertragen zwischen Benutzerknoten der Kunde, nicht der Cloudanbieter, der "Exporteur" ist, der dafür verantwortlich ist, sicherzustellen, dass übertragungen, Speicherung und Zugriff auf diese Daten oder Software mit dem EAR konform sind.

[Gemäß der BIS](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)bezieht sich der *Export* auf die Übertragung geschützter Technologien oder technischer Daten an ein fremdes Ziel oder deren Freigabe an eine fremde Person in den Vereinigten Staaten (auch als *Export bezeichnet).* Das EAR gilt allgemein für Folgendes:

- Exporte aus den Vereinigten Staaten.
- Exportiert oder retransfers von US-Ursprungselementen und bestimmten Fremdenursprungselementen mit mehr als einem *teil* des US-Ursprungsinhalts.
- Übertragungen oder Offenlegungen an Personen aus anderen Ländern.

Elemente, die dem EAR unterliegen, finden Sie in der Commerce Control List (CCL), in der jedem Element eine eindeutige [Export Control Classification Number (ECCN)](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn)zugewiesen ist. Elemente, die nicht im CCL aufgeführt sind, sind als EAR99 gekennzeichnet, und die meisten kommerziellen EAR99-Produkte erfordern keine Lizenz, um exportiert zu werden. Je nach Ziel, Endbenutzer oder Endverwendung des Elements kann jedoch auch für ein EAR99-Element eine BIS-Exportlizenz erforderlich sein.

In der im Juni 2016 [veröffentlichten endgültigen Regel](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)wurde erläutert, dass die EAR-Lizenzierungsanforderungen auch nicht für die Übertragung und Speicherung von nicht klassifizierten technischen Daten und Software gelten würden, wenn sie mit fips 140-2-validierten kryptografischen Modulen ende-to-end verschlüsselt und nicht absichtlich in einem Land mit Einem Handelsembargo oder in der Russischen Federation gespeichert wurden.

## <a name="microsoft-and-the-ear"></a>Microsoft und ear

Microsoft-Technologien, -Produkte und -Dienste unterliegen den US Export Administration Regulations (EAR). Obwohl es keine Compliance-Zertifizierung für ear gibt, bieten Microsoft Azure, Microsoft Azure Government und Microsoft Office 365 Government (GCCHigh- und DoD-Umgebungen) wichtige Features und Tools, die berechtigten Kunden, die dem EAR unterliegen, dabei helfen, Exportkontrollrisiken zu verwalten und ihre Complianceanforderungen zu erfüllen.

Die US-Handelsabteilung, die die EAR erzwingt, hat die Position eingenommen, dass Kunden, nicht Clouddienstanbieter wie Microsoft, als Exporteure ihrer eigenen Kundendaten betrachtet werden. Während die meisten Kundendaten nicht als "Technologie" oder "technische Daten" betrachtet werden, die den EAR-Exportkontrollen unterliegen, sind microsoft-bezogene Clouddienste strukturiert, um Kunden dabei zu helfen, die potenziellen Exportkontrollrisiken, mit denen sie konfrontiert sind, zu verwalten und erheblich zu verringern. Microsoft empfiehlt in der Regel, aber nicht ausschließlich, die Nutzung seiner Government Cloud Services für berechtigte Kunden. Bei der entsprechenden Planung können Kunden die folgenden Tools und ihre eigenen internen Verfahren verwenden, um die vollständige Einhaltung der US-Exportkontrollen sicherzustellen.

- **Steuerelemente am Datenspeicherort.** Kunden haben Einblick in den Speicherort ihrer Daten und zugriff auf robuste Tools, um ihren Speicher einzuschränken. Sie können daher sicherstellen, dass ihre Daten in den Vereinigten Staaten gespeichert werden, und die Übertragung kontrollierter Technologien oder technischer Daten außerhalb der VEREINIGTEn Staaten minimieren. Darüber hinaus werden Kundendaten nicht an einem nicht konformen Ort gespeichert, was mit den EAR-Beschränkungen im Einklang steht, in denen Daten "absichtlich gespeichert" werden: Kein Azure-Rechenzentrum befindet sich in einem der 25 Länder der Gruppe D:5 oder in der Russischen Federation.
- **End-to-End-Verschlüsselung**. Durch die Nutzung der End-to-End-Verschlüsselungssicherheit für physische Speicherorte, die im EAR angegeben sind, bieten microsoft-bezogene Clouddienste Verschlüsselungsfunktionen, die zum Schutz vor Exportkontrollrisiken beitragen können. Sie bieten Kunden auch eine [Vielzahl von Optionen zum Verschlüsseln von Daten](https://aka.ms/Azure-Encryption-Overview) während der Übertragung und im Ruhezustand sowie die Flexibilität, zwischen Verschlüsselungsoptionen zu wählen.
- **Tools und Protokolle, um nicht autorisierten Export zu verhindern.** Die Verwendung von Verschlüsselung trägt auch zum Schutz vor einem potenziellen export (oder als reexport betrachtet) im Rahmen des EAR bei, denn selbst wenn eine Nicht-US-Person Zugriff auf verschlüsselte Daten hat, wird nichts offengelegt, wenn sie die Daten während der Verschlüsselung nicht lesen oder verstehen können; daher gibt es keine "Freigabe" von kontrollierten Daten.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>In Microsoft eingeschlossene Cloudplattformen und -Dienste

- [Azure und Azure Government](https://aka.ms/AzureCompliance)
- [Office 365 Government (GCC-Hoch und DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>Implementierung

Übersicht über die US-Exportkontrollen und -anleitungen für Kunden, die ihre Verpflichtungen im Rahmen des EAR bewerten.

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Was sollte ich tun, um exportsteuerelemente bei Verwendung von Microsoft-Clouddiensten einzuhalten?**

Wenn Daten auf einen Cloudserver wie die Microsoft-Cloud hochgeladen werden, gilt unter dem EAR der Kunde, der die Daten besitzt – nicht der Clouddienstanbieter – als Exporteur. Aus diesem Grund muss der Besitzer der Daten – d. h. der Microsoft-Kunde – sorgfältig bewerten, wie sich die Nutzung der Microsoft-Cloud auf EXPORTkontrollen in den USA auswirken kann, und bestimmen, ob die Daten, die er dort verwenden oder speichern möchte, ear-Kontrollen unterliegen können, und falls ja, welche Kontrollen gelten. Erfahren Sie mehr darüber, wie [Azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) und [Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) Clouddienste Kunden dabei helfen können, ihre vollständige Compliance mit den US-Exportsteuerelementen sicherzustellen.

**Unterliegen Microsoft-Technologien, -Produkte und -Dienste dem EAR?**

Die meisten Microsoft-Technologien, -Produkte und -Dienste:

- nicht dem EAR unterliegen und daher nicht in der Liste der Handelssteuerungen enthalten sind und keine ECCN haben;
- Oder sie sind EAR99- oder 5D992-Massenmarkt-berechtigt für die Selbstklassifizierung durch Microsoft und können ohne Lizenz in nicht gesperrte Länder exportiert werden.

Allerdings wurde einigen Microsoft-Produkten ein ECCN zugewiesen, für das möglicherweise eine Lizenz erforderlich ist. Wenden Sie sich an den EAR oder Rechtsberater, um den geeigneten Lizenztyp und die berechtigten Länder für Exportzwecke zu ermitteln.

**Was ist der Unterschied zwischen der EAR- und der International Traffic in Arms Regulations (ITAR)?**

Die wichtigsten US-Exportsteuerelemente mit der umfassendsten Anwendung sind die EAR, die vom US-Handelsministerium verwaltet werden. Das EAR gilt für Dual-Use-Elemente, die sowohl kommerzielle als auch kommerzielle Anwendungen haben, sowie für Elemente mit rein kommerziellen Anwendungen.

Die Vereinigten Staaten verfügen auch über separate und speziellere Exportkontrollbestimmungen, wie z. B. itar, die die vertraulichsten Elemente und Technologien regeln. Verwaltet vom US-Amerikanischen Department of State, erzwingen sie Kontrollen für den Export, den temporären Import, den Erneuten Export und die Übertragung vieler Verteidigungs-, Verteidigungs- und Intelligence-Elemente (auch als "Verteidigungsartikel" bezeichnet), einschließlich verwandter technischer Daten.

## <a name="resources"></a>Ressourcen

- [Exportieren von Microsoft-Produkten: Übersicht](https://www.microsoft.com/exporting/overview.aspx)
- [Exportieren von Microsoft-Produkten: Häufig gestellte Fragen](https://www.microsoft.com/exporting/faq.aspx)
- [Exportieren von Microsoft-Produkten: Produktsuche](https://www.microsoft.com/exporting/exporting-information.aspx)
- [Exportbeschränkungen für Kryptografie](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft und FIPS 140-2](offering-fips-140-2.md)
- [Microsoft und ITAR](offering-itar.md)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
