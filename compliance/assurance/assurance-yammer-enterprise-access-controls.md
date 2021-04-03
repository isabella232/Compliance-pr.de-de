---
title: Microsoft 365 Yammer Unternehmenszugriffssteuerelemente
description: Dieser Artikel enthält eine kurze Zusammenfassung über Yammer Enterprise Access Controls in der Produktionsumgebung.
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
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497353"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="efdfb-103">Yammer Unternehmenszugriffssteuerelemente</span><span class="sxs-lookup"><span data-stu-id="efdfb-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="efdfb-104">Der physische und logische Zugriff auf Yammer Produktionsumgebung ist auf eine kleine Gruppe von Personen (Infrastruktur und Betrieb) beschränkt.</span><span class="sxs-lookup"><span data-stu-id="efdfb-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="efdfb-105">Wie bei anderen Microsoft 365-Technikern haben Yammer techniker keinen ständigen Zugriff auf Kundendaten.</span><span class="sxs-lookup"><span data-stu-id="efdfb-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="efdfb-106">Der Zugriff muss über ein genehmigungsbasiertes Just-in-Time-Zugriffssteuerungssystem angefordert werden, das lockbox mit einer begrenzten Anzahl von Genehmigende ähnelt.</span><span class="sxs-lookup"><span data-stu-id="efdfb-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="efdfb-107">Genehmiger überprüfen die Anforderung (sie überprüfen beispielsweise, ob die Anforderung aufgrund von Bedarf, Geschäftsfall, Uhrzeit usw.) legitim ist, und genehmigen oder verweigern die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="efdfb-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="efdfb-108">Wenn die Anforderung genehmigt wird, wird der JIT-Zugriff für einen definierten und begrenzten Zeitraum gewährt.</span><span class="sxs-lookup"><span data-stu-id="efdfb-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="efdfb-109">Nachdem die Zugriffszeit überschritten wurde, läuft der Zugriff automatisch ab.</span><span class="sxs-lookup"><span data-stu-id="efdfb-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="efdfb-110">Wie bei anderen Microsoft 365-Diensten wird bei allen Zugriffen Yammer Produktionsumgebung die mehrstufige Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="efdfb-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="efdfb-111">Der zugriffs- und befehlsverlauf wird einem Benutzer zugeordnet und vom Sicherheitsteam Yammer protokolliert und überprüft.</span><span class="sxs-lookup"><span data-stu-id="efdfb-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="efdfb-112">Weitere Informationen zu Yammer Verwaltung finden Sie unter [Yammer Admin Help](/yammer/yammer-landing-page).</span><span class="sxs-lookup"><span data-stu-id="efdfb-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>