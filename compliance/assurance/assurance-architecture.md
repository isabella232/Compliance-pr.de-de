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
ms.openlocfilehash: 423e90164b3c13c53d45ca98c2e1a981968f23a8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497696"
---
# <a name="architecture-overview"></a>Architekturübersicht

## <a name="what-is-microsoft-365"></a>Was ist Microsoft 365?

Microsoft 365 ist die cloudbasierte abonnementbasierte Version von Office, Windows 10, Enterprise Mobility + Security und Compliance. Microsoft 365-Kunden erhalten Clients wie Outlook und Windows und profitieren auch von Diensten, die Microsoft in ihrem Namen hostet, z. B. Exchange Online, Microsoft Teams und SharePoint Online. Alle Komponenten des Diensts werden im Rahmen des Abonnementmodells regelmäßig aktualisiert, sodass unsere Kunden über ein "immergrünes" Produkt verfügen. Microsoft verwaltet die Dienstinfrastruktur im Auftrag von Kunden, was bedeutet, dass Microsoft für die Sicherung der Infrastruktur verantwortlich ist, in der Kundendaten gespeichert werden.

Im Hinblick auf die Skalierung verwenden wir derzeit fast eine Million Computer, um Microsoft 365-Dienste zu nutzen. Die Infrastruktur, in der diese Dienste bereitgestellt werden, variiert stark zwischen dienstspezifischen Hardware- und virtualisierten Umgebungen in Azure, Windows und Linux sowie mehr mandanten- und dedizierten Plattformen. Microsoft 365 ist ein globales Unternehmen, und unsere Infrastruktur ist in Rechenzentren auf der ganzen Welt verteilt, so dass unsere Kunden die Anforderungen an die Datenspeicherung und Souveränität der Daten erfüllen können.

Kurz gesagt, der Dienst ist komplex, wird in einem unglaublichen Umfang ausgeführt und erfordert Tausende von Microsoft-Technikern zum Erstellen und Warten. Es ist unsere oberste Priorität, dass wir alle diese Infrastruktur schützen.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Wie stellt Microsoft 365 die Isolation zwischen Kunden mandanten sicher?

Die Clouddienste von Microsoft bauen auf der Annahme auf, dass alle Mandanten potenziell schädlich für alle anderen Mandanten sind. Um Mandanten ordnungsgemäß voneinander zu isolieren, implementiert Microsoft eine Vielzahl von Isolationstechnologien und -steuerelementen. Diese Steuerelemente sollen vor Informationslecks oder unbefugtem Zugriff auf Kundendaten über Mandanten hinweg hinweg schützen und verhindern, dass die Aktionen eines Mandanten den Dienst für einen anderen Mandanten beeinträchtigen.

Kundeninhalte werden in Microsoft 365-Mandanten mithilfe von Azure Active Directory (Azure AD) logisch isoliert. Die Benutzerauthentifizierung in Microsoft 365 überprüft nicht nur die Benutzeridentität, sondern auch die Mandantenidentität, der das Benutzerkonto angehört, wodurch verhindert wird, dass Benutzer auf Daten außerhalb Ihrer Mandantenumgebung zugreifen. Zur Ergänzung der logischen Isolation von Azure AD werden Kundeninhalte immer im Ruhe- und Transitbereich verschlüsselt. Einzelne Dienste können auch zusätzliche Ebenen der Mandantenisolation bereitstellen, z. B. die SharePoint Online-Isolation von Mandantendaten in separaten, verschlüsselten Datenbanken.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Wie entwickelt Microsoft 365 ausfallsichere Dienste, die einzelne Fehlerpunkte vermeiden?

Microsoft entwickelt und erstellt Clouddienste, um die Zuverlässigkeit zu maximieren und die negativen Auswirkungen auf Kunden angesichts von Fehlern und Herausforderungen für den normalen Betrieb zu minimieren. Diese Strategie beginnt mit dem Entwurf des Netzwerks, das unsere geografisch verteilten Rechenzentren verbindet. Die Netzwerkarchitektur von Microsoft umfasst direkte Verbindungen und mehrere Netzwerkpfade. Microsoft 365-Dienste nutzen diese Redundanz, um Datenverkehr automatisch um Fehler zu routen, um die Dienstqualität zu verbessern.

Auf Dienstebene priorisiert die Ausfallsicherheitsstrategie von Microsoft 365 die Ausfallsicherheit von Software. Wo immer möglich, werden unsere Dienste in aktiven/aktiven Konfigurationen mit automatisierter Dienstintegüberwachung bereitgestellt, sodass der Dienst viele häufige Fehler und Fehler ohne menschliches Eingreifen erkennen und wiederherstellen kann. Zusätzlich zu aktiven/aktiven Konfigurationen erhöhen Microsoft 365-Dienste die Fehlertoleranz, indem sichergestellt wird, dass der Dienst in separaten Fehlerzonen bereitgestellt wird, sodass ein Fehler in einer Zone die Verfügbarkeit anderer Zonen nicht beeinträchtigt.

Die Datenresilienz ergänzt die Dienstresilienz durch die Wahrung der Integrität und Verfügbarkeit von Daten in Microsoft 365-Diensten. Unsere Dienste verwenden lokale Speicherredundanz und Georedundanz, um Kopien von Kundendaten in verschiedene Fehlerzonen zu replizieren. Wenn Daten in einer Ausfallzone beschädigt wurden oder verloren gegangen sind, kann darauf in einer anderen Ausfallzone zugegriffen werden, ohne dass es zu einer Unterbrechung bei der Verfügbarkeit kommt. Durch die automatische Integritätsprüfung werden Daten, die von vielen Arten physischer oder logischer Beschädigungen betroffen sind, automatisch wiederhergestellt. Microsoft 365 bietet Kunden auch Tools zum Wiederherstellen versehentlich gelöschter oder geänderter Daten durch den Kunden in Exchange Online und SharePoint Online.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Wie verfolgt Microsoft 365 Abhängigkeiten und verhindert nicht autorisierte externe Systemverbindungen?

Microsoft 365-Dienstteams identifizieren wichtige Systemkomponenten und deren Abhängigkeiten im Rahmen des Business Continuity Managements. Darüber hinaus dokumentiert und verfolgt Microsoft 365 alle externen Systemverbindungen, um sicherzustellen, dass nur autorisierte Verbindungen in Netzwerkfirewallkonfigurationen zulässig sind. Microsoft 365-Systeme, Abhängigkeiten und externe Verbindungen sind in der Informationssicherheitsarchitektur von Microsoft 365 dokumentiert. Sowohl die Informationssicherheitsarchitektur als auch die entsprechenden Datenflussdiagramme werden mindestens einmal jährlich überprüft und aktualisiert sowie immer dann, wenn erhebliche Änderungen am System vorgenommen werden.

Die Microsoft 365-Architektur wird regelmäßig und automatisch mithilfe cloudbasierter Tools überprüft, um die Ausrichtung mit unseren Sicherheitsprinzipien zu überprüfen und Isolations- und Ausfallsicherheitsfeatures kontinuierlich zu testen. Die Architekturüberprüfung identifiziert automatisch Instanzen, bei denen der aktuelle Status des Diensts vom gewünschten Zustand abweicht, und zeigt abweichungen zur Überprüfung und Schadensminderung an. Das Ziel der Architekturüberprüfung besteht in der Sicherstellung, dass die Sicherheitsfunktionen unserer Dienstinfrastruktur weiterhin wie erwartet funktionieren.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Architektur von Microsoft 365.

| **Externe Prüfungen** | **Section** | **Datum des letzten Berichts** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: Erzwingung des Informationsflusses <br> CP-9: Sicherung des Informationssystems <br> PL-8: Architektur der Informationssicherheit <br> SC-7: Grenzschutz <br> SC-22: Architektur und Bereitstellung | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organisation der Informationssicherheit <br> A.13.1: Verwaltung der Netzwerksicherheit <br> A.17.2: Redundanzen | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organisation der Informationssicherheit <br> A.13.1: Verwaltung der Netzwerksicherheit | Februar 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: Mandantenisolation <br> CA-49: Sicherungsrichtlinien <br> CA-51: Datenreplikation | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: Datenflussdiagramme <br> CA-37: Mandantenisolation <br> CA-49: Sicherungsrichtlinien <br> CA-51: Datenreplikation | 24. Dezember 2020 |