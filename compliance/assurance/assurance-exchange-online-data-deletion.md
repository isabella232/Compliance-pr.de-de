---
title: Löschen von Microsoft 365 Exchange Online-Daten
description: Erfahren Sie, wie soft- und hard data deletions for mailboxes and items within mailboxes are handled in Exchange Online.
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
ms.openlocfilehash: b86c855a113706731ac6037a2851ae0f1adaccb9
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012961"
---
# <a name="exchange-online-data-deletion-in-microsoft-365"></a>Löschen von Exchange Online-Daten in Microsoft 365

In Exchange Online gibt es zwei Arten von Löschvorgängen: soft deletions und hard deletions. Dies gilt sowohl für Postfächer als auch für Elemente innerhalb eines Postfachs.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Soft-deleted- und hard-deleted mailboxes

Ein nicht gelöschtes Benutzerpostfach ist ein Postfach, das mit dem Microsoft 365 Admin Center oder dem Remove-Mailbox-Cmdlet gelöscht wurde und sich seit weniger als 30 Tagen im Azure Active Directory-Papierkorb befindet. Ein Postfach kann auf eine der folgenden Arten soft-deleted werden:

- Das zugeordnete Azure Active Directory-Benutzerkonto des Benutzerpostfachs wird soft-deleted (das Benutzerobjekt liegt nicht im Gültigkeitsbereich oder im Papierkorbcontainer).
- Das zugeordnete Azure Active Directory-Benutzerkonto des Benutzerpostfachs wurde gelöscht, für das Exchange Online-Postfach gilt jedoch ein In-Rechtsstreitigkeiten- oder eDiscovery-Speicher.
- Das zugeordnete Azure Active #A0 des Benutzerpostfachs wurde innerhalb der letzten 30 Tage gelöscht. Dies ist die maximale Aufbewahrungsdauer, über die Exchange Online das Postfach in einem zustand "Soft-Deleted" behalte, bevor es endgültig gelöscht und nicht wiederhergestellt werden kann.

Ein gelöschtes Benutzerpostfach ist ein Postfach, das auf eine der folgenden Arten gelöscht wurde:

- Das Benutzerpostfach wurde seit mehr als 30 Tagen soft-deleted, und der zugeordnete Azure Active Directory-Benutzer wurde gelöscht. Alle Postfachinhalte wie E-Mails, Kontakte und Dateien werden dauerhaft gelöscht.
- Das Benutzerkonto, das dem Benutzerpostfach zugeordnet ist, wurde aus dem Azure Active Directory gelöscht. Das Benutzerpostfach wird nun in Exchange Online soft-deleted und bleibt 30 Tage lang im Zustand "Soft-Deleted". Wenn in den 30-Tage-Zeitraum ein neuer Azure Active Directory-Benutzer aus dem ursprünglichen Empfängerkonto mit derselben **ExchangeGuid** oder **ArchiveGuid** synchronisiert wird und dieses neue Konto für Exchange Online lizenziert ist, führt dies zum löschen des ursprünglichen Benutzerpostfachs. Alle Postfachinhalte wie E-Mails, Kontakte und Dateien werden dauerhaft gelöscht.
- Ein endgültig gelöschtes Postfach wird mithilfe von **"Remove-Mailbox -PermanentlyDelete" gelöscht.**

In den oben genannten Löschszenarien wird davon ausgegangen, dass sich das Benutzerpostfach nicht in einem der Haltezustände befindet, z. B. in einem Archiv für rechtsstreitigkeiten oder in einem eDiscovery-Archiv. Wenn für das Postfach eine Art Von-Archiv-E-Mail-Aktiviert ist, kann das Postfach nicht gelöscht werden. Für alle E-Mail-Benutzerempfängertypen werden alle Halteeinstellungen ignoriert und haben keine Auswirkungen auf das löschen oder das löschen. [](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US)

## <a name="soft-deleted-and-hard-deleted-items"></a>Soft-deleted- und hard-deleted items

Wenn ein Benutzer ein Postfachelement löscht (z. B. eine E-Mail-Nachricht, einen Kontakt, einen Kalendertermin oder eine Aufgabe), wird das Element in den Ordner "Wiederherstellbare Elemente" und in einen Unterordner namens "Löschvorgänge" verschoben. Dies wird als "soft deletion" bezeichnet. Die Aufbewahrungsdauer für gelöschte Elemente im Ordner Löschvorgänge hängt von der Aufbewahrungsdauer für gelöschte Elemente ab, die für das Postfach festgelegt ist. In einem Exchange Online-Postfach werden gelöschte Elemente standardmäßig 14 Tage lang gespeichert. Exchange Online-Administratoren können diese Einstellung jedoch ändern, um den Zeitraum auf maximal 30 Tage zu erhöhen. (Ausführliche Schritte zum Erhöhen des Aufbewahrungszeitraums für gelöschte Elemente für ein Exchange Online-Postfach finden Sie unter "Ändern der Aufbewahrungsdauer für endgültig gelöschte Elemente für ein [Exchange Online-Postfach.)](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention) Benutzer können gelöschte Elemente wiederherstellen oder löschen, bevor die Aufbewahrungszeit für ein gelöschtes Element abläuft. Dazu verwenden sie das Feature "Gelöschte Elemente wiederherstellen" in Microsoft Outlook oder Outlook im Web.

Wenn ein Benutzer ein gelöschtes Element mithilfe des Features "Gelöschte Elemente wiederherstellen" in Outlook oder Outlook im Web löscht, wird dies als "Hard Deletion" bezeichnet. In Exchange Online ist die Wiederherstellung einzelner Elemente standardmäßig aktiviert, wenn [](https://docs.microsoft.com/Exchange/recipients/user-mailboxes/recover-deleted-messages) ein neues Postfach erstellt wird, sodass ein Administrator weiterhin hart gelöschte Elemente wiederherstellen kann, bevor der Aufbewahrungszeitraum für gelöschte Elemente abläuft. Zudem werden Kopien des ursprünglichen Elements, wenn die Wiederherstellung einzelner Elemente aktiviert ist, beibehalten, sofern die Nachricht durch einen Benutzer oder Prozess geändert wird.

## <a name="page-zeroing"></a>Unnullierung von Seiten

*Beim Löschen* handelt es sich um einen Sicherheitsmechanismus, der entweder Nullen oder ein binäres Muster über gelöschte Daten schreibt, sodass die wiederhergestellten Daten schwieriger wiederhergestellt werden können. In Exchange Online verwenden Postfachdatenbanken *Seiten* als Speichereinheit und implementieren einen überschreibenden Prozess, der als *Unnullierung* von Seiten bezeichnet wird. Das Unzenden von Seiten ist standardmäßig aktiviert und kann nicht von Kunden oder von Microsoft deaktiviert werden. Vorgänge zum Löschen von Seiten werden in den Transaktionsprotokolldateien aufgezeichnet, sodass alle Kopien einer bestimmten Datenbank auf ähnliche Weise vom Seitennulling entfernt werden. Durch das Löschen einer Seite für eine aktive Datenbankkopie wird die Seite für passive Kopien der Datenbank gelöscht.

Beim Unent zeroing wird ein binäres Muster über hart gelöschte Datensätze verfasst. Das Muster zum Löschen von Seiten ist spezifisch für Vorgänge des Extensible Storage Engine (ESE) (der Name des internen Datenbankmoduls, das von Servern in Exchange Online verwendet wird) und ist für Laufzeitvorgänge im Vergleich zu Wartungsvorgängen für Hintergrunddatenbanken unterschiedlich. (Die Hintergrundwartung von Datenbanken ist ein Prozess, der die einzelnen Datenbanken kontinuierlich überprüft und überprüft. Ihre primäre Funktion besteht in der Prüfsummendatenbankseiten, aber sie behandelt auch das Bereinigen von Speicherplatz und das Löschen von Datensätzen und Seiten, die aufgrund eines Absturzes des Store nicht gelöscht wurden.)

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

### <a name="page-zeroing-process"></a>Unzullvorgang für Seiten

Der Vorgang für das Löschen von Seiten hängt vom Löschszenario ab. In der folgenden Tabelle ist für verschiedene Datenbanklöschszenarien erläutert, wann Funktionen zum unwiderruflichen Löschen ausgeführt werden.

| Datenbanklöschszenario | ESE-Vorgang und -Zeitrahmen für unwiderrufliches Löschen von Datenbankdaten |
|:--------------------------|:------------------------------------------------|
| Das Element läuft basierend auf dem Aufbewahrungszeitraum für gelöschte Elemente ab. | Ein asynchroner Thread schreibt ein binäres Muster über die gelöschten Daten. Diese Aktion wird innerhalb von Millisekunden nach dem Datensatzlöschvorgang ausgeführt. Wenn der Speicherprozess abstürzt, während die asynchrone Unnullierung noch nicht abgeschlossen ist (oder die Versionsspeicherbereinigung aufgrund des Versionsspeicherwachstums abgebrochen wird), wird das Löschen abgeschlossen, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |
| Ansichtsszenario: Ablauf von Elementen aus der Outlook/Outlook im Web-Ordneransicht (z. B. Unterhaltungsansicht) | Unwiderrufliches Löschen von Daten wird ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |
| Szenario "Postfach verschieben/löschen": Quellpostfach gelöscht (Ablauf des gelöschten Postfachs) | Unwiderrufliches Löschen von Daten wird ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Postfachdatentypen ohne Unsummen von Seiten

Die folgenden Postfachdatentypen haben keine Vorkehrungen für das Löschen von Seiten:

- **Transaktionsprotokolle** der Postfachdatenbank: Wenn Transaktionsprotokolle im Rahmen des normalen Betriebs gelöscht werden, gibt es keinen Prozess zum Löschen der Blöcke im Dateisystem, in dem die gelöschten Protokolldateien gespeichert sind. Es ist wahrscheinlich, dass das Dateisystem den freien Speicherplatz für neu erstellte Protokolle schnell wieder auslastet, aber es gibt keine Garantie dafür.
- **Inhaltsindexkatalogdateien** – Exchange Online verwendet Search Foundation (auch bekannt als FAST) für die Suchindizierungsfunktionalität. Der Suchindexkatalog besteht aus mehreren Dutzend Dateien, die auf demselben Volume wie die Postfachdatenbankdatei gespeichert sind. Wenn eine Nachricht aus der Postfachdatenbank gelöscht wird, wird der zugeordnete Inhalt im Suchkatalog nicht sofort gelöscht. Das Löschen von Inhalten erfolgt, wenn Search Foundation einen Schatten (oder Masterzusammenführungsvorgang) vieler kleiner Katalogdateien in einer einzigen größeren Datei vorgibt. Nach Abschluss der Masterzusammenführung werden die kleineren Katalogdateien gelöscht. Es gibt keinen Prozess zum Nullen der Blöcke, die die gelöschten Katalogdateien gespeichert haben.

## <a name="continuous-replication"></a>Fortlaufende Replikation

Die fortlaufende Replikation (auch als Protokollversand und -wiedergabe bezeichnet) ist eine Technologie in Exchange Online, die Kopien jeder Postfachdatenbank erstellt und verwaltet, um hohe Verfügbarkeit, Ausfallsicherheit von Standorten und Notfallwiederherstellung zu gewährleisten. Die fortlaufende Replikation verwendet Exchange Server Unterstützung für die Wiederherstellung von Datenbankabstürzen, um Technologien zur asynchronen Aktualisierung einer oder mehreren Kopien einer Postfachdatenbank zu bieten. Jeder Postfachserver zeichnet Datenbankaktualisierungen für eine aktive Datenbank (z. B. Benutzer-E-Mail-Aktivität) als Protokolldatensätze in einem sequenziellen Satz von Transaktionsprotokolldateien mit 1 MB auf. Diese Gruppe von Dateien wird als Protokolldatenstrom bezeichnet. Bei der fortlaufenden Replikation wird der Protokolldatenstrom auch verwendet, um eine oder mehrere Kopien einer Datenbank asynchron zu aktualisieren. Dazu werden die Protokolle an einen Speicherort übertragen, der eine passive Kopie der aktiven Datenbank enthält, und diese dann in der passiven Datenbankkopie wiedergegeben. Wenn alle Protokolle aus der aktiven Datenbank für eine passive Kopie der Datenbank wiedergegeben werden, sind die beiden Datenbanken gleichwertig, und durch diesen Vorgang werden alle physischen Änderungen an einer aktiven Datenbank in alle passiven Kopien dieser Datenbank repliziert.

Jede Löschung aus einer Postfachdatenbank, unabhängig davon, ob es sich um ein Postfachelement oder ein gesamtes Postfach handelt und ob es sich um ein soft-delete- oder ein hard-delete-Element handelt, stellt eine physische Änderung an der aktiven Datenbank dar. Das Unentsprechen von Seiten umfasst auch das Vornehmen physischer Änderungen an der aktiven Datenbank. Diese Änderungen werden in die Protokolldateien über einen Prozess geschrieben, der als fortlaufende Replikation bezeichnet wird. Wenn diese Protokolldateien für passive Kopien der Datenbank wiedergegeben werden, werden dieselben physischen Änderungen an diesen passiven Datenbanken vorgenommen.
