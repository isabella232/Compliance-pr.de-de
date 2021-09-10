---
title: Sichern der Microsoft 365 Infrastruktur
description: Erfahren Sie, wie Microsoft die Microsoft 365-Infrastruktur sichert.
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
ms.openlocfilehash: 6c20c62feb1ff3ab23eeb97d5ad11abb5ad85a07
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947159"
---
# <a name="securing-the-microsoft-365-infrastructure"></a>Sichern der Microsoft 365 Infrastruktur

Microsoft 365 ist einer der größten Clouddienste für Unternehmen und Verbraucher weltweit und wächst weiterhin schnell, sowohl in der Kundenbasis als auch bei Produkten und Features. Kunden nutzen Microsoft 365 nicht nur für erstklassige Produktivitätslösungen, sondern auch, um ihre vertraulichsten Informationen vor der sich ständig weiterentwickelnden Cyberbedrohungslandschaft zu schützen. Es ist microsofts oberste Priorität, Kundendaten zu schützen und das Kundenvertrauen aufrechtzuerhalten.

Das Sichern eines Systems dieses Umfangs und dieser Komplexität ist nicht möglich, wenn die Sicherheit eine Nachfolgelösung ist, sie ist nur wirksam, wenn die Sicherheit während des anfänglichen Entwurfsprozesses integriert wird. Es erfordert ein robustes Bedrohungserkennungssystem mit prompten Antworten sowohl von automatisierten Systemen als auch von hoch qualifizierten Technikern. Die kontinuierliche Bewertung und Validierung dieser Systeme ist unerlässlich, um sicherzustellen, dass sichere Konfigurationen erhalten bleiben und zuvor unbekannte Sicherheitsrisiken identifiziert werden.

## <a name="core-security-principles"></a>Kernsicherheitsprinzipien

Sieben Sicherheitsprinzipien bilden die Grundlage für unseren Rahmen des *Schutzes* der Microsoft 365-Dienste vor Bedrohungen, *der Erkennung und Reaktion auf* Bedrohungen sowie der *kontinuierlichen Bewertung* des Sicherheitsstatus und der Verbesserung der Dienste basierend auf den Ergebnissen dieser Bewertungen.

- **Datenschutz:** Kunden besitzen ihre Daten, und Microsoft ist der Verwahrer. Microsoft 365 Dienste sind so konzipiert, dass sie ohne Techniker funktionieren, die auf Kundendaten zugreifen, es sei denn, der Kunde hat dies ausdrücklich angefordert und genehmigt.
- **Gehen Sie von einem Verstoß aus:** Personal und Dienste werden so behandelt, als wäre eine Kompromittierung eine echte Möglichkeit.
- **Geringste Rechte:** Der Zugriff und die Berechtigungen für Ressourcen sind auf das beschränkt, was zum Ausführen der erforderlichen Aufgaben erforderlich ist.
- **Grenzen von Sicherheitsverletzungen:** Identitäten und Infrastruktur in einer Grenze sind von Ressourcen in anderen Grenzen isoliert. Eine Gefährdung einer Grenze sollte nicht zu einer Gefährdung einer anderen führen.
- Integrierte Sicherheit in **Service Fabric:** Sicherheitsprioritäten und -anforderungen sind in den Entwurf neuer Features und Funktionen integriert, um sicherzustellen, dass ein starker Sicherheitsstatus bei jedem Dienst skaliert wird.
- **Automatisiert und automatisch:** Microsoft konzentriert sich auf die Entwicklung dauerhafter Produkte und Architekturen, die die Dienstsicherheit intelligent und automatisch erzwingen können, während Microsoft-Technikern die Möglichkeit gegeben wird, Antworten auf Sicherheitsbedrohungen im großen Maßstab sicher zu verwalten.
- **Adaptive Sicherheit:** Die Sicherheitsfunktionen von Microsoft passen sich an Machine Learning-Modelle, routinebezogene Penetrationstests und automatisierte Bewertungen an und werden durch diese verbessert.

## <a name="protection"></a>Schutz

### <a name="access-control"></a>Zugriffssteuerung

Standardmäßig verfügen Mitarbeiter, die für die Entwicklung und Wartung Microsoft 365 Dienste verantwortlich sind, über Zero Standing Access (ZSA) für die Dienstinfrastruktur. Microsoft ist zwar bestrebt, nur die besten Techniker zu beauftragen, und strenge Hintergrundüberprüfungen sind erforderlich, Microsoft geht jedoch nicht davon aus, dass sie standardmäßig in Betriebsdiensten als vertrauenswürdig eingestuft werden. Wenn Techniker für den privilegierten Zugriff genehmigt werden, wird ihnen außerdem nur für eine begrenzte Dauer Der Zugriff gewährt, um nur die für einen bestimmten Bereich der Dienstinfrastruktur erforderlichen Aktionen auszuführen. Microsoft bezeichnet diese Richtlinien als Just-in-Time (JIT) und Just-Enough-Access (JEA), die über ein System namens Lockbox implementiert werden.

Um erhöhte Rechte zu erhalten, senden Microsoft-Techniker eine Anforderung für die spezifische Aufgabe und geben den Zeitrahmen für die Ausführung an. Nach der Genehmigung generiert Lockbox ein spezielles JIT-Konto mit der Möglichkeit, nur die angeforderte Aufgabe auszuführen. Aktionen werden in der Regel in Form von automatisierten Workflows ausgeführt, mit denen alle erforderlichen Problembehandlungs- oder Wiederherstellungsvorgänge sicher ausgeführt werden. In seltenen Fällen, in denen direkter Zugriff auf die Infrastruktur erforderlich ist, sind streng überwachte Privileged Access Workstations (PAWs) erforderlich.

Nicht autorisierte Benutzer und kompromittierte Konten sind in jeder Organisation eine echte Möglichkeit, und unser Zugriffssteuerungssystem ist darauf ausgelegt, sich vor diesen Bedrohungen zu schützen.

Weitere Informationen zur Zugriffssteuerung finden Sie unter [Identity and Access Management Overview](assurance-identity-and-access-management.md).

### <a name="encryption"></a>Verschlüsselung

Während Zugriffssteuerungen eine wichtige Rolle bei der Verteidigung Microsoft 365 Dienste spielen, wird die Verschlüsselung während des gesamten Datenlebenszyklus verwendet, um die Vertraulichkeit und den Datenschutz für Microsoft-Kunden weiter zu schützen.

Daten, die zwischen Clientcomputern, Microsoft 365 servern und Servern ohne Microsoft 365 übertragen werden, werden mit TLS 1.2 verschlüsselt. Wir überprüfen regelmäßig die verwendeten Verschlüsselungen und Protokolle, fügen ggf. verbesserte Protokolle hinzu und entfernen bei Bedarf schwächere Protokolle.

Kundeninhalte, die sich auf Microsoft-Servern befinden, werden auf Volumeebene mit BitLocker verschlüsselt. Die Verschlüsselung auf Anwendungsebene kann zusätzlich mithilfe von Schlüsseln angewendet werden, die von Microsoft oder dem Kunden verwaltet werden. Der Zugriff auf von Microsoft verwaltete Schlüssel ist nur möglich, wenn sie über den JIT- und JEA-Prozess autorisiert und genehmigt werden.

Weitere Informationen zur Verschlüsselung in Microsoft 365 finden Sie unter [Verschlüsselung und Schlüsselverwaltung](assurance-encryption.md)( Übersicht).

### <a name="network-isolation"></a>Netzwerkisolation

Gemäß dem Prinzip der geringsten Rechte schränkt Microsoft 365 die Kommunikation zwischen verschiedenen Teilen der Dienstinfrastruktur auf das für den Betrieb erforderliche Maß ein. Der gesamte Netzwerkdatenverkehr wird standardmäßig verweigert, wobei nur explizit definierte Kommunikation zulässig ist. Diese Einschränkung legt Grenzen für Sicherheitsverletzungen in der gesamten Infrastruktur fest. Teams, die neue Netzwerkpfade hinzufügen möchten, um ihrem Dienst ein neues Feature hinzuzufügen, muss die Anforderung ausgewertet und genehmigt werden, bevor sie geöffnet werden kann.

Weitere Informationen zur Netzwerkisolation in Microsoft 365 finden Sie unter [Microsoft 365 Isolationssteuerelemente.](/microsoft-365/enterprise/microsoft-365-isolation-controls)

## <a name="detection--response"></a>Erkennung & Antwort

### <a name="security-monitoring"></a>Überwachung der Sicherheit

Sicherheitsüberwachung im großen Umfang von Microsoft ist nur möglich, indem hochgenaue Warnungen mithilfe automatisierter cloudbasierter Lösungen generiert werden. Überwachungsprotokolle von den einzelnen Diensten und Telemetriedaten, die aus der gesamten Kerninfrastruktur gesammelt werden, werden an eine proprietäre zentrale Verarbeitungs- und Benachrichtigungslösung in Nahezu-Echtzeit gesendet.

Erkannte Bedrohungen werden nach Möglichkeit mithilfe automatisch ausgelöster Aktionen behoben. Wenn automatisierte Lösungen nicht erfolgreich sind oder nicht in der Lage sind, das Problem zu beheben, ergreifen Microsoft-Techniker sofort maßnahmen, um die Bedrohung zu mindern.

Weitere Informationen zur Sicherheitsüberwachung in Microsoft 365 finden Sie unter ["Übersicht über die Sicherheitsüberwachung".](assurance-security-monitoring.md)

## <a name="assessment"></a>Bewertung

### <a name="automated-assessments"></a>Automatisierte Bewertungen

Unabhängig davon, wie ein System konzipiert ist, kann sich der Sicherheitsstatus aufgrund einer absichtlichen und unbeabsichtigten Konfigurationsverschiebung im Laufe der Zeit beeinträchtigen. Automatisierte Tools bewerten ständig Microsoft 365 Systeme, die nach nicht gepatchten und falsch konfigurierten Diensten suchen. Diese Bewertung wird häufig als Patching, Virenschutz, Sicherheitsrisiko und Konfigurationsüberprüfung (PATCHC) bezeichnet.

Unsere Architektur wird auch häufig überprüft und identifiziert Instanzen wie nicht verwendete offene Ports und Konten mit ständigem Administratorzugriff. Alle Dienste, die von einem vordefinierten gewünschten Zustand abweichen, werden automatisch wieder in die Ausrichtung zurückgesetzt.

Weitere Informationen zur Sicherheitsüberwachung in Microsoft 365 finden Sie unter [Übersicht über die Sicherheitsrisikoverwaltung.](assurance-vulnerability-management.md)

### <a name="attack-simulation-and-penetration-testing"></a>Angriffssimulation und Penetrationstests

Microsoft 365 hat oberste Priorität, um zu verhindern, dass Angriffe die Abwehr infiltrieren. Microsoft 365 verfügt über ein dediziertes Team von Sicherheitsexperten, die ständig simulierte Angriffe durchführen, um zuvor unbekannte Sicherheitsrisiken zu identifizieren und einen konstanten Datenstrom zur Verbesserung der Sicherheitsüberwachungsfunktionen bereitzustellen. Diese simulierten Angriffe haben die Form häufiger automatisierter Angriffe in kleinem Maßstab und von Experten gesteuerter Deep Dives. Anhand dieser Aktivitäten bewertet Microsoft die Fähigkeit, Angreifer zu erkennen, darauf zu reagieren und sie zu entfernen.

Weitere Informationen zur Sicherheitsüberwachung in Microsoft 365 finden Sie unter [Angriffssimulation in Microsoft 365.](assurance-monitoring-and-testing.md)

## <a name="resources"></a>Ressourcen

[Hinter den Kulissen: Sicherung der Infrastruktur beim Einbringen des Microsoft 365-Diensts](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
