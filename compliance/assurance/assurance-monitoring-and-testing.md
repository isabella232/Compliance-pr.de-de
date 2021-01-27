---
title: Angriffssimulation in Microsoft 365
description: In diesem Artikel erfahren Sie, wie Microsoft die Mandantengrenzen für Microsoft 365 kontinuierlich überwacht und testet.
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
ms.openlocfilehash: 9d38131a6ec8f3213c288d76dc3b176ceaa3aace
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012891"
---
# <a name="attack-simulation-in-microsoft-365"></a>Angriffssimulation in Microsoft 365

Microsoft überwacht und testet kontinuierlich auf Schwachstellen und Sicherheitslücken in Mandantengrenzen, einschließlich der Überwachung auf Eindringversuche, Versuche von Berechtigungsverstößen und Ressourcenverplatzung. Wir verwenden auch mehrere interne Systeme, um kontinuierlich auf unangemessene Ressourcenverwendung zu überwachen, was, falls erkannt, integrierte Drosselung auslöst.

Microsoft 365 verfügt über interne Überwachungssysteme, die kontinuierlich auf Fehler überwachen und die automatisierte Wiederherstellung bei Erkannten des Fehlers unterstützen. Microsoft 365-Systeme analysieren Abweichungen im Dienstverhalten und initiieren self-healing-Prozesse, die in das System integrierte sind. Microsoft 365 verwendet auch eine externe Überwachung, bei der die Überwachung von mehreren Standorten aus sowohl von vertrauenswürdigen Drittanbieterdiensten (für eine unabhängige SLA-Überprüfung) als auch von unseren eigenen Rechenzentren durchgeführt wird, um Warnungen zu auslösen. Für die Diagnose verfügen wir über umfassende Protokollierung, Überwachung und Ablaufverfolgung. Eine präzise Ablaufverfolgung und Überwachung hilft uns, Probleme zu isolieren und eine schnelle und effektive Ursachenanalyse durchzuführen.

Während Microsoft 365 nach Möglichkeit automatisierte Wiederherstellungsaktionen verwendet, stehen Die Techniker von Microsoft on-Call rund um die Uhr zur Verfügung, um alle Sicherheitseskalationen des Schweregrads 1 zu untersuchen, und die nachträgliche Überprüfung jedes Dienstvorfalls trägt zu kontinuierlichen Lern- und Verbesserungsmaßnahmen bei. Dieses Team umfasst Supporttechniker, Produktentwickler, Programmmanager, Produktmanager und führungskräfte. Unsere Anrufer bieten eine zeitnahe Sicherung und können häufig Wiederherstellungsaktionen automatisieren, sodass ein Ereignis beim nächsten Auftreten selbstbehingt werden kann.

Microsoft führt bei jedem Auftreten eines Microsoft 365-Sicherheitsvorfalls unabhängig von der Größe der Auswirkungen eine gründliche Überprüfung nach dem Vorfall durch. Eine Überprüfung nach einem Vorfall besteht aus einer Analyse, was passiert ist, wie wir reagiert haben und wie wir ähnliche Vorfälle in Der Zukunft verhindern. Im Interesse der Transparenz und Rechenschaftspflicht teilen wir die Überprüfung nach einem Vorfall für größere Dienstvorfälle mit den betroffenen Kunden. Weitere Informationen finden Sie unter [Office 365 Security Incident Management](https://aka.ms/Office365SIM).

## <a name="assume-breach-methodology"></a>Gehen Sie von einer Verletzungsmethode aus.

Basierend auf einer detaillierten Analyse der Sicherheitstrends plädiert Microsoft für weitere Investitionen in reaktive Sicherheitsprozesse und -technologien, die sich auf die Erkennung und Reaktion auf neue Bedrohungen konzentrieren und nicht nur die Verhinderung dieser Bedrohungen. Aufgrund von Änderungen in der Bedrohungslandschaft und einer eingehenden Analyse hat Microsoft seine Sicherheitsstrategie über das Verhindern von Sicherheitsverletzungen hinaus auf eine noch besser für den Umgang mit Sicherheitsverletzungen bei deren Auftreten überarbeitet. Eine Strategie, bei der wichtige Sicherheitsereignisse nicht als Frage berücksichtigt werden, ob, sondern wann.

Microsoft geht [](https://www.microsoft.com/TrustCenter/Security/default.aspx) zwar davon aus, dass Verletzungspraktiken seit vielen Jahren verwendet werden, viele Kunden sind sich jedoch der Arbeit im Hintergrund nicht bewusst, um die Microsoft Cloud zu härten. Gehen Sie davon aus, dass es sich bei der Verletzung um eine Mindset handelt, die Sicherheitsinvestitionen, Entwurfsentscheidungen und betriebliche Sicherheitspraktiken leitet. Gehen Sie davon aus, dass eine Verletzung das Vertrauen in Anwendungen, Dienste, Identitäten und Netzwerke einschränkt, indem alle – intern und extern – als unsicher und bereits gefährdet behandelt werden. Obwohl die Strategie "Assume Breach" nicht von einer tatsächlichen Verletzung von Microsoft Enterprise- oder Clouddiensten abhing, wurde erkannt, dass viele Organisationen in der gesamten Branche trotz aller Versuche, dies zu verhindern, verletzt wurden. Das Verhindern von Sicherheitsverletzungen ist zwar ein wichtiger Bestandteil der Vorgänge in einer Organisation, diese Praktiken müssen jedoch kontinuierlich getestet und erweitert werden, um moderne Widerskräfte und fortgeschrittene dauerhafte Bedrohungen effektiv zu adressieren. Damit sich eine Organisation auf eine Verletzung vorbereiten kann, muss sie zunächst robuste, wiederholbare und sorgfältig getestete Verfahren zur Sicherheitsreaktion erstellen und verwalten.

Während Sicherheitsprozesse zur Verhinderung von Sicherheitsverletzungen, z. B. Bedrohungsmodellierung, Codeüberprüfungen und Sicherheitstests, im Rahmen des [Security Development Lifecycle](https://www.microsoft.com/securityengineering/sdl/)sehr nützlich sind, bietet "Assume Breach" zahlreiche Vorteile, die bei der Berücksichtigung der Gesamtsicherheit helfen, indem reaktive Funktionen im Falle einer Verletzung verwendet und gemessen werden.

Bei Microsoft haben wir uns darauf festgelegt, dies durch fortlaufende Übungen zu Spielen und Penetrationstests für Livewebsites unserer Sicherheitsreaktionspläne zu erreichen, um unsere Erkennungs- und Reaktionsfähigkeit zu verbessern. Microsoft simuliert regelmäßig reale Sicherheitsverletzungen, führt eine kontinuierliche Sicherheitsüberwachung durch und führt die Verwaltung von Sicherheitsvorfällen durch, um die Sicherheit von Microsoft 365, Azure und anderen Microsoft Cloud Services zu überprüfen und zu verbessern.

Microsoft führt seine Sicherheitsstrategie "Assume Breach" mit zwei Hauptgruppen aus:

- Rote Teams (Angreifer)
- Blaue Teams (Verteidiger)

Sowohl Microsoft Azure- als auch Microsoft 365-Mitarbeiter trennen rote und blaue Vollzeitteams.

Der Ansatz, der als "Rotes[Teaming"](https://go.microsoft.com/fwlink/?linkid=518599)bezeichnet wird, besteht im Testen von Azure- und Microsoft 365-Systemen und -Vorgängen mit denselben Taktiken, Techniken und Verfahren wie echte Gegner gegen die Liveproduktionsinfrastruktur, ohne dass die Technik- oder Betriebsteams dies wissen müssen. Dies testet die Sicherheitserkennungs- und Reaktionsfunktionen von Microsoft und hilft dabei, Sicherheitsrisiken, Konfigurationsfehler, ungültige Annahmen und andere Sicherheitsprobleme kontrolliert zu identifizieren. Auf jede Verletzung des roten Teams folgt eine vollständige Offenlegung zwischen beiden Teams, um Lücken zu erkennen, Erkenntnisse zu beseitigen und die Reaktion auf Sicherheitsverletzungen zu verbessern.

**HINWEIS:** Während der Penetrationstests für rote Teams oder Livewebsites werden absichtlich keine Kundendaten gezielt verwendet. Die Tests werden mit der Microsoft 365- und der Azure-Infrastruktur und -Plattformen sowie mit den eigenen Mandanten, Anwendungen und Daten von Microsoft durchgeführt. Kunden-Mandanten, Anwendungen und Inhalte, die in Microsoft 365 oder Azure gehostet werden, sind nie zielgerichtet.

## <a name="red-teams"></a>Rote Teams

Das rote Team ist eine Gruppe von Vollzeitmitarbeitern in Microsoft, die sich auf die Verletzung der Infrastruktur, der Plattform und der eigenen Mandanten und Anwendungen von Microsoft konzentrieren. Sie sind der dedizierte Angreifer (eine Gruppe von ethischen Hackern), der gezielte und dauerhafte Angriffe auf Onlinedienste (Microsoft-Infrastruktur, -Plattformen und -Anwendungen, aber keine Anwendungen oder Inhalte von Endbenutzern) durchführen.

Das rote Team hat die Aufgabe, Umgebungen mit denselben Schritten wie ein Angreifer angreift und zu durchdringen:

![Phasen von Sicherheitsverletzungen](../media/office-365-isolation-breach-stages.png)

Neben anderen Funktionen versuchen rote Teams insbesondere, die Grenzen der Mandantenisolation zu überschreiten, um Fehler oder Lücken in unserem Isolationsentwurf zu finden.

## <a name="blue-teams"></a>Blaue Teams

Das blaue Team besteht entweder aus einer dedizierten Gruppe von Security Respondern oder Mitgliedern aus den Organisationen für die Reaktion auf Sicherheitsvorfälle, engineering und operations. Unabhängig von ihrem Make-up sind sie unabhängig und arbeiten separat vom roten Team. Das blaue Team folgt etablierten Sicherheitsprozessen und verwendet die neuesten Tools und Technologien, um Angriffe und Penetrationen zu erkennen und darauf zu reagieren. Genau wie reale Angriffe weiß das blaue Team nicht, wann oder wie die Angriffe des roten Teams auftreten oder welche Methoden verwendet werden können. Ihre Aufgabe ist es, alle Sicherheitsvorfälle zu erkennen und darauf zu reagieren, egal ob es sich um einen angriffsroten Teamangriff oder einen tatsächlichen Angriff handelt. Aus diesem Grund ist das blaue Team ständig im Anruf und muss auf Verstöße des roten Teams auf die gleiche Weise reagieren wie bei jeder anderen Verletzung.

Wenn ein Gegner, z. B. ein rotes Team, eine Umgebung verletzt hat, muss das blaue Team:

- Sammeln von Nachweisen, die vom Widerswilligen übrig bleiben
- Erkennen des Nachweises als Hinweis auf eine Bedrohung
- Warnen Sie die entsprechenden Entwicklungs- und Betriebsteams
- Überprüfen Sie die Warnungen, um festzustellen, ob sie eine weitere Untersuchung rechtfertigen.
- Erfassen von Kontext aus der Umgebung zum Umfang der Verletzung
- Erstellen eines Wartungsplans zum Ein- oder Zurückdingen des Gegners
- Ausführen des Wartungsplans und Wiederherstellen nach einer Verletzung

Diese Schritte bilden die Reaktion auf Sicherheitsvorfälle, die parallel zu den Sicherheitsvorfällen ausgeführt wird, wie unten dargestellt:

![Reaktionsphasen bei Sicherheitsverletzungen](../media/office-365-isolation-breach-response-stages.png)

Verstöße gegen das rote Team ermöglichen es, die Fähigkeit des blauen Teams, Reale Angriffe zu erkennen und darauf zu reagieren, von Ende zu Ende zu trainieren. Vor allem ermöglicht sie eine geübte Reaktion auf Sicherheitsvorfälle vor einer echten Verletzung. Darüber hinaus verbessert das blaue Team aufgrund von Verletzungen des roten Teams sein situationelles Bewusstsein, das beim Umgang mit zukünftigen Sicherheitsverletzungen (vom roten Team oder einem anderen Widerswilligen) nützlich sein kann. Während des Erkennungs- und Reaktionsprozesses erzeugt das blaue Team eine umsetzbare Intelligenz und erhält Einblick in die tatsächlichen Bedingungen der Umgebung(en), die sie zu schützen versuchen. Häufig erfolgt dies über Datenanalyse und Forensik, die vom blauen Team durchgeführt werden, wenn auf Angriffe des roten Teams reagiert und Bedrohungsindikatoren wie Gefährdungsindikatoren verwendet werden. Ähnlich wie das rote Team Lücken in der Sicherheitsgeschichte identifiziert, erkennen blaue Teams Lücken in ihrer Fähigkeit, zu erkennen und darauf zu reagieren. Da die roten Teams reale Angriffe modellieren, kann das blaue Team darüber hinaus genau auf ihre Fähigkeit oder Unfähigkeit bewertet werden, mit bestimmten und dauerhaften Angriffen um zu umgehen. Schließlich messen Verletzungen des roten Teams sowohl die Bereitschaft als auch die Auswirkungen unserer Reaktion auf Sicherheitsverletzungen.
