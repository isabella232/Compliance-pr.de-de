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
hideEdit: true
ms.openlocfilehash: 4782cb47bcd5da86daf11f01cb3a443a9b637c49
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497214"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Ausfallsicherheit von Exchange Online-Daten in Microsoft 365

>[!IMPORTANT]
>Da wir weiterhin auf unterschiedliche Weise investieren, um Postfachinhalte zu erhalten, wird die Rente von In-Place Holds im Exchange Admin Center (EAC) in Exchange Online angekündigt. Ab dem 1. Juli 2020 können Sie keine neuen In-Place erstellen. Sie können jedoch weiterhin die In-Place in der EAC oder mithilfe des **Cmdlets Set-MailboxSearch** in Exchange Online PowerShell verwalten. Ab dem 1. Oktober 2020 können Sie jedoch keine In-Place verwalten. Sie können sie nur in der EAC oder mithilfe des **Cmdlets Remove-MailboxSearch** entfernen. Die In-Place in Exchange Server und Exchange-Hybridbereitstellungen werden weiterhin unterstützt. Weitere Informationen zur Rente von In-Place in Exchange Online finden Sie unter [Retirement of legacy eDiscovery tools](/microsoft-365/compliance/legacy-ediscovery-retirement).

Bei einem Compliance-Archiv bleiben sämtliche Postfachinhalte einschließlich gelöschter Elemente und Originalversionen geänderter Elemente erhalten. Alle diese Postfachelemente werden bei einer [Compliance-eDiscovery](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery)-Suche zurückgegeben. Wenn Sie ein In-Place für das Postfach eines Benutzers platzieren, werden die Inhalte im entsprechenden Archivpostfach (sofern aktiviert) ebenfalls in der Warteschleife platziert und in einer eDiscovery-Suche zurückgegeben.

Es gibt zwei Arten von Beschädigungen, die sich auf eine Exchange-Datenbank auswirken können: physische Beschädigungen, die in der Regel durch Hardwareprobleme (insbesondere Speicherhardware) verursacht werden, und logische Beschädigungen, die aufgrund anderer Faktoren auftreten. Im Allgemeinen gibt es zwei Arten logischer Beschädigungen, die in einer Exchange-Datenbank auftreten können:

- **Logische Beschädigung der Datenbank** – Die Prüfsumme der Datenbankseite stimmt ab, aber die Daten auf der Seite sind logisch falsch. Dies kann auftreten, wenn das Datenbankmodul (das Extensible Storage Engine (ESE)) versucht, eine Datenbankseite zu schreiben, und obwohl das Betriebssystem eine Erfolgsmeldung zurückgibt, werden die Daten entweder nie auf den Datenträger geschrieben oder an die falsche Stelle geschrieben. Dies wird als *verlorene Leerung* bezeichnet. ESE umfasst zahlreiche Features und Garantien, die eine physische Beschädigung einer Datenbank und andere Szenarien für Datenverlust verhindern sollen. Um zu verhindern, dass verloren gegangene Leerungen Daten verlieren, enthält ESE einen Mechanismus zur Erkennung verlorener Leerungen in der Datenbank sowie ein Feature (Wiederherstellung einzelner Seiten), um diese zu korrigieren.
- **Logische Beschädigung speichern** : Daten werden auf eine Weise hinzugefügt, gelöscht oder bearbeitet, die der Benutzer nicht erwartet. Diese Fälle werden durch Drittanbieteranwendungen verursacht. Es ist in der Regel Beschädigung in dem Sinne, dass der Benutzer dies als Beschädigung betrachtet. Der Exchange-Speicher betrachtet die Transaktion, die zur logischen Beschädigung geführt hat, als eine Folge gültiger MAPI-Operationen. Die [In-Place-Speicherfeatures](/exchange/security-and-compliance/create-or-remove-in-place-holds) in Exchange Online bieten Schutz vor logischer Beschädigung des Speichers (da dadurch verhindert wird, dass Inhalte dauerhaft von einem Benutzer oder einer Anwendung gelöscht werden). 

Exchange Online führt mehrere Konsistenzprüfungen für replizierte Protokolldateien sowohl während der Protokollprüfung als auch während der Protokollwiedergabe durch. Diese Konsistenzprüfungen verhindern, dass physische Beschädigungen vom System repliziert werden. Bei der Protokollüberprüfung gibt es beispielsweise eine Überprüfung der physischen Integrität, die die Protokolldatei überprüft und überprüft, ob die in der Protokolldatei aufgezeichnete Prüfsumme der im Arbeitsspeicher generierten Prüfsumme entspricht. Darüber hinaus wird der Protokolldateiheader überprüft, um sicherzustellen, dass die im Protokollkopf aufgezeichnete Protokolldateisignatur mit der der Protokolldatei entspricht. Während der Protokollwiedergabe wird die Protokolldatei weiteren Überprüfungen unterzogen. Beispielsweise enthält der Datenbankheader auch die Protokollsignatur, die mit der Signatur der Protokolldatei verglichen wird, um sicherzustellen, dass sie übereinstimmen. 

Der Schutz vor Beschädigungen von Postfachdaten in Exchange Online wird durch die Verwendung von Exchange Native Data Protection erreicht, einer Ausfallsicherheitsstrategie, die die Replikation auf Anwendungsebene über mehrere Server und mehrere Rechenzentren sowie andere Features nutzt, mit denen Daten aufgrund von Beschädigungen oder anderen Gründen vor Datenverlust geschützt werden. Diese Features umfassen systemeigene Features, die von Microsoft oder der Exchange Online-Anwendung selbst verwaltet werden, z. B.:

- [Datenverfügbarkeitsgruppen](/exchange/back-up-email)
- Single Bit-Korrektur 
- Onlinedatenbankprüfung 
- Erkennung verlorener Leerungen 
- Wiederherstellung einzelner Seiten 
- Postfachreplikationsdienst 
- Protokolldateiprüfungen 
- Bereitstellung im ausfallsicheren Dateisystem 

Weitere Informationen zu den zuvor aufgeführten systemeigenen Features finden Sie unter Hyperlinks, und weitere Informationen und Details zu Elementen ohne Hyperlinks finden Sie im Folgenden. Zusätzlich zu diesen systemeigenen Features umfasst Exchange Online auch Funktionen zur Ausfallsicherheit von Daten, die Kunden verwalten können, z. B.: 
- [Wiederherstellung einzelner Elemente (standardmäßig aktiviert)](/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [In-Situ-Speicher und Beweissicherungsverfahren](/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Aufbewahrung gelöschter Elemente und Soft-Deleted Postfächer (beide standardmäßig aktiviert)](/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Datenbankverfügbarkeitsgruppen 
Jede Postfachdatenbank in Microsoft 365 wird in einer Datenbankverfügbarkeitsgruppe [(Database Availability Group, DAG)](/exchange/back-up-email) gehostet und in geografisch getrennte Rechenzentren innerhalb derselben Region repliziert. Die häufigste Konfiguration sind vier Datenbankkopien in vier Rechenzentren. Einige Regionen verfügen jedoch über weniger Rechenzentren (Datenbanken werden in drei Rechenzentren in Indien und zwei Rechenzentren in Australien und Japan repliziert). In allen Fällen verfügt jede Postfachdatenbank jedoch über vier Kopien, die auf mehrere Rechenzentren verteilt sind, wodurch sichergestellt wird, dass Postfachdaten vor Software-, Hardware- und sogar Datencenterfehlern geschützt sind. 

Von diesen vier Kopien sind drei als hoch verfügbar konfiguriert. Die vierte Kopie ist als eine in [die Jahre 2013 eingestellte Datenbankkopie konfiguriert.](/Exchange/high-availability/manage-ha/activate-lagged-db-copies) Die verschobene Datenbankkopie ist nicht für die Wiederherstellung einzelner Postfächer oder postfachelementwiederherstellung vorgesehen. Ihr Zweck besteht in der Bereitstellung eines Wiederherstellungsmechanismus für das seltene Ereignis einer systemweiten, katastrophalen logischen Beschädigung. 

Lagged database copies in Exchange Online are configured with a seven-day log file replay time. Darüber hinaus ist der Exchange Replay Lag Manager aktiviert, um eine dynamische Protokolldateiwiedergabe für zurückgefahrene Kopien zu ermöglichen, um die Selbstreparatur und Verwaltung des Protokolldateiwachstums zu ermöglichen. Auch wenn in Exchange Online lagged database copies verwendet werden, ist es wichtig zu wissen, dass es sich nicht um eine garantierte Point-in-Time-Sicherung handelt. Lagged database copies in Exchange Online have an availability threshold, typically around 90%, due to periods where the disk containing a lagged copy is lost due to disk failure, the lagged copy becoming a highly available copy (due to automatic play down), as well as the periods where the lagged database copy is rebuilding the log replay queue. 

## <a name="transport-resilience"></a>Ausfallsicherheit des Transports 
Exchange Online umfasst zwei primäre Funktionen für transportresilienz: Schattenredundanz und Sicherheitsnetz. Shadow Redundancy behält eine redundante Kopie einer Nachricht während der Übertragung bei. Das Sicherheitsnetz behält eine redundante Kopie einer Nachricht bei, nachdem die Nachricht erfolgreich zugestellt wurde. 

Bei Shadow Redundancy stellt jeder Exchange Online-Transportserver eine Kopie jeder empfangenen Nachricht vor, bevor er den erfolgreichen Empfang der Nachricht an den sendenden Server bestätigt. Dadurch werden alle Nachrichten in der Transportpipeline während der Übertragung redundant. Wenn Exchange Online feststellt, dass die ursprüngliche Nachricht bei der Übertragung verloren gegangen ist, wird eine redundante Kopie der Nachricht erneut belebt. 

Sicherheitsnetz ist eine Transportwarteschlange, die dem Transportdienst auf einem Postfachserver zugeordnet ist. In dieser Warteschlange werden Kopien von Nachrichten gespeichert, die vom Server erfolgreich verarbeitet wurden. Wenn für eine Postfachdatenbank oder einen Serverfehler das Aktivieren einer veralteten Kopie der Postfachdatenbank erforderlich ist, werden Nachrichten in der Sicherheitsnetzwarteschlange automatisch erneut an die neue aktive Kopie der Postfachdatenbank gesendet. Das Sicherheitsnetz ist ebenfalls redundant, wodurch der Transport als einzelner Fehlerpunkt eliminiert wird. Dabei wird das Konzept eines primären Sicherheitsnetzes und eines Schattensicherheitsnetzes verwendet, wobei, wenn das primäre Sicherheitsnetz länger als 12 Stunden nicht verfügbar ist, Anforderungen erneut übermittelt werden und Nachrichten aus dem Schattensicherheitsnetz erneut übermittelt werden.

Nachrichtenübertragungen aus dem Sicherheitsnetz werden automatisch von der Active Manager-Komponente des Microsoft Exchange-Replikationsdiensts initiiert, der DAGs und Postfachdatenbankkopien verwaltet. Es sind keine manuellen Aktionen erforderlich, um Nachrichten aus dem Sicherheitsnetz erneut zu übermitteln. 

## <a name="single-bit-correction"></a>Single Bit-Korrektur 
ESE enthält einen Mechanismus zum Erkennen und Beheben von Ein-Bit-CRC-Fehlern (auch als Single-Bit-Flips bekannt), die das Ergebnis von Hardwarefehlern sind (und daher physische Beschädigungen darstellen). Wenn diese Fehler auftreten, korrigiert ESE sie automatisch und protokolliert ein Ereignis im Ereignisprotokoll. 

## <a name="online-database-scanning"></a>Onlinedatenbankprüfung 
Die Onlinedatenbanküberprüfung (auch als Datenbanküberprüfungssumme *bezeichnet)* ist der Prozess, bei dem ein ESE eine Datenbankkonsistenzprüfung verwendet, um jede Seite zu lesen und nach Seitenbeschädigungen zu suchen. Der Hauptzweck besteht in der Erkennung physischer Beschädigungen und verlorener Leerungen, die möglicherweise nicht von Transaktionsvorgängen erkannt werden. Die Datenbankprüfung führt auch Absturzvorgänge nach dem Speicher aus. Aufgrund von Abstürze kann Speicherplatz verloren gehen, und die Onlinedatenbankprüfung findet und stellt verlorenen Speicherplatz wiederher. Das System ist so konzipiert, dass jede Datenbank alle sieben Tage vollständig überprüft wird. 

## <a name="lost-flush-detection"></a>Erkennung verlorener Leerungen 
Eine verlorene Leerung tritt auf, wenn ein Datenbankzugriffsvorgang, den das Als abgeschlossen zurückgegebene Datenträgersubsystem/Betriebssystem zurückgegeben hat, nicht tatsächlich auf den Datenträger geschrieben wurde oder am falschen Speicherort geschrieben wurde. Vorfälle mit nicht gelöschten Daten können zu logischen Beschädigungen der Datenbank führen. Um zu verhindern, dass verlorene Leerungen zu datenverlusten führen, enthält ESE einen Mechanismus zur Erkennung verlorener Leerungen. Wenn Datenbankseiten in passive Kopien geschrieben werden, wird eine Überprüfung auf verlorene Leerungen für die aktive Kopie durchgeführt. Wenn eine verlorene Leerung erkannt wird, kann ESE den Prozess mithilfe eines Seitenpatchingprozesses reparieren. 

## <a name="single-page-restore"></a>Wiederherstellung einzelner Seiten 
Die Wiederherstellung einzelner Seiten, auch als *Seitenpatching* bezeichnet, ist ein automatischer Prozess, bei dem beschädigte Datenbankseiten durch fehlerfreie Kopien aus einem fehlerfreien Replikat ersetzt werden. Der Reparaturvorgang für eine beschädigte Seite hängt davon ab, ob die Datenbankkopie aktiv oder passiv ist. Wenn eine aktive Datenbankkopie auf eine beschädigte Seite stößt, kann sie eine Seite aus einem ihrer Replikate kopieren, sofern die kopierte Seite auf dem neuesten Stand ist. Dieser Vorgang erfolgt, indem eine Anforderung für die Seite in den Protokolldatenstrom verschoben wird, der die Grundlage für die Postfachdatenbankreplikation ist. Sobald ein Replikat auf die Seitenanforderung trifft, antwortet es, indem es eine Kopie der Seite an die anfordernde Datenbankkopie sendet. Die Wiederherstellung einer einzelnen Seite stellt auch einen asynchronen Kommunikationsmechanismus für Aktive zum Anfordern einer Seite von Replikaten zur Verfügung, auch wenn die Replikate derzeit offline sind. 

Bei Beschädigungen in einer passiven Datenbankkopie, einschließlich einer zurückgelassenen Datenbankkopie, da sich diese Kopien immer hinter ihrer aktiven Kopie befinden, ist es immer sicher, jede Seite aus der aktiven Kopie in eine passive Kopie zu kopieren. Eine passive Datenbankkopie ist naturweise hoch verfügbar, sodass während des Seitenpatchingprozesses die Protokollwiedergabe angehalten wird, aber das Protokollkopien fortgesetzt wird. Die passive Datenbankkopie ruft eine Kopie der beschädigten Seite aus der aktiven Kopie ab, wartet, bis die Protokolldatei, die die maximal erforderliche Protokollgenerierungsanforderung erfüllt, kopiert und überprüft wird, und patches dann die beschädigte Seite. Nachdem die Seite gepatcht wurde, wird die Protokollwiedergabe fortgesetzt. Der Vorgang ist für die zurückgesetzte Datenbankkopie identisch, mit der Ausnahme, dass die zurückgesetzte Datenbank zunächst alle Protokolldateien wiederholt, die erforderlich sind, um einen patchbaren Zustand zu erreichen. 

## <a name="mailbox-replication-service"></a>Postfachreplikationsdienst 
Das Verschieben von Postfächern ist ein wichtiger Bestandteil der Verwaltung eines großen E-Mail-Diensts. Es gibt immer aktualisierte Technologien und Hardware- und Versionsupgrades, sodass ein robustes, gedrosseltes System zur Verfügung steht, das es unseren Technikern ermöglicht, diese Arbeit zu erledigen und gleichzeitig die Postfachbewegungen für Die Benutzer transparent zu halten (indem sie sicherstellen, dass sie während des gesamten Prozesses online bleiben) und sicherstellen, dass der Prozess entsprechend skaliert wird, wenn postfächer größer und größer werden. 

Der Exchange Mailbox Replication Service (MRS) ist für das Verschieben von Postfächern zwischen Datenbanken verantwortlich. Während des Verschiebens führt MRS eine Konsistenzprüfung für alle Elemente innerhalb des Postfachs durch. Wenn ein Konsistenzproblem gefunden wird, korrigiert MRS entweder das Problem, oder überspringt die beschädigten Elemente, wodurch die Beschädigung aus dem Postfach entfernt wird. 

Da MRS eine Komponente von Exchange Online ist, können wir Änderungen an seinem Code vornehmen, um neue Formen von Beschädigungen zu bekämpfen, die in der Zukunft erkannt werden. Wenn wir z. B. ein Konsistenzproblem erkennen, das von MRS nicht behoben werden kann, können wir die Beschädigung analysieren, den MRS-Code ändern und die Inkonsistenz korrigieren (wenn wir dies verstehen). 

## <a name="log-file-checks"></a>Protokolldateiprüfungen 
Alle von einer Exchange-Datenbank generierten Transaktionsprotokolldateien werden verschiedenen Arten von Konsistenzprüfungen unterzogen. Wenn eine Protokolldatei erstellt wird, wird zunächst ein Bitmuster geschrieben, und dann wird eine Reihe von Protokoll schreibvorgänge ausgeführt. Diese Struktur ermöglicht Exchange Online das Ausführen einer Reihe von Prüfungen (verloren gegangene Flush-, CRC- und andere Überprüfungen), um jede Protokolldatei beim Schreiben zu überprüfen, und erneut, während sie repliziert wird. 

## <a name="deployment-on-resilient-file-system"></a>Bereitstellung im ausfallsicheren Dateisystem 
Um zu verhindern, dass Beschädigungen auf Dateisystemebene auftreten, wird Exchange Online auf reresistenten Dateisystempartitionen (Resilient File System, ReFS) bereitgestellt, um verbesserte Wiederherstellungsfunktionen zu bieten. ReFS ist ein Dateisystem in Windows Server 2012 und höher, das widerstandsfähiger gegen Datenbeschädigungen sein soll, wodurch die Datenverfügbarkeit und -integrität maximiert wird. Insbesondere bietet ReFS Verbesserungen bei der Aktualisierung von Metadaten, was einen besseren Schutz für Daten bietet und Datenbeschädigungsfälle reduziert. Außerdem werden Prüfsummen verwendet, um die Integrität von Dateidaten und Metadaten zu überprüfen, um sicherzustellen, dass Datenbeschädigungen leicht gefunden und repariert werden können. 

Exchange Online nutzt mehrere ReFS-Vorteile: 
- Eine höhere Ausfallsicherheit bei der Datenintegrität bedeutet weniger Datenbeschädigungsvorfälle. Die Reduzierung der Anzahl von Beschädigungsvorfällen bedeutet weniger unnötige Datenbank-Erneutes Senden. 
- Prüfsummen, die auf Metadaten ausgeführt werden, wodurch Beschädigungsfälle früher und deterministisch erkannt werden können, sodass wir Kundendatenbeschädigungen beheben können, bevor graue Fehler auf Datenvolumes auftreten.
- Entwickelt für die gute Arbeit mit großen Datensätzen (Petabytes und größer) ohne Leistungsbelastung
- Unterstützung für andere von Exchange Online verwendete Features, z. B. BitLocker-Verschlüsselung. 

Exchange Online profitiert auch von anderen ReFS-Features: 
- **Integrität (Integrity Streams)** – ReFS speichert Daten so, dass sie vor vielen häufigen Fehlern geschützt werden, die normalerweise zu Datenverlusten führen können. Die Microsoft 365-Suche verwendet Integritätsstreams, um bei der Erkennung früher Datenträgerbeschädigungen und Prüfsummen von Dateiinhalten zu helfen. Das Feature reduziert auch Beschädigungsvorfälle, die durch "Zerrissene Schreibvorgänge" verursacht werden (wenn ein Schreibvorgang aufgrund von Stromausfällen usw. nicht abgeschlossen wird). 
- **Verfügbarkeit (Salvage)** – ReFS priorisiert die Verfügbarkeit von Daten. In der Vergangenheit waren Dateisysteme häufig anfällig für Datenbeschädigungen, bei denen das System zur Reparatur offline geschaltet werden musste. Obwohl selten, wenn Beschädigung auftritt, implementiert ReFS salvage, ein Feature, das die beschädigten Daten aus dem Namespace auf einem Livevolume entfernt und sicherstellt, dass gute Daten nicht durch nicht reparierbare beschädigte Daten beeinträchtigt werden. Das Anwenden des Salvage-Features und das Isolieren von Datenbeschädigungen auf Exchange Online-Datenbankvolumes bedeutet, dass wir nicht betroffene Datenbanken zwischen dem Zeitpunkt der Beschädigung und der Reparaturaktion auf einem beschädigten Volume fehlerfrei halten können. Diese Struktur erhöht die Verfügbarkeit von Datenbanken, die normalerweise von solchen Datenträgerbeschädigungsproblemen betroffen wären. 
