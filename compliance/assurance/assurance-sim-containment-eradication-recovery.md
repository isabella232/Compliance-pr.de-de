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
hideEdit: true
ms.openlocfilehash: 7fff9c1909f0acd076945e3d569b143fe2324c0f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496722"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a>Verwaltung von Sicherheitsvorfällen in Microsoft 365: Eindämmung, Beseitigung und Wiederherstellung

Basierend auf der Vom Microsoft 365 Security Response-Team, dem Dienstteam und anderen durchgeführten Analyse wird ein entsprechender Eindämmungs- und Wiederherstellungsplan entwickelt, um die Auswirkungen des Sicherheitsvorfalls zu minimieren. Die entsprechenden Dienstteams wenden diesen Plan dann in der Produktion mit Unterstützung des Microsoft 365 Security Response-Teams an.

## <a name="containment"></a>Eindämmung

Nach dem Erkennen eines Sicherheitsvorfalls ist es wichtig, den Angriff zu verhindern, bevor der Widersacher auf mehr Ressourcen zugreifen oder mehr Schaden angerichtet hat. Das Hauptziel unserer Verfahren zur Reaktion auf Sicherheitsvorfälle besteht in der Begrenzung der Auswirkungen auf Kunden oder deren Daten oder auf Microsoft-Systeme, -Dienste und -Anwendungen.

## <a name="eradication"></a>Beseitigung

Als Beseitigung wird der Prozess bezeichnet, bei dem die Ursache des Sicherheitsvorfalls mit einem hohen Maß an Zuverlässigkeit eliminiert wird. Das Ziel ist zweifach:

- , um den Widersacher vollständig aus der Umgebung zu verdingen
- um die Sicherheitslücke (sofern bekannt) zu verringern, die es dem Gegner ermöglichte oder ermöglichte, die Umgebung erneut zu aktivieren.

Abhängig von der Art des Vorfalls, dem Umfang des Sicherheitsvorfalls, der Tiefe der Penetration und möglichen Auswirkungen empfiehlt das Microsoft 365 Security Response-Team, dass Dienstteams Auslöschungstechniken anwenden. In Anbetracht der potenziellen geschäftlichen Auswirkungen, die durch diese Ausrottungsschritte verursacht werden können, werden diese Entscheidungen von Serviceteams und dem Microsoft 365 Security Response-Team nach einer detaillierten Analyse und Genehmigung durch den Executive Incident Manager (falls erforderlich) getroffen.

## <a name="recovery"></a>Wiederherstellung

Da das Reaktionsteam ein angemessenes Maß an Vertrauen darauf erhält, dass der Widersacher aus der Umgebung entfernt wurde und alle bekannten anfälligen Pfade entfernt wurden, werden die einzelnen Dienstteams Wiederherstellungsschritte einleiten, um den Dienst zu einer bekannten und guten Konfiguration zu bringen. Diese Wiederherstellungsschritte werden in Abstimmung mit dem Microsoft 365 Security Response-Team erstellt. Diese Aktivität umfasst das Identifizieren des letzten bekannten guten Zustands des Diensts, das Wiederherstellen von Sicherungen in diesen Zustand, das Überprüfen anfälliger Angriffspfade im wiederhergestellten Zustand usw. Das Microsoft 365 Security Response-Team bestimmt in Abstimmung mit den Dienstteams den bestmöglichen Wiederherstellungsplan für die Umgebung.

Ein wichtiger Aspekt der Wiederherstellung besteht in der besseren Überwachung und den Kontrollen, um zu überprüfen, ob der Wiederherstellungsplan erfolgreich ausgeführt wurde und dass in der Umgebung keine Anzeichen für eine Verletzung vorhanden sind.

## <a name="customer-notification-of-security-incident"></a>Kundenbenachrichtigung über Sicherheitsvorfälle

Wenn Microsoft feststellt, dass ein Sicherheitsvorfall aufgetreten ist, benachrichtigen wir Sie mit unangemessener Verzögerung und innerhalb der vertraglichen und einhaltungsanforderungen, die wir vereinbart haben. Nach der Identifizierung aller betroffenen Mandanten arbeitet das Microsoft 365 Customer Experience (CxP)-Kommunikationsteam daran, alle relevanten Bestimmungen zu identifizieren, die für betroffene Mandanten gelten könnten. Das Microsoft 365 CxP Communications-Team verwendet den entsprechenden Kommunikationskanal, der in den geltenden Vorschriften definiert ist, um den entsprechenden Mandantenkontakt zu benachrichtigen.

Die Benachrichtigung enthält detaillierte Informationen zu dem Vorfall, z. B. eine Beschreibung des Vorfalls, die Auswirkungen auf Kundendaten( falls möglich), von Microsoft ergriffene Aktionen und/oder vorgeschlagene Aktionen für Kunden, die das Problem beheben und Wiederholungen verhindern sollen. Die Benachrichtigung wird an die angegebenen Administratoren des Microsoft 365-Mandanten übermittelt. Um sicherzustellen, dass Benachrichtigungen empfangen werden, sollten Sie sicherstellen, dass Ihre Administratoren genaue Kontaktinformationen in ihren Mandantenprofilen bereitstellen und verwalten. Darüber hinaus können Kunden je nach Art des Vorfalls auch über das Microsoft 365 Service Health Dashboard benachrichtigt[werden.](http://status.yammer.com/)

## <a name="related-articles"></a>Verwandte Artikel

- [Verwaltung von Sicherheitsvorfällen unter Microsoft 365](assurance-security-incident-management.md)
- [Vorbereitung der Sicherheitsvorfälle in Microsoft 365](assurance-sim-preparation.md)
- [Erkennung und Analyse von Sicherheitsvorfällen in Microsoft 365](assurance-sim-detection-analysis.md)
- [Microsoft 365 Security Incident Management post-incident activity](assurance-sim-post-incident-activity.md)
