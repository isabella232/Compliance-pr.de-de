---
title: Anträge betroffener Personen für Intune im Rahmen der DSGVO und des CCPA
description: Dieser Leitfaden wird unseren Kunden dabei helfen, zu verstehen, wie sie mit Microsoft Intune personenbezogene Daten finden und behandeln und wie sie auf DSR- und CCPA-Anforderungen von Kunden reagieren können.
keywords: Microsoft 365, Microsoft 365 Education, Microsoft 365-Dokumentation, DSGVO, CCPA
ms.localizationpriority: high
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
ms.custom:
- seo-marvel-mar2020
hideEdit: true
titleSuffix: Microsoft GDPR
ms.openlocfilehash: b718c4121ebf32e1c87342f778b66ecb07203738
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947849"
---
# <a name="intune-data-subject-requests-for-the-gdpr-and-ccpa"></a>Anträge betroffener Personen für Intune im Rahmen der DSGVO und des CCPA

Die [Datenschutz-Grundverordnung (DSGVO)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) der Europäischen Union gewährt Personen (in den Bestimmungen als *betroffene Personen* bezeichnet) das Recht zum Verwalten ihrer personenbezogenen Daten, die von einem Arbeitgeber oder von einer anderen Art von Behörde oder Organisation (als *Datenverantwortlicher* oder nur *Verantwortlicher* bezeichnet) erfasst werden. Personenbezogene Daten sind im Rahmen der DSGVO weitgefasst als Daten definiert, die sich auf eine identifizierte oder identifizierbare natürliche Person beziehen. Die DSGVO erteilt betroffenen Personen bestimmte Rechte für ihre personenbezogenen Daten; dazu gehören das Kopieren der personenbezogenen Daten, das Anfordern von Korrekturen, das Einschränken der Verarbeitung, das Löschen oder das Erhalten in einem elektronischen Format, damit sie zu einem anderen Datenverantwortlichen bewegt werden können. Eine formale Anfrage einer betroffenen Person an einen Datenverantwortlichen im Hinblick auf eine bestimmte Aktion bezüglich ihrer personenbezogenen Daten wird als *Antrag einer betroffenen Person* bezeichnet.

In ähnlicher Weise bietet der California Consumer Privacy Act (CCPA) den kalifornischen Verbrauchern Datenschutzrechte und -pflichten, einschließlich von Rechten, die den Rechten von betroffenen Personen der DSGV entsprechen, wie z. B. das Recht auf Löschung, Zugriff und Empfang (Portabilität) der persönlichen Informationen.  Das CCPA ermöglicht außerdem bestimmte Offenlegungen, Schutz vor Diskriminierung bei der Wahl von Ausübungsrechten und Deaktivierungs-/Aktivierungsanforderungen für bestimmte Datentransfers, die als "Verkäufe" eingestuft werden. Die Definition von "Verkäufe" umfasst die Freigabe von Daten für eine angemessene Gegenleistung. Weitere Informationen zum CCPA finden Sie im ["California Consumer Privacy Act](offering-ccpa.md) und in den [häufig gestellten Fragen zum California Consumer Privacy Act](ccpa-faq.yml).

In diesem Leitfaden wird erläutert, wie Sie Microsoft-Produkte, -Dienste und -Verwaltungstools verwenden, um unseren Controller-Kunden dabei zu helfen, personenbezogene Daten zu finden und darauf zu reagieren, um auf Anträge betroffener Personen zu reagieren. Insbesondere umfasst dieser Leitfaden, wie sie personenbezogene Daten oder personenbezogene Informationen, die sich in der Microsoft-Cloud befinden, finden, darauf zugreifen und darauf reagieren. Hier ist eine kurze Übersicht über die in diesem Handbuch beschriebenen Prozesse:

- **Ermittlung:** Verwenden Sie Such- und Ermittlungstools, um Kundendaten leichter zu finden, die möglicherweise Gegenstand eines Antrags einer betroffenen Person sind. Sobald potenziell geeignete Dokumente gefunden wurden, können Sie eine oder mehrere der Aktionen für Anträge betroffener Personen durchführen, die in den folgenden Schritten beschrieben sind, um auf den Antrag der betroffenen Person zu reagieren. Andernfalls können Sie bestimmen, dass der Antrag nicht den Unternehmensrichtlinien für die Reaktion auf Anträge betroffener Personen entspricht.
- **Zugriff:** Rufen Sie personenbezogene Daten ab, die sich in der Microsoft Cloud befinden, und erstellen Sie eine Kopie, die der betroffenen Person zur Verfügung gestellt werden kann, sofern dies beantragt wurde.
- **Berichtigung:** Nehmen Sie gegebenenfalls Änderungen an den personenbezogenen Daten vor oder führen Sie andere Aktionen aus, die für die Daten angefordert werden.
- **Einschränkung:** Schränken Sie die Verarbeitung personenbezogener Daten entweder durch Zurückziehen von Lizenzen für verschiedenen Azure-Dienste oder durch Deaktivieren der gewünschten Dienste wo möglich ein. Des Weiteren können Sie Daten aus der Microsoft-Cloud entfernen und diese lokal oder an einem anderen Ort aufbewahren.
- **Löschung:** Entfernen Sie personenbezogene Daten, die sich in der Microsoft-Cloud befinden, dauerhaft.
- **Exportieren/Empfangen (Portierbarkeit):** Stellen Sie der betroffenen Person eine elektronische Kopie (in einem maschinenlesbaren Format) von personenbezogenen Daten oder persönlichen Informationen zur Verfügung. Personenbezogene Informationen gemäß CCPA sind alle Informationen, die eine identifizierte oder identifizierbare Person betreffen. Es wird nicht zwischen privaten, öffentlichen oder beruflichen Rollen einer Person unterschieden. Der definierte Begriff "persönliche Informationen" entspricht in etwa dem Begriff "persönliche Daten" unter der DSGVO. Allerdings umfasst das CCPA auch Familien- und Haushaltsdaten. Weitere Informationen zum CCPA finden Sie im ["California Consumer Privacy Act](offering-ccpa.md) und in den [häufig gestellten Fragen zum California Consumer Privacy Act](ccpa-faq.yml).

In jedem Abschnitt dieses Leitfadens werden die Prozesse beschrieben, die ein als Datenverantwortlicher handelndes Unternehmen nutzen kann, um auf einen Antrag einer betroffenen Person bezüglich ihrer personenbezogenen Daten in der Microsoft-Cloud zu reagieren.

#### <a name="terminology"></a>Begrifflichkeiten

In der nachfolgenden Liste finden Sie Definitionen von Begriffen, die für diesen Leitfaden relevant sind.

- **Datenverantwortlicher:** Eine natürliche oder juristische Person, öffentliche Behörde, Agentur oder andere Stelle, die allein oder gemeinsam mit anderen die Zwecke und Mittel der Verarbeitung personenbezogener Daten bestimmt. Sofern die Zwecke und Mittel der Verarbeitung durch das Recht der Union oder der Mitgliedstaaten bestimmt werden, können der Datenverantwortliche bzw. die spezifischen Kriterien für dessen Benennung durch das Recht der Union oder des Mitgliedstaats angegeben werden.
- **Personenbezogene Daten und betroffene Person:** Alle Informationen über eine identifizierte oder identifizierbare natürliche Person ("betroffene Person"). Eine identifizierbare natürliche Person ist eine Person, die direkt oder indirekt, insbesondere durch Zuordnung zu einer Kennung wie einem Namen, zu einer Kennnummer, zu Standortdaten, zu einer Online-Kennung oder zu einem oder mehreren besonderen Merkmalen identifiziert werden kann, die Ausdruck der physischen, physiologischen, genetischen, psychischen, wirtschaftlichen, kulturellen oder sozialen Identität dieser natürlichen Person sind.
- **Verarbeiter:** Eine natürliche oder juristische Person, öffentliche Behörde, Agentur oder andere Stelle, die personenbezogene Daten im Auftrag des Verantwortlichen verarbeitet.
- **Kundendaten:** Alle Daten, einschließlich aller Text-, Ton-, Video- oder Bilddateien und Software, die Microsoft durch oder im Auftrag eines Kunden durch die Verwendung des Enterprise-Dienstes bereitgestellt werden. Kundendaten umfassen sowohl (1) Informationen zur Identifikation von Endbenutzern (z. B. Benutzernamen und Kontaktinformationen in Azure Active Directory) als auch Kundeninhalte, die ein Kunde in einen bestimmten Dienst hochlädt oder in diesem erstellt (z. B. Kundeninhalte in einem Azure Storage-Konto, Kundeninhalte in einer Azure SQL-Datenbank oder das Image einer virtuellen Maschine eines Kunden in Azure Virtual Machines).
- **Vom System generierte Protokolle:** Von Microsoft generierte Protokolle und verbundene Daten, die Microsoft bei der Bereitstellung von Enterprise-Diensten für Benutzer unterstützen. Vom System generierte Protokolle enthalten in erster Linie pseudonymisierte Daten, z. B. eindeutige Bezeichner – in der Regel eine vom System generierte Zahl, die von sich aus eine Einzelperson nicht identifizieren kann, aber dazu verwendet wird, die Enterprise-Dienste für Benutzer bereitzustellen. Vom System generierte Protokolle enthalten möglicherweise auch Informationen zur Identifikation von Endbenutzern, wie z. B. einen Benutzernamen.

#### <a name="how-to-use-this-guide"></a>Verwenden dieses Leitfadens

Dieser Leitfaden besteht aus zwei Teilen:

- **Teil 1: Reaktion auf Anträge betroffener Personen bezüglich Kundendaten:** In Teil 1 dieses Leitfadens wird erläutert, wie Sie in Anwendungen, in denen Sie Daten verfasst haben, auf diese zugreifen, sie korrigieren, einschränken und exportieren können. Dieser Abschnitt enthält Informationen zum Ausführen von Anträgen betroffener Personen in Bezug auf Kundeninhalte und Informationen zur Identifizierung von Endbenutzern.
- **Teil 2: Reaktion auf Anträge betroffener Personen bezüglich vom System generierten Protokollen:** Wenn Sie die Microsoft Enterprise-Dienste verwenden, generiert Microsoft einige Informationen, die als vom System generierte Protokolle bekannt sind, um den Dienst bereitzustellen. In Teil 2 dieses Leitfadens wird erläutert, wie Sie auf solche Daten in Azure zugreifen können und wie Sie sie löschen und exportieren können.

### <a name="understanding-dsrs-for-azure-active-directory-and-microsoft-intune"></a>Grundlegendes zu Anträgen betroffener Personen für Azure Active Directory und Microsoft Intune

Im Rahmen von Diensten, die für Enterprise-Kunden bereitgestellt werden, ist das Ausführen von Anträgen betroffener Personen immer im Kontext eines bestimmten Azure Active Directory-Mandanten zu verstehen. Anträge betroffener Personen werden *nur* in einem bestimmten Azure Active Directory-Mandanten ausgeführt. Wenn ein Benutzer Teil mehrerer Mandanten ist, wird ein bestimmter Antrag einer betroffenen Person nur im Kontext des Mandanten ausgeführt, in dem die Anforderung empfangen wurde. Dieser Kontext ist eine wichtige Information, weil er bedeutet, dass die Ausführung eines Antrags einer betroffenen Person von einem Enterprise-Kunden **keine** Auswirkungen auf die Daten eines angrenzenden Enterprise-Kunden hat.

Das Gleiche gilt auch für Microsoft Intune, das einem Enterprise-Kunden bereitgestellt wird: die Ausführung eines Antrags einer betroffenen Person bezüglich eines Intune-Kontos, *das einem Azure Active Directory-Mandanten zugeordnet ist*, **betrifft nur** Daten innerhalb dieses Mandanten. Darüber hinaus ist es wichtig, Folgendes beim Umgang mit Intune-Konten in einem Mandanten zu wissen:

- Wenn ein Intune-Benutzer ein Azure-Abonnement erstellt, wird das Abonnement so behandelt, als wäre es ein Azure Active Directory-Mandant. Entsprechend beziehen sich Anträge betroffener Personen nur auf die personenbezogenen Daten innerhalb dieses Mandanten, wie bereits beschrieben.
- Wenn ein über ein Intune-Konto erstelltes Azure-Abonnement gelöscht wird, **hat dies keine Auswirkungen** auf das eigentliche Intune-Konto. Auch hier bezieht sich wie bereits beschrieben die Ausführung von Anträgen betroffener Personen nur auf die personenbezogenen Daten in dem Azure-Abonnement, das hier als Mandant fungiert.

Anträge betroffener Personen bezüglich eines Intune-Kontos selbst, **unabhängig von einem bestimmten Mandanten**, werden über das Datenschutz-Dashboard für unsere Kunden ausgeführt. Weitere Informationen finden Sie im Windows-Leitfaden zu Anträgen betroffener Personen.

## <a name="part-1-dsr-guide-for-customer-data"></a>Teil 1: Leitfaden zu Anträgen betroffener Personen bezüglich Kundendaten

### <a name="executing-dsrs-against-customer-data"></a>Ausführen von Anträgen betroffener Personen bezüglich Kundendaten

Microsoft bietet die Möglichkeit, auf bestimmte Kundendaten über das Azure-Portal und auch direkt über bereits vorhandene Anwendungsprogrammierschnittstellen (APIs) oder Benutzeroberflächen (UI) für bestimmte Dienste (auch bezeichnet als *Produkterfahrungen*) zuzugreifen und diese zu löschen und zu exportieren. Details zu diesen Produkterfahrungen finden Sie in der jeweiligen Referenzdokumentation der entsprechenden Dienste.

>[!IMPORTANT]  
>Dienste, die produktinterne Anträge betroffener Personen unterstützen, erfordern die direkte Verwendung der Anwendungsprogrammierschnittstelle (API) oder der Benutzeroberfläche (UI) des Dienstes, die anwendbare CRUD-Vorgänge (Erstellen, Lesen, Aktualisieren und Löschen) beschreiben. Aus diesem Grund muss die Ausführung von Anträgen betroffener Personen in einem bestimmten Dienst zusätzlich zur Ausführung eines Antrags einer betroffenen Person im Azure-Portal erfolgen, damit ein Antrag einer bestimmten betroffenen Person vollständig abgeschlossen werden kann. Weitere Details finden Sie in der Referenzdokumentation der jeweiligen Dienste.

### <a name="step-1-discover"></a>Schritt 1: Ermittlung

Der erste Schritt der Reaktion auf einen Antrag einer betroffenen Person ist die Suche nach den betroffenen personenbezogenen Daten. In diesem ersten Schritt – Suchen und Überprüfen der betroffenen personenbezogenen Daten – können Sie bestimmen, ob ein Antrag einer betroffenen Person den Anforderungen Ihres Unternehmens zur Anerkennung oder zur Ablehnung eines Antrags einer betroffenen Person entspricht. Nach dem Suchen und Überprüfen der betroffenen personenbezogenen Daten können Sie beispielsweise bestimmen, dass der Antrag nicht den Anforderungen Ihres Unternehmens entspricht, da dadurch Rechte und Freiheiten anderer beeinträchtigt werden könnten.

Nachdem Sie die Daten gefunden haben, können Sie eine bestimmte Aktion ausführen, um der Anforderung durch die betroffene Person gerecht zu werden. Details finden Sie in den folgenden Ressourcen:

- [Datenerfassung](/intune/privacy-data-collect)
- [Datenspeicherung und -verarbeitung](/intune/privacy-data-store-process)
- [Anzeige von personenbezogenen Daten](/intune/privacy-data-view-correct#view-personal-data)

### <a name="step-2-access"></a>Schritt 2: Zugriff

Nachdem Sie Kundendaten mit personenbezogenen Daten gefunden haben, die möglicherweise mit einem Antrag einer betroffenen Person zusammenhängen, liegt es an Ihnen und Ihrer Organisation, zu entscheiden, welche Daten Sie der betroffenen Person zur Verfügung stellen. Sie können ihr eine Kopie des tatsächlichen Dokuments, eine entsprechend geschwärzte Version oder einen Screenshot mit dem Bereich, den Sie als zur Freigabe geeignet eingestuft haben, zur Verfügung stellen. Bei jeder dieser Reaktionen auf eine Zugriffsanforderung müssen Sie eine Kopie des Dokuments oder des anderen Elements, das die entsprechenden Daten enthält, abrufen.

Wenn Sie der betroffenen Person eine Kopie zur Verfügung stellen, müssen Sie personenbezogene Daten zu anderen betroffenen Personen und sämtliche vertraulichen Informationen möglicherweise entfernen oder schwärzen.

Im Folgenden wird erläutert, wie Sie eine Kopie der Daten als Reaktion auf einen Antrag einer betroffenen Person erhalten können.

#### <a name="azure-active-directory"></a>Azure Active Directory

Microsoft bietet sowohl ein Portal als auch Oberflächen im Produkt, mit denen der Mandantenadministrator des Enterprise-Kunden Zugriffsanträge betroffener Personen verwalten kann. Zugriffsanträge betroffener Personen ermöglichen den Zugriff auf die personenbezogenen Daten des Benutzers, einschließlich: (a) Informationen zur Identifikation eines Endbenutzers und (b) vom System generierten Protokollen.

#### <a name="service-specific-interfaces"></a>Dienstspezifische Schnittstellen

Microsoft Intune bietet die Möglichkeit, Kundendaten direkt über Benutzeroberflächen (UIs) oder bereits vorhandene Anwendungsprogrammierschnittstellen (APIs) zu [ermitteln](#step-1-discover).

### <a name="step-3-rectify"></a>Schritt 3: Berichtigung

Wenn eine betroffene Person Sie gebeten hat, personenbezogene Daten zu berichtigen, die in den Daten Ihres Unternehmens gespeichert sind, müssen Sie und Ihr Unternehmen bestimmen, ob dem Antrag Folge zu leisten ist. Die Berichtigung der Daten kann Aktionen wie Bearbeiten, Schwärzen oder Entfernen von personenbezogenen Daten aus einem Dokument oder anderen Element umfassen.

Als Datenverantwortlicher bietet Microsoft nicht die Möglichkeit, die vom System generierten Protokolle zu korrigieren, da diese auf Fakten basierende Aktivitäten widerspiegeln und einen historischen Datensatz der Ereignisse innerhalb von Microsoft-Diensten bilden. Administratoren können keine geräte- oder appspezifischen Informationen im Zusammenhang mit Intune aktualisieren. Wenn ein Endbenutzer personenbezogene Daten (wie den Gerätenamen) korrigieren möchte, muss dies direkt auf dem Gerät erfolgen. Solche Änderungen werden beim nächsten Herstellen einer Verbindung mit Intune synchronisiert.

### <a name="step-4-restrict"></a>Schritt 4: Einschränkung

Betroffene Personen verlangen möglicherweise, dass Sie die Verarbeitung ihrer personenbezogenen Daten einschränken. Wir bieten sowohl das Azure-Portal als auch bereits vorhandene Anwendungsprogrammierschnittstellen (APIs) oder Benutzeroberflächen (UI). Diese Oberflächen bieten dem Mandantenadministrator des Enterprise-Kunden die Möglichkeit, solche Anträge betroffener Personen durch eine Kombination aus Export und Löschen von Daten zu verwalten. Details finden Sie unter [Verarbeitung von personenbezogenen Daten](/intune/privacy-data-store-process#processing-personal-data).

### <a name="step-5-delete"></a>Schritt 5: Löschung

Das „Recht auf Löschung“ durch das Entfernen personenbezogener Daten aus den Kundendaten einer Organisation ist ein wichtiger Schutz in der DSGVO. Das Entfernen personenbezogener Daten umfasst das Entfernen aller personenbezogenen Daten und vom System generierten Protokolle, mit Ausnahme der Überwachungsprotokollinformationen. Details finden Sie unter [Löschen der personenbezogenen von Endbenutzern](/intune/privacy-data-audit-export-delete#delete-end-user-personal-data).

## <a name="part-2-system-generated-logs"></a>Teil 2: Vom System generierte Protokolle

Überwachungsprotokolle bieten Mandantenadministratoren einen Datensatz von Aktivitäten, die eine Änderung in Microsoft Intune generieren. Überwachungsprotokolle stehen für zahlreiche Verwaltungsaktivitäten zur Verfügung und dienen in der Regel zum Erstellen, Aktualisieren (Bearbeiten), Löschen und Zuweisen von Aktionen. Remoteaufgaben, die Überwachungsereignisse generieren, können auch überprüft werden. Diese Überwachungsprotokolle enthalten möglicherweise personenbezogene Daten von Benutzern, deren Geräte bei Intune registriert sind. Administratoren können Überwachungsprotokolle nicht löschen. Details finden Sie unter [Überwachen von personenbezogenen Daten](/intune/privacy-data-audit-export-delete#audit-personal-data).

## <a name="notify-about-exporting-or-deleting-issues"></a>Benachrichtigung über Probleme beim Exportieren oder Löschen

Wenn beim Exportieren oder Löschen von Daten aus dem Azure-Portal Probleme auftreten, wechseln Sie zum Azure-Portalblatt **Hilfe und Support**, und übermitteln Sie ein neues Ticket unter **Abonnementverwaltung > Datenschutz- und Complianceanforderungen für Abonnements > Blatt "Datenschutz" und DSGVO-Anforderungen**.

## <a name="learn-more"></a>Weitere Informationen

- [Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
