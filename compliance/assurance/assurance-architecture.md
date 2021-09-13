---
title: Architekturübersicht
description: Informationen zur Architektur in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
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
ms.openlocfilehash: 97fe615296f03c8f72dbf23d886501988686b53a
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159297"
---
# <a name="architecture-overview"></a>Architekturübersicht

## <a name="what-are-microsoft-online-services"></a>Was sind Microsoft-Onlinedienste?

Microsoft-Onlinedienste beziehen sich auf die cloudbasierten Dienste, die von Microsoft angeboten werden, einschließlich Azure, Dynamics 365 und Microsoft 365.  Jeder Dienst bietet einzigartige Lösungen für allgemeine Geschäftsbetriebs- und Produktivitätsanforderungen und bedient Kunden auf der ganzen Welt, von kleinen Unternehmen bis hin zu großen Unternehmen und Behörden. Global verteilte Rechenzentren, die mit der unabhängig verwalteten Netzwerkinfrastruktur von Microsoft verbunden sind, dienen als Backbone zur Unterstützung von Onlinediensten und bieten die Möglichkeit, die Verfügbarkeit in fast jeder Situation aufrechtzuerhalten und auf die massive weltweite Nachfrage zu skalieren.

Alle Microsoft-Onlinedienste haben das gleiche Ziel, die von ihnen verwalteten Dienstinfrastruktur und die Daten ihrer Kunden zu schützen, aber jeder Onlinedienst wird von einer separaten Geschäftseinheit betrieben. In vielen Fällen werden Sicherheitskontrollen in allen Diensten auf die gleiche Weise implementiert, aber in einigen Fällen verfolgen sie einen anderen Ansatz, um ihre Kundenzusagen und Complianceverpflichtungen zu erfüllen.

## <a name="what-is-azure"></a>Was ist Azure?

Microsoft Azure ist eine Cloud Computing-Plattform zum Erstellen, Bereitstellen und Verwalten von Anwendungen über ein globales Netzwerk von von Microsoft und von Drittanbietern verwalteten Rechenzentren. Es unterstützt sowohl Platform as a Service (PaaS) als auch Infrastructure as a Service (IaaS)-Clouddienstmodelle und ermöglicht Hybridlösungen, die Clouddienste in die lokalen Ressourcen der Kunden integrieren. Microsoft Azure unterstützt viele Kunden, Partner und Behörden, die sich über eine breite Palette von Produkten und Diensten, Regionen und Branchen erstrecken. Microsoft Azure ist darauf ausgelegt, ihre Sicherheits-, Vertraulichkeits- und Complianceanforderungen zu erfüllen.

## <a name="what-is-dynamics-365"></a>Was ist Dynamics 365?

Dynamics 365 ist eine Online-Business-Anwendungssuite, die die Crm-Funktionen (Customer Relationship Management) und deren Erweiterungen in die Erp-Funktionen (Enterprise Resource Planning) integriert. Diese End-to-End-Geschäftsanwendungen helfen Kunden, Beziehungen in Umsatz umzuwandeln, Kunden zu verdienen und das Unternehmensplus zu beschleunigen. Dynamics 365 ist eine SaaS-Suite (Software as a Service), die auf der Azure-Infrastruktur basiert und kunden weltweit über ihre global verteilten Rechenzentren zur Verfügung gestellt wird.

## <a name="what-is-microsoft-365"></a>Was ist Microsoft 365?

Microsoft 365 ist die cloudbasierte, abonnementbasierte Version von Office, Windows 10, Enterprise Mobility + Security und Compliance. Microsoft 365 Kunden Clients wie Outlook und Windows erhalten, und sie profitieren auch von Diensten, die Microsoft in ihrem Auftrag hostet, z. B. Exchange Online, Microsoft Teams und SharePoint Online. Alle Komponenten des Diensts werden regelmäßig als Teil des Abonnementmodells aktualisiert, sodass unsere Kunden über ein "evergreen"-Produkt verfügen. Microsoft verwaltet die Dienstinfrastruktur im Auftrag von Kunden, was bedeutet, dass Microsoft für die Sicherung der Infrastruktur verantwortlich ist, in der Kundendaten gespeichert sind.

Hinsichtlich der Skalierung verwendet Microsoft derzeit fast eine Million Computer, um Microsoft 365 Dienste zu unterstützen. Die Infrastruktur, die diese Dienste unterstützt, ist je nach dienstspezifischer Hardware und virtualisierten Umgebungen in Azure, Windows und Linux sowie auf mehreren Mandanten und dedizierten Plattformen sehr unterschiedlich. Microsoft 365 ist ein globales Unternehmen, und unsere Infrastruktur ist in Rechenzentren auf der ganzen Welt verteilt, so dass unsere Kunden die Anforderungen an die Datenspeicherung und Souveränität der Daten erfüllen können.

## <a name="how-do-microsoft-online-services-ensure-isolation-between-customer-tenants"></a>Wie stellen Microsoft-Onlinedienste die Isolierung zwischen Kundenmandanten sicher?

Die Clouddienste von Microsoft basieren auf der Annahme, dass alle Mandanten potenziell ungern gegenüber allen anderen Mandanten sind. Um Mandanten ordnungsgemäß voneinander zu isolieren, implementiert Microsoft verschiedene Isolationstechnologien und -steuerelemente. Diese Steuerelemente dienen zum Schutz vor Informationslecks oder unbefugtem Zugriff auf Kundendaten über Mandanten hinweg und um zu verhindern, dass die Aktionen eines Mandanten den Dienst für einen anderen Mandanten beeinträchtigen.

Kundeninhalte werden logisch innerhalb von Mandanten isoliert, indem Azure Active Directory (Azure AD) verwendet wird. Die Benutzerauthentifizierung in Microsoft-Onlinediensten überprüft nicht nur die Benutzeridentität, sondern auch die Mandantenidentität, zu der das Benutzerkonto gehört, und verhindert, dass Benutzer auf Daten außerhalb ihrer Mandantenumgebung zugreifen können. Um die logische Isolierung von Azure AD zu ergänzen, werden Kundeninhalte immer im Ruhezustand und während der Übertragung verschlüsselt. Einzelne Dienste können auch zusätzliche Ebenen der Mandantenisolation bereitstellen, z. B. SharePoint Onlineisolation von Mandantendaten in separaten, verschlüsselten Datenbanken.

## <a name="how-do-microsoft-online-services-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Wie entwickeln Microsoft-Onlinedienste ausfallsichere Dienste, die einzelne Fehlerquellen vermeiden?

Microsoft entwirft und erstellt Clouddienste, um die Zuverlässigkeit zu maximieren und die negativen Auswirkungen auf Kunden angesichts von Fehlern und Herausforderungen für den normalen Betrieb zu minimieren. Diese Strategie beginnt mit dem Entwurf des Netzwerks, das unsere geografisch verteilten Rechenzentren verbindet. Die Netzwerkarchitektur von Microsoft umfasst direkte Verbindungen und mehrere Netzwerkpfade. Microsoft-Onlinedienste verwenden diese Redundanz, um Datenverkehr automatisch an Fehler weiterzuleiten, um die Dienstqualität zu verbessern.

Nach Möglichkeit werden Microsoft-Onlinedienste in aktiven/aktiven Konfigurationen mit automatisierter Dienstintegritätsüberwachung bereitgestellt, sodass der Dienst viele häufige Fehler und Fehler ohne menschliches Eingreifen erkennen und beheben kann. Zusätzlich zu den aktiven/aktiven Konfigurationen erhöhen Microsoft-Onlinedienste die Fehlertoleranz, indem sichergestellt wird, dass der Dienst in separaten Fehlerzonen bereitgestellt wird, wodurch verhindert wird, dass ein Fehler in einer Zone die Verfügbarkeit anderer Zonen beeinträchtigt.

Die Datenresilienz ergänzt die Dienstresilienz durch den Schutz der Integrität und Verfügbarkeit von Daten in Microsoft-Onlinediensten. Unsere Dienste verwenden lokale Speicherredundanz und Georedundanz, um Kopien von Kundendaten in verschiedene Fehlerzonen zu replizieren. Wenn Daten in einer Ausfallzone beschädigt wurden oder verloren gegangen sind, kann darauf in einer anderen Ausfallzone zugegriffen werden, ohne dass es zu einer Unterbrechung bei der Verfügbarkeit kommt. Die automatische Integritätsprüfung stellt Daten, die von vielen Arten physischer oder logischer Beschädigung betroffen sind, automatisch wieder her. Microsoft bietet Kunden auch Tools zum Wiederherstellen versehentlich gelöschter oder geänderter Daten durch den Kunden in Diensten wie Exchange Online und SharePoint Online.

## <a name="how-do-microsoft-online-services-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Wie verfolgen Microsoft-Onlinedienste Abhängigkeiten und verhindern nicht autorisierte externe Systemverbindungen?

Microsoft Online Services-Teams identifizieren wichtige Systemkomponenten und deren Abhängigkeiten als Teil des Geschäftskontinuitätsmanagements. Darüber hinaus dokumentiert und verfolgt Microsoft alle externen Systemverbindungen, um sicherzustellen, dass nur autorisierte Verbindungen in Netzwerkfirewallkonfigurationen zulässig sind. Microsoft-Onlinedienstsysteme, Abhängigkeiten und externe Verbindungen sind in der Informationssicherheitsarchitektur von Microsoft-Onlinediensten dokumentiert. Sowohl die Informationssicherheitsarchitektur als auch die entsprechenden Datenflussdiagramme werden mindestens einmal jährlich überprüft und aktualisiert, sowie bei wichtigen Änderungen am System.

Die Architektur von Microsoft-Onlinediensten wird regelmäßig und automatisch mithilfe von cloudbasierten Tools überprüft, um die Übereinstimmung mit unseren Sicherheitsprinzipien zu überprüfen und die Isolations- und Resilienzfeatures kontinuierlich zu testen. Die Architekturüberprüfung dient zum automatischen Identifizieren von Instanzen, in denen der aktuelle Status des Diensts vom gewünschten Zustand abweicht, und kennzeichnet alle Abweichungen zur Überprüfung und Risikominderung. Das Ziel der Architekturüberprüfung besteht darin, sicherzustellen, dass die Sicherheitsfunktionen unserer Dienstinfrastruktur weiterhin wie erwartet funktionieren.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Architektur finden Sie in der folgenden Tabelle.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organisation der Informationssicherheit <br> A.13.1: Verwaltung der Netzwerksicherheit <br> A.17.2: Redundanzen | 2. Dezember 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organisation der Informationssicherheit <br> A.13.1: Verwaltung der Netzwerksicherheit <br> A.17.2: Redundanzen | 2. Dezember 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1: Geschäftskontinuitätspläne <br> BC-3: BCDR-Prozeduren <br> BC-4: BCDR-Tests <br> BC-5: Risikobewertungen der Geschäftskontinuität <br> BC-6: Geschäftskontinuität von Drittanbietern <br> BC-7: Geschäftskontinuitätsverfahren für Rechenzentren <br> BC-8: Geschäftskontinuitätstests für Rechenzentren <br> BC-9: Bewertung der Ausfallsicherheit von Rechenzentren <br>  DS-6: Redundanz wichtiger Komponenten <br> DS-7: Replikation von Kundendaten <br> DS-14: Wiederherstellung von Kundendiensten <br> DS-16: Trennung von Kundendaten | 31. März 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-4: Erzwingung des Informationsflusses <br> CP-9: Sicherung des Informationssystems <br> PL-8: Informationssicherheitsarchitektur <br> SC-7: Grenzschutz <br> SC-22: Architektur und Bereitstellung | 24. September 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organisation der Informationssicherheit <br> A.13.1: Verwaltung der Netzwerksicherheit <br> A.17.2: Redundanzen | 20. April 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: Mandantenisolation <br> CA-49: Sicherungsrichtlinien <br> CA-51: Datenreplikation | 24. Dezember 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: Datenflussdiagramme <br> CA-37: Mandantenisolation <br> CA-49: Sicherungsrichtlinien <br> CA-51: Datenreplikation | 24. Dezember 2020 |