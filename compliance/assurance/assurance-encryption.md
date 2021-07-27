---
title: Verschlüsselung und Schlüsselverwaltung (Übersicht)
description: Erfahren Sie mehr über Verschlüsselung und Schlüsselverwaltung in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: c746f54081da90154efa22238e38e4a27185b530
ms.sourcegitcommit: 9f2132a2c723ddc25686c744caf1c9a8eadbb56c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/27/2021
ms.locfileid: "53596513"
---
# <a name="encryption-and-key-management-overview"></a>Verschlüsselung und Schlüsselverwaltung (Übersicht)

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Welche Rolle spielt die Verschlüsselung beim Schutz von Kundeninhalten?

Die meisten Microsoft Business Cloud Services sind mehrinstanzenfähig, d. h., Kundeninhalte können auf der gleichen physischen Hardware wie andere Kunden gespeichert werden. Um die Vertraulichkeit von Kundeninhalten zu schützen, verschlüsseln Microsoft-Onlinedienste alle ruhenden daten und während der Übertragung mit einigen der stärksten und sichersten Verschlüsselungsprotokolle, die verfügbar sind.

Verschlüsselung ist kein Ersatz für starke Zugriffssteuerungen. Die Microsoft-Richtlinie zur Zugriffssteuerung von Zero Standing Access (ZSA) schützt Kundeninhalte vor unbefugtem Zugriff durch Microsoft-Mitarbeiter. Die Verschlüsselung ergänzt die Zugriffssteuerung, indem die Vertraulichkeit von Kundeninhalten unabhängig davon geschützt wird, wo sie gespeichert werden, und indem verhindert wird, dass Inhalte während der Übertragung zwischen Microsoft-Onlinedienstsystemen oder zwischen Microsoft-Onlinediensten und dem Kunden gelesen werden.

## <a name="how-do-microsoft-online-services-encrypt-data-at-rest"></a>Wie verschlüsseln Microsoft-Onlinedienste ruhenden Daten?

Alle Kundeninhalte in Microsoft-Onlinediensten sind durch eine oder mehrere Formen der Verschlüsselung geschützt. Microsoft-Server verwenden BitLocker zum Verschlüsseln der Datenträgerlaufwerke, die Kundeninhalte auf Volumeebene enthalten. Die von BitLocker bereitgestellte Verschlüsselung schützt Kundeninhalte, wenn bei anderen Prozessen oder Steuerelementen (z. B. Zugriffssteuerung oder Wiederverwendung von Hardware) Fehler aufgetreten sind, die zu einem nicht autorisierten physischen Zugriff auf Datenträger mit Kundeninhalten führen können.

Zusätzlich zur Verschlüsselung auf Volumenebene verwenden Microsoft-Onlinedienste die Dienstverschlüsselung auf der Anwendungsebene, um Kundeninhalte zu verschlüsseln. Die Dienstverschlüsselung bietet Rechteschutz- und Verwaltungsfunktionen zusätzlich zu starkem Verschlüsselungsschutz. Es ermöglicht auch die Trennung zwischen Windows Betriebssystemen und den Kundendaten, die von diesen Betriebssystemen gespeichert oder verarbeitet werden.

## <a name="how-do-microsoft-online-services-encrypt-data-in-transit"></a>Wie verschlüsseln Microsoft-Onlinedienste Daten während der Übertragung?

Microsoft Online services use strong transport protocols, such as TLS, to prevent unauthorized parties from eavesdropping on customer data while it moves over a network. Beispiele für Daten während der Übertragung sind E-Mail-Nachrichten, die gerade übermittelt werden, Unterhaltungen, die in einer Onlinebesprechung stattfinden, oder Dateien, die zwischen Rechenzentren repliziert werden.

Bei Microsoft-Onlinediensten werden Daten immer dann als "während der Übertragung" betrachtet, wenn das Gerät eines Benutzers mit einem Microsoft-Server kommuniziert oder ein Microsoft-Server mit einem anderen Server kommuniziert.

## <a name="how-do-microsoft-online-services-manage-the-keys-used-for-encryption"></a>Wie verwalten Microsoft-Onlinedienste die für die Verschlüsselung verwendeten Schlüssel?

Eine starke Verschlüsselung ist nur so sicher wie die Schlüssel, die zum Verschlüsseln von Daten verwendet werden. Microsoft verwendet eigene Sicherheitszertifikate, um TLS-Verbindungen für Daten während der Übertragung zu verschlüsseln. Bei ruhenden Daten werden BitLocker-geschützte Volumes mit einem vollständigen Volumeverschlüsselungsschlüssel verschlüsselt, der mit einem Volumehauptschlüssel verschlüsselt wird, der wiederum an das Trusted Platform Module (TPM) auf dem Server gebunden ist. BitLocker verwendet FIPS-kompatible Algorithmen, um sicherzustellen, dass Verschlüsselungsschlüssel niemals im Klartext gespeichert oder über das Kabel gesendet werden.

Die Dienstverschlüsselung bietet eine weitere Verschlüsselungsebene für ruhenden Kundendaten, sodass Kunden zwei Optionen für die Verwaltung von Verschlüsselungsschlüsseln haben: von Microsoft verwaltete Schlüssel oder Customer Key. Bei Verwendung von von Microsoft verwalteten Schlüsseln generieren und speichern Microsoft-Onlinedienste automatisch die für die Dienstverschlüsselung verwendeten Stammschlüssel und speichern sie sicher.

Kunden mit Anforderungen zum Steuern ihrer eigenen Stammverschlüsselungsschlüssel können die Dienstverschlüsselung mit Kundenschlüssel verwenden. Mit Customer Key können Kunden ihre eigenen kryptografischen Schlüssel entweder mit einem lokalen Hardware Service Module (HSM) oder Azure Key Vault (AKV) generieren. Kundenstammschlüssel werden in AKV gespeichert, wo sie als Stamm einer der Schlüsselbunde verwendet werden können, die Kundendaten oder -dateien verschlüsseln. Auf Kundenstammschlüssel kann nur indirekt über Microsoft-Onlinedienstcode für die Datenverschlüsselung zugegriffen werden, und microsoft-Mitarbeiter können nicht direkt darauf zugreifen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit Verschlüsselung und Schlüsselverwaltung.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Kryptografische Steuerelemente <br> A.18.1.5: Kryptografische Steuerelemente | 2. Dezember 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Kryptografische Steuerelemente <br> A.18.1.5: Kryptografische Steuerelemente | 2. Dezember 2020 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Verschlüsselung von personenbezogenen Informationen, die über öffentliche Datenübertragungsnetzwerke übertragen werden | 2. Dezember 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | DS-1: Sichere Speicherung kryptografischer Zertifikate und Schlüssel <br> DS-2: Kundendaten werden während der Übertragung verschlüsselt <br> DS-3: Interne Kommunikation von Azure-Komponenten, die während der Übertragung verschlüsselt sind <br> DS-4: Kryptografische Steuerelemente und Verfahren | 31. März 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-8: Vertraulichkeit und Integrität der Übertragung <br> SC-13: Verwendung von Kryptografie <br> SC-28: Schutz ruhenden Informationen <br>  | 24. September 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Kryptografische Steuerelemente <br> A.18.1.5: Kryptografische Steuerelemente | 20. April 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Verschlüsselung von personenbezogenen Informationen, die über öffentliche Datenübertragungsnetzwerke übertragen werden | 20. April 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: Verschlüsselung während der Übertragung von Daten <br> CA-54: Daten-at-Rest-Verschlüsselung <br> CA-62: Verschlüsselung von Kundenschlüsselpostfächern <br> CA-63: Löschen von Kundendaten <br> CA-64: Kundenschlüssel | 24. Dezember 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: Kundenverschlüsselungsschlüssel <br> CUEC-17: Kundenschlüsseltresor <br>  CUEC-18: Kundenschlüsselrotation| 24. Dezember 2020 |
