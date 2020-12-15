---
title: Ausfallsicherheit und Kontinuität
description: Informationen zu Ausfallsicherheit und Kontinuität in Microsoft 365
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
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 2cc3f35a9d109a1a84159de8d0518f58270e3fe9
ms.sourcegitcommit: 1dc97ae3f0511cb1a41565da56e725bbe0cb013c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "49671180"
---
# <a name="resiliency-and-continuity-overview"></a>Ausfallsicherheit und Kontinuität (Übersicht)

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>Wie gewährleistet Microsoft die Geschäftskontinuität im Fall eines Notfalls oder einer anderen Bedrohung der Dienstverfügbarkeit?

Das Microsoft Enterprise Business Continuity Management (EBCM)-Team überwacht Geschäftskontinuitätsmanagement und Notfall Wiederherstellungsaktivitäten in Microsoft-Diensten und Cloud-angeboten. Vertreter von Microsoft Business Units, wie etwa Microsoft 365, koordinieren mit dem EBCM-Team, um Business Continuity-Pläne zu entwickeln und die Einhaltung von Business Continuity-Anforderungen zu validieren.

Im Mittelpunkt unserer Methodik für das Business Continuity-Management (BCM) steht der BCM-Lebenszyklus. Dieser dreistufige Prozess ist so konzipiert, dass er anpassungsfähig ist, sodass er von einer Vielzahl von Geschäftsmodellen in Microsoft implementiert werden kann. Es beginnt mit einer **Bewertungs** Phase, um wichtige Prozesse und Ziele zu identifizieren, die im Business Continuity-Programm berücksichtigt werden sollten. Die Bewertungsphase erfordert auch eine Business Impact Analysis (BIA). In der Phase **Planung** liegt der Schwerpunkt auf der Entwicklung und Umsetzung von Resilienz- und Wiederherstellungsstrategien sowie deren Dokumentation in offiziellen Geschäftskontinuitätsplänen. Schließlich testet die **Funktionsüberprüfung** Geschäftskontinuitätspläne und deren Implementierungen, um die Effektivität zu überprüfen und mögliche Verbesserungen zu identifizieren.

Die Business Continuity-Strategie von Microsoft 365 nutzt Hardware-, Netzwerk-und Rechenzentrums Redundanz. Die Datenreplikation zwischen Rechenzentren bietet hohe Verfügbarkeit und Zuverlässigkeit im Fall eines katastrophalen Vorfalls. Es erhöht auch die Ausfallsicherheit für banale Vorfälle wie isolierten Hardwarefehler oder Datenbeschädigung.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Wie testet Microsoft Business Continuity-und Notfallwiederherstellungspläne?

Die EBCM-Richtlinie (Enterprise Business Continuity Management) von Microsoft legt fest, dass alle Microsoft Business Continuity-und Notfallwiederherstellungspläne auf jährlicher Basis getestet, aktualisiert und überprüft werden müssen. Microsoft 365-Dienste testen Ihre Business Continuity-Pläne mindestens einmal jährlich pro EBCM-Richtlinien. Nachdem Aktionsberichte erstellt und überprüft wurden, um die Ergebnisse zu validieren, zu testen und die Planaktualisierungen als Reaktion auf Probleme zu informieren, die während der Tests erkannt wurden.

Zum Überprüfen von Resilienz- und Wiederherstellungsstrategien mit einer breiten Palette potenzieller Vorfälle definiert das EBCM-Programm mehrere Kategorien von Testszenarien, die sich auf Personen, Standorte und Technologie auswirken. Die für jeden Dienst erforderliche Validierungsebene basiert auf der Wichtigkeit des Diensts, wobei kritischere Dienste eine strengere Validierung erhalten. Jedes Microsoft 365-Dienst Team testet seinen geschäftskontinuitätsplan gemäß den EBCM-Richtlinien, um die Effektivität des Plans und die Bereitschaft des Service Teams zur Ausführung des Plans zu messen.

Pro EBCM-Richtlinien müssen jährliche Überprüfungen der Business Continuity-Pläne und die Funktionsüberprüfung innerhalb von 12 Monaten nach der letzten Überprüfung erfolgen. Die Funktionsüberprüfung muss eine Überprüfung der unterstützenden Dokumentation wie der BIA umfassen, um sicherzustellen, dass Sie korrekt bleibt. Microsoft stellt die Ergebnisse der Funktionsüberprüfung für ausgewählte Microsoft 365-Dienste über vierteljährliche Berichte für unsere Kunden zur Verfügung.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Wie stellt Microsoft 365 sicher, dass die Systemkapazität die Nachfrage erfüllt?

Die Kapazitätsplanung hilft den Serviceteams bei der Zuweisung der Ressourcen, die zur Unterstützung der Verfügbarkeit von Microsoft 365-Diensten erforderlich sind. Im Rahmen des EBCM-Programms von Microsoft ist eine reguläre Kapazitätsplanung erforderlich. Serviceteams überprüfen die Kapazitätsdaten während der vierteljährlichen Überprüfungen sowie in Notsituationen, in denen eine zusätzliche Kapazitätsprüfung erforderlich wird.

Die Rohdaten für die Kapazitätsplanung werden von jedem Service Team verwaltet und enthalten Metriken wie System Verarbeitung, Arbeitsspeicher und Hardwarekapazität. Bei geplanten Überprüfungen wird ein Modell der aktuellen Kapazität des Systems verwendet, und es wird in Notfallsituationen anhand der erwarteten Anforderungen getestet. Wenn das Modell Kapazitätsengpässe anzeigt, werden der Leitung des Serviceteams Änderungsvorschläge zur Prüfung unterbreitet. Genehmigte Änderungen werden in ein neues Modell integriert, bevor es von Serviceteamtechnikern implementiert wird.

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>Wie kann Microsoft 365 während routinemäßigen Systemfehlern die Dienstverfügbarkeit aufrecht erhalten?

Microsoft 365 erreicht Dienstausfall Sicherheit durch redundante Architektur, Datenreplikation und automatisierte Integritätsprüfung. Die redundante Architektur umfasst die Bereitstellung mehrerer Instanzen eines Diensts auf geografisch und physisch getrennter Hardware, wodurch die Fehlertoleranz für Microsoft 365-Dienste erhöht wird. Die Datenreplikation stellt sicher, dass es immer mehrere Kopien von Kundendaten in unterschiedlichen Fehler Zonen gibt, sodass wichtige Kundendaten wiederhergestellt werden können, wenn Sie beschädigt, verloren oder sogar versehentlich vom Kunden gelöscht wurden. Die automatische Integritätsüberprüfung erhöht die Datenverfügbarkeit, indem Daten automatisch wiederhergestellt werden, die durch viele Arten von physischen oder logischen Beschädigungen beeinträchtigt werden.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Verordnungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Bestimmungen und Zertifizierungen überprüft. Lesen Sie die folgende Tabelle zur Validierung von Steuerelementen im Zusammenhang mit Ausfallsicherheit und Kontinuität.

| **Externe Überprüfungen** | **Section** | **Letztes Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: Notfallplan <br> CP-3: Notfall Schulung <br> CP-4: Notfallplan Tests <br> CP-6: alternativer Speicherstandort <br> CP-7: Alternative Verarbeitungs Website <br> CP-9: Information System-Sicherung <br> CP-10: Wiederherstellung und Rekonstitution von Informationssystemen | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 17.1: Kontinuität der Informationssicherheit <br> A. 17.2: Redundanzen | Februar 22, 2020 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Alle Steuerelemente | 18. März 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: Sicherungsrichtlinien <br> CA-50: Business Continuity <br> CA-51: Datenreplikation | 30. September 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: Sicherungsrichtlinien <br> CA-50: Business Continuity <br> CA-51: Datenreplikation | 30. September 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-09: Exo-e-Mail-Wiederherstellung | 30. September 2019 |

## <a name="resources"></a>Ressourcen

- [Whitepaper zum Microsoft Enterprise Business Continuity-Management Programm](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft Cloud EBCM und Notfall Wiederherstellungs Plan – Validierungsbericht: FY21 Q1 und Q2](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=b4181ab3-b03d-4a62-b396-4bfd1c98ddb0&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Rechtlicher Haftungsausschluss

- [Enterprise-Geschäftskontinuität – Haftungsausschluss](assurance-ebcm-legal-disclaimer.md)