---
title: Identitäts- und Zugriffsverwaltung (Übersicht)
description: Informationen zur Identitäts- und Zugriffsverwaltung in Microsoft 365
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
ms.openlocfilehash: 933db3783c6672fa952f70f18c4815955bcedb21
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481957"
---
# <a name="identity-and-access-management-overview"></a>Identitäts- und Zugriffsverwaltung (Übersicht)

## <a name="how-do-microsoft-online-services-protect-production-systems-from-unauthorized-or-malicious-access"></a>Wie schützen Microsoft-Onlinedienste Produktionssysteme vor unbefugtem oder böswilligem Zugriff?

Microsoft-Onlinedienste sind so konzipiert, dass Microsoft-Techniker Dienste ausführen können, ohne auf Kundeninhalte zuzugreifen. Standardmäßig verfügen Microsoft-Techniker über Zero Standing Access (ZSA) für Kundeninhalte und keinen privilegierten Zugriff auf die Produktionsumgebung. Microsoft-Onlinedienste verwenden ein Just-In-Time (JIT), Just-Enough-Access (JEA)-Modell, um Serviceteamtechnikern temporären privilegierten Zugriff auf Produktionsumgebungen zu gewähren, wenn ein solcher Zugriff erforderlich ist, um Microsoft-Onlinedienste zu unterstützen. Das JIT-Zugriffsmodell ersetzt den traditionellen, dauerhaften administrativen Zugriff durch einen Prozess, bei dem Techniker bei Bedarf eine vorübergehende Erhöhung in privilegierte Rollen beantragen können.

Techniker, die einem Serviceteam zur Unterstützung von Produktionsdiensten zugewiesen sind, fordern die Berechtigung für ein Serviceteamkonto über eine Identitäts- und Zugriffsverwaltungslösung an. Die Anforderung der Berechtigung löst eine Reihe von Personalüberprüfungen aus, um sicherzustellen, dass der Techniker alle Cloud-Prüfungsanforderungen erfüllt, die erforderlichen Schulungen abgeschlossen und vor der Kontoerstellung eine entsprechende Verwaltungsgenehmigung erhalten hat. Erst nach Erfüllung aller Berechtigungsanforderungen kann ein Serviceteamkonto für die angeforderte Umgebung erstellt werden. Um die Berechtigung für ein Serviceteamkonto aufrechtzuerhalten, muss das Personal jährlich eine rollenbasierte Schulung durchlaufen und alle zwei Jahre erneut prüfen. Wenn diese Überprüfungen nicht abgeschlossen oder bestanden werden, werden die Berechtigungen automatisch widerrufen.

Serviceteamkonten gewähren keinen ständigen Administratorrechten oder Zugriff auf Kundeninhalte. Wenn ein Techniker zusätzlichen Zugriff benötigt, um Microsoft-Onlinedienste zu unterstützen, fordert er temporären erhöhten Zugriff auf die Ressourcen an, die er benötigt, mithilfe eines Zugriffsverwaltungstools namens Lockbox. Lockbox schränkt den erweiterten Zugriff auf die minimalen Privilegien, Ressourcen und Zeit ein, die für die Erledigung der zugewiesenen Aufgabe erforderlich sind. Wenn ein autorisierter Prüfer die JIT-Zugriffsanforderung genehmigt, erhält der Techniker ein temporäres Konto mit nur den Berechtigungen, die zum Abschließen der zugewiesenen Arbeit erforderlich sind. Dieses temporäre Konto erfordert eine mehrstufige Authentifizierung und wird nach Ablauf des genehmigten Zeitraums automatisch gelöscht.

JEA wird durch Berechtigungsberechtigungen und Lockbox-Rollen zum Zeitpunkt der Anforderung des JIT-Zugriffs erzwungen. Nur Anforderungen für den Zugriff auf Ressourcen im Rahmen der Berechtigungen des Technikers werden akzeptiert und an die genehmigende Person weitergegeben. Lockbox lehnt JIT-Anforderungen automatisch ab, die außerhalb des Bereichs der Berechtigungen des Technikers und der Lockbox-Rollen liegen, einschließlich Anforderungen, die zulässige Schwellenwerte überschreiten.  

## <a name="how-do-microsoft-online-services-use-role-based-access-control-rbac-with-lockbox-to-enforce-least-privilege"></a>Wie verwenden Microsoft-Onlinedienste die rollenbasierte Zugriffssteuerung (Role-Based Access Control, RBAC) mit Lockbox, um die geringsten Rechte zu erzwingen?

Serviceteamkonten gewähren keinen ständigen Administratorrechten oder Zugriff auf Kundeninhalte. JIT-Anforderungen für eingeschränkte Administratorrechte werden über Lockbox verwaltet. Lockbox verwendet RBAC, um die Arten von JIT-Rechteerweiterungsanforderungen einzuschränken, die Techniker ausführen können, und bietet eine zusätzliche Schutzebene, um die geringsten Rechte zu erzwingen. RBAC hilft auch bei der Durchsetzung der Aufgabentrennung, indem Serviceteamkonten auf die entsprechenden Rollen beschränkt werden.
Technikern, die einen Dienst unterstützen, wird basierend auf ihrer Rolle die Mitgliedschaft in Sicherheitsgruppen gewährt. Die Mitgliedschaft in einer Sicherheitsgruppe gewährt keinen privilegierten Zugriff. Sicherheitsgruppen ermöglichen Es Entwicklern stattdessen, Lockbox zu verwenden, um JIT-Rechteerweiterung anzufordern, wenn dies für die Unterstützung des Systems erforderlich ist. Die spezifischen JIT-Anforderungen, die ein Techniker stellen kann, sind durch ihre Sicherheitsgruppenmitgliedschaften begrenzt.

## <a name="how-do-microsoft-online-services-handle-remote-access-to-production-systems"></a>Wie behandeln Microsoft-Onlinedienste den Remotezugriff auf Produktionssysteme?

Microsoft Online Services-Systemkomponenten befinden sich in Rechenzentren, die geografisch von den Betriebsteams getrennt sind. Mitarbeiter von Rechenzentren haben keinen logischen Zugriff auf Microsoft-Onlinedienstsysteme. Daher verwalten Mitarbeiter des Microsoft-Serviceteams die Umgebung über den Remotezugriff. Serviceteammitarbeiter, die Remotezugriff benötigen, um Microsoft-Onlinedienste zu unterstützen, erhalten nur nach genehmigung durch einen autorisierten Vorgesetzten Remotezugriff. Für den Remotezugriff wird ausschließlich FIPS 140-2-kompatibles TLS für sichere Remoteverbindungen verwendet.

Microsoft Online services use Secure Admin Workstations (SAW) for service team remote access to protect Microsoft online service environments from compromise. Diese Arbeitsstationen sind so konzipiert, dass absichtlicher oder unbeabsichtigter Verlust von Produktionsdaten verhindert wird, z. B. das Sperren von USB-Anschlüssen und das Einschränken der auf der Secure Admin Workstation verfügbaren Software auf die zur Unterstützung der Umgebung erforderlichen Komponenten. Sichere Administratorarbeitsstationen werden genau nachverfolgt und überwacht, um böswillige oder unbeabsichtigte Kompromittierungen von Kundendaten durch Microsoft-Techniker zu erkennen und zu verhindern.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>Wie fügt Kunden-Lockbox zusätzlichen Schutz für Kundeninhalte hinzu?

Kunden können ihren Inhalten eine zusätzliche Zugriffskontrolle hinzufügen, indem sie die Kunden-Lockbox aktivieren. Wenn eine Lockbox-Erweiterungsanforderung den Zugriff auf Kundeninhalte umfasst, erfordert die Kunden-Lockbox eine Genehmigung durch den Kunden als letzten Schritt im Genehmigungsworkflow. Dieser Prozess bietet Organisationen die Möglichkeit, diese Anforderungen zu genehmigen oder zu verweigern, und bietet dem Kunden eine direkte Zugriffssteuerung. Wenn der Kunde eine Kunden-Lockbox-Anforderung ablehnt, wird der Zugriff auf den angeforderten Inhalt verweigert. Wenn der Kunde die Anforderung nicht innerhalb eines bestimmten Zeitraums ablehnt oder genehmigt, läuft die Anforderung automatisch ab, ohne dass Microsoft Zugriff auf Kundeninhalte erhält. Wenn der Kunde die Anforderung genehmigt, wird der temporäre Zugriff von Microsoft auf Kundeninhalte protokolliert, überwachbar und automatisch widerrufen, nachdem die Zum Abschluss des Problembehandlungsvorgangs zugewiesene Zeit abgelaufen ist.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit Identitäts- und Zugriffssteuerung finden Sie in der folgenden Tabelle.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Geschäftliche Anforderungen der Zugriffssteuerung <br> A.9.2: Verwaltung des Benutzerzugriffs <br> A.9.3: Verantwortlichkeiten des Benutzers <br> A.9.4: System- und Anwendungszugriffskontrolle <br> A.15.1: Informationssicherheit in Lieferantenbeziehungen | 2. Dezember 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Geschäftliche Anforderungen der Zugriffssteuerung <br> A.9.2: Verwaltung des Benutzerzugriffs <br> A.9.3: Verantwortlichkeiten des Benutzers <br> A.9.4: System- und Anwendungszugriffskontrolle <br> A.15.1: Informationssicherheit in Lieferantenbeziehungen | 2. Dezember 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | OA-2: Bereitstellen des Zugriffs <br> OA-7: JIT-Zugriff <br> OA-21: Sichere Administratorarbeitsstationen und MFA | 31. März 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2: Kontoverwaltung <br> AC-3: Zugriffserzwingung <br> AC-5: Aufgabentrennung <br> AC-6: Geringste Rechte <br> AC-17: Remotezugriff | 24. September 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Geschäftliche Anforderungen der Zugriffssteuerung <br> A.9.2: Verwaltung des Benutzerzugriffs <br> A.9.3: Verantwortlichkeiten des Benutzers <br> A.9.4: System- und Anwendungszugriffskontrolle <br> A.15.1: Informationssicherheit in Lieferantenbeziehungen | 20. April 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: Kontoänderung <br> CA-34: Benutzerauthentifizierung <br> CA-35: Privilegierter Zugriff <br> CA-36: Remotezugriff <br> CA-57: Microsoft-Verwaltungsgenehmigung für Kunden-Lockbox <br> CA-58: Kunden-Lockbox-Serviceanfragen <br> CA-59: Kunden-Lockbox-Benachrichtigungen <br> CA-61: JIT-Überprüfung und -Genehmigung | 24. Dezember 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: Richtlinie für freigegebene Konten <br> CA-33: Kontoänderung <br> CA-34: Benutzerauthentifizierung <br> CA-35: Privilegierter Zugriff <br> CA-36: Remotezugriff <br> CA-53: Überwachung durch Drittanbieter <br> CA-56: Kunden-Lockbox-Kundengenehmigung <br> CA-57: Microsoft-Verwaltungsgenehmigung für Kunden-Lockbox <br> CA-58: Kunden-Lockbox-Serviceanfragen <br> CA-59: Kunden-Lockbox-Benachrichtigungen <br> CA-61: JIT-Überprüfung und -Genehmigung | 24. Dezember 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: Kunden-Lockbox-Anforderungen | 24. Dezember 2020 |