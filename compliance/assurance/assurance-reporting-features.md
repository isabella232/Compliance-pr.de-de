---
title: Microsoft 365-Berichterstellungsfeatures
description: Erfahren Sie mehr über verschiedene Berichterstellungsfunktionen in Microsoft 365, einschließlich Azure Active Directory und Exchange Online.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-analytics
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: be05c96c725f8d0e05bc27f410d7f19e4e5d9a23
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947039"
---
# <a name="microsoft-365-reporting-features"></a>Microsoft 365-Berichterstellungsfeatures

Berichterstellungsfunktionen in Microsoft 365 bieten verschiedene Überwachungsberichte für Azure Active Directory (Azure AD), Exchange Online, Geräteverwaltung, Aufsichtsüberprüfung und Verhinderung von Datenverlust (Data Loss Prevention, DLP). Diese Berichte unterscheiden sich von den Microsoft 365 Aktivitätsberichten.

## <a name="microsoft-365-reports-dashboard"></a>Microsoft 365 Dashboard "Berichte"

Im Dashboard "Berichte" in der Microsoft 365 Admin Center Vorschau werden Nutzungsaktivitäten über Microsoft 365 hinweg angezeigt. Microsoft 365 globale Administratoren oder ein Exchange Online-, SharePoint Online- oder Skype for Business administrator können detaillierte Einblicke in die Nutzung dieses Diensts erhalten. Beispielsweise die Anzahl der Benutzer in einem bestimmten Microsoft 365 Dienst, die Anzahl der Benutzer, die Microsoft 365 Apps for Enterprise aktiviert haben (zuvor Office 365 ProPlus genannt), und die Anzahl der E-Mails, die durch die Organisation fließen. Berichte sind für die letzten 7, 30, 90 und 180 Tage verfügbar.

Die folgenden Berichte sind verfügbar:

- [E-Mail-Aktivitätsbericht](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office Aktivierungsbericht](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [SharePoint Bericht zur Nutzung von Onlinewebsites](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [OneDrive for Business Nutzungsbericht](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Yammer-Aktivitätsbericht](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Skype for Business Aktivitätsbericht](/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Skype for Business Bericht über Peer-to-Peer-Aktivitäten](/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Skype for Business Konferenzorganisatorbericht](/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Skype for Business Konferenzteilnehmeraktivitätsbericht](/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Weitere Informationen finden Sie [unter Aktivitätsberichte im Microsoft 365 Admin Center](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263).

## <a name="azure-ad-reports"></a>Azure AD-Berichte

Microsoft 365 verwendet Azure AD für die Authentifizierung und Identitätsverwaltung. Microsoft 365 Administratoren verwenden von Azure generierte Berichte, um ungewöhnliche Aktivitäten und nicht autorisierten Zugriff auf ihre Daten zu identifizieren. Sie können Zugriffs- und Verwendungsberichte in Azure AD verwenden, um Einblicke in die Verzeichnisintegrität und -sicherheit für Ihre Organisation zu erhalten. Mit diesen Informationen können Sie mögliche Sicherheitsrisiken identifizieren und mindern.

Azure AD-Berichte können in Microsoft Excel exportiert und mit anderen Daten aus Microsoft 365 korreliert werden. Beispielsweise können die Ergebnisse einer Überwachungsprotokollsuche Einblicke in Aktivitäten auf Zugriff, Authentifizierung und Anwendungsebene bieten. Erweiterte Anomalie- und Ressourcennutzungsberichte sind mit Azure AD Premium verfügbar. Diese erweiterten Berichte verbessern Ihren Sicherheitsstatus und helfen Ihnen, auf potenzielle Bedrohungen zu reagieren, indem Sie Analysen zum Gerätezugriff und zur Anwendungsnutzung anwenden. Weitere Informationen finden Sie unter [Azure Active Directory Berichterstellung.](/azure/active-directory/reports-monitoring/overview-reports/)

## <a name="exchange-online-audit-reports"></a>Exchange Online Überwachungsberichte

Exchange Online Überwachungsberichte enthalten Details zum Postfachzugriff und änderungen, die administratoren an Ihrem Exchange Online Mandanten vorgenommen haben. Bei der Postfachüberwachung können Sie die Aufgaben in der folgenden Tabelle verwenden, um Berichte auszuführen und Exchange Online Überwachungsprotokolle zu exportieren.

> [!NOTE]
> Sie müssen die Postfachüberwachungsprotokollierung für jedes Postfach aktivieren, damit überwachte Ereignisse im Überwachungsprotokoll für dieses Postfach gespeichert werden. Wenn die Postfachüberwachungsprotokollierung für ein Postfach nicht aktiviert ist, werden Ereignisse für dieses Postfach nicht im Überwachungsprotokoll gespeichert und nicht in Postfachüberwachungsberichten angezeigt. Weitere Informationen finden Sie unter [Aktivieren der Postfachüberwachung.](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918)

| Aufgabe | Description |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ausführen eines Berichts zum Postfachzugriff durch Nicht-Besitzer](/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Zeigt die Liste der Postfächer an, auf die von einer anderen Person als dem Besitzer des Postfachs zugegriffen wird. Der Bericht enthält Informationen darüber, wer auf das Postfach zugegriffen hat, welche Aktionen im Postfach ausgeführt wurden und ob die Aktionen erfolgreich waren. |
| [Exportieren von Postfachüberwachungsprotokollen](/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | Postfachüberwachungsprotokolle enthalten Informationen zum Zugriff und zu Aktionen in einem Postfach, die von einem anderen Benutzer als dem Postfachbesitzer ausgeführt werden. Administratoren können Postfächer zusammen mit einem Datumsbereich angeben, um Berichte zu generieren. Die Protokolle werden in XML exportiert, an eine Nachricht angefügt und wie vom Administrator festgelegt an bestimmte Benutzer gesendet. |
| [Ausführen eines Berichts für Administratorrollengruppen](/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | Die Administratorrollengruppe weist Benutzern Administratorrechte zu. Mit diesen Berechtigungen können Benutzer administrative Aufgaben ausführen, z. B. Kennwörter zurücksetzen, Postfächer erstellen oder ändern und anderen Benutzern Administratorrechte zuweisen. Der Administratorrollengruppenbericht zeigt Änderungen an Rollengruppen an, einschließlich des Hinzufügens oder Entfernens von Mitgliedern. |
| [Anzeigen des Administratorüberwachungsprotokolls](/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | Der Administratorüberwachungsprotokollbericht listet alle Erstellungs-, Aktualisierungs- und Löschfunktionen auf, die von Administratoren in Exchange Online ausgeführt werden. Protokolleinträge enthalten Informationen dazu, welches Cmdlet ausgeführt wurde, welche Parameter verwendet wurden, wer das Cmdlet ausgeführt hat und welche Objekte betroffen sind. |
| [Postfachinhaltssuche und -aufbewahrung](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Enthält Details zu allen Änderungen an In-Place eDiscovery- oder In-Place-Aufbewahrungseinstellungen für Postfächer. |
| [Exportieren des Administratorüberwachungsprotokolls](/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | Das Administratorüberwachungsprotokoll zeichnet bestimmte administrative Aktionen wie Erstellen, Aktualisieren und Löschen in Exchange Online auf. Die Ergebnisse aus dem Protokoll werden in XML exportiert, und Administratoren können dieses Protokoll an eine Gruppe von Benutzern senden. |
| [Ausführen eines Berichts zur Beweissicherung pro Postfach](/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Enthält Details zu allen Änderungen an Einstellungen für das Beweissicherungsverfahren für Postfächer. |
| [Anzeigen und Exportieren des Überwachungsprotokolls für externe Administratoren](/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Enthält Details zu Aktionen, die von externen Administratoren ausgeführt werden. Die Einträge enthalten Informationen dazu, welches Cmdlet ausgeführt wurde, welche Parameter verwendet wurden und welche Aktionen Objekte in Exchange Online erstellen, ändern oder löschen. |

## <a name="device-compliance-reports"></a>Gerätekompatibilitätsberichte

Sie verwalten und sichern mobile Geräte, die mit Ihrem Abonnement verbunden sind, mit basic Mobility and Security für Microsoft 365. Mobile Geräte, die für den Zugriff auf geschäftliche E-Mails, Kalender, Kontakte und Dokumente verwendet werden, spielen eine wichtige Rolle, um sicherzustellen, dass Mitarbeiter jederzeit und von überall aus arbeiten können. Es ist wichtig, dass Sie die Informationen Ihrer Organisation schützen. Sie verwenden basic Mobility and Security für Microsoft 365, um Gerätesicherheitsrichtlinien und Zugriffsregeln festzulegen. Wenn sie verloren gehen oder gestohlen werden, verwenden Sie auch Basic Mobility and Security für Microsoft 365, um mobile Geräte zu löschen.

Grundlegende Berichte zur Mobilitäts- und Sicherheitscompliance bieten eine Übersicht über richtlinien, die von einer Organisation eingerichtet wurden, um mobile Geräte zu schützen, die auf Microsoft 365 Daten zugreifen. Der Bericht ermöglicht das Filtern von Geräten nach Compliancestatus, gemeldeten Verstößen, blockierten Geräten und wie vielen Geräten aufgrund von Sicherheitsrichtlinien gelöscht wurden. Weitere Informationen finden Sie unter [Overview of Basic Mobility and Security for Microsoft 365](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a).

## <a name="data-loss-prevention"></a>Verhinderung von Datenverlust

DLP-Richtlinien helfen bei der Verwaltung der Sicherheit und des Informationsflusses in einer Organisation. Sie können Richtlinien einrichten, um den Zugriff auf Inhalte zu blockieren, Daten zu verschlüsseln oder Benutzer über Richtlinien- und Richtlinienverstöße mithilfe von in-Application DLP Policy Tipps zu benachrichtigen. DLP-Berichte bieten Einblicke in die Anzahl der Richtlinien- und Regelüberstimmungen, Außerkraftsetzungen und falsch positiven Ergebnisse.

Verwenden Sie die Microsoft 365 Admin Center, um Informationen über die Anzahl der von Ihren DLP-Richtlinien erkannten Nachrichten anzuzeigen. DLP-Berichte bieten Einblicke in Richtlinien- und Regelüberstimmungen für gesendete und empfangene E-Mails. Sie können auch die Anzahl der Übereinstimmungen, Außerkraftsetzungen und falsch positiven Ergebnisse für jede Richtlinie innerhalb der letzten 24 Stunden im Exchange Admin Center anzeigen. Wenn Sie einen Excel Bericht herunterladen, können Sie noch mehr Details anzeigen, z. B. wer welche Nachricht gesendet hat, an welchem Tag und welche Richtlinienübersprechung ausgelöst wurden. Weitere Informationen finden Sie unter [Anzeigen von Berichten über DLP-Richtlinienerkennungen.](/previous-versions/exchange-server/exchange-150/jj889415(v=exchg.150))

## <a name="auditing-in-yammer-enterprise"></a>Überwachung in Yammer Enterprise

Yammer Enterprise bietet Administratoren die Möglichkeit, Benutzeraktivitätsdaten aus ihrem Yammer Netzwerk über die [Yammer Datenexport-API](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)oder manuell über die Yammer Netzwerkadministratorseite zu exportieren. Die Möglichkeit zum Exportieren von Protokollen ist auf Netzwerkadministratoren in Yammer beschränkt. (Alle Microsoft 365 globalen Administratoren sind Yammer Netzwerkadministratoren.)

Die folgenden Daten können exportiert werden:

| Filename | Beschreibung |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | Alle neuen, ausstehenden und angehaltenen Benutzer im Netzwerk |
| Messages.csv | Alle Nachrichten im Netzwerk |
| Files.csv (Metadaten) | Metadaten wie Dateiname, Datei-API-URL, Uploader-ID, hochgeladen bei usw. |
| Files.csv (Originaldateien) | ZIP-Datei der ursprünglichen Dateien, die von Benutzern in Yammer hochgeladen wurden |
| Topics.csv | Im Netzwerk erstellte Themen |
| Pages.csv | Von Benutzern im Netzwerk erstellte Seiten (Notizen) |
| Admins.csv | Alle bestätigten Administratoren im Netzwerk |
| Networks.csv | Alle Yammer externen Netzwerke |

Yammer Enterprise Daten sind auch über die Microsoft 365 Aktivitätsberichte verfügbar. Darüber hinaus arbeitet Yammer aktiv daran, zusätzliche Protokollierung über die Microsoft 365-Verwaltungsaktivitäts-API verfügbar zu machen, und an der Möglichkeit, über Daten mithilfe von Power BI zu ermitteln. Weitere Informationen zu diesen Features finden Sie in der [roadmap für Office.](https://fasttrack.microsoft.com/roadmap?filters=yammer)
