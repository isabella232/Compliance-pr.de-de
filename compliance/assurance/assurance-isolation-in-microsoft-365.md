---
title: Isolierung und Zugriffskontrolle in Microsoft 365
description: 'Zusammenfassung: Eine Erläuterung der Isolation und Zugriffssteuerung in den verschiedenen Anwendungen von Microsoft 365.'
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
ms.openlocfilehash: f1166ce766c2b1158d50242b9411f051992bf121
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497051"
---
# <a name="isolation-and-access-control-in-microsoft-365"></a>Isolation und Zugriffssteuerung in Microsoft 365

Azure Active Directory (Azure AD) und Microsoft 365 verwenden ein hochkomplexes Datenmodell, das Dutzende von Diensten, Hunderte von Entitäten, Tausende von Beziehungen und Zehntausende von Attributen umfasst. Auf hoher Ebene sind Azure AD und die Dienstverzeichnissen die Container von Mandanten und Empfängern, die mithilfe zustandsbasierter Replikationsprotokolle synchron gehalten werden. Zusätzlich zu den Verzeichnisinformationen, die in Azure AD gespeichert sind, verfügen alle Dienstworkloads über eine eigene Verzeichnisdiensteinfrastruktur.
 
![Microsoft 365-Mandantendatensynchronisierung](../media/office-365-isolation-tenant-data-sync.png)

In diesem Modell gibt es keine einzige Quelle für Verzeichnisdaten. Bestimmte Systeme besitzen einzelne Datenteile, aber kein einzelnes System enthält alle Daten. Microsoft 365-Dienste arbeiten in diesem Datenmodell mit Azure AD zusammen. Azure AD ist das "System der Wahrheit" für freigegebene Daten, bei denen es sich in der Regel um kleine und statische Daten handelt, die von jedem Dienst verwendet werden. Das verbundmodell, das in Microsoft 365 und Azure AD verwendet wird, stellt die freigegebene Ansicht der Daten bereit.

Microsoft 365 verwendet sowohl physischen Speicher als auch Azure-Cloudspeicher. Exchange Online (einschließlich Exchange Online Protection) und Skype for Business verwenden ihren eigenen Speicher für Kundendaten. SharePoint Online verwendet sowohl SQL Server als auch Azure Storage, daher ist eine zusätzliche Isolation von Kundendaten auf Speicherebene nötig.

## <a name="exchange-online"></a>Exchange Online

Exchange Online speichert Kundendaten in Postfächern. Postfächer werden in ESE(Extensible Storage Engine)-Datenbanken gehostet, die als Postfachdatenbanken bezeichnet werden. Dazu gehören Benutzerpostfächer, verknüpfte Postfächer, freigegebene Postfächer und Postfächer für öffentliche Ordner. Benutzerpostfächer enthalten gespeicherte Skype for Business-Inhalte, z. B. Unterhaltungshistorien.

Zu den Inhalten von Benutzerpostfächern gehören:

- E-Mails und E-Mail-Anlagen
- Kalender- und Frei/Gebucht-Informationen
- Kontakte
- Aufgaben
- Anmerkungen
- Gruppen
- Rückschlussdaten

Jede Postfachdatenbank in Exchange Online enthält Postfächer von mehreren Mandanten. Ein Autorisierungscode sichert jedes Postfach, auch innerhalb einer Mandanz. Standardmäßig hat nur der zugewiesene Benutzer Zugriff auf ein Postfach. Die Zugriffssteuerungsliste (Access Control List, ACL), die ein Postfach sichert, enthält eine Identität, die von Azure AD auf Mandantenebene authentifiziert wurde. Die Postfächer für jeden Mandanten sind auf Identitäten beschränkt, die beim Authentifizierungsanbieter des Mandanten authentifiziert werden, der nur Benutzer aus diesem Mandanten umfasst. Inhalte in Mandant A können in keinem Fall von Benutzern in Mandant B erworben werden, es sei denn, sie wurden explizit von Mandant A genehmigt.

## <a name="skype-for-business"></a>Skype for Business

Skype for Business speichert Daten an verschiedenen Orten:

- Benutzer- und Kontoinformationen, die Verbindungsendpunkte, Mandanten-IDs, Wählpläne, Roamingeinstellungen, Anwesenheitsstatus, Kontaktlisten usw. umfassen, werden auf den Skype for Business Active Directory-Servern und auf verschiedenen Skype for Business-Datenbankservern gespeichert. Kontaktlisten werden im Exchange Online-Postfach des Benutzers gespeichert, wenn der Benutzer für beide Produkte aktiviert ist, oder auf Skype for Business-Servern, wenn der Benutzer dies nicht ist. Skype for Business-Datenbankserver werden nicht pro Mandant partitioniert, aber die Mehr-Mandanten-Isolation von Daten wird über die rollenbasierte Zugriffssteuerung (ROLEAC) erzwungen.
- Besprechungsinhalte und hochgeladene Daten werden in DFS-Freigaben (Distributed File System) gespeichert. Dieser Inhalt kann auch in Exchange Online archiviert werden, wenn er aktiviert ist. Die DFS-Freigaben werden nicht pro Mandant partitioniert. Der Inhalt wird mit ACLs gesichert, und mehrverdachtige Inhalte werden über die RBAC erzwungen.
- Anrufdetaildatensätze, bei denen es sich um den Aktivitätsverlauf handelt, z. B. Anrufverlauf, Anrufsitzungen, Anwendungsfreigabe, Anrufverlauf usw., können auch in Exchange Online gespeichert werden, die meisten Anrufdetaildatensätze werden jedoch vorübergehend auf Anrufdetaildatensätzen (Call Detail Record, CDR)-Servern gespeichert. Inhalte werden nicht pro Mandant partitioniert, aber mehr mandantenfähigkeit wird über rbAC erzwungen.

## <a name="sharepoint-online"></a>SharePoint Online

SharePoint Online verfügt über mehrere unabhängige Mechanismen, die die Datenisolation bereitstellen. Es speichert Objekte als abstrahierten Code in Anwendungsdatenbanken. Wenn ein Benutzer beispielsweise eine Datei in SharePoint Online hochlädt, wird die Datei zerlegt, in Anwendungscode übersetzt und in mehreren Tabellen in mehreren Datenbanken gespeichert.

Wenn ein Benutzer direkten Zugriff auf den Speicher mit den Daten erhalten könnte, ist der Inhalt für einen Menschen oder ein anderes System als SharePoint Online nicht interpretierbar. Zu diesen Mechanismen gehören die Sicherheitszugriffssteuerung und -eigenschaften. Alle SharePoint Online-Ressourcen werden durch den Autorisierungscode und die RBAC-Richtlinie gesichert, einschließlich innerhalb einer Mandanz. Die Zugriffssteuerungsliste (Access Control List, ACL), die eine Ressource sichert, enthält eine auf Mandantenebene authentifizierte Identität. SharePoint Online-Daten für einen Mandanten sind auf Identitäten beschränkt, die vom Authentifizierungsanbieter für den Mandanten authentifiziert werden.

Zusätzlich zu den ACLs wird eine Eigenschaft auf Mandantenebene, die den Authentifizierungsanbieter angibt (bei dem es sich um den mandantenspezifischen Azure AD handelt), einmal geschrieben und kann nicht einmal festgelegt geändert werden. Nachdem die Mandanteneigenschaft des Authentifizierungsanbieters für einen Mandanten festgelegt wurde, kann sie nicht mithilfe von APIs geändert werden, die für einen Mandanten verfügbar gemacht werden.

Für jeden Mandanten wird eine eindeutige *SubscriptionId* verwendet. Alle Kundenwebsites gehören einem Mandanten und haben eine *SubscriptionId zugewiesen,* die für den Mandanten eindeutig ist. Die *SubscriptionId-Eigenschaft* auf einer Website wird einmal geschrieben und ist dauerhaft. Nachdem sie einem Mandanten zugewiesen wurde, kann eine Website nicht in einen anderen Mandanten verschoben werden. Die *SubscriptionId ist* der Schlüssel, der zum Erstellen des Sicherheitsbereichs für den Authentifizierungsanbieter verwendet wird und an den Mandanten gebunden ist.

SharePoint Online verwendet SQL Server und Azure Storage für die Speicherung von Inhaltsmetadaten. Der Partitionsschlüssel für den Inhaltsspeicher ist *SiteId* in SQL. Beim Ausführen einer SQL verwendet SharePoint Online eine *SiteId,* die im Rahmen einer *SubscriptionId-Prüfung* auf Mandantenebene überprüft wurde.

SharePoint Online speichert verschlüsselte Dateiinhalte in Microsoft Azure-Blobs. Jede SharePoint Online-Farm verfügt über ein eigenes Microsoft Azure-Konto, und alle in Azure gespeicherten Blobs werden einzeln mit einem Schlüssel verschlüsselt, der im SQL gespeichert ist. Der Verschlüsselungsschlüssel, der im Code durch die Autorisierungsebene geschützt und nicht direkt für den Endbenutzer verfügbar gemacht wird. SharePoint Online verfügt über Echtzeitüberwachung, um zu erkennen, wann eine HTTP-Anforderung Daten für mehr als einen Mandanten liest oder schreibt. Die Anforderungsidentität *SubscriptionId* wird mit der *SubscriptionId* der ressource, auf die zugegriffen wird, nachverfolgt. Anforderungen für den Zugriff auf Ressourcen von mehr als einem Mandanten sollten von Endbenutzern niemals auftreten. Dienstanforderungen in einer Umgebung mit mehreren Mandanten sind die einzige Ausnahme. Der Suchcrawler z. B. zieht Inhaltsänderungen für eine gesamte Datenbank auf einmal ab. Dies umfasst in der Regel das Abfragen von Websites von mehr als einem Mandanten in einer einzelnen Dienstanforderung, was aus Effizienzgründen erfolgt.

## <a name="teams"></a>Teams

Ihre Teams-Daten werden je nach Inhaltstyp unterschiedlich gespeichert. 

Eine ausführliche Diskussion erhalten Sie in der [Ignite-Unterbrechungssitzung](https://channel9.msdn.com/Events/Ignite/Microsoft-Ignite-Orlando-2017/BRK3071) zur Microsoft Teams-Architektur.

### <a name="core-teams-customer-data"></a>Kernkundendaten von Teams

Wenn Ihr Mandant in Australien, Kanada, der Europäischen Union, Frankreich, Deutschland, Indien, Japan, Südafrika, Südkorea, der Schweiz (einschließlich Liechtenstein), den Vereinigten Arabischen Emiraten, dem Vereinigten Königreich oder den Vereinigten Staaten bereitgestellt wird, speichert Microsoft die folgenden Ruhedaten nur an diesem Ort:

- Teams-Chats, Team- und Kanalunterhaltungen, Bilder, Voicemailnachrichten und Kontakte.
- SharePoint Online-Websiteinhalt und die auf der Website gespeicherten Dateien.
- Dateien, die auf OneDrive für Arbeit oder Schule hochgeladen werden.

#### <a name="chat-channel-messages-team-structure"></a>Chat, Kanalnachrichten, Teamstruktur

Jedes Team in Teams wird von einer Microsoft 365-Gruppe und ihrer SharePoint-Website und dem Exchange-Postfach unterstützt. Private Chats (einschließlich Gruppenchats), Nachrichten, die als Teil einer Unterhaltung in einem Kanal gesendet werden, sowie die Struktur von Teams und Kanälen werden in einem Chatdienst gespeichert, der in Azure ausgeführt wird. Die Daten werden auch in einem ausgeblendeten Ordner in den Benutzer- und Gruppenpostfächern gespeichert, um Die Information Protection-Features zu aktivieren.

#### <a name="voicemail-and-contacts"></a>Voicemail und Kontakte

Voicemails werden in Exchange gespeichert. Kontakte werden im Exchange-basierten Clouddatenspeicher gespeichert. Exchange und der Exchange-basierte Cloudspeicher bieten bereits datenresidenz in jedem der weltweiten Rechenzentrums-Geos. Für alle Teams werden Voicemail und Kontakte für Australien, Kanada, Frankreich, Deutschland, Indien, Japan, die Vereinigten Arabischen Emirate, das Vereinigte Königreich, Südafrika, Südkorea, die Schweiz (einschließlich Liechtenstein) und die Vereinigten Staaten gespeichert. Für alle anderen Länder werden Dateien basierend auf der Mandantenaffinität in den USA, Europa oder Asia-Pacific gespeichert.

#### <a name="images-and-media"></a>Bilder und Medien

In Chats verwendete Medien (mit Ausnahme von Giphy-GIFs, die nicht gespeichert sind, aber ein Verweislink zur ursprünglichen Giphy-Dienst-URL sind, giphy ist ein Nicht-Microsoft-Dienst) werden in einem Azure-basierten Mediendienst gespeichert, der an denselben Speicherorten wie der Chatdienst bereitgestellt wird.

#### <a name="files"></a>Dateien

Dateien (einschließlich OneNote und Wiki), die jemand in einem Kanal teilt, werden auf der SharePoint-Website des Teams gespeichert. Dateien, die in einem privaten Chat oder einem Chat während einer Besprechung oder eines Anrufs freigegeben wurden, werden hochgeladen und im OneDrive for work- oder Schulkonto des Benutzers gespeichert, der die Datei freigegeben hat. Exchange, SharePoint und OneDrive bieten bereits datenresidenz in jedem der weltweiten Datencenter-Geos. Für vorhandene Kunden werden also alle Dateien, OneNote-Notizbücher, Teams-Wiki-Inhalte und Postfächer, die Teil der Teams-Erfahrung sind, bereits basierend auf Ihrer Mandantenaffinität am Speicherort gespeichert. Dateien werden im Land für Australien, Kanada, Frankreich, Deutschland, Indien, Japan, die Vereinigten Arabischen Emirate, das Vereinigte Königreich, Südafrika, Südkorea und die Schweiz (einschließlich Liechtenstein) gespeichert. Für alle anderen Länder werden Dateien basierend auf der Mandantenaffinität am Standort USA, Europa oder Asien-Pazifik gespeichert.
