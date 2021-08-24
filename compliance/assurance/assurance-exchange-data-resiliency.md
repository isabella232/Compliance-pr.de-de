---
title: Exchange Online-Datenresilienz in Microsoft 365
description: In diesem Artikel finden Sie eine Erläuterung der verschiedenen Aspekte der Datenresilienz innerhalb Exchange Online und Microsoft 365.
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
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 0e3f050c1f28fa0ca8ac89c8bb8d7151cf9cba10
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481997"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Exchange Online Datenresilienz in Microsoft 365

>[!IMPORTANT]
>Da wir weiterhin auf unterschiedliche Weise in die Aufbewahrung von Postfachinhalten investieren, kündigen wir die Einstellung von In-Place Haltebereichen im Exchange Admin Center (EAC) in Exchange Online an. Ab dem 1. Juli 2020 können Sie keine neuen In-Place-Haltebereiche erstellen. Sie können jedoch weiterhin In-Place Haltebereiche im EAC oder mithilfe des Cmdlets **"Set-MailboxSearch"** in Exchange Online PowerShell verwalten. Ab dem 1. Oktober 2020 können Sie jedoch In-Place Haltebereiche nicht mehr verwalten. Sie können sie nur im Exchange-Verwaltungskonsole (EAC) oder mithilfe des Cmdlets **"Remove-MailboxSearch"** entfernen. Die Verwendung von In-Place Haltebereichen in Exchange Server und Exchange Hybridbereitstellungen wird weiterhin unterstützt. Weitere Informationen zum Ausmustern von In-Place Haltebereichen in Exchange Online finden Sie unter ["Ausmustern von eDiscovery-Tools der Vorversion".](/microsoft-365/compliance/legacy-ediscovery-retirement)

Bei einem Compliance-Archiv bleiben sämtliche Postfachinhalte einschließlich gelöschter Elemente und Originalversionen geänderter Elemente erhalten. Alle diese Postfachelemente werden bei einer [Compliance-eDiscovery](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery)-Suche zurückgegeben. Wenn Sie eine In-Place Aufbewahrung für das Postfach eines Benutzers festlegen, werden die Inhalte im entsprechenden Archivpostfach (sofern aktiviert) ebenfalls in die Warteschleife eingecheckt und in einer eDiscovery-Suche zurückgegeben.

Es gibt zwei Arten von Beschädigungen, die sich auf eine Exchange Datenbank auswirken können: physische Beschädigungen, die in der Regel durch Hardwareprobleme (insbesondere Speicherhardware) verursacht werden, und logische Beschädigungen, die aufgrund anderer Faktoren auftreten. Im Allgemeinen gibt es zwei Arten logischer Beschädigungen, die innerhalb einer Exchange Datenbank auftreten können:

- **Logische Datenbankbeschädigung:** Die Prüfsumme der Datenbankseite stimmt überein, aber die Daten auf der Seite sind logisch falsch. Dies kann passieren, wenn das Datenbankmodul (das Extensible Storage Engine (ESE)) versucht, eine Datenbankseite zu schreiben, und obwohl das Betriebssystem eine Erfolgsmeldung zurückgibt, werden die Daten entweder nie auf den Datenträger geschrieben oder an die falsche Stelle geschrieben. Dies wird als *verlorene Leerung* bezeichnet. ESE enthält zahlreiche Features und Schutzmaßnahmen, die darauf ausgelegt sind, physische Beschädigungen einer Datenbank und andere Szenarien mit Datenverlust zu verhindern. Um zu verhindern, dass verloren gegangene Daten verloren gehen, enthält ESE einen Mechanismus zur Erkennung verlorener Daten in der Datenbank sowie ein Feature (Wiederherstellung auf einer seite), um es zu korrigieren.
- **Store logische Beschädigung:** Daten werden so hinzugefügt, gelöscht oder bearbeitet, dass der Benutzer dies nicht erwartet. Diese Fälle werden durch Drittanbieteranwendungen verursacht. Es handelt sich in der Regel um eine Beschädigung in dem Sinne, dass der Benutzer sie als Beschädigung angibt. Der Exchange-Speicher betrachtet die Transaktion, die zur logischen Beschädigung geführt hat, als eine Folge gültiger MAPI-Operationen. Die [In-Situ-Aufbewahrungsfunktionen](/exchange/security-and-compliance/create-or-remove-in-place-holds) in Exchange Online bieten Schutz vor logischer Beschädigung des Speichers (da dadurch verhindert wird, dass Inhalte von einem Benutzer oder einer Anwendung dauerhaft gelöscht werden). 

Exchange Online führt während der Protokollüberprüfung und der Protokollwiederholung mehrere Konsistenzprüfungen für replizierte Protokolldateien durch. Diese Konsistenzprüfungen verhindern, dass physische Beschädigungen vom System repliziert werden. Beispielsweise gibt es während der Protokollüberprüfung eine Überprüfung der physischen Integrität, die die Protokolldatei überprüft und überprüft, ob die in der Protokolldatei aufgezeichnete Prüfsumme mit der im Arbeitsspeicher generierten Prüfsumme übereinstimmt. Darüber hinaus wird der Protokolldateiheader untersucht, um sicherzustellen, dass die im Protokollheader aufgezeichnete Protokolldateisignatur mit der Signatur der Protokolldatei übereinstimmt. Während der Protokollwiederholung wird die Protokolldatei einer weiteren Prüfung unterzogen. Beispielsweise enthält der Datenbankheader auch die Protokollsignatur, die mit der Signatur der Protokolldatei verglichen wird, um sicherzustellen, dass sie übereinstimmen. 

Der Schutz vor Beschädigung von Postfachdaten in Exchange Online wird mithilfe von Exchange nativen Datenschutz erreicht, einer Resilienzstrategie, die replikation auf Anwendungsebene über mehrere Server und mehrere Rechenzentren hinweg sowie andere Features nutzt, die daten vor Datenverlust aufgrund von Beschädigungen oder anderen Gründen schützen. Diese Features umfassen systemeigene Features, die von Microsoft oder der Exchange Online Anwendung selbst verwaltet werden, z. B.:

- [Datenverfügbarkeitsgruppen](/exchange/back-up-email)
- Einzelbitkorrektur 
- Onlinedatenbanküberprüfung 
- Erkennung von verlorenen Leerungen 
- Wiederherstellung auf einer Seite 
- Postfachreplikationsdienst 
- Protokolldateiüberprüfungen 
- Bereitstellung im ausfallsicheren Dateisystem 

Weitere Informationen zu den zuvor aufgeführten systemeigenen Features erhalten Sie, indem Sie die Hyperlinks auswählen. Weitere Informationen und Details zu Elementen ohne Hyperlinks finden Sie im Folgenden. Zusätzlich zu diesen systemeigenen Features enthält Exchange Online auch Datenresilienzfeatures, die Kunden verwalten können, z. B.: 
- [Wiederherstellung einzelner Elemente (standardmäßig aktiviert)](/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [In-Situ-Speicher und Beweissicherungsverfahren](/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Aufbewahrung von gelöschten Elementen und Soft-Deleted Postfächer (beide standardmäßig aktiviert)](/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Datenbankverfügbarkeitsgruppen 
Jede Postfachdatenbank in Microsoft 365 wird in einer [Datenbankverfügbarkeitsgruppe (Database Availability Group, DAG)](/exchange/back-up-email) gehostet und in geografisch getrennten Rechenzentren innerhalb derselben Region repliziert. Die häufigste Konfiguration sind vier Datenbankkopien in vier Rechenzentren. Einige Regionen verfügen jedoch über weniger Rechenzentren (Datenbanken werden in drei Rechenzentren in Indien und zwei Rechenzentren in Australien und Japan repliziert). Aber in allen Fällen verfügt jede Postfachdatenbank über vier Kopien, die über mehrere Rechenzentren verteilt sind, wodurch sichergestellt wird, dass Postfachdaten vor Software-, Hardware- und sogar Rechenzentrumsfehlern geschützt sind. 

Von diesen vier Kopien sind drei als hoch verfügbar konfiguriert. Die vierte Kopie ist als [verzögerte Datenbankkopie](/Exchange/high-availability/manage-ha/activate-lagged-db-copies)konfiguriert. Die verzögerte Datenbankkopie ist nicht für die wiederherstellung einzelner Postfächer oder Postfachelemente vorgesehen. Der Zweck besteht darin, einen Wiederherstellungsmechanismus für das selten auftretende systemweite, schwerwiegende logische Beschädigungsereignis bereitzustellen. 

Verzögerte Datenbankkopien in Exchange Online werden mit einer Verzögerung von sieben Tagen bei der Wiedergabe der Protokolldatei konfiguriert. Darüber hinaus ist die Exchange Replay Lag Manager aktiviert, um dynamische Protokolldatei-Playdowns für verzögerte Kopien bereitzustellen, damit verzögerte Datenbankkopien sich selbst reparieren und das Wachstum der Protokolldatei verwalten können. Obwohl verzögerte Datenbankkopien in Exchange Online verwendet werden, ist es wichtig zu wissen, dass es sich nicht um eine garantierte Point-in-Time-Sicherung handelt. Verzögerte Datenbankkopien in Exchange Online verfügen über einen Verfügbarkeitsschwellenwert, in der Regel ca. 90 %, aufgrund von Zeiträumen, in denen der Datenträger mit einer verzögerten Kopie aufgrund eines Datenträgerfehlers verloren geht, die verzögerte Kopie zu einer hoch verfügbaren Kopie wird (aufgrund der automatischen Wiedergabe) sowie der Zeiträume, in denen die verzögerte Datenbankkopie die Protokollwiederholungswarteschlange neu erstellt. 

## <a name="transport-resilience"></a>Transportresilienz 
Exchange Online umfasst zwei primäre Transportresilienzfeatures: Schattenredundanz und Sicherheitsnetz. Schattenredundanz behält eine redundante Kopie einer Nachricht bei, während sie sich während der Übertragung befindet. Safety Net behält eine redundante Kopie einer Nachricht bei, nachdem die Nachricht erfolgreich übermittelt wurde. 

Mit Shadow Redundancy erstellt jeder Exchange Online Transportserver eine Kopie jeder empfangenen Nachricht, bevor bestätigt wird, dass die Nachricht erfolgreich an den sendenden Server empfangen wurde. Dadurch werden alle Nachrichten in der Transportpipeline während der Übertragung redundant. Wenn Exchange Online feststellt, dass die ursprüngliche Nachricht während der Übertragung verloren gegangen ist, wird eine redundante Kopie der Nachricht erneut zugestellt. 

Safety Net ist eine Transportwarteschlange, die dem Transportdienst auf einem Postfachserver zugeordnet ist. In dieser Warteschlange werden Kopien von Nachrichten gespeichert, die vom Server erfolgreich verarbeitet wurden. Wenn eine Postfachdatenbank oder ein Serverfehler die Aktivierung einer veralteten Kopie der Postfachdatenbank erfordert, werden Nachrichten in der Safety Net-Warteschlange automatisch an die neue aktive Kopie der Postfachdatenbank übermittelt. Das Sicherheitsnetz ist ebenfalls redundant, wodurch der Transport als einzelner Fehlerpunkt eliminiert wird. Es verwendet das Konzept eines primären Sicherheitsnetzes und eines Schattensicherheitsnetzes. Wenn das primäre Sicherheitsnetz mehr als 12 Stunden nicht verfügbar ist, werden anforderungen erneut gesendet und Nachrichten aus dem Shadow Safety Net erneut übermittelt.

Erneute Übermittlungen von Nachrichten aus dem Sicherheitsnetz werden automatisch von der Active Manager-Komponente des Microsoft Exchange Replikationsdiensts initiiert, der DAGs und Postfachdatenbankkopien verwaltet. Es sind keine manuellen Aktionen erforderlich, um Nachrichten aus dem Safety Net erneut zu übermitteln. 

## <a name="single-bit-correction"></a>Einzelbitkorrektur 
ESE enthält einen Mechanismus zum Erkennen und Beheben von Single-Bit-CRC-Fehlern (auch als Single-Bit-Flips bezeichnet), die das Ergebnis von Hardwarefehlern sind (und daher physische Beschädigungen darstellen). Wenn diese Fehler auftreten, korrigiert ESE diese automatisch und protokolliert ein Ereignis im Ereignisprotokoll. 

## <a name="online-database-scanning"></a>Onlinedatenbanküberprüfung 
Die Onlinedatenbanküberprüfung (auch als *Datenbanküberprüfungs-Summierung* bezeichnet) ist der Vorgang, bei dem ein ESE eine Datenbankkonsistenzprüfung verwendet, um jede Seite zu lesen und auf Seitenbeschädigung zu prüfen. Der Hauptzweck besteht darin, physische Beschädigungen und verloren gegangene Leerungen zu erkennen, die möglicherweise nicht von Transaktionvorgängen erkannt werden. Die Datenbanküberprüfung führt auch Absturzvorgänge nach dem Speicher aus. Aufgrund von Abstürzen kann Speicherplatz verloren gehen, und die Onlinedatenbanküberprüfung findet verlorenen Speicherplatz und stellt diesen wieder her. Das System wurde mit der Erwartung entworfen, dass jede Datenbank einmal alle sieben Tage vollständig gescannt wird. 

## <a name="lost-flush-detection"></a>Erkennung von verlorenen Leerungen 
Eine verloren gegangene Leerung tritt auf, wenn ein Datenbankschreibvorgang, den das Datenträgersubsystem/Betriebssystem, das als abgeschlossen zurückgegeben wird, nicht tatsächlich auf den Datenträger geschrieben wurde oder an der falschen Position geschrieben wurde. Verlorene Leerungsvorfälle können zu einer logischen Beschädigung der Datenbank führen. Um zu verhindern, dass verlorene Daten verloren gehen, enthält ESE einen Mechanismus zur Erkennung verlorener Daten. Wenn Datenbankseiten in passive Kopien geschrieben werden, wird eine Überprüfung auf verloren gegangene Leerungen der aktiven Kopie durchgeführt. Wenn eine verloren gegangene Leerung erkannt wird, kann ESE den Prozess mithilfe eines Seitenpatchingprozesses reparieren. 

## <a name="single-page-restore"></a>Wiederherstellung auf einer Seite 
Die Wiederherstellung einzelner Seiten, auch als *Seitenpatching* bezeichnet, ist ein automatischer Prozess, bei dem beschädigte Datenbankseiten durch fehlerfreie Kopien aus einem fehlerfreien Replikat ersetzt werden. Der Reparaturvorgang für eine beschädigte Seite hängt davon ab, ob die Datenbankkopie aktiv oder passiv ist. Wenn eine aktive Datenbankkopie auf eine beschädigte Seite trifft, kann sie eine Seite aus einem ihrer Replikate kopieren, vorausgesetzt, die kopierte Seite ist auf dem neuesten Stand. Dieser Vorgang wird erreicht, indem eine Anforderung für die Seite in den Protokolldatenstrom eingefügt wird, der die Basis der Postfachdatenbankreplikation ist. Sobald ein Replikat auf die Seitenanforderung trifft, antwortet es, indem es eine Kopie der Seite an die anfordernde Datenbankkopie sendet. Die Wiederherstellung auf einer einzelnen Seite stellt auch einen asynchronen Kommunikationsmechanismus bereit, mit dem die Aktiven eine Seite von Replikaten anfordern können, auch wenn die Replikate derzeit offline sind. 

Im Falle einer Beschädigung in einer passiven Datenbankkopie, einschließlich einer verzögerten Datenbankkopie, da sich diese Kopien immer hinter ihrer aktiven Kopie befinden, ist es immer sicher, jede Seite aus der aktiven Kopie in eine passive Kopie zu kopieren. Eine passive Datenbankkopie ist von Natur aus hoch verfügbar. Daher wird während des Seitenpatchings die Protokollwiederholung angehalten, aber das Kopieren des Protokolls wird fortgesetzt. Die passive Datenbankkopie ruft eine Kopie der beschädigten Seite aus der aktiven Kopie ab, wartet, bis die Protokolldatei, die die maximal erforderliche Protokollgenerierungsanforderung erfüllt, kopiert und überprüft wird, und patchet dann die beschädigte Seite. Nachdem die Seite gepatcht wurde, wird die Wiedergabe des Protokolls fortgesetzt. Der Vorgang ist für die verzögerte Datenbankkopie identisch, mit der Ausnahme, dass die verzögerte Datenbank zuerst alle Protokolldateien wiedergibt, die erforderlich sind, um einen patchbaren Zustand zu erreichen. 

## <a name="mailbox-replication-service"></a>Postfachreplikationsdienst 
Das Verschieben von Postfächern ist ein wichtiger Bestandteil der Verwaltung eines umfangreichen E-Mail-Diensts. Es gibt immer aktualisierte Technologien und Hardware- und Versionsupgrades, sodass ein robustes, gedrosseltes System, das es unseren Technikern ermöglicht, diese Arbeit auszuführen, während das Postfach für Benutzer transparent bleibt (indem sie sicherstellen, dass sie während des gesamten Prozesses online bleiben) wichtig ist und sicherstellen, dass der Prozess ordnungsgemäß skaliert wird, wenn Postfächer größer und größer werden. 

Der Exchange Mailbox Replication Service (MRS) ist für das Verschieben von Postfächern zwischen Datenbanken verantwortlich. Während der Verschiebung führt MRS eine Konsistenzprüfung für alle Elemente innerhalb des Postfachs durch. Wenn ein Konsistenzproblem gefunden wird, korrigiert MRS entweder das Problem oder überspringt die beschädigten Elemente, wodurch die Beschädigung aus dem Postfach entfernt wird. 

Da MRS eine Komponente von Exchange Online ist, können wir Änderungen am Code vornehmen, um neue Formen von Beschädigungen zu beheben, die in Zukunft erkannt werden. Wenn wir beispielsweise ein Konsistenzproblem erkennen, das MRS nicht beheben kann, können wir die Beschädigung analysieren, den MRS-Code ändern und die Inkonsistenz korrigieren (wenn wir wissen, wie dies funktioniert). 

## <a name="log-file-checks"></a>Protokolldateiüberprüfungen 
Alle Transaktionsprotokolldateien, die von einer Exchange Datenbank generiert werden, werden mehreren Konsistenzprüfungen unterzogen. Wenn eine Protokolldatei erstellt wird, wird zunächst ein Bitmuster geschrieben, und dann wird eine Reihe von Protokollschreiben ausgeführt. Diese Struktur ermöglicht es Exchange Online, eine Reihe von Prüfungen (verloren gegangene Leerungen, CRC und andere Prüfungen) auszuführen, um jede Protokolldatei zu überprüfen, während sie geschrieben wurde, und erneut, während sie repliziert wird. 

## <a name="deployment-on-resilient-file-system"></a>Bereitstellung im ausfallsicheren Dateisystem 
Um zu verhindern, dass auf Dateisystemebene Beschädigungen auftreten, wird Exchange Online auf ReFS-Partitionen (Resilient File System) bereitgestellt, um verbesserte Wiederherstellungsfunktionen bereitzustellen. ReFS ist ein Dateisystem in Windows Server 2012 und höher, das so konzipiert ist, dass es stabiler gegen Datenbeschädigung ist, wodurch die Datenverfügbarkeit und -integrität maximiert wird. Insbesondere bietet ReFS Verbesserungen in der Art und Weise, wie Metadaten aktualisiert werden, was einen besseren Schutz für Daten bietet und Datenbeschädigungsfälle reduziert. Außerdem werden Prüfsummen verwendet, um die Integrität von Dateidaten und Metadaten zu überprüfen, um sicherzustellen, dass die Datenbeschädigung leicht gefunden und repariert werden kann. 

Exchange Online nutzt mehrere ReFS-Vorteile: 
- Mehr Resilienz in der Datenintegrität bedeutet weniger Datenbeschädigungsvorfälle. Die Reduzierung der Anzahl von Beschädigungsvorfällen bedeutet weniger unnötige Erneutes Senden von Datenbanken. 
- Prüfsumme, die auf Metadaten ausgeführt wird und die Erkennung von Beschädigungsfällen früher und deterministischer ermöglicht, sodass wir die Beschädigung von Kundendaten beheben können, bevor graue Fehler auf Datenvolumes auftreten.
- Gut geeignet für große Datasets – Petabyte und größer – ohne Leistungseinbußen
- Unterstützung für andere Features, die von Exchange Online verwendet werden, z. B. BitLocker-Verschlüsselung. 

Exchange Online profitieren auch von anderen ReFS-Features: 
- **Integrität (Integrität Streams)** – ReFS speichert Daten so, dass sie vor vielen der häufigsten Fehler geschützt werden, die normalerweise zu Datenverlusten führen können. Microsoft 365 Die Suche verwendet Integrity Streams, um bei der frühzeitigen Erkennung von Datenträgerbeschädigungen und Prüfsummen von Dateiinhalten zu helfen. Das Feature reduziert auch Beschädigungsvorfälle, die durch "Torn Writes" verursacht werden (wenn ein Schreibvorgang aufgrund von Stromausfällen nicht abgeschlossen wird usw.). 
- **Verfügbarkeit (Salvage)** – ReFS priorisiert die Verfügbarkeit von Daten. In der Vergangenheit waren Dateisysteme häufig anfällig für Datenbeschädigungen, bei denen das System zur Reparatur offline geschaltet werden musste. Wenngleich es selten zu einer Beschädigung kommt, implementiert ReFS die Wiederherstellung, ein Feature, das die beschädigten Daten aus dem Namespace auf einem Livevolume entfernt und sicherstellt, dass gute Daten nicht von nicht reparierbaren beschädigten Daten beeinträchtigt werden. Das Anwenden des Salvage-Features und das Isolieren von Datenbeschädigungen auf Exchange Online Datenbankvolumes bedeutet, dass nicht betroffene Datenbanken zwischen dem Zeitpunkt der Beschädigung und Reparatur auf einem beschädigten Volume fehlerfrei bleiben können. Diese Struktur erhöht die Verfügbarkeit von Datenbanken, die normalerweise von solchen Datenträgerbeschädigungsproblemen betroffen wären. 
