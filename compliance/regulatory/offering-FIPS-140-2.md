---
title: FIPS-Publikation (Federal Information Processing Standard) 140-2
description: Microsoft bestätigt, dass seine kryptografischen Module den US Federal Information Processing Standard (US Federal Information Processing Standard) entsprechen.
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
ms.openlocfilehash: 0e087393901b76a798c4a4ea3bef25fad8dcda84
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947913"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>FIPS-Publikation (Federal Information Processing Standard) 140-2

## <a name="fips-140-2-standard-overview"></a>FIPS 140-2 – Standardübersicht

The Federal Information Processing Standard (FIPS) Publication 140-2 is a U.S. government standard that defines minimum security requirements for cryptographic modules in information technology products, as defined in Section 5131 of the Information Technology Management Reform Act of 1996.

Das [Kryptografiemodulvalidierungsprogramm (Cryptographic Module Validation Program,](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) CMVP), eine gemeinsame Aktion des U.S. National Institute of Standards and Technology (NIST) und des Canadian Centers for Cyber Security (CCPS), überprüft kryptografische Module auf die *Sicherheitsanforderungen für kryptografische Module* (z. B. FIPS 140-2) und verwandte FIPS-Kryptografiestandards. Die FIPS 140-2-Sicherheitsanforderungen umfassen 11 Bereiche im Zusammenhang mit dem Entwurf und der Implementierung eines kryptografischen Moduls. Das NIST Information Technology Labor betreibt ein verwandtes Programm, das die FIPS-genehmigten kryptografischen Algorithmen im Modul überprüft.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Microsoft-Ansatz zur FIPS 140-2-Validierung

Microsoft setzt sich aktiv dafür ein, die 140-2-Anforderungen zu erfüllen, indem kryptografische Module seit der Einführung des Standards im Jahr 2001 validiert wurden. Microsoft überprüft seine kryptografischen Module unter dem National Institute of Standards and Technology (NIST) [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP). Mehrere Microsoft-Produkte, einschließlich vieler Clouddienste, verwenden diese kryptografischen Module.

Technische Informationen zu Microsoft Windows kryptografischen Modulen, die Sicherheitsrichtlinie für jedes Modul und den Katalog mit CMVP-Zertifikatdetails finden Sie im [Windows und Windows Server FIPS 140-2-Inhalt.](https://aka.ms/AA6ehud)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>In Microsoft eingeschlossene Cloudplattformen und -Dienste

Während der aktuelle CMVP FIPS 140-2-Implementierungsleitfaden eine FIPS 140-2-Überprüfung für einen Clouddienst selbst verhindert; Clouddienstanbieter können fips 140-validierte kryptografische Module für die Computerelemente abrufen und betreiben, die ihren Clouddienst umfassen. Zu den Microsoft-Onlinediensten, die Komponenten enthalten, die FIPS 140-2 überprüft wurden, gehören unter anderem:

- Azure und Azure Government
- Dynamics 365 und Dynamics 365 Government
- Office 365, Office 365 U.S. Government und Office 365 U.S. Government Defense

## <a name="azure-dynamics-365-and-fips-140-2"></a>Azure, Dynamics 365 und FIPS 140-2

Weitere Informationen zu Azure, Dynamics 365 und anderen Onlinediensten finden Sie im [Azure FIPS 140-2-Angebot.](/azure/compliance/offerings/offering-fips-140-2)

## <a name="office-365-and-fips-140-2"></a>Office 365 und FIPS 140-2

### <a name="office-365-cloud-environments"></a>Office 365-Cloudumgebungen

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365-Anwendbarkeit und im Leistungsumfang enthaltene Dienste

Verwenden Sie die folgende Tabelle, um die Anwendbarkeit für Ihre Office 365-Dienste und -Abonnements zu bestimmen:

| **Anwendbarkeit** | **Im Leistungsumfang enthaltene Dienste** |
|:------------------|:----------------------|
| Office 365, GCC, GCC High, DoD | Siehe [FIPS 140-2 Validation](/windows/security/threat-protection/fips-140-validation) |

### <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Was ist der Unterschied zwischen "FIPS 140 Validated" und "FIPS 140 compliant"?**

"FIPS 140 Überprüft" bedeutet, dass das kryptografische Modul oder ein Produkt, das das Modul einbettet, vom CMVP als erfüllt die FIPS 140-2-Anforderungen überprüft ('zertifiziert'). "FIPS 140-kompatibel" ist ein Branchenbegriff für IT-Produkte, die fips 140 überprüfte Produkte für kryptografische Funktionen verwenden.

**Wann führt Microsoft eine FIPS 140-Überprüfung durch?**

Der Rhythmus zum Starten einer Modulüberprüfung richtet sich nach den Funktionsupdates von Windows 10 und Windows Server. Während sich die Softwarebranche weiterentwickelt hat, werden Betriebssysteme häufiger veröffentlicht, mit monatlichen Softwareupdates. Microsoft führt eine Überprüfung für Featureversionen durch, versucht jedoch zwischen den Versionen, die Änderungen an den kryptografischen Modulen zu minimieren.

**Welche Computer sind in einer FIPS 140-Überprüfung enthalten?**

Microsoft überprüft kryptografische Module anhand eines repräsentativen Beispiels von Hardwarekonfigurationen, die Windows 10 und Windows Server ausgeführt werden. Es ist in der Branche üblich, diese FIPS 140-2-Überprüfung zu akzeptieren, wenn eine Umgebung Hardware verwendet, die den Beispielen für den Überprüfungsprozess ähnelt.

**Auf der NIST-Website sind viele Module aufgeführt. Woher weiß ich, welche für meine Agentur gilt?**

Wenn Sie kryptografische Module verwenden müssen, die durch FIPS 140-2 überprüft wurden, müssen Sie überprüfen, ob die verwendete Version in der Überprüfungsliste angezeigt wird. Der CMVP und Microsoft verwalten eine Liste der validierten kryptografischen Module, sortiert nach Produktversion, zusammen mit Anweisungen zur Identifizierung der Module, die auf einem Windows System installiert sind. Weitere Informationen zum Konfigurieren konformer Systeme finden Sie in den [Inhalten Windows und Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**Was bedeutet "Im FIPS-Modus betrieben" für ein Zertifikat?**

Dieser Hinweis informiert den Leser, dass die erforderlichen Konfigurations- und Sicherheitsregeln befolgt werden müssen, um das kryptografische Modul in einer Weise zu verwenden, die mit seiner FIPS 140-2-Sicherheitsrichtlinie übereinstimmt. Jedes Modul verfügt über eine eigene Sicherheitsrichtlinie – eine genaue Spezifikation der Sicherheitsregeln, unter denen es ausgeführt wird – und verwendet genehmigte kryptografische Algorithmen, kryptografische Schlüsselverwaltung und Authentifizierungstechniken. Die Sicherheitsregeln sind in der Sicherheitsrichtlinie für jedes Modul definiert. Weitere Informationen, einschließlich Links zur Sicherheitsrichtlinie für jedes Modul, das über den CMVP überprüft wird, finden Sie im [Windows- und Windows Server FIPS 140-2-Inhalt.](https://aka.ms/AA6ehud)

**Erfordert FedRAMP die FIPS 140-2-Überprüfung?**

Ja, das Federal Risk and Authorization Management Program (FedRAMP) basiert auf Kontrollgrundwerten, die von [der NIST SP 800-53 Revision 4](https://nvd.nist.gov/800-53/Rev4/)definiert sind, einschließlich [SC-13 Cryptographic Protection,](https://nvd.nist.gov/800-53/Rev4/control/SC-13) der die Verwendung von FIPS-validierter Kryptografie oder NSA-genehmigter Kryptografie unterstützt.

**Kann ich die Einhaltung von FIPS 140-2 durch Microsoft im Zertifizierungsprozess meiner Organisation verwenden?**

Um FIPS 140-2 zu erfüllen, muss Ihr System so konfiguriert sein, dass es in einem FIPS-genehmigten Betriebsmodus ausgeführt wird. Dazu gehört auch, sicherzustellen, dass ein kryptografisches Modul nur FIPS-genehmigte Algorithmen verwendet. Weitere Informationen zum Konfigurieren konformer Systeme finden Sie in den [Inhalten Windows und Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**Welche Beziehung besteht zwischen FIPS 140-2 und allgemeinen Kriterien?**

Hierbei handelt es sich um zwei separate Sicherheitsstandards mit unterschiedlichen, aber ergänzenden Zwecken. FIPS 140-2 wurde speziell für die Überprüfung von kryptografischen Software- und Hardwaremodulen entwickelt, während die allgemeinen Kriterien für die Bewertung von Sicherheitsfunktionen in IT-Software- und Hardwareprodukten entwickelt wurden. Allgemeine Kriterienbewertungen basieren häufig auf FIPS 140-2-Validierungen, um sicherzustellen, dass grundlegende kryptografische Funktionen ordnungsgemäß implementiert werden.

### <a name="resources"></a>Ressourcen

- [FIPS Pub 140-2- Sicherheitsanforderungen für kryptografische Module](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [NIST Cryptographic Module Validation Program](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server und FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
