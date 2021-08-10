---
title: Microsoft 365 Yammer Unternehmenszugriffssteuerungen
description: Dieser Artikel enthält eine kurze Zusammenfassung zu Yammer Enterprise Zugriffssteuerungen in der Produktionsumgebung.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d9a3604bd987170ea266871cf4c384c0e071817dc10640eb01e560debb5d9664
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54291643"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer Unternehmenszugriffssteuerungen 

Der physische und logische Zugriff auf die Yammer Produktionsumgebung ist auf eine kleine Gruppe von Personen (Infrastruktur und Betrieb) beschränkt. Wie bei anderen Microsoft 365-Technikern haben Yammer Techniker keinen ständigen Zugriff auf Kundendaten. Der Zugriff muss mithilfe eines genehmigungsbasierten Just-in-Time-Zugriffssteuerungssystems angefordert werden, ähnlich wie Lockbox mit einer begrenzten Anzahl von Genehmigern. Genehmigende Personen überprüfen die Anforderung (z. B. überprüfen, ob die Anforderung je nach Bedarf, Geschäftsfall, Zeit usw. legitim ist) und genehmigen oder verweigern die Anforderung. Wenn die Anforderung genehmigt wurde, wird JIT-Zugriff für einen definierten und begrenzten Zeitraum gewährt. Nachdem die Zugriffszeit überschritten wurde, läuft der Zugriff automatisch ab.

Wie bei anderen Microsoft 365-Diensten verwendet jeder Zugriff auf die Yammer Produktionsumgebung die mehrstufige Authentifizierung. Der gesamte Zugriffs- und Befehlsverlauf wird einem Benutzer zugeordnet und vom sicherheitsteam Yammer regelmäßig protokolliert und überprüft.

Weitere Informationen zu Yammer Verwaltung und Verwaltung finden Sie in [Yammer Administratorhilfe.](/yammer/yammer-landing-page)