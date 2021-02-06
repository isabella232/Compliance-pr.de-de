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
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>Überwachen und Überwachen von Zugriffssteuerungen in Microsoft 365

Microsoft führt eine umfassende Überwachung aller Delegierung, Berechtigungen und Vorgänge aus, die in Microsoft 365 ausgeführt werden. Die Microsoft 365-Zugriffssteuerung ist ein automatisierter Prozess, der auf dem Prinzip der geringsten Rechte und der Integration von Datenzugriffssteuerungen und -überwachungen aufgebaut ist:

- Der zulässige Zugriff kann auf einen eindeutigen Benutzer nachverfolgt werden. Administratoren sind für die Verarbeitung von Kundeninhalten verantwortlich.
- Zugriffssteuerungsanforderungen, Genehmigungen und Verwaltungsprotokolle werden zur Analyse von Sicherheits- und Böswilligen Ereignissen erfasst.
- Zugriffsebenen werden nahezu in Echtzeit basierend auf der Mitgliedschaft in Sicherheitsgruppen überprüft, um sicherzustellen, dass nur Benutzer, die berechtigte geschäftliche Begründungen haben und die Berechtigungsanforderungen erfüllen, Zugriff auf die Systeme haben.
- Microsoft 365, seine Zugriffssteuerungen und unterstützenden Dienste, einschließlich Azure Active Directory und physischen Rechenzentren, werden regelmäßig von unabhängigen Drittanbietern auf Einhaltung von [ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)und anderen Standards [überprüft.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)
- Microsoft 365-Techniker müssen jährlich Sicherheitsschulungen machen, die bewährten Verfahren für den erweiterten Zugriff überprüfen und die Sicherheits- und Datenschutzrichtlinien von Microsoft zur Aufrechterhaltung von Berechtigungen für den Dienst bestätigen.

Automatisierte Warnungen werden ausgelöst, wenn verdächtige Aktivitäten erkannt werden, z. B. mehrere fehlgeschlagene Anmeldungen innerhalb eines kurzen Zeitraums. Das Microsoft 365 Security Response-Team verwendet maschinelles Lernen und Big Data-Analysen, um Aktivitäten zu überprüfen und zu analysieren, nach unregelmäßigen Zugriffsmustern zu suchen und proaktiv auf anomale und unrechtmäßige Aktivitäten zu reagieren. Microsoft setzt außerdem ein dediziertes Team von Penetrationstestern ein und verwendet regelmäßige Übungen des roten Teams und des blauen Teams, um Sicherheits- und Zugriffssteuerungsprobleme im Dienst zu finden. Kunden können die Effektivität von Zugriffskontrollsystemen mithilfe von Überwachungsberichten und der von Microsoft 365 bereitgestellten Verwaltungsaktivitäts-API überprüfen.

Weitere Informationen finden Sie unter [Office 365 Management Activity API reference](/office/office-365-management-api/office-365-management-activity-api-reference) and Auditing and reporting in Microsoft [365](assurance-auditing-and-reporting-overview.md).
