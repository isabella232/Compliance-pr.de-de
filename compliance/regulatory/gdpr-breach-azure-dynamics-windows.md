---
title: Azure-, Dynamics 365- und Windows-Benachrichtigungen zu Sicherheitsverletzungen gemäß der DSGVO
description: Hier erfahren Sie, wie Azure und Dynamics 365 Sie vor Verletzungen des Schutzes personenbezogener Daten schützen und wie Microsoft reagiert und Sie benachrichtigt, wenn eine Verletzung auftritt.
keywords: Azure, Microsoft 365, Dynamics 365, Microsoft 365-Dokumentation, DSGVO
ms.localizationpriority: high
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: 23d6b1ebb30f34fcb549e3e1f44c98a0c0e11b12
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58479807"
---
# <a name="azure-dynamics-365-and-windows-breach-notification-under-the-gdpr"></a>Azure-, Dynamics 365- und Windows-Benachrichtigungen zu Sicherheitsverletzungen gemäß der DSGVO

Microsoft nimmt seine Pflichten im Rahmen der Datenschutz-Grundverordnung (DSGVO) sehr ernst. Microsoft ergreift umfassende Sicherheitsmaßnahmen innerhalb seiner Onlinedienste, um vor Datenschutzverletzungen zu schützen. Diese Maßnahmen umfassen sowohl physische und logische Sicherheitskontrollen als auch automatisierte Sicherheitsprozesse, umfassende Richtlinien zur Informationssicherheit und zum Datenschutz sowie Schulungen zur Sicherheit und zum Datenschutz für Mitarbeiter.

Sicherheit ist in Microsoft Azure von Grund auf integriert, beginnend mit dem [Security Development Lifecycle](https://www.microsoft.com/sdl/), einem obligatorischen Entwicklungsprozess, der benutzerdefinierte und standardmäßige Datenschutz-Methodologien umfasst. Das Leitprinzip der Sicherheitsstrategie von Microsoft besteht darin, vom Vorhandensein einer Datenschutzverletzung auszugehen, und stellt somit eine Erweiterung der Strategie für tiefgreifende, vorbeugende Sicherheit dar. Indem die Sicherheitsfunktionen von Azure ständig getestet werden, kann Microsoft neuen Bedrohungen immer einen Schritt voraus bleiben. Weitere Informationen zur Sicherheit bei Azure finden Sie in diesen [Ressourcen](https://www.microsoft.com/trustcenter/security/azure-security).

Microsoft verfügt über einen dedizierten globalen, rund um die Uhr aktiven Service für die Reaktion auf Vorfälle, der daran arbeitet, die Auswirkungen von Angriffen gegen Microsoft Azure zu mindern. Microsoft nutzt in seinen Rechenzentren strenge Abläufe und Prozesse zur Verhinderung von nicht autorisiertem Zugriff, darunter 24-Stunden-Videoüberwachung, geschultes Sicherheitspersonal, Smartcards und biometrische Kontrollen. Dies wird durch mehrere Sicherheits- und Compliance-Audits bestätigt (z. B. [ISO/IEC 27018](offering-iso-27018.md)).

## <a name="detection-of-potential-breaches"></a>Erkennung potenzieller Sicherheitsverletzungen

Aufgrund der Beschaffenheit des modernen Cloud-Computing beziehen sich nicht alle Datenschutzverletzungen, die in einer Cloudumgebung des Kunden auftreten, auf Dienste von Microsoft Azure. Microsoft verwendet ein Modell der gemeinsamen Verantwortung für Azure-Dienste, in dem Verantwortlichkeiten für Sicherheit und Betrieb definiert sind. Gemeinsame Verantwortung ist besonders dann wichtig, wenn es um die Sicherheit von Clouddiensten geht, da sowohl der Anbieter des Clouddiensts als auch die Kunden jeweils für Teile der Cloudsicherheit zuständig sind.

Microsoft ist nicht verantwortlich für die Überwachung oder Reaktion auf Sicherheitsvorfälle, die auf Seiten des Kunden auftreten. Ein Sicherheitsproblem, das nur den Kunden betrifft, wird nicht als Azure-Sicherheitsvorfall verarbeitet, sondern muss vom Mandanten des Kunden behandelt werden. Die Reaktion des Kunden auf Sicherheitsvorfälle kann eine Zusammenarbeit mit dem [Kundensupport](https://azure.microsoft.com/support/options/) von Microsoft Azure umfassen, sofern entsprechende Serviceverträge bestehen. Microsoft Azure bietet auch verschiedene Dienste an (z. B. [Azure Security Center](https://azure.microsoft.com/services/security-center/)), die Kunden zur Entwicklung und Verwaltung einer Reaktion auf Sicherheitsvorfälle verwenden können.

Azure reagiert auf eine potenzielle Datenschutzverletzung entsprechend dem Prozess für die Reaktion auf Sicherheitsvorfälle, der Teil des Vorfallmanagementplans von Microsoft Azure ist. Die Reaktion auf Sicherheitsvorfälle seitens Microsoft Azure erfolgt in fünf Stufen: Erkennung, Analyse, Diagnose, Stabilisierung und Abschluss. Das Team für die Reaktion auf Sicherheitsvorfälle kann im Verlauf der Untersuchung zwischen den Stufen der Diagnose und der Stabilisierung wechseln. Nachfolgend finden Sie eine Übersicht über die Vorgehensweise bei Sicherheitsvorfällen:

| Stufe | Beschreibung |
|:------- |------------- |
| ***1: Erkennung*** | Erste Anzeichen für einen potenziellen Vorfall. |
| ***2: Analyse*** | Ein abrufbereites Mitglied des Teams für die Reaktion auf Sicherheitsvorfälle analysiert die Auswirkungen und den Schweregrad des Ereignisses. Basierend auf den Nachweisen kann die Analyse zu einer Eskalation an das Sicherheitsteam führen. |
| ***3: Diagnose*** | Sicherheitsexperten führen eine technische oder forensische Untersuchung durch und ermitteln Strategien für Eindämmung, Risikominderung und Abhilfe. Wenn das Sicherheitsteam der Meinung ist, dass möglicherweise Kundendaten gegenüber einer unbefugten Personen offengelegt wurden, wird parallel der Prozess zur Benachrichtigung des Kunden über den Sicherheitsvorfall in Gang gesetzt. |
| ***4: Stabilisierung und Wiederherstellung*** | Das Team für die Reaktion auf Sicherheitsvorfälle erstellt einen Wiederherstellungsplan, um das Problem zu mindern. Schritte zur Eindämmung der Auswirkungen, wie die Isolierung der betroffenen Systeme, können sofort und parallel zur Diagnose ausgeführt werden. Zudem können längerfristige Maßnahmen zur Risikominderung geplant werden, die umgesetzt werden, sobald die unmittelbare Gefahr gebannt ist. |
| ***5: Abschluss und nachträgliche Analyse*** | Das Team für die Reaktion auf Sicherheitsvorfälle erstellt eine nachträgliche Analyse, die den Vorfall detailliert untersucht, mit dem Ziel, die vorhandenen Richtlinien und Prozesse zu überarbeiten, um ein erneutes Auftreten des Ereignisses zu verhindern. |

Die Erkennungsprozesse von Microsoft Azure sind darauf ausgelegt, Ereignisse zu erkennen, welche die Vertraulichkeit, Integrität und Verfügbarkeit von Azure-Diensten gefährden. Verschiedene Ereignisse können eine Untersuchung auslösen:

- Automatisierte Systembenachrichtigungen über interne Überwachungs- und Warnungs-Frameworks. Diese Warnungen können in Form von signaturbasierten Alarmen eingehen wie Malwareschutz oder Eindringungserkennung oder über Algorithmen, die bei Anomalien ein Profil der erwarteten Aktivität oder Warnung erstellen.
- Erstanbieterberichte von Microsoft-Diensten, die unter Microsoft Azure und Azure Government ausgeführt werden.
- Sicherheitsrisiken werden dem [Microsoft Security Response Center (MSRC)](https://www.microsoft.com/msrc) über [Vorfall melden](https://msrc.microsoft.com/create-report) gemeldet. MSRC arbeitet mit Partnern und Sicherheitsforschern auf der ganzen Welt, um Sicherheitsvorfälle zu verhindern und die Sicherheit von Microsoft-Produkten zu erhöhen.
- Kundenberichte über das [Kundenportal](https://www.windowsazure.com/support/contact/) oder das Management Portal von Microsoft Azure und Azure Government, die der Azure-Infrastruktur zugeordnete verdächtige Aktivitäten beschreiben (im Gegensatz zu Aktivitäten, die in den Verantwortungsbereich des Kunden fallen).
- Aktivitäten der [roten und blauen Sicherheitsteams](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/). Bei dieser Strategie wird ein hoch qualifiziertes rotes Team aus offensiven Sicherheitsexperten von Microsoft eingesetzt, um potenzielle Schwächen in Azure aufzudecken und anzugreifen. Das blaue Sicherheitsteam muss die Aktivitäten des roten Teams erkennen und abwehren. Die Aktionen des roten wie auch des blauen Teams werden dazu verwendet, um zu überprüfen, ob die Sicherheitsmaßnahmen von Azure Sicherheitsvorfälle effektiv bewältigen. Die Aktivitäten des roten und blauen Sicherheitsteams müssen Regeln des Engagements einhalten, um den Schutz von Kundendaten zu gewährleisten.
- Eskalationen von Betreibern der Azure-Dienste. Microsoft-Mitarbeiter sind dahingehend geschult, potenzielle Sicherheitsprobleme zu identifizieren und zu eskalieren.

## <a name="azures-data-breach-response"></a>Reaktion auf Datenschutzverletzungen in Azure

Microsoft weist der Untersuchung angemessene Prioritäts- und Schweregrade zu, indem die funktionellen Auswirkungen, die Wiederherstellbarkeit und die Beeinträchtigung von Daten durch den Vorfall bestimmt werden. Priorität und Schweregrad können sich im Laufe der Untersuchung basierend auf neuen Erkenntnissen und Schlussfolgerungen ändern. Sicherheitsereignisse im Zusammenhang mit bevorstehenden oder bestätigten Risiken für Kundendaten werden als hoher Schweregrad behandelt und rund um die Uhr bearbeitet, um Lösungen zu finden.

Das Sicherheitsteam arbeitet mit Sicherheitstechnikern und Sicherheitsexperten (Subject Matter Experts, SMEs) von Microsoft Azure zusammen, um das Ereignis basierend auf Fakten aus den gewonnenen Erkenntnissen zu klassifizieren. Ein Sicherheitsereignis kann wie folgt klassifiziert werden:

- **Falsch positives Ergebnis**: Ein Ereignis, das die Erkennungskriterien erfüllt, aber Teil der normalen Geschäftsabläufe ist und möglicherweise herausgefiltert werden muss. Serviceteams identifizieren die Ursache für falsch positive Ereignisse und behandeln sie auf systematische Weise, um sie bei Bedarf zu optimieren.
- **Sicherheitsereignis**: Ein beobachtbares Vorkommen in einem System, Dienst und/oder Netzwerk für versuchten Angriff, Umgehung von Sicherheitskontrollen oder ein identifiziertes Problem, bei dem die Fakten darauf hindeuten, dass Kundendaten oder personenbezogene Daten möglicherweise verloren gegangen sind, zerstört, geändert, offengelegt oder ohne Autorisierung auf sie zugegriffen wurde.
- **Sicherheitsvorfall/Vom Kunden meldepflichtiger Sicherheits-/Datenschutzvorfall (Customer Reportable Security/Privacy Incident, CRSPI)**: Eine bestätigte (z. B. deklarierte) Sicherheitsverletzung, die zu versehentlicher oder unrechtmäßiger Zerstörung, Verlust, Änderung, unbefugter Offenlegung oder Zugriff auf Kundendaten oder personenbezogene Daten bei der Verarbeitung durch Microsoft führt.
- **Datenschutzereignis**: Ein Sicherheitsereignis, das sich auf personenbezogene Daten oder die Datenverarbeitung auswirkt und unbeabsichtigte Folgen für den Datenschutz hat, einschließlich der Nichtkonformität mit Microsoft-Datenschutzrichtlinien, -Standards und -Kontrollen.
- **Datenschutzvorfall/Vom Kunden meldepflichtiger Sicherheits-/Datenschutzvorfall (Customer Reportable Security/Privacy Incident, CRSPI)**: Ein Sicherheitsvorfall, der sich auf personenbezogene Daten, Daten oder die Datenverarbeitung auswirkt, die unbeabsichtigte Folgen für den Datenschutz haben, einschließlich der Nichtkonformität mit Microsoft-Datenschutzrichtlinien, -Standards und -Kontrollen.

Damit ein CRSPI deklariert werden kann, muss Microsoft feststellen, dass wahrscheinlich ein nicht autorisierter Zugriff auf Kundendaten stattgefunden hat und/oder dass eine gesetzliche oder vertragliche Verpflichtung zur Benachrichtigung besteht. Es ist wünschenswert, aber nicht zwingend erforderlich, dass die spezifische Auswirkung auf den Kunden, der Ressourcenzugriff und die Reparaturschritte bekannt sind.Ein Vorfall wird im Allgemeinen nach Abschluss der Diagnosestufe eines Sicherheitsvorfalls als CRSPI deklariert. Allerdings kann dies auch zu jedem beliebigen anderen Zeitpunkt stattfinden, an dem alle relevanten Informationen verfügbar sind.

Microsoft überprüft, ob das Risiko für Kunden und Unternehmen erfolgreich gebannt wurde und ob Abhilfemaßnahmen implementiert wurden. Bei Bedarf werden Notfallverfahren zum Beheben unmittelbarer Sicherheitsrisiken im Zusammenhang mit dem Ereignis ausgeführt.

Microsoft nimmt auch eine interne nachträgliche Analyse zu Datenschutzverletzungen vor. Im Rahmen dieser Übung wird die Angemessenheit von Reaktions- und Betriebsverfahren bewertet, und es werden etwaige notwendige Updates an dem SOP für die Reaktion auf Sicherheitsvorfälle oder zugehörigen Prozessen identifiziert und implementiert. Interne nachträgliche Analysen zu Datenschutzverletzungen sind streng vertrauliche Datensätze, die Kunden nicht zur Verfügung stehen. Diese Analysen können allerdings in zusammengefasster Form in andere Kundenbenachrichtigungen zu Ereignissen aufgenommen werden. Die Analysen werden im Rahmen des routinemäßigen Auditzyklus von Azure durch externe Auditoren geprüft.

## <a name="customer-notification"></a>Kundenbenachrichtigung

Microsoft benachrichtigt Kunden und Aufsichtsbehörden vorgabengerecht über Datenschutzverletzungen. Microsoft baut auf eine starke interne Trennung des Betriebs von Azure. Datenflussprotokolle sind ebenfalls robust. Ein Vorteil dieses Designs ist, dass die meisten Vorfälle bestimmten Kunden zugeordnet werden können. Das Ziel ist, den betroffenen Kunden präzise, umsetzbare und zeitgerechte Informationen bereitzustellen, wenn der Schutz ihrer Daten verletzt wurde.

Der Benachrichtigungsprozess nach einem deklarierten CRSPI wird so rasch wie möglich in Gang gesetzt, wobei auch die Sicherheitsrisiken eines schnellen Handelns berücksichtigt werden. Im Allgemeinen erfolgt der Prozess des Benachrichtigungsentwurfs, während der Vorfall untersucht wird. Ab dem Zeitpunkt, an dem wir eine Datenschutzverletzung deklarieren, vergehen nicht mehr als 72 Stunden, bis wir unsere Kunden informieren, *außer* in den folgenden Situationen:

- Microsoft ist der Meinung, dass eine Benachrichtigung das Risiko für andere Kunden erhöht. Beispielsweise kann die Benachrichtigung einem Angreifer einen Hinweis darauf geben, dass er nicht in der Lage ist, Abhilfe zu schaffen.
- Andere ungewöhnliche oder extreme Umstände, die von der Rechtsabteilung und dem leitenden Vorfall-Manager von Microsoft überprüft werden.
- Im Verlauf des 72-Stunden-Zeitlimits ergeben sich möglicherweise neue Erkenntnisse zum Vorfall. Diese Details werden Kunden und Aufsichtsbehörden bereitgestellt, sobald die Untersuchung fortschreitet.

Microsoft stellt betroffenen Kunden detaillierte Informationen bereit, sodass sie interne Untersuchungen ausführen können ihre Verpflichtungen gegenüber Endbenutzern erfüllen können, ohne den Benachrichtigungsprozess übermäßig zu verzögern.

Die Benachrichtigung zu einer Verletzung des Schutzes personenbezogener Daten wird dem betroffenen Kunden auf einem von Microsoft gewählten Weg übermittelt, möglicherweise auch per E-Mail. Die Benachrichtigung über eine Datenschutzverletzung wird der Liste der Sicherheitskontakte bereitgestellt, die im Azure Security Center hinterlegt ist und die mithilfe der [Implementierungsrichtlinien](/azure/security-center/security-center-provide-security-contact-details) konfiguriert werden kann. Wenn keine Kontaktinformationen im Azure Security Center bereitgestellt werden, erfolgt die Benachrichtigung an einen oder mehrere Administratoren in einem Azure-Abonnement. Um sicherzustellen, dass die Benachrichtigung erfolgreich zugestellt werden kann, muss der Kunde dafür sorgen, dass die administrativen Kontaktinformationen in dem jeweiligen Abonnement und Onlinedienst-Portal korrekt sind.

Das Team von Microsoft Azure oder Azure Government kann auch entscheiden, weiteres Microsoft-Personal zu benachrichtigen, z. B. Mitglieder des Microsoft-Kundendienst (Customer Support Service, CSS)-Teams und den/die Kundenbetreuer (Account Manager, AM) oder technischen Kundenbetreuer (Technical Account Manager, TAM) des Kunden. Diese Personen haben häufig enge Beziehungen zum Kunden und können eine schnellere Problembehebung erzielen.

## <a name="microsoft-dynamics-365-built-in-security-features"></a>Microsoft Dynamics 365 – Integrierte Sicherheitsfeatures

Microsoft Dynamics 365 nutzt die Cloud-Service-Infrastruktur und integrierten Sicherheitsfeatures, um Daten mithilfe von Sicherheitsmaßnahmen und -mechanismen zu schützen. Darüber hinaus bietet Dynamics 365 effizienten Datenzugriff und Zusammenarbeit plus Datenintegrität und Datenschutz in den folgenden Bereichen: [Sichere Identität, Datenschutz, rollenbasierte Sicherheit und Bedrohungsmanagement](https://www.microsoft.com/trustcenter/security/dynamics365-security).

Das Microsoft Dynamics 365-Angebot befolgt dieselben technischen und organisatorischen Maßnahmen, die ein oder mehrere Microsoft Azure-Dienstteams zur Sicherung gegen Datenverletzungsprozesse ergreifen. Daher sind alle Informationen, die im Benachrichtigungsdokument "Microsoft Azure-Datenverletzung" dokumentiert sind, analog zu Microsoft Dynamics 365.

## <a name="windows-diagnostic-data-processor-configuration"></a>Konfiguration für Windows-Diagnosedatenverarbeitung

Die [Konfiguration für die Windows-Diagnosedatenverarbeitung](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) nutzt die Clouddienst-Infrastruktur und die integrierten Sicherheitsfeatures, um Daten mithilfe von Sicherheitsmaßnahmen und Mechanismen zum Schutz von Daten zu schützen.

Es befolgt dieselben technischen und organisatorischen Maßnahmen, die ein oder mehrere Microsoft Azure-Dienstteams zur Sicherung gegen Datenleckprozesse ergreifen. Daher entsprechen alle Informationen, die hier im Benachrichtigungsdokument „Microsoft Azure-Datenleck“ dokumentiert sind, auch der Konfiguration für die Windows-Diagnosedatenverarbeitung.

## <a name="learn-more"></a>Weitere Informationen

[Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
