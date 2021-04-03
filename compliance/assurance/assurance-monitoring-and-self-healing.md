---
title: Datenüberwachung und Selbstheilung in Microsoft 365
description: In diesem Artikel erfahren Sie mehr über die Überwachungs- und Selbstheilungsfunktionen von Microsoft 365.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: baf73746fff5e4866c36975e082c84017e0b3083
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496944"
---
# <a name="data-monitoring-and-self-healing-in-microsoft-365"></a>Datenüberwachung und Selbstheilung in Microsoft 365

Angesichts des Umfangs von Microsoft 365 wäre es unmöglich, Kundendaten ausfallsicher und vor Schadsoftware zu schützen, ohne eine umfassende, intelligente Warnung und eine schnelle und zuverlässige Selbstheilung. Die Überwachung einer Reihe von Diensten im Umfang von Microsoft 365 ist sehr schwierig. Es mussten neue Denkweisen und Methoden eingeführt werden, und es mussten ganz neue Technologiesätze erstellt werden, um den Dienst in einer verbundenen globalen Umgebung zu betreiben und zu verwalten. Wir haben uns vom herkömmlichen Überwachungsansatz der Datensammlung und -filterung entfernt, um Warnungen zu einem Ansatz zu erstellen, der auf der Datenanalyse basiert. Signale zu empfangen und Vertrauen in diese Daten zu schaffen und anschließend Automatisierung zu verwenden, um das Problem wiederherzustellen oder zu beheben. Dieser Ansatz hilft, Menschen aus der Wiederherstellungsgleichung zu nehmen, was wiederum Vorgänge weniger kostspielig, schneller und weniger fehleranfällig macht. 

Grundlegend für die Microsoft 365-Überwachung ist eine Sammlung von Technologien, die unsere Data Insights Engine umfassen, die auf der Azure-, SQL Azure- und [Open-Source-Streamingdatenbanktechnologie baut.](https://cassandra.apache.org/) Sie dient zum Sammeln und Aggregieren von Daten und zum Erreichen von Schlussfolgerungen. Derzeit werden mehr als 500 Millionen Ereignisse pro Stunde von mehr als 100.000 Servern (ca. 15 TB pro Tag) verarbeitet, die über Dutzende von Rechenzentren in vielen Regionen verteilt sind, und diese Anzahl wächst. 

Microsoft 365 verwendet *die externe* Überwachung, bei der synthetische Transaktionen erstellt werden, um alles Wichtige zu testen. In Exchange Online testet jedes Szenario beispielsweise jede Datenbank weltweit alle fünf Minuten auf verteilte Weise und bietet nahezu kontinuierliche Abdeckung aller im System vorhandenen Daten. An mehreren Standorten werden 250 Millionen Testtransaktionen pro Tag ausgeführt, um eine stabile Basislinie oder einen Takt für den Dienst zu erstellen. 

Microsoft 365 verwendet auch das Konzept *"Red Alert",* das alle Überwachungssignale von allen Computern in unseren Rechenzentren auf etwas verkleinert, das von einem Menschen verwaltbar ist. Das Konzept ist ganz einfach: Wenn etwas über mehrere Signale geschieht, muss etwas passieren. Es geht nicht darum, Vertrauen in ein Signal zu schaffen, sondern darum, für jedes Signal eine angemessene Genauigkeit zu haben, damit Sie eine höhere Genauigkeit erhalten. Dieses Überwachungssystem ist so leistungsfähig, dass wir nicht über 24 x 7 Mitarbeiter verfügen, die unsere Monitore beobachten. Alles, was wir haben, ist der Maschinenpark, der aufwacht, wenn ein Problem erkannt wird. In diesem Fall wird das entsprechende Anrufpersonal oder häufiger, wie dies der Fall ist, weitergeleitet und das Problem gelöst. Sobald wir damit beginnen, Signale zu sammeln und rote Warnungen zu erstellen, können wir mit der Dreieckung über alle unsere Dienstpartitionen beginnen. 

Basierend auf der Kombination der Fehlerwarnung und den roten Warnungen gibt diese Warnung genau an, welche Komponenten ein Problem haben könnten, und dass das System versuchen wird, das Problem durch einen Neustart eines Postfachservers allein zu beheben. 

Zusätzlich zu Funktionen zur Selbstheilung, z. B. die Wiederherstellung einzelner Seiten, umfasst Exchange Online mehrere Features, die einen Ansatz zur Überwachung und Selbstheilung verwenden, die sich auf die Erhaltung der Endbenutzererfahrung konzentrieren. Zu diesen Features gehören *die verwaltete Verfügbarkeit*, die integrierte Überwachungs- und Wiederherstellungsaktionen bietet, und AutoReseed, mit dem die Datenbankredundanz nach einem Datenträgerfehler automatisch wiederhergestellt wird. 

## <a name="managed-availability"></a>Verwaltete Verfügbarkeit 

Die verwaltete Verfügbarkeit bietet eine systemeigene Lösung zur Integritätsprüfung und Wiederherstellung, die die Benutzererfahrung durch wiederherstellungsorientierte Aktionen überwacht und schützt. Verwaltete Verfügbarkeit ist die Integration von integrierten Überwachungs- und Wiederherstellungsaktionen in die Exchange-Hochverfügbarkeitsplattform. Sie ist dafür vorgesehen, vom System erkannte Probleme sofort zu ermitteln und zu beheben. Im Gegensatz zu früheren externen Überwachungslösungen und -techniken für Exchange versucht die verwaltete Verfügbarkeit nicht, die eigentliche Ursache eines Problems zu ermitteln oder zu kommunizieren. Stattdessen konzentriert er sich auf Wiederherstellungsaspekte, die drei wichtige Bereiche der Endbenutzererfahrung berücksichtigen:

- **Verfügbarkeit** – Können Benutzer auf den Dienst zugreifen? 
- **Latenz –** Wie sieht die Benutzererfahrung aus? 
- **Fehler** – Sind Benutzer in der Lage, das zu erreichen, was sie möchten? 

Die verwaltete Verfügbarkeit ist ein internes Feature, das auf jedem Microsoft 365-Server ausgeführt wird, auf dem Exchange Online ausgeführt wird. Dabei werden in jeder Sekunde Hunderte von Integritätsmetriken abgerufen. Wenn festgestellt wird, dass etwas falsch ist, wird es meist automatisch behoben. Es gibt jedoch immer Probleme, die die verwaltete Verfügbarkeit nicht allein beheben kann. In diesen Fällen wird das Problem durch die verwaltete Verfügbarkeit mittels Ereignisprotokollierung an ein Microsoft 365-Supportteam eskaliert.

## <a name="autoreseed"></a>AutoReseed

Exchange Online-Server werden in einer Konfiguration bereitgestellt, die mehrere Datenbanken und ihre Protokolldatenströme auf demselben Nicht-RAID-Datenträger speichert. Diese Konfiguration wird häufig nur als eine Reihe von *Datenträgern* (JBOD) bezeichnet, da keine Speicherredundanzmechanismen wie RAID zum Duplizieren der Daten auf dem Datenträger verwendet werden. Wenn ein Datenträger in einer JBOD-Umgebung ausfällt, gehen die Daten auf diesem Datenträger verloren. 

Aufgrund der Größe von Exchange Online und der Tatsache, dass es sich dabei um Millionen von Festplattenlaufwerken handelt, sind Datenträgerfehler in Exchange Online ein reguläres Vorkommen. Tatsächlich fallen täglich mehr als 100 Fehler aus. Wenn ein Datenträger in einer lokalen Unternehmensbereitstellung ausfällt, muss ein Administrator den ausgefallenen Datenträger manuell ersetzen und die betroffenen Daten wiederherstellen. In einer Cloudbereitstellung, die die Größe von Microsoft 365 hat, ist es weder praktikabel noch wirtschaftlich praktikabel, wenn Operatoren (Cloudadministratoren) Datenträger manuell ersetzen. 

Automatic Reseed oder *AutoReseed* ist ein Feature, das die normalerweise operatorgesteuerte Aktion als Reaktion auf einen Datenträgerfehler, ein Datenbankbeschädigungsereignis oder ein anderes Problem ersetzt, das ein erneutes Senden einer Datenbankkopie erfordert. AutoReseed wurde entwickelt, um die Datenbankredundanz nach einem Datenträgerfehler mithilfe von Ersatzdatenträgern, die auf dem System bereitgestellt wurden, automatisch wiederherzustellen. Wenn ein Datenträger ausfällt, werden die auf diesem Datenträger gespeicherten Datenbankkopien automatisch auf einen vorkonfigurierten Ersatzdatenträger auf dem Server erneut gesendet, wodurch redundanz wiederhergestellt wird. 