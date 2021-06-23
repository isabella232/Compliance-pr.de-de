---
title: Microsoft 365 interne Protokollierung für Microsoft 365 Engineering
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
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088594"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Interne Protokollierung für Microsoft 365-Engineering

Zusätzlich zu den für Kunden verfügbaren Ereignissen und Protokolldaten unterhält Microsoft ein internes System zur Erfassung von Protokolldaten, das Microsoft 365 Technikern zur Verfügung steht. Viele verschiedene Arten von Protokolldaten werden von Microsoft 365 Servern in eine proprietäre Lösung für die Sicherheitsüberwachung für die Analyse nahezu in Echtzeit (NRT) und einen internen Big Data Computing-Dienst (Cosmos) für die langfristige Speicherung hochgeladen. Diese Datenübertragung erfolgt über eine FIPS 140-2-validierte TLS-Verbindung an genehmigten Ports und Protokollen mithilfe eines proprietären Automatisierungstools namens Office Data Loader (ODL). Die in Microsoft 365 zum Sammeln und Verarbeiten von Überwachungsdatensätzen verwendeten Tools ermöglichen keine dauerhaften oder nicht rückgängig gemachten Änderungen am ursprünglichen Inhalt des Überwachungsdatensatzes oder an der Zeitreihenfolge.

Serviceteams verwenden Cosmos als zentrales Repository, um eine Analyse der Anwendungsnutzung durchzuführen, die System- und Betriebsleistung zu messen und nach Anomalien und Mustern zu suchen, die auf Probleme oder Sicherheitsprobleme hinweisen können. Jedes Serviceteam lädt einen Basisplan hoch, der Folgendes umfasst:

- Ereignisprotokolle
- AppLocker-Protokolle
- Leistungsdaten
- System Center Daten
- Anrufdetaildatensätze
- QoE-Daten
- IIS-Webserverprotokolle
- SQL Server Protokolle
- Syslog-Daten
- Sicherheitsüberwachungsprotokolle

Vor dem Hochladen verwendet die ODL-Anwendung einen Scrubbing-Dienst, um alle Felder zu entfernen, die Kundendaten enthalten, z. B. Mandanteninformationen und Informationen zur Identifizierung von Endbenutzern, und diese Felder durch einen Hashwert zu ersetzen. Die bereinigungsprotokolle werden in Cosmos und in die NRT-Sicherheitsüberwachungslösung hochgeladen, die die Protokolle auf potenzielle Sicherheitsereignisse und Leistungsindikatoren analysiert. Der Zeitraum der Aufbewahrung von Überwachungsprotokolldaten in Cosmos wird von den Serviceteams bestimmt. Die meisten Überwachungsprotokolldaten werden 90 Tage oder länger aufbewahrt, um Untersuchungen von Sicherheitsvorfällen zu unterstützen und gesetzliche Aufbewahrungsanforderungen zu erfüllen.

Der Zugriff auf Microsoft 365 in Cosmos gespeicherten Daten ist auf autorisiertes Personal beschränkt. Microsoft schränkt die Verwaltung von Überwachungsprotokollen auf eine begrenzte Teilmenge der Sicherheitsteammitglieder ein, die für die Überwachungsfunktionen verantwortlich sind. Das Sicherheitsteam hat keinen ständigen administrativen Zugriff auf Cosmos, und alle Änderungen werden aufgezeichnet und überwacht.

Nach der NRT-Analyse kann jedes Serviceteam Analysetools und Dashboards für Datenkorrelation, interaktive Abfragen und Datenanalyse verwenden. Diese Berichte werden verwendet, um die Gesamtleistung des Diensts zu überwachen und zu verbessern.
