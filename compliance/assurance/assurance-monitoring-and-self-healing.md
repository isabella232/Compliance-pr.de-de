---
title: Datenüberwachung und Selbstkorrektur in Microsoft 365
description: In diesem Artikel erfahren Sie mehr über die Überwachungs- und Selbstkorrekturfunktionen von Microsoft 365.
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
ms.openlocfilehash: d55621d10284c427afedeb3d60807411841d41dda2e07c52b293a676448dbe73
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290623"
---
# <a name="data-monitoring-and-self-healing-in-microsoft-365"></a>Datenüberwachung und Selbstkorrektur in Microsoft 365

Angesichts des Umfangs der Microsoft 365 wäre es unmöglich, Kundendaten stabil und vor Schadsoftware zu schützen, ohne eine integrierte Überwachung, die umfassend und intelligent ist und schnell und zuverlässig ist. Die Überwachung einer Reihe von Diensten im Umfang von Microsoft 365 ist sehr schwierig. Es mussten neue Mentalitäten und Methoden eingeführt werden, und es mussten ganz neue Technologiegruppen erstellt werden, um den Dienst in einer verbundenen globalen Umgebung zu betreiben und zu verwalten. Wir haben uns vom herkömmlichen Überwachungsansatz der Datenerfassung und -filterung entfernt, um Warnungen zu erstellen, zu einem Ansatz, der auf der Datenanalyse basiert. Signale zu nehmen und Vertrauen in diese Daten zu schaffen und dann die Automatisierung zu verwenden, um das Problem wiederherzustellen oder zu beheben. Dieser Ansatz hilft Menschen aus der Wiederherstellungsgleichung herauszunehmen, was wiederum Vorgänge kostengünstiger, schneller und weniger fehleranfällig macht. 

Grundlegend für Microsoft 365 Überwachung ist eine Sammlung von Technologien, die unser Daten-Insights-Modul umfassen, das auf Azure, SQL Azure und [Open-Source-Streamingdatenbanktechnologie](https://cassandra.apache.org/)basiert. Es ist darauf ausgelegt, Daten zu sammeln und zu aggregieren und Schlussfolgerungen zu erzielen. Derzeit verarbeitet sie mehr als 500 Millionen Ereignisse pro Stunde von mehr als 100.000 Servern (ca. 15 TB pro Tag), die über Dutzende von Rechenzentren in vielen Regionen verteilt sind, und diese Anzahl wächst. 

Microsoft 365 verwendet *die Externe Überwachung,* bei der synthetische Transaktionen erstellt werden, um alles Wichtige zu testen. In Exchange Online testet jedes Szenario beispielsweise jede Datenbank weltweit alle fünf Minuten und bietet nahezu fortlaufende Abdeckung über alles, was im System vorhanden ist. Von mehreren Standorten aus werden 250 Millionen Testtransaktionen pro Tag ausgeführt, um eine stabile Basislinie oder einen stabilen Takt für den Dienst zu erstellen. 

Microsoft 365 verwendet auch das Konzept *"Rote Warnung",* das alle Überwachungssignale von allen Computern in unseren Rechenzentren auf etwas verkleinert, das von einem Menschen verwaltet werden kann. Das Konzept ist ganz einfach: Wenn etwas über mehrere Signale hinweg geschieht, muss etwas los sein. Es geht nicht darum, Vertrauen in ein Signal zu schaffen, es geht darum, für jedes Signal eine angemessene Genauigkeit zu haben, damit Sie eine höhere Genauigkeit erhalten. Dieses Überwachungssystem ist so leistungsfähig, dass wir keine 24 x 7-Mitarbeiter haben, die unsere Monitore überwachen. Wir haben nur die Maschinen, die aufwachen, wenn ein Problem erkannt wird. In diesem Fall wird das entsprechende Bereitschaftspersonal auf der Seite angezeigt, oder häufiger, wie dies der Fall ist, wird es einfach weitergehen und das Problem lösen. Sobald wir damit beginnen, Signale zu sammeln und rote Warnungen zu erstellen, können wir mit der Triangulierung über alle Dienstpartitionen hinweg beginnen. 

Basierend auf der Kombination aus der Fehlerwarnung und den roten Warnungen gibt diese Warnung genau an, welche Komponenten ein Problem haben könnten, und dass das System versucht, das Problem selbst zu beheben, indem ein Postfachserver neu gestartet wird. 

Zusätzlich zu den Funktionen zur Selbstkorrektur, z. B. die Wiederherstellung auf einer Seite, enthält Exchange Online mehrere Features, die einen Ansatz für die Überwachung und Selbstkorrektur verfolgen, bei dem der Schwerpunkt auf der Erhaltung der Endbenutzererfahrung liegt. Zu diesen Features gehören *die verwaltete Verfügbarkeit*, die integrierte Überwachungs- und Wiederherstellungsaktionen bereitstellt, und AutoReseed, das die Datenbankredundanz nach einem Datenträgerfehler automatisch wiederherstellt. 

## <a name="managed-availability"></a>Verwaltete Verfügbarkeit 

Die verwaltete Verfügbarkeit bietet eine systemeigene Lösung zur Integritätsprüfung und Wiederherstellung, die die Benutzererfahrung durch wiederherstellungsorientierte Aktionen überwacht und schützt. Verwaltete Verfügbarkeit ist die Integration integrierter Überwachungs- und Wiederherstellungsaktionen in die Exchange Hochverfügbarkeitsplattform. Sie ist dafür vorgesehen, vom System erkannte Probleme sofort zu ermitteln und zu beheben. Im Gegensatz zu früheren externen Überwachungslösungen und -techniken für Exchange versucht die verwaltete Verfügbarkeit nicht, die eigentliche Ursache eines Problems zu ermitteln oder zu kommunizieren. Stattdessen konzentriert er sich auf Wiederherstellungsaspekte, die sich auf drei wichtige Bereiche der Endbenutzererfahrung beziehen:

- **Verfügbarkeit** – Können Benutzer auf den Dienst zugreifen? 
- **Latenz** – Wie ist die Erfahrung für Benutzer? 
- **Fehler** – Sind Benutzer in der Lage, die gewünschten Aufgaben auszuführen? 

Verwaltete Verfügbarkeit ist ein internes Feature, das auf jedem Microsoft 365 Server ausgeführt wird, auf dem Exchange Online ausgeführt wird. Dabei werden in jeder Sekunde Hunderte von Integritätsmetriken abgerufen. Wenn festgestellt wird, dass etwas falsch ist, wird es meistens automatisch behoben. Es gibt jedoch immer Probleme, die die verwaltete Verfügbarkeit nicht allein beheben kann. In diesen Fällen eskaliert die verwaltete Verfügbarkeit das Problem mithilfe der Ereignisprotokollierung an ein Microsoft 365 Supportteam.

## <a name="autoreseed"></a>AutoReseed

Exchange Online Server werden in einer Konfiguration bereitgestellt, die mehrere Datenbanken und deren Protokolldatenströme auf demselben Nicht-RAID-Datenträger speichert. Diese Konfiguration wird häufig nur als *eine Gruppe von Datenträgern* (JBOD) bezeichnet, da keine Speicherredundanzmechanismen wie RAID verwendet werden, um die Daten auf dem Datenträger zu duplizieren. Wenn ein Datenträger in einer JBOD-Umgebung ausfällt, gehen die Daten auf diesem Datenträger verloren. 

Angesichts der Größe der Exchange Online und der Tatsache, dass darin Millionen von Festplattenlaufwerken bereitgestellt werden, treten in Exchange Online regelmäßig Festplattenlaufwerkfehler auf. Tatsächlich schlagen mehr als 100 Fehler täglich fehl. Wenn ein Datenträger in einer lokalen Unternehmensbereitstellung fehlschlägt, muss ein Administrator den ausgefallenen Datenträger manuell ersetzen und die betroffenen Daten wiederherstellen. In einer Cloudbereitstellung ist die Größe der Microsoft 365, dass Operatoren (Cloudadministratoren) Datenträger manuell ersetzen, weder praktisch noch machbar. 

AutoReseed oder *AutoReseed* ist ein Feature, das die normalerweise operatorgesteuerte Aktion als Reaktion auf einen Datenträgerfehler, ein Datenbankbeschädigungsereignis oder ein anderes Problem ersetzt, das eine erneute Veröffentlichung einer Datenbankkopie erforderlich macht. AutoReseed wurde entwickelt, um Datenbankredundanz nach einem Datenträgerfehler automatisch wiederherzustellen, indem auf dem System bereitgestellte Ersatzdatenträger verwendet werden. Wenn ein Datenträger ausfällt, werden die auf diesem Datenträger gespeicherten Datenbankkopien automatisch auf einen vorkonfigurierten Ersatzdatenträger auf dem Server erneut gesendet, wodurch Redundanz wiederhergestellt wird. 