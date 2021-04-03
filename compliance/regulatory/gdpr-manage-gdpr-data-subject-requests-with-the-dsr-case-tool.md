---
title: Verwalten von Anträgen von DSGVO-Datensubjekten mit dem DSR-Falltool im Security & Compliance Center
description: Erfahren Sie, wie Sie Anträge von Datensubjekten der EU-Datenschutz-Grundverordnung (DSGVO) mit dem DSR-Falltool verwalten.
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
- MS-Compliance
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: f89faf915e31e375674020fda1fe56fe7cd78410
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496060"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-security--compliance-center"></a>Verwalten von DSGVO-Anfragen für Subjekte mit dem DSR-Falltool im Security & Compliance Center

In der EU-Datenschutz-Grundverordnung (DSGVO) geht es um den Schutz und die Aktivierung der Datenschutzrechte von Einzelpersonen innerhalb der Europäischen Union (EU). Die DSGVO gewährt Einzelpersonen in der Europäischen Union (auch als betroffene Personen bezeichnet) das Recht auf Zugriff, Abruf, Korrektur, Löschung und Einschränkung der Verarbeitung ihrer personenbezogenen Daten. Gemäß der DSGVO sind personenbezogene Daten alle Informationen im Zusammenhang mit einer identifizierten oder identifizierbaren natürlichen Person. Ein formeller Antrag einer Person an ihre Organisation, eine Aktion für ihre personenbezogenen Daten zu ergreifen, wird als Antrag der betroffenen Person oder DSR bezeichnet. Ausführliche Informationen zum Antworten auf Antragssubjekte für Daten in Office 365 finden Sie unter [Office 365 Data Subject Request Guide](https://go.microsoft.com/fwlink/?linkid=871169 ).
  
Zum Verwalten von Untersuchungen als Reaktion auf eine von einer Person in Ihrer Organisation übermittelte Antragsbeantwortung können Sie das DSR-Falltool im Security & Compliance Center verwenden, um inhalte zu finden, die in:
  
- Jedes Benutzerpostfach in Ihrer Organisation. Dazu gehören Skype for Business-Unterhaltungen und 1:1-Chats in Microsoft Teams
    
- Alle Postfächer, die einer Microsoft 365-Gruppe zugeordnet sind, und alle Teampostfächer in Microsoft Teams
    
- Alle SharePoint Online-Websites und OneDrive for Business-Konten in Ihrer Organisation
    
- Alle Teams-Websites und Microsoft 365-Gruppenwebsites in Ihrer Organisation
    
- Alle öffentlichen Ordner in Exchange Online
    
Mit dem DSR-Falltool können Sie:
  
- Erstellen Sie einen separaten Fall für jede Untersuchung eines Antrags einer betroffenen Person.
    
- Steuern, wer Zugriff auf den Fall DSR hat, indem Sie Personen als Mitglieder des Falls hinzufügen; Nur Mitglieder können auf den Fall zugreifen und ihre Fälle nur in der Liste der Fälle auf der Seite **DSR-Fälle** im Security & Compliance Center anzeigen. Darüber hinaus können Sie verschiedenen Mitgliedern desselben Falls unterschiedliche Berechtigungen zuweisen. Sie können beispielsweise einigen Mitgliedern erlauben, nur den Fall und die Suchergebnisse anzeigen und anderen Mitgliedern das Erstellen von Such- und Exportergebnissen zu ermöglichen. 
    
- Verwenden Sie die integrierte Suche, um nach allen Inhalten zu suchen, die von einer bestimmten Person erstellt oder hochgeladen wurden.
    
- Überarbeiten Sie optional die integrierte Suchabfrage, und führen Sie die Suche erneut aus, um die Suchergebnisse zu einenten.
    
- Fügen Sie weitere Inhaltssuchen hinzu, die dem Fall DSR zugeordnet sind. Dazu gehört das Erstellen von Suchen, die teilweise indizierte Elemente und vom System generierte Protokolle aus dem Office-Roamingdienst zurückgeben.
    
- Exportieren Sie Daten als Reaktion auf eine Zugriffs- oder Exportanforderung der DSR.
    
- Löschen Sie Fälle, wenn die Untersuchung eines Antrags einer betroffenen Person abgeschlossen wurde. Dadurch werden alle Such- und Exportaufträge entfernt, die dem Fall zugeordnet sind.
    
Hier sehen Sie den prozess auf hoher Ebene für die Verwendung des DSR-Falltools zum Verwalten von DSR-Untersuchungen:
  
[Step 1: Assign eDiscovery permissions to potential case members](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Schritt 2: Erstellen eines DSR-Falls und Hinzufügen von Mitgliedern](#step-2-create-a-dsr-case-and-add-members)

[Schritt 3: Ausführen der Suchabfrage](#step-3-run-the-search-query)

[Schritt 4: Exportieren der Daten](#step-4-export-the-data)

[(Optional) Schritt 5: Überarbeiten der integrierten Suchabfrage](#optional-step-5-revise-the-built-in-search-query)

[Weitere Informationen zur Verwendung des DSR-Falltools](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> Unsere Tools können Administratoren dabei unterstützen, Zugriffs- oder Exportanforderungen von Anträgen auf anträgesverdingte Benutzer durchzuführen, indem sie die integrierte Such- und Exportfunktionalität des DSR-Falltools nutzen können. Das Tool trägt dazu bei, eine best-effort-Methode zum Exportieren von Daten zu erleichtern, die für eine antragsrelevante Anforderung einer betroffenen Person relevant sind. Es ist jedoch wichtig zu beachten, dass die Suchergebnisse je nach betroffener Person oder den ausgeführten Administratoraktionen variieren können, die sich darauf auswirken können, ob ein Element zu Exportzwecken als "personenbezogene Daten" betrachtet wird. Wenn die betroffene Person beispielsweise die letzte Person war, die eine Datei geändert hat, die sie nicht erstellt hat, wird die Datei möglicherweise nicht in den Suchergebnissen zurückgegeben. Ebenso könnte ein Administrator Daten exportieren, ohne teilweise indizierte Elemente oder alle Versionen von SharePoint-Dokumenten zu enthalten. Daher können die bereitgestellten Tools dazu beitragen, den Zugriff auf Datenanforderungen und den Export zu erleichtern. Die Ergebnisse unterliegen jedoch bestimmten Verwendungsszenarien für Administratoren und Datensubjekte. 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Schritt 1: Zuweisen von eDiscovery-Berechtigungen zu potenziellen Fallmitgliedern

Standardmäßig kann ein globaler Administrator auf das DSR-Falltool im Security & Compliance Center zugreifen. Andere Benutzer, z. B. ein Datenschutzbeauftragter, ein Personalmanager oder andere Personen, die an DSR-Untersuchungen beteiligt sind, haben keinen Zugriff auf das DSR-Falltool und müssen über die entsprechenden Berechtigungen für den Zugriff auf das Tool verfügen. Am einfachsten können Sie dazu  im Security & Compliance Center zur Seite Berechtigungen wechseln und der Rollengruppe eDiscovery Manager Benutzer hinzufügen. Sie müssen diese Berechtigungen auch zuweisen, damit Sie sie als Mitglieder des Fall "DSR" hinzufügen können, den Sie in Schritt 2 erstellen. 
  
Schrittweise Anweisungen finden Sie unter [Assign eDiscovery permissions in the Office 365 Security & Compliance Center](/microsoft-365/compliance/assign-ediscovery-permissions).
  
> [!NOTE]
> Standardmäßig verfügt ein globaler Administrator (oder andere Mitglieder der Rollengruppe Organisationsverwaltung im Security & Compliance Center) nicht über die erforderlichen Berechtigungen zum Exportieren von Inhaltssuchergebnissen (siehe Schritt 4 in diesem Artikel). Um dies zu adressieren, kann sich ein Administrator selbst als Mitglied der Rollengruppe eDiscovery-Manager hinzufügen. 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a>Schritt 2: Erstellen eines DSR-Falls und Hinzufügen von Mitgliedern

Im nächsten Schritt erstellen Sie einen Fall mit einer DSR. Wenn Sie einen Fall erstellen, können Sie die integrierte Suche starten oder den Fall erstellen, ohne die Suche zu starten. Im folgenden Verfahren werden Sie angewiesen, den Fall zu erstellen, ohne die Suche zu starten. Anschließend wird gezeigt, wie Sie dem Fall Mitglieder hinzufügen.
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Arbeits- oder Schulkonto an. 
    
2. Klicken Sie & Security & Compliance  Center auf DatenschutzAnforderungen von Datensubjekten, und klicken Sie dann auf Symbol \> Hinzufügen ![ Neuer ](../media/ITPro-EAC-AddIcon.gif) **Fall** für datenschutzsubjekte .
    
3. Geben Sie auf der Seite Flyout für neue **DSR-Fälle** dem Fall einen Namen ein, geben Sie eine optionale Beschreibung ein, und klicken Sie dann auf **Weiter**. Der Name des Falls muss in Ihrer Organisation eindeutig sein.
    
    > [!TIP]
    > Erwägen Sie das Hinzufügen des Namens der Person, die die Antragserfordererung übermittelt hat, die Sie untersuchen, im Namen und/oder der Beschreibung des neuen Falls. Beachten Sie, dass nur Mitglieder dieses Falls (und eDiscovery-Administratoren) den Fall in der Liste der Fälle auf der Seite Anfragen von **Datensubjekten sehen** können. 
  
4. Wählen Sie **auf** der Seite Details anfordern unter Betroffene (die Person, die diese Anforderung eingereicht **hat)** die Person aus, für die Sie Daten suchen und exportieren möchten, und klicken Sie dann auf **Weiter**.
    
5. Auf der **Seite Falleinstellungen bestätigen** können Sie den Fallnamen und die Beschreibung ändern und eine andere Person auswählen. Klicken Sie andernfalls auf **Speichern**.
    
    Es wird eine Seite angezeigt, auf der bestätigt wird, dass der neue Fall "DSR" erstellt wurde.
    
    ![Starten Sie die Suche, oder schließen Sie die Seite Neue DSR-Fallseite.](../media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    An dieser Stelle können Sie eine der beiden Dinge tun:
    
    a. Wenn Sie auf **Suchergebnisse anzeigen klicken, wird** die Suche gestartet. Dies ist die Standardauswahl. Die integrierte Suche, die ausgeführt wird, wenn Sie diese Option auswählen, und die zurückgegebenen Ergebnisse werden in Schritt 3 erläutert.
    
    b. Wenn Sie **auf Fertig** stellen klicken, wird der neue Fall "DSR" geschlossen, ohne die integrierte Suche zu starten. Wenn Sie diese Option auswählen, wird der neue Fall für anträgessubjekte auf der Seite Anfragen von **Datensubjekten** angezeigt.
    
6. Klicken **Sie auf Fertig** stellen, damit Sie zum neuen Fall DSR wechseln und mitglieder hinzufügen können. 
    
7. Klicken Sie **auf der Seite** Anforderungen von Datensubjekten auf den Namen des von Ihnen erstellten Antrags auf Antragsersuchen. 
    
8. Klicken Sie **auf der Seite** Flyout für diesen Fall verwalten unter Mitglieder **verwalten** auf **Hinzufügen**. 
    
    Unter **Benutzer** wird eine Liste der Personen angezeigt, denen die entsprechenden eDiscovery-Berechtigungen zugewiesen sind. Die Personen, denen Sie in Schritt 1 eDiscovery-Berechtigungen zugewiesen haben, werden in dieser Liste angezeigt. 
    
9. Wählen Sie die Personen aus, die als Mitglieder des DSR-Falls hinzugefügt werden, klicken Sie auf **Hinzufügen**, und speichern Sie dann Ihre Änderungen.
    
    Sie können Rollengruppen auch als Mitglieder des Fall  DSR hinzufügen, indem Sie unter **Verwalten von Rollengruppen auf** Hinzufügen klicken. 
    
## <a name="step-3-run-the-search-query"></a>Schritt 3: Ausführen der Suchabfrage

Nachdem Sie einen Fall für den Fall "DSR" erstellt und Mitglieder hinzugefügt haben, besteht der nächste Schritt in der Ausführung der integrierten Suche, die dem Fall zugeordnet ist. Diese Standardsuchabfrage führt die folgenden Aufgaben aus:
  
- Durchsucht alle Postfächer in Ihrer Organisation nach allen E-Mail-Elementen, die von der person person gesendet oder empfangen wurden. Dies erfolgt mithilfe der Participants-E-Mail-Eigenschaft, die in allen Personenfeldern in einer E-Mail-Nachricht nach der Person sucht.  Diese Eigenschaft gibt Elemente zurück, in denen sich die Person in den Feldern **From,** **To,** **CC** und **BCC** befindet. Öffentliche Ordner in Exchange Online werden auch nach Nachrichten durchsucht, die von der person person gesendet oder empfangen wurden. 
    
- Durchsucht alle Websites in Ihrer Organisation nach Dokumenten und Elementen, die von der person person erstellt oder hochgeladen wurden. Dazu verwenden Sie die folgenden Websiteeigenschaften:
    
  - Die  *Author-Eigenschaft*  gibt Elemente zurück, bei denen die person im Feld Autor in Office-Dokumenten aufgeführt ist. Dieser Wert bleibt erhalten, auch wenn das Dokument von einer anderen Person kopiert und hochgeladen wird. 
    
  - Die  *CreatedBy-Eigenschaft*  gibt Elemente zurück, die von der person person erstellt oder hochgeladen wurden. 
    
So sieht die Stichwortabfrage für die integrierte Suche aus, die automatisch erstellt wird, wenn Sie einen Fall mit einer NSR erstellen.
  
```powershell
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

Wenn der Name der person person beispielsweise Ina Leonte ist, sieht die Schlüsselwortabfrage wie die folgende aus:
  
```powershell
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 **So führen Sie die integrierte Suche nach einem Fall mit einer DSR aus:**
  
1. Klicken Sie & Security &  Compliance Center auf DatenschutzDatensubjektanforderungen, und klicken Sie dann neben dem Fall \> DSR, den Sie in Schritt 2 erstellt haben, auf Öffnen.  
    
    Klicken Sie **oben** auf der Seite auf die Registerkarte Suchen, und klicken Sie dann auf das Kontrollkästchen neben der integrierten Suche, die beim Erstellen des DSR-Falls erstellt wurde. Die Suche hat denselben Namen wie der Fall DSR. 
    
2. Klicken Sie auf der Seite Suchf flyout auf **Abfrage öffnen**.
    
    Wenn Sie die Abfrage öffnen, wird die Suche gestartet und in wenigen Momenten abgeschlossen. 
    
3. Klicken Sie nach Abschluss der Suche auf **Ergebnisse anzeigen,** um eine Vorschau der Suchergebnisse anzuzeigen. Weitere Informationen finden Sie unter [Vorschau der Suchergebnisse](/microsoft-365/compliance/content-search#preview-search-results).
    
    > [!TIP]
    > Sie können auch die Suchabfragestatistiken anzeigen, um die Anzahl der Postfach- und Websiteelemente anzuzeigen, die von der Suche zurückgegeben werden, sowie die obersten Inhaltsspeicherorte, die Elemente enthalten, die mit der Suchabfrage übereinstimmen. Weitere Informationen finden Sie unter [Anzeigen von Informationen und Statistiken zu einer Suche](/microsoft-365/compliance/content-search#view-information-and-statistics-about-a-search). 
  
Sie können die integrierte Suchabfrage bearbeiten, die durchsuchten Inhaltsorte ändern und dann die Suche erneut ausführen. Weitere Informationen finden Sie unter Schritt [5.](#optional-step-5-revise-the-built-in-search-query) 
  
## <a name="step-4-export-the-data"></a>Schritt 4: Exportieren der Daten

Nachdem Sie die integrierte Suche ausgeführt haben, können Sie die Suchergebnisse exportieren. Alternativ können Sie die Abfrage vor dem Exportieren der Daten überarbeiten, um die Anzahl der Suchergebnisse zu reduzieren. Weitere Informationen zum Einen der Suchergebnisse finden Sie unter Schritt 5.
  
Wenn Sie Suchergebnisse exportieren, können Postfachelemente in PST-Dateien oder als einzelne Nachrichten heruntergeladen werden. Wenn Sie Inhalte aus SharePoint- und #A0 exportieren, werden Kopien systemeigener #A1 und anderer Dokumente exportiert. In den Suchergebnissen ist eine Ergebnisdatei enthalten, die Informationen zu jedem exportierten Element enthält. Ausführlichere Informationen zum Exportieren finden Sie unter [Exportieren von Inhaltssuchergebnissen](/microsoft-365/compliance/export-search-results).
  
> [!NOTE]
> Standardmäßig verfügt ein globaler Administrator (oder andere Mitglieder der Rollengruppe Organisationsverwaltung im Security & Compliance Center) nicht über die erforderlichen Berechtigungen zum Exportieren von Inhaltssuchergebnissen. Um dies zu adressieren, kann sich ein Administrator selbst als Mitglied der Rollengruppe eDiscovery-Manager hinzufügen. 
  
Der Computer, den Sie zum Exportieren von Daten verwenden, muss die folgenden Systemanforderungen erfüllen:
  
- 32-Bit- oder 64-Bit-Versionen von Windows 7 und höher
    
- Microsoft .NET Framework 4.7
    
- Einen unterstützten Browser:
    
  - Microsoft Edge
    
    Oder
    
  - Microsoft Internet Explorer 10 und höher
    
    > [!NOTE]
    > Microsoft stellt keine Drittanbietererweiterungen oder -add-ons für ClickOnce her. Das Exportieren von Daten mithilfe eines nicht unterstützten Browsers mit Drittanbietererweiterungen oder -add-ons wird nicht unterstützt. 
  
 **So exportieren Sie Daten aus der integrierten Suche in einem Fall mit DSR:**
  
1. Klicken Sie & Security & Compliance  Center auf DatenschutzAnforderungen von Datensubjekten, und klicken Sie dann neben dem Fall \> DSR, aus dem Sie Daten exportieren möchten, auf Öffnen.  
    
2. Klicken Sie **oben** auf der Seite auf die Registerkarte Suchen, und klicken Sie dann auf das Kontrollkästchen neben der integrierten Suche, die beim Erstellen des DSR-Falls erstellt wurde. Oder klicken Sie auf eine andere Suche, um Daten aus dieser Suche zu exportieren. 
    
3. Klicken Sie auf der Seite Suchf flyout auf Suchergebnisse exportieren (Symbol Weitere ), und wählen Sie dann Ergebnisse exportieren ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) in der Dropdownliste aus.  
    
4. Wählen Sie **auf der** Seite Ergebnisse exportieren die folgenden empfohlenen Optionen für DSR-Exportanforderungen aus. 
    
    ![Konfigurieren der Exporteinstellungen](../media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    a. Wählen Sie unter Ausgabeoptionen die erste Option (**Alle Elemente,** ausgenommen diejenigen, die über ein nicht unbekanntes Format verfügen, verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden), um nur indizierte Elemente zu exportieren. Der Grund, warum Sie nicht teilweise indizierte Elemente aus der integrierten Suche exportieren möchten, liegt daran, dass teilweise indizierte Elemente von anderen Benutzern ebenfalls exportiert werden. Um nur die teilweise indizierten Elemente für die person person zu exportieren, wird empfohlen, eine separate Suche zu erstellen. Weitere Informationen finden Sie unter Exportieren teilweise [indizierter](#exporting-partially-indexed-items) Elemente im Abschnitt "Weitere Informationen zur Verwendung des DSR-Falltools".
    
    b. Wählen **Sie unter Exportieren von Exchange-Inhalten als** die dritte Option aus, eine PST-Datei, die alle Nachrichten in einem **einzigen Ordner enthält.** Da einige der Ergebnisse für Elemente verwendet werden können, die aus dem Postfach eines anderen Benutzers stammen, listet diese Option das Element einfach in einem einzigen Ordner auf, ohne das tatsächliche Postfach anzuzeigen, und ist die beste Option, wenn Sie die Ergebnisse wie im nächsten Element empfohlen deduplizieren. Mit dieser Option kann die Person elemente auch in chronologischer Reihenfolge überprüfen (Elemente werden nach dem Gesendeten Datum sortiert), ohne in der ursprünglichen Postfachordnerstruktur für jedes Element navigieren zu müssen.
    
    c. Wählen **Sie Deduplizierung aktivieren** aus, um doppelte E-Mail-Nachrichten auszuschließen. Diese Option wird empfohlen, da bei der integrierten Suche alle Postfächer in Ihrer Organisation durchsucht werden. Wenn also mehrere Kopien derselben Nachricht in den durchsuchten Postfächern gefunden werden, bedeutet diese Option, dass nur eine Kopie einer Nachricht exportiert wird. Diese Option führt zusammen zum Exportieren von Nachrichten in einer PST-Datei in einem einzigen Ordner, was zu einer besten Benutzeroberfläche für DSR-Exportanforderungen führt. Im Results.csv Exportbericht werden alle Speicherorte aufgeführt, an denen doppelte Nachrichten gefunden wurden.
    
    Optional können Sie die Option Versionen **für #A0 enthalten** auswählen, um alle Versionen von SharePoint- und #A1 zu exportieren. Dies setzt voraus, dass die Versionsierung für Dokumentbibliotheken aktiviert ist. Diese Option trägt dazu bei, sicherzustellen, dass alle relevanten Daten exportiert werden.
    
5. Nachdem Sie die Exporteinstellungen festgelegt haben, klicken Sie auf **Exportieren**.
    
    Die Suchergebnisse werden zum Herunterladen vorbereitet, d. h. sie werden in den Azure Storage-Bereich für Ihre Organisation in der Microsoft Cloud hochgeladen. In den nächsten Schritten wird gezeigt, wie Sie diese Daten auf Ihren lokalen Computer herunterladen.
    
6. Klicken Sie auf die Registerkarte **Exportieren,** um den von Ihnen erstellten Exportauftrag anzeigen zu können. Exportaufträge haben denselben Namen wie  die entsprechende Suche mit _Export am Ende des Suchnamens angefügt. 
    
7. Klicken Sie auf den Exportauftrag, den Sie gerade erstellt haben, um die Exportf flyoutseite anzeigen zu können. Diese Seite enthält Informationen zur Suche, z. B. die Größe und Gesamtanzahl der zu exportierende Elemente und den Prozentsatz der Elemente, die in einen Azure-Speicherbereich übertragen wurden. Klicken **Sie auf Aktualisieren,** um die Uploadstatusinformationen zu aktualisieren. 
    
8. Klicken Sie unter **Schlüssel exportieren** auf **In Zwischenablage kopieren**. Sie verwenden diesen Schlüssel in Schritt 11, um die Suchergebnisse herunterzuladen.
    
9. Klicken Sie auf Suchergebnisse exportieren Symbol Ergebnisse herunterladen oben auf der ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)  Exportf flyout-Seite. 
    
10. Klicken Sie im Popupfenster am unteren Rand der Seite auf **Öffnen,** um das **eDiscovery-Exporttool zu öffnen.** Das **eDiscovery-Exporttool** wird beim ersten Herunterladen von Suchergebnissen installiert. 
    
11. Fügen Sie **im eDiscovery-Exporttool** den Exportschlüssel, den Sie in Schritt 8 kopiert haben, in das entsprechende Feld ein.
    
12. Klicken Sie auf **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen. 
    
    > [!NOTE]
    > Aufgrund der hohen Datenträgeraktivität (Lese- und Schreibvorgänge) sollten Sie Suchergebnisse auf ein lokales Datenträgerlaufwerk herunterladen. laden Sie sie nicht auf ein zugeordnetes Netzlaufwerk oder einen anderen Netzwerkspeicherort herunter. 
  
13. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Das **eDiscovery-Exporttool** zeigt Statusinformationen zum Exportvorgang an, einschließlich einer Schätzung der Anzahl (und Größe) der verbleibenden Elemente, die heruntergeladen werden sollen. Wenn der Exportvorgang abgeschlossen ist, können Sie auf die Dateien am Speicherort zugreifen, an dem sie heruntergeladen wurden. Weitere Informationen zu den Berichten, die beim Herunterladen [](/microsoft-365/compliance/export-search-results#more-information) von Inhaltssuchergebnissen enthalten waren, finden Sie im Abschnitt Weitere Informationen unter "Exportieren von Inhaltssuchergebnissen". 
    
Nachdem die Daten exportiert wurden, befinden sich die Suchergebnisse und Exportberichte in einem Ordner mit demselben Namen wie der Fall "DSR". Die PST-Dateien, die Postfachelemente enthalten, befinden sich in einem Unterordner namens **Exchange**. Dokumente und andere Elemente von Websites befinden sich in einem Unterordner namens **SharePoint**. 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a>(Optional) Schritt 5: Überarbeiten der integrierten Suchabfrage

Nachdem Sie die integrierte Suche ausgeführt haben, können Sie den Bereich so ändern, dass weniger Suchergebnisse angezeigt werden. Sie können dies tun, indem Sie der Abfrage Bedingungen hinzufügen. Eine Bedingung wird vom AND-Operator logisch mit der **Schlüsselwortabfrage** verbunden. Das bedeutet, dass Elemente in den Suchergebnissen zurückgegeben werden sollen und sowohl die Stichwortabfrage als auch alle von Ihnen hinzugefügten Bedingungen erfüllen müssen. Auf diese Weise helfen Bedingungen, die Ergebnisse zu einenten. Wenn Sie einer Suchabfrage zwei oder mehr eindeutige Bedingungen hinzufügen (Bedingungen, die unterschiedliche Eigenschaften angeben), werden diese Bedingungen logisch durch den **AND-Operator** verbunden. Das bedeutet, dass nur Elemente zurückgegeben werden, die alle Bedingungen (zusätzlich zur Schlüsselwortabfrage) erfüllen. Wenn Sie einer einzelnen Bedingung mehrere Werte (durch Kommas oder Semikolon getrennt) hinzufügen, werden diese Werte durch den **OR-Operator** verbunden. Das bedeutet, es werden Elemente zurückgegeben, die einen der angegebenen Werte für die Eigenschaft in der Bedingung enthalten. 
  
Im Folgenden finden Sie einige Beispiele für die Bedingungen, die Sie der integrierten Suchabfrage eines DSR-Falls hinzufügen können. Der Name der tatsächlichen Eigenschaft, die in einer Suchabfrage verwendet wird, wird in Klammern angezeigt.
  
- **Dateityp ( `filetype` )** – Gibt die Erweiterung eines Dokuments oder einer Datei an. Verwenden Sie diese Bedingung, um nach Dokumenten und Dateien zu suchen, die von bestimmten Office-Anwendungen wie Word, Excel und OneNote erstellt wurden. 
    
- **Nachrichtentyp ( `kind` )** – Gibt den Typ des E-Mail-Elements an, nach dem gesucht werden soll. Beispielsweise können Sie die Syntax verwenden, um nur E-Mail-Nachrichten und  `kind:email OR kind:im` Skype for #A0 oder 1:1-Chats in Microsoft Teams zurückzukehren. 
    
- **Compliancetag ( `compliancetag` )** – Gibt eine Bezeichnung an, die einer E-Mail-Nachricht oder einem Dokument zugewiesen ist. Diese Bedingung gibt Elemente zurück, die mit einer bestimmten Bezeichnung klassifiziert sind. Bezeichnungen werden verwendet, um E-Mails und Dokumente für die Datensteuerung zu klassifizieren und Aufbewahrungsregeln basierend auf der durch die Bezeichnung definierten Klassifizierung zu erzwingen. Dies ist eine nützliche Bedingung für DSR-Untersuchungen, da Ihre Organisation möglicherweise Bezeichnungen verwendet, um Inhalte im Zusammenhang mit dem Datenschutz zu klassifizieren oder die personenbezogene Daten oder vertrauliche Informationen enthalten. Verwenden Sie für den Wert dieser Bedingung den vollständigen Bezeichnungsnamen oder den ersten Teil des Bezeichnungsnamens mit einem Platzhalter. Weitere Informationen finden Sie [unter Informationen zu Aufbewahrungsrichtlinien und Aufbewahrungsbezeichnungen in Office 365](/microsoft-365/compliance/retention).
    
Eine Liste und Beschreibung aller im DSR-Falltool [](/microsoft-365/compliance/keyword-queries-and-search-conditions#search-conditions) verfügbaren Bedingungen finden Sie unter Suchbedingungen im Artikel "Schlüsselwortabfragen und Suchbedingungen für die Inhaltssuche". 
  
### <a name="changing-the-content-locations-that-are-searched"></a>Ändern der durchsuchten Inhaltsorte

Sie können nicht nur die integrierte Suche nach einem Fall mit einer DSR überdacht haben, sondern auch die durchsuchten Inhaltsorte ändern. Wie bereits erläutert, durchsucht die integrierte Suche jedes Postfach und jede Website in der Organisation sowie alle öffentlichen Exchange Online-Ordner. Beispielsweise könnten Sie die Suche so einendnen, dass nur das Postfach und das #A0 und ausgewählte #A1 durchsucht werden. Wenn Sie bestimmte Websites durchsuchen möchten, müssen Sie jede Website hinzufügen, die Sie durchsuchen möchten.
  
So ändern Sie die zu durchsuchende Inhaltsorte:
  
1. Öffnen Sie die integrierte Suche, für die Sie die Inhaltspositionen ändern möchten.
    
2. Klicken Sie in der Suchabfrage unter **Speicherorte** **neben** der Option Spezifische **Speicherorte auf** Ändern. 
    
    ![Klicken Sie auf Ändern, um die Inhaltspositionen der integrierten Suchabfrage zu ändern.](../media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    Die **Flyoutseite** Speicherorte ändern wird angezeigt. Hier finden Sie eine Beschreibung der Inhaltsorte in der integrierten Suche und einige Informationen zum Ändern der durchsuchten Speicherorte. 
    
    ![Ändern der Flyoutseite für Speicherorte](../media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    a. Die Umschalte **unter Alle** im Postfach auswählen am oberen Rand der Flyoutseite ist ausgewählt, was angibt, dass alle Postfächer durchsucht werden. Klicken Sie zum Einschnen des Suchbereichs auf die Umschalte, um die Auswahl zu deaktivieren, und klicken Sie dann auf **Benutzer, Gruppen** oder Teams auswählen, und wählen Sie bestimmte Zu durchsuchende Postfächer aus.
    
    b. Der Umschalter **unter Alle** auswählen im Abschnitt Websites in der Mitte der Flyoutseite ist ausgewählt, was angibt, dass alle Websites durchsucht werden. Wenn Sie die Suche auf ausgewählte Websites einenknen möchten, deaktivieren Sie die Umschaltflächen und klicken dann **auf Websites auswählen.** Sie müssen jede bestimmte Website hinzufügen, die Sie durchsuchen möchten, einschließlich des OneDrive-Kontos der Person.
    
    c. Der Umschalter im Abschnitt Öffentliche Exchange-Ordner ist ausgewählt, d. h. alle öffentlichen Exchange-Ordner werden durchsucht. Sie können nur alle öffentlichen Exchange-Ordner oder keine dieser Ordner durchsuchen. Sie können keine bestimmten suchen.
    
3. Wenn Sie die Inhaltspositionen in der integrierten Suche ändern, klicken Sie auf **Ausführen &amp; speichern,** um die Suche neu zu starten. 

> [!NOTE]
> Wenn Sie alle Postfachspeicherorte oder nur bestimmte Postfächer durchsuchen, werden Daten aus anderen Office 365-Anwendungen, die in Benutzerpostfächern gespeichert sind, einbezogen, wenn Sie die Ergebnisse der Suche exportieren. Diese Daten werden nicht in die geschätzten Suchergebnisse einbezogen und sind für die Vorschau nicht verfügbar. Sie ist jedoch enthalten, wenn Sie die Suchergebnisse exportieren und herunterladen. Weitere Informationen zu Anwendungen, die Daten im Postfach eines Benutzers speichern, finden Sie unter [Inhalt, der in Exchange Online-Postfächern gespeichert ist.](/microsoft-365/compliance/what-is-stored-in-exo-mailbox)
  
## <a name="more-information-about-using-the-dsr-case-tool"></a>Weitere Informationen zur Verwendung des DSR-Falltools

Die folgenden Abschnitte enthalten weitere Informationen zur Verwendung des DSR-Falltools, um auf DSR-Exportanforderungen zu reagieren.
  
[Exportieren von Daten aus dem Office-Roamingdienst](#exporting-data-from-the-office-roaming-service)

[Exportieren teilweise indizierter Elemente](#exporting-partially-indexed-items)

[Suchen und Exportieren von Daten aus Microsoft Teams und Microsoft 365-Gruppen](#searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups)

[Durchsuchen öffentlicher Exchange-Ordner](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-the-office-roaming-service"></a>Exportieren von Daten aus dem Office-Roamingdienst

Sie können das DSR-Falltool verwenden, um Nutzungsdaten zu suchen und zu exportieren, die vom Office-Roamingdienst generiert werden. Roaming ist ein Dienst, der Office-bezogene Einstellungen speichert, z. B. Office-Design, benutzerdefiniertes Wörterbuch, Spracheinstellungen, Entwicklermodus und automatische Korrektur. 
    
Die Daten des Office-Roamingdiensts werden im Postfach einer Person in einem ausgeblendeten Ordner gespeichert, der sich in einer Nicht-INTERM-Unterstruktur (Non-IPM) von Exchange Online-Postfächern befindet. Dies bedeutet, dass die Daten aus der Benutzeransicht ausgeblendet werden, wenn sie Outlook oder andere E-Mail-Clients für den Zugriff auf ihr Postfach verwenden. Weitere Informationen zu ausgeblendeten Ordnern finden Sie unter [MAPI Hidden Folders](https://go.microsoft.com/fwlink/?linkid=872758).
  
Sie können eine separate Inhaltssuche erstellen (und sie einem Fall mit einer DSR zuordnen), die die Verwendungsdaten des Office-Roamingdiensts im Postfach der Person zurückgibt. Diese Daten sind nicht in der Suchstatistik enthalten und stehen nicht für die Vorschau zur Verfügung. Sie können sie jedoch exportieren und dann als Antwort auf eine DSR-Exportanforderung an die person subjektorientierte Person senden.
  
Wenn Sie Daten aus dem Office-Roamingdienst exportieren, werden die Daten in einem separaten Ordner gespeichert, der sich im **Ordner ApplicationDataRoot** befindet, der sich unter einem Ordner befindet, der den Namen mit der E-Mail-Adresse der Person hat. Diese Daten werden als JSON-Dateien exportiert, bei denen es sich um lesbare Textdateien handelt, die XML- oder TXT-Dateien ähneln und an E-Mail-Nachrichten angefügt sind. Derzeit wird dieser Ordner mit der GUID (Globally Unique Identifier) benannt: **1caee58f-eb14-4a6b-9339-1fe2ddf6692b**. In zukünftigen Versionen des DSR-Falltools wird die GUID durch den Namen der tatsächlichen Anwendung ersetzt. 

   
 **So suchen und exportieren Sie Office Roaming Service-Daten:**
  
1. Klicken Sie & Security &  Compliance Center auf DatenschutzDatensubjektanforderungen, und klicken Sie dann auf Öffnen neben dem Fall DSR für die Person, für die Sie Nutzungsdaten exportieren \> möchten.  
    
2. Klicken Sie **oben** auf der Seite auf die Registerkarte Suchen, und klicken Sie dann auf ![ ](../media/ITPro-EAC-AddIcon.gif) **Symbolgesteuerte Suche hinzufügen.**
    
3. Klicken **Sie auf** der **Suchseite Name auf** Abbrechen. 
    
4. Aktivieren **Sie unter Suchabfrage** in der **Type-Bedingung** das Kontrollkästchen neben **Office Roaming Service**. 
    
    ![Aktivieren Sie das Kontrollkästchen Office-Roamingdienst, um Verwendungsdaten zu exportieren.](../media/O365_DSRCase_SDSDataExport1.png)
  
    Die **Type-Bedingung** (bei denen es sich um E-Mail-Nachrichtenklassen handelt) sollte das einzige Element in der Suchabfrage sein. Sie können das Feld **Schlüsselwörter** löschen oder leer lassen. 
    
5. Stellen **Sie unter Speicherorte** sicher, dass **bestimmte** Speicherorte ausgewählt sind, und klicken Sie dann auf **Ändern**.
    
6. Klicken Sie oben auf **der** Flyoutseite Speicherorte ändern (Abschnitt Postfach) auf **Benutzer, Gruppen oder Teams auswählen.**
    
7. Klicken Sie **auf** der Seite Speicherorte bearbeiten auf **Benutzer, Gruppen** oder Teams auswählen, wählen Sie das Postfach der Person aus, und speichern Sie dann Ihre Auswahl. 
    
8. Klicken **Sie auf & ausführen**, und benennen Sie die Suche, und speichern Sie sie.
    
    Die Suche wird gestartet.
    
 **So exportieren Sie Office Roaming Service-Daten:**
  
1. Wenn die im vorherigen Schritt erstellte Suche  abgeschlossen ist, klicken Sie oben auf der Seite auf die Registerkarte Suchen, und klicken Sie dann auf das Kontrollkästchen neben der Suche. Möglicherweise müssen Sie auf ![ Aktualisieren ](../media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **aktualisieren klicken,** um die Suche anzeigen zu können. 
    
2. Klicken Sie auf der Seite Suchf flyout auf Suchergebnisse exportieren (Symbol Weitere ), und wählen Sie dann Ergebnisse exportieren ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) in der Dropdownliste aus.  
    
3. Wählen Sie **auf der Seite** Ergebnisse exportieren die empfohlenen Optionen zum Exportieren von Verwendungsdaten aus. 
    
    ![Exportoptionen beim Exportieren von Verwendungsdaten des Office-Roamingdiensts](../media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    a. Wählen Sie unter Ausgabeoptionen die erste Option (**Alle Elemente,** ausgenommen diejenigen, die über ein nicht unbekanntes Format verfügen, verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden), um nur indizierte Elemente zu exportieren.
    
    b. Wählen **Sie unter Exportieren von Exchange-Inhalten als** die zweite Option, eine **PST-Datei mit allen Nachrichten aus.**
    
    c. Lassen Sie die restlichen Exportoptionen deaktiviert.
    
4. Nachdem Sie die Exporteinstellungen festgelegt haben, klicken Sie auf **Exportieren**.
    
    Die Suchergebnisse werden zum Herunterladen vorbereitet, d. h. sie werden in den Azure-Speicherbereich für Ihre Organisation in der Microsoft Cloud hochgeladen. In den nächsten Schritten wird gezeigt, wie Sie diese Daten auf Ihren lokalen Computer herunterladen.
    
5. Klicken Sie auf die Registerkarte **Exportieren,** um den von Ihnen erstellten Exportauftrag anzeigen zu können. Die Exportaufträge haben denselben Namen wie die entsprechende Suche **mit _Export** am Ende des Suchnamens angefügt. 
    
6. Klicken Sie auf den Exportauftrag, den Sie gerade erstellt haben, um die Exportf flyoutseite anzeigen zu können. 
    
7. Klicken Sie unter **Schlüssel exportieren** auf **In Zwischenablage kopieren**. Sie verwenden diesen Schlüssel in Schritt 10, um die Suchergebnisse herunterzuladen.
    
8. Klicken Sie auf Suchergebnisse exportieren Symbol Ergebnisse herunterladen oben auf der ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)  Exportf flyout-Seite. 
    
9. Klicken Sie im Popupfenster am unteren Rand der Seite auf **Öffnen,** um das **eDiscovery-Exporttool zu öffnen.** Das **eDiscovery-Exporttool** wird beim ersten Herunterladen von Suchergebnissen installiert. 
    
10. Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 7 kopiert haben, in das entsprechende Feld ein.
    
11. Klicken Sie auf **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen. 
    
    > [!NOTE]
    > Aufgrund der hohen Datenträgeraktivität (Lese- und Schreibvorgänge) sollten Sie Suchergebnisse auf ein lokales Datenträgerlaufwerk herunterladen. laden Sie sie nicht auf ein zugeordnetes Netzlaufwerk oder einen anderen Netzwerkspeicherort herunter. 
  
12. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Das **eDiscovery-Exporttool** zeigt Statusinformationen zum Exportvorgang an, einschließlich einer Schätzung der Anzahl (und Größe) der verbleibenden Elemente, die heruntergeladen werden sollen. Wenn der Exportvorgang abgeschlossen ist, können Sie die Exchange-PST-Datei in Outlook öffnen und dann zum **Ordner ApplicationDataRoot** wechseln, um auf den Unterordner für den Roamingdienst zu zugreifen. 
    
    Wie bereits erläutert, werden die JSON-Dateien, die Verwendungsdaten enthalten, an Nachrichten angefügt. Klicken Sie zum Anzeigen einer JSON-Datei auf eine Nachricht, und öffnen Sie dann die angefügte JSON-Datei. 
  
### <a name="exporting-partially-indexed-items"></a>Exportieren teilweise indizierter Elemente

Es wird empfohlen, nicht teilweise indizierte Elemente (auch als nicht indizierte Elemente bezeichnet) aus der integrierten Suche zu exportieren, die erstellt wird, wenn Sie einen DSR-Fall erstellen. Der Grund dafür ist, dass die Suchergebnisse wahrscheinlich nur teilweise indizierte Elemente für andere Benutzer in Ihrer Organisation und nicht nur teilweise indizierte Elemente für die personbehinderte Person enthalten. Stattdessen wird empfohlen, eine separate Inhaltssuche zu erstellen, die dem Fall DSR zugeordnet ist, der nur die teilweise indizierten Elemente exportiert, die sich auf die personbezogene Person bezogen. 
  
Hier ist ein Prozess auf hoher Ebene zum Exportieren teilweise indizierter Elemente. Nachdem sie exportiert wurden, können Sie sie überprüfen, um zu ermitteln, ob ein Element auf eine Zugriffs- oder Exportanforderung von DSR reagiert.
  
1. Öffnen Sie den Fall DSR, und erstellen Sie eine Suche auf der **Seite** Suchen. 
    
2. Verwenden Sie die folgenden Kriterien zum Konfigurieren der Suchabfrage und der zu durchsuchenden Inhaltsstandorte:
    
    - Verwenden Sie eine leere/leere Schlüsselwortabfrage. Dadurch werden alle Elemente in den durchsuchten Inhaltspositionen zurückgegeben.
    
    - Durchsuchen Sie nur das Exchange #A0 der Person und ihr OneDrive-Konto.
    
3. Nachdem Sie die Suche ausgeführt und abgeschlossen haben, können Sie die Suchergebnisse exportieren und herunterladen (wie in [Schritt 4 beschrieben).](#step-4-export-the-data) Verwenden Sie die folgenden Einstellungen, um teilweise indizierte Elemente zu exportieren. 
    
    - Wählen **Sie** unter Ausgabeoptionen die dritte Option aus ( Nur Elemente, die ein nicht unbekanntes Format **haben,** verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden), um nur teilweise indizierte Elemente zu exportieren.
    
    - Unter **Exportieren von Exchange-Inhalten als** können Sie eine beliebige Option basierend auf Ihren Einstellungen auswählen. 
    
    - Wenn Sie die **Option Versionen für SharePoint-Dokumente enthalten** auswählen, werden Versionen von Dokumenten exportiert, wenn eine Version teilweise indiziert ist. 
    
Weitere Informationen zu teilweise indizierten Elementen finden Sie unter: 
  
- [Teilweise indizierte Elemente in der Inhaltssuche in Office 365](/microsoft-365/compliance/partially-indexed-items-in-content-search)

- [Exportieren teilweise indizierter Elemente](/microsoft-365/compliance/export-search-results#exporting-partially-indexed-items)

### <a name="searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups"></a>Suchen und Exportieren von Daten aus Microsoft Teams und Microsoft 365-Gruppen

Unterhaltungen, die Teil der Chatliste in Microsoft Teams sind (als Teamchats oder 1:1-Chats bezeichnet), werden im Exchange Online-Postfach der Benutzer gespeichert, die an den Chats teilnehmen. Außerdem werden die Dateien, die eine Person in einem 1:1-Chat teilt, im #A0 der Person gespeichert, die die Datei teilt. Da bei der integrierten Suche alle Postfächer und #A0 in der Organisation durchsucht werden, werden Teamchats und Dokumente, die in einer Chatsitzung freigegeben wurden (die von der person erstellt oder hochgeladen wurden) von der integrierten Suche in einem #A1 zurückgegeben.
  
Alternativ werden Unterhaltungen, die Teil eines Teams-Kanals (auch Kanalnachrichten genannt) sind, im Postfach gespeichert, das einem Team zugeordnet ist. Diese Arten von Unterhaltungen, an der die person subjektierte Person teilgenommen hat, werden auch von der integrierten Suche zurückgegeben, da alle Postfächer durchsucht werden, die Teams zugeordnet sind. Darüber hinaus werden Dateien, die von einer person person in einem Teams-Kanal gemeinsam verwendet werden, auf der SharePoint-Website des Teams gespeichert. Von der person person erstellte oder hochgeladene Dateien werden von der integrierten Suche in einem Fall mit datenschutzersuchen zurückgegeben, da die Websites, die Teams zugeordnet sind, in die Suche einbezogen werden.
  
Ebenso sind Postfächer und SharePoint-Websites, die einer Microsoft 365-Gruppe entsprechen, auch in die integrierte Suche einbezogen. Dies bedeutet, dass von der Person gesendete oder empfangene E-Mail-Nachrichten und von der person erstellten oder hochgeladenen Dateien zurückgegeben werden. 
  
Weitere Informationen zur Verwendung der Inhaltssuche zum Suchen nach Elementen in Microsoft Teams und Microsoft 365-Gruppen oder zum Erhalten einer Liste von Mitgliedern finden Sie im Abschnitt "Durchsuchen von Microsoft Teams und Microsoft 365-Gruppen" in der Inhaltssuche [in Microsoft 365](/microsoft-365/compliance/content-search#searching-microsoft-teams-and-microsoft-365-groups). 
  
### <a name="searching-exchange-public-folders"></a>Durchsuchen öffentlicher Exchange-Ordner

Bei der integrierten Suche in einem Fall mit DSR werden nur E-Mail-Nachrichten von der person gesendet, die an einen E-Mail-aktivierten öffentlichen Ordner gesendet wurden, oder Nachrichten, die von einer anderen Person an einen öffentlichen Ordner gesendet und auch kopiert wurden. Es werden keine Nachrichten zurück, die die person in einem öffentlichen Ordner gepostet hat. Um nach Elementen zu suchen, die die in einem öffentlichen Ordner veröffentlichte Person veröffentlicht hat, können Sie eine separate Inhaltssuche erstellen, die nach jedem Element sucht, das von der person in einem öffentlichen Ordner veröffentlicht wurde.
  
Hier ist ein prozess auf hoher Ebene, um nach Elementen zu suchen, die die subjektgebte Person in einem öffentlichen Ordner veröffentlicht hat. 
  
1. Öffnen Sie den Fall DSR, und erstellen Sie eine Suche auf der **Seite** Suchen. 
    
2. Verwenden Sie die folgenden Kriterien zum Konfigurieren der Suchabfrage und der zu durchsuchenden Inhaltsstandorte:
    
  - Verwenden Sie **im Feld Schlüsselwörter** die folgende Suchabfrage: 
    
    ```powershell
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - Durchsuchen aller öffentlichen Exchange-Ordner
    
  - Nachdem Sie die Suche ausgeführt und abgeschlossen haben, können Sie die Suchergebnisse exportieren und herunterladen (wie in [Schritt 4 beschrieben).](#step-4-export-the-data) Verwenden Sie die folgenden Einstellungen, um teilweise indizierte Elemente zu exportieren. 
