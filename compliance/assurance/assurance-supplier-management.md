---
title: Lieferantenmanagement (Übersicht)
description: Informationen zum Lieferantenmanagement in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH'
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 8367f147e9d0e02ad76d97c665ad66559a743d06
ms.sourcegitcommit: 1f30616328d7deb04e41dcbd44a330ea937fe94f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2021
ms.locfileid: "60582505"
---
# <a name="supplier-management-overview"></a>Lieferantenmanagement (Übersicht)

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Wie verwaltet Microsoft Risiken im Zusammenhang mit Lieferanten?

Microsoft arbeitet mit Drittanbietern zusammen, um die Anforderungen unserer Kunden zu erfüllen. Diese Drittanbieter werden als Lieferanten oder Unterauftragsverarbeiter bezeichnet. Sicherheit und Datenschutz von Lieferanten bei Microsoft unterliegen unserem [Supplier Security and Privacy Assurance (SSPA)-Programm,](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)einem unternehmensweiten Satz von Anforderungen für alle Lieferanten, die mit Microsoft zusammenarbeiten, um unsere Onlinedienste bereitzustellen. Während das SSPA-Programm eine umfassende Steuerung und Verwaltung unserer Lieferantenbasis bietet, können einzelne Geschäftseinheiten zusätzliche Anforderungen für ihre Lieferanten beibehalten.

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Wie schützt das SSPA-Programm (Supplier Security and Privacy Assurance) von Microsoft Kundendaten?

SSPA ist eine Partnerschaft zwischen Microsoft Beschaffung, externer und rechtlicher Fragen von Unternehmen und Unternehmenssicherheit, um sicherzustellen, dass Lieferanten die Datenschutz- und Sicherheitsprinzipien von Microsoft einhalten. Der Umfang des SSPA gilt für alle Lieferanten, die personenbezogene Daten oder vertrauliche Microsoft-Daten verarbeiten. Die Registrierung des SSPA-Programms umfasst die Einhaltung der Datenschutzanforderungen (Data Protection Requirements, DPR) von Microsoft. Die DpR besteht aus Sicherheits- und Datenschutzkontrollen, die Lieferanten implementieren müssen, bevor sie mit der Vertragsarbeit mit Microsoft beginnen. Alle registrierten Lieferanten bestätigen jährlich die Einhaltung der DPR.

Die DPR-Anforderungen basieren auf sechs unterschiedlichen Datenverarbeitungskategorien, für die ein Lieferant im Rahmen seiner Registrierung bei SSPA genehmigt werden kann. Diese Kategorien werden verwendet, um das Risiko im Zusammenhang mit den Diensten zu identifizieren, die ein Lieferant für Microsoft bereitstellt. Das Datenverarbeitungsprofil des Lieferanten bestimmt, welche DPR-Kontrollen als im Umfang berücksichtigt werden, um einen geeigneten Datenschutz zu gewährleisten. Lieferanten, die Daten verarbeiten, die als ein höheres Risiko betrachtet werden, müssen alle DPR-Anforderungen erfüllen und müssen möglicherweise auch eine unabhängige Überprüfung der Compliance bereitstellen. Microsoft-Einkaufstools überprüfen den SSPA-Status aller Lieferanten, einschließlich der Einhaltung der geltenden Teile der DPR, bevor die Beschaffung dieses Lieferanten zugelassen wird.

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>Welche Arten von Unterauftragsverarbeitern bieten Dienste für Microsoft an?

Ein "Unterauftragsverarbeiter" ist ein Drittanbieter, den Microsoft einnimmt, dessen Aufgaben die Verarbeitung personenbezogener Daten von Microsoft umfassen, für die Microsoft ein Auftragsverarbeiter ist. Die Unterauftragsverarbeiter von Microsoft werden in drei unterschiedliche Kategorien unterteilt. Jede muss die Einhaltung der SSPA nachweisen, bevor sie Kundendaten im Auftrag von Microsoft verarbeiten können.

- **Technologie**-Unterauftragsverarbeiter bieten Technologien an, die zur Bereitstellung spezieller Microsoft-Onlinedienste verwendet werden. Wenn ein Kunde einen dieser Dienste bereitstellt, können die für diesen Dienst identifizierten Unterauftragsverarbeiter Kundendaten oder personenbezogene Daten verarbeiten, speichern oder anderweitig darauf zugreifen und dabei helfen, diesen Dienst bereitzustellen.
- **Zusätzliche** Unterauftragsverarbeiter stellen Dienste bereit, die die Onlinedienste unterstützen, betreiben und verwalten. Wenn ein Kunde einen dieser Dienste bereitstellt, können die identifizierten Unterauftragsverarbeiter eingeschränkte Kundendaten oder personenbezogene Daten verarbeiten, speichern oder anderweitig darauf zugreifen, während sie ihre zusätzlichen Dienste bereitstellen.
- Unterauftragsverarbeiter für die **Personalerweiterung** haben zwei unterschiedliche Formen: In beiden Szenarien befinden sich personenbezogene Daten nur in Microsoft-Einrichtungen, auf Microsoft-Systemen und unterliegen den Richtlinien und der Aufsicht von Microsoft.

    - Bei der ersten Form eines Personalaugmentations-Unterauftragsverarbeiters stellt dieser Personal zum Unterstützen, Betreiben und Verwalten von Microsoft-Onlinediensten bereit. Bei der Erfüllung ihrer Aufgaben können diese Unterauftragsverarbeiter möglicherweise auf Kunden- oder personenbezogene Daten zugreifen. So kann beispielsweise ein Unterauftragsverarbeiter eine Remoteproblembehandlung auf einem Microsoft-Server durchführen, in deren Verlauf Ausschnitte von Kundendaten in einem Serverabsturz-Speicherabbildprotokoll verfügbar werden können.
    - Die zweite Form der Personalerweiterung umfasst Unterauftragsverarbeiter, die parallel zu Microsoft-Vollzeitmitarbeitern arbeiten, um Microsoft-Onlinedienste zu unterstützen, zu betreiben und zu warten. Diese Unterauftragsverarbeiter können im Rahmen ihrer Zusammenarbeit mit Microsoft-Vollzeitmitarbeitern möglicherweise auf pseudonymisierte Daten zugreifen.

Technologie- und Hilfsunterauftragsverarbeiter sind erforderlich, um Zugriffskontrollen in Übereinstimmung mit den Datenschutzanforderungen (Data Protection Requirements, DPR) von Microsoft zu implementieren. Diese Anforderungen erfüllen oder überschreiten die vertraglichen Verpflichtungen, die Microsoft gegenüber seinen Kunden in den Onlinedienstbedingungen (ONLINE Service Terms, OST) eingeht. Lieferanten, die Personalerweiterungen durchführen, unterliegen den gleichen Zugriffssteuerungen für Vollzeitmitarbeiter von Microsoft.

## <a name="how-does-microsoft-onboard-suppliers"></a>Wie integriert Microsoft Lieferanten?

Drittanbieter müssen im Rahmen des Onboardings eine Microsoft-Mastervereinbarung unterzeichnen. Dieser Vertrag regelt die Beziehung zwischen Microsoft und seinen Lieferanten und stellt eine konsistente Verwaltung der Lieferantenbeziehungen sicher. Im Rahmen des Onboardings registrieren sich Lieferanten beim SSPA und müssen alle geltenden Anforderungen erfüllen, bevor sie für alle Datenverarbeitungskategorien genehmigt werden können. Microsoft-Geschäftseinheiten sind nur in der Lage, Interaktionen mit Lieferanten zu erstellen, wenn die Datenverarbeitungsaktivität für das Engagement mit den Datenverarbeitungskategorien übereinstimmt, für die der Lieferant genehmigt wurde.

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Wie benachrichtigt Microsoft Kunden über Änderungen an Lieferanten, die ihre Daten verarbeiten?

Gemäß dem Microsoft Online Service Data Protection-Nachtrag (Data Protection Addendum, DPA) unternimmt Microsoft zusätzliche Verpflichtungen hinsichtlich der Benachrichtigungszeiträume für die Hinzufügung von Unterauftragsverarbeitern. Beachten Sie, dass Zeitrahmen von der Art der Daten abhängen, die der Unterauftragsverarbeiter im Auftrag von Microsoft verarbeitet. Wie in der Datenschutzbehörde angegeben, verpflichtet sich Microsoft, Kunden mindestens sechs Monate vor jedem neuen Unterauftragsverarbeiter, der Kundendaten verarbeiten wird, eine Benachrichtigung zu übermitteln. Für alle anderen personenbezogenen Daten wird Microsoft mindestens 30 Tage im Voraus informieren. Beachten Sie das Update der [Microsoft Online Services-Unterauftragsverarbeiterliste.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=ede6342e-d641-4a9b-9162-7d66025003b0&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. Die Validierung von Steuerelementen im Zusammenhang mit der Lieferantenverwaltung finden Sie in der folgenden Tabelle.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|  
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Informationssicherheit in Lieferantenbeziehungen | 2. Dezember 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Informationssicherheit in Lieferantenbeziehungen | 2. Dezember 2020 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1: Offenlegung der verarbeitung von untervergebenen personenbezogenen Informationen | 2. Dezember 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | SOC2-25: Lieferantenrisikomanagement <br> C5-2: Überprüfung des Lieferantenrisikoprofils| 31. März 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CA-3: Systemverbindungen <br> IA-4: Bezeichnerverwaltung <br> PS-6: Zugriffsvereinbarungen <br> PS-7: Sicherheit des Personals von Drittanbietern <br> SA-4: Käufeprozess <br> SA-9: Externe Informationssystem-Dienste <br> SA-12: Lieferkettenschutz | 24. September 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1: Informationssicherheit in Lieferantenbeziehungen | 20. April 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.8.1: Offenlegung der verarbeitung von untervergebenen personenbezogenen Informationen | 24. Dezember 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-53: Überwachung durch Drittanbieter | 24. Dezember 2020 |

## <a name="resources"></a>Ressourcen

- [Supplier Security Privacy and Assurance-Programm](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
