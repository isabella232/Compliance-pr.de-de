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
ms.openlocfilehash: 77371208a5bd6d67fb9239ceebb18319b9a9253c265d7233ed789d75ba2e1815
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54287184"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>Verschlüsselung für Skype for Business, OneDrive for Business, SharePoint Online, Microsoft Teams und Exchange Online

Microsoft 365 ist eine äußerst sichere Umgebung, die umfassenden Schutz auf mehreren Ebenen bietet: Sicherheit des physischen Rechenzentrums, Netzwerksicherheit, Zugriffssicherheit, Anwendungssicherheit und Datensicherheit.

## <a name="skype-for-business"></a>Skype for Business

Skype for Business ruhenden Kundendaten können in Form von Dateien oder Präsentationen gespeichert werden, die von Besprechungsteilnehmern hochgeladen werden. Der Webkonferenzserver verschlüsselt Kundendaten mithilfe von AES mit einem 256-Bit-Schlüssel. Die verschlüsselten Kundendaten werden in einer Dateifreigabe gespeichert. Jedes Kundendaten wird mit einem anderen zufällig generierten 256-Bit-Schlüssel verschlüsselt. Wenn ein Teil der Kundendaten in einer Konferenz freigegeben wird, weist der Webkonferenzserver die Konferenzclients an, die verschlüsselten Kundendaten über HTTPS herunterzuladen. Er sendet den entsprechenden Schlüssel an Clients, damit die Kundendaten entschlüsselt werden können. Der Webkonferenzserver authentifiziert auch Konferenzclients, bevor er den Clients den Zugriff auf Konferenzkundendaten zulässt. Bei der Teilnahme an einer Webkonferenz richtet jeder Konferenzclient ein SIP-Dialogfeld mit der Konferenzfokuskomponente ein, die zuerst auf dem Front-End-Server über TLS ausgeführt wird. Der Konferenzfokus übergibt an den Konferenzclient ein vom Webkonferenzserver generiertes Authentifizierungscookie. Der Konferenzclient stellt dann eine Verbindung mit dem Webkonferenzserver her, der das Authentifizierungscookie darstellt, das vom Server authentifiziert werden soll.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online und OneDrive for Business

Alle Kundendateien in SharePoint Online werden durch eindeutige Dateischlüssel geschützt, die immer für einen einzelnen Mandanten exklusiv sind. Die Schlüssel werden entweder vom SharePoint Onlinedienst erstellt und verwaltet, oder wenn Customer Key von Kunden verwendet, erstellt und verwaltet wird. Wenn eine Datei hochgeladen wird, erfolgt die Verschlüsselung von SharePoint Online im Kontext der Uploadanforderung, bevor sie an Azure Storage gesendet wird. Wenn eine Datei heruntergeladen wird, ruft SharePoint Online die verschlüsselten Kundendaten basierend auf der eindeutigen Dokument-ID aus dem Azure-Speicher ab und entschlüsselt die Kundendaten, bevor sie an den Benutzer gesendet werden. Azure Storage hat keine Möglichkeit, Kundendaten zu entschlüsseln oder sogar zu identifizieren oder zu verstehen. Die gesamte Verschlüsselung und Entschlüsselung erfolgt in denselben Systemen, die die Mandantenisolation erzwingen, die Azure Active Directory und online SharePoint werden.

Mehrere Workloads in Microsoft 365 Daten in SharePoint Online speichern, einschließlich Microsoft Teams, die alle Dateien in SharePoint Online speichert, und OneDrive for Business, die SharePoint Online für den Speicher verwendet. Alle Kundendaten, die in SharePoint Online gespeichert sind, werden verschlüsselt (mit einem oder mehreren AES 256-Bit-Schlüsseln) und wie folgt über das Rechenzentrum verteilt. (Bei jedem Schritt dieses Verschlüsselungsprozesses wird FIPS 140-2 Level 2 überprüft. Weitere Informationen zur FIPS 140-2-Compliance finden Sie unter [FIPS 140-2 Compliance.)](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105))

- Jede Datei wird je nach Dateigröße in einen oder mehrere Blöcke aufgeteilt. Jeder Block wird mit einem eigenen eindeutigen AES-256-Bit-Schlüssel verschlüsselt.
- Wenn eine Datei aktualisiert wird, wird die Aktualisierung auf die gleiche Weise behandelt: Die Änderung wird in einen oder mehrere Blöcke aufgeteilt, und jeder Block wird mit einem separaten eindeutigen Schlüssel verschlüsselt.
- Diese Datenblöcke – Dateien, Dateiteile und Aktualisierungsdelta – werden als Blobs im Azure-Speicher gespeichert, die nach dem Zufallsprinzip über mehrere Azure-Speicherkonten verteilt werden.
- Der Satz von Verschlüsselungsschlüsseln für diese Kundendatenblöcke wird selbst verschlüsselt.

    - Die zum Verschlüsseln der Blobs verwendeten Schlüssel werden in der SharePoint Onlineinhaltsdatenbank gespeichert.
    - Die Inhaltsdatenbank ist durch Datenbankzugriffssteuerungen und ruhenden Verschlüsselung geschützt. Die Verschlüsselung erfolgt [mithilfe von Transparent Data Encryption](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (TDE) in [Azure SQL-Datenbank](/azure/sql-database/sql-database-technical-overview). (Azure SQL-Datenbank ist ein allgemeiner relationaler Datenbankdienst in Microsoft Azure, der Strukturen wie relationale Daten, JSON, räumliche Daten und XML unterstützt.) Diese geheimen Schlüssel befinden sich auf Dienstebene für SharePoint Online, nicht auf Mandantenebene. Diese geheimen Schlüssel (manchmal auch als Masterschlüssel bezeichnet) werden in einem separaten sicheren Repository gespeichert, das key Store genannt wird. TDE bietet ruhenden Sicherheit sowohl für die aktive Datenbank als auch für die Datenbanksicherungen und Transaktionsprotokolle.
    - Wenn Kunden den optionalen Schlüssel bereitstellen, wird der Kundenschlüssel in Azure Key Vault gespeichert, und der Dienst verwendet den Schlüssel zum Verschlüsseln eines Mandantenschlüssels, der zum Verschlüsseln eines Websiteschlüssels verwendet wird, der dann zum Verschlüsseln der Schlüssel auf Dateiebene verwendet wird. Im Wesentlichen wird eine neue Schlüsselhierarchie eingeführt, wenn der Kunde einen Schlüssel bereitstellt.
- Die Zuordnung, die zum erneuten Zusammenstellen der Datei verwendet wird, wird zusammen mit den verschlüsselten Schlüsseln in der Inhaltsdatenbank gespeichert, getrennt vom Hauptschlüssel, der zum Entschlüsseln benötigt wird.
- Jedes Azure-Speicherkonto verfügt über eigene eindeutige Anmeldeinformationen pro Zugriffstyp (Lesen, Schreiben, Aufzählen und Löschen). Jeder Satz von Anmeldeinformationen wird im sicheren Schlüsselspeicher aufbewahrt und regelmäßig aktualisiert. Wie oben beschrieben, gibt es drei verschiedene Speichertypen mit jeweils einer bestimmten Funktion:
    - Kundendaten werden als verschlüsselte Blobs im Azure-Speicher gespeichert. Der Schlüssel für jeden Datenblock wird verschlüsselt und separat in der Inhaltsdatenbank gespeichert. Die Kundendaten selbst enthalten keine Hinweise darauf, wie sie entschlüsselt werden können.
    - Die Inhaltsdatenbank ist eine SQL Server-Datenbank. Es enthält die zuordnung erforderlich, um die Kundendaten-Blobs im Azure-Speicher zu suchen und neu zusammenzusetzen, sowie die Schlüssel, die zum Verschlüsseln dieser Blobs erforderlich sind. Der Satz von Schlüsseln wird jedoch selbst verschlüsselt (wie oben erläutert) und in einem separaten Key-Store gespeichert.
    - Der schlüsselbasierte Store ist physisch von der Inhaltsdatenbank und dem Azure-Speicher getrennt. Es enthält die Anmeldeinformationen für jeden Azure-Speichercontainer und den Hauptschlüssel für den Satz verschlüsselter Schlüssel in der Inhaltsdatenbank.

Jede dieser drei Speicherkomponenten – der Azure Blob Store, die Inhaltsdatenbank und die Key-Store – ist physisch getrennt. Die Informationen in einer der Komponenten sind allein unbrauchbar. Ohne Zugriff auf alle drei Elemente ist es unmöglich, die Schlüssel für die Blöcke abzurufen, die Schlüssel zu entschlüsseln, um sie verwendbar zu machen, die Schlüssel den entsprechenden Blöcken zuzuordnen, jeden Block zu entschlüsseln oder ein Dokument aus den einzelnen Blöcken zu rekonstruieren.

BitLocker-Zertifikate, die die physischen Datenträgervolumes auf Computern im Rechenzentrum schützen, werden in einem sicheren Repository (dem SharePoint Geheimen Onlinespeicher) gespeichert, das durch den Farmschlüssel geschützt ist.

Die TDE-Schlüssel, die die blobbasierten Schlüssel schützen, werden an zwei Speicherorten gespeichert:

- Das sichere Repository, das die BitLocker-Zertifikate enthält und durch den Farmschlüssel geschützt ist; Und
- In einem sicheren Repository, das von Azure SQL-Datenbank verwaltet wird.

Die für den Zugriff auf die Azure-Speichercontainer verwendeten Anmeldeinformationen werden auch im SharePoint Geheimen Onlinespeicher gespeichert und bei Bedarf an jede SharePoint Onlinefarm delegiert. Bei diesen Anmeldeinformationen handelt es sich um Azure Storage SAS-Signaturen mit separaten Anmeldeinformationen, die zum Lesen oder Schreiben von Daten verwendet werden, und mit angewendeter Richtlinie, sodass sie alle 60 Tage automatisch ablaufen. Verschiedene Anmeldeinformationen werden zum Lesen oder Schreiben von Daten (nicht beides) verwendet, und SharePoint Onlinefarmen keine Berechtigungen zum Aufzählen erteilt werden.

> [!NOTE]
> Für kunden mit Office 365 US-Regierungsbehörden werden Datenblobs in Azure U.S. Government Storage gespeichert. Darüber hinaus ist der Zugriff auf SharePoint Onlineschlüssel in Office 365 U.S. Government auf Office 365 Mitarbeiter beschränkt, die speziell überprüft wurden. Mitarbeiter von Azure U.S. Government operations haben keinen Zugriff auf den SharePoint Online-Schlüsselspeicher, der zum Verschlüsseln von Datenblobs verwendet wird.

Weitere Informationen zur Datenverschlüsselung in SharePoint Online und OneDrive for Business finden Sie unter [Datenverschlüsselung in OneDrive for Business und SharePoint Online.](https://technet.microsoft.com/library/dn905447.aspx)

### <a name="list-items-in-sharepoint-online"></a>Elemente in SharePoint Online auflisten

Listenelemente sind kleinere Kundendatenblöcke, die ad-hoc erstellt werden oder dynamisch innerhalb einer Website ausgeführt werden können, z. B. Zeilen in einer vom Benutzer erstellten Liste, einzelne Beiträge in einem SharePoint Onlineblog oder Einträge innerhalb einer SharePoint Online-Wiki-Seite. Listenelemente werden in der Inhaltsdatenbank (Azure SQL-Datenbank) gespeichert und mit TDE geschützt.

## <a name="encryption-of-data-in-transit"></a>Verschlüsselung von Daten während der Übertragung

In OneDrive for Business und SharePoint Online gibt es zwei Szenarien, in denen Daten in Rechenzentren ein- und ausgehen.

- **Clientkommunikation mit dem Server** – Die Kommunikation mit SharePoint Online und OneDrive for Business über das Internet verwendet TLS-Verbindungen.
- **Datenverlagerung zwischen Rechenzentren** – Der Hauptgrund für das Verschieben von Daten zwischen Rechenzentren ist die Georeplikation, um die Notfallwiederherstellung zu ermöglichen. Beispielsweise werden SQL Server-Transaktionsprotokolle und BLOB-Speicher-Deltas entlang dieser Pipe übertragen. Während diese Daten bereits über ein privates Netzwerk übertragen werden, werden sie zusätzlich durch branchenbeste Verschlüsselung geschützt.

## <a name="exchange-online"></a>Exchange Online

Exchange Online BitLocker für alle Postfachdaten verwendet, und die BitLocker-Konfiguration wird in [BitLocker for Encryption](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption)beschrieben. Die Verschlüsselung auf Dienstebene verschlüsselt alle Postfachdaten auf Postfachebene. 

Zusätzlich zur Dienstverschlüsselung unterstützt Microsoft 365 Customer Key, der auf der Dienstverschlüsselung basiert. Customer Key ist eine von Microsoft verwaltete Schlüsseloption für Exchange Online Dienstverschlüsselung, die auch in der Microsoft-Roadmap enthalten ist. Diese Verschlüsselungsmethode bietet einen erhöhten Schutz, der nicht von BitLocker geboten wird, da es eine Trennung von Serveradministratoren und kryptografischen Schlüsseln ermöglicht, die für die Entschlüsselung von Daten erforderlich sind, und da die Verschlüsselung direkt auf die Daten angewendet wird (im Gegensatz zu BitLocker, das die Verschlüsselung auf dem logischen Datenträgervolume anwendet), bleiben alle von einem Exchange Server kopierten Kundendaten verschlüsselt.

Der Bereich für Exchange Online Dienstverschlüsselung sind Kundendaten, die im Ruhezustand innerhalb Exchange Online gespeichert werden. (Skype for Business speichert fast alle vom Benutzer generierten Inhalte im postfach Exchange Online des Benutzers und erbt daher das Dienstverschlüsselungsfeature von Exchange Online.)


## <a name="microsoft-teams"></a>Microsoft Teams

Teams verwendet TLS und MTLS zum Verschlüsseln von Chatnachrichten. Der gesamte Datenverkehr zwischen den Servern erfordert MTLS, und zwar unabhängig davon, ob die Daten innerhalb des internen Netzwerks verbleiben oder den internen Netzwerkumkreis verlassen.

In dieser Tabelle werden die von Teams verwendeten Protokolle zusammengefasst.

|**Datenverkehrstyp**|**Verschlüsselt von**|
|:-----|:-----|
|Server-zu-Server|Mtls|
|Client-zu-Server (z. B. Chat und Anwesenheit)|TLS|
|Medienflüsse (z. B. Audio- und Videofreigabe von Medien)|TLS|
|Audio- und Videofreigabe von Medien|SRTP/TLS|
|Signalisierung|TLS|

#### <a name="media-encryption"></a>Medienverschlüsselung

Der Mediendatenverkehr wird mit Secure RTP (SRTP) verschlüsselt, einem Profil von Real-Time Transport Protocol (RTP), das Vertraulichkeit, Authentifizierung und Replay-Angriffsschutz für RTP-Datenverkehr bereitstellt. SRTP verwendet einen Sitzungsschlüssel, der mithilfe eines sicheren Zufallszahlengenerators generiert wird und mithilfe des TLS-Signalkanals ausgetauscht wird. Client-zu-Client-Mediendatenverkehr wird über eine Client-zu-Server-Verbindungssignalisierung ausgehandelt, wird jedoch mit SRTP verschlüsselt, wenn Client-zu-Client direkt ausgeführt wird.

Teams verwendet ein anmeldeinformationsbasiertes Token für den sicheren Zugriff auf Medienrelays über TURN. Medienrelays tauschen das Token über einen TLS-gesicherten Kanal aus.

#### <a name="fips"></a>Fips

Teams verwendet FIPS-konforme Algorithmen (Federal Information Processing Standard) für den Austausch von Verschlüsselungsschlüsseln. Weitere Informationen zur Implementierung von FIPS finden Sie unter [Federal Information Processing Standard (FIPS) Publication 140-2.](/microsoft-365/compliance/offering-fips-140-2)
