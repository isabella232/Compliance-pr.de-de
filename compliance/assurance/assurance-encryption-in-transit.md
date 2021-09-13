---
title: Verschlüsselung für Daten während der Übertragung
description: In diesem Artikel finden Sie eine kurze Erläuterung dazu, wie Microsoft Microsoft 365 Kundendaten während der Übertragung verschlüsselt.
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ebeface33b0d5ba419773c13305c277d681e8400
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159075"
---
# <a name="encryption-for-data-in-transit"></a>Verschlüsselung für Daten während der Übertragung

Zusätzlich zum Schutz von ruhenden Kundendaten verwendet Microsoft Verschlüsselungstechnologien, um Kundendaten während der Übertragung zu schützen. Daten werden übertragen:

- wenn ein Clientcomputer mit einem Microsoft-Server kommuniziert;
- wenn ein Microsoft-Server mit einem anderen Microsoft-Server kommuniziert; Und
- wenn ein Microsoft-Server mit einem Nicht-Microsoft-Server kommuniziert (z. B. Exchange Online E-Mails an einen E-Mail-Server eines Drittanbieters zuzustellen).

Die Kommunikation zwischen Rechenzentren zwischen Microsoft-Servern erfolgt über TLS oder IPsec, und alle kundenorientierten Server handeln eine sichere Sitzung mit TLS mit Clientcomputern aus (z. B. wird Exchange Online TLS 1.2 mit 256-Bit-Verschlüsselungsstärke verwendet (FIPS 140-2 Level 2-validiert). (Eine Liste der von Office 365 unterstützten TLS-Verschlüsselungssammlungen finden Sie in den [technischen Referenzdetails zur Verschlüsselung.)](/microsoft-365/compliance/technical-reference-details-about-encryption) Dies gilt für die Protokolle, die von Clients wie Outlook, Skype for Business, Microsoft Teams und Outlook im Web verwendet werden (z. B. HTTP, POP3 usw.).

Die öffentlichen Zertifikate werden von Microsoft IT SSL mit SSLAdmin ausgestellt, einem internen Microsoft-Tool zum Schutz der Vertraulichkeit übertragener Informationen. Alle von Microsoft IT ausgestellten Zertifikate haben eine Länge von mindestens 2048 Bit, und die Webtrust-Compliance erfordert SSLAdmin, um sicherzustellen, dass Zertifikate nur für öffentliche IP-Adressen von Microsoft ausgestellt werden. Alle IP-Adressen, die dieses Kriterium nicht erfüllen, werden über einen Ausnahmeprozess weitergeleitet.

Alle Implementierungsdetails, z. B. die verwendete VERSION von TLS, ob Forward Secrecy (FS) aktiviert ist, die Reihenfolge der Verschlüsselungssammlungen usw., sind öffentlich verfügbar. Eine Möglichkeit, diese Details zu sehen, ist die Verwendung einer Drittanbieterwebsite, z. B. [Qualys SSL Labs.](https://www.ssllabs.com) Nachfolgend finden Sie die Links zu automatisierten Testseiten von Qualys, die Informationen für die folgenden Dienste anzeigen:

- [Office 365 Portal](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype for Business (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype for Business (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Bei Exchange Online Protection variieren URLs je nach Mandantennamen. Alle Kunden können jedoch Microsoft 365 mit **microsoft-com.mail.protection.outlook.com** testen.
