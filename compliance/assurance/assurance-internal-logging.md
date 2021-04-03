---
title: Interne Microsoft 365-Protokollierung für Microsoft 365 Engineering
description: In diesem Artikel finden Sie eine Erläuterung der Funktionsweise der internen Protokollierung für Microsoft 365 Engineering-Teams.
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
ms.openlocfilehash: 110a61c27a00380eede4d4f2303acfb025a27a1f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497075"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Interne Protokollierung für Microsoft 365-Engineering

Zusätzlich zu den für Kunden verfügbaren Ereignissen und Protokolldaten gibt es auch ein internes Protokolldatenerfassungssystem, das microsoft 365-Technikern bei Microsoft zur Verfügung steht. Viele verschiedene Arten von Protokolldaten werden von Microsoft 365-Servern auf einen internen Big Data Computing-Dienst namens Cosmos hochgeladen. Jedes Dienstteam lädt Überwachungsprotokolle von ihren jeweiligen Servern zur Aggregation und Analyse in die Cosmos-Datenbank hoch. Diese Datenübertragung erfolgt über eine FIPS 140-2-validierte TLS-Verbindung an speziell genehmigten Ports und Protokollen mithilfe eines proprietären Automatisierungstools namens Office Data Loader (ODL). Die tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.

Serviceteams verwenden Cosmos als zentrales Repository, um eine Analyse der Anwendungsverwendung durchzuführen, die System- und Betriebsleistung zu messen und nach Anomalien und Mustern zu suchen, die auf Probleme oder Sicherheitsprobleme hinweisen können. Jedes Dienstteam lädt eine Basis für Protokolle in Cosmos hoch, je nachdem, was sie analysieren möchten, die häufig Folgendes umfasst:

- Ereignisprotokolle
- AppLocker-Protokolle
- Leistungsdaten
- System Center-Daten
- Anrufdetaildatensätze
- Qualität der Erfahrungsdaten
- IIS-Webserverprotokolle
- SQL Server Protokolle
- Syslog-Daten
- Sicherheits-Überwachungsprotokolle

Vor dem Hochladen von Daten in Cosmos verwendet die #A0 einen Scrubbingdienst, um alle Felder zu verschleiern, die Kundendaten enthalten, z. B. Mandanteninformationen und benutzeridentifizierbare Informationen, und diese Felder durch einen Hashwert zu ersetzen. Die anonymisierten Und Hashprotokolle werden umgeschrieben und dann in Cosmos hochgeladen. Dienstteams führen Bereichsabfragen für ihre Daten in Cosmos zur Korrelation, Warnung und Berichterstellung aus. Der Zeitraum der Aufbewahrung von Überwachungsprotokolldaten in Cosmos wird von den Dienstteams bestimmt. Die meisten Überwachungsprotokolldaten werden für 90 Tage oder länger aufbewahrt, um Untersuchungen zu Sicherheitsvorfällen zu unterstützen und gesetzliche Aufbewahrungsanforderungen zu erfüllen.

Der Zugriff auf in Cosmos gespeicherte Microsoft 365-Daten ist auf autorisierte Mitarbeiter beschränkt. Microsoft beschränkt die Verwaltung der Überwachungsfunktionalität auf die begrenzte Untermenge von Dienstteammitgliedern, die für die Überwachungsfunktionalität verantwortlich sind. Diese Teammitglieder haben nicht die Möglichkeit, Daten aus Cosmos zu ändern oder zu löschen, und alle Änderungen an Protokollierungsmechanismen für Cosmos werden aufgezeichnet und überwacht.

Jedes Dienstteam stürzt sich zur Analyse auf seine Protokolldaten, indem es bestimmte Anwendungen zur Durchführung bestimmter Analysen autorisiert. Beispielsweise verwendet das Microsoft 365-Sicherheitsteam Daten von Cosmos über einen proprietären Ereignisprotokollparser, um Berichte zu möglichen verdächtigen Aktivitäten in der Microsoft 365-Produktionsumgebung zu korrelieren, zu warnen und zu generieren. Die Berichte aus diesen Daten werden verwendet, um Sicherheitsrisiken zu beheben und die Gesamtleistung des Diensts zu verbessern. Wenn eine bestimmte Warnung oder ein bestimmter Bericht eine weitere Untersuchung erfordert, können Servicemitarbeiter anfordern, dass Daten wieder in den Microsoft 365-Dienst importiert werden. Da das spezifische Protokoll, das aus Cosmos importiert wird, verschlüsselt ist und das Dienstpersonal keinen Zugriff auf Entschlüsselungsschlüssel hat, wird das Zielprotokoll programmgesteuert über einen Entschlüsselungsdienst übergeben, der bereichsspezifische Ergebnisse an das autorisierte Dienstpersonal zurückgibt. Alle in dieser Übung gefundenen Sicherheitsrisiken werden mithilfe der standardmäßigen Sicherheitsvorfallverwaltungskanäle von Microsoft gemeldet und eskaliert.
