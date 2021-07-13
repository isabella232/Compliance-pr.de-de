---
title: 'Microsoft-Sicherheitsvorfallverwaltung: Aktivitäten nach dem Vorfall'
description: Dieser Artikel bietet eine Übersicht über den Prozess der Aktivitäten nach dem Vorfall bei der Verwaltung von Sicherheitsvorfällen in Microsoft-Onlinediensten.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 965c7d6d0d469b9eea981252805bda598c92a4c8
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377532"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a><span data-ttu-id="cb9c3-103">Microsoft-Sicherheitsvorfallverwaltung: Aktivitäten nach dem Vorfall</span><span class="sxs-lookup"><span data-stu-id="cb9c3-103">Microsoft security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="cb9c3-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="cb9c3-104">Postmortem</span></span>

<span data-ttu-id="cb9c3-105">Einige Sicherheitsvorfälle, insbesondere solche, die auswirkungen auf den Kunden haben oder zu einer Datenschutzverletzung führen, unterliegen einem vollständigen Vorfallstatus.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="cb9c3-106">Das Sicherheitsteam führt ein detailliertes Postmortem mit allen an der Reaktion auf Sicherheitsvorfälle beteiligten Parteien durch:</span><span class="sxs-lookup"><span data-stu-id="cb9c3-106">The security response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="cb9c3-107">Dokumentieren Sie die Abfolge der Ereignisse, die den Vorfall verursacht haben.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-107">Document the sequence of events that caused the incident.</span></span>
- <span data-ttu-id="cb9c3-108">Erstellen Sie eine technische Zusammenfassung des Vorfalls, die durch die Nachweise unterstützt wird, die die an der Verletzung beteiligten Akteure (sofern bekannt) umfassen.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="cb9c3-109">Diese Zusammenfassung enthält die Ausführung der Antwort und andere Wichtigeinkäufe.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="cb9c3-110">Identifizieren von technischen Fehlern, Verfahrensfehlern, manuellen Fehlern, Prozessfehlern und Kommunikationsfehlern und/oder zuvor unbekannten Angriffsvektoren, die während der Reaktion auf Sicherheitsvorfälle identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="cb9c3-111">Das Postmortem wirkt sich direkt auf die Verbesserung des Microsoft-Onlinediensts, die betrieblichen Prozesse und die Dokumentation aus, indem neue Prioritäten im Entwicklungszyklus der Microsoft-Onlinedienste festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-111">The postmortem will directly influence Microsoft online service improvement, operational processes, and documentation by setting new priorities in the Microsoft online services engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="cb9c3-112">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="cb9c3-112">Documentation</span></span>

<span data-ttu-id="cb9c3-113">Alle wichtigen technischen Ergebnisse im postirtischen Prozess werden in einem Bericht erfasst, in dem Investitionen in Dienste oder Korrekturen in Form von Fehlern oder Entwicklungsänderungsanforderungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="cb9c3-114">Diese Ergebnisse werden mit den entsprechenden Entwicklungsteams nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="cb9c3-115">Bei Prozessfehlern und organisationsübergreifenden Problemen werden Probleme in der Datenbank des Sicherheitsreaktionsteams dokumentiert und mit den entsprechenden Gruppen verfolgt, um sie zu beheben.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-115">For process failures and cross-organizational issues, issues are documented in the security response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="cb9c3-116">Prozessverbesserung</span><span class="sxs-lookup"><span data-stu-id="cb9c3-116">Process improvement</span></span>

<span data-ttu-id="cb9c3-117">Die Reaktion auf einen Sicherheitsvorfall in Microsoft-Onlinediensten umfasst die Koordination mit mehreren Gruppen, die über verschiedene Organisationen innerhalb von Microsoft verteilt sind, und möglicherweise sogar mit geeigneten externen Organisationen wie Strafverfolgungsbehörden.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-117">Responding to a security incident in Microsoft online services involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="cb9c3-118">Wir wissen, dass es wichtig ist, unsere Antworten nach jedem Sicherheitsvorfall sowohl auf Ausreichendes als auch auf Vollständigkeit zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="cb9c3-119">Bei identifizierten Verbesserungen oder Änderungen wertet das Sicherheitsteam die Vorschläge in Abstimmung mit den entsprechenden Teams und Beteiligten aus und integriert sie gegebenenfalls in standardbetriebsverfahren.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-119">For any identified improvements or changes, the security response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="cb9c3-120">Alle erforderlichen Änderungen, Fehler oder Dienstverbesserungen, die während der Reaktion auf Sicherheitsvorfälle oder nachträgliche Aktivitäten identifiziert wurden, werden in einer internen Microsoft Engineering-Datenbank protokolliert und nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft engineering database.</span></span> <span data-ttu-id="cb9c3-121">Alle potenziellen Fehler oder Features werden dem entsprechenden Besitzer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="cb9c3-122">Das Microsoft Security Response-Team überprüft alle Einträge, bis das Problem behoben ist.</span><span class="sxs-lookup"><span data-stu-id="cb9c3-122">The Microsoft security response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="cb9c3-123">Verwandte Artikel</span><span class="sxs-lookup"><span data-stu-id="cb9c3-123">Related articles</span></span>

- [<span data-ttu-id="cb9c3-124">Microsoft-Sicherheitsvorfallverwaltung</span><span class="sxs-lookup"><span data-stu-id="cb9c3-124">Microsoft security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="cb9c3-125">Microsoft Security Incident Management: Vorbereitung</span><span class="sxs-lookup"><span data-stu-id="cb9c3-125">Microsoft security incident management: Preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="cb9c3-126">Microsoft Security Incident Management: Erkennung und Analyse</span><span class="sxs-lookup"><span data-stu-id="cb9c3-126">Microsoft security incident management: Detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="cb9c3-127">Microsoft Security Incident Management: Eindämmung, Beseitigung und Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="cb9c3-127">Microsoft security incident management: Containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="cb9c3-128">So protokollieren Sie ein Supportticket für Sicherheitsereignisse</span><span class="sxs-lookup"><span data-stu-id="cb9c3-128">How to Log a Security Event Support Ticket</span></span>](/azure/security/fundamentals/event-support-ticket)
- [<span data-ttu-id="cb9c3-129">Azure und Dynamics 365-Benachrichtigung bei Datenschutzverletzung im Rahmen der DSGVO</span><span class="sxs-lookup"><span data-stu-id="cb9c3-129">Azure and Dynamics 365 breach notification under the GDPR</span></span>](/compliance/regulatory/gdpr-breach-azure-dynamics)
