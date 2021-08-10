---
title: Department of Defense (DoD) Impact Level 5 (IL5)
description: Erfahren Sie, wie Microsoft die Standards der Stufe 5 (Il5) des Verteidigungsministeriums (Department of Defense, DoD) erfüllt.
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
ms.openlocfilehash: 539a53888ec859bb3b6942b48288659f73fa4b69807ce19e063cbfe104b7072d
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54294232"
---
# <a name="department-of-defense-dod-impact-level-5-il5"></a>Department of Defense (DoD) Impact Level 5 (IL5)

## <a name="dod-il5-overview"></a>Übersicht über DoD IL5

Die Defense Information Systems Agency (DISA) ist eine Agentur des US-Verteidigungsministeriums (DoD), die für die Entwicklung und Verwaltung des DoD Cloud Computing [Security Requirements Guide (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)verantwortlich ist. Die SRG definiert die grundlegenden Sicherheitsanforderungen, die doD verwendet, um den Sicherheitsstatus eines Clouddienstanbieters (CSP) zu bewerten und die Entscheidung zu unterstützen, eine vorläufige DoD-Autorisierung (Pa) zu erteilen, die es einem CSP ermöglicht, DoD-Missionen zu hosten. Es integriert, ersetzt und entfernt das zuvor veröffentlichte DoD Cloud Security Model (CSM) und ist dem DoD Risk Management Framework (RMF) zugeordnet.

DISA leitet DoD-Behörden und -Abteilungen bei der Planung und Autorisierung der Verwendung eines CSP. Darüber hinaus werden CSP-Angebote auf Die Einhaltung der SRG ausgewertet. Dabei handelt es sich um einen Autorisierungsprozess, bei dem CSPs Dokumentationen erstellen können, in denen ihre Einhaltung von DoD-Standards beschrieben wird. Es stellt gegebenenfalls vorläufige Genehmigungen (PAs) für DoD aus, sodass DoD-Behörden und unterstützende Organisationen Clouddienste nutzen können, ohne dass sie selbst einen vollständigen Genehmigungsprozess durchlaufen müssen, was Zeit und Mühe spart.

Gemäß [SRG-Abschnitt 3.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#3.2InformationImpactLevels) *Information Impact Levels* deckt IL5-Informationen Folgendes ab:

- Kontrollierte nicht klassifizierte Informationen (Unclassified Information, CUI), die ein höheres Schutzniveau erfordern als die von IL4 bereitgestellte
    - Die [CUI-Registrierung](https://www.archives.gov/cui) stellt bestimmte Kategorien von Informationen bereit, die vom Executive Branch geschützt werden, z. B. sind mehr als 20 Kategoriegruppierungen in der [CUI-Kategorieliste](https://www.archives.gov/cui/registry/category-list)enthalten.
    - [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations* is intended for use by federal agencies in contracts or other agreements established with non-federal organizations.

- National Security Systems (NSS)
    - [Die NIST SP 800-59-Richtlinie](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) *zur Identifizierung eines Informationssystems als nationales Sicherheitssystem* stellt Definitionen von NSS bereit.
    - [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *Security Categorization and Control Selection for National Security Systems* bietet Anleitungen zu den Sicherheitsstandards, die Bundesbehörden anwenden sollten, um nationale Sicherheitsinformationen zu kategorisieren.

Im [DoD-CIO-Memo vom 15. Dezember 2014](https://www.esi.mil/contentview.aspx?id=585) zu *aktualisierten Anleitungen zum Erwerb und zur Verwendung kommerzieller Cloud Computing Services* heißt es: "FedRAMP dient als Mindestsicherheitsgrundwert für alle DoD-Clouddienste". Die SRG verwendet den FedRAMP Moderate-Basisplan auf allen Informationsauswirkungsstufen (Information Impact Levels, IL) und berücksichtigt den high Baseline an einigen.

[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* states that a FedRAMP High PA, supplemented with DoD FedRAMP+ controls and control enhancements (C/CEs) and requirements in the SRG, are used to assess CSPs to awarding a DoD PA at IL5. Unabhängig davon, welcher C/CE-Basisplan als Grundlage für eine FedRAMP High PA verwendet wird, müssen zusätzliche Überlegungen und/oder Anforderungen bewertet und genehmigt werden, bevor eine DoD PA an IL5 vergeben werden kann. Insbesondere gibt [SRG Section 5.1.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD FedRAMP+ Security Controls/Enhancements* in Tabelle 2 an, dass 10 zusätzliche C/CEs über den FedRAMP High-Basisplan hinaus für eine DoD IL5 PA erforderlich sind.

Darüber hinaus müssen gemäß [SRG-Abschnitt 5.2.2.3](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL5-Standort- und Trennungsanforderungen* die folgenden Anforderungen (unter anderem) für eine Pa der Stufe 5 erfüllt sein:

- Die virtuelle/logische Trennung zwischen DoD- und Behördenmandanten/-missionen ist ausreichend. Es ist eine virtuelle/logische Trennung zwischen Mandanten-/Missionssystemen erforderlich.
- Es ist eine physische Trennung von Nicht-DoD-/Nicht-Bundesverwaltungsmandanten (d. h. öffentliche Mandanten, Lokale/Landesverwaltungsmandanten) erforderlich.
- Der CSP schränkt den potenziellen Zugriff auf DoD- und Community-Informationen auf CSP-Mitarbeiter ein, die US-Bürger sind.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Zu Microsoft gehörende Cloudplattformen und -dienste

- Azure
- Dynamics 365-Kundendienst
- Microsoft Defender für Endpunkt (früher Microsoft Defender Advanced Threat Protection)
- Microsoft Graph
- Microsoft Stream
- Office 365 U.S. Government Defense
- Power Automate (ehemals Microsoft Flow)
- Power BI

## <a name="azure-dynamics-365-and-dod-il5"></a>Azure, Dynamics 365 und DoD IL5

Weitere Informationen zu Azure, Dynamics 365 und anderen Onlinediensten finden Sie im [Azure DoD IL5-Angebot.](/azure/compliance/offerings/offering-dod-il5)

## <a name="office-365-and-dod-il5"></a>Office 365 und DoD IL5

### <a name="office-365-cloud-environments"></a>Office 365-Cloudumgebungen

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365-Anwendbarkeit und im Leistungsumfang enthaltene Dienste

Verwenden Sie die folgende Tabelle, um die Anwendbarkeit für Ihre Office 365-Dienste und -Abonnements zu bestimmen:

| **Anwendbarkeit** | **Im Leistungsumfang enthaltene Dienste** |
|:------------------|:----------------------|
| **DoD** | Activity Feed Service, Bing Services, Exchange Online, Exchange Online Protection, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |

### <a name="attestation-documents"></a>Nachweisdokumente

Kunden von US-Behörden können Office 365 FedRAMP-Dokumentation der US Government Defense direkt vom [FedRAMP Marketplace](https://marketplace.fedramp.gov/#!/products?sort=productName&productNameSearch=azure) anfordern, indem sie ein Paketzugriffsanforderungsformular übermitteln. Sie müssen über eine .gov- oder .mil-E-Mail-Adresse verfügen, um direkt über FedRAMP auf ein FedRAMP-Sicherheitspaket zugreifen zu können.

Wählen Sie FedRAMP- und DoD-Dokumentation aus, einschließlich Systemsicherheitsplan (SSP), kontinuierlicher Überwachungsberichte, Aktionsplan und Meilensteine (POA \& M) usw., ist für Kunden unter NDA und ausstehende Zugriffsautorisierung im Abschnitt "Überwachungsberichte des Service Trust Portals [– FedRAMP-Berichte"](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3) verfügbar. Wenden Sie sich an Ihren Microsoft-Kontomitarbeiter, um Unterstützung zu erhalten.

### <a name="resources"></a>Ressourcen

- [Microsoft Government-Lösungen](https://www.microsoft.com/enterprise/government)
- [Leitfaden zu den Sicherheitsanforderungen für DoD Cloud Computing](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [FedRAMP-Dokumente](https://www.fedramp.gov/documents/)
- [DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) für DoD Information Technology (IT)*
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*
- [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *Sicherheits- und Datenschutzkontrollen für Informationssysteme und Organisationen*
- [NIST SP 800-59-Richtlinie](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) *zur Identifizierung eines Informationssystems als nationales Sicherheitssystem*
- [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *– Sicherheitskategorisierung und Steuerelementauswahl für nationale Sicherheitssysteme*
- [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations*
- [Controlled](https://www.archives.gov/cui) Unclassified Information (CUI) Registry and CUI [category list](https://www.archives.gov/cui/registry/category-list).
