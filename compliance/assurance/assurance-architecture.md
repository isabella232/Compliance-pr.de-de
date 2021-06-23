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
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 9af5296cce34db6362638f025f38315f2e1d7b05
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088534"
---
# <a name="architecture-overview"></a>Architekturübersicht

## <a name="what-is-microsoft-365"></a>Was ist Microsoft 365?

Microsoft 365 ist die cloudbasierte, abonnementbasierte Version von Office, Windows 10, Enterprise Mobility + Security und Compliance. Microsoft 365 Kunden Clients wie Outlook und Windows erhalten, und sie profitieren auch von Diensten, die Microsoft in ihrem Auftrag hostet, z. B. Exchange Online, Microsoft Teams und SharePoint Online. Alle Komponenten des Diensts werden regelmäßig als Teil des Abonnementmodells aktualisiert, sodass unsere Kunden über ein "evergreen"-Produkt verfügen. Microsoft verwaltet die Dienstinfrastruktur im Auftrag von Kunden, was bedeutet, dass Microsoft für die Sicherung der Infrastruktur verantwortlich ist, in der Kundendaten gespeichert sind.

Hinsichtlich der Skalierung verwenden wir derzeit fast eine Million Computer, um Microsoft 365 Dienste zu unterstützen. Die Infrastruktur für diese Dienste variiert je nach dienstspezifischer Hardware und virtualisierten Umgebungen in Azure, Windows und Linux sowie auf mehreren Mandanten und dedizierten Plattformen. Microsoft 365 ist ein globales Unternehmen, und unsere Infrastruktur ist in Rechenzentren auf der ganzen Welt verteilt, so dass unsere Kunden die Anforderungen an die Datenspeicherung und Souveränität der Daten erfüllen können.

Kurz gesagt, der Dienst ist komplex, wird in großem Umfang ausgeführt und erfordert Tausende von Microsoft-Technikern, die erstellt und gewartet werden müssen. Es ist unsere oberste Priorität, diese gesamte Infrastruktur zu schützen.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Wie stellt Microsoft 365 die Isolierung zwischen Kundenmandanten sicher?

Die Clouddienste von Microsoft basieren auf der Annahme, dass alle Mandanten potenziell ungern gegenüber allen anderen Mandanten sind. Um Mandanten ordnungsgemäß voneinander zu isolieren, implementiert Microsoft eine Vielzahl von Isolationstechnologien und -kontrollen. Diese Steuerelemente dienen zum Schutz vor Informationslecks oder nicht autorisiertem Zugriff auf Kundendaten über Mandanten hinweg und um zu verhindern, dass die Aktionen eines Mandanten den Dienst für einen anderen Mandanten beeinträchtigen.

Kundeninhalte werden logisch innerhalb Microsoft 365 Mandanten mithilfe von Azure Active Directory (Azure AD) isoliert. Die Benutzerauthentifizierung in Microsoft 365 überprüft nicht nur die Benutzeridentität, sondern auch die Mandantenidentität, der das Benutzerkonto angehört, wodurch verhindert wird, dass Benutzer auf Daten außerhalb Ihrer Mandantenumgebung zugreifen. Um die logische Isolierung von Azure AD zu ergänzen, werden Kundeninhalte immer im Ruhezustand und während der Übertragung verschlüsselt. Einzelne Dienste können auch zusätzliche Ebenen der Mandantenisolation bereitstellen, z. B. SharePoint Onlineisolation von Mandantendaten in separaten, verschlüsselten Datenbanken.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Wie entwickelt Microsoft 365 ausfallsichere Dienste, die einzelne Fehlerquellen vermeiden?

Microsoft entwirft und erstellt Clouddienste, um die Zuverlässigkeit zu maximieren und die negativen Auswirkungen auf Kunden angesichts von Fehlern und Herausforderungen für den normalen Betrieb zu minimieren. Diese Strategie beginnt mit dem Entwurf des Netzwerks, das unsere geografisch verteilten Rechenzentren verbindet. Die Netzwerkarchitektur von Microsoft umfasst direkte Verbindungen und mehrere Netzwerkpfade. Microsoft 365 Dienste nutzen diese Redundanz, um Datenverkehr automatisch an Fehler weiterzuleiten, um die Dienstqualität zu verbessern.

Auf Dienstebene priorisiert die Resilienzstrategie Microsoft 365 die Softwareresilienz. Wenn möglich, werden unsere Dienste in aktiven/aktiven Konfigurationen mit automatisierter Dienstintegritätsüberwachung bereitgestellt, sodass der Dienst viele häufige Fehler und Fehler ohne menschliches Eingreifen erkennen und wiederherstellen kann. Zusätzlich zu aktiven/aktiven Konfigurationen erhöhen Microsoft 365 Dienste die Fehlertoleranz, indem sichergestellt wird, dass der Dienst in separaten Fehlerzonen bereitgestellt wird, um zu verhindern, dass ein Fehler in einer Zone die Verfügbarkeit anderer Zonen beeinflusst.

Die Datenresilienz ergänzt die Dienstresilienz durch die Wahrung der Integrität und Verfügbarkeit von Daten in Microsoft 365-Diensten. Unsere Dienste verwenden lokale Speicherredundanz und Georedundanz, um Kopien von Kundendaten in verschiedene Fehlerzonen zu replizieren. Wenn Daten in einer Ausfallzone beschädigt wurden oder verloren gegangen sind, kann darauf in einer anderen Ausfallzone zugegriffen werden, ohne dass es zu einer Unterbrechung bei der Verfügbarkeit kommt. Die automatische Integritätsprüfung stellt Daten, die von vielen Arten physischer oder logischer Beschädigung betroffen sind, automatisch wieder her. Microsoft 365 bietet Kunden auch Tools zum Wiederherstellen versehentlich gelöschter oder geänderter Daten in Exchange Online und SharePoint Online.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Wie verfolgt Microsoft 365 Abhängigkeiten und verhindert nicht autorisierte externe Systemverbindungen?

Microsoft 365 Serviceteams identifizieren wichtige Systemkomponenten und deren Abhängigkeiten im Rahmen der Geschäftskontinuitätsverwaltung. Darüber hinaus Microsoft 365 alle externen Systemverbindungen dokumentiert und verfolgt, um sicherzustellen, dass nur autorisierte Verbindungen in Netzwerkfirewallkonfigurationen zulässig sind. Microsoft 365 Systeme, Abhängigkeiten und externen Verbindungen sind in der Informationssicherheitsarchitektur Microsoft 365 dokumentiert. Sowohl die Informationssicherheitsarchitektur als auch die entsprechenden Datenflussdiagramme werden mindestens einmal jährlich überprüft und aktualisiert, sowie bei wichtigen Änderungen am System.

Microsoft 365 Architektur wird regelmäßig und automatisch mithilfe von cloudbasierten Tools überprüft, um die Übereinstimmung mit unseren Sicherheitsprinzipien zu überprüfen und Isolations- und Resilienzfeatures kontinuierlich zu testen. Die Architekturüberprüfung dient zum automatischen Identifizieren von Instanzen, in denen der aktuelle Status des Diensts vom gewünschten Zustand abweicht, und kennzeichnet alle Abweichungen zur Überprüfung und Risikominderung. Das Ziel der Architekturüberprüfung besteht darin, sicherzustellen, dass die Sicherheitsfunktionen unserer Dienstinfrastruktur weiterhin wie erwartet funktionieren.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Architektur von Microsoft 365.

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: Erzwingung des Informationsflusses <br> CP-9: Sicherung des Informationssystems <br> PL-8: Informationssicherheitsarchitektur <br> SC-7: Grenzschutz <br> SC-22: Architektur und Bereitstellung | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organisation der Informationssicherheit <br> A.13.1: Verwaltung der Netzwerksicherheit <br> A.17.2: Redundanzen | 20. April 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organisation der Informationssicherheit <br> A.13.1: Verwaltung der Netzwerksicherheit | 20. April 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: Mandantenisolation <br> CA-49: Sicherungsrichtlinien <br> CA-51: Datenreplikation | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: Datenflussdiagramme <br> CA-37: Mandantenisolation <br> CA-49: Sicherungsrichtlinien <br> CA-51: Datenreplikation | 24. Dezember 2020 |