---
title: 'Microsoft Security Incident Management: Eindämmung, Beseitigung und Wiederherstellung'
description: Dieser Artikel bietet eine Übersicht über den Eindämmungs-, Beseitigungs- und Wiederherstellungsprozess von Sicherheitsvorfällen in Microsoft-Onlinediensten.
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
ms.openlocfilehash: 95e52107df2f3e745d393c62929f7c169bcf9a33
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377552"
---
# <a name="microsoft-security-incident-management-containment-eradication-and-recovery"></a>Microsoft Security Incident Management: Eindämmung, Beseitigung und Wiederherstellung

Basierend auf der vom Sicherheitsteam, dem Serviceteam und anderen durchgeführten Analyse wird ein geeigneter Aufnahme- und Wiederherstellungsplan entwickelt, um die Auswirkungen des Sicherheitsvorfalls zu minimieren. Die entsprechenden Serviceteams wenden diesen Plan dann mit Unterstützung des Sicherheitsteams in der Produktion an.

## <a name="containment"></a>Eindämmung

Nach dem Erkennen eines Sicherheitsvorfalls ist es wichtig, den Angriff einzudämmen, bevor der Angreifer auf mehr Ressourcen zugreifen oder mehr Schaden verursachen kann. Das Hauptziel unserer Verfahren zur Reaktion auf Sicherheitsvorfälle besteht darin, die Auswirkungen auf Kunden oder deren Daten oder auf Microsoft-Systeme, -Dienste und -Anwendungen zu begrenzen.

## <a name="eradication"></a>Beseitigung

Als Beseitigung wird der Prozess bezeichnet, bei dem die Ursache des Sicherheitsvorfalls mit einem hohen Maß an Zuverlässigkeit eliminiert wird. Das Ziel besteht aus zwei Elementen:

- den Angreifer vollständig aus der Umgebung zu entfernen
- um die Sicherheitslücke (falls bekannt) zu verringern, die es dem Angreifer ermöglicht hat oder ermöglichen könnte, die Umgebung erneut zu aktivieren.

Abhängig von der Art des Vorfalls, dem Umfang des Sicherheitsvorfalls, der Tiefe der Penetration und möglichen Vorfällen empfiehlt das Sicherheitsteam, dass Serviceteams Techniken zur Beseitigung anwenden. Unter Berücksichtigung der potenziellen geschäftlichen Auswirkungen, die durch diese Beseitigungsschritte verursacht werden können, werden diese Entscheidungen von Serviceteams und dem Sicherheitsreaktionsteam nach einer detaillierten Analyse und Genehmigung durch den Executive Incident Manager (falls erforderlich) getroffen.

## <a name="recovery"></a>Wiederherstellung

Da das Reaktionsteam ein angemessenes Maß an Vertrauen erhält, dass der Angreifer aus der Umgebung ausgeschlossen wurde und alle bekannten anfälligen Pfade eliminiert wurden, initiieren die einzelnen Dienstteams Wiederherstellungsschritte, um den Dienst in eine bekannte und gute Konfiguration zu bringen. Diese Wiederherstellungsschritte werden in Abstimmung mit dem Sicherheitsteam ausgeführt. Diese Aktivität umfasst die Identifizierung des letzten bekannten ordnungsgemäßen Status des Diensts, das Wiederherstellen von Sicherungen in diesen Zustand, das Überprüfen anfälliger Angriffspfade im wiederhergestellten Zustand usw. Das Sicherheitsteam ermittelt in Abstimmung mit den Serviceteams den bestmöglichen Wiederherstellungsplan für die Umgebung.

Ein wichtiger Aspekt der Wiederherstellung besteht darin, dass verbesserte Überwachung und Kontrollen vorhanden sind, um zu überprüfen, ob der Wiederherstellungsplan erfolgreich ausgeführt wurde und dass in der Umgebung keine Anzeichen von Sicherheitsverletzungen vorhanden sind.

## <a name="customer-notification-of-security-incident"></a>Benachrichtigung des Kunden über Sicherheitsvorfälle

Wenn Microsoft feststellt, dass ein Sicherheitsvorfall aufgetreten ist, benachrichtigen wir Sie mit unangemessener Verzögerung und innerhalb der vertraglichen und Compliance-Anforderungen, denen wir zugestimmt haben. Nachdem alle betroffenen Mandanten identifiziert wurden, arbeitet das entsprechende Kommunikationsteam an der Identifizierung relevanter Vorschriften, die möglicherweise für betroffene Mandanten gelten. Das Kommunikationsteam verwendet den entsprechenden Kommunikationskanal, der in den geltenden Bestimmungen definiert ist, um den entsprechenden Mandantenkontakt zu benachrichtigen.

Die Benachrichtigung enthält detaillierte Informationen zu dem Vorfall, z. B. eine Beschreibung des Vorfalls, ggf. die Auswirkungen auf Kundendaten, von Microsoft ausgeführte Aktionen und/oder vorgeschlagene Aktionen, die Kunden ergreifen können, um das Problem zu beheben und Wiederholungen zu verhindern. Die Benachrichtigung wird an den/die designierten Administratoren des Microsoft-Onlinedienstmandanten übermittelt. Um sicherzustellen, dass Benachrichtigungen empfangen werden, sollten Sie sicherstellen, dass Ihre Administratoren genaue Kontaktinformationen in ihren Mandantenprofilen bereitstellen und verwalten. Darüber hinaus können Microsoft 365 Kunden je nach Art des Vorfalls auch über das [Microsoft 365 Service Health Dashboard](http://status.yammer.com/)benachrichtigt werden.

## <a name="related-articles"></a>Verwandte Artikel

- [Microsoft-Sicherheitsvorfallverwaltung](assurance-security-incident-management.md)
- [Microsoft Security Incident Management: Vorbereitung](assurance-sim-preparation.md)
- [Microsoft Security Incident Management: Erkennung und Analyse](assurance-sim-detection-analysis.md)
- [Microsoft-Sicherheitsvorfallverwaltung: Aktivitäten nach dem Vorfall](assurance-sim-post-incident-activity.md)
- [So protokollieren Sie ein Supportticket für Sicherheitsereignisse](/azure/security/fundamentals/event-support-ticket)
- [Azure und Dynamics 365-Benachrichtigung bei Datenschutzverletzung im Rahmen der DSGVO](/compliance/regulatory/gdpr-breach-azure-dynamics)
