---
title: Verschlüsselung und Schlüsselverwaltung (Übersicht)
description: Informationen zur Verschlüsselung und Schlüsselverwaltung in Microsoft 365
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
ms.openlocfilehash: ca13c5dfb229acd46ef0dd027b537afc2ac20b5a
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787344"
---
# <a name="encryption-and-key-management-overview"></a>Verschlüsselung und Schlüsselverwaltung (Übersicht)

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Welche Rolle spielt verschlüsselung beim Schutz von Kundeninhalten?

Die meisten Microsoft Business Cloud Services sind multitenant, was bedeutet, dass Kundeninhalte auf derselben physischen Hardware wie andere Kunden gespeichert werden können. Um die Vertraulichkeit von Kundeninhalten zu schützen, verschlüsselt Microsoft 365 alle ruhen und übertragenen Daten mit einigen der stärksten und sichersten Verschlüsselungsprotokolle, die verfügbar sind.

Verschlüsselung ist kein Ersatz für starke Zugriffssteuerungen. Die Microsoft 365-Richtlinie zur Zugriffssteuerung von Zero Standing Access (ZSA) schützt Kundeninhalte vor unbefugtem Zugriff durch Microsoft-Mitarbeiter. Verschlüsselung ergänzt die Zugriffssteuerung, indem die Vertraulichkeit von Kundeninhalten unabhängig davon geschützt wird, wo sie gespeichert werden, und indem verhindert wird, dass Inhalte während der Übertragung zwischen Microsoft 365-Systemen oder zwischen Microsoft 365 und dem Kunden gelesen werden.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Wie verschlüsselt Microsoft 365 Ruhedaten?

Alle Kundeninhalte in Microsoft 365 sind durch eine oder mehrere Formen der Verschlüsselung geschützt. Microsoft Server verwenden BitLocker zum Verschlüsseln der Festplattenlaufwerke, die Kundeninhalte auf Volumeebene enthalten. Die von BitLocker bereitgestellte Verschlüsselung schützt Kundeninhalte im Falle von Ausfällungen in anderen Prozessen oder Steuerelementen (z. B. Zugriffssteuerung oder Recycling von Hardware), die zu einem nicht autorisierten physischen Zugriff auf Datenträger mit Kundeninhalten führen könnten.

Exchange Online, Microsoft Teams, SharePoint Online und OneDrive for Business verwenden auch die Dienstverschlüsselung auf Anwendungsebene, um Kundeninhalte zu verschlüsseln. Die Dienstverschlüsselung bietet Rechteschutz- und Verwaltungsfeatures sowie starken Verschlüsselungsschutz. Es ermöglicht auch die Trennung zwischen den Windows-Betriebssystemen und den Kundendaten, die von diesen Betriebssystemen gespeichert oder verarbeitet werden.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Wie verschlüsselt Microsoft 365 Daten bei der Übertragung?

Microsoft 365-Produkte und -Dienste verwenden starke Transportprotokolle wie TLS, um zu verhindern, dass nicht autorisierte Parteien Kundendaten abhören, während sie sich über ein Netzwerk bewegen. Beispiele für Daten bei der Übertragung sind E-Mail-Nachrichten, die gerade zugestellt werden, Unterhaltungen, die in einer Online besprechung stattfinden, oder Dateien, die zwischen Rechenzentren repliziert werden.

In Microsoft 365 werden Daten immer dann als "übertragen" betrachtet, wenn das Gerät eines Benutzers mit einem Microsoft Server kommuniziert oder ein Microsoft Server mit einem anderen Server kommuniziert. Exchange Online, SharePoint Online, Microsoft Teams und Office Online verwenden TLS, um sicherzustellen, dass Daten während der Übertragung vertraulich bleiben.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Wie verwaltet Microsoft 365 die für die Verschlüsselung verwendeten Schlüssel?

Eine starke Verschlüsselung ist nur so sicher wie die Schlüssel, die zum Verschlüsseln von Daten verwendet werden. Microsoft verwendet eigene Sicherheitszertifikate zum Verschlüsseln von TLS-Verbindungen für Daten bei der Übertragung. Bei ruhen den Daten werden BitLocker-geschützte Volumes mit einem vollständigen Volumeverschlüsselungsschlüssel verschlüsselt, der mit einem Volumemasterschlüssel verschlüsselt wird, der wiederum an das Trusted Platform Module (TPM) auf dem Server gebunden ist. BitLocker verwendet FIPS-konforme Algorithmen, um sicherzustellen, dass Verschlüsselungsschlüssel niemals im klarsten Gitter gespeichert oder über das Netzwerk gesendet werden.

Die Dienstverschlüsselung bietet eine zusätzliche Verschlüsselungsebene für ruhede Kundendaten in Exchange Online, Microsoft Teams, SharePoint Online und OneDrive for Business. Die Dienstverschlüsselung bietet Kunden zwei Optionen für die Verwaltung von Verschlüsselungsschlüsseln: von Microsoft verwaltete Schlüssel oder Kundenschlüssel. Bei Verwendung von von Microsoft verwalteten Schlüsseln generieren und speichern Microsoft 365-Dienste automatisch die für die Dienstverschlüsselung verwendeten Stammschlüssel.

Kunden mit Anforderungen zur Steuerung ihrer eigenen Stammverschlüsselungsschlüssel können die Dienstverschlüsselung mit Customer Key nutzen. Mithilfe von Customer Key können Kunden ihre eigenen kryptografischen Schlüssel mithilfe eines lokalen Hardwaredienstmoduls (Hardware Service Module, HSM) oder Azure Key Vault (AKV) generieren. Kundenstammschlüssel werden in AKV gespeichert, wo sie als Stamm einer der Schlüsselbunde verwendet werden können, die Kundenpostfachdaten oder -dateien verschlüsselt. Auf Kundenstammschlüssel kann nur indirekt durch den Microsoft 365-Dienstcode für die Datenverschlüsselung zugegriffen werden, und microsoft-Mitarbeiter können nicht direkt darauf zugreifen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Bestimmungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf Einhaltung externer Bestimmungen und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit Verschlüsselung und Schlüsselverwaltung.

| **Externe Überwachungen** | **Section** | **Datum des letzten Berichts** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: Vertraulichkeit und Integrität der Übertragung <br> SC-13: Verwendung von Kryptografie <br> SC-28: Schutz ruherer Informationen <br>  | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Kryptografische Steuerelemente <br> A.18.1.5: Kryptografische Steuerelemente | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Kryptografische Steuerelemente <br> A.18.1.5: Kryptografische Steuerelemente | Februar 22, 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Verschlüsselung von personenbezogenen Informationen, die über öffentliche Datenübertragungsnetzwerke übertragen werden | Februar 22, 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: Verschlüsselung bei der Übertragung von Daten <br> CA-54: Verschlüsselung von Ruhedaten <br> CA-62: Verschlüsselung von Kundenschlüsselpostfächern <br> CA-63: Löschen von Kundenschlüsseldaten <br> CA-64: Kundenschlüssel | 24. Dezember 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: Kundenverschlüsselungsschlüssel <br> CUEC-17: Kundenschlüsseltresor <br>  CUEC-18: Drehung von Kundenschlüsseln| 24. Dezember 2020 |
