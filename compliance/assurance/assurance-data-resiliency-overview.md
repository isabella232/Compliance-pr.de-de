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
hideEdit: true
ms.openlocfilehash: a0745cda440b2262f4b09764e71514aeab946a6e8e0adcd4cdbccaffd14c5fe3
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54291333"
---
# <a name="data-resiliency-in-microsoft-365"></a>Datenresilienz in Microsoft 365

Angesichts der komplexitätsbezogenen Natur von Cloud Computing ist Microsoft sicher, dass es sich nicht um einen Fall handelt, wenn die Dinge schief gehen, sondern wann. Wir entwerfen unsere Clouddienste, um die Zuverlässigkeit zu maximieren und die negativen Auswirkungen auf Kunden zu minimieren, wenn dinge schief gehen. Wir haben die herkömmliche Strategie der Nutzung komplexer physischer Infrastruktur nicht mehr verfolgt, und wir haben Redundanz direkt in unsere Clouddienste integriert. Wir verwenden eine Kombination aus weniger komplexer physischer Infrastruktur und intelligenterer Software, die Datenresilienz in unsere Dienste integriert und unseren Kunden eine hohe Verfügbarkeit bietet.

## <a name="resiliency-and-recoverability-are-built-in"></a>Resilienz und Wiederherstellbarkeit sind integriert

Das Erstellen von Resilienz und Wiederherstellung beginnt mit der Annahme, dass die zugrunde liegende Infrastruktur und prozesse zu einem bestimmten Zeitpunkt fehlschlagen: Hardware (Infrastruktur) schlägt fehl, Menschen machen Fehler, und Software hat Fehler. Es wäre zwar falsch zu sagen, dass Softwareentwickler vor der Cloud nicht über diese Dinge nachdenkten, aber wie diese Probleme in einer typischen IT-Implementierung behandelt wurden, war vor der Cloud anders:

- Zunächst waren Hardware- und Infrastrukturschutz erheblich. Diese Struktur bedeutete, dass Rechenzentren mit einer Zuverlässigkeit von 99,99 % erhebliche Energie- und Netzwerkredundanz erforderten, und Server wurden mit hardwarebasiertem Clustering, dualen Stromversorgungen, dualen Netzwerkschnittstellen usw. implementiert.
- Zweitens war der Prozess äußerst wichtig. Betriebsteams führten strenge Verfahren durch, Änderungsfenster wurden eingesetzt, und häufig war der Projektmanagementaufwand erheblich.
- Drittens erfolgte die Bereitstellung in einem glanzgeschützten Tempo. Die Bereitstellung von Code ohne Besitzer der Quelle bedeutete, dass auf Patchversionen gewartet werden musste, und für Hauptversionsversionen waren Hardwareersetzung und erheblicher Kapitalaufwand erforderlich. Darüber hinaus bestand die einzige Möglichkeit zum Beheben eines Problems darin, ein Rollback auszuführen. Daher würden die meisten IT-Organisationen nur Hauptversionen bereitstellen, um die Arbeit zu vermeiden, um auf dem neuesten Stand zu bleiben.
- Schließlich waren die Größe der bereitgestellten Systeme und die Art ihrer Verbundenheit in der Vergangenheit wesentlich kleiner als jetzt.

Kunden erwarten heute kontinuierliche Innovationen von Microsoft, ohne die Qualität zu beeinträchtigen. Dies ist einer der Gründe, warum Die Dienste und Software von Microsoft unter Berücksichtigung von Resilienz und Wiederherstellbarkeit erstellt werden.

## <a name="microsoft-365-data-resiliency-principles"></a>Prinzipien der datenresilienz Microsoft 365

Resilienz bezieht sich auf die Fähigkeit eines cloudbasierten Diensts, bestimmte Arten von Fehlern zu beheben und dennoch aus Sicht des Kunden voll funktionsfähig zu bleiben. Datenresilienz bedeutet, dass kritische Kundendaten unabhängig davon, welche Fehler innerhalb Microsoft 365 auftreten, intakt und nicht betroffen bleiben. Zu diesem Zweck wurden Microsoft 365 Dienste auf fünf spezifische Resilienzprinzipien ausgelegt:

- Es gibt kritische und nicht kritische Daten. Nicht kritische Daten (z. B. ob eine Nachricht gelesen wurde) können in seltenen Fehlerszenarien gelöscht werden. Kritische Daten (z. B. Kundendaten wie E-Mail-Nachrichten) sollten mit extrem hohen Kosten geschützt werden. Als Entwurfsziel sind zugestellte E-Mail-Nachrichten immer kritisch, und Dinge wie das Lesen einer Nachricht sind nicht kritisch.
- Kopien von Kundendaten müssen in verschiedene Fehlerzonen oder so viele Fehlerdomänen wie möglich unterteilt werden (z. B. Rechenzentren, auf die über einzelne Anmeldeinformationen (Prozess, Server oder Operator) zugegriffen werden kann, um Fehlerisolation bereitzustellen. 
- Kritische Kundendaten müssen überwacht werden, wenn ein Teil der Atomität, Konsistenz, Isolation, Empfindlichkeit (ATOMICY) nicht erfüllt wird.
- Kundendaten müssen vor Beschädigungen geschützt werden. Es muss aktiv gescannt oder überwacht, repariert und wiederhergestellt werden können.
- Die meisten Datenverluste ergeben sich aus Kundenaktionen, sodass Kunden die Wiederherstellung selbst mithilfe einer GUI durchführen können, mit der sie versehentlich gelöschte Elemente wiederherstellen können.

Durch die Weiterentwicklung unserer Clouddienste auf diese Prinzipien, gepaart mit robusten Tests und Validierungen, ist Microsoft 365 in der Lage, die Anforderungen der Kunden zu erfüllen und zu überschreiten und gleichzeitig eine Plattform für kontinuierliche Innovation und Verbesserung zu gewährleisten.

## <a name="related-articles"></a>Verwandte Artikel

- [Umgang mit Datenbeschädigung](assurance-dealing-with-data-corruption.md)
- [Schutz vor Schadsoftware und Ransomware](assurance-malware-and-ransomware-protection.md)
- [Überwachung und Selbstreparatur](assurance-monitoring-and-self-healing.md)
- [Exchange Datenresilienz](assurance-exchange-data-resiliency.md)
