---
title: Microsoft 365 Yammer Zugriffssteuerungen für Unternehmen
description: Dieser Artikel enthält eine kurze Zusammenfassung Yammer Enterprise Access Controls in der Produktionsumgebung.
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
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120364"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer von Unternehmenszugriffssteuerungen 

Der physische und logische Zugriff auf die Yammer ist auf eine kleine Gruppe von Personen (Infrastruktur und Vorgänge) beschränkt. Wie andere Microsoft 365-Techniker haben Yammer keinen ständigen Zugriff auf Kundendaten. Der Zugriff muss über ein genehmigungsbasiertes Just-in-Time-Zugriffssteuerungssystem angefordert werden, das lockbox mit einer begrenzten Anzahl von Genehmigende ähnelt. Genehmiger überprüfen die Anforderung (sie überprüfen beispielsweise, ob die Anforderung aufgrund von Bedarf, Geschäftsfall, Zeit usw. legitim ist), und genehmigen oder verweigern die Anforderung. Wenn die Anforderung genehmigt wird, wird der Zugriff auf jit für einen definierten und begrenzten Zeitraum gewährt. Nach Überschreitung der Zugriffszeit läuft der Zugriff automatisch ab.

Wie bei anderen Microsoft 365-Diensten wird für den Yammer die mehrstufige Authentifizierung verwendet. Der Zugriffs- und Befehlsverlauf wird einem Benutzer zugeordnet und vom Sicherheitsteam Yammer protokolliert und überprüft.

Weitere Informationen zur Verwaltung Yammer Verwaltung finden Sie in Yammer [Administratorhilfe.](/yammer/yammer-landing-page)