---
title: Sicherheit des physischen Zugriffs in Rechenzentren
description: Erfahren Sie mehr über die Physische Zugriffssicherheit von Microsoft-Rechenzentren.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: f7cc71354c4be52d97c8b4b6efbe5a88ca9413a5
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265112"
---
# <a name="datacenter-physical-access-security"></a>Sicherheit des physischen Zugriffs in Rechenzentren

Microsoft ist sich der Bedeutung des Schutzes von Kundendaten bewusst und setzt sich für die Sicherung der Rechenzentren ein, in denen sie enthalten sind. Microsoft-Rechenzentren sind so konzipiert, aufgebaut und betrieben, dass der physische Zugriff auf die Bereiche, in denen Kundendaten gespeichert werden, strikt eingeschränkt wird.

Die physische Sicherheit in Rechenzentren entspricht dem Prinzip der Tiefenschutzmaßnahmen. Es werden mehrere Sicherheitsmaßnahmen implementiert, um das Risiko zu verringern, dass nicht autorisierte Benutzer auf Daten und andere Rechenzentrumsressourcen zugreifen.

- **Perimetersicherheit:** Microsoft-Rechenzentren sind nichtdescripte Gebäude mit Umkreis-Fencing und 24-Stunden-Beleuchtung im Außenbereich. Hohe Gitter aus Stählen und Konkretem umfassen jeden Zoll des Perimeters, und der gesamte Zugang zum Rechenzentrums-Campus muss über einen genau definierten Zugriffspunkt erfolgen. Mit Kameras überwachte Eingangstore und Rundgänge durch Wachdienstpersonal stellen sicher, dass das Betreten und Verlassen auf bestimmte Bereiche beschränkt ist. Poller und andere Maßnahmen schützen das Rechenzentrum von außen vor potenziellen Bedrohungen, einschließlich nicht autorisiertem Zugang.
- **Betreten des Rechenzentrums:** Der Eingang des Rechenzentrums ist mit professionellen Sicherheitsbeauftragten besetzt, die strenge Schulungen und Hintergrundüberprüfungen durchlaufen haben. Sicherheitsbeauftragte kontrollieren routinemäßig das Rechenzentrum, und Videofeeds von Kameras innerhalb des Rechenzentrums werden immer überwacht.
- **Innerhalb des Rechenzentrums:** Beim Betreten des Gebäudes ist die zweistufige Authentifizierung mit Biometrie erforderlich, um den Übergang durch das Rechenzentrum fortzusetzen. Nach der Authentifizierung wird zugriff auf den autorisierten Teil des Rechenzentrums gewährt und nur für die Zeit, die genehmigt wurde. Innerhalb des Rechenzentrums erfordern Bereiche, die als streng vertraulich gekennzeichnet sind, eine zusätzliche zweistufige Authentifizierung.
- **Rechenzentrumsfläche:** Auf die Rechenzentrumsfläche kann nur mit vorheriger Genehmigung und nach einer vollständigen Body-Metal-Erkennung zum Zeitpunkt der Eingabe zugegriffen werden. Um das Risiko zu verringern, dass nicht autorisierte Daten in das Rechenzentrum gelangen oder es verlassen, können nur genehmigte Geräte den Weg in die Rechenzentrumsfläche finden. Darüber hinaus überwachen Videokameras die Vorder- und Rückseite jedes Server-Racks. Beim Verlassen der Rechenzentrumsfläche werden alle Personen einer zusätzlichen Ganzkörper-Metal-Erkennungsuntersuchung unterzogen.
- **Verlassen des Rechenzentrums:** Um die Rechenzentrumseinrichtung zu verlassen, muss jede Person einen abschließenden Sicherheitsprüfpunkt durchlaufen, und alle Besucher müssen ihre temporären Badges ablegen. Nach der Sammlung werden alle Besucher-Badges entfernt, bevor sie für zukünftige Besuche wiederverwendet werden.

## <a name="access-provisioning"></a>Zugriffsbereitstellung

Das Dcm-Team (Datacenter Management) hat betriebliche Verfahren implementiert, um den physischen Zugriff nur auf autorisierte Mitarbeiter, Auftragnehmer und Besucher zu beschränken. Temporäre oder dauerhafte Zugriffsanforderungen werden mithilfe eines Ticketsystems nachverfolgt. Badges werden entweder für Personal ausgestellt oder aktiviert, das nach der Überprüfung der Identifizierung Zugriff benötigt. Physische Schlüssel und temporäre Zugriffsabzeichen werden im Security Operations Center (SOC) gesichert.

Microsoft-Rechenzentren unterliegen einer Richtlinie mit den geringsten Rechten, was bedeutet, dass der Zugriff auf Rechenzentren auf Mitarbeiter mit genehmigten geschäftlichen Anforderungen beschränkt ist, die nicht mehr Zugriff haben als nötig. Zugriffsanforderungen sind zeitlich begrenzt und werden nur verlängert, wenn der geschäftliche Zweck des Beantragenden gültig bleibt.

Datencenter-Zugriffseinträge werden in Form genehmigter Anforderungen verwaltet. Anforderungen können nur vom DCM-Team genehmigt werden, und Besucherzugriffsanforderungen an Rechenzentren werden aufgezeichnet und für zukünftige Untersuchungen zur Verfügung gestellt.

## <a name="datacenter-security-personnel"></a>Sicherheitspersonal des Rechenzentrums

Sicherheitsmitarbeiter in den Rechenzentren und auf dem Campus sind für die folgenden Aktivitäten verantwortlich:

- Betreiben Sie Arbeitsstationen, die sich im Security Operations Center innerhalb des primären Verwaltungsbaus befinden.
- Führen Sie regelmäßige Überprüfungen durch exemplarische Vorgehensweisen und Prüfungen der Anlage durch.
- Reagieren auf Brandalarm und Sicherheitsprobleme
- Verteilen von Sicherheitspersonal zur Unterstützung von Serviceanfragen und Notfällen
- Bereitstellen regelmäßiger Updates zu Sicherheitsereignissen und Eintragsprotokollen für das Rechenzentrumsverwaltungsteam
- Betreiben und Überwachen von Alarm-, Zugriffssteuerungs- und Überwachungssystemen

## <a name="visitor-access"></a>Besucherzugriff

Die Sicherheitsüberprüfung und -eincheckung ist für Mitarbeiter erforderlich, die vorübergehenden Zugriff auf das Innere der Rechenzentrumseinrichtung benötigen, einschließlich Tourgruppen und anderer Besucher. Besucher von Rechenzentren müssen vor ihrem geplanten Besuch einen Geheimhaltungsvereinbarung unterzeichnen, sich einer Überprüfung durch die Rechenzentrumsverwaltung unterziehen und eine Genehmigung der Rechenzentrumsverwaltung erhalten. Bei der ersten Ankunft werden Besucher des Rechenzentrums mit temporären, am wenigsten privilegierten Anmeldeinformationen versehen. Darüber hinaus wird ein Vollzeitmitarbeiter von Microsoft (Full-Time Employee, FTE) oder eine von der Rechenzentrumsverwaltung genehmigte und autorisierte, bestimmte Person zugewiesen, um Besucher während des Besuchs zu begleiten.

Alle Besucher, die über genehmigten Zugriff auf das Rechenzentrum verfügen, werden als *"Nur Begleitperson"* für ihre Badges festgelegt und müssen immer bei ihren Begleitpersonen bleiben. Begleitete Besucher haben keine Zugriffsebenen, die ihnen gewährt werden, und können nur mit dem Zugriff ihrer Begleitpersonen reisen. Die Begleitperson ist für die Überprüfung der Aktionen und des Zugriffs des Besuchers während des Besuchs des Rechenzentrums verantwortlich.

Der Besucherzugriff wird von der zugewiesenen Begleitperson und vom Control Room Supervisor über Closed Circuit Television (C XAML) und das Alarmüberwachungssystem überwacht. Besucher mit einer genehmigten Zugriffsanforderung lassen ihre Zugriffsanforderung zu dem Zeitpunkt überprüfen, zu dem ihre Identifizierung anhand einer von der Regierung ausgestellten Identifikation oder eines von Microsoft ausgestellten Badges überprüft wird. Besucher, die für den begleiteten Zugriff genehmigt wurden, erhalten ein selbst ablaufendes Sticky-Badge, und nach der Rückgabe wird der Zugriffsdatensatz innerhalb des Tools beendet. Wenn ein Besucher mit seiner Badge abbricht, läuft das Signal automatisch innerhalb von 24 Stunden ab.

Temporäre Zugriffsabzeichen werden im zugriffsgesteuerten SOC gespeichert und am Anfang und Ende jeder Schicht inventarisiert. Sicherheitsbeauftragte sind 24 x 7 besetzt, und physische Schlüssel werden in einem elektronischen Schlüsselverwaltungssystem gespeichert, das mit dem physischen Zugriffssystem verknüpft ist, das die PIN und das Zugriffssignal eines Sicherheitsbeauftragten erfordert, um Zugriff zu erhalten.

## <a name="access-review-and-deprovisioning"></a>Zugriffsüberprüfung und -bereitstellung

Das DCM-Team ist für die regelmäßige Überprüfung des Rechenzentrumszugriffs und die Durchführung einer vierteljährlichen Prüfung verantwortlich, um zu überprüfen, ob der einzelne Zugriff weiterhin erforderlich ist.

Bei Beendigungen oder Übertragungen wird der Zugriff der Person sofort aus dem System entfernt, und ihr Zugriffssignal wird entfernt. Dadurch werden alle Datencenterzugriffe entfernt, die die Person möglicherweise hatte. DCM-Teams führen auch vierteljährliche Zugriffsüberprüfungen durch, um die Eignung der Datencenter-Zugriffsliste im System zu überprüfen.

## <a name="key-management"></a>Schlüsselverwaltung

Physische/Hard-Tasten werden für bestimmte Mitarbeiter ausgecheckt, indem das Zugriffssignal der Person mit dem physischen Schlüssel abgeglichen wird. Eine Person muss über die entsprechende Zugriffsebene im Tool verfügen, um bestimmte Schlüssel auschecken zu können. Schlüssel sind außerhalb des Standorts nicht zulässig.

Die Hard Keys und Badges werden von Microsoft streng kontrolliert und täglich überwacht. Microsoft entschärft auch Risiken durch die Implementierung einer strikten Zuweisung von Zugriffsebenen sowie eine kontrollierte Verteilung und Verwaltung von Schlüsseln. Die primären Zugriffsmethoden in Rechenzentren sind elektronische Zugriffszeichen und biometrische Daten, die eine sofortige Sperrung des Zugriffs nach Bedarf ermöglichen. Microsoft verfügt über Verfahren, um geeignete Maßnahmen zu ermitteln, die dem Risiko für alle verlorenen Schlüssel entsprechen. Für diese Aktionen kann es erforderlich sein, einen Einzelnen-Server-Rack oder eine Einzelne-Server-Eingangstür und bis zur Erneutschlüsselung der gesamten Rechenzentrumseinrichtung neu zukeyen.

## <a name="access-logging-and-monitoring"></a>Zugriffsprotokollierung und -überwachung

Zugangsanträge sowie Betreten-/Verlassen-Ereignisse werden protokolliert und im Rahmen eines elektronischen Überwachungspfads gespeichert, sodass nach dem tatsächlichen Ereignis Datenabfragen und -abstimmungen erfolgen können. Zugangskontrollsystem-Berichte und Datenanalysen ermöglichen eine weitergehende Anomalieerkennung, um unnötigen und nicht autorisierten Zugriff zu erkennen und zu verhindern.

Überwachungssysteme für Rechenzentren überwachen kritische Rechenzentrumsbereiche wie den Haupteingang/-ausgang des Rechenzentrums, die Datencenter-Colocations-Eingangs-/-Exit-Bereiche, Diebesfelder, gesperrte Schränke, Gänge, Versand- und Empfangsbereiche, kritische Umgebungen, Umkreistüren und Parkbereiche. Überwachungsaufzeichnungen werden mindestens 90 Tage aufbewahrt, es sei denn, das lokale Recht schreibt etwas anderes vor.

Ein Kontrollraum-Supervisor ist immer im SOC, um den physischen Zugriff im Rechenzentrum zu überwachen. Die Videoüberwachung wird verwendet, um den physischen Zugriff auf das Rechenzentrum und das Informationssystem zu überwachen. Das Videoüberwachungssystem ist mit dem Gebäudealarmüberwachungssystem verknüpft, um die überwachung des physischen Zugriffs von Alarmpunkten zu unterstützen. Sicherheitsbeauftragte stellen sicher, dass nur das Personal mit ordnungsgemäßer Autorisierung Zugriff hat, und stellen sicher, dass alle Personen, die Geräte in kritische Infrastrukturanlagen bringen, die ordnungsgemäßen Verfahren befolgen.

Sicherheitsereignisse, die innerhalb des Rechenzentrums auftreten, werden vom Sicherheitsteam in einem Bericht dokumentiert, der als Sicherheitsereignisbenachrichtigung (Security Event Notification, SEN) bezeichnet wird. SEN-Berichte erfassen die Details eines Sicherheitsereignisses und müssen dokumentiert werden, nachdem ein Ereignis aufgetreten ist, um Details so genau wie möglich zu erfassen. SEN-Berichte enthalten auch die Untersuchungsanalyse, die in einem After Action Report (AAR) durchgeführt wird, der die Untersuchung eines Sicherheitsereignisses dokumentiert, versucht, die Ursache des Ereignisses zu identifizieren, und zeichnet alle Korrekturaktionen und gewonnenen Erkenntnisse auf. Korrekturmaßnahmen und gelernte Erkenntnisse werden verwendet, um Die Sicherheitsverfahren zu verbessern und die Wiederholung des Ereignisses zu verringern. Wenn sich ein Vorfall auf Microsoft-Ressourcen oder -Dienste auswirkt, verfügt das Sim-Team (Security Incident Management) über detaillierte Verfahren, um zu reagieren.

Zusätzlich zur 24 x 7-Sicherheit vor Ort nutzen Microsoft-Rechenzentren Alarmüberwachungssysteme, die Alarm- und Videoüberwachung in Echtzeit bereitstellen. Rechenzentrumstüren verfügen über Alarme, die über jede Öffnung berichten und nach einer programmierten Zeit geöffnet bleiben. Das Sicherheitssystem ist so programmiert, dass ein Livevideobild angezeigt wird, wenn ein Alarm ausgelöst wird. Zugriffskarten und biometrische Lesegeräte werden über das Alarmüberwachungssystem programmiert und überwacht. Alarme werden vom Control Room Supervisor überwacht und auf 24 x 7 geantwortet, der Kameras im Bereich des vorfalls verwendet, der untersucht wird, um dem Antwortenden Echtzeitinformationen zu liefern.
