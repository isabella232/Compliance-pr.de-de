---
title: Sicherheitsmaßnahmen für die Umgebung von Rechenzentren
description: Erfahren Sie mehr über die Sicherheitsvorkehrungen für die Umgebung von Microsoft-Rechenzentren.
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
ms.openlocfilehash: 525aab55d3f56490ecd1f1da1e00d6c5ddd32dc4
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265111"
---
# <a name="datacenter-environmental-safeguards"></a>Sicherheitsmaßnahmen für die Umgebung von Rechenzentren

Microsoft setzt verschiedene Sicherheitsvorkehrungen ein, um die Verfügbarkeit von Rechenzentren vor Umweltbedrohungen zu schützen. Diese Sicherheitsvorkehrungen ermöglichen Es Microsoft, sichere und verfügbare Cloudplattformen bereitzustellen, die von Kunden als vertrauenswürdig eingestuft werden.

## <a name="site-selection"></a>Standortauswahl

Der Schutz von Microsoft-Rechenzentren vor Umweltrisiken beginnt mit der Standortauswahl. Die Standorte von Microsoft-Rechenzentren werden vor der Auswahl für den Aufbau des Rechenzentrums streng ausgewertet. Microsoft-Rechenzentrumsstandorte werden strategische ausgewählt, um das Risiko durch mehrere Faktoren zu minimieren, einschließlich Überschwemmungen, Risikobewertungen, Naturkatastrophen und anderen Naturkatastrophen. Bei der Auswahl des Standorts gehören zusätzlich zum Minimieren der Umweltrisiken auch der Zugang zu einer kostengünstigen Strom- und einer zuverlässigen Telekommunikationsinfrastruktur zu den wichtigsten Aspekten.

## <a name="climate-control"></a>Klimakontrolle

Die Klimakontrolle ist ein wesentlicher Bestandteil der kritischen Infrastruktur innerhalb eines Rechenzentrums und wird zur Überwachung und Verwaltung von optimierten, konditionierten Räumen für Personal und Geräte/Hardware eingesetzt. Die Wärmelast (als Nebenprodukt des Energieverbrauchs) und die Feuchtigkeit müssen geregelt werden, um durch mechanische Eingriffe geeignete Betriebsbedingungen sicherzustellen. Die lokalen Klimabedingungen, die unterschiedlichen behördlichen Voraussetzungen und Einschränkungen geben den effektivsten Weg für eine Lösung vor.

Temperatur- und Feuchtigkeitsgrade werden in Übereinstimmung mit den Umgebungsanforderungen der IT-Hardware beibehalten, die in den einzelnen Rechenzentren erwartet wird. Microsoft-Rechenzentren halten eine Vereinbarung auf Betriebsebene mit ihren Kunden aufrecht, sodass eine optimale Effizienz bei gleichzeitiger Einhaltung der Mindestanforderungen an die Umgebung erreicht wird. Die Temperatur- und Feuchtigkeitsgrade werden kontinuierlich vom Gebäudeverwaltungssystem (Building Management System, BMS) des Rechenzentrums überwacht. Teammitglieder kritischer Umgebungen (CRITICAL Environments, CE) überwachen den BMS vom Facilities Operations Center (FOC), sodass sie die Temperatur und Feuchtigkeit innerhalb des Rechenzentrums verwalten können, bevor Alarmpunkte überschritten werden. BMS ist so konfiguriert, dass das CE-Team benachrichtigt wird, wenn bestimmte Markierungen erreicht werden, die dann untersuchen und Anpassungen vornehmen, um das Problem zu beheben. Zulässige Bereiche für Temperatur und Feuchtigkeit sind mit den AsHRAE-Richtlinien (American Country of Enthition, Lufttransporttechniker) oder ähnlichen lokal anwendbaren Richtlinien konsistent. Die Rechenzentrumsfeuchtigkeit wird durch den Relativen Feuchtigkeitsprozentsatz gemessen, nicht verdichtet mit dem aktuellen Bereich zwischen 40 % und 55 %. Der Temperaturbereich liegt in der Regel zwischen 18 Grad Und 27 Grad (zwischen 64,4 Grad Fahrenheit und 80,6 Grad Fahrenheit).

## <a name="fire-and-water-damage-protection"></a>Schutz vor Feuer- und Wasserschäden

Microsoft setzt in jedem Rechenzentrum Brandmelde- und Brandschutzsysteme ein. Systeme zur Brandverhütung werden von einer unabhängigen Energiequelle unterstützt, um den Schutz der Mitarbeiter und der Infrastruktur von Microsoft zu gewährleisten, wenn es zu einem Brand kommt. Rechenzentren werden außerdem durch Wassersensoren vor Wasserschäden geschützt, die in Bereichen platziert werden, an denen ein Leckagerisiko besteht. Diese Wassersensoren informieren das entsprechende Personal schnell, wenn es einen wasserbedingten Notfall gibt. Wasserabsperrventile sind barrierefrei konzipiert, und die Mitarbeiter sind in ihrer Bedienung und Position geschult.

Microsoft-Rechenzentren implementieren robuste Branderkennungsmechanismen, einschließlich Photoqualmerkennungen, die unterhalb des Bodens und an der Obergrenze installiert sind, Xtralis-Systeme für die Erkennung von Frühschäubungsgeräten (VERY Early Fire Detection Gerät, VESDA) in jeder Colocation, In den Rechenzentren installierte Löschalarmboxen der Pullstation, Brandmeldegeräte in den Rechenzentren, Brandlöscher in den Rechenzentren, Sicherheitsmitarbeiter, die in allen Gebäudebereichen mehrmals im Acht-Stunden-Schichtdienst arbeiten.  und Branderkennungs-/Unterdrückungssysteme und Notfallbeleuchtungssysteme sind mit den Sicherungssystemen des Rechenzentrums verkabelt, die eine redundante Stromversorgung bereitstellen. Bereiche mit sensiblen elektronischen Geräten werden durch Sprinklersysteme mit doppelter Interlockvoraktion (Trockenleitung) geschützt.

Das CE-Team führt einen täglichen Site-Walk-Through (DSWT) durch, um jeden Raum und viele Komponententeile darin zu überprüfen, um sicherzustellen, dass alle Anforderungen an die Brandüberwachung erfüllt werden.

Microsoft setzt Branderkennungsgeräte/-systeme für das Informationssystem ein, die automatisch aktiviert werden und das Personal des Rechenzentrums zusammen mit den Notfallaktivierern benachrichtigen, wenn ein Brand auftritt. Wenn einer der Branderkennungsmechanismen in einem Colocation-Raum aktiviert wird, werden die lokale Feuerwehr und das Global Security Operations Center in Redmond, Washington, automatisch benachrichtigt. Brandschutz- und Erkennungssysteme sind an das Sicherheitssystem gebunden, das die lokale Einrichtung und das Sicherheitspersonal benachrichtigt.

Microsoft bietet die Erkennung von Wasser/Lecks in Bereichen mit dem Risiko von Wasserlecks. Brandunterdrückungssysteme verfügen auch über Alarme zur Erkennung von Lecks, die überwacht werden. Das Wasser-/Leckerkennungssystem ist in das Alarm- und Benachrichtigungssystem der Einrichtung integriert, und Sprinklersysteme innerhalb der Rechenzentren sind zoneiert. Die CE- und Datacenter-Verwaltungsteams sind mit den Notfallverfahren vertraut, die die Verwendung der Wasserabsperrungsdrosseln und ihrer Standorte erfordern. Sprinkler-Steige können einzeln oder als Gruppe über Torsperren heruntergefahren werden. Alle Sprinkler im kritischen Raum sind Sprinkler vom Typ "Doppelte Verriegelung vor Aktion", die zwei Aktivierungsarten erfordern, bevor der Fluss initiiert wird. Der Druck des Sprinklersystems wird überwacht und vor Wasserlecks alarmiert.

## <a name="health-and-safety"></a>Gesundheit und Sicherheit

Das Engagement für die Gesundheit und Sicherheit von Microsoft-Mitarbeitern ist entscheidend für die Erfolgsmessung. Microsoft-Rechenzentren arbeiten in Übereinstimmung mit lokalen, regionalen, nationalen und nationalen Gesundheits- und Sicherheitsbestimmungen. In den meisten Fällen überschreiten die Microsoft-Richtlinien für Gesundheit und Sicherheit die gesetzlichen Anforderungen, um den Schutz der Gesundheit, Sicherheit und des Wohlbefindens aller Mitarbeiter von Rechenzentren während aller Phasen des Lebenszyklus des Rechenzentrums sicherzustellen, von der Konstruktion bis zur Außerbetriebnahme. Sicherheitsverwaltungspläne, Risikobewertung, Risikomanagement und Sicherheitsschulungen sind zentrale Grundsätze für die Bereitstellung einer sicheren Arbeitsumgebung für alle Mitarbeiter.

## <a name="energy-efficiency"></a>Energieeffizienz

Microsoft arbeitet seit 2012 CO2-neutral. Bis 2030 wird Microsoft co2-negativ sein, und bis 2050 wird Microsoft den gesamten Co2-Co2-Wert, den das Unternehmen seit seiner Gründung im Jahr 1975 entweder direkt oder durch Stromverbrauch ausgegeben hat, aus der Umgebung entfernt haben. Bis 2025 werden Microsoft-Rechenzentren um 100 Prozent verlängerbare Energie bereitgestellt. Um dieses Ziel zu erreichen, hat Microsoft Vertragstools implementiert, wie z. B. Verträge zur Proxygenerierung von Energie für grüne Energie, um 100 Prozent der von allen Rechenzentren verbrauchten Co2-emittierenden Energie zu liefern.
