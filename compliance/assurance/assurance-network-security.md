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
ms.openlocfilehash: c063460fdfba44265b3a1504a049a4772b484dff
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506693"
---
# <a name="network-security-overview"></a>Übersicht über die Netzwerksicherheit

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Wie sichert Microsoft 365 die Netzwerkgrenze?

Microsoft 365 verwendet mehrere Strategien zur Sicherung der Netzwerkgrenze, einschließlich der automatischen Erkennung und Verhinderung von netzwerkbasierten Angriffen, spezialisierten Firewall-Geräten und Exchange Online Schutz (EoP) für den Schutz vor Spam und Schadsoftware (Anti-Malware). Darüber hinaus trennt Microsoft 365 die Produktionsumgebung in logisch isolierte Netzwerksegmente, wobei nur die erforderliche Kommunikation zwischen den Segmenten zulässig ist. Der Netzwerkdatenverkehr wird mithilfe zusätzlicher Netzwerkfirewalls an Grenzpunkten gesichert, um Netzwerkangriffe zu erkennen, zu verhindern und zu mindern.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Wie schützt Microsoft 365 gegen DDoS-Angriffe?

Die große Internetpräsenz von Microsoft isoliert ihn vor den negativen Auswirkungen zahlreicher verteilter DDoS-Angriffe (Denial-of-Service). Verteilte Instanzen jedes Microsoft 365-Diensts und mehrere Routen zu den einzelnen Diensten begrenzen die Auswirkungen von DDoS-Angriffen auf das System. Diese Redundanz verbessert die Fähigkeit von Microsoft 365, DDoS-Angriffe zu absorbieren, und erhöht die verfügbare Zeit zum erkennen und verringern von DDoS-Angriffen, bevor Sie die Dienstverfügbarkeit beeinträchtigen.

Zusätzlich zur redundanten Systemarchitektur von Microsoft verwendet Microsoft hoch entwickelte Erkennungs-und Minderungs Tools, um auf DDoS-Angriffe zu reagieren. Spezielle Firewalls überwachen und löschen unerwünschten Datenverkehr, bevor Sie die Grenze in das Netzwerk überschreiten, wodurch sich die Spannung auf Systemen innerhalb der Netzwerkgrenze verringert. Um unsere Cloud-Dienste weiter zu schützen, verwendet Microsoft ein DDoS-Abwehrsystem, das im Rahmen von Microsoft Azure bereitgestellt wird. Das Azure DDoS-Abwehrsystem wurde entwickelt, um Angriffe von außen sowie von anderen Azure-Mandanten zu überstehen.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Wie schützt Microsoft 365 Benutzer vor Spam und Schadsoftware, die über Onlinedienste hochgeladen oder gesendet werden?

Microsoft 365 baut Schutz vor Schadsoftware in Diensten auf, die möglicherweise Vektoren für böswilligen Code wie Exchange Online und SharePoint Online sein können. Exchange Online Protection (EoP) scannt alle e-Mails und e-Mail-Anlagen auf Schadsoftware, wenn Sie das System betreten und beenden, und verhindert, dass infizierte Nachrichten und Anlagen zugestellt werden. Erweiterte Spamfilterung wird automatisch auf eingehende und ausgehende Nachrichten angewendet, um zu verhindern, dass Kundenorganisationen Spam empfangen und senden können. Diese Schutzebene schützt vor Angriffen, die unerwünschte oder nicht autorisierte e-Mails nutzen, beispielsweise Phishing-Angriffe. SharePoint Online verwendet das gleiche Viruserkennungsmodul, um hochgeladene Dateien selektiv auf Schadsoftware zu überprüfen. Wenn eine Datei als infiziert gekennzeichnet ist, wird verhindert, dass Benutzer die Datei herunterladen oder synchronisieren, um Clientendpunkte zu schützen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Verordnungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf die Einhaltung externer Bestimmungen und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Informationen zur Validierung von Steuerelementen im Zusammenhang mit der Netzwerksicherheit.

| **Externe Überprüfungen** | **Section** | **Letztes Berichtsdatum** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: Denial-of-Service-Schutz <br> SC-7: Grenzschutz <br> Si-2: Fehlerbehebung <br> Si-3: Schutz vor bösartigem Code <br> Si-8: Spam Schutz | 24. September 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27: Sicherheitsrisiko Überprüfung | 30. September 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27: Sicherheitsrisiko Überprüfung <br> CA-45: Anti-Malware | 30. September 2019 |