---
title: 'Microsoft 365 Security Incident Management: Vorbereitung'
description: Dieser Artikel enthält eine Übersicht über den Vorbereitungsprozess zur Vorbereitung von Sicherheitsvorfällen in Microsoft 365.
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
hideEdit: true
ms.openlocfilehash: b3f16620564d525245c21c375bbc9a3f5b0923b7
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497391"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Microsoft 365 Security Incident Management: Vorbereitung

## <a name="training-and-background-checks"></a>Schulungen und Hintergrundprüfungen

Jeder Mitarbeiter, der an Microsoft 365 arbeitet, wird über Schulungen zu Sicherheitsvorfällen und Reaktionsverfahren informiert, die für ihre Rolle geeignet sind. Jeder Microsoft 365-Mitarbeiter erhält bei seinem Beitritt eine Schulung und anschließend jedes Jahr eine jährliche Aktualisierungsschulung. Die Schulung dient dazu, den Mitarbeitern ein grundlegendes Verständnis von Microsofts Sicherheitsansatz zu bieten, sodass alle Mitarbeiter nach Abschluss der Schulung verstehen:

- Die Definition eines Sicherheitsvorfalls
- Die Verantwortung aller Mitarbeiter, Sicherheitsvorfälle zu melden
- So eskalieren Sie einen potenziellen Sicherheitsvorfall an das Microsoft 365 Security Response-Team
- Reaktion des Microsoft 365 Security Incident Response Teams auf Sicherheitsvorfälle
- Besondere Bedenken hinsichtlich des Datenschutzes, insbesondere des Datenschutzes der Kunden
- Informationen zu Sicherheit und Datenschutz sowie zu Eskalationskontakten
- Alle anderen relevanten Sicherheitsbereiche (nach Bedarf)

Die entsprechenden Mitarbeiter erhalten jährlich Eine Aktualisierungsschulung zur Sicherheit. Die jährliche Aktualisierungsschulung konzentriert sich auf:

- Änderungen an den Standardbetriebsverfahren im vorherigen Jahr
- Die Verantwortung aller, Sicherheitsvorfälle zu melden, und wie dies zu tun ist
- Informationen zu Sicherheit und Datenschutz sowie zu Eskalationskontakten
- Alle anderen Sicherheitsfokusbereiche, die jedes Jahr relevant sein können

Jeder Mitarbeiter, der an Microsoft 365 arbeitet, durchgeht außerdem eine entsprechende und sorgfältige Hintergrundüberprüfung, die bildungs-, beschäftigungs-, strafhistorisch und andere spezifische Informationen nach us-amerikanischen Vorschriften wie Health Insurance Portability and Accountability Act (HIPAA), International Traffic in Arms Regulations (ITAR), Federal Risk and Authorization Management Program (FedRAMP) und andere umfasst.

Die Hintergrundprüfungen sind für alle Mitarbeiter erforderlich, die innerhalb von Microsoft 365 Engineering arbeiten. Einige Microsoft 365-Umgebungen und Operatorrollen erfordern möglicherweise auch vollständige Fingerabdrücke, Anforderungen an die Staatsbürgerschaft, Anforderungen an die Genehmigung durch Behörden und andere strengere Kontrollen. Darüber hinaus können einige Dienstteams und Rollen bei Bedarf spezielle Sicherheitsschulungen durchgehen. Schließlich erhalten die Mitglieder des Sicherheitsteams selbst spezielle Schulungen und Konferenzteilnahmen, die sich direkt auf die Sicherheit beziehen. Diese Schulung variiert je nach Bedarf des Teams und der Mitarbeiter, umfasst jedoch Auch Branchenkonferenzen, interne Microsoft Security-Konferenzen und externe Schulungen über bekannte Anbieter von Sicherheitsschulungen in der Branche. Wir haben auch spezielle Artikel für Sicherheitsschulungen, die das ganze Jahr über für die Sicherheitsgemeinschaft in Microsoft veröffentlicht und regelmäßig auf Microsoft 365 spezialisiert sind.

## <a name="penetration-testing--assessment"></a>Penetrationstests & Bewertung

Microsoft arbeitet mit verschiedenen Branchenorganisationen und Sicherheitsexperten zusammen, um neue Bedrohungen und sich entwickelnde Trends zu verstehen. Microsoft bewertet kontinuierlich seine eigenen Systeme auf Sicherheitsrisiken und verträget mit verschiedenen unabhängigen externen Experten, die dies auch tun.

Die Tests, die für die Dienst hardening in Microsoft 365 durchgeführt werden, können in vier allgemeine Kategorien unterteilt werden:

1. **Automatisierte Sicherheitstests:** Interne und externe Mitarbeiter überprüfen regelmäßig die Microsoft 365-Umgebung basierend auf Microsoft SDL-Methoden, Open Web Application Security Project (OWASP) Top 10-Risiken und neuen Bedrohungen, die von verschiedenen Branchenorganisationen gemeldet werden.
2. **Sicherheitsrisikobewertungen:** Formale Engagements mit unabhängigen Testern von Drittanbietern überprüfen regelmäßig, ob wichtige logische Steuerelemente effektiv funktionieren, um die Dienstverpflichtungen verschiedener Aufsichtsbehörden zu erfüllen. Die Bewertungen werden vom Council of Registered Ethical Security Testers (CREST)-zertifizierten Personal durchgeführt und basieren auf OWASP Top 10-Risiken und anderen dienstbezogenen Bedrohungen. Alle gefundenen Bedrohungen werden bis zum Schließen nachverfolgt.
3. **Kontinuierliche Systemrisikotests:** Microsoft führt regelmäßige Tests durch, bei denen Teams versuchen, das System mit neuen Bedrohungen, gemischten Bedrohungen und/oder erweiterten dauerhaften Bedrohungen zu durchbrochen, während andere Teams versuchen, solche Versuche zu blockieren.
4. **Microsoft Online Services Bug Bounty Program**: Dieses Programm verwendet eine Richtlinie zum Zulassen begrenzter, vom Kunden stammender Sicherheitsrisikobewertungen auf Microsoft 365. Weitere Informationen finden Sie [unter Microsoft Online Services Bug Bounty Terms](https://www.microsoft.com/msrc/bounty-terms).

Das Microsoft 365-Engineering-Team veröffentlicht regelmäßig verschiedene Compliancedokumente. Mehrere dieser Dokumente sind im Rahmen einer Geheimhaltungsvereinbarung im [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) oder im Bereich Service Assurance des Microsoft [365 Compliance Centers verfügbar.](https://compliance.office.com)

>[!NOTE]
>Weitere Informationen zum Zugriff auf das Dienstvertrauensportal finden Sie unter Erste Schritte mit dem Dienstvertrauensportal für Office 365 Business-, Azure- und Dynamics CRM Online-Abonnements. Für den Zugriff auf das Microsoft 365 Compliance Center ist ein Microsoft 365-Abonnement erforderlich.

## <a name="attack-simulation"></a>Angriffssimulation

Microsoft setzt sich für laufende Angriffssimulationsübungen und Penetrationstests vor Ort unserer Sicherheits- und Reaktionspläne ein, um die Erkennungs- und Reaktionsfähigkeit zu verbessern. Microsoft simuliert regelmäßig reale Sicherheitsverletzungen, führt eine kontinuierliche Sicherheitsüberwachung durch und führt Sicherheitsvorfälle aus, um die Sicherheit von Microsoft 365 und Azure zu überprüfen und zu verbessern.

Microsoft führt eine Sicherheitsstrategie für Sicherheitsverletzungen mit zwei Kernteams aus:

### <a name="red-teams"></a>Rote Teams

Das Microsoft 365 Security Red Team ist eine Gruppe von Vollzeitmitarbeitern in Microsoft, die sich auf die Verletzung der Infrastruktur, plattform von Microsoft und der eigenen Mandanten und Anwendungen von Microsoft konzentriert. Sie sind der dedizierte Angreifer (eine Gruppe von ethischen Hackern), die gezielte und dauerhafte Angriffe auf Onlinedienste durchführen (aber keine Kundenanwendungen oder Daten). Sie bieten eine kontinuierliche Überprüfung des "vollständigen Spektrums" (z. B. technische Kontrollen, Papierrichtlinie, menschliche Reaktion usw.) der Funktionen zur Reaktion auf Dienstvorfälle.

### <a name="blue-teams"></a>Blaue Teams

Das Microsoft 365 Security Blue Team besteht aus einem dedizierten Satz von Sicherheitsantwortern und Mitgliedern aus den Teams für reaktions-, engineering- und betriebstechnische Sicherheitsvorfälle. Sie sind unabhängig und arbeiten getrennt vom Roten Team. Das Blaue Team folgt etablierten Sicherheitsprozessen und verwendet die neuesten Tools und Technologien, um Angriffe und Penetrationsversuche zu erkennen und darauf zu reagieren. Genau wie bei realen Angriffen weiß das Blaue Team nicht, wann oder wie die Angriffe des roten Teams auftreten oder welche Methoden verwendet werden können. Ihre Aufgabe ist es, alle Sicherheitsvorfälle zu erkennen und darauf zu reagieren, ob es sich um einen Angriff des roten Teams oder einen tatsächlichen Angriff handelt. Aus diesem Grund ist das blaue Team ständig in Abruf und muss auf Verstöße gegen das rote Team genauso reagieren wie für jeden anderen Gegner.

Die Mitarbeiter von Microsoft trennen vollzeitbearbeitende rote teams und blaue Teams in verschiedenen Abteilungen, die Vorgänge sowohl über die Dienste als auch innerhalb von Microsoft hinweg durchführen. Der Ansatz, der als Rotes *Teaming* bezeichnet wird, besteht in der Prüfung der Systeme und Vorgänge der Microsoft-Dienste mit denselben Taktiken, Techniken und Verfahren wie echte Gegner, ohne das Wissen der Infrastruktur- und Plattformtechnik- oder Betriebsteams. Dies testet die Erkennungs- und Reaktionsfunktionen der Sicherheit und hilft, Produktionsrisiken, Konfigurationsfehler, ungültige Annahmen oder andere Sicherheitsprobleme kontrolliert zu identifizieren. Auf jede Verletzung des roten Teams folgt eine vollständige Offenlegung zwischen dem Roten Team und dem Blauen Team, einschließlich Dienstteams, um Lücken zu identifizieren, Erkenntnisse zu beseitigen und die Reaktion auf Sicherheitsverletzungen erheblich zu verbessern.

>[!NOTE]
>Während der Übungen zum Roten Teaming oder bei Livewebsitedurchdringungsübungen werden keine Kundendaten gezielt verwendet. Die Tests sind für die Microsoft 365- und Azure-Infrastruktur und -Plattformen sowie für die eigenen Mandanten, Anwendungen und Daten von Microsoft geeignet. Kunden mandanten, Anwendungen und Daten, die in Microsoft 365 oder Azure gehostet werden, werden niemals nach den vereinbarten Verpflichtungsregeln ausgerichtet.

### <a name="joint-exercises"></a>Gemeinsame Übungen

Manchmal führen die Teams von Microsoft 365 Security Blue und Red gemeinsame Vorgänge durch, bei denen die Beziehung während des Vorgangs mehr Partner als gegnerisch mit einer ausgewählten Gruppe von Mitarbeitern aus jedem Team ist. Diese Übungen sind gut zwischen den Teams abgestimmt, um eine gezieltere Reihe von Ergebnissen durch die Echtzeitzusammenarbeit zwischen ethischen Hackern und Reaktionshelfern zu erzielen. Diese Übungen des "lila Team" sind auf jeden Vorgang zugeschnitten, um die Möglichkeit zu maximieren, aber grundlegend für jeden Vorgang ist die gemeinsame Nutzung von Informationen mit hoher Bandbreite und die Partnerschaft, um die Ziele zu erreichen.

## <a name="related-articles"></a>Verwandte Artikel

- [Verwaltung von Sicherheitsvorfällen unter Microsoft 365](assurance-security-incident-management.md)
- [Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365](assurance-sim-detection-analysis.md)
- [Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen in Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 Security Incident Management post-incident activity](assurance-sim-post-incident-activity.md)
