---
title: Ausfallsicherheit und Kontinuität
description: Erfahren Sie mehr über Resilienz und Kontinuität in Microsoft 365
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
ms.openlocfilehash: d05263c70b0e4210562b8a4ec7a8ec9c6600f9e5
ms.sourcegitcommit: 444a58b28f8611323e16d28b4c63a0f68eaaafa6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2021
ms.locfileid: "60779991"
---
# <a name="resiliency-and-continuity-overview"></a>Ausfallsicherheit und Kontinuität (Übersicht)

## <a name="how-does-microsoft-ensure-business-continuity-if-a-disaster-or-other-threat-to-service-availability-occurs"></a>Wie stellt Microsoft die Geschäftskontinuität sicher, wenn ein Notfall oder eine andere Bedrohung für die Dienstverfügbarkeit auftritt?

Das Team Enterprise Business Continuity Management (EBCM) von Microsoft überwacht aktivitäten im Bereich der Geschäftskontinuitätsverwaltung und Notfallwiederherstellung über Microsoft-Dienste und Cloudangebote hinweg. Vertreter von Microsoft-Geschäftseinheiten koordinieren sich mit dem EBCM-Team, um Geschäftskontinuitätspläne zu entwickeln und die Einhaltung der Geschäftskontinuitätsanforderungen zu überprüfen.

Der Geschäftskontinuitätsverwaltungs-Lebenszyklus (Business Continuity Management, BCM) ist der Kern unserer BCM-Methodik. Dieser dreistufige Prozess ist so konzipiert, dass er anpassungsfähig ist, sodass er von einer Vielzahl von Geschäftsprozessen in Microsoft implementiert werden kann. Es beginnt mit einer **Bewertungsphase,** um kritische Prozesse und Ziele zu identifizieren, die in das Geschäftskontinuitätsprogramm einbezogen werden sollten. Die Bewertungsphase erfordert auch eine Geschäftsauswirkungsanalyse (Business Impact Analysis, BIA). Die **Planungsphase** konzentriert sich auf die Entwicklung und Implementierung von Resilienz- und Wiederherstellungsstrategien und deren Dokumentation in offiziellen Geschäftskontinuitätsplänen. Schließlich testet **die Funktionsüberprüfung** Geschäftskontinuitätspläne und deren Implementierungen, um die Effektivität zu überprüfen und potenzielle Verbesserungen zu identifizieren.

Die Geschäftskontinuitätsstrategien von Microsoft Online Services verwenden Hardware-, Netzwerk- und Rechenzentrumsredundanz. Die Datenreplikation zwischen Rechenzentren bietet hohe Verfügbarkeit und Zuverlässigkeit während eines schwerwiegenden Vorfalls. Es erhöht auch die Resilienz gegenüber alltäglichen Vorfällen wie isolierten Hardwarefehlern oder Datenbeschädigungen.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Wie teste Microsoft Geschäftskontinuitäts- und Notfallwiederherstellungspläne?

Die Ebcm-Richtlinie (Enterprise Business Continuity Management) von Microsoft legt fest, dass alle Geschäftskontinuitäts- und Notfallwiederherstellungspläne von Microsoft auf jährlicher Basis getestet, aktualisiert und überprüft werden müssen. Microsoft-Onlinedienste testen ihre Geschäftskontinuitätspläne mindestens einmal jährlich pro EBCM-Richtlinien. Nachdem Aktionsberichte erstellt und überprüft wurden, um Aktualisierungen zu überprüfen, zu testen und Planupdates als Reaktion auf während der Tests erkannte Probleme zu informieren.

Zum Überprüfen von Resilienz- und Wiederherstellungsstrategien mit einer breiten Palette potenzieller Vorfälle definiert das EBCM-Programm mehrere Kategorien von Testszenarien, die sich auf Personen, Standorte und Technologie auswirken. Die für jeden Dienst erforderliche Überprüfungsebene basiert auf dem Maß, in dem der Dienst kritisch ist, wobei kritischere Dienste einer strengeren Überprüfung unterzogen werden. Jedes Microsoft-Onlinedienstteam testet seinen Geschäftskontinuitätsplan gemäß den EBCM-Richtlinien, um die Effektivität des Plans und die Bereitschaft des Serviceteams zur Ausführung des Plans zu messen.

Gemäß den EBCM-Richtlinien müssen jährliche Überprüfungen von Geschäftskontinuitätsplänen und die Funktionsüberprüfung innerhalb von 12 Monaten nach der letzten Überprüfung erfolgen. Die Funktionsüberprüfung muss eine Überprüfung der unterstützenden Dokumentation, z. B. des BIA, umfassen, um sicherzustellen, dass sie korrekt bleibt. Microsoft stellt unseren Kunden die Ergebnisse der Funktionsüberprüfung für ausgewählte Microsoft-Onlinedienste über Quartalsberichte zur Verfügung.

## <a name="how-do-microsoft-online-services-ensure-system-capacity-meets-demand"></a>Wie stellen Microsoft-Onlinedienste sicher, dass die Systemkapazität die Anforderungen erfüllt?

Die Kapazitätsplanung hilft Serviceteams, die zur Unterstützung der Verfügbarkeit von Microsoft-Onlinediensten erforderlichen Ressourcen zuzuweisen. Im Rahmen des EBCM-Programms von Microsoft ist eine regelmäßige Kapazitätsplanung erforderlich. Serviceteams überprüfen Kapazitätsdaten während vierteljährlicher Überprüfungen und in Notfallsituationen, die eine größere Kapazitätsüberprüfung erfordern.

Die Rohdaten für die Kapazitätsplanung werden von jedem Serviceteam verwaltet und umfassen Metriken wie Systemverarbeitung, Arbeitsspeicher und Hardwarekapazität. Geplante Überprüfungen verwenden ein Modell der aktuellen Kapazität des Systems und testen es gegen den prognostizierten Bedarf in Notfallsituationen. Wenn das Modell Kapazitätsengpässe anzeigt, werden der Leitung des Serviceteams Änderungsvorschläge zur Prüfung unterbreitet. Genehmigte Änderungen werden in ein neues Modell integriert, bevor es von Serviceteamtechnikern implementiert wird.

## <a name="how-do-microsoft-online-services-maintain-service-availability-during-routine-system-failures"></a>Wie verwalten Microsoft-Onlinedienste die Dienstverfügbarkeit bei routinemäßigen Systemfehlern?

Microsoft-Onlinedienste erzielen Dienstresilienz durch redundante Architektur, Datenreplikation und automatisierte Integritätsprüfung. Redundante Architektur umfasst die Bereitstellung mehrerer Instanzen eines Diensts auf geografisch und physisch getrennter Hardware, wodurch eine höhere Fehlertoleranz für Microsoft-Onlinedienste bereitgestellt wird. Die Datenreplikation stellt sicher, dass es immer mehrere Kopien von Kundendaten in verschiedenen Fehlerzonen gibt, sodass kritische Kundendaten wiederhergestellt werden können, wenn sie beschädigt sind, verloren gehen oder sogar versehentlich vom Kunden gelöscht werden. Die automatisierte Integritätsprüfung erhöht die Datenverfügbarkeit, indem Daten, die von vielen Physischen oder logischen Beschädigungen betroffen sind, automatisch wiederhergestellt werden.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit Resilienz und Kontinuität finden Sie in der folgenden Tabelle.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Kontinuität der Informationssicherheit <br> A.17.2: Redundanzen | 2. Dezember 2020 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=6d388547-fc88-46e3-8de2-6bc2edc08b06&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=ee4b611b-bb4d-4056-b189-00da36e88949&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Alle Steuerelemente | 13. Mai 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1: Geschäftskontinuitätspläne <br> BC-3: Verfahren für Geschäftskontinuität und Notfallwiederherstellung <br> BC-4: BCDR-Tests <br> BC-7: Geschäftskontinuitätspläne für Rechenzentren <br> BC-8: Geschäftskontinuitätstests für Rechenzentren <br> BC-9: Bewertung der Ausfallsicherheit von Rechenzentren <br> DS-5: Komponenten des Sicherungsschlüsseldiensts <br> DS-6: Redundanz wichtiger Komponenten <br> DS-7: Automatische Replikation von Kundendaten <br> DS-8: Sicherungszeitplan <br> DS-9: Verfahren zur Sicherung der Wiederherstellung <br> DS-11: Offsite-Sicherungen <br> DS-14: Automatische Wiederherstellung von Kundendiensten | 31. März 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CP-2: Notfallplan <br> CP-3: Notfallschulung <br> CP-4: Test des Notfallplans <br> CP-6: Alternativer Speicherort <br> CP-7: Alternativer Verarbeitungsstandort <br> CP-9: Sicherung des Informationssystems <br> CP-10: Wiederherstellung und Wiederherstellung des Informationssystems | 24. September 2020 |
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Kontinuität der Informationssicherheit <br> A.17.2: Redundanzen | 20. April 2021 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Alle Steuerelemente | 18. März 2019 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Sicherungsrichtlinien <br> CA-50: Geschäftskontinuität <br> CA-51: Datenreplikation | 24. Dezember 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09: EXO-E-Mail-Wiederherstellung | 24. Dezember 2020 |

## <a name="resources"></a>Ressourcen

- [Whitepaper zum Microsoft Enterprise Business Continuity Management-Programm](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f)
- [Microsoft Cloud EBCM and Disaster Recovery Plan Validation Report: FY22 Q1](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=f47df93a-f6a0-4013-96e6-35b91af90a78&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Haftungsausschluss

- [Enterprise-Geschäftskontinuität – Haftungsausschluss](assurance-ebcm-legal-disclaimer.md)