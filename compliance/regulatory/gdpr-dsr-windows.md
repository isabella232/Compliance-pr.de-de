---
title: Anträge betroffener Personen zur Konfiguration zur Verarbeitung von Windows-Diagnosedaten im Rahmen der DSGVO und des CCPA
description: Erlernen Sie die Verwendung von Microsoft-Produkten, -Diensten und -Verwaltungstools, um nach personenbezogenen Daten zu suchen und auf DSRs zu reagieren.
keywords: Microsoft 365, Microsoft 365 Education, Microsoft 365-Dokumentation, DSGVO
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmaz
manager: laurawi
ms.reviewer: delinat
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
hideEdit: true
ms.openlocfilehash: 8715ef1ee8133fe950e3ff42b0c53b49f916a018
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573843"
---
# <a name="windows-diagnostic-data-processor-configuration-data-subject-requests-for-the-gdpr-and-ccpa"></a>Anträge betroffener Personen zur Konfiguration zur Verarbeitung von Windows-Diagnosedaten im Rahmen der DSGVO und des CCPA

>[!NOTE]
>Dieses Thema bezieht sich auf Windows 10 Enterprise-, Pro- und Education-Editionen, Version 1809, mit dem Update von Juli 2021 und höher.

## <a name="introduction-to-data-subject-requests-dsrs"></a>Einführung in Anträge betroffener Personen

Die Datenschutz-Grundverordnung (DSGVO) der EU räumt natürlichen Personen (in der Verordnung als _betroffene Personen_ bezeichnet) das Recht ein, vom Arbeitgeber oder einer anderen Einrichtung oder Organisation (_Datenverantwortlicher_ oder _Verantwortlicher_) erhobene personenbezogene Daten zu verwalten. Personenbezogene Daten sind in der DSGVO allgemein als Daten definiert, die sich auf eine identifizierte oder identifizierbare natürliche Person beziehen. Die DSGVO gewährt betroffenen Personen bestimmte Rechte an ihren personenbezogenen Daten, z. B. das Recht auf Erhalt einer Kopie dieser personenbezogenen Daten, das Recht auf Korrektur der Daten, das Recht auf Einschränkung der Bearbeitung dieser Daten und das Recht auf Empfang dieser Daten in einem elektronischen Format, sodass sie an einen anderen Verantwortlichen übermittelt werden können. Ein von einer betroffenen Person formal gestellter Antrag an den Verantwortlichen, bestimmte Maßnahmen im Zusammenhang mit den personenbezogenen Daten der betroffenen Person zu ergreifen, wird als _Antrag einer betroffenen Person_ bezeichnet.

In ähnlicher Weise bietet der California Consumer Privacy Act (CCPA) den kalifornischen Verbrauchern Datenschutzrechte und -pflichten, einschließlich von Rechten, die den Rechten von betroffenen Personen der DSGV entsprechen, wie z. B. das Recht auf Löschung, Zugriff und Empfang (Portabilität) der persönlichen Informationen. Das CCPA ermöglicht außerdem bestimmte Offenlegungen, Schutz vor Diskriminierung bei der Wahl von Ausübungsrechten und Deaktivierungs-/Aktivierungsanforderungen für bestimmte Datentransfers, die als „Verkäufe“ eingestuft werden. Die Definition von "Verkäufe" umfasst die Freigabe von Daten für eine angemessene Gegenleistung. Weitere Informationen zum CCPA finden Sie im ["California Consumer Privacy Act](/microsoft-365/compliance/offering-ccpa) und in den [häufig gestellten Fragen zum California Consumer Privacy Act](/microsoft-365/compliance/ccpa-faq).

In diesem Leitfaden wird erläutert, wie Microsoft-Produkte, -Dienste und -Verwaltungstools verwendet werden können, um als Reaktion auf Anträge betroffener Personen unseren als Datenverantwortliche handelnden Kunden dabei zu helfen, personenbezogene Daten zu finden und auf diese zu reagieren. Dies umfasst das Suchen, den Zugriff und die Reaktion auf personenbezogene Daten innerhalb der Windows-Diagnosedaten, die von Microsoft gesammelt werden, wenn die Konfiguration zur Verarbeitung von Windows-Diagnosedaten aktiviert ist. Im Folgenden finden Sie eine kurze Übersicht der in diesem Leitfaden beschriebenen Prozesse:

1. **Zugriff**: Rufen Sie Windows-Diagnosedaten ab, die einer betroffenen Person zugeordnet sind, und erstellen Sie eine Kopie, die der betroffenen Person zur Verfügung gestellt werden kann, sofern dies beantragt wurde.
2. **Löschen**: Entfernen Sie Windows-Diagnosedaten, die einer betroffenen Person zugeordnet sind, dauerhaft.
3. **Exportier**: Stellen Sie der betroffenen Person eine elektronische Kopie (in einem maschinenlesbaren Format) ihrer Windows-Diagnosedaten zur Verfügung.

Personenbezogene Informationen gemäß CCPA sind alle Informationen, die eine identifizierte oder identifizierbare Person betreffen. Es wird nicht zwischen privaten, öffentlichen oder beruflichen Rollen einer Person unterschieden. Der definierte Begriff "personenbezogene Informationen" entspricht in etwa dem Begriff "personenbezogene Daten" unter der DSGVO. Allerdings umfasst das CCPA auch Familien- und Haushaltsdaten. Weitere Informationen zum CCPA finden Sie im ["California Consumer Privacy Act](/microsoft-365/compliance/offering-ccpa) und in den [häufig gestellten Fragen zum California Consumer Privacy Act](/microsoft-365/compliance/ccpa-faq).

In jedem Abschnitt dieses Handbuchs werden die technischen Verfahren beschrieben, die eine Organisation, die Datenverantwortlicher ist, ergreifen kann, um auf einen Antrag einer betroffenen Person für Windows-Diagnosedaten zu reagieren, die von Microsoft gesammelt werden, wenn die Konfiguration zur Verarbeitung von Windows-Diagnosedaten aktiviert ist.

## <a name="terminology"></a>Begrifflichkeiten

In der nachfolgenden Liste finden Sie Definitionen von Begriffen, die für diesen Leitfaden relevant sind.

* _Datenverantwortlicher:_ Eine natürliche oder juristische Person, öffentliche Behörde, Agentur oder andere Stelle, die allein oder gemeinsam mit anderen die Zwecke und Mittel der Verarbeitung personenbezogener Daten bestimmt. Sofern die Zwecke und Mittel der Verarbeitung durch das Recht der Union oder der Mitgliedstaaten bestimmt werden, können der Datenverantwortliche bzw. die spezifischen Kriterien für dessen Benennung durch das Recht der Union oder des Mitgliedstaats angegeben werden.

* _Personenbezogene Daten und betroffene Person:_ Alle Informationen über eine identifizierte oder identifizierbare natürliche Person („betroffene Person“). Eine identifizierbare natürliche Person ist eine Person, die direkt oder indirekt, insbesondere durch Zuordnung zu einer Kennung wie einem Namen, zu einer Kennnummer, zu Standortdaten, zu einer Online-Kennung oder zu einem oder mehreren besonderen Merkmalen identifiziert werden kann, die Ausdruck der physischen, physiologischen, genetischen, psychischen, wirtschaftlichen, kulturellen oder sozialen Identität dieser natürlichen Person sind.

* _Auftragsverarbeiter:_ Eine natürliche oder juristische Person, Behörde, Einrichtung oder andere Stelle, welche personenbezogene Daten im Auftrag des Datenverantwortlichen verarbeitet.

* _Kundendaten_: Alle Daten, einschließlich aller Text-, Sound-, Video- oder Bilddateien, die Microsoft vom Kunden oder im Auftrag des Kunden durch Nutzung von Enterprise-Diensten bereitgestellt werden. 

* _Windows-Diagnosedaten_: Technische Daten von Windows-Geräten über das Gerät sowie die Leistung von Windows und verwandter Software. Sie werden verwendet, um Windows auf dem neuesten Stand, sicher, zuverlässig und leistungsfähig zu halten und Produktverbesserungen vorzunehmen. Einige Beispiele für Windows-Diagnosedaten sind der Typ der verwendeten Hardware, die installierten Anwendungen mit ihrer jeweiligen Nutzung sowie Informationen zur Zuverlässigkeit von Gerätetreibern. Einige Windows-Komponenten und Apps bauen eine direkte Verbindung mit Microsoft-Diensten auf, aber bei den ausgetauschten Daten handelt es sich nicht um Windows-Diagnosedaten. So handelt es sich beispielsweise beim Erfassen des Standorts eines Benutzers für den lokalen Wetterbericht oder Nachrichten nicht um Windows-Diagnosedaten.

## <a name="how-to-use-this-guide"></a>Verwenden dieses Leitfadens

Wenn Sie die Konfiguration zur Verarbeitung von Windows-Diagnosedaten aktivieren, werden Sie zum Datenverantwortlichen für die von Geräten gesammelten Windows-Diagnosedaten. Weitere Informationen zu dieser Konfiguration finden Sie unter [Konfigurieren von Windows-Diagnosedaten in Ihrer Organisation](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

## <a name="windows-diagnostic-data"></a>Windows-Diagnosedaten

Microsoft bietet Ihnen die Möglichkeit, auf Windows-Diagnosedaten, die mit der Gerätenutzung eines Benutzers bei aktivierter Konfiguration zur Verarbeitung von Windows-Diagnosedaten in Verbindung stehen, zuzugreifen, sie zu löschen und zu exportieren.

> [!IMPORTANT]
> Einige Windows-Diagnosedaten sind nur einem Gerätebezeichner und keinem bestimmten Benutzer zugeordnet. Diese Art von Daten auf Geräteebene wird nicht exportiert und innerhalb von 30 Tagen aus unseren Systemen gelöscht.<br><br>
> Die Möglichkeit zur Berichtigung von Windows-Diagnosedaten wird nicht unterstützt. Windows-Diagnosedaten stellen tatsächliche Aktionen dar, die innerhalb von Windows durchgeführt wurden, und Änderungen an diesen Daten würden die historische Erfassung von Aktionen kompromittieren und das Sicherheitsrisiko erhöhen sowie die Zuverlässigkeit beschädigen.

Der nächste Abschnitt enthält Schritte zum Ausführen eines Antrags einer betroffenen Person für Windows-Diagnosedaten, die einer Azure Active Directory (AAD)-Benutzer-ID zugeordnet ist. Weitere Informationen finden Sie unter [Windows 10 – Datenschutz und Compliance: Leitfaden für IT- und Complianceexperten](/windows/privacy/windows-10-and-privacy-compliance).

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>Ausführen von Anträgen betroffener Personen für Windows-Diagnosedaten

Microsoft bietet die Möglichkeit, auf bestimmte Windows-Diagnosedaten über das Azure-Portal und auch direkt über bereits vorhandene Anwendungsprogrammierschnittstellen (APIs) zuzugreifen, diese zu löschen und zu exportieren.

### <a name="step-1-access"></a>Schritt 1: Zugriff

Microsoft bietet dem Mandantenadministrator innerhalb Ihrer Organisation eine Möglichkeit, auf Windows-Diagnosedaten zuzugreifen, die im Zusammenhang mit der Verwendung eines Geräts durch einen bestimmten Benutzer bei aktivierter Konfiguration zur Verarbeitung von Windows-Diagnosedaten gesammelt werden. Die für einen Zugriffsantrag abgerufenen Daten werden mittels Export in einem maschinell lesbaren Format sowie in Dateien bereitgestellt, durch die der Benutzer erkennen kann, welchen Geräten und Diensten die Daten zugeordnet sind. Die abgerufenen Daten enthalten keine Daten, welche die Sicherheit oder Stabilität des Windows-Geräts beeinträchtigen könnten.

Das Azure-Portal stellt dem Mandantenadministrator des Unternehmenskunden die Möglichkeit bereit, DSR-Zugriffsanforderungen betroffener Personen zu verwalten. [Azure-DSR, Teil 2, Schritt 3: Export](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), beschreibt, wie eine DSR-Zugriffsanforderung für Windows-Diagnosedaten mittels Export über das Azure-Portal durchzuführen ist.

### <a name="step-2-delete"></a>Schritt 2: Löschung

Microsoft bietet eine Möglichkeit zum Ausführen benutzerbasierter DSR-Löschungsanträge, basierend auf dem Azure Active Directory-Objekt eines bestimmten Benutzers.

Für benutzerbasierte Löschanforderungen bietet Microsoft zwei Lösungen an.  Es gibt eine Portal-Umgebung, über die der Mandantenadministrator des Unternehmenskunden DSR-Löschanforderungen betroffener Personen verwalten kann. [Azure-DSR, Teil 1, Schritt 5: Löschen](/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete), beschreibt, wie eine DSR-Löschanforderung für Windows-Diagnosedaten über das Azure-Portal durch Löschen eines Benutzers und der zugeordneten Daten durchzuführen ist.

Microsoft bietet zudem die Möglichkeit, Benutzer direkt über eine bereits vorhandene Anwendungsprogrammierschnittstelle (API) zu löschen, wodurch wiederum Windows-Diagnosedaten gelöscht werden. Details werden in der [Referenzdokumentation der API](/graph/api/directory-deleteditems-delete) beschrieben.

>[!IMPORTANT]
>Durch das Löschen von gesammelten Daten vom Gerät wird die weitere Sammlung nicht beendet. Um die Datensammlung zu beenden, befolgen Sie das in der [jeweiligen Referenzdokumentation des entsprechenden Diensts](/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management) beschriebene Verfahren.

### <a name="step-3-export"></a>Schritt 3: Export

Der Mandantenadministrator ist die einzige Person in Ihrer Organisation, die auf Windows-Diagnosedaten im Zusammenhang mit der Verwendung eines Geräts durch einen bestimmten Benutzer, die bei aktivierter Konfiguration zur Verarbeitung von Windows-Diagnosedaten gesammelt werden, zugreifen kann. Die für einen Exportantrag abgerufenen Daten werden in einem maschinell lesbaren Format bereitgestellt und in Dateien bereitgestellt, durch die der Benutzer erkennen kann, welchen Geräten und Diensten die Daten zugeordnet sind. Die abgerufenen Daten enthalten keine Daten, welche die Sicherheit oder Stabilität des Windows-Geräts beeinträchtigen könnten. [Azure-DSR, Teil 2, Schritt 3: Export](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), beschreibt, wie eine DSR-Exportanforderung für Windows-Diagnosedaten über das Azure-Portal durchzuführen ist.

Microsoft bietet zudem die Möglichkeit, Windows-Diagnosedaten direkt über eine bereits vorhandene Anwendungsprogrammierschnittstelle (API) zu exportieren. Details werden in der [Referenzdokumentation der API](/graph/api/user-exportpersonaldata) beschrieben.

## <a name="notify-us-about-exporting-or-deleting-issues"></a>Benachrichtigen Sie uns über Probleme beim Exportieren oder Löschen

Wenn beim Exportieren oder Löschen von Windows-Diagnosedaten aus dem Azure-Portal Probleme auftreten, wechseln Sie zum Azure-Portalblatt **Hilfe und Support**, und übermitteln Sie ein neues Ticket unter **Abonnementverwaltung > Datenschutz- und Complianceanforderungen für Abonnements > Blatt "Datenschutz" und DSGVO-Anforderungen**.

>[!NOTE]
>Es kann bis zu 5 Tage dauern, um eine Exportanforderung für Windows-Diagnosedaten abzuschließen. Wenn Sie Probleme haben, warten Sie bitte mindestens 7 Tage, bevor Sie ein Supportticket öffnen.
