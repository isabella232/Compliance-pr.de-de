---
title: Isolierung und Zugriffskontrolle in Microsoft 365
description: 'Zusammenfassung: Eine Erläuterung der Isolation und Zugriffssteuerung innerhalb der verschiedenen Anwendungen von Microsoft 365.'
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
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ca0371d51bfe0b403805f259d87a8162e32bfd1e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088584"
---
# <a name="isolation-and-access-control-in-microsoft-365"></a>Isolation und Zugriffssteuerung in Microsoft 365

Azure Active Directory (Azure AD) und Microsoft 365 ein hoch komplexes Datenmodell verwenden, das Dutzende von Diensten, Hunderte von Entitäten, Tausende von Beziehungen und Tausende von Attributen umfasst. Auf hoher Ebene sind Azure AD und die Dienstverzeichnisse die Container von Mandanten und Empfängern, die mithilfe von statusbasierten Replikationsprotokollen synchronisiert werden. Zusätzlich zu den verzeichnisbasierten Informationen in Azure AD verfügt jede Dienstarbeitsauslastung über eine eigene Verzeichnisdienstinfrastruktur.
 
![Microsoft 365 Mandantendatensynchronisierung](../media/office-365-isolation-tenant-data-sync.png)

In diesem Modell gibt es keine einzige Quelle von Verzeichnisdaten. Bestimmte Systeme besitzen einzelne Datenelemente, aber kein einzelnes System enthält alle Daten. Microsoft 365 Dienste arbeiten in diesem Datenmodell mit Azure AD zusammen. Azure AD ist das "System der Wahrheit" für freigegebene Daten, bei dem es sich in der Regel um kleine und statische Daten handelt, die von jedem Dienst verwendet werden. Das in Microsoft 365 und Azure AD verwendete Verbundmodell stellt die freigegebene Ansicht der Daten bereit.

Microsoft 365 verwendet sowohl physischen Speicher als auch Azure-Cloudspeicher. Exchange Online (einschließlich Exchange Online Protection) und Skype for Business ihren eigenen Speicher für Kundendaten verwenden. SharePoint Online verwendet sowohl SQL Server Speicher als auch Azure Storage, daher ist eine zusätzliche Isolierung von Kundendaten auf Speicherebene erforderlich.

## <a name="exchange-online"></a>Exchange Online

Exchange Online speichert Kundendaten in Postfächern. Postfächer werden in ESE-Datenbanken (Extensible Storage Engine) gehostet, die als Postfachdatenbanken bezeichnet werden. Dazu gehören Benutzerpostfächer, verknüpfte Postfächer, freigegebene Postfächer und Postfächer für öffentliche Ordner. Benutzerpostfächer enthalten gespeicherte Skype for Business Inhalte, z. B. Aufgezeichnete Unterhaltungen.

Benutzerpostfachinhalte umfassen:

- E-Mails und E-Mail-Anlagen
- Kalenderinformationen und Frei/Gebucht-Informationen
- Kontakte
- Aufgaben
- Anmerkungen
- Gruppen
- Abgeleitete Daten

Jede Postfachdatenbank innerhalb Exchange Online enthält Postfächer aus mehreren Mandanten. Ein Autorisierungscode schützt jedes Postfach, auch innerhalb eines Mandanten. Standardmäßig hat nur der zugewiesene Benutzer Zugriff auf ein Postfach. Die Zugriffssteuerungsliste (Access Control List, ACL), die ein Postfach sichert, enthält eine Identität, die von Azure AD auf Mandantenebene authentifiziert wurde. Die Postfächer für jeden Mandanten sind auf Identitäten beschränkt, die mit dem Authentifizierungsanbieter des Mandanten authentifiziert werden, der nur Benutzer aus diesem Mandanten umfasst. Inhalte in Mandant A können von Benutzern in Mandant B in keiner Weise abgerufen werden, es sei denn, sie wurden explizit von Mandant A genehmigt.

## <a name="skype-for-business"></a>Skype for Business

Skype for Business speichert Daten an verschiedenen Stellen:

- Benutzer- und Kontoinformationen, einschließlich Verbindungsendpunkte, Mandanten-IDs, Wählpläne, Roamingeinstellungen, Anwesenheitsstatus, Kontaktlisten usw., werden in den Skype for Business Active Directory-Servern und auf verschiedenen Skype for Business Datenbankservern gespeichert. Kontaktlisten werden im Exchange Online Postfach des Benutzers gespeichert, wenn der Benutzer für beide Produkte aktiviert ist, oder auf Skype for Business Servern, wenn dies nicht der Fall ist. Skype for Business Datenbankserver werden nicht pro Mandant partitioniert, aber die Isolation von Daten mit mehreren Mandanten wird durch die rollenbasierte Zugriffssteuerung (RBAC) erzwungen.
- Besprechungsinhalte und hochgeladene Daten werden in DFS-Freigaben (Distributed File System) gespeichert. Dieser Inhalt kann auch in Exchange Online archiviert werden, wenn er aktiviert ist. Die DFS-Freigaben werden nicht pro Mandant partitioniert. Der Inhalt wird mit ACLs gesichert, und der Mehrmandant wird über RBAC erzwungen.
- Anrufdetaildatensätze, die den Aktivitätsverlauf darstellen, z. B. Anrufverlauf, Chatsitzungen, Anwendungsfreigabe, Chatverlauf usw., können auch in Exchange Online gespeichert werden. Die meisten Anrufdetaildatensätze werden jedoch vorübergehend auf KDS-Servern (Call Detail Record) gespeichert. Inhalte werden nicht pro Mandant partitioniert, sondern mehrinstanzenfähig über RBAC erzwungen.

## <a name="sharepoint-online"></a>SharePoint Online

SharePoint Online verfügt über mehrere unabhängige Mechanismen, die Datenisolation bereitstellen. Es speichert Objekte als abstrahierten Code in Anwendungsdatenbanken. Wenn ein Benutzer beispielsweise eine Datei in SharePoint Online hochlädt, wird die Datei zerlegt, in Anwendungscode übersetzt und in mehreren Tabellen über mehrere Datenbanken hinweg gespeichert.

Wenn ein Benutzer direkten Zugriff auf den Speicher erhalten könnte, der die Daten enthält, kann der Inhalt nicht für ein menschliches oder ein anderes System als SharePoint Online interpretiert werden. Zu diesen Mechanismen gehören sicherheitsbezogene Zugriffssteuerung und Eigenschaften. Alle SharePoint Onlineressourcen werden durch den Autorisierungscode und die RBAC-Richtlinie geschützt, auch innerhalb eines Mandanten. Die Zugriffssteuerungsliste (Access Control List, ACL), die eine Ressource sichert, enthält eine Identität, die auf Mandantenebene authentifiziert wurde. SharePoint Onlinedaten für einen Mandanten sind auf Identitäten beschränkt, die vom Authentifizierungsanbieter für den Mandanten authentifiziert wurden.

Zusätzlich zu den ACLs wird eine Eigenschaft auf Mandantenebene, die den Authentifizierungsanbieter angibt (d. h. der mandantenspezifische Azure AD), einmal geschrieben und kann nicht geändert werden, sobald er festgelegt wurde. Sobald die Mandanteneigenschaft des Authentifizierungsanbieters für einen Mandanten festgelegt wurde, kann sie nicht mithilfe von APIs geändert werden, die für einen Mandanten verfügbar gemacht werden.

Für jeden Mandanten wird eine eindeutige *SubscriptionId* verwendet. Alle Kundenwebsites befinden sich im Besitz eines Mandanten und weisen eine für den Mandanten eindeutige *SubscriptionId* zu. Die *SubscriptionId-Eigenschaft* auf einer Website wird einmal geschrieben und ist dauerhaft. Nachdem eine Website einem Mandanten zugewiesen wurde, kann sie nicht auf einen anderen Mandanten verschoben werden. Die *SubscriptionId* ist der Schlüssel, der zum Erstellen des Sicherheitsumfangs für den Authentifizierungsanbieter verwendet wird und an den Mandanten gebunden ist.

SharePoint Online verwendet SQL Server und Azure Storage für die Speicherung von Inhaltsmetadaten. Der Partitionsschlüssel für den Inhaltsspeicher ist *"SiteId"* in SQL. Beim Ausführen einer SQL Abfrage verwendet SharePoint Online eine *SiteId, die* als Teil einer *Abonnement-ID-Prüfung* auf Mandantenebene überprüft wurde.

SharePoint Online speichert verschlüsselte Dateiinhalte in Microsoft Azure Blobs. Jede SharePoint Onlinefarm verfügt über ein eigenes Microsoft Azure Konto, und alle in Azure gespeicherten Blobs werden einzeln mit einem Schlüssel verschlüsselt, der im SQL Inhaltsspeicher gespeichert ist. Der Verschlüsselungsschlüssel, der im Code durch die Autorisierungsebene geschützt und nicht direkt für den Endbenutzer verfügbar gemacht wird. SharePoint Online verfügt über eine Echtzeitüberwachung, um zu erkennen, wann eine HTTP-Anforderung Daten für mehr als einen Mandanten liest oder schreibt. Die *SubscriptionId* der Anforderungsidentität wird anhand der *SubscriptionId* der abgerufenen Ressource nachverfolgt. Anforderungen für den Zugriff auf Ressourcen von mehr als einem Mandanten sollten von Endbenutzern niemals ausgeführt werden. Dienstanforderungen in einer mehrinstanzenfähigen Umgebung sind die einzige Ausnahme. Beispielsweise ruft der Suchcrawler Inhaltsänderungen für eine gesamte Datenbank auf einmal ab. Dies umfasst in der Regel das Abfragen von Websites mit mehr als einem Mandanten in einer einzigen Serviceanfrage, was aus Effizienzgründen erfolgt.

## <a name="teams"></a>Teams

Ihre Teams Daten werden je nach Inhaltstyp unterschiedlich gespeichert. 

Eine ausführliche Erläuterung finden Sie in der [Ignite-Breakoutsitzung zu Microsoft Teams Architektur.](https://channel9.msdn.com/Events/Ignite/Microsoft-Ignite-Orlando-2017/BRK3071)

### <a name="core-teams-customer-data"></a>Kernkundendaten Teams

Wenn Ihr Mandant in Australien, Kanada, der Europäischen Union, Frankreich, Deutschland, Indien, Japan, Südafrika, Südkorea, der Schweiz (einschließlich Liechtenstein), den Vereinigten Arabischen Emiraten, dem Vereinigten Königreich oder den Vereinigten Staaten bereitgestellt wird, speichert Microsoft die folgenden ruhenden Kundendaten nur an diesem Standort:

- Teams Chats, Team- und Kanalunterhaltungen, Bilder, Voicemailnachrichten und Kontakte.
- SharePoint Online-Websiteinhalt und die auf der Website gespeicherten Dateien.
- Dateien, die in OneDrive für Arbeit oder Schule hochgeladen wurden.

#### <a name="chat-channel-messages-team-structure"></a>Chat, Kanalnachrichten, Teamstruktur

Jedes Team in Teams wird von einer Microsoft 365-Gruppe sowie deren SharePoint Website und Exchange Postfach unterstützt. Private Chats (einschließlich Gruppenchats), Nachrichten, die als Teil einer Unterhaltung in einem Kanal gesendet werden, und die Struktur von Teams und Kanälen werden in einem Chatdienst gespeichert, der in Azure ausgeführt wird. Die Daten werden auch in einem verborgenen Ordner in den Benutzer- und Gruppenpostfächern gespeichert, um Information Protection-Features zu aktivieren.

#### <a name="voicemail-and-contacts"></a>Voicemail und Kontakte

Voicemails werden in Exchange gespeichert. Kontakte werden in Exchange-basierten Clouddatenspeicher gespeichert. Exchange und der Exchange-basierte Cloudspeicher bieten bereits Datenaufbewahrung in jedem der weltweiten Rechenzentrumsregionen. Für alle Teams werden Voicemail und Kontakte in einem Land für Australien, Kanada, Frankreich, Deutschland, Indien, Japan, die Vereinigten Arabischen Emirate, das Vereinigte Königreich, Südafrika, Südkorea, die Schweiz (einschließlich Liechtenstein) und die Vereinigten Staaten gespeichert. Für alle anderen Länder werden Dateien basierend auf der Mandantenaffinität in den USA, Europa oder Asia-Pacific Speicherort gespeichert.

#### <a name="images-and-media"></a>Bilder und Medien

Medien, die in Chats verwendet werden (mit Ausnahme von Giphy GIFs, die nicht gespeichert sind, aber ein Verweislink zur ursprünglichen Giphy-Dienst-URL sind, ist Giphy ein Nicht-Microsoft-Dienst) werden in einem Azure-basierten Mediendienst gespeichert, der an den gleichen Speicherorten wie der Chatdienst bereitgestellt wird.

#### <a name="files"></a>Dateien

Dateien (einschließlich OneNote und Wiki), die jemand in einem Kanal teilt, werden auf der SharePoint Website des Teams gespeichert. Dateien, die während einer Besprechung oder eines Anrufs in einem privaten Chat oder Chat freigegeben wurden, werden hochgeladen und im OneDrive für das Geschäfts-, Schul- oder Unikonto des Benutzers gespeichert, der die Datei freigibt. Exchange, SharePoint und OneDrive bereits Datenaufbewahrung in jedem der weltweiten Rechenzentrumsregionen bereitstellen. Für bestehende Kunden werden also alle Dateien, OneNote Notizbücher, Teams Wiki-Inhalte und Postfächer, die Teil der Teams sind, bereits basierend auf Ihrer Mandantenaffinität am Speicherort gespeichert. Dateien werden in einem Land für Australien, Kanada, Frankreich, Deutschland, Indien, Japan, die Vereinigten Arabischen Emirate, das Vereinigte Königreich, Südafrika, Südkorea und die Schweiz (einschließlich Liechtenstein) gespeichert. Für alle anderen Länder werden Dateien basierend auf der Mandantenaffinität in den USA, Europa oder Asien-Pazifik gespeichert.
