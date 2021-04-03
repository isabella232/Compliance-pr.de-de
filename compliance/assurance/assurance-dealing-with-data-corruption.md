---
title: Microsoft 365 Umgang mit Datenbeschädigung
description: In diesem Artikel werden die Datenbeschädigung in Microsoft 365 und die Von Microsoft unternommenen Anstrengungen zur Verhinderung und Wiederherstellung von Daten erläutert.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497596"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a><span data-ttu-id="9e39b-103">Umgang mit Datenbeschädigung in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9e39b-103">Dealing with data corruption in Microsoft 365</span></span>

<span data-ttu-id="9e39b-104">Einer der anspruchsvollen Aspekte bei der Ausführung eines großen Clouddiensts ist die Verarbeitung von Datenbeschädigungen angesichts der großen Datenmenge und unabhängiger Systeme.</span><span class="sxs-lookup"><span data-stu-id="9e39b-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="9e39b-105">Datenbeschädigungen können durch:</span><span class="sxs-lookup"><span data-stu-id="9e39b-105">Data corruption can be caused by:</span></span>

- <span data-ttu-id="9e39b-106">Anwendungs- oder Infrastrukturfehler, die den Anwendungsstatus teilweise oder ganz beschädigen</span><span class="sxs-lookup"><span data-stu-id="9e39b-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span>
- <span data-ttu-id="9e39b-107">Hardwareprobleme, die zu datenverlusten oder zu Unfähigkeit zum Lesen von Daten führen</span><span class="sxs-lookup"><span data-stu-id="9e39b-107">Hardware issues that result in lost data or an inability to read data</span></span>
- <span data-ttu-id="9e39b-108">Menschliche Betriebsfehler</span><span class="sxs-lookup"><span data-stu-id="9e39b-108">Human operational errors</span></span>
- <span data-ttu-id="9e39b-109">Böswillige Hacker und verärgerte Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="9e39b-109">Malicious hackers and disgruntled employees</span></span>
- <span data-ttu-id="9e39b-110">Vorfälle in externen Diensten, die zu datenverlusten führen</span><span class="sxs-lookup"><span data-stu-id="9e39b-110">Incidents in external services that result in some loss of data</span></span>

<span data-ttu-id="9e39b-111">Da eine höhere Ausfallsicherheit bei der Datenintegrität weniger Datenbeschädigungsvorfälle bedeutet, hat Microsoft in Microsoft 365-Schutzmechanismen integrierte, um zu verhindern, dass Beschädigungen entstehen, sowie Systeme und Prozesse, mit denen wir daten wiederherstellen können, falls dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="9e39b-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Microsoft 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="9e39b-112">Prüfungen und Prozesse sind in den verschiedenen Phasen des Technischen Veröffentlichungsprozesses vorhanden, um die Ausfallsicherheit gegen Datenbeschädigungen zu erhöhen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="9e39b-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>

- <span data-ttu-id="9e39b-113">Systemdesign</span><span class="sxs-lookup"><span data-stu-id="9e39b-113">System Design</span></span>
- <span data-ttu-id="9e39b-114">Codeorganisation und -struktur</span><span class="sxs-lookup"><span data-stu-id="9e39b-114">Code organization and structure</span></span>
- <span data-ttu-id="9e39b-115">Codeüberprüfung</span><span class="sxs-lookup"><span data-stu-id="9e39b-115">Code review</span></span>
- <span data-ttu-id="9e39b-116">Komponententests, Integrationstests und Systemtests</span><span class="sxs-lookup"><span data-stu-id="9e39b-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="9e39b-117">Trip-Leitungen-Tests/-Gates</span><span class="sxs-lookup"><span data-stu-id="9e39b-117">Trip wires tests/gates</span></span>

<span data-ttu-id="9e39b-118">In Microsoft 365-Produktionsumgebungen stellt die Peerreplikation zwischen Rechenzentren sicher, dass immer mehrere Livekopien aller Daten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9e39b-118">Within Microsoft 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="9e39b-119">Standardbilder und Skripts werden verwendet, um verlorene Server wiederherzustellen, und replizierte Daten werden zum Wiederherstellen von Kundendaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e39b-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="9e39b-120">Aufgrund der integrierten Überprüfungen und Prozesse der Datenresilienz verwaltet Microsoft nur Sicherungen der Dokumentation des Microsoft 365-Informationssystems (einschließlich sicherheitsbezogener Dokumentation) mithilfe der integrierten Replikation in SharePoint Online und unseres internen Coderepositorytools Source Depot.</span><span class="sxs-lookup"><span data-stu-id="9e39b-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Microsoft 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="9e39b-121">Die Systemdokumentation wird in SharePoint Online gespeichert, und Source Depot enthält System- und Anwendungsabbilder.</span><span class="sxs-lookup"><span data-stu-id="9e39b-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="9e39b-122">Sowohl SharePoint Online als auch Source Depot verwenden die Versionsverwaltung und werden nahezu in Echtzeit repliziert.</span><span class="sxs-lookup"><span data-stu-id="9e39b-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real time.</span></span>
