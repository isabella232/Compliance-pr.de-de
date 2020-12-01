---
title: Microsoft 365 jammern von Unternehmens Zugriffs Steuerelementen
description: Dieser Artikel enthält eine kurze Zusammenfassung über das Jammern von Enterprise-Zugriffs Steuerelementen in der Produktionsumgebung.
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
ms.openlocfilehash: d44bead3627ed9b99c93bcffc9f29f87731f7407
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506950"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="1d306-103">Jammern von Enterprise-Zugriffs Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="1d306-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="1d306-104">Der physische und logische Zugriff auf die Produktionsumgebung jammern ist auf eine kleine Gruppe von Personen (Infrastruktur und Betrieb) beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1d306-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="1d306-105">Wie bei anderen Microsoft 365-Ingenieuren haben Jammer Techniker keine ständigen Zugriff auf Kundendaten.</span><span class="sxs-lookup"><span data-stu-id="1d306-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="1d306-106">Der Zugriff muss mithilfe eines Genehmigungs basierten Just-in-Time-Zugriffs Steuerungssystems angefordert werden, ähnlich wie Lockbox mit einer begrenzten Anzahl von genehmigenden Personen.</span><span class="sxs-lookup"><span data-stu-id="1d306-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="1d306-107">Genehmigende Personen überprüfen die Anforderung (beispielsweise überprüfen, ob die Anforderung aufgrund von Bedarf, Geschäftsfall, Zeit usw. legitim ist), und genehmigen oder verweigern die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1d306-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="1d306-108">Wenn die Anforderung genehmigt wird, wird der JIT-Zugriff für eine definierte und beschränkte Zeit gewährt.</span><span class="sxs-lookup"><span data-stu-id="1d306-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="1d306-109">Nach Überschreiten der Zugriffszeit läuft der Zugriff automatisch ab.</span><span class="sxs-lookup"><span data-stu-id="1d306-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="1d306-110">Wie bei anderen Microsoft 365-Diensten verwendet jeder Zugriff auf die Produktionsumgebung von jammern mehrstufige Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="1d306-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="1d306-111">Der gesamte Zugriffs-und Befehlsverlauf wird einem Benutzer zugeschrieben und regelmäßig vom Sicherheitsteam "jammern" protokolliert und überprüft.</span><span class="sxs-lookup"><span data-stu-id="1d306-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="1d306-112">Weitere Informationen zur Verwaltung und Verwaltung von jammern finden Sie unter [jammern der Administratorhilfe](https://docs.microsoft.com/yammer/yammer-landing-page).</span><span class="sxs-lookup"><span data-stu-id="1d306-112">For more information about Yammer administration and management, see [Yammer admin help](https://docs.microsoft.com/yammer/yammer-landing-page).</span></span>