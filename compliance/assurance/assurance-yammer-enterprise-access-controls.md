---
title: Microsoft 365 Yammer Zugriffssteuerungen für Unternehmen
description: Dieser Artikel enthält eine kurze Zusammenfassung Yammer Enterprise Access Controls in der Produktionsumgebung.
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
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120364"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="06961-103">Yammer von Unternehmenszugriffssteuerungen</span><span class="sxs-lookup"><span data-stu-id="06961-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="06961-104">Der physische und logische Zugriff auf die Yammer ist auf eine kleine Gruppe von Personen (Infrastruktur und Vorgänge) beschränkt.</span><span class="sxs-lookup"><span data-stu-id="06961-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="06961-105">Wie andere Microsoft 365-Techniker haben Yammer keinen ständigen Zugriff auf Kundendaten.</span><span class="sxs-lookup"><span data-stu-id="06961-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="06961-106">Der Zugriff muss über ein genehmigungsbasiertes Just-in-Time-Zugriffssteuerungssystem angefordert werden, das lockbox mit einer begrenzten Anzahl von Genehmigende ähnelt.</span><span class="sxs-lookup"><span data-stu-id="06961-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="06961-107">Genehmiger überprüfen die Anforderung (sie überprüfen beispielsweise, ob die Anforderung aufgrund von Bedarf, Geschäftsfall, Zeit usw. legitim ist), und genehmigen oder verweigern die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="06961-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="06961-108">Wenn die Anforderung genehmigt wird, wird der Zugriff auf jit für einen definierten und begrenzten Zeitraum gewährt.</span><span class="sxs-lookup"><span data-stu-id="06961-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="06961-109">Nach Überschreitung der Zugriffszeit läuft der Zugriff automatisch ab.</span><span class="sxs-lookup"><span data-stu-id="06961-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="06961-110">Wie bei anderen Microsoft 365-Diensten wird für den Yammer die mehrstufige Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="06961-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="06961-111">Der Zugriffs- und Befehlsverlauf wird einem Benutzer zugeordnet und vom Sicherheitsteam Yammer protokolliert und überprüft.</span><span class="sxs-lookup"><span data-stu-id="06961-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="06961-112">Weitere Informationen zur Verwaltung Yammer Verwaltung finden Sie in Yammer [Administratorhilfe.](/yammer/yammer-landing-page)</span><span class="sxs-lookup"><span data-stu-id="06961-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>