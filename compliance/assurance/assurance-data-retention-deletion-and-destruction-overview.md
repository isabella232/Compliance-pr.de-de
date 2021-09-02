---
title: Aufbewahrung, Löschung und Vernichtung von Daten in Microsoft 365
description: Eine Übersicht über die Microsoft-Richtlinien für Microsoft 365 zur Aufbewahrung, Löschung und Vernichtung von Daten.
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
ms.openlocfilehash: c851b235a70104720457d08c51529ee7b25c65e4
ms.sourcegitcommit: 1fd50ef5f165228109a3f2f0aef4b0c2aa59b2ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2021
ms.locfileid: "58862355"
---
# <a name="data-retention-deletion-and-destruction-in-microsoft-365"></a>Aufbewahrung, Löschung und Vernichtung von Daten in Microsoft 365

Microsoft verfügt über eine Datenverarbeitungsstandardrichtlinie für Microsoft 365, die angibt, wie lange Kundendaten nach der Löschung aufbewahrt werden. Es gibt in der Regel zwei Szenarien, in denen Kundendaten gelöscht werden:

- **Aktive Löschung:** Der Mandant verfügt über ein aktives Abonnement, und ein Benutzer oder Administrator löscht Daten, oder Administratoren löschen einen Benutzer.
- **Passive Löschung:** Das Mandantenabonnement endet.

## <a name="data-retention"></a>Datenaufbewahrung

Für jedes dieser Löschszenarien zeigt die folgende Tabelle den maximalen Datenaufbewahrungszeitraum nach Datenkategorie und Klassifizierung:

| Datenkategorie | Datenklassifikation | Beschreibung | Beispiele | Aufbewahrungszeitraum |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| Kundendaten | Kundeninhalte| Inhalte, die direkt von Administratoren und Benutzern bereitgestellt/erstellt werden <br><br> Enthält alle Text-, Sound-, Video-, Bilddateien und Software, die in Microsoft-Rechenzentren erstellt und gespeichert werden, wenn die Dienste in Microsoft 365 | Beispiele für die am häufigsten verwendeten Microsoft 365 Anwendungen, mit denen Benutzer Daten erstellen können, sind Word, Excel, PowerPoint, Outlook und OneNote <br><br> Kundeninhalte umfassen auch vom Kunden bereitgestellte geheime Schlüssel (Kennwörter, Zertifikate, Verschlüsselungsschlüssel, Speicherschlüssel). | **Aktives Löschszenario:** höchstens 30 Tage <br><br> **Passives Löschszenario:** höchstens 180 Tage |
| Kundendaten | Informationen zur Identifizierung von Endbenutzern (END USER Identifiable Information, EUII) | Daten, die den Benutzer eines Microsoft-Diensts identifizieren oder verwenden können. EUII enthält keine Kundeninhalte | Benutzername oder Anzeigename (DOMAIN\UserName) <br><br> Benutzerprinzipalname (name@domain) <br><br>  Benutzerspezifische IP-Adressen | **Aktives Löschszenario:** höchstens 180 Tage (nur eine Mandantenadministratoraktion) <br><br> **Passives Löschszenario:** höchstens 180 Tage |
| Persönliche Daten <br> (Daten, die nicht in Kundendaten enthalten sind) | Pseudonyme Bezeichner für Endbenutzer (EUPI) | Ein von Microsoft erstellter Bezeichner, der an den Benutzer eines Microsoft-Diensts gebunden ist. In Kombination mit anderen Informationen, z. B. einer Zuordnungstabelle, identifiziert EUPI den Endbenutzer. <br><br> EUPI enthält keine Informationen, die vom Kunden hochgeladen oder erstellt wurden | Benutzer-GUIDs, PUIDs oder SIDs <br><br> Sitzungs-IDs | **Aktives Löschszenario:** höchstens 30 Tage <br><br> **Passives Löschszenario:** höchstens 180 Tage |

## <a name="subscription-retention"></a>Abonnementaufbewahrung

In der Laufzeit eines aktiven Abonnements kann ein Abonnent auf Kundendaten zugreifen, diese extrahieren oder löschen, die in Microsoft 365 gespeichert sind. Wenn ein kostenpflichtiges Abonnement endet oder gekündigt wird, speichert Microsoft Kundendaten, die in Microsoft 365 in einem Konto mit beschränkter Funktion gespeichert sind, 90 Tage lang, damit der Abonnent die Daten extrahieren kann. Nach Ablauf des 90-tägigen Aufbewahrungszeitraums deaktiviert Microsoft das Konto und löscht die Kundendaten. Spätestens 180 Tage nach Ablauf oder Kündigung eines Microsoft 365-Abonnements deaktiviert Microsoft das-Konto und löscht alle Kundendaten daraus. Sobald der maximale Aufbewahrungszeitraum für Daten abgelaufen ist, werden die Daten kommerziell nicht mehr wiederhergestellt.

Bei einer kostenlosen Testversion wechselt Ihr Konto in den meisten Ländern und Regionen 30 Tage lang in den Status "Kulanz". Innerhalb dieser Nachfrist können Sie Microsoft 365 kaufen. Wenn Sie sich entscheiden, Microsoft 365 nicht zu kaufen, können Sie entweder Ihre Testversion kündigen oder die Nachfrist ablaufen und Ihre Testkontoinformationen und -daten löschen lassen.

## <a name="expedited-deletion"></a>Beschleunigtes Löschen

Für jedes Abonnement kann ein Abonnent den Microsoft-Support kontaktieren und eine beschleunigte Deaktivierung anfordern. Bei diesem Vorgang werden alle Benutzerdaten drei Tage, nachdem der Administrator den von Microsoft bereitgestellten Sperrcode eingegeben hat, gelöscht. Dazu gehören Daten in SharePoint Online und Exchange Online, die gesperrt oder in inaktiven Postfächern gespeichert sind.

Weitere Informationen zur beschleunigten Debereitstellung finden Sie unter [Kündigen Ihres Abonnements.](/microsoft-365/commerce/subscriptions/cancel-your-subscription)

## <a name="related-links"></a>Links zu verwandten Themen

- [Vernichtung von Geräten, die Daten tragen](assurance-data-bearing-device-destruction.md)
- [Unveränderbarkeit in Office 365](assurance-data-immutability.md)
- [Löschen von Exchange Online-Daten](assurance-exchange-online-data-deletion.md)
- [Löschen von SharePoint Online-Daten](assurance-sharepoint-online-data-deletion.md)
