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
ms.openlocfilehash: e1b4e9701e76c1e758f683750c8ebfeda2bc1f1f
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787487"
---
# <a name="architecture-overview"></a>Architekturübersicht

## <a name="what-is-microsoft-365"></a>Was ist Microsoft 365?

Microsoft 365 ist die cloudbasierte, abonnementbasierte Version von Office, Windows 10, Enterprise Mobility + Security und Compliance. Microsoft 365-Kunden erhalten Clients wie Outlook und Windows und profitieren auch von Diensten, die Microsoft in ihrem Namen hostet, wie Exchange Online, Microsoft Teams und SharePoint Online. Alle Komponenten des Diensts werden im Rahmen des Abonnementmodells regelmäßig aktualisiert, sodass unsere Kunden über ein "immergrünes" Produkt verfügen. Microsoft verwaltet die Dienstinfrastruktur im Auftrag von Kunden, d. h., Microsoft ist für die Sicherung der Infrastruktur verantwortlich, in der Kundendaten gespeichert werden.

Im Hinblick auf die Skalierung verwenden wir derzeit fast eine Million Computer, um Microsoft 365-Dienste zu nutzen. Die Infrastruktur, die diese Dienste unterstützt, variiert stark zwischen dienstspezifischen Hardware- und virtualisierten Umgebungen in Azure, Windows und Linux sowie mehr mandanten- und dedizierten Plattformen. Microsoft 365 ist ein globales Unternehmen, und unsere Infrastruktur ist in Rechenzentren auf der ganzen Welt verteilt, so dass unsere Kunden die Anforderungen an die Datenspeicherung und Souveränität der Daten erfüllen können.

Kurz gesagt, der Dienst ist komplex, wird im großen Maßstab ausgeführt und erfordert Tausende von Microsoft-Technikern, um zu erstellen und zu warten. Es ist unsere höchste Priorität für uns, diese Infrastruktur zu schützen.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Wie stellt Microsoft 365 die Isolation zwischen kundenorientierten Mandanten sicher?

Die Clouddienste von Microsoft bauen auf der Annahme auf, dass alle Mandanten potenziell gegen alle anderen Mandanten verwächslich sind. Um Mandanten ordnungsgemäß voneinander zu isolieren, implementiert Microsoft eine Vielzahl von Isolationstechnologien und -kontrollen. Diese Steuerelemente sind so konzipiert, dass sie vor Informationslecks oder unbefugtem Zugriff auf Kundendaten mandantenübergreifend schützen und verhindern, dass die Aktionen eines Mandanten den Dienst für einen anderen Mandanten beeinträchtigen.

Kundeninhalte werden innerhalb von Microsoft 365-Mandanten mithilfe von Azure Active Directory (Azure AD) logisch isoliert. Die Benutzerauthentifizierung in Microsoft 365 überprüft nicht nur die Benutzeridentität, sondern auch die Mandantenidentität, der das Benutzerkonto angehört, wodurch verhindert wird, dass Benutzer auf Daten außerhalb Ihrer Mandantenumgebung zugreifen. Zur Ergänzung der logischen Isolierung von Azure AD werden Kundeninhalte immer im ruhen und während der Übertragung verschlüsselt. Einzelne Dienste können auch zusätzliche Ebenen der Mandantenisolation bereitstellen, z. B. die SharePoint Online-Isolation von Mandantendaten in separaten, verschlüsselten Datenbanken.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Wie entwickelt Microsoft 365 ausfallsichere Dienste, die einzelne Fehlerstellen vermeiden?

Microsoft entwirft und erstellt Clouddienste, um die Zuverlässigkeit zu maximieren und negative Auswirkungen auf Kunden bei Fehlern und Herausforderungen im normalen Betrieb zu minimieren. Diese Strategie beginnt mit dem Entwurf des Netzwerks, das unsere geografisch verteilten Rechenzentren verbindet. Die Netzwerkarchitektur von Microsoft umfasst direkte Verbindungen und mehrere Netzwerkpfade. Microsoft 365-Dienste nutzen diese Redundanz, um Datenverkehr automatisch um Fehler weiter zu routen, um die Dienstqualität zu verbessern.

Auf Dienstebene priorisiert die Ausfallsicherheitsstrategie von Microsoft 365 die Softwareresilienz. Wenn möglich, werden unsere Dienste in aktiv/aktiv-Konfigurationen mit automatisierter Dienstinte health monitoring bereitgestellt, sodass der Dienst viele häufige Fehler und Fehler ohne menschliches Eingreifen erkennen und wiederherstellen kann. Zusätzlich zu aktiven/aktiven Konfigurationen erhöhen Microsoft 365-Dienste die Fehlertoleranz, indem sichergestellt wird, dass der Dienst in separaten Fehlerzonen bereitgestellt wird, sodass ein Fehler in einer Zone die Verfügbarkeit anderer Zonen nicht beeinträchtigt.

Die Datenresilienz ergänzt die Dienstresilienz durch die Wahrung der Integrität und Verfügbarkeit von Daten in Microsoft 365-Diensten. Unsere Dienste verwenden lokale Speicherredundanz und Georedundanz, um Kopien von Kundendaten in verschiedene Fehlerzonen zu replizieren. Wenn Daten in einer Ausfallzone beschädigt wurden oder verloren gegangen sind, kann darauf in einer anderen Ausfallzone zugegriffen werden, ohne dass es zu einer Unterbrechung bei der Verfügbarkeit kommt. Durch die automatische Integritätsprüfung werden daten, die von vielen Arten von physischen oder logischen Beschädigungen betroffen sind, automatisch wiederhergestellt. Microsoft 365 bietet Kunden auch Tools zum Wiederherstellen von Daten, die versehentlich vom Kunden in Exchange Online und SharePoint Online gelöscht oder geändert wurden.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Wie verfolgt Microsoft 365 Abhängigkeiten nach und verhindert nicht autorisierte externe Systemverbindungen?

Microsoft 365-Serviceteams identifizieren wichtige Systemkomponenten und deren Abhängigkeiten als Teil des Geschäftskontinuitätsmanagements. Darüber hinaus dokumentiert Und verfolgt Microsoft 365 alle externen Systemverbindungen, um sicherzustellen, dass nur autorisierte Verbindungen in Netzwerkfirewallkonfigurationen zulässig sind. Microsoft 365-Systeme, Abhängigkeiten und externe Verbindungen sind in der Informationssicherheitsarchitektur von Microsoft 365 dokumentiert. Sowohl die Informationssicherheitsarchitektur als auch die entsprechenden Datenflussdiagramme werden jährlich mindestens einmal jährlich überprüft und aktualisiert sowie immer dann, wenn erhebliche Änderungen am System vorgenommen werden.

Die Microsoft 365-Architektur wird regelmäßig und automatisch mithilfe cloudbasierter Tools überprüft, um die Übereinstimmung mit unseren Sicherheitsprinzipien zu überprüfen und Isolations- und Ausfallsicherheitsfeatures kontinuierlich zu testen. Die Architekturüberprüfung identifiziert automatisch Instanzen, bei denen der aktuelle Status des Diensts vom gewünschten Zustand abweicht, und zeigt alle Abweichungen zur Überprüfung und Risikominderung an. Das Ziel der Architekturüberprüfung ist es, sicherzustellen, dass die Sicherheitsfunktionen unserer Dienstinfrastruktur weiterhin wie erwartet funktionieren.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Bestimmungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf Einhaltung externer Bestimmungen und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Architektur von Microsoft 365.

| **Externe Überwachungen** | **Section** | **Datum des letzten Berichts** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: Erzwingung des Informationsflusses <br> CP-9: Sicherung des Informationssystems <br> PL-8: Architektur der Informationssicherheit <br> SC-7: Grenzschutz <br> SC-22: Architektur und Bereitstellung | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organisation der Informationssicherheit <br> A.13.1: Verwaltung der Netzwerksicherheit <br> A.17.2: Redundanzen | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organisation der Informationssicherheit <br> A.13.1: Verwaltung der Netzwerksicherheit | Februar 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: Mandantenisolation <br> CA-49: Sicherungsrichtlinien <br> CA-51: Datenreplikation | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: Datenflussdiagramme <br> CA-37: Mandantenisolation <br> CA-49: Sicherungsrichtlinien <br> CA-51: Datenreplikation | 24. Dezember 2020 |