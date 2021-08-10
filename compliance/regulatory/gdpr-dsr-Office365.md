---
title: Anträge betroffener Personen für Office 365 im Rahmen der DSGVO und des CCPA
description: Verstehen der Benutzerrechte gemäß DSGVO und CCPA und wie Office 365 Unternehmen bei der Suche von und Reaktion auf Anträge betroffener Personen unterstützt.
keywords: Office 365, Anträge betroffener Personen, Microsoft 365, Microsoft 365 Education, Microsoft 365-Dokumentation, DSGVO, CCPA
localization_priority: Priority
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
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 0d48c7bc2c4b3b2dbfa8e4c102e22853c3ba5cc242cfebdf31ee4c6149f95756
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54293569"
---
# <a name="office-365-data-subject-requests-for-the-gdpr-and-ccpa"></a>Anträge betroffener Personen für Office 365 im Rahmen der DSGVO und des CCPA

## <a name="introduction-to-dsrs"></a>Einführung in Anträge betroffener Personen

Die [Datenschutz-Grundverordnung (DSGVO)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) der Europäischen Union gewährt Personen (die in den Bestimmungen als *betroffene Personen* bezeichnet werden) das Recht zum Verwalten der personenbezogenen Daten, die von einem Arbeitgeber oder von einer anderen Art von Behörde oder Organisation (als *Datenverantwortlicher* oder nur *Verantwortlicher* bezeichnet) erfasst werden. Personenbezogene Daten sind im Rahmen der DSGVO weitgefasst als Daten definiert, die sich auf eine identifizierte oder identifizierbare natürliche Person beziehen. Die DSGVO erteilt betroffenen Personen bestimmte Rechte im Hinblick auf ihre personenbezogenen Daten; dazu gehören das Kopieren der personenbezogenen Daten, das Anfordern von Korrekturen, das Einschränken ihrer Verarbeitung, das Löschen oder das Erhalten in einem elektronischen Format, damit sie zu einem anderen Datenverantwortlichen bewegt werden können. Eine formale Anfrage einer betroffenen Person an einen Datenverantwortlichen im Hinblick auf eine bestimmte Aktion bezüglich ihrer personenbezogenen Daten wird als *Antrag einer betroffenen Person* bezeichnet. Der Verantwortliche ist verpflichtet, jeden Antrag einer betroffenen Person unverzüglich zu bearbeiten und angemessen zu reagieren, entweder indem die angeforderte Aktion ausgeführt wird oder indem eine Erklärung abgegeben wird, warum dem Antrag der betroffenen Person vom Verantwortlichen nicht Folge geleistet werden kann. Ein Verantwortlicher sollte sich bezüglich der sachgerechten Bearbeitung der einzelnen Anträge betroffener Personen an seine eigenen Rechts- und Compliance-Berater wenden.

In ähnlicher Weise bietet der California Consumer Privacy Act (CCPA) den kalifornischen Verbrauchern Datenschutzrechte und -pflichten, einschließlich von Rechten, die den Rechten von betroffenen Personen der DSGV entsprechen, wie z. B. das Recht auf Löschung, Zugriff und Empfang (Portabilität) der persönlichen Informationen. Das CCPA ermöglicht außerdem bestimmte Offenlegungen, Schutz vor Diskriminierung bei der Wahl von Ausübungsrechten und Deaktivierungs-/Aktivierungsanforderungen für bestimmte Datentransfers, die als "Verkäufe" eingestuft werden. Die Definition von "Verkäufe" umfasst die Freigabe von Daten für eine angemessene Gegenleistung. Weitere Informationen zum CCPA finden Sie im ["California Consumer Privacy Act](offering-ccpa.md) und in den [häufig gestellten Fragen zum California Consumer Privacy Act](ccpa-faq.yml).

In diesem Leitfaden wird erläutert, wie Office 365-Produkte, -Dienste und -Verwaltungstools verwendet werden können, um in Antwort auf Anträge betroffener Personen personenbezogene Daten oder personenbezogene Informationen zu finden und zu verarbeiten. Dazu zählen insbesondere die Suche, der Zugriff und die Verarbeitung von personenbezogenen Daten oder personenbezogene Informationen, die in der Microsoft-Cloud gespeichert sind. Im Folgenden finden Sie eine kurze Übersicht der in diesem Leitfaden beschriebenen Prozesse:

- **Ermittlung:** Verwenden Sie Such- und Ermittlungstools, um Kundendaten leichter zu finden, die möglicherweise Gegenstand eines Antrags einer betroffenen Person sind. Sobald potenziell geeignete Dokumente gefunden wurden, können Sie eine oder mehrere der Aktionen für Anträge betroffener Personen durchführen, die in den folgenden Schritten beschrieben sind, um auf den Antrag der betroffenen Person zu reagieren. Andernfalls können Sie bestimmen, dass der Antrag nicht den Unternehmensrichtlinien für die Reaktion auf Anträge betroffener Personen entspricht.
- **Zugriff:** Rufen Sie personenbezogene Daten ab, die sich in der Microsoft Cloud befinden, und erstellen Sie eine Kopie, die der betroffenen Person zur Verfügung gestellt werden kann, sofern dies beantragt wurde.
- **Berichtigung:** Nehmen Sie gegebenenfalls Änderungen an den personenbezogenen Daten vor oder führen Sie andere Aktionen aus, die für die Daten angefordert werden.
- **Einschränkung:** Schränken Sie die Verarbeitung personenbezogener Daten entweder durch Zurückziehen von Lizenzen für verschiedene Microsoft-Clouddienste oder durch Deaktivieren der gewünschten Dienste wo möglich ein. Des Weiteren können Sie Daten aus der Microsoft-Cloud entfernen und diese lokal oder an einem anderen Ort aufbewahren.
- **Löschung:** Entfernen Sie personenbezogene Daten, die sich in der Microsoft-Cloud befinden, dauerhaft.
- **Exportieren/Empfangen (Portierbarkeit):** Stellen Sie der betroffenen Person eine elektronische Kopie (in einem maschinenlesbaren Format) von personenbezogenen Daten oder persönlichen Informationen zur Verfügung. Personenbezogene Informationen gemäß CCPA sind alle Informationen, die eine identifizierte oder identifizierbare Person betreffen. Es wird nicht zwischen privaten, öffentlichen oder beruflichen Rollen einer Person unterschieden. Der definierte Begriff "persönliche Informationen" entspricht in etwa dem Begriff "persönliche Daten" unter der DSGVO. Allerdings umfasst das CCPA auch Familien- und Haushaltsdaten. Weitere Informationen zum CCPA finden Sie im ["California Consumer Privacy Act](offering-ccpa.md) und in den [häufig gestellten Fragen zum California Consumer Privacy Act](ccpa-faq.yml).

### <a name="terminology"></a>Terminologie

Im Folgenden finden Sie Definitionen von Begriffen der DSGVO, die für diesen Leitfaden relevant sind.

- **Datenverantwortlicher:** Eine natürliche oder juristische Person, öffentliche Behörde, Agentur oder andere Stelle, die allein oder gemeinsam mit anderen die Zwecke und Mittel der Verarbeitung personenbezogener Daten bestimmt. Sofern die Zwecke und Mittel der Verarbeitung durch das Recht der Union oder der Mitgliedstaaten bestimmt werden, können der Datenverantwortliche bzw. die spezifischen Kriterien für dessen Benennung durch das Recht der Union oder des Mitgliedstaats angegeben werden.
- **Personenbezogene Daten und betroffene Person:** Alle Informationen über eine identifizierte oder identifizierbare natürliche Person ("betroffene Person"). Eine identifizierbare natürliche Person ist eine Person, die direkt oder indirekt, insbesondere durch Zuordnung zu einer Kennung wie einem Namen, zu einer Kennnummer, zu Standortdaten, zu einer Online-Kennung oder zu einem oder mehreren besonderen Merkmalen identifiziert werden kann, die Ausdruck der physischen, physiologischen, genetischen, psychischen, wirtschaftlichen, kulturellen oder sozialen Identität dieser natürlichen Person sind.
- **Verarbeiter:** Eine natürliche oder juristische Person, öffentliche Behörde, Agentur oder andere Stelle, die personenbezogene Daten im Auftrag des Verantwortlichen verarbeitet.
- **Kundendaten:** Alle Daten, einschließlich aller Text-, Ton-, Video- oder Bilddateien, und Software, die Microsoft von einem Kunden oder in dessen Namen durch die Nutzung des Enterprise-Dienstes bereitgestellt werden. Kundendaten umfassen sowohl (1) Informationen zur Identifikation von Endbenutzern (z. B. Benutzernamen und Kontaktinformationen in Azure Active Directory) als auch Kundeninhalte, die ein Kunde in einen bestimmten Dienst hochlädt oder in diesem erstellt (z. B. Kundeninhalte in einem Word- oder Excel-Dokument oder im Text einer Exchange Online-E-Mail; Kundeninhalte, die einer SharePoint Online-Site hinzugefügt oder in einem OneDrive for Business-Konto gespeichert werden).
- **Vom System generierte Protokolle:** Von Microsoft generierte Protokolle und verbundene Daten, die Microsoft bei der Bereitstellung von Enterprise-Diensten für Benutzer unterstützen. Vom System generierte Protokolle enthalten in erster Linie pseudonymisierte Daten, z. B. eindeutige Bezeichner (in der Regel eine vom System generierte Zahl), die nicht von sich aus eine Einzelperson identifizieren, aber dazu verwendet werden, die Enterprise-Dienste für Benutzer bereitzustellen. Vom System generierte Protokolle enthalten u. U. auch Informationen zur Identifikation von Endbenutzern, z. B. einen Benutzernamen.

### <a name="how-to-use-this-guide"></a>Verwenden dieses Leitfadens

Um das Auffinden relevanter Informationen zu Ihrem jeweiligen Anwendungsfall leichter zu gestalten, haben wir diesen Leitfaden in vier Bereiche unterteilt.

- **[Teil 1: Reagieren auf Anträge betroffener Personen bezüglich Kundendaten](#part-1-responding-to-dsrs-for-customer-data)***Kundendaten* sind Daten, die im täglichen Betrieb Ihres Geschäfts in Office 365 erzeugt und gespeichert werden. Beispiele für die am häufigsten verwendeten Office 365-Anwendungen, die Daten erstellen, sind Word, Excel, PowerPoint, Outlook und OneNote. Office 1 besteht auch aus Anwendungen, wie SharePoint Online, Microsoft Teams und Forms, mit denen Sie besser mit anderen Personen zusammenarbeiten können. In Teil 365 dieses Leitfadens wird erläutert, wie Sie auf Daten aus Office 365-Anwendungen zugreifen können, die verwendet wurden, um Daten in Office 365-Onlinediensten zu erstellen und zu speichern, und diese berichtigen, einschränken, löschen und exportieren können. Es werden Produkte und Dienste behandelt, für die Microsoft im Auftrag Ihrer Organisation als Verarbeiter agiert, aufgrund dessen Ihrem Mandantenadministrator die Funktionalität für Anträge betroffener Personen zur Verfügung gestellt wird.
- **[Teil 2: Reagieren auf Anträge betroffener Personen bezüglich von Office 365 generierten Erkenntnissen](#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365):** Office 365 stellt über Dienste wie Delve, MyAnalytics und Workplace Analytics bestimmte Erkenntnisse bereit. Die Art und Weise, wie diese Erkenntnisse generiert werden und wie auf Anträge betroffener Personen reagiert werden kann, wird in Teil 2 dieses Leitfadens erläutert.
- **[Teil 3: Reagieren auf Anträge betroffener Personen bezüglich vom System generierter Protokolle](#part-3-responding-to-dsrs-for-system-generated-logs):** Wenn Sie Office 365 Enterprise-Dienste verwenden, generiert Microsoft einige Informationen, wie etwa Dienstprotokolle, in denen die Verwendung oder Leistung der Funktionen in den Onlinediensten aufgezeichnet wird. Die meisten dieser von Diensten generierten Daten enthalten von Microsoft generierte pseudonyme Bezeichner. Diese Kategorie wird daher in diesem Dokument allgemein als *vom System generierte Protokolle* bezeichnet. Obwohl diese Daten ohne Zuhilfenahme zusätzlicher Informationen keiner bestimmten betroffenen Person zugeordnet werden können, können manche dieser Daten gemäß der Definition personenbezogener Daten in der DSGVO als personenbezogen gelten. In Teil 3 dieses Leitfadens wird erläutert, wie Sie auf vom System generierte Protokolle zugreifen und diese exportieren und löschen können.
- **[Teil 4: Weitere Ressourcen, die bei Anträgen betroffener Personen hilfreich sind](#part-4-additional-resources-to-assist-you-with-dsrs)** – In Teil 4 dieses Leitfadens wird eine Auswahl von Szenarios gegeben, in denen Microsoft als Verantwortlicher agiert, wenn bestimmte Office 365-Produkte und Dienste verwendet werden.

> [!NOTE]
> Wenn Benutzer in Ihrer Organisation Microsoft Office 365-Produkte und -Dienste verwenden, sind meistens Sie der Verantwortliche und Microsoft ist der Auftragsverarbeiter. Als Verantwortlicher ist es Ihre Pflicht, der betroffenen Person direkt zu antworten. In Teil 1 bis 3 dieses Leitfadens finden Sie detaillierte Informationen zu den technischen Möglichkeiten Ihrer Organisation, auf Anträge betroffener Personen zu reagieren. In einigen seltenen Fällen, wenn Benutzer ganz bestimmte Office 365-Produkte und -Dienste nutzen, ist jedoch Microsoft der Verantwortliche. Dann sind die Informationen in Teil 4 dieser Anleitung relevant, denn dort wird erläutert, wie betroffene Personen ihre Anträge direkt an Microsoft stellen können.

### <a name="office-365-national-clouds"></a>Nationale Office 365-Clouds

Die Microsoft Office 365-Dienste sind auch in den folgenden nationalen Cloud-Umgebungen verfügbar: [Office 365 Deutschland](/microsoft-365/admin/admin-overview/learn-about-office-365-germany), [Office 365 betrieben von 21Vianet (China)](/microsoft-365/admin/services-in-china/services-in-china) und [Office 365 US Government](https://www.microsoft.com/microsoft-365/government/compare-office-365-government-plans). Die meisten der in diesem Dokument beschriebenen Richtlinien für die Verwaltung von Anträgen betroffener Personen gelten für diese nationalen Cloud-Umgebungen. Aufgrund des isolierten Charakters dieser Umgebungen gibt es jedoch einige Ausnahmen. Soweit für einen bestimmten Unterabschnitt wichtig, werden diese Ausnahmen in einem entsprechenden Vermerk genannt.

### <a name="hybrid-deployments"></a>Hybridbereitstellungen

Ihre Organisation kann aus Microsoft-Angeboten bestehen, die eine Kombination aus cloudbasierten Diensten und lokalen Serverprodukten sind. Im Allgemeinen versteht man unter einer hybriden Bereitstellung die gemeinsame Nutzung von Benutzerkonten (Identitätsmanagement) und Ressourcen (wie Postfächer, Websites und Daten), die sowohl in der Cloud als auch lokal vorhanden sind. Gängige hybride Szenarien sind u. a:

- Exchange-Hybridbereitstellungen, bei denen einige Benutzer über ein lokales Postfach und andere Benutzer über ein Exchange Online-Postfach verfügen,
- SharePoint-Hybridbereitstellungen, bei denen Website- und Dateiserver vor Ort sind und OneDrive for Business-Konten in Office 365 sind,
- das lokale Identitätsmanagementsystem (Active Directory), das mit dem Azure Activity Directory synchronisiert ist, bei dem es sich um den zugrunde liegenden Verzeichnisdienst in Office 365 handelt.

Wenn Sie auf einen Antrag einer betroffenen Person reagieren, müssen Sie möglicherweise zunächst feststellen, ob sich Daten, die für den Antrag der betroffenen Person relevant sind, in der Microsoft-Cloud oder in Ihrer lokalen Organisation befinden. Anschließend können Sie die entsprechenden Schritte unternehmen, um auf diesen Antrag zu reagieren. Der Office 365-Leitfaden zu Anträgen betroffener Personen (dieser Leitfaden) bietet Anleitungen für die Reaktion auf Anträge bezüglich cloudbasierter Daten. Informationen zu Daten in Ihrer lokalen Organisation finden Sie unter [DSGVO für lokale Office-Server](/Office365/Enterprise/gdpr-for-office-servers).

## <a name="part-1-responding-to-dsrs-for-customer-data"></a>Teil 1: Reagieren auf Anträge betroffener Personen bezüglich Kundendaten

Die Anleitung zum Reagieren auf Anträge betroffener Personen bezüglich Kundendaten ist in die folgenden vier Abschnitte unterteilt:

- [Reagieren auf Anträge betroffener Personen mit dem eDiscovery-Tool für die Inhaltssuche](#using-the-content-search-ediscovery-tool-to-respond-to-dsrs)
- [Reagieren auf Anträge betroffener Personen mithilfe der In-App-Funktionalität](#using-in-app-functionality-to-respond-to-dsrs)
- [Reagieren auf Anträge betroffener Personen zur Berichtigung von Daten](#responding-to-dsr-rectification-requests)
- [Reagieren auf Anträge betroffener Personen zur Einschränkung der Datenverarbeitung](#responding-to-dsr-restriction-requests)

### <a name="how-to-determine-the-office-365-applications-that-may-be-in-scope-for-a-dsr-for-customer-data"></a>Bestimmen der Office 365-Anwendungen, die Ziel von Anträgen betroffener Person bezüglich Kundendaten sein können

Damit Sie bestimmen können, wo Sie nach personenbezogenen Daten suchen sollten oder wonach gesucht werden soll, ist es hilfreich, die Office 365-Anwendungen zu identifizieren, die Personen in Ihrem Unternehmen verwenden können, um Daten in Office 365 zu erstellen und zu speichern. So können Sie die Anzahl der Office 365-Anwendungen begrenzen, die als Ziel eines Antrags betroffener Person in Frage kommen, und bestimmen, wie Sie im Zusammenhang mit einem solchen Antrag nach personenbezogenen Daten suchen und darauf zugreifen. Genauer können Sie so entscheiden, ob Sie das Tool zur Inhaltssuche verwenden können oder ob Sie die In-App-Funktion der Anwendung verwenden müssen, in der die Daten erstellt wurden.

Eine schnelle Möglichkeit zum Identifizieren der Office 365-Anwendungen, die Personen in Ihrem Unternehmen verwenden, um Kundendaten zu erstellen, besteht darin, zu ermitteln, welche Anwendungen im Microsoft 365 Business-Abonnement Ihres Unternehmens enthalten sind. Zu diesem Zweck können Sie im Office 365-Administratorportal auf Benutzerkonten zugreifen und die Produktlizenzinformationen einsehen. Siehe [Benutzern Lizenzen zuweisen](/microsoft-365/admin/manage/assign-licenses-to-users).

## <a name="using-the-content-search-ediscovery-tool-to-respond-to-dsrs"></a>Reagieren auf Anträge betroffener Personen mit dem eDiscovery-Tool für die Inhaltssuche

Bei der Suche nach personenbezogenen Daten innerhalb des größeren Satzes von Daten, die Ihre Organisation bei der Verwendung von Office 365 erstellt und speichert, sollten Sie zuerst die Anwendungen berücksichtigen, die Personen vermutlich verwendet haben, um die Daten zu erstellen, nach denen Sie suchen. Microsoft schätzt, dass mehr als 90 % der Daten einer Organisation, die in Office 365 gespeichert sind, in Word, Excel, PowerPoint, OneNote und Outlook erstellt werden. In diesen Office-Programmen erstellte Dokumente sind höchstwahrscheinlich auf einer SharePoint Online-Website, im OneDrive for Business-Konto eines Benutzers oder im Exchange Online-Postfach eines Benutzers gespeichert, auch wenn sie über Microsoft 365-Apps for Enterprise oder eine unbefristete Office-Lizenz erworben wurden. Dies bedeutet, dass Sie das eDiscovery-Tool für die Inhaltssuche verwenden können, um in SharePoint Online-Websites, OneDrive for Business-Konten und Exchange Online-Postfächern (einschließlich der mit Microsoft 365-Gruppen, Microsoft Teams und EDU-Aufgaben verknüpften Websites und Postfächer) nach Dokumenten und Postfachelementen zu suchen (oder andere Aktionen im Zusammenhang mit Anträgen betroffener Personen auszuführen), die für den von Ihnen untersuchten Antrag einer betroffenen Person relevant sein könnten. Sie können das Tool für die Inhaltssuche auch verwenden, um Kundendaten zu ermitteln, die in anderen Office 365-Anwendungen erstellt wurden.

Die folgende Liste identifiziert die Office 365-Anwendungen, mit denen Personen Kundeninhalte erstellen, die über die Inhaltssuche ermittelt werden können. In diesem Abschnitt des Leitfadens zu Anträgen betroffener Personen wird erläutert, wie Sie mit diesen Office 365-Anwendungen erstellte Daten ermitteln, exportieren und löschen können und wie Sie darauf zugreifen können.

Anwendungen, bei denen die Inhaltssuche verwendet werden kann, um Kundendaten zu finden:

- Kalender
- Excel
- Office Lens
- OneDrive for Business
- OneNote
- Outlook/Exchange
- Personen
- PowerPoint
- SharePoint
- Skype for Business
- Aufgaben
- Teams
- To Do
- Video
- Visio
- Word

> [!NOTE]
> Das eDiscovery-Tool für die Inhaltssuche ist in [Office 365, das von 21Vianet (China) betrieben wird,](/microsoft-365/admin/services-in-china/services-in-china) nicht verfügbar. Dies bedeutet, dass Sie dieses Tool nicht verwenden können, um Kundendaten in den in Tabelle 1 dargestellten Office 365-Anwendungen zu suchen und zu exportieren. Sie können jedoch das direkte eDiscovery-Tool in Exchange Online verwenden, um nach Inhalten in Benutzerpostfächern zu suchen. Sie können auch das eDiscovery Center in SharePoint Online verwenden, um nach Inhalten auf SharePoint-Websites und in OneDrive-Konten zu suchen. Alternativ können Sie einen Dokumentbesitzer bitten, Ihnen beim Suchen und Ändern oder Löschen von Inhalten zu helfen oder diese bei Bedarf zu exportieren. Weitere Informationen finden Sie unter:
> 
> * [Erstellen einer In-Situ-eDiscovery-Suche](/exchange/create-in-place-ediscovery-search-exchange-2013-help)
> * [Einrichten eines eDiscovery Center in SharePoint Online](https://support.office.com/article/Set-up-an-eDiscovery-Center-in-SharePoint-Online-A18F8975-AA7F-43B4-A7D6-001D14744D8E)

### <a name="using-content-search-to-find-personal-data"></a>Verwenden der Inhaltssuche zum Suchen nach personenbezogenen Daten

Der erste Schritt der Reaktion auf einen Antrag einer betroffenen Person ist die Suche nach den personenbezogenen Daten, die Gegenstand des Antrags einer betroffenen Person sind. Hierbei kann das Office 365 eDiscovery-Tool zum Suchen nach personenbezogenen Daten (in den gesamten Daten Ihres Unternehmens in Office 365) oder direkt die systemeigene Anwendung verwendet werden, in der die Daten erstellt wurden. In diesem ersten Schritt – Suchen und Überprüfen der betroffenen personenbezogenen Daten – können Sie bestimmen, ob ein Antrag einer betroffenen Person die Anforderungen Ihres Unternehmens zur Annahme oder zur Ablehnung eines Antrags einer betroffenen Person erfüllt. Sie können beispielsweise nach dem Suchen und Überprüfen der betroffenen personenbezogenen Daten feststellen, dass die Anforderungen Ihres Unternehmens nicht erfüllt sind, da der Antrag die Rechte und Freiheiten anderer beeinträchtigen könnte oder da die enthaltenen personenbezogenen Daten Teil einer Geschäftsaufzeichnung sind, an deren Bewahrung Ihr Unternehmen ein berechtigtes Geschäftsinteresse hat.

Wie bereits erwähnt, schätzt Microsoft, dass mehr als 90 % der Daten einer Organisation mit Office-Anwendungen, wie Word und Excel, erstellt werden. Das bedeutet, dass Sie die Inhaltssuche im Security & Compliance Center verwenden können, um nach dem Großteil der Daten zu suchen, die im Zusammenhang mit einem Antrag einer betroffenen Person stehen.

In diesem Leitfaden wird davon ausgegangen, dass Sie oder die Person, die nach personenbezogenen Daten sucht, die für einen Antrag einer betroffenen Person möglicherweise relevant sind, mit dem Tool zur Inhaltssuche im Security & Compliance Center vertraut sind oder bereits Erfahrungen damit gemacht haben. Hinweise zur allgemeinen Verwendung des Leitfadens zur Inhaltssuche finden Sie unter [Inhaltssuche in Office 365](/microsoft-365/compliance/content-search). Achten Sie darauf, dass der Person, die die Suche ausführt, die erforderlichen Berechtigungen im Security & Compliance Center zugewiesen wurden. Diese Person sollte als Mitglied der Rollengruppe eDiscovery-Manager im Security & Compliance Center hinzugefügt werden; siehe [Zuweisen von eDiscovery-Berechtigungen im Security & Compliance Center](/microsoft-365/compliance/assign-ediscovery-permissions). Sie können ebenfalls andere Personen in Ihrer Organisation zur Rollengruppe eDiscovery-Manager hinzufügen, die an Anträgen betroffener Personen beteiligt sind, damit diese die erforderlichen Aktionen ausführen können, z. B. Vorschau und Export von Suchergebnissen im Tool zur Inhaltssuche. Beachten Sie jedoch, dass ein eDiscovery-Manager alle Inhaltsspeicherorte in Ihrer Organisation einsehen kann, einschließlich derer, die nicht mit Anträgen betroffener Personen im Zusammenhang stehen. Dies können Sie verhindern, indem Sie Compliance-Beschränkungen einrichten (wie [hier](#set-up-compliance-boundaries-to-limit-the-scope-of-content-searches) beschrieben).

Nachdem Sie die Daten gefunden haben, können Sie die bestimmte Aktion ausführen, die im Rahmen eines Antrags einer betroffenen Person angefordert wurde.

> [!NOTE]
> In Office 365 Deutschland ist das Security & Compliance Center hier verfügbar: https://protection.office.de.

#### <a name="searching-content-locations"></a>Durchsuchen von Speicherorten für Inhalte

Sie können nach folgenden Typen von Speicherorte für Inhalte mit dem Tool zur Inhaltssuche suchen.

- Exchange Online-Postfächer. Dies umfasst mit Microsoft 365-Gruppen und Microsoft Teams verbundene Postfächer
- Öffentliche Ordner in Exchange Online
- SharePoint Online-Websites. Dies umfasst mit Microsoft 365-Gruppen und Microsoft Teams verbundene Websites
- OneDrive for Business-Konten

> [!NOTE]
> In diesem Leitfaden wird davon ausgegangen, dass alle Daten, die möglicherweise für die Untersuchung im Rahmen eines Antrags einer betroffenen Person relevant sind, in Office 365 bzw. in anderen Worten in der Microsoft-Cloud gespeichert sind. Daten, die auf dem lokalen Computer des Benutzers oder lokal auf den Dateiservern Ihrer Organisation gespeichert sind, sind von der Untersuchung im Rahmen eines Antrags einer betroffenen Person bezüglich in Office 365 gespeicherten Daten ausgenommen. Anleitungen zur Reaktion auf Anträge betroffener Personen bezüglich Daten in lokalen Organisationen finden Sie unter [DSGVO für lokale Office-Server](/Office365/Enterprise/gdpr-for-office-servers).

#### <a name="tips-for-searching-content-locations"></a>Tipps zum Durchsuchen von Speicherorten für Inhalte

- Durchsuchen Sie zunächst alle Speicherorte für Inhalte in Ihrem Unternehmen (die Sie in einem einzigen Suchvorgang durchsuchen können), um schnell zu ermitteln, welche Speicherorte Elemente enthalten, die Ihrer Suchabfrage entsprechen. Anschließend können Sie die Suche erneut durchführen und den Suchbereich auf die bestimmten Speicherorte beschränken, die die relevanten Elemente enthalten.
- Verwenden Sie Suchstatistiken, um die am häufigsten verwendeten Speicherorte zu identifizieren, die Elemente enthalten, die der Suchabfrage entsprechen. Siehe [Anzeigen der Schlüsselwortstatistik für Inhaltssuchergebnisse](/microsoft-365/compliance/view-keyword-statistics-for-content-search).
- Suchen Sie im Überwachungsprotokoll nach zuletzt verwendeten Dateien und Ordneraktivitäten des Benutzers, der Gegenstand des Antrags einer betroffenen Person ist. Durch das Durchsuchen des Überwachungsprotokolls erhalten Sie eine Liste der Überwachungseinträge, die den Namen und den Speicherort der Ressourcen enthalten, mit denen der Benutzer zuletzt interagiert hat. Sie können diese Informationen evtl. verwenden, um eine Inhaltssuchabfrage zu erstellen. Siehe [Durchsuchen des Überwachungsprotokolls im Security & Compliance Center](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance).

#### <a name="building-search-queries-to-find-personal-data"></a>Erstellen von Suchabfragen zur Suche nach personenbezogenen Daten

Der untersuchte Antrag einer betroffenen Person enthält wahrscheinlich Bezeichner, die Sie bei der Suchabfrage zum Suchen nach den personenbezogenen Daten verwenden können. Im Folgenden finden Sie einige allgemeine Bezeichner, die Sie in einer Suchabfrage zum Suchen nach personenbezogenen Daten verwendet werden können:

- E-Mail-Adresse oder Alias
- Telefonnummer
- Postanschrift
- Mitarbeiter-ID-Nummer
- Nationale IDs oder die EU-Mitgliedversion einer Sozialversicherungsnummer

Der untersuchte Antrag einer betroffenen Person enthält wahrscheinlich einen Bezeichner und weitere Details zu den personenbezogenen Daten, die Gegenstand des Antrags sind, die Sie in einer Suchabfrage verwenden können.

Die Suche nur nach einer E-Mail-Adresse oder der Mitarbeiter-ID liefert wahrscheinlich mehrere Ergebnisse. Um den Bereich Ihrer Suche einzugrenzen und die relevantesten Inhalte für den Antrag einer betroffenen Person zu erhalten, können Sie der Suchabfrage Bedingungen hinzufügen. Wenn Sie eine Bedingung hinzufügen, sind das Schlüsselwort und die Suchbedingung logisch durch den booleschen Operator **AND** miteinander verbunden. Das bedeutet, dass nur Elemente in den Suchergebnissen zurückgegeben werden, die *sowohl* dem Schlüsselwort als auch der Bedingung entsprechen.

In der folgenden Tabelle werden einige Bedingungen aufgelistet, die Sie verwenden können, um den Bereich einer Suche einzugrenzen. Die Tabelle enthält auch die Werte, die Sie für jede Bedingung verwenden können, um nach bestimmten Dokumenttypen und Postfachelementen zu suchen.

***Tabelle 2: Bereich der Suche durch Verwenden von Bedingungen eingrenzen***

| Bedingung | Beschreibung | Beispiel für einen Bedingungswert |
| :--- | :--- |:--- |
| Dateityp | Die Erweiterung eines Dokuments oder einer Datei. Verwenden Sie diese Bedingung zum Suchen nach Office-Dokumente und -Dateien, die von Office 365-Anwendungen erstellt wurden. Verwenden Sie diese Bedingungen bei der Suche nach Dokumenten auf SharePoint Online-Websites und OneDrive for Business-Konten.<br/>Die entsprechende Dokumenteigenschaft ist der Dateityp. <br/>Eine vollständige Liste der Dateierweiterungen, nach denen Sie suchen können, finden Sie unter „Standardmäßig durchforstete Dateinamenerweiterungen und analysierte Dateitypen in SharePoint“](https://technet.microsoft.com/library/jj219530.aspx).|&nbsp;&bull;&nbsp;&nbsp;csv: Sucht nach durch Trennzeichen getrennten Dateien (CSV-Dateien); Excel-Dateien können im CSV-Format gespeichert werden, und CSV-Dateien können ganz einfach in Excel importiert werden.<br><br>&bull;&nbsp;&nbsp;docx: sucht nach Word-Dateien <br><br>&bull;&nbsp;&nbsp;mpp: sucht nach Projektdateien<br/><br>&bull;&nbsp;&nbsp;one: sucht nach OneNote-Dateien <br><br>&bull;&nbsp;&nbsp;pdf: Sucht nach Dateien, die in einem PDF-Format gespeichert sind. <br><br>&bull;&nbsp;&nbsp;pptx: sucht nach PowerPoint-Dateien <br><br>&bull;&nbsp;&nbsp;xlxs: sucht nach Excel-Dateien <br><br>&bull;&nbsp;&nbsp;vsd: sucht nach Visio-Dateien <br><br>&bull;&nbsp;&nbsp;wmv: sucht nach Windows Media Video-Dateien <br>|
| Nachrichtentyp | Der E-Mail-Nachrichtentyp, nach dem gesucht wird. Verwenden Sie diese Bedingung, um Postfächer nach Kontakten (Personen), Besprechungsaufgaben (Kalender) oder Skype for Business-Unterhaltungen zu durchsuchen. Die entsprechende E-Mail-Eigenschaft ist *kind*.|&bull;&nbsp;&nbsp;*contacts: sucht in der Liste „Meine Kontakte (Personen)“ eines Postfachs <br><br>&bull;&nbsp;&nbsp;* email: sucht nach E-Mail-Nachrichten <br><br>&bull;&nbsp;&nbsp;*im: sucht nach Skype for Business-Unterhaltungen <br><br>&bull;&nbsp;&nbsp;* meetings: durchsucht Termine und Besprechungsanfragen (Kalender) <br><br>&bull;&nbsp;&nbsp;*tasks: Sucht in der Liste „Meine Aufgaben“ (Aufgaben); dieser Wert gibt auch Aufgaben zurück, die in Microsoft To-Do erstellt wurden.<br>|
| Compliancetag |Die Beschriftung, die einer E-Mail-Nachricht oder einem Dokument zugewiesen wird. Beschriftungen werden verwendet, um E-Mails und Dokumente für die Datenkontrolle zu klassifizieren, die durch diese Beschriftung definiert wird, und um Aufbewahrungsregeln durchzusetzen. Verwenden Sie diese Bedingung, um nach Elementen suchen, denen automatisch oder manuell eine Beschriftung zugewiesen wurde.<br/>Dies ist eine nützliche Bedingung für Untersuchungen im Rahmen von Anträgen betroffener Personen, da Ihr Unternehmen möglicherweise Bezeichnungen verwendet, um Inhalte zu klassifizieren, die im Zusammenhang mit Datenschutz stehen, bzw. Inhalte, die personenbezogene Daten oder vertrauliche Informationen enthalten. Weitere Informationen finden Sie im Abschnitt „Verwenden der Inhaltssuche zum Auffinden aller Inhalte, denen eine bestimmte Bezeichnung zugewiesen wurde“ unter [Informationen zu Aufbewahrungsrichtlinien und Aufbewahrungsbezeichnungen](/microsoft-365/compliance/labels)|compliancetag="personenbezogene Daten"|
||||

Es gibt viele weitere E-Mail- und das Dokumenteigenschaften und Suchbedingungen, die Sie verwenden können, um komplexere Suchabfragen zu erstellen. Weitere Informationen finden Sie in den folgenden Abschnitten im Hilfethema [Schlüsselwortabfragen und Suchbedingungen für die Inhaltssuche](/microsoft-365/compliance/keyword-queries-and-search-conditions).

- [Durchsuchbare E-Mail-Eigenschaften](/microsoft-365/compliance/keyword-queries-and-search-conditions)
- [Durchsuchbare Websiteeigenschaften (Dokumenteigenschaften)](/microsoft-365/compliance/keyword-queries-and-search-conditions)
- [Suchbedingungen](/microsoft-365/compliance/keyword-queries-and-search-conditions)

#### <a name="searching-for-personal-data-in-sharepoint-lists-discussions-and-forms"></a>Suchen nach personenbezogenen Daten in SharePoint-Listen, -Diskussionen und -Formularen

Zusätzlich zum Durchsuchen personenbezogener Daten in Dokumenten können Sie auch die Inhaltssuche verwenden, um nach anderen Datentypen zu suchen, die mit systemeigenen SharePoint Online-Apps erstellt wurden. Dies umfasst Daten, die mit SharePoint-Listen, -Diskussionen und -Formularen erstellt wurden. Wenn Sie eine Inhaltssuche ausführen und SharePoint Online-Websites (oder OneDrive for Business-Konten) durchsuchen, werden Daten aus Listen, Diskussionen und Formularen in den Suchergebnissen angezeigt, die den Suchkriterien entsprechen.

##### <a name="examples-of-search-queries"></a>Beispiele für Suchabfragen

Hier sind einige Beispiele für Suchabfragen, die Schlüsselwörter und Bedingungen verwenden, um nach personenbezogenen Daten als Reaktion auf einen Antrag einer betroffenen Person zu suchen. Die Beispiele zeigen zwei Versionen der Abfrage: eine der Schlüsselwortsyntax (in der die Bedingung im Schlüsselwortfeld enthalten ist) und eine mit der GUI-basierten Version der Abfrage mit Bedingungen.

##### <a name="example-1"></a>Beispiel 1

In diesem Beispiel werden Excel-Dateien auf SharePoint Online-Websites und in OneDrive for Business-Konten zurückgegeben, die die angegebene E-Mail-Adresse enthalten. Möglicherweise werden Dateien zurückgegeben, wenn die E-Mail-Adresse in den Metadaten angezeigt wird.

***Schlüsselwortsyntax***

```Query
pilar@contoso.com AND filetype="xlxs"
```

***GUI***

![Beispiel-Schlüsselwortdialog 1](../media/O365-DSR-Doc_image18.png)

##### <a name="example-2&quot;></a>Beispiel 2

In diesem Beispiel werden Excel- oder Word-Dateien auf SharePoint Online-Websites und in OneDrive for Business-Konten wiedergegeben, die die angegebene Mitarbeiter-ID oder das Geburtsdatum enthalten.

```
(98765 OR &quot;01-20-1990") AND (filetype="xlxs" OR filetype="docx")
```

***GUI***

![Beispiel-Schlüsselwortdialog 2](../media/O365-DSR-Doc_image19.png)

##### <a name="example-3"></a>Beispiel 3

In diesem Beispiel werden E-Mail-Nachrichten zurückgegeben, die die angegebene ID-Nummer enthalten, bei der es sich hier um eine französische Sozialversicherungsnummer (INSEE) handelt.

```Query
"1600330345678 97" AND kind="email"
```

***GUI***

![Beispiel-Schlüsselwortdialog 3](../media/O365-DSR-Doc_image20.png)

#### <a name="working-with-partially-indexed-items-in-content-search"></a>Arbeiten mit teilweise indizierten Elemente in der Inhaltssuche

Teilweise indizierte Elemente (auch als *nicht indizierte Elemente* bezeichnet) sind Exchange Online-Postfachelemente und Dokumente in SharePoint Online- und OneDrive for Business-Sites, die aus irgendeinem Grund nicht für die Suche indiziert wurden, was bedeutet, dass Sie nicht mithilfe der Inhaltssuche durchsucht werden können. Die meisten E-Mail-Nachrichten und Websitedokumente werden erfolgreich indiziert, da sie innerhalb der [Indizierungsgrenzwerte für Office 365](/microsoft-365/compliance/limits-for-content-search) liegen. Zu den Gründen dafür, dass E-Mail-Nachrichten oder Dateien für die Suche nicht indiziert werden, zählt unter anderem Folgendes:

- Der Dateityp wird [für die Indizierung nicht erkannt oder nicht unterstützt](/microsoft-365/compliance/partially-indexed-items-in-content-search). Manchmal wird der Dateityp zwar für die Indizierung unterstützt, aber bei einer bestimmten Datei ist ein Indizierungsfehler aufgetreten.
- E-Mail-Nachrichten verfügen über eine angefügte Datei ohne einen gültigen Handler, wie Bilddatei (dies ist die häufigste Ursache für teilweise indizierten E-Mail-Elemente).
- An E-Mails angefügt Dateien sind zu groß oder es gibt zu viele Dateianlagen.

Es wird empfohlen, dass Sie mehr über teilweise indizierte Elemente in Erfahrung bringen, damit Sie bei der Reaktion auf Anträge betroffener Personen mit ihnen arbeiten können. Weitere Informationen finden Sie unter:

- [Teilweise indizierte Elemente in der Inhaltssuche in Office 365](/microsoft-365/compliance/partially-indexed-items-in-content-search)
- [Untersuchen von teilweise indizierten Elementen in Office 365 eDiscovery](/microsoft-365/compliance/investigating-partially-indexed-items-in-ediscovery)
- [Exportieren nicht indizierter Elemente](/microsoft-365/compliance/export-search-results)

#### <a name="tips-for-working-with-partially-indexed-items"></a>Tipps für die Arbeit mit teilweise indizierten Elementen

Es ist möglich, dass die Daten, die Gegenstand einer Untersuchung im Rahmen eines Antrags einer betroffenen Person sind, in einem teilweise indizierten Element befinden. Nachfolgend einige Vorschläge für die Arbeit mit teilweise indizierten Elementen:

- Nach dem Ausführen einer Suche wird die Anzahl der geschätzten teilweise indizierten Elemente in der Suchstatistik angezeigt. Diese Schätzung enthält keine teilweise indizierten Elemente in SharePoint Online und OneDrive for Business. Exportieren Sie die Berichte für eine Inhaltssuche, um Informationen zu teilweise indizierte Elemente zu erhalten. Der Bericht **Unindexed Items.csv** enthält Informationen zu nicht indizierten Elementen, z. B. den Speicherort des Elements, die URL, wenn sich das Element in SharePoint Online oder OneDrive for Business befindet, und die Betreffzeile (für Nachrichten) oder den Namen des Dokuments. Weitere Informationen finden Sie unter [Exportieren eines Berichts der Inhaltssuche](/microsoft-365/compliance/export-a-content-search-report).

- Die Statistik und die Liste der teilweise indizierten Elemente, die mit den Ergebnissen einer Inhaltssuche zurückgegeben werden, sind alle teilweise indizierte Elemente aus den durchsuchten Speicherorten für Inhalte.

- Um teilweise indizierte Elemente abzurufen, die für eine Untersuchung im Rahmen eines Antrags einer betroffenen Person potenziell relevant sind, können Sie eine der folgenden Aktionen ausführen:

##### <a name="export-all-partially-indexed-items"></a>Exportieren aller teilweise indizierten Elemente

Sie können sowohl die Ergebnisse einer Inhaltssuche als auch die teilweise indizierten Elemente aus dem durchsuchten Inhaltsspeicherort exportieren. Sie können auch nur die teilweise indizierten Elemente exportieren. Anschließend können Sie sie in ihrer nativen Anwendung öffnen und den Inhalt überprüfen. Diese Option muss verwendet werden, um Elemente aus SharePoint Online und OneDrive for Business zu exportieren. Siehe [Exportieren von Ergebnissen der Inhaltssuche aus dem Security & Compliance Center](/microsoft-365/compliance/export-search-results).

##### <a name="export-a-specific-set-of-partially-indexed-items-from-mailboxes"></a>Exportieren einer Reihe bestimmter, teilweise indizierter Elemente aus Postfächern

Statt alle teilweise indizierten Postfachelemente aus einer Suche zu exportieren, können Sie auch eine erneute Inhaltssuche durchführen, um nach einer Liste spezifischer, teilweise indizierter Elemente zu suchen und diese dann exportieren. Dies ist nur für Postfachelemente möglich. Siehe [Vorbereiten einer CSV-Datei für eine gezielte Inhaltssuche in Office 365](/microsoft-365/compliance/csv-file-for-an-id-list-content-search).

### <a name="next-steps"></a>Nächste Schritte

Nachdem Sie die personenbezogenen Daten, die für den Antrag einer betroffenen Person relevant sind, gefunden haben, müssen Sie unbedingt die bestimmte Inhaltssuche beibehalten, die Sie verwendet haben, um die Daten zu suchen. Sie verwenden wahrscheinlich diese Suche erneut, um andere Schritte im Rahmen der Reaktion auf einen Antrag einer betroffenen Person abzuschließen, wie zum Beispiel das [Erstellen einer Kopie](#providing-a-copy-of-personal-data), das [Exportieren](#exporting-personal-data) oder das [dauerhafte Löschen](#deleting-personal-data).

### <a name="additional-considerations-for-selected-applications"></a>Zusätzliche Aspekte bei ausgewählten Anwendungen

Die folgenden Abschnitte beschreiben die Aktionen, die Sie bei der Suche nach Daten in den folgenden Office 365-Anwendungen im Auge behalten sollten.

- [Office Lens](#office-lens)
- [OneDrive for Business- und SharePoint-Oberflächeneinstellungen](#onedrive-for-business-and-sharepoint-online-experience-settings)
- [Microsoft Teams für Bildungseinrichtungen](#microsoft-teams-for-education)
- [Microsoft Aufgaben](#microsoft-to-do)
- [Skype for Business](#skype-for-business)

#### <a name="office-lens"></a>Office Lens

Eine Person mit Office Lens (eine Kamera-App, die von Geräten unter iOS, Android und Windows unterstützt wird) kann Fotos von Whiteboards, Papierdokumenten, Visitenkarten und anderen Dingen aufnehmen, die eine große Textmenge enthalten. Office Lens verwendet OCR-Technologie (optische Zeichenerkennung), mit der Text in einem Bild extrahiert und in einem Office-Dokument, z. B. einer Word-, PowerPoint- oder OneNote-Datei, oder in einer PDF-Datei gespeichert wird. Benutzer können dann die Datei, die den Text aus dem Bild enthält, in ihr OneDrive for Business-Konto in Office 365 hochladen. Das bedeutet, dass Sie das Tool für die Inhaltssuche verwenden können, um auf Daten in Dateien zuzugreifen, die aus einem Office Lens-Bild erstellt wurden, und diese suchen, löschen und exportieren können. Weitere Informationen zu Office Lens finden Sie unter:

- [Office Lens für iOS](https://support.microsoft.com/office/microsoft-office-lens-for-ios-fbdca5f4-1b1b-4391-a931-dc1c2582397b)
- [Office Lens für Android](https://support.office.com/article/Office-Lens-for-Android-ec124207-0049-4201-afaf-b5874a8e6f2b)
- [Office Lens für Windows](https://support.microsoft.com/office/office-lens-for-windows-577ec09d-8da2-4029-8bb7-12f8114f472a)

#### <a name="onedrive-for-business-and-sharepoint-online-experience-settings"></a>OneDrive for Business- und SharePoint Online-Oberflächeneinstellungen

Diese Dienste speichern neben den von Benutzern erstellten Dateien, die in OneDrive for Business-Konten und auf SharePoint Online-Websites gespeichert sind, Informationen über den Benutzer, die verwendet werden, um die verschiedenen Oberflächen zu aktivieren. Benutzer, die weiterhin Ihrem Unternehmen zugehörig sind, können auf viele dieser Informationen zugreifen, indem Sie Funktionen im Produkt verwenden. Die folgenden Informationen bieten eine Anleitung zum Zugreifen auf und Anzeigen und Exportieren von OneDrive for Business- und SharePoint Online-Anwendungsdaten.

##### <a name="sharepoint-user-profiles"></a>SharePoint-Benutzerprofile

Mit dem Delve-Profil des Benutzers können Benutzer Eigenschaften verwalten, die im SharePoint Online-Benutzerprofil gespeichert werden, einschließlich Geburtstag, Mobiltelefonnummer (und andere Kontaktinformationen), „Über mich“, Projekte, Qualifikationen und Kompetenzen, Schulen und Ausbildung, Interessen und Hobbys.

###### <a name="end-users"></a>Endbenutzer

Endbenutzer können auf SharePoint Online-Benutzerprofildaten mithilfe der Delve-Profiloberfläche zugreifen und diese ermitteln und berichtigen. Weitere Informationen finden Sie unter [Anzeigen und Aktualisieren Ihres Profils in Office Delve](https://support.office.com/article/view-and-update-your-profile-in-office-delve-4e84343b-eedf-45a1-aeb9-8627ccca14ba).

Eine andere Möglichkeit für Benutzer, auf ihre SharePoint-Profildaten zuzugreifen, besteht darin, zur Seite **Profil bearbeiten** in ihrem OneDrive for Business-Konto zu navigieren, auf das über den Pfad **EditProfile.aspx** unter der OneDrive for Business-Konto-URL zugegriffen werden kann. Für den Benutzer <strong>user1@contoso.com</strong> befindet sich das OneDrive for Business-Konto des Benutzers beispielsweise unter:

```http
https://contoso-my.sharepoint.com/personal/user1\_contoso\_com/\_layouts/15/OneDrive.aspx
```

Die URL für die Seite „Profil bearbeiten“ wäre:

```http
https://contoso-my.sharepoint.com/personal/user1\_contoso\_com/\_layouts/15/EditProfile.aspx
```

In Azure Active Directory erstellte Eigenschaften können nicht in SharePoint Online geändert werden. Benutzer können jedoch zur Seite **Konto** wechseln, indem sie ihr **Foto** in der Office 365-Kopfzeile anklicken und dann **Mein Konto** auswählen. Zum Ändern der Eigenschaften müssen Benutzer möglicherweise mit ihren Administratoren zusammenarbeiten, um Benutzerprofileigenschaften zu ermitteln, auf diese zuzugreifen oder diese zu berichtigen.

###### <a name="admins"></a>Administratoren

Ein Administrator kann auf Profileigenschaften im SharePoint Admin Center zugreifen und diese berichtigen. Klicken Sie im **SharePoint Admin Center** auf die Registerkarte **Benutzerprofile**. Klicken Sie auf **Benutzerprofile verwalten**, geben Sie den Namen eines Benutzers ein, und klicken Sie dann auf **Suchen**. Der Administrator kann auf jeden Benutzer mit der rechten Maustaste klicken und **Mein Profil bearbeiten** auswählen. Beachten Sie, dass in Azure Active Directory erstellte Eigenschaften nicht in SharePoint Online geändert werden können.

Ein Administrator kann alle Benutzerprofileigenschaften für einen Benutzer mit dem Cmdlet **Export-SPOUserProfile** in SharePoint Online PowerShell exportieren. Siehe [Export-SPOUserProfile](/powershell/module/sharepoint-online/export-spouserprofile).

Weitere Informationen zu Benutzerprofilen finden Sie unter [Verwalten von Benutzerprofilen im SharePoint Admin Center](/sharepoint/manage-user-profiles).

##### <a name="user-information-list-on-sharepoint-online-sites"></a>Benutzerinformationsliste auf SharePoint Online-Websites

Ein Teil des SharePoint-Benutzerprofils eines Benutzers wird mit der Benutzerinformationsliste jeder Website synchronisiert, die er besucht oder für die er Zugriffsrechte hat. Dies wird von SharePoint Online-Oberflächen, wie den Spalten „Personen“ in Dokumentbibliotheken verwendet, um grundlegende Informationen über den Benutzer anzuzeigen, z. B. den Namen des Erstellers eines Dokuments. Die Daten in einer Benutzerinformationsliste stimmen mit den im SharePoint-Benutzerprofil gespeicherten Informationen überein und werden automatisch korrigiert, wenn die Quelle geändert wird. Für gelöschte Benutzer verbleiben diese Daten in den Websites, mit denen sie interagiert haben, um die referentielle Integrität der SharePoint-Spaltenfelder zu gewährleisten. 

Administratoren können steuern, welche Eigenschaften im SharePoint Admin Center replizierbar sind. Gehen Sie zu diesem Zweck wie folgt vor:

1. Wechseln Sie zum **SharePoint Admin Center**, und wählen Sie die Registerkarte **Benutzerprofile**.
2. Wählen Sie **Benutzereigenschaften verwalten** aus, um eine Liste mit Eigenschaften anzuzeigen.
3. Wählen Sie mit der rechten Maustaste eine beliebige Eigenschaft aus, und wählen Sie **Bearbeiten** aus, um verschiedene Einstellungen anzupassen.
4. Unter **Richtlinieneinstellungen** steuert die replizierbare Eigenschaft, ob die Eigenschaft in der Benutzerinformationsliste dargestellt wird. Nicht alle Eigenschaften können entsprechend angepasst werden.

Ein Administrator kann alle Benutzerinformationseigenschaften für einen Benutzer auf einer bestimmten Seite mit dem Cmdlet **Export-SPOUserProfile** in SharePoint Online PowerShell exportieren. Siehe [Export-SPOUserProfile](/powershell/module/sharepoint-online/export-spouserinfo).

##### <a name="onedrive-for-business-experience-settings"></a>OneDrive for Business-Oberflächeneinstellungen

Die OneDrive for Business-Oberfläche eines Benutzers speichert Daten, mit denen der Benutzer nach für ihn interessantem Inhalt suchen kann. Auf die meisten dieser Daten können Endbenutzer mit Funktionen im Produkt zugreifen. Ein Administrator kann die Informationen exportieren, indem er ein [PowerShell Script](/powershell/scripting/overview) und [SharePoint Client-Side Object Model(CSOM)](/sharepoint/dev/sp-add-ins/complete-basic-operations-using-sharepoint-client-library-code)-Befehle verwendet.

Weitere Informationen zu den Einstellungen, wie diese gespeichert werden und wie Sie sie exportieren können finden Sie unter [Exportieren von OneDrive for Business-Oberflächeneinstellungen](/sharepoint/export-odfb-lists).

##### <a name="onedrive-for-business-and-sharepoint-online-search"></a>OneDrive for Business- und SharePoint Online-Suche

Die In-App-Suchoberfläche in OneDrive for Business und SharePoint Online speichert die Suchanfragen eines Benutzers 30 Tage lang, um die Relevanz der Suchergebnisse zu erhöhen. Ein Administrator kann Suchanfragen für einen Benutzer mit dem Cmdlet **Export-SPOQueryLogs** in SharePoint Online PowerShell exportieren. Siehe [Export-SPOQueryLogs](/powershell/module/sharepoint-online/export-spoquerylogs).

#### <a name="microsoft-teams-for-education"></a>Microsoft Teams für Bildungseinrichtungen

Microsoft Teams für Bildungseinrichtungen bietet zwei zusätzliche Funktionen für die Zusammenarbeit, die Lehrer und Kursteilnehmer verwenden können, die personenbezogene Daten erstellen oder speichern: Aufgaben und OneNote-Kursnotizbuch. Sie können zur Ermittlung von Daten in beiden die Inhaltssuche verwenden.

##### <a name="assignments"></a>Aufgaben

Kursteilnehmerdateien im Zusammenhang mit einer Aufgabe werden in einer Dokumentbibliothek auf der entsprechenden Teams SharePoint Online-Website gespeichert. IT-Administratoren können das Tool zur Inhaltssuche verwenden, um nach Kursteilnehmerdateien zu suchen, die mit Aufgaben verknüpft sind. Ein Administrator kann z. B. alle SharePoint Online-Websites im Unternehmen durchsuchen und den Namen und den Kurs des Kursteilnehmers oder einen Aufgabennamen in der Suchabfrage verwenden, um nach für eine Anforderung einer betroffenen Person relevante Daten zu suchen.

Andere Daten in Verbindung mit Aufgaben werden nicht auf der SharePoint Online-Website des Kursteams gespeichert, was bedeutet, dass sie nicht mit der Inhaltssuche gefunden werden können. Dazu gehören:

- Dateien, die der Lehrer Kursteilnehmern im Rahmen der Aufgabe zuweist
- Kursteilnehmernoten und Feedback des Lehrers
- Die Liste der von jedem Teilnehmer für eine Aufgabe eingereichten Dokumente
- Aufgabenmetadaten

Bei diesen Datentypen muss ein IT-Administrator oder ein Datenbesitzer (z. B. ein Lehrer) möglicherweise zur Aufgabe im Kursteam navigieren, um nach für einen Antrag einer betroffenen Person relevanten Daten zu suchen.

##### <a name="onenote-class-notebook"></a>OneNote-Kursnotizbuch

Das OneNote-Kursnotizbuch wird auf der SharePoint Online-Website des Kursteams gespeichert. Jeder Kursteilnehmer in einem Kurs verfügt über ein privates Notizbuch, das für den Lehrer freigegeben ist. Es gibt auch eine Inhaltsbibliothek, in der Lehrer Dokumente für Kursteilnehmer freigeben kann, und einen gemeinsamen Bereich für alle Kursteilnehmer eines Kurses. Daten im Zusammenhang mit diesen Funktionen können mit der Inhaltssuche gefunden werden.

Hier finden Sie eine spezifische Anleitung für ein Kursnotizbuch.

1. Führen Sie eine Inhaltssuche mit folgenden Suchkriterien durch:

   - Durchsuchen Sie alle SharePoint Online-Websites.
   - Schließen Sie den Namen des Kursteams als Suchschlüsselwort ein; z. B. "9 C Biologie".

2. Lassen Sie sich eine Vorschau der Suchergebnisse anzeigen, und suchen Sie nach dem Element, das dem Kursnotizbuch entspricht.
3. Wählen Sie dieses Element aus, und kopieren Sie dann den Ordnerpfad, der im Detailbereich angezeigt wird. Dies ist der Stammordner des Kursnotizbuchs.
4. Bearbeiten Sie die Suche, die Sie in Schritt 1 erstellt haben, ersetzen Sie den Namen des Kurses in der Schlüsselwortabfrage durch den Ordnerpfad des Kursnotizbuchs, und fügen Sie vor den Ordnerpfad die Websiteeigenschaft **path** ein, z. B. **path: "<https://contosoedu.onmicrosoft.com/sites/9C> Biology/SiteAssets/9C Biology Notebook/"**. Achten Sie darauf, dass Sie die Anführungszeichen und den Schrägstrich am Ende einfügen.
5. Fügen Sie eine Suchbedingung hinzu, wählen Sie die Dateitypbedingung aus, und verwenden Sie dabei „one“ als Dateityp. Dadurch werden alle OneNote-Dateien in den Suchergebnissen zurückgegeben. Die sich daraus ergebende Schlüsselwortsyntax würde [folgendermaßen aussehen](#building-search-queries-to-find-personal-data):

   ```Query
   path:"<https://contosoedu.onmicrosoft.com/sites/9C> Biology/SiteAssets/9C Biology Notebook/" AND filetype="one"
   ```

6. Führen Sie die Inhaltssuche erneut aus. Die Suchergebnisse sollten alle OneNote-Dateien für das Kursnotizbuch aus dem Kursteam enthalten.

#### <a name="microsoft-to-do"></a>Microsoft Aufgaben

Aufgaben (auch *To-Dos* genannt, die in *Aufgabenlisten* gespeichert werden) in Microsoft To Do werden als Aufgaben im Exchange Online-Postfach des Benutzers gespeichert. Das bedeutet, dass Sie das Tool für die Inhaltssuche zum Suchen nach, Zugreifen auf und Löschen und Exportieren von Aufgaben verwenden können. Weitere Informationen finden Sie unter [Einrichten von Microsoft To Do](https://support.microsoft.com/office/set-up-microsoft-to-do-490c1a8c-2333-4952-8125-841afadb9620).

#### <a name="skype-for-business"></a>Skype for Business

Im Folgenden finden Sie einige zusätzliche Informationen dazu, wie Sie auf personenbezogene Daten in Skype for Business zugreifen können und diese anzeigen und exportieren können.

- Einer Besprechung angefügte Dateien werden 180 Tage lang in der tatsächlichen Besprechung aufbewahrt und stehen dann nicht mehr zum Zugriff zur Verfügung. Auf diese Dateien kann von anderen Besprechungsteilnehmern durch das Beitreten zu einer Besprechung über Besprechungsanfrage zugegriffen werden, und dann kann die angefügte Datei angezeigt oder heruntergeladen werden. Weitere Informationen finden Sie im Abschnitt "Verwenden der Anlagen in der Besprechung" in [Vorheriges Hochladen von Anlagen für eine Skype for Business-Besprechung](https://support.microsoft.com/office/preload-attachments-for-a-skype-for-business-meeting-fd3d9f9d-b448-4754-b813-02e49393f251).
- Unterhaltungen in Skype for Business werden im Ordner „Aufgezeichnete Unterhaltungen“ in den Benutzerpostfächern gespeichert. Sie können mit der Inhaltssuche Postfächer nach Daten in Skype-Unterhaltungen durchsuchen.
- Eine betroffene Person kann ihre Kontakte in Skype for Business exportieren. Dazu klickt sie mit der rechten Maustaste auf eine Kontaktgruppe in Skype for Business und dann auf **Kopieren**. Anschließend kann sie die Liste der E-Mail-Adressen in ein Text- oder Word-Dokument einfügen.
- Wenn für das Exchange Online-Postfach eines Besprechungsteilnehmers ein Beweissicherungsverfahren aktiviert wird oder einer Office 365-Aufbewahrungsrichtlinie zugewiesen wird, werden einer Besprechung angefügte Dateien im Postfach des Teilnehmers gespeichert. Mit der Inhaltssuche können Sie Dateien im Postfach des Teilnehmers suchen, wenn die Aufbewahrungsdauer für die Datei nicht abgelaufen ist. Weitere Informationen zum Aufbewahren von Dateien finden Sie unter [Aufbewahren großer einer Skype for Business-Besprechung angefügter Dateien](/skypeforbusiness/set-up-policies-in-your-organization/retaining-large-files-attached-to-a-meeting).

## <a name="providing-a-copy-of-personal-data"></a>Bereitstellen einer Kopie der personenbezogenen Daten

Nachdem Sie personenbezogene Daten gefunden haben, die möglicherweise mit einem Antrag einer betroffenen Person zusammenhängen, liegt es an Ihnen und Ihrer Organisation, zu entscheiden, welche Daten Sie der betroffenen Person zur Verfügung stellen. Sie können ihr beispielsweise eine Kopie des tatsächlichen Dokuments, eine entsprechend geschwärzte Version oder einen Screenshot mit dem Bereich, den Sie als zur Freigabe geeignet eingestuft haben, zur Verfügung stellen. Für jede der folgenden Antworten auf eine Zugriffsanforderung müssen Sie eine Kopie des Dokuments oder eines anderen Elements, das die entsprechenden Daten enthält, abrufen.

Wenn Sie der betroffenen Person eine Kopie zur Verfügung stellen, müssen Sie personenbezogene Daten zu anderen betroffenen Personen und sämtliche vertraulichen Informationen möglicherweise entfernen oder schwärzen.

### <a name="using-content-search-to-get-a-copy-of-personal-data"></a>Verwenden der Inhaltssuche zum Erhalten einer Kopie von personenbezogenen Daten

Sie können das Tool zur Inhaltssuche auf zwei Arten verwenden, um eine Kopie eines Dokuments oder ein Postfachelement zu erhalten, die Sie nach dem Ausführen einer Suche gefunden haben.

- Lassen Sie sich eine Vorschau der Suchergebnisse anzeigen, und laden Sie dann eine Kopie des Dokuments oder Elements herunter. Dies ist eine gute Möglichkeit, um einige Elemente oder Dateien herunterzuladen.
- Exportieren Sie die Suchergebnisse, und laden Sie dann eine Kopie aller Elemente herunter, die von der Suche zurückgegeben wurden. Diese Methode ist komplexer, aber sehr gut geeignet, um viele Elemente herunterzuladen, die für den Antrag einer betroffenen Person relevant sind. In den exportierten Suchergebnissen sind auch nützliche Berichte enthalten. Diese können Sie nutzen, um zusätzliche Informationen zu den einzelnen Elementen zu erhalten. Der Bericht **Results.csv** ist nützlich, da er viele Informationen zu den exportierten Elementen, z. B. den genauen Speicherort des Elements (z. B. das Postfach für E-Mail-Nachrichten oder die URL für Dokumente oder Listen auf den SharePoint Online- und OneDrive for Business-Sites) enthält. Diese Informationen helfen Ihnen, den Besitzer des Elements zu ermitteln, falls Sie ihn während der Untersuchung im Rahmen des Antrags einer betroffenen Person kontaktieren müssen. Weitere Informationen zu den Berichten, die beim Exportieren von Suchergebnissen enthalten sind, finden Sie unter [Exportieren eines Inhaltssuchberichts](/microsoft-365/compliance/export-a-content-search-report).

#### <a name="preview-and-download-items"></a>Vorschau anzeigen und Elemente herunterladen

Nachdem Sie eine neue Suche durchgeführt oder eine bestehende Suche geöffnet haben, können Sie jedes Element in einer Vorschau anzeigen, das der Suchabfrage entspricht, um zu verifizieren, dass es mit dem Antrag einer betroffenen Person übereinstimmt, den Sie untersuchen. Hierzu gehören auch SharePoint-Listen und -Webseiten, die als Suchergebnis aufgeführt werden. Sie können die ursprüngliche Datei herunterladen, wenn Sie diese der betroffenen Person bereitstellen müssen. In beiden Fällen könnten Sie einen Screenshot anfertigen, um dem Antrag der betroffenen Person auf Erhalt der Informationen nachzukommen.

Einige Arten von Elementen können nicht als Vorschau angezeigt werden. Wenn die Vorschau eines Elements oder eines Dateityps nicht unterstützt wird, haben Sie die Möglichkeit, ein einzelnes Element auf Ihren lokalen Computer oder auf ein zugeordnetes Netzwerklaufwerk oder auf eine andere Netzwerkadresse herunterzuladen. Die Anzeige einer Vorschau ist nur für [unterstützte Dateitypen](/microsoft-365/compliance/content-search) möglich.

Um Vorschau anzuzeigen und Elemente herunterzuladen:

1. Öffnen der Inhaltssuche im Security & Compliance Center.
2. Wenn die Ergebnisse nicht angezeigt werden, wählen Sie **Ergebnisvorschau** aus.
3. Klicken Sie auf ein Element, um es anzuzeigen.
4. Klicken Sie auf **ursprüngliche Datei herunterladen**, um das Element auf Ihren lokalen Computer herunterzuladen. Sie müssen auch Elemente herunterladen, die nicht als Vorschau angezeigt werden können.

Weitere Informationen über die Vorschau von Suchergebnissen finden Sie unter [Suchergebnisse in der Vorschau anzeigen](/microsoft-365/compliance/content-search).

#### <a name="export-and-download-items"></a>Exportieren und Herunterladen von Elementen

Sie können auch die Ergebnisse einer Inhaltssuche exportieren, um eine Kopie von E-Mail-Nachrichten, Dokumenten, Listen und Webseiten zu erhalten, die personenbezogene Daten beinhalten; diese Methode ist jedoch komplexer als Elemente in einer Vorschau anzuzeigen. Einzelheiten zum [Export der Ergebnisse einer Inhaltssuche](#export-and-download-content-using-content-search) finden Sie im nächsten Abschnitt.

## <a name="exporting-personal-data"></a>Exportieren von personenbezogenen Daten

Das "Recht auf Datenübertragbarkeit" ermöglicht es betroffenen Personen, eine elektronische Kopie ihrer personenbezogenen Daten in einem "strukturierten, gängigen, maschinenlesbaren Format" anzufordern sowie anzufordern, dass Ihr Unternehmen diese elektronischen Dateien an einen anderen Datenverantwortlichen übermittelt. Microsoft unterstützt dieses Recht auf zwei Arten:

- Durch Office 365-Anwendungen, die Daten in einem systemeigenen, maschinenlesbaren, gängigen elektronischen Format speichern. Weitere Informationen über Office-Dateiformate finden Sie unter [Office-Dateiformate – Technische Dokumentation](https://msdn.microsoft.com/library/office/cc313105(v=office.12).aspx).
- Befähigt Ihr Unternehmen, die Daten in ein systemeigenes Dateiformat oder ein Format (wie CSV, TXT und JSON) zu exportieren, das einfach in andere Anwendungen importiert werden kann.

Um einen Antrag einer betroffenen Person auf Export zu erfüllen, können Sie Office-Dokumente in ihr ursprüngliches Dateiformat exportieren und Daten aus anderen Office-365-Anwendungen exportieren.

### <a name="export-and-download-content-using-content-search"></a>Exportieren und Herunterladen von Inhalten mithilfe der Inhaltssuche

Wenn Sie die Ergebnisse einer Inhaltssuche exportieren, können E-Mail-Elemente als PTS-Dateien oder als einzelne Nachrichten (.msg-Dateien) heruntergeladen werden. Wenn Sie Dokumente und Listen aus SharePoint Online und OneDrive for Business-Websites exportieren, werden Kopien der systemeigenen Dateiformate exportiert. SharePoint-Listen werden beispielsweise als CSV-Dateien exportiert, Webseiten werden als .aspx- oder html-Dateien exportiert.

> [!NOTE]
> Elemente aus dem Postfach eines Benutzers mithilfe der Inhaltssuche zu exportieren setzt voraus, dass dem Benutzer (aus dessen Postfach Sie Elemente exportieren) eine Exchange Online Plan 2-Lizenz zugewiesen ist. 

Um Elemente zu exportieren und herunterzuladen:

1. Öffnen der Inhaltssuche im Security & Compliance Center.
2. Klicken Sie auf der Fly-out-Seite der Suche auf das ![Herunterladen-Symbol](../media/o365-dsr_image21.png)**Mehr** und dann auf **Ergebnisse exportieren**. Sie können auch einen Bericht exportieren.
3. Füllen Sie die Abschnitte auf der Fly-Out-Navigation der **Exportergebnisse** aus. Stellen Sie sicher, dass Sie Bildlaufleiste verwenden, um alle Exportoptionen anzuzeigen.
4. Wechseln Sie wieder zur Seite der Inhaltssuche im Security & Compliance Center und wählen Sie die Registerkarte **Export** aus.
5. Wählen Sie **aktualisieren**, um die Seite zu aktualisieren.
6. Klicken Sie unter der Spalte **Name** auf den Exportauftrag, den Sie soeben erstellt haben. Der Name des Exportauftrags ist der Name der Inhaltssuche gefolgt von der Endung **\_Export**.
7. Klicken Sie auf der Fly-out-Seite unter **Schlüssel exportieren** auf **In Zwischenablage kopieren**. Sie werden diesen Schlüssel in Schritt 10 nutzen, um die Suchergebnisse herunterzuladen.
8. Wählen Sie oben auf der Fly-out-Navigation ![Symbol herunterladen](../media/o365-dsr_image21.png) und **Ergebnisse herunterladen**.
9. Wenn Sie aufgefordert werden, das **Microsoft Office 365 eDiscovery Export Tool** zu installieren, wählen Sie **installieren** aus.
10. Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 7 kopiert haben, in das entsprechende Feld ein.
11. Wählen Sie **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen.
12. Wählen Sie zum Herunterladen der Suchergebnisse auf Ihren Computer **Starten** aus.

Wenn der Exportvorgang abgeschlossen ist, können Sie auf die Dateien in dem Speicherort auf dem lokalen Computer zugreifen, in den sie heruntergeladen wurden. Ergebnisse einer Inhaltssuche werden in einen Ordner heruntergeladen, der nach der Inhaltssuche benannt wird. Dokumente von Websites werden in einen Unterordner mit dem Namen **SharePoint** kopiert. Postfachelemente werden in einen Unterordner mit dem Namen **Exchange** kopiert.

Eine detaillierte Schritt-für-Schritt-Anleitung finden Sie unter [Exportieren der Inhaltssuchergebnisse aus dem Security & Compliance Center](/microsoft-365/compliance/export-search-results).

### <a name="downloading-documents-and-lists-from-sharepoint-online-and-onedrive-for-business"></a>Herunterladen von Dokumenten und Listen aus SharePoint Online und OneDrive for Business

Eine weitere Möglichkeit zum Exportieren von Daten aus SharePoint Online und OneDrive for Business besteht darin, Dokumente und Listen direkt von einer SharePoint Online-Website oder einem OneDrive for Business-Konto herunterzuladen. Ihnen müssen die Berechtigungen zum Zugriff auf eine Website zugewiesen werden, und Sie müssen dann zu der Website wechseln und die Inhalte herunterladen. Siehe:

- [Herunterladen von Dateien und Ordnern aus OneDrive oder SharePoint](https://support.office.com/article/download-files-and-folders-from-onedrive-or-sharepoint-5c7397b7-19c7-4893-84fe-d02e8fa5df05)
- [ Exportieren von SharePoint-Listen in Excel](https://support.office.com/article/export-to-excel-from-sharepoint-bfb2ea48-6118-4fa9-abb6-cced9424e5d9)

Bei einigen DSR-Exportaufträgen möchten Sie möglicherweise zulassen, dass die betroffene Person Inhalte selbst herunterladen kann. Dadurch kann die betroffene Person zu einer SharePoint Online-Website oder einem freigegebenen Ordner wechseln und dann auf **Synchronisierung** klicken, um alle Inhalte in der Dokumentbibliothek oder den ausgewählten Ordnern zu synchronisieren. Siehe:

- [Aktivieren von Benutzern zum Synchronisieren von SharePoint-Dateien mit dem neuen OneDrive-Synchronisierungsclient](/sharepoint/let-users-use-new-onedrive-sync-client)
- [Synchronisieren von SharePoint-Dateien mit dem neuen OneDrive-Synchronisierungsclient](https://support.office.com/article/sync-sharepoint-files-with-the-new-onedrive-sync-client-6de9ede8-5b6e-4503-80b2-6190f3354a88)

## <a name="deleting-personal-data"></a>Löschen von personenbezogenen Daten

Das „Recht auf Löschung“ durch das Entfernen personenbezogener Daten aus den Kundendaten eines Unternehmens ist ein wichtiger Schutz in der DSGVO. Das Entfernen personenbezogener Daten umfasst das Löschen ganzer Dokumente oder Dateien oder das Löschen von bestimmten Daten innerhalb eines Dokuments oder einer Datei (dies würde eine Aktion und einen Prozess erfordern, wie die oben im Abschnitt „Berichtigung“ dieses Leitfadens beschriebenen).

Nachfolgend finden Sie einige wichtige Informationen zum Löschen (und Aufbewahren)  in Office 365, die zu beachten sind, wenn Sie im Rahmen eines Antrags einer betroffenen Person das Löschen von personenbezogenen Daten untersuchen oder vorbereiten.

- **Vorläufiges Löschen im Vergleich zu endgültigem Löschen:** In Office 365-Diensten wie Exchange Online, SharePoint Online und OneDrive for Business gibt es die Begriffe *vorläufiges Löschen* und *endgültiges Löschen*, die sich auf die Wiederherstellbarkeit eines gelöschten Elements (in der Regel für einen begrenzten Zeitraum) beziehen, bevor es endgültig aus der Microsoft-Cloud entfernt wird und nicht mehr wiederhergestellt werden kann. In diesem Zusammenhang kann ein vorläufig gelöschtes Element durch einen Benutzer und/oder Administrator für einen begrenzten Zeitraum wiederhergestellt werden, bevor es endgültig gelöscht wird. Wenn ein Element endgültig gelöscht wurde, wird es zur endgültigen Entfernung markiert und gelöscht, sobald es vom entsprechenden Office 365-Dienst verarbeitet wird. Nachfolgend wird erläutert, wie das Vorläufige Löschen und Endgültige Löschen bei Elementen in Postfächern und auf Websites funktioniert (unabhängig davon, ob der Datenbesitzer oder ein Administrator ein Element löscht):

  - **Postfächer:** Ein Element wird vorübergehend gelöscht, wenn es aus dem Ordner "Gelöschte Elemente" gelöscht wird oder wenn ein Benutzer ein Element durch Drücken von **Umschalt + Entf** löscht. Vorläufig gelöschte Element werden in den Ordner "Wiederherstellbare Elemente" im Postfach verschoben. Zu diesem Zeitpunkt kann ein Element solange vom Benutzer wiederhergestellt werden, bis der Aufbewahrungszeitraum für gelöschte Elemente abgelaufen ist (in Office 365 beträgt die Aufbewahrungszeit 14 Tage, sie kann jedoch von einem Administrator auf bis zu 30 Tage heraufgesetzt werden). Nachdem der Aufbewahrungszeitraum abgelaufen ist, wird das Element endgültig gelöscht und in einen ausgeblendeten Ordner verschoben (der als Ordner *Löschvorgänge* bezeichnet wird). Das Element wird bei der nächsten Verarbeitung des Postfachs dauerhaft aus Office 365 entfernt (gelöscht) (Postfächer werden einmal alle sieben Tage verarbeitet).

  - **SharePoint Online- und OneDrive for Business-Websites**: Gelöschte Dateien oder Dokumente werden in den Papierkorb der Site verschoben (der auch *vorläufiger Papierkorb* genannt wird und dem Papierkorb in Windows entspricht). Das Element verbleibt 93 Tage im Papierkorb (dies ist der Aufbewahrungszeitraum für Sites in Office 365). Nach diesem Zeitraum wird das Element automatisch in den Papierkorb für die Sitesammlung verschoben, der auch als *endgültiger Papierkorb* bezeichnet wird. (Beachten Sie, dass Benutzer oder Administratoren – mit den geeigneten Berechtigungen – auch Elemente aus dem Standardpapierkorb löschen können). An diesem Punkt wird das Element vorläufig gelöscht; es kann weiterhin vom Administrator einer Websitesammlung in SharePoint Online oder von dem Benutzer oder Administrator in OneDrive for Business wiederhergestellt werden. Wenn ein Element aus dem endgültigen Papierkorb (entweder manuell oder automatisch) gelöscht wird, wird es endgültig gelöscht, und weder Benutzer noch ein Administrator können darauf zugreifen. Der Aufbewahrungszeitraum sowohl für den Standardpapierkorb als auch für den endgültigen Papierkorb beträgt 93 Tage. Das bedeutet, dass der Aufbewahrungszeitraum für den endgültigen Papierkorb dann beginnt, wenn das Element zum ersten Mal gelöscht wird; daher beträgt die gesamte maximale Aufbewahrungszeit 93 Tage für beide Papierkörbe.

> [!NOTE]
> Wenn Sie verstehen, welche Aktionen dazu führen, dass ein Element vorübergehend oder endgültig gelöscht wird, wird es Ihnen leichter fallen, zu bestimmen, wie Daten gelöscht werden müssen, um die Anforderungen der DSGVO im Rahmen einer Reaktion auf einen Antrag auf Löschung zu erfüllen.

- **Aufbewahrung für juristische Zwecke und Aufbewahrungsrichtlinien:** In Office 365 kann eine „Aufbewahrungspflicht“ für Postfächer und Websites gelten; das heißt, dass nichts dauerhaft entfernt (endgültig gelöscht) wird, wenn ein Postfach oder eine Site aufbewahrt werden muss, bis der Aufbewahrungszeitraum für ein Element abgelaufen ist oder bis die Aufbewahrungspflicht aufgehoben wird. Das ist im Zusammenhang mit dem Löschen von Kundeninhalten als Reaktion auf einen Antrag einer betroffenen Person wichtig: Wenn ein Element von einem Inhaltsspeicherort endgültig gelöscht wird, für den die Aufbewahrung festgelegt wurde, wird das Element nicht endgültig aus Office 365 entfernt. Das bedeutet, dass es von einem IT-Administrator möglicherweise wiederhergestellt werden kann. Wenn es in Ihrem Unternehmen eine Anforderung oder Richtlinie gibt, dass Daten in Office 365 als Reaktion auf einen Antrag einer betroffenen Person endgültig gelöscht werden müssen und nicht wiederherstellbar sein dürfen, muss die Aufbewahrungspflicht für ein Postfach oder eine Website aufgehoben werden, um Daten endgültig in Office 365 zu löschen. Höchstwahrscheinlich gibt es in Ihrem Unternehmen Leitfäden dazu, wie im Fall von Anträgen betroffener Personen vorzugehen ist, um festzustellen, ob ein bestimmter Antrag einer betroffenen Person auf Löschung Vorrang hat vor Aufbewahrung für juristische Zwecke. Wird die Aufbewahrung deaktiviert, um Elemente zu löschen, kann sie erneut eingerichtet werden, nachdem das Element gelöscht wurde.

### <a name="deleting-documents-in-sharepoint-online-and-onedrive-for-business"></a>Löschen von Dokumenten in SharePoint Online und OneDrive for Business

Nachdem Sie das Dokument auf einer SharePoint Online-Website oder in einem OneDrive for Business-Konto gefunden haben (entsprechend den Anweisungen im Abschnitt „Ermittlung“ dieses Leitfadens) und das gelöscht werden muss, muss ein Datenschutzbeauftragter oder IT-Administrator die erforderlichen Berechtigungen zum Zugriff auf die Website und zum Löschen des Dokuments zuweisen. Falls erforderlich, kann auch der Dokumentbesitzer angewiesen werden, das Dokument zu löschen.

Im Folgenden finden Sie Schritte auf einer hohen Ebene zum Löschen von Dokumenten von Websites.

1. Wechseln Sie zu der Website, und suchen Sie das Dokument.
2. Löschen Sie das Dokument. Wenn Sie ein Dokument von einer Website löschen, wird es in den Standardpapierkorb verschoben.
3. Wechseln Sie zum Standardpapierkorb (Papierkorb der Website), und löschen Sie dasselbe Dokument, das Sie im vorherigen Schritt gelöscht haben. Das Dokument wird in den endgültigen Papierkorb verschoben. **An diesem Punkt wurde das Dokument vorübergehend gelöscht**.
4. Wechseln Sie zum endgültigen Papierkorb (dem Papierkorb der Websitesammlung), und löschen Sie dasselbe Dokument, das Sie aus dem Standardpapierkorb gelöscht haben. **An diesem Punkt wurde das Dokument endgültig gelöscht.**

> [!IMPORTANT]
> Sie können ein Dokument nicht löschen, das sich auf einer Website befindet, für die eine Aufbewahrung festgelegt wurde (mithilfe einer der Funktionen für reguläre Aufbewahrung oder Aufbewahrung für juristische Zwecke in Office 365). Falls ein Antrag einer betroffenen Person auf Löschung Vorrang vor der Aufbewahrung hat, muss die Aufbewahrung für die Website entfernt werden, bevor ein Dokument endgültig gelöscht werden kann.

Ausführliche Prozeduren finden Sie unter den folgenden Themen:

- [Löschen einer Datei, eines Ordners oder eines Links aus einer SharePoint-Dokumentbibliothek](https://support.microsoft.com/office/delete-a-file-folder-or-link-from-a-sharepoint-document-library-71f3c90a-0d24-4d80-8b66-f88234b79a52)
- [Löschen von Elementen oder Leeren des Papierkorbs einer SharePoint-Website](https://support.microsoft.com/office/delete-items-or-empty-the-recycle-bin-of-a-sharepoint-site-2e713599-d13e-40d6-96dc-66f0a366f74e)
- [Löschen von Elementen aus dem Papierkorb der Websitesammlung](https://support.microsoft.com/office/delete-items-from-the-site-collection-recycle-bin-dd5c00c2-aef6-4458-9d04-80b185077653)
- Abschnitt "Erhalten von Zugriff auf OneDrive for Business-Dokumente eines ehemaligen Mitarbeiters" in [Erhalten von Zugriff auf die Daten eines ehemaligen Benutzers und Sichern dieser Daten](/microsoft-365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data)
- [Löschen von Dateien oder Ordnern in OneDrive for Business](https://support.office.com/article/Delete-files-or-folders-in-OneDrive-21fe345a-e488-4fa7-932b-f053c1bebe8a)
- [Löschen einer Liste in SharePoint](https://support.microsoft.com/office/delete-a-list-in-sharepoint-2a7bca5b-b8fd-4e5b-8f4b-2ac034f3070d)
- [Löschen von Listenelementen in SharePoint Online](https://support.office.com/article/delete-list-items-in-sharepoint-online-db722233-4a38-4889-a6cf-4b33fe5c60c0)

### <a name="deleting-a-sharepoint-site"></a>Löschen einer SharePoint-Website

Sie stellen möglicherweise fest, dass die beste Reaktion auf einen Antrag einer betroffenen Person auf Löschung darin besteht, eine gesamte SharePoint-Website zu löschen, wobei alle Daten auf der Website gelöscht werden. Dazu können Sie Cmdlets in SharePoint Online PowerShell ausführen.

- Verwenden Sie das Cmdlet [Remove-SPOSite](/powershell/module/sharepoint-online/remove-sposite), um die Website zu löschen und die Website zu löschen und in den SharePoint Online-Papierkorb zu verschieben (vorläufiges Löschen).
- Verwenden Sie das Cmdlet [Remove-SPODeletedSite](/powershell/module/sharepoint-online/remove-spodeletedsite), um die Website endgültig zu löschen (endgültiges Löschen).

Sie können eine Website nicht löschen, für die eine eDiscovery-Aufbewahrungspflicht gilt oder der eine Aufbewahrungsrichtlinie zugewiesen wurde. Websites müssen von einer eDiscovery-Aufbewahrungspflicht oder einer Aufbewahrungsrichtlinie entfernt werden, bevor Sie sie löschen können.

### <a name="deleting-a-onedrive-for-business-site"></a>Löschen einer OneDrive for Business-Website

Entsprechend bestimmen Sie möglicherweise, die OneDrive for Business-Website eines Benutzers als Reaktion auf einen Antrag einer betroffenen Person auf Löschung zu löschen. Wenn Sie das Office 365-Konto des Benutzers löschen, wird die OneDrive for Business-Website des Benutzers für 30 Tage aufbewahrt (und kann wiederhergestellt werden). Nach 30 Tagen wird sie in den SharePoint Online-Papierkorb verschoben (vorläufig gelöscht) und dann nach 93 Tagen dauerhaft gelöscht (endgültig gelöscht). Um diesen Vorgang zu beschleunigen, können Sie das Cmdlet [Remove-SPOSite](/powershell/module/sharepoint-online/remove-sposite) zum Verschieben der OneDrive for Business-Website in den Papierkorb oder das Cmdlet [Remove-SPODeletedSite](/powershell/module/sharepoint-online/remove-spodeletedsite) zum endgültigen Löschen verwenden. Wie bei Websites in SharePoint Online, können Sie die OneDrive for Business-Website eines Benutzers nicht Löschen, wenn sie einer eDiscovery-Aufbewahrung unterliegt oder ihr eine Aufbewahrungsrichtlinie zugewiesen wurde, bevor das Konto des Benutzers gelöscht wurde.

### <a name="deleting-onedrive-for-business-and-sharepoint-online-experience-settings"></a>Löschen von OneDrive for Business- und SharePoint Online-Oberflächeneinstellungen

Zusätzlich zu den vom Benutzer erstellten Dateien, die in OneDrive for Business-Konten und SharePoint Online-Websites gespeichert sind, speichern diese Dienste Informationen über den Benutzer, die verwendet werden, um verschiedene Erfahrungen zu ermöglichen. Diese wurden zuvor in diesem Dokument beschrieben. Weitere Informationen zum Zugriff, zur Anzeige und zum Export von OneDrive for Business- und SharePoint Online-Anwendungsdaten finden Sie im Abschnitt [Zusätzliche Hinweise für ausgewählte Anwendungen](#additional-considerations-for-selected-applications) unter [Verwendung des eDiscovery-Tools für die Inhaltssuche als Reaktion auf Anträge betroffener Personen](#using-the-content-search-ediscovery-tool-to-respond-to-dsrs).

#### <a name="deleting-a-sharepoint-user-profile"></a>Löschen eines SharePoint-Benutzerprofils

Das SharePoint-Benutzerprofil wird 30 Tage nachdem das Benutzerkonto in Azure Active Directory gelöscht wurde endgültig gelöscht. Sie können das Benutzerkonto auch endgültig, wodurch das SharePoint-Benutzerprofil entfernt wird. Weitere Informationen finden Sie im Abschnitt [Löschen eines Benutzers in diesem Leitfaden](#deleting-a-user).

Ein Administrator kann das Löschen des Benutzerprofils für einen Benutzer beschleunigen, indem er das Cmdlet **Remove-SPOUserProfile** in SharePoint Online PowerShell verwendet. Siehe [Remove-SPOUserProfil](/powershell/module/sharepoint-online/remove-spouserprofile). Dies setzt voraus, dass der Benutzer mindestens vorläufig in Azure Active Directory gelöscht wurde.

#### <a name="deleting-user-information-lists-on-sharepoint-online-sites"></a>Löschen von Benutzerinformationslisten auf SharePoint Online-Websites

Für Benutzer, die die Organisation verlassen haben, verbleiben diese Daten auf den Websites, mit denen sie interagiert haben, um die referentielle Integrität der SharePoint-Spaltenfelder zu gewährleisten. Ein Administrator kann mit dem Befehl **Remove-SPOUserInfo** in SharePoint Online PowerShell alle Benutzerinformationseigenschaften für einen Benutzer auf einer bestimmten Website löschen. Weitere Informationen zum Ausführen dieses PowerShell-Cmdlets finden Sie unter [Remove-SPOUserInfo](/powershell/module/sharepoint-online/remove-spouserinfo).

Standardmäßig speichert dieser Befehl den Anzeigenamen des Benutzers und gelöschte Eigenschaften wie Telefonnummer, E-Mail-Adresse, Qualifikationen und Kompetenzen oder andere Eigenschaften, die aus dem SharePoint Online-Benutzerprofil kopiert wurden. Ein Administrator kann mit dem Parameter **RedactUser** einen alternativen Anzeigenamen für den Benutzer in der Benutzerinformationsliste angeben. Dies wirkt sich auf mehrere Teile der Benutzeroberfläche aus und führt zu einem Informationsverlust, wenn der Verlauf der Dateien auf der Website angezeigt wird.

Schlussendlich wird die Bearbeitungsfunktion nicht alle Metadaten oder Inhalte aus Dokumenten entfernen, die auf einen Benutzer hinweisen. Die Möglichkeit, die Bearbeitung von Dateiinhalten und Metadaten zu erreichen wird im Abschnitt [Vornehmen von Änderungen am Inhalt in OneDrive for Business und SharePoint Online](#making-changes-to-content-in-onedrive-for-business-and-sharepoint-online) in diesem Leitfaden erläutert. Bei dieser Methode wird eine Datei heruntergeladen und gelöscht und dann eine bearbeitete Kopie der Datei hochgeladen.

#### <a name="deleting-onedrive-for-business-experience-settings"></a>Löschen der OneDrive for Business-Oberflächeneinstellungen

Der empfohlene Weg, alle Einstellungen und Informationen von OneDrive for Business zu löschen, besteht darin, die OneDrive for Business-Website des Benutzers zu entfernen, nachdem Sie alle gespeicherten Dateien anderen Benutzern zugewiesen haben. Ein Administrator kann diese Listen mit den Befehlen [PowerShell Script](/powershell/scripting/overview) und [SharePoint Client-Side Object Model (CSOM)](/sharepoint/dev/sp-add-ins/complete-basic-operations-using-sharepoint-client-library-code) löschen. Weitere Informationen zu den Einstellungen, wie diese gespeichert werden und wie sie gelöscht werden, finden Sie unter [Löschen von OneDrive for Business-Oberflächeneinstellungen](/sharepoint/delete-odfb-lists).

#### <a name="onedrive-for-business-and-sharepoint-online-search-queries"></a>OneDrive for Business- und SharePoint Online-Suchabfragen

Die Suchabfragen eines Benutzers, die in der OneDrive for Business- und SharePoint Online-Suchoberfläche erstellt wurden, werden 30 Tage nachdem der Benutzer die Abfrage erstellt hat automatisch gelöscht.

### <a name="deleting-items-in-exchange-online-mailboxes"></a>Löschen von Elementen in Exchange Online-Postfächern

Sie müssen möglicherweise Elemente in Exchange Online-Postfächern löschen, um einem Antrag einer betroffenen Person auf Löschung Folge zu leisten. Es gibt zwei Möglichkeiten, wie ein IT-Administrator Elemente im Postfach löschen kann, abhängig davon, ob Elemente vorläufig oder endgültig gelöscht werden sollen. Wie bei Dokumenten auf SharePoint Online- oder OneDrive for Business-Websites können Elemente in einem Postfach, das einer Aufbewahrung unterliegt, nicht endgültig aus Office 365 gelöscht werden. Die Aufbewahrung muss entfernt werden, bevor das Element gelöscht werden kann. In diesem Fall müssen Sie bestimmen, ob die Aufbewahrung für das Postfach oder der Antrag der betroffenen Person auf Löschung Vorrang hat.

#### <a name="soft-delete-mailbox-items"></a>Vorläufiges Löschen von Postfachelementen

Sie können die Funktion der Inhaltssuchaktion verwenden, um Elemente vorläufig zu löschen, die von einer Inhaltssuche zurückgegeben werden. Wie bereits erläutert, werden vorläufig gelöschte Objekte in den Ordner "Wiederherstellbare Objekte" im Postfach verschoben, während dauerhaft gelöschte Objekte endgültig gelöscht werden und nicht wiederhergestellt werden können.

Hier finden Sie einen kurzen Überblick über die Funktionsweise dieses Verfahrens:

1. Erstellen Sie eine Inhaltssuche und führen Sie sie aus, um die Elemente zu finden, die Sie aus dem Postfach des Benutzers löschen möchten. Möglicherweise müssen Sie die Suche erneut ausführen, um die Suchergebnisse einzuschränken, sodass nur die Elemente in den Suchergebnissen zurückgegeben werden, die Sie löschen möchten.
2. Verwenden Sie den Befehl **New-ComplianceSearchAction** **-Purge** **PurgeType** **SoftDelete** oder **New-ComplianceSearchAction** **-Purge** **PurgeType** **HardDelete** in Office 365 PowerShell, um Elemente zu löschen, die von der Inhaltssuche zurückgegeben werden, die im vorhergehenden Schritt erstellt wurde.

Ausführliche Anweisungen finden Sie unter [Suchen nach und Löschen von E-Mail-Nachrichten in Ihrer Organisation](/microsoft-365/compliance/search-for-and-delete-messages-in-your-organization).

#### <a name="hard-delete-items-in-a-mailbox-on-hold"></a>Endgültiges Löschen von Elementen in einem Postfach, das aufbewahrt wird

Wenn Sie Elemente in einem Postfach mit einer Aufbewahrungspflicht endgültig löschen, werden die Elemente wie zuvor erläutert nicht aus dem Postfach entfernt. Sie werden in einen ausgeblendeten Ordner im Ordner „Wiederherstellbare Elemente“ verschoben (der Ordner **Löschvorgänge**) und die dort verbleiben, bis das Element abläuft oder bis die Aufbewahrungspflicht für das Postfach deaktiviert wird. Wenn einer dieser Fälle vorliegt, werden die Elemente von Office 365 das nächste Mal gelöscht, wenn das Postfach verarbeitet wird.

Ihr Unternehmen kann bestimmen, dass das endgültige Löschen von Elementen nach Ablauf der Aufbewahrung die Anforderungen eines Antrags einer betroffenen Person auf Löschung erfüllt. Wenn Postfachelemente in Office 365 jedoch sofort endgültig gelöscht werden müssen, müssen Sie die Aufbewahrung entfernen und die Elemente endgültig aus dem Postfach löschen. Detaillierte Anweisungen finden Sie unter [Löschen von Elementen im Ordner „Wiederherstellbare Elemente“ für cloudbasierte Postfächer mit Aufbewahrungspflicht](/microsoft-365/compliance/delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold).

> [!NOTE]
> Um in Reaktion auf einen Antrag einer betroffenen Person auf Löschung Postfachelemente entsprechend der im vorhergehenden Thema beschriebenen Vorgehensweise endgültig zu löschen, müssen Sie diese Elemente möglicherweise vorläufig löschen, während für das Postfach noch eine Aufbewahrung gilt, was bedeutet, dass die Postfachelemente in den Ordner „Wiederherstellbare Elemente“ verschoben werden.

## <a name="deleting-a-user"></a>Löschen eines Benutzers

Neben der Löschung personenbezogener Daten in Reaktion auf einen Antrag einer betroffenen Person kann dem "Recht auf Vergessenwerden" einer betroffenen Person auch Folge geleistet werden, indem ihr Benutzerkonto gelöscht wird. Hier sind einige Gründe für das Löschen eines Benutzers:

- Die betroffene Person hat Ihr Unternehmen verlassen (oder ist gerade dabei, es zu verlassen).
- Die betroffene Person hat Sie aufgefordert, vom System erzeugte Protokolle, die über sie gesammelt wurden, zu löschen. Beispiele für Daten in systemgenerierten Protokollen sind Office 365-Anwendungs- und Servicenutzungsdaten, Informationen über Suchanfragen der betroffenen Person und Daten, die von Produkten und Diensten als Produkt der Systemfunktionalität und Interaktion von Benutzern oder anderen Systemen generiert werden. Weitere Informationen siehe [Teil 3: Reagieren auf Anträge betroffener Personen bezüglich vom System generierten Protokollen](#part-3-responding-to-dsrs-for-system-generated-logs) in diesem Leitfaden.
- Verhindern Sie dauerhaft den Zugriff oder die Verarbeitung von Daten in Office 365 (im Gegensatz zu einer vorübergehenden Einschränkung des Zugriffs durch die im Abschnitt [Reagieren auf Anträge betroffener Personen zur Einschränkung der Datenverarbeitung](#responding-to-dsr-restriction-requests) beschriebenen Methoden).

Nachdem Sie ein Benutzerkonto gelöscht haben gilt Folgendes:

- Der Benutzer kann sich nicht mehr bei Office 365 anmelden oder auf die Microsoft-Ressourcen Ihres Unternehmens zugreifen, z. B. auf das OneDrive for Business-Konto, die SharePoint Online-Websites oder das Exchange Online-Postfach.
- Personenbezogene Daten wie E-Mail-Adresse, Alias, Telefonnummer und Postanschrift, die mit dem Benutzerkonto verknüpft sind, werden gelöscht.
- Einige Office 365-Anwendungen entfernen Informationen über den Benutzer. Beispielsweise ist in Microsoft Flow der gelöschte Benutzer aus der Liste der Besitzer für einen gemeinsamen Fluss entfernt.
- Vom System generierte Protokolle zur betroffenen Person, mit Ausnahme von Daten, die für die Sicherheit oder Stabilität des Diensts wesentlich sind, werden 30 Tage nach dem Löschen des Benutzerkontos gelöscht. Weitere Informationen finden Sie im Abschnitt [Vom System generierte Protokolle löschen](#deleting-system-generated-logs).

> [!IMPORTANT]
> Nachdem Sie ein Benutzerkonto löschen, kann sich die betreffende Person weder bei Office 365 noch bei den Produkten oder Diensten anmelden, die sie über ihr Geschäfts-, Schul- oder Unikonto genutzt hat. Diese Person könnte auch keine Anträge betroffener Personen direkt über Microsoft initialisieren in Fällen, in denen Microsoft der Datenverantwortliche ist. Weitere Informationen finden Sie im Abschnitt [Produkte und Dienste, die mit einer Unternehmens-ID authentifiziert wurden, für die Microsoft ein Datenverantwortlicher ist](#product-and-services-authenticated-with-an-org-id-for-which-microsoft-is-a-data-controller) in Teil 4 dieses Leitfadens.

> [!NOTE]
> Für den Fall, dass Sie als Kunde derzeit an FastTrack-Migrationen beteiligt sind, wird durch das Löschen des Benutzerkontos nicht die Datenkopie im Besitz des Microsoft FastTrack-Teams gelöscht, die ausschließlich für das Abschließen der Migration beibehalten wird. Wenn Sie möchten, dass das Microsoft FastTrack-Team während der Migration auch die Datenkopie löscht, können Sie eine diesbezügliche [Anforderung übermitteln](https://go.microsoft.com/fwlink/?linkid=874544). Im normalen Geschäftsverlauf löscht Microsoft FastTrack alle Datenkopien, sobald die Migration abgeschlossen ist.

Wie das vorläufige Löschen und das endgültige Löschen von Daten, die im vorherigen Abschnitt zum Löschen personenbezogener Daten beschrieben wurden, gibt es auch einen vorläufig gelöschten und einen endgültig gelöschten Status, wenn Sie ein Benutzerkonto löschen.

- Wenn Sie zunächst ein Benutzerkonto (durch Löschen des Benutzers im Admin Center oder im Azure-Portal) löschen, ist das Benutzerkonto vorübergehend gelöschte und wird für bis zu 30 Tage in den Papierkorb in Azure verschoben. An diesem Punkt kann das Benutzerkonto wiederhergestellt werden.
- Wenn Sie das Benutzerkonto endgültig gelöscht haben, wird das Benutzerkonto endgültig gelöscht und aus dem Papierkorb in Azure entfernt. An diesem Punkt kann das Benutzerkonto nicht wiederhergestellt werden, und alle mit dem Benutzerkonto verbundenen Daten werden aus der Microsoft-Cloud dauerhaft entfernt. Beim endgültigen Löschen eines Kontos werden vom System generierte Protokolle zur betroffenen Person gelöscht, mit Ausnahme von Daten, die für die Sicherheit oder die Stabilität des Dienstes wesentlich sind.

Im Folgenden finden Sie die grundlegenden Schritte zum Löschen eines Benutzers aus Ihrer Organisation.

1. Wechseln Sie zum Admin Center oder zum Azure-Portal, und suchen Sie nach dem Benutzer.

2. Löschen Sie den Benutzer. Wenn Sie den Benutzer das erste Mal löschen, wird das Konto des Benutzers in den Papierkorb verschoben. An diesem Punkt ist der Benutzer vorübergehend gelöscht. Das Konto bleibt 30 Tage vorläufig gelöscht, was Ihnen ermöglicht, das Konto wiederherzustellen. Nach 30 Tagen wird das Konto automatisch endgültig gelöscht. Spezifische Anweisungen finden Sie unter [Löschen von Benutzern aus Azure AD](/azure/active-directory/add-users-azure-active-directory).<br><br> Sie können ein Benutzerkonto auch im Admin Center vorläufig löschen. Siehe [Löschen eines Benutzers aus Ihrer Organisation](/microsoft-365/admin/add-users/delete-a-user).

3. Wenn Sie nicht 30 Tage warten wollen, bis das Benutzerkonto endgültig gelöscht wird, können Sie es manuell endgültig löschen. Gehen Sie dazu im Azure-Portal in die Liste „Zuletzt gelöschte Benutzer“, und löschen Sie den Benutzer endgültig. An dieser Stelle ist der Benutzer endgültig gelöscht. Anweisungen finden Sie unter [So löschen Sie einen kürzlich gelöschten Benutzer endgültig](/azure/active-directory/active-directory-users-restore).

Sie können einen Benutzer im Office 365-Verwaltungsportal nicht endgültig löschen.

> [!NOTE]
> In Office 365, das von 21Vianet betrieben wird (China), können Sie einen Benutzer nicht wie zuvor beschrieben dauerhaft löschen. Um einen Benutzer dauerhaft zu löschen, können Sie eine Anforderung über das Office 365-Verwaltungsportal unter dieser [URL](https://portal.partner.microsoftonline.cn/AdminPortal/Home#/homepage) stellen. Gehen Sie zu **Handel**, und wählen Sie dann **Abonnement** -> **Datenschutz** ->  **DSGVO** aus, und geben Sie die erforderlichen Informationen ein.

### <a name="removing-exchange-online-data"></a>Entfernen von Exchange Online-Daten

Eine Sache, die beim Löschen eines Benutzers zu verstehen ist, ist, was mit dem Exchange Online-Postfach des Benutzers geschieht. Nach dem Löschen des Benutzerkontos (in Schritt 3 des vorherigen Prozesses) wird das Postfach des gelöschten Benutzers nicht automatisch aus Office 365 gelöscht. Es dauert bis zu 60 Tage, nachdem das Benutzerkonto endgültig gelöscht wurde, um es dauerhaft aus Office 365 zu entfernen. Hier ist der Postfach-Lebenszyklus nach dem Löschen des Benutzerkontos und eine Beschreibung des Status der Postfachdaten während dieser Zeit:

- **Tag 1 – Tag 30**: Das Postfach kann vollständig wiederhergestellt werden, indem das vorläufig gelöschte Benutzerkonto wiederhergestellt wird.
- **Tag 31 – Tag 60**: 30 Tage lang, nachdem das Benutzerkonto endgültig gelöscht wurde, kann ein Administrator in Ihrem Unternehmen die Daten im Postfach wiederherstellen und in ein anderes Postfach importieren. Dies gibt Organisationen die Möglichkeit, die Postfachdaten bei Bedarf wiederherzustellen.
- **Tag 61 – Tag 90**: Ein Administrator kann die Daten im Postfach nicht mehr wiederherstellen. Die Postfachdaten werden für die dauerhafte Entfernung markiert, und es dauert bis zu 30 weitere Tage, bis die Postfachdaten aus Office 365 gelöscht werden.

Sollten Sie feststellen, dass dieser Postfachlebenszyklus nicht die Anforderungen Ihres Unternehmens für die Reaktion auf einen Antrag einer betroffenen Person erfüllt, können Sie [den Microsoft-Support](https://support.microsoft.com/) kontaktieren, *nachdem* Sie das Benutzerkonto endgültig gelöscht haben, und Microsoft auffordern, den Prozess zur dauerhaften Entfernung der Postfachdaten manuell einzuleiten. Dieser Prozess zur dauerhaften Entfernung von Postfachdaten beginnt automatisch nach Tag 61 im Lebenszyklus, sodass es keinen Grund gibt, Microsoft nach diesem Zeitpunkt im Lebenszyklus zu kontaktieren.

## <a name="using-in-app-functionality-to-respond-to-dsrs"></a>Reagieren auf Anträge betroffener Personen mithilfe der In-App-Funktionalität

Während die meisten Kundendaten mit den im vorherigen Abschnitt beschriebenen Anwendungen erstellt und produziert werden, bietet Office 365 auch viele andere Anwendungen, mit denen Kunden Kundendaten erstellen und speichern können. Die Inhaltssuche ist jedoch derzeit nicht in der Lage, nach Daten zu suchen, die in diesen anderen Office 365-Anwendungen erstellt wurden. Um die von diesen Anwendungen generierten Daten zu finden, müssen Sie oder der Dateneigentümer die produktinterne Funktionalität oder Funktionen verwenden, um Daten zu finden, die für einen Antrag einer betroffenen Person relevant sein können. Die folgende Liste identifiziert diese Office 365-Anwendungen.

Anwendungen, bei denen die In-App-Funktion verwendet werden kann, um Kundendaten zu finden:

- Zugriff
- Business-App für Office 365
- Education
- Flow
- Forms
- Kaizala
- Planner
- Power-Apps
- Power BI
- Project
- Publisher
- Stream
- Yammer

### <a name="access"></a>Zugriff

In den folgenden Abschnitten wird erläutert, wie die in-App-Funktion in Microsoft Access verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

##### <a name="discover"></a>Ermittlung

Es gibt mehrere Möglichkeiten, in einer Access-Datenbank nach Datensätzen zu suchen, die für einen Antrag einer betroffenen Person relevant sein können. Im Rahmen einer Untersuchung eines Antrags einer betroffenen Person können Sie nach Datensätzen suchen, die sich auf die betroffene Person beziehen, oder nach Datensätzen, die bestimmte Daten enthalten. Beispielsweise können Sie entweder nach einem Datensatz suchen oder zu einem Datensatz wechseln, der zur betroffenen Person gehört. Sie können alternativ nach Datensätzen suchen, die bestimmte Daten enthalten, z. B. personenbezogene Daten der betroffenen Person. Weitere Informationen finden Sie unter:

- [Suchen nach Datensätzen in einer Access-Datenbank](https://support.microsoft.com/office/find-records-in-an-access-database-705220b7-0255-4ef9-9349-6bd7442d1b7e) 
- [Erstellen einer einfachen Auswahlabfrage](https://support.office.com/article/create-a-simple-select-query-de8b1c8d-14e9-4b25-8e22-70888d54de59)

##### <a name="access"></a>Access

Nachdem Sie die für den Antrag einer betroffenen Person relevanten Datensätze oder Felder gefunden haben, können Sie einen Screenshot der Daten machen oder diese in eine Excel-, Word- oder Textdatei exportieren. Sie können auch einen Bericht erstellen und ausdrucken, der auf einer Datensatzquelle oder einer Auswahlabfrage basiert, die Sie erstellt haben, um nach den Daten zu suchen. Siehe:

- [Einführung in Berichte in Access](https://support.office.com/article/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Exportieren von Daten in Excel](https://support.office.com/article/export-data-to-excel-64e974e6-ae43-4301-a53e-20463655b1a9)
- [Exportieren von Daten in ein Word-Dokument](https://support.microsoft.com/office/export-access-data-to-a-word-document-6e954c8e-2243-4cb9-8544-607e5b7bfc12)
- [Exportieren von Daten in eine Textdatei](https://support.microsoft.com/office/export-data-to-a-text-file-f72dfc38-a8a0-4c5b-8c2c-bf2950814140)

##### <a name="export"></a>Export

Wie bereits erläutert, können Sie Daten aus einer Access-Datenbank in verschiedene Dateiformate exportieren. Das Dateiformat, in das exportiert werden soll, hängt möglicherweise von dem spezifischen Antrag einer betroffenen Person auf Export ab. Im Abschnitt zum [Importieren und Exportieren](https://support.microsoft.com/office/import-and-export-c060505b-d8ac-4499-8879-733e56c6106f) finden Sie eine Themenliste mit Erläuterungen, wie Sie Access-Daten in unterschiedliche Dateiformate exportieren können.

##### <a name="delete"></a>Löschen

Sie können einen ganzen Datensatz oder nur ein Feld aus einer Access-Datenbank löschen. Der schnellste Weg, einen Datensatz aus einer Access-Datenbank zu löschen, besteht darin, die Tabelle in der Datenblattansicht zu öffnen, den Datensatz (Zeile) oder nur die Daten in einem Feld auszuwählen, den bzw. die Sie löschen möchten, und dann auf „Löschen“ zu drücken. Sie können auch eine von Ihnen erstellte Auswahlabfrage verwenden, um Daten zu finden und diese dann in eine Löschabfrage umzuwandeln. Siehe:

- [Löschen von einem oder mehreren Datensätzen aus einer Datenbank](https://support.office.com/article/ways-to-add-edit-and-delete-records-5e90a80c-106d-4c55-996e-07d7200980ce)
- [Erstellen und Ausführen einer Löschanforderung](https://support.office.com/article/create-and-run-a-delete-query-6da65fe1-0fc7-4a64-8ef0-c052cd4c3ec5)

### <a name="business-apps-for-office-365"></a>Geschäftliche Apps für Office 365

In diesem Abschnitt wird erläutert, wie Sie die In-App-Funktionalität in den einzelnen folgenden Business-Apps für Office 365 verwenden können, um auf Anträge betroffener Personen zu reagieren.

- [Bookings](#bookings)
- [Listings](#listings)
- [Connections](#connections)

#### <a name="bookings"></a>Bookings

In den folgenden Abschnitten wird erläutert, wie Sie die In-App-Funktionalität von Microsoft Bookings nutzen können, um nach personenbezogenen Daten zu suchen, auf diese zuzugreifen und diese zu exportieren und zu löschen. Dies gilt sowohl für die eigenständige Bookings-App als auch für Bookings, wenn es über das Geschäftszentrum aufgerufen wird.

Microsoft Bookings ermöglicht es Administratoren und Benutzern oder Mitarbeitern mit einer Bookings-Lizenz in ihrer Organisation, Buchungsseiten einzurichten, damit Kunden Termine planen und ändern können und Bestätigungen, Updates, Stornierungen und Erinnerungen per E-Mail erhalten können. Unternehmer und ihre Mitarbeiter können mit Bookings ebenfalls Veranstaltungen für ihre Kunden buchen. 

Die folgenden Datentypen werden von Kunden, Administratoren oder Mitarbeitern angelegt:

- **Kontaktinformationen von Kunden, Partnern und Freunden**: Diese Daten enthalten Namen, Telefonnummern, E-Mail-Adressen, Adressen und Notizen.

    - Kontakte für alle Benutzer können manuell erstellt werden, indem die Bookings Web-, iOS- und Android-Clients verwendet werden.
    
    - Kontakte für alle Benutzer können von einem C1-Mobilgerät in Bookings mit den Bookings-iOS- und Android-Clients importiert werden.
    
    - Kontakte werden auch automatisch zum Zeitpunkt der Buchungserstellung über den Buchungsworkflow für alle gebuchten Personen erstellt, unabhängig davon, ob die Buchung von einem Benutzer im Namen eines Kunden oder vom Kunden über die Buchungsseite des Besitzers erstellt wurde.

- **Booking-Ereignisse**: Dabei handelt es sich um Besprechungen zwischen dem Geschäftsinhaber oder seinen Mitarbeitern und einem Kunden, die entweder vom Geschäftsinhaber oder dem Kunden über die öffentliche Buchungsseite des Geschäftsinhabers erstellt werden. Diese Daten umfassen Name, Adresse, E-Mail-Adresse, Telefonnummer und alle anderen Informationen, die der Geschäftsinhaber zum Zeitpunkt der Buchung vom Kunden erfasst.

- **E-Mail-Bestätigungen/Stornierungen/Updates**: Dabei handelt es sich um E-Mail-Nachrichten, die das System im Zusammenhang mit bestimmten Buchungsvorgängen generiert und versendet. Sie enthalten personenbezogene Daten zu den Mitarbeitern, die für die Erbringung des jeweiligen Dienstes vorgesehen sind, und sie enthalten personenbezogene Daten zu dem Kunden, die entweder vom Geschäftsbesitzer oder vom Kunden bei der Buchung eingegeben wurden.

Alle Kundeninhalte werden im Exchange Online-Postfach gespeichert, in dem die Bookings-Instanz der Organisation gehostet wird. Diese Inhalte bleiben so lange erhalten, wie der Geschäftsbesitzer und der Kunde im Dienst aktiv sind, es sei denn, sie verlangen ausdrücklich die Löschung der Daten oder verlassen den Dienst. Dieser Inhalt kann mit der Benutzeroberfläche im Produkt, mit einem Cmdlet oder durch Löschen des entsprechenden Buchungspostfachs gelöscht werden. Sobald die gelöschte Aktion eingeleitet wird, werden die Daten innerhalb des vom Geschäftsbesitzer festgelegten Zeitraums gelöscht. 

Entscheidet sich ein Kunde, den Dienst zu verlassen, werden seine Kundeninhalte nach 90 Tagen gelöscht. Weitere Informationen darüber, wann Postfachinhalte nach dem Löschen von Benutzerkonten gelöscht werden, finden Sie unter [Entfernen von Exchange Online-Daten](#removing-exchange-online-data).

#### <a name="end-user-identifiable-information"></a>Informationen zur Identifizierung von Endbenutzern

Informationen zur Identifizierung von Endbenutzern (End User Identifiable Information, EUII) beinhalten personenbezogene Daten und Kontaktinformationen zu den Mitarbeitern, die in Bookings geplant werden. Sie werden zu den Personaldetailseiten hinzugefügt, wenn der Geschäftsbesitzer Bookings einrichtet und nach der Einrichtung Aktualisierungen vornimmt. Sie enthalten den Namen, die Initialen, die E-Mail-Adresse und die Telefonnummer des Mitarbeiters. Diese Daten werden im Exchange Online-Postfach gespeichert, in dem Bookings gehostet wird.

Diese Daten werden so lange gespeichert, wie der Mitarbeiter im Dienst aktiv ist, es sei denn, er hat den Geschäftsbesitzer oder einen Administrator über die In-App-Benutzeroberfläche oder durch Löschen des entsprechenden Bookings-Postfachs explizit gelöscht. Wenn der Administrator die Löschung der Mitarbeiterdaten veranlasst oder wenn der Mitarbeiter den Dienst verlässt, werden seine Daten gemäß den vom Geschäftsbesitzer oder Administrator festgelegten Richtlinien für die Aufbewahrung von Inhalten im Exchange Online-Postfach gelöscht.

##### <a name="discoveraccess"></a>Ermitteln/Zugriff

Bookings erfasst und speichert die folgenden Arten von Daten:

- **Informationen zum Geschäftsprofil:** Kundeninhalte über das Unternehmen, das Bookings verwendet, werden über das Bookings-Unternehmensinformationsformular gesammelt und mit dem Business Center-Geschäftsprofil synchronisiert, wenn ein Kunde Bookings in Verbindung mit dem Business Center verwendet. Die einzige EUII diese Daten zugeordnet ist, ist eine E-Mail-Adresse des C1. An diese Adresse werden neue Buchungsbenachrichtigungen und Update-E-Mails gesendet.
- **Kundenkontakte:** Kontakte können manuell im Web-, iOS- und Android-Client von Bookings erstellt oder von einem mobilen Gerät importiert werden. Kontakte werden auch automatisch während der Nutzung der Self-Service-Buchungsseite angelegt. Sie enthalten EUII und werden im Bookings-Postfach gespeichert.
- **Mitarbeiterdetails:** Die Kundeninhalte enthalten Daten zu den Mitarbeitern, die berechtigt sind, die von den Web-, iOS- oder Android-Clients von Booking erstellten Dienste bereitzustellen. Mitarbeiterdetails können Namen, E-Mail-Adresse und Telefonnummer enthalten.
- **Booking-Ereignisse:** Hierbei handelt es sich um Kundenbesprechungen und zugehörige Kundeninhalte, die vom Unternehmen über einen Web-Client oder eine Android/iOS-App oder vom Kunden über eine öffentliche Buchungsseite (oder eine Facebook-Seite) erstellt wurden. Diese Ereignisse können Namen, Adresse, E-Mail-Adresse, Telefonnummer und Termindetails enthalten.
- **Besprechungsanfragen, E-Mail-Bestätigungen/Stornierungen/Updates und E-Mail-Erinnerungen:** Dies sind E-Mail-Nachrichten vom System im Zusammenhang mit Buchungen. Sie enthaltenen Mitarbeiter- und Kundendaten, die zum Zeitpunkt der Buchung eingegeben wurden.

##### <a name="export"></a>Exportieren

Für den Export von Daten, die dem Geschäftsbesitzer, Mitarbeitern und Kunden entsprechen, können Sie das [Geschäftscenter-Datenschutzportal](https://businessaccount.microsoft.com/) verwenden.

##### <a name="delete"></a>Löschen

Sie können die folgenden Arten von Bookings-Daten als Reaktion auf einen Antrag einer betroffenen Person auf Löschung löschen:

- **Geschäftsprofil-Informationen und Kontakte**: Sie können das Bookings-Postfach im Admin Center löschen. Nachdem Sie das Postfach gelöscht haben, können Sie es innerhalb von 30 Tagen wiederherstellen. Nach 30 Tagen werden das Konto und das entsprechende Postfach endgültig gelöscht. Weitere Informationen zum Löschen eines Benutzerkontos finden Sie im Abschnitt [Löschen eines Benutzers](#deleting-a-user).
- **Mitarbeiterdetails:** Sie können Mitarbeiter aus dem Bookings-Dashboard löschen. Um Mitarbeiter endgültig zu löschen, können Sie ihr Office 365-Konto löschen.
- **Bookings-Ereignisse:** Sie können Buchungsereignisse aus dem Bookings-Kalender löschen, wodurch die Daten des Kunden gelöscht werden.
- **Besprechungsanfragen, E-Mail-Bestätigungen/Stornierungen/Updates und E-Mail Erinnerungen:** Sie können diese aus dem Bookings-Kalender löschen, wodurch die Informationen des Kunden entfernt werden.

Für den Export von Daten, die dem Geschäftsbesitzer, Mitarbeitern und Kunden entsprechen, können Sie das [Geschäftscenter-Datenschutzportal](https://businessaccount.microsoft.com/) verwenden.

Zusätzlich können Sie Geschäftsinhaber- und Mitarbeiterdaten löschen, indem Sie das entsprechende Benutzerkonto löschen. Siehe den Abschnitt [Löschen eines Benutzers](#deleting-a-user).

#### <a name="listings"></a>Listings

In den folgenden Abschnitten wird erläutert, wie die in-App-Funktion in Microsoft Listings verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

##### <a name="discover"></a>Ermittlung

Listings-Besitzer können ihr Unternehmen mit Google, Bing, Yelp und Facebook verbinden, um eine aggregierte Ansicht der Bewertungen und Rezensionen zu erhalten. Listings sammelt und speichert die folgenden Arten von Daten:

- Google-Rezensionen und -Bewertungen
- Bing-Rezensionen und -Bewertungen
- Yelp-Rezensionen und -Bewertungen
- Facebook-Rezensionen und -Bewertungen

##### <a name="access"></a>Access
Listings-Besitzer können sich beim Listings-Dashboard anmelden und ihre Rezensionen und Bewertungen einsehen.

##### <a name="export"></a>Exportieren

Für den Export von Daten, die dem Geschäftsbesitzer, Mitarbeitern und Kunden entsprechen, können Sie das [Geschäftscenter-Datenschutzportal](https://businessaccount.microsoft.com/) verwenden.

##### <a name="delete"></a>Löschen

Wenn ein Listings-Besitzer seine Listings-Informationen löschen möchte, kann er die Verbindung zum Anbieter auf der Listings-Seite trennen. Nachdem sie die Verbindung getrennt haben, werden ihre Listings-Informationen gelöscht.

#### <a name="connections"></a>Connections

In den folgenden Abschnitten wird erläutert, wie die in-App-Funktion in Microsoft Connections verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

##### <a name="discover"></a>Ermittlung

Connections sammelt und speichert die folgenden Arten von Daten: 

- Kunden/Kontakte werden vom Unternehmen über den Web-Client oder die mobile App (iOS, Android) oder über die App erstellt, wenn ein Geschäftskontakt eine E-Mail-Marketingkampagne erhält. Zu den Kundendaten können Name, Adresse, E-Mail-Adresse und Steuernummer gehören. Die Kontakte werden in allen Geschäftscenter-Apps gemeinsam genutzt.
- Kunden können sich auf der Connections-Registrierungsseite registrieren und ihre personenbezogenen Daten speichern.
- Links von E-Mail-Kampagnen

##### <a name="access"></a>Access

Ein Connections-Besitzer kann sich im Connections-Dashboard anmelden und die von ihm gesendeten E-Mail-Kampagnen einsehen.

##### <a name="export"></a>Exportieren

Für den Export von Daten, die dem Geschäftsbesitzer, Mitarbeitern und Kunden entsprechen, können Sie das [Geschäftscenter-Datenschutzportal](https://businessaccount.microsoft.com/) verwenden.

##### <a name="delete"></a>Löschen

Nachdem ein Connections-Besitzer eine E-Mail-Kampagne verschickt hat, kann er die Kampagne nicht mehr löschen. Wenn es Entwürfe von Kampagnen gibt, die sie löschen möchten, können sie sich im Connections-Dashboard anmelden und die Entwürfe der Kampagnen löschen.

### <a name="education"></a>Education

In diesem Abschnitt wird erläutert, wie Sie die In-App-Funktionalität in den folgenden Microsoft Education-Apps verwenden können, um auf Anträge betroffener Personen zu reagieren.

- Aufgaben
- Kursnotizbuch

#### <a name="assignments"></a>Aufgaben

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Aufgaben verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

##### <a name="discoveraccess"></a>Ermitteln/Zugriff

Aufgaben speichert Informationen, die sowohl von Lehrern als auch von Kursteilnehmern erzeugt werden. Einige dieser Informationen werden in SharePoint gespeichert, andere an einem anderen Ort als SharePoint.

##### <a name="finding-assignments-data-stored-in-sharepoint"></a>Suchen nach Aufgabendaten, die in SharePoint gespeichert werden

Kursteilnehmerdateien, die mit einer Übermittlung für Aufgaben verbunden sind, werden in einer Dokumentenbibliothek (mit dem Namen **Arbeit von Kursteilnehmern**) gespeichert und Dateien, die mit Aufgaben verbunden sind, die von Lehrern erstellt wurden (und für Kursteilnehmer zugänglich sind) werden in einer anderen Dokumentenbibliothek (mit dem Namen **Kursdateien**) gespeichert. Beide Dokumentbibliotheken befinden sich in der entsprechenden SharePoint-Website des Kursteams.

Ein Admin kann mit der Inhaltssuche im Security & Compliance Center nach Kursteilnehmerdateien (in den Bibliotheken Arbeit von Kursteilnehmern und Kursdateien) suchen, die sich auf Übermittlungen zu Aufgaben und auf Dateien zu Aufgaben beziehen. Beispielsweise könnte ein Administrator alle SharePoint-Websites in der Organisation durchsuchen und in der Suchanfrage den Namen und den Kurs des Kursteilnehmers oder den Aufgabennamen verwenden, um nach Daten zu suchen, die für einen Antrag einer betroffenen Person relevant sind.

In ähnlicher Weise kann ein Administrator Lehrerdateien suchen, die sich auf Aufgaben für Dateien beziehen, die ein Lehrer an Kursteilnehmer verteilt hat. Beispielsweise könnte ein Administrator alle SharePoint-Websites in der Organisation durchsuchen und in der Suchanfrage den Namen und den Kurs des Lehrers oder den Aufgabennamen verwenden, um nach Daten zu suchen, die für einen Antrag einer betroffenen Person relevant sind.

Weitere Informationen finden Sie unter:

- [Dokumentation für Administratoren zu "Aufgaben"](/microsoft-365/education/deploy/assignments-admin-documentation)
- [Reagieren auf Anträge betroffener Personen mit dem eDiscovery-Tool für die Inhaltssuche](#using-the-content-search-ediscovery-tool-to-respond-to-dsrs) (in diesem Leitfaden)

##### <a name="finding-assignments-data-not-stored-in-sharepoint"></a>Suchen nach Aufgabendaten, die nicht in SharePoint gespeichert werden

Die folgenden Arten von Aufgabendaten werden nicht auf der SharePoint-Website des Kursteams gespeichert und sind daher über die Inhaltssuche nicht auffindbar. Dazu gehören unter anderem die folgenden Daten:

- Kursteilnehmerergebnisse und Feedback des Lehrers
- Die Liste der von jedem Teilnehmer für eine Aufgabe eingereichten Dokumente
- Details der Aufgabe, z. B. das Datum, an dem die Aufgabe fällig ist

Um Daten zu finden, muss ein Administrator oder ein Lehrer auf der Website des Kursteams nach Daten suchen, die für einen Antrag einer betroffenen Person relevant sein könnten. Ein Administrator kann sich selbst als Besitzer in den Kurs eintragen und alle Aufgaben für dieses Kursteam einsehen.

Auch wenn ein Kursteilnehmer nicht mehr Teil eines Kurses ist, können seine Daten im Kurs vorhanden sein und als „nicht mehr eingeschrieben“ gekennzeichnet sein. In diesem Fall müsste ein Kursteilnehmer, der einen Antrag einer betroffenen Person stellt, dem Administrator die Liste der Kurse zur Verfügung stellen, in denen er eingeschrieben war.

##### <a name="export"></a>Exportieren

Sie können Aufgabendaten eines bestimmten Kursteilnehmers für alle Klassen exportieren, in denen der Kursteilnehmer registriert ist, indem Sie ein PowerShell-Skript verwenden, um eine Liste der Kurse des Kursteilnehmers abzurufen und dann ein PowerShell-Skript zum Exportieren der Daten verwenden. Siehe:

- [Konfigurieren von Aufgaben für Teams](/microsoft-365/education/deploy/configure-assignments-for-teams)
- [Abrufen einer Kursliste für einen bestimmten Kursteilnehmer](/microsoft-365/education/deploy/assignments-script-get)
- [Exportieren von Kursteilnehmer- und Lehrerdaten aus Aufgaben](/microsoft-365/education/deploy/assignments-script-export)

Wenn der Kursteilnehmer von der Teamkurs-Website entfernt wurde, kann der Administrator den Kursteilnehmer zurück zur Website hinzufügen, bevor er das Exportskript ausführt. Oder der Administrator kann die Eingabedatei für das Skript verwenden, um jeden Kurs zu identifizieren, in dem der Kursteilnehmer jemals eingeschrieben war. Sie können auch das Aufgabenexportskript verwenden, um die Übermittlungsdaten für alle Aufgaben zu exportieren, auf die ein Lehrer Zugriff hat.

##### <a name="delete"></a>Löschen

Sie können Aufgabendaten eines bestimmten Kursteilnehmers für alle Klassen löschen, in denen der Kursteilnehmer registriert ist, indem Sie ein PowerShell-Skript verwenden, um eine Liste der Kurse des Kursteilnehmers abzurufen und dann ein PowerShell-Skript zum Löschen der Daten verwenden. Sie sollten dies tun, bevor Sie den Kursteilnehmer aus dem Kurs entfernen. Siehe:

- [Konfigurieren von Aufgaben für Teams](/microsoft-365/education/deploy/configure-assignments-for-teams)
- [Abrufen einer Kursliste für einen bestimmten Kursteilnehmer](/microsoft-365/education/deploy/assignments-script-get)
- [Löschen von Teilnehmerdaten aus Aufgaben](/microsoft-365/education/deploy/assignments-script-delete)

Wenn der Kursteilnehmer von der Teamkurs-Website entfernt wurde, kann der Administrator den Kursteilnehmer zurück zur Website hinzufügen, bevor er das Exportskript ausführt. Oder der Administrator kann die Eingabedatei für das Skript verwenden, um jeden Kurs zu identifizieren, in dem der Kursteilnehmer jemals eingeschrieben war. Sie können das Aufgaben-Löschskript nicht zum Löschen von Lehrerdaten verwenden, da alle Aufgaben auf der Website des Kursteams gemeinsam genutzt werden. Als Alternative müsste sich ein Administrator auf der Seite des Kursteams eintragen und dann eine bestimmte Aufgabe löschen.

#### <a name="class-notebook"></a>Kursnotizbuch

Die Suche nach Inhalten im Kursnotizbuch wurde bereits in diesem Leitfaden erläutert. Gehen Sie hierzu zum Abschnitt [OneNote-Kursnotizbuch](#onenote-class-notebook). Sie können außerdem das Tool für die Inhaltssuche verwenden, um Daten aus einem Kursnotizbuch zu exportieren. Alternativ können ein Administrator oder die betroffene Person Daten aus einem Kursnotizbuch exportieren. Informationen hierzu finden Sie unter [Speichern einer Kopie eines Kursnotizbuchs](https://support.office.com/article/44733e18-0ef1-4d4b-be51-fc2ac5bfe9ec).

### <a name="flow"></a>Flow

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Microsoft Flow verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

#### <a name="discover"></a>Ermittlung

Mit Flow können Personen datenbezogene Aufgaben wie das Synchronisieren von Dateien zwischen Anwendungen, das Kopieren von Dateien von einem Office 365-Dienst zu einem anderen und das Sammeln von Daten aus einer Office 365-Anwendung und deren Speicherung in einer anderen ausführen. Beispielsweise könnte ein Benutzer einen Fluss einrichten, um Outlook-E-Mail-Anhänge in seinem OneDrive for Business-Konto zu speichern. In diesem Beispiel können Sie das Tool für die Inhaltssuche verwenden, um das Postfach des Benutzers nach der E-Mail-Nachricht zu durchsuchen, die den Anhang enthält, oder das OneDrive for Business-Konto nach der Datei durchsuchen. Dies ist ein Beispiel, bei dem Daten, die von Flow verarbeitet werden, in den Office 365-Diensten, die durch einen Flow-Workflow verbunden sind, auffindbar sein könnten.

Darüber hinaus können Personen mit Flow Dateien von Office 365 zu einem externen Dienst, wie z. B. Dropbox, kopieren oder hochladen. In diesen Fällen müsste ein Antrag einer betroffenen Person bezüglich der Daten in einem externen Dienst an den externen Dienst gestellt werden, der die Daten in einem solchen Szenario verarbeitet.

Wenn ein Administrator einen Antrag einer betroffenen Person erhält, kann er sich selbst als Besitzer der Flüsse eines Benutzers hinzufügen. Dies ermöglicht es einem Administrator, Funktionen wie das Exportieren von Flussdefinitionen, das Ausführen von Verläufen und das erneute Zuweisen von Flussberechtigungen auszuführen. Siehe [Verwalten von Flows im Admin Center](https://flow.microsoft.com/blog/managing-flow-resources-in-the-admin-center/).

Die Fähigkeit eines Administrators, sich selbst als Besitzer eines Flusses hinzuzufügen, erfordert ein Konto mit den folgenden Berechtigungen:

- Flow/PowerApps-Lizenz Plan 2 (kostenpflichtig oder Testabonnement)

- [Globaler Administrator\ ](/microsoft-365/admin/add-users/assign-admin-roles)

    oder

- [Globaler Azure Active Directory-Administrator](/azure/active-directory/active-directory-assign-admin-roles-azure-portal)

Mit diesen Rechten kann der Administrator über das Flow admin center auf alle Flüsse im Unternehmen zugreifen.

Um sich selbst als Besitzer eines Flusses hinzuzufügen.

1. Wechseln Sie zu <https://admin.flow.microsoft.com>.
2. Melden Sie sich mit Ihrem Office 365-Anmeldeinformationen an.
3. Wählen Sie auf der Seite **Umgebungen** die Umgebung für die Flüsse, auf die Sie zugreifen möchten. Organisationen verfügen über eine Standardumgebung.
4. Wählen Sie auf der Seite für die ausgewählte Umgebung **Ressourcen** und dann **Flows**. Eine Liste aller Flüsse in der Umgebung wird angezeigt.
5. Wählen Sie **Details anzeigen** für den Fluss, für den Sie sich selbst als Mitglied hinzufügen möchten.
6. Wählen Sie unter **Besitzer** **Verwalten der Freigabe**.
7. Auf dem Fly-out **Freigeben** fügen Sie sich selbst als Mitglied hinzu und speichern Sie dann die Änderung.

Nachdem Sie sich selbst zu einem Besitzer gemacht haben, wechseln Sie zu **Fluss** \> **Meine Flüsse** \> **Teamflüsse**, um auf den Fluss zuzugreifen. Von dort aus können Sie den Ausführungsverlauf herunterladen oder den Fluss exportieren. Siehe:

- [Herunterladen des Ausführungsverlaufs](https://flow.microsoft.com/blog/download-history-recurrence/)
- [Exportieren und Importieren Ihrer Flüsse umgebungsübergreifend mit Verpacken](https://flow.microsoft.com/blog/import-export-bap-packages/)

#### <a name="access"></a>Zugriff

Ein Benutzer auf die Definitionen und Ausführungsverläufe ihre Flüsse zugreifen.

- **Flussdefinitionen:** Ein Benutzer kann die Definition eines Flusses (die als Flusspaket exportiert und als JSON in einer ZIP-Datei formatiert wird) exportieren. Siehe [Exportieren und Importieren Ihrer Flüsse umgebungsübergreifend mit Verpacken](https://flow.microsoft.com/blog/import-export-bap-packages/).
- **Ausführungsverläufe:** Ein Benutzer kann den Ausführungsverlauf jedes seiner Abläufe herunterladen. Ein Ausführungsverlauf wird als CSV-Datei heruntergeladen, die zum Filtern oder Durchsuchen in Excel geöffnet werden kann. Benutzer können auch den Ausführungsverlauf mehrerer Flüsse herunterladen. Siehe hierzu [Herunterladen des Ausführungsverlaufs](https://flow.microsoft.com/blog/download-history-recurrence/).

#### <a name="delete"></a>Löschen

Ein Admin kann sich selbst als Besitzer der Flüsse eines Benutzers im Flow Admin Center hinzufügen. Wenn ein Benutzer Ihr Unternehmen verlässt und sein Office 365-Konto gelöscht wird, werden die Flüsse, deren alleiniger Besitzer er ist, beibehalten. Dies soll Ihrem Unternehmen helfen, die Flüsse auf neue Besitzer umzustellen und jegliche Unterbrechung Ihres Geschäfts für Flüsse, die für gemeinsame Geschäftsprozesse verwendet werden können, zu vermeiden. Ein Administrator muss dann entscheiden, ob er die Flüsse, die sich im Besitz des Benutzers befanden, löschen oder neuen Besitzern zuweisen möchte, und diese Aktion durchführen.

Wenn ein Benutzer auf Ihrem Unternehmen gelöscht wurde, wird sein Name bei freigegebenen Flüssen aus der Liste der Besitzer entfernt.

#### <a name="export"></a>Exportieren

Ein Administrator kann die Definition und den Ausführungsverlauf der Flüsse eines Benutzers exportieren. Dazu muss sich ein Administrator als Besitzer des Flusses des Benutzers im Flow Admin Center hinzufügen.

- **Flussdefinitionen**: Nachdem ein Administrator sich selbst als Besitzer eines Flusses hinzugefügt hat, kann er zu **Fluss** \> **Meine Flüsse** \> **Teamflows** wechseln, um die Definition eines Flusses (die als Flusspaket exportiert und als JSON in einer ZIP-Datei formatiert wird) zu exportieren. Siehe [Exportieren und Importieren Ihrer Flüsse umgebungsübergreifend mit Verpacken](https://flow.microsoft.com/blog/import-export-bap-packages/).

- **Ausführungsverläufe:** Ebenso muss sich ein Administrator selbst als Besitzer eines Flusses hinzufügen, um dessen Ausführungsverlauf zu exportieren. Ein Ausführungsverlauf wird als CSV-Datei heruntergeladen. Diese kann zum Filtern oder Durchsuchen in Excel geöffnet werden. Sie können auch den Ausführungsverlauf mehrerer Flüsse herunterladen, sofern Sie deren Besitzer sind. Siehe hierzu [Herunterladen des Ausführungsverlaufs](https://flow.microsoft.com/blog/download-history-recurrence/).

#### <a name="connections-and-custom-connectors-in-flow"></a>Verbindungen und benutzerdefinierte Connectors in Flow

Verbindungen erfordern, dass Benutzer Anmeldeinformationen für die Verbindung mit APIs, SaaS-Anwendungen und benutzerdefinierte Systeme bereitstellen. Diese Verbindungen gehören dem Benutzer, der die Verbindung eingerichtet hat, und können im Produkt [verwaltet](/flow/add-manage-connections) werden. Nachdem Flüsse neu zugewiesen wurden, kann ein Administrator PowerShell-Cmdlets verwenden, um diese Verbindungen im Rahmen der Löschung von Benutzerdaten aufzuführen und zu löschen.

Benutzerdefinierte Connectors ermöglichen es Unternehmen, die Funktionen von Flow zu erweitern, indem es mit Systemen verbunden wird, für die ein Out-of-Box-Connector nicht verfügbar ist. Der Autor eines benutzerdefinierten Connectors kann seinen Connector mit Dritten innerhalb seines Unternehmens [teilen](/flow/register-custom-api). Nach Erhalt eines Antrags einer betroffenen Person auf Löschung sollte ein Administrator diese Connectors neuen Besitzern zuweisen, um Betriebsunterbrechungen zu vermeiden. Um diesen Prozess zu beschleunigen, kann ein Administrator PowerShell-Cmdlets verwenden, um benutzerdefinierte Connectors aufzulisten, neu zuzuweisen oder zu löschen.

### <a name="forms"></a>Formulare

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion von Microsoft Forms verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

#### <a name="discover"></a>Ermittlung

Benutzer von Forms können zu <https://forms.office.com> gehen und **Meine Formulare** auswählen, um die von ihnen erstellten Formulare anzuzeigen. Sie können auch **Für mich freigegeben** auswählen, um Formulare anzuzeigen, die andere über einen Link freigegeben haben. Wenn es viele Formulare gibt, die durchsucht werden müssen, können Benutzer die produktinterne Suchleiste verwenden, um nach Formularen nach Titel oder Autor zu suchen. Um festzustellen, ob Microsoft Forms ein Ort ist, an dem personenbezogene Daten, die für Ihre Anforderung einer betroffenen Person relevant sind, wahrscheinlich gespeichert sind, können Sie die betroffene Person bitten, seine Liste **Für mich freigegeben** zu durchsuchen, um festzustellen, welche Benutzer ("Formularbesitzer") Formulare an die betroffene Person gesendet haben. Sie können dann die Formularbesitzer bitten, **Freigeben** in der oberen Navigationsleiste auszuwählen und Ihnen einen Link zu einem bestimmten Formular zu senden, damit Sie es ansehen und weiter bestimmen können, ob es für Ihren Antrag einer betroffenen Person relevant ist.

#### <a name="access"></a>Access

Nachdem die entsprechenden Formulare gefunden wurden, können Sie auf die Antworten zum Formular zugreifen, indem Sie auf die Registerkarte **Antworten** klicken. Erfahren Sie mehr darüber, wie Sie Ihre [Quizergebnisse](https://support.microsoft.com/office/check-and-share-your-quiz-results-c4a9b45c-d62f-4eb7-b5db-ad81892c7c07) oder [Formularergebnisse](https://support.office.com/article/02859424-341d-406f-b32a-9a0fbaf357af) überprüfen können. Um die Antwortergebnisse in Excel zu überprüfen, wählen Sie die Registerkarte **Antworten** aus, und wählen Sie dann **In Excel öffnen**. Wenn Sie der betroffenen Person eine Kopie des Formulars zusenden möchten, können Sie entweder Screenshots der relevanten Fragen und Antworten erstellen, die in der Anwendung im Rich-Text-Format angezeigt werden, oder der betroffenen Person eine Excel-Kopie der Ergebnisse zusenden. Wenn Sie Excel verwenden und nur Teile des Umfrageergebnisses mit der betroffenen Person teilen möchten, können Sie bestimmte Zeilen oder Spalten löschen oder die restlichen Abschnitte bearbeiten, bevor Sie die Ergebnisse weitergeben. Alternativ können Sie auch zu **Freigeben \> Link zum Duplizieren abrufen** (unter „Freigeben als Vorlage“), um der betroffenen Person eine Kopie des gesamten Formulars zur Verfügung zu stellen.

#### <a name="delete"></a>Löschen

Alle Umfragen, Quizze, Fragebögen oder Abstimmungen können vom Besitzer dauerhaft gelöscht werden. Wenn Sie einen Antrag einer betroffenen Person auf „Meine persönlichen Informationen löschen“ annehmen und ein Formular vollständig löschen möchten, suchen Sie das Formular in der Liste der Formulare, wählen Sie die Punktereihe (Ellipse) in der oberen rechten Ecke des Formularvorschaufensters aus, und wählen Sie dann **Löschen**. Ein einmal gelöschtes Formular kann nicht mehr aufgerufen werden. Informationen hierzu finden Sie unter [Löschen eines Formulars](https://support.microsoft.com/office/delete-a-form-2207e468-ce1b-4c4a-a256-caf631d87af0).

#### <a name="export"></a>Exportieren

Um Formularfragen und -antworten in eine Excel-Datei zu exportieren, öffnen Sie das Formular, wählen Sie die Registerkarte **Antworten** und wählen Sie anschließend **In Excel öffnen** aus.

### <a name="kaizala"></a>Kaizala

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Microsoft Kaizala verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

#### <a name="discover"></a>Ermittlung

Die Organisationsdaten eines Benutzers, d. h. Daten, die in Organisationsgruppen geteilt werden, können von einem Administrator über das Kaizala-Verwaltungsportal abgerufen werden. Organisationsdaten werden für einen Zeitraum aufbewahrt, der durch die Aufbewahrungsrichtlinien Ihrer Organisation bestimmt wird. Zusätzlich zu den Benutzerdaten speichern die Kaizala-Server auch die folgenden Arten von Organisationsdaten:

- Liste der Mitglieder, die der Organisationsgruppe angehören
- Daten der Organisationsgruppennachrichten, d. h. Nachrichten und Antworten, die über Organisationsgruppen hinweg ausgetauscht werden
- Eine Liste der Benutzer in den Organisationen
- Nutzungsdaten von Produkten und Diensten, die für alle Benutzer in der Organisation erfasst wurden
- Von der Organisation erstellte Kaizala-Aktionen
- Kaizala-Konnektorendaten

Auf die Verbraucherdaten eines Benutzers kann die betroffene Person über die mobile Kaizala-App für Verbraucherdaten zugreifen. Zu den Verbraucherdaten gehören die folgenden Arten von Daten:

- Daten von privaten Gruppen auf Kaizala (Speicherung auf Kaizala-Servern für 90 Tage)
- Profilinformationen eines Benutzers und Kontakte des Benutzers
- Liste der Mitglieder, die derselben Gruppe wie der Benutzer angehören
- Gruppennachrichten und -antworten, die über Gruppen hinweg ausgetauscht werden
- Die Kontaktliste des Benutzers (im Kaizala-Dienst gespeichert)
- Transaktionen des Benutzers auf Kaizala (gilt nur für Kaizala-Benutzer in Indien)
- Nutzungsdaten für Produkte und Dienste für den Benutzer

#### <a name="access"></a>Zugriff

Kaizala-Benutzer können ihr mobiles Gerät nutzen, um Kaizala-Inhalte zu sehen, die sie auf ihrem Gerät erstellt haben. Um festzustellen, ob in den mobilen Kaizala möglicherweise personenbezogene Daten gespeichert werden, die für einen Antrag einer betroffenen Person relevant sind, können Sie die betroffene Person bitten, ihre Kaizala-App nach den gewünschten Informationen zu durchsuchen.

#### <a name="export"></a>Exportieren

Wenn Benutzer in Ihrer Organisation Kaizala verwenden, werden Verbraucherdaten generiert, und Organisationsdaten können generiert werden, wenn der Benutzer an einer Organisationsgruppe teilnimmt. Administratoren können die Organisationsdaten eines Benutzers aus dem Kaizala-Verwaltungsportal exportieren. Kaizala-Verbraucherbenutzer können ihre privaten Daten aus der mobilen Kaizala-App exportieren. In beiden Fällen ist zu beachten, dass Produkt- und Dienstnutzungsdaten auch exportiert werden, wenn ein Administrator oder Benutzer Kaizala-Daten exportiert. Details finden Sie unter:

- [Exportieren oder Löschen von Organisationsdaten eines Benutzers in Kaizala](/office365/kaizala/export-or-delete-a-user-s-data)
- [Exportieren oder Löschen von Daten in der mobilen Kaizala-App](/office365/kaizala/export-or-delete-your-data)

#### <a name="delete"></a>Löschen

Ein Kaizala-Administrator kann das Konto eines Kaizala-Benutzers im Kaizala-Verwaltungsportal löschen. Nach dem Löschen eines Benutzerkontos wird der Benutzer aus allen Gruppen entfernt, die zu Ihrer Organisation gehören, und die Organisationsdaten werden von ihrem Gerät gelöscht. 

Um alle privaten Daten vom mobilen Gerät des Benutzers zu entfernen, kann der Kaizala-Benutzer sein Kaizala-Konto löschen. Nachdem das Konto gelöscht wurde, werden alle zugehörigen Kaizala-Inhalte wie Chats, Fotos und andere Daten vom Gerät gelöscht.

Weitere Informationen finden Sie unter:

- [Exportieren oder Löschen von Organisationsdaten eines Benutzers in Kaizala](/office365/kaizala/export-or-delete-a-user-s-data)
- [Exportieren oder Löschen von Daten in der mobilen Kaizala-App](/office365/kaizala/export-or-delete-your-data)

### <a name="planner"></a>Planner

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Microsoft Planner verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

#### <a name="discover"></a>Entdecken

Planner-Pläne sind mit einer Microsoft 365-Gruppe verknüpft, und die Dateien für Microsoft 365-Gruppen werden in einer der Gruppe zugeordneten SharePoint Online-Website gespeichert. Das bedeutet, dass Sie die Inhaltssuche verwenden können, um nach Planner-Dateien zu suchen, indem Sie die Website nach der Microsoft 365-Gruppe durchsuchen. Zu diesem Zweck benötigen Sie die URL für die Microsoft 365-Gruppe. Im Hilfethema "Inhaltssuche in Office 365" unter [Durchsuchen von Microsoft Teams und Microsoft 365-Gruppen](/microsoft-365/compliance/content-search) finden Sie Tipps zum Abrufen von Informationen zu Microsoft 365-Gruppen für die Suche nach Planner-Dateien in der jeweiligen SharePoint Online-Website.

#### <a name="access"></a>Access

Wie bereits erläutert können Sie die zugrunde liegende SharePoint Online-Website und das Postfach, die einem Plan zugeordnet sind, suchen. Dann können Sie eine Vorschau anzeigen oder die zugehörigen Suchergebnisse herunterzuladen, um auf Daten zuzugreifen.

#### <a name="delete"></a>Löschen

Sie können die personenbezogenen Daten eines Benutzers manuell löschen, indem Sie sich selbst die Zugriffsberechtigung für die Pläne erteilen, denen der Benutzer angehört, oder indem Sie sich als der Benutzer anmelden, um die Änderungen vorzunehmen. Siehe [Benutzerdaten in Microsoft Planner löschen](https://support.office.com/article/delete-user-data-in-microsoft-planner-4349ded2-1891-4896-8e27-05fd40f3929f).

#### <a name="export"></a>Exportieren

Sie können ein PowerShell-Skript verwenden, um die Daten eines Benutzers aus Planner zu exportieren. Wenn Sie die Daten exportieren, wird eine separate JSON-Datei für jeden Plan exportiert, dem der Benutzer angehört. Siehe [Benutzerdaten aus Microsoft Planner exportieren](https://support.office.com/article/export-user-data-from-microsoft-planner-91258c96-b353-4da1-b6d9-d78e4809cf08).

### <a name="power-bi"></a>Power BI

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Microsoft Power BI verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

#### <a name="discover"></a>Ermittlung
Sie können nach Inhalten in den verschiedenen Arbeitsbereichen von Power BI suchen, darunter Dashboards, Berichte, Arbeitsmappen und Datensätze. Jeder Typ von Arbeitsbereich enthält ein Suchfeld, mit dem Sie diesen Arbeitsbereich durchsuchen können. Siehe [Suchen, Finden und Sortieren von Inhalten im Power BI-Dienst](/power-bi/service-navigation-search-filter-sort).

#### <a name="access"></a>Access

Sie können Dashboards, Berichte und visuelle Objekte aus Berichten in Power BI drucken, um eine physische Kopie zu erzeugen. Sie können jedoch nicht ganze Berichte, sondern jeweils nur eine Seite drucken. Gehen Sie hierzu zu einem Bericht, nutzen Sie das Suchfeld, um nach bestimmten Daten zu suchen, und drucken Sie dann die betreffende Seite aus. Siehe [Drucken aus Power BI-Dienst](/power-bi/service-print).

#### <a name="delete"></a>Löschen

Um Dashboards, Berichte und und Arbeitsmappen zu löschen, siehe [Allgemeines löschen im Power BI-Dienst](/power-bi/service-delete).

Das Löschen eines Dashboards, Berichts oder einer Arbeitsmappe löscht nicht das zugrunde liegende Dataset. Da Power BI auf einer Live Connection zu den zugrunde liegenden Quelldaten basiert, muss die Löschung personenbezogener Daten dort vorgenommen werden. (Beispielsweise wenn Sie einen Power BI-Bericht erstellen, der mit Dynamics 365 for Sales als Live-Quelldaten verbunden ist, müssten Sie Korrekturen an den Daten in Dynamics 365 for Sales vornehmen.)

Nachdem die Daten gelöscht sind, können Sie die Funktion [Geplante Datenaktualisierung](/power-bi/refresh-scheduled-refresh) in Power BI verwenden, um das Dataset zu aktualisieren, das in Power BI gespeichert ist. Danach werden die gelöschten Daten nicht mehr in Berichten oder Dashboards von Power BI angezeigt, die die Daten genutzt haben. Um die Anforderungen der DSGVO einzuhalten, sollten Sie Richtlinien eingeführt haben, um sicherzustellen, dass die Daten in angemessenen Abständen aktualisiert werden.

#### <a name="export"></a>Export

Um einen Antrag auf Datenübertragbarkeit zu erfüllen, können Sie Dashboard und Berichte aus Power BI exportieren:

- Sie können die zugrunde liegenden Daten für Dashboards und Berichte in eine statische Excel-Datei exportieren. Sehen Sie sich das Video [Drucken aus Power BI-Dienst](/power-bi/service-print) an. Mithilfe von Excel können Sie die personenbezogenen Daten dann bearbeiten, die in den Antrag auf Übertragbarkeit eingeschlossen werden sollen, und sie in einem gängigen, maschinenlesbaren Format wie as .csv oder .xml speichern.
- Sie können einen Bericht aus dem Power BI-Dienst in Office 365 in eine .pbix-Datei exportieren (herunterladen), wenn dieser ursprünglich mit Power BI Desktop veröffentlicht wurde. Sie können diese Datei dann in den Power BI Desktop-Dienst eines anderen Unternehmens importieren. Siehe [Bericht aus Power BI-Dienst in Desktop exportieren](/power-bi/service-export-to-pbix).

### <a name="powerapps"></a>PowerApps

In den folgenden Abschnitten wird erläutert, wie die in-App-Funktion in Microsoft Power-Apps verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen. Diese Schritte zeigen, wie ein Administrator Apps und die dazugehörigen Ressourcen an neue Besitzer übertragen kann, um Betriebsunterbrechungen zu beschränken.

#### <a name="discover"></a>Entdecken

PowerApps ist ein Dienst zum Erstellen von Apps, die innerhalb Ihres Unternehmens freigegeben und verwendet werden können. Im Rahmen dieses Prozesses der Erstellung oder Nutzung einer App speichert der Benutzer mehrere Arten von Ressourcen und Daten im PowerApps-Dienst, darunter Apps, Umgebungen, Verbindungen, benutzerdefinierte Connectors und Zustimmungen.

Um einen Antrag betroffener Personen bezüglich PowerApps zu erfüllen, können Sie die Verwaltungsvorgänge, die im [PowerApps Admin Center](https://admin.powerapps.com/) zur Verfügung stehen, sowie [PowerApps Admin PowerShell-Cmdlets](https://go.microsoft.com/fwlink/?linkid=871804) nutzen. Für den Zugriff auf diese Tools ist ein Konto mit den folgenden Berechtigungen erforderlich:

- Eine kostenpflichtige PowerApps Plan 2-Lizenz oder eine PowerApps Plan 2-Testlizenz. Sie können sich [hier](https://web.powerapps.com/trial) für eine 30-tägige Testlizenz registrieren.
- [Globaler Administrator](/microsoft-365/admin/add-users/assign-admin-roles) oder
- [Globaler Azure Active Directory-Administrator](/azure/active-directory/active-directory-assign-admin-roles-azure-portal)

Weitere Informationen zur Suche von personenbezogenen Daten finden Sie unter [Personenbezogene Daten in PowerApps ermitteln](https://go.microsoft.com/fwlink/?linkid=871880).

Der PowerApps-Dienst umfasst darüber hinaus den Common Data Service für Apps, mit dem Benutzer Daten in standardmäßigen und benutzerdefinierten Einheiten innerhalb einer Common Data Service-Datenbank speichern können. Sie können die in diesen Einheiten gespeicherten Daten im [PowerApps Maker Portal](https://web.powerapps.com) anzeigen und die Suchfunktionen des Produkts zur [Erweiterten Suche](/dynamics365/customer-engagement/basics/save-advanced-find-search) nutzen, um in der Einheit nach spezifischen Daten zu suchen. Weitere Einzelheiten zur Ermittlung personenbezogener Daten im Common Data Service finden Sie unter [Personenbezogene Daten in Common Data Service ermitteln](https://go.microsoft.com/fwlink/?linkid=871881).

#### <a name="access"></a>Access

Administratoren können sich selbst Berechtigungen zuweisen, um auf Apps und die dazugehörigen Ressourcen zuzugreifen und diese auszuführen (darunter Flows, Verbindungen und benutzerdefinierte Connectors) mithilfe des [PowerApps Admin Center](https://admin.powerapps.com/) oder mithilfe von [PowerApps Admin PowerShell-Cmdlets](https://go.microsoft.com/fwlink/?linkid=871804).

Nachdem Sie den Zugriff auf die App des Benutzers haben, können Sie einen Webbrowser verwenden, um die App zu öffnen. Nachdem Sie eine App geöffnet haben, können Sie einen Screenshot der Daten machen. Siehe [PowerApps in einem Webbrowser verwenden](/powerapps/run-app-browser).

#### <a name="delete"></a>Löschen

Da PowerApps den Benutzern die Erstellung von Branchenanwendungen ermöglicht, die ein wesentlicher Bestandteil der täglichen Abläufe Ihrer Organisation sein können, muss der Administrator festlegen, ob die Apps eines Benutzers gelöscht werden müssen oder nur neuen Besitzern zugewiesen werden müssen, wenn ein Benutzer Ihre Organisation verlässt und sein Office 365-Konto gelöscht wird. Dies soll Ihre Organisation dabei unterstützen, Apps auf neue Besitzer zu übertragen und Unterbrechungen Ihres Betriebs für Apps einzuschränken, die für gemeinsame Geschäftsprozesse verwendet werden können.

Bei freigegebenen Daten wie Apps müssen Administratoren entscheiden, ob sie die freigegebenen Daten des Benutzers dauerhaft löschen möchten oder sie durch deren Neuzuweisung an sich selbst oder einen Dritten innerhalb ihres Unternehmens erhalten wollen. Siehe [Löschen personenbezogener Daten aus PowerApps](https://go.microsoft.com/fwlink/?linkid=871883).

Alle Daten, die von einem Benutzer in einer Einheit in einer Common Data Service für Apps-Datenbank gespeichert wurden, müssen außerdem von einem Administrator geprüft und (wenn erwünscht) mithilfe der produkteigenen Funktionen gelöscht werden. Siehe [Personenbezogene Daten eines Benutzers aus Common Data Service löschen](https://go.microsoft.com/fwlink/?linkid=871886).

#### <a name="export"></a>Exportieren

Administratoren haben die Möglichkeit, die für einen Benutzer innerhalb des PowerApps-Dienstes gespeicherten personenbezogenen Daten mithilfe des [PowerApps Admin Center](https://admin.powerapps.com/) und mithilfe von [PowerApps Admin-PowerShell-Cmdlets](https://go.microsoft.com/fwlink/?linkid=871804) zu exportieren. Siehe [Personenbezogene Daten aus PowerApps exportieren](https://go.microsoft.com/fwlink/?linkid=871883).

Sie können Sie auch die produkteigenen Suchfunktionen der [Erweiterten Suche](/dynamics365/customer-engagement/basics/save-advanced-find-search) nutzen, um nach den personenbezogenen Daten eines Benutzers in allen Einheiten zu suchen. Einzelheiten zum Export von personenbezogenen Daten aus dem Common Data Service finden Sie unter [Personenbezogene Daten aus Common Data Service exportieren](https://go.microsoft.com/fwlink/?linkid=871889).

#### <a name="connections-and-custom-connectors-in-powerapps"></a>Verbindungen und benutzerdefinierte Connectors in PowerApps

Verbindungen erfordern, dass Benutzer Anmeldeinformationen für die Verbindung mit APIs, SaaS-Anwendungen und benutzerdefinierte Systeme bereitstellen. Diese Verbindungen gehören dem Benutzer, der die Verbindung eingerichtet hat, und können im Produkt [verwaltet](/powerapps/maker/canvas-apps/add-data-connection) werden. Nachdem PowerApps neu zugewiesen wurden, kann ein Administrator PowerShell-Cmdlets verwenden, um diese Verbindungen im Rahmen der Löschung von Benutzerdaten aufzuführen und zu löschen.

Benutzerdefinierte Connectors ermöglichen es Unternehmen, die Funktionen von PowerApps zu erweitern, indem es mit Systemen verbunden wird, für die ein Out-of-Box-Connector nicht verfügbar ist. Der Autor eines benutzerdefinierten Connectors kann seinen Connector mit Dritten innerhalb seines Unternehmens [teilen](/connectors/custom-connectors/use-custom-connector-powerapps). Nach Erhalt eines Antrags einer betroffenen Person auf Löschung sollte ein Administrator diese Connectors neuen Besitzern zuweisen, um Betriebsunterbrechungen zu vermeiden. Um diesen Prozess zu beschleunigen, kann ein Administrator PowerShell-Cmdlets verwenden, um benutzerdefinierte Connectors aufzulisten, neu zuzuweisen oder zu löschen.

### <a name="project-online"></a>Project Online

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Microsoft Project Online verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

#### <a name="discover-and-access"></a>Ermittlung und Zugriff

Sie können die SharePoint-Online-Website, die mit einem Projekt verbunden ist (beim Erstellen eines Projekts besteht eine Option zur Erstellung einer verbundenen SharePoint-Online-Website) mithilfe der Inhaltssuche durchsuchen; die Inhaltssuche durchsucht nicht die Daten in einem tatsächlichen Projekt in Project Online, sondern nur die verbundene Seite. Die Inhaltssuche sucht jedoch nach Metadaten über Projekte und Personen, die im Betreff genannt werden. Dies kann Ihnen jedoch bei der Suche nach (und beim Zugriff auf) das Projekt helfen, das die mit dem Antrag der betroffenen Personen verbundenen Daten enthält.

> [!TIP]
> Die URL für die Websitesammlung in Ihrer Organisation, in der Websites mit Projekten verknüpft sind, lautet `https://<your org>.sharepoint.com/sites/pwa`; zum Beispiel, **<https://contoso.sharepoint.com/pwa>**. Sie können diese spezifische Websitesammlung als Speicherort Ihrer Inhaltssuche und dann den Namen des Projekts in der Suchanfrage verwenden. Zusätzlich kann ein IT-Administrator die Websitesammlungsseite im SharePoint Online Admin Center verwenden, um eine Liste der PWA-Websitesammlungen in der Organisation zu erhalten.

#### <a name="delete"></a>Löschen

Sie können Informationen über einen Benutzer aus Ihrer Project Online-Umgebung löschen. Siehe [Benutzerdaten aus Project Online löschen](https://support.office.com/article/delete-user-data-from-project-online-252fa593-9c25-47ed-b861-643fe8bf1cb7).

#### <a name="export"></a>Exportieren

Sie können die Inhalte eines bestimmten Benutzers aus Ihrer Project Online-Umgebung exportieren. Diese Daten werden in mehrere Dateien des JSON-Formats exportiert. Schrittweise Anweisungen finden Sie unter [Benutzerdaten aus Project Online exportiert](https://support.office.com/article/export-user-data-from-project-online-27f3838d-3dbe-4b98-80dc-df55f851154d). Genauere Informationen über die Dateien, die exportiert werden, finden Sie unter [Project Online-Export-JSON-Objektdefinitionen](https://support.office.com/article/project-online-export-json-object-definitions-ce5faeae-9af4-4696-b847-a1f4f20327c7).

### <a name="publisher"></a>Publisher

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Microsoft Publisher verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

#### <a name="discover"></a>Ermitteln

Mit der In-App-Suchfunktion können Sie Text in einer Publisher-Datei auf die gleiche Weise finden wie in den meisten Office-Anwendungen. Siehe [Suchen und Ersetzen von Text](https://support.office.com/article/find-and-replace-text-bfe54275-b7c7-4d0f-904d-a2f38d322268).

#### <a name="access"></a>Access

Nachdem Sie Daten gefunden haben, können Sie einen Screenshot davon machen oder ihn kopieren und in eine Word- oder Textdatei einfügen und ihn der betroffenen Person bereitstellen. Sie können auch eine Publikation als Word-, PDF- oder XPS-Datei speichern. Siehe:

  - [Speichern einer Publikation als Word-Dokument](https://support.microsoft.com/office/save-a-publication-as-a-word-document-b5eaaae5-6f1b-48c1-bebc-44460376b693)
  - [Speichern einer Publikation als PDF- oder XPS-Datei oder Konvertieren in das PDF- oder XPS-Format mit Publisher](https://support.microsoft.com/office/save-as-or-convert-a-publication-to-pdf-or-xps-using-publisher-657332d0-d2c2-464a-9870-e9b3d22e6469)

#### <a name="export"></a>Exportieren

Sie können einer betroffenen Person die tatsächliche Publisher-Datei bereitstellen oder wie bereits erläutert, eine Publikation als Word-, PDF- oder XPS-Datei speichern. Siehe:

  - [Speichern einer Publikation als Word-Dokument](https://support.microsoft.com/office/save-a-publication-as-a-word-document-b5eaaae5-6f1b-48c1-bebc-44460376b693)
  - [Speichern einer Publikation als PDF- oder XPS-Datei oder Konvertieren in das PDF- oder XPS-Format mit Publisher](https://support.microsoft.com/office/save-as-or-convert-a-publication-to-pdf-or-xps-using-publisher-657332d0-d2c2-464a-9870-e9b3d22e6469)

#### <a name="delete"></a>Löschen

Sie können Inhalte aus einer Publikation löschen, ganze Seiten löschen oder eine ganze Publisher-Datei löschen. Siehe [Hinzufügen oder Löschen von Seiten](https://support.office.com/article/add-or-delete-pages-daf71e39-86e0-4bbc-a186-d5ec70450b08).

### <a name="stream"></a>Stream

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Microsoft Stream verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

#### <a name="discover"></a>Ermittlung

Um Inhalte zu finden, die in Stream generiert oder hochgeladen wurden und die möglicherweise für einen Antrag einer betroffenen Person relevant sind, kann ein Stream-Administrator einen Benutzerbericht ausführen, um festzustellen, welche Videos, Videobeschreibungen, Gruppen, Kanäle oder Kommentare ein Stream-Benutzer hochgeladen, erstellt oder gepostet hat. Anweisungen zum Erstellen eines Berichts finden Sie unter [Verwalten von Benutzerdaten in Microsoft Stream](/stream/managing-user-data). Die Berichtsausgabe erfolgt im HTML-Format und enthält Hyperlinks, mit denen Sie zu potenziell interessanten Videos navigieren können. Wenn Sie ein Video mit benutzerdefinierten Berechtigungen anzeigen möchten und nicht zu den ursprünglichen Benutzern gehören, für die das Video bestimmt war, können Sie es im Administratormodus anzeigen. Siehe [Administratorfunktionen in Microsoft Stream](/stream/manage-content-permissions).  

#### <a name="access"></a>Access

Je nach Art des Antrags einer betroffenen Person kann eine Kopie des oben beschriebenen Berichts verwendet werden, um dem Antrag der betroffenen Person nachzukommen. Der Benutzerbericht enthält den Namen und die eindeutige ID des Stream-Benutzers, eine Liste der vom Benutzer hochgeladenen Videos, eine Liste der Videos, auf die der Benutzer Zugriff hat, eine Liste der vom Benutzer erstellten Kanäle, eine Liste aller Gruppen, in denen der Benutzer Mitglied ist, und eine Liste aller Kommentare, die der Benutzer zu Videos hinterlassen hat. Der Bericht zeigt außerdem an, ob der Benutzer jedes im Benutzerbericht aufgeführte Video angesehen hat. Wenn Sie der betroffenen Person Zugriff auf ein Video gewähren möchten, um einem Antrag einer betroffenen Person nachzukommen, können Sie das Video freigeben.

#### <a name="export"></a>Exportieren

Siehe Abschnitt Zugriff für Stream. 

#### <a name="delete"></a>Löschen

Um Videos oder andere Stream-Inhalte zu löschen oder zu bearbeiten, kann ein Stream-Administrator die Ansicht im Administratormodus auswählen, um die erforderliche Funktion auszuführen. Siehe [Administratormöglichkeiten in Microsoft Stream](/stream/manage-content-permissions). Wenn ein Benutzer die Organisation verlassen hat und möchte, dass sein Name nicht mehr neben den hochgeladenen Videos angezeigt wird, können Sie seinen Namen entfernen oder durch einen anderen ersetzen. Siehe [Verwaltung gelöschter Benutzer in Microsoft Stream](/stream/managing-deleted-users).

### <a name="sway"></a>Sway

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Microsoft Sway verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

#### <a name="discover"></a>Ermittlung

Mithilfe von Sway erstellte Inhalte (unter [www.sway.com](https://sway.office.com/)) können nur vom Besitzer und denjenigen Benutzern angezeigt werden, denen der Autor die Berechtigung zum Anzeigen gewährt hat. Weitere Informationen finden Sie unter [Datenschutzeinstellungen in Sway](https://support.microsoft.com/office/privacy-settings-in-sway-394b551c-be6f-4bd7-a70a-f318d72bf217). Um festzustellen, ob in Sway personenbezogene Daten vorhanden sind, die für Anträge betroffener Personen relevant sind, können Sie die betroffene Person und die Organisationsbenutzer, die wahrscheinlich Inhalte zu der betroffenen Person generiert haben, bitten, in Sway nach diesen Daten zu suchen und die Sways mitzuteilen, in denen wahrscheinlich personenbezogene Daten enthalten sind, die für den Antrag einer betroffenen Person relevant sind. Informationen zum Teilen von Sways finden Sie unter "Teilen eines Sway aus Ihrem Organisationskonto" im Artikel [Teilen Ihres Sways](https://support.microsoft.com/office/share-your-sway-1cf853b8-ef7e-46b0-b704-003e58d28998).

#### <a name="access"></a>Access

Wenn Sie personenbezogene Daten in einem Sway gefunden haben, die Sie für die betroffene Person freigeben möchten, können Sie der betroffenen Person auf verschiedene Arten Zugriff auf die Daten gewähren. Sie können der betroffenen Person eine Kopie der Onlineversion von Sway (wie oben beschrieben) bereitstellen. Sie können Screenshots des relevanten Teils von Sway erstellen, den Sie freigeben möchten. Sie können auch das Sway in Word drucken oder herunterladen und es in eine PDF-Datei konvertieren. Informationen zum Herunterladen eines Sways finden Sie weiter unten im Abschnitt „Exportieren“.

#### <a name="delete"></a>Löschen

Informationen zum Löschen eines Sways finden Sie im Abschnitt "Wie kann ich Sway löschen?" in den [Datenschutzeinstellungen in Sway](https://support.microsoft.com/office/privacy-settings-in-sway-394b551c-be6f-4bd7-a70a-f318d72bf217).

#### <a name="export"></a>Exportieren

Öffnen Sie zum Exportieren von Sway das Sway, das Sie herunterladen möchten, wählen Sie die drei Punkte (...) in der oberen rechten Ecke **Exportieren**, und wählen Sie dann entweder **Word** oder **PDF**.

### <a name="whiteboard"></a>Whiteboard

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Microsoft Whiteboard verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

- [Whiteboard 2016 auf Surface Hub](#whiteboard-2016-on-surface-hub)
- [Whiteboard auf allen anderen Plattformen](#whiteboard-for-pc-surface-hub-and-other-platforms)

#### <a name="whiteboard-2016-on-surface-hub"></a>Whiteboard 2016 auf Surface Hub

Dieser Abschnitt beschreibt die Reaktion auf Anträge betroffener Personen bezüglich Daten, die mit der integrierten Whiteboard 2016-App auf Surface Hub erstellt wurden.

##### <a name="discover"></a>Ermittlung

Whiteboard-Dateien (WBX-Dateien) werden im OneDrive for Business-Konto des Benutzers gespeichert. Sie können die betroffene Person oder andere Benutzer fragen, ob die von ihnen erstellten Whiteboards personenbezogene Daten enthalten können, die für einen Antrag einer betroffenen Person relevant sind. Diese können ein Whiteboard mit Ihnen teilen, oder Sie können eine Kopie davon bekommen, um sie der betroffenen Person zu geben.

So greifen Sie auf Whiteboards zu und übertragen diese: 

1. Ermöglichen Sie sich selbst Zugriff auf das OneDrive for Business-Konto des Benutzers. Siehe Abschnitt "Erhalten von Zugriff auf OneDrive for Business-Dokumente eines ehemaligen Mitarbeiters" in [Erhalten von Zugriff auf die Daten eines ehemaligen Benutzers und Sichern dieser Daten](/microsoft-365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data).
2. Gehen Sie in den Ordner Whiteboard-App-Daten im OneDrive for Business-Konto des Benutzers, und kopieren Sie die WBX-Dateien der Whiteboards, die Sie übertragen möchten.
3. Gewähren Sie sich selbst Zugriff auf das OneDrive for Business-Konto der betroffenen Person, und wechseln Sie dann zum Ordner Whiteboard-App-Daten.
4. Fügen Sie die .wbx-Dateien ein, die Sie im vorherigen Schritt kopiert haben.

##### <a name="access"></a>Access

Wenn Sie personenbezogene Daten in einem Whiteboard finden, die für einen Antrag einer betroffenen Person auf Zugriff relevant sind, können Sie der betroffenen Person auf verschiedene Weise Zugriff auf ein Whiteboard gewähren:

- Machen Sie Screenshots der relevanten Bereiche eines Whiteboards.
- Laden Sie eine Kopie der WBX-Datei auf das OneDrive for Business-Konto der betroffenen Person hoch. Im vorherigen Abschnitt finden Sie Schritte zum Zugriff auf und zur Übertragung von WBX-Dateien.
- Exportieren Sie eine Kopie eines Whiteboards als .png-Datei.

##### <a name="export"></a>Exportieren

Wenn Sie eine Kopie eines Whiteboards erhalten haben, können Sie sie exportieren. 

1. Starten Sie das Whiteboard auf dem Surface Hub.
2. Tippen Sie auf die Schaltfläche „Freigeben“, und wählen Sie dann „Eine Kopie exportieren“ aus. Sie können ein Whiteboard in eine OneNote-Datei (.one) oder in eine Bilddatei (.png) exportieren.

##### <a name="delete"></a>Löschen

Sie können sich selbst Zugang zum OneDrive for Business-Konto des Benutzers ermöglichen und dann die Whiteboards löschen.

1. Ermöglichen Sie sich selbst Zugriff auf das OneDrive for Business-Konto der betroffenen Person. Siehe Abschnitt "Erhalten von Zugriff auf OneDrive for Business-Dokumente eines ehemaligen Mitarbeiters" in [Erhalten von Zugriff auf die Daten eines ehemaligen Benutzers und Sichern dieser Daten](/microsoft-365/admin/add-users/get-access-to-and-back-up-a-former-user-s-data).
2. Wechseln Sie zu dem Ordner Whiteboard-App-Daten, und löschen Sie den Inhalt dieses Ordners.

#### <a name="whiteboard-for-pc-surface-hub-and-other-platforms"></a>Whiteboard für PC, Surface Hub und andere Plattformen

Wenn ein Administrator einen Antrag einer betroffenen Person bezüglich Daten in der neuen Whiteboard-App erhält, kann er Whiteboard PowerShell verwenden, um sich selbst (oder andere Benutzer) als Besitzer der Whiteboards eines Benutzers hinzuzufügen. Dies ermöglicht es einem Administrator, Aktionen wie den Zugriff auf, den Export und das Löschen von Whiteboards durchzuführen. Verwenden Sie entweder das Cmdlet **Set-WhiteboardOwner**, um sich selbst oder einen anderen Benutzer als Besitzer eines Whiteboards hinzuzufügen, oder verwenden Sie das Cmdlet **Invoke-TransferAllWhiteboards**, um den Besitz aller Whiteboards für einen bestimmten Benutzer auf einen neuen Besitzer zu übertragen. Informationen zur Verwendung dieser Cmdlets und zur Installation des Whiteboard PowerShell-Moduls finden Sie in der Microsoft Whiteboard-Cmdlet-Referenz. Nachdem Sie oder eine andere Person als Besitzer eines Whiteboards hinzugefügt haben, rufen Sie die [Microsoft Whiteboard-Cmdlet-Referenz](/powershell/module/whiteboard/) auf.

Nachdem Sie oder eine andere Person als Besitzer eines Whiteboards hinzugefügt wurde, finden Sie im [Whiteboard-Support-Artikel](https://go.microsoft.com/fwlink/?linkid=872780) detaillierte Anleitungen für den Zugriff auf, das Exportieren und Löschen von Whiteboards.

### <a name="yammer"></a>Yammer

In den folgenden Abschnitten wird erläutert, wie die In-App-Funktion in Microsoft Yammer verwendet werden kann, um personenbezogene Daten zu suchen, auf sie zuzugreifen, sie zu exportieren und zu löschen.

#### <a name="discover"></a>Ermitteln

Im Yammer Admin Center kann ein bestätigter Yammer-Administrator (globaler Administrator oder ein bestätigter Administrator in Yammer) Daten für einen bestimmten Benutzer exportieren. Der Export enthält die vom Benutzer geposteten und bearbeiteten Nachrichten und Dateien sowie Informationen zu den Themen und Gruppen, die vom Benutzer erstellt wurden. Beim Ausführen eines benutzerspezifischen Datenexports erhält der Administrator auch eine Nachricht mit den Aktivitätsdaten des Benutzerkontos, die Sie dem Benutzer bei Bedarf bereitstellen können. Eine detaillierte Anleitung finden Sie unter [Yammer Enterprise: Datenschutz](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise).

Benutzerspezifische Exporte werden für ein einzelnes Netzwerk erstellt. Wenn der Benutzer also in einem externen Yammer-Netzwerk ist, muss der Administrator die Daten für dieses externe Netzwerk sowie für das Heimnetzwerk exportieren.

Um auf nicht im Datenexport enthaltene Daten zuzugreifen, können Sie Screenshots des Profils, der Einstellungen, Gruppenmitgliedschaften, mit einer Textmarke versehenen Nachrichten, Benutzer und Themen, denen gefolgt wird, des Benutzers erstellen. Benutzer oder Administratoren können diese Informationen sammeln. Weitere Informationen finden Sie unter [Yammer Enterprise: Datenschutz](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise).

#### <a name="access"></a>Zugriff

Sie können Daten in den exportierten Dateien, einschließlich vollständiger Text der Nachrichten sowie Inhalte der Dateien, anzeigen. Sie können auch die Links in den exportierten Dateien auswählen, um direkt zu den geposteten Nachrichten und Dateien in Yammer, zu von dem Benutzer erstellten Gruppen und Themen, den Nachrichten, die dem Benutzer gefallen haben, Nachrichten, in denen der Benutzer erwähnt wurde, Umfragen, an denen der Benutzer teilgenommen hat, und zu den vom Benutzer hinzugefügten Links zu navigieren.

Im Datenexport pro Benutzer ist Folgendes nicht enthalten:

- Das Profil des Benutzers:
    - Wenn der Benutzer über ein Yammer-Konto verfügt, hat der Benutzer die vollständige Kontrolle über sein Profil. Informationen zum Anzeigen und Ändern des Profils finden Sie unter [Ändern des Profils und den Einstellungen in Yammer](https://support.office.com/article/change-my-yammer-profile-and-settings-a3aeca0e-de34-4897-9b59-de6516542851).
    
    - Wenn der Benutzer ein Office 365-Konto hat, wird das Yammer-Benutzerprofil automatisch von Office 365 abgerufen, darunter die Profilinformationen von Azure Active Directory (AAD). Yammer-Benutzer können ihre Profile in Yammer vorübergehend ändern, diese Änderungen werden jedoch überschrieben, wenn eine Änderung in AAD vorgenommen wird, sodass Verzeichnisdaten in AAD angezeigt und geprüft werden müssen. Weitere Informationen finden Sie unter [Verwalten von Yammer-Benutzern über ihren gesamten Lebenszyklus in Office 365](/yammer/manage-yammer-users/manage-users-across-their-lifecycle) und [Hinzufügen oder Ändern von Profilinformationen für einen Benutzer in Azure Active Directory](/azure/active-directory/active-directory-users-profile-azure-portal).

-   Die Einstellungen des Benutzers:

- Der Benutzer kann seine eigenen Einstellungen anzeigen und ändern. Informationen zum Anzeigen und Ändern von Benutzereinstellungen finden Sie unter [Ändern des Profils und der Einstellungen in Yammer](https://support.office.com/article/change-my-yammer-profile-and-settings-a3aeca0e-de34-4897-9b59-de6516542851). Ein Administrator kann diese Informationen anzeigen und Screenshots erstellen, sie aber nicht ändern. Wechseln Sie zu Yammer-Einstellungen \> **Personen**, und wählen Sie dann den Namen des Benutzers aus.<br/>
    - Die Gruppenmitgliedschaft des Benutzers, mit Lesezeichen versehene Nachrichten, Benutzer und Themen, denen der Benutzer folgt.
    
    - Der Benutzer kann diese Informationen anzeigen. Informationen zur Vorgehensweise finden Sie unter [Tips for staying organized in Yammer](https://support.office.com/article/tips-for-staying-organized-in-yammer-40ae9666-75c0-4254-a84c-d87a9542f380) (Tipps zum strukturierten Umgang mit Yammer). Ein Administrator kann diese Informationen anzeigen und Screenshots erstellen, sie aber nicht ändern. Wechseln Sie zu Yammer-Einstellungen \> **Personen**, und wählen Sie dann den Namen des Benutzers aus.

#### <a name="export"></a>Exportieren

Anweisungen zum Exportieren von Daten finden Sie unter [Verwalten von DSGVO-Datensubjektanforderungen in Yammer Enterprise](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise). Sie müssen einen Export pro Benutzer für jedes Yammer-Netzwerk ausführen, bei dem der Benutzer Mitglied ist.

Yammer verfügt über Einstellungen für die Aufbewahrung von Daten, mit denen Daten entweder vorläufig oder endgültig gelöscht werden, wenn ein Benutzer eine Nachricht oder eine Datei löscht. Wenn diese Einstellung auf vorläufiges Löschen festgelegt ist, sind die Daten, die ein Benutzer gelöscht hat, in dem Export enthalten. Wenn diese Einstellung auf endgültiges Löschen Einstellung festgelegt ist, werden die gelöschten Daten nicht mehr in Yammer gespeichert und sind daher auch nicht im Export enthalten.

#### <a name="delete"></a>Löschen

Yammer ermöglicht bestätigten Administratoren das Ausführen von DSGVO-kompatiblen Löschvorgängen über das Yammer Admin Center, wenn sie einen Antrag einer betroffenen Person erhalten. Diese Option heißt „Benutzer löschen“ und sperrt den Benutzer für 14 Tage und entfernt dann alle personenbezogenen Daten des Benutzers, mit Ausnahme von Dateien und Nachrichten. Wenn der Benutzer ein Gastbenutzer ist, muss dies für jedes externe Netzwerk erfolgen, bei denen der Gast Mitglied ist.

> [!NOTE]
> Wenn ein Administrator die Dateien und Nachrichten eines Benutzers innerhalb von 14 Tagen entfernen möchte, muss er einen Export auf Benutzerebene ausführen, um die Dateien und Nachrichten zu bestimmen, und anschließend entscheiden, welche zu löschen sind, entweder mithilfe der Löschfunktion des Produkts oder mithilfe eines PowerShell-Skripts. Nach Ablauf von 14 Tagen kann der Administrator den Benutzer nicht mehr den Dateien oder Nachrichten zuordnen.

Wenn ein Benutzer mit der Option "Benutzer löschen" gelöscht wurde, wird eine Benachrichtigung an den Yammer-Posteingang aller Netzwerkadministratoren und bestätigter Administratoren gesendet. Mit der Option "Benutzer löschen" wird das Yammer-Profil des Benutzers gelöscht, jedoch nicht das Office 365- oder Azure Active Directory-Profil.

Ausführliche Schritte zum Entfernen eines Benutzers finden Sie unter [Verwalten von Anträgen betroffener Personen nach der DSGVO in Yammer Enterprise](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise).

## <a name="responding-to-dsr-rectification-requests"></a>Reagieren auf Anträge betroffener Personen auf Berichtigung von Daten

Wenn eine betroffene Person Sie gebeten hat, die personenbezogenen Daten, die sich in den in Office 365 gespeicherten Daten Ihrer Organisation befinden, zu berichtigen, müssen Sie und Ihre Organisation entscheiden, ob es angemessen ist, dem Antrag nachzukommen. Wenn Sie sich dafür entscheiden, dem Antrag nachzukommen, kann die Berichtigung der Daten auch Maßnahmen wie das Bearbeiten, Berichtigen oder Entfernen personenbezogener Daten aus einem Dokument oder einem anderen Typ oder Element umfassen. Am effizientesten ist es, den Daten-/Dokumentbesitzer zu bitten, die entsprechende Office 365-Anwendung zu verwenden, um die gewünschte Änderung vorzunehmen. Alternativ kann ein IT-Administrator in Ihrer Organisation die Änderung vornehmen. Hierfür muss der der IT-Administrator (oder eine andere Personen in Ihrer Organisation mit den entsprechenden Berechtigungen, z. B. ein SharePoint Online-Websitesammlungsadministrator) wahrscheinlich sich selbst oder einer anderen Person, die an dem Antrag einer betroffenen Person arbeitet, die erforderlichen Berechtigungen zuweisen, um Zugriff auf das Dokument oder den Speicherort des Inhalts zu erhalten, um die Änderung direkt im Dokument vorzunehmen.

### <a name="requesting-that-the-data-owner-to-make-the-approved-change"></a>Aufforderung an den Dateneigentümer, die genehmigte Änderung vorzunehmen

Der direkteste Weg, personenbezogene Daten zu berichtigen, besteht darin, den Dateninhaber zu bitten, die Änderung vorzunehmen. Nachdem Sie die Daten gefunden haben, die Gegenstand des Antrags einer betroffenen Person sind, können Sie dem Dateninhaber die folgenden Informationen bereitstellen, damit dieser die Änderung vornehmen kann.

- Der Speicherort und Dateiname (für Dokumente und andere Dateien) des zu ändernden Elements. Die Suche der betreffenden Daten ist Teil des [Suchvorgangs](#using-content-search-to-find-personal-data), der zuvor bereits erläutert wurde.
- Die genehmigte Änderung, die der Dateneigentümer vornehmen soll

Möglicherweise möchten Sie einen Bestätigungsprozess implementieren, bei dem Sie oder eine andere Person, die an dem Antrag einer betroffenen Person arbeitet, prüft, ob die gewünschte Änderung vorgenommen wurde.

### <a name="gaining-access-to-a-sharepoint-online-site-or-onedrive-for-business-account-to-make-changes"></a>Zugriff auf eine SharePoint Online-Website oder ein OneDrive for Business-Konto, um Änderungen vorzunehmen

Wenn es für den Dateneigentümer nicht möglich ist, den Antrag einer betroffenen Person auf Berichtigung umzusetzen, kann ein IT-Administrator oder SharePoint-Administrator in Ihrer Organisation auf den Speicherort des Inhalts zugreifen und die erforderlichen Änderungen vornehmen. Alternativ kann ein Administrator Ihnen oder einem anderen Datenschutzbeauftragten die notwendigen Berechtigungen gewähren.

#### <a name="sharepoint-online"></a>SharePoint Online

Informationen zum Erteilen von Administrator- oder Besitzerberechtigungen für eine SharePoint Online-Website, damit Sie oder eine andere Person auf dieses Dokument zugreifen und es bearbeiten kann, finden Sie unter

- [Verwalten der Administratoren für eine Websitesammlung](/sharepoint/manage-site-collection-administrators)

- [Bearbeiten und Verwalten von Berechtigungen für eine SharePoint-Liste oder -Bibliothek](https://support.office.com/article/Edit-and-manage-permissions-for-a-SharePoint-list-or-library-02d770f3-59eb-4910-a608-5f84cc297782)

#### <a name="onedrive-for-business"></a>OneDrive for Business

Ein globaler Administrator kann auf das OneDrive for Business-Konto eines Benutzers zugreifen.

1. Melden Sie sich mit den Anmeldeinformationen des globalen Administrators bei Office 365 an.
2. Wechseln Sie zum Admin Center.
3. Wechseln Sie zu **Aktive Benutzer**, und wählen Sie den Benutzer aus.
4. Erweitern Sie im Detailbereich **OneDrive for Business-Einstellungen**, und wählen Sie dann **Auf Dateien zugreifen**.
5. Wählen Sie die URL aus, um zum OneDrive for Business-Konto des Benutzers zu wechseln.

### <a name="gaining-access-to-an-exchange-online-mailbox-to-make-changes-to-data"></a>Zugriff auf ein Exchange Online-Postfach zum Ändern von Daten

Ein globaler Administrator kann sich selbst die erforderlichen Berechtigungen zum Öffnen und Bearbeiten (oder Löschen) von Elementen im Postfach eines anderen Benutzers gewähren, so als wäre er Besitzer des Postfachs. Ein globaler Administrator kann diese Berechtigungen auch einem anderen Benutzer erteilen. Der globale Administrator muss insbesondere die Berechtigung **Lesen und Verwalten** hinzufügen, welche Vollzugriff in Exchange Online bedeutet. Weitere Informationen finden Sie unter:

- [Erteilen von Postfachberechtigungen für einen anderen Benutzer in Office 365](/microsoft-365/admin/add-users/give-mailbox-permissions-to-another-user)
- [Zugreifen auf das Postfach einer anderen Person](https://support.office.com/article/Access-another-person-s-mailbox-A909AD30-E413-40B5-A487-0EA70B763081)

Wenn für das Benutzerpostfach eine Aufbewahrung für juristische Zwecke aktiviert ist oder wenn das Benutzerpostfach einer Aufbewahrungsrichtlinie zugewiesen wurde, werden alle Versionen des Postfachs beibehalten, bis die Aufbewahrungsdauer abläuft oder bis die Aufbewahrung für juristische Zwecke für das Postfach inaktiviert wird. Das heißt, wenn ein Postfachelement in Reaktion auf einen Antrag einer betroffenen Person auf Berichtigung geändert wird, wird eine Kopie des ursprünglichen Elements (vor der Änderung) beibehalten und in einem versteckten Ordner im Ordner „Wiederherstellbare Elemente“ im Postfach des Benutzers gespeichert.

### <a name="making-changes-to-content-in-onedrive-for-business-and-sharepoint-online"></a>Änderungen an Inhalten in OneDrive for Business und SharePoint Online

Administratoren oder Datenbesitzer können Änderungen an Dokumente, Listen und Seiten in SharePoint Online vornehmen. Beachten Sie die folgenden Punkte, wenn Sie Änderungen an SharePoint-Inhalten vornehmen:

- Beim Aktualisieren eines Dokuments wird eine neue Version des Dokuments gespeichert, die die Überarbeitung enthält. Ältere Versionen des Dokuments werden nicht aktualisiert. Dies bedeutet, dass die Daten, die für den Antrag einer betroffenen Person auf Berichtigung relevant sind, in älteren Versionen des Dokuments enthalten sein können. Ältere Versionen eines Dokuments können gelöscht und dann endgültig aus Office 365 entfernt werden. Informationen dazu finden Sie im Abschnitt [Löschen von Dokumenten in SharePoint Online und OneDrive for Business](#deleting-documents-in-sharepoint-online-and-onedrive-for-business) in dieser Anleitung.
- Um eine SharePoint-Datei so zu bearbeiten, dass alle Spuren der betroffenen Person daraus entfernt werden, einschließlich aller Versionen der Datei und aller aufgezeichneten Aktivitäten der betroffenen Person, müssen Sie die folgenden Schritte ausführen:

    1. Laden Sie eine Kopie der Datei auf Ihrem lokalen Computer herunter.
    2. Löschen Sie die Datei endgültig aus SharePoint Online, indem Sie die Datei löschen und sie dann aus dem Standard- und dem endgültigen Papierkorb löschen. Informationen dazu finden Sie im Abschnitt [Löschen von Dokumenten in SharePoint Online und OneDrive for Business](#deleting-documents-in-sharepoint-online-and-onedrive-for-business) in dieser Anleitung..
    3. Nehmen Sie die Änderungen an der Kopie des Dokuments auf Ihrem lokalen Computer vor.
    4. Laden Sie die überarbeitete Datei am ursprünglichen Speicherort in SharePoint Online hoch.

- Daten in SharePoint-Listen können bearbeitet werden. Informationen dazu finden Sie unter [Hinzufügen, Bearbeiten oder Löschen von Listenelementen](https://support.microsoft.com/office/add-edit-or-delete-list-items-a4b31f53-f044-470e-9823-4526594bacde).

IT-Administratoren können auch bestimmte persönlichen Eigenschaften korrigieren, die mit einem Dokument verknüpft sind:

Benutzerinformationen aus dem SharePoint-Benutzerprofil oder Office 365 sind häufig mit OneDrive for Business- und SharePoint Online-Dokumenten zur Darstellung dieser Person verknüpft. Zum Beispiel der Name des Benutzers in der Spalte „Erstellt von“ oder „Geändert von“ eines Dokuments oder Listenelements. Diese Benutzerinformationen können je nach Quelle auf verschiedene Arten korrigiert werden:

- Korrigieren Sie die Benutzereigenschaften im Windows Server Active Directory. Für Kunden, die Benutzereigenschaften wie Anzeigename, Vorname usw. aus einem lokalen AD synchronisieren, sollten diese Eigenschaften dort korrigiert werden. Zugeordnete Eigenschaften werden entsprechend an Office 365 und dann an OneDrive for Business und SharePoint Online übermittelt.
- Korrigieren Sie die Benutzereigenschaften im Admin Center. Hier vorgenommene Änderungen an den Kontoinformationen werden automatisch in OneDrive for Business und SharePoint Online übernommen. Informationen hierzu finden Sie unter [Hinzufügen oder Ändern von Profilinformationen für einen Benutzer in Azure Active Directory](https://go.microsoft.com/fwlink/?linkid=864809). Für Eigenschaften in Office 365 können keine Änderungen auf SharePoint-Seite vorgenommen werden.
- Korrigieren Sie die Benutzereigenschaften im SharePoint-Benutzerprofil des SharePoint Admin Centers. Auf der Registerkarte „Benutzerprofile“ des SharePoint Admin Centers können Administratoren **Benutzerprofile verwalten** auswählen und nach den Eigenschaften des Benutzers suchen. Anschließend können sie die Eigenschaften des Benutzers bearbeiten.
- Korrigieren Sie die Benutzereigenschaften in einer benutzerdefinierten Quelle. Benutzerdefinierte SharePoint-Profileigenschaften werden möglicherweise von einer benutzerdefinierten Quelle über Microsoft Identity Manager (MIM) oder mit einer anderen Methode synchronisiert.

Dies betrifft nicht alle Oberflächen, die ältere Informationen enthalten. Zum Beispiel Name des Benutzers als Text im Dokument.

### <a name="making-changes-to-content-in-power-bi"></a>Änderungen an Inhalten in Power BI

Power BI basiert auf den zugrundeliegenden Quelldaten, die in Dashboards und Berichten verwendet werden. Daher müssen nicht korrekte oder unvollständige Quelldaten dort korrigiert werden. Wenn Sie zum Beispiel einen Power BI-Bericht erstellen, der mit Dynamics 365 for Sales als Livedatenquelle verbunden ist, müssten Sie Korrekturen an den Daten in Dynamics 365 for Sales vornehmen.

Sobald die Änderungen an den Daten vorgenommen wurden, können Sie die Funktion [Geplante Datenaktualisierung](/power-bi/refresh-scheduled-refresh) verwenden, um das Dataset zu aktualisieren, das in Power BI gespeichert ist, damit die geprüften Daten in den abhängigen Power BI-Bestände angezeigt werden. Um die Anforderungen der DSGVO einzuhalten, sollten Sie Richtlinien eingeführt haben, um sicherzustellen, dass Sie die Daten in angemessenen Abständen aktualisieren.

### <a name="making-changes-to-content-in-yammer"></a>Änderungen an Inhalten in Yammer

Bei Nachrichten können Benutzer eine bestimmte Nachricht bearbeiten, um eventuelle Unstimmigkeiten zu korrigieren. Sie können eine Liste aller Nachrichten von einem bestätigten Yammer-Administrator anfordern und dann einen Link in der Datei auswählen, um die jeweilige Nachricht zu prüfen.

Bei Dateien können Benutzer eine bestimmte Datei bearbeiten, um eventuelle Unstimmigkeiten zu korrigieren. Sie können eine Liste aller geposteten Dateien von einem bestätigten Yammer-Administrator anfordern und dann auf die Dateien in Yammer zugreifen. Dateien, die in den Ordner „Dateien“ exportiert werden, können angezeigt werden, indem Sie anhand der Nummer nach der Datei suchen. Verwenden Sie z. B. für eine Datei mit dem Namen „12345678.ppx“ im Export das Suchfeld in Yammer, um nach „1235678.ppx“ zu suchen. Alternativ können Sie zu <strong>https://www.yammer.com/\<network\_name\>/\#/files/\<file\_number\></strong>; zum Beispiel <strong>https://www.yammer.com/contosomkt.onmicrosoft.com/\#/files/12345678</strong>.

Bei Daten, auf die der Benutzer über das Profil und die Einstellungen zugreifen kann, kann der Benutzer alle nötigen Änderungen vornehmen.

- Das Profil des Benutzers:

    - Wenn der Benutzer über ein Yammer-Konto verfügt, hat der Benutzer die vollständige Kontrolle über sein Profil. Informationen zum Anzeigen und Ändern des Profils finden Sie unter [Ändern des Profils und den Einstellungen in Yammer](https://support.office.com/article/change-my-yammer-profile-and-settings-a3aeca0e-de34-4897-9b59-de6516542851).
    - Wenn der Benutzer ein Office 365-Konto hat, wird das Yammer-Benutzerprofil automatisch von Office 365 abgerufen, welches die Profilinformationen von Azure Active Directory (AAD) erhält. Yammer-Benutzer können ihre Profile in Yammer vorübergehend ändern, diese Änderungen werden jedoch überschrieben, wenn eine Änderung in AAD vorgenommen wird. Somit ist AAD der beste Ort zum Anzeigen und Ändern von Verzeichnisdaten. Der Benutzer muss die Aktualisierung von AAD anfordern. Weitere Informationen finden Sie unter [Verwalten von Yammer-Benutzern über ihren gesamten Lebenszyklus in Office 365](/yammer/manage-yammer-users/manage-users-across-their-lifecycle) und [Hinzufügen oder Ändern von Profilinformationen für einen Benutzer in Azure Active Directory](/azure/active-directory/active-directory-users-profile-azure-portal).

- Die Einstellungen des Benutzers:

    - Der Benutzer kann eigene Einstellungen ändern. Informationen zum Anzeigen und Ändern von Benutzereinstellungen finden Sie unter [Ändern des Profils und der Einstellungen in Yammer](https://support.office.com/article/change-my-yammer-profile-and-settings-a3aeca0e-de34-4897-9b59-de6516542851).
    - Die Gruppenmitgliedschaft des Benutzers, mit Lesezeichen versehene Nachrichten, Benutzer und Themen, denen ein Benutzer folgt. Der Benutzer kann diese Informationen ändern. Informationen dazu finden Sie unter [Tipps für die Organisation in Yammer](https://support.office.com/article/tips-for-staying-organized-in-yammer-40ae9666-75c0-4254-a84c-d87a9542f380).

## <a name="responding-to-dsr-restriction-requests"></a>Reagieren auf Anträge betroffener Personen auf Einschränkung der Datenverarbeitung

Mit den folgenden Methoden können Sie die Verarbeitung von Daten in Office 365 einschränken:

- Entfernen Sie eine Office 365-Anwendungslizenz, um zu verhindern, dass Benutzer über eine Anwendung auf Daten zugreifen.
- Verhindern Sie, dass Benutzer auf das OneDrive for Business-Konto zugreifen können.
- Deaktivieren Sie die Verarbeitung von Daten für einen Office 365-Dienst.
- Entfernen Sie die Daten vorübergehend aus SharePoint Online und OneDrive for Business, und bewahren Sie sie lokal auf.
- Schränken Sie vorübergehend den Zugriff auf eine SharePoint Online-Website ein.
- Verhindern Sie, dass sich ein Benutzer bei Office 365 anmeldet.

Wenn Ihre Organisation später feststellt, dass eine Einschränkung nicht mehr gilt, können Sie diese aufheben, indem Sie die Schritte, die Sie ausgeführt haben, um sie einzurichten, jetzt in umgekehrter Reihenfolge ausführen, z. B. erneutes Zuweisen von Lizenzen, erneutes Aktivieren eines Diensts oder Zulassen der Anmeldung bei Office 365.

### <a name="removing-the-license-for-an-office-365-application"></a>Entfernen der Lizenz für eine Office 365-Anwendung

Wie zuvor erläutert, werden Lizenzen für alle Office 365-Anwendungen, die in dem Microsoft 365 Business-Abonnement Ihrer Organisation enthalten sind, standardmäßig allen Benutzern zugewiesen. Wenn Sie den Zugriff auf Daten einschränken müssen, die Gegenstand eines Antrags einer betroffenen Person sind, kann ein IT-Administrator über das Office 365-Administratorportal eine Benutzerlizenz für eine Anwendung vorübergehend deaktivieren. Wenn ein Benutzer dann versucht, diese Anwendung zu verwenden, erhält er die Benachrichtigung „Nicht lizenziertes Produkt“ oder eine Meldung, die besagt, dass er keinen Zugriff mehr hat. Weitere Informationen dazu finden Sie unter [Entfernen von Lizenzen für Benutzer in Office 365 Business](/microsoft-365/admin/add-users/delete-a-user).

**Hinweise:**

- Um einen Benutzer daran zu hindern, auf Yammer zuzugreifen, müssen Sie zunächst die [Office 365-Identifizierung für Yammer-Benutzer](/yammer/configure-your-yammer-network/enforce-office-365-identity) erzwingen und dann die Yammer-Lizenz des Benutzers entfernen.

- Für Szenarien, die die Vorteile von Power BI Embedded nutzen, können Sie den Zugriff auf die Anwendung des unabhängigen Softwareanbieters (ISV), in die der Inhalt eingebettet ist, einschränken.

### <a name="preventing-users-from-accessing-their-onedrive-for-business-account"></a>Verhindern, dass Benutzer auf das OneDrive for Business-Konto zugreifen können

Das Entfernen der SharePoint-Online-Lizenz eines Benutzers hindert ihn nicht daran, auf sein OneDrive for Business-Konto zuzugreifen, wenn es bereits existiert. Sie müssen auch die Berechtigungen des Benutzers für sein OneDrive for Business-Konto entfernen. Sie können dies tun, indem Sie den Benutzer als Besitzer der Websitesammlung seines OneDrive for Business-Kontos entfernen. Insbesondere müssen Sie den Benutzer aus den Gruppen „Primärer Websitesammlungsadministrator“ und „Websitesammlungsadministrator“ in dessen Benutzerprofil entfernen. Siehe Abschnitt "Hinzufügen und Entfernen von Administratoren in einem OneDrive for Business-Konto" in [Verwalten von Benutzerprofilen im SharePoint Admin Center](/sharepoint/manage-user-profiles).

### <a name="turning-off-an-office-365-service"></a>Deaktivieren eines Office 365-Dienstes

Eine andere Möglichkeit, einem Antrag einer betroffenen Person auf Einschränkung der Verarbeitung von Daten nachzukommen, ist das Deaktivieren eines Office 365-Dienstes. Dies wirkst sich auf alle Benutzer in Ihrer gesamten Organisation aus und hindert jeden daran, den Dienst zu verwenden oder auf darin befindliche Daten zuzugreifen.

Der zweckmäßigste Weg, einen Dienst zu deaktivieren, besteht darin, Office 365 PowerShell zu verwenden und die entsprechende Benutzerlizenz von allen Benutzern im Unternehmen zu entfernen. Dies wird alle Personen vom Zugriff auf Daten in diesem Dienst abhalten. Ausführliche Anweisungen finden Sie unter [Deaktivieren des Zugriffs auf Dienste mit Office 365 PowerShell](/microsoft-365/enterprise/disable-access-to-services-with-microsoft-365-powershell), und befolgen Sie die Verfahren zum Deaktivieren von Office 365-Diensten für Benutzer aus einem einzigen Lizenzplan.

> [!NOTE]
> Für Yammer müssen Sie zusätzlich zum Entfernen der Yammer-Lizenz aus Benutzerkonten auch die Möglichkeit der Benutzer deaktivieren, sich bei Yammer mit Yammer-Anmeldeinformationen anzumelden (indem Sie die Verwendung ihrer Office 365-Anmeldeinformationen beim Anmelden erzwingen). Detaillierte Anweisungen dazu finden Sie unter [Deaktivieren des Yammer-Zugriffs für Microsoft 365-Benutzer](https://support.office.com/article/Turn-off-Yammer-access-for-Office-365-users-1f79bfad-f713-4143-aa5d-5584985ce53a).

### <a name="temporarily-removing-data-from-sharepoint-online-or-onedrive-for-business-sites"></a>Vorübergehende Entfernung von Daten aus SharePoint Online oder OneDrive for Business-Websites

Eine weitere Möglichkeit zum Einschränken der Verarbeitung personenbezogener Daten in Reaktion auf einen Antrag einer betroffenen Person besteht darin, diese vorübergehend aus Office 365 zu entfernen. Wenn Ihre Organisation feststellt, dass die Einschränkung nicht mehr gilt, können Sie die Daten zurück in Office 365 importieren.

Da die meisten Office-Dokumente auf einer SharePoint Online- oder OneDrive for Business-Website gespeichert sind, wird im Folgenden eine allgemeine Vorgehensweise für das Entfernen von Dokumenten von Websites und deren erneuten Import beschrieben.

1. Rufen Sie eine Kopie des Dokuments ab, das Gegenstand des Antrags auf Einschränkung ist. Möglicherweise müssen Sie entweder den Zugriff auf die Website beantragen oder einen globalen Administrator bzw. einen Websitesammlungsadministrator bitten, Ihnen eine Kopie des Dokuments zur Verfügung zu stellen.
2. Speichern Sie das Dokument an einem lokalen Speicherort (z. B. einem Dateiserver oder einer Dateifreigabe) oder einem anderen Ort, außer an Ihrem Office 365-Mandanten in der Microsoft-Cloud.
3. Dauerhafte Löschung des Originaldokuments aus Office 365. Dies ist ein 3-stufiger Prozess:

   1.  Die Originalkopie des Dokuments löschen. Wenn Sie ein Dokument aus einer Website löschen, wird es an den Website-Papierkorb (auch *Papierkorb der ersten Stufe* genannt) gesendet.

   1.  Gehen Sie zum Papierkorb der Website und löschen Sie diese Kopie des Dokuments. Wenn Sie ein Dokument aus dem Website-Papierkorb löschen, wird es an den Papierkorb der Website-Sammlung (auch *Papierkorb der zweiten Stufe* genannt) gesendet. Siehe [Löschen einer Datei, eines Ordners oder eines Links aus einer SharePoint-Dokumentbibliothek](https://support.microsoft.com/office/delete-a-file-folder-or-link-from-a-sharepoint-document-library-71f3c90a-0d24-4d80-8b66-f88234b79a52).

   1.  Rufen Sie den Papierkorb der Websitesammlung auf und löschen Sie diese Kopie des Dokuments, wodurch diese dauerhaft aus Office 365 entfernt wird. Siehe [Löschen von Elementen aus dem Papierkorb der Websitesammlung](https://support.microsoft.com/office/delete-items-from-the-site-collection-recycle-bin-dd5c00c2-aef6-4458-9d04-80b185077653).

4. Wenn die Einschränkung nicht mehr gültig ist, kann die Kopie des Dokuments, das lokal gespeichert wurde, wieder auf die Website in Office 365 hochgeladen werden.

> [!IMPORTANT]
> Der vorstehend beschriebene Vorgang funktioniert nicht, wenn sich das Dokument auf einer Website befindet, für die eine Aufbewahrung eingerichtet wurde (mithilfe einer der Funktionen für reguläre Aufbewahrung oder Aufbewahrung für juristische Zwecke in Office 365). Wenn ein Antrag einer betroffenen Person auf Einschränkung Vorrang vor einer Aufbewahrung hat, muss die Aufbewahrung für die Website inaktiviert werden, bevor ein Dokument endgültig gelöscht werden kann. Zudem wird der Dokumentenverlauf für gelöschte Dokumente dauerhaft entfernt.

### <a name="temporarily-restricting-access-to-sharepoint-online-sites"></a>Vorübergehende Einschränkung des Zugriffs auf SharePoint Online-Websites

Ein SharePoint Online-Administrator kann den Zugriff aller Benutzer auf eine SharePoint Online-Websitesammlung vorübergehend verhindern, indem er die Websitesammlung sperrt (durch den Befehl **Set-SPOSite -LockState** in SharePoint Online PowerShell). Dadurch wird verhindert, dass Benutzer auf die Websitesammlung und alle Inhalte oder Daten, die sich auf der Website befinden, zugreifen können. Wenn Sie dann feststellen, dass Benutzer auf die Website zugreifen können, kann der Administrator die Website entsperren. Weitere Informationen zum Ausführen dieses PowerShell-Cmdlets finden Sie unter [Set-SPOSite](/powershell/module/sharepoint-online/set-sposite).

### <a name="preventing-a-user-from-signing-in-to-office-365"></a>Verhindern, dass einen Benutzer sich bei Office 365 anmeldet

Ein IT-Administrator kann auch verhindern, dass sich ein Benutzer bei Office 365 anmeldet, was den Zugriff auf einen Office 365-Onlinedienst oder die Verarbeitung von in Office 365 gespeicherten Daten verhindern würde. Siehe [Blockieren des Zugriffs eines ehemaligen Mitarbeiters auf Office 365-Daten](/microsoft-365/admin/add-users/remove-former-employee).

## <a name="part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365"></a>Teil 2: Reaktion auf Anträge betroffener Personen bezüglich von Office 365 generierten Erkenntnissen

Die Microsoft-Suite der Office 365-Dienste umfassen Onlinedienste, die Benutzern und Organisationen, die sich für ihre Nutzung entschieden haben, Einblicke gewähren.

- Delve und MyAnalytics ermöglichen Einblicke für einzelne Benutzer.
- Workplace Analytics bietet Einblicke Organisationen.

Diese Dienste werden in den folgenden Abschnitten ausführlich behandelt.

### <a name="delve"></a>Delve

In Delve können Benutzer ihr Office 365-Profil verwalten und Personen und Dokumente entdecken, die für sie relevant sein könnten. Benutzer können nur Dokumente sehen, auf die sie Zugriff haben. Eine Reihe hilfreicher Artikel über Delve finden Sie unter [Office Delve](https://support.office.com/article/What-is-Office-Delve-1315665a-c6af-4409-a28d-49f8916878ca).

#### <a name="access-and-export"></a>Zugriff und Export

Administratoren können nicht auf die Delve-Daten eines Benutzers zugreifen oder diese exportieren. Dies bedeutet, dass die Benutzer selbst auf Delve-Daten zugreifen und diese exportieren müssen. Die meisten Datentypen können direkt aus Delve heraus aufgerufen und exportiert werden, aber einige Datentypen sind nur über andere Dienste verfügbar.

##### <a name="data-available-in-the-delve-user-interface"></a>In der Delve-Benutzeroberfläche verfügbare Daten

- **Profildaten:** Dies sind die Profilinformationen aus der globalen Adressliste Ihrer Organisation in der Azure Active Directory sowie optionale Informationen, die Benutzer über sich selbst hinzugefügt haben. Um auf Profildaten in Delve zuzugreifen oder sie zu exportieren, kann ein Benutzer auf **Ich** \> **Profil aktualisieren** klicken. Sie können entweder den Inhalt direkt von der Seite kopieren oder
- **Blog-Daten:** Dies sind Blogbeiträge, die von einem Benutzer veröffentlicht wurden. Um auf Blog-Daten zuzugreifen oder sie zu exportieren, kann ein Benutzer auf **Mich** \> **Alle Beiträge** klicken. Sie können entweder den Inhalt direkt von der Seite kopieren oder einen Screenshot machen.
- **Aktuelle Personendaten:** Dies sind die Personen in der Organisation, von denen Delve gefolgert hat, dass sie für den Benutzer zu einem bestimmten Zeitpunkt am relevantesten sind. Wenn ein Benutzer im Bereich "Klicken Sie auf eine Person, um zu sehen, woran sie gerade arbeitet" **Mich** \> **Alle ansehen** auswählt, zeigt Delve die relevantesten Personen für einen Benutzer zu einem bestimmten Zeitpunkt an.

##### <a name="data-available-through-an-export-link-in-delve"></a>Über einen Exportlink in Delve verfügbare Daten

- **Personenlistendaten:** Dies sind die Personen, die der Benutzer in Delve angesehen hat. Die Liste **Personen** wird im linken Bereich der Startseite angezeigt. Benutzer können die Liste der Personen, die sie zuletzt in Delve angesehen haben, exportieren.
- **Favoriten-Daten:** Dies sind Boards und Dokumente, die der Benutzer als seine Favoriten markiert hat. Die Seite **Favoriten** zeigt Boards und Dokumente, die der Benutzer zu seinen Favoriten hinzugefügt hat. Benutzer können eine Liste ihrer aktuellen Favoriten-Boards und Dokumente exportieren.
- **Funktionseinstellungsdaten:** Dies sind Delve-Konfigurationen oder -Aktionen, die sich aus der Verwendung von Delve durch einen Benutzer ergeben. Benutzer können eine vollständige Liste dieser Einstellungen exportieren.

Um auf die obigen Daten zuzugreifen oder sie zu exportieren, kann der Benutzer das Zahnradsymbol in der oberen rechten Ecke von Delve auswählen und dann **Funktionseinstellungen** > **Daten exportieren**. Informationen werden im JSON-Format exportiert.

##### <a name="data-thats-available-through-other-services"></a>Daten, die über andere Dienste zur Verfügung stehen

- **Daten von beliebten Dokumenten:** Hierbei handelt es sich um Dokumente und E-Mail-Anhänge, die für den Benutzer relevant sein könnten. Delve organisiert diese Dokumente und E-Mail-Nachrichten dynamisch auf der Grundlage der Aktivitäten des Benutzers und der Personen, mit denen er in Office 365 arbeitet. Wenn ein Benutzer Delve öffnet oder auf **Startseite** klickt, zeigt Delve die relevantesten Dokumente oder Anhänge für den Benutzer zu einem bestimmten Zeitpunkt an. Um auf die tatsächlichen Dokumente und Anhänge zuzugreifen oder sie zu exportieren, kann der Benutzer zu dem Office 365-Dienst wechseln, über den das Dokument oder der Anhang bereitgestellt wurde (z. B. Office.com, SharePoint Online, OneDrive for Business oder Exchange Online).
- **Daten der zuletzt verwendeten Dokumente und E-Mail-Anhänge:** Dies sind die Dokumente und E-Mail-Anhänge, die der Benutzer zuletzt geändert hat. Wenn ein Benutzer im Bereich "Zurück zu Ihren letzten Dokumenten und E-Mail-Anhängen" auf **Mich** \> **Alle ansehen** klickt, zeigt Delve die aktuellsten Dokumente und E-Mail-Anhänge an, die der Benutzer zu einem bestimmten Zeitpunkt geändert hat. Um auf die tatsächlichen Dokumente und Anhänge zuzugreifen oder sie zu exportieren, kann der Benutzer zu dem Office 365-Dienst wechseln, über den das Dokument oder der Anhang bereitgestellt wurde wie zum Beispiel Office.com, SharePoint Online, OneDrive for Business oder Exchange Online.
- **Daten von Dokumenten von Personen in Ihrer Nähe:** Hierbei handelt es sich um die Dokumente von denen Delve gefolgert hat, dass sie für den Benutzer zu einem bestimmten Zeitpunkt am relevantesten sind. Wenn ein Benutzer im Bereich "Dokumente von Personen in Ihrer Umgebung ermitteln" auf **Mich** \> **Alle ansehen** klickt, zeigt Delve die relevantesten Dokumente für einen Benutzer zu einem bestimmten Zeitpunkt an. Um auf die tatsächlichen Dokumente zuzugreifen oder sie zu exportieren, kann der Benutzer zu dem Office 365-Dienst wechseln, über den das Dokument oder der Anhang bereitgestellt wurde (zum Beispiel Office.com, SharePoint Online, OneDrive for Business oder Exchange Online).

#### <a name="rectify"></a>Berichtigung

Benutzer können die folgenden Informationen in Delve ändern:

- **Profilinformationen:** Ein Benutzer kann **Ich** \> **Profil aktualisieren** auswählen, um seine Informationen zu aktualisieren. Abhängig von den Einstellungen Ihrer Organisation in der globalen Adressliste können Benutzer möglicherweise nicht alle ihre Profilinformationen, wie z. B. ihren Namen oder ihre Position, ändern.
- **Featureeinstellungen:** Ein Benutzer kann  das Zahnradsymbol in der oberen rechten Ecke in Delve auswählen und dann **Featureeinstellungen** \>, um die gewünschten Einstellungen zu ändern.

#### <a name="restrict"></a>Einschränkung

Um die Verarbeitung in Delve für Ihre Organisation einzuschränken, können Sie Office Graph deaktivieren. Weitere Informationen finden Sie [hier](/sharepoint/delve-for-office-365-admins).

#### <a name="delete"></a>Löschen

Benutzer können die folgenden Informationen in Delve löschen:

- **Profilinformationen:** Um Profilinformationen zu löschen, kann ein Benutzer **Ich** \> **Profil aktualisieren** auswählen und Freiformtext löschen. Abhängig von den Einstellungen Ihrer Organisation in der globalen Adressliste können Benutzer möglicherweise nicht alle ihre Profilinformationen, wie z. B. ihren Namen oder ihre Position, löschen.
- **Dokumente und E-Mail-Anhänge:** Um ein Dokument oder eine Anlage zu löschen, müssen Benutzer zu dem Dienst gehen, in dem das Dokument oder die Anlage gespeichert ist (z. B. SharePoint Online, OneDrive for Business oder Exchange Online) und das Dokument dort löschen.

### <a name="myanalytics"></a>MyAnalytics

MyAnalytics stellt den Benutzern Statistiken zur Verfügung, die ihnen dabei helfen, zu sehen, wie sie ihre Zeit bei der Arbeit verbringen. Um Ihren Benutzern zu helfen, die Daten, die ihnen in ihrem persönlichen Dashboard angezeigt werden und wie diese Daten berechnet werden, besser zu verstehen, verweisen Sie Ihre Benutzer auf [MyAnalytics – Persönliches Dashboard](/workplace-analytics/myanalytics/use/dashboard-2).

#### <a name="access-and-export"></a>Zugriff und Export

Wenn Ihre Organisation MyAnalytics verwendet, generiert Microsoft Erkenntnisse für alle Benutzer. Alle MyAnalytics-Erkenntnisse werden aus den E-Mail- und Besprechungsheadern im Postfach des Benutzers abgeleitet. Benutzer können das [MyAnalytics-Dashboard](https://delve.office.com) aufrufen, während sie in ihrem Office 365-Konto angemeldet sind, um die Erkenntnisse darüber einzusehen, wie sie ihre Zeit bei der Arbeit verbringen. Sie können Screenshots von MyAnalytics-Erkenntnissen machen, wenn sie dauerhafte Kopien ihrer Informationen erhalten möchten.

#### <a name="rectify"></a>Berichtigung

Benutzer mit dem E-Mail- und Kalenderelemente werden alle Einblicke von MyAnalytics generiert abgeleitet. Aus diesem Grund erübrigen sich andere als die ursprüngliche E-Mail oder eines der Elemente zu beheben.

#### <a name="restrict"></a>Einschränkung

Um die Verarbeitung für einen bestimmten Benutzer einzuschränken, können Sie MyAnalytics für diesen Benutzer inaktivieren. Eine Anleitung dazu finden Sie unter [Benutzereinstellungen für MyAnalytics konfigurieren](/workplace-analytics/myanalytics/setup/configure-myanalytics).

#### <a name="delete"></a>Löschen

Alle Postfachinhalte, einschließlich der MyAnalytics-Daten, werden gelöscht, wenn ein Benutzerkonto aus dem Active Directory "endgültig gelöscht" wird. Weitere Informationen finden Sie im Abschnitt [Löschen eines Benutzers](#deleting-a-user) in diesem Leitfaden.

### <a name="workplace-analytics"></a>Workplace Analytics

Workplace Analytics ermöglicht es Unternehmen, Office 365-Daten mit ihren eigenen Geschäftsdaten zu ergänzen, um Einblicke in die Produktivität der Organisation, die Zusammenarbeit und das Engagement der Mitarbeiter zu gewinnen. [Dieser Artikel](/workplace-analytics/index-orig) erklärt die Kontrolle, die Ihre Organisation über die Daten hat, die Workplace Analytics verarbeitet, und wer Zugriff auf diese Daten hat.

Um Sie bei Anträgen betroffener Personen in Workplace Analytics zu unterstützen: 

1. Stellen Sie fest, ob Ihre Organisation Workplace Analytics verwendet. Weitere Informationen dazu finden Sie unter [Zuweisen von Lizenzen zu Benutzern](/microsoft-365/admin/manage/assign-licenses-to-users). Wenn Ihr Unternehmen nicht mit Workplace Analytics arbeitet, gibt es keine weiteren Aktionen.

2. Wenn Ihre Organisation Workplace Analytics einsetzt, sehen Sie nach, welchem Benutzer in Ihrer Organisation die Rolle des Workplace Analytics-Administrators zugewiesen ist. Außerdem sollten Sie feststellen, ob das Postfach der betroffenen Person für Workplace Analytics lizenziert ist. Bitten Sie bei Bedarf den Workplace Analytics-Administrator, Microsoft-Support zu kontaktieren, um die folgenden Anträge betroffener Personen zu bearbeiten: 

#### <a name="access-and-export"></a>Zugriff und Export

Von Ihnen erstellte Workplace Analytics-Erkenntnisberichte können personenbezogene Daten von Benutzern enthalten, die Ihre Organisation für Workplace Analytics lizenziert hat, abhängig von den Informationen, die Ihr Unternehmen zur Ergänzung der Office 365-Daten verwendet hat. Ihr Workplace Analytics-Administrator muss diese Berichte überprüfen, um festzustellen, ob sie die personenbezogene Daten eines Benutzers enthalten. Wenn ein Bericht die personenbezogene Daten eines Benutzers enthält, müssen Sie entscheiden, ob Sie dem Benutzer eine Kopie dieses Berichts zur Verfügung stellen möchten. Mit Workplace Analytics können Sie den Bericht exportieren. 

#### <a name="rectify"></a>Berichtigen

Wie oben erläutert, verwendet Workplace Analytics Office 365-Daten mit den von Ihnen zur Verfügung gestellten Organisationsdaten, um für Sie interessante Berichte zu erstellen. Die Office 365-Daten können nicht korrigiert werden – sie basieren auf den E-Mail- und Kalenderaktivitäten eines Benutzers. Die Organisationsdaten, die Sie in Workplace Analytics hochgeladen haben, um den Bericht zu generieren, können jedoch korrigiert werden. Dazu müssen Sie die Quelldaten korrigieren, hochladen und den Bericht erneut ausführen, um einen neuen Workplace Analytics-Bericht zu erstellen.

#### <a name="restrict"></a>Einschränkung

Um die Verarbeitung für einen bestimmten Benutzer einzuschränken, können Sie dessen Workplace Analytics-Lizenz entfernen.

#### <a name="delete"></a>Löschen

Wenn eine betroffene Person aus einem Workplace-Analytics-Bericht oder einem Satz von Berichten entfernt werden möchte, können Sie den Bericht löschen. Es liegt in Ihrer Verantwortung, Benutzer aus allen Organisationsdaten, die Sie zur Erstellung des Berichts verwendet haben, zu löschen und die Daten erneut hochzuladen. Alle Daten über den Benutzer werden entfernt, wenn ein Benutzerkonto aus dem Azure Active Directory "endgültig gelöscht" wird. 

Um die personenbezogenen Daten einer betroffenen Person zu entfernen, kann ein globaler Administrator die folgenden Schritte ausführen: 

1. Die Workspace Analytics-Lizenz der betroffenen Person entfernen.
2. Den Eintrag über die betroffene Person in Azure Active Directory (AAD) löschen. (Weitere Informationen finden Sie unter [Einen Benutzer entfernen](/azure/active-directory/fundamentals/add-users-azure-active-directory#delete-a-user).)
3. Den Support kontaktieren, damit dieser ein Ticket für einen Antrag einer betroffenen Person auf Löschung ihrer Benutzerdaten eröffnet. In diesem Ticket muss die betroffene Person anhand ihres Benutzerprinzipalnamens angegeben werden.
4. Eine Kopie der Personaldaten aus dem Personalsystem des Unternehmens exportieren (weitere Informationen finden Sie unter [Daten exportieren](/workplace-analytics/setup/prepare-organizational-data)), die Informationen über die betroffene Person aus dieser Personaldatendatei entfernen und dann die bearbeitete Personaldatendatei im Format .csv in Workplace Analytics hochladen (weitere Informationen finden Sie unter [Organisationsdaten hochladen](/workplace-analytics/setup/upload-organizational-data)).

## <a name="part-3-responding-to-dsrs-for-system-generated-logs"></a>Teil 3: Reaktion auf Anträge betroffener Personen für vom System generierte Protokolle

Microsoft bietet Ihnen außerdem die Möglichkeit, auf vom System erzeugte Protokolle zuzugreifen, sie zu exportieren und zu löschen, die nach der weit gefassten Definition der DSGVO als "personenbezogene Daten" gelten können. Beispiele für vom System generierte Protokolle, die unter der DSGVO als personenbezogen angesehen werden können:

- Daten zu Produkt- und Dienstnutzung, z. B. Aktivitätsprotokolle
- Suchanfragen und Abfragedaten von Benutzern
- Daten, die durch Produkte und Dienste als Produkt der Systemfunktionalität und Interaktion von Benutzern oder anderen Systemen erzeugt werden

Die Möglichkeit, Daten in vom System generierten Protokollen einzuschränken oder zu korrigieren, wird nicht unterstützt. Daten in vom System generierten Protokollen geben auf Fakten basierende Aktionen innerhalb der Microsoft-Cloud und Diagnosedaten wieder, und Änderungen an diesen Daten würden den historischen Datensatz von Aktionen kompromittieren und das Betrugs- und Sicherheitsrisiko erhöhen.

### <a name="accessing-and-exporting-system-generated-logs"></a>Zugreifen auf und Exportieren von vom System generierte(n) Protokolle(n)

Der Mandantenadministrator ist die einzige Person in Ihrem Unternehmen, die auf vom System generierte Protokolle in Verbindung mit der Verwendung von Office 365-Diensten und -Anwendungen eines bestimmten Benutzers zugreifen kann. Die Daten, die für einen Exportanforderung abgerufen werden, werden in einem maschinenlesbaren Format und in Dateien bereitgestellt, über die der Benutzer Rückschlüsse darauf ziehen kann, aus welchen Diensten die Daten stammen. Wie bereits oben erwähnt, enthalten die abgerufenen Daten keine Daten, welche die Sicherheit oder die Stabilität des Dienstes gefährden könnten.

So können Sie auf vom System generierte Protokolle zugreifen und sie exportieren:

1. Melden Sie sich beim Azure-Portal an, und wählen Sie **Alle Dienste** aus.
2. Geben Sie "Richtlinie" in den Filter ein, und wählen Sie dann **Richtlinie** aus.
3. Wählen Sie im Blatt **Richtlinie** die Option **Datenschutz** und dann die Option **Benutzeranforderungen verwalten** aus, und wählen Sie dann **Exportanforderung hinzufügen** aus.
4. Schließen Sie die **Anforderung zum Exportieren von Daten** ab:

    - **Benutzer**. Geben Sie die E-Mail-Adresse des Azure Active Directory-Benutzers ein, der den Export angefordert hat.
    - **Abonnement**. Wählen Sie das Konto aus, über das Sie die Ressourcennutzung berichten und Dienste in Rechnung stellen. Dies ist auch der Speicherort Ihres Azure-Speicherkontos.
    - **Speicherkonto**. Wählen Sie den Speicherort Ihres Azure Storage (Blob) aus. Weitere Informationen finden Sie im Artikel Einführung in Microsoft Azure Storage – Blob-Speicher.
    - **Container**. Erstellen Sie einen neuen Container (oder wählen Sie einen vorhandenen aus) als Speicherort für die exportieren vertraulichen Daten des Benutzers.

5. Wählen Sie **Erstellen** aus.

Die Exportanforderung wechselt in den Status **Ausstehend**. Sie können den Berichtstatus auf dem Blatt **Benutzerdatenschutz** > **Datenschutz – Übersicht** anzeigen.

> [!IMPORTANT]
> Da personenbezogene Daten aus mehreren Systemen stammen können, kann es bis zu einen Monat dauern, bis der Exportvorgang abgeschlossen ist.

### <a name="notify-about-exporting-or-deleting-issues"></a>Benachrichtigung über Probleme beim Exportieren oder Löschen

Wenn beim Exportieren oder Löschen von Daten aus dem Azure-Portal Probleme auftreten, wechseln Sie zum Azure-Portalblatt **Hilfe und Support**, und übermitteln Sie ein neues Ticket unter **Abonnementverwaltung** > **Datenschutz- und Complianceanforderungen für Abonnements** > **Blatt "Datenschutz" und DSGVO-Anforderungen**.

> [!NOTE]
> Wenn Sie eine Anforderung zum Exportieren von Daten aus dem Azure-Portal erstellen, werden die vom System generierten Daten für einige Anwendungen nicht exportiert. Um Daten zu diesen Anwendungen zu exportieren, lesen Sie [Zusätzliche Schritte zum Exportieren der vom System generierten Protokolldaten](/microsoft-365/compliance/gdpr-system-generated-log-data).

Nachfolgend eine Zusammenfassung zum Thema Zugriff auf und Exportieren von vom System generierte(n) Protokolle(n):

- **Wie lange dauert es, bis eine Exportanforderung über das Azure-Portal abgeschlossen ist?** Dies kann von mehreren Faktoren abhängen. Normalerweise sollte die Anforderung nach ein bis zwei Tagen abgeschlossen sein, es kann aber auch bis zu 30 Tage dauern.
- **Welches Format wird die Ausgabe haben?** Die Ausgabe erfolgt in strukturierten, maschinenlesbaren Dateien wie XML, CSV oder JSON.
- **Wer kann auf das Azure-Portal zugreifen, um Zugriffsanforderungen für vom System generierte Daten zu übermitteln?** Auf das Azure-Portal können globale Office 365-Administratoren zugreifen.
- **Welche Daten sind in den Exportergebnissen enthalten?** Die Ergebnisse enthalten von Microsoft gespeicherte, vom System generierte Protokolle. Die exportierten Daten umfassen mehrere Microsoft-Dienste, einschließlich Office 365, Azure und Dynamics. Die Ergebnisse enthalten keine Daten, die die Sicherheit oder Stabilität des Diensts beeinträchtigen könnten.
- **Wie werden Daten an den Benutzer ausgegeben?** Die Daten werden an den Azure-Speicherort Ihrer Organisation exportiert; es ist Sache der Administratoren in Ihrer Organisation, zu bestimmen, wie sie diese Daten den Benutzern anzeigen/bereitstellen.
- **Wie sehen die vom System generierten Protokolldaten aus?** Nachfolgend sehen Sie ein Beispiel für Daten im JSON-Format:

    ```JSON
    [{
    "DateTime": "2017-04-28T12:09:29-07:00",
    "AppName": "SharePoint",
    "Action": "OpenFile",
    "IP": "154.192.13.131",
    "DevicePlatform": "Windows 1.0.1607"
    }]
    ```

Produkt- und Servicenutzungsdaten für einige der am häufigsten genutzten Dienste von Microsoft wie Exchange Online, SharePoint Online, Skype for Business, Yammer und Office 365-Gruppen können auch über das Office 365-Auditprotokoll im Security & Compliance Center abgerufen werden. Weitere Informationen finden Sie unter [Verwenden des Office 365-Überwachungsprotokoll-Suchtools für Untersuchungen von Anforderungen betroffener Personen](#use-the-audit-log-search-tool-in-dsr-investigations) in Anhang A. Die Verwendung des Überwachungsprotokolls kann für Sie von Interesse sein, da es möglich ist, anderen Personen in Ihrer Organisation (z. B. Ihrem Compliance Officer) Berechtigungen zuzuweisen, um im Überwachungsprotokoll nach diesen Daten zu suchen.

### <a name="deleting-system-generated-logs"></a>Löschen von vom System generierten Protokollen

Um vom System generierte Protokolle zu löschen, die über eine Zugriffsanforderung abgerufen werden, müssen Sie den Benutzer aus dem Dienst entfernen und sein Azure Active Directory-Konto dauerhaft löschen. Anweisungen zum dauerhaften Löschen eines Benutzers finden Sie im Abschnitt [Löschen eines Benutzers](#deleting-a-user) in diesem Leitfaden. Es ist wichtig zu beachten, dass das dauerhafte Löschen eines Benutzerkontos nach dem Start unwiderruflich ist.

Durch die dauerhafte Löschung eines Benutzerkontos werden die Daten des Benutzers – mit Ausnahme von Daten, die für die Sicherheit und die Stabilität des Dienstes wesentlich sind – innerhalb von 30 Tagen aus vom System generierten Protokollen für fast alle Office 365-Dienste entfernt. 

Eine Ausnahme bildet Exchange Online, da die dauerhafte Löschung des Benutzerkontos hier länger als 30 Tage dauert. Angesichts der kritischen Natur von Exchange Online-Inhalten und zur Vermeidung von versehentlichem Datenverlust wurde dieses System so konzipiert, dass es Daten bis zu 60 Tage nach der endgültigen Löschung eines Benutzerkontos absichtlich in einen Haltestatus versetzt. Um die Exchange Online-Daten eines Benutzers in einem Zeitraum von 30 Tagen dauerhaft zu löschen, löschen Sie das Benutzerkonto in Azure Active Directory dauerhaft, und wenden Sie sich dann an den [Microsoft-Support](https://support.microsoft.com/) mit der Bitte, die Exchange Online-Daten des Benutzers abweichend vom geplanten Löschvorgang manuell zu entfernen. Weitere Informationen finden Sie unter [Entfernen von Exchange Online-Daten](#removing-exchange-online-data), das zuvor in diesem Leitfaden erläutert wurde.

Beim Löschen eines Benutzerkontos werden die vom System generierten Protokolle für Yammer und Kaizala nicht entfernt. Siehe die folgenden Links, um Daten aus diesen Anwendungen zu entfernen:

- Yammer – [Verwalten von Anträgen betroffener Personen nach der DSGVO in Yammer Enterprise](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)
- Kaizala – [Exportieren oder Löschen der Organisationsdaten eines Benutzers in Kaizala](/office365/kaizala/export-or-delete-a-user-s-data)

#### <a name="national-clouds"></a>Nationale Clouds

Ein globaler IT-Administrator muss in den folgenden nationalen Clouds Folgendes tun, um vom System generierte Protokolle zu exportieren:

- **Office 365 Deutschland**: Führen Sie die vorstehenden Schritte aus.
- **Office 365 US Government**: [Wechseln Sie zum Office 365-Verwaltungsportal](https://portal.office365.us), und reichen Sie eine Anforderung beim Microsoft-Support ein.
- **Office 365, das von 21Vianet betrieben wird (China)**: [ Navigieren Sie zum Office 365-Verwaltungsportal, das von 21Vianet betrieben wird](https://portal.partner.microsoftonline.cn/AdminPortal/Home#/homepage), gehen Sie zu **Handel** > **Abonnement** > **Datenschutz** > **DSGVO**, und geben Sie die erforderlichen Informationen ein.

## <a name="part-4-additional-resources-to-assist-you-with-dsrs"></a>Teil 4: Weitere Ressourcen, die bei Anträgen betroffener Personen hilfreich sind

### <a name="dsr-guides-for-other-microsoft-enterprise-services"></a>Leitfäden für Anträge betroffener Personen für andere Microsoft-Unternehmensdienste

Dieser Leitfaden ist dem Thema gewidmet, wie Sie bei der Verwendung von Office 365-Produkten, -Diensten und -Verwaltungstools personenbezogene Daten finden und damit umgehen und wie Sie auf Anträge betroffener Personen reagieren können. Gehen Sie zum [Microsoft Service Trust Portal](https://servicetrust.microsoft.com/), um auf ähnliche Leitfäden für andere Microsoft Enterprise Services zuzugreifen.

### <a name="microsoft-support"></a>Microsoft-Support

"Support-Daten" sind die Daten, die Sie und Ihre Benutzer Microsoft zur Verfügung stellen, wenn Ihre Organisation oder Ihre Benutzer mit Microsoft interagieren, um Produkt-Support in Bezug auf Office 365 oder andere Microsoft-Produkte und -Dienste zu erhalten (zum Beispiel, um unerwartetes Produktverhalten zu beheben). Einige dieser Daten können personenbezogene Daten enthalten. Weitere Informationen finden Sie unter [Anträge betroffener Personen nach der DSGVO in Microsoft-Support und Professional Services](/microsoft-365/compliance/gdpr-dsr-prof-services).

### <a name="product-and-services-authenticated-with-an-org-id-for-which-microsoft-is-a-data-controller"></a>Produkte und Dienste, die mit einer Org-ID authentifiziert sind, für die Microsoft ein Datenverantwortlicher ist

Teile 1–3 dieses Leitfadens beziehen sich auf Produkte und Dienste, bei denen Microsoft ein Datenauftragsverarbeiter für Ihre Organisation ist, wodurch Ihrem Mandantenadministrator die Funktionalität für Anträge betroffener Personen zur Verfügung gestellt wird. Es gibt verschiedene Umstände, unter denen sich die Benutzer Ihrer Organisation mit ihrem Geschäfts-, Schul- oder Unikonto (auch als „Azure Active Directory ID“ oder „AAD“ bezeichnet) bei Microsoft-Produkten und -Diensten anmelden, für die Microsoft ein Datenverantwortlicher ist. Für alle diese Produkte und Dienste müssen Ihre Benutzer ihre eigenen Anträge betroffener Personen direkt an Microsoft stellen, und Microsoft bearbeitet diese Anträge in direkter Zusammenarbeit mit dem Benutzer. Produkte und Dienste, die Inhalte speichern, die von Benutzern erstellt wurden, es den Benutzern ermöglichen, auf die von ihnen erstellten Inhalte zuzugreifen, sie zu exportieren, zu korrigieren und zu löschen, was Bestandteil der inhärenten Funktionalität der Produkte ist. Zu den Szenarien, in denen dies zutreffen kann, gehören die folgenden:

- **Optionale verbundene Onlinedienste:** Microsoft 365 Apps for Enterprise stellt dem Benutzer bestimmte optionale verbundene Onlinedienste zur Verfügung. Die Liste dieser Dienste und die dazugehörigen Benutzersteuerelemente finden Sie [hier](https://support.office.com/article/microsoft-s-other-connected-services-92c234f1-dc91-4dc1-925d-6c90fc3816d8). Sie können entscheiden, ob Sie Ihren Endbenutzern die Nutzung dieser Dienste erlauben möchten. Weitere Informationen finden Sie unter [Wie Administratoren Verantwortlichendienste in Microsoft 365 Apps for Enterprise verwalten können](/DeployOffice/manage-controller-services-office-365-proplus). Soweit diese optionalen Dienste personenbezogene Daten, ist Microsoft ein Datenverantwortlicher für diese Dienste verantwortlich.
- **Benutzer-Feedback:** Wenn Ihre Benutzer sich dafür entscheiden, Feedback zu Microsoft-Produkten und -Diensten zu geben, ist Microsoft ein Datenverantwortlicher für dieses Feedback, soweit es personenbezogene Daten enthält. Microsoft kommt allen Anfragen betroffener Personen zu von Microsoft erfasstem Feedback (einschließlich von Microsoft-Vertragsverarbeitern verwaltetes Feedbacks) nach, außer in Fällen, in denen Microsoft die Benutzer angewiesen hatte, während des Feedback-Erfassungsprozesses keine persönlichen Daten einzubeziehen. Ausnahmen: Wenn Microsoft die Benutzer angewiesen hat, keine personenbezogenen Daten während des Feedback-Erfassungsprozesses anzugeben, verlässt sich Microsoft auf diese Anweisung und geht davon aus, dass keine personenbezogenen Daten zur Verfügung gestellt wurden. Benutzer, die ein separates Konto bei externen Feedback-Dienstleistern eingerichtet haben, müssen ihre Anträge betroffener Personen direkt an diese Anbieter richten.
- **Windows-Authentifizierung über ein Geschäfts-, Schul- oder Unikonto:** Wenn Ihre Organisation Windows-Lizenzen erworben hat und Ihre Benutzer sich mit ihrem Geschäfts-, Schul- oder Unikonto beim vom Unternehmen bereitgestellten Windows authentifizieren, fungiert Microsoft als Datenverantwortlicher.
- **Vom Benutzer erworbene Produkte oder Dienste:** Wenn Sie Ihren Benutzern erlauben, in ihrer Eigenschaft als Einzelpersonen Microsoft-Produkte oder -Dienste zu erwerben, die AAD zur Authentifizierung verwenden, zum Beispiel Office Add-Ons oder Anwendungen, die in einem Microsoft Store verfügbar sind, ist Microsoft unter Umständen ein Datenverantwortlicher. Für solche Microsoft-Produkte oder -Dienste müssen sich Benutzer direkt an Microsoft wenden, um einen Antrag als betroffene Person zu stellen.

> [!IMPORTANT]
> Wenn Sie einen Benutzer löschen, der über Azure Active Directory aktiviert wurde, kann sich Ihr (früherer) Benutzer nicht mehr bei den Produkten oder Diensten anzumelden, für die er früher ein Geschäfts-, Schul- oder Unikonto genutzt hat. Außerdem wäre Microsoft dann nicht mehr in der Lage, den Benutzer in Verbindung mit einem Antrag einer betroffenen Personen für Produkte oder Dienste, für die Microsoft ein Datenverantwortlicher ist, zu authentifizieren. Wenn Sie es einem Benutzer ermöglichen möchten, Anträge betroffener Personen für solche Dienste zu stellen, ist es wichtig, dass Sie Ihren Benutzer anweisen, dies zu tun, bevor Sie das AAD-Konto sein löschen.

### <a name="personal-accounts"></a>Persönliche Konten

Wenn Ihre Benutzer Microsoft-Konten (also persönliche Konten) verwendet haben, um Produkte und Dienste von Microsoft, für die Microsoft ein Datenverantwortlicher ist, für ihren persönlichen Gebrauch zu erwerben, können diese Benutzer Anträge betroffener Personen über das [Microsoft Datenschutz-Dashboard](https://account.microsoft.com/account/privacy) stellen.

### <a name="third-party-products"></a>Produkte von Drittanbietern

Wenn Ihre Organisation oder Ihre Benutzer in ihrer Eigenschaft als Einzelpersonen Produkte oder Dienste von Dritten erworben haben und ihr Microsoft-Geschäfts-, Schul- oder Unikonto zur Authentifizierung verwenden, sollten alle Anträge betroffener Personen an den jeweiligen Dritten gerichtet werden.

## <a name="appendix-a-preparing-for-dsr-investigations"></a>Anhang A: Untersuchungen für Anträge von betroffenen Personen vorbereiten

Beachten Sie die folgenden Empfehlungen, wenn Sie Ihre Organisation dabei unterstützen, sich auf Untersuchungen für Anträge betroffener Personen vorzubereiten:

- Verwenden des eDiscovery-Falltools für Anträge betroffener Personen im Security & Compliance Center zum Verwalten von Untersuchungen von Anträgen betroffener Personen
- Einrichten von Compliance-Grenzen, um den Bereich der Inhaltssuchen einzuschränken
- Verwenden des Überwachungsprotokoll-Suchtools für Untersuchungen im Rahmen von Anträgen betroffener Personen

### <a name="use-the-dsr-case-tool-to-manage-dsr-investigations"></a>Verwenden des Falltools für Anträge betroffener Personen zum Verwalten von Untersuchungen von Anträgen betroffener Personen

Wir empfehlen Ihnen, das Falltool für Anträge betroffener Personen im Security & Compliance Center zu verwenden, um Untersuchungen von Anträgen betroffener Personen zu verwalten. Mit dem Falltool für Anträge betroffener Personen können Sie Folgendes tun:

- Erstellen Sie einen separaten Fall für jede Untersuchung eines Antrags einer betroffenen Person.

- Verwenden Sie die integrierte Suchanfrage, um nach allen Inhalten zu einem bestimmten Thema zu suchen. Wenn Sie einen Fall anlegen und die Suche starten, werden diese Speicherorte für Inhalte durchsucht:

   - Alle Postfächer in Ihrer Organisation (einschließlich der Postfächer aller Microsoft Teams und Microsoft 365-Gruppen)
   - Alle SharePoint Online-Websites und OneDrive for Business-Konten in Ihrer Organisation
   - Alle Microsoft Teams-Websites und Microsoft 365-Gruppenwebsites in Ihrem Unternehmen
   - Alle öffentlichen Ordner in Exchange Online

- Überarbeiten Sie die standardmäßige Suchabfrage und führen Sie die Suche erneut aus, um die Suchergebnisse einzuschränken.

- Kontrollieren Sie, wer Zugriff auf den Fall hat, indem Sie Personen als Mitglieder des Falls hinzufügen; nur Mitglieder können auf den Fall zugreifen, und diese Mitglieder können nur ihre eigenen Fälle in der Liste der Fälle auf der Seite mit den Fällen für Anträge betroffener Personen im Security & Compliance Center anzeigen. Zusätzlich können Sie verschiedenen Mitgliedern desselben Falls unterschiedliche Berechtigungen zuweisen. Beispielsweise können Sie festlegen, dass einige Mitglieder nur den Fall und die Ergebnisse einer Inhaltssuche anzeigen können, und dass andere Mitglieder Suchabfragen erstellen und Suchergebnisse exportieren können.

- Erstellen Sie Exportaufträge. um in Reaktion auf einen Antrag einer betroffenen Person auf Export die Suchergebnisse zu exportieren. Sie können alle Inhalte, die von der Inhaltssuche zurückgegeben werden, exportieren. Andere Office 365-Daten im Zusammenhang mit einer betroffenen Person werden auch exportiert.

- Erstellen Sie Exportaufträge. um in Reaktion auf einen Antrag einer betroffenen Person auf Export die Suchergebnisse zu exportieren. Sie können alle Inhalte, die von der Inhaltssuche zurückgegeben werden, exportieren. Sie können auch vom System generierte Protokolle für den Office Roaming-Dienst exportieren.

- Löschen Sie Fälle, nachdem die Untersuchung des Antrags einer betroffenen Person abgeschlossen wurde. Dadurch werden alle Inhaltssuchen und Exportaufgaben entfernt, die mit dem Fall verbunden sind.

Informationen zu den ersten Schritten mit Anträgen betroffener Personen finden Sie in unter [Verwalten von Anträgen betroffener Personen nach der DSGVO mit dem Falltool für Anträge betroffener Personen im Security & Compliance Center](/microsoft-365/compliance/manage-gdpr-data-subject-requests-with-the-dsr-case-tool).

> [!IMPORTANT]
> Ein eDiscovery-Administrator kann alle Fälle für Anträge betroffener Personen in Ihrer Organisation verwalten. Weitere Informationen zu den verschiedenen Rollen im Zusammenhang mit eDiscovery finden Sie unter [Zuweisen von eDiscovery-Berechtigungen für potenzielle Fallmitglieder](/Office365/SecurityCompliance/assign-ediscovery-permissions).

### <a name="set-up-compliance-boundaries-to-limit-the-scope-of-content-searches"></a>Einrichten von Compliance-Grenzen, um den Bereich der Inhaltssuchen einzuschränken

Compliance-Grenzen werden mit Suchberechtigungsfilterfunktion im Security & Compliance Center implementiert. Compliance-Grenzen schaffen logische Suchgrenzen innerhalb eines Unternehmens, die steuern/einschränken, welche Speicherorte für Inhalte (z. B. Exchange Online-Postfächer und SharePoint Online-Websites) ein IT-Administrator oder Compliance Officer durchsuchen kann. Compliance-Grenzen sind nützlich für multinationale Organisationen, die geografische Grenzen respektieren müssen, Regierungsorganisationen, die verschiedene Behörden trennen müssen, und Geschäftsorganisationen, die in Unternehmenseinheiten oder Abteilungen aufgeteilt sind. In all diesen Szenarien können Compliance-Grenzen in Untersuchungen von Anträgen betroffener Personen verwendet werden, um einzuschränken, welche Postfächer und Websites von den an der Untersuchung beteiligten Personen durchsucht werden können.

Sie können Compliance-Grenzen zusammen mit eDiscovery-Fällen verwenden, um die Inhaltsspeicherorte, die im Rahmen einer Untersuchung durchsucht werden, auf Speicherorte innerhalb der Agentur oder Unternehmenseinheit einzuschränken.

Hier ist eine allgemeine Übersicht zum Implementieren von Compliance-Grenzen (zusammen mit eDiscovery-Fällen) für Untersuchungen von Anträgen betroffener Personen.

1. Bestimmen Sie die Agenturen in Ihrem Unternehmen, die als eine Compliance-Grenze bestimmt werden sollen.

2. Legen Sie fest, welches Benutzerobjektattribut in Azure Active Directory zur Definition der Compliance-Grenze verwendet wird. Beispielsweise können Sie die Attribute Country, CountryCode oder Department wählen, sodass Mitglieder der Rollengruppe Administrator, die Sie im nächsten Schritt anlegen, nur die Speicherorte für Inhalte der Benutzer durchsuchen können, die einen bestimmten Wert für dieses Attribut haben. So schränken Sie ein, wer in einer bestimmten Agentur nach Inhalten suchen darf.

   > [!NOTE]
   > Derzeit müssen Sie für OneDrive for Business einen zusätzlichen Schritt ausführen und eine Microsoft-Support-Anforderung einreichen, damit das Attribut mit OneDrive for Business-Konten synchronisiert wird.

3. Erstellen Sie eine Administrator-Rollengruppe im Security & Compliance Center für jede Compliance-Grenze. Es wird empfohlen, dass Sie diese Rollengruppen durch Kopieren der integrierten eDiscovery-Manager-Rollengruppe erstellen, und dann Rollen nach Bedarf entfernen.

4. Fügen Sie Mitglieder zu den bestimmten Rollengruppen als eDiscovery-Manager hinzu. Mitglieder sind die Personen, die für das Untersuchen und Reagieren auf Anträge betroffener Personen verantwortlich sind. In der Regel sind dies IT-Administratoren, Datenschutzbeauftrage, Compliance-Manager und Personalverantwortliche.

5. Erstellen Sie einen Filter für jede Compliance-Grenze, damit die Mitglieder der entsprechenden Administrator-Rollengruppe nur Postfächer und Websites für Benutzer innerhalb dieser Agentur-/Compliance-Grenze suchen können. Der Suchberechtigungsfilter ermöglicht Mitgliedern der entsprechenden Rollengruppe nur auf die Speicherorte zu durchsuchen, die den Benutzerobjektattributwert aufweisen, der der Agentur-/Compliance-Grenze entspricht.

Eine Schritt-für-Schritt-Anleitung finden Sie unter [Einrichten von Compliance-Grenzen für eDiscovery-Untersuchungen in Office 365](/microsoft-365/compliance/set-up-compliance-boundaries).

### <a name="use-the-audit-log-search-tool-in-dsr-investigations"></a>Verwenden des Überwachungsprotokoll-Suchtools für Untersuchungen im Rahmen von Anträgen betroffener Personen

IT-Administratoren können das Überwachungsprotokoll-Suchtool im Security & Compliance Center nutzen, um Dokumente, Dateien und andere Office 365-Ressourcen zu identifizieren, die Benutzer erstellt, geändert oder gelöscht haben oder auf die zugegriffen wurde. Die Suche nach dieser Art von Aktivitäten kann bei Untersuchungen von Anträgen betroffener Personen nützlich sein. Beispielsweise werden in SharePoint Online und OneDrive for Business Überwachungsereignisse protokolliert, wenn Benutzer folgende Aktivitäten ausgeführt haben:

- Auf eine Datei zugreifen
- Eine Datei ändern
- Eine Datei verschieben
- Eine Datei hochladen oder herunterladen

Sie können das Überwachungsprotokoll nach bestimmten Aktivitäten, Typen von Aktivitäten, Aktivitäten eines bestimmten Benutzers und anderen Suchkriterien durchsuchen. Neben SharePoint Online und OneDrive for Business können Sie auch nach Aktivitäten in Flow, Power BI und Microsoft Teams suchen. Überwachungsdatensätze werden 90 Tage lang aufbewahrt. Daher können Sie nicht nach Benutzeraktivitäten suchen, die vor mehr als 90 Tagen stattgefunden haben. Eine vollständige Liste der geprüften Aktivitäten und wie Sie das Überwachungsprotokoll durchsuchen können, finden Sie unter [Durchsuchen des Überwachungsprotokolls im Security & Compliance Center](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance).

> [!TIP]
> Um die oben beschriebene 90-Tage-Beschränkung zu umgehen und einen kontinuierlichen Verlauf der Überwachungsdatensätze Ihrer Organisation zu erhalten, könnten Sie alle Aktivitäten nach einem wiederkehrenden Zeitplan (z. B. alle 30 Tage) exportieren, um eine kontinuierliche Aufzeichnung der Überwachungsdatensätze Ihrer Organisation zu erhalten.

## <a name="appendix-b-change-log"></a>Anhang B: Änderungsprotokoll

In der folgende Tabelle sind die Änderungen an dem Leitfaden für Office 365-Anträge betroffener Personen seit der ersten Veröffentlichung am 25. Mai 2018 aufgeführt.

|Datum  |Abschnitt/App |Änderung  |
|:---------|:---------|:---------|
|18.09.2018 | [Whiteboard](#whiteboard) |Whiteboard Preview ist nicht mehr in der Vorschau und wurde für allgemeine Verfügbarkeit veröffentlicht. Daher wurde der Abschnitt zur Whiteboard-Vorschau in „Whiteboard für PC, Surface Hub und andere Plattformen“ umbenannt; Vorgehensweisen zum Zugreifen auf Daten, zum Exportieren und Löschen von Daten wurden aus diesem Abschnitt entfernt und durch einen Link zum Whiteboard-Support-Artikel ersetzt.|
|08.11.2018 | [Workplace Analytics](#workplace-analytics) |Schrittweise Anleitung für den Abschnitt „Löschen“ mit Informationen zum Entfernen einer betroffenen Person aus Workplace Analytics und zum Entfernen von Informationen über eine betroffene Person aus einem Workplace Analytics-Bericht.|
|12.11.2018| Alle| Fehlerhafte Lesezeichen und fehlerhafte Links zu externen Themen wurden korrigiert.|
|09. Januar 2019| StaffHub |Im Abschnitt "Löschen" wurde die Beschreibung aktualisiert, was passiert, wenn ein Benutzerkonto dauerhaft gelöscht wird.|
|8.5.2019| [Publisher](#publisher)|Informationen zur Reaktion auf Anträge betroffener Personen in Publisher wurden hinzugefügt.|
|11.7.2019| [MyAnalytics](#myanalytics)|Die Möglichkeit für einen Administrator, das Falltool für Anträge betroffener Personen im Security & Compliance Center zum Exportieren von myAnalytics-Daten zu verwenden, wurde entfernt, da alle Benutzer ihre Daten jetzt in der myAnalytics-App anzeigen können. |
|06.11.2019|[Bildung](#education)|Mit neuen Themen zur Verwendung von PowerShell-Skripts zum Abrufen einer Liste der Kurse für einen bestimmten Kursteilnehmer verknüpft, um diese dann zu exportieren oder zu löschen.|
|28.01.2020| Alle | StaffHub aus Dokument entfernt; StaffHub wurde eingestellt. |
||||
