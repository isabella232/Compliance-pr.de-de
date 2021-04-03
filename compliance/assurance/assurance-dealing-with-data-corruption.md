---
title: Microsoft 365 Umgang mit Datenbeschädigung
description: In diesem Artikel werden die Datenbeschädigung in Microsoft 365 und die Von Microsoft unternommenen Anstrengungen zur Verhinderung und Wiederherstellung von Daten erläutert.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497596"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a>Umgang mit Datenbeschädigung in Microsoft 365

Einer der anspruchsvollen Aspekte bei der Ausführung eines großen Clouddiensts ist die Verarbeitung von Datenbeschädigungen angesichts der großen Datenmenge und unabhängiger Systeme. Datenbeschädigungen können durch:

- Anwendungs- oder Infrastrukturfehler, die den Anwendungsstatus teilweise oder ganz beschädigen
- Hardwareprobleme, die zu datenverlusten oder zu Unfähigkeit zum Lesen von Daten führen
- Menschliche Betriebsfehler
- Böswillige Hacker und verärgerte Mitarbeiter
- Vorfälle in externen Diensten, die zu datenverlusten führen

Da eine höhere Ausfallsicherheit bei der Datenintegrität weniger Datenbeschädigungsvorfälle bedeutet, hat Microsoft in Microsoft 365-Schutzmechanismen integrierte, um zu verhindern, dass Beschädigungen entstehen, sowie Systeme und Prozesse, mit denen wir daten wiederherstellen können, falls dies der Fall ist. Prüfungen und Prozesse sind in den verschiedenen Phasen des Technischen Veröffentlichungsprozesses vorhanden, um die Ausfallsicherheit gegen Datenbeschädigungen zu erhöhen, einschließlich:

- Systemdesign
- Codeorganisation und -struktur
- Codeüberprüfung
- Komponententests, Integrationstests und Systemtests
- Trip-Leitungen-Tests/-Gates

In Microsoft 365-Produktionsumgebungen stellt die Peerreplikation zwischen Rechenzentren sicher, dass immer mehrere Livekopien aller Daten verfügbar sind. Standardbilder und Skripts werden verwendet, um verlorene Server wiederherzustellen, und replizierte Daten werden zum Wiederherstellen von Kundendaten verwendet. Aufgrund der integrierten Überprüfungen und Prozesse der Datenresilienz verwaltet Microsoft nur Sicherungen der Dokumentation des Microsoft 365-Informationssystems (einschließlich sicherheitsbezogener Dokumentation) mithilfe der integrierten Replikation in SharePoint Online und unseres internen Coderepositorytools Source Depot. Die Systemdokumentation wird in SharePoint Online gespeichert, und Source Depot enthält System- und Anwendungsabbilder. Sowohl SharePoint Online als auch Source Depot verwenden die Versionsverwaltung und werden nahezu in Echtzeit repliziert.
