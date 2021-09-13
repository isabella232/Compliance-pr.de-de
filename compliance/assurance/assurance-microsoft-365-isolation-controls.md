---
title: Microsoft 365-Isolierungssteuerungen
description: Informationen zu Isolationssteuerelementen in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 312de9f1417ba6298898d47b2b7e05b5fa7034fe
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159195"
---
# <a name="microsoft-365-isolation-controls"></a>Microsoft 365-Isolierungssteuerungen

Microsoft arbeitet kontinuierlich daran, sicherzustellen, dass die mehrinstanzenfähige Architektur von Microsoft 365 Sicherheit, Vertraulichkeit, Datenschutz, Integrität, lokale, internationale und [Verfügbarkeitsstandards](https://www.microsoft.com/trust-center/compliance/compliance-overview)auf Unternehmensebene unterstützt. Aufgrund des Umfangs und des Umfangs der von Microsoft bereitgestellten Dienste ist es schwierig und nicht unzuverwalten, Microsoft 365 mit erheblichen menschlichen Interaktionen zu verwalten. Microsoft 365 Dienste werden über global verteilte Rechenzentren bereitgestellt, jedes hoch automatisiert mit wenigen Vorgängen, die eine menschliche Berührung erfordern, oder über zugriff auf Kundeninhalte. Unsere Mitarbeiter unterstützen diese Dienste und Rechenzentren mit automatisierten Tools und äußerst sicherem Remotezugriff.

Microsoft 365 besteht aus mehreren Diensten, die wichtige Geschäftsfunktionen bereitstellen und zur gesamten Microsoft 365 Erfahrung beitragen. Jeder dieser Dienste ist eigenständig und für die Integration ineinander konzipiert. Microsoft 365 ist auf die folgenden Prinzipien ausgelegt:

- Dienstorientierte Architektur: Entwerfen und Entwickeln von Software in Form von interoperablen Diensten, die eine gut definierte Geschäftsfunktionalität bereitstellen.
- [Betriebssicherheitssicherheit](https://www.microsoft.com/securityengineering/osa): ein Framework, das das durch verschiedene Funktionen erworbene Wissen einbezieht, die für Microsoft einzigartig sind, einschließlich des Microsoft [Security Development Lifecycle,](https://www.microsoft.com/sdl/default.aspx)des [Microsoft Security Response Centers](https://www.microsoft.com/msrc)und des tiefen Bewusstseins für die Bedrohungslandschaft im Zusammenhang mit der Cybersicherheit.

Microsoft 365 Dienste arbeiten miteinander, sind jedoch so konzipiert und implementiert, dass sie unabhängig voneinander als autonome Dienste bereitgestellt und betrieben werden können. Microsoft trennt Aufgaben und Zuständigkeitsbereiche für Microsoft 365, um Möglichkeiten für nicht autorisierte oder unbeabsichtigte Änderungen oder Missbrauch der Ressourcen der Organisation zu verringern. Microsoft 365 Teams haben Rollen als Teil eines umfassenden rollenbasierten Zugriffssteuerungsmechanismus definiert.

## <a name="tenant-isolation"></a>Mandantenisolierung

Einer der Hauptvorteile von Cloud Computing ist das Konzept einer gemeinsamen, gemeinsamen Infrastruktur für zahlreiche Kunden gleichzeitig, was zu Größenvorteilen führt. Microsoft arbeitet kontinuierlich daran, sicherzustellen, dass die mehrmandantenfähigen Architekturen unserer Clouddienste Sicherheits-, Vertraulichkeits-, Datenschutz-, Integritäts- und Verfügbarkeitsstandards auf Unternehmensebene unterstützen.

Microsoft-Clouddienste wurden mit der Annahme konzipiert, dass alle Mandanten potenziell ungern gegenüber allen anderen Mandanten sind, und wir haben Sicherheitsmaßnahmen implementiert, um zu verhindern, dass die Aktionen eines Mandanten die Sicherheit oder den Dienst eines anderen Mandanten beeinträchtigen oder auf den Inhalt eines anderen Mandanten zugreifen.

Die beiden Hauptziele der Aufrechterhaltung der Mandantenisolation in einer mehrinstanzenfähigen Umgebung sind:

- Verhindern von Lecks oder nicht autorisiertem Zugriff auf Kundeninhalte über Mandanten hinweg; Und
- Verhindern, dass sich aktionen eines Mandanten negativ auf den Dienst für einen anderen Mandanten auswirken

In Microsoft 365 wurden mehrere Schutzformen implementiert, um zu verhindern, dass Kunden Microsoft 365 Dienste oder Anwendungen gefährden oder nicht autorisierten Zugriff auf die Informationen anderer Mandanten oder des Microsoft 365 Systems selbst erhalten, einschließlich:

- Die logische Isolierung von Kundeninhalten innerhalb jedes Mandanten für Microsoft 365 Dienste wird durch Azure Active Directory Autorisierung und rollenbasierte Zugriffssteuerung erreicht.
- SharePoint Online bietet Datenisolationsmechanismen auf Speicherebene.
- Microsoft verwendet strenge physische Sicherheit, Hintergrundprüfung und eine mehrstufige Verschlüsselungsstrategie, um die Vertraulichkeit und Integrität von Kundeninhalten zu schützen. Alle Microsoft 365 Rechenzentren verfügen über biometrische Zugriffssteuerungen, wobei die meisten Handflächendrucke benötigen, um physischen Zugriff zu erhalten. Darüber hinaus müssen alle IN den USA ansässigen Microsoft-Mitarbeiter im Rahmen des Einstellungsprozesses eine Standard-Hintergrundüberprüfung erfolgreich abschließen. Weitere Informationen zu den Steuerelementen, die für den administrativen Zugriff in Microsoft 365 verwendet werden, finden Sie unter [Microsoft 365 Kontoverwaltung.](assurance-microsoft-365-account-management.md)
- Microsoft 365 verwendet dienstseitige Technologien, die Ruhe- und Übertragungsdaten von Kundeninhalten verschlüsseln, einschließlich BitLocker, Dateiverschlüsselung, TLS (Transport Layer Security) und Internet Protocol Security (IPsec). Ausführliche Informationen zur Verschlüsselung in Microsoft 365 finden Sie unter ["Datenverschlüsselungstechnologien" in Microsoft 365.](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)

Zusammen bieten die oben aufgeführten Schutzmaßnahmen robuste logische Isolationskontrollen, die Bedrohungsschutz und Risikominderung bieten, die dem durch physische Isolation allein bereitgestellten entsprechen.

## <a name="resources"></a>Ressourcen

- [Isolation und Zugriffssteuerung in Azure Active Directory](/microsoft-365/enterprise/microsoft-365-isolation-in-azure-active-directory)
- [Überwachen und Testen von Mandantengrenzen](assurance-monitoring-and-testing.md)
- [Isolation und Zugriffssteuerung in Microsoft 365](/microsoft-365/enterprise/microsoft-365-isolation-in-microsoft-365)
