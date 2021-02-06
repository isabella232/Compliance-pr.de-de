---
title: Aufbewahrung, Löschung und Vernichtung von Daten in Microsoft 365
description: Eine Übersicht über die Microsoft-Richtlinien für Microsoft 365 in Bezug auf die Aufbewahrung, Löschung und Vernichtung von Daten.
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
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 025e2c422c05dbffdf5a510f93809beaed3fe09d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120654"
---
# <a name="data-retention-deletion-and-destruction-in-microsoft-365"></a>Aufbewahrung, Löschung und Vernichtung von Daten in Microsoft 365

Microsoft verfügt über eine Datenverarbeitungsstandardrichtlinie für Microsoft 365, die angibt, wie lange Kundendaten nach dem Löschen aufbewahrt werden. Es gibt in der Regel zwei Szenarien, in denen Kundendaten gelöscht werden:

- **Aktive Löschung:** Der Mandant verfügt über ein aktives Abonnement, und ein Benutzer oder Administrator löscht Daten, oder Administratoren löschen einen Benutzer.
- **Passive Löschung:** Das Mandantenabonnement endet.

## <a name="data-retention"></a>Datenaufbewahrung

Für jedes dieser Löschszenarien ist in der folgenden Tabelle der maximale Aufbewahrungszeitraum nach Datenkategorie und Klassifizierung aufgeführt:

| Datenkategorie | Datenklassifikation | Beschreibung | Beispiele | Aufbewahrungszeitraum |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| Kundendaten | Kundeninhalte| Von Administratoren und Benutzern direkt bereitgestellte/erstellte Inhalte <br><br> Enthält alle Text-, Sound-, Video-, Bilddateien und Software, die bei Verwendung der Dienste in Microsoft 365 in Microsoft Rechenzentren erstellt und gespeichert wird. | Beispiele für die am häufigsten verwendeten Microsoft 365-Anwendungen, mit denen Benutzer Daten erstellen können, sind Word, Excel, PowerPoint, Outlook und OneNote. <br><br> Kundeninhalte umfassen auch geheime Schlüssel im Besitz des Kunden (Kennwörter, Zertifikate, Verschlüsselungsschlüssel, Speicherschlüssel) | **Aktives Löschszenario:** mindestens 30 Tage <br><br> **Szenario für passives Löschen:** mindestens 180 Tage |
| Kundendaten | Endbenutzeridentifizierbare Informationen (EUII) | Daten, die den Benutzer eines Microsoft-Diensts identifizieren oder verwenden können. EUII enthält keine Kundeninhalte | Benutzername oder Anzeigename (DOMAIN\UserName) <br><br> Benutzerprinzipalname (name@domain) <br><br>  Benutzerspezifische IP-Adressen | **Active Deletion Scenario:** at most 180 days (only a tenant administrator action) <br><br> **Passives Löschszenario:** bis zu 180 Tage |
| Persönliche Daten <br> (Daten, die nicht in Kundendaten enthalten sind) | Pseudonyme Bezeichner für Endbenutzer (EUPI) | Ein von Microsoft erstellter Bezeichner, der an den Benutzer eines Microsoft-Diensts gebunden ist. In Kombination mit anderen Informationen, z. B. einer Zuordnungstabelle, identifiziert der EUPI den Endbenutzer. <br><br> DER EUPI enthält keine Vom Kunden hochgeladenen oder erstellten Informationen. | Benutzer-GUIDs, PUIDs oder SIDs <br><br> Sitzungs-IDs | **Aktives Löschszenario:** mindestens 30 Tage <br><br> **Passives Löschszenario:** bis zu 180 Tage |

## <a name="subscription-retention"></a>Abonnementaufbewahrung

In der Laufzeit eines aktiven Abonnements kann ein Teilnehmer auf Kundendaten zugreifen, diese extrahieren oder löschen, die in Microsoft 365 gespeichert sind. Wenn ein kostenpflichtiges Abonnement endet oder gekündigt wird, behält Microsoft Kundendaten, die in Microsoft 365 gespeichert sind, 90 Tage lang in einem Konto mit eingeschränkter Funktion bei, damit der Abonnent die Daten extrahieren kann. Nach Ende des 90-tägigen Aufbewahrungszeitraums deaktiviert Microsoft das Konto und löscht die Kundendaten. Spätestens 180 Tage nach Ablauf oder Kündigung eines Microsoft 365-Abonnements deaktiviert Microsoft das-Konto und löscht alle Kundendaten daraus. Sobald der maximale Aufbewahrungszeitraum für Daten abgelaufen ist, werden die Daten kommerziell nicht mehr wiederhergestellt.

Bei einer kostenlosen Testversion wechselt Ihr Konto in den meisten Ländern und Regionen für 30 Tage in einen Nachfriststatus. Innerhalb dieser Nachfrist können Sie Microsoft 365 kaufen. Wenn Sie sich entscheiden, Microsoft 365 nicht zu kaufen, können Sie entweder Ihre Testversion kündigen oder die Nachfrist ablaufen und Ihre Testkontoinformationen und -daten löschen lassen.

## <a name="expedited-deletion"></a>Beschleunigte Löschung

Für jedes Abonnement kann ein Abonnent den Microsoft-Support kontaktieren und eine beschleunigte Deaktivierung anfordern. Bei diesem Vorgang werden alle Benutzerdaten drei Tage, nachdem der Administrator den von Microsoft bereitgestellten Sperrcode eingegeben hat, gelöscht. Dazu gehören Daten in SharePoint Online und Exchange Online, die gesperrt oder in inaktiven Postfächern gespeichert sind.

Weitere Informationen zur beschleunigten Debereitstellung finden Sie unter [Kündigen Ihres Abonnements.](/microsoft-365/commerce/subscriptions/cancel-your-subscription)

## <a name="related-links"></a>Links zu verwandten Themen

- [Zerstörung von Daten](assurance-data-destruction.md)
- [Unveränderbarkeit in Office 365](assurance-data-immutability.md)
- [Löschen von Exchange Online-Daten](assurance-exchange-online-data-deletion.md)
- [Löschen von SharePoint Online-Daten](assurance-sharepoint-online-data-deletion.md)
