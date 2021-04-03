---
title: Microsoft 365 Yammer Unternehmenszugriffssteuerelemente
description: Dieser Artikel enthält eine kurze Zusammenfassung über Yammer Enterprise Access Controls in der Produktionsumgebung.
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
hideEdit: true
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497353"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer Unternehmenszugriffssteuerelemente 

Der physische und logische Zugriff auf Yammer Produktionsumgebung ist auf eine kleine Gruppe von Personen (Infrastruktur und Betrieb) beschränkt. Wie bei anderen Microsoft 365-Technikern haben Yammer techniker keinen ständigen Zugriff auf Kundendaten. Der Zugriff muss über ein genehmigungsbasiertes Just-in-Time-Zugriffssteuerungssystem angefordert werden, das lockbox mit einer begrenzten Anzahl von Genehmigende ähnelt. Genehmiger überprüfen die Anforderung (sie überprüfen beispielsweise, ob die Anforderung aufgrund von Bedarf, Geschäftsfall, Uhrzeit usw.) legitim ist, und genehmigen oder verweigern die Anforderung. Wenn die Anforderung genehmigt wird, wird der JIT-Zugriff für einen definierten und begrenzten Zeitraum gewährt. Nachdem die Zugriffszeit überschritten wurde, läuft der Zugriff automatisch ab.

Wie bei anderen Microsoft 365-Diensten wird bei allen Zugriffen Yammer Produktionsumgebung die mehrstufige Authentifizierung verwendet. Der zugriffs- und befehlsverlauf wird einem Benutzer zugeordnet und vom Sicherheitsteam Yammer protokolliert und überprüft.

Weitere Informationen zu Yammer Verwaltung finden Sie unter [Yammer Admin Help](/yammer/yammer-landing-page).