---
title: Lieferantenmanagement (Übersicht)
description: Informationen zur Lieferantenverwaltung in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH'
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 73ec8ca99f880a3c6277bd917dab99b9aff49999
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496698"
---
# <a name="supplier-management-overview"></a>Lieferantenmanagement (Übersicht)

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Wie verwaltet Microsoft risiken im Zusammenhang mit Lieferanten?

Microsoft partner with third-party companies to help meet our customers' needs. Diese Drittanbieterunternehmen werden als Lieferanten oder Unterverarbeiter bezeichnet. Die Sicherheit und der Datenschutz von Lieferanten bei Microsoft wird durch unser Programm zur Lieferantensicherheit und Datenschutzsicherung [(Supplier Security and Privacy Assurance, SSPA)](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)geregelt, einem unternehmensweiten Anforderungssatz für alle Lieferanten, die mit Microsoft zusammenarbeiten, um unsere Onlinedienste zu liefern. Während das SSPA-Programm eine umfassende Steuerung und Verwaltung unserer Lieferantenbasis bietet, können einzelne Geschäftsbereiche wie Microsoft 365 zusätzliche Anforderungen für ihre Lieferanten erfüllen.

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Wie schützt das Microsoft Supplier Security and Privacy Assurance (SSPA)-Programm Kundendaten?

SSPA ist eine Partnerschaft zwischen Microsoft Procurement, Corporate External and Legal Affairs und Corporate Security, um sicherzustellen, dass Lieferanten die Datenschutz- und Sicherheitsprinzipien von Microsoft einhalten. Der Umfang von SSPA umfasst alle Lieferanten, die personenbezogene Daten oder vertrauliche Daten von Microsoft verarbeiten. Die Registrierung des SSPA-Programms umfasst die Einhaltung der Datenschutzanforderungen (Data Protection Requirements, DPR) von Microsoft. Die Datenschutzrichtlinien bestehen aus Sicherheits- und Datenschutzkontrollen, die Lieferanten implementieren müssen, bevor sie mit der Vertragsarbeit mit Microsoft beginnen. Alle registrierten Lieferanten bestätigen die Einhaltung der Datenschutzrichtlinien jährlich selbst.

DpR-Anforderungen basieren auf sechs unterschiedlichen Datenverarbeitungskategorien, für die ein Anbieter im Rahmen seiner Registrierung bei SSPA genehmigt werden kann. Diese Kategorien werden verwendet, um das Risiko zu identifizieren, das mit den Diensten verbunden ist, die ein Anbieter Microsoft bietet. Das Datenverarbeitungsprofil des Lieferanten bestimmt, welche DpR-Steuerelemente als in-Scope betrachtet werden, um einen geeigneten Datenschutz zu gewährleisten. Lieferanten, die Daten verarbeiten, die als ein höheres Risiko betrachtet werden, müssen alle Anforderungen an die Datenschutzrichtlinien erfüllen und müssen möglicherweise auch eine unabhängige Überprüfung der Compliance bereitstellen. Microsoft-Einkaufstools überprüfen den SSPA-Status aller Lieferanten, einschließlich der Einhaltung der geltenden Teile der Datenschutzrichtlinien, bevor sie die Beschaffung dieses Lieferanten zulassen.

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>Welche Arten von Unterprozessoren bieten Dienste für Microsoft an?

Ein "Unterverarbeiter" ist ein Drittanbieter, den Microsoft einnimmt, dessen Aufgaben die Verarbeitung personenbezogener Daten von Microsoft umfassen, für die Microsoft auftragsverarbeiter ist. Die Unterprozessoren von Microsoft sind in drei unterschiedliche Kategorien unterteilt. Jeder muss die Einhaltung der SSPA nachweisen, bevor er Kundendaten im Auftrag von Microsoft verarbeiten kann.

- **Technologie**-Unterauftragsverarbeiter bieten Technologien an, die zur Bereitstellung spezieller Microsoft-Onlinedienste verwendet werden. Wenn ein Kunde einen dieser Dienste zur Verfügung stellt, können die für diesen Dienst identifizierten Unterverarbeiter Kundendaten oder personenbezogene Daten verarbeiten, speichern oder anderweitig darauf zugreifen und dabei helfen, diesen Dienst zur Verfügung zu stellen.
- **Nebenverarbeiter** stellen Dienste zur Verfügung, die die Onlinedienste unterstützen, betreiben und warten. Wenn ein Kunde einen dieser Dienste zur Verfügung stellt, können die identifizierten Unterverarbeiter eingeschränkte Kundendaten oder personenbezogene Daten verarbeiten, speichern oder anderweitig darauf zugreifen, während sie ihre Hilfsdienste bereitstellen.
- **Unterverarbeiter** der Mitarbeiterintegation haben zwei unterschiedliche Formen: In beiden Szenarien befinden sich personenbezogene Daten nur in Microsoft-Einrichtungen, auf Microsoft-Systemen und unterliegen microsoft-Richtlinien und -Aufsicht.

    - Bei der ersten Form eines Personalaugmentations-Unterauftragsverarbeiters stellt dieser Personal zum Unterstützen, Betreiben und Verwalten von Microsoft-Onlinediensten bereit. Bei der Erfüllung ihrer Aufgaben können diese Unterauftragsverarbeiter möglicherweise auf Kunden- oder personenbezogene Daten zugreifen. So kann beispielsweise ein Unterauftragsverarbeiter eine Remoteproblembehandlung auf einem Microsoft-Server durchführen, in deren Verlauf Ausschnitte von Kundendaten in einem Serverabsturz-Speicherabbildprotokoll verfügbar werden können.
    - Die zweite Form der Mitarbeitervergrößerung umfasst Unterprozessoren, die mit Vollzeitmitarbeitern von Microsoft zusammenarbeiten, um Microsoft Onlinedienste zu unterstützen, zu betreiben und zu warten. Diese Unterauftragsverarbeiter können im Rahmen ihrer Zusammenarbeit mit Microsoft-Vollzeitmitarbeitern möglicherweise auf pseudonymisierte Daten zugreifen.

Technologie- und Hilfsunterprozessoren sind erforderlich, um Zugriffskontrollen in Übereinstimmung mit den Datenschutzanforderungen (Data Protection Requirements, DPR) von Microsoft zu implementieren. Diese Anforderungen erfüllen oder überschreiten die vertraglichen Verpflichtungen, die Microsoft seinen Kunden in den Onlinedienstbedingungen (OST) gegenüber macht. Lieferanten, die Mitarbeitervergrößerungen durchführen, unterliegen den gleichen Zugriffskontrollen für Vollzeitmitarbeiter von Microsoft.

## <a name="how-does-microsoft-onboard-suppliers"></a>Wie onboardt Microsoft Lieferanten?

Drittanbieter müssen im Rahmen des Onboardingprozesses einen Microsoft-Mastervertrag unterzeichnen. Dieser Vertrag regelt die Beziehung zwischen Microsoft und seinen Lieferanten und stellt eine konsistente Verwaltung der Lieferantenbeziehungen sicher. Im Rahmen des Onboardings registrieren sich Lieferanten bei der SSPA und müssen alle anwendbaren Anforderungen erfüllen, bevor sie für alle Datenverarbeitungskategorien genehmigt werden können. Microsoft-Geschäftseinheiten können Nur dann Engagements mit Lieferanten erstellen, wenn die Datenverarbeitungsaktivität für das Engagement den Datenverarbeitungskategorien entspricht, für die der Anbieter genehmigt wurde.

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Wie benachrichtigt Microsoft Kunden über Änderungen an Lieferanten, die ihre Daten verarbeiten?

Nach dem Microsoft Online Service Data Protection Addendum (DPA) macht Microsoft zusätzliche Verpflichtungen in Bezug auf Kündigungsfristen für das Hinzufügen eines Beliebigen Unterprozessors. Hinweis Zeitrahmen hängen von der Art der Daten ab, die der Unterverarbeiter im Auftrag von Microsoft verarbeitet. Wie in der DPA erwähnt, verpflichtet sich Microsoft, Kunden mindestens sechs Monate vor jedem neuen Unterverarbeiter, der Kundendaten verarbeitet, eine Benachrichtigung zu geben. Für alle anderen personenbezogenen Daten stellt Microsoft mindestens 30 Tage Benachrichtigung zur Verfügung. Hinweis wird durch das Update der Microsoft Online Services [Unterprozessorliste bereitgestellt.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Lieferantenverwaltung.

| **Externe Prüfungen** | **Section** | **Datum des letzten Berichts** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CA-3: Systemverbindungen <br> IA-4: Bezeichnerverwaltung <br> PS-6: Zugriffsvereinbarungen <br> PS-7: Sicherheit der Mitarbeiter von Drittanbietern <br> SA-4: Übernahmeprozess <br> SA-9: Externe Informationssystemdienste <br> SA-12: Schutz der Lieferkette | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Informationssicherheit in Lieferantenbeziehungen | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Informationssicherheit in Lieferantenbeziehungen | Februar 22, 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1: Offenlegung der Verarbeitung von personenbezogenen Daten von Unterauftragsaufträgen | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-53: Drittanbieterüberwachung | 24. Dezember 2020 |

## <a name="resources"></a>Ressourcen

- [Supplier Security Privacy and Assurance Program](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
