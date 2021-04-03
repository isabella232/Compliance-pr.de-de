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
hideEdit: true
ms.openlocfilehash: 54ea001e542cdd1ab078546cf96bd011e27ab1dc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497497"
---
# <a name="service-resource-limits"></a>Dienstressourcenbeschränkungen

Ressourcenbeschränkungen werden mithilfe von Kontingenten (Grenzwerten) und Drosselung erzwungen. Azure Active Directory (Azure AD) und die einzelnen Microsoft 365-Dienste verwenden beide Dienste. Grenzwerte sind dienstspezifisch und ändern sich im Laufe der Zeit, wenn neue Funktionen hinzugefügt werden. Weitere Informationen zu den aktuellen Grenzwerten für die verschiedenen Dienste finden Sie in den folgenden Themen:

- [Azure AD-Dienstbeschränkungen und -einschränkungen](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Exchange Online-Begrenzungen](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [Grenzen und Grenzen der SharePoint Online-Software](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype for Business-Beschränkungen](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer REST-API und Geschwindigkeitsbeschränkungen](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Dateigrößenbeschränkungen in Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Zusätzlich zu diesen Grenzwerten werden verschiedene Drosselungsmechanismen in Azure AD und Microsoft 365 verwendet. Die Einschränkung innerhalb des Diensts ist besonders wichtig, da Die Netzwerkressourcen in den Rechenzentren von Microsoft für die breite Palette von Kunden optimiert sind, die die Dienste verwenden. Zu den Drosselungsmechanismen gehören:

- Azure AD und Microsoft 365 bieten Eine Einschränkung auf Benutzerebene, die die Anzahl von Transaktionen oder gleichzeitigen Anrufen (durch Skript oder Code) eingrenzt, die von einem einzelnen Benutzer ausgeführt werden können.
- Jedem Mandanten wird bei der Mandantenerstellung eine standardmäßige PowerShell-Einschränkungsrichtlinie zugewiesen. Diese Einstellungen wirken sich auf andere Elemente aus, z. B. die maximale Anzahl gleichzeitiger PowerShell-Sitzungen, die von einem einzelnen Administrator geöffnet werden können.
- Jeder Exchange Online-Kunde verfügt über eine Standardmäßige Exchange Web Services (EWS)-Richtlinie, die auf EWS-Clientvorgänge abgestimmt ist, und Drosselung, die für alle Outlook-Clients gilt.
