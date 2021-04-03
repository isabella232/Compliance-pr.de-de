---
title: Datenklassifizierung & Vertraulichkeitsbezeichnungstaxonomie
description: In diesem Artikel finden Sie eine Übersicht über die Verwendung der Datenklassifizierung & Vertraulichkeitsbezeichnungstaxonomie mit Microsoft 365.
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
ms.openlocfilehash: fcfe98116f4d0629f322383f2992605d2dcf19de
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497801"
---
# <a name="data-classification--sensitivity-label-taxonomy"></a>Datenklassifizierung & Vertraulichkeitsbezeichnungstaxonomie

Vertrauliche Daten sind für ein Unternehmen ein erhebliches Risiko, wenn sie gestohlen, versehentlich freigegeben oder durch eine Verletzung verfügbar gemacht werden. Zu den Risikofaktoren gehören Reputationsschäden, finanzielle Auswirkungen und der Verlust von Wettbewerbsvorteilen. Der Schutz der Daten und Informationen, die Ihr Unternehmen verwaltet, hat für Ihre Organisation oberste Priorität. Es kann jedoch schwierig sein, zu wissen, ob Ihre Bemühungen angesichts der Menge an Inhalten ihres Unternehmens wirklich effektiv sind.

Neben der Lautstärke können Ihre Inhalte von hochsensiblen und auswirkungenreichen bis zu trivialen und vorübergehenden Inhalten reichen. Es kann auch unter der Aufsicht verschiedener gesetzlicher Complianceanforderungen sein. Es kann eine Herausforderung sein, zu wissen, was priorisiert und wo Steuerelemente angewendet werden sollen. Lesen Sie weiter, um mehr über die Datenklassifizierung *zu* erfahren, ein wichtiges Tool zum Schutz Ihrer Inhalte vor Diebstahl, Sabotage oder unbeabsichtigter Zerstörung und darüber, wie Microsoft 365 Ihnen dabei helfen kann, Ihre Ziele für die Informationssicherheit zu erreichen.

## <a name="what-is-data-classification"></a>Was ist datenklassifizierung?

[Die](/microsoft-365/compliance/data-classification-overview) Datenklassifizierung ist ein spezieller Begriff, der in den Bereichen Cybersicherheit und Informationsverwaltung verwendet wird, um den Prozess der Identifizierung, Kategorisierung und des Abwehrens von Inhalten entsprechend ihrer Vertraulichkeits- oder Auswirkungsebene zu beschreiben. In ihrer grundlegendsten Form ist die Datenklassifizierung ein Mittel zum Schutz Ihrer Daten vor nicht autorisierter Offenlegung, Änderung oder Zerstörung basierend auf ihrer Sensiblen oder Auswirkung.

## <a name="what-is-a-data-classification-framework"></a>Was ist ein Datenklassifizierungsframework?

Häufig in einer formalen, unternehmensweiten Richtlinie kodifiziert, besteht ein Datenklassifizierungsframework (manchmal auch als "Datenklassifizierungsrichtlinie" bezeichnet) in der Regel aus 3 bis 5 Klassifizierungsstufen. Diese umfassen in der Regel drei Elemente: einen Namen, eine Beschreibung und reale Beispiele. Microsoft empfiehlt nicht mehr als fünf übergeordnete Bezeichnungen auf oberster Ebene mit jeweils fünf Unterbezeichnungen (insgesamt 25), um die Benutzeroberfläche (Ui) verwaltbar zu halten. Ebenen werden in der Regel von der geringsten bis zur sensibelsten Ebene angeordnet, z. B. *öffentlich,* *intern,* *vertraulich* und *streng* 
 *vertraulich.* Andere Variationen von Ebenennamen, auf die Sie stoßen können, sind *Restricted*, *Unrestricted* und *Consumer Protected*. Microsoft empfiehlt Bezeichnungsnamen, die selbstdeskriptiv sind und deren relative Vertraulichkeit deutlich hervorheben. Beispielsweise können *vertrauliche* *und* eingeschränkte Benutzer erraten, welche  Bezeichnung geeignet ist, während *Vertrauliche* und Streng Vertrauliche klarer sind, was sensibler ist. Die folgende Tabelle enthält Beispiele für Datenklassifizierungsframeworkebenen.

|**Klassifizierungsebene**|**Beschreibung**|**Beispiele**|
|:-----------------------|:--------------|:-----------|
| Streng vertraulich | Streng vertrauliche Daten sind die vertraulichsten Arten von Daten, die vom Unternehmen gespeichert oder verwaltet werden und möglicherweise rechtliche Benachrichtigungen erfordern, wenn sie verletzt oder anderweitig offengelegt werden. <br><br> Eingeschränkte Daten erfordern die höchste Ebene an Kontrolle und Sicherheit, und der Zugriff sollte auf "Bedürfnis nach Wissen" beschränkt sein. | Vertrauliche personenbezogene Informationen (vertrauliche PII) <br> Cardholder-Daten <br> Geschützte Integritätsinformationen (Protected Health Information, PHI) <br> Bankkontodaten |

>[!TIP]
>Das Microsoft-Framework für die Unternehmensdatenklassifizierung verwendete ursprünglich eine Kategorie und Bezeichnung namens "Internal" während der Pilotphase, stellte jedoch fest, dass es legitime Gründe für die externe Freigabe eines Dokuments und die Umstellung auf "Allgemein" gab.

Eine weitere wichtige Komponente eines Datenklassifizierungsframework sind die Steuerelemente, die jeder Ebene zugeordnet sind. Datenklassifizierungsstufen sind einfach Bezeichnungen (oder Tags), die den Wert oder die Vertraulichkeit des Inhalts angeben. Um *diese* Inhalte zu schützen, definieren Datenklassifizierungsframeworks die Steuerelemente, die für jede Ihrer Datenklassifizierungsstufen verwendet werden sollten. Diese Steuerelemente können Anforderungen im Zusammenhang mit folgenden Themen umfassen:

- Speichertyp und Speicherort
- Verschlüsselung
- Zugriffssteuerung
- Datenvernichtung
- Verhinderung von Datenverlust
- Öffentliche Offenlegung
- Protokollierung und Nachverfolgung des Zugriffs
- Andere Kontrollziele nach Bedarf

Ihre Sicherheitssteuerelemente variieren je nach Datenklassifizierungsstufe, damit die in Ihrem Framework definierten Schutzmaßnahmen der Vertraulichkeit Ihrer Inhalte mehrEntsprechen. Beispielsweise variieren die Anforderungen für die Datenspeicherung abhängig von den verwendeten Medien sowie von der Klassifizierungsstufe, die auf einen bestimmten Inhalt angewendet wird. Die folgende Tabelle zeigt ein Beispiel für Datenklassifizierungssteuerelemente für einen bestimmten Speichertyp:

|**Speichertyp**|**Vertraulich**|**Intern**|**Uneingeschränkt**|
|:---------------|:---------------|:-----------|:---------------|
| Wechselmedienspeicher | Verboten | Verboten, es sei denn, verschlüsselt | Kein Steuerelement erforderlich |

Das richtige Anwenden der richtigen Ebene der Datenklassifizierung kann in realen Situationen komplex sein und manchmal die Endbenutzer überfordern. Nachdem eine Richtlinie oder ein Standard erstellt wurde, die die erforderlichen Ebenen der Datenklassifizierung definiert, ist es wichtig, endbenutzern zu zeigen, wie sie dieses Framework in ihrer täglichen Arbeit zum Leben erhalten. In diesem Bereich werden Regeln oder Richtlinien für die Verarbeitung von Datenklassifizierungen verwendet.

Richtlinien für die Verarbeitung von Datenklassifizierungen helfen Endbenutzern mit spezifischen Anleitungen zum angemessenen Umgang mit den einzelnen Datenebenen für unterschiedliche Speichermedien während ihres gesamten Lebenszyklus. Diese Richtlinien helfen Endbenutzern bei der ordnungsgemäßen Anwendung von Regeln in der Praxis, z. B. beim Freigeben von Dokumenten, beim Senden von E-Mails oder bei der Zusammenarbeit über verschiedene Plattformen und Organisationen hinweg.

Microsoft-Kunden geben an, dass ca. 50 % eines Information Protection-Projekts geschäftsorientiert und nicht technisch ausgerichtet sind, sodass Endbenutzerschulungen und -kommunikation entscheidend für den Erfolg sind.
