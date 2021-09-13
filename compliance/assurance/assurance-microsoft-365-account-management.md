---
title: Kontoverwaltung in Microsoft 365
description: Informationen zur Kontoverwaltung in Microsoft 365
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
ms.openlocfilehash: d525edfb9854df156f5b7b8571199b7a0102a0bf
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159184"
---
# <a name="account-management-in-microsoft-365"></a>Kontoverwaltung in Microsoft 365

Microsoft hat stark in Systeme und Kontrollen investiert, die die meisten Microsoft 365 Vorgänge automatisieren und gleichzeitig die Notwendigkeit des direkten Zugriffs auf Server und Kundendaten durch Servicemitarbeiter absichtlich einschränken. Menschen steuern den Dienst, und die Software betreibt den Dienst. Mit dieser Struktur kann Microsoft Microsoft 365 im großen Maßstab verwalten und die Risiken interner und externer Bedrohungen minimieren. Microsoft geht von der Zugriffssteuerung aus, wobei davon ausgegangen wird, dass jeder eine potenzielle Bedrohung für Microsoft 365 Dienste und Kundendaten ist. Aus diesem Grund bildet das Zero Standing Access (ZSA)-Prinzip die Grundlage für die gesamte Zugriffssteuerungsstruktur, die von Microsoft 365 verwendet wird.

Microsoft-Mitarbeiter haben standardmäßig keinen ständigen privilegierten Zugriff auf Microsoft 365 Umgebung oder Kundendaten für eine Organisation. Nur durch ein robustes System von Prüfungen und Genehmigungen können Serviceteammitarbeiter mit einer begrenzten Aktion und einem begrenzten Zeitbereich privilegierten Zugriff erhalten. Mit diesem System kann Microsoft das Risiko, dass Microsoft 365 Servicepersonal und Angreifer nicht autorisierten Zugriff erhalten oder böswilligen oder versehentlichen Schaden für Microsoft-Dienste und Kunden verursachen, erheblich reduzieren.

## <a name="account-types"></a>Kontotypen

Microsoft 365 erfüllt alle Organisatorischen Missionen und Geschäftsfunktionen mit drei Kategorien von Konten: Serviceteamkonten, Dienstkonten und Kundenkonten. Die Verwaltung dieser Konten liegt in der gemeinsamen Verantwortung von Microsoft und Kunden. Microsoft verwaltet sowohl Serviceteam- als auch Dienstkonten, die verwendet werden, um Microsoft-Produkte und -Dienste zu betreiben und zu unterstützen. Kundenkonten werden vom Kunden verwaltet und ermöglichen es ihnen, den Kontozugriff so anzupassen, dass sie ihren internen Anforderungen an die Zugriffssteuerung entsprechen.

![Gemeinsame Verantwortung für Konten](../media/assurance-shared-responsibility-for-accounts.png)

## <a name="microsoft-managed-accounts"></a>Von Microsoft verwaltete Konten

**Serviceteamkonten** werden von Microsoft 365 Serviceteammitarbeitern verwendet, die Microsoft 365 Dienste entwickeln und verwalten. Diese Konten haben keinen ständigen privilegierten Zugriff auf Microsoft 365 Dienste, sondern können stattdessen verwendet werden, um temporären und eingeschränkten privilegierten Zugriff anzufordern, um eine bestimmte Auftragsfunktion auszuführen. Nicht jedes Serviceteamkonto kann dieselben Aktionen ausführen, die Aufgabentrennung wird mithilfe der rollenbasierten Zugriffssteuerung (Role-Based Access Control, RBAC) erzwungen. Rollen stellen sicher, dass Die Mitglieder des Dienstteams und ihre Konten nur über den minimalen Zugriff verfügen, der zum Ausführen bestimmter Aufgaben erforderlich ist. Darüber hinaus können Dienstteamkonten nicht zu mehreren Rollen gehören, in denen sie als Genehmiger für ihre eigenen Aktionen fungieren können.

**Dienstkonten** werden von Microsoft 365 Diensten für die Authentifizierung bei der Kommunikation mit anderen Diensten über automatisierte Prozesse verwendet. Ebenso wie Den Serviceteamkonten nur der mindeste Zugriff gewährt wird, der zur Erfüllung der Aufgaben des jeweiligen Personals erforderlich ist, erhalten Dienstkonten nur den minimalen Zugriff, der für ihren beabsichtigten Zweck erforderlich ist. Darüber hinaus gibt es mehrere Arten von Dienstkonten, die darauf ausgelegt sind, eine bestimmte Notwendigkeit zu erfüllen. Ein Microsoft 365 Dienst kann mehrere Dienstkonten haben, die jeweils eine andere Rolle haben.

## <a name="customer-managed-accounts"></a>Von Kunden verwaltete Konten

**Kundenkonten** werden für den Zugriff auf Microsoft 365 Dienst verwendet und sind die einzigen Konten, für die jeder Kunde verantwortlich ist. Es ist die Pflicht des Kunden, die Konten in seiner Organisation zu erstellen und zu verwalten, um eine sichere Umgebung zu gewährleisten. Die Verwaltung von Kundenkonten erfolgt über Azure Active Directory (AAD) oder verbunden mit dem lokalen Active Directory (AD). Jeder Kunde hat einen eindeutigen Satz von Anforderungen an die Zugriffssteuerung, die er erfüllen muss, und Kundenkonten gewähren jedem Kunden die Möglichkeit, seine individuellen Anforderungen zu erfüllen. Kundenkonten können nicht auf Daten außerhalb ihrer Kundenorganisation zugreifen.

## <a name="service-team-account-management"></a>Verwaltung von Serviceteamkonten

Microsoft 365 verwaltet Serviceteamkonten während ihres gesamten Lebenszyklus mithilfe eines Kontoverwaltungssystems namens Identity Management (IDM). IDM verwendet eine Kombination aus automatisierten Überprüfungsprozessen und Genehmigung durch die Führung, um die Sicherheitsanforderungen im Zusammenhang mit dem Zugriff auf das Serviceteamkonto zu erzwingen.

Serviceteammitglieder erhalten nicht automatisch ein Serviceteamkonto, sie müssen zuerst die Berechtigungsanforderungen erfüllen und eine Genehmigung von einem autorisierten Vorgesetzten erhalten. Um für ein Serviceteamkonto berechtigt zu sein, müssen Die Mitarbeiter des Serviceteams zunächst das [Personalscreening vor der Einstellung,](assurance-pre-employment-screening.md)eine [Cloud-Hintergrundüberprüfung](assurance-cloud-background-check.md)und alle standardmäßigen und erforderlichen rollenbasierten Schulungen durchlaufen. Sobald alle Berechtigungsanforderungen erfüllt sind, kann eine Anforderung für ein Serviceteamkonto gestellt werden und muss von einem autorisierten Vorgesetzten genehmigt werden.

![Personalprüfungsprozess](../media/assurance-personnel-screening-process.png)

IDM ist auch für die Nachverfolgung der regelmäßigen Neuscreening und Schulungen verantwortlich, die zum Verwalten eines Serviceteamkontos erforderlich sind. Die Microsoft Cloud-Hintergrundüberprüfung muss alle zwei Jahre abgeschlossen werden, und alle Schulungsmaterialien müssen jährlich überprüft werden. Wenn eine dieser Anforderungen bis zum Ablaufdatum nicht erfüllt ist, wird die Berechtigung widerrufen, und das Serviceteamkonto wird automatisch deaktiviert.

Darüber hinaus wird die Berechtigung des Serviceteamkontos automatisch durch Die Übertragung und Beendigung des [Personals](assurance-employee-transfer-termination.md)aktualisiert. Änderungen am Personalinformationssystem (HRIS) lösen IDM zum Ergreifen von Maßnahmen aus, die je nach Situation unterschiedlich sind. Für Mitarbeiter, die zu einem anderen Serviceteam wechseln, wird ein Ablaufdatum für ihre Berechtigungen festgelegt, und eine Anforderung zur Aufrechterhaltung der Berechtigungen muss vom Serviceteammitglied übermittelt und von ihrem neuen Vorgesetzten genehmigt werden. Gekündigte Mitarbeiter haben automatisch alle Berechtigungen widerrufen, und ihr Serviceteamkonto ist am letzten Tag deaktiviert. Für unfreiwillige Kündigungen kann eine dringende Anforderung zur Kontosperrung gestellt werden.

Standardmäßig haben Serviceteamkonten eingeschränkten Lesezugriff auf allgemeine Systemmetadaten, die für die regelmäßige Problembehandlung verwendet werden. Darüber hinaus können geplante Serviceteamkonten keinen privilegierten Zugriff auf Microsoft 365 oder Kundendaten anfordern. Es muss eine weitere Anforderung gestellt werden, damit das Dienstteamkonto einer Rolle hinzugefügt wird, die es dem Serviceteammitglied ermöglicht, erhöhte Rechte anzufordern, um bestimmte Aufgaben und Vorgänge auszuführen.
