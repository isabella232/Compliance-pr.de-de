---
title: DSGVO für Project Server
description: Erfahren Sie, wie Sie mit Anforderungen der Datenschutz-Grundverordnung (DSGVO) in einer lokalen Project Server-Instanz umgehen.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: 092bbe9e7abe0329e822b011d41b5db96f33d169606945f5801bc36771a1944c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292942"
---
# <a name="gdpr-for-project-server"></a>DSGVO für Project Server

Project Server verwendet benutzerdefinierte Skripts zum Exportieren und Bearbeiten von Benutzerdaten in Project Web App. Die grundlegende Vorgehensweise sieht folgendermaßen aus:

1.  Suchen Sie die Project Web App-Websites in Ihrer Farm.

2.  Suchen Sie auf jeder Website die Projekte, die den Benutzer enthalten.

3.  Exportieren und überprüfen Sie die Arten von Daten, die Sie überprüfen möchten.

4.  Bearbeiten Sie die Daten bei Bedarf.

In den folgenden Artikeln werden diese Schritte ausführlich beschrieben:

- [Exportieren von Benutzerdaten aus Project Server](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [Löschen von Benutzerdaten aus Project Server](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


Beachten Sie, dass Project Server auf SharePoint Server aufbaut und Ereignisse in SharePoint-ULS-Protokollen und in der Verwendungsdatenbank protokolliert. Weitere Informationen finden Sie unter [DSGVO für SharePoint Server](gdpr-for-sharepoint-server.md).
