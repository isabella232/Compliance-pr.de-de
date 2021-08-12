---
title: Taxonomie der Datenklassifizierung & Vertraulichkeitsbezeichnungen
description: In diesem Artikel finden Sie eine Übersicht über die Verwendung der Datenklassifizierung & Taxonomie von Vertraulichkeitsbezeichnungen mit Microsoft 365.
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
ms.openlocfilehash: dc2a1a27994c1f3fc69f35b4b764ae80d3df7defd3b4d0dec97520de7760f815
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "54288713"
---
# <a name="data-classification--sensitivity-label-taxonomy"></a>Taxonomie der Datenklassifizierung & Vertraulichkeitsbezeichnungen

Vertrauliche Daten stellen ein erhebliches Risiko für ein Unternehmen dar, wenn sie gestohlen, versehentlich freigegeben oder durch eine Verletzung offengelegt werden. Zu den Risikofaktoren gehören Reputationsschäden, finanzielle Auswirkungen und Verlust von Wettbewerbsvorteilen. Der Schutz der Daten und Informationen, die Ihr Unternehmen verwaltet, hat für Ihre Organisation oberste Priorität. Es kann jedoch schwierig sein, zu wissen, ob Ihre Anstrengungen angesichts der Menge an Inhalten in Ihrem Unternehmen wirklich effektiv sind.

Zusätzlich zum Volume können Ihre Inhalte von hochgradig vertraulicher und wirkungsvoller bis zu trivialer und vorübergehender Bedeutung reichen. Es kann auch unter dem Blick auf verschiedene gesetzliche Compliance-Anforderungen stehen. Es kann eine Herausforderung sein, zu wissen, was priorisiert werden muss und wo Steuerelemente angewendet werden sollen. Lesen Sie weiter, um mehr über *die Datenklassifizierung* zu erfahren, ein wichtiges Tool zum Schutz Ihrer Inhalte vor Diebstahl, Simplifizierung oder unbeabsichtigter Vernichtung, und wie Microsoft 365 Ihnen helfen können, Ihre Ziele in Bezug auf die Informationssicherheit zu erreichen.

## <a name="what-is-data-classification"></a>Was ist die Datenklassifizierung?

[Die Datenklassifizierung](/microsoft-365/compliance/data-classification-overview) ist ein spezieller Begriff, der in den Bereichen Internetsicherheit und Informationsgovernance verwendet wird, um den Prozess der Identifizierung, Kategorisierung und des Schutzes von Inhalten gemäß ihrer Vertraulichkeits- oder Auswirkungsstufe zu beschreiben. In ihrer grundlegendsten Form ist die Datenklassifizierung ein Mittel zum Schutz Ihrer Daten vor unbefugter Offenlegung, Änderung oder Zerstörung basierend auf ihrer Vertraulichkeit oder Auswirkung.

## <a name="what-is-a-data-classification-framework"></a>Was ist ein Datenklassifizierungsframework?

Häufig in einer formalen, unternehmensweiten Richtlinie codiert, besteht ein Datenklassifizierungsframework (manchmal auch als "Datenklassifizierungsrichtlinie" bezeichnet) in der Regel aus 3 bis 5 Klassifizierungsebenen. Diese enthalten in der Regel drei Elemente: einen Namen, eine Beschreibung und Beispiele aus der Praxis. Microsoft empfiehlt nicht mehr als fünf übergeordnete Beschriftungen auf oberster Ebene mit jeweils fünf Unterbezeichnungen (insgesamt 25), um die Benutzeroberfläche (UI) verwaltbar zu halten. Ebenen werden in der Regel von der niedrigsten bis zur sensibelsten Ebene angeordnet, z. B. *öffentlich,* *intern,* *vertraulich* und *streng* 
 *vertraulich.* Andere Ebenennamenvarianten, auf die Sie möglicherweise stoßen können, sind *eingeschränkt,* *uneingeschränkt* und *verbrauchergeschützt.* Microsoft empfiehlt Bezeichnungsnamen, die selbstdeskriptiv sind und ihre relative Vertraulichkeit deutlich hervorheben. Beispielsweise können *"Vertraulich"* und *"Eingeschränkt"* benutzerdeklarieren, welche Bezeichnung geeignet ist, während *"Vertraulich"* und *"Streng vertraulich"* eindeutiger sind, was sensibler ist. Die folgende Tabelle zeigt Beispiele für Frameworkebenen der Datenklassifizierung.

|**Klassifizierungsstufe**|**Beschreibung**|**Beispiele**|
|:-----------------------|:--------------|:-----------|
| Streng vertraulich | Streng vertrauliche Daten sind die vertraulichsten Daten, die vom Unternehmen gespeichert oder verwaltet werden, und erfordern möglicherweise rechtliche Benachrichtigungen, wenn sie verletzt oder anderweitig offengelegt werden. <br><br> Eingeschränkte Daten erfordern das höchste Maß an Kontrolle und Sicherheit, und der Zugriff sollte auf "Erforderlichkeit" beschränkt werden. | Vertrauliche personenbezogene Informationen (vertrauliche personenbezogene Informationen) <br> Karteninhaberdaten <br> Geschützte Integritätsinformationen (Protected Health Information, PHI) <br> Bankkontodaten |

>[!TIP]
>Das Microsoft-Framework für die Unternehmensdatenklassifizierung verwendete ursprünglich während der Pilotphase eine Kategorie und Bezeichnung namens "Intern", es gab jedoch berechtigte Gründe dafür, dass ein Dokument extern freigegeben und auf "Allgemein" umgestellt wurde.

Eine weitere wichtige Komponente eines Datenklassifizierungsframeworks sind die Steuerelemente, die jeder Ebene zugeordnet sind. Datenklassifizierungsebenen selbst sind einfach Bezeichnungen (oder Tags), die den Wert oder die Vertraulichkeit des Inhalts angeben. Um diese Inhalte zu *schützen,* definieren Datenklassifizierungsframeworks die Steuerelemente, die für jede Ihrer Datenklassifizierungsebenen vorhanden sein sollten. Diese Steuerelemente können Anforderungen in Bezug auf Folgendes umfassen:

- Storage Typ und Speicherort
- Verschlüsselung
- Zugriffssteuerung
- Datenvernichtung
- Verhinderung von Datenverlust
- Öffentliche Offenlegung
- Protokollieren und Nachverfolgen des Zugriffs
- Andere Kontrollziele, je nach Bedarf

Ihre Sicherheitskontrollen variieren je nach Datenklassifizierungsstufe, sodass die in Ihrem Framework definierten Schutzmaßnahmen der Vertraulichkeit Ihrer Inhalte entsprechen. Die Anforderungen an die Datenspeicherungssteuerung variieren z. B. je nach verwendeten Medien sowie nach der Klassifizierungsstufe, die auf einen bestimmten Inhalt angewendet wird. Die folgende Tabelle zeigt ein Beispiel für Datenklassifizierungssteuerelemente für einen bestimmten Speichertyp:

|**Speichertyp**|**Vertraulich**|**Intern**|**Uneingeschränkte**|
|:---------------|:---------------|:-----------|:---------------|
| Wechselmedien Storage | Verboten | Unzulässig, es sei denn, er verschlüsselt | Kein Steuerelement erforderlich |

Das richtige Anwenden der richtigen Datenklassifizierungsstufe kann in realen Situationen komplex sein und endbenutzer manchmal überfordern. Sobald eine Richtlinie oder ein Standard erstellt wurde, die die erforderlichen Ebenen der Datenklassifizierung definiert, ist es wichtig, Endbenutzer zu führen, wie sie dieses Framework in ihrer täglichen Arbeit zum Leben erwecken können. In diesem Bereich kommen Regeln oder Richtlinien für die Behandlung von Datenklassifizierungen ins Raum.

Richtlinien für die Behandlung von Datenklassifizierungen helfen Endbenutzern mit spezifischen Anleitungen zum ordnungsgemäßen Umgang mit den einzelnen Datenebenen für unterschiedliche Speichermedien während des gesamten Lebenszyklus. Diese Richtlinien helfen Endbenutzern bei der richtigen Anwendung von Regeln in der Praxis, z. B. beim Teilen von Dokumenten, Senden von E-Mails oder Zusammenarbeiten über verschiedene Plattformen und Organisationen hinweg.

Microsoft-Kunden geben an, dass etwa 50 % eines Information Protection-Projekts nicht auf technische, sondern auf Geschäftsaktivitäten ausgerichtet sind. Daher sind Schulungen und Kommunikation für Endbenutzer entscheidend für den Erfolg.
