---
title: Löschen von Microsoft 365 Exchange Online-Daten
description: Erfahren Sie, wie Löschvorgänge für weiche und harte Daten für Postfächer und Elemente in Postfächern in Exchange Online behandelt werden.
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
ms.openlocfilehash: c88e7359931fb964fbc4cb6531c5151072a50df0
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497198"
---
# <a name="exchange-online-data-deletion-in-microsoft-365"></a>Löschen von Exchange Online-Daten in Microsoft 365

In Exchange Online gibt es zwei Arten von Löschvorgängen: soft deletions und hard deletions. Dies gilt sowohl für Postfächer als auch für Elemente innerhalb eines Postfachs.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Gelöschte und fest gelöschte Postfächer

Ein soft-deleted user mailbox ist ein Postfach, das mit dem Microsoft 365 Admin Center oder dem cmdlet Remove-Mailbox gelöscht wurde und sich seit weniger als 30 Tagen im Azure Active Directory-Papierkorb befindet. Ein Postfach kann auf eine der folgenden Arten soft-deleted werden:

- Das zugeordnete Azure Active Directory-Benutzerkonto des Benutzerpostfachs wird soft-deleted (das Benutzerobjekt befindet sich nicht im Bereich oder im Papierkorbcontainer).
- Das zugeordnete Azure Active Directory-Benutzerkonto des Benutzerpostfachs wurde hart gelöscht, aber das Exchange Online-Postfach befindet sich in einem Rechtsstreit oder einer eDiscovery-Speicher.
- Das zugeordnete Azure Active #A0 des Benutzerpostfachs wurde innerhalb der letzten 30 Tage gelöscht. Dies ist die maximale Aufbewahrungsdauer, mit der Exchange Online das Postfach in einem zustand des soft-deleted-Zustands behalte, bevor es endgültig gelöscht und nicht wiederhergestellt werden kann.

Ein fest gelöschtes Benutzerpostfach ist ein Postfach, das auf eine der folgenden Arten gelöscht wurde:

- Das Benutzerpostfach wurde seit mehr als 30 Tagen soft-deleted, und der zugeordnete Azure Active Directory-Benutzer wurde hart gelöscht. Alle Postfachinhalte wie E-Mails, Kontakte und Dateien werden dauerhaft gelöscht.
- Das dem Benutzerpostfach zugeordnete Benutzerkonto wurde aus Azure Active Directory gelöscht. Das Benutzerpostfach wird nun in Exchange Online soft-deleted und bleibt 30 Tage lang in einem Zustand mit soft-deleted. Wenn in dem Zeitraum von 30 Tage ein neuer Azure Active Directory-Benutzer vom ursprünglichen Empfängerkonto mit demselben **ExchangeGuid-** oder **ArchiveGuid-Konto** synchronisiert wird und dieses neue Konto für Exchange Online lizenziert ist, führt dies zu einem harten Löschen des ursprünglichen Benutzerpostfachs. Alle Postfachinhalte wie E-Mails, Kontakte und Dateien werden dauerhaft gelöscht.
- Ein unbefristetes Postfach wird mit **Remove-Mailbox -PermanentlyDelete gelöscht.**

In den oben genannten Löschszenarien wird davon ausgegangen, dass sich das Benutzerpostfach nicht in einem der Haltezustände befindet, z. B. im Prozesssicherungsverfahren oder im eDiscovery-Archiv. Wenn für das Postfach ein Haltespeicher besteht, kann das Postfach nicht gelöscht werden. Für alle E-Mail-Benutzer-Empfängertypen werden [alle](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) Halteeinstellungen ignoriert und haben keine Auswirkungen auf das löschende oder das automatische Löschen.

## <a name="soft-deleted-and-hard-deleted-items"></a>Elemente mit soft-deleted und hard-deleted

Wenn ein Benutzer ein Postfachelement löscht (z. B. eine E-Mail-Nachricht, einen Kontakt, einen Kalendertermin oder eine Aufgabe), wird das Element in den Ordner "Wiederherstellbare Elemente" und in einen Unterordner namens "Deletions" verschoben. Dies wird als "soft deletion" bezeichnet. Die Aufbewahrungsdauer für gelöschte Elemente im Ordner Löschvorgänge hängt von der Aufbewahrungsdauer für gelöschte Elemente ab, die für das Postfach festgelegt ist. In einem Exchange Online-Postfach werden gelöschte Elemente standardmäßig 14 Tage lang gespeichert. Exchange Online-Administratoren können diese Einstellung jedoch ändern, um den Zeitraum auf maximal 30 Tage zu erhöhen. (Ausführliche Schritte zum Erhöhen des Aufbewahrungszeitraums für gelöschte Elemente für ein Exchange Online-Postfach finden Sie unter [Change how long permanent deleted items are kept for an Exchange Online mailbox](/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention).) Benutzer können gelöschte Elemente wiederherstellen oder löschen, bevor die Aufbewahrungszeit für ein gelöschtes Element abläuft. Dazu verwenden sie das Feature Gelöschte Elemente wiederherstellen in Microsoft Outlook oder Outlook im Web.

Wenn ein Benutzer ein gelöschtes Element mithilfe des Features Gelöschte Elemente wiederherstellen in Outlook oder Outlook im Web löscht, wird dies als hartes Löschen bezeichnet. In Exchange Online ist die Wiederherstellung einzelner Elemente standardmäßig aktiviert, wenn [](/Exchange/recipients/user-mailboxes/recover-deleted-messages) ein neues Postfach erstellt wird, sodass ein Administrator weiterhin hart gelöschte Elemente wiederherstellen kann, bevor der Aufbewahrungszeitraum für gelöschte Elemente abläuft. Zudem werden Kopien des ursprünglichen Elements, wenn die Wiederherstellung einzelner Elemente aktiviert ist, beibehalten, sofern die Nachricht durch einen Benutzer oder Prozess geändert wird.

## <a name="page-zeroing"></a>Seitennullierung

*Zeroing* ist ein Sicherheitsmechanismus, der entweder Nullen oder ein binäres Muster über gelöschte Daten schreibt, sodass die gelöschten Daten schwieriger wiederhergestellt werden können. In Exchange Online verwenden  Postfachdatenbanken Seiten als Speichereinheit und implementieren einen Overwritingprozess namens *Page Zeroing*. Das Seitennulling ist standardmäßig aktiviert und kann weder von Kunden noch von Microsoft deaktiviert werden. Seitennullierungsvorgänge werden in den Transaktionsprotokolldateien aufgezeichnet, sodass alle Kopien einer bestimmten Datenbank auf ähnliche Weise seitennulliert werden. Wenn eine Seite in einer aktiven Datenbankkopie nulliert wird, wird die Seite für passive Kopien der Datenbank nulliert.

Das Seitennulling schreibt ein binäres Muster über hart gelöschte Datensätze. Das Seitennullierungsmuster ist spezifisch für Extensible Storage Engine (ESE)-Vorgänge (der Name des internen Datenbankmoduls, das von Servern in Exchange Online verwendet wird) und ist für Laufzeitvorgänge im Vergleich zu Hintergrunddatenbankwartungsvorgängen unterschiedlich. (Die Hintergrunddatenbankwartung ist ein Prozess, der jede Datenbank kontinuierlich überprüft und überprüft. Seine primäre Funktion besteht in der Überprüfung von Datenbankseiten, aber es behandelt auch das Bereinigen von Speicherplatz und das Löschen von Datensätzen und Seiten, die aufgrund eines Storeabsturzes nicht gelöscht wurden.)

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

### <a name="page-zeroing-process"></a>Seitennullierungsprozess

Der Vorgang für das Löschen von Seiten hängt vom Löschszenario ab. In der folgenden Tabelle ist für verschiedene Datenbanklöschszenarien erläutert, wann Funktionen zum unwiderruflichen Löschen ausgeführt werden.

| Datenbanklöschszenario | ESE-Vorgang und -Zeitrahmen für unwiderrufliches Löschen von Datenbankdaten |
|:--------------------------|:------------------------------------------------|
| Das Element läuft basierend auf dem Aufbewahrungszeitraum für gelöschte Elemente ab. | Ein asynchroner Thread schreibt ein binäres Muster über die gelöschten Daten. Diese Aktion wird innerhalb von Millisekunden nach dem Datensatzlöschvorgang ausgeführt. Wenn der Store-Prozess abstürzt, während die asynchrone Nullierungsarbeit noch ausstehend ist (oder die Versionsspeicherbereinigung aufgrund des Versionsspeicherwachstums abgebrochen wird), wird die Nullierung abgeschlossen, wenn die Hintergrunddatenbankwartung diesen Abschnitt der Datenbank verarbeitet. |
| Ansichtsszenario: Ablauf von Elementen aus Outlook/Outlook in der Webordneransicht (z. B. Unterhaltungsansicht) | Unwiderrufliches Löschen von Daten wird ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |
| Szenario "Postfach verschieben/löschen": Quellpostfach gelöscht (Ablauf des gelöschten Postfachs) | Unwiderrufliches Löschen von Daten wird ausgeführt, wenn die Hintergrundwartung der Datenbank diesen Abschnitt der Datenbank verarbeitet. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Postfachdatentypen ohne Seitennullierung

Die folgenden Postfachdatentypen enthalten keine Bestimmungen für das Löschen von Seiten:

- **Transaktionsprotokolle** für Postfachdatenbanken: Wenn Transaktionsprotokolle im Rahmen normaler Vorgänge gelöscht werden, gibt es keinen Prozess zum Nullen der Blöcke im Dateisystem, in dem die gelöschten Protokolldateien gespeichert wurden. Es ist wahrscheinlich, dass das Dateisystem diesen freien Speicherplatz für neu erstellte Protokolle schnell wieder nutzt, aber es gibt keine Garantie dafür.
- **Inhaltsindexkatalogdateien** – Exchange Online verwendet Search Foundation (auch bekannt als FAST) für die Suchindizierungsfunktionalität. Der Suchindexkatalog besteht aus mehreren Dutzend Dateien, die auf demselben Volume wie die Postfachdatenbankdatei gespeichert sind. Wenn eine Nachricht aus der Postfachdatenbank gelöscht wird, wird der zugeordnete Inhalt im Suchkatalog nicht sofort gelöscht. Das Löschen von Inhalten erfolgt, wenn Search Foundation einen Schatten (oder Masterzusammenführung) vieler kleiner Katalogdateien in einer einzelnen größeren Datei vorgibt. Nach Abschluss der Masterzusammenführung werden die kleineren Katalogdateien gelöscht. Es gibt keinen Prozess zum Nullen der Blöcke, die die gelöschten Katalogdateien gespeichert haben.

## <a name="continuous-replication"></a>Kontinuierliche Replikation

Die kontinuierliche Replikation (auch als Protokollversand und Wiedergabe bezeichnet) ist eine Technologie in Exchange Online, die Kopien jeder Postfachdatenbank erstellt und verwaltet, um hohe Verfügbarkeit, Ausfallsicherheit von Standorten und Notfallwiederherstellung zu gewährleisten. Die fortlaufende Replikation verwendet Exchange Server Unterstützung für die Wiederherstellung von Datenbankabstürzen, um Technologie zur asynchronen Aktualisierung einer oder mehreren Kopien einer Postfachdatenbank zur Verfügung zu stellen. Jeder Postfachserver zeichnet Datenbankupdates für eine aktive Datenbank (z. B. Benutzer-E-Mail-Aktivität) als Protokolldatensätze in einem sequenziellen Satz von 1 MB-Transaktionsprotokolldateien auf. Dieser Satz von Dateien wird als Protokolldatenstrom bezeichnet. Bei der fortlaufenden Replikation wird der Protokolldatenstrom auch zum asynchronen Aktualisieren einer oder mehreren Kopien einer Datenbank verwendet. Dazu werden die Protokolle an einen Speicherort mit einer passiven Kopie der aktiven Datenbank übertragen und anschließend in die passive Datenbankkopie wiedergegeben. Wenn alle Protokolle aus der aktiven Datenbank für eine passive Kopie der Datenbank wiedergegeben werden, sind die beiden Datenbanken gleichwertig, und durch diesen Vorgang werden alle physischen Änderungen, die an einer aktiven Datenbank vorgenommen wurden, in alle passiven Kopien dieser Datenbank repliziert.

Jeder Löschvorgang aus einer Postfachdatenbank, sei es ein Postfachelement oder ein gesamtes Postfach, und unabhängig davon, ob es sich um ein soft-delete oder ein hard-delete handelt, stellt eine physische Änderung an der aktiven Datenbank dar. Das Löschen von Seiten bedeutet auch, dass physische Änderungen an der aktiven Datenbank vorgenommen werden. Diese Änderungen werden in die Protokolldateien über einen Prozess geschrieben, der als kontinuierliche Replikation bezeichnet wird. Wenn diese Protokolldateien mit passiven Kopien der Datenbank wiedergegeben werden, werden dieselben physischen Änderungen an diesen passiven Datenbanken vorgenommen.
