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
# <a name="service-resource-limits"></a><span data-ttu-id="49dcc-103">Dienstressourcenbeschränkungen</span><span class="sxs-lookup"><span data-stu-id="49dcc-103">Service resource limits</span></span>

<span data-ttu-id="49dcc-104">Ressourcenbeschränkungen werden mithilfe von Kontingenten (Grenzwerten) und Drosselung erzwungen.</span><span class="sxs-lookup"><span data-stu-id="49dcc-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="49dcc-105">Azure Active Directory (Azure AD) und die einzelnen Microsoft 365-Dienste verwenden beide.</span><span class="sxs-lookup"><span data-stu-id="49dcc-105">Azure Active Directory (Azure AD) and the individual Microsoft 365 services use both.</span></span> <span data-ttu-id="49dcc-106">Die Grenzwerte sind dienstspezifisch und ändern sich im Laufe der Zeit, wenn neue Funktionen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="49dcc-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="49dcc-107">Weitere Informationen zu den aktuellen Grenzwerten für die verschiedenen Dienste finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="49dcc-107">For details on the current limits for the various services, see the following topics:</span></span>

- [<span data-ttu-id="49dcc-108">Azure AD -Dienstbeschränkungen und -einschränkungen</span><span class="sxs-lookup"><span data-stu-id="49dcc-108">Azure AD service limits and restrictions</span></span>](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [<span data-ttu-id="49dcc-109">Exchange Online-Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="49dcc-109">Exchange Online Limits</span></span>](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [<span data-ttu-id="49dcc-110">SharePoint Online Softwarebeschränkungen und -grenzen</span><span class="sxs-lookup"><span data-stu-id="49dcc-110">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="49dcc-111">Grenzwerte für Skype for Business</span><span class="sxs-lookup"><span data-stu-id="49dcc-111">Skype for Business Limits</span></span>](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="49dcc-112">Yammer REST-API und -Grenzwerte</span><span class="sxs-lookup"><span data-stu-id="49dcc-112">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="49dcc-113">Dateigrößenbeschränkungen in Sway</span><span class="sxs-lookup"><span data-stu-id="49dcc-113">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="49dcc-114">Zusätzlich zu diesen Grenzwerten werden mehrere Drosselungsmechanismen in Azure AD und Microsoft 365 verwendet.</span><span class="sxs-lookup"><span data-stu-id="49dcc-114">In addition to these limits, several throttling mechanisms are used throughout Azure AD and Microsoft 365.</span></span> <span data-ttu-id="49dcc-115">Die Einschränkung innerhalb des Diensts ist besonders wichtig, da die Netzwerkressourcen in den Rechenzentren von Microsoft für die breite Palette von Kunden optimiert sind, die die Dienste nutzen.</span><span class="sxs-lookup"><span data-stu-id="49dcc-115">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="49dcc-116">Zu den Drosselungsmechanismen gehören:</span><span class="sxs-lookup"><span data-stu-id="49dcc-116">Throttling mechanisms include:</span></span>

- <span data-ttu-id="49dcc-117">Azure AD und Microsoft 365 bieten Drosselung auf Benutzerebene, die die Anzahl von Transaktionen oder gleichzeitigen Aufrufen (durch Skript oder Code) eingrenzt, die von einem einzelnen Benutzer ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="49dcc-117">Azure AD and Microsoft 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="49dcc-118">Jedem Mandanten wird bei der Mandantenerstellung eine standardmäßige PowerShell-Einschränkungsrichtlinie zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="49dcc-118">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="49dcc-119">Diese Einstellungen wirken sich auf andere Elemente aus, z. B. die maximale Anzahl gleichzeitiger PowerShell-Sitzungen, die von einem einzelnen Administrator geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="49dcc-119">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="49dcc-120">Jeder Exchange Online-Kunde verfügt über eine standardmäßige Exchange Web Services (EWS)-Richtlinie, die auf die Vorgänge des EWS-Clients abgestimmt ist, und Drosselung, die für alle Outlook-Clients gilt.</span><span class="sxs-lookup"><span data-stu-id="49dcc-120">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
