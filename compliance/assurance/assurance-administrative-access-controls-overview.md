---
title: Administrative Zugriffssteuerungen in Microsoft 365
description: Dieser Artikel bietet eine Übersicht über die Administrativen Zugriffssteuerungen und die Daten kategorisierung in Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e7dc9d73b6eb1961387d85910bb558e85498ffae
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497702"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>Administrative Zugriffssteuerungen in Microsoft 365 

Microsoft hat stark in Systeme und Steuerelemente investiert, die die meisten Microsoft 365-Vorgänge automatisieren und den Zugriff auf Kundeninhalte durch Microsoft bewusst einschränken. Menschen steuern den Dienst, und Software betreibt den Dienst. Diese Struktur ermöglicht Es Microsoft, Microsoft 365 im Großen und Umfang zu verwalten und die Risiken interner Bedrohungen für Kundeninhalte zu verwalten.

Standardmäßig haben Microsoft-Techniker keine ständigen Administratorrechte und keinen ständigen Zugriff auf Kundeninhalte in Microsoft 365. Ein Microsoft-Techniker kann über einen begrenzten, überwachten und gesicherten Zugriff auf die Inhalte eines Kunden für einen begrenzten Zeitraum verfügen. Der Zugriff ist nur bei Bedarf für Dienstvorgänge und nur bei Genehmigung durch ein Mitglied der Geschäftsleitung von Microsoft erforderlich. Für kundenlizenzierte Kunden von Lockbox stellt der Kunde die Zugriffsgenehmigung für die inhalte zur Verfügung, die in Microsoft 365 gehostet werden.

Microsoft stellt Onlinedienste mit mehreren Formen der Cloudzustellung zur Verfügung:

- **Öffentliche Clouds:** Enthält mehrstufige Versionen von Microsoft 365, Azure und anderen Diensten, die in Nordamerika, Südamerika, Europa, Asien, Australien usw. gehostet werden.
- **Nationale Clouds:** Umfasst alle unabhängigen und von Drittanbietern betriebenen Clouds außerhalb der Vereinigten Staaten (mit Ausnahme der zuvor erwähnten), z. B. Microsoft 365 in China (betrieben von 21Vianet) und Microsoft 365 in Deutschland (betrieben von Microsoft, aber unter einem Modell, in dem ein deutscher Datentreuhänder, die Deutsche Telekom, den Zugriff von Microsoft auf Kundendaten und Systeme steuert und überwacht, die Kundendaten enthalten).
- **Government Clouds:** Enthält Microsoft 365- und Azure-Dienste, die für Us-Government-Kunden verfügbar sind.

Für die Zwecke dieses Artikels umfassen Microsoft 365-Dienste Folgendes:

- [Exchange Online](/Exchange/exchange-online)
- [Exchange Online Protection](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [OneDrive for Business](/OneDrive/onedrive)
- [Skype for Business](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Microsoft 365-Zugriffssteuerelemente

Zu Zwecken der Zugriffssteuerung kategorisiert Microsoft Microsoft 365-Daten als Kundendaten oder andere Arten von Daten.

### <a name="customer-data"></a>Kundendaten

Kundendaten sind alle Daten, die von oder im Auftrag eines Kunden bei der Verwendung von Microsoft 365-Diensten bereitgestellt werden. Diese Daten sind Kundeninhalte, die direkt von Microsoft 365-Benutzern erstellt oder hochgeladen werden, einschließlich:

- E-Mails
- SharePoint Online-Inhalte
- Chatnachrichten
- Kalenderelemente
- Dokumente
- Kontakte
- Identifizierbare Endbenutzerinformationen (EUII) (Daten, die für einen Benutzer eindeutig sind oder mit einem einzelnen Benutzer verknüpfen können, aber keine Kundeninhalte enthalten)

### <a name="other-types-of-data"></a>Andere Datentypen

Weitere Datentypen sind:

- **Kontodaten:** Enthält administrative Daten (Informationen, die von Administratoren bei der Anmeldung oder dem Kauf von Diensten bereitgestellt werden) und Zahlungsdaten (Informationen zu Zahlungsinstrumenten, z. B. Kreditkartendetails).
- **Organisatorisch identifizierbare Informationen:** Enthält Daten, die verwendet werden, um einen Mandanten zu identifizieren, Nutzungsdaten und nicht mit einem einzelnen Benutzer zu verknüpfen oder in Kundeninhalten enthalten zu sein.
- **Systemmetadaten:** Enthält Dienstprotokolle mit Konfigurationseinstellungen, Systemstatus, Microsoft-IP-Adressen und technischen Informationen zu Abonnements und Mandanten.

Microsoft hat Zugriffskontrollesmechanismen eingerichtet, um sicherzustellen, dass niemand nicht genehmigten Zugriff auf Kundendaten oder Zugriffssteuerungsdaten hat. Zugriffssteuerungsdaten verwalten den Zugriff auf andere Arten von Daten oder Funktionen in der Umgebung, einschließlich Zugriff auf Kundeninhalte oder EUII, Microsoft-Kennwörter, Sicherheitszertifikate und andere Authentifizierungsdaten. Zugriffssteuerungsmechanismen schützen auch vor nicht genehmigten physischen, logischen oder Remotezugriffen auf die Microsoft 365-Produktionsumgebung.

Es gibt drei Kategorien von Zugriffssteuerelementen, die von Microsoft für den Betrieb von Microsoft 365 verwendet werden:

- Isolierungssteuerungen
- Personalsteuerungen
- Technologiesteuerungen

In Kombination helfen diese Steuerelemente, böswillige Aktionen in Microsoft 365 zu verhindern und zu erkennen. Zusätzlich zu den von Microsoft verwendeten Isolations-, Personal- und Technologiesteuerelementen gibt es eine vierte Kategorie von Steuerelementen: diese Steuerelemente, die von Kunden implementiert werden.

Mit Microsoft 365 können Sie Daten auf die gleiche Weise verwalten, wie Daten in lokalen Umgebungen verwaltet werden. Die Person, die eine Organisation für Microsoft 365 einschreibt, wird automatisch globaler Administrator. Der globale Administrator hat Zugriff auf alle Features in Verwaltungsportalen und kann:

- Erstellen oder Bearbeiten von Benutzern
- Zuweisen von Administratorrollen zu anderen Personen
- Zurücksetzen von Benutzerkennwörtern
- Verwalten von Benutzerlizenzen
- Verwalten von Domänen
- Genehmigen von Kunden-Lockbox-Anforderungen

Es wird empfohlen, dass jede Organisation mindestens zwei Administratorkonten konfiguriert. Für große Unternehmensorganisationen empfehlen wir spezielle Administratorkonten, die unterschiedliche Funktionen erfüllen.

Informationen zum Zuweisen von Administratorrollen und -berechtigungen finden Sie unter Zuweisen von [Administratorrollen](/microsoft-365/admin/add-users/assign-admin-roles) und [Informationen zu Administratorrollen](/microsoft-365/admin/add-users/about-admin-roles).

## <a name="related-links"></a>Links zu verwandten Themen

- [Isolation in Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Überprüfung vor der Einstellung durch Microsoft](assurance-pre-employment-screening.md)
- [Microsoft Cloud-Hintergrundprüfung](assurance-cloud-background-check.md)
- [Überwachung und Überprüfung von Zugriffssteuerungen](assurance-monitoring-and-auditing-access-controls.md)
- [Yammer Enterprise-Zugriffssteuerungen](assurance-yammer-enterprise-access-controls.md)
