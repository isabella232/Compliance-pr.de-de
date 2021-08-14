---
title: NEN 7510
description: Organisationen in den Niederlanden müssen ihre Kontrolle über Patientendaten gemäß des NEN 7510-Standards nachweisen.
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
ms.openlocfilehash: f3012269f613d5b403882c1718c3fbdc1f745519
ms.sourcegitcommit: 01938022a292c07e98041dc6ae1312a1b8c617db
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "58259784"
---
# <a name="nen-7510"></a>NEN 7510

## <a name="nen-7510-overview"></a>Übersicht über NEN 7510

Organisationen in den Niederlanden, die Gesundheitsdaten von Patienten verarbeiten, müssen nachweisen, dass sie die Kontrolle über diese Daten haben und die im Standard NEN 7510 festgelegten Anforderungen erfüllen. Microsoft unterliegt zwar nicht selbst dem NEN 7510-Standard, aber seine Cloudkunden im Gesundheitswesen müssen Compliance mit NEN 7510 für Lösungen auf Basis der Microsoft Cloud nachweisen. Microsoft-Clouddienste werden regelmäßig verschiedenen Zertifizierungen und Prüfungen unterzogen. Einige dieser Zertifizierungen und Prüfungen enthalten Elemente, die eng an den im Standard NEN 7510 festgelegten Anforderungen ausgerichtet sind.

## <a name="microsoft-and-nen-75102011"></a>Microsoft und NEN 7510:2011

Microsoft hat seine aktuellen Zertifizierungen und Erklärungen analysiert und einen [NEN 7510-Abdeckungsbericht](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=3285c45c-921c-49ad-b881-be43e0b70490&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Compliance_Guides) erstellt und auf der Service Trust Platform bereitgestellt. In diesem Bericht werden die Zertifizierungen und Erklärungen den NEN 7510-Kontrollen zugeordnet, für die Microsoft als Clouddienstanbieter verantwortlich ist. Anhand dieses Dokuments können Kunden ermitteln, welche anderen Kontrollen sie implementieren müssen, um sicherzustellen, dass ihre Verwendung von Microsoft Cloud Services für die Speicherung oder Verarbeitung von Patientendaten die Anforderungen von NEN 7510 erfüllt.

So können Sie Ihre NEN 7510-Implementierung mithilfe der Azure Security and Compliance Blueprints beschleunigen: [Microsoft Cloud: Azure und Office 365 NEN7510-2011 Standardabdeckung Benutzerhandbuch herunterladen](https://aka.ms/Azure-NEN7510-2011)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>In Microsoft eingeschlossene Cloudplattformen und -Dienste

- Azure und Azure Government
- Intune
- Office 365

## <a name="office-365-and-iso-27001"></a>Office 365 und ISO 27001

### <a name="office-365-cloud-environments"></a>Office 365-Cloudumgebungen

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365-Anwendbarkeit und im Leistungsumfang enthaltene Dienste

Verwenden Sie die folgende Tabelle, um die Anwendbarkeit für Ihre Office 365-Dienste und -Abonnements zu bestimmen:

| **Anwendbarkeit** | **Im Leistungsumfang enthaltene Dienste** |
|:------------------|:----------------------|
| **Kommerziell** | Azure Information Protection, Bookings, Delve, Exchange Online, Exchange Online Protection, Kaizala, Microsoft Analytics, Microsoft Booking, Microsoft Graph, Microsoft Teams, Microsoft To Do für das Web, MyAnalytics, Office 365 Cloud App Security, Office 365-Gruppen, Office 365 Video, OneDrive for Business, Planner, Power Apps, Power Automate, Power BI für Office 365, PowerApps, SharePoint Online, Skype for Business, StaffHub, Stream, Sway, Yammer Enterprise |

## <a name="audits-reports-and-certificates"></a>Prüfungen, Berichte und Zertifikate

- [Azure und Office 365-Abdeckung in Bezug auf den NEN 7510:2011-Standard](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=15d5a5fa-fbb6-4ea6-8126-2a2c684ae789&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_GRC_Assessment_Reports)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Sind Kunden, die Microsoft Cloud Services nutzen, konform mit NEN 7510?**

Für den Nachweis der NEN-Konformität ist die Gesundheitsorganisation (der „Kunde“) verantwortlich. Wenn ein Kunde mit einem Clouddienstanbieter zusammenarbeitet, fordert er in der Regel einen Nachweis vom Anbieter und muss eigene (andere) technische und betriebliche Funktionen, Auswahlmöglichkeiten und Prozesse einrichten. Das führt zu einer Gesamtbeurteilung durch Kunden bezüglich der Einhaltung der NEN 7510, die für eine externe Überprüfung oder Zertifizierung eingereicht werden kann. Der NEN 7510-Abdeckungsbericht gibt Erkenntnisse darüber, welche NEN 7510-Kontrollen von Microsoft Cloud Services abgedeckt werden, deckt aber als solche nicht die End-to-End-Compliance ab.

**Hat Microsoft Compliance mit NEN 7510 erzielt?**

Die Verantwortung für die Compliance mit NEN 7510 liegt bei niederländischen Organisationen im Gesundheitswesen. Das Unternehmen muss ein Managementsystem für Informationssicherheit einrichten und Risiken mit entsprechenden technischen und betrieblichen Maßnahmen entgegenwirken. Für Microsoft in seiner Rolle als Clouddienstanbieter ist Compliance mit NEN 7510 weder das Ziel noch technisch machbar. Wenn Kunden Microsoft Cloud Services implementieren oder nutzen, können diese Dienste in den Anwendungsbereich einer NEN 7510-Evaluierung fallen. Die Organisation muss jedoch ihre eigenen (anderen) Kontrollen, Wahlmöglichkeiten und Prozesse hinzufügen, die Teil der NEN 7510-Gesamtbewertung sind. Ziel des Berichts ist der Nachweis, dass eine Organisation des Gesundheitswesens Microsoft Cloud Services auf eine Weise nutzen kann, die mit NEN 7510 konform ist.

**Der Bericht weist keine 100-prozentige Abdeckung nach. Kann die NEN 7510-Compliance nicht erzielt werden?**

Die Microsoft Cloud Services bieten viele Kontrollen, die Organisationen im niederländischen Gesundheitswesen bei der Einhaltung von NEN 7510 unterstützen. Das Unternehmen muss diese Anbieterzusicherungen trotzdem mit eigenen Implementierungsoptionen, anderen technologischen Kontrollen und Verwaltungsprozessen erweitern. Der Bericht weist bereits eine direkte 94-prozentige Abdeckung der gesamten Liste der anwendbaren Kontrollen auf. Für die verbleibenden Kontrollen stellt Microsoft im Bericht Anweisungen zur Verfügung, wie Compliance mit diesen Kontrollen nachgewiesen werden kann.

> [!NOTE]
> Die Implementierung der vollständigen Kontrollliste ist nicht der primäre Zweck von NEN 7510 (allerdings ist die umfassende Abdeckung der Microsoft-Onlinedienste hilfreich). NEN 7510 ordnet die Implementierung eines risikobasierten Informationssicherheitssystems an, mit dessen Hilfe eine Organisation ermitteln kann, welche Kontrollen für sie relevant sind.

**Ist der NEN 7510-Abdeckungsbericht ein rechtlich bindendes Dokument?**

Nein. Es ist ein unterstützendes Tool, das die internen Prozesse von Kunden zur Herstellung der Compliance mit NEN 7510 unterstützt und ihnen die Sicherheit und das Vertrauen gibt, dass die Compliance mit NEN 7510 erreicht werden kann. Der Bericht wurde vom unabhängigen Prüfunternehmen KPMG erstellt, ist beschreibender Art und enthält einen Haftungsausschluss.

**Hat Microsoft den Bericht bezahlt?**

Microsoft hat seine globalen Mechanismen den Kontrollen des NEN 7510-Standards zugeordnet. Anschließend hat Microsoft das unabhängige Prüfunternehmen KPMG damit beauftragt, die Zuordnung der Mechanismen zu den Kontrollen des NEN 7510-Standards unabhängig zu prüfen. Das Ergebnis dieser Prüfung ist der Bericht.

**Können wir diesen Bericht weitergeben?**

Der Bericht wird Ihnen im Rahmen einer Vertraulichkeitsvereinbarung (Non Disclosure Agreement, NDA) unter der Voraussetzung zur Verfügung gestellt, dass er nur der Information von Kunden dient und weder kopiert noch über andere Kanäle als das Microsoft Service Trust Portal offengelegt wird.

Kunden können den Bericht im Rahmen ihrer Compliance- oder Assurance-Prozesse an ihren eigenen internen oder externen Prüfer weitergeben.

## <a name="resources"></a>Ressourcen

- [Informationen zu NEN](https://www.nen.nl/About-NEN.htm)
- [NEN 7510:2011-Standard](https://www.nen.nl/NEN-Shop-2/Standard/NEN-75102011-nl.htm)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
