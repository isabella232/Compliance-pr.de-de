---
title: Verschlüsselung für Skype, OneDrive, SharePoint und Exchange
description: 'Zusammenfassung: Eine Beschreibung der Verschlüsselung für Skype, OneDrive, SharePoint, Microsoft Teams und Exchange Online.'
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- SPO_Content
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 9317b112d1fa759b1f90e072203e7b8093a432fd
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120544"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>Verschlüsselung für Skype for Business, OneDrive for Business, SharePoint Online, Microsoft Teams und Exchange Online

Microsoft 365 ist eine äußerst sichere Umgebung, die umfassenden Schutz auf mehreren Ebenen bietet: Sicherheit im physischen Rechenzentrum, Netzwerksicherheit, Zugriffssicherheit, Anwendungssicherheit und Datensicherheit.

## <a name="skype-for-business"></a>Skype for Business

Skype for Business-Kundendaten können im Ruhebetrieb in Form von Dateien oder Präsentationen gespeichert werden, die von Besprechungsteilnehmern hochgeladen werden. Der Webkonferenzserver verschlüsselt Kundendaten mithilfe von AES mit einem 256-Bit-Schlüssel. Die verschlüsselten Kundendaten werden in einer Dateifreigabe gespeichert. Jeder Teil der Kundendaten wird mit einem anderen zufällig generierten 256-Bit-Schlüssel verschlüsselt. Wenn ein Teil der Kundendaten in einer Konferenz freigegeben wird, werden die Konferenzclients vom Webkonferenzserver angewiesen, die verschlüsselten Kundendaten über HTTPS herunterzuladen. Er sendet den entsprechenden Schlüssel an Clients, damit die Kundendaten entschlüsselt werden können. Der Webkonferenzserver authentifiziert auch Konferenzclients, bevor er den Clients den Zugriff auf Kundendaten von Konferenzen ermöglicht. Bei der Teilnahme an einer Webkonferenz richtet jeder Konferenzclient zuerst ein SIP-Dialogfeld ein, in dem die Konferenzfokuskomponente auf dem Front-End-Server über TLS ausgeführt wird. Der Konferenzfokus übergibt ein vom Webkonferenzserver generiertes Authentifizierungscookie an den Konferenzclient. Der Konferenzclient stellt dann eine Verbindung mit dem Webkonferenzserver, der das Authentifizierungscookie zur Authentifizierung durch den Server präsentiert.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online und OneDrive for Business

Alle Kundendateien in SharePoint Online sind durch eindeutige Schlüssel pro Datei geschützt, die immer exklusiv für einen einzelnen Mandanten sind. Die Schlüssel werden entweder vom SharePoint Online-Dienst erstellt und verwaltet, oder wenn Kundenschlüssel verwendet, von Kunden erstellt und verwaltet werden. Wenn eine Datei hochgeladen wird, wird die Verschlüsselung von SharePoint Online im Kontext der Uploadanforderung ausgeführt, bevor sie an Azure Storage gesendet wird. Wenn eine Datei heruntergeladen wird, ruft SharePoint Online die verschlüsselten Kundendaten aus azure storage basierend auf der eindeutigen Dokument-ID ab und entschlüsselt die Kundendaten, bevor sie an den Benutzer senden. Azure Storage kann die Kundendaten nicht entschlüsseln oder sogar identifizieren oder verstehen. Sämtliche Verschlüsselung und Entschlüsselung geschieht in denselben Systemen, die die Mandantenisolation erzwingen, d. h. Azure Active Directory und SharePoint Online.

Mehrere Workloads in Microsoft 365 speichern Daten in SharePoint Online, einschließlich Microsoft Teams, das alle Dateien in SharePoint Online speichert, und OneDrive for Business, das SharePoint Online als Speicher verwendet. Alle in SharePoint Online gespeicherten Kundendaten werden verschlüsselt (mit einem oder mehreren AES 256-Bit-Schlüsseln) und wie folgt über das Datencenter verteilt. (Jeder Schritt dieses Verschlüsselungsprozesses ist FIPS 140-2 Level 2 überprüft. Weitere Informationen zur FIPS 140-2-Compliance finden Sie unter [FIPS 140-2 Compliance.)](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105))

- Jede Datei wird je nach Dateigröße in einen oder mehrere Blöcke aufgeteilt. Jeder Block wird mit einem eigenen eindeutigen AES-256-Bit-Schlüssel verschlüsselt.
- Wenn eine Datei aktualisiert wird, wird die Aktualisierung auf die gleiche Weise behandelt: Die Änderung wird in einen oder mehrere Blöcke aufgeteilt, und jeder Block wird mit einem separaten eindeutigen Schlüssel verschlüsselt.
- Diese Blöcke – Dateien, Dateiteile und Aktualisierungsdeltas – werden als BLOBs im Azure-Speicher gespeichert, die nach dem Zufallsprinzip auf mehrere Azure -Speicherkonten verteilt werden.
- Der Satz von Verschlüsselungsschlüsseln für diese Datenblöcke von Kundendaten wird selbst verschlüsselt.

    - Die Schlüssel, die zum Verschlüsseln der Blobs verwendet werden, werden in der SharePoint Online-Inhaltsdatenbank gespeichert.
    - Die Inhaltsdatenbank ist durch Datenbankzugriffssteuerungen und die Verschlüsselung im Ruhe ruhend geschützt. Die Verschlüsselung erfolgt mithilfe [der transparenten Datenverschlüsselung](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (Transparent Data Encryption, TDE) in [Azure SQL Database](/azure/sql-database/sql-database-technical-overview). (Azure SQL Database ist ein allgemeiner relationaler Datenbankdienst in Microsoft Azure, der Strukturen wie relationale Daten, JSON, spatial und XML unterstützt.) Diese geheimen Schlüssel befinden sich auf Dienstebene für SharePoint Online, nicht auf Mandantenebene. Diese geheimen Schlüssel (auch als Hauptschlüssel bezeichnet) werden in einem separaten sicheren Repository gespeichert, das als Schlüsselspeicher bezeichnet wird. TDE bietet sicherheit im Ruhedienst sowohl für die aktive Datenbank als auch für die Datenbanksicherungen und Transaktionsprotokolle.
    - Wenn Kunden den optionalen Schlüssel bereitstellen, wird der Kundenschlüssel im Azure Key Vault gespeichert, und der Dienst verwendet den Schlüssel zum Verschlüsseln eines Mandantenschlüssels, der zum Verschlüsseln eines Websiteschlüssels verwendet wird, der dann zum Verschlüsseln der Schlüssel auf Dateiebene verwendet wird. Im Wesentlichen wird eine neue Schlüsselhierarchie eingeführt, wenn der Kunde einen Schlüssel liefert.
- Die Karte, die zum erneuten Zusammenstellen der Datei verwendet wird, wird in der Inhaltsdatenbank zusammen mit den verschlüsselten Schlüsseln getrennt vom Hauptschlüssel gespeichert, der zum Entschlüsseln erforderlich ist.
- Jedes Azure -Speicherkonto verfügt über eigene eindeutige Anmeldeinformationen pro Zugriffstyp (Lesen, Schreiben, Aufzählen und Löschen). Jeder Satz von Anmeldeinformationen wird im sicheren Schlüsselspeicher aufbewahrt und regelmäßig aktualisiert. Wie oben beschrieben, gibt es drei verschiedene Arten von Speichern, die jeweils eine unterschiedliche Funktion haben:
    - Kundendaten werden als verschlüsselte Blobs im Azure Storage gespeichert. Der Schlüssel zu jedem Datenblöcke von Kundendaten wird verschlüsselt und separat in der Inhaltsdatenbank gespeichert. Die Kundendaten selbst haben keinen Hinweis darauf, wie sie entschlüsselt werden können.
    - Die Inhaltsdatenbank ist eine SQL Server-Datenbank. Sie enthält die Karte, die zum Suchen und erneuten Zusammenfinden der Kundendaten-BLOBs im Azure-Speicher erforderlich ist, sowie die Schlüssel, die zum Verschlüsseln dieser Blobs erforderlich sind. Der Schlüsselsatz wird jedoch selbst verschlüsselt (wie oben erläutert) und in einem separaten Schlüsselspeicher gespeichert.
    - Der Schlüsselspeicher ist physisch getrennt von der Inhaltsdatenbank und dem Azure-Speicher. Sie enthält die Anmeldeinformationen für jeden Azure-Speichercontainer und den Hauptschlüssel für die verschlüsselten Schlüssel, die in der Inhaltsdatenbank gespeichert sind.

Jede dieser drei Speicherkomponenten – der Azure BLOB-Speicher, die Inhaltsdatenbank und der Schlüsselspeicher – ist physisch getrennt. Die Informationen in einer der Komponenten sind allein unbrauchbar. Ohne Zugriff auf alle drei ist es unmöglich, die Schlüssel für die Blöcke abzurufen, die Schlüssel zu entschlüsseln, um sie verwendbar zu machen, die Schlüssel den entsprechenden Blöcken zuzuordnen, jeden Block zu entschlüsseln oder ein Dokument aus den einzelnen Blöcken zu rekonstruieren.

BitLocker-Zertifikate, die die physischen Datenträgervolumes auf Computern im Datencenter schützen, werden in einem sicheren Repository (dem geheimen SharePoint Online-Speicher) gespeichert, das durch den Farmschlüssel geschützt ist.

Die TDE-Schlüssel, die die Schlüssel pro Blob schützen, werden an zwei Speicherorten gespeichert:

- Das sichere Repository, in dem sich die #A0 befinden und das durch den Farmschlüssel geschützt ist; und
- In einem sicheren Repository, das von Azure SQL wird.

Die Für den Zugriff auf die Azure -Speichercontainer verwendeten Anmeldeinformationen werden auch im geheimen SharePoint Online Store gespeichert und bei Bedarf an jede SharePoint Online-Farm delegiert. Bei diesen Anmeldeinformationen handelt es sich um Azure Storage-SAS-Signaturen, mit separaten Anmeldeinformationen, die zum Lesen oder Schreiben von Daten verwendet werden, und mit angewendeter Richtlinie, sodass sie alle 60 Tage automatisch ablaufen. Zum Lesen oder Schreiben von Daten (nicht beides) werden unterschiedliche Anmeldeinformationen verwendet, und SharePoint Online-Farmen werden keine Berechtigungen zum Aufzählen erteilt.

> [!NOTE]
> Für Kunden von Office 365 U.S. Government werden Datenblobs im Azure U.S. Government Storage gespeichert. Darüber hinaus ist der Zugriff auf SharePoint Online-Schlüssel in Office 365 U.S. Government auf Office 365-Mitarbeiter beschränkt, die speziell angezeigt wurden. Mitarbeiter von Azure U.S. Government haben keinen Zugriff auf den SharePoint Online-Schlüsselspeicher, der zum Verschlüsseln von DatenbloBs verwendet wird.

Weitere Informationen zur Datenverschlüsselung in SharePoint Online und OneDrive for Business finden Sie unter [Datenverschlüsselung in OneDrive for Business und SharePoint Online.](https://technet.microsoft.com/library/dn905447.aspx)

### <a name="list-items-in-sharepoint-online"></a>Listenelemente in SharePoint Online

Listenelemente sind kleinere Segmente von Kundendaten, die ad-hoc erstellt werden oder dynamischer innerhalb einer Website vorhanden sein können, z. B. Zeilen in einer vom Benutzer erstellten Liste, einzelne Beiträge in einem SharePoint Online-Blog oder Einträge auf einer SharePoint Online-Wiki-Seite. Listenelemente werden in der Inhaltsdatenbank (Azure SQL Database) gespeichert und mit TDE geschützt.

## <a name="encryption-of-data-in-transit"></a>Verschlüsselung von Daten während der Übertragung

In OneDrive for Business und SharePoint Online gibt es zwei Szenarien, in denen Daten in Rechenzentren ein- und ausgehen.

- **Clientkommunikation mit dem Server** – Die Kommunikation mit SharePoint Online und OneDrive for Business über das Internet verwendet TLS-Verbindungen.
- **Datenbewegung zwischen Rechenzentren:** Der Hauptgrund für das Verschieben von Daten zwischen Rechenzentren ist die Georeplikation, um die Notfallwiederherstellung zu ermöglichen. Beispielsweise werden SQL Server-Transaktionsprotokolle und BLOB-Speicher-Deltas entlang dieser Pipe übertragen. Während diese Daten bereits über ein privates Netzwerk übertragen werden, werden sie zusätzlich durch branchenbeste Verschlüsselung geschützt.

## <a name="exchange-online"></a>Exchange Online

Exchange Online verwendet BitLocker für alle Postfachdaten, und die Konfiguration von BitLocker wird in [BitLocker for Encryption beschrieben.](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption) Die Verschlüsselung auf Dienstebene verschlüsselt alle Postfachdaten auf Postfachebene. 

Zusätzlich zur Dienstverschlüsselung unterstützt Microsoft 365 den Kundenschlüssel, der auf der Dienstverschlüsselung aufgebaut ist. Customer Key ist eine von Microsoft verwaltete Schlüsseloption für die Exchange Online-Dienstverschlüsselung, die auch in der Roadmap von Microsoft steht. Diese Verschlüsselungsmethode bietet einen erhöhten Schutz, der bitLocker nicht bietet, da sie eine Trennung von Serveradministratoren und den kryptografischen Schlüsseln ermöglicht, die für die Entschlüsselung von Daten erforderlich sind, und da die Verschlüsselung direkt auf die Daten angewendet wird (im Gegensatz zu BitLocker, das Verschlüsselung auf dem logischen Datenträgervolume angewendet wird), bleiben alle Kundendaten verschlüsselt, die von einem Exchange Server kopiert werden.

Der Bereich für die Exchange Online-Dienstverschlüsselung sind Kundendaten, die in Exchange Online gespeichert werden. (Skype for Business speichert fast alle vom Benutzer generierten Inhalte im Exchange Online-Postfach des Benutzers und erbt daher die Dienstverschlüsselungsfunktion von Exchange Online.)


## <a name="microsoft-teams"></a>Microsoft Teams

Teams verwendet TLS und MTLS zum Verschlüsseln von Chatnachrichten. Der gesamte Datenverkehr zwischen den Servern erfordert MTLS, und zwar unabhängig davon, ob die Daten innerhalb des internen Netzwerks verbleiben oder den internen Netzwerkumkreis verlassen.

In dieser Tabelle sind die von Teams verwendeten Protokolle zusammengefasst.

|**Datenverkehrstyp**|**Verschlüsselt von**|
|:-----|:-----|
|Server-zu-Server|MTLS|
|Client-zu-Server (z. B. Chat und Anwesenheit)|TLS|
|Medienflüsse (z. B. Audio- und Videofreigabe von Medien)|TLS|
|Audio- und Videofreigabe von Medien|SRTP/TLS|
|Signalisierung|TLS|

#### <a name="media-encryption"></a>Medienverschlüsselung

Der Mediendatenverkehr wird mit SRTP (Secure RTP) verschlüsselt, einem Profil von Real-Time Transport Protocol (RTP), das vertraulichkeits-, Authentifizierungs- und Replay-Angriffsschutz für den Datenverkehr von RTP bietet. SRTP verwendet einen Sitzungsschlüssel, der mithilfe eines sicheren Zufallszahlengenerators generiert wird und über den signalisierten TLS-Kanal ausgetauscht wird. Der Client-zu-Client-Mediendatenverkehr wird über eine Client-zu-Server-Verbindungssignalisierung ausgehandelt, wird jedoch mithilfe von SRTP verschlüsselt, wenn client-zu-client direkt vor dem Client-zu-Client-Datenverkehr ausgeführt wird.

Teams verwendet ein anmeldebasiertes Token für den sicheren Zugriff auf Medienrelais über TURN. Medienrelais tauschen das Token über einen TLS-gesicherten Kanal aus.

#### <a name="fips"></a>FIPS

Teams verwendet FIPS (Federal Information Processing Standard) kompatible Algorithmen für den Austausch von Verschlüsselungsschlüsseln. Weitere Informationen zur Implementierung von FIPS finden Sie unter [Federal Information Processing Standard (FIPS) Publication 140-2](/microsoft-365/compliance/offering-fips-140-2).
