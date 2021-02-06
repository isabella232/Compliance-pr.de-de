---
title: Microsoft 365- und Überwachungszugriffssteuerungen
description: 'Zusammenfassung: Eine Zusammenfassung der verschiedenen Überwachungs- und Überwachungszugriffskontrollen, die in Microsoft 365 verfügbar sind.'
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
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 3021ce1dd59d5d071edec22286ae9c63833f1277
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120444"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a><span data-ttu-id="7ca5e-103">Überwachen und Überwachen von Zugriffssteuerungen in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7ca5e-103">Monitoring and auditing access controls in Microsoft 365</span></span>

<span data-ttu-id="7ca5e-104">Microsoft führt eine umfassende Überwachung aller Delegierung, Berechtigungen und Vorgänge aus, die in Microsoft 365 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7ca5e-104">Microsoft performs extensive monitoring and auditing of all delegation, privileges, and operations that occur within Microsoft 365.</span></span> <span data-ttu-id="7ca5e-105">Die Microsoft 365-Zugriffssteuerung ist ein automatisierter Prozess, der auf dem Prinzip der geringsten Rechte und der Integration von Datenzugriffssteuerungen und -überwachungen aufgebaut ist:</span><span class="sxs-lookup"><span data-stu-id="7ca5e-105">Microsoft 365 access control is an automated process built on the principle of least privilege and incorporating data access controls and audits:</span></span>

- <span data-ttu-id="7ca5e-106">Der zulässige Zugriff kann auf einen eindeutigen Benutzer nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="7ca5e-106">All permitted access is traceable to a unique user.</span></span> <span data-ttu-id="7ca5e-107">Administratoren sind für die Verarbeitung von Kundeninhalten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="7ca5e-107">Administrators are accountable for their handling of customer content.</span></span>
- <span data-ttu-id="7ca5e-108">Zugriffssteuerungsanforderungen, Genehmigungen und Verwaltungsprotokolle werden zur Analyse von Sicherheits- und Böswilligen Ereignissen erfasst.</span><span class="sxs-lookup"><span data-stu-id="7ca5e-108">Access control requests, approvals, and administrative operations logs are captured for analysis of security and malicious events.</span></span>
- <span data-ttu-id="7ca5e-109">Zugriffsebenen werden nahezu in Echtzeit basierend auf der Mitgliedschaft in Sicherheitsgruppen überprüft, um sicherzustellen, dass nur Benutzer, die berechtigte geschäftliche Begründungen haben und die Berechtigungsanforderungen erfüllen, Zugriff auf die Systeme haben.</span><span class="sxs-lookup"><span data-stu-id="7ca5e-109">Access levels are reviewed in near real-time based on security group membership to ensure that only users who have authorized business justifications and meet the eligibility requirements have access to the systems.</span></span>
- <span data-ttu-id="7ca5e-110">Microsoft 365, seine Zugriffssteuerungen und unterstützenden Dienste, einschließlich Azure Active Directory und physischen Rechenzentren, werden regelmäßig von unabhängigen Drittanbietern auf Einhaltung von [ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)und anderen Standards [überprüft.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)</span><span class="sxs-lookup"><span data-stu-id="7ca5e-110">Microsoft 365, its access controls, and supporting services, including Azure Active Directory and physical datacenters, are regularly audited by independent third-parties for compliance with [ISO/IEC 27001](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/TrustCenter/Compliance/SOC), [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP), and other [standards](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons).</span></span>
- <span data-ttu-id="7ca5e-111">Microsoft 365-Techniker müssen jährlich Sicherheitsschulungen machen, die bewährten Verfahren für den erweiterten Zugriff überprüfen und die Sicherheits- und Datenschutzrichtlinien von Microsoft zur Aufrechterhaltung von Berechtigungen für den Dienst bestätigen.</span><span class="sxs-lookup"><span data-stu-id="7ca5e-111">Microsoft 365 engineers must take yearly security training, review elevated access best procedures, and acknowledge Microsoft's security and privacy policies to maintain entitlements to the service.</span></span>

<span data-ttu-id="7ca5e-112">Automatisierte Warnungen werden ausgelöst, wenn verdächtige Aktivitäten erkannt werden, z. B. mehrere fehlgeschlagene Anmeldungen innerhalb eines kurzen Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="7ca5e-112">Automated alerts trigger when suspicious activity is detected, such as multiple failed logins within a short period.</span></span> <span data-ttu-id="7ca5e-113">Das Microsoft 365 Security Response-Team verwendet maschinelles Lernen und Big Data-Analysen, um Aktivitäten zu überprüfen und zu analysieren, nach unregelmäßigen Zugriffsmustern zu suchen und proaktiv auf anomale und unrechtmäßige Aktivitäten zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="7ca5e-113">The Microsoft 365 Security Response team uses machine learning and big data analysis to review and analyze activity, look for irregular access patterns, and proactively respond to anomalous and illicit activities.</span></span> <span data-ttu-id="7ca5e-114">Microsoft setzt außerdem ein dediziertes Team von Penetrationstestern ein und verwendet regelmäßige Übungen des roten Teams und des blauen Teams, um Sicherheits- und Zugriffssteuerungsprobleme im Dienst zu finden.</span><span class="sxs-lookup"><span data-stu-id="7ca5e-114">Microsoft also employs a dedicated team of penetration testers and engages in periodic Red Team and Blue Team exercises to find security and access control issues in the service.</span></span> <span data-ttu-id="7ca5e-115">Kunden können die Effektivität von Zugriffskontrollsystemen mithilfe von Überwachungsberichten und der von Microsoft 365 bereitgestellten Verwaltungsaktivitäts-API überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7ca5e-115">Customers can verify the effectiveness of access control systems by using audit reports and the management activity API provided by Microsoft 365.</span></span>

<span data-ttu-id="7ca5e-116">Weitere Informationen finden Sie unter [Office 365 Management Activity API reference](/office/office-365-management-api/office-365-management-activity-api-reference) and Auditing and reporting in Microsoft [365](assurance-auditing-and-reporting-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7ca5e-116">For more information, see [Office 365 Management Activity API reference](/office/office-365-management-api/office-365-management-activity-api-reference) and [Auditing and reporting in Microsoft 365](assurance-auditing-and-reporting-overview.md).</span></span>
