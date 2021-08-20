---
title: Co je nového, duben 2021 - omezené nasazení Project Operations
description: Tento téma poskytuje informace o aktualizacích kvality, které jsou k dispozici v omezeném nasazení Project Operations z dubna 2021.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c85e0230840753bc1d28a46b065bce002446f5d8c62da9666d58bc9d2a68af8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009388"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Co je nového, duben 2021 - omezené nasazení Project Operations

_Platí pro: Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

  - Project Operations v prostředí Dataverse verze 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

V této vydané verzi jsou zahrnuty následující funkce:

- Neuskladněné materiály pro projekty. Mezi klíčové funkce patří:
  - Odhad a stanovení ceny neuskladněných materiálů během prodejního cyklu projektu. Více informací najdete v tématu [Nastavení nákladových a prodejních sazeb pro produkty katalogu - omezené](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Sledování využití neskladovaných materiálů během dodání projektu. Více informací najdete v tématu [Záznam využití materiálu na projektech a projektových úkolech](../../material/material-usage-log.md).
  - Fakturace použitého materiálu, který není na skladě. Více informací najdete v tématu [Správa nedokončené fakturace - omezené](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Nová rozhraní API v Dynamics 365 Dataverse umožňují operace vytváření, aktualizace a odstraňování **entit plánování**. Více informací najdete v tématu [Používání rozhraní Schedule API k provádění operací s entitami plánování](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| Fakturace a ceny | 2224568 | Přidaná logika povolující přizpůsobení, která zahrnuje vyvolání doplňku pro potvrzení faktury. |
| Fakturace a ceny | 2101098 | Vylepšena logika výchozích polí proforma faktury: **Fakturační adresa**, **Fakturační adresa – název** a **Platební podmínky** nyní přebírají výchozí hodnotu z příslušného záznamu zákazníka projektové smlouvy. |
| Fakturace a ceny | 2021413 | Aktualizována pole **Skutečná cena** a **Prodeje** u entity **Úkol**, která nově zahrnují hodnoty prodeje z nevyfakturovaných a fakturovaných výdajů na úkoly. |
| Fakturace a ceny | 2182110 | Při kopírování projektové smlouvy se ID řádku smlouvy znovu vygeneruje v cílové projektové smlouvě, aby se zajistilo, že je jedinečné. |
| Správa příležitostí | 2186741 | Přidaná ověření, která zajištují, že u polí **Původ** a **Typ transakce** nelze aktualizovat existující podrobnosti řádku nabídky. |
| Správa příležitostí | 2191353 | Milníky nesmí být vytvářeny na řádku smlouvy s časem a materiálem. |
| Správa příležitostí | 2216956 | Opraveny problémy ve funkci **Aktualizovat ceny**. |
| Plánování a sledování | 2182979 | Vylepšena funkce kopírování projektu, aby bylo zajištěno, že řádky odhadu výdajů budou zkopírovány z původního projektu. |
| Plánování a sledování | 2184144 | Vylepšena funkce kopírování projektu, aby bylo zajištěno, že název pozice zdroje bude zkopírován z původního projektu. |
| Plánování a sledování | 2184799 | Kopie projektu: Zpřísněna kontrola zajišťující, že odhadované datum zahájení nelze během kopírování změnit. |
| Plánování a sledování | 2185134 | Kopie projektu: Odhadované datum zahájení cílového projektu je nastaveno na dnešní datum. |
| Plánování a sledování | 2196373 | Kopie projektu: Zajištění, aby záznamy projektového manažera a člena týmu nebyly v projektovém týmu duplikovány. |
| Plánování a sledování | 2211833 | Kopie projektu: Přiřazení zdrojů se zkopírují z úlohy zdrojového projektu do cílového projektu. |
| Plánování a sledování | 2186541 | Opraveny problémy v mřížce **Odhady** při seskupování podle zdrojů. |
| Plánování a sledování | 2166906 | Kategorie transakcí z úkolu musí být zkopírována do entity **Přiřazení zdrojů**. |
| Správa zdrojů | 2125362 | Opraveny problémy při vytváření obecného člena týmu pomocí metody přidělování podle hodin. |
| Čas a výdaje | 2113603 | Opraven problém související s přizpůsobením při odstraňování atributů ze stránky **Zadání času**. Systém nyní před přístupem s využitím skriptu zkontroluje, zda atribut na stránce existuje. |
| Čas a výdaje | 2204377 | Zkopírované časové rozvrhy se musí automaticky zobrazit, když během zadávání času vyberete možnost **Kopírovat týden**. |
| Čas a výdaje | 2209059 | Pole **Stav** lze u časových údajů Dynamics 365 Field Service upravit. |
