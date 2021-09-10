---
title: Überwachung und Berichterstellung in Microsoft Cloud Services
description: Eine Übersicht über die Überwachungs- und Berichterstellungsfunktionen in Office 365, Microsoft 365 und Service Assurance.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
hideEdit: true
ms.openlocfilehash: c1a2cc9e770678683fb3823da73ed667de6d1f2b
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947033"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Überwachung und Berichterstellung in Microsoft Cloud Services

Microsoft-Clouddienste umfassen verschiedene Überwachungs- und Berichterstellungsfunktionen, die Sie verwenden können, um Benutzer- und Verwaltungsaktivitäten innerhalb ihres Mandanten nachzuverfolgen. Beispiele sind Änderungen an Exchange Online und SharePoint Online-Mandantenkonfigurationseinstellungen und Änderungen, die von Benutzern an Dokumenten und anderen Elementen vorgenommen wurden. Sie können in Microsoft Cloud Services verfügbare Überwachungsinformationen und Berichte verwenden, um die Benutzererfahrung effektiver zu verwalten, Risiken zu mindern und Compliance-Verpflichtungen zu erfüllen.

## <a name="security--compliance-centers"></a>Security & Compliance Center

Das [Microsoft 365 Security & Compliance Center,](https://protection.office.com) [Microsoft 365 Security Center](https://security.microsoft.com)und [Microsoft 365 Compliance Center](https://compliance.microsoft.com) sind One-Stop-Portale zum Schutz von Daten in Ihrer Organisation und umfassen viele Überwachungs- und Berichtsfunktionen. Diese Center helfen Ihnen bei Ihren Anforderungen im Hinblick auf Datenschutz oder Compliance und bei der Überwachung von Benutzer- und Administratoraktivitäten. Sie können über Ihr Abonnementadministratorkonto auf diese Center zugreifen.

Diese Center umfassen Navigationsbereiche für den Zugriff auf mehrere Features:

- **Warnungen:** Ermöglicht es Ihnen, Warnungen zu verwalten, sicherheitsrelevante Warnungen anzuzeigen und erweiterte Warnungen mit [Cloud App Security](/cloud-app-security/what-is-cloud-app-security)zu verwalten.
- **Berechtigungen:** Ermöglicht es Ihnen, Personen in Ihrer Organisation Berechtigungen wie Complianceadministrator, eDiscovery-Manager und andere [zuzuweisen,](/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) damit sie Aufgaben in diesen Centern ausführen können. Sie weisen berechtigungen für die meisten Features in jedem Center zu, aber andere Berechtigungen müssen mit dem Exchange Admin Center und SharePoint Admin Center konfiguriert werden.
- **Bedrohungsmanagement:** Ermöglicht ihnen das Erstellen und Anwenden von Geräteverwaltungsrichtlinien mit basic [Mobility and Security for Microsoft 365,](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)zum Einrichten von DLP-Richtlinien [(Data Loss Prevention, Verhinderung von Datenverlust)](/microsoft-365/compliance/data-loss-prevention-policies) für Ihre Organisation, zum Konfigurieren von E-Mail-Filterung, Antischadsoftware, DomainKeys Identified Mail (DKIM), sicheren Anlagen, sicheren Links und OAuth-Apps.
- **Datengovernance:** Ermöglicht es Ihnen, [E-Mails oder SharePoint Daten aus anderen Systemen in Microsoft 365](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84)zu importieren, [Archivpostfächer zu konfigurieren](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)und [Aufbewahrungsrichtlinien](/microsoft-365/compliance/retention-policies) für E-Mails und andere Inhalte in Ihrer Organisation festzulegen.
- **Suche & Untersuchung:** Stellt [Tools für inhaltssuche,](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a) [Überwachungsprotokoll,](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)Quarantäne und [eDiscovery-Fallverwaltung](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) bereit, um Schnellinformationen zu Aktivitäten in Exchange Online Postfächern, Gruppen und öffentlichen Ordnern, SharePoint Online und OneDrive for Business zu erhalten.
- **Berichte:** Ermöglicht ihnen den schnellen Zugriff auf [Berichte](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) für SharePoint Online, OneDrive for Business, Exchange Online und Azure AD.
- **Dienstsicherung:** Enthält Informationen dazu, wie Microsoft Sicherheit, Datenschutz und Compliance mit globalen Standards für Microsoft 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune und andere Clouddienste aufrechterhält. Umfasst außerdem den Zugriff auf ISO-, SOC- und andere Überwachungsberichte von Drittanbietern sowie überwachte Kontrollen, die Details zu den verschiedenen Steuerelementen bereitstellen, die von Prüfern von Drittanbietern von Microsoft 365 getestet und überprüft wurden.

## <a name="service-assurance"></a>Service Assurance

Viele Organisationen in regulierten Branchen unterliegen umfangreichen Complianceanforderungen. Um ihre eigenen Risikobewertungen durchzuführen, benötigen Kunden häufig ausführliche Informationen darüber, wie Microsoft 365 die Sicherheit und den Datenschutz ihrer Daten aufrechterhält. Microsoft setzt sich für die Sicherheit und den Datenschutz von Kundendaten in seinen Clouddiensten ein und verdient das Vertrauen der Kunden, indem es eine transparente Übersicht über seine Vorgänge bietet und einfachen Zugriff auf unabhängige Complianceberichte und Bewertungen bietet.

Service Assurance bietet Transparenz von Vorgängen und Informationen darüber, wie Microsoft die Sicherheit, den Datenschutz und die Einhaltung von Kundendaten in Microsoft 365 verwaltet. Sie enthält Überwachungsberichte von Drittanbietern sowie eine Bibliothek mit Whitepapers, häufig gestellten Fragen und anderen Materialien zu Microsoft 365 Themen wie Datenverschlüsselung, Datenresilienz, Verwaltung von Sicherheitsvorfällen und mehr. Kunden können diese Informationen verwenden, um ihre eigenen regulatorischen Risikobewertungen durchzuführen. Compliance Officer können die Rolle "Service Assurance-Benutzer" zuweisen, um Benutzern Zugriff auf Service Assurance zu gewähren. Der Mandantenadministrator kann externen Benutzern, z. B. unabhängigen Auditoren, auch Zugriff auf Informationen im Service Assurance-Dashboard über das [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) (STP) gewähren.

## <a name="onedrive-for-business-admin-center"></a>OneDrive for Business Admin Center

Das Microsoft OneDrive Admin Center hilft Ihnen, die OneDrive for Business Einstellungen Ihrer Organisation schnell und einfach an einem Ort zu verwalten. Um das OneDrive Admin Center zu verwenden, ist der Zugriff auf onedrive.com erforderlich. Sie müssen auch ein globaler Administrator für Ihre Organisation oder ein benutzerdefinierter Administrator mit der SharePoint Administratorrolle sein. Greifen Sie auf das OneDrive for Business Admin Center unter [https://admin.onedrive.com](https://admin.onedrive.com/) zu.

Zu den wichtigsten Features gehört ein Compliancebereich, der Administratoren Links zum entsprechenden Verwaltungscenter für wichtige Szenarien wie das Durchsuchen des Überwachungsprotokolls, das Arbeiten mit DLP, die Aufbewahrung, eDiscovery und warnungen bereitstellt.

## <a name="related-links"></a>Links zu verwandten Themen

- [Berichtsfeatures in Microsoft 365](assurance-reporting-features.md)
- [Interne Protokollierung für Microsoft 365 Engineering](assurance-internal-logging.md)
