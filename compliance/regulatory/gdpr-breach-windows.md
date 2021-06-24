---
title: Benachrichtigung des Datenauftragsverarbeiterdiensts für Windows Enterprise gemäß DSGVO
description: Wie der Datenauftragsverarbeiterdienst für Windows Enterprise Schutz vor Datenschutzverletzungen für persönliche Daten bietet und wie Microsoft reagiert und Sie benachrichtigt, wenn eine Datenschutzverletzung auftritt.
keywords: Datenauftragsverarbeiterdienst für Windows Enterprise, Microsoft 365, Microsoft 365-Dokumentation, DSGVO
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmaz
manager: laurawi
ms.reviewer: delinat
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
ms.openlocfilehash: 1fbbdb16fd1231d6044ed556090823cd36f90c78
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088864"
---
# <a name="data-processor-service-for-windows-enterprise-breach-notification-under-the-gdpr"></a>Benachrichtigung des Datenauftragsverarbeiterdiensts für Windows Enterprise über eine Datenschutzverletzung gemäß DSGVO

>[!NOTE]
>Dieser Artikel richtet sich an Teilnehmer am Vorschauprogramm „Datenauftragsverarbeiterdienst für Windows Enterprise“ und setzt die Zustimmung zu bestimmten Nutzungsbedingungen voraus. Wenn Sie mehr über das Programm erfahren und den Nutzungsbedingungen zustimmen möchten, wechseln Sie zu [https://aka.ms/WindowsEnterprisePublicPreview](https://aka.ms/WindowsEnterprisePublicPreview).

Der Microsoft-Datenauftragsverarbeiterdienst für Windows Enterprise nimmt seine Verpflichtungen gemäß der Datenschutz-Grundverordnung (DSGVO) ernst. Der Microsoft-Datenauftragsverarbeiterdienst für Windows Enterprise ergreift umfangreiche Sicherheitsmaßnahmen zum Schutz vor Datenschutzverletzungen. Diese umfassen dedizierte Threat Management-Teams, die in der Lage sind, böswillige Zugriffe proaktiv vorherzusehen, zu verhindern und abzuschwächen.Interne Sicherheitsmaßnahmen, z. B. Portüberwachung, Prüfung des Perimeters auf Sicherheitslücken und Erkennung von Eindringversuchen, erkennen und verhindern böswilligen Zugriff als auch automatisierte Sicherheitsprozesse, umfassende Informationen zu Sicherheits- und Datenschutzrichtlinien sowie Sicherheits- und Datenschutzschulungen für alle Mitarbeiter.

Sicherheit ist in den Microsoft-Datenauftragsverarbeiterdienst für Windows Enterprise von Grund auf integriert, beginnend mit dem [Security Development Lifecycle](https://www.microsoft.com/sdl/), einem obligatorischen Entwicklungsprozess, der Methoden für entwurfsgemäßen und standardmäßigen Datenschutz umfasst. Das Leitprinzip der Sicherheitsstrategie von Microsoft besteht darin, vom „Vorhandensein einer Datenschutzverletzung auszugehen“, und stellt somit eine Erweiterung der Strategie für tiefgreifende, vorbeugende Sicherheit dar. Indem die Sicherheitsfunktionen des Datenauftragsverarbeiterdiensts für Windows Enterprise ständig getestet werden, kann Microsoft neuen Bedrohungen immer einen Schritt voraus bleiben. Weitere Informationen zur Sicherheit des Datenauftragsverarbeiterdiensts für Windows Enterprise finden Sie in [diesen Ressourcen](https://www.microsoft.com/TrustCenter/Security/windows10-security). Der Datenauftragsverarbeiterdienst für Windows Enterprise reagiert auf eine potenzielle Datenschutzverletzung gemäß dem Prozess für die Reaktion auf Sicherheitsvorfälle. Die Reaktion des Datenauftragsverarbeiterdiensts für Windows Enterprise auf einen Sicherheitsvorfall ist in Form eines fünfstufigen Prozesses implementiert: Erkennen, Bewerten, Diagnostizieren, Stabilisieren und Schließen. Im Verlauf der Untersuchung kann das Reaktionsteam für Sicherheitsvorfälle zwischen den Stufen der Diagnose und Stabilisierung wechseln. Eine Übersicht des Prozesses für die Reaktion auf Sicherheitsvorfälle finden Sie im Folgenden:

|**Stage**|**Beschreibung**|
|:------- |:------------- |
| **_1: Erkennung_* _ | Erste Anzeichen für einen potenziellen Vorfall. |
| _*_2: Analyse_*_ | Ein abrufbereites Mitglied des Teams für die Reaktion auf Sicherheitsvorfälle analysiert die Auswirkungen und den Schweregrad des Ereignisses. Basierend auf den Nachweisen kann die Analyse zu einer Eskalation an das Sicherheitsteam führen. |
| _*_3: Diagnose_*_ | Sicherheitsexperten führen eine technische oder forensische Untersuchung durch und ermitteln Strategien für Eindämmung, Risikominderung und Abhilfe. Wenn das Sicherheitsteam der Meinung ist, dass möglicherweise Kundendaten gegenüber einer unbefugten Personen offengelegt wurden, wird parallel der Prozess zur Benachrichtigung des Kunden über den Sicherheitsvorfall in Gang gesetzt. |
| _*_4: Stabilisierung und Wiederherstellung_*_ | Das Team für die Reaktion auf Sicherheitsvorfälle erstellt einen Wiederherstellungsplan, um das Problem zu mindern. Schritte zur Eindämmung der Auswirkungen, wie die Isolierung der betroffenen Systeme, können sofort und parallel zur Diagnose ausgeführt werden. Zudem können längerfristige Maßnahmen zur Risikominderung geplant werden, die umgesetzt werden, sobald die unmittelbare Gefahr gebannt ist. |
| _*_5: Abschluss und nachträgliche Analyse_*_ | Das Team für die Reaktion auf Sicherheitsvorfälle erstellt eine nachträgliche Analyse mit den Details des Vorfalls, anhand derer Richtlinien, Verfahren und Prozesse geprüft werden sollen, um ein erneutes Auftreten des Ereignisses zu verhindern. |

Die Erkennungsprozesse, die der Datenauftragsverarbeiterdienst von Microsoft für Windows Enterprise verwendet, sind darauf ausgelegt, Ereignisse zu erkennen, die die Vertraulichkeit, Integrität und Verfügbarkeit des Datenauftragsverarbeiterdiensts für Windows Enterprise gefährden. Verschiedene Ereignisse können eine Untersuchung auslösen:

- Automatisierte Systembenachrichtigungen über interne Überwachungs- und Warnungs-Frameworks. Diese Warnungen können in Form von signaturbasierten Alarmen eingehen wie Malwareschutz oder Eindringungserkennung oder über Algorithmen, die bei Anomalien ein Profil der erwarteten Aktivität oder Warnung erstellen.
- Erstanbieterberichte von Microsoft-Diensten, die unter Microsoft Azure und Azure Government ausgeführt werden.
- Sicherheitslücken werden dem [Microsoft Security Response Center (MSRC)](https://technet.microsoft.com/security/dn440717) über [secure@microsoft.com] (mailto:secure@microsoft.com) gemeldet. MSRC arbeitet mit Partnern und Sicherheitsforschern auf der ganzen Welt, um Sicherheitsvorfälle zu verhindern und die Sicherheit von Microsoft-Produkten zu erhöhen.
- Kundenberichte über das Kundenportal oder das Management Portal von Microsoft Azure und Azure Government, die der Azure-Infrastruktur zugeordnete verdächtige Aktivitäten beschreiben (im Gegensatz zu Aktivitäten, die in den Verantwortungsbereich des Kunden fallen).
- Aktivitäten der [roten und blauen Sicherheitsteams](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/). Bei dieser Strategie wird ein hoch qualifiziertes rotes Team aus offensiven Sicherheitsexperten von Microsoft eingesetzt, um potenzielle Schwächen in Azure aufzudecken und anzugreifen. Das blaue Sicherheitsteam muss die Aktivitäten des roten Teams erkennen und abwehren. Die Aktionen des roten wie auch des blauen Teams werden dazu verwendet, um zu überprüfen, ob die Sicherheitsmaßnahmen von Azure Sicherheitsvorfälle effektiv bewältigen. Die Aktivitäten des roten und blauen Sicherheitsteams müssen Regeln des Engagements einhalten, um den Schutz von Kundendaten zu gewährleisten.
- Eskalationen von Operatoren der Azure-Dienste. Microsoft-Mitarbeiter sind dahingehend geschult, potenzielle Sicherheitsprobleme zu identifizieren und zu eskalieren.

## <a name="data-processor-service-for-windows-enterprise-data-breach-response"></a>Reaktion des Datenauftragsverarbeiterdiensts für Windows Enterprise auf eine Datenschutzverletzung

 Microsoft weist der Untersuchung die entsprechende Priorität und den Schweregrad zu, indem es die funktionalen Auswirkungen, die Wiederherstellbarkeit und die Informationsauswirkungen des Vorfalls bestimmt. Sowohl die Priorität als auch der Schweregrad können sich im Laufe der Untersuchung ändern, basierend auf neuen Erkenntnissen und Schlussfolgerungen. Sicherheitsereignisse, die eine unmittelbare oder bestätigte Gefahr für die Kundendaten darstellen, werden mit einem hohen Schweregrad behandelt und es wird rund um die Uhr an einer Lösung gearbeitet. Der Microsoft Datenverarbeitungsdienst für Windows Enterprise kategorisiert die Informationsauswirkungen des Vorfalls in die folgenden Verletzungskategorien:

| _ *Kategorie** | **Definition** |
|:------------ |:-------------- |
| **_Keine_* _ | Es wurden keine Daten entfernt, geändert, gelöscht oder anderweitig kompromittiert. |
| _*_Datenschutzverletzung_*_ | Es wurde auf vertrauliche personenbezogene Daten von Steuerzahlern, Mitarbeitern, Begünstigten etc. zugegriffen oder diese wurden entfernt. |
| _*_Verletzung des Schutzes unternehmenseigener Daten_*_ | Es wurde auf nicht klassifizierte, unternehmenseigene Daten, z. B. geschützte kritische Infrastrukturdaten (Protected Critical Infrastructure Information, PCII), zugegriffen oder diese wurden entfernt. |
| _*_Integritätsverlust_*_ | Vertrauliche oder unternehmenseigene Daten wurden geändert oder gelöscht. |

Das Sicherheitsreaktionsteam arbeitet mit Sicherheitsingenieuren und Sicherheitsexperten (Subject Matter Experts, SMEs) des Datenverarbeitungsdienstes von Microsoft für Windows Enterprise zusammen, um das Ereignis basierend auf Fakten aus den gewonnenen Erkenntnissen zu klassifizieren. Ein Sicherheitsereignis kann klassifiziert werden als:

- _*Falsch positives Ereignis**: Ein Ereignis, das die Erkennungskriterien erfüllt, aber Teil der normalen Geschäftsabläufe ist und möglicherweise gefiltert werden muss. Das Serviceteam identifiziert die Ursache für falsch positive Ereignisse und behandelt sie auf systematische Weise unter Verwendung von Erkennungsquellen und bedarfsgerechter Optimierung.
- **Sicherheitsvorfall:** Ein Vorfall, bei dem ein unrechtmäßiger Zugriff auf Kundendaten oder Supportdaten, die auf Geräten oder in Einrichtungen von Microsoft gespeichert sind, bzw. ein nicht autorisierter Zugriff auf diese Geräte oder Einrichtungen erfolgt ist, der zu Verlust, Offenlegung oder Änderung von Kundendaten oder Supportdaten geführt hat.
- **Meldepflichtiger Sicherheitsvorfall (Customer-Reportable Security Incident, CRSI)**: Unrechtmäßiger oder nicht autorisierter Zugriff auf Systeme, Geräte oder Anlagen von Microsoft bzw. deren Verwendung, der bzw. die zu Offenlegung, Änderung oder Verlust von Kundendaten geführt hat.
- **Datenschutzverletzung**: Ein Untertyp von Sicherheitsvorfällen im Zusammenhang mit persönlichen Daten. Die Verfahren gleichen denen bei Sicherheitsvorfällen.

 Damit ein CRSI erklärt werden kann, muss Microsoft bestimmen, dass ein nicht autorisierter Zugriff auf Kundendaten erfolgt ist oder wahrscheinlich erfolgt ist und/oder dass eine rechtliche oder vertragliche Meldepflicht besteht. Es ist wünschenswert, aber nicht erforderlich, dass bestimmte Kundenauswirkungen, Ressourcenzugriff und Schritte zur Behebung bekannt sind. Ein Vorfall wird im Allgemeinen nach Abschluss der Diagnosestufe eines Sicherheitsvorfalls zu einem CRSI erklärt. Die Erklärung kann aber zu einem beliebigen Zeitpunkt erfolgen, wenn alle relevanten Informationen zur Verfügung stehen. Der Manager des Sicherheitsvorfalls muss zweifelsfrei nachweisen, dass ein meldepflichtiges Ereignis aufgetreten ist, um mit der Ausführung des Prozesses zur Benachrichtigung des Kunden über den Sicherheitsvorfall zu beginnen.

Während der Untersuchung arbeitet das Sicherheitsteam eng mit globalen Rechtsberatern zusammen, um sicherzustellen, dass die Forensik entsprechend den gesetzlichen Verpflichtungen und Pflichten gegenüber dem Kunden ausgeführt wird. Es gibt zudem erhebliche Beschränkungen für das Anzeigen und Behandeln von System- und Kundendaten in verschiedenen Betriebsumgebungen. Sensible oder vertrauliche Daten und Kundendaten werden ohne explizite schriftliche Genehmigung des Vorfall-Managers, die im entsprechenden Vorfallsticket aufgezeichnet wird, nicht aus der Produktionsumgebung heraus übertragen.

Microsoft überprüft, ob das Risiko für Kunden und Unternehmen erfolgreich gebannt wurde und ob Abhilfemaßnahmen implementiert wurden. Bei Bedarf werden Notfallverfahren zum Beheben unmittelbarer Sicherheitsrisiken im Zusammenhang mit dem Ereignis ausgeführt.

Microsoft nimmt auch eine interne nachträgliche Analyse zu Datenschutzverletzungen vor. Im Rahmen dieser Übung wird die Angemessenheit von Reaktions- und Betriebsverfahren bewertet und es werden etwaige notwendige Updates an dem SOP für die Reaktion auf Sicherheitsvorfälle oder zugehörigen Prozessen identifiziert und implementiert. Interne nachträgliche Analysen zu Datenschutzverletzungen sind streng vertrauliche Datensätze, auf die Kunden keinen Zugriff haben. Diese Analysen können allerdings in zusammengefasster Form in andere Kundenbenachrichtigungen zu Ereignissen aufgenommen werden. Die Analysen werden im Rahmen des routinemäßigen Auditzyklus von Windows Enterprise durch externe Auditoren geprüft.

## <a name="customer-notice"></a>Kundenbenachrichtigung

Der Microsoft-Datenverarbeitungsdienst für Windows Enterprise benachrichtigt Kunden und Aufsichtsbehörden bei Bedarf über Datenverletzungen. Microsoft verlässt sich beim Betrieb des Datenverarbeitungsdienstes für Windows Enterprise auf eine starke interne Abschottung. Die Datenflussprotokolle sind ebenfalls robust. Ein Vorteil dieses Designs ist, dass die meisten Vorfälle auf bestimmte Kunden eingegrenzt werden können. Ziel ist es, den betroffenen Kunden eine genaue, umsetzbare und rechtzeitige Benachrichtigung zukommen zu lassen, wenn ihre Daten verletzt worden sind.

Der Benachrichtigungsprozess bei einem deklarierten CRSI wird so rasch wie möglich in Gang gesetzt, wobei auch die Sicherheitsrisiken eines schnellen Handelns berücksichtigt werden. Im Allgemeinen wird der Prozess des Benachrichtigungsentwurfs durchgeführt, während der Vorfall untersucht wird. Kundenbenachrichtigungen werden ab dem Zeitpunkt, an dem wir einen Verstoß deklarieren, innerhalb von 72 Stunden übermittelt, mit Ausnahme  der folgenden Situationen:

- Microsoft ist der Meinung, dass eine Benachrichtigung das Risiko für andere Kunden erhöht. Beispielsweise wenn durch die Benachrichtigung der Übeltäter gewarnt und der Schaden daraufhin nicht mehr behoben werden kann.
- Andere ungewöhnliche oder extreme Umstände, die von der Rechtsabteilung Corporate External and Legal Affairs (CELA) und dem leitenden Vorfall-Manager von Microsoft überprüft werden.

 Der Microsoft-Datenauftragsverarbeiterdienst für Windows Enterprise bietet Kunden ausführliche Informationen, sodass sie interne Untersuchungen ausführen können und die Erfüllung von Verpflichtungen gegenüber Endbenutzern erleichtert wird, ohne den Benachrichtigungsprozess übermäßig zu verzögern.

Die Benachrichtigung zu einer Verletzung des Schutzes personenbezogener Daten wird dem Kunden auf einem von Microsoft gewählten Weg übermittelt, möglicherweise auch per E-Mail. Die Benachrichtigung über eine Datenschutzverletzung wird der Liste der Sicherheitskontakte bereitgestellt, die im Azure Security Center hinterlegt ist und die mithilfe der [Implementierungsrichtlinien](/azure/security-center/security-center-provide-security-contact-details) konfiguriert werden kann. Wenn keine Kontaktinformationen im Azure Security Center bereitgestellt werden, erfolgt die Benachrichtigung an einen oder mehrere Administratoren in einem Azure-Abonnement. Um sicherzustellen, dass die Benachrichtigung erfolgreich zugestellt werden kann, muss der Kunde dafür sorgen, dass die administrativen Kontaktinformationen in dem jeweiligen Abonnement und Onlinedienst-Portal korrekt sind.

Das Team des Datenverarbeitungsdienstes für Windows Enterprise kann sich auch dafür entscheiden, zusätzliches Microsoft-Personal zu benachrichtigen, z. B. den Kundendienst (CSS) und den/die Account Manager (AM) oder den/die Technical Account Manager (TAM) des Kunden. Diese Personen haben oft enge Beziehungen zum Kunden und können eine schnellere Behebung ermöglichen.

Weitere Informationen darüber, wie Microsoft eine Verletzung des Schutzes personenbezogener Daten erkennt und darauf reagiert, finden Sie im Service Trust Portal unter [Benachrichtigung bei Datenschutzverletzungen im Rahmen der DSGVO](https://servicetrust.microsoft.com/ViewPage/GDPRBreach).
