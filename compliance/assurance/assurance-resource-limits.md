---
title: Microsoft 365 Ressourcenbeschränkungen
description: In diesem Artikel finden Sie Informationen zu Ressourcenbeschränkungen für die verschiedenen Anwendungen innerhalb Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: 764259e22b23ecc7cea363283fc313a94875a2d1
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481787"
---
# <a name="service-resource-limits"></a>Dienstressourcenbeschränkungen

Ressourcenbeschränkungen werden mithilfe von Kontingenten (Grenzwerten) und Drosselung erzwungen. Azure Active Directory (Azure AD) und die einzelnen Microsoft 365-Dienste verwenden beide Dienste. Grenzwerte sind dienstspezifisch und ändern sich im Laufe der Zeit, wenn neue Funktionen hinzugefügt werden. Ausführliche Informationen zu den aktuellen Grenzwerten für die verschiedenen Dienste finden Sie in den folgenden Themen:

- [Azure AD-Dienstbeschränkungen und -Einschränkungen](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Exchange Online-Begrenzungen](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePoint Grenzen und Grenzen von Onlinesoftware](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype for Business Grenzen](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer REST-API und Ratengrenzen](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Dateigrößenbeschränkungen in Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Zusätzlich zu diesen Grenzwerten werden mehrere Drosselungsmechanismen in Azure AD und Microsoft 365 verwendet. Die Drosselung innerhalb des Diensts ist besonders wichtig, da Netzwerkressourcen in den Rechenzentren von Microsoft für die breite Gruppe von Kunden optimiert sind, die die Dienste verwenden. Zu den Einschränkungsmechanismen gehören:

- Azure AD und Microsoft 365 Drosselung auf Featureebene, die die Anzahl der Transaktionen oder gleichzeitigen Aufrufe (durch Skript oder Code) einschränkt, die von einem einzelnen Benutzer ausgeführt werden können.
- Jeder Mandant wird bei der Mandantenerstellung eine Standardmäßige PowerShell-Einschränkungsrichtlinie zugewiesen. Diese Einstellungen wirken sich auf andere Elemente aus, z. B. die maximale Anzahl gleichzeitiger PowerShell-Sitzungen, die von einem einzelnen Administrator geöffnet werden können.
- Jeder Exchange Online Kunde verfügt über eine standardmäßige EWS-Richtlinie (Exchange Web Services), die auf EWS-Clientvorgänge abgestimmt ist, sowie eine Einschränkung, die für alle Outlook Clients gilt.
