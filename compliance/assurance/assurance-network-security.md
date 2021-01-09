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
ms.openlocfilehash: e246cc3c84a17fe697baea29eda285599832b0fa
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787428"
---
# <a name="network-security-overview"></a>Netzwerksicherheit (Übersicht)

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Wie sichert Microsoft 365 die Netzwerkgrenze?

Microsoft 365 verwendet mehrere Strategien zum Sichern der Netzwerkgrenze, einschließlich der automatisierten Erkennung und Verhinderung von netzwerkbasierten Angriffen, spezialisierten Firewallgeräten und Exchange Online Protection (EOP) für Antispam- und Ansoftwareschutz. Darüber hinaus trennt Microsoft 365 seine Produktionsumgebung in logisch isolierte Netzwerksegmente, mit der nur die erforderliche Kommunikation zwischen den Segmenten zulässig ist. Der Netzwerkdatenverkehr wird durch zusätzliche Netzwerkfirewalls an Grenzpunkten gesichert, um Netzwerkangriffe zu erkennen, zu verhindern und zu mindern.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Wie wehrt sich Microsoft 365 gegen DDoS-Angriffe?

Die große Internetpräsenz von Microsoft isoliert sie vor den negativen Auswirkungen vieler verteilter Denial-of-Service-Angriffe (DDoS). Verteilte Instanzen jedes Microsoft 365-Diensts und mehrere Routen zu jedem Dienst begrenzen die Auswirkungen von DDoS-Angriffen auf das System. Diese Redundanz verbessert die Fähigkeit von Microsoft 365, DDoS-Angriffe aufzufangen, und erhöht die Verfügbare Zeit zum Erkennen und Verringern von DDoS-Angriffen, bevor sie sich auf die Dienstverfügbarkeit auswirken.

Zusätzlich zur redundanten Systemarchitektur von Microsoft verwendet Microsoft komplexe Erkennungs- und Risikominderungstools, um auf DDoS-Angriffe zu reagieren. Spezielle Firewalls überwachen unerwünschten Datenverkehr und legen ihn ab, bevor er die Grenze in das Netzwerk überquert, wodurch die Belastung von Systemen innerhalb der Netzwerkgrenze reduziert wird. Um unsere Clouddienste weiter zu schützen, verwendet Microsoft ein DDoS-Abwehrsystem, das als Teil von Microsoft Azure bereitgestellt wird. Das Azure DDoS-Abwehrsystem ist darauf ausgelegt, Angriffe von außen und von anderen Azure-Mandanten zu verhindern.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Wie schützt Microsoft 365 Benutzer vor Spam und Schadsoftware, die über Onlinedienste hochgeladen oder gesendet werden?

Microsoft 365 erstellt Schutz vor Schadsoftware in Diensten, die Vektoren für bösartigen Code sein können, z. B. Exchange Online und SharePoint Online. Exchange Online Protection (EOP) überprüft alle E-Mails und E-Mail-Anlagen auf Schadsoftware, wenn sie das System betreten und verlassen, um zu verhindern, dass infizierte Nachrichten und Anlagen zugestellt werden. Die erweiterte Spamfilterung wird automatisch auf eingehende und ausgehende Nachrichten angewendet, um zu verhindern, dass Kundenorganisationen Spam empfangen und senden. Diese Schutzebene bietet Schutz vor Angriffen, die unerwünschte oder nicht autorisierte E-Mails nutzen, z. B. Phishing-Angriffe. SharePoint Online verwendet dasselbe Virenerkennungsmodul, um hochgeladene Dateien selektiv auf Schadsoftware zu überprüfen. Wenn eine Datei als infiziert gekennzeichnet ist, werden Benutzer am Herunterladen oder Synchronisieren der Datei gehindert, um Clientendpunkte zu schützen.

## <a name="related-external-regulations--certifications"></a>Verwandte externe Bestimmungen & Zertifizierungen

Die Onlinedienste von Microsoft werden regelmäßig auf Einhaltung externer Bestimmungen und Zertifizierungen überprüft. In der folgenden Tabelle finden Sie Eine Überprüfung der Kontrollen im Zusammenhang mit der Netzwerksicherheit.

| **Externe Überwachungen** | **Section** | **Datum des letzten Berichts** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: Schutz vor Dienstverweigerung <br> SC-7: Grenzschutz <br> SI-2: Behebung von Fehlern <br> SI-3: Schutz vor bösartigem Code <br> SI-8: Spamschutz | 24. September 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Sicherheitsrisikoprüfung | 24. Dezember 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Sicherheitsrisikoprüfung <br> CA-45: Ansoftware | 24. Dezember 2020 |