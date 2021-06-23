---
title: 'Microsoft 365 Security-Vorfallverwaltung: Erkennung und Analyse'
description: Dieser Artikel bietet eine Übersicht über den Prozess der Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365.
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
ms.openlocfilehash: 3eb42b340ed6a137d0bec7b58d015009a1b20621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087577"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a>Microsoft 365 Security-Vorfallverwaltung: Erkennung und Analyse

Um böswillige Aktivitäten zu erkennen, protokolliert Microsoft 365 Sicherheitsereignisse und andere Daten zentral und führt verschiedene Analysetechniken aus, um anomale oder verdächtige Aktivitäten zu finden. Protokolldateien werden von Microsoft 365 Servern und Infrastrukturgeräten erfasst und in einer zentralen und konsolidierten Datenbank gespeichert.

Microsoft verfolgt einen risikobasierten Ansatz, um böswillige Aktivitäten zu erkennen. Wir verwenden Vorfalldaten und Bedrohungserkennung, um unsere Erkennungen zu definieren und zu priorisieren.

Die Verwendung eines Teams aus erfahrenen, erfahrenen und erfahrenen Mitarbeitern ist eine der wichtigsten Säulen für den Erfolg in der Erkennungs- und Analysephase. Microsoft 365 mehrere Serviceteams beschäftigt, und diese Teams umfassen Mitarbeiter mit Kompetenzen für alle Komponenten innerhalb des Stapels, einschließlich Netzwerk, Router, Firewalls, Lastenausgleichsmodule, Betriebssysteme und Anwendungen.

Die Sicherheitserkennungsmechanismen in Microsoft 365 auch Benachrichtigungen und Warnungen enthalten, die von verschiedenen Quellen initiiert werden. Das Microsoft 365 Security Response-Team ist der wichtigste Orchestrator des Eskalationsprozesses für Sicherheitsvorfälle. Dieses Team empfängt alle Eskalationen und ist für die Analyse und Bestätigung der Gültigkeit des Sicherheitsvorfalls verantwortlich.

![Workflow für die Verwaltung von Sicherheitsvorfällen](../media/assurance-sim-workflow.png)

Eine der wichtigsten Säulen der Erkennung ist die Benachrichtigung:

- Jedes Serviceteam ist dafür verantwortlich, alle Aktionen oder Ereignisse innerhalb des Diensts basierend auf den Anforderungen des Microsoft 365 Security-Teams zu protokollieren. Alle von den verschiedenen Serviceteams erstellten Protokolle werden von einer SIEM-Lösung (Security Information and Event Management) mit vordefinierten Sicherheits- und Erkennungsregeln verarbeitet. Diese Regeln entwickeln sich basierend auf der Empfehlung des Microsoft 365 Sicherheitsteams anhand von Informationen aus vorherigen Sicherheitsvorfällen weiter, um festzustellen, ob verdächtige oder böswillige Aktivitäten vorliegen.
- Wenn ein Kunde feststellt, dass ein Sicherheitsvorfall ausgeführt wird, kann er einen Supportfall bei Microsoft öffnen, der dem Kommunikationsteam Microsoft 365 Customer Experience (CxP) zugewiesen ist und in eine Eskalation für alle entsprechenden Teams umgewandelt wird.

Microsoft 365 Serviceteams nutzen auch die in der Trendanalyse gewonnenen Informationen durch Sicherheitsüberwachung und Protokollierung, um Anomalien in Microsoft 365 Informationssystemen zu erkennen, die auf einen Angriff oder einen Sicherheitsvorfall hinweisen können. Microsoft 365 Server die Ausgabe aus diesen Protokollen in der Produktionsumgebung auf einem zentralen Protokollierungsserver aggregieren. Auf diesem zentralen Protokollierungsserver werden Protokolle untersucht, um Trends in der gesamten Produktionsumgebung zu erkennen. Daten, die auf dem zentralen Server aggregiert werden, werden sicher in einen Protokollierungsdienst übertragen, um erweiterte Abfragen, Dashboarderstellung und Erkennung von anomales und bösartigen Aktivitäten zu ermöglichen. Der Dienst verwendet auch maschinelles Lernen, um Anomalien mit protokollbasierter Ausgabe zu erkennen.

In der Eskalationsphase und je nach Art des Sicherheitsvorfalls kann das Microsoft 365 Security Response-Team einen oder mehrere Fachexperten aus verschiedenen Teams bei Microsoft einbeziehen:

- Team für Sicherheit und Compliance für Onlinedienste
- Microsoft Threat Intelligence Center (MSTIC)
- Microsoft Security Response Center (MSRC)
- Unternehmens-, Außen- und Rechtsfragen (CELA)
- Azure Security
- Microsoft 365 Engineering und andere.

Bevor eine Eskalation zum Microsoft 365 Security Response-Team erfolgt, ist das Serviceteam für die Ermittlung und Festlegung des Schweregrads des Sicherheitsvorfalls basierend auf definierten Kriterien verantwortlich, z. B.:

- Datenschutz
- Auswirkung
- Bereich
- Anzahl der betroffenen Mandanten
- Region
- Dienst
- Details des Vorfalls
- Spezifische Branchen- oder Marktbestimmungen für Kunden.

Die Priorisierung von Vorfällen wird anhand verschiedener Faktoren bestimmt, einschließlich, aber nicht beschränkt auf die funktionalen Auswirkungen des Vorfalls, die informationsbezogene Auswirkung des Vorfalls und die Wiederherstellbarkeit des Vorfalls.

Nachdem das Microsoft 365 Sicherheitsteam eine Eskalation zu einem Sicherheitsvorfall erhalten hat, organisiert es ein virtuelles Team (v-Team), das aus Mitgliedern aus Microsoft 365 Security Response-Team, Serviceteams und dem Microsoft 365 Incident Communication-Team besteht. Der komplexere Teil der Aktivitäten dieses v-Teams besteht darin, den Sicherheitsvorfall zu bestätigen und falsch positive Ergebnisse zu vermeiden. Die Genauigkeit der Informationen, die von den in der Vorbereitungsphase ermittelten Indikatoren bereitgestellt werden, ist entscheidend. Durch die Analyse dieser Informationen nach Kategorie des Vektorangriffs kann das v-Team ermitteln, ob der Sicherheitsvorfall ein berechtigtes Problem ist.

Zu Beginn der Untersuchung zeichnet das Office Security Incident Response-Team alle Informationen zu dem Vorfall gemäß unseren Fallverwaltungsrichtlinien auf. Im weiteren Verlauf des Falls verfolgen wir fortlaufende Aktionen und folgen den Standards für die Beweisverarbeitung zum Sammeln, Aufbewahren und Sichern dieser Daten während des gesamten Vorfalllebenszyklus.

Beispiele für diese Aktionen sind:

- Eine Zusammenfassung, die eine kurze Beschreibung des Vorfalls und seiner potenziellen Auswirkungen darstellt.
- Schweregrad und Priorität des Vorfalls, die durch die Bewertung der potenziellen Auswirkungen abgeleitet werden
- Eine Liste aller identifizierten Indikatoren, die zur Erkennung des Vorfalls geführt haben
- Eine Liste aller ähnlichen Vorfälle
- Eine Liste aller Aktionen, die vom v-Team ausgeführt werden
- Alle gesammelten Nachweise, die auch für die nachträgliche Analyse und zukünftige forensische Untersuchungen aufbewahrt werden
- Empfohlene nächste Schritte

Nach der Bestätigung des Sicherheitsvorfalls besteht das Hauptziel des Microsoft 365 Security Response-Teams und des entsprechenden Serviceteams darin, den Angriff einzudämmen, die angegriffenen Dienste zu schützen und eine größere globale Auswirkung zu vermeiden. Gleichzeitig arbeiten die entsprechenden Entwicklungsteams daran, die Ursache zu ermitteln und den ersten Wiederherstellungsplan vorzubereiten.

In der nächsten Phase identifiziert das Microsoft 365 Security Response-Team die Kunden, die von dem Sicherheitsvorfall betroffen sind, sofern vorhanden. Der Wirkungsbereich kann einige Zeit in Anspruch nehmen, um basierend auf Region, Rechenzentrum, Dienst, Serverfarm, Server usw. zu bestimmen. Die Liste der betroffenen Kunden wird vom Serviceteam und dem Microsoft 365 CxP Communications-Team zusammengestellt, das dann den Benachrichtigungsprozess des Kunden im Rahmen vertraglicher und Compliance-Verpflichtungen verarbeitet.

## <a name="related-articles"></a>Verwandte Artikel

- [Microsoft 365 Security-Vorfallverwaltung](assurance-security-incident-management.md)
- [Vorbereitung des Microsoft 365 Sicherheitsvorfallmanagements](assurance-sim-preparation.md)
- [Microsoft 365 Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 Aktivitäten zur Verwaltung von Sicherheitsvorfällen nach einem Vorfall](assurance-sim-post-incident-activity.md)
