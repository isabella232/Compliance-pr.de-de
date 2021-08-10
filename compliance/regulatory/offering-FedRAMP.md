---
title: FedRAMP (Federal Risk and Authorization Management Program)
description: Microsoft wurde das Us Federal Risk and Authorization Management Program P-ATOs und ATOs gewährt.
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
ms.openlocfilehash: f613e35cfcfa6f15946572901cb0c9f3c7a5fa0407a970ccd3b4e19d8efc138a
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292772"
---
# <a name="federal-risk-and-authorization-management-program-fedramp"></a>FedRAMP (Federal Risk and Authorization Management Program)

## <a name="fedramp-overview"></a>FedRAMP-Übersicht

Das US Federal Risk and Authorization Management Program (FedRAMP) wurde eingerichtet, um einen standardisierten Ansatz für die Bewertung, Überwachung und Autorisierung von Cloud Computing-Produkten und -Diensten gemäß dem Federal Information Security Management Act (FISMA) bereitzustellen und die Einführung sicherer Cloud-Lösungen durch Bundesbehörden zu beschleunigen.

Die Office von Management und Budget erfordert jetzt, dass alle leitenden Bundesbehörden FedRAMP verwenden, um die Sicherheit von Clouddiensten zu überprüfen. (Andere Behörden haben sie auch angenommen, sodass sie auch in anderen Bereichen des öffentlichen Sektor nützlich ist.) Das National Institute of Standards and Technology (NIST) SP 800-53 legt die obligatorischen Standards fest, legt Sicherheitskategorien von Informationssystemen fest – Vertraulichkeit, Integrität und Verfügbarkeit –, um die potenziellen Auswirkungen auf eine Organisation zu bewerten, wenn ihre Informations- und Informationssysteme kompromittiert werden. FedRAMP ist das Programm, das bestätigt, dass ein Clouddienstanbieter (CSP) diese Standards erfüllt.

CSPs, die Dienstleistungen an eine Bundesstelle verkaufen möchten, können drei Wege gehen, um die FedRAMP-Compliance nachzuweisen:

- Verdienen Sie eine vorläufige Betriebsautorität (P-ATO) vom Joint Authorization Board (JAB). Die JAB ist die primäre Governance- und Entscheidungsinstanz für FedRAMP. Vertreter des Verteidigungsministeriums, des Department of Security und der General Services Administration sind im Board tätig. Das Board gewährt CSPs, die die FedRAMP-Compliance nachgewiesen haben, eine P-ATO.
- Erhalten Sie eine Autorität zum Arbeiten (Authority to Operate, ATO) von einer Bundesstelle.
- Oder arbeiten Sie unabhängig daran, ein vom CSP bereitgestelltes Paket zu entwickeln, das die Programmanforderungen erfüllt.

Jeder dieser Pfade erfordert eine strenge technische Überprüfung durch die FedRAMP-Programmverwaltung Office (PMO) und eine Bewertung durch eine unabhängige Drittanbieterorganisation, die vom Programm akkreditiert ist.

FedRAMP-Autorisierungen werden auf drei Auswirkungsstufen basierend auf den NIST-Richtlinien gewährt: niedrig, mittel und hoch. Diese Stufen bewerten die Auswirkungen, die der Verlust der Vertraulichkeit, Integrität oder Verfügbarkeit auf eine Organisation haben könnte – niedrig (begrenzte Auswirkung), mittel (schwerwiegende nachteilige Auswirkung) und hoch (schwerwiegende oder schwerwiegende Auswirkung).

## <a name="microsoft-and-fedramp"></a>Microsoft und FedRAMP

Die Clouddienste von Microsoft, einschließlich Azure Government, Dynamics 365 Government und Office 365 U.S. Government, erfüllen die anspruchsvollen Anforderungen des US Federal Risk and Authorization Management Program (FedRAMP), sodass US-Bundesbehörden von den Kosteneinsparungen und der strengen Sicherheit der Microsoft Cloud profitieren können.

Microsoft Government Cloud Services bieten Kunden aus dem öffentlichen Sektor eine vielzahl von Diensten, die FedRAMP entsprechen, sowie robuste Anleitungen und Implementierungstools, einschließlich des [FedRAMP High-Blueprints,](https://aka.ms/fedrampblueprint)das Kunden dabei hilft, eine reihe von Kernrichtlinien für alle von Azure bereitgestellten Architekturen bereitzustellen, die FedRAMP High-Kontrollen implementieren müssen.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Zu Microsoft gehörende Cloudplattformen und -dienste

- Azure und Azure Government
- [Dynamics 365 U.S. Government](https://aka.ms/d365-compliance-list)
- Intune
- Office 365 U.S. Government, Office 365 U.S. Government – High, Office 365 U.S. Government Defense
- Power BI-Clouddienst als eigenständiger Dienst oder in einem firmenspezifischen Office 365-Plan oder einer -Anwendungssuite enthalten

## <a name="azure-dynamics-365-and-fedramp"></a>Azure, Dynamics 365 und FedRAMP

Weitere Informationen zu Azure, Dynamics 365 und anderen Onlinediensten finden Sie im [Azure FedRAMP-Angebot.](/azure/compliance/offerings/offering-fedramp)

## <a name="office-365-and-fedramp"></a>Office 365 und FedRAMP

- Office 365 und Office 365 U.S. Government verfügen über eine ATO des US Department of Health and Human Services (DHHS).
- Office 365 Us Government Defense has a P-ATO from the US Defense Information Systems Agency (DISA). Jeder Kunde, der Office 365 U.S. Government Defense bereitstellen möchte, kann die DISA P-ATO verwenden, um eine Agentur-ATO zu generieren, um deren Zustimmung zu dokumentieren.
- Office 365 (Unternehmens- und Geschäftspläne) und Office 365 US-Regierung verfügen über eine FedRAMP-Agentur-ATO auf der Stufe "Moderate Auswirkungen" der DHHS-Office des Generalinspektors. Office 365 U.S. Government war der erste cloudbasierte E-Mail- und Zusammenarbeitsdienst, der diese Autorisierung erhielt.

### <a name="office-365-cloud-environments"></a>Office 365-Cloudumgebungen

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365-Anwendbarkeit und im Leistungsumfang enthaltene Dienste

Verwenden Sie die folgende Tabelle, um die Anwendbarkeit für Ihre Office 365-Dienste und -Abonnements zu bestimmen:

| **Anwendbarkeit** | **Im Leistungsumfang enthaltene Dienste** |
|:------------------|:----------------------|
| **GCC** | Activity Feed Service, Bing Services, Delve, Exchange Online, Exchange Online Protection, Infrastructure, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |
| **GCC Hoch** | Activity Feed Service, Bing Services, Exchange Online, Exchange Online Protection, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |
| **DoD** | Activity Feed Service, Bing Services, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365-Prüfungen, -Berichte und -Zertifikate

Microsoft muss seine Clouddienste jedes Jahr rezertifizieren, um seine P-ATOs und ATOs zu behalten. Dazu muss Microsoft seine Sicherheitskontrollen kontinuierlich überwachen und bewerten und nachweisen, dass die Sicherheit seiner Dienste weiterhin eingehalten wird.

- [FedRAMP-Prüfberichte für Microsoft](https://aka.ms/MicrosoftFedRAMPAuditDocuments)  

### <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Entsprechen Microsoft Cloud Services dem Federal Information Security Management Act (FISMA)?**

FISMA ist das Bundesgesetz, nach dem US-Bundesbehörden und ihre Partner Informationssysteme und -dienste nur von Organisationen beschaffen müssen, die den FISMA-Anforderungen entsprechen. Die meisten Behörden und deren Lieferanten, die angeben, dass sie FISMA-konform sind, beziehen sich darauf, wie sie die vom NIST in special Publication 800-53 rev 4 identifizierten Kontrollen erfüllen. Der FISMA-Prozess (aber nicht die zugrunde liegenden Standards selbst) wurde 2011 durch FedRAMP ersetzt.

**Für wen gilt FedRAMP?**

"FedRAMP ist für Cloudbereitstellungen und Dienstmodelle der Federal Agency auf niedriger und moderater Risikostufe obligatorisch." Jede Bundesstelle, die einen CSP einbinden möchte, muss möglicherweise die FedRAMP-Spezifikationen erfüllen. Darüber hinaus müssen Unternehmen, die Cloudtechnologien in Produkten oder Diensten verwenden, die von der Regierung verwendet werden, möglicherweise eine ATO erhalten.

**Wo startet meine Agentur ihre eigenen Compliance-Anstrengungen?**

Eine Übersicht über die Schritte, die Bundesbehörden ausführen müssen, um FedRAMP erfolgreich zu navigieren und seine Anforderungen zu erfüllen, finden Sie unter ["Autorisiert: Autorisierung](https://www.fedramp.gov/agency-authorization/)der Agentur".

**Kann ich die Microsoft-Compliance im Autorisierungsprozess meiner Organisation verwenden?**

Ja. Sie können die Zertifizierungen von Microsoft Cloud Services als Grundlage für jedes Programm oder jede Initiative verwenden, die eine ATO einer Bundesbehörden erfordert. Sie müssen jedoch Ihre eigenen Autorisierungen für Komponenten außerhalb dieser Dienste erreichen.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Verwenden von Microsoft Compliance-Manager zur Einschätzung des Risikos

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) ist eine Funktion im [Microsoft 365 Compliance Center](/microsoft-365/compliance/microsoft-365-compliance-center), die Ihnen hilft, die Compliance-Position Ihres Unternehmens zu verstehen und Maßnahmen zu ergreifen, um Risiken zu reduzieren. Compliance Manager bietet eine Premiumvorlage für die Erstellung einer Bewertung für diese Verordnung. Suchen Sie die Vorlage auf der Seite **Bewertungsvorlagen** im Compliance Manager. Erfahren Sie, wie Sie [Bewertungen im Compliance-Manager erstellen](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Ressourcen

- [Federal Risk and Authorization Management Program](https://www.fedramp.gov/)
- [FedRAMP Security Assessment Framework](https://www.fedramp.gov/assets/resources/documents/FedRAMP_Security_Assessment_Framework.pdf)
- [Verwalten der Compliance in der Cloud bei Microsoft](https://www.microsoft.com/trustcenter/common-controls-hub)
- [Microsoft Government Cloud](https://go.microsoft.com/fwlink/p/?linkid=2087246)
