---
title: Datenvernichtung in Microsoft 365
description: Eine Übersicht über Microsoft-Richtlinien zum Recycling, zur Entsorgung oder Zerstörung von Microsoft 365-Datenträgerlaufwerken und -servern.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 1b9d410422e22fe67cb27617ba16e2ddbbaec0fd
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497638"
---
# <a name="data-destruction-in-microsoft-365"></a>Datenvernichtung in Microsoft 365

## <a name="physical-data-destruction"></a>Phyische Datenvernichtung

Microsoft verfügt über Standardrichtlinien für die Umgang mit Daten, die das Recyceln und die Entsorgung von Festplattenlaufwerken sowie die Außerbetriebnahme von Servern behandeln. Bevor Microsoft 365-Festplattenlaufwerke erneut verwendet werden, führt Microsoft einen physikalischen Bestörungsprozess durch, der mit dem National Institute of Standards and Technology Special Publication 800-88 ([NIST SP 800-88 Guidelines for Media Sanitization](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)) konsistent ist. Da alle Festplattenlaufwerke in Microsoft 365 mithilfe der BitLocker-Verschlüsselung auf Volumeebene verschlüsselt werden, ist eine NIST SP 800-88-kompatible Löschung technisch nicht erforderlich. Dennoch führt Microsoft diesen Prozess durch.

Fehlgeschlagene Datenträger, die in Microsoft 365-Rechenzentren verwendet werden, werden physisch zerstört und über den ISO-Prozess überwacht. Anhand des Ressourcentyps werden die jeweils geeigneten Entsorgungsmethoden ermittelt. Bei Festplatten, die nicht gelöscht werden können, verwendet Microsoft einen Vernichtungsprozess, um die Medien zu zerstören und die Wiederherstellung von Informationen unmöglich zu machen. So werden beispielsweise Datenträger physisch vernichtet, pulverisiert oder verbrannt. Microsoft behält alle Aufzeichnungen der Zerstörung bei und führt einen ähnlichen Besentisierungsprozess auf Servern durch, die in Microsoft 365 wiederverwendet werden. Diese Richtlinien umfassen sowohl elektronische als auch physische Bereinigung.

Jedes Rechenzentrum verwendet einen lokalen physischen Vernichtungsprozess, um seine Datenträger zu entsorgen. In jedem Bereich des Rechenzentrums sind sichere Container für Speichermedien vorhanden, die zur Entsorgung bestimmt sind. Jeder sichere Container für Speichermedien ist videoüberwacht. Sobald ein solcher Container eine Füllmenge von ungefähr 50% erreicht hat, kontaktiert das Standortdienst-Team das Team für physische Sicherheit, um die Entfernung zu koordinieren. Mitarbeiter des Standortdienstes und eines Sicherheitsbüros entfernen den sicheren Entsorgungsbehälter und legen ihn in einem festgelegten, geschützten Lagerbereich ab. Die Richtlinien und Verfahren zur Regelung der Handhabung von Datenträgern während der Entsorgung werden routinemäßig getestet, einschließlich Verfahren zur Sicherstellung des Zustands der Maschinen, die zur Vernichtung zugelassen sind.

Beim Datenvernichtungsprozess werden Datenträger auf eine Weise gelöscht, die mit NIST 800-88 (sofern möglich) konform ist und dann in einen industriellen Zerkleinerer gelegt und physisch zerstört. Microsoft erfüllt seine Verantwortung für Objekte, die das Rechenzentrum verlassen, durch NIST SP 800-88-konforme Reinigung, Vernichtung von Objekten, Verschlüsselung, genaue Bestandsverwaltung, Überwachung und den Schutz der Kontrollkette während des Transports. Dieser Vorgang wird über Videoüberwachungsanlagen beobachtet und nach Abschluss wird ein Vernichtungszertifikat ausgestellt.

Microsoft verwendet Datenlöschungs-Einheiten aus [Extreme Protocol Solutions](https://www.enterprisedataerasure.com/) (EPS). EPS-Software unterstützt die NIST SP 800-88 Anforderungen zum Säubern und Bereinigen/Sicheren Löschen. Vor der Bereinigung oder Vernichtung wird ein Bestand vom Microsoft-Objektverwalter erstellt. Wird ein Vertragspartner mit der Vernichtung beauftragt, stellt der Vertragspartner für jedes zerstörte Objekt ein Vernichtungszertifikat aus, welches vom Objektverwalter validiert wird.

## <a name="virtual-data-destruction"></a>Virtuelle Zerstörung von Daten

Microsoft verfügt über Richtlinien und Verfahren zur Regelung der Handhabung von Daten, die sich mit der effektiven virtuellen Zerstörung von Daten beschäftigen, um die Möglichkeit auszuschließen, dass Daten anangebrachterweise zwischen Dienstmandanten ausgetauscht werden oder nach der harten Löschung aus dem Dienst abrufbar bleiben. Auf Daten, die in einem Mandanten aus dem Dienst gelöscht wurden, kann nicht von einem anderen Dienstmandanten aus zugegriffen werden, auch wenn der zugrunde liegende physische Speicher neu zugeordnet wurde. Dies ist ein Ergebnis der gemeinsamen Effekte mehrerer Virtualisierungs- und Fragmentierungstechnologien, mit denen virtuelle Umgebungen skaliert werden, den aktiven Löschverhalten von Anwendungen innerhalb der einzelnen Dienstmandanten (z.B.: [unwiderrufliches Löschen](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)) sowie den erforderlichen Medien- und Anwendungsinhalts-Verschlüsselungsprozessen.