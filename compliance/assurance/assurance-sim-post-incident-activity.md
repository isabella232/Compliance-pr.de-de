---
title: 'Microsoft 365 Security Incident Management: Aktivitäten nach dem Vorfall'
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
hideEdit: true
ms.openlocfilehash: 4ebd31c16f8abb3eddd6ed924a045d88597aba40
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496714"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a><span data-ttu-id="debdb-103">Microsoft 365 Security Incident Management: Aktivitäten nach dem Vorfall</span><span class="sxs-lookup"><span data-stu-id="debdb-103">Microsoft 365 security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="debdb-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="debdb-104">Postmortem</span></span>

<span data-ttu-id="debdb-105">Einige Sicherheitsvorfälle, insbesondere solche Vorfälle, die sich auf Kunden auswirken oder zu einer Datenschutzverletzung führen, unterliegen einem vollständigen Vorfall nach dem Vorfall.</span><span class="sxs-lookup"><span data-stu-id="debdb-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="debdb-106">Das Microsoft 365 Security Response-Team führt ein detailliertes Postmortem mit allen an der Reaktion auf Sicherheitsvorfälle beteiligten Parteien durch:</span><span class="sxs-lookup"><span data-stu-id="debdb-106">The Microsoft 365 Security Response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="debdb-107">Dokumentieren der Reihenfolge der Ereignisse, die den Vorfall verursacht haben</span><span class="sxs-lookup"><span data-stu-id="debdb-107">Document the sequence of events that caused the incident</span></span>
- <span data-ttu-id="debdb-108">Erstellen Sie eine technische Zusammenfassung des Vorfalls, die von den Nachweisen unterstützt wird, die die an der Verletzung beteiligten Akteure (sofern bekannt) enthalten.</span><span class="sxs-lookup"><span data-stu-id="debdb-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="debdb-109">Diese Zusammenfassung enthält die Ausführung der Antwort und andere wichtige Informationen.</span><span class="sxs-lookup"><span data-stu-id="debdb-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="debdb-110">Identifizieren Sie technische Fehler, Verfahrensfehler, manuelle Fehler, Prozessfehler und Kommunikationsfehler und/oder zuvor unbekannte Angriffsvektoren, die während der Reaktion auf Sicherheitsvorfälle identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="debdb-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="debdb-111">Das Postmortem hat direkten Einfluss auf die Verbesserung der Microsoft 365-Dienste, die operativen Prozesse und die Dokumentation, indem neue Prioritäten im Microsoft 365-Entwicklungszyklus festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="debdb-111">The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="debdb-112">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="debdb-112">Documentation</span></span>

<span data-ttu-id="debdb-113">Alle wichtigen technischen Erkenntnisse im postmortem-Prozess werden in einem Bericht und in Serviceinvestitionen oder -korrekturen in Form von Fehlern oder Entwicklungsänderungsanforderungen erfasst.</span><span class="sxs-lookup"><span data-stu-id="debdb-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="debdb-114">Diese Erkenntnisse werden mit den entsprechenden Technischen Teams weiterverarbeiten.</span><span class="sxs-lookup"><span data-stu-id="debdb-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="debdb-115">Bei Prozessfehlern und organisationsübergreifenden Problemen werden Probleme in der Datenbank des Microsoft 365 Security Response-Teams dokumentiert und mit den entsprechenden Gruppen zur Problembesprechung nachgegangen.</span><span class="sxs-lookup"><span data-stu-id="debdb-115">For process failures and cross-organizational issues, issues are documented in the Microsoft 365 Security Response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="debdb-116">Prozessverbesserung</span><span class="sxs-lookup"><span data-stu-id="debdb-116">Process improvement</span></span>

<span data-ttu-id="debdb-117">Die Reaktion auf einen Sicherheitsvorfall in Microsoft 365 umfasst die Koordination mit mehreren Gruppen, die über verschiedene Organisationen in Microsoft verteilt sind, und potenziell sogar geeignete externe Organisationen wie die Strafverfolgung.</span><span class="sxs-lookup"><span data-stu-id="debdb-117">Responding to a security incident in Microsoft 365 involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="debdb-118">Wir wissen, dass es wichtig ist, unsere Antworten nach jedem Sicherheitsvorfall sowohl auf Dieligkeit als auch auf Vollständigkeit auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="debdb-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="debdb-119">Für identifizierte Verbesserungen oder Änderungen wertet das Microsoft 365 Security Response-Team die Vorschläge in Abstimmung mit den entsprechenden Teams und Beteiligten aus und integriert sie gegebenenfalls in standardbetriebsverfahren.</span><span class="sxs-lookup"><span data-stu-id="debdb-119">For any identified improvements or changes, the Microsoft 365 Security Response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="debdb-120">Alle erforderlichen Änderungen, Fehler oder Dienstverbesserungen, die während der Reaktion auf Sicherheitsvorfälle oder postmortem Aktivitäten identifiziert wurden, werden protokolliert und in einer internen Microsoft 365-Engineeringdatenbank nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="debdb-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft 365 engineering database.</span></span> <span data-ttu-id="debdb-121">Alle potenziellen Fehler oder Features werden dem entsprechenden Besitzer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="debdb-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="debdb-122">Das Microsoft 365 Security Response-Team überprüft alle Einträge, bis das Problem behoben ist.</span><span class="sxs-lookup"><span data-stu-id="debdb-122">The Microsoft 365 Security Response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="debdb-123">Verwandte Artikel</span><span class="sxs-lookup"><span data-stu-id="debdb-123">Related articles</span></span>

- [<span data-ttu-id="debdb-124">Verwaltung von Sicherheitsvorfällen unter Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="debdb-124">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="debdb-125">Vorbereitung der Sicherheitsvorfälle in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="debdb-125">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="debdb-126">Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="debdb-126">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="debdb-127">Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="debdb-127">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
