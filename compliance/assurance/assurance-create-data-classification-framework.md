---
title: Erstellen eines gut entworfenen Datenklassifizierungsframeworks
description: In diesem Artikel finden Sie eine Übersicht darüber, wie Sie ein gut entworfenes Datenklassifizierungsframework für Microsoft 365 erstellen.
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
ms.openlocfilehash: df2bc373fea046ac120c40c57af2ba061d2b0781
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497808"
---
# <a name="create-a-well-designed-data-classification-framework"></a>Erstellen eines gut entworfenen Datenklassifizierungsframeworks

Berücksichtigen Sie bei der Entwicklung, Überarbeitung oder Verfeinerung Ihres Datenklassifizierungsframework die folgenden führenden Methoden:

- Gehen Sie nicht von 0 bis **100 am 1.** Tag aus: Microsoft empfiehlt einen Crawl-Walk-Run-Ansatz, bei dem für die Organisation wichtige Features priorisiert und einer Zeitachse zugeordnet werden. Führen Sie den ersten Schritt aus, stellen Sie sicher, dass er erfolgreich war, und gehen Sie dann mit der nächsten Phase fort, in der die gelernten Erkenntnisse angewendet werden. Denken Sie daran, dass Ihre Organisation beim Entwerfen ihres Datenklassifizierungsframeworks weiterhin Risiken ausgesetzt ist. Daher ist es in Ordnung, klein mit nur wenigen Klassifizierungsstufen zu beginnen und später nach Bedarf zu erweitern.
- **Sie schreiben nicht** nur für Cybersicherheitsexperten: Datenklassifizierungsframeworks sind für eine breite Zielgruppe gedacht, einschließlich Ihrer durchschnittlichen Mitarbeiter, Ihrer Rechts- und Complianceteams und Ihres IT-Teams. Es ist wichtig, klare, leicht verständliche Definitionen für Ihre Datenklassifizierungsebenen zu schreiben und möglichst reale Beispiele zu bieten. Versuchen Sie, den Jargon zu vermeiden und ein Glossar für Akronyme und hoch technische Begriffe in Betracht zu ziehen. Verwenden Sie beispielsweise "Personenbezogene Informationen" und stellen Sie eine Definition zur Verfügung, anstatt einfach "PII" zu sagen.
- **Datenklassifizierungsframeworks** sollen implementiert werden: Damit Datenklassifizierungsframeworks erfolgreich sind, müssen sie implementiert werden. Dies ist besonders wichtig, wenn die Steuerungsanforderungen für jede Datenklassifizierungsstufe angepasst werden. Stellen Sie sicher, dass die Anforderungen klar definiert sind und dass sie alle Mehrdeutigkeiten antizipieren und beseitigen, die während der Implementierung auftreten können. Wenn Sie z. B. über ein Steuerelement für personenbezogene Informationen verfügen, müssen Sie genau sagen, was dieses Steuerelement bedeutet, z. B. sozialversicherungs- oder reisepassnummer.
- **Gehen Sie nur präzise vor, wenn** Sie : Datenklassifizierungsframeworks in der Regel zwischen 3 und 5 Datenklassifizierungsebenen enthalten. Aber nur weil *Sie fünf* Ebenen enthalten können, bedeutet dies nicht, dass Sie *sollten*. Berücksichtigen Sie bei der Entscheidung über die Anzahl der benötigten Klassifizierungsstufen die folgenden Kriterien:

    - Ihre Branche und ihre damit verbundenen behördlichen Verpflichtungen (stark regulierte Branchen benötigen in der Regel mehr Klassifizierungsebenen)
    - Der betriebsbereite Aufwand, der für die Aufrechterhaltung eines komplexeren Frameworks erforderlich ist
    - Ihre Benutzer und ihre Fähigkeit, die mit mehr Klassifizierungsstufen verbundene erhöhte Komplexität und Nuance zu erfüllen
    - Benutzerfreundlichkeit und Barrierefreiheit beim Anwenden einer manuellen Klassifizierung auf mehrere Gerätetypen

- **Holen Sie die richtigen Personen mit** ein: Die Einbindung eines hochrangigen Stakeholders ist für den Erfolg wichtig, da viele Projekte ohne Unterstützung durch die Geschäftsleitung nur schwer beginnen oder länger dauern können. Datenklassifizierungsframeworks befinden sich in der Regel im Besitz von Informationstechnologieteams, können jedoch rechtliche, compliance-, datenschutz- und änderungsverwaltungsauswirkungen haben. Um sicherzustellen, dass Sie ein Framework erstellen, das Zum Schutz Ihres Unternehmens beitrat, müssen Sie die Datenschutz- und Rechtsbeteiligten wie Ihren Chief Privacy Officer und das Office of General Counsel in die Entwicklung Ihrer Richtlinie mit einbesorgen. Wenn Ihre Organisation über eine Complianceabteilung, Experten für informationspolitische Steuerung oder ein Datensatzverwaltungsteam verfügt, kann sie auch wertvollen Input haben. Da Ihr Framework für das Unternehmen freigegeben wird, spielt Ihre Kommunikationsabteilung auch eine wichtige Rolle für interne Nachrichtenübermittlung und -einführung.
- **Balance zwischen Sicherheit und Komfort:** Ein häufiger Fehler besteht im Entwurf eines sicheren, aber zu restriktiven Datenklassifizierungsframeworks. Dieses Framework wurde möglicherweise im Sinne der Sicherheit entworfen, ist aber in der Praxis oft schwierig zu implementieren. Wenn Benutzer komplexe, starre und zeitaufwändige Verfahren befolgen müssen, um das Framework in ihrem täglichen Leben anzuwenden, besteht immer das Risiko, dass sie nicht mehr an ihren Wert glauben und schließlich die folgenden Verfahren beenden. Dieses Risiko besteht auf allen Ebenen der Organisation, einschließlich Führungskräften (C-Suite) innerhalb der Organisation. Eine gute Balance zwischen Sicherheit und Komfort sowie einfach zu verwendende Tools führen in der Regel zu einer umfassenderen Benutzeradzeptanz und -verwendung. Wenn ihr Framework Lücken hat, warten Sie nicht, bis alles perfekt ist, um mit der Implementierung zu beginnen. Bewerten Sie stattdessen das Risiko oder die Lücke, erstellen Sie einen Plan zur Minderung, und gehen Sie weiter. Denken Sie daran, dass der Informationsschutz eine Reise ist und nicht über Nacht aktiviert und dann durchgeführt wird. Planen, implementieren Sie einige Funktionen, bestätigen Sie den Erfolg, und iterieren Sie den nächsten Meilenstein, während tools sich weiterentwickeln und Benutzer Reife und Erfahrung erlangen.

Beachten Sie außerdem, dass ein Datenklassifizierungsframework nur das *behandelt, was* Ihre Organisation zum Schutz vertraulicher Daten tun sollte. Datenklassifizierungsframeworks werden häufig von  Regeln oder Richtlinien für die Datenverarbeitung begleitet, die definieren, wie diese Richtlinien aus technischer und technischer Sicht festgelegt werden. In den folgenden Abschnitten wenden wir uns einigen praktischen Anleitungen zu, wie Sie Ihr Datenklassifizierungsframework von einem Richtliniendokument zu einer vollständig implementierten und umsetzbaren Initiative nutzen können.

## <a name="pain-points-in-creating-a-data-classification-framework"></a>Schmerzpunkte beim Erstellen eines Datenklassifizierungsframework

Die Datenklassifizierungsbemühungen sind naturgeblich weit reichend und berühren nahezu jede Geschäftsfunktion innerhalb eines Unternehmens. Aufgrund dieses breiten Umfangs und der Komplexität der Verwaltung von Inhalten in modernen digitalen Umgebungen stehen Unternehmen häufig vor Herausforderungen, wenn sie wissen, wo sie beginnen, wie sie eine erfolgreiche Implementierung verwalten und wie sie ihren Fortschritt messen können. Häufige Schmerzpunkte sind häufig:

- Entwerfen eines robusten und leicht verständlichen Datenklassifizierungsframeworks, einschließlich der Festlegung von Klassifizierungsstufen und zugeordneten Sicherheitskontrollen.
- Entwickeln eines Implementierungsplans, der die Bestätigung der geeigneten Technologielösung, das Ausrichten des Plans an vorhandene Geschäftsprozesse und die Identifizierung von Auswirkungen auf die Mitarbeiter umfasst.
- Einrichten eines Datenklassifizierungsframework innerhalb der ausgewählten Technologielösung und Behebung von Lücken zwischen den Technologiefunktionen des Tools und dem Framework selbst.
- Einrichten einer Steuerungsstruktur, die die wartung und integrität von Datenklassifizierungsbemühungen überwacht.
- Identifizieren bestimmter KpIs (Key Performance Indicators) zum Überwachen und Messen des Fortschritts.
- Verbesserung des Bewusstseins und Verständnisses von Datenklassifizierungsrichtlinien, warum sie wichtig sind und wie sie erfüllt werden können.
- Einhaltung interner Überprüfungen, die auf Kontrollen für Datenverlust und Cybersicherheit zielen.
- Schulung und Einbindung von Benutzern, damit sie die Notwendigkeit einer richtigen Klassifizierung in ihrer täglichen Arbeit berücksichtigen und die richtigen Klassifizierungsmaßnahmen anwenden.

## <a name="change-management-and-training"></a>Änderungsverwaltung und -schulung

Organisationen verwenden heute Tools wie Microsoft 365, um ihr Datenklassifizierungsframework zu implementieren. Der Zweck besteht in dem Versuch, die Klassifizierung von Daten zu automatisieren und die Belastung ihrer Mitarbeiter nicht zu erhöhen. Diese Struktur bedeutet nicht, dass Ihre Organisation nicht dafür verantwortlich ist, das Bewusstsein für die Notwendigkeit zu erhöhen, Inhalte zu verwalten und die Organisation vor den in diesem Dokument behandelten Risiken zu schützen. Die führende Methode besteht weiterhin in der Durchführung von Sensibilisierungsschulungen in der gesamten Organisation im Rahmen des jährlichen Schulungsplans. Unsere Erfahrung zeigt, dass die Durchführung von robusten und umfassenden Anstrengungen bei der Schulung Ihrer Benutzer, die die Hauptbenutzer dieser Arbeit sind, ihr "Buy-In" erhöht und die Akzeptanz und Qualität steigern kann. Das [Hinzufügen von Bezeichnungsempfehlungen](/microsoft-365/compliance/apply-sensitivity-label-automatically#recommend-that-the-user-apply-a-sensitivity-label) und In-App-Tipps kann diese Bemühungen verstärken. Diese Schulung muss kein umfangreicher eigenständiger Kurs sein. Ihre Organisation kann sie in andere reguläre Schulungen integrieren, z. B. ihre jährliche Schulung zur Informationssicherheit, und dann eine Übersicht über Datenklassifizierungsebenen und -definitionen enthalten. Der Hauptpunkt ist, dass Ihre Mitarbeiter das Verständnis haben, dass das Tool zwar die Klassifizierung von Daten automatisiert, jedoch nicht die gesamtverantwortliche Verantwortung jedes Benutzers für den Schutz der Daten gemäß Ihrer Unternehmensrichtlinie beseitigt.

Darüber hinaus sollten Sie eine detailliertere Schulung für IT- und Informationssicherheitsteams in Betracht ziehen, um die betriebsbereite Bereitschaft zu verstärken. Die Teams, die das Tool und das Datenklassifizierungsframework verwalten, müssen auf derselben Seite sein. Bei dieser Koordination müssen Sie möglicherweise in einen stabileren Schulungszeitplan investieren, der häufiger als jährlich sein kann. Investitionen in häufigere Schulungen stellen eine weitere Möglichkeit dar, das Risiko für Ihre Organisation zu reduzieren. Dieses Team ist für die Implementierung verantwortlich und kann daher ein Fehlerpunkt sein, wenn es nicht für das Tool und die Richtlinie geschult wird.

Wenn Sie Inhalte im Tool manuell markieren müssen, ist die Entwicklung einer Gruppe von Superbenutzern geeignet, die erweiterte Schulungen erhalten haben. Diese Superbenutzer wären für Situationen engagiert, in denen Benutzer Dokumente manuell mit Datensensitivitätsbezeichnungen kennzeichnen müssen und ein tiefes Verständnis des Datenklassifizierungsframework und der gesetzlichen Anforderungen Ihrer Organisation haben.

Schließlich sollte Ihre Führung die Förderung von Informationssicherheitsverhalten priorisieren, um die Bedeutung von Risikomanagement-Initiativen für die Belegschaft zu stärken. Dazu gehören die Entwicklung und Implementierung eines robusten Datenklassifizierungsframeworks und die Zuweisung wichtiger Führungskräfte zur Förderung der Initiative, die manchmal als "Gesandte" oder "Champions der Änderung" bezeichnet werden.

## <a name="governance-and-maintenance"></a>Steuerung und Wartung

Nachdem Sie Ihr Datenklassifizierungsframework entwickelt und implementiert haben, sind fortlaufende Steuerung und Wartung entscheidend für Ihren Erfolg. Sie müssen nicht nur nachverfolgen, wie Vertraulichkeitsbezeichnungen in der Praxis verwendet werden, sondern auch Ihre Kontrollanforderungen basierend auf Änderungen an Vorschriften, führenden Methoden zur Cybersicherheit und der Art der von Ihnen verwalteten Inhalte aktualisieren. Die Steuerungs- und Wartungsbemühungen können Folgendes umfassen:

- Einrichten eines Steuerungsgremiums für die Datenklassifizierung oder Hinzufügen einer Verantwortlichkeit für die Datenklassifizierung zur Charter eines vorhandenen Informationssicherheitsorgans.
- Definieren von Rollen und Verantwortlichkeiten für Benutzer, die die Datenklassifizierung überwachen.
- Einrichten von KPIs zum Überwachen und Messen des Fortschritts.
- Nachverfolgen führender Praktiken und behördlicher Änderungen in der Cybersicherheit.
- Entwickeln von Standardbetriebsverfahren, die ein Datenklassifizierungsframework unterstützen und erzwingen.

## <a name="industry-considerations"></a>Überlegungen in der Branche

Während die grundlegenden Prinzipien für die Entwicklung eines starken Datenklassifizierungsframework universell sind, hängen die Details Ihres Frameworks von der Art Ihrer Branche und den einzigartigen Compliance- und Sicherheitsfaktoren ab, die Ihre Daten fordern.

Beispielsweise müssen Finanzdienstleister je nach Umfang ihres Geschäfts und den Regionen, in denen sie tätig sind, die Einhaltung mehrerer gesetzlicher Rahmenbedingungen in Betracht ziehen. Wertpapierfirmen in den Vereinigten Staaten müssen Kontobestimmungen wie [SEC Rule 17a-4(f)](/compliance/regulatory/offering-sec-17a-4) oder [FINRA Rule 4511](/microsoft-365/compliance/offering-finra-4511) einhalten, die Anforderungen im Einklang mit der Sicherheit und Aufbewahrung von Büchern und Datensätzen erfüllen. Entsprechend müssen Unternehmen, die im Vereinigten Königreich tätig sind, die [FCA-Compliance berücksichtigen.](/microsoft-365/compliance/offering-fca-uk)

Behörden sehen sich verschiedenen Vorschriften für ihre Daten gegenüber, die je nach Gebiet und Art ihrer Arbeit variieren. In den USA unterliegen beispielsweise Behörden und ihre Agenten, die auf Bundessteuerinformationen (Federal Tax Information, FTI) zugreifen, [IRS 1075](/microsoft-365/compliance/offering-irs-1075), mit dem das Risiko eines Verlusts, einer Verletzung oder eines Missbrauchs von Steuerinformationen des Bundes minimiert werden soll.

Während Finanzdienstleister und Regierungsbehörden zu den am stärksten regulierten Organisationen der Welt gehören, haben die meisten Unternehmen branchenspezifische Überlegungen, die berücksichtigt werden müssen. Beispiele:

- Organisationen der [Gesundheitsbranche, die die Einhaltung von HIPAA sicherstellen.](/microsoft-365/compliance/offering-hipaa-hitech)
- Bildungseinrichtungen, von K-12-Schulen bis zu Universitäten, verwalten [die FERPA-Compliance.](/microsoft-365/compliance/offering-ferpa)
- Drug manufacturers working to comply to [GxP guidelines](/microsoft-365/compliance/offering-gxp) in their country or region around information security.
- Medien, Einzelhandel und viele andere Unternehmen, die sich mit der Einhaltung der [DSGVO beschäftigt haben.](/microsoft-365/compliance/gdpr)
- Übermittlung und Speicherung von Unterhaltungs-, Software- und Informationsinhalten im Umgang mit [CDSA](/microsoft-365/compliance/offering-cdsa).
- Energiebranche Informationssicherheit, die dem [NERC CIP-Standard entspricht.](/microsoft-365/compliance/offering-nerc-cip)

## <a name="implementing-your-data-classification-framework-in-microsoft-365"></a>Implementieren Ihres Datenklassifizierungsframework in Microsoft 365

Nachdem Sie Ihr Datenklassifizierungsframework entwickelt haben, ist der nächste Schritt die Implementierung. Das [Microsoft 365 Compliance Center](https://compliance.microsoft.com/) ermöglicht Administratoren das Ermitteln, Klassifizieren, Überprüfen und Überwachen ihrer Daten in Übereinstimmung mit ihrem Datenklassifizierungsframework. Vertraulichkeitsbezeichnungen können verwendet werden, um Ihre Daten zu schützen, indem verschiedene Schutzmaßnahmen wie Verschlüsselung und Inhaltskennzeichnung durchgesetzt werden. Sie können manuell auf Daten angewendet werden. standardmäßig basierend auf Richtlinieneinstellungen; oder automatisch, als Ergebnis einer Bedingung, z. B. identifizierter PII.

Für kleinere Organisationen oder Organisationen mit einem relativ optimierten Datenklassifizierungsframework kann die Erstellung einer einzelnen Vertraulichkeitsbezeichnung für jede Ihrer Datenklassifizierungsstufen ausreichen. Das folgende Beispiel zeigt eine 1:1-Datenklassifizierungsstufe für die Zuordnung von Vertraulichkeitsbezeichnungen:

|**Klassifizierungsbezeichnung**|**Vertraulichkeitsbezeichnung**|**Bezeichnungseinstellungen**|**Veröffentlicht in**|
|:-----------------------|:--------------------|:-----------------|:---------------|
| Uneingeschränkt | Uneingeschränkt | Anwenden der Fußzeile "Uneingeschränkt" | Alle Benutzer |
| Allgemein | Allgemein | Anwenden der Fußzeile "Allgemein" | Alle Benutzer |

>[!TIP]
>Während eines Internen Microsoft-Pilotprojekts zum Schutz von Informationen gab es Schwierigkeiten beim Verständnis und der Verwendung der Bezeichnung "Personal". Die Benutzer waren verwirrt, ob dies piI bedeutete oder lediglich mit einer persönlichen Angelegenheit zusammenhing. Die Bezeichnung wurde in "Nicht-Geschäftliches" geändert, um klarer zu sein. Dieses Beispiel zeigt, dass die Taxonomie nicht von Anfang an perfekt sein muss. Beginnen Sie mit dem, was Sie für richtig halten, pilotieren Sie sie, und passen Sie die Bezeichnung bei Bedarf basierend auf Feedback an.

Für größere Organisationen mit globaler Reichweite oder komplexeren Informationssicherheitsanforderungen ist diese 1:1-Beziehung zwischen der Anzahl der Klassifizierungsebenen in Ihrer Richtlinie und der Anzahl der Vertraulichkeitsbezeichnungen in Ihrer Microsoft 365-Umgebung eine Herausforderung. Diese Herausforderung gilt insbesondere in globalen Organisationen, in denen eine bestimmte Datenklassifizierungsstufe wie "Restricted" je nach Region eine andere Definition oder einen anderen Satz von Steuerelementen haben kann.

Weitere Informationen zur Implementierung finden Sie unter [Verstehen der Datenklassifizierung](/microsoft-365/compliance/data-classification-overview) und [Informationen zu Vertraulichkeitsbezeichnungen](/microsoft-365/compliance/sensitivity-labels).

## <a name="references"></a>Informationsquellen

- [Microsoft Compliance-Angebote](/microsoft-365/compliance/offering-home)
