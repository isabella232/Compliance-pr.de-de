---
title: Technologiesteuerelemente in Microsoft 365
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
ms.openlocfilehash: c3b443505c78832af47719e6840c8b7011f9dfe1
ms.sourcegitcommit: 2b347c9b778ac9b6450daf20fdf8eb74ed14cbbd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/23/2021
ms.locfileid: "51002165"
---
# <a name="technology-controls-in-microsoft-365"></a>Technologiesteuerelemente in Microsoft 365 

Microsoft verwendet mehrere Tools und Technologien, um den Zugriff auf Kundendaten in seinen Onlinediensten zu steuern, zu verwalten und zu überwachen. Diese gelten für Exchange Online, SharePoint Online, Lockbox und Customer Lockbox, mehrstufige Authentifizierung und vieles mehr. Yammer verwendet ähnliche Steuerelemente, die in Yammer [Enterprise Access Controls beschrieben werden.](assurance-yammer-enterprise-access-controls.md)

Microsoft 365-Techniker haben keinen ständigen Zugriff auf Microsoft 365-Kundendaten. Techniker müssen einen Microsoft-Genehmigungsprozess durchgehen, bevor der Zugriff auf Kundendaten für Dienstvorgänge erfolgt. Wenn der Kunde das Feature Customer Lockbox für Exchange Online und SharePoint Online lizenziert, erfordert der Zugriff auf Kundendaten die Kundengenehmigung. Nach der Genehmigung werden dienstspezifische Administratorkonten just-in-time-Zugriff für Aufgaben bereitgestellt, die für die Dienstanforderung erforderlich sind.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox und Customer Lockbox

Obwohl selten, könnte ein Kunde Unterstützung von Microsoft anfordern, die Kundeninhalte für einen Microsoft-Techniker verfügbar macht. Zum Steuern des Zugriffs auf Exchange Online verwendet Microsoft das Zugriffssteuerungssystem Lockbox. Bevor ein Microsoft-Techniker auf Exchange Online- oder SharePoint Online-Systeme oder -Daten zutritt, muss er eine Zugriffsanforderung mithilfe von Lockbox übermitteln. Alle Dienstanforderungen für Exchange Online und SharePoint Online werden vom Lockbox-System verarbeitet. Bei Lockbox und Customer Lockbox ist der genehmigte Zugriff auf einen eindeutigen Benutzer nachverfolgt, wodurch Techniker für den Umgang mit Kundendaten rechenschaftsbar sind.

> [!NOTE]
> Exchange Online enthält alle Skype for Business-Daten, die in Benutzerpostfächern gespeichert sind. Die Skype for Business-Abdeckung umfasst keine Skype Meeting Broadcast-Aufzeichnungen oder Inhalte, die von Benutzern in Besprechungen hochgeladen wurden. SharePoint Online umfasst OneDrive for Business.

Lockbox verarbeitet Anforderungen nach Berechtigungen, die Technikern die Möglichkeit geben, betriebs- und verwaltungstechnische Funktionen innerhalb des Diensts durchzuführen. Techniker übermitteln Anforderungen über Lockbox, und ein Microsoft-Manager muss die Anforderung genehmigen, bevor der Techniker auf Kundendaten zugreifen kann. Nach der Genehmigung durch den Vorgesetzten hat der Techniker zeitlich begrenzten und eingeschränkten Zugriff auf Kundendaten, um an dem Problem des Kunden zu arbeiten.

Kunden-Lockbox für Microsoft 365 hilft Ihnen bei der Erfüllung von Complianceverpflichtungen, wenn Sie Verfahren für die explizite Autorisierung des Datenzugriffs benötigen. Dies ist eine Anforderung für einige Compliancestandards, z. B. FedRAMP und HIPAA. Customer Lockbox fügt Sie in den Genehmigungsprozess von Lockbox ein und bietet Ihnen die Möglichkeit, die Autorisierung des Microsoft-Zugriffs auf Ihre Exchange Online- oder SharePoint Online-Inhalte für Dienstvorgänge zu steuern.

In der seltenen Instanz, in der ein Microsoft-Servicetechniker Zugriff auf Ihre Daten benötigt, gewähren Sie nur Zugriff auf Daten, die zum Beheben des Problems und für einen begrenzten Zeitraum erforderlich sind. Wenn Sie eine Zugriffsanforderung ablehnen, haben Die Microsoft-Techniker keinen Zugriff auf Ihre Inhalte und können keine Dienstvorgänge abschließen. Wenn Sie die Anforderung genehmigen, haben die Microsoft-Techniker begrenzten Just-in-Time-Zugriff auf Ihre Inhalte über die überwachten und eingeschränkten Verwaltungsschnittstellen.

Vom Supporttechniker durchgeführte Aktionen werden zu Überwachungszwecken protokolliert und können über die [Office 365-Verwaltungsaktivitäts-API](/office/office-365-management-api/get-started-with-office-365-management-apis) und das [Security and Compliance Center zugegriffen werden.](https://protection.office.com/)

>[!NOTE]
> Customer Lockbox ist in [Microsoft 365 E5 als](https://products.office.com/business/office-365-enterprise-e5-business-software) Add-On-Kauf verfügbar. Weitere Informationen finden Sie unter [Microsoft 365 Customer Lockbox Requests](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2).

## <a name="just-in-time-access"></a>Just-in-Time-Zugriff

Microsoft verwendet das Just-in-Time(JIT)-Zugriffsprinzip für Microsoft 365, um Risiken der Manipulation von Anmeldeinformationen und laterale Angriffe zu mindern. JIT entfernt den dauerhaften Administratorzugriff auf Dienste und ersetzt Berechtigungen durch die Möglichkeit, diese Rollen bei Bedarf zu erhöhen. Durch das Entfernen von Beständigen Zugriffsrechten von Administratoren wird sichergestellt, dass Anmeldeinformationen nur verfügbar sind, wenn sie benötigt werden, und die Risiken für den Diebstahl von Anmeldeinformationen werden verringert.

Das JIT-Zugriffsmodell erfordert, dass Techniker für einen begrenzten Zeitraum erhöhte Rechte anfordern, um Administrative Aufgaben ausführen zu können. Darüber hinaus verwenden Techniker temporäre Konten, die mit vom Computer generierten komplexen Kennwörtern erstellt wurden, und gewährten nur die Rollen, mit denen sie die erforderlichen Aufgaben ausführen können. Beispielsweise ist der von Lockbox gewährte Administratorzugriff zeitgebunden, und der gewährte Zeitzugriff hängt von der angeforderten Rolle ab. Ein Techniker gibt die Dauer des Zeitzugriffs an, der in der Anforderung an das Lockbox-System benötigt wird. Das Lockbox-System lehnt Anforderungen ab, wenn die angeforderte Zeit die maximal zulässige Zeit für die Erhöhung überschreitet. Nach Ablauf wird der Administratorzugriff entfernt, und das temporäre Konto läuft ab.

Wenn die Techniker für den Zugriff autorisiert und genehmigt werden, erhalten sie ein einmal vom Autorisierungssystem generiertes Administratorkennwort. Jedes Mal, wenn eine Anforderung für erhöhten Zugriff genehmigt wird, werden neue Kennwörter generiert. Das Kennwort wird in einen Kennwortschutz kopiert, ist von den Anmeldeinformationen des Technikers für die Microsoft-Unternehmensumgebung getrennt und nur für die genehmigte Sitzung mit erhöhten Zugriffen gut.

## <a name="constrained-management-interfaces"></a>Eingeschränkte Verwaltungsschnittstellen

Techniker verwenden zwei Verwaltungsschnittstellen, um administrative Aufgaben auszuführen: Remotedesktop über gesicherte Terminaldienstgateways (TSGs) und Remote PowerShell. Innerhalb dieser Verwaltungsschnittstellen gelten für Softwarerichtlinien und Zugriffssteuerungen erhebliche Einschränkungen, welche Anwendungen ausgeführt werden und welche Befehle und Cmdlets verfügbar sind.

Microsoft 365-Server beschränken gleichzeitige Sitzungen auf eine Sitzung pro Dienstteamadministrator pro Server. TSGs erlauben benutzern nur eine einzige gleichzeitige Sitzung und nicht mehrere Sitzungen. Mithilfe einer einzelnen Sitzung pro Server können Microsoft 365-Dienstteamadministratoren gleichzeitig eine Verbindung mit mehreren Servern herstellen, damit Administratoren ihre Aufgaben effektiv ausführen können. Dienstteamadministratoren verfügen nicht über Berechtigungen für die TSGs selbst. Die TSG wird nur verwendet, um mehrstufige Authentifizierungs- und Verschlüsselungsanforderungen zu erzwingen. Sobald sich der Dienstteamadministrator über eine TSG mit einem bestimmten Server verbindet, erzwingt der spezifische Server eine Sitzungsbeschränkung von 1 pro Administrator.

Verwendungseinschränkungen sowie Verbindungs- und Konfigurationsanforderungen für Microsoft 365-Mitarbeiter werden durch Active Directory-Gruppenrichtlinien festgelegt. Diese Richtlinien umfassen die folgenden Merkmale:

- TSGs verwenden nur [die fips](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2-validierte Verschlüsselung.
- TsG-Sitzungen trennen sich nach 30 Minuten Inaktivität.
- TSG-Sitzungen melden sich nach 24 Stunden automatisch ab.

Verbindungen mit TSGs erfordern auch MFA mithilfe einer separaten physischen Smartcard und eines Kontos, das von den Microsoft-Unternehmensanmeldeinformationen des Technikers getrennt ist. Techniker erhalten unterschiedliche Smartcards für verschiedene Plattformen, und geheime Verwaltungsplattformen stellen die sichere Speicherung von Anmeldeinformationen sicher. TSGs verwenden Active Directory-Gruppenrichtlinien, um zu steuern, wer sich bei Remoteservern anmelden kann, wie viele zugelassene Sitzungen und Timeouteinstellungen im Leerlauf vorhanden sind. Zusätzliche Richtlinien beschränken den Zugriff auf zulässige Anwendungen und den Internetzugriff.

Zusätzlich zum Remotezugriff mit speziell konfigurierten TSGs ermöglicht Exchange Online Benutzern mit der Rolle Service Engineer Operations den Zugriff auf bestimmte Verwaltungsfunktionen auf Produktionsservern mithilfe von Remote PowerShell. Dazu muss der Benutzer für den schreibgeschützten Zugriff (Debuggen) auf die Microsoft 365-Produktionsumgebung autorisiert sein. Die Berechtigungseskalation ist auf die gleiche Weise aktiviert, wie sie für TSGs mithilfe des Lockbox-Prozesses aktiviert ist.

Für den Remotezugriff verfügt jedes Datencenter über eine virtuelle IP mit Lastenausgleich, die als einzelner Zugriffspunkt dient. Die verfügbaren Remote-PowerShell-Cmdlets basieren auf der Berechtigungsstufe, die in dem während der Authentifizierung erhaltenen Zugriffsanspruch identifiziert wurde. Diese Cmdlets stellen die einzige administrative Funktionalität bereit, auf die Benutzer über diese Methode eine Verbindung herstellen können. Remote PowerShell beschränkt den Umfang der Befehle, die dem Techniker zur Verfügung stehen, und basiert auf der Über den Lockbox-Prozess gewährten Zugriffsebene. In Exchange Online ist z. B. Get-Mailbox verfügbar, aber Set-Mailbox nicht.
