---
title: 'Technologiesteuerelemente in Microsoft 365 '
description: Dieser Artikel bietet eine Übersicht über die Tools und Technologien, die von Microsoft für die Technologiesteuerung in Microsoft 365 verwendet werden.
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
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 2c02e1739f6d3b5981e4327139477a12f987ed68
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120734"
---
# <a name="technology-controls-in-microsoft-365"></a>Technologiesteuerelemente in Microsoft 365 

Microsoft verwendet mehrere Tools und Technologien, um den Zugriff auf Kundendaten in seinen Onlinediensten zu steuern, zu verwalten und zu überwachen. Diese gelten für Exchange Online, SharePoint Online, Lockbox und Kunden-Lockbox, mehrstufige Authentifizierung und vieles mehr. Yammer verwendet ähnliche Steuerelemente, die in Yammer [Enterprise Access Controls beschrieben werden.](assurance-yammer-enterprise-access-controls.md)

Microsoft 365-Techniker haben keinen ständigen Zugriff auf Microsoft 365-Kundendaten. Techniker müssen einen Genehmigungsprozess von Microsoft durcharbeiten, bevor der Zugriff auf Kundendaten für Dienstvorgänge erfolgt. Wenn der Kunde die Kunden-Lockbox-Funktion für Exchange Online und SharePoint Online lizenziert, ist für den Zugriff auf Kundendaten eine Kundengenehmigung erforderlich. Nach der Genehmigung werden dienstspezifische Administratorkonten just-in-time-Zugriff für Aufgaben bereitgestellt, die für die Serviceanfrage erforderlich sind.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox und Kunden-Lockbox

Auch wenn dies selten der Fall ist, könnte ein Kunde Unterstützung von Microsoft anfordern, die Kundeninhalte einem Microsoft-Techniker zur Verfügung stellt. Um den Zugriff auf Exchange Online zu steuern, verwendet Microsoft ein Zugriffssteuerungssystem namens Lockbox. Bevor ein Microsoft-Techniker auf Exchange Online- oder SharePoint Online-Systeme oder -Daten zutritt, muss er eine Zugriffsanforderung mithilfe von Lockbox übermitteln. Alle Dienstanforderungen für Exchange Online und SharePoint Online werden vom Lockboxsystem verarbeitet. Bei Lockbox und Customer Lockbox kann der genehmigte Zugriff auf einen eindeutigen Benutzer nachverfolgt werden, wodurch Techniker für die Verarbeitung von Kundendaten zur Rechenschaft gezogen werden.

> [!NOTE]
> Exchange Online enthält alle Skype for Business-Daten, die in Benutzerpostfächern gespeichert sind. Skype for Business umfasst keine Skype Meeting Broadcast-Aufzeichnungen oder Inhalte, die von Benutzern in Besprechungen hochgeladen wurden. SharePoint Online umfasst OneDrive for Business.

Lockbox verarbeitet Anforderungen für Berechtigungen, die Technikern die Möglichkeit geben, betriebs- und verwaltungstechnische Funktionen innerhalb des Diensts durchzuführen. Techniker übermitteln Anfragen über Lockbox, und ein Microsoft Manager muss die Anforderung genehmigen, bevor der Techniker auf Kundendaten zugreifen kann. Nach der Genehmigung durch den Vorgesetzten hat der Techniker zeitlich begrenzten und eingeschränkten Zugriff auf Kundendaten, um am Problem des Kunden zu arbeiten.

Die Kunden-Lockbox für Microsoft 365 hilft Ihnen bei der Einhaltung von Complianceverpflichtungen, wenn Sie Verfahren für die explizite Autorisierung des Datenzugriffs benötigen. Dies ist eine Anforderung für einige Compliancestandards, z. B. FedRAMP und HIPAA. Die Kunden-Lockbox fügt Sie in den Genehmigungsprozess der Lockbox ein und bietet Ihnen die Möglichkeit, die Autorisierung des Microsoft-Zugriffs auf Ihre Exchange Online- oder SharePoint Online-Inhalte für Dienstvorgänge zu steuern.

In der seltenen Situation, in der ein Microsoft-Servicetechniker Zugriff auf Ihre Daten benötigt, gewähren Sie nur Zugriff auf Daten, die zum Beheben des Problems und für einen begrenzten Zeitraum erforderlich sind. Wenn Sie eine Zugriffsanforderung ablehnen, haben die Microsoft Techniker keinen Zugriff auf Ihre Inhalte und können keine Dienstvorgänge abschließen. Wenn Sie die Anforderung genehmigen, haben die Microsoft-Techniker begrenzten Just-in-Time-Zugriff auf Ihre Inhalte über die überwachten und eingeschränkten Verwaltungsschnittstellen.

Vom Supporttechniker durchgeführte Aktionen werden zu Überwachungszwecken protokolliert und können über die [Office 365-Verwaltungsaktivitäts-API](/office/office-365-management-api/get-started-with-office-365-management-apis) und das [Security and Compliance Center verwendet werden.](https://protection.office.com/)

>[!NOTE]
> Die Kunden-Lockbox ist in [Microsoft 365 E5 als](https://products.office.com/business/office-365-enterprise-e5-business-software) Add-On-Kauf verfügbar. Weitere Informationen finden Sie unter [Microsoft 365 Customer Lockbox Requests](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2).

## <a name="just-in-time-access"></a>Just-in-Time-Zugriff

Microsoft verwendet das Just-in-Time-Zugriffsprinzip (JIT) für Microsoft 365, um Risiken der Manipulation von Anmeldeinformationen und laterale Angriffe zu mindern. JIT entfernt den dauerhaften Administrativen Zugriff auf Dienste und ersetzt Berechtigungen durch die Möglichkeit, bei Bedarf auf diese Rollen zu erhöhen. Durch das Entfernen dauerhafter Zugriffsrechte von Administratoren wird sichergestellt, dass Anmeldeinformationen nur verfügbar sind, wenn sie benötigt werden, und die Risiken beim Diebstahl von Anmeldeinformationen werden reduziert.

Das Jit-Zugriffsmodell erfordert, dass Techniker erhöhte Rechte für einen begrenzten Zeitraum anfordern, um administrative Aufgaben ausführen zu können. Darüber hinaus verwenden Techniker temporäre Konten, die mit vom Computer generierten komplexen Kennwörtern erstellt wurden, und erteilten nur die Rollen, mit denen sie die erforderlichen Aufgaben ausführen können. Beispielsweise ist der von Lockbox gewährte Administratorzugriff zeitgebunden, und die gewährte Zeit hängt von der angeforderten Rolle ab. Ein Techniker gibt die Dauer des Zeitzugriffs an, der in der Anforderung an das Lockboxsystem erforderlich ist. Das Lockboxsystem lehnt Anforderungen ab, wenn die angeforderte Zeit die maximal zulässige Zeit für die Rechteerweiterung überschreitet. Nach Ablauf wird der Administratorzugriff entfernt, und das temporäre Konto läuft ab.

Wenn die Techniker für den Zugriff autorisiert und genehmigt wurden, erhalten sie ein einmal vom Autorisierungssystem generiertes Administratorkennwort. Jedes Mal, wenn eine Anforderung für erhöhten Zugriff genehmigt wird, werden neue Kennwörter generiert. Das Kennwort wird in ein kennwortsicheres Kennwort kopiert, ist von den Anmeldeinformationen des Technikers für die Microsoft-Unternehmensumgebung getrennt und nur für die genehmigte Sitzung mit erhöhten Zugriffsberechtigungen gut.

## <a name="constrained-management-interfaces"></a>Eingeschränkte Verwaltungsschnittstellen

Techniker verwenden zwei Verwaltungsschnittstellen, um Verwaltungsaufgaben auszuführen: Remotedesktop über gesicherte Terminaldienstgateways (TSGs) und Remote PowerShell. Innerhalb dieser Verwaltungsschnittstellen gelten für Softwarerichtlinien und Zugriffssteuerungen erhebliche Einschränkungen hinsichtlich der ausgeführten Anwendungen und der verfügbaren Befehle und Cmdlets.

Microsoft 365-Server schränken gleichzeitige Sitzungen auf eine Sitzung pro Teamadministrator pro Server ein. TSGs erlauben benutzern nur eine einzige gleichzeitige Sitzung und nicht mehrere Sitzungen. Mithilfe einer einzelnen Sitzung pro Server können Microsoft 365-Serviceteamadministratoren gleichzeitig eine Verbindung mit mehreren Servern herstellen, damit Administratoren ihre Aufgaben effektiv ausführen können. Dienstteamadministratoren verfügen nicht über Berechtigungen für die TSGs selbst. Die TSG wird nur verwendet, um mehrstufige Authentifizierung (Multi-Factor Authentication, MFA) und Verschlüsselungsanforderungen zu erzwingen. Sobald der Dienstteamadministrator über eine TSG eine Verbindung mit einem bestimmten Server herstellt, erzwingt der serverspezifische Server eine Sitzungsbeschränkung von 1 pro Administrator.

Nutzungseinschränkungen sowie Verbindungs- und Konfigurationsanforderungen für Microsoft 365-Mitarbeiter werden durch Active Directory-Gruppenrichtlinien festgelegt. Diese Richtlinien umfassen die folgenden Merkmale:

- TSGs verwenden nur [FIPS](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2-validierte Verschlüsselung.
- TsG-Sitzungen werden nach 30 Minuten Inaktivität getrennt.
- TsG-Sitzungen melden sich automatisch nach 24 Stunden ab.

Verbindungen mit TSGs erfordern auch MFA mithilfe einer separaten physischen Smartcard und eines Kontos, das von den Microsoft-Unternehmensanmeldeinformationen des Technikers getrennt ist. Techniker erhalten unterschiedliche Smartcards für verschiedene Plattformen, und Geheime Verwaltungsplattformen stellen die sichere Speicherung von Anmeldeinformationen sicher. TSGs verwenden Active Directory-Gruppenrichtlinien, um zu steuern, wer sich bei Remoteservern anmelden kann, wie viele zugelassene Sitzungen zulässig sind und welche Timeouteinstellungen im Leerlauf sind. Zusätzliche Richtlinien beschränken den Zugriff auf zulässige Anwendungen und beschränken den Internetzugriff.

Zusätzlich zum Remotezugriff mithilfe speziell konfigurierter TSGs ermöglicht Exchange Online Benutzern mit der Rolle "Diensttechniker-Vorgänge" den Zugriff auf bestimmte Verwaltungsfunktionen auf Produktionsservern mithilfe von Remote PowerShell. Dazu muss der Benutzer für den schreibgeschützten Zugriff (Debuggen) auf die Microsoft 365-Produktionsumgebung autorisiert sein. Die Berechtigungseskalation ist auf die gleiche Weise aktiviert wie die Aktivierung für TSGs mithilfe des Lockbox-Prozesses.

Für den Remotezugriff verfügt jedes Rechenzentrum über eine virtuelle IP mit Lastenausgleich, die als einzelner Zugriffspunkt dient. Die verfügbaren Remote-PowerShell-Cmdlets basieren auf der Berechtigungsstufe, die in dem während der Authentifizierung erhaltenen Zugriffsanspruch identifiziert wird. Diese Cmdlets bieten die einzige Verwaltungsfunktionalität, auf die Benutzer über diese Methode zugriffen können. Remote PowerShell beschränkt den Umfang der Befehle, die dem Techniker zur Verfügung stehen, und basiert auf der Zugriffsebene, die über den Lockbox-Prozess gewährt wird. In Exchange Online ist beispielsweise Get-Mailbox verfügbar, aber Set-Mailbox nicht.
