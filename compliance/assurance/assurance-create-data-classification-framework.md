---
title: Erstellen eines gut gestalteten Datenklassifizierungsframeworks
description: In diesem Artikel finden Sie eine Übersicht über die Erstellung eines gut gestalteten Datenklassifizierungsframeworks für Microsoft 365.
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
ms.openlocfilehash: 17aa73258f1ecc4db9cc13a5df08b1aa76a583a7
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482158"
---
# <a name="create-a-well-designed-data-classification-framework"></a>Erstellen eines gut gestalteten Datenklassifizierungsframeworks

Berücksichtigen Sie bei der Entwicklung, Überarbeitung oder Verfeinerung Ihres Datenklassifizierungsframeworks die folgenden führenden Methoden:

- **Gehen Sie nicht von 0 bis 100 Uhr an Tag 1:** Microsoft empfiehlt einen Durchforstungs-Walk-Run-Ansatz, bei dem für die Organisation wichtige Features priorisiert und anhand einer Zeitachse zugeordnet werden. Führen Sie den ersten Schritt aus, stellen Sie sicher, dass er erfolgreich war, und fahren Sie dann mit der nächsten Phase fort, in der die gewonnenen Erkenntnisse angewendet werden. Denken Sie daran, dass Ihre Organisation beim Entwerfen des Datenklassifizierungsframeworks möglicherweise weiterhin Risiken ausgesetzt ist. Daher ist es in Ordnung, mit nur wenigen Klassifizierungsstufen klein zu beginnen und später nach Bedarf zu erweitern.
- **Sie schreiben nicht nur für Cybersicherheitsexperten:** Datenklassifizierungsframeworks sind für ein breites Publikum gedacht, einschließlich Ihres durchschnittlichen Mitarbeiters, Ihrer Rechts- und Complianceteams und Ihres IT-Teams. Es ist wichtig, klare, leicht verständliche Definitionen für Ihre Datenklassifizierungsebenen zu schreiben und nach Möglichkeit Beispiele aus der Praxis bereitzustellen. Vermeiden Sie Jargon, und ziehen Sie ein Glossar für Akronyme und hoch technische Begriffe in Betracht. Verwenden Sie beispielsweise "Personenbezogene Informationen" und geben Sie eine Definition an, anstatt einfach "PERSONENBEZOGENe Informationen" zu sagen.
- **Datenklassifizierungsframeworks sollen implementiert werden:** Damit Datenklassifizierungsframeworks erfolgreich sind, müssen sie implementiert werden. Es ist besonders relevant, wenn die Steuerungsanforderungen für jede Datenklassifizierungsebene erstellt werden. Stellen Sie sicher, dass die Anforderungen klar definiert sind und dass sie jegliche Mehrdeutigkeit vorwegnehmen und beheben, die während der Implementierung auftreten kann. Wenn Sie beispielsweise über ein Steuerelement für personenbezogene Informationen verfügen, stellen Sie sicher, dass Sie genau die Bedeutung dieses Steuerelements, z. B. sozialversicherungs- oder Reisepassnummer, festlegen.
- **Gehen Sie nur dann präzise vor, wenn Sie dies benötigen:** Datenklassifizierungsframeworks enthalten in der Regel eine beliebige Ebene zwischen 3 und 5 Datenklassifizierungsebenen. Aber nur weil Sie fünf Ebenen einschließen *können,* bedeutet dies nicht, dass Sie *dies sollten.* Berücksichtigen Sie bei der Entscheidung über die Anzahl der benötigten Klassifizierungsebenen die folgenden Kriterien:

    - Ihre Branche und ihre zugehörigen regulatorischen Verpflichtungen (stark regulierte Branchen benötigen in der Regel mehr Klassifizierungsstufen)
    - Der für die Aufrechterhaltung eines komplexeren Frameworks erforderliche Betriebsaufwand
    - Ihre Benutzer und ihre Fähigkeit, der erhöhten Komplexität und Nuance zu entsprechen, die mit mehr Klassifizierungsstufen verbunden sind
    - Benutzerfreundlichkeit und Barrierefreiheit bei der Suche nach einer manuellen Klassifizierung über mehrere Gerätetypen hinweg

- **Holen Sie sich die richtigen Personen:** Die Einbindung eines leitenden Projektbeteiligten ist für den Erfolg entscheidend, da viele Projekte ohne Die Sicherung der Geschäftsleitung nicht beginnen oder länger dauern müssen. Datenklassifizierungsframeworks befinden sich in der Regel im Besitz von IT-Teams, können jedoch rechtliche, Compliance-, Datenschutz- und Änderungsmanagement-Auswirkungen haben. Um sicherzustellen, dass Sie ein Framework erstellen, das Zum Schutz Ihres Unternehmens beiträgt, achten Sie darauf, datenschutz- und rechtliche Interessengruppen wie Ihren Chief Privacy Officer und die Office des GeneralAnwalts in die Entwicklung Ihrer Richtlinie einzubeziehen. Wenn Ihre Organisation über eine Complianceabteilung, Informationsgovernance-Experten oder ein Datensatzverwaltungsteam verfügt, können sie auch wertvolle Beiträge haben. Wenn Ihr Framework für das Unternehmen eingeführt wird, spielt Ihre Kommunikationsabteilung auch eine wichtige Rolle für interne Nachrichten und die Einführung.
- **Balance zwischen Sicherheit und Komfort:** Ein häufiger Fehler besteht darin, ein sicheres, aber zu restriktives Datenklassifizierungsframework zu entwerfen. Dieses Framework wurde möglicherweise unter Berücksichtigung der Sicherheit entworfen, ist jedoch in der Praxis häufig schwierig zu implementieren. Wenn Benutzer komplexe, strenge und zeitaufwändige Verfahren befolgen müssen, um das Framework in ihrem täglichen Leben anzuwenden, besteht immer das Risiko, dass sie nicht mehr an ihren Wert glauben und schließlich nicht mehr den Verfahren folgen. Dieses Risiko besteht auf allen Ebenen der Organisation, einschließlich Managern auf Geschäftsleitungsebene (C-Suite) innerhalb der Organisation. Ein gutes Gleichgewicht zwischen Sicherheit und Komfort zusammen mit einfach zu verwendenden Tools führt in der Regel zu einer breiteren Benutzerakzeptanz und -verwendung. Wenn es Lücken in Ihrem Framework gibt, warten Sie nicht, bis alles perfekt ist, um mit der Implementierung zu beginnen. Bewerten Sie stattdessen das Risiko oder die Lücke, erstellen Sie einen Plan zur Minimierung und fahren Sie fort. Denken Sie daran, dass der Informationsschutz eine Reise ist, die nicht über Nacht aktiviert und dann durchgeführt wird. Planen, implementieren Sie einige Funktionen, bestätigen Sie den Erfolg und durchlaufen Sie den nächsten Meilenstein, wenn sich die Tools weiterentwickeln und die Benutzer reif und erfahren werden.

Bedenken Sie außerdem, dass ein Datenklassifizierungsframework nur *die* Aktionen Ihrer Organisation zum Schutz vertraulicher Daten betrifft. Datenklassifizierungsframeworks werden häufig von Regeln oder Richtlinien für die Datenverarbeitung begleitet, die definieren, *wie* diese Richtlinien aus technischer und technischer Sicht eingerichtet werden. In den folgenden Abschnitten befassen wir uns mit einigen praktischen Anleitungen, wie Sie Ihr Datenklassifizierungsframework von einem Richtliniendokument auf eine vollständig implementierte und umsetzbare Initiative anwenden können.

## <a name="pain-points-in-creating-a-data-classification-framework"></a>Probleme beim Erstellen eines Datenklassifizierungsframeworks

Die Datenklassifizierungsaktivitäten sind von Natur aus weitreichend und betreffen fast jede Geschäftsfunktion innerhalb eines Unternehmens. Aufgrund dieses breiten Umfangs und der Komplexität der Verwaltung von Inhalten in modernen digitalen Umgebungen stehen Unternehmen häufig vor Herausforderungen, wenn sie wissen, wo sie beginnen, wie eine erfolgreiche Implementierung verwaltet wird und wie sie ihren Fortschritt messen können. Häufige Problempunkte sind häufig:

- Entwerfen eines robusten und leicht verständlichen Datenklassifizierungsframeworks, einschließlich der Bestimmung von Klassifizierungsstufen und zugehörigen Sicherheitskontrollen.
- Entwickeln eines Implementierungsplans, der die Bestätigung der entsprechenden Technologielösung, die Anpassung des Plans an vorhandene Geschäftsprozesse und die Ermittlung der Auswirkungen auf die Mitarbeiter umfasst.
- Einrichten eines Datenklassifizierungsframeworks innerhalb der ausgewählten Technologielösung und Beheben von Lücken zwischen den Technologiefunktionen des Tools und dem Framework selbst.
- Einrichten einer Governancestruktur, die die laufende Wartung und Integrität der Datenklassifizierungsaktivitäten überwacht.
- Identifizieren bestimmter Key Performance Indicators (KPIs), um den Fortschritt zu überwachen und zu messen.
- Sensibilisierung und Verständnis für Datenklassifizierungsrichtlinien, warum sie wichtig sind und wie sie eingehalten werden.
- Einhaltung interner Überprüfungen, die auf Datenverlust und Cybersicherheitskontrollen abzielen.
- Schulung und Einbindung von Benutzern, damit sie sich der Notwendigkeit einer korrekten Klassifizierung in ihrer täglichen Arbeit und der Anwendung der richtigen Klassifizierungsmaßnahmen berücksichtigen.

## <a name="change-management-and-training"></a>Change Management und Schulungen

Organisationen verwenden heute Tools wie Microsoft 365, um ihr Datenklassifizierungsframework zu implementieren. Der Zweck besteht darin, die Klassifizierung von Daten zu automatisieren und nicht den Aufwand für Ihre Mitarbeiter zu erhöhen. Diese Struktur bedeutet nicht, dass Ihre Organisation nicht dafür verantwortlich ist, das Bewusstsein für die Notwendigkeit der Verwaltung von Inhalten zu erhöhen und die Organisation vor den in diesem Dokument beschriebenen Risiken zu schützen. Die führende Methode besteht weiterhin darin, Sensibilisierungsschulungen im Rahmen des jährlichen Schulungsplans organisationsweit durchzuführen. Unsere Erfahrung zeigt, dass die Bereitstellung robuster und umfassender Anstrengungen bei der Schulung Ihrer Benutzer, die die wichtigste Zielgruppe sind, die diese Arbeit ausführt, ihren "Buy-In"-Aufwand erhöht und die Akzeptanz und Qualität steigern kann. Das Hinzufügen von [Bezeichnungsempfehlungen](/microsoft-365/compliance/apply-sensitivity-label-automatically#recommend-that-the-user-apply-a-sensitivity-label) und In-App-Tipps kann diese Bemühungen verstärken. Diese Schulung muss kein umfangreicher eigenständiger Kurs sein. Ihre Organisation kann sie in andere regelmäßige Schulungen wie ihre jährliche Schulung zur Informationssicherheit integrieren und dann eine Übersicht über die Datenklassifizierungsstufen und Definitionen enthalten. Der Wichtigste ist, dass Ihre Mitarbeiter wissen, dass das Tool zwar die Klassifizierung von Daten automatisiert, aber die Gesamtverantwortlichkeit der einzelnen Benutzer für den Schutz der Daten gemäß Ihrer Unternehmensrichtlinie nicht beseitigt.

Darüber hinaus sollten Sie eine ausführlichere Schulung für IT- und Informationssicherheitsteams in Betracht ziehen, um die Betriebsbereitschaft zu erhöhen. Die Teams, die das Tool und das Datenklassifizierungsframework verwalten, müssen sich auf derselben Seite befinden. Für diese Koordination müssen Sie möglicherweise in einen robusteren Schulungsplan investieren, der möglicherweise häufiger als jährlich ist. Investitionen in häufigere Schulungen stellen einen weiteren Weg dar, um risiken für Ihre Organisation zu verringern. Dieses Team ist für die Implementierung verantwortlich und kann daher ein Fehlerpunkt sein, wenn es nicht mit dem Tool und der Richtlinie trainiert wird.

Wenn Sie Inhalte im Tool manuell markieren müssen, ist die Entwicklung einer Gruppe von Superbenutzern, die erweiterte Schulungen erhalten haben, angemessen. Diese Superbenutzer würden in Situationen eingebunden, in denen Benutzer Dokumente manuell mit Datenempfindlichkeitsbezeichnungen kennzeichnen müssen und tiefgehende Kenntnisse über das Datenklassifizierungsframework und die gesetzlichen Anforderungen Ihrer Organisation haben.

Schließlich sollte Ihre Führung die Förderung von Informationssicherheitsverhalten priorisieren, um die Bedeutung von Risikomanagement-Initiativen für die Mitarbeiter zu stärken. Dazu gehören die Entwicklung und Implementierung eines stabilen Datenklassifizierungsframeworks und die Zuweisung wichtiger Führungskräfte zur Förderung der Initiative, die manchmal als Pioniere oder Champions der Änderung bezeichnet werden.

## <a name="governance-and-maintenance"></a>Governance und Wartung

Nachdem Sie Ihr Datenklassifizierungsframework entwickelt und implementiert haben, sind fortlaufende Governance und Wartung entscheidend für Ihren Erfolg. Zusätzlich zur Nachverfolgung, wie Vertraulichkeitsbezeichnungen in der Praxis verwendet werden, müssen Sie Ihre Kontrollanforderungen basierend auf Änderungen der Vorschriften, führenden Praktiken für die Cybersicherheit und der Art der von Ihnen verwalteten Inhalte aktualisieren. Governance- und Wartungsaktivitäten können Folgendes umfassen:

- Einrichten eines Governancekörpers, der der Datenklassifizierung oder dem Hinzufügen einer Datenklassifizierungsverantwortlichkeit zur Chart einer vorhandenen Informationssicherheitsinstanz zugeordnet ist.
- Definieren von Rollen und Zuständigkeiten für Benutzer, die die Datenklassifizierung überwachen.
- Einrichten von KPIs zum Überwachen und Messen des Fortschritts.
- Nachverfolgen führender Praktiken und regulatorischer Änderungen im Bereich Internetsicherheit.
- Entwickeln von Standardvorgehensweisen, die ein Datenklassifizierungsframework unterstützen und erzwingen.

## <a name="industry-considerations"></a>Überlegungen zur Branche

Obwohl die Grundprinzipien für die Entwicklung eines starken Datenklassifizierungsframeworks universell sind, hängen die Details Ihres Frameworks von der Art Ihrer Branche und den einzigartigen Compliance- und Sicherheitsfaktoren ab, die Ihre Daten erfordern.

Beispielsweise müssen Finanzdienstleistungsunternehmen je nach Umfang ihres Unternehmens und der Regionen, in denen sie tätig sind, möglicherweise die Einhaltung mehrerer gesetzlicher Rahmenwerken in Betracht ziehen. Wertpapierunternehmen in den Vereinigten Staaten müssen Kontobestimmungen wie [sec Rule 17a-4(f)](/compliance/regulatory/offering-sec-17a-4) oder [FINRA Rule 4511](/microsoft-365/compliance/offering-finra-4511) entsprechen, die Anforderungen im Zusammenhang mit der Sicherheit und Aufbewahrung von Büchern und Datensätzen erfüllen. Entsprechend müssen Firmen, die im Vereinigten Königreich tätig sind, die [FCA-Compliance](/microsoft-365/compliance/offering-fca-uk)berücksichtigen.

Regierungsbehörden sehen sich verschiedenen Vorschriften für ihre Daten gegenüber, die je nach Gebiet und Art ihrer Arbeit variieren. In den Vereinigten Staaten unterliegen beispielsweise Regierungsbehörden und ihre Agenten, die auf Federal Tax Information (FTI) zugreifen, [DEM IRS 1075,](/microsoft-365/compliance/offering-irs-1075)der darauf abzielt, das Risiko von Verlust, Verletzung oder Missbrauch von Federal Tax Information zu minimieren.

Während Finanzdienstleistungsunternehmen und Behörden zu den am stärksten regulierten Organisationen der Welt gehören, müssen die meisten Unternehmen branchenspezifische Überlegungen berücksichtigen. Beispiele:

- Organisationen der [Gesundheitsbranche, die die Einhaltung von HIPAA sicherstellen.](/microsoft-365/compliance/offering-hipaa-hitech)
- Bildungseinrichtungen, von K-12-Schulen bis hin zu Schulen, verwalten [FERPA-Compliance.](/microsoft-365/compliance/offering-ferpa)
- Hersteller von Betäubereien, die an den [GxP-Richtlinien](/microsoft-365/compliance/offering-gxp) in ihrem Land oder ihrer Region rund um die Informationssicherheit arbeiten.
- Medien, Einzelhandel und viele andere Unternehmen, die mit [der DSGVO-Compliance](/microsoft-365/compliance/gdpr)zu tun haben.
- Bereitstellung und Speicherung von Unterhaltungs-, Software- und Informationsinhalten im Zusammenhang mit [CDSA.](/microsoft-365/compliance/offering-cdsa)
- Informationssicherheit der Energiebranche, die dem [NERC CIP-Standard entspricht.](/microsoft-365/compliance/offering-nerc-cip)

## <a name="implementing-your-data-classification-framework-in-microsoft-365"></a>Implementieren des Datenklassifizierungsframeworks in Microsoft 365

Nachdem Sie Ihr Datenklassifizierungsframework entwickelt haben, ist der nächste Schritt die Implementierung. Mit [dem Microsoft 365 Compliance Center](https://compliance.microsoft.com/) können Administratoren ihre Daten in Übereinstimmung mit ihrem Datenklassifizierungsframework ermitteln, klassifizieren, überprüfen und überwachen. Vertraulichkeitsbezeichnungen können zum Schutz Ihrer Daten verwendet werden, indem verschiedene Schutzmaßnahmen wie Verschlüsselung und Inhaltskennzeichnung erzwungen werden. Sie können manuell auf Daten angewendet werden. standardmäßig basierend auf Richtlinieneinstellungen; oder automatisch als Ergebnis einer Bedingung wie z. B. identifizierter personenbezogener Informationen.

Für kleinere Organisationen oder Organisationen mit einem relativ optimierten Datenklassifizierungsframework reicht die Erstellung einer einzigen Vertraulichkeitsbezeichnung für jede Ihrer Datenklassifizierungsstufen möglicherweise aus. Das folgende Beispiel zeigt eine 1:1-Datenklassifizierungsebene zur Zuordnung von Vertraulichkeitsbezeichnungen:

|**Klassifizierungsbezeichnung**|**Vertraulichkeitsbezeichnung**|**Bezeichnungseinstellungen**|**Veröffentlicht in**|
|:-----------------------|:--------------------|:-----------------|:---------------|
| Uneingeschränkte | Uneingeschränkte | Anwenden der Fußzeile "Uneingeschränkt" | Alle Benutzer |
| Allgemein | Allgemein | Anwenden der Fußzeile "Allgemein" | Alle Benutzer |

>[!TIP]
>Während eines internen Pilotprojekts zum Schutz von Informationen von Microsoft gab es Probleme mit dem Verständnis und der Verwendung der Bezeichnung "Persönlich". Die Benutzer waren verunsichert, ob dies personenbezogene Informationen bedeutete oder nur mit einer persönlichen Frage zusammenhängt. Die Bezeichnung wurde in "Nicht-Geschäft" geändert, um übersichtlicher zu sein. Dieses Beispiel zeigt, dass taxonomie nicht von Anfang an perfekt sein muss. Beginnen Sie mit dem, was Sie für richtig halten, testen Sie es, und passen Sie die Bezeichnung bei Bedarf basierend auf Feedback an.

Für größere Organisationen mit globaler Reichweite oder komplexeren Anforderungen an die Informationssicherheit kann diese 1:1-Beziehung zwischen der Anzahl der Klassifizierungsebenen in Ihrer Richtlinie und der Anzahl der Vertraulichkeitsbezeichnungen in Ihrer Microsoft 365 Umgebung eine Herausforderung darstellen. Diese Herausforderung gilt insbesondere für globale Organisationen, in denen eine bestimmte Datenklassifizierungsstufe, z. B. "Eingeschränkt", je nach Region eine andere Definition oder unterschiedliche Gruppe von Steuerelementen aufweisen kann.

Weitere Informationen zur Implementierung finden Sie unter ["Grundlegendes zur Datenklassifizierung"](/microsoft-365/compliance/data-classification-overview) und ["Informationen zu Vertraulichkeitsbezeichnungen".](/microsoft-365/compliance/sensitivity-labels)

## <a name="references"></a>Informationsquellen

- [Microsoft Compliance-Angebote](/microsoft-365/compliance/offering-home)
