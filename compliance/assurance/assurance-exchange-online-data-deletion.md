---
title: Microsoft 365 Exchange Online Löschen von Daten
description: Erfahren Sie, wie vorläufige und feste Datenlöschungen für Postfächer und Elemente in Postfächern in Exchange Online behandelt werden.
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
ms.openlocfilehash: 9dd365e075226d8fdbfd1a9f9e371df2668f814d
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481987"
---
# <a name="exchange-online-data-deletion-in-microsoft-365"></a>Exchange Online der Datenlöschung in Microsoft 365

Innerhalb Exchange Online gibt es zwei Arten von Löschungen: vorläufige Löschungen und endgültige Löschungen. Dies gilt sowohl für Postfächer als auch für Elemente innerhalb eines Postfachs.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Vorläufig gelöschte und endgültig gelöschte Postfächer

Ein vorläufig gelöschtes Benutzerpostfach ist ein Postfach, das mit dem Microsoft 365 Admin Center oder dem Cmdlet Remove-Mailbox gelöscht wurde und sich noch weniger als 30 Tage im Azure Active Directory Papierkorb befindet. Ein Postfach kann auf eine der folgenden Arten vorläufig gelöscht werden:

- Die dem Benutzerpostfach zugeordnete Azure Active Directory Benutzerkonto wird vorläufig gelöscht (das Benutzerobjekt liegt außerhalb des Gültigkeitsbereichs oder im Papierkorbcontainer).
- Das dem Benutzerpostfach zugeordnete Azure Active Directory Benutzerkonto wurde endgültig gelöscht, aber das Exchange Online Postfach unterliegt einem Beweissicherungsverfahren oder einer eDiscovery-Aufbewahrungspflicht.
- Das dem Benutzerpostfach zugeordnete Azure Active Directory Benutzerkonto wurde innerhalb der letzten 30 Tage gelöscht. Dies ist die maximale Aufbewahrungsdauer, Exchange Online das Postfach in einem vorläufig gelöschten Zustand belässt, bevor es endgültig gelöscht und nicht wiederhergestellt werden kann.

Ein endgültig gelöschtes Benutzerpostfach ist ein Postfach, das auf eine der folgenden Arten gelöscht wurde:

- Das Benutzerpostfach wurde seit mehr als 30 Tagen vorläufig gelöscht, und die zugeordnete Azure Active Directory Benutzer wurde endgültig gelöscht. Alle Postfachinhalte wie E-Mails, Kontakte und Dateien werden dauerhaft gelöscht.
- Das dem Benutzerpostfach zugeordnete Benutzerkonto wurde aus dem Azure Active Directory endgültig gelöscht. Das Benutzerpostfach wird nun in Exchange Online vorläufig gelöscht und bleibt 30 Tage lang in einem vorläufig gelöschten Zustand. Wenn im Zeitraum von 30 Tagen ein neuer Azure Active Directory Benutzer vom ursprünglichen Empfängerkonto mit demselben **ExchangeGuid-** oder **ArchiveGuid-Konto** synchronisiert wird und dieses neue Konto für Exchange Online lizenziert ist, führt dies zu einem endgültigen Löschen des ursprünglichen Benutzerpostfachs. Alle Postfachinhalte wie E-Mails, Kontakte und Dateien werden dauerhaft gelöscht.
- Ein vorläufig gelöschtes Postfach wird mit **remove-Mailbox -PermanentlyDelete** gelöscht.

Bei den oben genannten Löschszenarien wird davon ausgegangen, dass sich das Benutzerpostfach nicht in einem der Haltestatus befindet, z. B. Beweissicherung für juristische Zwecke oder eDiscovery-Aufbewahrung. Wenn für das Postfach eine Aufbewahrungsart vorhanden ist, kann das Postfach nicht gelöscht werden. Für alle Empfängertypen von E-Mail-Benutzern werden alle [Aufbewahrungseinstellungen](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) ignoriert und haben keine Auswirkungen auf endgültige Löschungen oder vorläufige Löschungen.

## <a name="soft-deleted-and-hard-deleted-items"></a>Vorläufig gelöschte und endgültig gelöschte Elemente

Wenn ein Benutzer ein Postfachelement löscht (z. B. eine E-Mail-Nachricht, einen Kontakt, einen Kalendertermin oder eine Aufgabe), wird das Element in den Ordner "Wiederherstellbare Elemente" und in einen Unterordner mit dem Namen "Deletions" verschoben. Dies wird als vorläufige Löschung bezeichnet. Die Aufbewahrungsdauer für gelöschte Elemente im Ordner Löschvorgänge hängt von der Aufbewahrungsdauer für gelöschte Elemente ab, die für das Postfach festgelegt ist. Ein Exchange Online Postfach behält gelöschte Elemente standardmäßig 14 Tage lang bei, aber Exchange Online Administratoren können diese Einstellung ändern, um den Zeitraum auf maximal 30 Tage zu erhöhen. (Ausführliche Schritte zum Erhöhen des Aufbewahrungszeitraums für gelöschte Elemente für ein Exchange Online Postfach finden Sie unter [Ändern, wie lange dauerhaft gelöschte Elemente für ein Exchange Online Postfach aufbewahrt werden.)](/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention) Benutzer können gelöschte Elemente wiederherstellen oder löschen, bevor die Aufbewahrungszeit für ein gelöschtes Element abläuft. Dazu verwenden sie das Feature "Gelöschte Elemente wiederherstellen" in Microsoft Outlook oder Outlook im Web.

Wenn ein Benutzer ein gelöschtes Element mithilfe der Funktion "Gelöschte Elemente wiederherstellen" in Outlook oder Outlook im Web löscht, wird dies als endgültiger Löschvorgang bezeichnet. In Exchange Online ist die Wiederherstellung einzelner Elemente standardmäßig aktiviert, wenn ein neues Postfach erstellt wird, sodass ein Administrator dauerhaft gelöschte Elemente [wiederherstellen](/Exchange/recipients/user-mailboxes/recover-deleted-messages) kann, bevor der Aufbewahrungszeitraum für gelöschte Elemente abläuft. Zudem werden Kopien des ursprünglichen Elements, wenn die Wiederherstellung einzelner Elemente aktiviert ist, beibehalten, sofern die Nachricht durch einen Benutzer oder Prozess geändert wird.

## <a name="page-zeroing"></a>Seiten zeroing

*Zeroing* ist ein Sicherheitsmechanismus, der entweder Nullen oder ein binäres Muster über gelöschte Daten schreibt, sodass die Wiederherstellung der gelöschten Daten schwieriger ist. In Exchange Online verwenden *Postfachdatenbanken Seiten* als Speichereinheit und implementieren einen Überschreibenprozess, der als *Seiten-Nulling* bezeichnet wird. Das Nullen von Seiten ist standardmäßig aktiviert und kann von Kunden oder von Microsoft nicht deaktiviert werden. Vorgänge zum Nullen von Seiten werden in den Transaktionsprotokolldateien aufgezeichnet, sodass alle Kopien einer bestimmten Datenbank auf ähnliche Weise mit Seiten null versehen werden. Durch das Nullen einer Seite in einer aktiven Datenbankkopie wird die Seite bei passiven Kopien der Datenbank mit Null versehen.

Beim Nullen von Seiten wird ein binäres Muster über endgültig gelöschte Datensätze geschrieben. Das Seiten-Null-Muster ist spezifisch für ESE-Vorgänge (Extensible Storage Engine) (der Name des internen Datenbankmoduls, das von Servern in Exchange Online verwendet wird) und unterscheidet sich für Laufzeitvorgänge im Vergleich zu Wartungsvorgängen für Hintergrunddatenbanken. (Die Wartung von Hintergrunddatenbanken ist ein Prozess, bei dem jede Datenbank kontinuierlich überprüft und überprüft wird. Die primäre Funktion besteht in der Überprüfung von Datenbankseiten, aber es behandelt auch das Bereinigen von Speicherplatz und das Nullen von Datensätzen und Seiten, die aufgrund eines Store Absturzes nicht mit Null versehen wurden.)

In der folgenden Tabelle sind die Füllmuster zusammengestellt, die für die speziellen Laufzeitvorgänge verwendet werden.

| ESE-Laufzeitvorgang   | Füllmuster |
|--------------------------|--------------|
| Ersetzen                  | R            |
| Datensatz/Long-Wert löschen | D            |
| Freigegebener Seitenspeicherplatz         | H            |

In der folgenden Tabelle sind die Füllmuster zusammengestellt, die den speziellen Vorgängen entsprechen, die bei der Hintergrundwartung einer ESE-Datenbank ausgeführt werden.

| Hintergrundwartungsvorgang für ESE-Datenbank | Füllmuster |
|-----------------------------------------------|--------------|
| Datensatz löschen                                 | D            |
| Long-Wert löschen                             | L            |
| Freigegebener Seitenspeicherplatz einer teilweise verwendeten Seite       | Z            |
| Freigegebener Seitenspeicherplatz einer nicht verwendeten Seite               | U            |

### <a name="page-zeroing-process"></a>Prozess zum Nullen von Seiten

Der Prozess für das Nullen von Seiten hängt vom Löschszenario ab. In der folgenden Tabelle ist für verschiedene Datenbanklöschszenarien erläutert, wann Funktionen zum unwiderruflichen Löschen ausgeführt werden.

| Datenbanklöschszenario | ESE-Vorgang und -Zeitrahmen für unwiderrufliches Löschen von Datenbankdaten |
|:--------------------------|:------------------------------------------------|
| Das Element läuft basierend auf dem Aufbewahrungszeitraum für gelöschte Elemente ab. | Ein asynchroner Thread schreibt ein binäres Muster über die gelöschten Daten. Diese Aktion wird innerhalb von Millisekunden nach dem Datensatzlöschvorgang ausgeführt. Wenn der Store-Prozess abstürzt, während die asynchrone Bereinigung noch aussteht (oder die Bereinigung des Versionsspeichers aufgrund des Versionsspeichers abgebrochen wird), wird die Nullierung abgeschlossen, wenn die Wartung der Hintergrunddatenbank diesen Abschnitt der Datenbank verarbeitet. |
| Ansichtsszenario: Ablauf von Elementen aus Outlook/Outlook im Web Ordneransicht (z. B. Unterhaltungsansicht) | Unwiderrufliches Löschen von Daten wird ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |
| Szenario "Postfach verschieben/Postfach löschen": Quellpostfach gelöscht (Ablauf des gelöschten Postfachs) | Unwiderrufliches Löschen von Daten wird ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Postfachdatentypen ohne Seiten zeroing

Für die folgenden Postfachdatentypen gibt es keine Bestimmungen für das Nullen von Seiten:

- **Postfachdatenbanktransaktionsprotokolle** – Wenn Transaktionsprotokolle im Rahmen des normalen Betriebs gelöscht werden, gibt es keinen Prozess zum Nullen der Blöcke im Dateisystem, in denen die gelöschten Protokolldateien gespeichert wurden. Es ist wahrscheinlich, dass das Dateisystem diesen freien Speicherplatz für neu erstellte Protokolle schnell wieder nutzt, aber es gibt keine Garantie dafür.
- **Inhaltsindexkatalogdateien** – Exchange Online verwendet Search Foundation (auch als FAST bezeichnet) für die Suchindizierungsfunktionalität. Der Suchindexkatalog besteht aus mehreren Dutzend Dateien, die auf demselben Volume wie die Postfachdatenbankdatei gespeichert sind. Wenn eine Nachricht endgültig aus der Postfachdatenbank gelöscht wird, wird der zugeordnete Inhalt im Suchkatalog nicht sofort gelöscht. Das Löschen von Inhalten erfolgt, wenn Search Foundation einen Schatten (oder master merge) von vielen kleinen Katalogdateien in einer einzigen größeren Datei ausführt. Nach Abschluss der Masterzusammenführung werden die kleineren Katalogdateien gelöscht. Es gibt keinen Prozess zum Nullen der Blöcke, die die gelöschten Katalogdateien gespeichert haben.

## <a name="continuous-replication"></a>Fortlaufende Replikation

Die fortlaufende Replikation (auch als Protokollversand und -wiedergabe bezeichnet) ist eine Technologie in Exchange Online, die Kopien jeder Postfachdatenbank erstellt und verwaltet, um hohe Verfügbarkeit, Ausfallsicherheit und Notfallwiederherstellung zu gewährleisten. Bei der kontinuierlichen Replikation wird die Exchange Server Datenbankabstürzwiederherstellungsunterstützung verwendet, um Eine Technologie bereitzustellen, die asynchrone Aktualisierungen einer oder mehrerer Kopien einer Postfachdatenbank durchführt. Jeder Postfachserver zeichnet Datenbankaktualisierungen auf, die in einer aktiven Datenbank (z. B. E-Mail-Aktivität des Benutzers) als Protokolldatensätze in einer sequenziellen Gruppe von 1 MB Transaktionsprotokolldateien vorgenommen wurden. Dieser Satz von Dateien wird als Protokolldatenstrom bezeichnet. Bei der kontinuierlichen Replikation wird der Protokolldatenstrom auch verwendet, um eine oder mehrere Kopien einer Datenbank asynchron zu aktualisieren. Dies wird erreicht, indem die Protokolle an einen Speicherort übertragen werden, der eine passive Kopie der aktiven Datenbank enthält, und diese dann in der passiven Datenbankkopie wiedergeben. Wenn alle Protokolle aus der aktiven Datenbank für eine passive Kopie der Datenbank wiedergegeben werden, sind die beiden Datenbanken gleichwertig, und durch diesen Vorgang werden physische Änderungen an einer aktiven Datenbank in alle passiven Kopien dieser Datenbank repliziert.

Jeder Löschvorgang aus einer Postfachdatenbank, unabhängig davon, ob es sich um ein Postfachelement oder ein gesamtes Postfach handelt und ob ein vorläufiges oder ein endgültiges Löschen, stellt eine physische Änderung der aktiven Datenbank dar. Das Nullen von Seiten bedeutet auch, dass physische Änderungen an der aktiven Datenbank vorgenommen werden. Diese Änderungen werden über einen Prozess, der als fortlaufende Replikation bezeichnet wird, in die Protokolldateien geschrieben, und wenn diese Protokolldateien für passive Kopien der Datenbank wiedergegeben werden, werden die gleichen physischen Änderungen an diesen passiven Datenbanken vorgenommen.
