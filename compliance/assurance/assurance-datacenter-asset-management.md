---
title: Verwaltung von Datencenterobjekten
description: Eine Übersicht über die Ressourcenverwaltung von Microsoft-Rechenzentren.
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
ms.openlocfilehash: fafba29a25c5b01fa37d091fb210185a98365192
ms.sourcegitcommit: b228be59e13ae2e05ba85f65c1d4648fef5e9260
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2021
ms.locfileid: "60356384"
---
# <a name="datacenter-asset-management"></a>Verwaltung von Datencenterobjekten

Microsoft-Rechenzentren bestehen aus verschiedenen physischen und virtuellen Komponenten, die jeweils als Ressource bezeichnet werden. Die Microsoft Cloud Operations and Innovation (CO+I)-Engineeringgruppe folgt sicheren standardisierten Prozessen für die Bereitstellung, Nachverfolgung und Außerbetriebnahme von physischen und virtuellen Ressourcen.

## <a name="supply-chain-integrity"></a>Integrität der Lieferkette

Das Sichern von Ressourcen beginnt mit der Sicherung der Lieferkette. Microsoft setzt sich für die Integrität der Lieferkette und eine End-to-End-Sicherheit der Lieferkette ein. Lieferanten befolgen strenge Verfahren zur Verkettung der Kontrolle beim Transport unserer Cloudkomponenten, um das Risiko von Änderungen und Manipulationen zu verringern. Alle eingehenden und ausgehenden Bestände werden sorgfältig geprüft und überwacht, um die Integrität der Firmware und Komponenten sicherzustellen.

Informationssystem-Komponenten, die an Microsoft-Rechenzentren übergeben werden, sind in der Regel geplant. Bei ungeplanten Käufen prüft Microsoft sorgfältig und stellt sicher, dass sie für die Eingabe in einen Microsoft-Computerraum vor der physischen Eingabe genehmigt wurden. Wenn eine Informationssystem-Komponente in das Gebäude eintritt, vergleicht das Team für die Objektverwaltung das empfangene Element mit dem referenzierten Ticket und scannt das Gerät in das Ressourcenverwaltungstool. Alle empfangenen oder ausgelieferten Komponenten des Informationssystems werden vom Workflowticketingtool und in den Versandprotokollen im Ressourcenverwaltungstool nachverfolgt. Besucher dürfen keine persönlichen Laptops und Mobiltelefone verwenden (mit Ausnahme von Notrufen und Notizen), obwohl sie in der Produktionsumgebung (Colocations) zugelassen sind. Das Anschließen von Mobiltelefonen an ein Gerät oder das Aufnehmen von Fotos ist gemäß rechenzentrumsbasierter Richtlinie nicht zulässig. Wenn das Gerät, das in das Rechenzentrum eintritt, für Wartungszwecke verwendet wird, erfordert die Ausrüstung die Genehmigung der Rechenzentrumsverwaltung im Datacenter Access Tool-System.

## <a name="asset-inventory"></a>Bestandsaufnahme

Microsoft fordert, dass alle Rechenzentrumsressourcen berücksichtigt werden und einen bestimmten Besitzer haben. Besitzer tragen die Verantwortung dafür, die Ressourceninformationen für ihre physischen und virtuellen Ressourcen auf dem neuesten Stand zu halten. Wenn einem Rechenzentrum neue physische Ressourcen hinzugefügt werden, werden sie registriert, gescannt, eindeutig gekennzeichnet und in die Warenwirtschaftssysteme eingecheckt. Automatisierte Überwachungstools helfen bei der Nachverfolgung sowohl physischer wie virtueller Objekte.

## <a name="asset-maintenance"></a>Wartung von Ressourcen

Microsoft verfügt über zwei Teams, die unterschiedliche Arten der Objektwartung bereitstellen: die Teams für kritische Umgebungen (CRITICAL Environment, CE) und Site Services. Das CE-Team stellt die Einrichtungsverwaltung für stromtechnische, mechanische und physische Systeme bereit, die die Betriebsinfrastruktur der Anlage umfassen. Sie planen, führen, dokumentieren und überprüfen auch alle Wartungsaktivitäten, die auf CE-Komponenten durchgeführt werden. Microsoft-Rechenzentren basieren auf einem computerisierten Wartungsverwaltungssystem, um Wartungszeitpläne und Arbeitsaufträge zu verwalten. Das Site Services-Team bedient alle Microsoft-Onlinedienstressourcen, die sich in den Microsoft-Rechenzentren befinden. Darüber hinaus bietet das Site Services-Team vor Ort technischen Support und Break-Fix-Dienst für Objekte, die zu Bereitstellungsdiensten für Eigenschaften aus dem Rechenzentrum gehören.

## <a name="asset-classification"></a>Ressourcenklassifizierung

Microsoft-Ressourcen – einschließlich Daten – werden gemäß Enterprise Datentaxonomierichtlinien klassifiziert. Diese Richtlinien fördern die Standardisierung im gesamten Unternehmen und werden jährlich überprüft und aktualisiert. Die Standards für die Klassifizierung von Objekten und den Schutz von Objekten beschreiben die Sicherheitsverfahren, die Mitarbeiter bei der Interaktion mit den einzelnen Ressourcen befolgen müssen. Kunden werden als Besitzer ihrer Daten betrachtet, die in der Microsoft-Cloudumgebung gespeichert sind. Als Kundeninhalte oder Kundendaten klassifizierte Datenressourcen werden durch geeignete Sicherheitsmaßnahmen geschützt.

Microsoft betrachtet die gesamte Dokumentation als systemeigene Ressource. Das Team für Websitedienste ist für die Klassifizierung seiner Objekte und die Anwendung der zugehörigen Sicherheitsvorkehrungen gemäß den Standards für die Objektklassifizierung und den Objektschutz sowie für alle zusätzlichen Vom Serviceteam definierten Anforderungen verantwortlich.

Objektbesitzer müssen ihren Ressourcen aus ausnahme eine Objektklassifizierung zuweisen. In Microsoft-Rechenzentrumsumgebungen beziehen sich Ressourcen auf Server und Netzwerkgeräte. Andere digitale Medien wie USB-Speichersticks, externe Festplatten oder CD/DVDs werden nicht für den Dienstbetrieb verwendet. Nicht digitale Medien werden in Rechenzentren nicht verwendet.

## <a name="media-storage"></a>Medienspeicherung

Digitale Medienobjekte von Microsoft werden physisch und sicher in Microsoft Datacenter-Colocation-Räumen gespeichert. Mehrere Ebenen physischer Zugriffssteuerungen und Videoüberwachung sind vorhanden, um diese Ressourcen zu schützen und zu überwachen. Wenn digitale Medienressourcen das Ende ihres Lebenszyklus erreichen, werden sie mithilfe von Methoden gelöscht, gelöscht oder zerstört, die mit NIST SP 800-88 vor der Entsorgung konsistent sind. Der Artikel ["Vernichtung](assurance-data-bearing-device-destruction.md) von Geräten, die Daten tragen" behandelt den Prozess der sicheren Entsorgung von Objekten.

## <a name="media-transport"></a>Medientransport

Microsoft schränkt Aktivitäten für den Objekttransport auf autorisiertes Personal über die Kette von Schutzmechanismen ein. Durch die Verwendung von Sperren, manipulationssicheren Plomben und der erforderlichen Überprüfung des Bestands wird sichergestellt, dass nur autorisiertes Personal an der Objektübertragung beteiligt ist.

Alle Medien, die aus Microsoft-Rechenzentren übertragen werden, erfordern eine genaue Nachverfolgung. Microsoft hat einen Vertrag mit mehreren genehmigten Lieferanten abgeschlossen, um sichere Versanddienste bereitzustellen. Der sichere Transport beginnt mit einem genauen Inventar und einer genauen Aufbewahrungskette. Am Lieferort muss das genehmigte Personal des Transportunternehmens Zeuge der Entfernung des manipulationssicheren Versiegelungszeichens und der Entsperrung des Containers sein. Das empfangende Personal inventarisiert die Lieferung und sendet eine Nachricht, die den Empfang der Objekte bestätigt. Microsoft hat auch einen Vertrag mit einem Lieferanten abgeschlossen, um die Vernichtung von Geräten bereitzustellen. Je nach Klassifizierung des Objekts müssen einige Geräte vor Ort zerstört werden.

Der Transport von digitalen Microsoft-Medien außerhalb des sicherheitsgesteuerten Bereichs erfordert die Aufsicht von zwei Teammitgliedern des Rechenzentrumsbetriebs. Die Objekte werden kontinuierlich von autorisiertem Personal begleitet und überwacht, bis sie vernichtet werden.

Das Datacenter Management-Team steuert die Bereitstellung und Entfernung von Komponenten des Informationssystems über Tickets, die im Ticketingtool nachverfolgt werden. Die Bereitstellung und Entfernung von Komponenten des Informationssystems wird von Systembesitzern autorisiert.

## <a name="asset-retention"></a>Aufbewahrung von Ressourcen

Im Besitz von Microsoft befindliche Objekte werden je nach Bedarf basierend auf aufbewahrungsanforderungen aufbewahrt, die von der Unternehmensdatensatzverwaltung, der Klassifizierung von Objekten oder vertraglichen Anforderungen festgelegt werden. Weitere Informationen zur Datenaufbewahrung finden Sie unter [Datenaufbewahrung, Löschung und Vernichtung in Microsoft 365](assurance-data-retention-deletion-and-destruction-overview.md).
