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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 1317d8507156ee7752c3eca96e3cf0e9813a5784
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573883"
---
# <a name="technology-controls-in-microsoft-365"></a>Technologiesteuerelemente in Microsoft 365 

Microsoft verwendet mehrere Tools und Technologien, um den Zugriff auf Kundendaten in seinen Onlinediensten zu steuern, zu verwalten und zu überwachen. Diese gelten für Exchange Online, SharePoint Online, Lockbox und Kunden-Lockbox, mehrstufige Authentifizierung und vieles mehr. Yammer ähnliche Steuerelemente verwendet, die in Yammer Enterprise Access Controls beschrieben [sind.](assurance-yammer-enterprise-access-controls.md)

Microsoft 365 Techniker haben keinen ständigen Zugriff auf Microsoft 365 Kundendaten. Techniker müssen einen Microsoft-Genehmigungsprozess durchlaufen, bevor der Zugriff auf Kundendaten für Servicevorgänge erfolgt. Wenn der Kunde die Kunden-Lockbox-Funktion für Exchange Online und SharePoint Online lizenziert, erfordert der Zugriff auf Kundendaten eine Genehmigung durch den Kunden. Nach der Genehmigung werden dienstspezifische Administratorkonten just-in-time-Zugriff für Aufgaben bereitgestellt, die für die Serviceanfrage erforderlich sind.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox und Kunden-Lockbox

Obwohl selten, könnte ein Kunde Unterstützung von Microsoft anfordern, die Kundeninhalte für einen Microsoft-Techniker verfügbar macht. Um den Zugriff auf Exchange Online zu steuern, verwendet Microsoft ein Zugriffssteuerungssystem namens Lockbox. Bevor ein Microsoft-Techniker auf Exchange Online oder SharePoint Onlinesysteme oder -Daten zugreift, muss er eine Zugriffsanforderung mithilfe von Lockbox senden. Alle Dienstanforderungen für Exchange Online und SharePoint Online werden vom Lockbox-System verarbeitet. Mit Lockbox und Kunden-Lockbox kann der gesamte genehmigte Zugriff für einen eindeutigen Benutzer nachverfolgt werden, sodass Techniker für ihre Verarbeitung von Kundendaten verantwortlich sind.

> [!NOTE]
> Exchange Online enthält alle Skype for Business Daten, die in Benutzerpostfächern gespeichert sind. Skype for Business Abdeckung umfasst nicht Skype-Besprechung Aufzeichnungen oder Inhalte, die von Benutzern in Besprechungen hochgeladen wurden. SharePoint Online umfasst OneDrive for Business.

Lockbox verarbeitet Anforderungen für Berechtigungen, die Technikern die Möglichkeit geben, operative und administrative Funktionen innerhalb des Diensts auszuführen. Techniker übermitteln Anforderungen über Lockbox, und ein Microsoft-Manager muss die Anforderung genehmigen, bevor der Techniker auf Kundendaten zugreifen kann. Nach der Genehmigung durch den Vorgesetzten hat der Techniker zeitlich begrenzten und eingeschränkten Zugriff auf Kundendaten, um das Problem des Kunden zu bearbeiten.

Kunden-Lockbox für Microsoft 365 hilft Ihnen bei der Erfüllung von Complianceverpflichtungen, wenn Sie Verfahren für die explizite Autorisierung des Datenzugriffs benötigen. Dies ist eine Anforderung für einige Compliancestandards, z. B. FedRAMP und HIPAA. Kunden-Lockbox fügt Sie in den Lockbox-Genehmigungsprozess ein und bietet Ihnen die Möglichkeit, die Autorisierung des Microsoft-Zugriffs auf Ihre Exchange Online oder SharePoint Onlineinhalte für Dienstvorgänge zu steuern.

In den seltenen Fällen, in denen ein Microsoft-Servicetechniker Zugriff auf Ihre Daten benötigt, gewähren Sie nur Zugriff auf Daten, die zur Behebung des Problems erforderlich sind, und für einen begrenzten Zeitraum. Wenn Sie eine Zugriffsanforderung ablehnen, haben Microsoft-Techniker keinen Zugriff auf Ihre Inhalte und können keine Dienstvorgänge ausführen. Wenn Sie die Anforderung genehmigen, haben die Microsoft-Techniker begrenzten Just-in-Time-Zugriff auf Ihre Inhalte über die überwachten und eingeschränkten Verwaltungsschnittstellen.

Aktionen, die vom Supporttechniker ausgeführt werden, werden zu Überwachungszwecken protokolliert und sind über die [Office 365 Verwaltungsaktivitäts-API](/office/office-365-management-api/get-started-with-office-365-management-apis) und das [Security and Compliance Center](https://protection.office.com/)zugänglich.

>[!NOTE]
> Kunden-Lockbox ist in [Microsoft 365 E5](https://products.office.com/business/office-365-enterprise-e5-business-software) als Add-On-Kauf verfügbar. Weitere Informationen finden Sie unter [Microsoft 365 Kunden-Lockbox-Anforderungen.](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)

## <a name="just-in-time-access"></a>Just-in-Time-Zugriff

Microsoft verwendet das JIT-Zugriffsprinzip (Just-in-Time) für Microsoft 365, um Risiken bei der Manipulation von Anmeldeinformationen und laterale Angriffe zu mindern. JIT entfernt beständigen administrativen Zugriff auf Dienste und ersetzt Berechtigungen durch die Möglichkeit, bei Bedarf in diese Rollen zu erhöhen. Durch das Entfernen persistenter Zugriffsrechte von Administratoren wird sichergestellt, dass Anmeldeinformationen nur verfügbar sind, wenn sie benötigt werden, und das Risiko des Diebstahls von Anmeldeinformationen wird reduziert.

Das JIT-Zugriffsmodell erfordert, dass Techniker erhöhte Berechtigungen für einen begrenzten Zeitraum anfordern, um administrative Aufgaben auszuführen. Darüber hinaus verwenden Techniker temporäre Konten, die mit computergenerierten komplexen Kennwörtern erstellt wurden, und gewährten nur die Rollen, mit denen sie die erforderlichen Aufgaben ausführen können. Beispielsweise ist der von Lockbox gewährte administrative Zugriff zeitgebunden, und der gewährte Zeitzugriff hängt von der angeforderten Rolle ab. Ein Techniker gibt die Dauer des Zugriffs an, die in der Anforderung an das Lockbox-System benötigt wird. Das Lockbox-System lehnt Anforderungen ab, wenn die angeforderte Zeit die maximal zulässige Zeit für die Rechteerweiterung überschreitet. Nach Ablauf wird der Administratorzugriff entfernt, und das temporäre Konto läuft ab.

Wenn die Techniker autorisiert und für den Zugriff genehmigt wurden, erhalten sie ein einmaliges, vom Autorisierungssystem generiertes Administratives Kennwort. Jedes Mal, wenn eine Anforderung für erhöhten Zugriff genehmigt wird, werden neue Kennwörter generiert. Das Kennwort wird in einen kennwortsicheren Ordner kopiert, ist von den Anmeldeinformationen des Technikers für die Microsoft-Unternehmensumgebung getrennt und eignet sich nur für die genehmigte Sitzung mit erhöhten Zugriffen.

## <a name="constrained-management-interfaces"></a>Eingeschränkte Verwaltungsschnittstellen

Techniker verwenden zwei Verwaltungsschnittstellen, um administrative Aufgaben auszuführen: Remotedesktop über gesicherte Terminaldienstgateways (TSGs) und Remote-PowerShell. Innerhalb dieser Verwaltungsschnittstellen legen Softwarerichtlinien und Zugriffssteuerungen erhebliche Einschränkungen hinsichtlich der ausgeführten Anwendungen und der verfügbaren Befehle und Cmdlets fest.

Microsoft 365 Server beschränken gleichzeitige Sitzungen auf eine Sitzung pro Dienstteamadministrator und pro Server. TSGs erlauben nur eine einzige gleichzeitige Sitzung für Benutzer und nicht mehrere Sitzungen. Mithilfe einer einzelnen Sitzung pro Server ermöglichen TSGs Microsoft 365 Serviceteamadministratoren, gleichzeitig eine Verbindung mit mehreren Servern herzustellen, damit Administratoren ihre Aufgaben effektiv ausführen können. Dienstteamadministratoren verfügen über keine Berechtigungen für die TSGs selbst. Die TSG wird nur verwendet, um mehrstufige Authentifizierung (Multi-Factor Authentication, MFA) und Verschlüsselungsanforderungen zu erzwingen. Sobald der Dienstteamadministrator über eine TSG eine Verbindung mit einem bestimmten Server herstellt, erzwingt der spezifische Server ein Sitzungslimit von 1 pro Administrator.

Nutzungseinschränkungen und Verbindungs- und Konfigurationsanforderungen für Microsoft 365 Personal werden durch Active Directory-Gruppenrichtlinien festgelegt. Diese Richtlinien umfassen die folgenden Merkmale:

- TSGs verwenden nur [FIPS](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2-validierte Verschlüsselung.
- TSG-Sitzungen werden nach 30 Minuten Inaktivität getrennt.
- TSG-Sitzungen melden sich nach 24 Stunden automatisch ab.

Verbindungen mit TSGs erfordern auch eine MFA mit einer separaten physischen Smartcard und einem Konto, das von den Microsoft-Unternehmensanmeldeinformationen des Technikers getrennt ist. Techniker erhalten unterschiedliche Smartcards für verschiedene Plattformen und geheime Verwaltungsplattformen, um die sichere Speicherung von Anmeldeinformationen zu gewährleisten. TSGs verwenden Active Directory-Gruppenrichtlinien, um zu steuern, wer sich bei Remoteservern anmelden kann, wie viele Sitzungen zulässig sind und welche Timeout-Einstellungen im Leerlauf zulässig sind. Zusätzliche Richtlinien schränken den Zugriff auf zulässige Anwendungen und den Internetzugriff ein.

Zusätzlich zum Remotezugriff mit speziell konfigurierten TSGs ermöglicht Exchange Online Benutzern mit der Rolle "Service Engineer Operations" den Zugriff auf bestimmte Verwaltungsfunktionen auf Produktionsservern mithilfe von Remote PowerShell. Hierzu muss der Benutzer für den schreibgeschützten Zugriff (Debuggen) auf die Microsoft 365 Produktionsumgebung autorisiert sein. Die Berechtigungseskalation wird auf die gleiche Weise aktiviert, wie sie für TSGs mithilfe des Lockbox-Prozesses aktiviert ist.

Für den Remotezugriff verfügt jedes Rechenzentrum über eine virtuelle IP mit Lastenausgleich, die als einzelner Zugriffspunkt dient. Die verfügbaren Remote-PowerShell-Cmdlets basieren auf der Berechtigungsstufe, die in dem Während der Authentifizierung abgerufenen Zugriffsanspruch angegeben ist. Diese Cmdlets bieten die einzige Verwaltungsfunktionalität, auf die Benutzer mit dieser Methode zugreifen können. Remote-PowerShell schränkt den Umfang der Befehle ein, die dem Techniker zur Verfügung stehen, und basiert auf der Zugriffsebene, die über den Lockbox-Prozess gewährt wird. In Exchange Online sind möglicherweise Get-Mailbox verfügbar, Set-Mailbox jedoch nicht.
