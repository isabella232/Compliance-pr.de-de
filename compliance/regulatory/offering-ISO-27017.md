---
title: ISO/IEC 27017:2015-Verhaltenskodex für Informationssicherheitskontrollen
description: Microsoft-Clouddienste haben diesen Verhaltenskodex für Informationssicherheitskontrollen implementiert.
keywords: Microsoft 365, Compliance, Angebote
localization_priority: Priority
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
ms.openlocfilehash: 54ae2345f72e6ea0b9b0e856721acc7ff6590e52
ms.sourcegitcommit: 01938022a292c07e98041dc6ae1312a1b8c617db
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "58260477"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a>ISO/IEC 27017:2015 Verhaltenskodex für Informationssicherheitskontrollen

## <a name="iso-iec-27017-overview"></a>Übersicht über ISO-IEC 27017

Der ISO/IEC 27017:2015-Verhaltenskodex ist als Referenz für Organisationen vorgesehen, um sie während der Implementierung eines Systems für die Verwaltung der Cloud Computing-Informationssicherheit gemäß ISO/IEC 27002:2013 bei der Auswahl von Informationssicherheitskontrollen für Clouddienste zu unterstützen. Er kann auch von Cloud Service-Anbietern als Leitfaden zum Implementieren von allgemein anerkannten Schutzkontrollen verwendet werden.

Dieser internationale Standard bietet zusätzliche cloudspezifische Implementierungsanleitungen auf der Grundlage von ISO/IEC 27002 und stellt zusätzliche Kontrollen für Kontrollen, Implementierungsanleitungen und andere Informationen zur Verfügung, um cloudspezifischen Bedrohungen und Risiken der Informationssicherheit zu begegnen, die sich auf die Abschnitte 5–18 in ISO/IEC 27002: 2013 beziehen. Insbesondere stellt dieser Standard Anleitungen zu 37 Kontrollen in ISO/IEC 27002 zur Verfügung und enthält außerdem sieben neue Kontrollen, die nicht in ISO/IEC 27002 dupliziert sind. Diese neuen Kontrollen beziehen sich auf die folgenden wichtigen Bereiche:

- Gemeinsame Rollen und Pflichten innerhalb einer Cloud Computing-Umgebung
- Entfernen und Rückgabe von Kundenressourcen in Cloud Services nach Vertragsende
- Schutz und Trennung der virtuellen Umgebung eines Kunden von den Umgebungen anderer Kunden
- Erfordernisse zur Stärkung virtueller Maschinen um Geschäftsanforderungen zu erfüllen
- Verfahren für administrative Abläufe einer Cloud Computing-Umgebung
- Überwachung relevanter Aktivitäten innerhalb einer Cloud Computing-Umgebung durch den Kunden
- Ausrichtung der Sicherheitsverwaltung für virtuelle und physische Netzwerke

## <a name="microsoft-and-isoiec-27017"></a>Microsoft und ISO/IEC 27017

ISO/IEC 27017 ist einzigartig, da es Anleitungen für Anbieter und Kunden von Clouddiensten bereitstellt. Der Standard stellt außerdem Cloud Service-Kunden praktische Informationen im Hinblick auf ihre Erwartungen an Cloud Service-Anbieter zur Verfügung. Kunden können die Vorteile von ISO/IEC 27017 direkt nutzen, indem sie sich der gemeinsamen Verantwortung in der Cloud bewusst sind.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Zu Microsoft gehörende Cloudplattformen und -dienste

- [Azure und Azure Government und Azure Deutschland](https://aka.ms/AzureCompliance)
- Microsoft Cloud App-Sicherheit
- [Dynamics 365, Dynamics 365 und Dynamics 365 Deutschland](https://aka.ms/d365-compliance-list)
- Intune
- Microsoft Defender für Endpunkt
- Microsoft Graph
- Microsoft Healthcare Bot
- [Microsoft Managed Desktop](/microsoft-365/managed-desktop/intro/compliance)
- Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense und Office 365 Deutschland
- Power Automate-Clouddienst (ehemals Microsoft Flow) als eigenständiger Dienst oder in einem Office 365- oder Dynamics 365-Plan bzw. -Anwendungssuite enthalten
- PowerApps-Clouddienst als eigenständiger Dienst oder in einem firmenspezifischen Office 365- oder Dynamics 365-Plan oder einer -Anwendungssuite enthalten
- Power BI-Clouddienst als eigenständiger Dienst oder in einem firmenspezifischen Office 365-Plan oder einer -Anwendungssuite enthalten
- Power BI Embedded

## <a name="azure-dynamics-365-and-iso-270172015"></a>Azure, Dynamics 365 und ISO 27017:2015

Weitere Informationen zur Compliance mit Azure, Dynamics 365 und anderen Onlinedienste finden Sie im [Azure ISO 27017-Angebot](/azure/compliance/offerings/offering-iso-27017).

## <a name="office-365-and-iso-270172015"></a>Office 365 und ISO 27017:2015

### <a name="office-365-cloud-environments"></a>Office 365-Cloudumgebungen

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365-Anwendbarkeit und im Leistungsumfang enthaltene Dienste

Verwenden Sie die folgende Tabelle, um die Anwendbarkeit für Ihre Office 365-Dienste und -Abonnements zu bestimmen:

| **Anwendbarkeit** | **Im Leistungsumfang enthaltene Dienste** |
|:------------------|:----------------------|
| **Kommerziell** | Access Online, Azure Active Directory, Azure Communications Service, Compliance Manager, Kunden-Lockbox, Delve, Exchange Online, Exchange Online Protection, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Defender für Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance-Add-On, Office 365-Kundenportal, Office 365-Microservices (einschließlich, aber nicht beschränkt auf Kaizala, ObjectStore, Sway, PowerPoint Online-Dokumentdienst, Abfrageanmerkungsdienst, School Data Sync, Sifon, Speech, StaffHub, eXtensible-Anwendungsprogramm), Office 365 Security & Compliance Center, Office Online, Office Pro Plus, Office Services-Infrastruktur, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Project Online, Dienstverschlüsselung mit Kundenschlüssel, SharePoint Online, Skype for Business, Stream |
| **GCC** | Azure Active Directory, Azure Communications Service, Compliance-Manager, Delve, Exchange Online, Forms, Microsoft Defender für Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance-Add-On, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream |
| **GCC Hoch** | Azure Active Directory, Azure Communications Service, Exchange Online, Forms, Microsoft Defender für Office 365, Microsoft Teams, Office 365 Advanced Compliance-Add-On, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business |
| **DoD** | Azure Active Directory, Azure Communications Service, Exchange Online, Forms, Microsoft Defender für Office 365, Microsoft Teams, Office 365 Advanced Compliance-Add-On, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, Power BI, SharePoint Online, Skype for Business |

### <a name="office-365-audits-reports-and-certificates"></a>Office 365-Audits, -Berichte und -Zertifikate

Microsoft-Clouddienste werden einmal jährlich im Rahmen des Zertifizierungsprozesses nach ISO/IEC 27001:2013 hinsichtlich des ISO/IEC 27017:2015-Verhaltenskodex überprüft.

- [Office 365: ISO 27001, 27018 und 27017-Prüfbericht](https://aka.ms/o365isoreport)

### <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Für wen gilt der Standard?**

Dieser Verhaltenskodex stellt Kontrollen und Implementierungsanleitungen für Anbieter und Kunden von Clouddiensten bereit. Er ist ähnlich strukturiert wie ISO/IEC 27002:2013.

**Wo kann ich Microsofts Konformitätsinformationen für ISO/IEC 27017:2015 einsehen?**

Sie können das [ISO/IEC 27017:2015-Zertifikat](https://aka.ms/azureiso27017) für Azure, Intune und Power BI herunterladen.

**Kann ich die ISO/IEC 27017-Konformität von Microsoft-Diensten im Zertifizierungsprozess meiner Organisation nutzen?**

Ja. Wenn Ihr Unternehmen eine Zertifizierung für Installationen anstrebt, die in einem der im Umfang enthaltenen Microsoft Enterprise Cloud Services bereitgestellt werden, können Sie die entsprechenden Zertifizierungen von Microsoft für Ihre Compliancebewertung verwenden. Sie sind jedoch dafür verantwortlich, einen Auditor mit der Prüfung Ihrer Implementierung unter Wahrung der Compliance zu beauftragen. Außerdem sind Sie für die Kontrollen und Prozesse in Ihrer eigenen Organisation zuständig.

**Wie erhalte ich Kopien der entsprechenden Prüfberichte?**

Im [Service Trust Portal](https://aka.ms/stphelp) erhalten Sie unabhängige Prüfberichte von Dritten und weitere zugehörige Dokumentation. Sie können diese Dokumentation aus dem Portal herunterladen und prüfen, um Unterstützung bei der Erfüllung Ihrer eigenen gesetzlichen Anforderungen zu erhalten.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Verwenden Sie den Microsoft Compliance Manager, um Ihr Risiko einzuschätzen

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) ist eine Funktion im [Microsoft 365 Compliance Center](/microsoft-365/compliance/microsoft-365-compliance-center), die Ihnen hilft, die Compliance-Position Ihres Unternehmens zu verstehen und Maßnahmen zu ergreifen, um Risiken zu reduzieren. Compliance Manager bietet eine Premiumvorlage für die Erstellung einer Bewertung für diese Verordnung. Suchen Sie die Vorlage auf der Seite **Bewertungsvorlagen** im Compliance Manager. Erfahren Sie, wie Sie [Bewertungen im Compliance-Manager erstellen](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Ressourcen

- [ISO/IEC 27017:2015-Verhaltenskodex](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [Nutzungsbedingungen für Microsoft-Onlinedienste](https://aka.ms/Online-Services-Terms)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
