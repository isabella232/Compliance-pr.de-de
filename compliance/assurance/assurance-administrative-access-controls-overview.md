---
title: Administrative Zugriffssteuerungen in Microsoft 365
description: Dieser Artikel bietet eine Übersicht über die administrativen Zugriffssteuerungen und die Datenkategorisierung in Microsoft 365.
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
ms.openlocfilehash: 06bdd239e2845d3495a40fc83bd33cbb0e43dbdb3d025bd8fa77b5d5451a680c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54289263"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>Administrative Zugriffssteuerungen in Microsoft 365 

Microsoft hat stark in Systeme und Steuerelemente investiert, die die meisten Microsoft 365 Vorgänge automatisieren und gleichzeitig den Zugriff auf Kundeninhalte durch Microsoft absichtlich einschränken. Menschen steuern den Dienst, und Software betreibt den Dienst. Mit dieser Struktur kann Microsoft Microsoft 365 im großen Maßstab verwalten und die Risiken interner Bedrohungen für Kundeninhalte verwalten.

Standardmäßig verfügen Microsoft-Techniker über keine ständigen Administratorrechte und keinen ständigen Zugriff auf Kundeninhalte in Microsoft 365. Ein Microsoft-Techniker kann für einen begrenzten Zeitraum eingeschränkten, überwachten und sicheren Zugriff auf die Inhalte eines Kunden haben. Der Zugriff erfolgt nur, wenn dies für Dienstvorgänge erforderlich ist und nur, wenn er von einem Mitglied der Geschäftsleitung von Microsoft genehmigt wird. Für Kunden-Lockbox-lizenzierte Kunden stellt der Kunde eine Zugriffsgenehmigung für seine Inhalte bereit, die auf Microsoft 365 gehostet werden.

Microsoft bietet Onlinedienste mit mehreren Formen der Cloudbereitstellung an:

- **Öffentliche Clouds:** Umfasst mehrinstanzenfähige Versionen von Microsoft 365, Azure und anderen Diensten, die in Nordamerika, Nordamerika, Europa, Asien, Australien usw. gehostet werden.
- **Nationale Clouds:** Umfasst alle unabhängigen und von Drittanbietern betriebenen Clouds außerhalb der Vereinigten Staaten (mit Ausnahme der zuvor erwähnten), z. B. Microsoft 365 in China (betrieben von 21Vianet) und Microsoft 365 in Deutschland (betrieben von Microsoft, jedoch unter einem Modell, in dem ein deutscher Datenverwalter, deutsche Telekom, den Zugriff von Microsoft auf Kundendaten und Systeme kontrolliert und überwacht, die Kundendaten enthalten).
- **Government Clouds:** Umfasst Microsoft 365 und Azure-Dienste, die us-Regierungsbehörden zur Verfügung stehen.

Für die Zwecke dieses Artikels umfassen Microsoft 365 Dienste Folgendes:

- [Exchange Online](/Exchange/exchange-online)
- [Exchange Online Protection](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [OneDrive for Business](/OneDrive/onedrive)
- [Skype for Business](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Microsoft 365 Zugriffssteuerungen

Zu Zwecken der Zugriffssteuerung kategorisiert Microsoft Microsoft 365 Daten als Kundendaten oder andere Arten von Daten.

### <a name="customer-data"></a>Kundendaten

Kundendaten sind alle Daten, die von oder im Auftrag eines Kunden bereitgestellt werden, wenn Microsoft 365 Dienste verwendet werden. Bei diesen Daten handelt es sich um Kundeninhalte, die direkt von Microsoft 365 Benutzern erstellt oder hochgeladen werden, einschließlich:

- E-Mails
- SharePoint Onlineinhalte
- Chatnachrichten
- Kalenderelemente
- Dokumente
- Kontakte
- Informationen zur Identifizierung von Endbenutzern (EUII) (Daten, die für einen Benutzer eindeutig sind oder mit einem einzelnen Benutzer verknüpft werden können, aber keine Kundeninhalte enthalten)

### <a name="other-types-of-data"></a>Andere Datentypen

Andere Datentypen sind:

- **Kontodaten:** Umfasst Administrative Daten (Von Administratoren bereitgestellte Informationen beim Registrieren oder Erwerben von Diensten) und Zahlungsdaten (Informationen zu Zahlungssinstrumenten, z. B. Kreditkartendetails).
- **Organisatorisch identifizierbare Informationen:** Enthält Daten, die verwendet werden, um einen Mandanten zu identifizieren, Nutzungsdaten und nicht mit einem einzelnen Benutzer verknüpft oder in Kundeninhalten enthalten sind.
- **Systemmetadaten:** Enthält Dienstprotokolle, die Konfigurationseinstellungen, Systemstatus, Microsoft-IP-Adressen und technische Informationen zu Abonnements und Mandanten enthalten.

Microsoft hat Zugriffssteuerungsmechanismen eingerichtet, um sicherzustellen, dass niemand nicht genehmigten Zugriff auf Kundendaten oder Zugriffssteuerungsdaten hat. Zugriffssteuerungsdaten verwalten den Zugriff auf andere Arten von Daten oder Funktionen innerhalb der Umgebung, einschließlich des Zugriffs auf Kundeninhalte oder EUII, Microsoft-Kennwörter, Sicherheitszertifikate und andere daten im Zusammenhang mit der Authentifizierung. Zugriffssteuerungsmechanismen schützen auch vor nicht genehmigten physischen, logischen oder Remotezugriffen auf die Microsoft 365 Produktionsumgebung.

Es gibt drei Kategorien von Zugriffssteuerungen, die von Microsoft für den Betrieb von Microsoft 365 verwendet werden:

- Isolierungssteuerungen
- Personalsteuerungen
- Technologiesteuerungen

In Kombination helfen diese Steuerelemente dabei, böswillige Aktionen in Microsoft 365 zu verhindern und zu erkennen. Zusätzlich zu den von Microsoft verwendeten Isolierungs-, Personal- und Technologiesteuerelementen gibt es eine vierte Kategorie von Steuerelementen: die von Kunden implementierten Kontrollen.

Microsoft 365 ermöglicht es Ihnen, Daten auf die gleiche Weise zu verwalten, wie Daten in lokalen Umgebungen verwaltet werden. Die Person, die eine Organisation für Microsoft 365 registriert, wird automatisch ein globaler Administrator. Der globale Administrator hat Zugriff auf alle Funktionen in Verwaltungsportalen und kann:

- Erstellen oder Bearbeiten von Benutzern
- Zuweisen von Administratorrollen zu anderen
- Zurücksetzen von Benutzerkennwörtern
- Verwalten von Benutzerlizenzen
- Verwalten von Domänen
- Genehmigen von Kunden-Lockbox-Anforderungen

Es wird empfohlen, dass jede Organisation mindestens zwei Administratorkonten konfiguriert. Für große Unternehmen empfehlen wir spezielle Administratorkonten, die unterschiedliche Funktionen erfüllen.

Informationen zum Zuweisen von Administratorrollen und -berechtigungen finden Sie unter ["Zuweisen von Administratorrollen"](/microsoft-365/admin/add-users/assign-admin-roles) und ["Informationen zu Administratorrollen".](/microsoft-365/admin/add-users/about-admin-roles)

## <a name="related-links"></a>Links zu verwandten Themen

- [Isolation in Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Überprüfung vor der Einstellung durch Microsoft](assurance-pre-employment-screening.md)
- [Microsoft Cloud-Hintergrundprüfung](assurance-cloud-background-check.md)
- [Überwachung und Überprüfung von Zugriffssteuerungen](assurance-monitoring-and-auditing-access-controls.md)
- [Yammer Enterprise-Zugriffssteuerungen](assurance-yammer-enterprise-access-controls.md)
