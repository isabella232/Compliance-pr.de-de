---
title: 'Verwaltung von Sicherheitsvorfällen in Microsoft 365: Erkennung und Analyse'
description: Dieser Artikel bietet eine Übersicht über die Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365.
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
ms.openlocfilehash: 1fbdca0c0b08c793732ba31414bedd943d4dc115
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037602"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a>Verwaltung von Sicherheitsvorfällen in Microsoft 365: Erkennung und Analyse

Um böswillige Aktivitäten zu erkennen, protokolliert Microsoft 365 Sicherheitsereignisse und andere Daten zentral und führt verschiedene Analysetechniken aus, um anomale oder verdächtige Aktivitäten zu finden. Protokolldateien werden von Microsoft 365-Servern und Infrastrukturgeräten gesammelt und in einer zentralen und konsolidierten Datenbank gespeichert.

Microsoft verwendet einen risikobasierten Ansatz zum Erkennen bösartiger Aktivitäten. Wir verwenden Vorfalldaten und Informationen zu Bedrohungen, um unsere Erkennungen zu definieren und zu priorisieren.

Die Beschäftigung eines Teams aus erfahrenen, erfahrenen und qualifizierten Personen ist eine der wichtigsten Säulen für den Erfolg in der Erkennungs- und Analysephase. Microsoft 365 beschäftigt mehrere Serviceteams, und diese Teams umfassen Mitarbeiter mit Kompetenzen für alle Komponenten innerhalb des Stapels, einschließlich Netzwerk, Router, Firewalls, Lastenausgleichssysteme, Betriebssysteme und Anwendungen.

Die Sicherheitsmaßnahmen in Microsoft 365 umfassen auch Benachrichtigungen und Warnungen, die von verschiedenen Quellen initiiert werden. Das Microsoft 365 Security Response-Team ist der wichtigste Orchestrierungsor des Eskalationsprozesses für Sicherheitsvorfälle. Dieses Team empfängt alle Eskalationen und ist für die Analyse und Bestätigung der Gültigkeit des Sicherheitsvorfalls verantwortlich.

Eine der wichtigsten Säulen der Erkennung ist die Benachrichtigung:

- Jedes Serviceteam ist dafür verantwortlich, alle Aktionen oder Ereignisse innerhalb des Diensts basierend auf den Anforderungen des Microsoft 365 -Sicherheitsteams zu protokollieren. Alle Protokolle, die von den verschiedenen Serviceteams erstellt werden, werden von einer SIEM (Security Information and Event Management)-Lösung mit vordefinierten Sicherheits- und Erkennungsregeln verarbeitet. Diese Regeln werden basierend auf der Empfehlung des Microsoft 365 -Sicherheitsteams auf Grundlage von Informationen aus vorherigen Sicherheitsvorfällen weiterentwickelt, um festzustellen, ob verdächtige oder böswillige Aktivitäten vor sich sind.
- Wenn ein Kunde feststellt, dass ein Sicherheitsvorfall läuft, kann er einen Supportfall bei Microsoft öffnen, der dem Microsoft 365 Customer Experience (CxP)-Kommunikationsteam zugewiesen ist und zu einer Eskalation an alle entsprechenden Teams wird.

Microsoft 365-Serviceteams nutzen auch die in der Trendanalyse durch Sicherheitsüberwachung und Protokollierung gewonnenen Informationen, um Anomalien in Microsoft 365-Informationssystemen zu erkennen, die auf einen Angriff oder einen Sicherheitsvorfall hinweisen können. Microsoft 365-Server aggregieren die Ausgabe aus diesen Protokollen in der Produktionsumgebung in einem zentralisierten Protokollierungsserver. Von diesem zentralisierten Protokollierungsserver werden Protokolle untersucht, um Trends in der gesamten Produktionsumgebung zu erkennen. Auf dem zentralen Server aggregierte Daten werden sicher in einen Protokollierungsdienst übertragen, um erweiterte Abfragen, Dashboards zu erstellen und anomale und schädliche Aktivitäten zu erkennen. Der Dienst verwendet auch maschinelles Lernen, um Anomalien mit der Protokollausgabe zu erkennen.

Während der Eskalationsphase und in Abhängigkeit von der Art des Sicherheitsvorfalls kann das Microsoft 365 Security Response-Team einen oder mehrere Experten aus verschiedenen Teams bei Microsoft an einem oder mehreren Experten beteiligen:

- Sicherheits- und Complianceteam für Onlinedienste
- Microsoft Threat Intelligence Center (MSTIC)
- Microsoft Security Response Center (MSRC)
- Corporate, External, and Legal Affairs (CELA)
- Azure Security
- Microsoft 365 Engineering und andere.

Bevor es zu einer Eskalation an das Microsoft 365 Security Response-Team kommt, ist das Serviceteam für die Ermittlung und Festlegung des Schweregrads des Sicherheitsvorfalls auf der Grundlage definierter Kriterien verantwortlich, z. B.:

- Datenschutz
- Auswirkung
- Bereich
- Anzahl der betroffenen Mandanten
- Region
- Dienst
- Details zum Vorfall
- Spezifische Branchen- oder Marktbestimmungen für Kunden.

Die Vorfalls priorisierung wird anhand unterschiedlicher Faktoren bestimmt, einschließlich, aber nicht beschränkt auf die funktionalen Auswirkungen des Vorfalls, die Informationswirkung des Vorfalls und die Wiederherstellbarkeit des Vorfalls.

Nach dem Empfang einer Eskalation zu einem Sicherheitsvorfall organisiert das Microsoft 365 -Sicherheitsteam ein virtuelles Team (v-Team), das aus Mitgliedern aus dem Microsoft 365 Security Response-Team, Serviceteams und dem Microsoft 365 Incident Communication Team besteht. Der komplexere Teil der Aktivitäten dieses v-Teams besteht in der Bestätigung des Sicherheitsvorfalls und der Beseitigung falsch positiver Ergebnisse. Die Genauigkeit der Informationen, die von den in der Vorbereitungsphase ermittelten Indikatoren bereitgestellt werden, ist von entscheidender Bedeutung. Durch Analysieren dieser Informationen nach Kategorie des Vektorangriffs kann das v-Team ermitteln, ob der Sicherheitsvorfall ein berechtigtes Problem ist.

Zu Beginn der Untersuchung zeichnet das Office Security Incident Response Team alle Informationen zu dem Vorfall gemäß unseren Fallverwaltungsrichtlinien auf. Im Laufe des Falls verfolgen wir laufende Aktionen und befolgen Standards für die Behandlung von Nachweisen zum Sammeln, Beibehalten und Schützen dieser Daten während des gesamten Vorfallslebenszyklus.

Beispiele für diese Aktionen sind:

- Eine Zusammenfassung, die eine kurze Beschreibung des Vorfalls und seiner potenziellen Auswirkungen ist
- Schwere und Priorität des Vorfalls, die durch Bewerten der potenziellen Auswirkungen abgeleitet werden
- Eine Liste aller identifizierten Indikatoren, die zur Erkennung des Vorfalls geführt haben
- Eine Liste aller ähnlichen Vorfälle
- Eine Liste aller Vom v-Team ergriffenen Aktionen
- Alle gesammelten Nachweise, die auch für die nachträgliche Analyse und zukünftige forensische Untersuchungen aufbewahrt werden
- Empfohlene nächste Schritte

Nach der Bestätigung des Sicherheitsvorfalls sind die Hauptziele des Microsoft 365 Security Response-Teams und des entsprechenden Serviceteams die Eindämmung des Angriffs, der Schutz der angegriffenen Dienste und die Vermeidung größerer globaler Auswirkungen. Gleichzeitig arbeiten die entsprechenden Entwicklungsteams an der Ermittlung der Hauptursache und der Vorbereitung des ersten Wiederherstellungsplans.

In der nächsten Phase identifiziert das Microsoft 365 Security Response-Team gegebenenfalls die von dem Sicherheitsvorfall betroffenen Kunden. Der Wirkungsbereich kann je nach Region, Rechenzentrum, Dienst, Serverfarm, Server usw. einige Zeit dauern. Die Liste der betroffenen Kunden wird vom Serviceteam und dem Microsoft 365 CxP Communications-Team zusammengestellt, die dann den Kundenbenachrichtigungsprozess im Rahmen vertraglicher und Complianceverpflichtungen verarbeiten.

## <a name="related-articles"></a>Verwandte Artikel

- [Verwaltung von Sicherheitsvorfällen in Microsoft 365](assurance-security-incident-management.md)
- [Vorbereitung der Verwaltung von Sicherheitsvorfällen in Microsoft 365](assurance-sim-preparation.md)
- [Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen in Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365-Sicherheitsvorfallverwaltung nach einem Vorfall](assurance-sim-post-incident-activity.md)
