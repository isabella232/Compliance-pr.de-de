---
title: Übersicht über die Überwachungsprotokollierung
description: Informationen zur Überwachungsprotokollierung in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 3714a5df73253d0814e1d4067248116cb6e10a40
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507116"
---
# <a name="audit-logging-overview"></a>Übersicht über die Überwachungsprotokollierung

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Wie verwendet Microsoft 365 die Überwachungsprotokollierung?

Microsoft 365 verwendet die Überwachungsprotokollierung, um nicht autorisierte Aktivitäten in ihren Produkten und Diensten zu erkennen und die Verantwortlichkeit für Microsoft-Mitarbeiter zu gewährleisten. In Überwachungsprotokollen werden Details zu System Konfigurationsänderungen und Zugriffsereignissen erfasst, und es werden Details angegeben, wer für die Aktivität zuständig war, wann und wo die Aktivität stattfand und was das Ergebnis der Aktivität war. Die automatische Protokollanalyse unterstützt die nahe Echtzeiterkennung verdächtigen Verhaltens. Potenzielle Vorfälle werden zur weiteren Untersuchung an das Microsoft 365-Sicherheitsantwort Team eskaliert.

In der internen Überwachungsprotokollierung von Microsoft 365 werden Protokolldaten aus einer Vielzahl von Quellen erfasst, beispielsweise:

- Ereignisprotokolle
- AppLocker-Protokolle
- Leistungsdaten
- System Center-Daten
- Anruf Detaildatensätze
- Quality of Experience-Daten
- IIS-Webserverprotokolle
- SQL Server Protokolle
- Syslog-Daten
- Sicherheitsüberwachungsprotokolle

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Wie zentralisiert und meldet Microsoft 365 Überwachungsprotokolle?

Viele verschiedene Typen von Protokolldaten werden von Microsoft 365-Servern in einen internen, großen Daten Datenverarbeitungsdienst mit dem Namen Cosmos hochgeladen. Jedes Service Team lädt Überwachungsprotokolle von den jeweiligen Servern in die Cosmos-Datenbank für Aggregation und Analyse hoch. Diese Datenübertragung erfolgt über eine FIPS 140-2-validierte TLS-Verbindung an genehmigten Ports und Protokollen mithilfe eines proprietären Automatisierungstools namens Office Data Loader (ODL).

Dienst Teams führen bereichsbezogene Abfragen für Ihre Daten in Cosmos für Protokoll Korrelation, Warnungen und Berichterstellung aus. Beispielsweise verwendet das Microsoft 365-Sicherheitsteam Daten aus Cosmos mit einem proprietären Ereignisprotokoll Parser, um Protokolldaten zu korrelieren, Warnungen zu senden und umsetzbare Berichte über mögliche verdächtige Aktivitäten in der Microsoft 365-Produktionsumgebung zu generieren. Die Berichte aus diesen Daten werden verwendet, um Sicherheitsrisiken zu beheben und die Gesamtleistung des Diensts zu verbessern.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Wie schützt Microsoft 365 Überwachungsprotokolle?

Die in Microsoft 365 zum Erfassen und Verarbeiten von Überwachungsdatensätzen verwendeten Tools ermöglichen keine permanenten oder irreversiblen Änderungen am ursprünglichen Inhalt oder der Zeitreihenfolge des Überwachungseintrags. Der Zugriff auf Microsoft 365-Daten, die in Cosmos gespeichert sind, ist auf autorisiertes Personal beschränkt. Microsoft 365 schränkt die Verwaltung der Überwachungsfunktionen auf die beschränkte Teilmenge der Dienst Teammitglieder ein, die für die Überwachungsfunktionen zuständig sind. Diese Teammitglieder haben nicht die Möglichkeit, Daten aus dem Kosmos zu ändern oder zu löschen, und alle Änderungen an den Protokollierungsmechanismen für Cosmos werden aufgezeichnet und überwacht. Überwachungsprotokolle werden lang genug aufbewahrt, um Vorfall Untersuchungen zu unterstützen und behördliche Anforderungen zu erfüllen. Der genaue Zeitraum der Aufbewahrung von Überwachungsprotokolldaten in Cosmos wird von den Service Teams bestimmt. die meisten Überwachungsprotokolldaten werden für 90 Tage oder länger aufbewahrt.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Wie schützt Microsoft 365 benutzerbezogene Informationen, die in Überwachungsprotokollen erfasst werden können?

Vor dem Hochladen von Daten in Cosmos verwendet die ODL-Anwendung einen Scrubbing-Dienst, um alle Felder zu verbergen, die Kundendaten enthalten, beispielsweise Mandanteninformationen und benutzerbezogene Informationen, und diese Felder durch einen Hashwert ersetzen. Die anonymisierten und gehashten Protokolle werden umgeschrieben und dann in Cosmos hochgeladen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Verordnungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Bestimmungen und Zertifizierungen überprüft. Informationen zur Validierung von Steuerelementen im Zusammenhang mit der Überwachungsprotokollierung erhalten Sie in der folgenden Tabelle.

| **Externe Überprüfungen** | **Section** | **Letztes Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | Au-2: Überwachungsereignisse <br> Au-3: Inhalt der Überwachungsdatensätze <br> Au-4: Überwachen der Speicherkapazität <br> AU-5: Antwort auf Fehler bei der Überwachungs Verarbeitung <br> Au-6: Überwachungsüberprüfung, Analyse und Berichterstellung <br> AU-7: Überwachungs Reduzierung und Berichtsgenerierung <br> AU-8: Zeitstempel <br> Au-9: Schutz von Überwachungsinformationen  <br> Au-10: nicht-Ablehnung <br> AU-11: Aufbewahrung von Überwachungsdatensätzen <br> AU-12: Überwachungs Generierung  | 24. September 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.4: Protokollierung und Überwachung | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.4: Protokollierung und Überwachung | Februar 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48: Datencenter Protokollierung <br> CA-60: Überwachungsprotokollierung | 30. September 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48: Datencenter Protokollierung <br> CA-60: Überwachungsprotokollierung | 30. September 2019 |