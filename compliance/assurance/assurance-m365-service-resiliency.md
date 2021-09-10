---
title: Integrierte Dienstresilienz in Microsoft 365
description: Beschreibung der Dienstresilienz Microsoft 365
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: o365-solutions
ms.localizationpriority: medium
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 592cfcdf3da33e6c26e90d5a83fb6bcd3b4241e0
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947111"
---
# <a name="built-in-service-resiliency-in-microsoft-365"></a>Integrierte Dienstresilienz in Microsoft 365

Als Ihr Cloud-Zusammenarbeitsanbieter erkennt Microsoft die Notwendigkeit, sich kontinuierlich Ihr Vertrauen zu verdienen, indem es Lösungen anbietet, die konsistent funktionieren und die Ihre Benutzer lieben. Wenn ein bestimmter Dienst nicht verfügbar ist, wird er als Ausfallzeit bezeichnet. Die Definition von Ausfallzeit variiert für jeden Microsoft 365-Dienst, aber sie konzentriert sich in der Regel auf jeden Zeitraum, in dem Benutzer die wesentlichen Funktionen des Dienstes nicht nutzen können. Hier ist beispielsweise die Definition von Ausfallzeit für SharePoint Online, die vom Microsoft 365-SLA (Vereinbarung zum Servicelevel) abgenommen wird:

**"Ausfallzeit von SharePoint Online**: Jeder Zeitraum, in dem Benutzer keine Teile einer SharePoint Online-Websitesammlung lesen oder schreiben können, für die Sie über die entsprechenden Berechtigungen verfügen."

Sie finden die Definitionen für Ausfallzeiten in den [Vereinbarungen zum Servicelevel](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=37).

Um die Ausfallzeiten – geplant oder unerwartet – zu minimieren, sind Microsoft 365-Dienste so konzipiert und ausgeführt, dass Sie hochgradig verfügbar und Ausfall resistent sind, indem Sie sich auf vier Bereiche konzentrieren:

## <a name="activeactive-design"></a>Aktiv/Aktiv-Ausführung

In Microsoft 365 setzen wir darauf, dass alle Dienste in einem aktiven/aktiven Design entwickelt und betrieben werden, das die Resilienz erhöht. Dieses Design bedeutet, dass immer mehrere Instanzen eines Diensts ausgeführt werden, der auf Benutzeranforderungen reagieren kann und in geografisch verteilten Rechenzentren gehostet wird. Der gesamte Benutzerdatenverkehr wird über den Microsoft Front Door-Dienst durchgeführt. Er wird automatisch an die optimal lokalisierte Instanz des Diensts und zu allen Dienstfehlern geleitet, um die Auswirkungen auf die Kunden zu verhindern oder zu verringern.

## <a name="reduce-incident-scope"></a>Reduzieren des Vorfallumfangs

Der Umfang eines Dienstvorfalls wird anhand des Schweregrads, der Dauer und der Anzahl der Kunden ermittelt. Wir sind bestrebt, den Umfang aller Vorfälle zu begrenzen durch:

- mehrere Instanzen jedes Dienstes voneinander getrennt zu haben
- die kontrollierte, abgestufte Bereitstellung von Updates mit Hilfe von Validierungsringen, so dass alle Probleme, die sich aus dem Update ergeben könnten, frühzeitig im Bereitstellungsprozess erkannt und behoben werden können. Dieses Design ermöglicht bei Bedarf eine Regression des Updates und tritt zuerst in einer kleinen Gruppe innerhalb von Microsoft (innerer Ring) auf, bevor es für größere Gruppen wie alle 140.000 Microsoft-Mitarbeiter (Ring 2), dann für Early Adopter-Ringe (Ring 3) und letztendlich für alle Kunden global (Ring 4) bereitgestellt wird.
- Verbesserungen bei der Überwachung durch Automatisierung. Microsoft 365 ist ein großer Dienst, und die SLA-Ziel-Betriebszeit ist hoch. Am Anfang eines Dienstvorfalls, wenn Menschen an der Erkennung und Reaktion beteiligt sein mussten, konnten wir nicht schnell genug reagieren, um SLAs zu erfüllen. Die Automatisierung ist der Schlüssel für die schnelle und effektive Erkennung und Reaktion von Dienstvorfällen. Je früher wir etwas wissen, desto schneller lässt es sich beheben.

Zusammen mit den aktiven/aktiven Funktionen, die in Microsoft 365 Dienstarchitektur integriert sind, verringern diese Anstrengungen den Schweregrad, die Dauer und die Anzahl der betroffenen Kunden während eines Dienstvorfalls.  

## <a name="fault-isolation"></a>Fehlerisolation

So wie die Dienste aktiv/aktiv konzipiert und betrieben werden und voneinander getrennt sind, um zu verhindern, dass ein Fehler in einem Dienst einen anderen beeinflusst, wird die Codebasis des Dienstes nach ähnlichen Partitionsprinzipien entwickelt, der sogenannten Fehlerisolation. Maßnahmen zur Fehlerisolation sind inkrementelle Schutzmaßnahmen, die innerhalb der Codebasis selbst durchgeführt werden. Diese Maßnahmen tragen dazu bei, dass ein Problem in einem Bereich nicht in andere Betriebsbereiche übergeht.
Fehlerisolationsmaßnahmen werden in mehreren Phasen der Entwicklung und Bereitstellung eines Diensts angewendet, einschließlich Codeentwicklung, Dienstbereitstellung, Lastenausgleich und Datenbankreplikation.

Der Microsoft Security Development Lifecycle (SDL) fördert die Resilienz weiter und besteht aus einer Reihe von Praktiken, die Sicherheits-und Compliance-Anforderungen unterstützen. SDL leitet unsere Entwickler in den Aufbau widerstandsfähiger, sicherer und kompatibler Dienste. Zu den Schlüsselelementen von SDL gehören Codeüberprüfungen, Bedrohungsmodellierung, Penetrationstests und standardisierte Prozesse zur Ereignisreaktion in der Microsoft-Cloud.

Microsoft 365 Dienste sind in hohem Maße miteinander verbunden, aber die systeme und die technologie hinter ihnen sind so konzipiert, dass die Auswirkungen eines Dienstvorfalls durch das Übertragen auf andere Dienste begrenzt werden. Beispielsweise wirkt sich ein Problem, das sich auf Exchange Online auswirkt, nicht auf die Kernfunktionalität in Teams aus, oder ein Problem mit der Suchfunktionalität in SharePoint Online wirkt sich nicht auf die Möglichkeit von Benutzern aus, Dateien hoch- oder herunterzuladen.

## <a name="continuous-service-improvement"></a>Kontinuierliche Serviceverbesserung

Wenn wir einen Vorfall erleben, nehmen wir ihn ernst. Denn unsere redundante Cloud-Architektur und strenge interne Prozesse zielen darauf ab, unsere Dienste barrierefrei zu halten. Während eines Vorfalls erkennt unsere Überwachung schnell die betroffenen Dienste, und wenn Ihr Mandant betroffen ist, werden Sie sofort über verschiedene Kanäle benachrichtigt. Gleichzeitig folgen Entwickler genau definierten Prozessen, um das Problem zu analysieren, und führen die erforderlichen Schritte aus, um den normalen Betrieb so schnell wie möglich wiederherzustellen. Sobald der Dienst ordnungsgemäß funktioniert, führen wir im Rahmen des Zyklus der kontinuierlichen Serviceverbesserung Post Incident Reviews durch. Während der Post Incident Review identifizieren wir die eigentlichen Ursachen des Vorfalls und was zur Behebung der Probleme erforderlich war. Anschließend nehmen wir das, was aus der Situation gelernt wurde, und wenden es auf die Entwicklung und den Betrieb aller unserer Angebotspakete an. Mit diesem Wissen können wir verhindern, dass sich dieselbe Ursache auf andere Dienste und zusätzliche Kunden auswirkt.
