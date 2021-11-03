---
title: Zugriffssteuerung für Microsoft 365 Servicetechniker
description: Eine Übersicht über die Zugriffssteuerungsarchitektur Microsoft 365 Servicetechnikers.
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
ms.openlocfilehash: 2700c95feb5c32765e2dc3420c67800b154b1e9d
ms.sourcegitcommit: 85b36ce8c79fb111980cc6462f2addb44a924065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2021
ms.locfileid: "60678472"
---
# <a name="microsoft-365-service-engineer-access-control"></a>Zugriffssteuerung für Microsoft 365 Servicetechniker

Zero Standing Access (ZSA) bedeutet, dass Mitarbeiter des Microsoft-Serviceteams keinen ständigen privilegierten Zugriff auf die Microsoft 365 Produktionsumgebung oder auf Kundendaten haben. Wenn ein Microsoft-Serviceteammitglied den Dienst aktualisieren oder aus irgendeinem Grund auf Kundendaten zugreifen möchte, muss er eine Anforderung übermitteln, die die Notwendigkeit rechtfertigen, und die Genehmigung von einem autorisierten Vorgesetzten erhalten. Im großen Maßstab ist es nicht machbar, den Zugriff manuell bereitzustellen und zu entfernen, wenn dies erforderlich ist, um Microsoft 365 Dienste zu verwalten. Daher hat Microsoft eine automatisierte Lösung entwickelt, um den privilegierten Zugriff nach Bedarf zu verwalten.

## <a name="lockbox"></a>Lockbox

Der gesamte Zugriff auf Microsoft 365 Systeme und Kundendaten wird von Lockbox vermittelt, einem Zugriffssteuerungssystem, das ein Just-In-Time-Modell (JIT) und ein JEA-Modell (Just-Enough-Access) verwendet, um Servicetechnikern temporären privilegierten Zugriff auf angegebene Microsoft 365 Dienste und Daten zu gewähren. Darüber hinaus werden alle Anforderungen und Aktionen zu Überwachungszwecken protokolliert und können über die [Office 365-Verwaltungsaktivitäts-API](/office/office-365-management-api/get-started-with-office-365-management-apis) und das [Security and Compliance Center](https://protection.office.com/)aufgerufen werden.

Bevor ein Microsoft-Servicetechniker eine Verbindung mit beliebigen Microsoft 365 Systemen herstellen oder auf Kundendaten zugreifen kann, muss er eine Zugriffsanforderung über Lockbox senden. Diese Anforderung kann nur genehmigt werden, wenn bestimmte Kriterien erfüllt sind:

- Der Servicetechniker erfüllt die [Berechtigungsanforderungen für ein Serviceteamkonto,](assurance-microsoft-365-account-management.md)
- Sie gehören zur Lockbox-Rolle, die der Arbeit in der Anforderung zugeordnet ist.
- Die angeforderte Zugriffszeit überschreitet nicht die maximal zulässige Zeit,
- Sie haben eine berechtigte geschäftliche Begründung,
- Die angeforderte Ressource, auf die sie zugreifen möchten, liegt innerhalb ihres Arbeitsumfangs und
- Sie erhalten eine Genehmigung durch den Vorgesetzten

Sobald alle Kriterien erfüllt und von Lockbox überprüft wurden, wird der temporäre Zugriff gewährt, um die spezifische angeforderte Aktion auszuführen. Nachdem die Zeit für die Anforderung abgelaufen ist, wird der Zugriff widerrufen.

![Lockbox-Zugriffsprozess.](../media/assurance-lockbox-process.png)

Wenn ein Kunde die [Kunden-Lockbox-Funktion](/microsoft-365/compliance/customer-lockbox-requests) lizenziert und aktiviert, müssen alle Versuche eines Microsoft-Servicetechnikers, auf Kundendaten zuzugreifen, zusätzlich von einem Administrator im Kundenmandanten genehmigt werden. Der Zugriff auf Kundendaten kann sowohl von Kunden als auch von Microsoft erfolgen. Beispielsweise kann ein von einem Kunden ausgelöster Vorfall Zugriff auf seine Daten erfordern, um das Problem zu beheben, oder wenn Microsoft Datenzugriff benötigt, um ein bestimmtes Update anzuwenden.

![Kunden-Lockbox-Zugriffsprozess.](../media/assurance-customer-lockbox-process.png)

Kunden verfügen nicht über Tools zum Initiieren einer Kunden-Lockbox-Anforderung. sie müssen ein Ticket an Microsoft übermitteln, für das eine Kunden-Lockbox-Anforderung ausgelöst werden muss. Eine von einem Microsoft-Servicetechniker ausgelöste Kunden-Lockbox-Anforderung muss von einem Microsoft-Manager und einem autorisierten Administrator im Kundenmandanten genehmigt werden.

### <a name="lockbox-roles"></a>Lockbox-Rollen

Um die Trennung von Aufgaben und das Prinzip der geringsten Rechte zu erzwingen, müssen Servicetechniker zu einer Lockbox-Rolle gehören, die ihrer Rolle im Team entspricht. Lockbox-Rollen werden innerhalb des Identitätsverwaltungstools verwaltet und definieren die Berechtigungen und Aktionen, für die ein Serviceteammitglied über den Lockbox-Anforderungsprozess genehmigt werden kann. Serviceteammitarbeiter müssen anfordern, Mitglied einer Lockbox-Rolle zu sein, und die Genehmigung erhalten. Wenn dies genehmigt ist, wird das Serviceteamkonto des Mitarbeiters in einer Sicherheitsgruppe platziert, die von Active Directory (AD) und Azure Active Directory (AAD) erzwungen wird.

## <a name="constrained-management-interfaces"></a>Eingeschränkte Verwaltungsschnittstellen

Servicetechniker verwenden zwei Verwaltungsschnittstellen, um administrative Aufgaben auszuführen: Remotedesktop von einer Arbeitsstation mit sicherem Zugriff (SAW) über ein sicheres Terminaldienstgateway (TSG) und Remote-PowerShell. Innerhalb dieser Verwaltungsschnittstellen gelten für Zugriffssteuerungen, die auf der genehmigten Lockbox-Anforderung basieren, und Softwarerichtlinien erhebliche Einschränkungen, welche Anwendungen ausgeführt werden und welche Befehle und Cmdlets verfügbar sind.

## <a name="remote-desktop"></a>Remote Desktop

Serviceteammitglieder, die ihren Dienst über Remotedesktop verwalten, müssen eine Verbindung von einer SAW herstellen, die speziell für diesen Anwendungsfall von Microsoft verwaltet wird. Microsoft arbeitet mit Lieferanten zusammen, um SAWs zu erstellen und eine kurze und sichere Lieferkette zu erstellen. SAWs verwenden gehärtete Betriebssysteme, die so konfiguriert sind, dass sie alle Funktionen einschränken, außer was für definierte Verwaltungsaufgaben erforderlich ist. Zu diesen Einschränkungen gehören das Deaktivieren aller USB-Anschlüsse, strenge Anwendungszugriffslisten, das Entfernen des E-Mail-Zugriffs, das Einschränken des Internetbrowsens und das Erzwingen von Inaktivitätsbildschirmaver-Sperren. Microsoft-Zugriffssteuerungssysteme überprüfen SAW-Computer regelmäßig, um sicherzustellen, dass sie mit den neuesten Sicherheitssteuerelementen kompatibel sind, und deaktiviert Computer automatisch, wenn sie als nicht konform eingestuft werden.

Servicetechniker dürfen nur jeweils eine Verbindung mit einer TSG herstellen, und mehrere Sitzungen sind nicht zulässig. TSGs ermöglichen es Microsoft 365 Serviceteamadministratoren jedoch, eine Verbindung mit mehreren Servern herzustellen, die jeweils nur eine gleichzeitige Sitzung haben, sodass Administratoren ihre Aufgaben effektiv ausführen können. Dienstteamadministratoren verfügen über keine Berechtigungen für die TSGs selbst. Die TSG wird nur verwendet, um mehrstufige Authentifizierung (MFA) und Verschlüsselungsanforderungen zu erzwingen. Sobald der Dienstteamadministrator über eine TSG eine Verbindung mit einem bestimmten Server herstellt, erzwingt der spezifische Server ein Sitzungslimit von 1 pro Administrator.

Nutzungseinschränkungen, Verbindungs- und Konfigurationsanforderungen für Microsoft 365 Personal werden durch Active Directory-Gruppenrichtlinien festgelegt. Diese Richtlinien umfassen die folgenden TSG-Merkmale:

- Nur [FIPS 140-2-validierte](/compliance/regulatory/offering-FIPS-140-2) Verschlüsselung verwenden
- Sitzungstrennung nach 15 Minuten Inaktivität
- Sitzungen werden nach 24 Stunden automatisch abgemeldet

Verbindungen mit TSGs erfordern auch MFA mit einer separaten physischen Smartcard. Servicetechniker erhalten unterschiedliche Smartcards für verschiedene Plattformen und geheime Verwaltungsplattformen, um die sichere Speicherung von Anmeldeinformationen zu gewährleisten. TSGs verwenden Active Directory-Gruppenrichtlinien, um zu steuern, wer sich bei Remoteservern anmelden kann, wie viele Sitzungen zulässig sind und welche Timeout-Einstellungen im Leerlauf zulässig sind.

## <a name="remote-powershell"></a>Remote-PowerShell

Zusätzlich zum Remotezugriff mit speziell konfigurierten TSGs können Serviceteammitarbeiter mit der Rolle "Service Engineer Operations Lockbox" mithilfe von Remote PowerShell auf bestimmte Verwaltungsfunktionen auf Produktionsservern zugreifen. Um diesen Zugriff zu verwenden, muss der Benutzer für den schreibgeschützten Zugriff (Debuggen) auf die Microsoft 365 Produktionsumgebung autorisiert sein. Die Berechtigungseskalation wird auf die gleiche Weise aktiviert, wie sie für TSGs mithilfe des Lockbox-Prozesses aktiviert ist.

Für den Remotezugriff verfügt jedes Rechenzentrum über eine virtuelle IP mit Lastenausgleich, die als einzelner Zugriffspunkt dient. Die verfügbaren Remote-PowerShell-Cmdlets basieren auf der Berechtigungsstufe, die in dem Während der Authentifizierung abgerufenen Zugriffsanspruch angegeben ist. Diese Cmdlets bieten die einzige Verwaltungsfunktionalität, auf die Benutzer mit dieser Methode zugreifen können. Remote-PowerShell schränkt den Umfang der Befehle ein, die dem Techniker zur Verfügung stehen, und basiert auf der Zugriffsebene, die über den Lockbox-Prozess gewährt wird. In Exchange Online ist das cmdlet Get-Mailbox möglicherweise verfügbar, das Cmdlet Set-Mailbox jedoch nicht.

## <a name="resources"></a>Ressourcen

- [Isolation in Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Microsoft Pre-Employment Screening](assurance-pre-employment-screening.md)[Microsoft Cloud Background Check](assurance-cloud-background-check.md)
