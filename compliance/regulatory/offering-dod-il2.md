---
title: Department of Defense (DoD) Impact Level 2 (IL2)
description: Erfahren Sie, wie Microsoft die Standards der Stufe 2 (Il2) des Verteidigungsministeriums (Department of Defense, DoD) erfüllt.
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
ms.openlocfilehash: c57183a53c563fffa2bb3eb1cedb2fca23db26f4
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947889"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a>Department of Defense (DoD) Impact Level 2 (IL2)

## <a name="dod-il2-overview"></a>Übersicht über DoD IL2

Die Defense Information Systems Agency (DISA) ist eine Agentur des US-Verteidigungsministeriums (DoD), die für die Entwicklung und Verwaltung des DoD Cloud Computing [Security Requirements Guide (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)verantwortlich ist. Die SRG definiert die grundlegenden Sicherheitsanforderungen, die doD verwendet, um den Sicherheitsstatus eines Clouddienstanbieters (CSP) zu bewerten und die Entscheidung zu unterstützen, eine vorläufige DoD-Autorisierung (Pa) zu erteilen, die es einem CSP ermöglicht, DoD-Missionen zu hosten. Es integriert, ersetzt und entfernt das zuvor veröffentlichte DoD Cloud Security Model (CSM) und ist dem DoD Risk Management Framework (RMF) zugeordnet.

DISA leitet DoD-Behörden und -Abteilungen bei der Planung und Autorisierung der Verwendung eines CSP. Darüber hinaus werden CSP-Angebote auf Die Einhaltung der SRG ausgewertet. Dabei handelt es sich um einen Autorisierungsprozess, bei dem CSPs Dokumentationen erstellen können, in denen ihre Einhaltung von DoD-Standards beschrieben wird. Es stellt gegebenenfalls vorläufige Genehmigungen (PAs) für DoD aus, sodass DoD-Behörden und unterstützende Organisationen Clouddienste nutzen können, ohne dass sie selbst einen vollständigen Genehmigungsprozess durchlaufen müssen, was Zeit und Mühe spart.

Im [DoD-CIO-Memo vom 15. Dezember 2014](https://www.esi.mil/contentview.aspx?id=585) zu *aktualisierten Anleitungen zum Erwerb und zur Verwendung kommerzieller Cloud Computing Services* heißt es: "FedRAMP dient als Mindestsicherheitsgrundwert für alle DoD-Clouddienste". Die SRG verwendet den FedRAMP Moderate-Basisplan auf allen Informationsauswirkungsstufen (Information Impact Levels, IL) und berücksichtigt den high Baseline an einigen.

[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* states that IL2 information may be hosted in a CSP that minimal holds a FedRAMP Moderate PA and a DoD Level 2 PA, subject to compliance with the personnel security requirements outlined in Section 5.6.2. Dieser Ansatz verringert jedoch nicht, dass der CSP andere Sicherheits- und Integrationsanforderungen erfüllt, die vom Mission Owner benötigt werden. Gemäß [SRG Section 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2 Location and Separation Requirements* wird DoD IL2 PA angemessen von einer FedRAMP Moderate PA abgedeckt, sodass die Anforderungen für eine IL2 PA nicht zusätzlich bewertet werden.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Zu Microsoft gehörende Cloudplattformen und -dienste

- Azure
- Dynamics 365
- Microsoft Cloud App Security
- Microsoft Defender für Endpunkt
- Microsoft Graph
- Microsoft Intune
- Microsoft Stream
- Office 365 U.S. Government, Office 365 U.S. Government – High
- Power Apps
- Power Automate
- Power BI

## <a name="azure-dynamics-365-and-dod-il2"></a>Azure, Dynamics 365 und DoD IL2

Weitere Informationen zu Azure, Dynamics 365 und anderen Onlinediensten finden Sie im [Azure DoD IL2-Angebot.](/azure/compliance/offerings/offering-dod-il2)

## <a name="office-365-and-dod-il2"></a>Office 365 und DoD IL2

### <a name="office-365-cloud-environments"></a>Office 365-Cloudumgebungen

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365-Anwendbarkeit und im Leistungsumfang enthaltene Dienste

Verwenden Sie die folgende Tabelle, um die Anwendbarkeit für Ihre Office 365-Dienste und -Abonnements zu bestimmen:

| **Anwendbarkeit** | **Im Leistungsumfang enthaltene Dienste** |
|:------------------|:----------------------|
| **GCC** | Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |
| **GCC Hoch** | Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |

### <a name="resources"></a>Ressourcen

- [Microsoft Government-Lösungen](https://www.microsoft.com/enterprise/government)
- [Leitfaden zu den Sicherheitsanforderungen für DoD Cloud Computing](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [FedRAMP-Dokumente](https://www.fedramp.gov/documents/)
- [NIST SP 800-37 Risk](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*
- [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *Sicherheits- und Datenschutzkontrollen für Informationssysteme und Organisationen*
- [DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) für DoD Information Technology (IT)*
