---
title: 'Microsoft Security Incident Management: Vorbereitung'
description: Dieser Artikel bietet eine Übersicht über den Vorbereitungsprozess für das Sicherheitsvorfallmanagement in Microsoft-Onlinediensten.
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
ms.openlocfilehash: faa44ccc21ce4252745b7878bf0a280c7ec69f7a5d51e96a236a68359cf8f4ea
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54291783"
---
# <a name="microsoft-security-incident-management-preparation"></a>Microsoft Security Incident Management: Vorbereitung

## <a name="training-and-background-checks"></a>Schulungen und Hintergrundüberprüfungen

Jeder Mitarbeiter, der an Microsoft-Onlinediensten arbeitet, erhält Schulungen zu Sicherheitsvorfällen und Reaktionsverfahren, die ihrer Rolle entsprechen. Jeder Microsoft-Mitarbeiter erhält nach dem Beitritt eine Schulung und danach jedes Jahr eine jährliche Auffrischungsschulung. Die Schulung soll den Mitarbeitern ein grundlegendes Verständnis des Microsoft-Sicherheitsansatzes vermitteln, damit alle Mitarbeiter nach Abschluss der Schulung Folgendes verstehen:

- Definition eines Sicherheitsvorfalls
- Die Verantwortung aller Mitarbeiter, Sicherheitsvorfälle zu melden
- So eskalieren Sie einen potenziellen Sicherheitsvorfall an das entsprechende Sicherheitsreaktionsteam von Microsoft
- Reaktion von Microsoft-Sicherheitsvorfällen auf Sicherheitsvorfälle
- Besondere Bedenken hinsichtlich des Datenschutzes, insbesondere des Datenschutzes beim Kunden
- Hier finden Sie zusätzliche Informationen zu Sicherheit und Datenschutz sowie Zuspitzungskontakten
- Alle anderen relevanten Sicherheitsbereiche (nach Bedarf)

Die entsprechenden Mitarbeiter erhalten jährlich eine Auffrischungsschulung zur Sicherheit. Die jährliche Auffrischungsschulung konzentriert sich auf:

- Alle Änderungen, die im vorherigen Jahr an den Standardvorgehensweisen vorgenommen wurden
- Die Verantwortung aller Personen, Sicherheitsvorfälle zu melden, und wie dies geschieht
- Hier finden Sie zusätzliche Informationen zu Sicherheit und Datenschutz sowie Zuspitzungskontakten
- Alle anderen Sicherheitsfokusbereiche, die jedes Jahr relevant sein können

Jeder Mitarbeiter, der an Microsoft-Onlinediensten arbeitet, unterliegt einer geeigneten und gründlichen Hintergrundüberprüfung, die die Ausbildung, das Arbeitsverhältnis, die vorbestraften Informationen und andere spezifische Informationen gemäß us-amerikanischen Bestimmungen wie Health Insurance Portability and Accountability Act (HIPAA), International Traffic in Arms Regulations (ITAR), Federal Risk and Authorization Management Program (FedRAMP) und andere enthält.

Die Hintergrundüberprüfungen sind für alle Mitarbeiter, die im Microsoft Engineering arbeiten, obligatorisch. Einige Microsoft-Onlinedienstumgebungen und -Operatorrollen erfordern möglicherweise auch vollständige Fingerabdruck- und Kontrollanforderungen, Behördenfreigabeanforderungen und andere strengere Kontrollen. Darüber hinaus können einige Serviceteams und -rollen bei Bedarf spezielle Sicherheitsschulungen durchlaufen. Schließlich erhalten die Mitglieder des Sicherheitsteams selbst spezielle Schulungen und Konferenzteilnahmen, die sich direkt auf die Sicherheit beziehen. Diese Schulung variiert je nach Bedarf des Teams und der Mitarbeiter, umfasst jedoch Branchenkonferenzen, interne Microsoft Security-Konferenzen und externe Schulungskurse über bekannte Anbieter von Sicherheitsschulungen in der Branche. Wir haben auch dedizierte Artikel zur Sicherheitsschulung, die im laufe des Jahres für die Sicherheitscommunity in Microsoft veröffentlicht wurden und sich regelmäßig auf Microsoft-Onlinedienste spezialisiert haben.

## <a name="penetration-testing--assessment"></a>Penetrationstests & Bewertung

Microsoft arbeitet mit verschiedenen Branchenorganisationen und Sicherheitsexperten zusammen, um neue Bedrohungen und sich entwickelnde Trends zu verstehen. Microsoft bewertet kontinuierlich seine eigenen Systeme für Sicherheitsrisiken und schließt Verträge mit verschiedenen unabhängigen, externen Experten, die dies tun.

Die Tests für die Diensthärtung innerhalb von Microsoft-Onlinediensten können in vier allgemeine Kategorien unterteilt werden:

1. **Automatisierte Sicherheitstests:** Interne und externe Mitarbeiter überprüfen regelmäßig Microsoft-Onlinedienstumgebungen basierend auf Microsoft SDL-Praktiken, Open Web Application Security Project (OWASP) top 10-Risiken und neuen Bedrohungen, die von verschiedenen Branchenorganisationen gemeldet werden.
2. **Sicherheitsrisikobewertungen:** Formale Engagements mit unabhängigen Testern von Drittanbietern überprüfen regelmäßig, ob wichtige logische Kontrollen effektiv funktionieren, um die Serviceverpflichtungen verschiedener Aufsichtsbehörden zu erfüllen. Die Bewertungen werden vom Crest -zertifizierten Personal (Council of Registered Ethical Security Testers) durchgeführt und basieren auf den OWASP Top 10-Risiken und anderen dienstbezogenen Bedrohungen. Alle gefundenen Bedrohungen werden bis zum Schließen nachverfolgt.
3. **Fortlaufende Tests von Systemrisiken:** Microsoft führt regelmäßige Tests durch, bei denen Teams versuchen, das System mit neuen Bedrohungen, gemischten Bedrohungen und/oder erweiterten dauerhaften Bedrohungen zu verletzen, während andere Teams versuchen, solche Versuche zu blockieren.
4. **Microsoft Online Services Bug Bounty-Programm:** Dieses Programm betreibt eine Richtlinie, die eingeschränkte, von Kunden stammende Bewertungen von Sicherheitsrisiken in Microsoft-Onlinediensten zulässt. Weitere Informationen finden Sie unter [Microsoft Online Services Bug Bounty Terms](https://www.microsoft.com/msrc/bounty-terms).

Die Microsoft Online Services-Entwicklungsteams veröffentlichen regelmäßig verschiedene Compliance-Dokumente. Mehrere dieser Dokumente sind im Rahmen einer Geheimhaltungsvereinbarung über das [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) oder über den Bereich "Service Assurance" des [Microsoft 365 Compliance Center](https://compliance.office.com)

>[!NOTE]
>Weitere Informationen zum Zugriff auf das Service Trust Portal finden Sie unter "Erste Schritte mit dem Service Trust Portal für Office 365 for Business-, Azure- und Dynamics CRM Online-Abonnements". Für den Zugriff auf die Microsoft 365 Compliance Center ist ein Microsoft 365 Abonnement erforderlich.

## <a name="attack-simulation"></a>Angriffssimulation

Microsoft beteiligt sich an laufenden Angriffssimulationsübungen und Penetrationstests unserer Sicherheits- und Reaktionspläne auf Live-Websites, um die Erkennungs- und Reaktionsfähigkeit zu verbessern. Microsoft simuliert regelmäßig Verletzungen in der Praxis, führt eine kontinuierliche Sicherheitsüberwachung durch und führt Die Reaktion auf Sicherheitsvorfälle durch, um die Sicherheit von Microsoft-Onlinediensten zu überprüfen und zu verbessern.

Microsoft führt mithilfe von zwei Kernteams eine Sicherheitsstrategie zur Annahme von Sicherheitsverletzungen aus:

### <a name="red-teams"></a>Rote Teams

Microsoft Red Teams sind Gruppen von Vollzeitmitarbeitern innerhalb von Microsoft, die sich auf die Verletzung der Infrastruktur, Plattform und der eigenen Mandanten und Anwendungen von Microsoft konzentrieren. Sie sind der dedizierte Angreifer (eine Gruppe von ethischen Hackern), der gezielte und dauerhafte Angriffe auf Onlinedienste durchführt (jedoch keine Kundenanwendungen oder Daten). Sie bieten eine kontinuierliche "vollständige" Validierung (z. B. technische Kontrollen, Papierrichtlinie, menschliche Reaktion usw.) der Funktionen zur Reaktion auf Dienstvorfälle.

### <a name="blue-teams"></a>Blaue Teams

Microsoft Blue-Teams bestehen aus dedizierten Gruppen von Sicherheitsbeantwortern und Mitgliedern aus den Teams für Reaktion auf Sicherheitsvorfälle, Technik und Betrieb. Sie sind unabhängig und arbeiten getrennt von den roten Teams. Die blauen Teams folgen etablierten Sicherheitsprozessen und verwenden die neuesten Tools und Technologien, um Angriffe und Penetrationsversuche zu erkennen und darauf zu reagieren. Genau wie reale Angriffe wissen die blauen Teams nicht, wann oder wie die Angriffe des roten Teams auftreten oder welche Methoden verwendet werden können. Ihre Aufgabe ist es, alle Sicherheitsvorfälle zu erkennen und darauf zu reagieren, unabhängig davon, ob es sich um einen Angriff eines roten Teams oder einen tatsächlichen Angriff handelt. Aus diesem Grund sind die blauen Teams ständig im Bereitschaftsdienst und müssen auf Verstöße gegen das rote Team auf die gleiche Weise reagieren wie bei jedem anderen Angreifer.

Microsoft-Mitarbeiter trennen rote teams in Vollzeit und blaue Teams in verschiedenen Abteilungen, die Vorgänge sowohl über Dienste als auch innerhalb von Microsoft durchführen. Der Ansatz, der als *"Red Teaming"* bezeichnet wird, besteht darin, die Systeme und Vorgänge Microsoft-Dienste mit denselben Taktiken, Techniken und Verfahren wie echte Angreifer gegen die Liveproduktionsinfrastruktur zu testen, ohne dass die Infrastruktur und die Plattformtechnik oder die Betriebsteams bekannt sind. Dadurch werden die Funktionen zur Sicherheitserkennung und -reaktion getestet und Produktionssicherheitsrisiken, Konfigurationsfehler, ungültige Annahmen oder andere Sicherheitsprobleme auf kontrollierte Weise identifiziert. Auf jede Verletzung des roten Teams folgt die vollständige Offenlegung zwischen dem roten und dem blauen Team, einschließlich Serviceteams, um Lücken zu erkennen, Ergebnisse zu beheben und die Reaktion auf Sicherheitsverletzungen erheblich zu verbessern.

>[!NOTE]
>Während der Penetration von Red Teaming- oder Livewebsite-Penetrationsübungen werden keine Kundendaten verwendet. Die Tests beziehen sich auf Microsoft 365 und Azure-Infrastruktur und -Plattformen sowie auf die eigenen Mandanten, Anwendungen und Daten von Microsoft. Kundenmandanten, Anwendungen und Daten, die in Azure, Dynamics 365 oder Microsoft 365 gehostet werden, werden niemals gemäß den vereinbarten Engagementregeln ausgerichtet.

### <a name="joint-exercises"></a>Gemeinsame Übungen

Manchmal führen die Blau- und Rot-Teams von Microsoft gemeinsame Operationen durch, bei denen die Beziehung während des Vorgangs mit einer ausgewählten Gruppe von Mitarbeitern aus den einzelnen Teams partnerfreundlicher als unumstritten ist. Diese Übungen sind gut zwischen den Teams koordiniert, um durch die Zusammenarbeit zwischen ethischen Hackern und Antwortenden in Echtzeit gezieltere Ergebnisse zu erzielen. Diese "lilafarbenen Team"-Übungen sind für jeden Vorgang in hohem Maße zugeschnitten, um die Möglichkeiten zu maximieren, aber für jeden Vorgang ist die Freigabe von Informationen mit hoher Bandbreite und die Partnerschaft von grundlegender Bedeutung, um die Ziele zu erreichen.

## <a name="related-articles"></a>Verwandte Artikel

- [Microsoft-Sicherheitsvorfallverwaltung](assurance-security-incident-management.md)
- [Microsoft Security Incident Management: Erkennung und Analyse](assurance-sim-detection-analysis.md)
- [Microsoft Security Incident Management: Eindämmung, Beseitigung und Wiederherstellung](assurance-sim-containment-eradication-recovery.md)
- [Microsoft-Sicherheitsvorfallverwaltung: Aktivitäten nach dem Vorfall](assurance-sim-post-incident-activity.md)
- [So protokollieren Sie ein Supportticket für Sicherheitsereignisse](/azure/security/fundamentals/event-support-ticket)
- [Azure und Dynamics 365-Benachrichtigung bei Datenschutzverletzung im Rahmen der DSGVO](/compliance/regulatory/gdpr-breach-azure-dynamics)