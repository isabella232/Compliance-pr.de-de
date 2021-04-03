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
# <a name="encryption-for-data-in-transit"></a><span data-ttu-id="65359-103">Verschlüsselung für Daten bei der Übertragung</span><span class="sxs-lookup"><span data-stu-id="65359-103">Encryption for data-in-transit</span></span>

<span data-ttu-id="65359-104">Zusätzlich zum Schutz von ruhenden Kundendaten verwendet Microsoft Verschlüsselungstechnologien, um Kundendaten während der Übertragung zu schützen.</span><span class="sxs-lookup"><span data-stu-id="65359-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect customer data in transit.</span></span> <span data-ttu-id="65359-105">Daten werden transitiv:</span><span class="sxs-lookup"><span data-stu-id="65359-105">Data is in transit:</span></span>

- <span data-ttu-id="65359-106">wenn ein Clientcomputer mit einem #A0 kommuniziert;</span><span class="sxs-lookup"><span data-stu-id="65359-106">when a client machine communicates with a Microsoft server;</span></span>
- <span data-ttu-id="65359-107">wenn ein #A0 mit einem anderen #A1 kommuniziert; und</span><span class="sxs-lookup"><span data-stu-id="65359-107">when a Microsoft server communicates with another Microsoft server; and</span></span>
- <span data-ttu-id="65359-108">wenn ein Microsoft-Server mit einem Nicht-Microsoft-Server kommuniziert (z. B. Exchange Online, der E-Mails an einen E-Mail-Server eines Drittanbieters übermittelt).</span><span class="sxs-lookup"><span data-stu-id="65359-108">when a Microsoft server communicates with a non-Microsoft server (for example, Exchange Online delivering email to a third-party email server).</span></span>

<span data-ttu-id="65359-109">Die Kommunikation zwischen Den Rechenzentren zwischen Microsoft-Servern erfolgt über TLS oder IPsec, und alle kundenorientierten Server verhandeln eine sichere Sitzung mithilfe von TLS mit Clientcomputern (z. B. verwendet Exchange Online TLS 1.2 mit 256-Bit-Verschlüsselungsstärke wird verwendet (FIPS 140-2 Level 2-validiert).</span><span class="sxs-lookup"><span data-stu-id="65359-109">Inter-data center communications between Microsoft servers take place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (for example, Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="65359-110">(Eine [Liste der](/microsoft-365/compliance/technical-reference-details-about-encryption) von Office 365 unterstützten TLS-Verschlüsselungssuiten finden Sie unter Technische Referenzdetails zur Verschlüsselung.) Dies gilt für die Protokolle, die von Clients wie Outlook, Skype for Business, Microsoft Teams und Outlook im Web verwendet werden (z. B. HTTP, POP3 usw.).</span><span class="sxs-lookup"><span data-stu-id="65359-110">(See [Technical reference details about encryption](/microsoft-365/compliance/technical-reference-details-about-encryption) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, Microsoft Teams, and Outlook on the web (for example, HTTP, POP3, etc.).</span></span>

<span data-ttu-id="65359-111">Die öffentlichen Zertifikate werden von Microsoft IT SSL mit SSLAdmin ausgestellt, einem internen Microsoft-Tool zum Schutz der Vertraulichkeit übermittelter Informationen.</span><span class="sxs-lookup"><span data-stu-id="65359-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="65359-112">Alle von Microsoft IT ausgestellten Zertifikate haben eine Länge von mindestens 2048 Bit, und die Webtrust-Compliance erfordert SSLAdmin, um sicherzustellen, dass Zertifikate nur für öffentliche IP-Adressen ausgestellt werden, die im Besitz von Microsoft sind.</span><span class="sxs-lookup"><span data-stu-id="65359-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="65359-113">Alle IP-Adressen, die dieses Kriterium nicht erfüllen, werden über einen Ausnahmeprozess geroutet.</span><span class="sxs-lookup"><span data-stu-id="65359-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="65359-114">Alle Implementierungsdetails, z. B. die verwendete Version von TLS, ob Forward Secrecy (FS) aktiviert ist, die Reihenfolge der Verschlüsselungssuiten usw., sind öffentlich verfügbar.</span><span class="sxs-lookup"><span data-stu-id="65359-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="65359-115">Eine Möglichkeit, diese Details anzuzeigen, ist die Verwendung einer Drittanbieterwebsite, z. B. [Qualys SSL Labs](https://www.ssllabs.com).</span><span class="sxs-lookup"><span data-stu-id="65359-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="65359-116">Nachfolgend finden Sie die Links zu automatisierten Testseiten von Qualys, die Informationen für die folgenden Dienste anzeigen:</span><span class="sxs-lookup"><span data-stu-id="65359-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="65359-117">Office 365 Portal</span><span class="sxs-lookup"><span data-stu-id="65359-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="65359-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="65359-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="65359-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="65359-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="65359-120">Skype for Business (SIP)</span><span class="sxs-lookup"><span data-stu-id="65359-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="65359-121">Skype for Business (Web)</span><span class="sxs-lookup"><span data-stu-id="65359-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="65359-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="65359-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="65359-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="65359-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="65359-124">Für Exchange Online Protection variieren URLs nach Mandantennamen. Allerdings können alle Kunden Microsoft 365 mithilfe von **microsoft-com.mail.protection.outlook.com.**</span><span class="sxs-lookup"><span data-stu-id="65359-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
