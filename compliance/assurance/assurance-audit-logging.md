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
ms.openlocfilehash: e6bf564f182f2dfabc6561602e5a4cb5c8c3445e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088687"
---
# <a name="audit-logging-overview"></a>Überwachungsprotokollierung (Übersicht)

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Wie verwendet Microsoft 365 die Überwachungsprotokollierung?

Microsoft 365 verwendet die Überwachungsprotokollierung, um nicht autorisierte Aktivitäten in seinen Produkten und Diensten zu erkennen und die Verantwortlichkeit für Microsoft-Mitarbeiter zu gewährleisten. Überwachungsprotokolle erfassen Details zu Systemkonfigurationsänderungen und Zugriffsereignissen mit Details, um zu identifizieren, wer für die Aktivität verantwortlich war, wann und wo die Aktivität stattgefunden hat und was das Ergebnis der Aktivität war. Die automatische Protokollanalyse unterstützt nahezu in Echtzeit die Erkennung verdächtigen Verhaltens. Potenzielle Vorfälle werden zur weiteren Untersuchung an das Microsoft 365 Security Response-Team eskaliert.

Microsoft 365 interne Überwachungsprotokollierung erfasst Protokolldaten aus verschiedenen Quellen, z. B.:

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

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Wie wird Microsoft 365 zentralisiert und über Überwachungsprotokolle berichtet?

Viele verschiedene Arten von Protokolldaten werden von Microsoft 365 Servern in eine proprietäre Sicherheitsüberwachungslösung für die Analyse nahezu in Echtzeit (NRT) und einen internen Big Data Computing-Dienst (Cosmos) für die langfristige Speicherung hochgeladen. Diese Datenübertragung erfolgt über eine FIPS 140-2-validierte TLS-Verbindung an genehmigten Ports und Protokollen mithilfe eines proprietären Automatisierungstools namens Office Data Loader (ODL).

Protokolle werden in NRT mithilfe regelbasierter, statistischer und maschineller Lernmethoden verarbeitet, um Systemleistungsindikatoren und potenzielle Sicherheitsereignisse zu erkennen. Machine Learning-Modelle verwenden eingehende Protokolldaten und Verlaufsprotokolldaten, die in Cosmos gespeichert sind, um die Erkennungsfunktionen kontinuierlich zu verbessern. Sicherheitsrelevante Erkennungen generieren Warnungen, benachrichtigen Bereitschaftstechniker über einen potenziellen Vorfall und lösen ggf. automatisierte Abhilfemaßnahmen aus. Zusätzlich zur automatisierten Sicherheitsüberwachung verwenden Serviceteams Analysetools und Dashboards für Datenkorrelation, interaktive Abfragen und Datenanalyse. Diese Berichte werden verwendet, um die Gesamtleistung des Diensts zu überwachen und zu verbessern.

Weitere Informationen zur Sicherheitsüberwachung und -warnung finden Sie in der Übersicht über die [Sicherheitsüberwachung.](assurance-security-monitoring.md)

![Überwachen des Datenflusses](../media/assurance-audit-data-flow.png)

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Wie schützt Microsoft 365 Überwachungsprotokolle?

Die in Microsoft 365 zum Sammeln und Verarbeiten von Überwachungsdatensätzen verwendeten Tools ermöglichen keine dauerhaften oder nicht rückgängig gemachten Änderungen am ursprünglichen Inhalt des Überwachungsdatensatzes oder an der Zeitreihenfolge. Der Zugriff auf Microsoft 365 in Cosmos gespeicherten Daten ist auf autorisiertes Personal beschränkt. Darüber hinaus beschränkt Microsoft 365 die Verwaltung von Überwachungsprotokollen auf eine begrenzte Teilmenge der Sicherheitsteammitglieder, die für die Überwachungsfunktionen verantwortlich sind. Das Sicherheitsteam hat keinen ständigen administrativen Zugriff auf Cosmos. Für den Administrativen Zugriff ist die Genehmigung des JIT-Zugriffs (Just-In-Time) erforderlich, und alle Änderungen an Protokollierungsmechanismen für Cosmos werden aufgezeichnet und überwacht. Überwachungsprotokolle werden lange genug aufbewahrt, um Vorfalluntersuchungen zu unterstützen und behördliche Anforderungen zu erfüllen. Der genaue Zeitraum der Aufbewahrung von Überwachungsprotokolldaten in Cosmos wird von den Serviceteams bestimmt. die meisten Überwachungsprotokolldaten werden 90 Tage oder länger aufbewahrt.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Wie schützt Microsoft 365 identifizierbare Endbenutzerinformationen, die möglicherweise in Überwachungsprotokollen erfasst werden?

Vor dem Hochladen von Protokolldaten verwendet die ODL-Anwendung einen Scrubbing-Dienst, um alle Felder zu entfernen, die Kundendaten enthalten, z. B. Mandanteninformationen und Endbenutzerinformationen, und diese Felder durch einen Hashwert zu ersetzen. Die anonymisierten und gehashten Protokolle werden umgeschrieben und dann in Cosmos hochgeladen. Alle Protokollübertragungen erfolgen über eine TLS-verschlüsselte Verbindung (FIPS 140-2).

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. Die Überprüfung von Steuerelementen im Zusammenhang mit der Überwachungsprotokollierung finden Sie in der folgenden Tabelle.

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: Überwachungsereignisse <br> AU-3: Inhalt von Überwachungsdatensätzen <br> AU-4: Überwachen der Speicherkapazität <br> AU-5: Reaktion auf Verarbeitungsfehler bei der Überwachung <br> AU-6: Prüfung, Analyse und Berichterstellung <br> AU-7: Audit-Reduzierung und Berichterstellung <br> AU-8: Zeitstempel <br> AU-9: Schutz von Überwachungsinformationen  <br> AU-10: Nichtabstreitbarkeit <br> AU-11: Aufbewahrung von Überwachungsdatensatz <br> AU-12: Überwachung der Generierung  | 24. September 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Protokollierung und Überwachung | 20. April 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Protokollierung und Überwachung | 20. April 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Rechenzentrumsprotokollierung <br> CA-60: Überwachungsprotokollierung | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Rechenzentrumsprotokollierung <br> CA-60: Überwachungsprotokollierung | 24. Dezember 2020|