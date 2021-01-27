---
title: Datenresilienz in Microsoft 365
description: In diesem Artikel erfahren Sie mehr über den Entwurf und die Prinzipien der Datenresilienz und -wiederherstellung in Microsoft 365.
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
ms.openlocfilehash: 361400bf6330fb82d34f384d17e4d4ee438ccf08
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012901"
---
# <a name="data-resiliency-in-microsoft-365"></a>Datenresilienz in Microsoft 365

Angesichts des komplexen Charakters von Cloud Computing ist Microsoft der Meinung, dass es nicht darum geht, ob etwas schief geht, sondern wann. Wir entwerfen unsere Clouddienste, um die Zuverlässigkeit zu maximieren und die negativen Auswirkungen auf Kunden zu minimieren, wenn etwas schief geht. Wir haben uns über die herkömmliche Strategie der Basierten auf komplexe physische Infrastruktur hinaus bewegt und Redundanz direkt in unsere Clouddienste integrierte. Wir verwenden eine Kombination aus weniger komplexerer physischer Infrastruktur und intelligenterer Software, die Datenresilienz in unsere Dienste einf?pft und unseren Kunden hohe Verfügbarkeit bietet.

## <a name="resiliency-and-recoverability-are-built-in"></a>Resilienz und Wiederherstellbarkeit sind integrierte

Der Aufbau von Resilienz und Wiederherstellung beginnt mit der Annahme, dass die zugrunde liegende Infrastruktur und die zugrunde liegenden Prozesse zu einem bestimmten Zeitpunkt fehlschlagen: Hardware (Infrastruktur) wird fehlschlagen, Menschen machen Fehler, und die Software hat Fehler. Es wäre zwar falsch zu sagen, dass Softwareentwickler vor der Cloud nicht über diese Dinge nachdenkten, aber wie diese Probleme in einer typischen IT-Implementierung behandelt wurden, war vor der Cloud anders:

- Zunächst waren Hardware- und Infrastrukturschutz erheblich. Diese Struktur bedeutete, dass Rechenzentren mit einer Zuverlässigkeit von 99,99 % erhebliche Energie- und Netzwerkredundanz erforderten, und Server wurden mit hardwarebasiertem Clustering, dualen Netzteilen, dualen Netzwerkschnittstellen und deren Implementierung implementiert.
- Zweitens war der Prozess äußerst wichtig. Betriebsteams verwalteten strenge Verfahren, Änderungsfenster wurden eingesetzt, und es gab häufig einen erheblichen Mehraufwand für das Projektmanagement.
- Die dritte Bereitstellung erfolgte in einem besonderen Tempo. Das Bereitstellen von Code ohne die Quelle bedeutete warten auf Patchversionen, und Hauptversionsversionen setzten Hardwareersetzung und erhebliche Investitionen ein. Darüber hinaus war die einzige Möglichkeit, ein Problem zu beheben, das Rollback. Daher würden die meisten IT-Organisationen nur Hauptversionen bereitstellen, um die Arbeit zu vermeiden, um auf dem neuesten Stand zu bleiben.
- Schließlich war das Ausmaß der bereitgestellten Systeme und die Ebene ihrer Verbundenheit in der Vergangenheit viel kleiner als jetzt.

Kunden erwarten heutzutage kontinuierliche Innovationen von Microsoft, ohne die Qualität zu kompromittieren. Dies ist einer der Gründe, warum die Dienste und Software von Microsoft unter Bedenken von Resilienz und Wiederherstellbarkeit erstellt werden.

## <a name="microsoft-365-data-resiliency-principles"></a>Prinzipien der Datenresilienz von Microsoft 365

Resilienz bezieht sich auf die Fähigkeit eines cloudbasierten Diensts, bestimmte Arten von Fehlern zu überstehen und dennoch aus Sicht der Kunden voll funktionsfähig zu bleiben. Datenresilienz bedeutet, dass kritische Kundendaten unabhängig davon, welche Fehler in Microsoft 365 auftreten, intakt bleiben und nicht betroffen sind. Zu diesem Zweck wurden Microsoft 365-Dienste auf fünf spezifische Resilienzprinzipien ausgelegt:

- Es gibt kritische und nicht kritische Daten. Nicht kritische Daten (z. B. ob eine Nachricht gelesen wurde) können in seltenen Fehlerszenarien gelöscht werden. Kritische Daten (z. B. Kundendaten wie E-Mail-Nachrichten) sollten mit äußersten Kosten geschützt werden. Als Entwurfsziel sind zugestellte E-Mail-Nachrichten immer wichtig, und Dinge wie die Frage, ob eine Nachricht gelesen wurde, sind unkritisch.
- Kopien von Kundendaten müssen in verschiedene Fehlerzonen oder so viele Fehlerdomänen wie möglich unterteilt werden (z. B. Rechenzentren, auf die durch einzelne Anmeldeinformationen (Prozess, Server oder Operator) zugegriffen werden kann), um eine Fehlerisolation zu ermöglichen. 
- Kritische Kundendaten müssen darauf überwacht werden, dass sie einen Teil von Atomarität, Konsistenz, Isolation, Isolierung (Isolierung, Isolierung) nicht erreichen.
- Kundendaten müssen vor Beschädigungen geschützt werden. Sie muss aktiv überprüft oder überwacht, repariert und wiederherstellbar sein.
- Die meisten Datenverluste werden durch Kundenaktionen erzielt, sodass Kunden die Wiederherstellung selbst mithilfe einer GUI durchführen können, mit der sie versehentlich gelöschte Elemente wiederherstellen können.

Durch die Entwicklung unserer Clouddienste nach diesen Prinzipien in Verbindung mit robusten Tests und Validierungen kann Microsoft 365 die Anforderungen von Kunden erfüllen und übertreffen und gleichzeitig eine Plattform für kontinuierliche Innovation und Verbesserung sicherstellen.

## <a name="related-articles"></a>Verwandte Artikel

- [Umgang mit Datenbeschädigung](assurance-dealing-with-data-corruption.md)
- [Schutz vor Schadsoftware und Ransomware](assurance-malware-and-ransomware-protection.md)
- [Überwachung und Selbstreparatur](assurance-monitoring-and-self-healing.md)
- [Ausfallsicherheit von Exchange-Daten](assurance-exchange-data-resiliency.md)
