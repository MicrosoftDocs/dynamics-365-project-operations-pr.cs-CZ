---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 17, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Project Service Automation, vydání Update 17, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915682"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, vydání aktualizace 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.  Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v PSA V3, vydání Update 17. Tato verze má číslo sestavení V3.10.6.34 a je obecně k dispozici prostřednictvím automatické aktualizace v březnu 2020.


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
