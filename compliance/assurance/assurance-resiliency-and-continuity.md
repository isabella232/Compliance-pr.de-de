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
ms.openlocfilehash: 0201ad28f25af78ec69f99725e12118dc205b338
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573803"
---
# <a name="resiliency-and-continuity-overview"></a>Ausfallsicherheit und Kontinuität (Übersicht)

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>Wie gewährleistet Microsoft die Geschäftskontinuität im Falle eines Notfalls oder einer anderen Bedrohung für die Dienstverfügbarkeit?

Das Team Enterprise Business Continuity Management (EBCM) von Microsoft überwacht die Geschäftskontinuitätsmanagement- und Notfallwiederherstellungsaktivitäten über Microsoft-Dienste- und Cloudangebote hinweg. Vertreter von Microsoft-Geschäftsbereichen, z. B. Microsoft 365, koordinieren sich mit dem EBCM-Team, um Geschäftskontinuitätspläne zu entwickeln und die Einhaltung der Geschäftskontinuitätsanforderungen zu überprüfen.

Der Kern unserer BCM-Methodik (Business Continuity Management) ist der BCM-Lebenszyklus. Dieser dreistufige Prozess ist so konzipiert, dass er anpassungsfähig ist, sodass er von einer Vielzahl von Geschäftsprozessen in Microsoft implementiert werden kann. Es beginnt mit einer **Bewertungsphase,** um kritische Prozesse und Ziele zu identifizieren, die in das Geschäftskontinuitätsprogramm einbezogen werden sollten. Die Bewertungsphase erfordert auch eine Geschäftsauswirkungsanalyse (Business Impact Analysis, BIA). In der Phase **Planung** liegt der Schwerpunkt auf der Entwicklung und Umsetzung von Resilienz- und Wiederherstellungsstrategien sowie deren Dokumentation in offiziellen Geschäftskontinuitätsplänen. Schließlich testet **die Funktionsüberprüfung** Geschäftskontinuitätspläne und deren Implementierungen, um die Effektivität zu überprüfen und potenzielle Verbesserungen zu identifizieren.

Die Geschäftskontinuitätsstrategie von Microsoft 365 nutzt Hardware-, Netzwerk- und Rechenzentrumsredundanz. Die Datenreplikation zwischen Rechenzentren bietet hohe Verfügbarkeit und Zuverlässigkeit im Falle eines schwerwiegenden Vorfalls. Es erhöht auch die Resilienz gegenüber alltäglichen Vorfällen wie isolierten Hardwarefehlern oder Datenbeschädigungen.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Wie teste Microsoft Geschäftskontinuitäts- und Notfallwiederherstellungspläne?

Die Ebcm-Richtlinie (Enterprise Business Continuity Management) von Microsoft legt fest, dass alle Microsoft-Pläne für Geschäftskontinuität und Notfallwiederherstellung auf jährlicher Basis getestet, aktualisiert und überprüft werden müssen. Microsoft 365-Dienste testen ihre Geschäftskontinuitätspläne mindestens einmal jährlich pro EBCM-Richtlinien. Nachdem Aktionsberichte erstellt und überprüft wurden, um Aktualisierungen zu überprüfen, zu testen und Planupdates als Reaktion auf während der Tests erkannte Probleme zu informieren.

Zum Überprüfen von Resilienz- und Wiederherstellungsstrategien mit einer breiten Palette potenzieller Vorfälle definiert das EBCM-Programm mehrere Kategorien von Testszenarien, die sich auf Personen, Standorte und Technologie auswirken. Der für jeden Dienst erforderliche Überprüfungsgrad basiert auf der Kritikalität des Diensts, wobei kritischere Dienste eine strengere Überprüfung erhalten. Jedes Microsoft 365 Serviceteam testet seinen Geschäftskontinuitätsplan gemäß den EBCM-Richtlinien, um die Effektivität des Plans und die Bereitschaft des Serviceteams zur Ausführung des Plans zu messen.

Gemäß den EBCM-Richtlinien müssen jährliche Überprüfungen von Geschäftskontinuitätsplänen und die Funktionsüberprüfung innerhalb von 12 Monaten nach der letzten Überprüfung erfolgen. Die Funktionsüberprüfung muss eine Überprüfung der unterstützenden Dokumentation, z. B. des BIA, umfassen, um sicherzustellen, dass sie korrekt bleibt. Microsoft stellt unseren Kunden die Ergebnisse der Funktionsüberprüfung für ausgewählte Microsoft 365 Dienste über Quartalsberichte zur Verfügung.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Wie stellt Microsoft 365 sicher, dass die Systemkapazität die Anforderungen erfüllt?

Die Kapazitätsplanung hilft den Serviceteams bei der Zuweisung der Ressourcen, die zur Unterstützung der Verfügbarkeit von Microsoft 365-Diensten erforderlich sind. Im Rahmen des EBCM-Programms von Microsoft ist eine regelmäßige Kapazitätsplanung erforderlich. Serviceteams überprüfen die Kapazitätsdaten während der vierteljährlichen Überprüfungen sowie in Notsituationen, in denen eine zusätzliche Kapazitätsprüfung erforderlich wird.

Die Rohdaten für die Kapazitätsplanung werden von jedem Serviceteam verwaltet und umfassen Metriken wie Systemverarbeitung, Arbeitsspeicher und Hardwarekapazität. Geplante Überprüfungen verwenden ein Modell der aktuellen Kapazität des Systems und testen es gegen den prognostizierten Bedarf in Notfallsituationen. Wenn das Modell Kapazitätsengpässe anzeigt, werden der Leitung des Serviceteams Änderungsvorschläge zur Prüfung unterbreitet. Genehmigte Änderungen werden in ein neues Modell integriert, bevor es von Serviceteamtechnikern implementiert wird.

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>Wie verwaltet Microsoft 365 die Dienstverfügbarkeit bei routinemäßigen Systemfehlern?

Microsoft 365 die Dienstresilienz durch redundante Architektur, Datenreplikation und automatisierte Integritätsprüfung erreicht. Redundant architecture involves deploying multiple instances of a service on geoly and physically separate hardware, providing increased fault-tolerance for Microsoft 365 services. Die Datenreplikation stellt sicher, dass es immer mehrere Kopien von Kundendaten in verschiedenen Fehlerzonen gibt, sodass kritische Kundendaten wiederhergestellt werden können, wenn sie beschädigt sind, verloren gehen oder sogar versehentlich vom Kunden gelöscht werden. Die automatisierte Integritätsprüfung erhöht die Datenverfügbarkeit, indem Daten, die von vielen Physischen oder logischen Beschädigungen betroffen sind, automatisch wiederhergestellt werden.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit Resilienz und Kontinuität finden Sie in der folgenden Tabelle.

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: Notfallplan <br> CP-3: Notfallschulung <br> CP-4: Test des Notfallplans <br> CP-6: Alternativer Speicherort <br> CP-7: Alternativer Verarbeitungsstandort <br> CP-9: Sicherung des Informationssystems <br> CP-10: Wiederherstellung und Wiederherstellung des Informationssystems | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Kontinuität der Informationssicherheit <br> A.17.2: Redundanzen | 20. April 2021 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Alle Steuerelemente | 18. März 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Sicherungsrichtlinien <br> CA-50: Geschäftskontinuität <br> CA-51: Datenreplikation | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Sicherungsrichtlinien <br> CA-50: Geschäftskontinuität <br> CA-51: Datenreplikation | 24. Dezember 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09: EXO-E-Mail-Wiederherstellung | 24. Dezember 2020 |

## <a name="resources"></a>Ressourcen

- [Whitepaper zum Microsoft Enterprise Business Continuity Management-Programm](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft Cloud EBCM and Disaster Recovery Plan Validation Report: FY21 Q4](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=83dc940a-2078-4e14-8b7d-07128e5b453d&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Haftungsausschluss

- [Enterprise-Geschäftskontinuität – Haftungsausschluss](assurance-ebcm-legal-disclaimer.md)