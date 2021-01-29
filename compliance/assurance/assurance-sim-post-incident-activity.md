---
title: 'Microsoft 365-Sicherheitsvorfallverwaltung: Aktivitäten nach dem Vorfall'
description: Dieser Artikel bietet eine Übersicht über den Prozess der Sicherheitsvorfallverwaltung nach einem Vorfall in Microsoft 365.
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
ms.openlocfilehash: 66c25503ac574de512f5201981112a0e54714968
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040348"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a><span data-ttu-id="0e484-103">Microsoft 365-Sicherheitsvorfallverwaltung: Aktivitäten nach dem Vorfall</span><span class="sxs-lookup"><span data-stu-id="0e484-103">Microsoft 365 security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="0e484-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="0e484-104">Postmortem</span></span>

<span data-ttu-id="0e484-105">Einige Sicherheitsvorfälle, insbesondere solche, die Auswirkungen auf Kunden haben oder zu einer Datenschutzverletzung führen, unterliegen einem vollständigen Vorfall nach dem Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0e484-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="0e484-106">Das Microsoft 365 Security Response-Team führt eine ausführliche Nachergänzung mit allen Beteiligten durch, die an der Reaktion auf Sicherheitsvorfälle beteiligt sind für:</span><span class="sxs-lookup"><span data-stu-id="0e484-106">The Microsoft 365 Security Response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="0e484-107">Dokumentieren der Reihenfolge der Ereignisse, die den Vorfall verursacht haben</span><span class="sxs-lookup"><span data-stu-id="0e484-107">Document the sequence of events that caused the incident</span></span>
- <span data-ttu-id="0e484-108">Erstellen Sie eine technische Zusammenfassung des Vorfalls, wie von den Nachweisen unterstützt, die die an der Verletzung beteiligten Akteure umfassen (sofern bekannt).</span><span class="sxs-lookup"><span data-stu-id="0e484-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="0e484-109">Diese Zusammenfassung enthält die Ausführung der Antwort und andere Wichtige.</span><span class="sxs-lookup"><span data-stu-id="0e484-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="0e484-110">Identifizieren Sie technische Fehler, Verfahrensfehler, manuelle Fehler, Prozessfehler und Kommunikationsfehler und/oder zuvor unbekannte Angriffsvektoren, die während der Reaktion auf Sicherheitsvorfälle identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="0e484-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="0e484-111">Das Postmortem hat direkten Einfluss auf die Verbesserung des Microsoft 365-Diensts, die betrieblichen Prozesse und die Dokumentation, indem neue Prioritäten im Microsoft 365 Engineering-Entwicklungszyklus festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0e484-111">The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="0e484-112">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="0e484-112">Documentation</span></span>

<span data-ttu-id="0e484-113">Alle wichtigen technischen Erkenntnisse im post-anstammischen Prozess werden in einem Bericht erfasst, und es werden Dienstinvestitionen oder Korrekturen in Form von Fehlern oder Entwicklungsänderungsanforderungen erfasst.</span><span class="sxs-lookup"><span data-stu-id="0e484-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="0e484-114">Diese Erkenntnisse werden mit den entsprechenden Entwicklungsteams verfolgt.</span><span class="sxs-lookup"><span data-stu-id="0e484-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="0e484-115">Bei Prozessfehlern und organisationsübergreifenden Problemen werden Probleme in der Datenbank des Microsoft 365 Security Response-Teams dokumentiert und mit den entsprechenden Gruppen verfolgt, um sie zu beheben.</span><span class="sxs-lookup"><span data-stu-id="0e484-115">For process failures and cross-organizational issues, issues are documented in the Microsoft 365 Security Response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="0e484-116">Prozessverbesserung</span><span class="sxs-lookup"><span data-stu-id="0e484-116">Process improvement</span></span>

<span data-ttu-id="0e484-117">Die Reaktion auf einen Sicherheitsvorfall in Microsoft 365 umfasst die Koordination mit mehreren Gruppen, die über verschiedene Organisationen innerhalb von Microsoft verteilt sind, und potenziell sogar geeignete externe Organisationen wie Strafverfolgungsbehörden.</span><span class="sxs-lookup"><span data-stu-id="0e484-117">Responding to a security incident in Microsoft 365 involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="0e484-118">Wir wissen, dass es wichtig ist, unsere Antworten nach jedem Sicherheitsvorfall sowohl aus Gründen der Genauigkeit als auch der Vollständigkeit auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="0e484-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="0e484-119">Für identifizierte Verbesserungen oder Änderungen wertet das Microsoft 365 Security Response-Team die Vorschläge in Abstimmung mit den entsprechenden Teams und Beteiligten aus und integriert sie gegebenenfalls in Standardbetriebsverfahren.</span><span class="sxs-lookup"><span data-stu-id="0e484-119">For any identified improvements or changes, the Microsoft 365 Security Response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="0e484-120">Alle erforderlichen Änderungen, Fehler oder Dienstverbesserungen, die während der Reaktion auf Sicherheitsvorfälle oder der nach dem Ereignis identifiziert wurden, werden protokolliert und in einer internen Microsoft 365-Engineering-Datenbank nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="0e484-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft 365 engineering database.</span></span> <span data-ttu-id="0e484-121">Alle potenziellen Fehler oder Features werden dem entsprechenden Besitzer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0e484-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="0e484-122">Das Microsoft 365 Security Response-Team überprüft alle Einträge, bis das Problem behoben ist.</span><span class="sxs-lookup"><span data-stu-id="0e484-122">The Microsoft 365 Security Response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="0e484-123">Verwandte Artikel</span><span class="sxs-lookup"><span data-stu-id="0e484-123">Related articles</span></span>

- [<span data-ttu-id="0e484-124">Verwaltung von Sicherheitsvorfällen in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0e484-124">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="0e484-125">Vorbereitung der Verwaltung von Sicherheitsvorfällen in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0e484-125">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="0e484-126">Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0e484-126">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="0e484-127">Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0e484-127">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
