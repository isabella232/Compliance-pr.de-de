---
title: Administrative Zugriffssteuerungen in Microsoft 365
description: Dieser Artikel bietet eine Übersicht über die Administrativen Zugriffssteuerungen und die Daten kategorisierung in Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e7dc9d73b6eb1961387d85910bb558e85498ffae
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497702"
---
# <a name="administrative-access-controls-in-microsoft-365"></a><span data-ttu-id="de51c-103">Administrative Zugriffssteuerungen in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="de51c-103">Administrative access controls in Microsoft 365</span></span> 

<span data-ttu-id="de51c-104">Microsoft hat stark in Systeme und Steuerelemente investiert, die die meisten Microsoft 365-Vorgänge automatisieren und den Zugriff auf Kundeninhalte durch Microsoft bewusst einschränken.</span><span class="sxs-lookup"><span data-stu-id="de51c-104">Microsoft has invested heavily in systems and controls that automate most Microsoft 365 operations while intentionally limiting access to customer content by Microsoft.</span></span> <span data-ttu-id="de51c-105">Menschen steuern den Dienst, und Software betreibt den Dienst.</span><span class="sxs-lookup"><span data-stu-id="de51c-105">Humans govern the service, and software operates the service.</span></span> <span data-ttu-id="de51c-106">Diese Struktur ermöglicht Es Microsoft, Microsoft 365 im Großen und Umfang zu verwalten und die Risiken interner Bedrohungen für Kundeninhalte zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="de51c-106">This structure enables Microsoft to manage Microsoft 365 at scale and manage the risks of internal threats to customer content.</span></span>

<span data-ttu-id="de51c-107">Standardmäßig haben Microsoft-Techniker keine ständigen Administratorrechte und keinen ständigen Zugriff auf Kundeninhalte in Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="de51c-107">By default, Microsoft engineers have zero standing administrative privileges and zero standing access to customer content in Microsoft 365.</span></span> <span data-ttu-id="de51c-108">Ein Microsoft-Techniker kann über einen begrenzten, überwachten und gesicherten Zugriff auf die Inhalte eines Kunden für einen begrenzten Zeitraum verfügen.</span><span class="sxs-lookup"><span data-stu-id="de51c-108">A Microsoft engineer can have limited, audited, and secured access to a customer's content for a limited amount of time.</span></span> <span data-ttu-id="de51c-109">Der Zugriff ist nur bei Bedarf für Dienstvorgänge und nur bei Genehmigung durch ein Mitglied der Geschäftsleitung von Microsoft erforderlich.</span><span class="sxs-lookup"><span data-stu-id="de51c-109">Access is only when necessary for service operations and only when approved by a member of Microsoft senior management.</span></span> <span data-ttu-id="de51c-110">Für kundenlizenzierte Kunden von Lockbox stellt der Kunde die Zugriffsgenehmigung für die inhalte zur Verfügung, die in Microsoft 365 gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="de51c-110">For Customer Lockbox licensed customers, the customer provides access approval to their content hosted on Microsoft 365.</span></span>

<span data-ttu-id="de51c-111">Microsoft stellt Onlinedienste mit mehreren Formen der Cloudzustellung zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="de51c-111">Microsoft provides online services using multiple forms of cloud delivery:</span></span>

- <span data-ttu-id="de51c-112">**Öffentliche Clouds:** Enthält mehrstufige Versionen von Microsoft 365, Azure und anderen Diensten, die in Nordamerika, Südamerika, Europa, Asien, Australien usw. gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="de51c-112">**Public clouds:** Includes multi-tenant versions of Microsoft 365, Azure, and other services hosted in North America, South America, Europe, Asia, Australia, etc.</span></span>
- <span data-ttu-id="de51c-113">**Nationale Clouds:** Umfasst alle unabhängigen und von Drittanbietern betriebenen Clouds außerhalb der Vereinigten Staaten (mit Ausnahme der zuvor erwähnten), z. B. Microsoft 365 in China (betrieben von 21Vianet) und Microsoft 365 in Deutschland (betrieben von Microsoft, aber unter einem Modell, in dem ein deutscher Datentreuhänder, die Deutsche Telekom, den Zugriff von Microsoft auf Kundendaten und Systeme steuert und überwacht, die Kundendaten enthalten).</span><span class="sxs-lookup"><span data-stu-id="de51c-113">**National clouds:** Includes all sovereign and third party-operated clouds outside of the United States (except ones noted previously), such as Microsoft 365 in China (operated by 21Vianet), and Microsoft 365 in Germany (operated by Microsoft, but under a model in which a German data trustee, Deutsche Telekom, controls and monitors Microsoft's access to customer data and systems that contain customer data).</span></span>
- <span data-ttu-id="de51c-114">**Government Clouds:** Enthält Microsoft 365- und Azure-Dienste, die für Us-Government-Kunden verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="de51c-114">**Government clouds:** Includes Microsoft 365 and Azure services that are available to United States government customers.</span></span>

<span data-ttu-id="de51c-115">Für die Zwecke dieses Artikels umfassen Microsoft 365-Dienste Folgendes:</span><span class="sxs-lookup"><span data-stu-id="de51c-115">For purposes of this article, Microsoft 365 services include:</span></span>

- [<span data-ttu-id="de51c-116">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="de51c-116">Exchange Online</span></span>](/Exchange/exchange-online)
- [<span data-ttu-id="de51c-117">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="de51c-117">Exchange Online Protection</span></span>](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [<span data-ttu-id="de51c-118">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="de51c-118">SharePoint Online</span></span>](/sharepoint/sharepoint-online)
- [<span data-ttu-id="de51c-119">OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="de51c-119">OneDrive for Business</span></span>](/OneDrive/onedrive)
- [<span data-ttu-id="de51c-120">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="de51c-120">Skype for Business</span></span>](/SkypeForBusiness/skype-for-business-online)
- [<span data-ttu-id="de51c-121">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="de51c-121">Microsoft Teams</span></span>](/MicrosoftTeams/Teams-overview)
- [<span data-ttu-id="de51c-122">Yammer</span><span class="sxs-lookup"><span data-stu-id="de51c-122">Yammer</span></span>](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a><span data-ttu-id="de51c-123">Microsoft 365-Zugriffssteuerelemente</span><span class="sxs-lookup"><span data-stu-id="de51c-123">Microsoft 365 access controls</span></span>

<span data-ttu-id="de51c-124">Zu Zwecken der Zugriffssteuerung kategorisiert Microsoft Microsoft 365-Daten als Kundendaten oder andere Arten von Daten.</span><span class="sxs-lookup"><span data-stu-id="de51c-124">For access control purposes, Microsoft categorizes Microsoft 365 data as customer data or other types of data.</span></span>

### <a name="customer-data"></a><span data-ttu-id="de51c-125">Kundendaten</span><span class="sxs-lookup"><span data-stu-id="de51c-125">Customer data</span></span>

<span data-ttu-id="de51c-126">Kundendaten sind alle Daten, die von oder im Auftrag eines Kunden bei der Verwendung von Microsoft 365-Diensten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="de51c-126">Customer data is all data provided by or on behalf of a customer when using Microsoft 365 services.</span></span> <span data-ttu-id="de51c-127">Diese Daten sind Kundeninhalte, die direkt von Microsoft 365-Benutzern erstellt oder hochgeladen werden, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="de51c-127">This data is customer content directly created or uploaded by Microsoft 365 users, including:</span></span>

- <span data-ttu-id="de51c-128">E-Mails</span><span class="sxs-lookup"><span data-stu-id="de51c-128">Emails</span></span>
- <span data-ttu-id="de51c-129">SharePoint Online-Inhalte</span><span class="sxs-lookup"><span data-stu-id="de51c-129">SharePoint Online content</span></span>
- <span data-ttu-id="de51c-130">Chatnachrichten</span><span class="sxs-lookup"><span data-stu-id="de51c-130">Instant messages</span></span>
- <span data-ttu-id="de51c-131">Kalenderelemente</span><span class="sxs-lookup"><span data-stu-id="de51c-131">Calendar items</span></span>
- <span data-ttu-id="de51c-132">Dokumente</span><span class="sxs-lookup"><span data-stu-id="de51c-132">Documents</span></span>
- <span data-ttu-id="de51c-133">Kontakte</span><span class="sxs-lookup"><span data-stu-id="de51c-133">Contacts</span></span>
- <span data-ttu-id="de51c-134">Identifizierbare Endbenutzerinformationen (EUII) (Daten, die für einen Benutzer eindeutig sind oder mit einem einzelnen Benutzer verknüpfen können, aber keine Kundeninhalte enthalten)</span><span class="sxs-lookup"><span data-stu-id="de51c-134">End-user identifiable information (EUII) (data that is unique to a user or that is linkable to an individual user but does not include customer content)</span></span>

### <a name="other-types-of-data"></a><span data-ttu-id="de51c-135">Andere Datentypen</span><span class="sxs-lookup"><span data-stu-id="de51c-135">Other types of data</span></span>

<span data-ttu-id="de51c-136">Weitere Datentypen sind:</span><span class="sxs-lookup"><span data-stu-id="de51c-136">Other types of data include:</span></span>

- <span data-ttu-id="de51c-137">**Kontodaten:** Enthält administrative Daten (Informationen, die von Administratoren bei der Anmeldung oder dem Kauf von Diensten bereitgestellt werden) und Zahlungsdaten (Informationen zu Zahlungsinstrumenten, z. B. Kreditkartendetails).</span><span class="sxs-lookup"><span data-stu-id="de51c-137">**Account data:** Includes administrative data (information provided by administrators when they sign-up or purchase services), and payment data (information about payment instruments, such as credit card details).</span></span>
- <span data-ttu-id="de51c-138">**Organisatorisch identifizierbare Informationen:** Enthält Daten, die verwendet werden, um einen Mandanten zu identifizieren, Nutzungsdaten und nicht mit einem einzelnen Benutzer zu verknüpfen oder in Kundeninhalten enthalten zu sein.</span><span class="sxs-lookup"><span data-stu-id="de51c-138">**Organizationally identifiable information:** Includes data used to identify a tenant, usage data, and not linkable to an individual user or included in customer content.</span></span>
- <span data-ttu-id="de51c-139">**Systemmetadaten:** Enthält Dienstprotokolle mit Konfigurationseinstellungen, Systemstatus, Microsoft-IP-Adressen und technischen Informationen zu Abonnements und Mandanten.</span><span class="sxs-lookup"><span data-stu-id="de51c-139">**System metadata:** Includes service logs that contain configuration settings, system status, Microsoft IP addresses, and technical information about subscriptions and tenants.</span></span>

<span data-ttu-id="de51c-140">Microsoft hat Zugriffskontrollesmechanismen eingerichtet, um sicherzustellen, dass niemand nicht genehmigten Zugriff auf Kundendaten oder Zugriffssteuerungsdaten hat.</span><span class="sxs-lookup"><span data-stu-id="de51c-140">Microsoft has established access control mechanisms to ensure that no one has unapproved access to Customer Data or access control data.</span></span> <span data-ttu-id="de51c-141">Zugriffssteuerungsdaten verwalten den Zugriff auf andere Arten von Daten oder Funktionen in der Umgebung, einschließlich Zugriff auf Kundeninhalte oder EUII, Microsoft-Kennwörter, Sicherheitszertifikate und andere Authentifizierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="de51c-141">Access control data manages access to other types of data or functions within the environment, including access to customer content or EUII, Microsoft passwords, security certificates, and other authentication-related data.</span></span> <span data-ttu-id="de51c-142">Zugriffssteuerungsmechanismen schützen auch vor nicht genehmigten physischen, logischen oder Remotezugriffen auf die Microsoft 365-Produktionsumgebung.</span><span class="sxs-lookup"><span data-stu-id="de51c-142">Access control mechanisms also guard against unapproved physical, logical, or remote access to the Microsoft 365 production environment.</span></span>

<span data-ttu-id="de51c-143">Es gibt drei Kategorien von Zugriffssteuerelementen, die von Microsoft für den Betrieb von Microsoft 365 verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="de51c-143">There are three categories of access controls used by Microsoft for operating Microsoft 365:</span></span>

- <span data-ttu-id="de51c-144">Isolierungssteuerungen</span><span class="sxs-lookup"><span data-stu-id="de51c-144">Isolation controls</span></span>
- <span data-ttu-id="de51c-145">Personalsteuerungen</span><span class="sxs-lookup"><span data-stu-id="de51c-145">Personnel controls</span></span>
- <span data-ttu-id="de51c-146">Technologiesteuerungen</span><span class="sxs-lookup"><span data-stu-id="de51c-146">Technology controls</span></span>

<span data-ttu-id="de51c-147">In Kombination helfen diese Steuerelemente, böswillige Aktionen in Microsoft 365 zu verhindern und zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="de51c-147">When combined, these controls help prevent and detect malicious actions in Microsoft 365.</span></span> <span data-ttu-id="de51c-148">Zusätzlich zu den von Microsoft verwendeten Isolations-, Personal- und Technologiesteuerelementen gibt es eine vierte Kategorie von Steuerelementen: diese Steuerelemente, die von Kunden implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="de51c-148">In addition to the isolation, personnel, and technology controls used by Microsoft, there is a fourth category of controls: those controls implemented by customers.</span></span>

<span data-ttu-id="de51c-149">Mit Microsoft 365 können Sie Daten auf die gleiche Weise verwalten, wie Daten in lokalen Umgebungen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="de51c-149">Microsoft 365 allows you to manage data the same way data is managed in on-premises environments.</span></span> <span data-ttu-id="de51c-150">Die Person, die eine Organisation für Microsoft 365 einschreibt, wird automatisch globaler Administrator.</span><span class="sxs-lookup"><span data-stu-id="de51c-150">The person who signs up an organization for Microsoft 365 automatically becomes a global administrator.</span></span> <span data-ttu-id="de51c-151">Der globale Administrator hat Zugriff auf alle Features in Verwaltungsportalen und kann:</span><span class="sxs-lookup"><span data-stu-id="de51c-151">The global admin has access to all features in Management Portals and can:</span></span>

- <span data-ttu-id="de51c-152">Erstellen oder Bearbeiten von Benutzern</span><span class="sxs-lookup"><span data-stu-id="de51c-152">Create or edit users</span></span>
- <span data-ttu-id="de51c-153">Zuweisen von Administratorrollen zu anderen Personen</span><span class="sxs-lookup"><span data-stu-id="de51c-153">Assign admin roles to others</span></span>
- <span data-ttu-id="de51c-154">Zurücksetzen von Benutzerkennwörtern</span><span class="sxs-lookup"><span data-stu-id="de51c-154">Reset user passwords</span></span>
- <span data-ttu-id="de51c-155">Verwalten von Benutzerlizenzen</span><span class="sxs-lookup"><span data-stu-id="de51c-155">Manage user licenses</span></span>
- <span data-ttu-id="de51c-156">Verwalten von Domänen</span><span class="sxs-lookup"><span data-stu-id="de51c-156">Manage domains</span></span>
- <span data-ttu-id="de51c-157">Genehmigen von Kunden-Lockbox-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de51c-157">Approve Customer Lockbox requests</span></span>

<span data-ttu-id="de51c-158">Es wird empfohlen, dass jede Organisation mindestens zwei Administratorkonten konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="de51c-158">We recommend that each organization configure at least two admin accounts.</span></span> <span data-ttu-id="de51c-159">Für große Unternehmensorganisationen empfehlen wir spezielle Administratorkonten, die unterschiedliche Funktionen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="de51c-159">For large enterprise organizations, we recommend specialized admin accounts that serve different functions.</span></span>

<span data-ttu-id="de51c-160">Informationen zum Zuweisen von Administratorrollen und -berechtigungen finden Sie unter Zuweisen von [Administratorrollen](/microsoft-365/admin/add-users/assign-admin-roles) und [Informationen zu Administratorrollen](/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="de51c-160">For information about assigning admin roles and permissions, see [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles) and [About admin roles](/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-links"></a><span data-ttu-id="de51c-161">Links zu verwandten Themen</span><span class="sxs-lookup"><span data-stu-id="de51c-161">Related Links</span></span>

- [<span data-ttu-id="de51c-162">Isolation in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="de51c-162">Isolation in Microsoft 365</span></span>](assurance-isolation-in-microsoft-365.md)
- [<span data-ttu-id="de51c-163">Überprüfung vor der Einstellung durch Microsoft</span><span class="sxs-lookup"><span data-stu-id="de51c-163">Microsoft pre-employment screening</span></span>](assurance-pre-employment-screening.md)
- [<span data-ttu-id="de51c-164">Microsoft Cloud-Hintergrundprüfung</span><span class="sxs-lookup"><span data-stu-id="de51c-164">Microsoft cloud background check</span></span>](assurance-cloud-background-check.md)
- [<span data-ttu-id="de51c-165">Überwachung und Überprüfung von Zugriffssteuerungen</span><span class="sxs-lookup"><span data-stu-id="de51c-165">Monitoring and Auditing Access Controls</span></span>](assurance-monitoring-and-auditing-access-controls.md)
- [<span data-ttu-id="de51c-166">Yammer Enterprise-Zugriffssteuerungen</span><span class="sxs-lookup"><span data-stu-id="de51c-166">Yammer Enterprise Access Controls</span></span>](assurance-yammer-enterprise-access-controls.md)
