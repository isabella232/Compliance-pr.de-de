---
title: Netzwerksicherheit
description: Informationen zur Netzwerksicherheit in Microsoft 365
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
ms.openlocfilehash: 18f5bfa40fc8827ec840a764ae3224765aadae81156738fe30a51acd6ca244ab
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292762"
---
# <a name="network-security-overview"></a>Netzwerksicherheit (Übersicht)

## <a name="how-do-microsoft-online-services-secure-the-network-boundary"></a>Wie sichern Microsoft-Onlinedienste die Netzwerkgrenze?

Microsoft-Onlinedienste verwenden mehrere Strategien zum Sichern der Netzwerkgrenze, einschließlich der automatisierten Erkennung und Verhinderung von netzwerkbasierten Angriffen, spezialisierten Firewallgeräten und Exchange Online Protection (EOP) für Antispam- und Antischadsoftwareschutz. Darüber hinaus trennen Microsoft-Onlinedienste ihre Produktionsumgebungen in logisch isolierte Netzwerksegmente, wobei nur die erforderliche Kommunikation zwischen Segmenten zulässig ist. Der Netzwerkdatenverkehr wird mithilfe zusätzlicher Netzwerkfirewalls an Begrenzungspunkten gesichert, um Netzwerkangriffe zu erkennen, zu verhindern und zu mindern.

## <a name="how-do-microsoft-online-services-defend-against-ddos-attacks"></a>Wie schützen Microsoft-Onlinedienste vor DDoS-Angriffen?

Die große Internetpräsenz von Microsoft schützt sie vor den negativen Auswirkungen vieler verteilter Denial-of-Service (DDoS)-Angriffe. Verteilte Instanzen jedes Microsoft-Onlinediensts und mehrere Routen zu jedem Dienst begrenzen die Auswirkungen von DDoS-Angriffen auf das System. Diese Redundanz verbessert die Fähigkeit von Microsoft-Onlinediensten, DDoS-Angriffe aufzufangen, und erhöht den Zeitaufwand, um DDoS-Angriffe zu erkennen und zu mindern, bevor sie sich auf die Dienstverfügbarkeit auswirken.

Zusätzlich zur redundanten Systemarchitektur von Microsoft verwendet Microsoft komplexe Erkennungs- und Risikominderungstools, um auf DDoS-Angriffe zu reagieren. Spezielle Firewalls überwachen und löschen unerwünschten Datenverkehr, bevor sie die Grenze in das Netzwerk überschreiten, wodurch der Stress auf Systemen innerhalb der Netzwerkgrenze reduziert wird. Um unsere Clouddienste weiter zu schützen, verwendet Microsoft ein DDoS-Abwehrsystem, das als Teil der Microsoft Azure bereitgestellt wird. Das Azure DDoS-Abwehrsystem wurde entwickelt, um Angriffe von außen und von anderen Azure-Mandanten zu verhindern.

## <a name="how-does-microsoft-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Wie schützt Microsoft Benutzer vor Spam und Schadsoftware, die über Onlinedienste hochgeladen oder gesendet werden?

Microsoft Online services build antimalware protection into services that might be vectors for malicious code, such as Exchange Online and SharePoint Online. Exchange Online Protection (EOP) überprüft alle E-Mails und E-Mail-Anlagen beim Ein- und Verlassen des Systems auf Schadsoftware, um zu verhindern, dass infizierte Nachrichten und Anlagen zugestellt werden. Die erweiterte Spamfilterung wird automatisch auf eingehende und ausgehende Nachrichten angewendet, um zu verhindern, dass Kundenorganisationen Spam empfangen und senden. Diese Schutzebene schützt vor Angriffen, die unerwünschte oder nicht autorisierte E-Mails wie Phishingangriffe nutzen. SharePoint Online verwendet dasselbe Virenerkennungsmodul, um hochgeladene Dateien selektiv auf Schadsoftware zu überprüfen. Wenn eine Datei als infiziert markiert ist, können Benutzer die Datei nicht herunterladen oder synchronisieren, um Clientendpunkte zu schützen. Ebenso vergleicht Azure Hashes im Zusammenhang mit Dateien, die in Azure Storage hochgeladen wurden, mit diesen Hashes bekannter Schadsoftware. Wenn Übereinstimmungen gefunden werden, wird eine Warnung im Azure Security Center ausgelöst, in der eine Entscheidung über die Dringlichkeit der Warnung und deren Behebung getroffen wird.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Vorschriften & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Vorschriften und Zertifizierungen überprüft. Informationen zur Überprüfung von Steuerelementen im Zusammenhang mit der Netzwerksicherheit finden Sie in der folgenden Tabelle.

### <a name="azure-and-dynamics-365"></a>Azure und Dynamics 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1: Protokollierung von Sicherheitsereignissen <br> VM-3: Erkennung und Überwachung von Eindringversuchen <br> VM-4: Untersuchung bösartiger Ereignisse <br> VM-6: Überprüfung von Sicherheitsrisiken <br> VM-7: Netzwerkgerätekonfiguration <br> VM-8: Penetrationstests <br> VM-9: Protokollierung von Sicherheitsereignissen für Netzwerkgeräte <br> VM-13: Schutz vor Sicherheitsrisiken für Netzwerkgeräte | 31. März. 2021 |

### <a name="office-365"></a>Office 365

| **Externe Überwachungen** | **Section** | **Aktuelles Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-5: Denial-of-Service-Schutz <br> SC-7: Grenzschutz <br> SI-2: Fehlerbehebung <br> SI-3: Schutz vor bösartigem Code <br> SI-8: Spamschutz | 24. September 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Überprüfung von Sicherheitsrisiken | 24. Dezember 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Überprüfung von Sicherheitsrisiken <br> CA-45: Antischadsoftware | 24. Dezember 2020 |