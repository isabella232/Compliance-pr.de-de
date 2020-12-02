---
title: Anträge betroffener Personen zum Datenauftragsverarbeiterdienst für Windows Enterprise im Rahmen der DSGVO und des CCPA
description: Erlernen Sie die Verwendung von Microsoft-Produkten, -Diensten und -Verwaltungstools, um nach personenbezogenen Daten zu suchen und auf DSRs zu reagieren.
keywords: Microsoft 365, Microsoft 365 Education, Microsoft 365-Dokumentation, DSGVO
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: daniha
author: DaniHalfin
manager: dansimp
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
ms.openlocfilehash: 196796cbbfe7755f2639ed5acc163cce130d98d8
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507051"
---
# <a name="data-processor-service-for-windows-enterprise-data-subject-requests-for-the-gdpr-and-ccpa"></a>Anträge betroffener Personen zum Datenauftragsverarbeiterdienst für Windows Enterprise im Rahmen der DSGVO und des CCPA 

>[!NOTE]
>Dieser Artikel richtet sich an Teilnehmer am Vorschauprogramm „Datenauftragsverarbeiterdienst für Windows Enterprise“ und setzt die Zustimmung zu bestimmten Nutzungsbedingungen voraus. Wenn Sie mehr über das Programm erfahren und den Nutzungsbedingungen zustimmen möchten, wechseln Sie zu [https://aka.ms/WindowsEnterprisePublicPreview](https://aka.ms/WindowsEnterprisePublicPreview).

## <a name="introduction-to-data-subject-requests-dsrs"></a>Einführung in Anträge betroffener Personen 

Die europäische Datenschutz-Grundverordnung (DSGVO) gewährt Personen (die in den Bestimmungen als _betroffene Personen_ bezeichnet werden) Berechtigungen zum Verwalten der personenbezogenen Daten, die von einem Arbeitgeber oder von einer anderen Art von Behörde oder Organisation (als _Datenverantwortlicher_ oder nur _Verantwortlicher_ bezeichnet) erfasst werden. Personenbezogene Daten werden in der DSGVO allgemein als alle Daten definiert, die sich auf eine identifizierte oder identifizierbare natürliche Person beziehen. Die DSGVO erteilt betroffenen Personen bestimmte Rechte für ihre personenbezogenen Daten; dazu gehören das Kopieren der personenbezogenen Daten, das Anfordern von Korrekturen, das Einschränken der Verarbeitung, das Löschen oder das Erhalten in einem elektronischen Format, damit sie zu einem anderen Datenverantwortlichen bewegt werden können. Ein formaler Antrag einer betroffenen Person an einen Datenverantwortlichen im Hinblick auf eine bestimmte Aktion für deren persönliche Daten wird als _Antrag einer betroffenen Person_ bezeichnet. 

In ähnlicher Weise sieht der California Consumer Privacy Act (CCPA) Datenschutzrechte und -pflichten für kalifornische Verbraucher vor, einschließlich der Rechte, die den Rechten der betroffenen Person der DSGVO ähneln, wie beispielsweise das Recht, ihre persönlichen Daten zu löschen, darauf zuzugreifen und sie zu empfangen (Portabilität). Die CCPA sieht auch bestimmte Offenlegungen, Schutz vor Diskriminierung bei der Wahl von Ausübungsrechten und Deaktivierungs-/Aktivierungsanforderungen für bestimmte Datenübertragungen vor, die als „Verkäufe“ klassifiziert sind. Verkäufe werden allgemein so definiert, dass sie den Austausch von Daten für einen Wertgegenstand umfassen. Weitere Informationen zum CCPA finden Sie im [California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/offering-ccpa) und in den [häufig gestellten Fragen zum California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/ccpa-faq).

In diesem Leitfaden wird erläutert, wie Microsoft-Produkte, -Dienste und -Verwaltungstools verwendet werden können, um als Reaktion auf Anträge betroffener Personen unseren als Datenverantwortliche handelnden Kunden dabei zu helfen, personenbezogene Daten zu finden und auf diese zu reagieren. Dies umfasst das Suchen, den Zugriff und die Reaktion auf personenbezogene Daten, die in der Microsoft-Cloud gespeichert sind. Im Folgenden finden Sie eine kurze Übersicht der in diesem Leitfaden beschriebenen Prozesse: 

1. **Zugriff** – rufen Sie personenbezogene Daten ab, die sich in der Microsoft-Cloud befinden, und erstellen Sie eine Kopie, die der betroffenen Person zur Verfügung gestellt werden kann, sofern dies beantragt wurde. 
2. **Löschung** – entfernen Sie personenbezogene Daten, die sich in der Microsoft-Cloud befinden, dauerhaft. 
3. **Export** – Stellen Sie der betroffenen Person eine elektronische Kopie (in einem maschinenlesbaren Format) personenbezogener Daten zur Verfügung. Personenbezogene Daten im Rahmen des CCPA sind alle Informationen, die sich auf eine identifizierte oder identifizierbare Person beziehen.

Personenbezogene Daten im Rahmen des CCPA sind alle Informationen, die sich auf eine identifizierte oder identifizierbare Person beziehen. Es gibt keinen Unterschied zwischen den privaten, öffentlichen oder beruflichen Rollen einer Person. Der definierte Begriff „personenbezogene Informationen“ stimmt in etwa mit „personenbezogenen Daten“ unter DSGVO überein. Die CCPA enthält jedoch auch Familien- und Haushaltsdaten. Weitere Informationen zum CCPA finden Sie im [California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/offering-ccpa) und in den [häufig gestellten Fragen zum California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/ccpa-faq).

In jedem Abschnitt dieses Leitfadens werden die Prozesse beschrieben, die ein als Datenverantwortlicher handelndes Unternehmen nutzen kann, um auf einen Antrag einer betroffenen Person bezüglich ihrer personenbezogenen Daten in der Microsoft-Cloud zu reagieren. 

## <a name="terminology"></a>Begrifflichkeiten

In der nachfolgenden Liste finden Sie Definitionen von Begriffen, die für diesen Leitfaden relevant sind. 

* _Datenverantwortlicher:_ Eine natürliche oder juristische Person, öffentliche Behörde, Agentur oder andere Stelle, die allein oder gemeinsam mit anderen die Zwecke und Mittel der Verarbeitung personenbezogener Daten bestimmt. Sofern die Zwecke und Mittel der Verarbeitung durch das Recht der Union oder der Mitgliedstaaten bestimmt werden, können der Datenverantwortliche bzw. die spezifischen Kriterien für dessen Benennung durch das Recht der Union oder des Mitgliedstaats angegeben werden. 

* _Personenbezogene Daten und betroffene Person:_ Alle Informationen über eine identifizierte oder identifizierbare natürliche Person („betroffene Person“). Eine identifizierbare natürliche Person ist eine Person, die direkt oder indirekt, insbesondere durch Zuordnung zu einer Kennung wie einem Namen, zu einer Kennnummer, zu Standortdaten, zu einer Online-Kennung oder zu einem oder mehreren besonderen Merkmalen identifiziert werden kann, die Ausdruck der physischen, physiologischen, genetischen, psychischen, wirtschaftlichen, kulturellen oder sozialen Identität dieser natürlichen Person sind. 

* _Auftragsverarbeiter:_ Eine natürliche oder juristische Person, Behörde, Einrichtung oder andere Stelle, welche personenbezogene Daten im Auftrag des Datenverantwortlichen verarbeitet. 

* _Kundendaten_: Alle Daten, einschließlich aller Text-, Sound-, Video- oder Bilddateien, die Microsoft vom Kunden oder im Auftrag des Kunden durch Nutzung von Enterprise-Diensten bereitgestellt werden. 

* _Windows-Diagnosedaten_ – Wichtige technische Daten von Windows-Geräten zum Gerät und zur Leistung von Windows und verwandter Software. Sie werden verwendet, um Windows auf dem neuesten Stand, sicher, zuverlässig und leistungsfähig zu halten und Windows durch die aggregierte Analyse der Verwendung von Windows zu verbessern. Einige Beispiele für Windows-Diagnosedaten sind die Art der verwendeten Hardware, die mit ihrer jeweiligen Verwendung installierten Anwendungen und Informationen zur Zuverlässigkeit der Gerätetreiber. Einige Windows-Komponenten und -Apps stellen eine direkte Verbindung zu Microsoft-Diensten her, aber die Daten, die sie austauschen, sind keine Windows-Diagnosedaten. Das Austauschen des Standorts eines Benutzers gegen lokales Wetter oder Nachrichten ist beispielsweise kein Beispiel für Windows-Diagnosedaten. 

## <a name="how-to-use-this-guide"></a>Verwenden dieses Leitfadens 

Bei Verwendung von Geräten, die beim Datenauftragsverarbeiterdienst für Windows Enterprise registriert sind, generiert Windows einige Informationen, die als „Windows-Diagnosedaten“ bezeichnet werden, um den Dienst bereitzustellen.

## <a name="windows-diagnostic-data"></a>Windows-Diagnosedaten 

Microsoft bietet Ihnen die Möglichkeit, auf Windows-Diagnosedaten, die mit der Nutzung des Datenauftragsverarbeiterdiensts für Windows Enterprise durch den Benutzer in Verbindung stehen, zuzugreifen, sie zu löschen und zu exportieren.

>[!IMPORTANT]
>Die Möglichkeit, Windows-Diagnosedaten zu korrigieren, wird nicht unterstützt. Windows-Diagnosedaten stellen tatsächliche Aktionen dar, die innerhalb von Windows durchgeführt wurden, und Änderungen an diesen Daten würden die historische Erfassung von Aktionen kompromittieren und das Sicherheitsrisiko erhöhen sowie die Zuverlässigkeit beschädigen. Alle in diesem Dokument behandelten Daten gelten als Windows-Diagnosedaten. 

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>Ausführen von DSRs an Windows-Diagnosedaten 

Microsoft bietet die Möglichkeit, auf bestimmte Windows-Diagnosedaten über das Azure-Portal und auch direkt über bereits vorhandene Anwendungsprogrammierschnittstellen (APIs) zuzugreifen, diese zu löschen und zu exportieren.

### <a name="step-1-access"></a>Schritt 1: Zugriff 

Der Mandantenadministrator ist die einzige Person in Ihrem Unternehmen, die auf Windows-Diagnosedaten zugreifen kann, die mit der Verwendung eines Datenverarbeitungsdienstes durch einen bestimmten Benutzer für ein in Windows Enterprise registriertes Gerät verbunden sind. Die für eine Zugriffsanforderung abgerufenen Daten werden über den Export in einem maschinenlesbaren Format bereitgestellt und in Dateien bereitgestellt, mit denen der Benutzer erkennen kann, welchen Geräten und Diensten die Daten zugeordnet sind. Wie bereits erwähnt, enthalten die abgerufenen Daten keine Daten, die die Sicherheit oder Stabilität des Windows-Geräts beeinträchtigen könnten. 

Microsoft bietet ein Portal-Erlebnis, das dem Mandantenadministrator des Unternehmenskunden die Möglichkeit bietet, DSR-Zugriffsanforderungen zu verwalten. [Azure DSR, Teil 2, Schritt 3: Exportieren](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), beschreibt, wie eine DSR-Zugriffsanforderung über den Export über das Azure-Portal ausgeführt wird.

### <a name="step-2-delete"></a>Schritt 2: Löschung 

Microsoft bietet eine Möglichkeit zum Ausführen benutzerbasierter DSR-Löschungsanträge, basierend auf dem Azure Active Directory-Objekt eines bestimmten Benutzers.

Für benutzerbasierte Löschanträge bietet Microsoft eine Portalerfahrung, die dem Mandantenadministrator des Unternehmenskunden die Möglichkeit bietet, DSR-Löschungsanträge zu verwalten. [Azure DSR, Teil 1, Schritt 5: Löschen](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete), beschreibt, wie ein DSR-Löschantrag über das Azure-Portal ausgeführt wird. 

Microsoft bietet die Möglichkeit, Benutzer direkt über eine bereits vorhandene Anwendungsprogrammierschnittstelle (API) zu löschen, wodurch wiederum Kundendaten gelöscht werden. Details sind in der [API-Referenzdokumentation beschrieben](https://docs.microsoft.com/graph/api/directory-deleteditems-delete). 

>[!IMPORTANT]  
>Das Löschen der gesammelten Daten stoppt die weitere Sammlung nicht. Befolgen Sie zum Deaktivieren der Datenerfassung das in der [Referenzdokumentation des jeweiligen Dienstes](https://docs.microsoft.com/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management) beschriebene Verfahren.
 
 Darüber hinaus erfordern benutzerbasierte Löschungsanträge, dass das Benutzerkonto selbst gelöscht wird. 

### <a name="step-3-export"></a>Schritt 3: Export 

Der Mandantenadministrator ist die einzige Person in Ihrer Organisation, die auf Windows-Diagnosedaten zugreifen kann, die mit der Verwendung eines Datenprozessordienstes durch einen bestimmten Benutzer für ein in Windows Enterprise registriertes Gerät verbunden sind. Die für eine Exportanträge abgerufenen Daten werden in einem maschinenlesbaren Format bereitgestellt und in Dateien bereitgestellt, mit denen der Benutzer erkennen kann, welchen Geräten und Diensten die Daten zugeordnet sind. Wie bereits erwähnt, enthalten die abgerufenen Daten keine Daten, die die Sicherheit oder Stabilität des Windows-Geräts beeinträchtigen könnten. [Azure DSR, Teil 2, Schritt 3: Exportieren](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), beschreibt, wie ein DSR-Exportantrag über das Azure-Portal ausgeführt wird. 

Microsoft bietet die Möglichkeit, Kundendaten direkt über eine bereits vorhandene Anwendungsprogrammierschnittstelle (API) zu exportieren. Details sind in der [API-Referenzdokumentation](https://docs.microsoft.com/graph/api/user-exportpersonaldata) beschrieben.

## <a name="notify-about-exporting-or-deleting-issues"></a>Benachrichtigung über Probleme beim Exportieren oder Löschen 

Wenn beim Exportieren oder Löschen von Daten aus dem Azure-Portal Probleme auftreten, rufen Sie das Azure-Portalblatt **Hilfe + Support** auf, und übermitteln Sie unter **Abonnementverwaltung > Andere Sicherheits- und Complianceanforderung > Datenschutzblatt und DSGVO-Anforderungen** ein neues Ticket. 
