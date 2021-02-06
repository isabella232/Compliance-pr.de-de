---
title: Verwalten von Anträgen von datensubjektsubjekten Der DSGVO mit dem Falltool für Anträge der DSGVO im Security & Compliance Center
description: Erfahren Sie, wie Sie Anträge von datensubjekten Der EU-Datenschutz-Grundverordnung (DSGVO) mit dem Falltool für Anträge der DSGVO verwalten.
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
ms.openlocfilehash: 67aadb6e9ccda3a84a06b39570c680c8b30ce775
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121494"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-security--compliance-center"></a>Verwalten von Anträgen von datensubjektsubjekten Der DSGVO mit dem Falltool für Anträge von Anträgensubjekten im Security & Compliance Center

In der EU-Datenschutz-Grundverordnung (DSGVO) geht es um den Schutz und die Aktivierung der Datenschutzrechte von Einzelpersonen innerhalb der Europäischen Union (EU). Die DSGVO gibt Einzelpersonen in der Europäischen Union (auch als betroffene Personen bezeichnet) das Recht, auf ihre personenbezogenen Daten zu zugreifen, diese abzurufen, zu korrigieren, zu löschen und einzuschränken. Unter der DSGVO sind personenbezogene Daten alle Informationen im Zusammenhang mit einer identifizierten oder identifizierbaren natürlichen Person. Ein formaler Antrag einer Person an ihre Organisation, maßnahmen gegen ihre personenbezogenen Daten zu ergreifen, wird als Antrag einer betroffenen Person oder antrags einer betroffenen Person bezeichnet. Ausführliche Informationen zum Reagieren auf DSRs für Daten in Office 365 finden Sie im [Office 365-Antragshandbuch](https://go.microsoft.com/fwlink/?linkid=871169 )für Datensubjekte.
  
Um Untersuchungen als Reaktion auf einen Antrag einer betroffenen Person in Ihrer Organisation zu verwalten, können Sie das Falltool für Anträge einer betroffenen Person im Security & Compliance Center verwenden, um inhalte zu finden, die in:
  
- Ein beliebiges Benutzerpostfach in Ihrer Organisation. Dies umfasst Skype for Business-Unterhaltungen und 1:1-Chats in Microsoft Teams.
    
- Alle Postfächer, die einer Microsoft 365-Gruppe zugeordnet sind, und alle Teampostfächer in Microsoft Teams
    
- Alle SharePoint Online-Websites und OneDrive for Business-Konten in Ihrer Organisation
    
- Alle Microsoft Teams- und Microsoft 365-Gruppenwebsites in Ihrer Organisation
    
- Alle öffentlichen Ordner in Exchange Online
    
Mit dem Falltool für den Fall einer DSR können Sie:
  
- Erstellen Sie einen separaten Fall für jede Untersuchung eines Antrags einer betroffenen Person.
    
- Steuern, wer Zugriff auf den Fall einer DSR hat, indem Sie Personen als Mitglieder des Falls hinzufügen; Nur Mitglieder können auf den Fall zugreifen und ihre Fälle  nur in der Liste der Fälle auf der Seite mit den Fällen für datenbehinderische Daten im Security & Compliance Center anzeigen. Darüber hinaus können Sie verschiedenen Mitgliedern desselben Falls unterschiedliche Berechtigungen zuweisen. Beispielsweise können Sie einigen Mitgliedern erlauben, nur den Fall und die Suchergebnisse anzeigen und anderen Mitgliedern das Erstellen von Suchen und exportieren von Suchergebnissen zu ermöglichen. 
    
- Verwenden Sie die integrierte Suche, um nach allen Inhalten zu suchen, die von einer bestimmten datensubjektspezifischen Person erstellt oder hochgeladen wurden.
    
- Überarbeiten Sie optional die integrierte Suchabfrage, und führen Sie die Suche erneut aus, um die Suchergebnisse zu einengt.
    
- Fügen Sie weitere Inhaltssuchen hinzu, die dem Fall einer DSR zugeordnet sind. Dazu gehört das Erstellen von Suchen, die teilweise indizierte Elemente und vom System generierte Protokolle vom Office-Roamingdienst zurückgeben.
    
- Exportieren Sie Daten als Reaktion auf einen Antrag einer anforderung einer anforderung für den Zugriff oder export einer Anforderung einer anforderung einer Anforderung einer anforderung einer DSR.
    
- Löschen Sie Fälle, wenn die Untersuchung eines Antrags einer betroffenen Person abgeschlossen wurde. Dadurch werden alle Such- und Exportaufträge entfernt, die dem Fall zugeordnet sind.
    
Dies ist der prozess auf hoher Ebene für die Verwendung des Falltools für Den Fall von Daten zur Verwaltung von Untersuchungen von DSR:
  
[Step 1: Assign eDiscovery permissions to potential case members](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Schritt 2: Erstellen eines Fall einer datenserforderten Benutzerin und Hinzufügen von Mitgliedern](#step-2-create-a-dsr-case-and-add-members)

[Schritt 3: Ausführen der Suchabfrage](#step-3-run-the-search-query)

[Schritt 4: Exportieren der Daten](#step-4-export-the-data)

[(Optional) Schritt 5: Überarbeiten der integrierten Suchabfrage](#optional-step-5-revise-the-built-in-search-query)

[Weitere Informationen zur Verwendung des Falltools für Den Fall einer Daten dazu](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> Unsere Tools können Administratoren dabei unterstützen, Zugriffs- oder Exportanforderungen von Anträgen von Anträgen einer datenvermittelten Datengruppe durchzuführen, indem sie ihnen die Verwendung der integrierten Such- und Exportfunktionen im Falltool für Anträge von Anträgen einer antragsgehörigen Benutzergruppe ermöglichen. Das Tool erleichtert eine Best-Effort-Methode zum Exportieren von Daten, die für einen Antrag einer betroffenen Person auf Antrag einer betroffenen Person relevant sind. Es ist jedoch wichtig zu beachten, dass die Suchergebnisse je nach betroffener Person oder den vom Administrator ergriffenen Aktionen variieren können, die sich darauf auswirken können, ob ein Element zu Exportzwecken als "personenbezogene Daten" eingestuft wird. Wenn die betroffene Person beispielsweise die letzte Person war, die eine Datei geändert hat, die sie nicht erstellt hat, wird die Datei möglicherweise nicht in den Suchergebnissen zurückgegeben. Ebenso könnte ein Administrator Daten exportieren, ohne teilweise indizierte Elemente oder alle Versionen von SharePoint-Dokumenten zu verwenden. Daher können die bereitgestellten Tools dazu beitragen, den Zugriff auf und den Export von Datenanforderungen zu erleichtern. Die Ergebnisse unterliegen jedoch bestimmten Verwendungsszenarien für Administratoren und Datensubjekte. 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Schritt 1: Zuweisen von eDiscovery-Berechtigungen zu potenziellen Fallmitgliedern

Standardmäßig kann ein globaler Administrator im Security & Compliance Center auf das Falltool für DSR zugreifen. Standardmäßig haben andere Benutzer, z. B. ein Datenschutzbeauftragter, ein Personalmanager oder andere Personen, die an Untersuchungen betroffener Personen beteiligt sind, keinen Zugriff auf das Falltool für Den Betroffenen und müssen über die entsprechenden Berechtigungen für den Zugriff auf das Tool verfügen. Die einfachste Möglichkeit dazu besteht im  Wechseln zur Seite "Berechtigungen" im Security & Compliance Center und zum Hinzufügen von Benutzern zur Rollengruppe "eDiscovery-Manager". Sie müssen diese Berechtigungen auch zuweisen, damit Sie sie als Mitglieder des In-DSR-Falls hinzufügen können, den Sie in Schritt 2 erstellt haben. 
  
Schrittweise Anweisungen finden Sie unter ["Zuweisen von eDiscovery-Berechtigungen im Office 365 Security & Compliance Center".](/microsoft-365/compliance/assign-ediscovery-permissions)
  
> [!NOTE]
> Standardmäßig verfügt ein globaler Administrator (oder andere Mitglieder der Rollengruppe "Organisationsverwaltung" im Security & Compliance Center) nicht über die erforderlichen Berechtigungen zum Exportieren von Inhaltssuchergebnissen (siehe Schritt 4 in diesem Artikel). Um dies zu adressieren, kann sich ein Administrator selbst als Mitglied der Rollengruppe "eDiscovery-Manager" hinzufügen. 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a>Schritt 2: Erstellen eines Fall einer datenserforderten Benutzerin und Hinzufügen von Mitgliedern

Der nächste Schritt besteht im Erstellen eines Falls für einen Fall einer DSR. Wenn Sie einen Fall erstellen, können Sie die integrierte Suche starten, oder Sie können den Fall erstellen, ohne die Suche zu starten. Mit dem folgenden Verfahren werden Sie angewiesen, den Fall zu erstellen, ohne die Suche zu starten, und anschließend wird gezeigt, wie Sie dem Fall Mitglieder hinzufügen.
  
1. Melden Sie [https://protection.office.com](https://protection.office.com) sich mit Ihrem Arbeits- oder Schulkonto an. 
    
2. Klicken Sie & Security & Compliance  Center auf Anträge von Datensubjekten, und klicken Sie dann auf "Hinzufügen " Symbol " Neuer \> Fall ![ einer ](../media/ITPro-EAC-AddIcon.gif) **antragsbegründenden Person".**
    
3. Geben Sie auf der **Flyoutseite für** den Fall eines neuen DSR einen Namen ein, geben Sie eine optionale Beschreibung ein, und klicken Sie dann auf **"Weiter".** Der Name des Falls muss in Ihrer Organisation eindeutig sein.
    
    > [!TIP]
    > Erwägen Sie das Hinzufügen des Namens der Person, die den Antrag einer betroffenen Person gestellt hat, die Sie untersuchen, im Namen und/oder in der Beschreibung des neuen Falls. Beachten Sie, dass nur Mitglieder dieses Falls (und eDiscovery-Administratoren) den Fall in der Liste der Fälle auf der Seite "Anfragen von **Datensubjekten" anzeigen** können. 
  
4. Wählen Sie **auf** der Seite "Anforderungsdetails" unter "Betroffene" **(die** Person, die diese Anfrage gestellt hat) die Person aus, für die Sie Daten suchen und exportieren möchten, und klicken Sie dann auf **"Weiter".**
    
5. Auf der **Seite "Falleinstellungen bestätigen"** können Sie den Fallnamen und die Beschreibung ändern und eine andere person auswählen. Klicken Sie andernfalls auf **"Speichern".**
    
    Es wird eine Seite angezeigt, auf der bestätigt wird, dass der neue Fall einer datenserforderten Anzeige erstellt wurde.
    
    ![Starten sie die Suche, oder schließen Sie die Fallseite für einen neuen Fall eines Datendungsrs.](../media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    An dieser Stelle können Sie zwei Dinge tun:
    
    a. Wenn Sie auf **Suchergebnisse anzeigen klicken,** wird die Suche gestartet. Dies ist die Standardauswahl. Die integrierte Suche, die ausgeführt wird, wenn Sie diese Option auswählen, und die zurückgegebenen Ergebnisse werden in Schritt 3 erläutert.
    
    b. Wenn Sie **auf "Fertig** stellen" klicken, wird der neue Fall für den Fall einer erneuten DSR geschlossen, ohne die integrierte Suche zu starten. Wenn Sie diese Option auswählen, wird der neue Fall einer antragssubjektsubjektierten Person auf der Seite mit den Anfragen **von Datensubjekten** angezeigt.
    
6. Klicken **Sie auf** "Fertig stellen", damit Sie zum neuen Fall für einen Fall einer datendnesten Benutzerin wechseln und Mitglieder hinzufügen können. 
    
7. Klicken Sie **auf der Seite "Anträge** von Datensubjekten" auf den Namen des von Ihnen erstellten Antrags einer antragssubjekten Person. 
    
8. Klicken Sie **auf der Flyoutseite "Diesen Fall** verwalten" unter **"Mitglieder verwalten"** auf **"Hinzufügen".** 
    
    Unter **"Benutzer"** wird eine Liste der Personen angezeigt, denen die entsprechenden eDiscovery-Berechtigungen zugewiesen sind. Die Personen, denen Sie in Schritt 1 eDiscovery-Berechtigungen zugewiesen haben, werden in dieser Liste angezeigt. 
    
9. Wählen Sie die Personen aus, die als Mitglieder des Falles einer DSR hinzugefügt werden, klicken Sie auf "Hinzufügen", und speichern Sie dann Ihre Änderungen.
    
    Sie können Rollengruppen auch als Mitglieder des Falls  einer DSR hinzufügen, indem Sie unter "Rollengruppen **verwalten" auf "Hinzufügen" klicken.** 
    
## <a name="step-3-run-the-search-query"></a>Schritt 3: Ausführen der Suchabfrage

Nachdem Sie einen Fall für einen Datenverdingten erstellt und Mitglieder hinzugefügt haben, führen Sie im nächsten Schritt die integrierte Suche aus, die dem Fall zugeordnet ist. Diese Standardsuchabfrage führt die folgenden Aufgaben aus:
  
- Durchsucht alle Postfächer in Ihrer Organisation nach allen E-Mail-Elementen, die von der person gesendet oder empfangen wurden. Dazu wird die E-Mail-Eigenschaft  *"Teilnehmer"*  verwendet, die in allen Personenfeldern in einer E-Mail-Nachricht nach der betreffs person sucht. Diese Eigenschaft gibt Elemente zurück, in denen sich die person in den Feldern **"Von",** **"An",** **"CC"** und **"BCC"** befindet. Öffentliche Ordner in Exchange Online werden auch nach Nachrichten durchsucht, die von der datensubjektierten Person gesendet oder empfangen wurden. 
    
- Durchsucht alle Websites in Ihrer Organisation nach Dokumenten und Elementen, die von der person erstellt oder hochgeladen wurden. Dazu werden die folgenden Websiteeigenschaften verwendet:
    
  - Die  *Eigenschaft "Author"*  gibt Elemente zurück, bei denen die person im Feld "Autor" in Office-Dokumenten aufgeführt ist. Dieser Wert bleibt auch dann erhalten, wenn das Dokument von einer anderen Person kopiert und hochgeladen wird. 
    
  - Die  *CreatedBy -Eigenschaft*  gibt Elemente zurück, die von der datensubjekt erstellt oder hochgeladen wurden. 
    
So sieht die Stichwortabfrage für die integrierte Suche aus, die automatisch erstellt wird, wenn Sie einen Fall einer anfrageverdingten Anfrage erstellen.
  
```powershell
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

Wenn z. B. der Name der datensubjekten Person Ina Bestehtte ist, würde die Stichwortabfrage wie die folgende aussehen:
  
```powershell
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 **So führen Sie die integrierte Suche nach einem Fall einer DSR aus:**
  
1. Klicken Sie & Security &  Compliance Center auf Anfragen von Datensubjekten, und klicken Sie dann auf "Öffnen" neben dem Fall einer antragsbegründenden Person, den Sie in Schritt \> 2 erstellt  haben. 
    
    Klicken Sie **oben** auf der Seite auf die Registerkarte "Suchen", und klicken Sie dann auf das Kontrollkästchen neben der integrierten Suche, die beim Erstellen des Falls mit einer DSR erstellt wurde. Die Suche hat denselben Namen wie der Fall einer DSR. 
    
2. Klicken Sie auf der Flyoutseite "Suche" auf **"Abfrage öffnen".**
    
    Wenn Sie die Abfrage öffnen, wird die Suche gestartet und in wenigen Sekunden abgeschlossen. 
    
3. Wenn die Suche abgeschlossen ist, klicken Sie auf **"Ergebnisse anzeigen",** um eine Vorschau der Suchergebnisse anzuzeigen. Weitere Informationen finden Sie unter Vorschau [der Suchergebnisse.](/microsoft-365/compliance/content-search#preview-search-results)
    
    > [!TIP]
    > Sie können auch die Suchabfragestatistiken anzeigen, um die Anzahl der Postfach- und Websiteelemente anzuzeigen, die von der Suche zurückgegeben werden, sowie die Obersten Inhaltsspeicherorte, die Elemente enthalten, die der Suchabfrage entsprechen. Weitere Informationen finden Sie unter [Anzeigen von Informationen und Statistiken zu einer Suche.](/microsoft-365/compliance/content-search#view-information-and-statistics-about-a-search) 
  
Sie können die integrierte Suchabfrage bearbeiten, die durchsuchten Inhaltsorte ändern und dann die Suche erneut ausführen. Weitere Informationen finden Sie in Schritt [5.](#optional-step-5-revise-the-built-in-search-query) 
  
## <a name="step-4-export-the-data"></a>Schritt 4: Exportieren der Daten

Nachdem Sie die integrierte Suche ausgeführt haben, können Sie die Suchergebnisse exportieren. Alternativ können Sie vor dem Exportieren der Daten die Abfrage überarbeiten, um die Anzahl der Suchergebnisse zu reduzieren. Weitere Informationen zum Einen der Suchergebnisse finden Sie in Schritt 5.
  
Wenn Sie Suchergebnisse exportieren, können Postfachelemente in PST-Dateien oder als einzelne Nachrichten heruntergeladen werden. Wenn Sie Inhalte aus SharePoint- und #A0 exportieren, werden Kopien systemeigener #A1 und anderer Dokumente exportiert. Eine Ergebnisdatei, die Informationen zu jedem exportierten Element enthält, ist in den Suchergebnissen enthalten. Ausführlichere Informationen zum Exportieren finden Sie unter [Exportieren von Inhaltssuchergebnissen.](/microsoft-365/compliance/export-search-results)
  
> [!NOTE]
> Standardmäßig verfügt ein globaler Administrator (oder andere Mitglieder der Rollengruppe "Organisationsverwaltung" im Security & Compliance Center) nicht über die erforderlichen Berechtigungen zum Exportieren von Inhaltssuchergebnissen. Um dies zu adressieren, kann sich ein Administrator selbst als Mitglied der Rollengruppe "eDiscovery-Manager" hinzufügen. 
  
Der Computer, den Sie zum Exportieren von Daten verwenden, muss die folgenden Systemanforderungen erfüllen:
  
- 32-Bit- oder 64-Bit-Versionen von Windows 7 und höher
    
- Microsoft .NET Framework 4.7
    
- Einen unterstützten Browser:
    
  - Microsoft Edge
    
    Oder
    
  - Microsoft Internet Explorer 10 und spätere Versionen
    
    > [!NOTE]
    > Microsoft stellt keine Drittanbietererweiterungen oder -add-ons für ClickOnce her. Das Exportieren von Daten mithilfe eines nicht unterstützten Browsers mit Drittanbietererweiterungen oder -add-ons wird nicht unterstützt. 
  
 **So exportieren Sie Daten aus der integrierten Suche in einem Fall einer DSR**
  
1. Klicken Sie & Security & Compliance  Center auf Anfragen von Datensubjekten, und klicken Sie dann auf "Öffnen" neben dem Fall einer datensubjektorientierten Person, aus dem Sie Daten exportieren \> möchten.  
    
2. Klicken Sie **oben** auf der Seite auf die Registerkarte "Suchen", und klicken Sie dann auf das Kontrollkästchen neben der integrierten Suche, die beim Erstellen des Falls mit einer DSR erstellt wurde. Oder klicken Sie auf eine andere Suche, um Daten aus dieser Suche zu exportieren. 
    
3. Klicken Sie auf der Such-Flyout-Seite auf das Symbol "Suchergebnisse exportieren" (More), und wählen Sie dann ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)  **"Ergebnisse exportieren"** aus der Dropdownliste aus. 
    
4. Wählen Sie **auf der Seite** "Ergebnisse exportieren" die folgenden empfohlenen Optionen für DSR-Exportanforderungen aus. 
    
    ![Konfigurieren der Exporteinstellungen](../media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    a. Wählen Sie unter Ausgabeoptionen die erste Option ( Alle Elemente, mit Ausnahme von Elementen, die ein unbekanntes Format **haben,** verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden) aus, um nur indizierte Elemente zu exportieren. Der Grund, warum Sie teilweise indizierte Elemente aus der integrierten Suche nicht exportieren möchten, liegt daran, dass teilweise indizierte Elemente von anderen Benutzern ebenfalls exportiert werden. Um nur die teilweise indizierten Elemente für die benutzerdefinierte Person zu exportieren, wird empfohlen, eine separate Suche zu erstellen. Weitere Informationen finden Sie [unter "Exportieren teilweise indizierter](#exporting-partially-indexed-items) Elemente" im Abschnitt "Weitere Informationen zur Verwendung des Falltools für DSR".
    
    b. Wählen **Sie unter "Exchange-Inhalte exportieren als"** die dritte Option aus, eine PST-Datei, die **alle Nachrichten in einem einzigen Ordner enthält.** Da einige der Ergebnisse möglicherweise für Elemente aus dem Postfach eines anderen Benutzers stammen, listet diese Option nur das Element in einem einzelnen Ordner auf, ohne das tatsächliche Postfach anzuzeigen, und ist die beste Option, wenn Sie die Ergebnisse wie im nächsten Element empfohlen deduplizieren. Mit dieser Option kann die person auch Elemente in chronologischer Reihenfolge überprüfen (Elemente werden nach dem Gesendeten Datum sortiert), ohne in der ursprünglichen Postfachordnerstruktur für jedes Element navigieren zu müssen.
    
    c. Wählen **Sie die Option "Deduplizierung aktivieren"** aus, um doppelte E-Mail-Nachrichten auszuschließen. Wir empfehlen diese Option, da bei der integrierten Suche alle Postfächer in Ihrer Organisation durchsucht werden. Wenn also mehrere Kopien derselben Nachricht in den durchsuchten Postfächern gefunden werden, bedeutet diese Option, dass nur eine Kopie einer Nachricht exportiert wird. Diese Option führt zusammen zum Exportieren von Nachrichten in einer PST-Datei in einem einzigen Ordner, was die beste Benutzererfahrung für Exportanforderungen von Anträgen einer datenorientierten Nachricht zur Folge hat. Im Results.csv Exportbericht werden alle Speicherorte aufgeführt, an denen doppelte Nachrichten gefunden wurden.
    
    Optional können Sie die Option **"Versionen** für #A0 enthalten" auswählen, um alle Versionen von SharePoint- und #A1 zu exportieren. Dies erfordert, dass die Versionsierung für Dokumentbibliotheken aktiviert ist. Mit dieser Option wird sichergestellt, dass alle relevanten Daten exportiert werden.
    
5. Nachdem Sie die Exporteinstellungen festgelegt haben, klicken Sie auf **"Exportieren".**
    
    Die Suchergebnisse werden zum Herunterladen vorbereitet, d. h., sie werden in den Azure -Speicherbereich für Ihre Organisation in der Microsoft Cloud hochgeladen. In den nächsten Schritten wird gezeigt, wie Sie diese Daten auf Ihren lokalen Computer herunterladen.
    
6. Klicken Sie auf die **Registerkarte "Exportieren",** um den erstellten Exportauftrag anzeigen zu können. Exportaufträge haben den gleichen Namen wie die entsprechende Suche, **_Export** am Ende des Suchnamens angefügt ist. 
    
7. Klicken Sie auf den Exportauftrag, den Sie gerade erstellt haben, um die Exportf flyoutseite anzeigen zu können. Diese Seite enthält Informationen zur Suche, z. B. die Größe und Gesamtanzahl der zu exportierende Elemente und den Prozentsatz der Elemente, die in einen Azure-Speicherbereich übertragen wurden. Klicken **Sie auf "Aktualisieren",** um die Uploadstatusinformationen zu aktualisieren. 
    
8. Klicken Sie unter **Schlüssel exportieren** auf **In Zwischenablage kopieren**. Verwenden Sie diesen Schlüssel in Schritt 11, um die Suchergebnisse herunterzuladen.
    
9. Klicken Sie oben auf der Export-Flyoutseite auf das Symbol "Suchergebnisse ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)  exportieren". 
    
10. Klicken Sie im Popupfenster am unteren Rand  der Seite auf "Öffnen", um das **eDiscovery-Exporttool zu öffnen.** Das **eDiscovery-Exporttool** wird beim ersten Herunterladen von Suchergebnissen installiert. 
    
11. Fügen Sie **im eDiscovery-Exporttool** den Exportschlüssel, den Sie in Schritt 8 kopiert haben, in das entsprechende Feld ein.
    
12. Klicken Sie auf **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen. 
    
    > [!NOTE]
    > Aufgrund der hohen Datenträgeraktivität (Lese- und Schreibvorgänge) sollten Sie suchergebnisse auf ein lokales Laufwerk herunterladen. laden Sie sie nicht auf ein zugeordnetes Netzlaufwerk oder einen anderen Netzwerkspeicherort herunter. 
  
13. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Das **eDiscovery-Exporttool** zeigt Statusinformationen zum Exportvorgang an, einschließlich einer Schätzung der Anzahl (und Größe) der verbleibenden Elemente, die heruntergeladen werden sollen. Wenn der Exportvorgang abgeschlossen ist, können Sie auf die Dateien am Speicherort zugreifen, an dem sie heruntergeladen wurden. Weitere Informationen zu den Berichten, die beim Herunterladen [](/microsoft-365/compliance/export-search-results#more-information) von Inhaltssuchergebnissen enthalten waren, finden Sie im Abschnitt "Weitere Informationen" unter "Exportieren von Inhaltssuchergebnissen". 
    
Nachdem die Daten exportiert wurden, befinden sich die Suchergebnisse und Exportberichte in einem Ordner, der denselben Namen wie der Fall einer DSR hat. Die PST-Dateien, die Postfachelemente enthalten, befinden sich in einem Unterordner mit dem Namen **Exchange**. Dokumente und andere Elemente von Websites befinden sich in einem Unterordner mit dem Namen **SharePoint**. 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a>(Optional) Schritt 5: Überarbeiten der integrierten Suchabfrage

Nachdem Sie die integrierte Suche ausgeführt haben, können Sie sie überarbeiten, um den Bereich zu einengt, um weniger Suchergebnisse zurückzukehren. Sie können dies tun, indem Sie der Abfrage Bedingungen hinzufügen. Eine Bedingung wird durch den Operator AND logisch mit der **Stichwortabfrage** verbunden. Dies bedeutet, dass Elemente in den Suchergebnissen zurückgegeben werden müssen, um sowohl die Stichwortabfrage als auch alle von Ihnen hinzugefügten Bedingungen zu erfüllen. Auf diese Weise helfen Bedingungen, die Ergebnisse zu einendnen. Wenn Sie einer Suchabfrage zwei oder mehr eindeutige Bedingungen hinzufügen (Bedingungen, die unterschiedliche Eigenschaften angeben), werden diese Bedingungen logisch durch den Operator **AND** verbunden. Das bedeutet, dass nur Elemente zurückgegeben werden, die (zusätzlich zur Schlüsselwortabfrage) alle Bedingungen erfüllen. Wenn Sie einer einzelnen Bedingung mehrere Werte (durch Kommas oder Semikolon getrennt) hinzufügen, werden diese Werte durch den Operator **OR** verbunden. Das bedeutet, es werden Elemente zurückgegeben, die einen der angegebenen Werte für die Eigenschaft in der Bedingung enthalten. 
  
Hier sind einige Beispiele für die Bedingungen, die Sie der integrierten Suchabfrage eines Falls einer datenverdingten Anfrage hinzufügen können. Der Name der tatsächlich in einer Suchabfrage verwendeten Eigenschaft wird in Klammern angezeigt.
  
- **Dateityp ( `filetype` )** – Gibt die Erweiterung eines Dokuments oder einer Datei an. Verwenden Sie diese Bedingung, um nach Dokumenten und Dateien zu suchen, die von bestimmten Office-Anwendungen wie Word, Excel und OneNote erstellt wurden. 
    
- **Nachrichtentyp ( `kind` )** – Gibt den Typ des E-Mail-Elements an, nach dem gesucht werden soll. Beispielsweise können Sie die Syntax verwenden, um nur E-Mail-Nachrichten und Skype for #A0 oder  `kind:email OR kind:im` 1:1-Chats in Microsoft Teams zurückzukehren. 
    
- **Compliancetag ( `compliancetag` )** – Gibt eine Bezeichnung an, die einer E-Mail-Nachricht oder einem Dokument zugewiesen ist. Diese Bedingung gibt Elemente zurück, die mit einer bestimmten Bezeichnung klassifiziert sind. Bezeichnungen werden verwendet, um E-Mails und Dokumente für die Datensteuerung zu klassifizieren und Aufbewahrungsregeln basierend auf der von der Bezeichnung definierten Klassifizierung zu erzwingen. Dies ist eine nützliche Bedingung für Untersuchungen im Zusammenhang mit datenbezogenen Daten, da Ihre Organisation möglicherweise Bezeichnungen verwendet, um Inhalte im Zusammenhang mit dem Datenschutz zu klassifizieren oder die personenbezogene Daten oder vertrauliche Informationen enthalten. Verwenden Sie für den Wert dieser Bedingung den vollständigen Bezeichnungsnamen oder den ersten Teil des Bezeichnungsnamens mit einem Platzhalter. Weitere Informationen finden Sie unter [Informationen zu Aufbewahrungsrichtlinien und Aufbewahrungsbezeichnungen in Office 365.](/microsoft-365/compliance/retention)
    
Eine Liste und Beschreibung aller bedingungen, die im Falltool für die DSR verfügbar sind, finden Sie unter Suchbedingungen [im](/microsoft-365/compliance/keyword-queries-and-search-conditions#search-conditions) Artikel "Stichwortabfragen und Suchbedingungen für die Inhaltssuche". 
  
### <a name="changing-the-content-locations-that-are-searched"></a>Ändern der durchsuchten Inhaltsorte

Zusätzlich zur Überarbeitung der integrierten Suche für einen Fall einer datenverhinderten Benutzerin können Sie auch die durchsuchten Inhaltsorte ändern. Wie bereits erläutert, durchsucht die integrierte Suche jedes Postfach und jede Website in der Organisation sowie alle öffentlichen Exchange Online-Ordner. Beispielsweise könnten Sie die Suche so eindnen, dass nur das Postfach und das #A0 und ausgewählte #A1 durchsucht werden. Wenn Sie bestimmte Websites durchsuchen möchten, müssen Sie jede Website hinzufügen, die Sie durchsuchen möchten.
  
So ändern Sie die zu durchsuchende Inhaltsorte:
  
1. Öffnen Sie die integrierte Suche, für die Sie die Inhaltsorte ändern möchten.
    
2. Klicken Sie in der Suchabfrage unter **"Speicherorte"** auf **"Ändern"** neben der Option **"Bestimmte Speicherorte".** 
    
    ![Klicken Sie auf "Ändern", um die Inhaltsorte der integrierten Suchabfrage zu ändern.](../media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    Die **Flyoutseite zum** Ändern von Speicherorten wird angezeigt. Hier finden Sie eine Beschreibung der Inhaltsorte in der integrierten Suche und einige Informationen zum Ändern der durchsuchten Speicherorte. 
    
    ![Flyoutseite "Speicherorte ändern"](../media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    a. Die Umschaltfunktion unter **"Alle** auswählen" im Abschnitt "Postfach" am oberen Rand der Flyoutseite ist aktiviert, was darauf hinweist, dass alle Postfächer durchsucht werden. Um den Suchbereich zu einengt, klicken Sie auf den Umschalter, um die Auswahl zu deaktivieren, und klicken Sie dann auf **"Benutzer, Gruppen** oder Teams auswählen" und dann auf bestimmte zu durchsuchende Postfächer.
    
    b. Die Umschaltflächen unter **"Alle** auswählen" im Abschnitt "Websites" in der Mitte der Flyoutseite sind aktiviert, was bedeutet, dass alle Websites durchsucht werden. Um die Suche auf ausgewählte Websites zu verengt, deaktivieren Sie die Umschaltflächen und klicken dann auf **"Websites auswählen".** Sie müssen jede bestimmte Website hinzufügen, die Sie durchsuchen möchten, einschließlich des #A0 der datensubjektspezifischen Person.
    
    c. Die Umschaltfunktion im Abschnitt "Öffentliche Exchange-Ordner" ist aktiviert, was bedeutet, dass alle öffentlichen Ordner in Exchange durchsucht werden. Sie können nur alle öffentlichen Ordner in Exchange oder keines davon durchsuchen. Sie können keine bestimmten suchen.
    
3. Wenn Sie die Inhaltsorte in der integrierten Suche ändern, klicken Sie auf "Ausführen speichern", **um &amp;** die Suche neu zu starten. 

> [!NOTE]
> Wenn Sie alle Postfachspeicherorte oder nur bestimmte Postfächer durchsuchen, werden Daten aus anderen Office 365-Anwendungen, die in Benutzerpostfächern gespeichert sind, einbezogen, wenn Sie die Ergebnisse der Suche exportieren. Diese Daten werden nicht in die geschätzten Suchergebnisse einbezogen und sind für die Vorschau nicht verfügbar. Sie ist jedoch enthalten, wenn Sie die Suchergebnisse exportieren und herunterladen. Weitere Informationen zu den Anwendungen, die Daten im Postfach eines Benutzers speichern, finden Sie [unter "In Exchange Online-Postfächern gespeicherter Inhalt".](/microsoft-365/compliance/what-is-stored-in-exo-mailbox)
  
## <a name="more-information-about-using-the-dsr-case-tool"></a>Weitere Informationen zur Verwendung des Falltools für Den Fall einer Daten dazu

Die folgenden Abschnitte enthalten weitere Informationen zur Verwendung des Falltools für Anträge von Anträgen aufgrund
  
[Exportieren von Daten aus dem Office-Roamingdienst](#exporting-data-from-the-office-roaming-service)

[Exportieren teilweise indizierter Elemente](#exporting-partially-indexed-items)

[Suchen und Exportieren von Daten aus Microsoft Teams und Microsoft 365-Gruppen](#searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups)

[Durchsuchen öffentlicher Ordner in Exchange](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-the-office-roaming-service"></a>Exportieren von Daten aus dem Office-Roamingdienst

Sie können das Falltool für den Fall einer DSR verwenden, um nutzungsdaten zu suchen und zu exportieren, die vom Office-Roamingdienst generiert werden. Roaming ist ein Dienst, der Office-bezogene Einstellungen speichert, z. B. Office-Design, Benutzerwörterbuch, Spracheinstellungen, Entwicklermodus und automatische Korrektur. 
    
Die Daten aus dem Office-Roamingdienst werden im Postfach einer datensubjektübergreifenden Person in einem ausgeblendeten Ordner gespeichert, der sich in einer Nicht-IPM-Unterstruktur (Non-IPM) von Exchange Online-Postfächern befindet. Dies bedeutet, dass die Daten aus der Ansicht des Benutzers ausgeblendet werden, wenn sie Outlook oder andere E-Mail-Clients für den Zugriff auf ihr Postfach verwenden. Weitere Informationen zu ausgeblendeten Ordnern finden Sie unter [MAPI Hidden Folders](https://go.microsoft.com/fwlink/?linkid=872758).
  
Sie können eine separate Inhaltssuche erstellen (und sie einem Fall eines Datensubjekts zuordnen), die die Nutzungsdaten des Office-Roamingdiensts im Postfach der person zurückgibt. Diese Daten sind nicht in der Suchstatistik enthalten und stehen nicht für die Vorschau zur Verfügung. Sie können sie jedoch exportieren und dann als Reaktion auf einen Antrag einer personsorientierten Person auf Export an die person senden.
  
Wenn Sie Daten aus dem Office-Roamingdienst exportieren, werden die Daten in einem separaten Ordner gespeichert, der sich im Ordner **"ApplicationDataRoot"** befindet, der sich unter einem Ordner mit dem Namen der E-Mail-Adresse der person befindet. Diese Daten werden als JSON-Dateien exportiert, bei denen es sich um lesbare Textdateien handelt, die XML- oder TXT-Dateien ähneln und an E-Mail-Nachrichten angefügt sind. Derzeit wird dieser Ordner mit der GUID (Globally Unique Identifier) benannt: **1caee58f-eb14-4a6b-9339-1fe2ddf6692b**. In zukünftigen Versionen des DSR-Falltools wird die GUID durch den Namen der tatsächlichen Anwendung ersetzt. 

   
 **So suchen Und exportieren Sie Office-Roamingdienstdaten:**
  
1. Klicken Sie im Security &  Compliance Center auf Anträge von Datensubjekten, und klicken Sie dann auf "Öffnen" neben dem Fall einer person, für die Sie Nutzungsdaten exportieren \> möchten.  
    
2. Klicken Sie **oben** auf der Seite auf die Registerkarte "Suchen", und klicken Sie dann auf "Symbolgeführte ![ Suche ](../media/ITPro-EAC-AddIcon.gif) **hinzufügen".**
    
3. Klicken **Sie auf** der **Suchseite auf "Abbrechen".** 
    
4. Aktivieren **Sie unter Suchabfrage** in der **Bedingung "Typ"** das Kontrollkästchen neben **dem Office-Roamingdienst.** 
    
    ![Aktivieren Sie das Kontrollkästchen "Office-Roamingdienst", um Verwendungsdaten zu exportieren.](../media/O365_DSRCase_SDSDataExport1.png)
  
    Die **Type-Bedingung** (bei der es sich um E-Mail-Nachrichtenklassen handelt) sollte das einzige Element in der Suchabfrage sein. Sie können das Feld **"Schlüsselwörter"** löschen oder leer lassen. 
    
5. Stellen **Sie unter "Speicherorte"** **sicher,** dass bestimmte Speicherorte ausgewählt sind, und klicken Sie dann auf **"Ändern".**
    
6. Klicken Sie oben  auf der Flyoutseite "Speicherorte ändern" (Postfachabschnitt) auf **"Benutzer, Gruppen oder Teams auswählen".**
    
7. Klicken Sie **auf der** Seite "Speicherorte bearbeiten" auf "Benutzer, Gruppen oder **Teams** auswählen", wählen Sie das Postfach der Person aus, und speichern Sie ihre Auswahl. 
    
8. Klicken **Sie auf & ausführen,** benennen Sie die Suche, und speichern Sie sie.
    
    Die Suche wird gestartet.
    
 **So exportieren Sie Office-Roamingdienstdaten:**
  
1. Wenn die im vorherigen Schritt erstellte Suche  abgeschlossen ist, klicken Sie oben auf der Seite auf die Registerkarte "Suchen", und klicken Sie dann auf das Kontrollkästchen neben der Suche. Möglicherweise müssen Sie auf ![ ](../media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **"Aktualisieren" klicken,** um die Suche anzeigen zu können. 
    
2. Klicken Sie auf der Such-Flyout-Seite auf das Symbol "Suchergebnisse exportieren" (More), und wählen Sie dann ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)  **"Ergebnisse exportieren"** aus der Dropdownliste aus. 
    
3. Wählen Sie **auf der Seite** Ergebnisse exportieren die empfohlenen Optionen zum Exportieren von Verwendungsdaten aus. 
    
    ![Exportoptionen beim Exportieren von Nutzungsdaten des Office-Roamingdiensts](../media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    a. Wählen Sie unter Ausgabeoptionen die erste Option ( Alle Elemente, mit Ausnahme von Elementen, die ein unbekanntes Format **haben,** verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden) aus, um nur indizierte Elemente zu exportieren.
    
    b. Wählen **Sie unter "Exchange-Inhalte exportieren als"** die zweite Option aus, **eine PST-Datei, die alle Nachrichten enthält.**
    
    c. Lassen Sie die restlichen Exportoptionen deaktiviert.
    
4. Nachdem Sie die Exporteinstellungen festgelegt haben, klicken Sie auf **"Exportieren".**
    
    Die Suchergebnisse werden zum Herunterladen vorbereitet, d. h., sie werden in den Azure-Speicherbereich für Ihre Organisation in der Microsoft Cloud hochgeladen. In den nächsten Schritten wird gezeigt, wie Sie diese Daten auf Ihren lokalen Computer herunterladen.
    
5. Klicken Sie auf die Registerkarte **"Exportieren",** um den erstellten Exportauftrag anzeigen zu können. Die Exportaufträge haben denselben Namen  wie die entsprechende Suche, _Export am Ende des Suchnamens angefügt ist. 
    
6. Klicken Sie auf den Exportauftrag, den Sie gerade erstellt haben, um die Exportf flyoutseite anzeigen. 
    
7. Klicken Sie unter **Schlüssel exportieren** auf **In Zwischenablage kopieren**. Verwenden Sie diesen Schlüssel in Schritt 10, um die Suchergebnisse herunterzuladen.
    
8. Klicken Sie oben auf der Export-Flyoutseite auf das Symbol "Suchergebnisse ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)  exportieren". 
    
9. Klicken Sie im Popupfenster am unteren Rand  der Seite auf "Öffnen", um das **eDiscovery-Exporttool zu öffnen.** Das **eDiscovery-Exporttool** wird beim ersten Herunterladen von Suchergebnissen installiert. 
    
10. Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 7 kopiert haben, in das entsprechende Feld ein.
    
11. Klicken Sie auf **Durchsuchen**, um das Verzeichnis anzugeben, in das die Dateien mit den Suchergebnissen heruntergeladen werden sollen. 
    
    > [!NOTE]
    > Aufgrund der hohen Datenträgeraktivität (Lese- und Schreibvorgänge) sollten Sie suchergebnisse auf ein lokales Laufwerk herunterladen. laden Sie sie nicht auf ein zugeordnetes Netzlaufwerk oder einen anderen Netzwerkspeicherort herunter. 
  
12. Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**. 
    
    Das **eDiscovery-Exporttool** zeigt Statusinformationen zum Exportvorgang an, einschließlich einer Schätzung der Anzahl (und Größe) der verbleibenden Elemente, die heruntergeladen werden sollen. Wenn der Exportvorgang abgeschlossen ist, können Sie die Exchange -PST-Datei in Outlook öffnen und dann zum Ordner **"ApplicationDataRoot"** wechseln, um auf den Unterordner für den Roamingdienst zu zugreifen. 
    
    Wie zuvor erläutert, werden die JSON-Dateien, die Nutzungsdaten enthalten, an Nachrichten angefügt. Klicken Sie zum Anzeigen einer JSON-Datei auf eine Nachricht, und öffnen Sie dann die angefügte JSON-Datei. 
  
### <a name="exporting-partially-indexed-items"></a>Exportieren teilweise indizierter Elemente

Es wird empfohlen, teilweise indizierte Elemente (auch als nicht indizierte Elemente bezeichnet) nicht aus der integrierten Suche zu exportieren, die erstellt wird, wenn Sie einen Fall einer datenverhinderten Benutzerindung erstellen. Der Grund dafür ist, dass die Suchergebnisse wahrscheinlich nur teilweise indizierte Elemente für andere Benutzer in Ihrer Organisation enthalten und nicht nur teilweise indizierte Elemente für die person. Stattdessen wird empfohlen, eine separate Inhaltssuche zu erstellen, die mit dem Fall einer datensubjektbezogenen Person verknüpft ist, die nur zum Exportieren der teilweise indizierten Elemente im Zusammenhang mit der datensubjektbezogenen Person dient. 
  
Hier ist ein Prozess auf hoher Ebene zum Exportieren teilweise indizierter Elemente. Nachdem sie exportiert wurden, können Sie sie überprüfen, um festzustellen, ob ein Element für einen Zugriff oder eine Exportanforderung eines Antrags einer antrags einer anforderung einer Anforderung einer anforderung einer anforderung einer Anforderung einer anforderung einer anforderung einer Anforderung
  
1. Öffnen Sie den Fall "DSR", und erstellen Sie eine Suche auf der **Seite "Suche".** 
    
2. Verwenden Sie die folgenden Kriterien, um die Suchabfrage und die zu durchsuchenden Inhaltsorte zu konfigurieren:
    
    - Verwenden Sie eine leere/leere Schlüsselwortabfrage. Dadurch werden alle Elemente in den durchsuchten Inhaltspositionen zurückgegeben.
    
    - Durchsuchen Sie nur das Exchange #A0 der person und ihr OneDrive-Konto.
    
3. Nachdem Sie die Suche ausgeführt und abgeschlossen haben, können Sie die Suchergebnisse exportieren und herunterladen (wie in [Schritt 4 beschrieben).](#step-4-export-the-data) Verwenden Sie die folgenden Einstellungen, um teilweise indizierte Elemente zu exportieren. 
    
    - Wählen **Sie** unter Ausgabeoptionen die dritte Option ( Nur Elemente, die ein unbekanntes Format **haben,** verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden) aus, um nur teilweise indizierte Elemente zu exportieren.
    
    - Unter **"Exchange-Inhalte exportieren als"** können Sie eine beliebige Option basierend auf Ihren Einstellungen auswählen. 
    
    - Wenn Sie **die Option "Versionen für SharePoint-Dokumente** enthalten" auswählen, werden Versionen von Dokumenten exportiert, wenn eine Version teilweise indiziert ist. 
    
Weitere Informationen zu teilweise indizierten Elementen finden Sie unter: 
  
- [Teilweise indizierte Elemente in der Inhaltssuche in Office 365](/microsoft-365/compliance/partially-indexed-items-in-content-search)

- [Exportieren teilweise indizierter Elemente](/microsoft-365/compliance/export-search-results#exporting-partially-indexed-items)

### <a name="searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups"></a>Suchen und Exportieren von Daten aus Microsoft Teams und Microsoft 365-Gruppen

Unterhaltungen, die Teil der Chatliste in Microsoft Teams sind (so genannte Teamchats oder 1:1-Chats), werden im Exchange Online-Postfach der Benutzer gespeichert, die an den Chats teilnehmen. Außerdem werden die Dateien, die eine Person in einem 1:1-Chat teilt, im #A0 der Person gespeichert, die die Datei teilt. Da bei der integrierten Suche alle Postfächer und #A0 in der Organisation durchsucht werden, werden Teamchats und Dokumente, die in einer Chatsitzung freigegeben wurden (die von der person erstellt oder hochgeladen wurde) von der integrierten Suche in einem Fall einer DSR zurückgegeben.
  
Alternativ dazu werden Unterhaltungen, die Teil eines Teams-Kanals (auch Kanalnachrichten genannt) sind, in dem Postfach gespeichert, das einem Team zugeordnet ist. Diese Arten von Unterhaltungen, an der die subjektgebte Person teilgenommen hat, werden auch von der integrierten Suche zurückgegeben, da alle Postfächer durchsucht werden, die Teams zugeordnet sind. Darüber hinaus werden Dateien, die eine datensubjekte Person in einem Teams-Kanal teilt, auf der SharePoint-Website des Teams gespeichert. Dateien, die von der personenbezogenen Person erstellt oder hochgeladen wurden, werden von der integrierten Suche in einem Fall einer datensubjektsubjektverhinderten Person zurückgegeben, da die websites, die Teams zugeordnet sind, in die Suche einbezogen werden.
  
Ebenso werden Postfächer und SharePoint-Websites, die einer Microsoft 365-Gruppe entsprechen, ebenfalls in die integrierte Suche einbezogen. Dies bedeutet, dass von der person gesendete oder empfangene E-Mail-Nachrichten und von der person erstellten oder hochgeladenen Dateien zurückgegeben werden. 
  
Weitere Informationen zur Verwendung der Inhaltssuche zum Suchen nach Elementen in Microsoft Teams und Microsoft 365-Gruppen oder zum Erhalten einer Liste von Mitgliedern finden Sie im Abschnitt "Durchsuchen von Microsoft Teams und Microsoft 365-Gruppen" in der Inhaltssuche [in Microsoft 365.](/microsoft-365/compliance/content-search#searching-microsoft-teams-and-microsoft-365-groups) 
  
### <a name="searching-exchange-public-folders"></a>Durchsuchen öffentlicher Ordner in Exchange

Die integrierte Suche in einem Fall einer personserforderten Person gibt nur E-Mail-Nachrichten zurück, die die subjektfähige Person an einen E-Mail-aktivierten öffentlichen Ordner gesendet hat, oder Nachrichten, die ein anderer Benutzer an einen öffentlichen Ordner gesendet und die datensubjekte Person auch kopiert hat. Es werden keine Nachrichten zurück, die die subjektsubjekte Person in einem öffentlichen Ordner gepostet hat. Um nach Elementen zu suchen, die die person in einem öffentlichen Ordner gepostet hat, können Sie eine separate Inhaltssuche erstellen, die nach elementen sucht, die von der person in einem öffentlichen Ordner veröffentlicht wurden.
  
Hier ist ein verfahren auf hoher Ebene zum Suchen nach Elementen, die die subjektgebte Person in einem öffentlichen Ordner veröffentlicht hat. 
  
1. Öffnen Sie den Fall "DSR", und erstellen Sie eine Suche auf der **Seite "Suche".** 
    
2. Verwenden Sie die folgenden Kriterien, um die Suchabfrage und die zu durchsuchenden Inhaltsorte zu konfigurieren:
    
  - Verwenden Sie **im Feld "Schlüsselwörter"** die folgende Suchabfrage: 
    
    ```powershell
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - Durchsuchen aller öffentlichen Ordner in Exchange
    
  - Nachdem Sie die Suche ausgeführt und abgeschlossen haben, können Sie die Suchergebnisse (wie in Schritt 4 beschrieben) exportieren [und herunterladen.](#step-4-export-the-data) Verwenden Sie die folgenden Einstellungen, um teilweise indizierte Elemente zu exportieren. 
