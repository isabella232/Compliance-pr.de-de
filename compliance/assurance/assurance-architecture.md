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
ms.openlocfilehash: 7ceceb59d0afcbc72fac9758f3de500082b8b365
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507117"
---
# <a name="architecture-overview"></a>Architekturübersicht

## <a name="what-is-microsoft-365"></a>Was ist Microsoft 365?

Microsoft 365 ist die in der Cloud unterstützte, abonnementbasierte Version von Office, Windows 10, Enterprise Mobility + Security und Compliance. Microsoft 365-Kunden erhalten Clients wie Outlook und Windows, und Sie profitieren auch von Diensten, die Microsoft in Ihrem Namen hostet, beispielsweise Exchange Online, Microsoft Teams und SharePoint Online. Alle Komponenten des Diensts werden regelmäßig im Rahmen des Abonnementmodells aktualisiert, sodass unsere Kunden ein "Evergreen"-Produkt haben. Microsoft verwaltet die Dienstinfrastruktur im Auftrag von Kunden, was bedeutet, dass Microsoft für die Sicherung der Infrastruktur zuständig ist, in der Kundendaten gespeichert sind.

Im Hinblick auf die Skalierung verwenden wir derzeit nahezu eine Million Computer, um Microsoft 365-Dienste zu nutzen. Die Infrastruktur, die diese Dienste durchmacht, variiert weitgehend in der dienstspezifischen Hardware und virtualisierten Umgebungen in Azure, Windows und Linux sowie in mehrmandantenfähigen und dedizierten Plattformen. Microsoft 365 ist ein globales Unternehmen, und unsere Infrastruktur ist in Rechenzentren auf der ganzen Welt verteilt, so dass unsere Kunden die Anforderungen an die Datenspeicherung und Souveränität der Daten erfüllen können.

Kurz gesagt, der Dienst ist komplex, wird in unglaublicher Größenordnung ausgeführt und erfordert Tausende von Microsoft-Ingenieuren für die Erstellung und Verwaltung. Für uns ist es oberste Priorität, diese Infrastruktur sicher zu halten.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Wie gewährleistet Microsoft 365 die Isolierung zwischen Kundenmandanten?

Die Cloud-Dienste von Microsoft basieren auf der Annahme, dass alle Mandanten potenziell für alle anderen Mandanten feindlich sind. Um Mandanten ordnungsgemäß voneinander zu isolieren, implementiert Microsoft eine Vielzahl von Isolations Technologien und-Steuerelementen. Diese Steuerelemente dienen dem Schutz vor Informationsverlusten oder nicht autorisiertem Zugriff auf Kundendaten über Mandanten hinweg und verhindern, dass sich die Aktionen eines Mandanten negativ auf den Dienst für einen anderen Mandanten auswirken.

Kunden Inhalte werden in Microsoft 365-Mandanten mithilfe von Azure Active Directory (Azure AD) logisch isoliert. Die Benutzerauthentifizierung in Microsoft 365 überprüft nicht nur die Benutzeridentität, sondern auch die Mandantenidentität, der das Benutzerkonto angehört, wodurch verhindert wird, dass Benutzer auf Daten außerhalb Ihrer Mandantenumgebung zugreifen. Um die logische Isolierung von Azure AD zu ergänzen, werden Kunden Inhalte immer im Ruhezustand und bei der Übertragung verschlüsselt. Einzelne Dienste bieten möglicherweise auch zusätzliche Ebenen der mandantenisolation, beispielsweise SharePoint Online Isolierung von Mandantendaten in getrennten, verschlüsselten Datenbanken.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Wie funktioniert Microsoft 365-Techniker, die ausfallsichere Dienste vermeiden, die einzelne Fehlerpunkte vermeiden?

Microsoft entwickelt und erstellt Cloud-Dienste, um die Zuverlässigkeit zu maximieren und die negativen Auswirkungen auf die Kunden angesichts von Fehlern und Herausforderungen für normale Vorgänge zu minimieren. Diese Strategie beginnt mit dem Entwurf des Netzwerks, das unsere geografisch verteilten Rechenzentren verbindet. Die Netzwerkarchitektur von Microsoft umfasst direkte Verbindungen und mehrere Netzwerkpfade. Microsoft 365-Dienste nutzen diese Redundanz, um den Datenverkehr automatisch um Fehler zu leiten, um die Dienstqualität zu verbessern.

Auf Dienstebene priorisiert die Sicherheitsstrategie von Microsoft 365 die Ausfallsicherheit von Software. Wo immer möglich, werden unsere Dienste in Active/Active-Konfigurationen mit automatischer Dienst Integritätsüberwachung bereitgestellt, sodass der Dienst viele häufige Fehler und Fehler ohne menschlichen Eingriff erkennen und wiederherstellen kann. Zusätzlich zu den Active/Active-Konfigurationen erhöht Microsoft 365 Services die Fehlertoleranz, indem sichergestellt wird, dass der Dienst in separaten Fehler Zonen bereitgestellt wird, wodurch verhindert wird, dass ein Fehler in einer Zone die Verfügbarkeit anderer Zonen beeinträchtigt.

Die Datenresilienz ergänzt die Dienstresilienz durch die Wahrung der Integrität und Verfügbarkeit von Daten in Microsoft 365-Diensten. Unsere Dienste verwenden lokale Speicherredundanz und Geo-Redundanz, um Kopien von Kundendaten in unterschiedliche Fehler Zonen zu replizieren. Wenn Daten in einer Ausfallzone beschädigt wurden oder verloren gegangen sind, kann darauf in einer anderen Ausfallzone zugegriffen werden, ohne dass es zu einer Unterbrechung bei der Verfügbarkeit kommt. Bei der automatischen Integritätsüberprüfung werden Daten, die durch viele Arten physischer oder logischer Beschädigungen beeinträchtigt werden, automatisch wiederhergestellt. Microsoft 365 bietet Kunden auch Tools zum Wiederherstellen von Daten, die versehentlich gelöscht oder vom Kunden in Exchange Online und SharePoint Online geändert wurden.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Wie verfolgt Microsoft 365 Abhängigkeiten und verhindert nicht autorisierte externe Systemverbindungen?

Microsoft 365-Dienst Teams identifizieren wichtige Systemkomponenten und deren Abhängigkeiten im Rahmen der Business Continuity-Verwaltung. Darüber hinaus dokumentiert und überwacht Microsoft 365 alle externen Systemverbindungen, um sicherzustellen, dass nur autorisierte Verbindungen in Netzwerkfirewall-Konfigurationen zulässig sind. Microsoft 365-Systeme,-Abhängigkeiten und externe Verbindungen sind in der Microsoft 365-Architektur für Informationssicherheit dokumentiert. Sowohl die Informationssicherheitsarchitektur als auch entsprechende Datenfluss Diagramme werden mindestens einmal jährlich überprüft und aktualisiert, sowie wenn erhebliche Änderungen am System vorgenommen werden.

Die Microsoft 365-Architektur wird regelmäßig und automatisch mithilfe von Cloud-basierten Tools validiert, um die Übereinstimmung mit unseren Sicherheitsprinzipien zu überprüfen und die Isolations-und Ausfallsicherheit-Features kontinuierlich zu testen. Durch die Architektur Überprüfung werden Instanzen automatisch identifiziert, bei denen der aktuelle Status des Diensts vom gewünschten Zustand abgewichen ist, wobei etwaige Abweichungen zur Überprüfung und Minderung gekennzeichnet werden. Das Ziel der Architektur Überprüfung besteht darin, sicherzustellen, dass die Sicherheitsfunktionen unserer Dienstinfrastruktur weiterhin wie erwartet funktionieren.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Verordnungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Bestimmungen und Zertifizierungen überprüft. In der folgenden Tabelle erhalten Sie Informationen zur Validierung von Steuerelementen im Zusammenhang mit der Architektur von Microsoft 365.

| **Externe Überprüfungen** | **Section** | **Letztes Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: Durchsetzung des Informationsflusses <br> CP-9: Information System-Sicherung <br> PL-8: Architektur der Informationssicherheit <br> SC-7: Grenzschutz <br> SC-22: Architektur und proprovisionierung | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 6: Organisation der Informationssicherheit <br> A. 13.1: Netzwerk Sicherheitsverwaltung <br> A. 17.2: Redundanzen | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 6: Organisation der Informationssicherheit <br> A. 13.1: Netzwerk Sicherheitsverwaltung | Februar 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-37: Mandanten Isolierung <br> CA-49: Sicherungsrichtlinien <br> CA-51: Datenreplikation | 30. September 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-05: Datenfluss Diagramme <br> CA-37: Mandanten Isolierung <br> CA-49: Sicherungsrichtlinien <br> CA-51: Datenreplikation | 30. September 2019 |