---
title: Zerstörung von Datenträgern
description: In diesem Artikel finden Sie eine Übersicht über den Prozess der Gerätevernichtung für Microsoft-Rechenzentren.
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
ms.openlocfilehash: 6a26334b805be069298302d3ad1e8e5b9e728150
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947024"
---
# <a name="data-bearing-device-destruction"></a>Zerstörung von Datenträgern

## <a name="data-destruction-overview"></a>Übersicht über die Datenvernichtung

Microsoft verfügt über Richtlinien, Richtlinien, Sicherheitsanforderungen und Verfahren für die Handhabung und Verwaltung von DBDs in Microsoft-Rechenzentren.

Ein DBD ist jedes Speichergerät, das Kunden- oder proprietäre Microsoft-Daten speichern kann:

- Festplattenlaufwerke (HDD)
- Solid-State-Laufwerke (SSD)
- USB-Laufwerke
- IO Accelerator-Karten
- SD/Compact Flash-Karten
- HSM-Karten
- PCIe-SSD-Karten
- NVDIMM (Nicht veränderliches duales Inlinespeichermodul)

Fehlgeschlagene DBDs, die in Microsoft-Rechenzentren verwendet werden, werden im Rechenzentrums-Campus überwacht und zerstört. Jedes aus dem Dienst eingestellte Objekt wird für die Entsorgung in einer Weise ausgewertet, die seinen Sicherheits-/Datenschutzanforderungen und der Klassifizierung des Objekts entspricht, und in Übereinstimmung mit den geltenden Regeln, Gesetzen und Bestimmungen.

Microsoft verwendet drei Kategorien der Datenbereinigung für DBDs und Ressourcen, die Daten enthalten:

- **Klar:** bezieht sich auf die logischen Techniken, die beim Bereinigung von Daten an allen benutzeradressierbaren Speicherorten zum Schutz vor einfachen, nicht dynamischen Datenwiederherstellungstechniken helfen. Dies sind Techniken, die in der Regel über die standardmäßigen Lese- und Schreibbefehle auf das Speichergerät angewendet werden, z. B. durch Umschreiben mit einem neuen Wert oder Verwenden einer Menüoption, um das Gerät auf den Werkszustand zurückzusetzen (wobei das Umschreiben nicht unterstützt wird).
- **Bereinigung:** bezieht sich auf physische oder logische Techniken, die die Wiederherstellung von Zieldaten mithilfe aktueller Techniken des Labors unbrauchbar machen.
- **Destroy**: rendert die Zieldatenwiederherstellung mithilfe aktueller Techniken und führt zu der nachfolgenden Unfähigkeit, die Medien für die Speicherung von Daten zu verwenden.

Das Bereinigen und Zerstören der Bereinigung erfolgt mithilfe von Tools und Prozessen, die von der Sicherheitsgruppe genehmigt wurden. Es werden Aufzeichnungen über die Löschung und Vernichtung von Objekten aufbewahrt. Geräte, die das Löschen nicht abschließen, werden erfolgreich entfernt (nur für magnetische Medien), mehrfach angeheftete (für gechipte basierte Boards wie SSDs) oder zerstört.

## <a name="clear"></a>Deaktivieren

Wenn ein veraltetes Objekt ausgewertet und als nicht zugänglich eingestuft wird, wird es von einer genehmigten Lösung zur Datenlöschung gelöscht. Microsoft-Rechenzentren verwenden die klaren Richtlinien für NIST SP-800-88.

## <a name="purge"></a>Säubern

Je nach Konfiguration vor Ort und Geräteverfügbarkeit werden einige Geräte vor der Vernichtung gelöscht. Zu den Bereinigungsgeräten gehören von der NSA genehmigte Entbindungsgeräte für magnetische Medien und Multi-Pin-Löschgeräte für Festkörpermedien. Microsoft-Rechenzentren verwenden die NIST SP-800-88-Bereinigungsrichtlinien.

## <a name="destroy"></a>Vernichten

Wenn ein veraltetes Objekt ausgewertet und als barrierefrei eingestuft wird, wird es vor Ort mithilfe eines genehmigten Standardbetriebsverfahrens zerstört, das den NIST SP-800-88-Richtlinien entspricht. Diese DBDs werden physisch und logisch nachverfolgt, um die Verwahrungskette durch endgültige Disposition aufrechtzuerhalten.

Jedes Microsoft-Rechenzentrum verwendet einen Prozess vor Ort, um fehlerhafte und veraltete DBDs zu bereinigt und zu löschen. Während dieses Prozesses stellen Microsoft-Mitarbeiter sicher, dass die Aufbewahrungskette während des gesamten Entsorgungsprozesses aufrechterhalten wird.

## <a name="resources"></a>Ressourcen

- [NIST Special Publication 800-88](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)
