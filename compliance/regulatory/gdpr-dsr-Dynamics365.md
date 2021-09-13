---
title: Auskunftsrecht betroffener Personen für Dynamics 365 im Rahmen der DSGVO und CCPA
description: Lernen Sie, wie Sie personenbezogene Daten finden und behandeln und wie Sie auf DSR- und CCPA-Anforderungen von Dynamics 365-Kunden reagieren können.
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
hideEdit: true
ms.custom:
- seo-marvel-mar2020
titleSuffix: Microsoft GDPR
ms.openlocfilehash: 7b6919cbdf2ece468eeec8931b652972a74b07dc
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159837"
---
# <a name="dynamics-365-data-subject-requests-for-the-gdpr-and-ccpa"></a>Auskunftsrecht betroffener Personen für Dynamics 365 im Rahmen der DSGVO und CCPA

Die europäische [Datenschutz-Grundverordnung (DSGVO)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) gewährt Personen (die in den Bestimmungen als *betroffene Personen* bezeichnet werden) Berechtigungen zum Verwalten der personenbezogenen Daten, die von einem Arbeitgeber oder von einer anderen Art von Behörde oder Organisation (als *Datenverantwortlicher* oder nur *Verantwortlicher* bezeichnet) erfasst werden. Personenbezogene Daten sind im Rahmen der DSGVO weitgefasst als Daten definiert, die sich auf eine identifizierte oder identifizierbare natürliche Person beziehen. Die DSGVO erteilt betroffenen Personen bestimmte Rechte für ihre personenbezogenen Daten; dazu gehören das Kopieren der personenbezogenen Daten, das Anfordern von Änderungen, das Einschränken der Verarbeitung, das Löschen oder das Erhalten in einem elektronischen Format, damit sie zu einem anderen Datenverantwortlichen bewegt werden können. Eine formale Anforderung von einer betroffenen Person an einen Datenverantwortlichen im Hinblick auf eine bestimmte Aktion für deren personenbezogene Daten wird in diesem Dokument als *Anforderung einer betroffenen Person* bezeichnet.

In ähnlicher Weise bietet der California Consumer Privacy Act (CCPA) den kalifornischen Verbrauchern Datenschutzrechte und -pflichten, einschließlich von Rechten, die den Rechten von betroffenen Personen der DSGV entsprechen, wie z. B. das Recht auf Löschung, Zugriff und Empfang (Portabilität) der persönlichen Informationen.  Das CCPA ermöglicht außerdem bestimmte Offenlegungen, Schutz vor Diskriminierung bei der Wahl von Ausübungsrechten und Deaktivierungs-/Aktivierungsanforderungen für bestimmte Datentransfers, die als "Verkäufe" eingestuft werden. Die Definition von "Verkäufe" umfasst die Freigabe von Daten für eine angemessene Gegenleistung. Weitere Informationen zum CCPA finden Sie im ["California Consumer Privacy Act](offering-ccpa.md) und in den [häufig gestellten Fragen zum California Consumer Privacy Act](ccpa-faq.yml).

In diesem Leitfaden wird erläutert, wie Microsoft-Produkte, -Dienste und -Verwaltungstools verwendet werden können, um als Reaktion auf Anträge betroffener Personen unseren als Datenverantwortliche handelnden Kunden dabei zu helfen, personenbezogene Daten zu finden und auf diese zu reagieren. Dies umfasst das Suchen, den Zugriff und die Reaktion auf personenbezogene Daten bzw. Informationen, die in der Microsoft-Cloud gespeichert sind. Im Folgenden finden Sie eine kurze Übersicht den in diesem Leitfaden beschriebenen Prozesse:

- **Ermittlung:** Verwenden Sie Such- und Ermittlungstools, um Kundendaten leichter zu finden, die möglicherweise Gegenstand eines Antrags einer betroffenen Person sind. Sobald potenziell geeignete Dokumente gefunden wurden, können Sie eine oder mehrere der Aktionen für Anträge betroffener Personen ausführen, die in den folgenden Schritten beschrieben sind, um auf den Antrag zu reagieren. Andernfalls können Sie bestimmen, dass der Antrag nicht Ihren Unternehmensrichtlinien für die Reaktion auf Anträge betroffener Personen entspricht.
- **Zugriff:** Rufen Sie personenbezogene Daten ab, die sich in der Microsoft Cloud befinden, und erstellen Sie eine Kopie, die der betroffenen Person zur Verfügung gestellt wird, sofern dies beantragt wurde.
- **Berichtigung:** Nehmen Sie gegebenenfalls Änderungen an den personenbezogenen Daten vor oder führen Sie andere Aktionen aus, die für die Daten angefordert werden.
- **Einschränken:** Schränken Sie die Verarbeitung von personenbezogenen Daten ein, indem Sie entweder die Lizenzen für verschiedene Onlinedienste entfernen oder die gewünschten Dienste, wenn möglich, deaktivieren.
- **Löschen:** Entfernen Sie personenbezogene Daten, die sich in der Microsoft-Cloud befinden, dauerhaft.
- **Exportieren/Empfangen (Portierbarkeit):** Stellen Sie der betroffenen Person eine elektronische Kopie (in einem maschinenlesbaren Format) von personenbezogenen Daten oder persönlichen Informationen zur Verfügung. Personenbezogene Informationen gemäß CCPA sind alle Informationen, die eine identifizierte oder identifizierbare Person betreffen. Es wird nicht zwischen privaten, öffentlichen oder beruflichen Rollen einer Person unterschieden. Der definierte Begriff "persönliche Informationen" entspricht in etwa dem Begriff "persönliche Daten" unter der DSGVO. Allerdings umfasst das CCPA auch Familien- und Haushaltsdaten. Weitere Informationen zum CCPA finden Sie im ["California Consumer Privacy Act](offering-ccpa.md) und in den [häufig gestellten Fragen zum California Consumer Privacy Act](ccpa-faq.yml).

In jedem Abschnitt dieses Leitfadens werden die Prozesse beschrieben, die ein als Datenverantwortlicher handelndes Unternehmen nutzen kann, um auf einen Antrag einer betroffenen Person bezüglich ihrer personenbezogenen Daten in der Microsoft-Cloud zu reagieren.

## <a name="gdpr-terminology"></a>Terminologie der DSGVO

In der nachfolgenden Liste finden Sie Definitionen von Begriffen, die für diesen Leitfaden relevant sind:

- **Datenverantwortlicher:** Eine natürliche oder juristische Person, öffentliche Behörde, Agentur oder andere Stelle, die allein oder gemeinsam mit anderen die Zwecke und Mittel der Verarbeitung personenbezogener Daten bestimmt. Sofern die Zwecke und Mittel der Verarbeitung durch das Recht der Union oder der Mitgliedstaaten bestimmt werden, können der Datenverantwortliche bzw. die spezifischen Kriterien für dessen Benennung durch das Recht der Union oder des Mitgliedstaats angegeben werden.
- **Personenbezogene Daten und betroffene Person:** Alle Informationen über eine identifizierte oder identifizierbare natürliche Person ("betroffene Person"). Eine identifizierbare natürliche Person ist eine Person, die direkt oder indirekt, insbesondere durch Zuordnung zu einer Kennung wie einem Namen, zu einer Kennnummer, zu Standortdaten, zu einer Online-Kennung oder zu einem oder mehreren besonderen Merkmalen identifiziert werden kann, die Ausdruck der physischen, physiologischen, genetischen, psychischen, wirtschaftlichen, kulturellen oder sozialen Identität dieser natürlichen Person sind.
- **Verarbeiter:** Eine natürliche oder juristische Person, öffentliche Behörde, Agentur oder andere Stelle, die personenbezogene Daten im Auftrag des Verantwortlichen verarbeitet.
- **Kundendaten:** Alle Daten, einschließlich aller Text-, Ton-, Video- oder Bilddateien und Software, die Microsoft durch oder im Auftrag eines Kunden durch die Verwendung des Enterprise-Dienstes bereitgestellt werden. Kundendaten umfassen sowohl (1) Informationen zur Identifikation von Endbenutzern (z. B. Benutzernamen und Kontaktinformationen in Azure Active Directory) als auch Kundeninhalte, die ein Kunde in einen bestimmten Dienst hochlädt oder in diesem erstellt (z. B. Kundeninhalte in einem Azure Storage-Konto, Kundeninhalte in einer Azure SQL-Datenbank oder das Image einer virtuellen Maschine eines Kunden in Azure Virtual Machines).
- **Vom System generierte Protokolle:** Von Microsoft generierte Protokolle und verbundene Daten, die Microsoft bei der Bereitstellung von Enterprise-Diensten für Benutzer unterstützen. Vom System generierte Protokolle enthalten in erster Linie pseudonymisierte Daten, z. B. eindeutige Bezeichner – in der Regel eine vom System generierte Zahl, die von sich aus eine Einzelperson nicht identifizieren kann, aber dazu verwendet wird, die Enterprise-Dienste für Benutzer bereitzustellen. Vom System generierte Protokolle enthalten möglicherweise auch Informationen zur Identifikation von Endbenutzern, wie z. B. einen Benutzernamen.

## <a name="how-this-guide-can-help-you-meet-your-controller-responsibilities"></a>So kann Sie dieser Leitfaden bei der Einhaltung Ihrer Verantwortlichkeiten als Datenverantwortlicher unterstützen

Der aus zwei Teilen bestehende Leitfaden erklärt, wie Dynamics 365-Produkte, -Dienste und -Verwaltungstools verwendet werden können, um Daten in der Microsoft-Cloud zu finden und zu nutzen als Reaktion auf Anforderungen von betroffenen Personen, die von ihren Rechten gemäß der DSGVO Gebrauch machen. Der erste Teil befasst sich mit personenbezogenen Daten, die in Kundendaten enthalten sind, gefolgt von einem Teil zu sonstigen pseudonymisierten personenbezogenen Daten, die in vom System generierten Protokollen enthalten sind.

- **Teil 1: Reaktion auf Anträge betroffener Personen bezüglich personenbezogener Daten, die in Kundendaten enthalten sind:** Teil 1 dieses Leitfadens erläutert, wie auf personenbezogene Daten in Dynamics 365-Anwendungen (Software-as-a-Service), die als Teil der Kundendaten verarbeitet werden, die Sie dem Onlinedienst zur Verfügung gestellt haben, zugegriffen, wie diese berichtigt, eingeschränkt, gelöscht und exportiert werden können.
- **Teil 2: Reaktion auf Anträge betroffener Personen bezüglich pseudonymisierter Daten:** Wenn Sie Enterprise-Dienste von Dynamics 365 nutzen, protokolliert Microsoft im Rahmen der Bereitstellung des Service Informationen über die Verwendung des Service durch den Endbenutzer (in diesem Dokument als *vom System generierte Protokolle* bezeichnet), um deren Aktionen im System zu ermitteln. Obwohl diese Daten nicht ohne zusätzliche Informationen einer bestimmten betroffenen Person zugeordnet werden können, können manche dieser Daten gemäß der DSGVO als personenbezogen klassifiziert werden. Teil 2 dieses Leitfadens erläutert, wie auf vom System generierte Protokolle von Dynamics 365 zugegriffen werden kann und wie diese gelöscht und exportiert werden können.

## <a name="preparing-for-data-subject-rights-investigations"></a>Vorbereiten auf Untersuchungen im Rahmen von Anträgen betroffener Personen

Wenn betroffene Personen Gebrauch von Ihren Rechten machen und Anforderungen stellen, müssen die folgenden Punkte berücksichtigt werden:

- Korrekte Identifizierung der Person und Rolle (wie Mitarbeiter, Kunde, Lieferant) mithilfe von Informationen, die die betroffene Person Ihnen im Rahmen seiner/ihrer Anforderung bereitgestellt hat. Diese Informationen können ein Name, eine Mitarbeiter-ID oder Kundennummer sowie sonstige Bezeichnet sein.
- Aufzeichnen von Datum und Uhrzeit der Anforderung. (Sie haben 30 Tage Zeit, um die Anforderung zu erfüllen.)
- Bestätigen Sie, dass der Antrag den Anforderungen Ihres Unternehmens bezüglich der Erfüllung oder Ablehnung von Anträgen betroffener Personen entspricht. Zum Beispiel müssen Sie sicherstellen, dass die Ausführung des Antrags nicht im Widerspruch zu anderen rechtlichen, finanziellen oder regulatorischen Verpflichtungen steht, die Sie haben, oder die Rechte und Freiheiten anderer verletzt.
- Vergewissern Sie sich, dass Sie über die Informationen zu dem Antrag verfügen.

## <a name="part-1-responding-to-data-subject-rights-requests-for-personal-data-included-in-customer-data"></a>Teil 1: Reaktion auf Anträge betroffener Personen bezüglich personenbezogenen Daten, die in Kundendaten enthalten sind.

In den folgenden Artikeln finden Sie Informationen zur Vorbereitung und Reaktion auf Anträge betroffener Personen bezüglich personenbezogener Daten, die in den von Dynamics 365 verarbeiteten Kundendaten enthalten sind. Es ist zu beachten, dass personenbezogene Daten in anderen Kategorien von Daten enthalten sein können, die von Microsoft im Rahmen eines Abonnements für Onlinedienste verarbeitet werden, wie z. B. Administratordaten oder Unterstützungsdaten, die in den Microsoft-Datenschutzbestimmungen definiert sind. Dieses Dokument ist darauf beschränkt, Sie bei der Ermittlung und Verwaltung von Anträgen betroffener Personen zu unterstützen, die personenbezogene Daten betreffen, die in den Kundendaten enthalten sind, die Sie Dynamics 365 zur Verfügung gestellt haben.

Dynamics 365 ist ein Onlinedienst, der mehrere Datenverarbeitungsfunktionen als Software-as-a-Service (SaaS) anbietet. Damit bietet Dynamics 365 eine breite Palette von Funktionen zur Verarbeitung einer vielfältigen Sammlung von Daten, die je nach Art, Zweck oder anderen spezifischen Merkmalen wie Verkaufsdaten, Transaktionen, Finanzen, Personalinformationen usw. variieren können. Angesichts dieser Vielfalt bietet Dynamics 365 mehrere Formulare, Felder, Schemata, Endpunkte und Logik zur Verarbeitung von Kundendaten, was sich auch in den vielfältigen Möglichkeiten widerspiegelt, mit denen Anträge betroffener Personen in den einzelnen Anwendungen bearbeitet werden können. Wenn Dynamics 365-Anwendungen mehrere Möglichkeiten bieten, um auf spezifische Anträge betroffener Personen zu reagieren, werden wir darauf in diesem Leitfaden hinweisen, indem wir auf die technischen Beschreibungen der einzelnen Anwendungen verweisen.

### <a name="dynamics-365"></a>Dynamics 365

#### <a name="finding-customer-data"></a>Suchen nach Kundendaten

Der erste Schritt der Reaktion auf einen Antrag einer betroffenen Person ist es, die Kundendaten zu suchen und zu ermitteln, die von dem Antrag betroffen sind.

Die angemessene Klassifizierung von Kundendaten ist der Grundstein für die Arbeit mit personenbezogenen Daten in Dynamics 365 Customer Engagement-Geschäftsanwendungen. Dynamics 365 for Customer Engagement bietet die Flexibilität, Anwendungserweiterungen für die Datenklassifizierung zu erstellen. Die richtige Klassifizierung ermöglicht es Ihnen, Informationen als personenbezogene Daten zu identifizieren, wodurch sie im Rahmen eines Antrags einer betroffenen Person gefunden und abgerufen werden können. Es kann auch dazu beitragen, die gesetzlichen und behördlichen Vorschriften für die Erhebung und Verwaltung personenbezogener Daten einzuhalten.

Microsoft bietet Funktionen, die Sie bei der Reaktion auf Anträge betroffener Personen und in diesem Zusammenhang beim Zugriff auf Kundendaten unterstützen können. Es liegt jedoch in Ihrer Verantwortung, dafür zu sorgen, dass personenbezogenen Daten gefunden und klassifiziert werden.

***Dynamics 365 for Customer Engagement*** bietet Ihnen mehrere Methoden, um in Datensätzen nach personenbezogenen Daten zu suchen, z. B.: Erweiterte Suche und Suche nach Datensätzen. Diese Funktionen ermöglichen es Ihnen, personenbezogene Daten zu identifizieren (zu finden).

- [Erweiterte Suche](/dynamics365/customer-engagement/basics/save-advanced-find-search)
- [Suchen Sie nach Datensätzen](/dynamics365/customer-engagement/basics/search-records) für mehrere Typen von Datensätzen

In Dynamics 365 for Marketing haben Sie die folgenden zusätzlichen Funktionen:

1. [Erstellen von Power BI-Berichten](/power-bi/service-connect-to-microsoft-dynamics-crm), um Kundendaten zu filtern und zu identifizieren.
2. Nutzen Sie die Insight-Ansichten für Kontakte und Objekte der Marketingversion, um zusätzliche Datenpunkte zu identifizieren, die Kundendaten enthalten können.

***Dynamics 365 Customer Service Insights*** bietet eine Liste von Ressourcen, die Ihnen helfen, [Kundendaten zu finden](/dynamics365/ai/customer-service-insights/gdpr-discovery), um auf DSGVO-Anträge von Kunden zu reagieren.

***Dynamics 365 for Finance and Operations*** bietet Ihnen mehrere Möglichkeiten, nach Kundendaten zu suchen. Sie als Mandantenadministrator können die folgenden Aktionen durchführen, um nach Kundendaten zu suchen:

- Sie können Ihre Kundendaten so organisieren, dass sie dem schnellen Auffinden personenbezogener Daten dienen. Hier finden Sie Informationen dazu, [wie Sie den Datenbestand klassifizieren](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#detailed-inventory).
- Verwenden des [Personensuchberichts](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#the-person-search-report), um personenbezogene Daten zu suchen und zu erfassen.
- [Erweitern des Personensuchberichts](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) durch Erstellen einer neuen Entität oder Erweitern einer vorhandenen Entität.
- Verwenden Sie Such- und Filterfunktionen, um bestimmte personenbezogene Daten zu finden und diese mit Hilfe der Microsoft Office-Exportfunktion zu exportieren, oder drucken Sie diese Informationen mit Hilfe von Browsererweiterungen in ein .pdf-Format.
- Erstellen Sie ein benutzerdefiniertes Formular, das personenbezogene Daten sucht und exportiert.
- Erstellen Sie ein externes Portal oder eine externe Website, das bzw. die es einem authentifizierten Kunden ermöglicht, seine personenbezogenen Daten einzusehen.

***Dynamics 365 Business Central*** bietet mehrere Optionen, mit denen Sie nach Daten suchen können. Einzelheiten hierzu finden Sie unter [Suchen, Filtern und Sortieren von Daten](/dynamics365/business-central/ui-enter-criteria-filters).

***Dynamics 365 for Talent*** bietet erweiterte Such- und Filterfunktionen, um bestimmte personenbezogene Daten zu finden. Außerdem stellt es Microsoft Office-Exportfunktionen zur Verfügung, um diese Informationen mithilfe von Browsererweiterungen in ein .pdf-Format zu exportieren oder zu drucken.

- Verwenden des [Personensuchberichts](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#the-person-search-report), um Kundendaten zu suchen und zu erfassen.
- [Erweitern des Personensuchberichts](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) durch Erstellen einer neuen Entität oder Erweitern einer vorhandenen Entität.

### <a name="providing-a-copy-of-customer-data"></a>Bereitstellen einer Kopie der Kundendaten

Kundendaten in ***Dynamics 365 for Customer Engagement*** können mit den umfangreichen Exportfunktionen exportiert werden. Kundendaten können in eine statische Excel-Datei exportiert werden, um einen Antrag auf Datenübertragbarkeit einfacher erfüllen zu können.Mit Excel können Sie dann die personenbezogenen Daten, die in den Antrag auf Datenübertragbarkeit aufgenommen werden sollen, bearbeiten und in einem gängigen, maschinenlesbaren Format, wie z. B. CSV oder XML, speichern. Dynamics 365 for Customer Engagement-Datensätze können auch über die [Common Data Service-Web-API](/powerapps/developer/common-data-service/webapi/overview) exportiert werden.

Zusätzlich wird für Dynamics 365 for Marketing eine [dedizierte API](/dynamics365/customer-engagement/marketing/developer/retrieve-interactions-contact) bereitgestellt, über die der Kunde Erweiterungen erstellen kann, die zusätzliche Datensätze von erfassten Kundeninteraktionen, die personenbezogene Daten enthalten können, abrufen. Die API lädt alle relevanten Informationen aus dem Back-End-System und fasst sie zu einem einzigen, portablen Dokument zusammen.

***Dynamics 365 Customer Service Insights*** ermöglicht es Ihnen, mithilfe von Datenexporten [eine Kopie der Kundendaten bereitzustellen](/dynamics365/ai/customer-service-insights/gdpr-export).

Kundendaten in ***Dynamics 365 for Finance and Operations** _ können mithilfe der umfassenden Exportfunktionen für Entitäten exportiert werden. Mithilfe der [_Datenverwaltungs- und Integrationsentitäten*](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-integration-data-entity) kann der Mandantenadministrator bereitgestellte Entitäten verwenden, neue Entitäten erstellen oder vorhandene Entitäten für einen wiederholbaren Export personenbezogener Daten nach Excel oder eine Reihe anderer gängiger Formate mit [*Datenimport- und -exportaufträgen*](/dynamics365/unified-operations/dev-itpro/data-entities/data-import-export-job)erweitern.  Alternativ können viele Listen in eine statische Excel-Datei exportiert werden, um einen Antrag auf Datenübertragbarkeit zu erleichtern. Werden Kundendaten nach Excel exportiert, können Sie die personenbezogenen Daten, die in den Antrag auf Datenübertragbarkeit aufgenommen werden sollen, bearbeiten und die Datei dann in einem gängigen, maschinenlesbaren Format, wie z. B. CSV oder XML, speichern. Sie können auch die Verwendung des *Personensuchberichts* in Betracht ziehen, um der betroffenen Person Daten bereitzustellen, die Sie als personenbezogene Daten klassifiziert haben.

In ***Dynamics 365 Business Central*** können Sie zwei Funktionen nutzen, um eine Kopie der Kundendaten an eine betroffene Person zu übermitteln:

Sie können Kundendaten in eine Excel-Datei exportieren. In Excel können Sie dann die Kundendaten, die in die Anforderung auf Datenübertragbarkeit aufgenommen werden sollen, bearbeiten und in einem gängigen, maschinenlesbaren Format, wie z. B. .csv oder .xml, speichern. Weitere Informationen finden Sie unter [Exportieren Ihrer Geschäftsdaten nach Excel](/dynamics365/business-central/about-export-data).

In ***Dynamics 365 for Talent*** können Sie die Option [Personensuchbericht erweitern](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) verwenden, um Informationen zu erfassen, die für den Antrag einer betroffenen Person auf eine Kopie ihrer personenbezogenen Daten hilfreich sind.

### <a name="rectifying-customer-data"></a>Berichtigen von Kundendaten

***Dynamics 365 for Customer Engagement*** gibt Ihnen folgende Möglichkeiten, ungenaue oder unvollständige Kundendaten zu korrigieren oder Kundendaten zu löschen:

- Suchen Sie nach Kundendaten mit den unter „Kundendaten finden“ genannten Möglichkeiten und bearbeiten Sie die Daten direkt in Kundenbindungsformularen. Änderungen können auf einer einzigen Zeilenebene oder direkt in mehreren Zeilen vorgenommen werden.
- Für die Massenverarbeitung mehrerer Customer Engagement-Berichte können Sie das Microsoft Office-Add-In verwenden, um Daten nach Microsoft Excel zu exportieren, Ihre Änderungen vorzunehmen und die geänderten Daten aus Excel in Dynamics 365 for Customer Engagement zu importieren.

Darüber hinaus haben Sie in Dynamics 365 for Marketing auch folgende Optionen:

- Aktualisieren meiner Datenzielseite, indem Sie einzelne oder mehrere Zeilen direkt bearbeiten
- Vorbereiten einer [Abonnementcenter](/dynamics365/customer-engagement/marketing/set-up-subscription-center)-Seite, die so viele editierbare Kontaktfelder wie möglich enthält. Diese Seite ermöglicht einem Endbenutzer, seine eigenen Informationen so weit wie möglich zu aktualisieren.

***Dynamics 365 Customer Service Insights*** bietet auch Funktionen, mit denen Organisationen [Kundendaten korrigieren oder ändern](/dynamics365/ai/customer-service-insights/gdpr-summary) können.

In ***Dynamics 365 for Finance and Operations** _ können Sie auch [_Anpassungstools*](/dynamics365/unified-operations/dev-itpro/dev-tools/developer-home-page) verwenden, aber die Entscheidung und Umsetzung liegt in Ihrer Verantwortung.

***Dynamics 365 Business Central*** bietet zwei Möglichkeiten, ungenaue oder unvollständige Kundendaten zu korrigieren.

Um mehrere Business Central-Datensätze schnell in großen Mengen zu bearbeiten, können Sie Listen mit dem [Business Central Excel-Add-In](/dynamics365/business-central/finance-analyze-excel#the--excel-add-in) nach Excel exportieren, um mehrere Datensätze zu korrigieren, und dann die geänderten Daten aus Excel in Business Central veröffentlichen. Weitere Informationen finden Sie unter [Exportieren Ihrer Geschäftsdaten nach Excel](/dynamics365/business-central/about-export-data).

Sie können Kundendaten, die in einem beliebigen Feld gespeichert sind, z. B. Informationen über einen Kunden in der Kundenkarte, ändern, indem Sie das Datenelement, das die betroffenen personenbezogenen Daten enthält, manuell bearbeiten. Für Details siehe [Eingabe von Daten](/dynamics365/business-central/ui-enter-data).

#### <a name="brief-note-about-modifying-entries-in-business-transactions"></a>Kurzer Hinweis zum Ändern von Einträgen in geschäftlichen Transaktionen

Für die Integrität eines Ressourcen-Planungssystems eines Unternehmens sind Transaktionsdatensätze, wie z. B. allgemeine Buchungen, Debitorenbuchungen und Steuerbuchungen, unerlässlich. Personenbezogene Daten, die Teil einer finanziellen oder anderen Transaktion sind, werden im Ist-Zustand für die Einhaltung von Finanzgesetzen (z. B. Steuergesetze), die Verhinderung von Betrug (z. B. Security Audit Trail) oder die Einhaltung von Branchenzertifizierungen aufbewahrt. Daher beschränken Dynamics 365 for Finance and Operations und Dynamics 365 Business Central das Ändern von Daten in solchen Datensätzen.

Wenn Sie personenbezogene Daten in Geschäftsdatensätzen speichern, besteht die einzige Möglichkeit, die Verarbeitung personenbezogener Daten zu korrigieren, zu löschen oder einzuschränken, um dem Antrag einer betroffenen Person nachzukommen, darin, die [Anpassungsfunktionen](/dynamics365/business-central/dev-itpro/index) von Dynamics 365 Business Central zu verwenden. [Die Entscheidung, einen Antrag einer betroffenen Person auf Änderung zur berücksichtigen,](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#reasons-why-certain-personal-data-may-not-be-modified-or-deleted) sowie dessen Umsetzung liegt in Ihrer Verantwortung.

### <a name="restricting-the-processing-of-customer-data"></a>Einschränken der Verarbeitung von Kundendaten

Wenn Sie einen Antrag einer betroffenen Person auf Einschränkung der Verarbeitung von Kundendaten erhalten, können Sie die betroffenen Kundendaten einfach aus dem Onlinedienst extrahieren und in einem separaten Container (d. h. Vor-Ort-Speicherung oder separater Webdienst mit Datenisolierung) speichern, der von den Verarbeitungsfunktionen einer beliebigen Cloud-Anwendung isoliert ist.

Alternative Mechanismen wie z. B. Datenverarbeitungsblocks werden von ***Dynamics 365 Business Central*** angeboten, wo den Benutzern die Möglichkeit geboten wird, bestimmte Datensätze zu blockieren. Einzelheiten finden Sie unter [Datenverarbeitung für eine betroffene Person einschränken](/dynamics365/business-central/admin-responding-to-requests-about-personal-data#restrict-data-processing-for-a-data-subject). Wenn ein Datensatz als gesperrt markiert ist, stellt Dynamics 365 Business Central die Verarbeitung der Kundendaten der betroffenen Person ein. Sie können keine neuen Transaktionen anlegen, die einen gesperrten Datensatz verwenden; z. B. können Sie keine neue Rechnung für einen Kunden erstellen, wenn entweder der Kunde oder der Verkäufer gesperrt ist.

### <a name="deleting-customer-data"></a>Löschen von Kundendaten

Wenn eine betroffene Person Sie auffordert, ihre Kundendaten zu löschen, gibt es mehrere Möglichkeiten, dies zu tun:

- Für die Massenverarbeitung mehrerer Dynamics 365-Berichte können Sie das Microsoft Office-Add-In verwenden, um Daten nach Microsoft Excel zu exportieren, Ihre Änderungen vorzunehmen und die geänderten Daten aus Excel in den Onlinedienst zu importieren.
- Sie können Kundendaten, die in einem beliebigen Feld gespeichert sind, löschen, indem Sie die zu löschenden Daten suchen und dann das Datenelement, das die Zielkundendaten enthält, manuell löschen, z. B. durch ein endgültiges Löschen des Kontaktdatensatzes, der die betroffene Person repräsentiert, und anderer Datensätze, die personenbezogene Daten enthalten.

Darüber hinaus wird durch das Löschen eines Kontakts für Dynamics 365 Marketing sichergestellt, dass auch ausgehende Marketinginteraktionsdaten mit personenbezogene Daten entfernt werden. Für alle benutzerdefinierten Felder oder Entitäten müssen Sie Ihr System so anpassen, dass es alle Kundendaten aus zugehörigen Datensätzen löscht und/oder deren Verknüpfung mit dem Kontaktdatensatz löscht, sodass alle personenbezogenen Daten entfernt werden. Kunden, die das Echtzeit-Marketingmodul verwenden, sollten auch ein Supportticket mit ihrer Löschanfrage einreichen, damit alle Echtzeitinteraktionsdaten entfernt werden. Weitere Informationen finden Sie im [Entwicklerhandbuch (Marketing)](/dynamics365/customer-engagement/marketing/developer/marketing-developer-guide).

***Dynamics 365 Customer Service Insights*** bietet Unternehmen auch die Möglichkeit, [Kundendaten zu löschen](/dynamics365/ai/customer-service-insights/gdpr-delete).

Alternativ können Sie in ***Dynamics 365 for Finance and Operations** _ auch [_Anpassungstools*](/dynamics365/unified-operations/dev-itpro/dev-tools/developer-home-page) verwenden, um Kundendaten zu löschen/ändern.

Wenn eine betroffene Person Sie auffordert, seine/ihre personenbezogenen Daten zu löschen, die in Ihren Kundendaten enthalten sind, gibt es in ***Dynamics 365 Business Central*** mehrere Möglichkeiten, diese Anforderung zu erfüllen:

- Um mehrere Business Central-Datensätze schnell in großen Mengen zu bearbeiten, können Sie Daten mit dem [Business Central Excel-Add-In](/dynamics365/business-central/finance-analyze-excel#the--excel-add-in) nach Excel exportieren, um mehrere Datensätze zu löschen, und dann die Änderungen aus Excel in Business Central veröffentlichen. Weitere Informationen finden Sie unter [Exportieren Ihrer Geschäftsdaten nach Excel](/dynamics365/business-central/about-export-data).
- Sie können in jedem Feld gespeicherte Kundendaten löschen, indem Sie das Datenelement, das die Zielkundendaten enthält, manuell löschen. Für Details siehe [Eingabe von Daten](/dynamics365/business-central/ui-enter-data).
- Sie können Kundendaten direkt löschen, indem Sie z. B. einen Kontakt löschen und anschließend den Batchauftrag „Protokolleinträge zu abgebrochenen Interaktionen löschen“ ausführen, um Interaktionen für diesen Kontakt zu löschen.
- Sie können [Dokumente löschen](/dynamics365/business-central/admin-manage-documents), die Kundendaten enthalten, z. B. Notizen und gebuchte Verkaufs- und Eingangsrechnungen.

Neben der Massen- oder Einzellöschung diskreter Datensätze ist zu beachten, dass nur gekündigte Mitarbeiter aus ***Dynamics 365 for Talent*** vollständig gelöscht werden können. [Folgen Sie diesen Schritten, um gekündigte Mitarbeiter zu löschen](/dynamics365/unified-operations/dev-itpro/gdpr/respond-dsr-request-talent#additional-notes-that-apply-to-requests-for-personal-data).

### <a name="exporting-customer-data"></a>Exportieren von Kundendaten

Um auf eine Anforderung auf Datenübertragbarkeit zu reagieren, können Kundendaten in ***Dynamics 365 for Customer Engagement*** mit Hilfe der umfassenden Exportfunktionen der Einheit exportiert werden. Kundendaten können in eine statische Excel-Datei exportiert werden, um die Datenübertragbarkeit zu erleichtern. Mit Excel können Sie dann die personenbezogenen Daten, die in die Anforderung auf Datenübertragbarkeit aufgenommen werden sollen, bearbeiten und dann in einem gängigen, maschinenlesbaren Format wie .csv oder.xml speichern.

Zusätzlich wird für Dynamics 365 for Marketing eine [dedizierte API](/dynamics365/customer-engagement/marketing/developer/retrieve-interactions-contact) bereitgestellt, über die der Kunde Erweiterungen erstellen kann, die zusätzliche Datensätze von erfassten Kundeninteraktionen, die personenbezogene Daten enthalten können, abrufen. Die API lädt alle relevanten Informationen aus dem Back-End-System und fasst sie zu einem einzigen, portablen Dokument zusammen.

Für ***Dynamics 365 Customer Service Insights*** können Sie zum [Exportieren von Kundendaten](/dynamics365/ai/customer-service-insights/gdpr-export) das Azure-Verwaltungsportal verwenden.

***Dynamics 365 for Finance and Operations*** bietet [Datenverwaltungs- und Integrationsentitäten, die bereitgestellte Entitäten, neu erstellte Entitäten oder erweiterte Entitäten für einen wiederholbaren Export personenbezogener Daten nach Excel oder eine Reihe anderer gängiger Formate mit [Datenimport- und -exportaufträgen](/dynamics365/unified-operations/dev-itpro/data-entities/data-import-export-job) ermöglichen.  Alternativ können viele Listen in eine statische Excel-Datei exportiert werden, um einen Antrag auf Datenübertragbarkeit zu erleichtern. Werden Kundendaten auf diese Weise nach Excel exportiert, können Sie die personenbezogenen Daten, die in den Antrag auf Datenübertragbarkeit aufgenommen werden sollen, bearbeiten und die Datei dann in einem gängigen, maschinenlesbaren Format, wie z. B. CSV oder XML, speichern.

Sowohl Dynamics 365 for Finance and Operations als auch ***Dynamics 365 for Talent*** bieten einen Personensuchbericht an, um der betroffenen Person die Daten bereitzustellen, die Sie als personenbezogene Daten klassifiziert haben.

***Dynamics 365 Business Central*** bietet die folgenden Funktionen:

- Sie können Kundendaten in eine Excel-Datei exportieren. In Excel können Sie dann die Kundendaten, die in die Anforderung auf Datenübertragbarkeit aufgenommen werden sollen, bearbeiten und in einem gängigen, maschinenlesbaren Format, wie z. B. .csv oder .xml, speichern. Weitere Informationen finden Sie unter [Exportieren Ihrer Geschäftsdaten nach Excel](/dynamics365/business-central/about-export-data).
- Sie können Kundendaten in eine Excel-Datei exportieren. In Excel können Sie dann die Kundendaten, die in die Anforderung auf Datenübertragbarkeit aufgenommen werden sollen, bearbeiten und in einem gängigen, maschinenlesbaren Format, wie z. B. .csv oder .xml, speichern. Weitere Informationen finden Sie unter [Exportieren Ihrer Geschäftsdaten nach Excel](/dynamics365/business-central/about-export-data).


## <a name="part-2-responding-to-dsrs-for-system-generated-logs"></a>Teil 2: Reagieren auf Anträge betroffener Personen für vom System generierte Protokolle

Microsoft bietet Ihnen außerdem die Möglichkeit, auf vom System erzeugte Protokolle zuzugreifen, sie zu exportieren und zu löschen, die nach der weit gefassten Definition der DSGVO als "personenbezogene Daten" gelten können. Beispiele für vom System generierte Protokolle, die unter der DSGVO als personenbezogen angesehen werden können:

- Daten zu Produkt- und Dienstnutzung, z. B. Aktivitätsprotokolle
- Suchanfragen und Abfragedaten von Benutzern
- Daten, die durch Produkte und Dienste als Produkt der Systemfunktionalität und Interaktion von Benutzern oder anderen Systemen erzeugt werden

Die Möglichkeit, Daten in vom System generierten Protokollen einzuschränken oder zu korrigieren, wird nicht unterstützt. Daten in vom System generierten Protokollen geben auf Fakten basierende Aktionen innerhalb der Microsoft-Cloud und Diagnosedaten wieder, und Änderungen an diesen Daten würden den historischen Datensatz von Aktionen kompromittieren und das Betrugs- und Sicherheitsrisiko erhöhen.

### <a name="accessing-and-exporting-system-generated-logs"></a>Zugreifen auf und Exportieren von vom System generierte(n) Protokolle(n)

Administratoren können auf vom System generierte Protokolle zugreifen, die mit der Nutzung von Dynamics 365-Diensten und -Anwendungen durch einen bestimmten Benutzer verbunden sind. So greifen Sie auf vom System generierte Protokolle zu und exportieren diese:

1. Gehen Sie zum [Microsoft Service Trust-Portal](https://servicetrust.microsoft.com/) und melden Sie sich mit den Anmeldeinformationen des globalen Dynamics 365-Administrators an.
2. In der **Datenschutz**-Dropdownliste klicken Sie am oberen Rand der Seite auf **Antrag einer betroffenen Person**.
3. Auf der Seite **Antrag einer betroffenen Person** unter **Vom System generierte Protokolle** klicken Sie auf **Datenprotokollexport**.
    > [!NOTE]
    > Der **Datenprotokollexport** wird angezeigt. Beachten Sie, dass eine Liste der von Ihrer Organisation übermittelten Datenexportanfragen angezeigt wird.
4. Wenn Sie eine neue Anforderung für einen Benutzer erstellen möchten, klicken Sie auf **Anforderung zum Exportieren von Daten erstellen**.

Nachdem Sie eine neue Anforderung erstellt haben, wird sie auf der Seite **Datenprotokollexport** aufgelistet, wo Sie ihren Status nachverfolgen können. Nachdem eine Anforderung abgeschlossen ist, können Sie auf einen Link klicken, um auf die vom System generierten Protokolle zuzugreifen, die innerhalb von 30 Tagen nach Erstellung der Anforderung in den Azure-Speicherort Ihrer Organisation exportiert werden. Die Daten werden in gängigen, maschinenlesbaren Dateiformaten wie JSON oder XML gespeichert. Wenn Sie kein Azure-Konto und keinen Azure-Speicherort haben, müssen Sie ein Azure-Konto und/oder einen Azure-Speicherort für Ihre Organisation erstellen, damit das Datenprotokollexport-Tool die vom System generierten Protokolle exportieren kann.

Azure unterstützt diese Anforderung, indem es Ihrer Organisation ermöglicht, die Daten im nativen JSON-Format in den angegebenen Azure Storage-Container zu exportieren. Artikel [Einführung in Microsoft Azure Storage – Blob-Speicher](/azure/storage/common/storage-introduction#blob-storage). Die abgerufenen Daten enthalten keine Daten, die die Sicherheit und Stabilität des Diensts beeinträchtigen können.

> [!IMPORTANT]
> Sie müssen ein Mandantenadministrator sein, um Benutzerdaten aus dem Mandanten exportieren können.

Die folgende Tabelle fasst den Zugriff auf und den Export von vom System generierten Protokollen zusammen:

| **Frage** | **Answer** |
|:----|:---|
|**Wie lange benötigt das Tool für den Datenprotokollexport von Microsoft, um eine Anforderung abzuschließen?**| Dies hängt von mehreren Faktoren ab. In den meisten Fällen sollte der Abschluss in einem oder zwei Tagen möglich sein, es kann jedoch auch bis zu 30 Tage dauern. |
|**Welches Format weist die Ausgabe auf?**| Die Ausgabe ist in maschinenlesbaren Dateien, z. B. XML, CSV oder JSON, strukturiert. |
|**Welche Daten werden durch das Tool für den Datenprotokollexport ausgegeben?**| Das Datenprotokollexport-Tool gibt vom System generierte Protokolle aus, die von Microsoft gespeichert werden. Die exportierten Daten erstrecken sich über verschiedene Microsoft-Dienste wie Office 365, Azure und Dynamics. |
|***Wer hat Zugriff auf das Tool für den Datenprotokollexport und kann Zugriffsanforderungen für vom System generierte Protokolle senden?**| Globale Administratoren von Dynamics 365 haben Zugriff auf das DSGVO-Hilfsprogramm zur Verwaltung von Protokollen. |
|**Wie werden Daten an den Benutzer zurückgegeben?**| Die Daten werden an den Azure-Speicherort Ihrer Organisation exportiert; es ist Sache der Administratoren in Ihrer Organisation, zu bestimmen, wie sie diese Daten den Benutzern anzeigen/bereitstellen. |
|**Wie werden Daten in vom System generierten Protokollen dargestellt?**| Beispiel für ein vom System generiertes Protokoll im JSON-Format: <br><br> "DateTime": "2017-04-28T12:09:29-07:00", <br> "AppName": "SharePoint", <br> "Action": "OpenFile", <br> "IP": "154.192.13.131", <br> "DevicePlatform": "Windows 1.0.1607" |

### <a name="deleting-system-generated-logs"></a>Löschen von vom System generierten Protokollen

Wenn Sie vom System generierte Protokolle löschen möchten, die über eine Zugriffsanforderung abgerufen wurden, müssen Sie den Benutzer aus dem Dienst entfernen und dessen Azure Active Directory-Konto endgültig löschen. Anweisungen dazu, wie ein Benutzer dauerhaft gelöscht wird, finden Sie im Abschnitt [Schritt 5: Löschen](gdpr-dsr-azure.md#step-5-delete) im Thema „Leitfaden für Anträge betroffener Personen in Azure“. Es ist wichtig zu beachten, dass das Benutzerkonto nach dem Initiieren des Löschvorgangs endgültig gelöscht wird. Durch die dauerhafte Löschung eines Benutzerkontos werden die Daten des Benutzers – mit Ausnahme von Daten, die für die Sicherheit und die Stabilität des Dienstes wesentlich sind – innerhalb von 30 Tagen aus vom System generierten Protokollen für fast alle Dynamics 365-Dienste entfernt.

## <a name="learn-more"></a>Mehr erfahren

- [Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
