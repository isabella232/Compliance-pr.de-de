---
title: Payment Card Industry (PCI) Data Security Standard (DSS)
description: Azure, SharePoint Online und OneDrive for Business erfüllen die Payment Card Industry Data Security Standards der Stufe 1, Version 3.2.
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
ms.openlocfilehash: 63303389fc8fae69b9a6803a513efeb1281f781e
ms.sourcegitcommit: 4afc3ca7f8c18ae7136b4c82c572531947e82daa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2021
ms.locfileid: "59349959"
---
# <a name="payment-card-industry-pci-data-security-standard-dss"></a>Payment Card Industry (PCI) Data Security Standard (DSS)

## <a name="pci-dss-overview"></a>PCI DSS – Überblick

Der Payment Card Industry (PCI) Data Security Standards (DSS) ist ein globaler Informationssicherheitsstandard, der Betrug durch verstärkte Kontrolle von Kreditkartendaten verhindern soll. Unternehmen aller Größen müssen die PCI DSS-Standards einhalten, wenn sie Zahlungskarten der fünf wichtigsten Kreditkartenmarken Visa, MasterCard, American Express, Discover und JCB (Japan Credit Bureau) akzeptieren. Compliance mit den PCI DSS-Standards ist für jedes Unternehmen erforderlich, das Daten von Zahlungen und Karteninhabern speichert, verarbeitet oder überträgt.

## <a name="microsoft-and-pci-dss"></a>Microsoft und PCI DSS

Microsoft hat eine jährliche PCI-DSS-Bewertung mit einem anerkannten Qualified Security Assessor (QSA) durchgeführt. Die Prüfer überprüften Microsoft Azure-, Microsoft OneDrive for Business- und Microsoft SharePoint Online-Umgebungen, in denen die Infrastruktur, die Entwicklung, der Betrieb, die Verwaltung, der Support und die In-Scope-Services überprüft wurden. Der PCI-DSS legt vier Compliance-Ebenen fest, die auf dem Transaktionsvolumen basieren. Azure, OneDrive for Business und SharePoint Online sind gemäß PCI DSS Version 3.2 auf Dienstanbieter-Ebene 1 als konform zertifiziert (das höchste Transaktionsvolumen von mehr als 6 Millionen pro Jahr).

Die Bewertung führt zu einer Attestation of Compliance (AoC), die den Kunden zur Verfügung steht, und einem vom QSA herausgegebenen Bericht über die Konformität (RoC). Die effektive Frist für die Einhaltung beginnt mit dem Bestehen des Audits und dem Erhalt der AoC vom Assessor und endet ein Jahr ab dem Datum der Unterzeichnung der AoC. 

Kunden, die eine Umgebung für Karteninhaber oder einen Kartenverarbeitungsdienst entwickeln möchten, können diese Zertifizierung in vielen der zugrunde liegenden Bereiche verwenden, wodurch sich der Aufwand und die Kosten für die Erlangung einer eigenen PCI-DSS-Zertifizierung verringern.

Es ist wichtig zu verstehen, dass der PCI-DSS-Kompatibilitätsstatus für Azure, OneDrive for Business und SharePoint Online nicht automatisch in eine PCI-DSS-Zertifizierung für die Dienste übersetzt wird, die Kunden auf diesen Plattformen erstellen oder hosten. Kunden sind dafür verantwortlich, dass sie die Compliance mit den PCI-DSS-Anforderungen erfüllen.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>In Microsoft eingeschlossene Cloudplattformen und -Dienste

- Azure und Azure Government
- Intune
- Microsoft Cloud App Security
- [Microsoft Defender für Endpunkt](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- Microsoft Graph
- Office 365
- OneDrive for Business und SharePoint Online (nur in den Vereinigten Staaten)
- PowerApps-Clouddienst als eigenständigen Dienst oder in einem firmenspezifischen Office 365- oder Dynamics 365-Plan bzw. -Anwendungssuite enthalten
- Power Automate (entweder als eigenständiger Dienst oder in einem Office 365- oder Dynamics 365-Plan bzw. einer -Anwendungssuite enthalten)
- Power BI-Clouddienst entweder als eigenständiger Dienst oder enthalten in einem Office 365-Plan oder -Suite

## <a name="azure-dynamics-365-and-pci-dss"></a>Azure, Dynamics 365 und PCI-DSS

Weitere Informationen zur Compliance mit Azure, Dynamics 365 und anderen Onlinediensten finden Sie im [Azure PCI-DSS-Angebot](/azure/compliance/offerings/offering-pci-dss).

## <a name="office-365-and-pci-dss"></a>Office 365 und PCI-DSS

### <a name="office-365-cloud-environments"></a>Office 365-Cloudumgebungen

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365-Anwendbarkeit und im Leistungsumfang enthaltene Dienste

Verwenden Sie die folgende Tabelle, um die Anwendbarkeit für Ihre Office 365-Dienste und -Abonnements zu bestimmen:

| **Anwendbarkeit** | **Im Leistungsumfang enthaltene Dienste** |
|:------------------|:----------------------|
| **Kommerziell** | OneDrive for Business (Vereinigte Staaten), SharePoint Online (Vereinigte Staaten) |

### <a name="office-365-audit-reports-and-certificates"></a>Office 365-Audit, -Berichte und -Zertifikate

- [OneDrive for Business und SharePoint Online PCI-DSS-Compliancenachweis (AoC)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=f1962237-32ea-4123-939e-1c8f04d13c16&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_PCI_DSS)

### <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Warum steht auf dem Deckblatt der Attestation of Compliance (AoC) „Juni 2018“?**

Das Datum Juni 2018 auf dem Deckblatt ist der Zeitpunkt, an dem die AoC-Vorlage veröffentlicht wurde. Das Datum der Bescheinigung können Sie dem Abschnitt 2 entnehmen. 

**Welche Beziehung besteht zwischen PA DSS und PCI DSS?**

Der Payment Application Data Security Standard (PA DSS) enthält eine Reihe von Anforderungen, die mit dem PCI DSS übereinstimmen. Er ersetzt die Best Practices von Visa für Zahlungsanwendungen und konsolidiert die Compliance-Anforderungen der anderen primären Kartenaussteller. Der PA DSS unterstützt Softwareanbieter bei der Entwicklung von Anwendungen von Drittanbietern, die im Rahmen eines Kartenautorisierungs- oder Abrechnungsprozesses Zahlungsdaten von Karteninhabern speichern, verarbeiten oder übertragen. Einzelhändler müssen nach PA DSS zertifizierte Anwendungen verwenden, um Compliance mit PCI DSS wirksam zu erreichen. Der PA DSS gilt nicht für Azure.

**Was ist ein Acquirer und setzt Azure einen solchen ein?**

Ein Acquirer ist eine Bank oder ein anderes Unternehmen, das Zahlungskartentransaktionen abwickelt. Azure bietet die Verarbeitung von Zahlungskarten nicht als Dienst an und setzt daher keinen Acquirer ein.

**Für welche Organisationen und Händler gilt der PCI DSS-Standard?**

PCI DSS gilt für jedes Unternehmen, unabhängig von der Größe oder Anzahl der Transaktionen, das Karteninhaberdaten akzeptiert, überträgt oder speichert. Das heißt, wenn ein Kunde jemals ein Unternehmen mit einer Kredit- oder Debitkarte bezahlt, gelten die PCI-DSS-Anforderungen. Unternehmen werden auf einer von vier Ebenen basierend auf dem Gesamttransaktionsvolumen über einen Zeitraum von 12 Monaten validiert. Level 1 ist für Unternehmen gedacht, die mehr als 6 Millionen Transaktionen pro Jahr abwickeln. Level 2 für 1 Million bis 6 Millionen Transaktionen; Level 3 gilt für 20.000 bis 1 Million Transaktionen und Level 4 für weniger als 20.000 Transaktionen.

**Gibt es Pläne, damit OneDrive for Business und SharePoint Online außerhalb der Vereinigten Staaten PCI DSS-konform sind?**

Derzeit ist OneDrive for Business und SharePoint Online nur in den Vereinigten Staaten PCI-DSS-kompatibel. Microsoft bewertet die Anforderungen und Zeitpläne für Regionen außerhalb der Vereinigten Staaten und stellt Updates bereit, wenn und wenn andere Regionen zur Roadmap hinzugefügt werden.

**Was ist in OneDrive for Business und SharePoint Online enthalten?**

Derzeit sind nur Dateien und Dokumente, die zu OneDrive for Business und SharePoint Online hochgeladen wurden, mit PCI DSS kompatibel.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Verwenden von Microsoft Compliance-Manager zur Einschätzung des Risikos

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) ist eine Funktion im [Microsoft 365 Compliance Center](/microsoft-365/compliance/microsoft-365-compliance-center), die Ihnen hilft, die Compliance-Position Ihres Unternehmens zu verstehen und Maßnahmen zu ergreifen, um Risiken zu reduzieren. Compliance Manager bietet eine Premiumvorlage für die Erstellung einer Bewertung für diese Verordnung. Suchen Sie die Vorlage auf der Seite **Bewertungsvorlagen** im Compliance Manager. Erfahren Sie, wie Sie [Bewertungen im Compliance-Manager erstellen](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Ressourcen

- [PCI Security Standards Council](https://www.pcisecuritystandards.org/)
- [PCI Data Security Standard](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-1.pdf)
- [PCI DSS Quick Reference Guide](https://www.pcisecuritystandards.org/documents/PCISSC%20QRG%20August%202014%20-print.pdf)
- [Compliance im Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
