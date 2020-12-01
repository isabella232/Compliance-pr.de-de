---
title: Grundlegendes zur Enterprise Business Continuity-Verwaltung mit Clouddiensten
description: Hier erfahren Sie, wie sich die Planung und Implementierung von Geschäftskontinuität ändert, wenn Clouddienste Bestandteil Ihres IT-Angebots sind.
author: chrfox
ms.author: chrfox
manager: laurawi
ms.reviewer: sosstah
ms.date: ''
audience: ITPro
ms.topic: article
f1.keywords:
- NOCSH
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- remotework
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: f92a1d79c435059918113dbeacdc3536d10933d6
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506678"
---
# <a name="enterprise-business-continuity-management-ebcm-with-cloud-services"></a><span data-ttu-id="9d7b9-103">Enterprise Business Continuity-Verwaltung (EBCM) mit Clouddiensten</span><span class="sxs-lookup"><span data-stu-id="9d7b9-103">Enterprise business continuity management (EBCM) with cloud services</span></span>

<span data-ttu-id="9d7b9-104">Als Bestandteil der digitalen Transformation Ihrer Organisation müssen Sie Ihre Notfallwiederherstellungs- und Geschäftskontinuitätspläne überprüfen und aktualisieren, um die Geschäftsprozesse zu berücksichtigen, die von Microsoft 365-Clouddiensten abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="9d7b9-104">As part of your organizations digital transformation, you need to revisit and update your disaster recovery and business continuity plans to account for the business process that depend on Microsoft 365 Cloud services.</span></span> <span data-ttu-id="9d7b9-105">Konzeption und Betrieb von Microsoft 365-Clouddiensten wie Exchange Online, SharePoint Online und OneDrive for Business sind auf hohe Ausfallsicherheit ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="9d7b9-105">Microsoft 365 Cloud services, like Exchange Online, SharePoint Online and OneDrive for Business are designed and operated to be highly resilient.</span></span>

> [!NOTE]
> <span data-ttu-id="9d7b9-106">Weitere Informationen zum eigenen EBCM-Plan finden Sie im [Whitepaper zum Enterprise Business Continuity Management-Programm](https://go.microsoft.com/fwlink/?linkid=2121521) von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9d7b9-106">You can learn more about Microsoft's own EBCM plan in the [Enterprise Business Continuity Management Program whitepaper](https://go.microsoft.com/fwlink/?linkid=2121521).</span></span> <span data-ttu-id="9d7b9-107">Anmeldung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d7b9-107">Login is required.</span></span>

<span data-ttu-id="9d7b9-108">Aber selbst bei hoher Ausfallsicherheit können Dienstincidents auftreten.</span><span class="sxs-lookup"><span data-stu-id="9d7b9-108">Even with this resilience, service incidents do occur.</span></span> <span data-ttu-id="9d7b9-109">In diesen Fällen sollte Ihre Organisation vorbereitet sein und über eine definierte Geschäftskontinuitätsstrategie verfügen.</span><span class="sxs-lookup"><span data-stu-id="9d7b9-109">When they do, your organization should be prepared and have a well-defined business continuity strategy.</span></span>

<span data-ttu-id="9d7b9-110">Wenn Sie Ihre Pläne noch nicht aktualisiert haben, hilft Ihnen diese Themenreihe bei der Planung Ihrer Strategie, damit ihre Dienste bei einen Fehler mit einem bekannten Status wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="9d7b9-110">If you haven't updated your plans yet this series of topics helps you to plan your strategy so your services can fail to a known state.</span></span> <span data-ttu-id="9d7b9-111">In diesen Themen werden die Hauptüberlegungen zur Verbesserung der Kontinuitätsbereitschaft behandelt.</span><span class="sxs-lookup"><span data-stu-id="9d7b9-111">These topics highlight key considerations for improving your continuity readiness.</span></span>

## <a name="list-of-topics-with-links"></a><span data-ttu-id="9d7b9-112">Liste der Themen mit Links</span><span class="sxs-lookup"><span data-stu-id="9d7b9-112">List of topics with links</span></span>

- [<span data-ttu-id="9d7b9-113">Verantwortlichkeit von Kunden und Cloudpartnern</span><span class="sxs-lookup"><span data-stu-id="9d7b9-113">Customer and cloud partner responsibilities</span></span>](assurance-customer-and-cloud-partner-ebcm-responsibilities.md)
- [<span data-ttu-id="9d7b9-114">Microsoft 365-Dienstausfallsicherheit</span><span class="sxs-lookup"><span data-stu-id="9d7b9-114">Microsoft 365 service resiliency</span></span>](assurance-m365-service-resiliency.md)
- [<span data-ttu-id="9d7b9-115">Entwickeln Ihres Kontinuitätsplans</span><span class="sxs-lookup"><span data-stu-id="9d7b9-115">Developing your continuity plan</span></span>](assurance-developing-your-ebcm-plan.md)
- [<span data-ttu-id="9d7b9-116">Schadensbegrenzungsszenarien für Microsoft 365-Dienstincidents</span><span class="sxs-lookup"><span data-stu-id="9d7b9-116">Microsoft 365 service incident mitigation scenarios</span></span>](assurance-microsoft-365-mitigations.md)
- [<span data-ttu-id="9d7b9-117">Microsoft 365 für Geschäftskontinuitätsplanung – Schulung und Probelauf</span><span class="sxs-lookup"><span data-stu-id="9d7b9-117">Microsoft 365 for business continuity plan training and rehearsal</span></span>](assurance-ebcm-plan-rehearsal-and-user-training.md)

## <a name="see-also"></a><span data-ttu-id="9d7b9-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d7b9-118">See also</span></span>

- [<span data-ttu-id="9d7b9-119">Enterprise-Geschäftskontinuität – Haftungsausschluss</span><span class="sxs-lookup"><span data-stu-id="9d7b9-119">Enterprise business continuity legal disclaimer</span></span>](assurance-ebcm-legal-disclaimer.md)
