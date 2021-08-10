---
title: DSGVO für Office Online Server und Office Web Apps Server
description: In diesem Artikel erfahren Sie, wie die DSGVO-Anforderungen für Office Online Server und Office Web Apps Server behandelt werden.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: MS-Compliance
ms.custom:
- seo-marvel-mar2020
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: fd47e5099d4ef57356658d6ee87f8f8307f4c084275e8d7afc2708fbde0ff19d
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54293036"
---
# <a name="gdpr-for-office-web-apps-server-and-office-online-server"></a>DSGVO für Office Web Apps Server und Office Online Server

Telemetriedaten von Office Online Server und Office Web Apps Server werden in Form von ULS-Protokollen gespeichert. Sie können ULS-Protokolle von Ihrem lokalen Mandanten mit [ULS Viewer](https://www.microsoft.com/download/details.aspx?id=44020) anzeigen.

Jede Protokollzeile enthält eine CorrelationID. Verwandte Protokollzeilen teilen sich die gleiche CorrelationID. Jede CorrelationID ist mit einer einzelnen SessionID verknüpft, und eine SessionID kann mit vielen CorrelationIDs zusammenhängen. Jede SessionID kann mit einer einzelnen UserID verknüpft sein, wobei einige Sitzungen anonym sein können und daher keine zugehörige UserID besitzen. Um zu bestimmen, welche Daten einem bestimmten Benutzer zugeordnet sind, ist es daher möglich, Zuordnungen vorzunehmen von einer einzelnen UserID zu den diesem Benutzer zugeordneten SessionIDs, von diesen SessionIDs zu den zugehörigen CorrelationIDs und von diesen CorrelationIDs zu allen Protokollen in diesen Korrelationen. Im nachstehenden Diagramm sind die Beziehungen zwischen den unterschiedlichen IDs dargestellt.

![Flussdiagramm, in dem die Beziehung zwischen SessionIDs und CorrelationIds dargestellt wird](../media/gdpr-for-office-online-server-image1.jpg)

## <a name="gathering-logs"></a>Erfassen von Protokollen

Um beispielsweise alle mit der UserID 1 verknüpften Protokolle zu sammeln, besteht der erste Schritt darin, alle Sitzungen zu sammeln, die mit UserID 1 verknüpft sind (d. h. SessionID 1 und SessionID2). Im nächsten Schritt werden alle Korrelationen erfasst, die SessionID 1 (d. h. CorrelationIDs 1, 2 und 3) und SessionID 2 (d. h. CorrelationID 4) zugeordnet sind. Sammeln Sie dann alle Protokolle, die mit jeder der Korrelationen in der Liste verknüpft sind.

1. ULS Viewer starten

2. Öffnen Sie das ULS-Protokoll für den gewünschten Zeitrahmen; ULS-Protokolle werden gespeichert unter %PROGRAMDATA%\\Microsoft\\OfficeWebApps\\Data\\Logs\\ULS

3. Bearbeiten | Filter ändern

4. Wenden Sie einen Filter folgender Art an:

    - EventID ist gleich apr3y

      Oder

    - EventID ist gleich bp2d6

5. Gehashte UserIDs werden sich in der Nachricht eines dieser beiden Ereignisse befinden.

6. Für apr3y wird die Nachricht einen Wert "UserID" und einen Wert "PUID" enthalten.

7. Für bp2d6 wird die Nachricht ziemlich viele Informationen enthalten. Das Feld für den Wert "LoggableUserId" enthält die gehashte UserID.

8. Nachdem die gehashte UserID aus einem der beiden Tags abgerufen wurde, enthält der Wert "WacSessionId" dieser Zeile in ULS Viewer die diesem Benutzer zugeordnete WacSessionId.

9. Erfassen Sie alle Werte "WacSessionId" für den betreffenden Benutzer.

10. Filtern Sie nach allen EventId gleich "xmnv", Nachrichten gleich „UserSessionId =\<WacSessionId\>“ für die erste WacSessionId in der Liste (ersetzen Sie den \<WacSessionId\>-Teil des Filters durch Ihre WacSessionId)

11. Erfassen Sie alle Korrelationswerte, die mit dieser WacSessionId übereinstimmen.

12. Wiederholen Sie die Schritte 10 bis 11 für alle Werte "WacSessionId" in der Liste für den betreffenden Benutzer.

13. Filtern Sie nach allen Korrelationen, die der ersten Korrelation in Ihrer Liste entsprechen.

14. Erfassen Sie alle Protokolle, die mit dieser Korrelation übereinstimmen.

15. Wiederholen Sie die Schritte 13 bis 14 für alle Korrelationswerte in der Liste für den betreffenden Benutzer.

## <a name="types-of-data"></a>Arten von Daten

Office-Protokolle enthalten eine Vielzahl von verschiedenen Arten von Daten. Nachfolgend finden Sie Beispiele für die Daten, die in ULS-Protokollen enthalten sein können:

- Fehlercodes für Probleme, die während der Nutzung des Produkts auftreten

- Klicks auf Schaltflächen und andere Daten zur App-Verwendung

- Leistungsdaten über die App und/oder bestimmte Features der App

- Allgemeine Standortinformationen darüber, wo sich der Computer des Benutzers befindet (z. B. Land/Region, Bundesland und Stadt, abgeleitet von der IP-Adresse), aber nicht der genaue geografische Standort.

- Grundlegende Metadaten über den Browser, z. B. Browsername und -version, und den Computer, z. B. Betriebssystemtyp und -version

- Fehlermeldungen vom Dokumentenhost (z. B. OneDrive, SharePoint, Exchange)

- Informationen zu App-internen Prozessen, die mit keiner Aktion des Benutzers zusammenhängen
