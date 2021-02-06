---
title: Federal Information Processing Standard (FIPS) Publikation 140-2
description: Microsoft bestätigt, dass seine Kryptografiemodule dem US Federal Information Processing Standard entsprechen.
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
ms.openlocfilehash: d7d1f47d7f76f9fc6d3cefa6cac5be807af98cbc
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120834"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>Federal Information Processing Standard (FIPS) Publikation 140-2

## <a name="fips-140-2-standard-overview"></a>FIPS 140-2-Standardübersicht

The Federal Information Processing Standard (FIPS) Publication 140-2 is a U.S. Government standard that defines minimum security requirements for cryptographic modules in information technology products, as defined in Section 5131 of the Information Technology Management Reform Act of 1996.

Das [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP), eine gemeinsame Anstrengung des U.S. National Institute of Standards and Technology (NIST)  und des Canadian Centre for Cyber Security (CCCS), überprüft kryptografische Module auf die Sicherheitsanforderungen für den Kryptografiemodulstandard (d. h. FIPS 140-2) und zugehörige FIPS-Kryptografiestandards. Die FIPS 140-2-Sicherheitsanforderungen umfassen 11 Bereiche im Zusammenhang mit dem Entwurf und der Implementierung eines kryptografischen Moduls. Das NIST Information Technology Labor betreibt ein verwandtes Programm, das die vom FIPS genehmigten kryptografischen Algorithmen im Modul überprüft.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Microsofts Ansatz zur FIPS 140-2-Überprüfung

Microsoft verpflichtet sich aktiv, die 140-2-Anforderungen zu erfüllen, da seit der Einführung des Standards im Jahr 2001 kryptografische Module überprüft wurden. Microsoft überprüft seine kryptografischen Module im Rahmen des Kryptografiemodulüberprüfungsprogramms [(Cryptographic Module Validation Program,](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) CMVP) des National Institute of Standards and Technology (NIST). Mehrere Microsoft-Produkte, einschließlich vieler Clouddienste, verwenden diese kryptografischen Module.

Technische Informationen zu Kryptografiemodulen von Microsoft Windows, zur Sicherheitsrichtlinie für jedes Modul und zum Katalog der CMVP-Zertifikatdetails finden Sie in den Windows- und [Windows Server FIPS 140-2-Inhalten.](https://aka.ms/AA6ehud)

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft Cloud Services im Leistungsumfang

Der aktuelle CMVP FIPS 140-2-Implementierungsleitfaden schließt zwar eine FIPS 140-2-Überprüfung für einen Clouddienst selbst aus. Clouddienstanbieter können fiPS 140-validierte Kryptografiemodule für die Computerelemente abrufen und betreiben, aus denen ihr Clouddienst besteht. Zu den Microsoft-Onlinediensten, die Komponenten enthalten, die von FIPS 140-2 überprüft wurden, gehören u. a.:

- [Azure und Azure Government](/azure/azure-government/documentation-government-plan-security)
- [Dynamics 365 und Dynamics 365 Government](/microsoft-365/compliance/office-365-encryption-in-microsoft-dynamics-365)
- [Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense](/microsoft-365/compliance/office-365-encryption-risks-and-protections)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Was ist der Unterschied zwischen "FIPS 140 Validated" und "FIPS 140 compliant"?**

"FIPS 140 Validated" bedeutet, dass das kryptografische Modul oder ein Produkt, das das Modul einbettet, vom CMVP überprüft ("zertifiziert") wurde, um die FIPS 140-2-Anforderungen zu erfüllen. "FIPS 140-konform" ist ein Branchenbegriff für IT-Produkte, die fips 140 validierte Produkte für Kryptografiefunktionen verwenden.

**Wann führt Microsoft eine FIPS 140-Überprüfung durch?**

Die Schrittfrequenz zum Starten einer Modulüberprüfung richtet sich nach den Funktionsupdates von Windows 10 und Windows Server. Mit der Weiterentwicklung der Softwarebranche werden Betriebssysteme häufiger mit monatlichen Softwareupdates veröffentlicht. Microsoft übernimmt die Überprüfung für Featureversionen, versucht jedoch zwischen den Versionen, die Änderungen an den kryptografischen Modulen zu minimieren.

**Welche Computer sind in einer FIPS 140-Überprüfung enthalten?**

Microsoft überprüft kryptografische Module anhand eines repräsentativen Beispiels von Hardwarekonfigurationen unter Windows 10 und Windows Server. Es ist in der Branche üblich, diese FIPS 140-2-Überprüfung zu akzeptieren, wenn eine Umgebung Hardware verwendet, was den Beispielen für den Überprüfungsprozess ähnelt.

**Auf der NIST-Website sind viele Module aufgeführt. Wo kann ich wissen, welche für meine Agentur gilt?**

Wenn Sie kryptografische Module verwenden müssen, die über FIPS 140-2 überprüft wurden, müssen Sie überprüfen, ob die von Ihnen verwendeten Versionen in der Validierungsliste angezeigt werden. CMVP und Microsoft verwalten eine Liste der überprüften kryptografischen Module, organisiert nach Produktversion, zusammen mit Anweisungen zum Identifizieren, welche Module auf einem Windows-System installiert sind. Weitere Informationen zum Konfigurieren von Systemen für die Konformität finden Sie im Windows- und [Windows Server FIPS 140-2-Inhalt.](https://aka.ms/AA6ehud)

**Was bedeutet "Im FIPS-Modus betrieben" für ein Zertifikat?**

Diese Einschränkung informiert den Leser darüber, dass die erforderlichen Konfigurations- und Sicherheitsregeln eingehalten werden müssen, um das kryptografische Modul auf eine Weise zu verwenden, die mit der FIPS 140-2-Sicherheitsrichtlinie konsistent ist. Jedes Modul verfügt über eine eigene Sicherheitsrichtlinie – eine genaue Spezifikation der Sicherheitsregeln, unter denen es verwendet wird – und verwendet genehmigte Kryptografiealgorithmen, die Verwaltung kryptografischer Schlüssel und Authentifizierungstechniken. Die Sicherheitsregeln werden in der Sicherheitsrichtlinie für jedes Modul definiert. Weitere Informationen, einschließlich Links zur Sicherheitsrichtlinie für jedes Modul, das über das CMVP überprüft wurde, finden Sie in den Windows- und [Windows Server FIPS 140-2-Inhalten.](https://aka.ms/AA6ehud)

**Erfordert FedRAMP FIPS 140-2-Überprüfung?**

Ja, das Federal Risk and Authorization Management Program (FedRAMP) basiert auf Kontrollgrundwerten, die von [NIST SP 800-53 Revision 4](https://nvd.nist.gov/800-53/Rev4/)definiert wurden, einschließlich [SC-13 Cryptographic Protection,](https://nvd.nist.gov/800-53/Rev4/control/SC-13) der die Verwendung von FIPS-validierter Kryptografie oder NSA-genehmigter Kryptografie anfordert.

**Wie unterstützt Microsoft Azure FIPS 140-2?**

Azure wird mit einer Kombination aus Hardware, kommerziellen Betriebssystemen (Linux und Windows) und Azure-spezifischer Version von Windows erstellt. Über den Microsoft [Security Development Lifecycle](https://www.microsoft.com/securityengineering/sdl/) (SDL) verwenden alle Azure-Dienste genehmigte FIPS 140-2-Algorithmen für die Datensicherheit, da das Betriebssystem FIPS 140-2-genehmigte Algorithmen verwendet, während es in einer Cloud mit Hyperskalen arbeitet.

**Kann ich die Einhaltung von FIPS 140-2 durch Microsoft im Zertifizierungsprozess meiner Agentur verwenden?**

Zur Einhaltung von FIPS 140-2 muss Ihr System für die Ausführung in einem vom FIPS genehmigten Betriebsmodus konfiguriert werden. Dies umfasst die Sicherstellung, dass ein kryptografisches Modul nur FIPS-genehmigte Algorithmen verwendet. Weitere Informationen zum Konfigurieren von Systemen für die Konformität finden Sie in den Windows- und [Windows Server FIPS 140-2-Inhalten.](https://aka.ms/AA6ehud)

**Wie ist die Beziehung zwischen FIPS 140-2 und allgemeinen Kriterien?**

Dies sind zwei separate Sicherheitsstandards mit unterschiedlichen, aber ergänzenden Zwecken. FIPS 140-2 wurde speziell für die Validierung von Kryptografiemodulen für Software und Hardware entwickelt, während die allgemeinen Kriterien darauf ausgelegt sind, Sicherheitsfunktionen in IT-Software- und Hardwareprodukten auszuwerten. Allgemeine Kriterienauswertungen beruhen häufig auf FIPS 140-2-Überprüfungen, um zu gewährleisten, dass grundlegende kryptografische Funktionen ordnungsgemäß implementiert werden.

## <a name="resources"></a>Ressourcen

- [FIPS Pub 140-2 Security Requirements for Cryptographic Modules](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [NIST Cryptographic Module Validation Program](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server und FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
