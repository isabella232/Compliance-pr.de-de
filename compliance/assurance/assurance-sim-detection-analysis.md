---
title: 'Microsoft Security Incident Management: Erkennung und Analyse'
description: Dieser Artikel bietet eine Übersicht über den Prozess der Erkennung und Analyse von Sicherheitsvorfällen in Microsoft-Onlinediensten.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: ba9d4c5f3e2781613ef3946e1089deff6e6266f7
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481687"
---
# <a name="microsoft-security-incident-management-detection-and-analysis"></a>Microsoft Security Incident Management: Erkennung und Analyse

Um bösartige Aktivitäten zu erkennen, protokolliert jeder Microsoft-Onlinedienst Sicherheitsereignisse und andere Daten zentral und führt verschiedene Analysetechniken aus, um anomale oder verdächtige Aktivitäten zu finden. Protokolldateien werden von Microsoft-Onlinedienstservern und Infrastrukturgeräten gesammelt und in zentralen und konsolidierten Datenbanken gespeichert.

Microsoft verfolgt einen risikobasierten Ansatz, um böswillige Aktivitäten zu erkennen. Wir verwenden Vorfalldaten und Bedrohungserkennung, um unsere Erkennungen zu definieren und zu priorisieren.

Die Verwendung eines Teams aus erfahrenen, erfahrenen und erfahrenen Mitarbeitern ist eine der wichtigsten Säulen für den Erfolg in der Erkennungs- und Analysephase. Microsoft setzt mehrere Serviceteams ein, die Mitarbeiter mit Kompetenzen für alle Komponenten innerhalb des Stapels umfassen, einschließlich Netzwerk, Router, Firewalls, Lastenausgleichsmodule, Betriebssysteme und Anwendungen.

Die Sicherheitserkennungsmechanismen in Microsoft-Onlinediensten umfassen auch Benachrichtigungen und Warnungen, die von verschiedenen Quellen initiiert werden. Microsoft Online Services Security Response Teams sind die wichtigsten Orchestratoren des Eskalationsprozesses für Sicherheitsvorfälle. Diese Teams empfangen alle Eskalationen und sind für die Analyse und Bestätigung der Gültigkeit des Sicherheitsvorfalls verantwortlich.

![Workflow für die Verwaltung von Sicherheitsvorfällen](../media/assurance-sim-workflow.png)

Eine der wichtigsten Säulen der Erkennung ist die Benachrichtigung:

- Jedes Serviceteam ist dafür verantwortlich, alle Aktionen oder Ereignisse innerhalb des Diensts basierend auf den Anforderungen des Sicherheitsteams des Onlinediensts zu protokollieren. Alle von den verschiedenen Serviceteams erstellten Protokolle werden von einer SIEM-Lösung (Security Information and Event Management) mit vordefinierten Sicherheits- und Erkennungsregeln verarbeitet. Diese Regeln werden basierend auf Empfehlungen des Sicherheitsteams, basierend auf Informationen aus vorherigen Sicherheitsvorfällen, weiterentwickelt, um festzustellen, ob verdächtige oder böswillige Aktivitäten vorhanden sind.
- Wenn ein Kunde feststellt, dass ein Sicherheitsvorfall ausgeführt wird, kann er einen Supportfall bei Microsoft öffnen, der dem Microsoft-Kommunikationsteam zugewiesen und in eine Eskalation für alle entsprechenden Teams umgewandelt wird.

Azure, Dynamics 365 und Microsoft 365 Serviceteams nutzen auch die in der Trendanalyse gewonnenen Informationen durch Sicherheitsüberwachung und -protokollierung, um Anomalien in Microsoft-Onlinedienst-Informationssystemen zu erkennen, die auf einen Angriff oder einen Sicherheitsvorfall hinweisen können. Microsoft-Onlinedienstsysteme fassen die Ausgabe aus diesen Protokollen in der Produktionsumgebung in zentralisierte Protokollierungsserver zusammen. Von diesen zentralisierten Protokollierungsservern aus werden Protokolle untersucht, um Trends in der gesamten Produktionsumgebung zu erkennen. Daten, die auf den zentralisierten Servern aggregiert werden, werden sicher in einen Protokollierungsdienst übertragen, um erweiterte Abfragen zu erstellen, Dashboards zu erstellen und anomale und schädliche Aktivitäten zu erkennen. Der Dienst verwendet auch maschinelles Lernen, um Anomalien mit protokollbasierter Ausgabe zu erkennen.

In der Eskalationsphase und je nach Art des Sicherheitsvorfalls können Sicherheitsteams einen oder mehrere Fachexperten aus verschiedenen Teams bei Microsoft einbeziehen:

- Team für Sicherheit und Compliance für Onlinedienste
- Microsoft Threat Intelligence Center (MSTIC)
- Microsoft Security Response Center (MSRC)
- Unternehmens-, Außen- und Rechtsfragen (CELA)
- Azure Security
- Microsoft 365 Engineering und andere.

Bevor eine Eskalation zu einem Sicherheitsreaktionsteam erfolgt, ist das Serviceteam für die Bestimmung und Festlegung des Schweregrads des Sicherheitsvorfalls basierend auf definierten Kriterien verantwortlich, z. B.:

- Datenschutz
- Auswirkung
- Umfang
- Anzahl der betroffenen Mandanten
- Region
- Dienst
- Details des Vorfalls
- Spezifische Branchen- oder Marktbestimmungen für Kunden.

Die Priorisierung von Vorfällen wird anhand verschiedener Faktoren bestimmt, einschließlich, aber nicht beschränkt auf die funktionalen Auswirkungen des Vorfalls, die informationsbezogene Auswirkung des Vorfalls und die Wiederherstellbarkeit des Vorfalls.

Nachdem eine Eskalation zu einem Sicherheitsvorfall empfangen wurde, organisiert das Sicherheitsteam ein virtuelles Team (v-Team), das aus Mitgliedern des Microsoft Online Service Security Response-Teams, der Serviceteams und des Teams für die Vorfallkommunikation besteht. Das v-Team muss dann die Dringlichkeit des Sicherheitsvorfalls bestätigen und falsch positive Ergebnisse ausschließen. Die Genauigkeit der Informationen, die von den in der Vorbereitungsphase ermittelten Indikatoren bereitgestellt werden, ist von entscheidender Bedeutung. Durch die Analyse dieser Informationen nach Kategorie des Vektorangriffs kann das v-Team ermitteln, ob der Sicherheitsvorfall ein berechtigtes Problem ist.

Zu Beginn der Untersuchung zeichnet das Team für die Reaktion auf Sicherheitsvorfälle alle Informationen zu dem Vorfall gemäß unseren Fallverwaltungsrichtlinien auf. Im weiteren Verlauf des Falls verfolgen wir fortlaufende Aktionen und folgen den Standards für die Beweisverarbeitung zum Sammeln, Aufbewahren und Sichern dieser Daten während des gesamten Vorfalllebenszyklus.

Beispiele für diese Aktionen sind:

- Eine Zusammenfassung, die eine kurze Beschreibung des Vorfalls und seiner potenziellen Auswirkungen darstellt.
- Schweregrad und Priorität des Vorfalls, die durch die Bewertung der potenziellen Auswirkungen abgeleitet werden
- Eine Liste aller identifizierten Indikatoren, die zur Erkennung des Vorfalls geführt haben
- Eine Liste aller ähnlichen Vorfälle
- Eine Liste aller Aktionen, die vom v-Team ausgeführt werden
- Alle gesammelten Nachweise, die auch für die nachträgliche Analyse und zukünftige forensische Untersuchungen aufbewahrt werden
- Empfohlene nächste Schritte

Nach der Bestätigung von Sicherheitsvorfällen besteht das Hauptziel des Sicherheitsreaktionsteams und des entsprechenden Serviceteams darin, den Angriff einzudämmen, die dienste unter Angriff zu schützen und eine größere globale Auswirkung zu vermeiden. Gleichzeitig arbeiten die entsprechenden Entwicklungsteams daran, die Ursache zu ermitteln und den ersten Wiederherstellungsplan vorzubereiten.

In der nächsten Phase identifiziert das Sicherheitsteam die Kunden, die von dem Sicherheitsvorfall betroffen sind, sofern vorhanden. Der Wirkungsbereich kann einige Zeit in Anspruch nehmen, um basierend auf Region, Rechenzentrum, Dienst, Serverfarm, Server usw. zu bestimmen. Die Liste der betroffenen Kunden wird vom Serviceteam und dem entsprechenden Microsoft-Kommunikationsteam zusammengestellt, das dann den Benachrichtigungsprozess des Kunden im Rahmen vertraglicher und Compliance-Verpflichtungen verarbeitet.

## <a name="related-articles"></a>Verwandte Artikel

- [Microsoft-Sicherheitsvorfallverwaltung](assurance-security-incident-management.md)
- [Microsoft Security Incident Management: Vorbereitung](assurance-sim-preparation.md)
- [Microsoft Security Incident Management: Eindämmung, Beseitigung und Wiederherstellung](assurance-sim-containment-eradication-recovery.md)
- [Microsoft-Sicherheitsvorfallverwaltung: Aktivitäten nach dem Vorfall](assurance-sim-post-incident-activity.md)
- [So protokollieren Sie ein Supportticket für Sicherheitsereignisse](/azure/security/fundamentals/event-support-ticket)
- [Azure und Dynamics 365-Benachrichtigung bei Datenschutzverletzung im Rahmen der DSGVO](/compliance/regulatory/gdpr-breach-azure-dynamics)
