---
title: 'Verwaltung von Sicherheitsvorfällen in Microsoft 365: Eindämmung, Beseitigung und Wiederherstellung'
description: Dieser Artikel bietet eine Übersicht über den Prozess zur Eindämmung, Beseitigung und Wiederherstellung von Sicherheitsvorfällen in Microsoft 365.
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
ms.openlocfilehash: 702735ed2ba35a4f3b0a02123f0c58b5fb4d397e
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037607"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a>Verwaltung von Sicherheitsvorfällen in Microsoft 365: Eindämmung, Beseitigung und Wiederherstellung

Basierend auf der vom Microsoft 365 Security Response-Team, dem Serviceteam und anderen durchgeführten Analyse wird ein geeigneter Eindämmungs- und Wiederherstellungsplan entwickelt, um die Auswirkungen des Sicherheitsvorfalls zu minimieren. Die entsprechenden Serviceteams wenden diesen Plan dann in der Produktion mit Unterstützung des Microsoft 365 Security Response-Teams an.

## <a name="containment"></a>Eindämmung

Nachdem Sie einen Sicherheitsvorfall erkannt haben, ist es wichtig, den Angriff zu enthalten, bevor der Widerswillige auf weitere Ressourcen zugreifen oder mehr Schaden verursachen kann. Das Hauptziel unserer Verfahren zur Reaktion auf Sicherheitsvorfälle ist es, die Auswirkungen auf Kunden oder deren Daten oder auf Microsoft-Systeme, -Dienste und -Anwendungen zu begrenzen.

## <a name="eradication"></a>Beseitigung

Als Beseitigung wird der Prozess bezeichnet, bei dem die Ursache des Sicherheitsvorfalls mit einem hohen Maß an Zuverlässigkeit eliminiert wird. Das Ziel besteht in zweiFachen:

- um den Gegner vollständig aus der Umgebung zu verdingen
- um die Sicherheitslücke (sofern bekannt) zu verringern, die den Widerswilligen aktiviert hat oder es dem Gegner ermöglichen könnte, die Umgebung erneut zu aktivieren.

Abhängig von der Art des Vorfalls, dem Umfang des Sicherheitsvorfalls, der Tiefe der Penetration und möglichen Maßnahmen empfiehlt das Microsoft 365 Security Response-Team, dass Serviceteams Beseitigungstechniken anwenden. Angesichts der potenziellen geschäftlichen Auswirkungen, die durch diese Beseitigungsschritte verursacht werden können, werden diese Entscheidungen von Serviceteams und dem Microsoft 365 Security Response Team nach einer ausführlichen Analyse und Genehmigung durch den Leitenden Vorfallmanager (falls erforderlich) getroffen.

## <a name="recovery"></a>Wiederherstellung

Da das Reaktionsteam ein angemessenes Maß an Vertrauen erhält, dass der Widerswillige aus der Umgebung entfernt wurde und alle bekannten anfälligen Pfade beseitigt wurden, werden die einzelnen Serviceteams Wiederherstellungsschritte initiieren, um den Dienst zu einer bekannten und guten Konfiguration zu bringen. Diese Wiederherstellungsschritte werden in Abstimmung mit dem Microsoft 365 Security Response-Team sein. Diese Aktivität umfasst das Identifizieren des letzten als gut bekannten Status des Diensts, das Wiederherstellen aus Sicherungen in diesem Zustand, das Überprüfen anfälliger Angriffspfade im wiederhergestellten Zustand usw. Das Microsoft 365 Security Response-Team ermittelt in Abstimmung mit den Serviceteams den bestmöglichen Wiederherstellungsplan für die Umgebung.

Ein wichtiger Aspekt bei der Wiederherstellung besteht in der Verbesserung der Leistung und der Kontrollen, um zu überprüfen, ob der Wiederherstellungsplan erfolgreich ausgeführt wurde und dass in der Umgebung keine Anzeichen von Sicherheitsverletzungen vorhanden sind.

## <a name="customer-notification-of-security-incident"></a>Benachrichtigung des Kunden über Sicherheitsvorfälle

Wenn Microsoft feststellt, dass ein Sicherheitsvorfall aufgetreten ist, benachrichtigen wir Sie mit unangemessener Verzögerung sowie im Rahmen der vertraglichen und compliance-Anforderungen, die wir vereinbart haben. Nachdem alle betroffenen Mandanten identifiziert wurden, arbeitet das Microsoft 365 Customer Experience (CxP)-Kommunikationsteam daran, relevante Bestimmungen zu identifizieren, die möglicherweise für betroffene Mandanten gelten. Das Microsoft 365 CxP Communications-Team verwendet den geeigneten Kommunikationskanal, der in den geltenden Bestimmungen definiert ist, um den entsprechenden Mandantenkontakt zu benachrichtigen.

Die Benachrichtigung enthält ausführliche Informationen zu dem Vorfall, z. B. eine Beschreibung des Vorfalls, gegebenenfalls die Auswirkungen auf Kundendaten, von Microsoft ergriffene Aktionen und/oder vorgeschlagene Maßnahmen für Kunden, um das Problem zu beheben und Wiederholungen zu verhindern. Die Benachrichtigung wird den designierten Administratoren des Microsoft 365-Mandanten zugestellt. Um sicherzustellen, dass Benachrichtigungen empfangen werden, sollten Sie sicherstellen, dass Ihre Administratoren genaue Kontaktinformationen in ihren Mandantenprofilen bereitstellen und verwalten. Darüber hinaus können Kunden je nach Art des Vorfalls auch über das Microsoft 365 Service Health Dashboard benachrichtigt[werden.](http://status.yammer.com/)

## <a name="related-articles"></a>Verwandte Artikel

- [Verwaltung von Sicherheitsvorfällen in Microsoft 365](assurance-security-incident-management.md)
- [Vorbereitung der Verwaltung von Sicherheitsvorfällen in Microsoft 365](assurance-sim-preparation.md)
- [Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365](assurance-sim-detection-analysis.md)
- [Microsoft 365-Sicherheitsvorfallverwaltung nach einem Vorfall](assurance-sim-post-incident-activity.md)
