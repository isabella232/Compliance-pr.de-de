---
title: Geschäftskontinuität und Notfallwiederherstellung von Rechenzentren
description: Erfahren Sie mehr über die Geschäftskontinuität und Notfallwiederherstellung von Microsoft-Rechenzentren.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 948e1f9e1b15b83817c072e63ffaae0b444445f8
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265104"
---
# <a name="datacenter-business-continuity-and-disaster-recovery"></a>Geschäftskontinuität und Notfallwiederherstellung von Rechenzentren

Katastrophen sind nicht vorhersehbar, aber die Rechenzentren und das Betriebspersonal von Microsoft bereiten sich auf Katastrophen vor, um die Kontinuität des Betriebs zu gewährleisten, falls unerwartete Ereignisse eintreten sollten. Eine robuste Architektur und aktuelle, getestete Kontinuitätspläne mindern potenzielle Schäden und fördern die schnelle Wiederherstellung des Rechenzentrumsbetriebs. Krisenmanagementpläne schaffen Klarheit über Rollen, Verantwortlichkeiten und Minderungsaktivitäten vor, während und nach einer Krise. Die in diesen Plänen festgelegten Rollen und Kontakte erleichtern in Krisensituationen eine wirksame Eskalation in der Befehlskette nach oben.

## <a name="business-resilience"></a>Widerstandsfähigkeit von Unternehmen

Im Rahmen des Geschäftskontinuitätsprogramms für Microsoft Cloud Operations and Innovation (CO+I) müssen Rechenzentren den fortgesetzten Betrieb und die Reaktion auf Krisenereignisse testen. Jedes von Microsoft verwaltete Rechenzentrum verfügt über einen eigenen Geschäftskontinuitätsplan, der mithilfe des wichtigsten Fachwissens des CO+I Resilience Centers für Kompetenz- und Rechenzentrumsvorgänge erstellt wurde, um sicherzustellen, dass der standortspezifische Kontext in die Notfallbereitschaft einbezogen wird. Diese Pläne beschreiben Rollen, Zuständigkeiten, Verfahren zur Personalsicherheit, Benachrichtigungskriterien, Eskalationsschritte und Prüflisten für verschiedene Notfallszenarien.

Die Resilienzfunktion der CO+I-Organisation von Microsoft wird durch das Enterprise Business Continuity Management-Programm gesteuert und folgt den Enterprise Richtlinien und Standards. Die Leistung des Programms wird in regelmäßigen Abständen vom Business Continuity Council, der Abteilungsleitung und schließlich dem Geschäftsleitungsteam von Microsoft überprüft.

## <a name="crisis-management-and-pandemic-response"></a>Krisenmanagement und Pandemiebewältigung

Das Krisenmanagementprogramm ist angesichts der globalen Präsenz von Microsoft ein integraler Bestandteil der Reaktion auf wichtige Ereignisse. Microsofts Krisenmanagementplan für Rechenzentren basiert auf den branchenweit bewährten Methoden und enthält die kritischen Komponenten, die für einen taktischen Ansatz bei der Reaktion auf wichtige Ereignisse erforderlich sind. Darüber hinaus hat das CO+I Resilienzcenter für Kompetenz entwickelt und verwaltet weiterhin einen Pandemie- und Ausfallplan, der verwendet wird, um auf bedingte Beschwerden zu reagieren, die sich auf den Betrieb auswirken können. Im Rahmen unserer Pandemiereaktion bietet das Resilienzunterstützungsteam kritische und zeitnahe informationen zu lokalen Intelligenzen für die Microsoft-Führung in Redmond, um eine umfassende Strategie zur Risikominderung zu ermöglichen.

Microsoft hat ein organisationsweites Enterprise Business Continuity Management (EBCM)-Framework eingerichtet, das als Richtlinie für die Entwicklung des Geschäftskontinuitätsprogramms im gesamten Unternehmen dient. Das Programm umfasst Geschäftskontinuitätsrichtlinie, Implementierungsrichtlinien, Business Impact Analysis (BIA), Risikobewertung, Abhängigkeitsanalyse und Verfahren zur Überwachung und Verbesserung des Programms. Enterprise Resilienz Office verwaltet die Governance- und Leistungsberichte in Microsoft. Das CO+I-Resilienzprogramm wird über das CO+I Resilience Center of Kompetenz koordiniert, um sicherzustellen, dass das Programm einer kohärenten langfristigen Vision und Mission entspricht und mit Unternehmensprogrammstandards, -methoden, -richtlinien und -metriken konsistent ist. Das CO+I Resilience Center of Kompetenz hat eine Reihe von Standards eingerichtet, die der CO+I-Organisation zusätzliche Governance bieten sollen.

Die CO+I-Technologieresilienzpläne (TRPs) sind für verschiedene Engineering-Gruppen innerhalb von CO+I für die Wiederherstellung von Vorfällen oder Notfallen mit hohem Schweregrad vorgesehen, um sicherzustellen, dass unsere kritische Technologie verfügbar bleibt.

Der Business Resilience Plan (BRP) und TRP umfassen den Umfang und die anwendbaren Abhängigkeiten für die Dienste, Wiederherstellungsverfahren und die Kommunikation mit dem Incident Management-Team. BRP und TRP werden mindestens einmal jährlich von dedizierten Planbesitzern überprüft und genehmigt und allen anwendbaren Benutzern zur Verfügung gestellt. Die Pläne werden gemäß dem definierten Testzeitplan als Teil der geltenden Standards getestet.

## <a name="resiliency-program"></a>Resilienzprogramm

Microsoft hat das BRP definiert, das als Leitfaden zum Reagieren, Wiederherstellen und Fortsetzen von Vorgängen während eines schwerwiegenden nachteiligen Ereignisses dient. Das BRP deckt die wichtigsten Mitarbeiter, Ressourcen, Dienste und Aktionen ab, die erforderlich sind, um kritische Geschäftsprozesse und -vorgänge fortzusetzen. Die Entwicklung des BRP basiert auf den empfohlenen Richtlinien der Microsoft-Enterprise Resilienz Office.

Für diesen Plan gelten die kritischen Geschäftsprozesse von Microsoft, die nach Bedarf innerhalb von 24 Stunden oder weniger definiert sind. Diese Prozesse werden während eines BIA bestimmt, in dem Microsoft potenzielle betriebliche und finanzielle Auswirkungen geschätzt hat, wenn sie keinen Prozess ausführen konnten, und das Ziel für die Wiederherstellungszeit (Recovery Time Objective, RTO) und den Wiederherstellungspunkt (Recovery Point Objective, RPO) ermittelt. Im Anschluss an die BIA wird eine nicht technische Abhängigkeitsanalyse durchgeführt, um die spezifischen Personen, Anwendungen, wichtigen Datensätze und Benutzeranforderungen zu ermitteln, die zur Durchführung des Prozesses erforderlich sind.

Microsoft testet das BRP in regelmäßigen Abständen, um seine Effektivität, Benutzerfreundlichkeit und Bereiche zu bewerten, in denen Risiken beseitigt oder abgemildert werden können. Falls zutreffend, sind Dritte an dem Test beteiligt, wenn ihnen Abhängigkeiten zugeordnet sind. Die Ergebnisse der Tests werden dokumentiert, validiert und vom entsprechenden Personal genehmigt. Diese Informationen werden verwendet, um Arbeitsaufgaben zu erstellen und zu priorisieren.

## <a name="datacenter-resilience-program"></a>Datencenter-Resilienzprogramm

Im Rahmen des Rechenzentrums-Resilienzprogramms entwickelt das CO+I Resilience Center of Kompetenzteam die Methoden, Richtlinien und Metriken, die die Anforderungen an die Informationssicherheit erfüllen, die für die Geschäftskontinuität der Organisation erforderlich sind. Das Team entwickelt TRPs für den fortgesetzten Betrieb kritischer Prozesse und erforderlicher Ressourcen, wenn Unterbrechungen auftreten.
