---
title: Microsoft 365-Zugriffssteuerungen für Überwachung und Überwachung
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
hideEdit: true
ms.openlocfilehash: e9a9ea713afbf7568c1ae67d31a57dd9dce51fc3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497543"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>Überwachen und Überwachen von Zugriffssteuerungen in Microsoft 365

Microsoft führt umfassende Überwachung und Überwachung aller Delegierung, Berechtigungen und Vorgänge durch, die in Microsoft 365 ausgeführt werden. Die Microsoft 365-Zugriffssteuerung ist ein automatisierter Prozess, der auf dem Prinzip der geringsten Rechte und der Einbindung von Datenzugriffssteuerelementen und -überwachungen baut:

- Der zulässige Zugriff kann auf einen eindeutigen Benutzer zurückverfolgt werden. Administratoren sind für den Umgang mit Kundeninhalten verantwortlich.
- Zugriffssteuerungsanforderungen, Genehmigungen und Verwaltungsprotokolle werden zur Analyse von Sicherheits- und Böswilligen Ereignissen erfasst.
- Zugriffsstufen werden nahezu in Echtzeit basierend auf der Mitgliedschaft in Sicherheitsgruppen überprüft, um sicherzustellen, dass nur Benutzer, die über autorisierte geschäftliche Begründungen verfügen und die Berechtigungsanforderungen erfüllen, Zugriff auf die Systeme haben.
- Microsoft 365, seine Zugriffssteuerungen und unterstützende Dienste, einschließlich Azure Active Directory und physischen Rechenzentren, werden regelmäßig von unabhängigen Drittanbietern auf Die Einhaltung von [ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)und anderen Standards [überprüft.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)
- Microsoft 365-Techniker müssen jährlich Sicherheitsschulungen machen, bewährte Verfahren für den erhöhten Zugriff überprüfen und die Sicherheits- und Datenschutzrichtlinien von Microsoft zur Aufrechterhaltung von Berechtigungen für den Dienst bestätigen.

Automatisierte Warnungen werden ausgelöst, wenn verdächtige Aktivitäten erkannt werden, z. B. mehrere fehlgeschlagene Anmeldungen innerhalb eines kurzen Zeitraums. Das Microsoft 365 Security Response-Team verwendet maschinelles Lernen und big data analysis, um Aktivitäten zu überprüfen und zu analysieren, nach unregelmäßigen Zugriffsmustern zu suchen und proaktiv auf anomale und unrechtmäßige Aktivitäten zu reagieren. Microsoft setzt außerdem ein dediziertes Team von Penetrationstestern ein und verwendet regelmäßig Übungen des Roten Teams und des Blauen Teams, um Sicherheits- und Zugriffssteuerungsprobleme im Dienst zu finden. Kunden können die Effektivität von Zugriffssteuerungssystemen mithilfe von Überwachungsberichten und der von Microsoft 365 bereitgestellten Verwaltungsaktivitäts-API überprüfen.

Weitere Informationen finden Sie unter [Office 365 Management Activity API reference](/office/office-365-management-api/office-365-management-activity-api-reference) and Auditing and reporting in Microsoft [365](assurance-auditing-and-reporting-overview.md).
