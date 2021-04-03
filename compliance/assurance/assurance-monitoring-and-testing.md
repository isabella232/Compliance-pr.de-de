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
hideEdit: true
ms.openlocfilehash: b37ca23fa403bd0a4a657be78654a02bf23721b3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497531"
---
# <a name="attack-simulation-in-microsoft-365"></a>Angriffssimulation in Microsoft 365

Microsoft überwacht und testet kontinuierlich auf Schwachstellen und Sicherheitsrisiken in Mandantengrenzen, einschließlich überwachung auf Eindringversuche, Berechtigungsverletzungsversuche und Ressourcenhunger. Wir verwenden auch mehrere interne Systeme, um kontinuierlich auf unangemessene Ressourcenauslastung zu überwachen, was bei Erkannten eine integrierte Drosselung auslöst.

Microsoft 365 verfügt über interne Überwachungssysteme, die kontinuierlich auf Fehler überwachen und die automatische Wiederherstellung beim Erkennen eines Fehlers unterstützen. Microsoft 365-Systeme analysieren Abweichungen im Dienstverhalten und initiieren Selbstheilungsprozesse, die in das System integrierte sind. Microsoft 365 verwendet auch externe Überwachung, bei der die Überwachung von mehreren Standorten aus sowohl von vertrauenswürdigen Drittanbieterdiensten (zur unabhängigen SLA-Überprüfung) als auch von unseren eigenen Rechenzentren durchgeführt wird, um Warnungen zu auslösen. Für die Diagnose verfügen wir über umfangreiche Protokollierung, Überwachung und Ablaufverfolgung. Die detaillierte Ablaufverfolgung und Überwachung hilft uns, Probleme zu isolieren und eine schnelle und effektive Ursachenanalyse durchzuführen.

Während Microsoft 365 nach Möglichkeit automatisierte Wiederherstellungsaktionen hat, stehen Die Techniker von Microsoft rund um die Uhr zur Verfügung, um alle Sicherheitseskalationen des Schweregrads 1 zu untersuchen, und post-mortem-Überprüfungen aller Dienstvorfälle tragen zu kontinuierlichem Lernen und zur Verbesserung bei. Dieses Team umfasst Supporttechniker, Produktentwickler, Programmmanager, Produktmanager und führungskräfte. Unsere On-Call-Experten stellen eine zeitnahe Sicherung zur Verfügung und können häufig Wiederherstellungsaktionen automatisieren, sodass das nächste Mal, wenn ein Ereignis auftritt, selbstverheilt werden kann.

Microsoft führt jedes Mal, wenn ein Microsoft 365-Sicherheitsvorfall auftritt, unabhängig von der Größe der Auswirkungen eine sorgfältige Überprüfung nach dem Vorfall durch. Eine Überprüfung nach dem Vorfall besteht aus einer Analyse der Ereignisse, der Reaktionen und der Zukünftigen Verhinderung ähnlicher Vorfälle. Im Interesse der Transparenz und Rechenschaftspflicht teilen wir die Überprüfung nach einem Vorfall für wichtige Dienstvorfälle mit betroffenen Kunden. Weitere Informationen finden Sie unter [Office 365 Security Incident Management](https://aka.ms/Office365SIM).

## <a name="assume-breach-methodology"></a>Nehmen wir eine Verletzungsmethode an

Basierend auf einer detaillierten Analyse der Sicherheitstrends setzt sich Microsoft für weitere Investitionen in reaktive Sicherheitsprozesse und -technologien ein, die sich auf die Erkennung und Reaktion auf neue Bedrohungen konzentrieren, anstatt diese Bedrohungen nur zu verhindern. Aufgrund von Änderungen in der Bedrohungslandschaft und einer eingehenden Analyse hat Microsoft seine Sicherheitsstrategie über die Verhinderung von Sicherheitsverstößen hinaus auf eine besser für den Umgang mit Sicherheitsverletzungen bei deren Auftreten besser ausgestattete Strategie verfeinern können. eine Strategie, die wichtige Sicherheitsereignisse nicht als Eine Frage des Falls, sondern wann betrachtet.

Während microsofts [Annahme,](https://www.microsoft.com/TrustCenter/Security/default.aspx) dass Verstöße seit vielen Jahren in Der Praxis sind, wissen viele Kunden nicht, dass hinter den Kulissen gearbeitet wird, um die Microsoft-Cloud zu verbessern. Angenommen, Die Verletzung ist eine Einstellung, die Sicherheitsinvestitionen, Entwurfsentscheidungen und betriebliche Sicherheitspraktiken leitet. Gehen Sie davon aus, dass die Verletzung das Vertrauen in Anwendungen, Dienste, Identitäten und Netzwerke einschränkt, indem alle – intern und extern – als unsicher und bereits gefährdet behandelt werden. Obwohl die Strategie "Verletzung annehmen" nicht aus einer tatsächlichen Verletzung von Microsoft Enterprise- oder Clouddiensten erwingt wurde, wurde erkannt, dass viele Organisationen in der gesamten Branche trotz aller Versuche, sie zu verhindern, verletzt wurden. Das Verhindern von Verstößen ist zwar ein wichtiger Bestandteil der Geschäftstätigkeit einer Organisation, diese Methoden müssen jedoch kontinuierlich getestet und erweitert werden, um moderne Gegner und erweiterte dauerhafte Bedrohungen effektiv zu bekämpfen. Damit sich jede Organisation auf eine Verletzung vorbereiten kann, muss sie zunächst robuste, wiederholbare und gründlich getestete Verfahren für die Sicherheitsantwort erstellen und beibehalten.

Auch wenn Sicherheitsprozesse wie Bedrohungsmodellierung, Codeüberprüfungen und Sicherheitstests im Rahmen des Security [Development Lifecycle](https://www.microsoft.com/securityengineering/sdl/)sehr nützlich sind, bietet "Assume Breach" zahlreiche Vorteile, die zur Berücksichtigung der Gesamtsicherheit beitragen, indem reaktive Funktionen im Falle einer Verletzung trainiert und gemessen werden.

Bei Microsoft haben wir uns darauf festgelegt, dies durch laufende Übungen zum Spielen und Durchdringungstests unserer Sicherheitsreaktionspläne zu erreichen, mit dem Ziel, unsere Erkennungs- und Reaktionsfähigkeit zu verbessern. Microsoft simuliert regelmäßig reale Sicherheitsverletzungen, führt eine kontinuierliche Sicherheitsüberwachung durch und führt Sicherheitsvorfälle ein, um die Sicherheit von Microsoft 365, Azure und anderen Microsoft Cloud Services zu überprüfen und zu verbessern.

Microsoft führt seine Sicherheitsstrategie Assume Breach mithilfe von zwei Kerngruppen aus:

- Rote Teams (Angreifer)
- Blaue Teams (Verteidiger)

Sowohl Microsoft Azure- als auch Microsoft 365-Mitarbeiter trennen rote und blaue Vollzeitteams.

Der Ansatz, der als["Rotes Teaming"](https://go.microsoft.com/fwlink/?linkid=518599)bezeichnet wird, besteht im Testen von Azure- und Microsoft 365-Systemen und -Vorgängen mit denselben Taktiken, Techniken und Verfahren wie echte Gegner, ohne das Wissen der Engineering- oder Operations-Teams. Dadurch werden die Sicherheitserkennungs- und Reaktionsfunktionen von Microsoft getestet und es wird unterstützt, Produktionsrisiken, Konfigurationsfehler, ungültige Annahmen und andere Sicherheitsprobleme kontrolliert zu identifizieren. Auf jede Verletzung des roten Teams folgt eine vollständige Offenlegung zwischen beiden Teams, um Lücken zu identifizieren, Erkenntnisse zu beseitigen und die Reaktion auf Sicherheitsverletzungen zu verbessern.

**HINWEIS:** Während der Tests der roten Teaming- oder Livewebsitedurchdringung werden keine Kundendaten gezielt gezielt verwendet. Die Tests sind für die Microsoft 365- und Azure-Infrastruktur und -Plattformen sowie für die eigenen Mandanten, Anwendungen und Daten von Microsoft geeignet. Kunden mandanten, Anwendungen und Inhalte, die in Microsoft 365 oder Azure gehostet werden, sind nie zielgerichtet.

## <a name="red-teams"></a>Rote Teams

Das rote Team ist eine Gruppe von Vollzeitmitarbeitern in Microsoft, die sich auf die Verletzung der Infrastruktur, plattform von Microsoft und der eigenen Mandanten und Anwendungen von Microsoft konzentriert. Sie sind der dedizierte Angreifer (eine Gruppe von ethischen Hackern), die gezielte und dauerhafte Angriffe auf Onlinedienste (Microsoft-Infrastruktur, Plattformen und Anwendungen, aber keine Anwendungen oder Inhalte von Endbenutzern) ausführen.

Die Rolle des roten Teams besteht in der Angriffs- und Durchdrangsfunktion von Umgebungen mit denselben Schritten wie ein Gegner:

![Phasen der Verletzung](../media/office-365-isolation-breach-stages.png)

Unter anderem versuchen rote Teams, die Grenzen der Mandantenisolation zu überschreiten, um Fehler oder Lücken in unserem Isolationsentwurf zu finden.

## <a name="blue-teams"></a>Blaue Teams

Das blaue Team besteht entweder aus einer dedizierten Gruppe von Sicherheitsantwortern oder Mitgliedern aus den Organisationen für die Reaktion auf Sicherheitsvorfälle, engineering und Operations. Unabhängig von ihrem Make-up sind sie unabhängig und arbeiten getrennt vom roten Team. Das blaue Team folgt etablierten Sicherheitsprozessen und verwendet die neuesten Tools und Technologien, um Angriffe und Penetrationen zu erkennen und darauf zu reagieren. Genau wie bei realen Angriffen weiß das blaue Team nicht, wann oder wie die Angriffe des roten Teams auftreten oder welche Methoden verwendet werden können. Ihre Aufgabe ist es, alle Sicherheitsvorfälle zu erkennen und darauf zu reagieren, ob es sich um einen roten Teamangriff oder einen tatsächlichen Angriff handelt. Aus diesem Grund ist das blaue Team ständig im Abruf und muss auf Verstöße gegen rote Teams genauso reagieren wie bei jeder anderen Verletzung.

Wenn ein Gegner, z. B. ein rotes Team, eine Umgebung verletzt hat, muss das blaue Team:

- Sammeln von Nachweisen, die vom Widersacher übrig bleiben
- Erkennen der Nachweise als Anzeichen für einen Kompromiss
- Warnung der entsprechenden Engineering- und Betriebsteams
- Triage der Warnungen, um festzustellen, ob sie eine weitere Untersuchung rechtfertigen
- Erfassen des Kontexts aus der Umgebung, um die Verletzung zu erfassen
- Erstellen eines Korrekturplans, um den Widersacher zu enthalten oder zu verdingen
- Ausführen des Behebungsplans und Wiederherstellung nach Verletzung

Diese Schritte bilden die Reaktion auf Sicherheitsvorfälle, die parallel zu den Reaktionen des Widersachers ausgeführt wird, wie unten gezeigt:

![Phasen der Reaktion auf Sicherheitsverletzungen](../media/office-365-isolation-breach-response-stages.png)

Verstöße gegen rote Teams ermöglichen es dem blauen Team, End-to-End-Angriffe zu erkennen und auf diese zu reagieren. Am wichtigsten ist, dass sie eine geübte Reaktion auf Sicherheitsvorfälle vor einer echten Verletzung ermöglicht. Darüber hinaus verbessert das blaue Team aufgrund von Verletzungen des roten Teams sein situationelles Bewusstsein, das bei zukünftigen Verstößen (ob vom roten Team oder einem anderen Gegner) hilfreich sein kann. Während des gesamten Erkennungs- und Reaktionsprozesses erzeugt das blaue Team eine effektive Intelligenz und erhält Einblick in die tatsächlichen Bedingungen der Umgebung, die sie zu verteidigen versuchen. Häufig erfolgt dies über Datenanalyse und Forensik, die vom blauen Team durchgeführt werden, wenn es auf Angriffe von roten Teams reagiert und Bedrohungsindikatoren wie z. B. Gefährdungsindikatoren aufbaut. Ähnlich wie das rote Team Lücken in der Sicherheitsgeschichte identifiziert, identifizieren blaue Teams Lücken in ihrer Fähigkeit, zu erkennen und zu reagieren. Da die roten Teams reale Angriffe modellieren, kann das blaue Team darüber hinaus genau bewertet werden, ob es in der Lage ist oder nicht, mit bestimmten und dauerhaften Gegnern umgehbar zu sein. Schließlich messen Verstöße gegen das rote Team sowohl die Bereitschaft als auch die Auswirkungen unserer Verletzungsreaktion.
