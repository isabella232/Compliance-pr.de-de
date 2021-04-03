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
# <a name="service-resource-limits"></a><span data-ttu-id="32627-103">Dienstressourcenbeschränkungen</span><span class="sxs-lookup"><span data-stu-id="32627-103">Service resource limits</span></span>

<span data-ttu-id="32627-104">Ressourcenbeschränkungen werden mithilfe von Kontingenten (Grenzwerten) und Drosselung erzwungen.</span><span class="sxs-lookup"><span data-stu-id="32627-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="32627-105">Azure Active Directory (Azure AD) und die einzelnen Microsoft 365-Dienste verwenden beide Dienste.</span><span class="sxs-lookup"><span data-stu-id="32627-105">Azure Active Directory (Azure AD) and the individual Microsoft 365 services use both.</span></span> <span data-ttu-id="32627-106">Grenzwerte sind dienstspezifisch und ändern sich im Laufe der Zeit, wenn neue Funktionen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="32627-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="32627-107">Weitere Informationen zu den aktuellen Grenzwerten für die verschiedenen Dienste finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="32627-107">For details on the current limits for the various services, see the following topics:</span></span>

- [<span data-ttu-id="32627-108">Azure AD-Dienstbeschränkungen und -einschränkungen</span><span class="sxs-lookup"><span data-stu-id="32627-108">Azure AD service limits and restrictions</span></span>](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [<span data-ttu-id="32627-109">Exchange Online-Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="32627-109">Exchange Online Limits</span></span>](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [<span data-ttu-id="32627-110">Grenzen und Grenzen der SharePoint Online-Software</span><span class="sxs-lookup"><span data-stu-id="32627-110">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="32627-111">Skype for Business-Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="32627-111">Skype for Business Limits</span></span>](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="32627-112">Yammer REST-API und Geschwindigkeitsbeschränkungen</span><span class="sxs-lookup"><span data-stu-id="32627-112">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="32627-113">Dateigrößenbeschränkungen in Sway</span><span class="sxs-lookup"><span data-stu-id="32627-113">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="32627-114">Zusätzlich zu diesen Grenzwerten werden verschiedene Drosselungsmechanismen in Azure AD und Microsoft 365 verwendet.</span><span class="sxs-lookup"><span data-stu-id="32627-114">In addition to these limits, several throttling mechanisms are used throughout Azure AD and Microsoft 365.</span></span> <span data-ttu-id="32627-115">Die Einschränkung innerhalb des Diensts ist besonders wichtig, da Die Netzwerkressourcen in den Rechenzentren von Microsoft für die breite Palette von Kunden optimiert sind, die die Dienste verwenden.</span><span class="sxs-lookup"><span data-stu-id="32627-115">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="32627-116">Zu den Drosselungsmechanismen gehören:</span><span class="sxs-lookup"><span data-stu-id="32627-116">Throttling mechanisms include:</span></span>

- <span data-ttu-id="32627-117">Azure AD und Microsoft 365 bieten Eine Einschränkung auf Benutzerebene, die die Anzahl von Transaktionen oder gleichzeitigen Anrufen (durch Skript oder Code) eingrenzt, die von einem einzelnen Benutzer ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="32627-117">Azure AD and Microsoft 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="32627-118">Jedem Mandanten wird bei der Mandantenerstellung eine standardmäßige PowerShell-Einschränkungsrichtlinie zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="32627-118">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="32627-119">Diese Einstellungen wirken sich auf andere Elemente aus, z. B. die maximale Anzahl gleichzeitiger PowerShell-Sitzungen, die von einem einzelnen Administrator geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="32627-119">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="32627-120">Jeder Exchange Online-Kunde verfügt über eine Standardmäßige Exchange Web Services (EWS)-Richtlinie, die auf EWS-Clientvorgänge abgestimmt ist, und Drosselung, die für alle Outlook-Clients gilt.</span><span class="sxs-lookup"><span data-stu-id="32627-120">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
