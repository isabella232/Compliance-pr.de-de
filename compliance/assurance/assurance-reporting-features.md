---
title: Microsoft 365-Berichtsfeatures
description: Erfahren Sie mehr über verschiedene Berichtsfunktionen in Microsoft 365, einschließlich Azure Active Directory und Exchange Online.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-analytics
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: a745c470dc30703f438258985169431c1053e65d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120784"
---
# <a name="microsoft-365-reporting-features"></a>Microsoft 365-Berichtsfeatures

Berichterstellungsfunktionen in Microsoft 365 bieten verschiedene Überwachungsberichte für Azure Active Directory (Azure AD), Exchange Online, Geräteverwaltung, Aufsichtsüberprüfung und Verhinderung von Datenverlust (Data Loss Prevention, DLP). Diese Berichte unterscheiden sich von den Microsoft 365-Aktivitätsberichten.

## <a name="microsoft-365-reports-dashboard"></a>Dashboard "Microsoft 365-Berichte"

Das Dashboard "Berichte" in der Vorschau des Microsoft 365 Admin Centers zeigt Nutzungsaktivitäten in Microsoft 365 an. Globale Microsoft 365-Administratoren oder Exchange Online-, SharePoint Online- oder Skype for Business-Administratoren erhalten detaillierte Einblicke in die Nutzung dieses Diensts. Beispielsweise die Anzahl der Benutzer in einem bestimmten Microsoft 365-Dienst, die Anzahl der Benutzer, die Microsoft 365 Apps for Enterprise (zuvor Office 365 ProPlus genannt) aktiviert haben und wie viele E-Mails über die Organisation fließen. Berichte sind für die letzten 7, 30, 90 und 180 Tage verfügbar.

Die folgenden Berichte sind verfügbar:

- [E-Mail-Aktivitätsbericht](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office von Aktivierungen](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [SharePoint Online -Websiteverwendungsbericht](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [OneDrive for #A0](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Yammer-Aktivitätsbericht](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Skype for Business-Aktivitätsbericht](/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Bericht über Skype for Business-Peer-zu-Peer-Aktivitäten](/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Bericht "Skype for Business Conference Organizer"](/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Skype for Business Conference Participant Activity Report](/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Weitere Informationen finden Sie unter [Aktivitätsberichte im Microsoft 365 Admin Center.](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263)

## <a name="azure-ad-reports"></a>Azure AD Reports

Microsoft 365 verwendet Azure AD für die Authentifizierung und Identitätsverwaltung. Microsoft 365-Administratoren verwenden von Azure generierte Berichte, um ungewöhnliche Aktivitäten und nicht autorisierten Zugriff auf ihre Daten zu identifizieren. Sie können Zugriffs- und Verwendungsberichte in Azure AD verwenden, um Einblicke in die Verzeichnisintegrität und -sicherheit für Ihre Organisation zu erhalten. Mit diesen Informationen können Sie mögliche Sicherheitsrisiken identifizieren und mindern.

Azure AD-Berichte können nach Microsoft Excel exportiert und mit anderen Daten aus Microsoft 365 korreliert werden. Beispielsweise können die Ergebnisse einer Überwachungsprotokollsuche Einblicke in Zugriff, Authentifizierung und Aktivitäten auf Anwendungsebene bieten. Erweiterte Anomalie- und Ressourcenverwendungsberichte sind mit Azure AD Premium verfügbar. Diese erweiterten Berichte helfen Ihnen, Ihre Sicherheitslage zu verbessern und auf potenzielle Bedrohungen zu reagieren, indem Sie Analysen zum Gerätezugriff und zur Anwendungsnutzung anwenden. Weitere Informationen finden Sie in [der Azure Active Directory-Berichterstellung.](/azure/active-directory/reports-monitoring/overview-reports/)

## <a name="exchange-online-audit-reports"></a>Exchange Online Audit Reports

Exchange Online-Überwachungsberichte enthalten Details zum Postfachzugriff und zu Änderungen, die von Administratoren an Ihrem Exchange Online-Mandanten vorgenommen wurden. Bei der Postfachüberwachung können Sie die Aufgaben in der folgenden Tabelle verwenden, um Berichte auszuführen und Exchange Online-Überwachungsprotokolle zu exportieren.

> [!NOTE]
> Sie müssen die Postfach-Überwachungsprotokollierung für jedes Postfach aktivieren, damit überwachte Ereignisse im Überwachungsprotokoll für dieses Postfach gespeichert werden. Wenn die Postfach-Überwachungsprotokollierung für ein Postfach nicht aktiviert ist, werden Ereignisse für dieses Postfach nicht im Überwachungsprotokoll gespeichert und nicht in Postfach-Überwachungsberichten angezeigt. Weitere Informationen finden Sie unter Aktivieren [der Postfachüberwachung.](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918)

| Aufgabe | Beschreibung |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ausführen eines Berichts zum Postfachzugriff durch Nicht-Besitzer](/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Zeigt die Liste der Postfächer an, auf die von einer anderen Person als dem Besitzer des Postfachs zugegriffen wird. Der Bericht enthält Informationen dazu, wer auf das Postfach zugegriffen hat, welche Aktionen im Postfach sie ausführen und ob die Aktionen erfolgreich waren. |
| [Exportieren von Postfachüberwachungsprotokollen](/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | Postfach-Überwachungsprotokolle enthalten Informationen zu Zugriff und Aktionen in einem Postfach, die von einem anderen Benutzer als dem Postfachbesitzer ergriffen wurden. Administratoren können Postfächer zusammen mit einem Datumsbereich angeben, um Berichte zu generieren. Die Protokolle werden in XML exportiert, an eine Nachricht angefügt und an bestimmte Benutzer gesendet, wie vom Administrator festgelegt. |
| [Ausführen eines Berichts für Administratorrollengruppen](/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | Die Administratorrollegruppe weist Benutzern Administratorrechte zu. Mit diesen Berechtigungen können Benutzer Verwaltungsaufgaben ausführen, z. B. Kennwörter zurücksetzen, Postfächer erstellen oder ändern und anderen Benutzern Administratorrechte zuweisen. Der Bericht über Administrator-Rollengruppen zeigt Änderungen an Rollengruppen an, einschließlich des Hinzu- oder Entfernens von Mitgliedern. |
| [Anzeigen des Administrator-Überwachungsprotokolls](/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | Im Administrator-Überwachungsprotokollbericht sind alle Erstellungs-, Aktualisierungs- und Löschfunktionen aufgeführt, die von Administratoren in Exchange Online ausgeführt werden. Protokolleinträge enthalten Informationen dazu, welches Cmdlet ausgeführt wurde, welche Parameter verwendet wurden, wer das Cmdlet ausgeführt hat und welche Objekte betroffen sind. |
| [Durchsuchen und Archivieren von Postfachinhalten](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Enthält Details zu allen Änderungen an In-Place eDiscovery- oder In-Place für Postfächer. |
| [Exportieren des Administrator-Überwachungsprotokolls](/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | Im Administrator-Überwachungsprotokoll werden bestimmte Verwaltungsaktionen aufgezeichnet, z. B. erstellen, aktualisieren und löschen in Exchange Online. Die Ergebnisse aus dem Protokoll werden in XML exportiert, und Administratoren können dieses Protokoll an eine Gruppe von Benutzern senden. |
| [Ausführen eines Berichts zur Beweissicherung pro Postfach](/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Enthält Details zu allen Änderungen an den Einstellungen für das Archiv für Rechtsstreitigkeiten für Postfächer. |
| [Anzeigen und Exportieren des externen Administrator-Überwachungsprotokolls](/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Enthält Details zu Aktionen, die von externen Administratoren ausgeführt werden. Die Einträge enthalten Informationen dazu, welches Cmdlet ausgeführt wurde, welche Parameter verwendet wurden und welche Aktionen Objekte in Exchange Online erstellen, ändern oder löschen. |

## <a name="device-compliance-reports"></a>Berichte zur Gerätekonformität

Sie verwalten und sichern mobile Geräte, die mit Ihrem Abonnement verbunden sind, mit Basic Mobility and Security für Microsoft 365. Mobile Geräte, die für den Zugriff auf Arbeits-E-Mails, Kalender, Kontakte und Dokumente verwendet werden, spielen eine wichtige Rolle dabei, sicherzustellen, dass Mitarbeiter jederzeit und von überall aus arbeiten können. Es ist wichtig, dass Sie die Informationen Ihrer Organisation schützen. Sie verwenden Basic Mobility and Security für Microsoft 365 zum Festlegen von Gerätesicherheitsrichtlinien und Zugriffsregeln. Wenn sie verloren gehen oder gestohlen werden, verwenden Sie auch Basic Mobility and Security für Microsoft 365, um mobile Geräte zu löschen.

Grundlegende Berichte zur Mobilität und Sicherheit bieten eine Übersicht über Richtlinien, die von einer Organisation zum Sichern mobiler Geräte eingerichtet wurden, die auf Microsoft 365-Daten zugreifen. Der Bericht ermöglicht das Filtern von Geräten nach Compliancestatus, gemeldeten Verstößen, blockierten Geräten und der Anzahl von Geräten, die aufgrund von Sicherheitsrichtlinien gelöscht wurden. Weitere Informationen finden Sie unter [Overview of Basic Mobility and Security for Microsoft 365](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a).

## <a name="data-loss-prevention"></a>Verhinderung von Datenverlust

Mithilfe von DLP-Richtlinien können Sie die Sicherheit und den Informationsfluss in einer Organisation verwalten. Sie können Richtlinien einrichten, um den Zugriff auf Inhalte zu blockieren, Daten zu verschlüsseln oder Benutzer über Richtlinien- und Richtlinienverstöße mithilfe von in der Anwendung verwendeten DLP-Richtlinientipps zu benachrichtigen. DLP Reports provide insight into the number of policy and rule matches, overrides, and false positives.

Sie verwenden das Microsoft 365 Admin Center, um Informationen über die Anzahl der Nachrichten, die von Ihren DLP-Richtlinien erkannt wurden, anzeigen zu können. DLP-Berichte bieten Einblicke in Richtlinien- und Regel übereinstimmungen für gesendete und empfangene E-Mails. Sie können auch die Anzahl der Übereinstimmungen, Außerkraftsetzungen und falsch positiven Ergebnisse für jede Richtlinie innerhalb der letzten 24 Stunden im Exchange Admin Center anzeigen. Wenn Sie einen Excel-Bericht herunterladen, können Sie noch mehr Details anzeigen, z. B. wer welche Nachricht gesendet hat, an welchem Tag und welche Richtlinien übereinstimmungen ausgelöst wurden. Weitere Informationen finden Sie unter [Anzeigen von Berichten über DLP-Richtlinienerkennungen.](/previous-versions/exchange-server/exchange-150/jj889415(v=exchg.150))

## <a name="auditing-in-yammer-enterprise"></a>Überwachung in Yammer Enterprise

Yammer Enterprise bietet Administratoren die Möglichkeit, Benutzeraktivitätsdaten aus ihrem Yammer-Netzwerk über die [Yammer-Datenexport-API](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)oder manuell über die Yammer-Netzwerkadministratorseite zu exportieren. Die Möglichkeit zum Exportieren von Protokollen ist auf Netzwerkadministratoren in Yammer. (Alle globalen Microsoft 365-Administratoren Yammer Netzwerkadministratoren.)

Die folgenden Daten können exportiert werden:

| Filename | Beschreibung |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | Alle neuen, ausstehenden und angehaltenen Benutzer im Netzwerk |
| Messages.csv | Alle Nachrichten im Netzwerk |
| Files.csv (Metadaten) | Metadaten wie Dateiname, Datei-API-URL, Uploader-ID, hochgeladen unter usw. |
| Files.csv (Originaldateien) | Zip-Datei der ursprünglichen Dateien, die von Benutzern in die Datei Yammer |
| Topics.csv | Im Netzwerk erstellte Themen |
| Pages.csv | Von Benutzern im Netzwerk erstellte Seiten (Notizen) |
| Admins.csv | Alle überprüften Administratoren im Netzwerk |
| Networks.csv | Alle Yammer externen Netzwerke |

Yammer Enterprise-Daten sind auch über die Microsoft 365-Aktivitätsberichte verfügbar. Darüber hinaus arbeitet Yammer aktiv daran, zusätzliche Protokollierung über die Microsoft 365-Verwaltungsaktivitäts-API verfügbar zu machen und die Möglichkeit zu haben, Daten mithilfe von Power BI zu begrunden. Weitere Informationen [zu diesen Features finden](https://fasttrack.microsoft.com/roadmap?filters=yammer) Sie in der Office-Roadmap.
