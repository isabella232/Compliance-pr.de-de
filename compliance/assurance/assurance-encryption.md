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
ms.openlocfilehash: 96a3871657dc1e6021949ca9fc2376df382fe15b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506869"
---
# <a name="encryption-and-key-management-overview"></a>Verschlüsselung und Schlüsselverwaltung (Übersicht)

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Welche Rolle spielt die Verschlüsselung beim Schutz von Kundeninhalten?

Die meisten Microsoft Business Cloud-Dienste sind Multimandanten, was bedeutet, dass Kunden Inhalte möglicherweise auf derselben physischen Hardware wie die anderer Kunden gespeichert werden. Um die Vertraulichkeit von Kundeninhalten zu schützen, verschlüsselt Microsoft 365 alle Daten im Ruhezustand und in der Übertragung mit einigen der stärksten und sichersten Verschlüsselungsprotokolle, die verfügbar sind.

Die Verschlüsselung ist kein Ersatz für starke Zugriffssteuerungen. Die Zugriffssteuerungsrichtlinie von Microsoft 365 von "Zero standing Access (") schützt Benutzer Inhalte vor nicht autorisiertem Zugriff durch Microsoft-Mitarbeiter. Die Verschlüsselung ergänzt die Zugriffssteuerung, indem Sie die Vertraulichkeit von Kundeninhalten überall dort schützt, wo Sie gespeichert wird, und verhindert, dass Inhalte während der Übertragung zwischen Microsoft 365-Systemen oder zwischen Microsoft 365 und dem Kunden gelesen werden.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Wie verschlüsseln Microsoft 365 Data-at-Rest?

Alle Kunden Inhalte in Microsoft 365 werden durch eine oder mehrere Formen der Verschlüsselung geschützt. Microsoft-Server verwenden BitLocker zum Verschlüsseln von Datenträgerlaufwerken, die Kunden Inhalte auf der Lautstärke Ebene enthalten. Die von BitLocker bereitgestellte Verschlüsselung schützt Kunden Inhalte im Falle von Ausfällen in anderen Prozessen oder Steuerelementen (beispielsweise Zugriffssteuerung oder Wiederverwendung von Hardware), die zu unbefugtem Zugriff auf Datenträger mit Kundeninhalten führen könnten.

Exchange Online, Microsoft Teams, SharePoint Online und OneDrive für Unternehmen verwenden auch die Dienst Verschlüsselung auf der Anwendungsebene, um Kunden Inhalte zu verschlüsseln. Die Dienst Verschlüsselung bietet Rechte Schutz-und Verwaltungsfunktionen über einen starken Verschlüsselungsschutz hinaus. Sie ermöglicht außerdem eine Trennung zwischen Windows-Betriebssystemen und den Kundendaten, die von diesen Betriebssystemen gespeichert oder verarbeitet werden.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Wie verschlüsseln Microsoft 365 Daten in Transit?

Microsoft 365-Produkte und-Dienste verwenden starke Transportprotokolle wie TLS, um zu verhindern, dass nicht autorisierte Personen bei der Verschiebung über ein Netzwerk auf Kundendaten abhören. Beispiele für Daten in Transit sind e-Mail-Nachrichten, die gerade zugestellt werden, Unterhaltungen, die in einer Onlinebesprechung stattfinden, oder Dateien, die zwischen den Rechenzentren repliziert werden.

In Microsoft 365 werden Daten als "in der Übertragung" betrachtet, wenn das Gerät eines Benutzers mit einem Microsoft-Server kommuniziert oder ein Microsoft-Server mit einem anderen Server kommuniziert. Exchange Online, SharePoint Online, Microsoft Teams und Office Online alle verwenden TLS, um sicherzustellen, dass die Daten während der Übertragung vertraulich bleiben.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Wie verwaltet Microsoft 365 die für die Verschlüsselung verwendeten Schlüssel?

Die starke Verschlüsselung ist nur so sicher wie die Schlüssel, die zum Verschlüsseln von Daten verwendet werden. Microsoft verwendet eigene Sicherheitszertifikate zum Verschlüsseln von TLS-Verbindungen für Daten in Transit. Bei Data-at-Rest-Datenträgern werden mit BitLocker geschützte Volumes mit einem vollständigen Verschlüsselungsschlüssel verschlüsselt, der mit einem Volumen Masterschlüssel verschlüsselt ist, der wiederum an das TPM (Trusted Platform Module) auf dem Server gebunden ist. BitLocker verwendet FIPS-konforme Algorithmen, um sicherzustellen, dass Verschlüsselungsschlüssel nie im Klartext gespeichert oder über den Draht gesendet werden.

Die Dienst Verschlüsselung stellt eine zusätzliche Verschlüsselungsebene für Kundendaten bereit, die in Exchange Online, Microsoft Teams, SharePoint Online und OneDrive für Unternehmen unterstützt werden. Die Dienst Verschlüsselung bietet Kunden zwei Optionen für die Verschlüsselungsschlüsselverwaltung: von Microsoft verwaltete Schlüssel oder Kundenschlüssel. Bei Verwendung von von Microsoft verwalteten Tasten werden die für die Dienst Verschlüsselung verwendeten Stammschlüssel von Microsoft 365-Diensten automatisch generiert und sicher gespeichert.

Kunden mit Anforderungen zur Steuerung Ihrer eigenen Stamm Verschlüsselungsschlüssel können die Dienst Verschlüsselung mit dem Kundenschlüssel nutzen. Mithilfe des Kunden Schlüssels können kundeneigene kryptografische Schlüssel mithilfe eines lokalen Hardware Dienst Moduls (HSM) oder eines Azure Key Vault (AKV) erstellen. Kundenstamm Schlüssel werden in AKV gespeichert, wo Sie als Stamm einer der keychains verwendet werden können, die Kunden Postfachdaten oder-Dateien verschlüsseln. Auf Kundenstamm Schlüssel kann nur indirekt durch Microsoft 365-Dienstcode für die Datenverschlüsselung zugegriffen werden, und es kann nicht direkt von Microsoft-Mitarbeitern darauf zugegriffen werden.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Verordnungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Bestimmungen und Zertifizierungen überprüft. In der folgenden Tabelle erhalten Sie Informationen zur Validierung von Steuerelementen im Zusammenhang mit Verschlüsselung und Schlüsselverwaltung.

| **Externe Überprüfungen** | **Section** | **Letztes Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: Vertraulichkeit und Integrität der Übertragung <br> SC-13: Verwenden von Kryptografie <br> SC-28: Schutz von Informationen im Ruhezustand <br>  | 24. September 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: kryptografische Steuerelemente <br> A. 18.1.5: kryptografische Steuerelemente | Februar 22, 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: kryptografische Steuerelemente <br> A. 18.1.5: kryptografische Steuerelemente | Februar 22, 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Anwendungsbeschreibung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Zertifizierung](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 11.6: Verschlüsselung von PII, die über öffentliche Daten Übertragungsnetzwerke übertragen werden | Februar 22, 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-44: Verschlüsselung mit Daten in Transit <br> CA-54: Data-at-Rest-Verschlüsselung <br> CA-62: Verschlüsselung von Kundenschlüssel Postfächern <br> CA-63: Löschung von Kundenschlüssel Daten <br> CA-64: Kundenschlüssel | 30. September 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-16: Kunden Verschlüsselungsschlüssel <br> CUEC-17: Kundenschlüssel Depot <br>  CUEC-18: Kundenschlüssel Rotation| 30. September 2019 |
