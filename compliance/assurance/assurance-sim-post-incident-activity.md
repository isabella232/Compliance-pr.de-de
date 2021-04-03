---
title: 'Microsoft 365 Security Incident Management: Aktivitäten nach dem Vorfall'
description: Dieser Artikel bietet eine Übersicht über den Prozess der Sicherheitsvorfallverwaltung nach einem Vorfall in Microsoft 365.
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
ms.openlocfilehash: 4ebd31c16f8abb3eddd6ed924a045d88597aba40
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496714"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a>Microsoft 365 Security Incident Management: Aktivitäten nach dem Vorfall

## <a name="postmortem"></a>Postmortem

Einige Sicherheitsvorfälle, insbesondere solche Vorfälle, die sich auf Kunden auswirken oder zu einer Datenschutzverletzung führen, unterliegen einem vollständigen Vorfall nach dem Vorfall. Das Microsoft 365 Security Response-Team führt ein detailliertes Postmortem mit allen an der Reaktion auf Sicherheitsvorfälle beteiligten Parteien durch:

- Dokumentieren der Reihenfolge der Ereignisse, die den Vorfall verursacht haben
- Erstellen Sie eine technische Zusammenfassung des Vorfalls, die von den Nachweisen unterstützt wird, die die an der Verletzung beteiligten Akteure (sofern bekannt) enthalten. Diese Zusammenfassung enthält die Ausführung der Antwort und andere wichtige Informationen.
- Identifizieren Sie technische Fehler, Verfahrensfehler, manuelle Fehler, Prozessfehler und Kommunikationsfehler und/oder zuvor unbekannte Angriffsvektoren, die während der Reaktion auf Sicherheitsvorfälle identifiziert wurden.

Das Postmortem hat direkten Einfluss auf die Verbesserung der Microsoft 365-Dienste, die operativen Prozesse und die Dokumentation, indem neue Prioritäten im Microsoft 365-Entwicklungszyklus festgelegt werden.

## <a name="documentation"></a>Dokumentation

Alle wichtigen technischen Erkenntnisse im postmortem-Prozess werden in einem Bericht und in Serviceinvestitionen oder -korrekturen in Form von Fehlern oder Entwicklungsänderungsanforderungen erfasst. Diese Erkenntnisse werden mit den entsprechenden Technischen Teams weiterverarbeiten. Bei Prozessfehlern und organisationsübergreifenden Problemen werden Probleme in der Datenbank des Microsoft 365 Security Response-Teams dokumentiert und mit den entsprechenden Gruppen zur Problembesprechung nachgegangen.

## <a name="process-improvement"></a>Prozessverbesserung

Die Reaktion auf einen Sicherheitsvorfall in Microsoft 365 umfasst die Koordination mit mehreren Gruppen, die über verschiedene Organisationen in Microsoft verteilt sind, und potenziell sogar geeignete externe Organisationen wie die Strafverfolgung. Wir wissen, dass es wichtig ist, unsere Antworten nach jedem Sicherheitsvorfall sowohl auf Dieligkeit als auch auf Vollständigkeit auszuwerten. Für identifizierte Verbesserungen oder Änderungen wertet das Microsoft 365 Security Response-Team die Vorschläge in Abstimmung mit den entsprechenden Teams und Beteiligten aus und integriert sie gegebenenfalls in standardbetriebsverfahren. Alle erforderlichen Änderungen, Fehler oder Dienstverbesserungen, die während der Reaktion auf Sicherheitsvorfälle oder postmortem Aktivitäten identifiziert wurden, werden protokolliert und in einer internen Microsoft 365-Engineeringdatenbank nachverfolgt. Alle potenziellen Fehler oder Features werden dem entsprechenden Besitzer zugewiesen. Das Microsoft 365 Security Response-Team überprüft alle Einträge, bis das Problem behoben ist.

## <a name="related-articles"></a>Verwandte Artikel

- [Verwaltung von Sicherheitsvorfällen unter Microsoft 365](assurance-security-incident-management.md)
- [Vorbereitung der Sicherheitsvorfälle in Microsoft 365](assurance-sim-preparation.md)
- [Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365](assurance-sim-detection-analysis.md)
- [Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen in Microsoft 365](assurance-sim-containment-eradication-recovery.md)
