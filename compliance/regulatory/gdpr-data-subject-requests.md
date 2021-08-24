---
title: Anträge betroffener Personen im Rahmen der DSGVO und des CCPA
keywords: Microsoft 365, Microsoft 365 Education, Microsoft 365-Dokumentation, DSGVO, CCPA
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
titleSuffix: Microsoft GDPR
description: Hier erfahren Sie, wie Sie DSRs im Rahmen der Datenschutz-Grundverordnung (DSGVO) und der kalifornischen Verbraucherschutzgesetzgebung (CCPA) mithilfe von Microsoft-Produkten und -Diensten durchführen.
ms.custom: seo-marvel-mar2020
hideEdit: true
ms.openlocfilehash: b5ef9464a686a5f2c8823f196408fd71026fa52d
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58479837"
---
# <a name="data-subject-requests-and-the-gdpr-and-ccpa"></a>Anträge betroffener Personen im Rahmen der DSGVO und des CCPA

Die Datenschutz-Grundverordnung (DSGVO) führt neue Regeln für Organisationen ein, die Waren und Dienstleistungen in der Europäischen Union (EU) anbieten oder Daten von in der EU ansässigen natürlichen Personen erfassen und analysieren, unabhängig von deren Wohnsitz und Unternehmenssitz. Weitere Details finden Sie in der [Zusammenfassung zum Thema DSGVO](gdpr.md).

In ähnlicher Weise bietet der California Consumer Privacy Act (CCPA) den kalifornischen Verbrauchern Datenschutzrechte und -pflichten, einschließlich von Rechten, die den Rechten von betroffenen Personen der DSGV entsprechen, wie z. B. das Recht auf Löschung, Zugriff und Empfang (Portabilität) der persönlichen Informationen.  Das CCPA ermöglicht außerdem bestimmte Offenlegungen, Schutz vor Diskriminierung bei der Wahl von Ausübungsrechten und Deaktivierungs-/Aktivierungsanforderungen für bestimmte Datentransfers, die als "Verkäufe" eingestuft werden. Dieses Dokument führt Sie zu Informationen zur Bearbeitung von Anfragen von betroffenen Personen (Datensubjekten) im Rahmen der DSGVO unter Verwendung von Microsoft-Produkten und -Diensten.

- [Office 365](gdpr-dsr-Office365.md)
- [Azure](gdpr-dsr-Azure.md)
- [Intune](gdpr-dsr-Intune.md)
- [Dynamics 365](gdpr-dsr-Dynamics365.md)
- [Visual Studio-Produktfamilie](gdpr-dsr-visual-studio-family.md)
- [Azure DevOps Services](gdpr-dsr-vsts.md)
- [Microsoft-Support und Professional Services](gdpr-dsr-prof-services.md)

## <a name="terminology"></a>Begrifflichkeiten

Hilfreiche Definitionen für DSGVO-Ausdrücke, die in diesem Dokument verwendet werden:

- *Datenverantwortlicher (Verantwortlicher)*: eine juristische Person, Behörde, Einrichtung oder andere Stelle, die allein oder gemeinsam mit anderen über die Zwecke und Mittel der Verarbeitung von personenbezogenen Daten entscheidet.  
- *Personenbezogene Daten* und *betroffene Person*: alle Informationen, die sich auf eine identifizierte oder identifizierbare natürliche Person (betroffene Person) beziehen; als identifizierbar wird eine natürliche Person angesehen, die direkt oder indirekt identifiziert werden kann.  
- *Auftragsverarbeiter*: eine natürliche oder juristische Person, Behörde, Einrichtung oder andere Stelle, die personenbezogene Daten im Auftrag des Verantwortlichen verarbeitet.  
- *Kundendaten*: Daten, die bei den tagtäglichen Geschäftsausführung erstellt und gespeichert werden.

## <a name="what-is-a-dsr"></a>Was sind Anfragen von betroffenen Personen?

Die Allgemeine Datenschutz-Grundverordnung (DSGVO) räumt natürlichen Personen (in der Verordnung als betroffene Personen bezeichnet) das Recht ein, vom Arbeitgeber oder einer anderen Einrichtung oder Organisation (Datenverantwortlicher oder Verantwortlicher) erhobene personenbezogene Daten zu verwalten. Die DSGVO gewährt betroffenen Personen bestimmte Rechte an ihren personenbezogenen Daten. Zu diesen Rechten gehören das Abrufen von Kopien der Daten, das Anfordern von Änderungen daran, die Beschränkung deren Verarbeitung, das Löschen der Daten oder das Empfangen der Daten in einem elektronischen Format, damit sie auf einen anderen Controller verschoben werden können.

Der California Consumer Privacy Act (CCPA) bietet den kalifornischen Verbrauchern Datenschutzrechte und -pflichten, einschließlich von Rechten, die den Rechten von betroffenen Personen der DSGVO entsprechen, wie z. B. das Recht auf Löschung, Zugriff und Empfang (Portabilität) der persönlichen Informationen.  

Als Verantwortlicher sind Sie verpflichtet, jede Datensubjektanfrage sofort zu überprüfen und darauf zu reagieren, und zwar entweder, indem Sie die angeforderte Maßnahme ergreifen oder indem Sie erläutern, warum der Anfrage der betroffenen Person seitens des Verantwortlichen nicht nachgekommen werden kann. Ein Verantwortlicher sollte sich mit seinen eigenen Rechts- oder Complianceberatern hinsichtlich der geeigneten Disposition bezüglich einer bestimmten Datensubjektanfrage beraten.

Es sind möglicherweise mehrere Prozesse involviert, um eine Datensubjektanfrage entsprechend der DSGVO-Complianceregeln Ihrer Organisation zu erfüllen.
  
- **Ermittlung**. Der Vorgang, mit dem ermittelt wird, welche Daten zum Erfüllen einer Datensubjektanfrage erforderlich sind.
- **Zugriff**. Abrufen der ermittelten Daten und deren potenzielle Übermittlung an das Datensubjekt.
- **Berichtigung**. Implementieren von Änderungen oder andere angeforderte Änderungen der personenbezogenen Daten.
- **Einschränkung**. Ändern des Zugriffs oder der Verarbeitung von personenbezogenen Daten durch Einschränken des Zugriffs oder Entfernen von Daten aus der Microsoft-Cloud.
- **Export**. Bereitstellen personenbezogener Daten in einem „strukturierten, häufig verwendeten, maschinell lesbaren Format“ an die betroffene Person gemäß dem „Recht auf Datenübertragbarkeit“ gemäß DSGVO.
- **Delete** Permanentes Entfernen personenbezogener Daten aus der Microsoft-Cloud.

## <a name="specific-dsr-considerations"></a>Spezifische Überlegungen zu Datensubjektanfragen

### <a name="insights-generated-by-microsoft-products-or-services"></a>Von Microsoft-Produkten oder -Diensten generierte Erkenntnisse

[Einblicke](/microsoft-365/compliance/gdpr-dsr-office365#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365) können durch Dienste (MyAnalytics usw.) generiert werden. Office 365 umfasst Onlinedienste, die Benutzern und Organisationen, die diese Dienste nutzen, Einblicke gewähren. Die von diesen Diensten generierten Daten erzeugen möglicherweise personenbezogene Daten, die für eine Datensubjektanfrage relevant sind. Folgen Sie dem Link in der nachstehenden Liste, um Details zu dienstspezifischen Datensubjektanfrage-Prozessen anzuzeigen.  

### <a name="dsrs-for-system-generated-logs"></a>Datensubjektanfragen bezüglich vom System generierten Protokollen

Protokolle und verwandte Daten, die von Microsoft generiert werden, enthalten möglicherweise Daten, die gemäß der DSGVO-Definition "personenbezogene Daten" sind. Daten in vom System generierten Protokollen einzuschränken oder zu korrigieren, wird nicht unterstützt. Daten in vom System generierten Protokollen geben auf Fakten basierende Aktionen innerhalb der Microsoft-Cloud sowie Diagnosedaten wieder. Änderungen würden die historische Erfassung von Aktionen kompromittieren und das Betrugs- und Sicherheitsrisiko erhöhen. Microsoft bietet die Möglichkeit, auf vom System generierte Protokolle zuzugreifen, sie zu exportieren und zu löschen, wenn dies zur Erfüllung einer Datensubjektanfrage erforderlich ist. Beispiele für solche Daten sind unter anderem:  

- Daten zu Produkt- und Dienstnutzung, z. B. Aktivitätsprotokolle
- Suchanfragen und Abfragedaten von Benutzern
- Daten, die durch Produkte und Dienste infolge der Systemfunktionalität und Interaktion von Benutzern oder anderen Systemen erzeugt werden.  

### <a name="yammer-and-kaizala"></a>Yammer und Kaizala

Durch das Löschen eines Benutzerkontos werden keine vom System generierten Protokolle für Yammer und Kaizala entfernt. Informationen zum Entfernen der Daten aus diesen Anwendungen finden Sie in einer der folgenden Ressourcen:

- [Verwalten von DSGVO-Datensubjektanforderungen in Yammer Enterprise](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)
- [Exportieren oder Löschen von Organisationsdaten eines Benutzers in Kaizala](/office365/kaizala/export-or-delete-a-user-s-data)

### <a name="national-clouds"></a>Nationale Clouds

In einigen nationalen Clouds muss ein globaler IT-Administrator vom System generierte Protokolle löschen.

### <a name="microsoft-services"></a>Microsoft Services

Wenn Ihre Organisation oder Ihre Benutzer sich mit Microsoft in Verbindung setzen, um Support für Microsoft-Produkte und -Dienste zu erhalten, können einige der übermittelten Daten personenbezogene Daten enthalten. Weitere Informationen finden Sie unter [Microsoft-Support und Professional Services für Anfragen von betroffenen Personen im Rahmen der DSGVO](gdpr-dsr-prof-services.md).

### <a name="microsoft-controller-products"></a>Produkte, deren Datenverantwortlicher Microsoft ist

Unter bestimmten Umständen greifen die Benutzer Ihrer Organisation auf Microsoft-Produkte oder -Dienste zu, für die Microsoft der Datenverantwortliche ist. In diesen Fällen müssen Ihre Benutzer die eigenen Datensubjektanfragen direkt an Microsoft stellen, und Microsoft erfüllt die Anforderungen direkt an den Benutzer.

### <a name="third-party-products"></a>Produkte von Drittanbietern

Datensubjektanfragen für Produkte und Dienste von Drittanbietern, auf die über die Microsoft-Kontoauthentifizierung zugegriffen wird, sollten direkt an den entsprechenden Drittanbieter gerichtet werden.

## <a name="data-subject-request-admin-tools"></a>Werkzeuge zur Verwaltung von Anträgen betroffener Personen

- **Security & Compliance Center**: Vom Benutzer generierte Daten werden aus dem [Security & Compliance Center](https://aka.ms/stpsecurityandcompliance) oder durch anwendungsinterne Features exportiert.
- **Azure AD Admin Center**: Löschen Sie ein Datensubjekt aus Azure Active Directory und den zugehörigen Diensten mithilfe von [Azure AD Admin Center](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/Allusers/menuId/).
- **Microsoft-Datenprotokollexport**: Vom System generierte Protokolle können von Mandantenadministratoren mithilfe von [Microsoft-Datenprotokollexport](https://aka.ms/MicrosoftGDPR) exportiert werden.

## <a name="learn-more"></a>Weitere Informationen

- [Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
