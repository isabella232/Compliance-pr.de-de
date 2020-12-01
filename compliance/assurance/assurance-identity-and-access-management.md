---
title: Übersicht über die Identitäts-und Zugriffsverwaltung
description: Informationen zur Identitäts-und Zugriffsverwaltung in Microsoft 365
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
ms.openlocfilehash: b62219faa5bc55ef4bef9557d953caf1a2f95fc7
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506722"
---
# <a name="identity-and-access-management-overview"></a>Übersicht über die Identitäts-und Zugriffsverwaltung

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Wie schützt Microsoft 365 Produktionssysteme vor nicht autorisiertem oder böswilligem Zugriff?

Microsoft 365 wurde entwickelt, um Microsoft-Ingenieuren den Betrieb des Diensts ohne Zugriff auf Kunden Inhalte zu ermöglichen. Standardmäßig verfügen Microsoft 365-Techniker über keinen ständigen Zugriff auf Kunden Inhalte und keinen privilegierten Zugriff auf die Produktionsumgebung. Microsoft 365 verwendet ein Just-in-time (JIT), Just-Enough-Access (Jea)-Modell, um Service Team Ingenieuren temporären privilegierten Zugriff auf Produktionsumgebungen bereitzustellen, wenn ein solcher Zugriff zur Unterstützung von Microsoft 365 erforderlich ist. Das JIT-Zugriffsmodell ersetzt den traditionellen, dauerhaften administrativen Zugriff durch einen Prozess, bei dem Techniker bei Bedarf eine vorübergehende Erhöhung in privilegierte Rollen beantragen können.

Ingenieure, die einem Dienst Team zur Unterstützung der Produktionsdienste-Anforderung für ein Dienst Team Konto über das Identity Management Tool (IDM) zugewiesen sind. Die Anforderung für die Berechtigung löst eine Reihe von Personal Prüfungen aus, um sicherzustellen, dass der Ingenieur alle Anforderungen für die Cloud-Prüfung erfüllt, die erforderliche Schulung abgeschlossen und eine entsprechende Genehmigung für das Management vor der Kontoerstellung erhalten hat. Erst nach Erfüllung aller Berechtigungsanforderungen kann ein Serviceteamkonto für die angeforderte Umgebung erstellt werden.

Dienst-Team Konten gewähren keine ständigen Administratorrechte oder Zugriff auf Kunden Inhalte. Wenn ein Techniker zusätzlichen Zugriff benötigt, um seinen Microsoft 365-Dienst zu unterstützen, fordern Sie einen temporären erhöhten Zugriff auf die Ressourcen an, die Sie mit einem Zugriffs Verwaltungstool namens Lockbox benötigen. Lockbox schränkt den erweiterten Zugriff auf die minimalen Privilegien, Ressourcen und Zeit ein, die für die Erledigung der zugewiesenen Aufgabe erforderlich sind. Wenn ein autorisierter Prüfer die JIT-Zugriffsanforderung genehmigt, erhält der Techniker ein temporäres Konto mit nur den erforderlichen Berechtigungen, um die zugewiesene Arbeit abzuschließen. Dieses temporäre Konto erfordert mehrstufige Authentifizierung und wird nach Ablauf des genehmigten Zeitraums automatisch gelöscht.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Wie behandelt Microsoft 365 den Remotezugriff auf Produktionssysteme?

Die Microsoft 365-Systemkomponenten sind in Rechenzentren untergebracht, die von den Betriebsteams geographisch getrennt sind. Mitarbeiter des Rechenzentrums haben keinen logischen Zugriff auf Microsoft 365-Systeme. Folglich verwalten die Mitarbeiter des Microsoft 365-Dienst Teams die Umgebung über den Remotezugriff. Mitarbeiter des Serviceteams, die für Supportdienste für Microsoft 365 Remotezugriff benötigen, erhalten diesen nur nach Genehmigung durch einen autorisierten Verantwortlichen. Für den Remotezugriff wird ausschließlich FIPS 140-2-kompatibles TLS für sichere Remoteverbindungen verwendet.

Microsoft 365 verwendet sichere Verwaltungsarbeitsstationen (SAWs) für den Remotezugriff von Dienst Mitarbeitern, um Microsoft 365-Umgebungen vor Kompromissen zu schützen. Diese Workstations sind speziell darauf ausgelegt, den beabsichtigten oder ungewollten Verlust von Produktionsdaten zu verhindern, einschließlich Sperren von USB-Ports und Einschränken der verfügbaren Software für die Saw auf das, was für die Unterstützung der Umgebung erforderlich ist. Sägen werden eng verfolgt und überwacht, um böswillige oder unbeabsichtigte Beeinträchtigungen von Kundendaten durch Microsoft-Techniker zu erkennen und zu verhindern.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>Wie fügt Kunden-Lockbox zusätzlichen Schutz für Kunden Inhalte hinzu?

Kunden können Ihrem Inhalt eine zusätzliche Zugriffs Steuerungsebene hinzufügen, indem Sie die Kunden-Lockbox aktivieren. Wenn für eine Lockbox-Ansichts Anforderung der Zugriff auf Kunden Inhalte erforderlich ist, erfordert die Kunden-Lockbox die Genehmigung des Kunden als letzten Schritt im Genehmigungsworkflow. Dadurch erhalten Organisationen die Möglichkeit, diese Anforderungen zu genehmigen oder zu verweigern und dem Kunden eine direkte Zugriffssteuerung bereitzustellen. Wenn der Kunde eine Kunden-Lockbox-Anforderung ablehnt, wird der Zugriff auf den angeforderten Inhalt verweigert. Wenn der Kunde die Anforderung nicht innerhalb eines bestimmten Zeitraums ablehnt oder genehmigt, läuft die Anforderung automatisch ab, ohne dass Microsoft Zugriff auf Kunden Inhalte erhält. Wenn der Kunde die Anforderung genehmigt, wird der temporäre Zugriff von Microsoft auf Kunden Inhalte protokolliert, überprüfbar und wird automatisch widerrufen, nachdem die zum Abschließen der Problem Behandlungs Operation zugewiesene Zeit abgelaufen ist.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Verordnungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Bestimmungen und Zertifizierungen überprüft. Informationen zur Validierung von Steuerelementen im Zusammenhang mit Identität und Zugriffssteuerung erhalten Sie in der folgenden Tabelle.

| **Externe Überprüfungen** | **Section** | **Letztes Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Kontoverwaltung <br> AC-3: Zugriffs Erzwingung <br> AC-5: Trennung von Zöllen <br> AC-6: geringste Berechtigung <br> AC-17: Remote Zugriff | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 9.1: geschäftliche Anforderungen für die Zugriffssteuerung <br> A. 9.2: Benutzerzugriffsverwaltung <br> A. 9.3: Benutzer Verantwortlichkeiten <br> A. 9.4: System-und Anwendungszugriffs Steuerung <br> A. 15.1: Informationssicherheit in Lieferantenbeziehungen | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 9.2: Benutzerzugriffsverwaltung <br> A. 9.4: System-und Anwendungszugriffs Steuerung <br> A. 15.1: Informationssicherheit in Lieferantenbeziehungen | Februar 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-33: Kontoänderung <br> CA-34: Benutzerauthentifizierung <br> CA-35: privilegierter Zugriff <br> CA-36: Remote Zugriff <br> CA-57: Kunden-Lockbox – Microsoft-Verwaltungsgenehmigung <br> CA-58: Kunden-Lockbox-Dienstanforderungen <br> CA-59: Kunden-Lockbox-Benachrichtigungen <br> CA-61: JIT-Überprüfung und Genehmigung | 30. September 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-32: gemeinsame Kontorichtlinie <br> CA-33: Kontoänderung <br> CA-34: Benutzerauthentifizierung <br> CA-35: privilegierter Zugriff <br> CA-36: Remote Zugriff <br> CA-53: Überwachung durch Drittanbieter <br> CA-56: Kundenzulassung für Kunden-Lockbox <br> CA-57: Kunden-Lockbox – Microsoft-Verwaltungsgenehmigung <br> CA-58: Kunden-Lockbox-Dienstanforderungen <br> CA-59: Kunden-Lockbox-Benachrichtigungen <br> CA-61: JIT-Überprüfung und Genehmigung | 30. September 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-15: Kunden-Lockbox-Anforderungen | 30. September 2019 |