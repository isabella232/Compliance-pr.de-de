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
ms.openlocfilehash: 5cca0c3cf70a0fe2c660c0b168a157056e1d4c56942fdeee2b71e7448c1dc50b
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54291013"
---
# <a name="identity-and-access-management-overview"></a>Identitäts- und Zugriffsverwaltung (Übersicht)

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Wie schützt Microsoft 365 Produktionssysteme vor unbefugtem oder böswilligem Zugriff?

Microsoft 365 ist so konzipiert, dass Die Techniker von Microsoft den Dienst ausführen können, ohne auf Kundeninhalte zuzugreifen. Standardmäßig verfügen Microsoft 365 Techniker über Zero Standing Access (ZSA) für Kundeninhalte und keinen privilegierten Zugriff auf die Produktionsumgebung. Microsoft 365 verwendet ein Just-In-Time (JIT), Just-Enough-Access (JEA)-Modell, um Serviceteamtechnikern temporären privilegierten Zugriff auf Produktionsumgebungen zu gewähren, wenn ein solcher Zugriff erforderlich ist, um Microsoft 365 zu unterstützen. Das JIT-Zugriffsmodell ersetzt den traditionellen, dauerhaften administrativen Zugriff durch einen Prozess, bei dem Techniker bei Bedarf eine vorübergehende Erhöhung in privilegierte Rollen beantragen können.

Techniker, die einem Serviceteam zur Unterstützung von Produktionsdiensten zugewiesen sind, fordern die Berechtigung für ein Serviceteamkonto über das Identity Management Tool (IDM) an. Die Anforderung der Berechtigung löst eine Reihe von Personalüberprüfungen aus, um sicherzustellen, dass der Techniker alle Cloud-Prüfungsanforderungen erfüllt, die erforderlichen Schulungen abgeschlossen und vor der Kontoerstellung eine entsprechende Verwaltungsgenehmigung erhalten hat. Erst nach Erfüllung aller Berechtigungsanforderungen kann ein Serviceteamkonto für die angeforderte Umgebung erstellt werden. Um die Berechtigung für ein Serviceteamkonto aufrechtzuerhalten, muss das Personal jährlich eine rollenbasierte Schulung durchlaufen und alle zwei Jahre erneut prüfen. Wenn diese Überprüfungen nicht abgeschlossen oder bestanden werden, werden die Berechtigungen automatisch widerrufen.

Serviceteamkonten gewähren keinen ständigen Administratorrechten oder Zugriff auf Kundeninhalte. Wenn ein Techniker zusätzlichen Zugriff benötigt, um seine Microsoft 365 Dienst zu unterstützen, fordert er temporären erhöhten Zugriff auf die Ressourcen an, die er benötigt, mithilfe eines Zugriffsverwaltungstools namens Lockbox. Lockbox schränkt den erweiterten Zugriff auf die minimalen Privilegien, Ressourcen und Zeit ein, die für die Erledigung der zugewiesenen Aufgabe erforderlich sind. Wenn ein autorisierter Prüfer die JIT-Zugriffsanforderung genehmigt, erhält der Techniker ein temporäres Konto mit nur den Berechtigungen, die zum Abschließen der zugewiesenen Arbeit erforderlich sind. Dieses temporäre Konto erfordert eine mehrstufige Authentifizierung und wird nach Ablauf des genehmigten Zeitraums automatisch gelöscht.

JEA wird durch IDM-Berechtigungen und Lockbox-Rollen zum Zeitpunkt der Anforderung des JIT-Zugriffs erzwungen. Nur Anforderungen für den Zugriff auf Ressourcen im Rahmen der Berechtigungen des Technikers werden akzeptiert und an die genehmigende Person weitergegeben. Lockbox lehnt JIT-Anforderungen automatisch ab, die außerhalb des Bereichs der Berechtigungen des Technikers und der Lockbox-Rollen liegen, einschließlich Anforderungen, die zulässige Schwellenwerte überschreiten.  

## <a name="how-does-microsoft-365-use-role-based-access-control-rbac-with-lockbox-to-enforce-least-privilege"></a>Wie verwendet Microsoft 365 die rollenbasierte Zugriffssteuerung (Role-Based Access Control, RBAC) mit Lockbox, um die geringsten Rechte zu erzwingen?

Serviceteamkonten gewähren keinen ständigen Administratorrechten oder Zugriff auf Kundeninhalte. JIT-Anforderungen für eingeschränkte Administratorrechte werden über Lockbox verwaltet. Lockbox verwendet RBAC, um die Arten von JIT-Rechteerweiterungsanforderungen einzuschränken, die Techniker ausführen können, und bietet eine zusätzliche Schutzebene, um die geringsten Rechte zu erzwingen. RBAC hilft auch bei der Durchsetzung der Aufgabentrennung, indem Serviceteamkonten auf die entsprechenden Rollen beschränkt werden.
Technikern, die einen Dienst unterstützen, wird basierend auf ihrer Rolle die Mitgliedschaft in Sicherheitsgruppen gewährt. Die Mitgliedschaft in einer Sicherheitsgruppe gewährt keinen privilegierten Zugriff. Sicherheitsgruppen ermöglichen Es Entwicklern stattdessen, Lockbox zu verwenden, um JIT-Rechteerweiterung anzufordern, wenn dies für die Unterstützung des Systems erforderlich ist. Die spezifischen JIT-Anforderungen, die ein Techniker stellen kann, sind durch ihre Sicherheitsgruppenmitgliedschaften begrenzt.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Wie behandelt Microsoft 365 den Remotezugriff auf Produktionssysteme?

Die Microsoft 365-Systemkomponenten sind in Rechenzentren untergebracht, die von den Betriebsteams geographisch getrennt sind. Mitarbeiter von Rechenzentren haben keinen logischen Zugriff auf Microsoft 365 Systeme. Daher verwalten Microsoft 365 Serviceteammitarbeiter die Umgebung über den Remotezugriff. Mitarbeiter des Serviceteams, die für Supportdienste für Microsoft 365 Remotezugriff benötigen, erhalten diesen nur nach Genehmigung durch einen autorisierten Verantwortlichen. Für den Remotezugriff wird ausschließlich FIPS 140-2-kompatibles TLS für sichere Remoteverbindungen verwendet.

Microsoft 365 verwendet Secure Admin Workstations für den Remotezugriff des Serviceteams, um Microsoft 365 Umgebungen vor Kompromittierung zu schützen. Diese Arbeitsstationen sind so konzipiert, dass absichtlicher oder unbeabsichtigter Verlust von Produktionsdaten verhindert wird, z. B. das Sperren von USB-Anschlüssen und das Einschränken der auf der Secure Admin Workstation verfügbaren Software auf die zur Unterstützung der Umgebung erforderlichen Komponenten. Sichere Administratorarbeitsstationen werden genau nachverfolgt und überwacht, um böswillige oder unbeabsichtigte Kompromittierungen von Kundendaten durch Microsoft-Techniker zu erkennen und zu verhindern.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>Wie fügt Kunden-Lockbox zusätzlichen Schutz für Kundeninhalte hinzu?

Kunden können ihren Inhalten eine zusätzliche Zugriffskontrolle hinzufügen, indem sie die Kunden-Lockbox aktivieren. Wenn eine Lockbox-Erweiterungsanforderung den Zugriff auf Kundeninhalte umfasst, erfordert die Kunden-Lockbox eine Genehmigung durch den Kunden als letzten Schritt im Genehmigungsworkflow. Dieser Prozess bietet Organisationen die Möglichkeit, diese Anforderungen zu genehmigen oder zu verweigern, und bietet dem Kunden eine direkte Zugriffssteuerung. Wenn der Kunde eine Kunden-Lockbox-Anforderung ablehnt, wird der Zugriff auf den angeforderten Inhalt verweigert. Wenn der Kunde die Anforderung nicht innerhalb eines bestimmten Zeitraums ablehnt oder genehmigt, läuft die Anforderung automatisch ab, ohne dass Microsoft Zugriff auf Kundeninhalte erhält. Wenn der Kunde die Anforderung genehmigt, wird der temporäre Zugriff von Microsoft auf Kundeninhalte protokolliert, überwachbar und automatisch widerrufen, nachdem die Zum Abschluss des Problembehandlungsvorgangs zugewiesene Zeit abgelaufen ist.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit Identitäts- und Zugriffssteuerung finden Sie in der folgenden Tabelle.

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Kontoverwaltung <br> AC-3: Zugriffserzwingung <br> AC-5: Aufgabentrennung <br> AC-6: Geringste Rechte <br> AC-17: Remotezugriff | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Geschäftliche Anforderungen der Zugriffssteuerung <br> A.9.2: Verwaltung des Benutzerzugriffs <br> A.9.3: Verantwortlichkeiten des Benutzers <br> A.9.4: System- und Anwendungszugriffskontrolle <br> A.15.1: Informationssicherheit in Lieferantenbeziehungen | 20. April 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.2: Verwaltung des Benutzerzugriffs <br> A.9.4: System- und Anwendungszugriffskontrolle <br> A.15.1: Informationssicherheit in Lieferantenbeziehungen | 20. April 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: Kontoänderung <br> CA-34: Benutzerauthentifizierung <br> CA-35: Privilegierter Zugriff <br> CA-36: Remotezugriff <br> CA-57: Microsoft-Verwaltungsgenehmigung für Kunden-Lockbox <br> CA-58: Kunden-Lockbox-Serviceanfragen <br> CA-59: Kunden-Lockbox-Benachrichtigungen <br> CA-61: JIT-Überprüfung und -Genehmigung | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: Richtlinie für freigegebene Konten <br> CA-33: Kontoänderung <br> CA-34: Benutzerauthentifizierung <br> CA-35: Privilegierter Zugriff <br> CA-36: Remotezugriff <br> CA-53: Überwachung durch Drittanbieter <br> CA-56: Kunden-Lockbox-Kundengenehmigung <br> CA-57: Microsoft-Verwaltungsgenehmigung für Kunden-Lockbox <br> CA-58: Kunden-Lockbox-Serviceanfragen <br> CA-59: Kunden-Lockbox-Benachrichtigungen <br> CA-61: JIT-Überprüfung und -Genehmigung | 24. Dezember 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: Kunden-Lockbox-Anforderungen | 24. Dezember 2020 |