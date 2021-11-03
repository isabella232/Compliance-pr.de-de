---
title: Führungslinie zur Risikobewertung für Microsoft Cloud
description: Erfahren Sie mehr über den Leitfaden zur Risikobewertung für Microsoft Cloud
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: df4b98f90c70bab3bd7f09e6312833d8a7ea768b
ms.sourcegitcommit: 85b36ce8c79fb111980cc6462f2addb44a924065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2021
ms.locfileid: "60678432"
---
# <a name="risk-assessment-guide-for-microsoft-cloud"></a>Führungslinie zur Risikobewertung für Microsoft Cloud

Das Ziel einer Cloudrisikobewertung besteht darin, sicherzustellen, dass das System und die daten, die für die Migration in die Cloud berücksichtigt werden, kein neues oder nicht identifiziertes Risiko in die Organisation einführen. Der Schwerpunkt liegt auf der Gewährleistung der Vertraulichkeit, Integrität, Verfügbarkeit und Destität der Informationsverarbeitung sowie darauf, identifizierte Risiken unterhalb des zulässigen internen Risikoschwellenwerts zu halten.

In einem Modell für gemeinsame Verantwortung ist der Clouddienstanbieter (Cloud Service Provider, CSP) für die Verwaltung der Sicherheit und Compliance *der Cloud* als Anbieter verantwortlich. Der Kunde bleibt für die Verwaltung und Konfiguration von Sicherheit und Compliance *in der Cloud* gemäß ihren Anforderungen und risikotoleranz verantwortlich.

![Modell für gemeinsame Verantwortung.](../media/assurance-shared-responsibility-model.png)

In diesem Leitfaden werden bewährte Methoden zur effizienten Bewertung von Lieferantenrisiken und zur Verwendung der von Microsoft zur Verfügung gestellten Ressourcen und Tools vorgestellt.

## <a name="understand-shared-responsibility-in-the-cloud"></a>Verstehen der gemeinsamen Verantwortung in der Cloud

Cloudbereitstellungen können als Infrastructure as a Service (IaaS), Platform as a Service (PaaS) oder Software as a Service (SaaS) kategorisiert werden. Je nach dem zutreffenden Clouddienstmodell wechselt die Verantwortung für die Sicherheitskontrollen der Lösungen zwischen dem CSP und dem Kunden. Bei einem herkömmlichen lokalen Modell ist der Kunde für den gesamten Stapel verantwortlich. Wenn Sie in die Cloud wechseln, werden alle physischen Sicherheitsaufgaben an den CSP übertragen. Abhängig vom Clouddienstmodell für Ihre Organisation wechseln zusätzliche Zuständigkeiten zum CSP. In den meisten Dienstmodellen bleibt Ihre Organisation jedoch für die Geräte verantwortlich, die für den Zugriff auf die Cloud, die Netzwerkkonnektivität, Ihre Konten und Identitäten und Ihre Daten verwendet werden. Microsoft investiert stark in die Erstellung von Diensten, mit denen Kunden während des gesamten Lebenszyklus die Kontrolle über ihre Daten behalten können.

Microsoft Cloud arbeitet auf einer Hyperskala und basiert auf einer Kombination aus DevSecOps und Automatisierung, um Betriebsmodelle zu standardisieren. Das Microsoft-Betriebssystem ändert die Art und Weise, wie Risiken im Vergleich zu herkömmlichen lokalen Betriebsmodellen entwickelt werden, was zur Implementierung verschiedener und manchmal unbekannter Kontrollen zur Verwaltung von Risiken führt. Bedenken Sie bei der Durchführung Ihrer Cloud-Risikobewertung, dass microsofts Ziel darin besteht, sicherzustellen, dass alle Risiken berücksichtigt werden, aber nicht unbedingt die gleichen Kontrollen implementiert werden, die Ihre Organisation durchführt. Microsoft kann die gleichen Risiken mit einer anderen Gruppe von Steuerelementen behandeln, die in der Cloudrisikobewertung berücksichtigt werden sollten. Durch das Entwerfen und Implementieren starker präventiver Kontrollen kann ein Großteil der Von den Erkennungs- und Korrekturkontrollen benötigten Arbeit reduziert werden. Ein Beispiel hierfür ist die Implementierung von [Zero Standing Access (ZSA)](assurance-microsoft-365-service-engineer-access-control.md)durch Microsoft.

## <a name="adopt-a-framework"></a>Einführen eines Frameworks

Microsoft empfiehlt Kunden, ihr internes Risiko- und Kontrollframework einem unabhängigen Framework zuzuordnen, das Cloudrisiken auf standardisierte Weise behandelt. Wenn Ihre vorhandenen modelle für die interne Risikobewertung die spezifischen Herausforderungen im Zusammenhang mit Cloud Computing nicht bewältigen, profitieren Sie von diesen allgemein verwendeten und standardisierten Frameworks. Ein sekundärer Vorteil besteht darin, dass Microsoft Zuordnungen zu diesen Frameworks in Dokumentationen und Tools bereitstellt, die Ihre Risikobewertung beschleunigen. Beispiele für diese Frameworks sind der [ISO 27001 Information Security Standard,](/compliance/regulatory/offering-iso-27001) [CIS Benchmark](/compliance/regulatory/offering-cis-benchmark)und [NIST SP 800-53.](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) Microsoft bietet die umfassendsten Complianceangebote aller CSP. Weitere Informationen finden Sie unter [Microsoft Compliance-Angebote.](/compliance/regulatory/offering-home)

Verwenden Sie [Microsoft Compliance Manager,](/microsoft-365/compliance/compliance-manager) um Ihre eigenen Bewertungen zu erstellen, die die Einhaltung der branchen- und regionalen Vorschriften bewerten, die für Ihre Organisation gelten. Bewertungen basieren auf dem Rahmen von Bewertungsvorlagen, die die erforderlichen Kontrollen, Verbesserungsmaßnahmen und gegebenenfalls Microsoft-Maßnahmen zum Abschließen der Bewertung enthalten. Für Microsoft-Aktionen werden detaillierte Implementierungspläne und aktuelle Überwachungsergebnisse bereitgestellt. Auf diese Weise kann Zeit für die Suche nach Fakten, die Zuordnung und die Suche nach der Implementierung bestimmter Steuerelemente durch Microsoft gespart werden. Weitere Informationen finden Sie im Microsoft Compliance Manager-Artikel.

## <a name="understand-how-microsoft-operates-to-safeguard-your-data"></a>Verstehen, wie Microsoft arbeitet, um Ihre Daten zu schützen

Während der Kunde für die Verwaltung und Konfiguration von Sicherheit und Compliance *in der Cloud* verantwortlich ist, ist der CSP für die Verwaltung der Sicherheit und Compliance der *Cloud* verantwortlich. Eine Möglichkeit, zu überprüfen, ob der CSP seine Zuständigkeiten effektiv erfüllt und seine Zusagen erfüllt, besteht darin, die externen Prüfberichte wie ISO und SOC zu überprüfen. Microsoft stellt externen Überwachungsberichten authentifizierten Benutzergruppen im [Service Trust Portal](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)zur Verfügung.

Zusätzlich zu externen Prüfberichten empfiehlt Microsoft Kunden dringend, die folgenden Ressourcen zu nutzen, um zu verstehen, wie Microsoft im Detail arbeitet:

- [On-Demand Learning Path:](/learn/roles/auditor)Die Lernplattform von Microsoft bietet Hunderte von Lernpfaden und Modulen zu verschiedenen Themen. Erfahren Sie unter anderem, [wie Microsoft Kundendaten schützt,](/learn/paths/audit-safeguard-customer-data/) um die grundlegenden Sicherheits- und Datenschutzpraktiken von Microsoft zu verstehen.

- [Service Assurance zu Microsoft Compliance:](/compliance/#service-assurance)Artikel zu Microsoft-Praktiken sind zur einfacheren Überprüfung in 16 Domänen unterteilt. Jede Domäne enthält eine Übersicht, in der erfasst wird, wie Microsoft die mit den einzelnen Bereichen verbundenen Risiken verwaltet. Überwachungstabellen werden mit Links zu den zuletzt im Service Trust Portal gespeicherten Berichten, verwandten Abschnitten und dem Datum, an dem der Überwachungsbericht für Microsoft-Onlinedienste durchgeführt wurde, bereitgestellt. Falls verfügbar, werden Links zu Artefakten bereitgestellt, die die Implementierung der Steuerung demonstrieren, z. B. Sicherheitsrisikobewertungen von Drittanbietern und Überprüfungsberichte des Geschäftskontinuitätsplans. Wie Überwachungsberichte werden diese Artefakte auf STP gehostet und erfordern eine Authentifizierung für den Zugriff.

| **Domäne** |**Beschreibung** |
|:---------- |:-------------- |
| [**Architektur**](assurance-architecture.md) | Das Design von Microsoft-Onlinediensten und die Sicherheitsprinzipien, die als Grundlage dienen. |
| [**Überwachungsprotokollierung**](assurance-audit-logging.md) | Wie Microsoft die Protokolle erfasst, verarbeitet, speichert und schützt, die eine Sicherheits- und Leistungsüberwachung ermöglichen. |
| [**Sicherheit von Rechenzentren**](assurance-datacenter-security.md) | Wie Microsoft die Rechenzentren sicher betreibt, die die Mittel zum weltweiten Betrieb von Microsoft-Onlinediensten bereitstellen. |
| [**Verschlüsselung und Schlüsselverwaltung**](assurance-encryption.md) | Der kryptografische Schutz der Kundenkommunikation und der in der Cloud gespeicherten und verarbeiteten Daten. |
| [**Governance**](assurance-governance.md) | Wie Microsoft Sicherheitsrichtlinien im gesamten Unternehmen erstellt, verteilt, aktualisiert und erzwingt, um kundenbezogene Zusagen und Complianceanforderungen zu erfüllen. |
| [**Personalwesen**](assurance-human-resources.md) | Die Überprüfungsprozesse und die sichere Verwaltung des Personals während ihrer gesamten Zeit bei Microsoft. |
| [**Identitäts- und Zugriffsverwaltung**](assurance-identity-and-access-management.md) | Der Schutz von Microsoft-Onlinediensten und Kundendaten vor unbefugtem oder böswilligem Zugriff. |
| [**Verwaltung von Sicherheitsvorfällen**](assurance-incident-management.md) | Die Von Microsoft verwendeten Prozesse zum Vorbereiten, Erkennen, Reagieren und Kommunizieren aller Sicherheits- und Datenschutzvorfälle. |
| [**Netzwerksicherheit**](assurance-network-security.md) | Wie Microsoft seine Netzwerkgrenzen vor externen Angriffen schützt und sein internes Netzwerk verwaltet, um deren Verbreitung zu begrenzen. |
| [**Datenschutz**](assurance-privacy.md) | Wie Microsoft Kundendaten behandelt und schützt, um ihre Datenrechte zu erhalten. |
| [**Ausfallsicherheit und Kontinuität**](assurance-resiliency-and-continuity.md) | Prozesse und Technologien, die verwendet werden, um die Dienstverfügbarkeit aufrechtzuerhalten und die Geschäftskontinuität und -wiederherstellung sicherzustellen. |
| [**Risikomanagement**](assurance-risk-management.md) | Identifizierung, Bewertung und Maßnahmen zur Minimierung des Risikos im gesamten Unternehmen. |
| [**Entwicklung und Verfahren im Sicherheitsbereich**](assurance-security-development-and-operation.md) | Wie Microsoft sicherstellt, dass seine Dienste während des gesamten Lebenszyklus sicher entworfen, ausgeführt und verwaltet werden. |
| [**Überwachung der Sicherheit**](assurance-security-monitoring.md) | Die zentrale Analyse von Protokollen, um Mitarbeiter von nicht autorisierten oder bösartigen Aktivitäten zu erkennen und darauf hinzuweisen. |
| [**Lieferantenmanagement**](assurance-supplier-management.md) | Wie Microsoft Drittanbieter, die Microsoft-Onlinedienste unterstützen, überprüft und verwaltet. |
| [**Bedrohungs- und Sicherheitsrisikomanagement**](assurance-vulnerability-management.md) | Die Prozesse, die Microsoft zum Suchen, Erkennen und Beheben von Sicherheitsrisiken und Schadsoftware verwendet. |

## <a name="resources"></a>Ressourcen

- [Leitfaden zur Risikobewertung und Compliance für Finanzinstitute in der Microsoft Cloud](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Risiko der Konzentration: Perspektiven von Microsoft](https://azure.microsoft.com/mediahandler/files/resourcefiles/concentration-risk-perspectives-from-microsoft-/Concentration_Risk_Perspectives_092020.pdf)
- [Vertrauensstellungsportal (STP)](https://servicetrust.microsoft.com/)
