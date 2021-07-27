---
title: Angriffssimulation in Microsoft 365
description: In diesem Artikel erfahren Sie, wie Microsoft mandantengrenzen kontinuierlich auf Microsoft 365 überwacht und testet.
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
ms.openlocfilehash: 5708ab20d78d1862af5613c64ea492c40bea9da1
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573833"
---
# <a name="attack-simulation-in-microsoft-365"></a>Angriffssimulation in Microsoft 365

Microsoft überwacht und testet kontinuierlich explizit auf Schwachstellen und Schwachstellen in Mandantengrenzen, einschließlich der Überwachung auf Eindringversuche, Berechtigungsverletzungsversuche und Ressourcenhunger. Wir verwenden auch mehrere interne Systeme, um kontinuierlich auf unangemessene Ressourcennutzung zu überwachen, die, wenn erkannt, eine integrierte Drosselung auslöst.

Microsoft 365 verfügt über interne Überwachungssysteme, die kontinuierlich auf Fehler überwachen und die automatische Wiederherstellung steuern, wenn ein Fehler erkannt wird. Microsoft 365 Systeme analysieren Abweichungen im Dienstverhalten und initiieren Selbstkorrekturprozesse, die in das System integriert sind. Microsoft 365 verwendet auch externe Überwachung, bei der die Überwachung von mehreren Standorten aus sowohl von vertrauenswürdigen Diensten von Drittanbietern (für die unabhängige SLA-Überprüfung) als auch von unseren eigenen Rechenzentren ausgeführt wird, um Warnungen auszulösen. Für die Diagnose verfügen wir über umfangreiche Protokollierung, Überwachung und Ablaufverfolgung. Eine präzise Ablaufverfolgung und Überwachung hilft uns, Probleme zu isolieren und eine schnelle und effektive Ursachenanalyse durchzuführen.

Während Microsoft 365 nach Möglichkeit automatisierte Wiederherstellungsmaßnahmen hat, stehen Microsoft-Bereitschaftstechniker 24 x 7 zur Verfügung, um alle Sicherheitseskalationen des Schweregrads 1 zu untersuchen, und nachträgliche Überprüfungen jedes Dienstvorfalls tragen zur kontinuierlichen Schulung und Verbesserung bei. Dieses Team umfasst Supporttechniker, Produktentwickler, Programmmanager, Produktmanager und leitende Führungskräfte. Unsere Bereitschaftsexperten bieten eine zeitnahe Sicherung und können häufig Wiederherstellungsaktionen automatisieren, sodass ein Ereignis beim nächsten Auftreten selbstgeschützt werden kann.

Microsoft führt jedes Mal, wenn ein Microsoft 365 Sicherheitsvorfall auftritt, eine umfassende Überprüfung nach dem Vorfall durch, unabhängig von der Größe der Auswirkungen. Eine Überprüfung nach einem Vorfall besteht aus einer Analyse der Ereignisse, der Reaktion und der Verhinderung ähnlicher Vorfälle in der Zukunft. Im Interesse von Transparenz und Rechenschaftspflicht teilen wir Nach-Vorfall-Überprüfungen für alle wichtigen Dienstvorfälle mit betroffenen Kunden. Spezifische Details finden Sie unter [Microsoft Security Incident Management.](assurance-security-incident-management.md)

## <a name="assume-breach-methodology"></a>Gehen Sie von einer Methodik der Verletzung aus

Basierend auf der detaillierten Analyse von Sicherheitstrends empfiehlt und hebt Microsoft die Notwendigkeit anderer Investitionen in reaktive Sicherheitsprozesse und -technologien hervor, die sich auf die Erkennung und Reaktion auf neue Bedrohungen konzentrieren, anstatt nur die Verhinderung dieser Bedrohungen. Aufgrund von Änderungen in der Bedrohungslandschaft und einer eingehenden Analyse hat Microsoft seine Sicherheitsstrategie über die Vermeidung von Sicherheitsverletzungen hinaus auf eine weise optimiert, die besser für die Behandlung von Sicherheitsverletzungen geeignet ist, wenn sie auftreten. Eine Strategie, bei der wichtige Sicherheitsereignisse nicht als Eine Frage des Falls, sondern wann betrachtet werden.

Obwohl Microsoft [davon ausgeht, dass Es](https://www.microsoft.com/TrustCenter/Security/default.aspx) bereits seit vielen Jahren Praktiken bei Sicherheitsverletzungen gibt, sind vielen Kunden die Arbeit, die hinter den Kulissen zur Härtung der Microsoft-Cloud durchgeführt wird, nicht bewusst. Es wird davon ausgegangen, dass eine Verletzung eine Mentalität ist, die sicherheitsbezogene Investitionen, Entwurfsentscheidungen und betriebliche Sicherheitspraktiken leitet. Gehen Sie davon aus, dass die Verletzung das Vertrauen in Anwendungen, Dienste, Identitäten und Netzwerke einschränkt, indem sie alle – internen und externen – als unsicher und bereits kompromittiert behandeln. Obwohl die Annahme, dass die Strategie für Sicherheitsverletzungen nicht von einer tatsächlichen Verletzung eines Microsoft-Unternehmens oder von Clouddiensten abgeleitet wurde, wurde erkannt, dass viele Organisationen in der gesamten Branche trotz aller Versuche, dies zu verhindern, verletzt wurden. Die Verhinderung von Verstößen ist zwar ein wichtiger Bestandteil der Vorgänge einer Organisation, diese Praktiken müssen jedoch kontinuierlich getestet und erweitert werden, um moderne Angreifer und fortgeschrittene dauerhafte Bedrohungen effektiv zu beheben. Damit sich jede Organisation auf eine Verletzung vorbereiten kann, müssen sie zuerst robuste, wiederholbare und sorgfältig getestete Sicherheitsmaßnahmen erstellen und aufrechterhalten.

Während sicherheitsbezogene Sicherheitsprozesse wie Bedrohungsmodellierung, Codeüberprüfungen und Sicherheitstests im Rahmen des [Security Development Lifecycles](https://www.microsoft.com/securityengineering/sdl/)sehr nützlich sind, wird davon ausgegangen, dass Sicherheitsverletzungen zahlreiche Vorteile bieten, die dazu beitragen, die Gesamtsicherheit zu berücksichtigen, indem reaktive Funktionen im Falle einer Verletzung ausgeführt und gemessen werden.

Bei Microsoft haben wir uns vorgenommen, dies durch laufende Übungen zu Spielen und Penetrationstests auf Livewebsites unserer Sicherheitsreaktionspläne zu erreichen, um unsere Erkennungs- und Reaktionsfähigkeit zu verbessern. Microsoft simuliert regelmäßig verletzungen in der Praxis, führt eine kontinuierliche Sicherheitsüberwachung durch und führt Sicherheitsvorfälle aus, um die Sicherheit von Microsoft 365, Azure und anderen Microsoft-Clouddiensten zu überprüfen und zu verbessern.

Microsoft führt seine Sicherheitsstrategie zur Annahme von Sicherheitsverletzungen mithilfe von zwei Kerngruppen aus:

- Rote Teams (Angreifer)
- Blaue Teams (Verteidiger)

Sowohl Microsoft Azure als auch Microsoft 365 Mitarbeiter trennen die red Teams- und blue-Teams in Vollzeit.

Der Ansatz, der als["Rotes Teaming"](https://go.microsoft.com/fwlink/?linkid=518599)bezeichnet wird, besteht darin, Azure und Microsoft 365 Systeme und Vorgänge mit denselben Taktiken, Techniken und Verfahren wie echte Angreifer gegen die Liveproduktionsinfrastruktur zu testen, ohne dass die Engineering- oder Operations-Teams bekannt sind. Dadurch werden die Sicherheitserkennungs- und Reaktionsfunktionen von Microsoft getestet und Produktionssicherheitsrisiken, Konfigurationsfehler, ungültige Annahmen und andere Sicherheitsprobleme auf kontrollierte Weise identifiziert. Auf jede Verletzung des roten Teams folgt eine vollständige Offenlegung zwischen beiden Teams, um Lücken zu identifizieren, Ergebnisse zu beheben und die Reaktion auf Sicherheitsverletzungen zu verbessern.

**HINWEIS:** Bei Penetrationstests für Red Teaming oder Livewebsites werden keine Kundendaten absichtlich verwendet. Die Tests beziehen sich auf Microsoft 365 und Azure-Infrastruktur und -Plattformen sowie auf die eigenen Mandanten, Anwendungen und Daten von Microsoft. Kundenmandanten, Anwendungen und Inhalte, die in Microsoft 365 oder Azure gehostet werden, sind nie zielgerichtet.

## <a name="red-teams"></a>Rote Teams

Das rote Team ist eine Gruppe von Vollzeitmitarbeitern innerhalb von Microsoft, die sich auf die Verletzung der Infrastruktur, Der Plattform und der eigenen Mandanten und Anwendungen von Microsoft konzentriert. Sie sind der dedizierte Angreifer (eine Gruppe von ethischen Hackern), die gezielte und dauerhafte Angriffe auf Onlinedienste (Microsoft-Infrastruktur, Plattformen und Anwendungen, aber nicht die Anwendungen oder Inhalte von Endbenutzern) durchführen.

Die Rolle des roten Teams besteht darin, Umgebungen mit denselben Schritten wie ein Angreifer anzugreifen und einzudringen:

![Phasen von Sicherheitsverletzungen](../media/office-365-isolation-breach-stages.png)

Unter anderem versuchen rote Teams, die Grenzen der Mandantenisolation zu überschreiten, um Fehler oder Lücken in unserem Isolationsdesign zu finden.

Um die Angriffssimulation zu skalieren, hat das rote Team ein automatisiertes Angriffsemulationstool erstellt, das regelmäßig sicher in bestimmten Microsoft 365 Umgebungen ausgeführt wird. Das Tool verfügt über eine Vielzahl vordefinierter Angriffe, die ständig erweitert und verbessert werden, um die sich entwickelnde Bedrohungslandschaft widerzuspiegeln. Zusätzlich zur Erweiterung der Abdeckung der Tests des roten Teams hilft es dem blauen Team, seine Sicherheitsüberwachungslogik zu überprüfen und zu verbessern. Die regelmäßige, fortlaufende Angriffsemulation bietet dem blauen Team einen konsistenten und vielfältigen Signalstrom, der mit den erwarteten Antworten verglichen und überprüft wird. Dies führt zu Verbesserungen in der Sicherheitsüberwachungslogik und den Reaktionsfunktionen von Microsoft 365.

## <a name="blue-teams"></a>Blaue Teams

Das blaue Team besteht aus einer dedizierten Gruppe von Sicherheitsbeantwortern oder Mitgliedern aus den Organisationen "Reaktion auf Sicherheitsvorfälle", "Engineering" und "Operations". Unabhängig von ihrem Make-Up sind sie unabhängig und arbeiten separat vom roten Team. Das blaue Team folgt etablierten Sicherheitsprozessen und verwendet die neuesten Tools und Technologien, um Angriffe und Penetration zu erkennen und darauf zu reagieren. Genau wie reale Angriffe weiß das blaue Team nicht, wann oder wie die Angriffe des roten Teams auftreten werden oder welche Methoden verwendet werden können. Ihre Aufgabe ist es, alle Sicherheitsvorfälle zu erkennen und darauf zu reagieren, unabhängig davon, ob es sich um einen Roten Team-Angriff oder einen tatsächlichen Vorfall handelt. Aus diesem Grund ist das blaue Team ständig im Bereitschaftsdienst und muss auf Verstöße gegen das rote Team auf die gleiche Weise reagieren wie bei jeder anderen Verletzung.

Wenn ein Angreifer, z. B. ein rotes Team, eine Umgebung verletzt hat, muss das blaue Team:

- Sammeln von Vom Angreifer hinterlassenen Nachweisen
- Erkennen der Nachweise als Hinweis auf eine Kompromittation
- Benachrichtigen der entsprechenden Entwicklungs- und Betriebsteams
- Überprüfen der Warnungen, um festzustellen, ob eine weitere Untersuchung erforderlich ist
- Sammeln von Kontext aus der Umgebung, um die Verletzung einzugrenzen
- Erstellen eines Korrekturplans, um den Angreifer einzudämmen oder zu löschen
- Ausführen des Wartungsplans und Wiederherstellen nach einer Verletzung

Diese Schritte bilden die Reaktion auf Sicherheitsvorfälle, die parallel zum Angreifer ausgeführt wird, wie unten dargestellt:

![Reaktionsphasen bei Sicherheitsverletzungen](../media/office-365-isolation-breach-response-stages.png)

Verstöße gegen rote Teams ermöglichen es, die Fähigkeit des blauen Teams zu trainieren, reale Angriffe end-to-end zu erkennen und darauf zu reagieren. Am wichtigsten ist, dass es eine geübten Reaktion auf Sicherheitsvorfälle vor einer echten Verletzung ermöglicht. Darüber hinaus verbessert das blaue Team aufgrund von Verstößen gegen das rote Team sein situationsbezogenes Bewusstsein, was bei zukünftigen Verstößen (vom roten Team oder von einem anderen Angreifer) hilfreich sein kann. Während des gesamten Erkennungs- und Reaktionsprozesses erzeugt das blaue Team umsetzbare Informationen und erhält Einblicke in die tatsächlichen Bedingungen der Umgebung(en), die sie zu schützen versuchen. Dies geschieht häufig über die Datenanalyse und Forensik, die vom blauen Team durchgeführt wird, wenn es auf Red Team-Angriffe reagiert und Bedrohungsindikatoren wie Gefährdungsindikatoren erstellt. Ähnlich wie das rote Team Lücken in der Sicherheit identifiziert, identifizieren blaue Teams Lücken in ihrer Fähigkeit, zu erkennen und zu reagieren. Da die roten Teams reale Angriffe modellieren, kann das blaue Team darüber hinaus genau hinsichtlich seiner Fähigkeit oder Unfähigkeit bewertet werden, mit bestimmten und dauerhaften Angreifern umzugehen. Schließlich messen Verstöße des roten Teams sowohl die Bereitschaft als auch die Auswirkungen unserer Reaktion auf Sicherheitsverletzungen.
