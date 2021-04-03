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
hideEdit: true
ms.openlocfilehash: 3907a9a3f085af3d778daa2a385209f4dc9699a4
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497554"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>Verschlüsselung für Skype for Business, OneDrive for Business, SharePoint Online, Microsoft Teams und Exchange Online

Microsoft 365 ist eine hochgradig sichere Umgebung, die umfassenden Schutz in mehreren Ebenen bietet: Sicherheit des physischen Rechenzentrums, Netzwerksicherheit, Zugriffssicherheit, Anwendungssicherheit und Datensicherheit.

## <a name="skype-for-business"></a>Skype for Business

Skype for Business-Kundendaten können in Form von Dateien oder Präsentationen gespeichert werden, die von Besprechungsteilnehmern hochgeladen werden. Der Webkonferenzserver verschlüsselt Kundendaten mithilfe von AES mit einem 256-Bit-Schlüssel. Die verschlüsselten Kundendaten werden in einer Dateifreigabe gespeichert. Jeder Teil der Kundendaten wird mit einem anderen zufällig generierten 256-Bit-Schlüssel verschlüsselt. Wenn ein Teil der Kundendaten in einer Konferenz freigegeben wird, werden die Konferenzclients vom Webkonferenzserver angewiesen, die verschlüsselten Kundendaten über HTTPS herunterzuladen. Er sendet den entsprechenden Schlüssel an Clients, damit die Kundendaten entschlüsselt werden können. Der Webkonferenzserver authentifiziert auch Konferenzclients, bevor er den Clients Zugriff auf Kundendaten von Konferenzen gewährt. Bei der Teilnahme an einer Webkonferenz richtet jeder Konferenzclient ein SIP-Dialogfeld ein, in dem zuerst die Konferenzfokuskomponente ausgeführt wird, die innerhalb des Front-End-Servers über TLS ausgeführt wird. Der Konferenzfokus übergibt ein vom Webkonferenzserver generiertes Authentifizierungscookie an den Konferenzclient. Der Konferenzclient stellt dann eine Verbindung mit dem Webkonferenzserver ein, auf dem das Authentifizierungscookie angezeigt wird, das vom Server authentifiziert werden soll.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online und OneDrive for Business

Alle Kundendateien in SharePoint Online sind durch eindeutige, dateispezifische Schlüssel geschützt, die immer exklusiv für einen einzelnen Mandanten sind. Die Schlüssel werden entweder vom SharePoint Online-Dienst erstellt und verwaltet, oder wenn Kundenschlüssel von Kunden verwendet, erstellt und verwaltet werden. Wenn eine Datei hochgeladen wird, wird die Verschlüsselung von SharePoint Online im Kontext der Uploadanforderung ausgeführt, bevor sie an den Azure-Speicher gesendet wird. Wenn eine Datei heruntergeladen wird, ruft SharePoint Online die verschlüsselten Kundendaten aus dem Azure-Speicher basierend auf der eindeutigen Dokument-ID ab und entschlüsselt die Kundendaten, bevor sie an den Benutzer senden. Azure Storage kann die Kundendaten nicht entschlüsseln oder sogar identifizieren oder verstehen. Die Verschlüsselung und Entschlüsselung geschieht in denselben Systemen, die die Mandantenisolation erzwingen, d. h. Azure Active Directory und SharePoint Online.

Mehrere Workloads in Microsoft 365 speichern Daten in SharePoint Online, einschließlich Microsoft Teams, das alle Dateien in SharePoint Online speichert, und OneDrive for Business, das SharePoint Online für seinen Speicher verwendet. Alle in SharePoint Online gespeicherten Kundendaten werden verschlüsselt (mit einem oder mehreren AES 256-Bit-Schlüsseln) und wie folgt über das Datencenter verteilt. (Jeder Schritt dieses Verschlüsselungsprozesses ist FIPS 140-2 Level 2 überprüft. Weitere Informationen zur FIPS 140-2-Compliance finden Sie unter [FIPS 140-2 Compliance](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105)).)

- Jede Datei wird je nach Dateigröße in einen oder mehrere Blöcke aufgeteilt. Jeder Block wird mit einem eigenen eindeutigen AES-256-Bit-Schlüssel verschlüsselt.
- Wenn eine Datei aktualisiert wird, wird das Update auf die gleiche Weise behandelt: Die Änderung wird in einen oder mehrere Blöcke aufgeteilt, und jeder Abschnitt wird mit einem separaten eindeutigen Schlüssel verschlüsselt.
- Diese Blöcke – Dateien, Dateiteile und Updatedeltas – werden als Blobs im Azure-Speicher gespeichert, die zufällig auf mehrere Azure-Speicherkonten verteilt werden.
- Der Satz von Verschlüsselungsschlüsseln für diese Datenblöcke wird selbst verschlüsselt.

    - Die Schlüssel zum Verschlüsseln der Blobs werden in der SharePoint Online-Inhaltsdatenbank gespeichert.
    - Die Inhaltsdatenbank ist durch Datenbankzugriffssteuerelemente und ruhende Verschlüsselung geschützt. Die Verschlüsselung erfolgt mithilfe der [transparenten Datenverschlüsselung](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (Transparent Data Encryption, TDE) in [Azure SQL Database](/azure/sql-database/sql-database-technical-overview). (Azure SQL Database ist ein allgemeiner relationaler Datenbankdienst in Microsoft Azure, der Strukturen wie relationale Daten, JSON, spatial und XML unterstützt.) Diese Geheim geheimen Schlüssel befinden sich auf Dienstebene für SharePoint Online, nicht auf Mandantenebene. Diese Geheimschlüssel (auch als Hauptschlüssel bezeichnet) werden in einem separaten sicheren Repository gespeichert, das als Schlüsselspeicher bezeichnet wird. TDE bietet ruhende Sicherheit sowohl für die aktive Datenbank als auch für datenbanksicherungen und Transaktionsprotokolle.
    - Wenn Kunden den optionalen Schlüssel bereitstellen, wird der Kundenschlüssel in Azure Key Vault gespeichert, und der Dienst verwendet den Schlüssel zum Verschlüsseln eines Mandantenschlüssels, der zum Verschlüsseln eines Standortschlüssels verwendet wird, der dann zum Verschlüsseln der Schlüssel auf Dateiebene verwendet wird. Im Wesentlichen wird eine neue Schlüsselhierarchie eingeführt, wenn der Kunde einen Schlüssel liefert.
- Die Karte, die zum erneuten Zusammenstellen der Datei verwendet wird, wird in der Inhaltsdatenbank zusammen mit den verschlüsselten Schlüsseln getrennt vom Hauptschlüssel gespeichert, der zum Entschlüsseln dieser Dateien erforderlich ist.
- Jedes Azure-Speicherkonto verfügt über eigene eindeutige Anmeldeinformationen pro Zugriffstyp (Lesen, Schreiben, Aufzählen und Löschen). Jeder Satz von Anmeldeinformationen wird im sicheren Schlüsselspeicher aufbewahrt und regelmäßig aktualisiert. Wie oben beschrieben, gibt es drei verschiedene Arten von Speichern, die jeweils eine unterschiedliche Funktion haben:
    - Kundendaten werden als verschlüsselte Blobs im Azure-Speicher gespeichert. Der Schlüssel zu den einzelnen Kundendatenblöcken wird verschlüsselt und separat in der Inhaltsdatenbank gespeichert. Die Kundendaten selbst enthalten keinen Hinweis darauf, wie sie entschlüsselt werden können.
    - Die Inhaltsdatenbank ist eine SQL Server-Datenbank. Sie enthält die Karte, die zum Suchen und Erneuten Zusammenbauen der Kundendatenblobs im Azure-Speicher erforderlich ist, sowie die Schlüssel, die zum Verschlüsseln dieser Blobs erforderlich sind. Der Schlüsselsatz wird jedoch selbst verschlüsselt (wie oben erläutert) und in einem separaten Key Store gespeichert.
    - Der Schlüsselspeicher ist physisch getrennt von der Inhaltsdatenbank und dem Azure-Speicher. Sie enthält die Anmeldeinformationen für jeden Azure-Speichercontainer und den Hauptschlüssel für den Satz verschlüsselter Schlüssel, die in der Inhaltsdatenbank gespeichert sind.

Jede dieser drei Speicherkomponenten – der Azure-Blobspeicher, die Inhaltsdatenbank und der Schlüsselspeicher – ist physisch getrennt. Die Informationen in einer der Komponenten sind allein unbrauchbar. Ohne Zugriff auf alle drei Ist es unmöglich, die Schlüssel zu den Blöcken abzurufen, die Schlüssel zu entschlüsseln, um sie verwendbar zu machen, die Schlüssel ihren entsprechenden Blöcken zuzuordnen, jeden Abschnitt zu entschlüsseln oder ein Dokument aus den einzelnen Blöcken zu rekonstruieren.

BitLocker-Zertifikate, die die physischen Datenträgervolumes auf Computern im Datencenter schützen, werden in einem sicheren Repository (dem geheimen SharePoint Online-Speicher) gespeichert, das durch den Farmschlüssel geschützt ist.

Die TDE-Schlüssel, die die Tasten pro Blob schützen, werden an zwei Speicherorten gespeichert:

- Das sichere Repository, in dem die BitLocker-Zertifikate gespeichert sind und durch den Farmschlüssel geschützt sind; und
- In einem sicheren Repository, das von Azure SQL wird.

Die Anmeldeinformationen für den Zugriff auf die Azure-Speichercontainer werden auch im geheimen SharePoint Online-Speicher gespeichert und bei Bedarf an jede SharePoint Online-Farm delegiert. Bei diesen Anmeldeinformationen handelt es sich um Azure Storage -SAS-Signaturen mit separaten Anmeldeinformationen, die zum Lesen oder Schreiben von Daten verwendet werden, und bei der Richtlinie angewendet wird, sodass sie alle 60 Tage automatisch ablaufen. Unterschiedliche Anmeldeinformationen werden zum Lesen oder Schreiben von Daten (nicht beides) verwendet, und SharePoint Online-Farmen erhalten keine Berechtigungen zum Aufzählen.

> [!NOTE]
> Für Office 365 U.S. Government-Kunden werden Datenblobs im Azure U.S. Government Storage gespeichert. Darüber hinaus ist der Zugriff auf SharePoint Online-Schlüssel in Office 365 U.S. Government auf Office 365-Mitarbeiter beschränkt, die speziell gescreent wurden. Mitarbeiter von Azure U.S. Government Operations haben keinen Zugriff auf den SharePoint Online-Schlüsselspeicher, der zum Verschlüsseln von Datenblobs verwendet wird.

Weitere Informationen zur Datenverschlüsselung in SharePoint Online und OneDrive for Business finden Sie unter [Datenverschlüsselung in OneDrive for Business und SharePoint Online.](https://technet.microsoft.com/library/dn905447.aspx)

### <a name="list-items-in-sharepoint-online"></a>Auflisten von Elementen in SharePoint Online

Listenelemente sind kleinere Abschnitte von Kundendaten, die ad-hoc erstellt werden oder dynamischer auf einer Website gespeichert werden können, z. B. Zeilen in einer vom Benutzer erstellten Liste, einzelne Beiträge in einem SharePoint Online-Blog oder Einträge auf einer SharePoint Online-Wikiseite. Listenelemente werden in der Inhaltsdatenbank (Azure SQL Database) gespeichert und mit TDE geschützt.

## <a name="encryption-of-data-in-transit"></a>Verschlüsselung von Daten während der Übertragung

In OneDrive for Business und SharePoint Online gibt es zwei Szenarien, in denen Daten in Rechenzentren ein- und ausgehen.

- **Clientkommunikation mit dem Server** – Kommunikation mit SharePoint Online und OneDrive for Business über das Internet verwendet TLS-Verbindungen.
- **Datenbewegung zwischen Rechenzentren** – Der hauptgrund für das Verschieben von Daten zwischen Rechenzentren ist die Georeplikation, um die Notfallwiederherstellung zu ermöglichen. Beispielsweise werden SQL Server-Transaktionsprotokolle und BLOB-Speicher-Deltas entlang dieser Pipe übertragen. Während diese Daten bereits über ein privates Netzwerk übertragen werden, werden sie zusätzlich durch branchenbeste Verschlüsselung geschützt.

## <a name="exchange-online"></a>Exchange Online

Exchange Online verwendet BitLocker für alle Postfachdaten, und die BitLocker-Konfiguration wird in [BitLocker for Encryption beschrieben.](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption) Die Verschlüsselung auf Dienstebene verschlüsselt alle Postfachdaten auf Postfachebene. 

Zusätzlich zur Dienstverschlüsselung unterstützt Microsoft 365 den Kundenschlüssel, der auf der Dienstverschlüsselung aufgebaut ist. Customer Key ist eine von Microsoft verwaltete Schlüsseloption für die Exchange Online-Dienstverschlüsselung, die sich auch in der Roadmap von Microsoft befindet. Diese Verschlüsselungsmethode bietet einen erhöhten Schutz, der von BitLocker nicht gewährt wird, da sie eine Trennung von Serveradministratoren und den für die Entschlüsselung von Daten erforderlichen kryptografischen Schlüsseln ermöglicht und da die Verschlüsselung direkt auf die Daten angewendet wird (im Gegensatz zu BitLocker, das verschlüsselungsorientierte Daten auf dem logischen Datenträgervolume verwendet), bleiben alle kundendaten, die von einem Exchange-Server kopiert werden, verschlüsselt.

Der Bereich für die Exchange Online-Dienstverschlüsselung sind Kundendaten, die in Exchange Online gespeichert werden. (Skype for Business speichert fast alle vom Benutzer generierten Inhalte im Exchange Online-Postfach des Benutzers und erbt daher das Dienstverschlüsselungsfeature von Exchange Online.)


## <a name="microsoft-teams"></a>Microsoft Teams

Teams verwendet TLS und MTLS zum Verschlüsseln von Chatnachrichten. Der gesamte Datenverkehr zwischen den Servern erfordert MTLS, und zwar unabhängig davon, ob die Daten innerhalb des internen Netzwerks verbleiben oder den internen Netzwerkumkreis verlassen.

In dieser Tabelle werden die von Teams verwendeten Protokolle zusammengefasst.

|**Datenverkehrstyp**|**Verschlüsselt von**|
|:-----|:-----|
|Server-zu-Server|MTLS|
|Client-zu-Server (z. B. Instant Messaging und Anwesenheit)|TLS|
|Medienflüsse (z. B. Audio- und Videofreigabe von Medien)|TLS|
|Audio- und Videofreigabe von Medien|SRTP/TLS|
|Signalisierung|TLS|

#### <a name="media-encryption"></a>Medienverschlüsselung

Mediendatenverkehr wird mit Secure RTP (SRTP) verschlüsselt, einem Profil von Real-Time Transport Protocol (RTP), das Vertraulichkeit, Authentifizierung und Schutz vor Wiedergabeangriffen für RTP-Datenverkehr bietet. SRTP verwendet einen Sitzungsschlüssel, der mithilfe eines sicheren Zufallszahlengenerators generiert wird und über den signalisierten TLS-Kanal ausgetauscht wird. Der Client-zu-Client-Mediendatenverkehr wird über eine Client-zu-Server-Verbindungssignalisierung ausgehandelt, wird jedoch mithilfe von SRTP verschlüsselt, wenn client-to-client direkt verwendet wird.

Teams verwendet ein anmeldeinformationsbasiertes Token für den sicheren Zugriff auf Medienrelais über TURN. Medienrelais tauschen das Token über einen TLS-gesicherten Kanal aus.

#### <a name="fips"></a>FIPS

Teams verwendet FIPS (Federal Information Processing Standard) kompatible Algorithmen für den Austausch von Verschlüsselungsschlüsseln. Weitere Informationen zur Implementierung von FIPS finden Sie unter [Federal Information Processing Standard (FIPS) Publication 140-2](/microsoft-365/compliance/offering-fips-140-2).
