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
hideEdit: true
ms.openlocfilehash: 5e46fdb5ddc3b1b80df0bcadf9054b9353a0dc8e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088644"
---
# <a name="encryption-and-key-management-overview"></a>Verschlüsselung und Schlüsselverwaltung (Übersicht)

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Welche Rolle spielt die Verschlüsselung beim Schutz von Kundeninhalten?

Die meisten Microsoft Business Cloud Services sind mehrinstanzenfähig, d. h., Kundeninhalte können auf der gleichen physischen Hardware wie die anderer Kunden gespeichert werden. Um die Vertraulichkeit von Kundeninhalten zu schützen, verschlüsselt Microsoft 365 alle ruhenden daten und während der Übertragung mit einigen der stärksten und sichersten Verschlüsselungsprotokolle, die verfügbar sind.

Verschlüsselung ist kein Ersatz für starke Zugriffssteuerungen. die Microsoft 365-Richtlinie zur Zugriffssteuerung von Zero Standing Access (ZSA) schützt Kundeninhalte vor unbefugtem Zugriff durch Microsoft-Mitarbeiter. Die Verschlüsselung ergänzt die Zugriffssteuerung, indem die Vertraulichkeit von Kundeninhalten unabhängig davon geschützt wird, wo sie gespeichert sind, und indem verhindert wird, dass Inhalte während der Übertragung zwischen Microsoft 365 Systemen oder zwischen Microsoft 365 und dem Kunden gelesen werden.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Wie verschlüsselt Microsoft 365 ruhenden Daten?

Alle Kundeninhalte in Microsoft 365 werden durch eine oder mehrere Formen der Verschlüsselung geschützt. Microsoft-Server verwenden BitLocker zum Verschlüsseln der Datenträgerlaufwerke, die Kundeninhalte auf Volumeebene enthalten. Die von BitLocker bereitgestellte Verschlüsselung schützt Kundeninhalte bei Ausläufen in anderen Prozessen oder Steuerelementen (z. B. Zugriffssteuerung oder Wiederverwendung von Hardware), die zu unbefugtem physischen Zugriff auf Datenträger mit Kundeninhalten führen können.

Exchange Online, Microsoft Teams, SharePoint Online und OneDrive for Business auch die Dienstverschlüsselung auf anwendungsebene verwenden, um Kundeninhalte zu verschlüsseln. Die Dienstverschlüsselung bietet Rechteschutz- und Verwaltungsfunktionen zusätzlich zu starkem Verschlüsselungsschutz. Es ermöglicht auch die Trennung zwischen Windows Betriebssystemen und den Kundendaten, die von diesen Betriebssystemen gespeichert oder verarbeitet werden.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Wie verschlüsselt Microsoft 365 Daten während der Übertragung?

Microsoft 365 Produkte und Dienste starke Transportprotokolle wie TLS verwenden, um zu verhindern, dass unbefugte Parteien Kundendaten abhören, während sie über ein Netzwerk übertragen werden. Beispiele für Daten während der Übertragung sind E-Mail-Nachrichten, die gerade übermittelt werden, Unterhaltungen, die in einer Onlinebesprechung stattfinden, oder Dateien, die zwischen Rechenzentren repliziert werden.

In Microsoft 365 werden Daten als "während der Übertragung" betrachtet, wenn das Gerät eines Benutzers mit einem Microsoft-Server kommuniziert oder ein Microsoft-Server mit einem anderen Server kommuniziert. Exchange Online, SharePoint Online, Microsoft Teams und Office Online verwenden TLS, um sicherzustellen, dass Daten während der Übertragung vertraulich bleiben.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Wie verwaltet Microsoft 365 die für die Verschlüsselung verwendeten Schlüssel?

Eine starke Verschlüsselung ist nur so sicher wie die Schlüssel, die zum Verschlüsseln von Daten verwendet werden. Microsoft verwendet eigene Sicherheitszertifikate, um TLS-Verbindungen für Daten während der Übertragung zu verschlüsseln. Bei ruhenden Daten werden BitLocker-geschützte Volumes mit einem vollständigen Volumeverschlüsselungsschlüssel verschlüsselt, der mit einem Volumehauptschlüssel verschlüsselt wird, der wiederum an das Trusted Platform Module (TPM) auf dem Server gebunden ist. BitLocker verwendet FIPS-kompatible Algorithmen, um sicherzustellen, dass Verschlüsselungsschlüssel niemals im Klartext gespeichert oder über das Kabel gesendet werden.

Die Dienstverschlüsselung bietet eine zusätzliche Verschlüsselungsebene für ruhenden Kundendaten in Exchange Online, Microsoft Teams, SharePoint Online und OneDrive for Business. Die Dienstverschlüsselung bietet Kunden zwei Optionen für die Verwaltung von Verschlüsselungsschlüsseln: von Microsoft verwaltete Schlüssel oder Kundenschlüssel. Bei Verwendung von von Microsoft verwalteten Schlüsseln generieren Microsoft 365 Dienste automatisch die für die Dienstverschlüsselung verwendeten Stammschlüssel und speichern sie sicher.

Kunden mit Anforderungen zum Steuern ihrer eigenen Stammverschlüsselungsschlüssel können die Dienstverschlüsselung mit Customer Key nutzen. Mit Customer Key können Kunden ihre eigenen kryptografischen Schlüssel entweder mit einem lokalen Hardware Service Module (HSM) oder Azure Key Vault (AKV) generieren. Kundenstammschlüssel werden in AKV gespeichert, wo sie als Stamm einer der Schlüsselbunde verwendet werden können, die Kundendaten oder -dateien verschlüsseln. Auf Kundenstammschlüssel kann nur indirekt über Microsoft 365 Dienstcode für die Datenverschlüsselung zugegriffen werden, und microsoft-Mitarbeiter können nicht direkt darauf zugreifen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit Verschlüsselung und Schlüsselverwaltung finden Sie in der folgenden Tabelle.

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: Vertraulichkeit und Integrität der Übertragung <br> SC-13: Verwendung von Kryptografie <br> SC-28: Schutz ruhenden Informationen <br>  | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Kryptografische Steuerelemente <br> A.18.1.5: Kryptografische Steuerelemente | 20. April 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Kryptografische Steuerelemente <br> A.18.1.5: Kryptografische Steuerelemente | 20. April 2021 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Erklärung zur Anwendbarkeit](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Verschlüsselung von personenbezogenen Informationen, die über öffentliche Datenübertragungsnetzwerke übertragen werden | 20. April 2021 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: Verschlüsselung während der Übertragung von Daten <br> CA-54: Daten-at-Rest-Verschlüsselung <br> CA-62: Verschlüsselung von Kundenschlüsselpostfächern <br> CA-63: Löschen von Kundendaten <br> CA-64: Kundenschlüssel | 24. Dezember 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: Kundenverschlüsselungsschlüssel <br> CUEC-17: Kundenschlüsseltresor <br>  CUEC-18: Kundenschlüsselrotation| 24. Dezember 2020 |
