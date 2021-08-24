---
title: Datenvernichtung in Microsoft 365
description: Eine Übersicht über die Microsoft-Richtlinien zur Wiederverwendung, Entsorgung oder Vernichtung Microsoft 365 Datenträgerlaufwerke und -server im Rechenzentrum.
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
ms.openlocfilehash: 229221d9cba2d7cc92e99086d647071556dae9e3
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482128"
---
# <a name="data-destruction-in-microsoft-365"></a>Datenvernichtung in Microsoft 365

## <a name="physical-data-destruction"></a>Phyische Datenvernichtung

Microsoft verfügt über Standardrichtlinien für die Umgang mit Daten, die das Recyceln und die Entsorgung von Festplattenlaufwerken sowie die Außerbetriebnahme von Servern behandeln. Bevor Microsoft 365 Festplattenlaufwerke wiederverwendet werden, führt Microsoft einen physischen Bereinigungsprozess durch, der mit der Speziellen Publikation 800-88 des National Institute of Standards and Technology ([NIST SP 800-88 Guidelines for Media Sanitization)](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)konsistent ist. Da alle Laufwerke in Microsoft 365 mithilfe der BitLocker-Volumeebene verschlüsselt werden, ist das Löschen von NIST SP 800-88 technisch nicht erforderlich. Dennoch führt Microsoft diesen Prozess durch.

Fehlerhafte Datenträger, die in Microsoft 365 Rechenzentren verwendet werden, werden physisch zerstört und über den ISO-Prozess überwacht. Anhand des Ressourcentyps werden die jeweils geeigneten Entsorgungsmethoden ermittelt. Bei Festplatten, die nicht gelöscht werden können, verwendet Microsoft einen Vernichtungsprozess, um die Medien zu zerstören und die Wiederherstellung von Informationen unmöglich zu machen. So werden beispielsweise Datenträger physisch vernichtet, pulverisiert oder verbrannt. Microsoft bewahrt alle Aufzeichnungen der Vernichtung auf und führt einen ähnlichen Bereinigungsprozess auf Servern durch, die innerhalb Microsoft 365 wiederverwendet werden. Diese Richtlinien umfassen sowohl elektronische als auch physische Bereinigung.

Jedes Rechenzentrum verwendet einen lokalen physischen Vernichtungsprozess, um seine Datenträger zu entsorgen. In jedem Bereich des Rechenzentrums sind sichere Container für Speichermedien vorhanden, die zur Entsorgung bestimmt sind. Jeder sichere Container für Speichermedien ist videoüberwacht. Sobald ein solcher Container eine Füllmenge von ungefähr 50% erreicht hat, kontaktiert das Standortdienst-Team das Team für physische Sicherheit, um die Entfernung zu koordinieren. Mitarbeiter des Standortdienstes und eines Sicherheitsbüros entfernen den sicheren Entsorgungsbehälter und legen ihn in einem festgelegten, geschützten Lagerbereich ab. Die Richtlinien und Verfahren zur Regelung der Handhabung von Datenträgern während der Entsorgung werden routinemäßig getestet, einschließlich Verfahren zur Sicherstellung des Zustands der Maschinen, die zur Vernichtung zugelassen sind.

Beim Datenvernichtungsprozess werden Datenträger auf eine Weise gelöscht, die mit NIST 800-88 (sofern möglich) konform ist und dann in einen industriellen Zerkleinerer gelegt und physisch zerstört. Microsoft erfüllt seine Verantwortung für Objekte, die das Rechenzentrum verlassen, durch NIST SP 800-88-konforme Reinigung, Vernichtung von Objekten, Verschlüsselung, genaue Bestandsverwaltung, Überwachung und den Schutz der Kontrollkette während des Transports. Dieser Vorgang wird über Videoüberwachungsanlagen beobachtet und nach Abschluss wird ein Vernichtungszertifikat ausgestellt.

Microsoft verwendet Datenlöschungs-Einheiten aus [Extreme Protocol Solutions](https://www.enterprisedataerasure.com/) (EPS). EPS-Software unterstützt die NIST SP 800-88 Anforderungen zum Säubern und Bereinigen/Sicheren Löschen. Vor der Bereinigung oder Vernichtung wird ein Bestand vom Microsoft-Objektverwalter erstellt. Wird ein Vertragspartner mit der Vernichtung beauftragt, stellt der Vertragspartner für jedes zerstörte Objekt ein Vernichtungszertifikat aus, welches vom Objektverwalter validiert wird.

## <a name="virtual-data-destruction"></a>Virtuelle Zerstörung von Daten

Microsoft verfügt über Richtlinien und Verfahren zur Regelung der Handhabung von Daten, die sich mit der effektiven virtuellen Zerstörung von Daten beschäftigen, um die Möglichkeit auszuschließen, dass Daten anangebrachterweise zwischen Dienstmandanten ausgetauscht werden oder nach der harten Löschung aus dem Dienst abrufbar bleiben. Auf Daten, die in einem Mandanten aus dem Dienst gelöscht wurden, kann nicht von einem anderen Dienstmandanten aus zugegriffen werden, auch wenn der zugrunde liegende physische Speicher neu zugeordnet wurde. Dies ist ein Ergebnis der gemeinsamen Effekte mehrerer Virtualisierungs- und Fragmentierungstechnologien, mit denen virtuelle Umgebungen skaliert werden, den aktiven Löschverhalten von Anwendungen innerhalb der einzelnen Dienstmandanten (z.B.: [unwiderrufliches Löschen](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)) sowie den erforderlichen Medien- und Anwendungsinhalts-Verschlüsselungsprozessen.