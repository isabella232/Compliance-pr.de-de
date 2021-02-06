---
title: Überwachung und Berichterstellung in Microsoft Cloud Services
description: Eine Übersicht über Überwachungs- und Berichterstellungsfunktionen in Office 365, Microsoft 365 und Service Assurance.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- M365-analytics
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 4cb9f68f2c5861905a4246582a3b4530c30988ca
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120704"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Überwachung und Berichterstellung in Microsoft Cloud Services

Microsoft Cloud Services umfassen mehrere Überwachungs- und Berichtsfunktionen, mit deren Rahmen Sie Benutzer- und Verwaltungsaktivitäten innerhalb ihres Mandanten nachverfolgen können. Beispiele hierfür sind Änderungen an den Konfigurationseinstellungen von Exchange Online- und SharePoint Online-Mandanten sowie Änderungen, die von Benutzern an Dokumenten und anderen Elementen vorgenommen wurden. Sie können Überwachungsinformationen und Berichte verwenden, die in Microsoft Cloud Services verfügbar sind, um die Benutzererfahrung effektiver zu verwalten, Risiken zu mindern und Complianceverpflichtungen zu erfüllen.

## <a name="security--compliance-centers"></a>Security & Compliance Center

Das [Microsoft 365 Security & Compliance Center,](https://protection.office.com) [Microsoft 365 Security Center](https://security.microsoft.com)und Microsoft [365 Compliance Center](https://compliance.microsoft.com) sind One-Stop-Portale zum Schutz von Daten in Ihrer Organisation und umfassen zahlreiche Überwachungs- und Berichtsfunktionen. Diese Center unterstützen Sie bei Ihren Datenschutz- oder Complianceanforderungen und überwachen Benutzer- und Administratoraktivitäten. Sie können mit Ihrem Abonnementadministratorkonto auf diese Center zugreifen.

Diese Center enthalten Navigationsbereich für den Zugriff auf mehrere Features:

- **Warnungen:** Ermöglicht ihnen das Verwalten von Warnungen, das Anzeigen sicherheitsrelevanter Warnungen und das Verwalten erweiterter Warnungen mithilfe [von Cloud App Security.](/cloud-app-security/what-is-cloud-app-security)
- **Berechtigungen:** Ermöglicht es Ihnen, [Personen](/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) in Ihrer Organisation Berechtigungen wie complianceadministrator, eDiscovery Manager und andere zuzuordnen, damit sie Aufgaben in diesen Centern ausführen können. Sie weisen Berechtigungen für die meisten Features in jedem Center zu, andere Berechtigungen müssen jedoch über das Exchange Admin Center und das SharePoint Admin Center konfiguriert werden.
- **Bedrohungsverwaltung:** Ermöglicht ihnen das Erstellen und Anwenden von Geräteverwaltungsrichtlinien mithilfe von [Basic Mobility and Security für Microsoft 365,](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)um Richtlinien zur Verhinderung von Datenverlust [(Data Loss Prevention,](/microsoft-365/compliance/data-loss-prevention-policies) DLP) für Ihre Organisation zu erstellen und anzuwenden, um E-Mail-Filterung, Ansoftware, DKIM (DomainKeys Identified Mail), sichere Anlagen, sichere Links und OAuth-Apps zu konfigurieren.
- **Datensteuerung:** Ermöglicht das Importieren von E-Mails oder SharePoint-Daten [](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)aus anderen Systemen in [](/microsoft-365/compliance/retention-policies) [Microsoft 365,](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84)das Konfigurieren von Archivpostfächern und das Festlegen von Aufbewahrungsrichtlinien für E-Mails und andere Inhalte in Ihrer Organisation.
- **Suche & Untersuchung:** Bietet [Inhaltssuche,](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a) [Überwachungsprotokoll,](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)Quarantäne und [eDiscovery-Fallverwaltungstools,](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) um schnell einen Drilldown zu Aktivitäten in Exchange Online-Postfächern, Gruppen und öffentlichen Ordnern, SharePoint Online und OneDrive for Business zu machen.
- **Berichte:** Ermöglicht ihnen den schnellen Zugriff [auf](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) Berichte für SharePoint Online, OneDrive for Business, Exchange Online und Azure AD.
- **Dienstsicherung:** Enthält Informationen dazu, wie Microsoft Sicherheit, Datenschutz und Compliance mit globalen Standards für Microsoft 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune und andere Clouddienste beibehält. Umfasst auch den Zugriff auf ISO, SOC und andere Überwachungsberichte von Drittanbietern sowie überwachte Kontrollen, die Details zu den verschiedenen Kontrollen enthalten, die von Prüfern von Microsoft 365 von Drittanbietern getestet und überprüft wurden.

## <a name="service-assurance"></a>Service Assurance

Viele Organisationen in regulierten Branchen unterliegen umfangreichen Complianceanforderungen. Um eigene Risikobewertungen durchführen zu können, benötigen Kunden häufig ausführliche Informationen dazu, wie Microsoft 365 die Sicherheit und den Datenschutz ihrer Daten beibehält. Microsoft setzt sich für die Sicherheit und den Datenschutz von Kundendaten in seinen Clouddiensten ein und setzt sich dafür ein, kundenbasiertes Vertrauen zu gewinnen, indem es einen transparenten Blick auf seinen Betrieb bietet und einfachen Zugriff auf unabhängige Complianceberichte und Bewertungen bietet.

Service Assurance bietet Transparenz der Vorgänge und Informationen darüber, wie Microsoft die Sicherheit, den Datenschutz und die Compliance von Kundendaten in Microsoft 365 beibehält. Sie umfasst Überwachungsberichte von Drittanbietern zusammen mit einer Bibliothek mit Whitepapern, FAQs und anderen Materialien zu Microsoft 365-Themen wie Datenverschlüsselung, Datenresilienz, Verwaltung von Sicherheitsvorfällen und vielem mehr. Kunden können diese Informationen verwenden, um ihre eigenen behördlichen Risikobewertungen durchzuführen. Compliance Officers können die Rolle "Service Assurance User" zuweisen, um Benutzern Zugriff auf Service Assurance zu ermöglichen. Der Mandantenadministrator kann auch externen Benutzern, z. B. unabhängigen Auditoren, Zugriff auf Informationen im Service Assurance-Dashboard über das [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) (STP) bieten.

## <a name="onedrive-for-business-admin-center"></a>OneDrive for Business Admin Center

Das Microsoft OneDrive Admin Center hilft Ihnen, die OneDrive for #A0 Ihrer Organisation schnell und einfach an einem Ort zu verwalten. Um das OneDrive Admin Center zu verwenden, ist zugriff auf onedrive.com erforderlich. Sie müssen auch ein globaler Administrator für Ihre Organisation oder ein benutzerdefinierter Administrator mit der Rolle des SharePoint-Administrators sein. Greifen Sie auf das OneDrive for Business Admin Center unter [https://admin.onedrive.com](https://admin.onedrive.com/) zu.

Zu den wichtigsten Features gehört ein Compliancebereich, der Administratoren Links zum entsprechenden Verwaltungscenter für wichtige Szenarien wie das Durchsuchen des Überwachungsprotokolls, das Arbeiten mit DLP, Aufbewahrung, eDiscovery und Benachrichtigungen bietet.

## <a name="related-links"></a>Links zu verwandten Themen

- [Berichtsfeatures in Microsoft 365](assurance-reporting-features.md)
- [Interne Protokollierung für Microsoft 365 Engineering](assurance-internal-logging.md)
