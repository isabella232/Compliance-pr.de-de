---
title: Microsoft 365 Überwachung und Überwachung von Zugriffssteuerungen
description: 'Zusammenfassung: Eine Zusammenfassung der verschiedenen Überwachungs- und Überwachungszugriffssteuerungen, die in Microsoft 365 verfügbar sind.'
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: bf760bf68169092f99fe5a668c9f0087060f7ea2
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947153"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>Überwachen und Überwachen von Zugriffssteuerungen in Microsoft 365

Microsoft führt umfassende Überwachung und Überwachung aller Delegierungen, Berechtigungen und Vorgänge durch, die innerhalb Microsoft 365 auftreten. Microsoft 365 Zugriffssteuerung ist ein automatisierter Prozess, der auf dem Prinzip der geringsten Rechte und der Integration von Datenzugriffssteuerungen und -überwachungen basiert:

- Alle zulässigen Zugriffe können für einen eindeutigen Benutzer nachverfolgt werden. Administratoren sind für die Verarbeitung von Kundeninhalten verantwortlich.
- Zugriffssteuerungsanforderungen, Genehmigungen und Verwaltungsprotokolle werden zur Analyse von Sicherheits- und böswilligen Ereignissen erfasst.
- Zugriffsebenen werden nahezu in Echtzeit basierend auf der Mitgliedschaft in Sicherheitsgruppen überprüft, um sicherzustellen, dass nur Benutzer, die autorisierte geschäftliche Begründungen haben und die Berechtigungsanforderungen erfüllen, Zugriff auf die Systeme haben.
- Microsoft 365, seine Zugriffssteuerungen und unterstützenden Dienste, einschließlich Azure Active Directory und physischen Rechenzentren, werden regelmäßig von unabhängigen Drittanbietern auf die Einhaltung von [ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)und anderen [Standards](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)überprüft.
- Microsoft 365 Techniker müssen jährliche Sicherheitsschulungen durchführen, bewährte Verfahren für erhöhten Zugriff überprüfen und die Sicherheits- und Datenschutzrichtlinien von Microsoft bestätigen, um Berechtigungen für den Dienst aufrechtzuerhalten.

Automatisierte Warnungen werden ausgelöst, wenn verdächtige Aktivitäten erkannt werden, z. B. mehrere fehlgeschlagene Anmeldungen innerhalb eines kurzen Zeitraums. Das Microsoft 365 Security Response-Team verwendet maschinelles Lernen und Big Data-Analysen, um Aktivitäten zu überprüfen und zu analysieren, nach unregelmäßigen Zugriffsmustern zu suchen und proaktiv auf anomale und unrechtmäßige Aktivitäten zu reagieren. Microsoft setzt auch ein dediziertes Team von Penetrationstestern ein und setzt sich in regelmäßigen Übungen des roten und blauen Teams ein, um Sicherheits- und Zugriffssteuerungsprobleme im Dienst zu finden. Kunden können die Effektivität von Zugriffssteuerungssystemen überprüfen, indem sie Überwachungsberichte und die von Microsoft 365 bereitgestellte Verwaltungsaktivitäts-API verwenden.

Weitere Informationen finden Sie unter [Office 365 Management Activity API reference](/office/office-365-management-api/office-365-management-activity-api-reference) and Auditing and reporting in [Microsoft 365](assurance-auditing-and-reporting-overview.md).
