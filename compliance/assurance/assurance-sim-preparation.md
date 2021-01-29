---
title: 'Verwaltung von Sicherheitsvorfällen in Microsoft 365: Vorbereitung'
description: Dieser Artikel bietet eine Übersicht über den Vorbereitungsprozess für die Verwaltung von Sicherheitsvorfällen in Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: b14a9fa236cd71cff7dd02baf04a30c249bc4346
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040338"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Verwaltung von Sicherheitsvorfällen in Microsoft 365: Vorbereitung

## <a name="training-and-background-checks"></a>Schulungen und Hintergrundprüfungen

Jeder Mitarbeiter, der an Microsoft 365 arbeitet, wird mit Schulungen zu Sicherheitsvorfällen und Reaktionsverfahren entsprechend seiner Rolle versorgt. Jeder Microsoft 365-Mitarbeiter erhält bei seinem Beitritt eine Schulung und danach jedes Jahr eine jährliche Auffrischungsschulung. Die Schulung dient dazu, den Mitarbeitern ein grundlegendes Verständnis des Sicherheitsansatzes von Microsoft zu bieten, damit alle Mitarbeiter nach Abschluss der Schulung verstehen:

- Die Definition eines Sicherheitsvorfalls
- Die Verantwortung aller Mitarbeiter, Sicherheitsvorfälle zu melden
- So eskalieren Sie einen potenziellen Sicherheitsvorfall an das Microsoft 365 Security Response-Team
- Reaktion des Microsoft 365 Security Incident Response Teams auf Sicherheitsvorfälle
- Besondere Bedenken hinsichtlich des Datenschutzes, insbesondere des Datenschutzes von Kunden
- Wo zusätzliche Informationen zu Sicherheit und Datenschutz sowie zu Eskalationskontakten zu finden sind
- Alle anderen relevanten Sicherheitsbereiche (nach Bedarf)

Die entsprechenden Mitarbeiter erhalten jährlich eine Auffrischungsschulung zur Sicherheit. Die jährliche Aktualisierungsschulung konzentriert sich auf:

- Änderungen an den Standardbetriebsverfahren im vorherigen Jahr
- Die Verantwortung aller, Sicherheitsvorfälle zu melden, und wie dies funktioniert
- Wo zusätzliche Informationen zu Sicherheit und Datenschutz sowie zu Eskalationskontakten zu finden sind
- Alle anderen Sicherheitsfokusbereiche, die jedes Jahr relevant sein können

Jeder Mitarbeiter, der an Microsoft 365 arbeitet, durchgeht auch eine geeignete und gründliche Hintergrundprüfung, die die Ausbildung, das Anstellungswesen, die Geschichte des Strafvollbilds und andere spezifische Informationen nach us-amerikanischen Bestimmungen wie Health Insurance Portability and Accountability Act (HIPAA), International Traffic in Arms Regulations (ITAR), Federal Risk and Authorization Management Program (FedRAMP) und andere umfasst.

Die Hintergrundprüfungen sind für alle Mitarbeiter obligatorisch, die in Microsoft 365 Engineering arbeiten. Einige Microsoft 365-Umgebungen und Operatorrollen erfordern möglicherweise auch vollständige Fingerabdrücke, Anforderungen an die Bürgerschaft, Freigabeanforderungen für Behörden und andere strengere Kontrollen. Darüber hinaus werden einige Serviceteams und Rollen bei Bedarf spezielle Sicherheitsschulungen durchgehen. Schließlich erhalten die Mitglieder des Sicherheitsteams selbst spezielle Schulungen und Konferenzteilnahmen, die sich direkt auf die Sicherheit beziehen. Diese Schulung variiert je nach Bedarf des Teams und der Mitarbeiter, umfasst aber auch Branchenkonferenzen, interne Microsoft -Sicherheitskonferenzen und externe Schulungskurse über bekannte Sicherheitsschulungsanbieter in der Branche. Wir haben auch dedizierte Artikel zu Sicherheitsschulungen veröffentlicht, die das ganze Jahr über für die Sicherheits-Community in Microsoft veröffentlicht werden und regelmäßig auf Microsoft 365 spezialisiert sind.

## <a name="penetration-testing--assessment"></a>Penetrationstests & Bewertung

Microsoft arbeitet mit verschiedenen Branchenorganisationen und Sicherheitsexperten zusammen, um neue Bedrohungen und sich entwickelnde Trends zu verstehen. Microsoft überprüft kontinuierlich seine eigenen Systeme auf Sicherheitsrisiken und bevertragt sich mit verschiedenen unabhängigen, externen Experten, die dies tun.

Die Tests für die Dienstprüfung in Microsoft 365 können in vier allgemeine Kategorien unterteilt werden:

1. **Automatisierte Sicherheitstests:** Interne und externe Mitarbeiter überprüfen regelmäßig die Microsoft 365-Umgebung basierend auf Microsoft SDL-Praktiken, Open Web Application Security Project (OWASP) Top 10-Risiken und neuen Bedrohungen, die von verschiedenen Branchenorganisationen gemeldet werden.
2. **Sicherheitsrisikobewertungen:** Formelle Engagements mit unabhängigen Testern von Drittanbietern überprüfen regelmäßig, ob wichtige logische Kontrollen effektiv funktionieren, um die Dienstverpflichtungen verschiedener Aufsichtsbehörden zu erfüllen. Die Bewertungen werden vom Council of Registered Ethical Security Testers (CREST)-zertifizierten Personal durchgeführt und basieren auf den OWASP Top 10-Risiken und anderen dienstbezogenen Bedrohungen. Alle gefundenen Bedrohungen werden bis zum Schließen nachverfolgt.
3. **Kontinuierliche Tests von Sicherheitslücken im System:** Microsoft führt regelmäßige Tests durch, bei denen Teams versuchen, das System durch neue Bedrohungen, gemischte Bedrohungen und/oder fortgeschrittene dauerhafte Bedrohungen zu verletzten, während andere Teams versuchen, solche Versuche zu blockieren.
4. **Microsoft Online Services Bug Bounty-Programm:** Dieses Programm betreibt eine Richtlinie zum Zulassen eingeschränkter, vom Kunden stammender Sicherheitsrisikobewertungen in Microsoft 365. Weitere Informationen finden Sie unter [Microsoft Online Services Bug Bounty Terms](https://www.microsoft.com/msrc/bounty-terms).

Das Microsoft 365-Entwicklungsteam veröffentlicht regelmäßig verschiedene Compliancedokumente. Mehrere dieser Dokumente sind im Rahmen einer Geheimhaltungsvereinbarung im [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) oder im Bereich Service Assurance des Microsoft [365 Compliance Centers verfügbar.](https://compliance.office.com)

>[!NOTE]
>Weitere Informationen zum Zugriff auf das Service Trust Portal finden Sie unter "Erste Schritte mit dem Service Trust Portal für Office 365 Business-, Azure- und Dynamics CRM Online-Abonnements". Für den Zugriff auf das Microsoft 365 Compliance Center ist ein Microsoft 365-Abonnement erforderlich.

## <a name="attack-simulation"></a>Angriffssimulation

Microsoft setzt sich an kontinuierlichen Angriffssimulationsübungen und Penetrationstests unserer Sicherheits- und Reaktionspläne am Standort durch, um die Erkennungs- und Reaktionsfähigkeit zu verbessern. Microsoft simuliert regelmäßig reale Sicherheitsverletzungen, führt eine fortlaufende Sicherheitsüberwachung durch und verwendet Die Reaktion auf Sicherheitsvorfälle, um die Sicherheit von Microsoft 365 und Azure zu überprüfen und zu verbessern.

Microsoft führt eine Sicherheitsstrategie mit zwei Kernteams aus:

### <a name="red-teams"></a>Rote Teams

Das rote Microsoft 365 Security Team ist eine Gruppe von Vollzeitmitarbeitern innerhalb von Microsoft, die sich auf die Verletzung der Infrastruktur, der Plattform und der eigenen Mandanten und Anwendungen von Microsoft von Microsoft konzentriert. Sie sind der dedizierte Angreifer (eine Gruppe von ethischen Hackern), der gezielte und dauerhafte Angriffe auf Onlinedienste (aber keine Kundenanwendungen oder -daten) durchführen. Sie bieten eine kontinuierliche Überprüfung des vollständigen Spektrums (z. B. technische Kontrollen, Papierrichtlinien, menschliche Reaktion usw.) der Funktionen zur Reaktion auf Dienstvorfälle.

### <a name="blue-teams"></a>Blaue Teams

Das Microsoft 365 Security Blue Team besteht aus einem dedizierten Satz von Security Respondern und Mitgliedern aus den Teams für die Reaktion auf Sicherheitsvorfälle, Technik und Betrieb. Sie sind unabhängig und arbeiten separat vom roten Team. Das Blaue Team folgt etablierten Sicherheitsprozessen und verwendet die neuesten Tools und Technologien, um Angriffe und Penetrationsversuche zu erkennen und darauf zu reagieren. Genau wie reale Angriffe weiß das blaue Team nicht, wann oder wie die Angriffe des roten Teams auftreten oder welche Methoden verwendet werden können. Ihre Aufgabe ist es, alle Sicherheitsvorfälle zu erkennen und darauf zu reagieren, ob es sich um einen Angriff des roten Teams oder einen tatsächlichen Angriff handelt. Aus diesem Grund ist das blaue Team ständig im Anruf und muss auf Verstöße des roten Teams auf die gleiche Weise reagieren wie bei jedem anderen Widerswilligen.

Die Mitarbeiter von Microsoft trennen vollzeitbearbeitende rote teams und blaue Teams in verschiedenen Abteilungen, die Vorgänge sowohl über Dienste als auch innerhalb von Microsoft hinweg durchführen. Der Ansatz, der als *"Rotes Teaming"* bezeichnet wird, besteht im Testen der Systeme und Vorgänge von Microsoft-Diensten mit denselben Taktiken, Techniken und Verfahren wie echte Gegner gegen die Liveproduktionsinfrastruktur, ohne das Wissen der Infrastruktur- und Plattformentwicklungs- oder Betriebsteams. Dies testet die Sicherheitserkennungs- und Reaktionsfunktionen und hilft dabei, Sicherheitsrisiken, Konfigurationsfehler, ungültige Annahmen oder andere Sicherheitsprobleme kontrolliert zu identifizieren. Auf jede Verletzung des roten Teams folgt eine vollständige Offenlegung zwischen dem roten Team und dem blauen Team, einschließlich Serviceteams, um Lücken zu identifizieren, Erkenntnisse zu beseitigen und die Reaktion auf Sicherheitsverletzungen erheblich zu verbessern.

>[!NOTE]
>Bei Übungen zur Penetration von roten Teams oder Livewebsites werden keine Kundendaten gezielt verwendet. Die Tests werden mit der Microsoft 365- und der Azure-Infrastruktur und -Plattformen sowie mit den eigenen Mandanten, Anwendungen und Daten von Microsoft durchgeführt. Kunden-Mandanten, Anwendungen und Daten, die in Microsoft 365 oder Azure gehostet werden, werden niemals nach den vereinbarten Interaktionsregeln ausgerichtet.

### <a name="joint-exercises"></a>Gemeinsame Übungen

Manchmal führen die Teams von Microsoft 365 Security Blue und Red gemeinsame Vorgänge durch, bei denen die Beziehung während des Vorgangs mehr Partner ist als mit einer ausgewählten Gruppe von Mitarbeitern aus den einzelnen Teams. Diese Übungen sind zwischen den Teams gut koordiniert, um durch die Zusammenarbeit zwischen ethischen Hackern und Reaktionskräften in Echtzeit eine gezieltere Ergebnisgruppe zu erzielen. Diese "lila Team"-Übungen sind sehr genau auf jeden Vorgang zugeschnitten, um die Gelegenheit zu maximieren, aber grundlegend für jeden Vorgang ist die Gemeinsame Nutzung von Informationen mit hoher Bandbreite und die Partnerschaft, um die Ziele zu erreichen.

## <a name="related-articles"></a>Verwandte Artikel

- [Verwaltung von Sicherheitsvorfällen in Microsoft 365](assurance-security-incident-management.md)
- [Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365](assurance-sim-detection-analysis.md)
- [Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen in Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365-Sicherheitsvorfallverwaltung nach einem Vorfall](assurance-sim-post-incident-activity.md)
