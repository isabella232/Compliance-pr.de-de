---
title: Microsoft 365 Umgang mit Datenbeschädigung
description: In diesem Artikel werden die Datenbeschädigung in Microsoft 365 und die Anstrengungen von Microsoft zum Verhindern und Wiederherstellen von Daten erläutert.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 860a150760e080df4a577d73478a75ac94b8700b
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482078"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a>Umgang mit Datenbeschädigungen in Microsoft 365

Einer der schwierigen Aspekte beim Ausführen eines großen Clouddiensts ist die Behandlung von Datenbeschädigungen, angesichts der großen Menge an Daten und unabhängigen Systemen. Datenbeschädigungen können durch Folgendes verursacht werden:

- Anwendungs- oder Infrastrukturfehler, wodurch der Anwendungsstatus teilweise oder vollständig beschädigt wird
- Hardwareprobleme, die zu datenverlusten oder unfähigkeit zum Lesen von Daten führen
- Menschliche Betriebsfehler
- Böswillige Hacker und verärgerte Mitarbeiter
- Vorfälle in externen Diensten, die zu datenverlusten führen

Da eine höhere Resilienz in der Datenintegrität weniger Datenbeschädigungsvorfälle bedeutet, hat Microsoft Microsoft 365 Schutzmechanismen integriert, um zu verhindern, dass eine Beschädigung erfolgt, sowie Systeme und Prozesse, die es uns ermöglichen, Daten wiederherzustellen, wenn dies der Fall ist. Überprüfungen und Prozesse sind innerhalb der verschiedenen Phasen des Engineering-Veröffentlichungsprozesses vorhanden, um die Resilienz gegenüber Datenbeschädigung zu erhöhen, einschließlich:

- Systemdesign
- Codeorganisation und -struktur
- Codeüberprüfung
- Komponententests, Integrationstests und Systemtests
- Trip wires tests/gate

Innerhalb Microsoft 365 Produktionsumgebungen stellt die Peerreplikation zwischen Rechenzentren sicher, dass immer mehrere Livekopien von Daten vorhanden sind. Standardimages und Skripts werden verwendet, um verloren gegangene Server wiederherzustellen, und replizierte Daten werden verwendet, um Kundendaten wiederherzustellen. Aufgrund der integrierten Überprüfungen und Prozesse zur Datenresilienz verwaltet Microsoft Sicherungen nur von Microsoft 365 Dokumentation des Informationssystems (einschließlich sicherheitsrelevanter Dokumentation) mithilfe der integrierten Replikation in SharePoint Online und unserem internen Coderepository-Tool Source Depot. Die Systemdokumentation wird in SharePoint Online gespeichert, und das Quelldepot enthält System- und Anwendungsimages. Sowohl SharePoint Online- als auch das Quelldepot verwenden Versionsverwaltung und werden nahezu in Echtzeit repliziert.
