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
ms.localizationpriority: medium
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
ms.openlocfilehash: 5bc064ccf982b9a67ec5cedc33e85f58e1d7dfc1
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481617"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer Unternehmenszugriffssteuerungen 

Der physische und logische Zugriff auf die Yammer Produktionsumgebung ist auf eine kleine Gruppe von Personen (Infrastruktur und Betrieb) beschränkt. Wie bei anderen Microsoft 365-Technikern haben Yammer Techniker keinen ständigen Zugriff auf Kundendaten. Der Zugriff muss mithilfe eines genehmigungsbasierten Just-in-Time-Zugriffssteuerungssystems angefordert werden, ähnlich wie Lockbox mit einer begrenzten Anzahl von Genehmigern. Genehmigende Personen überprüfen die Anforderung (z. B. überprüfen, ob die Anforderung je nach Bedarf, Geschäftsfall, Zeit usw. legitim ist) und genehmigen oder verweigern die Anforderung. Wenn die Anforderung genehmigt wurde, wird JIT-Zugriff für einen definierten und begrenzten Zeitraum gewährt. Nachdem die Zugriffszeit überschritten wurde, läuft der Zugriff automatisch ab.

Wie bei anderen Microsoft 365-Diensten wird für den gesamten Zugriff auf die Yammer Produktionsumgebung die mehrstufige Authentifizierung verwendet. Der gesamte Zugriffs- und Befehlsverlauf wird einem Benutzer zugeordnet und vom sicherheitsteam Yammer regelmäßig protokolliert und überprüft.

Weitere Informationen zu Yammer Verwaltung und Verwaltung finden Sie in [Yammer Administratorhilfe.](/yammer/yammer-landing-page)