---
title: Microsoft 365 interne Protokollierung für Microsoft 365 Engineering
description: In diesem Artikel finden Sie eine Erläuterung der Funktionsweise der internen Protokollierung für Microsoft 365 Engineering-Teams.
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
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088594"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a><span data-ttu-id="2e046-103">Interne Protokollierung für Microsoft 365-Engineering</span><span class="sxs-lookup"><span data-stu-id="2e046-103">Internal logging for Microsoft 365 engineering</span></span>

<span data-ttu-id="2e046-104">Zusätzlich zu den für Kunden verfügbaren Ereignissen und Protokolldaten unterhält Microsoft ein internes System zur Erfassung von Protokolldaten, das Microsoft 365 Technikern zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="2e046-104">In addition to the events and log data available for customers, Microsoft maintains an internal log data collection system that is available to Microsoft 365 engineers.</span></span> <span data-ttu-id="2e046-105">Viele verschiedene Arten von Protokolldaten werden von Microsoft 365 Servern in eine proprietäre Lösung für die Sicherheitsüberwachung für die Analyse nahezu in Echtzeit (NRT) und einen internen Big Data Computing-Dienst (Cosmos) für die langfristige Speicherung hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="2e046-105">Many different types of log data are uploaded from Microsoft 365 servers to a proprietary security monitoring solution for near real-time (NRT) analysis and an internal, big data computing service (Cosmos) for long-term storage.</span></span> <span data-ttu-id="2e046-106">Diese Datenübertragung erfolgt über eine FIPS 140-2-validierte TLS-Verbindung an genehmigten Ports und Protokollen mithilfe eines proprietären Automatisierungstools namens Office Data Loader (ODL).</span><span class="sxs-lookup"><span data-stu-id="2e046-106">This data transfer occurs over a FIPS 140-2-validated TLS connection on approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL).</span></span> <span data-ttu-id="2e046-107">Die in Microsoft 365 zum Sammeln und Verarbeiten von Überwachungsdatensätzen verwendeten Tools ermöglichen keine dauerhaften oder nicht rückgängig gemachten Änderungen am ursprünglichen Inhalt des Überwachungsdatensatzes oder an der Zeitreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="2e046-107">The tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.</span></span>

<span data-ttu-id="2e046-108">Serviceteams verwenden Cosmos als zentrales Repository, um eine Analyse der Anwendungsnutzung durchzuführen, die System- und Betriebsleistung zu messen und nach Anomalien und Mustern zu suchen, die auf Probleme oder Sicherheitsprobleme hinweisen können.</span><span class="sxs-lookup"><span data-stu-id="2e046-108">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues.</span></span> <span data-ttu-id="2e046-109">Jedes Serviceteam lädt einen Basisplan hoch, der Folgendes umfasst:</span><span class="sxs-lookup"><span data-stu-id="2e046-109">Each service team uploads a baseline that includes:</span></span>

- <span data-ttu-id="2e046-110">Ereignisprotokolle</span><span class="sxs-lookup"><span data-stu-id="2e046-110">Event logs</span></span>
- <span data-ttu-id="2e046-111">AppLocker-Protokolle</span><span class="sxs-lookup"><span data-stu-id="2e046-111">AppLocker logs</span></span>
- <span data-ttu-id="2e046-112">Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="2e046-112">Performance data</span></span>
- <span data-ttu-id="2e046-113">System Center Daten</span><span class="sxs-lookup"><span data-stu-id="2e046-113">System Center data</span></span>
- <span data-ttu-id="2e046-114">Anrufdetaildatensätze</span><span class="sxs-lookup"><span data-stu-id="2e046-114">Call detail records</span></span>
- <span data-ttu-id="2e046-115">QoE-Daten</span><span class="sxs-lookup"><span data-stu-id="2e046-115">Quality of experience data</span></span>
- <span data-ttu-id="2e046-116">IIS-Webserverprotokolle</span><span class="sxs-lookup"><span data-stu-id="2e046-116">IIS Web Server logs</span></span>
- <span data-ttu-id="2e046-117">SQL Server Protokolle</span><span class="sxs-lookup"><span data-stu-id="2e046-117">SQL Server logs</span></span>
- <span data-ttu-id="2e046-118">Syslog-Daten</span><span class="sxs-lookup"><span data-stu-id="2e046-118">Syslog data</span></span>
- <span data-ttu-id="2e046-119">Sicherheitsüberwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="2e046-119">Security audit logs</span></span>

<span data-ttu-id="2e046-120">Vor dem Hochladen verwendet die ODL-Anwendung einen Scrubbing-Dienst, um alle Felder zu entfernen, die Kundendaten enthalten, z. B. Mandanteninformationen und Informationen zur Identifizierung von Endbenutzern, und diese Felder durch einen Hashwert zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="2e046-120">Prior to uploading, the ODL application uses a scrubbing service to remove any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value.</span></span> <span data-ttu-id="2e046-121">Die bereinigungsprotokolle werden in Cosmos und in die NRT-Sicherheitsüberwachungslösung hochgeladen, die die Protokolle auf potenzielle Sicherheitsereignisse und Leistungsindikatoren analysiert.</span><span class="sxs-lookup"><span data-stu-id="2e046-121">The scrubbed logs are uploaded to Cosmos and to the NRT security monitoring solution that analyzes the logs for potential security events and performance indicators.</span></span> <span data-ttu-id="2e046-122">Der Zeitraum der Aufbewahrung von Überwachungsprotokolldaten in Cosmos wird von den Serviceteams bestimmt. Die meisten Überwachungsprotokolldaten werden 90 Tage oder länger aufbewahrt, um Untersuchungen von Sicherheitsvorfällen zu unterstützen und gesetzliche Aufbewahrungsanforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="2e046-122">The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="2e046-123">Der Zugriff auf Microsoft 365 in Cosmos gespeicherten Daten ist auf autorisiertes Personal beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2e046-123">Access to Microsoft 365 data stored in Cosmos is restricted to authorized personnel.</span></span> <span data-ttu-id="2e046-124">Microsoft schränkt die Verwaltung von Überwachungsprotokollen auf eine begrenzte Teilmenge der Sicherheitsteammitglieder ein, die für die Überwachungsfunktionen verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="2e046-124">Microsoft restricts the management of audit logs to a limited subset of Security Team members responsible for audit functionality.</span></span> <span data-ttu-id="2e046-125">Das Sicherheitsteam hat keinen ständigen administrativen Zugriff auf Cosmos, und alle Änderungen werden aufgezeichnet und überwacht.</span><span class="sxs-lookup"><span data-stu-id="2e046-125">The Security Team does not have standing administrative access to Cosmos, and all changes are recorded and audited.</span></span>

<span data-ttu-id="2e046-126">Nach der NRT-Analyse kann jedes Serviceteam Analysetools und Dashboards für Datenkorrelation, interaktive Abfragen und Datenanalyse verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e046-126">After NRT analysis, each service team can use analysis tools and dashboards for data correlation, interactive queries, and data analytics.</span></span> <span data-ttu-id="2e046-127">Diese Berichte werden verwendet, um die Gesamtleistung des Diensts zu überwachen und zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="2e046-127">These reports are used to monitor and improve the overall performance of the service.</span></span>
