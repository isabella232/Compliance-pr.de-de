---
title: Benchmarks des Center for Internet Security (CIS)
description: Das Center for Internet Security (CIS) hat eine Reihe von Benchmarks für Microsoft-Produkte und -Dienste veröffentlicht.
keywords: Microsoft 365, Compliance, Angebote
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
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 18da1f6b422327f42dc517fa0f9c8abe9c91e253
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159777"
---
# <a name="center-for-internet-security-cis-benchmarks"></a>Benchmarks des Center for Internet Security (CIS)

## <a name="about-cis-benchmarks"></a>Informationen zu CIS-Benchmarks

Das [Center for Internet Security](https://www.cisecurity.org/) ist eine gemeinnützige Organisation, die es sich zum Ziel gesetzt hat, „Bewährte Lösungsmethoden zum Schutz vor Cyberbedrohungen zu identifizieren, zu entwickeln, zu bewerten, zu fördern und zu unterstützen“. Die Organisation macht sich dabei das Know-how zum Thema Internetsicherheit und das Wissen von IT-Experten aus Regierung, Unternehmen und Akademien auf der ganzen Welt zu Nutze. Zur Entwicklung von Standards und bewährten Methoden, einschließlich CIS-Benchmarks, Steuerungen und gehärteten Images, wird ein konsensbasiertes Entscheidungsmodell befolgt.  
  
[CIS-Benchmarks](https://www.cisecurity.org/cis-benchmarks/) sind Basispläne für Konfiguration und bewährte Methoden zur sicheren Konfiguration eines Systems. Jede Empfehlung verweist auf eine oder mehrere [CIS-Steuerungen](https://www.cisecurity.org/controls/), die entwickelt wurden, um Organisationen bei der Verbesserung ihrer Verteidigung gegen Cyberangriffe zu unterstützen. Die CIS-Steuerungen entsprechen zahlreichen etablierten Normen und aufsichtsrechtlichen Rahmenbedingungen, einschließlich des NIST Cybersecurity Framework (CSF) und des NIST-SP 800-53, der ISO 27000-Reihe von Standards, PCI DSS, HIPAA und weiteren.  
  
Jeder Benchmark unterliegt zwei Phasen der konsensbasierten Überprüfung. Die erste Phase erfolgt während der anfänglichen Entwicklung, wenn sich Experten treffen, um Arbeitsentwürfe zu besprechen, zu erstellen und zu testen, bis sie eine Einigung über den Benchmark erzielen. In der zweiten Phase, nach der Veröffentlichung des Benchmarks, überprüft das Team das Feedback der Internetcommunity im Hinblick auf die Einbindung in den Benchmark.  
  
CIS-Benchmarks bieten zwei Ebenen von Sicherheitseinstellungen:

- **Ebene 1** empfiehlt grundlegende Sicherheitsanforderungen, die in jedem System konfiguriert werden können und zu geringen oder gar keinen Dienstunterbrechungen oder eingeschränkter Funktionalität führen sollten.
- **Ebene 2** empfiehlt Sicherheitseinstellungen für Umgebungen, die mehr Sicherheit erfordern, was zu einer verringerten Funktionalität führen kann.

[Gehärtete CIS-Images](https://www.cisecurity.org/blog/cis-hardened-images-now-in-microsoft-azure-marketplace/) sind sicher konfigurierte Images von virtuellen Maschinen basierend auf CIS-Benchmarks, die auf einem CIS-Benchmarkprofil der Ebene 1 oder Ebene 2 gehärtet wurden. Das „Härten“ ist ein Prozess, der Schutz vor unbefugtem Zugriff, Denial-of-Service-Angriffen und anderen Cyberbedrohungen bietet, indem potenzielle Schwachstellen eingeschränkt werden, die für Cyberattacken anfällig sind.

## <a name="microsoft-and-the-cis-benchmarks"></a>Microsoft und die CIS-Benchmarks

Das Center for Internet Security (CIS) veröffentlicht Benchmarks für Microsoft-Produkte und -Dienste, einschließlich der Foundation-Benchmarks für Microsoft Azure und Microsoft 365, des Benchmarks für Windows 10 und des Benchmarks für Windows Server 2016. Der [CIS Microsoft Azure Foundation Benchmark](https://www.cisecurity.org/benchmark/azure/) richtet sich an Kunden, die Lösungen, die Azure integrieren, entwickeln, bereitstellen, bewerten oder sichern möchten. Das Dokument enthält verbindliche Anweisungen für die Einrichtung einer sicheren Basislinienkonfiguration für Azure.
  
CIS-Benchmarks werden international als Sicherheitsstandards für den Schutz von IT-Systemen und Daten vor Cyberangriffen anerkannt. Sie werden von Tausenden von Unternehmen verwendet und bieten verbindliche Anweisungen für die Einrichtung einer sicheren Basislinienkonfiguration. System- und Anwendungsadministratoren, Sicherheitsexperten und andere Personen, die Lösungen mithilfe von Microsoft-Produkten und -Diensten entwickeln, können diese bewährten Methoden verwenden, um die Sicherheit ihrer Anwendungen zu bewerten und zu verbessern.  
  
Wie alle CIS-Benchmarks wurden auch die Microsoft-Benchmarks anhand eines konsensbasierten Überprüfungsprozesses basierend auf den Beiträgen von Sachverständigen mit unterschiedlichen Hintergründen im Hinblick auf Softwareentwicklung, Überwachung und Compliance, Sicherheitsforschung, Arbeitsabläufe, Behörden und Rechtsvorschriften entwickelt. Bei diesen CIS-Bemühungen war Microsoft ein unentbehrlicher Partner. Office 365 wurde beispielsweise anhand der aufgeführten Dienste getestet, und die daraus resultierenden Benchmarks für Microsoft 365 decken ein breites Spektrum von Empfehlungen zum Einrichten geeigneter Sicherheitsrichtlinien ab, die sich auf Konten und Authentifizierung, Datenverwaltung, Anwendungsberechtigungen, Speicher und andere Bereiche von Sicherheitsrichtlinien beziehen.  
  
Zusätzlich zu den Benchmarks für Microsoft-Produkte und -Dienste hat CIS [gehärtete CIS-Images in Azure](https://www.cisecurity.org/cis-hardened-images/microsoft/) veröffentlicht, die so konfiguriert sind, dass sie CIS-Benchmarks erfüllen und im Microsoft Azure Marketplace verfügbar sind. Zu diesen Images gehören die gehärteten CIS-Images für Windows Server 2016 und Windows Server 2019 sowie verschiedene Versionen von Linux. Alle gehärtete CIS-Images, die im Azure Marketplace verfügbar sind, sind für die Ausführung auf Microsoft Azure zertifiziert. Wie von [CIS erwähnt](https://www.cisecurity.org/blog/cis-hardened-images-now-in-microsoft-azure-marketplace/), „wurden sie vorab auf Bereitschaft und Kompatibilität mit der öffentlichen Microsoft Azure-Cloud, der Microsoft-Cloudplattform, die von Dienstanbietern über das Netzwerk des Cloudbetriebssystems gehostet wird, und den Windows Server Hyper-V-Bereitstellungen in der lokalen privaten Cloud getestet, die von Kunden verwaltet werden“.

[Gehärtete CIS-Images](https://www.cisecurity.org/cis-hardened-images/) sind sicher konfigurierte Images von virtuellen Computern basierend auf CIS-Benchmarks, die auf einem CIS-Benchmarkprofil der Ebene 1 oder Ebene 2 gehärtet wurden. Das „Härten“ ist ein Prozess, der Schutz vor unbefugtem Zugriff, Denial-of-Service-Angriffen und anderen Cyberbedrohungen bietet, indem potenzielle Schwachstellen eingeschränkt werden, die für Cyberattacken anfällig sind. Gehärtete CIS-Images sind sowohl in Azure als auch in Azure Government verfügbar.

Für zusätzliche Kundenunterstützung stellt Microsoft [Azure Blueprints](https://azure.microsoft.com/services/blueprints/)bereit. Dies ist ein Dienst, der Ihnen hilft, Cloudumgebungen auf wiederholbare Weise bereitzustellen und zu aktualisieren, indem sie zusammensetzbare Artefakte wie Azure Resource Manager-Vorlagen zum Bereitstellen von Ressourcen, rollenbasierten Zugriffssteuerungen und Richtlinien verwendet. Ressourcen, die über Azure Blueprints bereitgestellt werden, entsprechen den Standards, Mustern und Complianceanforderungen einer Organisation. Das übergeordnete Ziel von Azure Blueprints ist die Automatisierung der Compliance und des Cybersicherheitsrisikomanagements in Cloudumgebungen. Um Ihnen bei der Bereitstellung eines zentralen Satzes von Richtlinien für jede Azure-basierte Architektur, die CIS Azure Foundations-Benchmarkempfehlungen implementieren muss, zu helfen, hat Microsoft den [Azure Blueprint für den CIS Microsoft Azure Foundation Benchmark](/azure/governance/blueprints/samples/cis-azure-1-3-0) veröffentlicht. Wenn sie einer Architektur zugewiesen sind, werden Ressourcen von Azure Policy auf ihre Kompatibilität mit zugewiesenen Richtliniendefinitionen ausgewertet.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>In Microsoft eingeschlossene Cloudplattformen und -Dienste

- [Azure und Azure Government](https://aka.ms/AzureCompliance)
- [Office und Microsoft 365](https://aka.ms/o365-compliance-framework)
- SQL Server
- Windows 10
- Windows Server 2016

## <a name="audits-reports-and-certificates"></a>Prüfungen, Berichte und Zertifikate

Rufen Sie eine [vollständige Liste von CIS-Benchmarks](https://www.cisecurity.org/cis-benchmarks/) für Microsoft-Produkte und -Dienste ab.

- [CIS Azure Foundations Benchmark](https://www.cisecurity.org/benchmark/azure/)
- [CIS Microsoft 365 Foundations Benchmark](https://www.cisecurity.org/benchmark/microsoft_office/)
- [Windows 10 Benchmark](https://www.cisecurity.org/benchmark/microsoft_windows_desktop/)
- [Windows Server 2016 Benchmark](https://www.cisecurity.org/benchmark/microsoft_windows_server/)

## <a name="how-to-implement"></a>Implementierung

- [CIS-Benchmark für Azure](https://azure.microsoft.com/mediahandler/files/resourcefiles/cis-microsoft-azure-foundations-security-benchmark/CIS_Microsoft_Azure_Foundations_Benchmark_v1.0.0.pdf): Hier erhalten Sie verbindliche Anweisungen für die Einrichtung einer sicheren Basislinienkonfiguration für Azure.  
- [Inhaltsübersicht für die Sicherheit von Microsoft 365](/microsoft-365/security/office-365-security/security-roadmap): Minimieren Sie das Risiko einer Datenschutzverletzung oder eines kompromittierten Kontos, indem Sie diese Roadmap befolgen.
- [Windows-Sicherheitsbasispläne](/windows/security/threat-protection/windows-security-baselines): Befolgen Sie diese Richtlinien, um Sicherheitsbasislinien in Ihrer Organisation effektiv zu nutzen.
- [CIS Controls Cloud Companion Guide](https://www.cisecurity.org/white-papers/cis-controls-cloud-companion-guide/): Hier finden Sie Anweisungen zum Anwenden bewährter Sicherheitsmethoden in CIS-Steuerungen, Version 7, auf Cloudanwendungen.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Wird durch eine Einhaltung der CIS-Benchmarkeinstellungen die Sicherheit meiner Anwendungen gewährleistet?**

CIS-Benchmarks legen das grundlegende Maß an Sicherheit für alle Personen fest, die Microsoft-Produkte und -Dienste einführen. Diese Benchmarks sollten jedoch nicht als umfassende Liste aller möglichen Sicherheitskonfigurationen und -architekturen, sondern eher als Ausgangspunkt betrachtet werden. Jede Organisation muss weiterhin ihre spezifische Situation, Arbeitslast und Complianceanforderungen auswerten und ihre Umgebung entsprechend anpassen.

**Wie oft werden CIS-Benchmarks aktualisiert?**

Die Veröffentlichung überprüfter CSI-Benchmarks ändert sich in Abhängigkeit von der Community von IT-Experten, die den Benchmark entwickelt haben, und in Abhängigkeit vom Veröffentlichungsplan der Technologie, die der Benchmark unterstützt. CIS veröffentlicht monatliche Berichte, in denen neue Benchmarks und Aktualisierungen an vorhandenen Benchmarks angekündigt werden. Um diese zu erhalten, registrieren Sie sich für die [CIS Workbench](https://workbench.cisecurity.org/) (kostenlos), und aktivieren Sie die entsprechende Option in Ihrem Profil, um den Newsletter zu erhalten.

**Wer hat zur Entwicklung von Microsoft-CIS-Benchmarks beigetragen?**

CIS betont, dass seine „Benchmarks mithilfe der großzügigen Freiwilligenarbeit von Sachverständigen, Technologieanbietern, öffentlichen und privaten Mitgliedern der CIS-Community sowie des CIS-Benchmark-Entwicklungsteams entwickelt werden“. Unter [CIS Microsoft Azure Foundations Benchmark v1.0.0 Now Available](https://www.cisecurity.org/blog/cis-microsoft-azure-foundations-benchmark-v1-0-0-now-available/) finden Sie beispielsweise eine Liste der Personen, die an Azure mitgewirkt haben.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Verwenden von Microsoft Compliance-Manager zur Einschätzung des Risikos

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) ist eine Funktion im [Microsoft 365 Compliance Center](/microsoft-365/compliance/microsoft-365-compliance-center), die Ihnen hilft, die Compliance-Position Ihres Unternehmens zu verstehen und Maßnahmen zu ergreifen, um Risiken zu reduzieren. Compliance Manager bietet eine Premiumvorlage für die Erstellung einer Bewertung für diese Verordnung. Suchen Sie die Vorlage auf der Seite **Bewertungsvorlagen** im Compliance Manager. Erfahren Sie, wie Sie [Bewertungen im Compliance-Manager erstellen](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Ressourcen

- [Azure Compliance-Dokumentation](/azure/compliance/)
- [Azure ermöglicht eine Welt der Compliance](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [Microsoft 365 Compliance-Angebote](/compliance/regulatory/offering-home)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
- Der [CIS Microsoft Azure Foundation Benchmark](https://www.cisecurity.org/benchmark/azure/) bietet eine Schritt-für-Schritt-Checkliste zum Sichern von Azure.
- [Gehärtete CIS-Images auf Microsoft Azure](https://www.cisecurity.org/cis-hardened-images/microsoft/) sind Azure-zertifiziert und gemäß den Sicherheitsempfehlungen der CIS-Benchmarks vorkonfiguriert.  Sie sind sowohl in Azure als auch in Azure Government verfügbar.
- Der [Azure Blueprint für CIS Microsoft Azure Foundation Benchmark](/azure/governance/blueprints/samples/cis-azure-1-3-0) hilft Kunden bei der Bereitstellung eines zentralen Richtliniensatzes für alle Azure-basierten Architekturen, die CIS Azure Foundation Benchmarkempfehlungen implementieren müssen.
- Die [Zuordnung von Azure-Richtlinienempfehlungen](/azure/governance/policy/samples/cis-azure-1-3-0) enthält Details zu Richtliniendefinitionen, die im obigen Blueprint enthalten sind und dazu, wie diese Richtliniendefinitionen den Compliancedomänen und -kontrollen in CIS Microsoft Azure Foundation Benchmark zugeordnet sind. Wenn sie einer Architektur zugewiesen sind, werden Ressourcen von Azure Policy auf ihre Nichtkonformität mit den zugewiesenen Richtliniendefinitionen ausgewertet.
- Im [CIS Controls Cloud Companion Guide](https://www.cisecurity.org/white-papers/cis-controls-cloud-companion-guide/) finden Sie Anweisungen zum Anwenden bewährter Sicherheitsmethoden in CIS-Steuerungen, Version 7, auf Cloudanwendungen.
- Der [CIS Microsoft 365 Foundation Benchmark](https://www.cisecurity.org/benchmark/microsoft_office/) bietet eine verbindliche Anleitung zum Einrichten einer sicheren Basiskonfiguration für Microsoft 365.
- [Sicherheitsrichtlinieneinstellungen in Windows 10](/windows/security/threat-protection/security-policy-settings/security-policy-settings)
- [Sicherheit in Windows 10 Enterprise](/windows/security/index)
