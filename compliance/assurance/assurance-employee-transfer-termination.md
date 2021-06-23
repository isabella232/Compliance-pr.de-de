---
title: Versetzung und Beendigung von Microsoft-Mitarbeitern
description: Erfahren Sie mehr über den Transfer- und Beendigungsprozess von Microsoft-Mitarbeitern in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: b31dd13f4a6209712a9cc212ab3bcd9c5addf6b7
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089625"
---
# <a name="microsoft-employee-transfer-and-termination"></a>Versetzung und Beendigung von Microsoft-Mitarbeitern

Mitarbeiterübertragungen und Kündigungen sind Teil des normalen Geschäftsbetriebs jedes Unternehmens. Wenn ein Mitarbeiter seine Position ändert oder das Unternehmen verlässt, ist es wichtig, unangemessenen Zugriff zeitnah zu widerrufen. Um effiziente Zugriffsänderungen und Zugriffssperrungen zu ermöglichen, verwendet Microsoft 365 standardisierte Verfahren und automatisierte Prozesse, um das Personalinformationssystem (HRIS) mit dem Identity Management (IDM)-System zu koordinieren. Die automatische Orchestrierung zwischen diesen beiden Systemen ist für die Aufrechterhaltung der betriebsbereiten Konsistenz, den Schutz der Dienste und Daten Microsoft 365, die Verhinderung von Rechteerweiterungen und die Verringerung von Risiken im Zusammenhang mit Insiderbedrohungen unerlässlich.

Microsoft 365 Systeme sind für den Betrieb ohne ständigen administrativen Zugriff auf Produktionsumgebungen für unsere Techniker konzipiert. Microsoft verwendet ein Just-In-Time (JIT), Just-Enough-Access (JEA)-Modell, um Technikern den temporären Zugriff bereitzustellen, der erforderlich ist, um ihren Dienst bei Bedarf zu unterstützen. Um ein Serviceteamkonto für JIT-Zugriff anzufordern und zu verwenden, müssen Techniker Berechtigungen über das IDM-Tool anfordern und verwalten. Wenn Mitarbeiter übertragen oder beendet werden, werden ihr Serviceteamkonto und die zugehörigen Berechtigungen automatisch geändert, um unangemessenen Zugriff zu verhindern.

## <a name="transfer-and-reassignment"></a>Übertragung und Neuzuweisung

Mitarbeiterübertragungen werden durch eine Übertragungstransaktionsanforderung durch den Vorgesetzten des Mitarbeiters initiiert. Der Manager erstellt eine Anforderung und setzt sich für den Angebotsschreibenprozess mit global talent acquisition ein. Sobald der Mitarbeiter das Angebot für die neue Rolle annimmt, schließt der Personaldienst die Übertragung in den HR-Kerntools ab, wodurch IDM ein Ablaufdatum für alle Berechtigungen des Mitarbeiters festlegen kann. Der Mitarbeiter muss eine Anforderung übermitteln und die Genehmigung des neuen Vorgesetzten erhalten, um seine Berechtigung beizubehalten. Wenn Sie keine Anforderung übermitteln oder die Genehmigung durch den Vorgesetzten erhalten, führt dies zur Sperrung der Berechtigungsberechtigungen des übertragenen Mitarbeiters. Bei Übertragungen mit bestimmten Sicherheitsauswirkungen werden Systemzugriffe und Sicherheitsgruppenmitgliedschaften sofort neu ausgewertet, um ihre neue Rolle widerzuspiegeln.

## <a name="termination"></a>Abschluss

Microsoft verwendet eindeutig definierte Richtlinien und Verfahren, um den physischen und logischen Zugriff auf Microsoft-Systeme und -Ressourcen unverzüglich zu widerrufen, wenn ein Mitarbeiter gekündigt wird. Wenn ein Mitarbeiter seine Benachrichtigung gibt, gibt der Vorgesetzte des Mitarbeiters das Kündigungsdatum in die HRIS ein. Nach dem letzten Arbeitstag des Mitarbeiters kennzeichnet der HRIS den Mitarbeiter als gekündigt und gibt die Informationen an IDM weiter, wodurch alle Serviceteamkonten und Berechtigungen automatisch entfernt werden.

Bei unfreiwilligen Kündigungen arbeitet HR mit dem Vorgesetzten des Mitarbeiters zusammen, um die entsprechenden Schritte zum Beenden und Offboarden des Mitarbeiters auszuführen. Ähnlich wie bei einer freiwilligen Beendigung werden die Beendigungsinformationen zusammen mit allen erforderlichen Schritten wie der Koordinierung des effektiven Datums und der Entfernung des Zugriffs in das HRIS eingegeben. und alle anderen Schritte im Zusammenhang mit dem Übergang von der Rolle.
