---
title: Datenresilienz in Microsoft 365
description: In diesem Artikel erfahren Sie mehr über das Design und die Prinzipien der Datenresilienz und -wiederherstellung in Microsoft 365.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 6e990facde47b07d50f594afb55353a5ef81dd78
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497624"
---
# <a name="data-resiliency-in-microsoft-365"></a>Datenresilienz in Microsoft 365

Angesichts der Komplexität des Cloud Computings ist Microsoft nicht der Fall, ob etwas schief geht, sondern wann. Wir entwerfen unsere Clouddienste, um die Zuverlässigkeit zu maximieren und negative Auswirkungen auf Kunden zu minimieren, wenn etwas schief geht. Wir haben die herkömmliche Strategie, auf eine komplexe physische Infrastruktur zu setzen, verlassen und Redundanz direkt in unsere Clouddienste eingebaut. Wir verwenden eine Kombination aus weniger komplexer physischer Infrastruktur und intelligenterer Software, die datenresilienz in unseren Diensten aufbaut und unseren Kunden hohe Verfügbarkeit bietet.

## <a name="resiliency-and-recoverability-are-built-in"></a>Ausfallsicherheit und Wiederherstellbarkeit sind integrierte

Die Entwicklung von Ausfallsicherheit und Wiederherstellung beginnt mit der Annahme, dass die zugrunde liegende Infrastruktur und Prozesse irgendwann fehlschlagen werden: Hardware (Infrastruktur) wird fehlschlagen, Menschen machen Fehler, und Software hat Fehler. Es wäre zwar falsch zu sagen, dass Softwareentwickler vor der Cloud nicht über diese Dinge nachdenkten, aber wie diese Probleme in einer typischen IT-Implementierung behandelt wurden, war vor der Cloud anders:

- Zunächst waren Hardware- und Infrastrukturschutz erheblich. Diese Struktur bedeutete, dass Rechenzentren mit einer Zuverlässigkeit von 99,99 % erhebliche Energie- und Netzwerkredundanz erforderten, und Server wurden mit hardwarebasiertem Clustering, dualen Stromversorgungen, dualen Netzwerkschnittstellen und deren Basis implementiert.
- Zweitens stand der Prozess im Vordergrund. Betriebsteams pflegten strenge Verfahren, Änderungsfenster wurden verwendet, und es gab häufig einen erheblichen Aufwand für die Projektverwaltung.
- Drittens erfolgte die Bereitstellung in einem glazialen Tempo. Das Bereitstellen von Code ohne die Quelle bedeutete, auf Patchversionen zu warten, und hauptversionsversionen bedeuteten Hardwareersetzung und erhebliche Kapitalaufwand. Darüber hinaus war die einzige Möglichkeit, ein Problem zu beheben, das Rollback. Daher würden die meisten IT-Organisationen nur wichtige Versionen bereitstellen, um die Arbeit zu vermeiden, um auf dem neuesten Stand zu bleiben.
- Schließlich war der Umfang der bereitgestellten Systeme und die Ebene ihrer Vernetzung in der Vergangenheit viel kleiner als jetzt.

Heute erwarten Kunden kontinuierliche Innovationen von Microsoft, ohne die Qualität zu kompromittieren. Dies ist einer der Gründe, warum die Dienste und Software von Microsoft unter Beeinträchtigung der Ausfallsicherheit und Wiederherstellbarkeit erstellt werden.

## <a name="microsoft-365-data-resiliency-principles"></a>Prinzipien der Datenresilienz von Microsoft 365

Resilienz bezieht sich auf die Fähigkeit eines cloudbasierten Diensts, bestimmte Arten von Fehlern zu überstehen und dennoch aus Kundensicht voll funktionsfähig zu bleiben. Datenresilienz bedeutet, dass kritische Kundendaten unabhängig davon, welche Fehler in Microsoft 365 auftreten, intakt bleiben und nicht betroffen sind. Zu diesem Zweck wurden Microsoft 365-Dienste auf fünf spezifische Ausfallsicherheitsprinzipien ausgelegt:

- Es gibt kritische und nicht kritische Daten. Nicht kritische Daten (z. B. ob eine Nachricht gelesen wurde) können in Szenarien mit seltenen Fehlern gelöscht werden. Kritische Daten (z. B. Kundendaten wie E-Mail-Nachrichten) sollten mit äußersten Kosten geschützt werden. Als Entwurfsziel sind zugestellte E-Mail-Nachrichten immer wichtig, und Dinge wie die Frage, ob eine Nachricht gelesen wurde, sind nicht kritisch.
- Kopien von Kundendaten müssen in verschiedene Fehlerzonen oder so viele Fehlerdomänen wie möglich unterteilt werden (z. B. Rechenzentren, auf die durch einzelne Anmeldeinformationen (Prozess, Server oder Operator) zugegriffen werden kann), um eine Fehlerisolation zu ermöglichen. 
- Kritische Kundendaten müssen überwacht werden, um einen Teil von Atomicity, Consistency, Isolation, Durability (ACID) nicht zu erreichen.
- Kundendaten müssen vor Beschädigungen geschützt werden. Es muss aktiv gescannt oder überwacht, repariert und wiederherstellbar sein.
- Die meisten Datenverluste werden durch Kundenaktionen erzielt, sodass Kunden die Wiederherstellung selbst mithilfe einer GUI durchführen können, mit der sie versehentlich gelöschte Elemente wiederherstellen können.

Durch die Entwicklung unserer Clouddienste zu diesen Prinzipien, gepaart mit robusten Tests und Überprüfungen, kann Microsoft 365 die Anforderungen der Kunden erfüllen und übertreffen und gleichzeitig eine Plattform für kontinuierliche Innovationen und Verbesserungen sicherstellen.

## <a name="related-articles"></a>Verwandte Artikel

- [Umgang mit Datenbeschädigung](assurance-dealing-with-data-corruption.md)
- [Schutz vor Schadsoftware und Ransomware](assurance-malware-and-ransomware-protection.md)
- [Überwachung und Selbstreparatur](assurance-monitoring-and-self-healing.md)
- [Ausfallsicherheit von Exchange-Daten](assurance-exchange-data-resiliency.md)
