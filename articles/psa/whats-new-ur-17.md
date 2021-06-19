---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 17, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 17, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006683"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, vydání aktualizace 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.  Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 17 pro aplikaci PSA V3. Tato verze má číslo sestavení V3.10.6.34 a je obecně k dispozici prostřednictvím automatické aktualizace v březnu 2020.


## <a name="update-release-17"></a>Aktualizace verze 17

### <a name="bug-fixes"></a>Opravy chyb

**Obecné**

- Oprava: Aktualizace Project Service Automation za účelem vynucení licencí Team Member (Centrum projektových zdrojů bude zahrnovat metadata servisního plánu pro členy týmu 3.x)
 
**Čas a výdaje**

- Oprava: Není možné změnit odhad výdajů z nenulové ceny na nulu (0). Změna je ignorována.

**Správa projektů**

- Oprava: Do názvu pozice člena týmu byla přidána kontrola nulových hodnot.
- Oprava: Pole **msdyn_userresourceid** v entitě **msdyn_resourceassignment** je zastaralé.
- Oprava: Upgrade z 2.x na 3.x nyní zpracovává prázdné křivky úsilí při přiřazování úkolů.

**Sales**

- Oprava: **Invoice.PreValidateInvoiceUpdate** nyní zpracovává scénář správného opětovného přiřazení vlastníků záznamů.
- Oprava: Když je třída transakce **Čas**, **UnitGroup** nelze upravovat pro všechny entity, včetně **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, a **ContractLineDetails**. Nicméně **Jednotka** je needitovatelná pouze pro **JournalLine** a **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]