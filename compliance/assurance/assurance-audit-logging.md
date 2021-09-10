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
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 11695a941e5d5e6740833ab19bf2d68ac487c1c5
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947045"
---
# <a name="audit-logging-overview"></a>Überwachungsprotokollierung (Übersicht)

## <a name="how-do-microsoft-online-services-employ-audit-logging"></a>Wie verwenden Microsoft-Onlinedienste die Überwachungsprotokollierung?

Microsoft-Onlinedienste verwenden die Überwachungsprotokollierung, um nicht autorisierte Aktivitäten zu erkennen und die Verantwortlichkeit für Microsoft-Mitarbeiter zu gewährleisten. Überwachungsprotokolle erfassen Details zu Systemkonfigurationsänderungen und Zugriffsereignissen mit Details, um zu ermitteln, wer für die Aktivität verantwortlich war, wann und wo die Aktivität stattgefunden hat und was das Ergebnis der Aktivität war. Die automatische Protokollanalyse unterstützt nahezu in Echtzeit die Erkennung verdächtigen Verhaltens. Potenzielle Vorfälle werden zur weiteren Untersuchung an das entsprechende Microsoft-Sicherheitsteam eskaliert.

Die interne Überwachungsprotokollierung von Microsoft Online Services erfasst Protokolldaten aus verschiedenen Quellen, z. B.:

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

## <a name="how-do-microsoft-online-services-centralize-and-report-on-audit-logs"></a>Wie zentralisieren und berichten Microsoft-Onlinedienste über Überwachungsprotokolle?

Viele verschiedene Arten von Protokolldaten werden von Microsoft-Servern in eine proprietäre Sicherheitsüberwachungslösung für die Analyse in nahezu Echtzeit (NRT) und einen internen Big Data Computing-Dienst (Cosmos) oder Azure Data Explorer (Kusto) für die langfristige Speicherung hochgeladen. Diese Datenübertragung erfolgt über eine FIPS 140-2-validierte TLS-Verbindung an genehmigten Ports und Protokollen mithilfe automatisierter Protokollverwaltungstools.

Protokolle werden in NRT mithilfe regelbasierter, statistischer und maschineller Lernmethoden verarbeitet, um Systemleistungsindikatoren und potenzielle Sicherheitsereignisse zu erkennen. Machine Learning-Modelle verwenden eingehende Protokolldaten und Verlaufsprotokolldaten, die in Cosmos oder Kusto gespeichert sind, um die Erkennungsfunktionen kontinuierlich zu verbessern. Sicherheitsrelevante Erkennungen generieren Warnungen, benachrichtigen Bereitschaftstechniker über einen potenziellen Vorfall und lösen ggf. automatisierte Abhilfemaßnahmen aus. Zusätzlich zur automatisierten Sicherheitsüberwachung verwenden Serviceteams Analysetools und Dashboards für Datenkorrelation, interaktive Abfragen und Datenanalyse. Diese Berichte werden verwendet, um die Gesamtleistung des Diensts zu überwachen und zu verbessern.

Weitere Informationen zur Sicherheitsüberwachung und -warnung finden Sie in der Übersicht über die [Sicherheitsüberwachung.](assurance-security-monitoring.md)

![Überwachen des Datenflusses.](../media/assurance-audit-data-flow.png)

## <a name="how-do-microsoft-online-services-protect-audit-logs"></a>Wie schützen Microsoft-Onlinedienste Überwachungsprotokolle?

Die Tools, die in Microsoft-Onlinediensten zum Sammeln und Verarbeiten von Überwachungsdatensätzen verwendet werden, lassen keine dauerhaften oder nicht rückgängig gemachten Änderungen am ursprünglichen Inhalt des Überwachungsdatensatzes oder an der Zeitreihenfolge zu. Der Zugriff auf Microsoft-Onlinedienstdaten, die in Cosmos oder Kusto gespeichert sind, ist auf autorisiertes Personal beschränkt. Darüber hinaus beschränkt Microsoft die Verwaltung von Überwachungsprotokollen auf eine begrenzte Teilmenge von Sicherheitsteammitgliedern, die für die Überwachungsfunktionen verantwortlich sind. Mitarbeiter des Sicherheitsteams haben keinen ständigen administrativen Zugriff auf Cosmos oder Kusto. Für den administrativen Zugriff ist die Genehmigung des JIT-Zugriffs (Just-In-Time) erforderlich, und alle Änderungen an Protokollierungsmechanismen für Cosmos werden aufgezeichnet und überwacht. Überwachungsprotokolle werden lange genug aufbewahrt, um Vorfalluntersuchungen zu unterstützen und behördliche Anforderungen zu erfüllen. Der genaue Zeitraum der Aufbewahrung von Überwachungsprotokolldaten, der von den Serviceteams bestimmt wird; Die meisten Überwachungsprotokolldaten werden 90 Tage in Cosmos und 180 Tage in Kusto aufbewahrt.

## <a name="how-do-microsoft-online-services-protect-user-personal-data-that-may-be-captured-in-audit-logs"></a>Wie schützen Microsoft-Onlinedienste personenbezogene Daten von Benutzern, die möglicherweise in Überwachungsprotokollen erfasst werden?

Vor dem Hochladen von Protokolldaten verwendet eine automatisierte Protokollverwaltungsanwendung einen Scrubbing-Dienst, um alle Felder zu entfernen, die Kundendaten enthalten, z. B. Mandanteninformationen und persönliche Benutzerdaten, und diese Felder durch einen Hashwert zu ersetzen. Die anonymisierten und gehashten Protokolle werden umgeschrieben und dann in Cosmos hochgeladen. Alle Protokollübertragungen erfolgen über eine TLS-verschlüsselte Verbindung (FIPS 140-2).

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. Die Überprüfung von Steuerelementen im Zusammenhang mit der Überwachungsprotokollierung finden Sie in der folgenden Tabelle.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Protokollierung und Überwachung | 2. Dezember 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Protokollierung und Überwachung | 2. Dezember 2020 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Protokollierung und Überwachung | 2. Dezember 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1: Protokollierung und Sammlung von Sicherheitsereignissen | 31. März 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | C5-6: Eingeschränkter Zugriff auf Protokolle <br> VM-1: Protokollierung und Sammlung von Sicherheitsereignissen | 31. März 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AU-2: Überwachungsereignisse <br> AU-3: Inhalt von Überwachungsdatensätzen <br> AU-4: Überwachen der Speicherkapazität <br> AU-5: Reaktion auf Verarbeitungsfehler bei der Überwachung <br> AU-6: Prüfung, Analyse und Berichterstellung <br> AU-7: Audit-Reduzierung und Berichterstellung <br> AU-8: Zeitstempel <br> AU-9: Schutz von Überwachungsinformationen  <br> AU-10: Nichtabstreitbarkeit <br> AU-11: Aufbewahrung von Überwachungsdatensatz <br> AU-12: Überwachung der Generierung  | 24. September 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Protokollierung und Überwachung | 20. April 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Rechenzentrumsprotokollierung <br> CA-60: Überwachungsprotokollierung | 24. Dezember 2020 |