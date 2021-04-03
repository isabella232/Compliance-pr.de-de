---
title: Verschlüsselung für Daten bei der Übertragung
description: In diesem Artikel finden Sie eine kurze Erläuterung, wie Microsoft Microsoft 365-Kundendaten bei der Übertragung verschlüsselt.
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
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
ms.openlocfilehash: 227f74140ecd9b6283b92e8b0e87bd70912ec8e3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497252"
---
# <a name="encryption-for-data-in-transit"></a>Verschlüsselung für Daten bei der Übertragung

Zusätzlich zum Schutz von ruhenden Kundendaten verwendet Microsoft Verschlüsselungstechnologien, um Kundendaten während der Übertragung zu schützen. Daten werden transitiv:

- wenn ein Clientcomputer mit einem #A0 kommuniziert;
- wenn ein #A0 mit einem anderen #A1 kommuniziert; und
- wenn ein Microsoft-Server mit einem Nicht-Microsoft-Server kommuniziert (z. B. Exchange Online, der E-Mails an einen E-Mail-Server eines Drittanbieters übermittelt).

Die Kommunikation zwischen Den Rechenzentren zwischen Microsoft-Servern erfolgt über TLS oder IPsec, und alle kundenorientierten Server verhandeln eine sichere Sitzung mithilfe von TLS mit Clientcomputern (z. B. verwendet Exchange Online TLS 1.2 mit 256-Bit-Verschlüsselungsstärke wird verwendet (FIPS 140-2 Level 2-validiert). (Eine [Liste der](/microsoft-365/compliance/technical-reference-details-about-encryption) von Office 365 unterstützten TLS-Verschlüsselungssuiten finden Sie unter Technische Referenzdetails zur Verschlüsselung.) Dies gilt für die Protokolle, die von Clients wie Outlook, Skype for Business, Microsoft Teams und Outlook im Web verwendet werden (z. B. HTTP, POP3 usw.).

Die öffentlichen Zertifikate werden von Microsoft IT SSL mit SSLAdmin ausgestellt, einem internen Microsoft-Tool zum Schutz der Vertraulichkeit übermittelter Informationen. Alle von Microsoft IT ausgestellten Zertifikate haben eine Länge von mindestens 2048 Bit, und die Webtrust-Compliance erfordert SSLAdmin, um sicherzustellen, dass Zertifikate nur für öffentliche IP-Adressen ausgestellt werden, die im Besitz von Microsoft sind. Alle IP-Adressen, die dieses Kriterium nicht erfüllen, werden über einen Ausnahmeprozess geroutet.

Alle Implementierungsdetails, z. B. die verwendete Version von TLS, ob Forward Secrecy (FS) aktiviert ist, die Reihenfolge der Verschlüsselungssuiten usw., sind öffentlich verfügbar. Eine Möglichkeit, diese Details anzuzeigen, ist die Verwendung einer Drittanbieterwebsite, z. B. [Qualys SSL Labs](https://www.ssllabs.com). Nachfolgend finden Sie die Links zu automatisierten Testseiten von Qualys, die Informationen für die folgenden Dienste anzeigen:

- [Office 365 Portal](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype for Business (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype for Business (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Für Exchange Online Protection variieren URLs nach Mandantennamen. Allerdings können alle Kunden Microsoft 365 mithilfe von **microsoft-com.mail.protection.outlook.com.**
