---
title: Administrative Zugriffssteuerungen in Microsoft 365
description: Dieser Artikel bietet eine Übersicht über die Steuerelemente für den administrativen Zugriff und die Daten kategorisierung in Microsoft 365.
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
ms.openlocfilehash: d3d6cd30fbe682de979d5c04943c57cedc86552f
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120714"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>Administrative Zugriffssteuerungen in Microsoft 365 

Microsoft hat stark in Systeme und Steuerelemente investiert, die die meisten Microsoft 365-Vorgänge automatisieren und gleichzeitig den Zugriff auf Kundeninhalte durch Microsoft absichtlich einschränken. Menschen steuern den Dienst, und software betreibt den Dienst. Diese Struktur ermöglicht Es Microsoft, Microsoft 365 im großen Maßstab zu verwalten und die Risiken interner Bedrohungen für Kundeninhalte zu verwalten.

Standardmäßig verfügen die Microsoft-Techniker über keine ständigen Administratorrechte und keinen ständigen Zugriff auf Kundeninhalte in Microsoft 365. Ein Microsoft-Techniker kann über einen begrenzten, überwachten und gesicherten Zugriff auf die Inhalte eines Kunden für einen begrenzten Zeitraum verfügen. Der Zugriff ist nur erforderlich, wenn dies für Dienstvorgänge erforderlich ist, und nur, wenn er von einem Mitglied der Geschäftsleitung von Microsoft genehmigt wird. Für Kunden mit Lockboxlizenz erteilt der Kunde Zugriffsgenehmigungen für inhalte, die auf Microsoft 365 gehostet werden.

Microsoft stellt Onlinedienste mit mehreren Formen der Cloudbereitstellung zur Verfügung:

- **Öffentliche Clouds:** Enthält mehr mandantenversionen von Microsoft 365, Azure und andere Dienste, die in Nordamerika, Südamerika, Europa, Asien, Australien usw. gehostet werden.
- **Nationale Clouds:** Umfasst alle unabhängigen und von Drittanbietern betriebenen Clouds außerhalb der Vereinigten Staaten (mit Ausnahme der oben erwähnten), wie Microsoft 365 in China (betrieben von 21Vianet) und Microsoft 365 in Deutschland (betrieben von Microsoft, aber unter einem Modell, bei dem ein deutscher Datentreuhänder, Deutsche Telekom, den Zugriff von Microsoft auf Kundendaten und Systeme, die Kundendaten enthalten, steuert und überwacht).
- **Behörden-Clouds:** Umfasst Microsoft 365- und Azure-Dienste, die für Kunden der US-Regierung verfügbar sind.

Zu den Microsoft 365-Diensten im Sinne dieses Artikels gehören:

- [Exchange Online](/Exchange/exchange-online)
- [Exchange Online Protection](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [OneDrive for Business](/OneDrive/onedrive)
- [Skype for Business](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Microsoft 365-Zugriffssteuerungen

Zur Zugriffssteuerung kategorisiert Microsoft Microsoft 365-Daten als Kundendaten oder andere Arten von Daten.

### <a name="customer-data"></a>Kundendaten

Kundendaten sind alle Daten, die von oder im Auftrag eines Kunden bei Verwendung von Microsoft 365-Diensten bereitgestellt werden. Diese Daten sind Kundeninhalte, die direkt von Microsoft 365-Benutzern erstellt oder hochgeladen wurden, einschließlich:

- E-Mails
- SharePoint Online-Inhalte
- Chatnachrichten
- Kalenderelemente
- Dokumente
- Kontakte
- Endbenutzeridentifizierbare Informationen (EUII) (Daten, die für einen Benutzer eindeutig sind oder mit einem einzelnen Benutzer verlinkbar sind, aber keine Kundeninhalte enthalten)

### <a name="other-types-of-data"></a>Andere Datentypen

Zu den anderen Datentypen gehören:

- **Kontodaten:** Umfasst Administrative Daten (Informationen, die von Administratoren beim Registrieren oder Erwerben von Diensten bereitgestellt werden) und Zahlungsdaten (Informationen zu Zahlungsgeräten, z. B. Kreditkartendetails).
- **Organisationsidentifizierbare Informationen:** Enthält Daten, die verwendet werden, um einen Mandanten, Nutzungsdaten zu identifizieren und nicht mit einem einzelnen Benutzer zu verknüpfen oder in Kundeninhalte einbezogen zu werden.
- **Systemmetadaten:** Umfasst Dienstprotokolle mit Konfigurationseinstellungen, Systemstatus, Microsoft-IP-Adressen und technischen Informationen zu Abonnements und Mandanten.

Microsoft hat Zugriffskontrollmechanismen eingerichtet, um sicherzustellen, dass niemand nicht genehmigten Zugriff auf Kundendaten oder Zugriffssteuerungsdaten hat. Zugriffssteuerungsdaten verwalten den Zugriff auf andere Arten von Daten oder Funktionen innerhalb der Umgebung, einschließlich zugriff auf Kundeninhalte oder EUII, Microsoft-Kennwörter, Sicherheitszertifikate und andere Authentifizierungsdaten. Zugriffskontrollmechanismen schützen auch vor nicht genehmigten physischen, logischen oder Remotezugriffen auf die Microsoft 365-Produktionsumgebung.

Es gibt drei Kategorien von Zugriffssteuerungen, die von Microsoft für den Betrieb von Microsoft 365 verwendet werden:

- Isolierungssteuerungen
- Personalsteuerungen
- Technologiesteuerungen

In Kombination helfen diese Steuerelemente dabei, bösartige Aktionen in Microsoft 365 zu verhindern und zu erkennen. Zusätzlich zu den von Microsoft verwendeten Isolierungs-, Personal- und Technologiekontrollen gibt es eine vierte Kategorie von Steuerelementen: diese Steuerelemente, die von Kunden implementiert werden.

Mit Microsoft 365 können Sie Daten auf die gleiche Weise verwalten, wie Daten in lokalen Umgebungen verwaltet werden. Die Person, die eine Organisation für Microsoft 365 einschreibt, wird automatisch ein globaler Administrator. Der globale Administrator hat Zugriff auf alle Funktionen in Verwaltungsportalen und kann:

- Erstellen oder Bearbeiten von Benutzern
- Zuweisen von Administratorrollen zu anderen Personen
- Zurücksetzen von Benutzerkennwörtern
- Verwalten von Benutzerlizenzen
- Verwalten von Domänen
- Genehmigen von Kunden-Lockbox-Anforderungen

Es wird empfohlen, dass jede Organisation mindestens zwei Administratorkonten konfiguriert. Für große Unternehmensorganisationen empfehlen wir spezielle Administratorkonten, die unterschiedliche Funktionen erfüllen.

Informationen zum Zuweisen von Administratorrollen und -berechtigungen finden Sie unter ["Zuweisen von Administratorrollen"](/microsoft-365/admin/add-users/assign-admin-roles) und ["Informationen zu Administratorrollen".](/microsoft-365/admin/add-users/about-admin-roles)

## <a name="related-links"></a>Links zu verwandten Themen

- [Isolation in Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Überprüfung vor der Einstellung durch Microsoft](assurance-pre-employment-screening.md)
- [Microsoft Cloud-Hintergrundprüfung](assurance-cloud-background-check.md)
- [Überwachung und Überprüfung von Zugriffssteuerungen](assurance-monitoring-and-auditing-access-controls.md)
- [Yammer Enterprise-Zugriffssteuerungen](assurance-yammer-enterprise-access-controls.md)
