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
ms.openlocfilehash: ac02d8ba8719d9ef78a24bee37732007af7cba8b
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573573"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer Unternehmenszugriffssteuerungen 

Der physische und logische Zugriff auf die Yammer Produktionsumgebung ist auf eine kleine Gruppe von Personen (Infrastruktur und Betrieb) beschränkt. Wie bei anderen Microsoft 365-Technikern haben Yammer Techniker keinen ständigen Zugriff auf Kundendaten. Der Zugriff muss mithilfe eines genehmigungsbasierten Just-in-Time-Zugriffssteuerungssystems angefordert werden, ähnlich wie Lockbox mit einer begrenzten Anzahl von Genehmigern. Genehmigende Personen überprüfen die Anforderung (z. B. überprüfen, ob die Anforderung je nach Bedarf, Geschäftsfall, Zeit usw. legitim ist) und genehmigen oder verweigern die Anforderung. Wenn die Anforderung genehmigt wurde, wird JIT-Zugriff für einen definierten und begrenzten Zeitraum gewährt. Nachdem die Zugriffszeit überschritten wurde, läuft der Zugriff automatisch ab.

Wie bei anderen Microsoft 365-Diensten verwendet jeder Zugriff auf die Yammer Produktionsumgebung die mehrstufige Authentifizierung. Der gesamte Zugriffs- und Befehlsverlauf wird einem Benutzer zugeordnet und vom sicherheitsteam Yammer regelmäßig protokolliert und überprüft.

Weitere Informationen zu Yammer Verwaltung und Verwaltung finden Sie in [Yammer Administratorhilfe.](/yammer/yammer-landing-page)