---
title: Microsoft 365-Ressourcenbeschränkungen
description: In diesem Artikel finden Sie Informationen zu Ressourcenbeschränkungen für die verschiedenen Anwendungen in Microsoft 365.
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
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 632a0b78c5c5ba02a59f8863c2e751f009cc968e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120754"
---
# <a name="service-resource-limits"></a>Dienstressourcenbeschränkungen

Ressourcenbeschränkungen werden mithilfe von Kontingenten (Grenzwerten) und Drosselung erzwungen. Azure Active Directory (Azure AD) und die einzelnen Microsoft 365-Dienste verwenden beide. Die Grenzwerte sind dienstspezifisch und ändern sich im Laufe der Zeit, wenn neue Funktionen hinzugefügt werden. Weitere Informationen zu den aktuellen Grenzwerten für die verschiedenen Dienste finden Sie in den folgenden Themen:

- [Azure AD -Dienstbeschränkungen und -einschränkungen](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Exchange Online-Begrenzungen](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePoint Online Softwarebeschränkungen und -grenzen](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Grenzwerte für Skype for Business](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer REST-API und -Grenzwerte](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Dateigrößenbeschränkungen in Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Zusätzlich zu diesen Grenzwerten werden mehrere Drosselungsmechanismen in Azure AD und Microsoft 365 verwendet. Die Einschränkung innerhalb des Diensts ist besonders wichtig, da die Netzwerkressourcen in den Rechenzentren von Microsoft für die breite Palette von Kunden optimiert sind, die die Dienste nutzen. Zu den Drosselungsmechanismen gehören:

- Azure AD und Microsoft 365 bieten Drosselung auf Benutzerebene, die die Anzahl von Transaktionen oder gleichzeitigen Aufrufen (durch Skript oder Code) eingrenzt, die von einem einzelnen Benutzer ausgeführt werden können.
- Jedem Mandanten wird bei der Mandantenerstellung eine standardmäßige PowerShell-Einschränkungsrichtlinie zugewiesen. Diese Einstellungen wirken sich auf andere Elemente aus, z. B. die maximale Anzahl gleichzeitiger PowerShell-Sitzungen, die von einem einzelnen Administrator geöffnet werden können.
- Jeder Exchange Online-Kunde verfügt über eine standardmäßige Exchange Web Services (EWS)-Richtlinie, die auf die Vorgänge des EWS-Clients abgestimmt ist, und Drosselung, die für alle Outlook-Clients gilt.
