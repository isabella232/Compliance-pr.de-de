---
title: 'Microsoft 365 Security Incident Management: Erkennung und Analyse'
description: Dieser Artikel bietet eine Übersicht über den Prozess zur Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365.
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
ms.openlocfilehash: 433b8da98e25c4f465473143074eda055419234d
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497402"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a>Microsoft 365 Security Incident Management: Erkennung und Analyse

Um schädliche Aktivitäten zu erkennen, protokolliert Microsoft 365 Sicherheitsereignisse und andere Daten zentral und führt verschiedene Analysetechniken aus, um anomale oder verdächtige Aktivitäten zu finden. Protokolldateien werden von Microsoft 365-Servern und Infrastrukturgeräten gesammelt und in einer zentralen und konsolidierten Datenbank gespeichert.

Microsoft verwendet einen risikobasierten Ansatz, um schädliche Aktivitäten zu erkennen. Wir verwenden Vorfalldaten und Bedrohungserkennung, um unsere Erkennungen zu definieren und zu priorisieren.

Die Beschäftigung eines Teams aus erfahrenen, erfahrenen und qualifizierten Personen ist eine der wichtigsten Säulen für den Erfolg in der Erkennungs- und Analysephase. Microsoft 365 beschäftigt mehrere Serviceteams, zu denen Mitarbeiter gehören, die über Kompetenzen für alle Komponenten innerhalb des Stapels verfügen, einschließlich Netzwerk, Router, Firewalls, Lastenausgleich, Betriebssysteme und Anwendungen.

Die Sicherheitserkennungsmechanismen in Microsoft 365 umfassen auch Benachrichtigungen und Warnungen, die von verschiedenen Quellen initiiert werden. Das Microsoft 365 Security Response-Team ist der zentrale Orchestrierungsor des Eskalationsprozesses für Sicherheitsvorfälle. Dieses Team empfängt alle Eskalationen und ist für die Analyse und Bestätigung der Gültigkeit des Sicherheitsvorfalls verantwortlich.

Eine der wichtigsten Säulen der Erkennung ist die Benachrichtigung:

- Jedes Dienstteam ist dafür verantwortlich, alle Aktionen oder Ereignisse innerhalb des Diensts basierend auf den Anforderungen des Microsoft 365-Sicherheitsteams zu protokollieren. Alle von den verschiedenen Dienstteams erstellten Protokolle werden von einer SIEM-Lösung (Security Information and Event Management) mit vordefinierten Sicherheits- und Erkennungsregeln verarbeitet. Diese Regeln werden basierend auf der Empfehlung des Microsoft 365-Sicherheitsteams basierend auf Informationen aus früheren Sicherheitsvorfällen entwickelt, um festzustellen, ob verdächtige oder böswillige Aktivitäten vor sich sind.
- Wenn ein Kunde feststellt, dass ein Sicherheitsvorfall im Gange ist, kann er einen Supportfall bei Microsoft öffnen, der dem Microsoft 365 Customer Experience (CxP)-Kommunikationsteam zugewiesen ist und zu einer Eskalation für alle entsprechenden Teams wurde.

Microsoft 365-Dienstteams nutzen auch die in der Trendanalyse durch Sicherheitsüberwachung und Protokollierung gewonnenen Erkenntnisse, um Anomalien in Microsoft 365-Informationssystemen zu erkennen, die auf einen Angriff oder einen Sicherheitsvorfall hinweisen können. Microsoft 365-Server aggregieren die Ausgabe aus diesen Protokollen in der Produktionsumgebung in einem zentralen Protokollierungsserver. Von diesem zentralisierten Protokollierungsserver werden Protokolle untersucht, um Trends in der gesamten Produktionsumgebung zu erkennen. Daten, die auf dem zentralen Server aggregiert werden, werden sicher an einen Protokollierungsdienst übertragen, um erweiterte Abfragen, Dashboards zu erstellen und anomale und schädliche Aktivitäten zu erkennen. Der Dienst verwendet auch maschinelles Lernen, um Anomalien bei der Protokollausgabe zu erkennen.

Während der Eskalationsphase und je nach Art des Sicherheitsvorfalls kann das Microsoft 365 Security Response-Team einen oder mehrere Experten aus verschiedenen Teams bei Microsoft an sich beteiligen:

- Sicherheits- und Complianceteam für Onlinedienste
- Microsoft Threat Intelligence Center (MSTIC)
- Microsoft Security Response Center (MSRC)
- Corporate, External, and Legal Affairs (CELA)
- Azure Security
- Microsoft 365 Engineering und andere.

Bevor es zu einer Eskalation an das Microsoft 365 Security Response-Team kommt, ist das Dienstteam für die Ermittlung und Festlegung des Schweregrads des Sicherheitsvorfalls auf der Grundlage definierter Kriterien wie z. B.:

- Datenschutz
- Auswirkung
- Bereich
- Anzahl der betroffenen Mandanten
- Region
- Dienst
- Details des Vorfalls
- Spezifische Branchen- oder Marktbestimmungen für Kunden.

Die Priorisierung von Vorfällen wird anhand unterschiedlicher Faktoren bestimmt, einschließlich, aber nicht beschränkt auf die funktionalen Auswirkungen des Vorfalls, die Informationswirkung des Vorfalls und die Wiederherstellbarkeit des Vorfalls.

Nach dem Empfang einer Eskalation zu einem Sicherheitsvorfall organisiert das Microsoft 365-Sicherheitsteam ein virtuelles Team (v-Team), das aus Mitgliedern des Microsoft 365 Security Response-Teams, service teams und dem Microsoft 365 Incident Communication-Team besteht. Der komplexere Teil der Aktivitäten dieses v-Teams besteht in der Bestätigung des Sicherheitsvorfalls und der Beseitigung falsch positiver Ergebnisse. Die Genauigkeit der Informationen, die von den in der Vorbereitungsphase ermittelten Indikatoren bereitgestellt werden, ist entscheidend. Durch die Analyse dieser Informationen nach Kategorie des Vektorangriffs kann das v-Team ermitteln, ob der Sicherheitsvorfall ein berechtigtes Problem ist.

Zu Beginn der Untersuchung zeichnet das Office Security Incident Response-Team alle Informationen zu dem Vorfall gemäß unseren Fallverwaltungsrichtlinien auf. Im Laufe des Falls verfolgen wir fortlaufende Aktionen und befolgen Standards für die Beweisbehandlung für das Sammeln, Speichern und Sichern dieser Daten während des gesamten Lebenszyklus von Vorfällen.

Beispiele für diese Aktionen sind:

- Eine Zusammenfassung, die eine kurze Beschreibung des Vorfalls und seiner potenziellen Auswirkungen ist.
- Schweregrad und Priorität des Vorfalls, die durch die Bewertung der potenziellen Auswirkungen abgeleitet werden
- Eine Liste aller identifizierten Indikatoren, die zur Erkennung des Vorfalls geführt haben
- Eine Liste aller ähnlichen Vorfälle
- Eine Liste aller vom v-team ergriffenen Aktionen
- Alle gesammelten Nachweise, die auch für die Post-Mortem-Analyse und zukünftige forensische Untersuchungen aufbewahrt werden
- Empfohlene nächste Schritte

Nach der Bestätigung von Sicherheitsvorfällen sind die Hauptziele des Microsoft 365 Security Response-Teams und des entsprechenden Serviceteams, den Angriff zu verhindern, die angegriffenen Dienste zu schützen und größere globale Auswirkungen zu vermeiden. Gleichzeitig arbeiten die entsprechenden Entwicklungsteams an der Ermittlung der Ursache und der Vorbereitung des ersten Wiederherstellungsplans.

In der nächsten Phase identifiziert das Microsoft 365 Security Response-Team gegebenenfalls die kunden, die von dem Sicherheitsvorfall betroffen sind. Der Wirkungsbereich kann je nach Region, Rechenzentrum, Dienst, Serverfarm, Server usw. einige Zeit dauern. Die Liste der betroffenen Kunden wird vom Serviceteam und dem Microsoft 365 CxP Communications-Team kompiliert, das dann den Benachrichtigungsprozess des Kunden im Rahmen vertraglicher Und Complianceverpflichtungen ab verarbeiten.

## <a name="related-articles"></a>Verwandte Artikel

- [Verwaltung von Sicherheitsvorfällen unter Microsoft 365](assurance-security-incident-management.md)
- [Vorbereitung der Sicherheitsvorfälle in Microsoft 365](assurance-sim-preparation.md)
- [Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen in Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 Security Incident Management post-incident activity](assurance-sim-post-incident-activity.md)
