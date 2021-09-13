---
title: 'Microsoft-Sicherheitsvorfallverwaltung: Aktivitäten nach dem Vorfall'
description: Dieser Artikel bietet eine Übersicht über den Prozess der Aktivitäten nach dem Vorfall bei der Verwaltung von Sicherheitsvorfällen in Microsoft-Onlinediensten.
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
ms.openlocfilehash: 820c912dc55d5cc98cedc38676b5039591cf5baa
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159573"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a>Microsoft-Sicherheitsvorfallverwaltung: Aktivitäten nach dem Vorfall

## <a name="postmortem"></a>Postmortem

Einige Sicherheitsvorfälle, insbesondere solche, die auswirkungen auf den Kunden haben oder zu einer Datenschutzverletzung führen, unterliegen einem vollständigen Vorfallstatus. Das Sicherheitsteam führt ein detailliertes Postmortem mit allen an der Reaktion auf Sicherheitsvorfälle beteiligten Parteien durch:

- Dokumentieren Sie die Abfolge der Ereignisse, die den Vorfall verursacht haben.
- Erstellen Sie eine technische Zusammenfassung des Vorfalls, die durch die Nachweise unterstützt wird, die die an der Verletzung beteiligten Akteure (sofern bekannt) umfassen. Diese Zusammenfassung enthält die Ausführung der Antwort und andere Wichtigeinkäufe.
- Identifizieren Von technischen Fehlern, Verfahrensfehlern, manuellen Fehlern, Prozessfehlern und Kommunikationsfehlern und/oder zuvor unbekannten Angriffsvektoren, die während der Reaktion auf Sicherheitsvorfälle identifiziert wurden.

Das Postmortem wirkt sich direkt auf die Verbesserung des Microsoft-Onlinediensts, die betrieblichen Prozesse und die Dokumentation aus, indem neue Prioritäten im Entwicklungszyklus der Microsoft-Onlinedienste festgelegt werden.

## <a name="documentation"></a>Dokumentation

Alle wichtigen technischen Ergebnisse im postirtischen Prozess werden in einem Bericht erfasst, in dem Investitionen in Dienste oder Korrekturen in Form von Fehlern oder Entwicklungsänderungsanforderungen vorgenommen werden. Diese Ergebnisse werden mit den entsprechenden Entwicklungsteams nachverfolgt. Bei Prozessfehlern und organisationsübergreifenden Problemen werden Probleme in der Datenbank des Sicherheitsreaktionsteams dokumentiert und mit den entsprechenden Gruppen verfolgt, um sie zu beheben.

## <a name="process-improvement"></a>Prozessverbesserung

Die Reaktion auf einen Sicherheitsvorfall in Microsoft-Onlinediensten umfasst die Koordination mit mehreren Gruppen, die über verschiedene Organisationen innerhalb von Microsoft verteilt sind, und möglicherweise sogar mit geeigneten externen Organisationen wie Strafverfolgungsbehörden. Wir wissen, dass es wichtig ist, unsere Antworten nach jedem Sicherheitsvorfall sowohl auf Ausreichendes als auch auf Vollständigkeit zu bewerten. Bei identifizierten Verbesserungen oder Änderungen wertet das Sicherheitsteam die Vorschläge in Abstimmung mit den entsprechenden Teams und Beteiligten aus und integriert sie gegebenenfalls in standardbetriebsverfahren. Alle erforderlichen Änderungen, Fehler oder Dienstverbesserungen, die während der Reaktion auf Sicherheitsvorfälle oder nachträgliche Aktivitäten identifiziert wurden, werden in einer internen Microsoft Engineering-Datenbank protokolliert und nachverfolgt. Alle potenziellen Fehler oder Features werden dem entsprechenden Besitzer zugewiesen. Das Microsoft Security Response-Team überprüft alle Einträge, bis das Problem behoben ist.

## <a name="related-articles"></a>Verwandte Artikel

- [Microsoft-Sicherheitsvorfallverwaltung](assurance-security-incident-management.md)
- [Microsoft Security Incident Management: Vorbereitung](assurance-sim-preparation.md)
- [Microsoft Security Incident Management: Erkennung und Analyse](assurance-sim-detection-analysis.md)
- [Microsoft Security Incident Management: Eindämmung, Beseitigung und Wiederherstellung](assurance-sim-containment-eradication-recovery.md)
- [So protokollieren Sie ein Supportticket für Sicherheitsereignisse](/azure/security/fundamentals/event-support-ticket)
- [Azure und Dynamics 365-Benachrichtigung bei Datenschutzverletzung im Rahmen der DSGVO](/compliance/regulatory/gdpr-breach-azure-dynamics)
