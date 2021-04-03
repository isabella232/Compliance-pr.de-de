---
title: Überwachungsprotokollierung (Übersicht)
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
hideEdit: true
ms.openlocfilehash: dc56d0413811d59309c974931e1fa50ee184e94a
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497681"
---
# <a name="audit-logging-overview"></a>Überwachungsprotokollierung (Übersicht)

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Wie verwendet Microsoft 365 die Überwachungsprotokollierung?

Microsoft 365 verwendet die Überwachungsprotokollierung, um nicht autorisierte Aktivitäten in seinen Produkten und Diensten zu erkennen und rechenschaftsberechtigte Mitarbeiter von Microsoft zu unterstützen. Überwachungsprotokolle erfassen Details zu Systemkonfigurationsänderungen und Zugriffsereignissen, mit Details, um zu ermitteln, wer für die Aktivität verantwortlich war, wann und wo die Aktivität stattgefunden hat und was das Ergebnis der Aktivität war. Die automatisierte Protokollanalyse unterstützt die nahezu echtzeitnahe Erkennung verdächtigen Verhaltens. Mögliche Vorfälle werden zur weiteren Untersuchung an das Microsoft 365 Security Response-Team eskaliert.

Die interne Überwachungsprotokollierung von Microsoft 365 erfasst Protokolldaten aus einer Vielzahl von Quellen, z. B.:

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

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Wie zentralisiert Microsoft 365 Überwachungsprotokolle und meldet diese?

Viele verschiedene Arten von Protokolldaten werden von Microsoft 365-Servern auf einen internen Big Data Computing-Dienst namens Cosmos hochgeladen. Jedes Dienstteam lädt Überwachungsprotokolle von ihren jeweiligen Servern zur Aggregation und Analyse in die Cosmos-Datenbank hoch. Diese Datenübertragung erfolgt über eine FIPS 140-2-validierte TLS-Verbindung an genehmigten Ports und Protokollen mithilfe eines proprietären Automatisierungstools namens Office Data Loader (ODL).

Dienstteams führen Bereichsabfragen für ihre Daten in Cosmos zur Protokollkorrelation, Warnung und Berichterstellung aus. Beispielsweise verwendet das Microsoft 365-Sicherheitsteam Daten aus Cosmos mit einem proprietären Ereignisprotokollparser, um Protokolldaten zu korrelieren, Warnungen zu senden und Berichte mit Aktionen zu möglichen verdächtigen Aktivitäten in der Microsoft 365-Produktionsumgebung zu generieren. Die Berichte aus diesen Daten werden verwendet, um Sicherheitsrisiken zu beheben und die Gesamtleistung des Diensts zu verbessern.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Wie schützt Microsoft 365 Überwachungsprotokolle?

Die tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering. Der Zugriff auf in Cosmos gespeicherte Microsoft 365-Daten ist auf autorisierte Mitarbeiter beschränkt. Microsoft 365 beschränkt die Verwaltung der Überwachungsfunktionalität auf die begrenzte Teilmenge der Dienstteammitglieder, die für die Überwachungsfunktionalität verantwortlich sind. Diese Teammitglieder haben nicht die Möglichkeit, Daten aus Cosmos zu ändern oder zu löschen, und alle Änderungen an Protokollierungsmechanismen für Cosmos werden aufgezeichnet und überwacht. Überwachungsprotokolle werden lange genug aufbewahrt, um Vorfalluntersuchungen zu unterstützen und gesetzliche Anforderungen zu erfüllen. Der genaue Zeitraum der Aufbewahrung von Überwachungsprotokolldaten in Cosmos wird von den Dienstteams bestimmt. Die meisten Überwachungsprotokolldaten werden 90 Tage oder länger aufbewahrt.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Wie schützt Microsoft 365 identifizierbare Endbenutzerinformationen, die in Überwachungsprotokollen erfasst werden können?

Vor dem Hochladen von Daten in Cosmos verwendet die #A0 einen Scrubbingdienst, um alle Felder zu verschleiern, die Kundendaten enthalten, z. B. Mandanteninformationen und benutzeridentifizierbare Informationen, und diese Felder durch einen Hashwert zu ersetzen. Die anonymisierten Und Hashprotokolle werden umgeschrieben und dann in Cosmos hochgeladen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Überwachungsprotokollierung.

| **Externe Prüfungen** | **Section** | **Datum des letzten Berichts** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: Überwachungsereignisse <br> AU-3: Inhalt von Überwachungsdatensätzen <br> AU-4: Überwachen der Speicherkapazität <br> AU-5: Reaktion auf Fehler bei der Überwachung der Verarbeitung <br> AU-6: Überprüfung, Analyse und Berichterstellung <br> AU-7: Reduzierung der Überwachung und Generierung von Berichten <br> AU-8: Zeitstempel <br> AU-9: Schutz von Überwachungsinformationen  <br> AU-10: Nicht-Ablehnung <br> AU-11: Aufbewahrung von Überwachungsdatensatz <br> AU-12: Überwachungsgenerierung  | 24. September 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Protokollierung und Überwachung | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Statement of Applicability](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Protokollierung und Überwachung | Februar 22, 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Datencenterprotokollierung <br> CA-60: Überwachungsprotokollierung | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Datencenterprotokollierung <br> CA-60: Überwachungsprotokollierung | 24. Dezember 2020|