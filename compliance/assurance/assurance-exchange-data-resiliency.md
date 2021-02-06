---
title: Exchange Online-Datenresilienz in Microsoft 365
description: In diesem Artikel finden Sie eine Erläuterung der verschiedenen Aspekte der Datenresilienz in Exchange Online und Microsoft 365.
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
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 044bd637241c566a5e44df6522fca4dcab8b8534
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120524"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Exchange Online Data Resiliency in Microsoft 365

>[!IMPORTANT]
>Da wir weiterhin auf unterschiedliche Weise investieren, um Postfachinhalte zu erhalten, kündigen wir die Deaktivierung von In-Place-Archiven im Exchange Admin Center (EAC) in Exchange Online an. Ab dem 1. Juli 2020 können Sie keine neuen In-Place erstellen. Sie können jedoch weiterhin In-Place in der EAC oder mithilfe des **Cmdlets "Set-MailboxSearch"** in Exchange Online PowerShell verwalten. Ab dem 1. Oktober 2020 können Sie jedoch keine In-Place verwalten. Sie können sie nur im EAC oder mithilfe des **Cmdlets "Remove-MailboxSearch"** entfernen. Die In-Place in Exchange Server und Exchange-Hybridbereitstellungen wird weiterhin unterstützt. Weitere Informationen zum Austritt von In-Place in Exchange Online finden Sie unter "Deversion von älteren [eDiscovery-Tools".](/microsoft-365/compliance/legacy-ediscovery-retirement)

Bei einem Compliance-Archiv bleiben sämtliche Postfachinhalte einschließlich gelöschter Elemente und Originalversionen geänderter Elemente erhalten. Alle diese Postfachelemente werden bei einer [Compliance-eDiscovery](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery)-Suche zurückgegeben. Wenn Sie ein In-Place Für das Postfach eines Benutzers aktivieren, wird der Inhalt des entsprechenden Archivpostfachs (sofern aktiviert) ebenfalls archiviert und in einer eDiscovery-Suche zurückgegeben.

Es gibt zwei Arten von Beschädigungen, die sich auf eine Exchange-Datenbank auswirken können: physische Beschädigungen, die in der Regel durch Hardwareprobleme (insbesondere Speicherhardware) verursacht werden, und logische Beschädigungen, die aufgrund anderer Faktoren auftreten. Im Allgemeinen gibt es zwei Arten logischer Beschädigungen, die in einer Exchange-Datenbank auftreten können:

- **Logische Beschädigung der Datenbank:** Die Prüfsumme der Datenbankseite stimmt ab, aber die Daten auf der Seite sind logisch falsch. Dies kann auftreten, wenn das Datenbankmodul (das Extensible Storage Engine (ESE)) versucht, eine Datenbankseite zu schreiben, und obwohl das Betriebssystem eine Erfolgsmeldung zurückgibt, werden die Daten entweder nie auf den Datenträger geschrieben oder an den falschen Ort geschrieben. Dies wird als *verlorene Leerung* bezeichnet. ESE umfasst zahlreiche Features und Schutzmaßnahmen, die darauf ausgelegt sind, physische Beschädigungen einer Datenbank und andere Datenverlustszenarien zu verhindern. Um zu verhindern, dass verlorene Leerungen Daten verlieren, enthält ESE einen Erkennungsmechanismus für verlorene Leerungen in der Datenbank sowie ein Feature (Einzelseitenwiederherstellung), um dies zu korrigieren.
- **Logische Beschädigung speichern** – Daten werden auf eine Weise hinzugefügt, gelöscht oder bearbeitet, die der Benutzer nicht erwartet. Diese Fälle werden durch Drittanbieteranwendungen verursacht. In der Regel ist dies eine Beschädigung in dem Sinne, dass der Benutzer sie als Beschädigung betrachtet. Der Exchange-Speicher betrachtet die Transaktion, die zur logischen Beschädigung geführt hat, als eine Folge gültiger MAPI-Operationen. Das [In-Place Hold-Features](/exchange/security-and-compliance/create-or-remove-in-place-holds) in Exchange Online bietet Schutz vor logischer Beschädigung des Speichers (da dadurch verhindert wird, dass Inhalte von einem Benutzer oder einer Anwendung dauerhaft gelöscht werden). 

Exchange Online führt mehrere Konsistenzprüfungen für replizierte Protokolldateien sowohl während der Protokollüberprüfung als auch der Protokollwiedergabe durch. Diese Konsistenzprüfungen verhindern, dass physische Beschädigungen vom System repliziert werden. Während der Protokollüberprüfung gibt es beispielsweise eine Überprüfung der physischen Integrität, die die Protokolldatei überprüft und überprüft, ob die in der Protokolldatei aufgezeichnete Prüfsumme der im Arbeitsspeicher generierten Prüfsumme entspricht. Darüber hinaus wird der Protokolldateiheader überprüft, um sicherzustellen, dass die im Protokollheader aufgezeichnete Protokolldateisignatur mit der Protokolldatei entspricht. Während der Protokollwiedergabe wird die Protokolldatei weiter überprüft. Beispielsweise enthält der Datenbankheader auch die Protokollsignatur, die mit der Signatur der Protokolldatei verglichen wird, um sicherzustellen, dass sie übereinstimmen. 

Der Schutz vor Beschädigungen von Postfachdaten in Exchange Online wird mithilfe von Exchange Native Data Protection erreicht, einer Resilienzstrategie, die die Replikation auf Anwendungsebene über mehrere Server und mehrere Rechenzentren sowie andere Features nutzt, die dazu beitragen, dass Daten aufgrund von Beschädigungen oder anderen Gründen nicht verloren gehen. Diese Features umfassen systemeigene Features, die von Microsoft oder der Exchange Online-Anwendung selbst verwaltet werden, z. B.:

- [Datenverfügbarkeitsgruppen](/exchange/back-up-email)
- Single-Bit-Korrektur 
- Onlinedatenbankprüfung 
- Erkennung verlorener Leerungen 
- Einzelseitenwiederherstellung 
- Postfachreplikationsdienst 
- Protokolldateiprüfungen 
- Bereitstellung im ausfallsicheren Dateisystem 

Weitere Informationen zu den zuvor aufgeführten systemeigenen Features finden Sie unter "Hyperlinks". Weitere Informationen und Details zu Elementen ohne Hyperlinks finden Sie in den folgenden Themen. Zusätzlich zu diesen systemeigenen Features enthält Exchange Online auch Funktionen zur Datenresilienz, die Kunden verwalten können, z. B.: 
- [Wiederherstellung einzelner Elemente (standardmäßig aktiviert)](/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [In-Situ-Speicher und Beweissicherungsverfahren](/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Aufbewahrung gelöschter Elemente und Soft-Deleted Postfächer (beide standardmäßig aktiviert)](/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Database Availability Groups 
Jede Postfachdatenbank in Microsoft 365 wird in einer Database [Availability Group (DAG)](/exchange/back-up-email) gehostet und in geografisch getrennte Rechenzentren innerhalb derselben Region repliziert. Die am häufigsten verwendeten Konfigurationen sind vier Datenbankkopien in vier Rechenzentren; Einige Regionen verfügen jedoch über weniger Rechenzentren (Datenbanken werden in drei Rechenzentren in Indien und zwei Rechenzentren in Australien und Japan repliziert). In allen Fällen verfügt jede Postfachdatenbank jedoch über vier Kopien, die auf mehrere Rechenzentren verteilt sind, wodurch sichergestellt wird, dass Postfachdaten vor Software-, Hardware- und sogar Rechenzentrumsfehlern geschützt sind. 

Von diesen vier Kopien sind drei als hoch verfügbar konfiguriert. Die vierte Kopie ist als eine [ladte Datenbankkopie konfiguriert.](/Exchange/high-availability/manage-ha/activate-lagged-db-copies) Die verschobene Datenbankkopie ist nicht für die Wiederherstellung einzelner Postfächer oder Postfachelement vorgesehen. Ihr Zweck besteht in der Bereitstellung eines Wiederherstellungsmechanismus für das seltenen Ereignis einer systemweiten, katastrophalen logischen Beschädigung. 

Bei ladierten Datenbankkopien in Exchange Online wird eine Wiedergabeverzögerung von sieben Tagen für Protokolldateien konfiguriert. Darüber hinaus ist der Exchange Replay Lag Manager aktiviert, um die dynamische Protokolldateiwiedergabe für ladte Kopien zu ermöglichen, damit sich verzögerungende Datenbankkopien selbst reparieren und das Wachstum der Protokolldateien verwalten können. Auch wenn in Exchange Online ladte Datenbankkopien verwendet werden, ist es wichtig zu wissen, dass sie keine garantierte Zeitpunktsicherung sind. Bei ladten Datenbankkopien in Exchange Online liegt der Verfügbarkeitsschwellenwert in der Regel bei ca. 90 %, da der Datenträger mit einer zurückgefahrenen Kopie aufgrund eines Datenträgerfehlers verloren geht, die zurückgespeicherte Kopie (aufgrund der automatischen Wiedergabe) zu einer hochverf genden Kopie wird, sowie aufgrund der Zeiträume, in denen die Protokollwiedergabewarteschlange von der zurückgespeicherten Datenbankkopie neu erstellt wird. 

## <a name="transport-resilience"></a>Transportresilienz 
Exchange Online umfasst zwei primäre Transportresilienzfeatures: Shadow-Redundanz und Sicherheitsnetz. Die Schattenredundanz behält eine redundante Kopie einer Nachricht während der Übertragung bei. Das Sicherheitsnetz bewahrt eine redundante Kopie einer Nachricht auf, nachdem die Nachricht erfolgreich zugestellt wurde. 

Mit der Shadow-Redundanz stellt jeder Exchange Online-Transport-Server eine Kopie jeder nachricht, die er empfängt, bevor er den erfolgreichen Empfang der Nachricht an den sendenden Server bestätigt. Dadurch werden alle Nachrichten in der Transportpipeline während der Übertragung redundant. Wenn Exchange Online ermittelt, dass die ursprüngliche Nachricht bei der Übertragung verloren gegangen ist, wird eine redundante Kopie der Nachricht erneut zugestellt. 

Das Sicherheitsnetz ist eine Transportwarteschlange, die dem Transportdienst auf einem Postfachserver zugeordnet ist. In dieser Warteschlange werden Kopien von Nachrichten gespeichert, die vom Server erfolgreich verarbeitet wurden. Wenn für eine Postfachdatenbank oder ein Serverausfall die Aktivierung einer veralteten Kopie der Postfachdatenbank erforderlich ist, werden Nachrichten in der Warteschlange für das Sicherheitsnetz automatisch erneut an die neue aktive Kopie der Postfachdatenbank übermittelt. Das Sicherheitsnetz ist ebenfalls redundant, wodurch der Transport als einzelne Fehlerstelle eliminiert wird. Es wird das Konzept eines primären Sicherheitsnetzes und eines Schattensicherheitsnetzes verwendet, wobei Nachrichten aus dem Schattensicherheitsnetz erneut übermittelt werden, wenn das primäre Sicherheitsnetz länger als 12 Stunden nicht verfügbar ist.

Erneute Nachrichtenübertragungen aus dem Sicherheitsnetz werden automatisch von der Active -Manager-Komponente des Microsoft Exchange-Replikationsdiensts initiiert, der DAGs und Postfachdatenbankkopien verwaltet. Es sind keine manuellen Aktionen erforderlich, um Nachrichten aus dem Sicherheitsnetz erneut zu übermitteln. 

## <a name="single-bit-correction"></a>Single-Bit-Korrektur 
ESE enthält einen Mechanismus zum Erkennen und Beheben von Single-Bit-CRC-Fehlern (auch als Single-Bit-Flips bekannt), die das Ergebnis von Hardwarefehlern sind (und daher physische Beschädigungen darstellen). Wenn diese Fehler auftreten, korrigiert ESE diese automatisch und protokolliert ein Ereignis im Ereignisprotokoll. 

## <a name="online-database-scanning"></a>Onlinedatenbankprüfung 
Die Onlinedatenbanküberprüfung (auch als Datenbanküberprüfungssumme *bezeichnet)* ist der Prozess, bei dem ein ESE eine Datenbankkonsistenzprüfung verwendet, um jede Seite zu lesen und auf Eine Seitenbeschädigung zu prüfen. Der Hauptzweck besteht in der Erkennung physischer Beschädigungen und verlorener Leerungen, die möglicherweise nicht von Transaktionsvorgängen erkannt werden. Die Datenbankprüfung führt auch Nachspeicherabstürze aus. Aufgrund von Abstürzen kann Speicherplatz verloren gehen, und bei der Onlinedatenbankprüfung wird verlorener Speicherplatz gefunden und wiederhergestellt. Das System ist so konzipiert, dass jede Datenbank alle sieben Tage vollständig überprüft wird. 

## <a name="lost-flush-detection"></a>Erkennung verlorener Leerungen 
Eine verloren gegangene Leerung tritt auf, wenn ein Datenbank-Schreibvorgang, den das Datenträgersubsystem/Betriebssystem als abgeschlossen zurückgegeben hat, nicht tatsächlich auf den Datenträger geschrieben wurde oder am falschen Speicherort geschrieben wurde. Verlorene Leerungsvorfälle können zu logischen Beschädigungen der Datenbank führen. Um zu verhindern, dass verlorene Leerungen zu verlorenen Daten führen, bietet ESE einen Mechanismus zur Erkennung verlorener Leerungen. Wenn Datenbankseiten in passive Kopien geschrieben werden, wird eine Überprüfung auf verlorene Leerungen der aktiven Kopie durchgeführt. Wenn eine verlorene Leerung erkannt wird, kann ESE den Prozess mithilfe eines Seitenpatchingprozesses reparieren. 

## <a name="single-page-restore"></a>Einzelseitenwiederherstellung 
Die Wiederherstellung einzelner Seiten, auch als *Seitenpatching* bezeichnet, ist ein automatischer Prozess, bei dem beschädigte Datenbankseiten durch fehlerfreie Kopien aus einem fehlerfreien Replikat ersetzt werden. Der Reparaturprozess für eine beschädigte Seite hängt davon ab, ob die Datenbankkopie aktiv oder passiv ist. Wenn eine aktive Datenbankkopie auf eine beschädigte Seite stößt, kann sie eine Seite aus einem ihrer Replikate kopieren, sofern die kopierte Seite auf dem neuesten Stand ist. Zu diesem Vorgang wird eine Anforderung für die Seite in den Protokolldatenstrom verschoben, der die Grundlage für die Replikation der Postfachdatenbank ist. Sobald ein Replikat die Seitenanforderung trifft, antwortet es, indem es eine Kopie der Seite an die anfordernde Datenbankkopie sendet. Die Wiederherstellung einzelner Seiten bietet auch einen asynchronen Kommunikationsmechanismus, mit dem die aktiven Mitglieder eine Seite von Replikaten anfordern können, auch wenn die Replikate derzeit offline sind. 

Im Falle einer Beschädigung einer passiven Datenbankkopie, einschließlich einer zurückgelassenen Datenbankkopie, da sich diese Kopien immer hinter ihrer aktiven Kopie befinden, ist es immer sicher, jede Seite von der aktiven Kopie in eine passive Kopie zu kopieren. Eine passive Datenbankkopie ist naturweise hoch verfügbar, daher wird die Protokollwiedergabe während des Seitenpatchingprozesses angehalten, aber das Kopieren von Protokollen wird fortgesetzt. Die passive Datenbankkopie ruft eine Kopie der beschädigten Seite von der aktiven Kopie ab, wartet, bis die Protokolldatei, die die maximal erforderliche Protokollgenerierungsanforderung erfüllt, kopiert und überprüft wird, und patches dann die beschädigte Seite. Nachdem die Seite gepatcht wurde, wird die Protokollwiedergabe fortgesetzt. Der Vorgang ist für die zurückgesetzte Datenbankkopie identisch, mit der Ausnahme, dass von der zurückgesetzten Datenbank zunächst alle Protokolldateien wiedergegeben werden, die zum Erreichen eines patchbaren Zustands erforderlich sind. 

## <a name="mailbox-replication-service"></a>Postfachreplikationsdienst 
Das Verschieben von Postfächern ist ein wichtiger Bestandteil der Verwaltung eines großen E-Mail-Diensts. Es gibt immer aktualisierte Technologien sowie Hardware- und Versionsupgrades. Daher ist ein robustes, gedrosseltes System erforderlich, mit dem unsere Techniker diese Arbeit ausführen können, während die Postfachbewegungen für Benutzer transparent bleiben (indem sichergestellt wird, dass sie während des gesamten Prozesses online bleiben) und dass der Prozess entsprechend skaliert wird, sobald die Postfächer größer und größer werden. 

Der Exchange-Postfachreplikationsdienst ist für das Verschieben von Postfächern zwischen Datenbanken zuständig. Während des Verschiebens führt mrs eine Konsistenzprüfung für alle Elemente innerhalb des Postfachs durch. Wenn ein Konsistenzproblem gefunden wird, korrigiert mrs das Problem oder überspringt die beschädigten Elemente, wodurch die Beschädigung aus dem Postfach entfernt wird. 

Da MRS eine Komponente von Exchange Online ist, können wir Änderungen am Code vornehmen, um neue Formen von Beschädigungen zu adressiert, die in Zukunft erkannt werden. Wenn z. B. ein Konsistenzproblem erkannt wird, das von MRS nicht behoben werden kann, können wir die Beschädigung analysieren, den Mrs.-Code ändern und die Inkonsistenz korrigieren (wenn wir dies verstehen). 

## <a name="log-file-checks"></a>Protokolldateiprüfungen 
Alle von einer Exchange-Datenbank generierten Transaktionsprotokolldateien werden verschiedenen Arten von Konsistenzprüfungen unterzogen. Wenn eine Protokolldatei erstellt wird, wird zunächst ein Bitmuster geschrieben, und anschließend wird eine Reihe von Protokoll schreibvorgängen ausgeführt. Diese Struktur ermöglicht Exchange Online das Ausführen einer Reihe von Prüfungen (verlorene Leerung, CRC und andere Überprüfungen), um jede Protokolldatei beim Schreiben und erneut bei der Replikation zu überprüfen. 

## <a name="deployment-on-resilient-file-system"></a>Bereitstellung im ausfallsicheren Dateisystem 
Um zu verhindern, dass Beschädigungen auf Dateisystemebene auftreten, wird Exchange Online auf ReFS (Resilient File System)-Partitionen bereitgestellt, um verbesserte Wiederherstellungsfunktionen zu bieten. ReFS ist ein Dateisystem in Windows Server 2012 und höher, das stabiler gegen Datenbeschädigungen ist, wodurch die Datenverfügbarkeit und -integrität maximiert wird. ReFS bietet insbesondere Verbesserungen bei der Art und Weise, wie Metadaten aktualisiert werden, was einen besseren Schutz für Daten bietet und Datenbeschädigungsfälle reduziert. Außerdem werden Prüfsummen verwendet, um die Integrität von Dateidaten und Metadaten zu überprüfen, um sicherzustellen, dass Datenbeschädigungen leicht gefunden und repariert werden können. 

Exchange Online nutzt mehrere ReFS-Vorteile: 
- Mehr Resilienz in der Datenintegrität bedeutet weniger Datenbeschädigungsvorfälle. Eine Verringerung der Anzahl von Beschädigungsvorfällen bedeutet weniger unnötige erneutes Senden von Datenbanken. 
- Prüfsummen, die auf Metadaten ausgeführt werden und die Erkennung von Beschädigungsfällen früher und deterministisch ermöglichen, sodass wir Kundendatenbeschädigungen beheben können, bevor graue Fehler auf Datenvolumes auftreten.
- Entwickelt für die gute Arbeit mit großen Datensätzen – Petabytes und größer – ohne Auswirkungen auf die Leistung
- Unterstützung für andere von Exchange Online verwendete Features, z. B. BitLocker-Verschlüsselung. 

Exchange Online profitiert auch von anderen ReFS-Features: 
- **Integrität (Integrity Streams)** – ReFS speichert Daten auf eine Weise, die sie vor vielen häufigen Fehlern schützt, die normalerweise zu Datenverlusten führen können. Die Microsoft 365-Suche verwendet Integritätsstreams, um eine frühzeitige Erkennung von Datenträgerbeschädigungen und Prüfsummen von Dateiinhalten zu unterstützen. Mit diesem Feature werden auch Beschädigungsvorfälle reduziert, die durch "Schreiben von Schreibvorgängen" verursacht werden (wenn ein Schreibvorgang aufgrund von Stromausfällen usw. nicht abgeschlossen wird). 
- **Verfügbarkeit (Restwert):** ReFS priorisiert die Verfügbarkeit von Daten. In der Vergangenheit waren Dateisysteme häufig anfällig für Datenbeschädigungen, die erforderten, dass das System zur Reparatur offline geschaltet wurde. Wenngleich selten, implementiert ReFS die Restfunktion, die die beschädigten Daten aus dem Namespace auf einem Livevolume entfernt und sicherstellt, dass gute Daten nicht von nicht reparierbaren beschädigten Daten beeinträchtigt werden. Das Anwenden des Restfunktionsfeatures und das Isolieren von Datenbeschädigungen auf Exchange Online-Datenbankvolumes bedeutet, dass nicht betroffene Datenbanken zwischen dem Zeitpunkt der Beschädigung und der Reparaturaktion fehlerfrei auf einem beschädigten Volume gespeichert werden können. Diese Struktur erhöht die Verfügbarkeit von Datenbanken, die normalerweise von solchen Datenträgerbeschädigungsproblemen betroffen wären. 
