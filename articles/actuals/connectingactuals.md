---
title: Propojení transakcí – Propojte skutečné hodnoty různých typů transakcí
description: Tento článek vysvětluje, jak se propojení transakcí používá k propojení skutečných hodnot různých typů, což pomáhá sledovat ziskovost, nevyřízené fakturace a výpočty fakturovaných versus nevyfakturovaných příjmů.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926078"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Propojení transakcí – Propojte skutečné hodnoty různých typů transakcí

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Záznamy o připojení transakcí jsou vytvářeny za účelem propojení skutečných hodnot různých typů, jak se čas, náklady nebo využití materiálu během svého životního cyklu přesouvají z fáze nabídky nebo předprodeje do fáze smlouvy, schvalování a/nebo odvolání, fakturace a případně kreditní nebo opravné fakturace.

Následující příklad ukazuje typické zpracování časových záznamů v životním cyklu projektu Project Operations.

> ![Zpracování časových záznamů v Project Operations.](media/basic-guide-17.png)

Zpracování časových záznamů v životním cyklu projektu Project Operations dodržuje tyto kroky: 

1. Odeslání časového záznamu způsobí vytvoření dvou řádků deníku: jednoho pro náklady a jednoho pro nefakturovaný prodej. 
2. Případné schválení časového záznamu způsobí vytvoření dvou skutečných hodnot: jedné pro náklady a jedné pro nefakturovaný prodej. Tyto 2 skutečné hodnoty jsou propojeny pomocí transakčních připojení.
3. Když uživatel vytvoří projektovou fakturu, transakce řádku faktury se vytvoří pomocí dat z nefakturovaného skutečného prodeje.
4. Po potvrzení faktury se vytvoří dvě nové skutečné hodnoty: storno nefakturovaného prodeje a skutečný fakturovaný prodej. Storno nevyfakturovaného prodeje a původní skutečný nevyfakturovaný prodej jsou propojeny pomocí reverzních transakčních spojení. Fakturované prodeje a původní skutečné nevyfakturované prodeje jsou také propojeny, aby se zobrazily vazby mezi tím, co bylo dříve nevyřízeným nebo nedokončeným (WIP) výnosem, a tím, co je nyní fakturovaným výnosem.   

Každá událost v pracovním postupu zpracování spouští vytváření záznamů v tabulce **Propojení transakcí**. To pomáhá vytvořit trasování vztahů mezi záznamy, které jsou vytvořeny za celý časový záznam, řádek deníku, skutečné údaje a podrobnosti řádku faktury.

Následující tabulka zobrazuje záznamy v entitě **Propojení transakcí** pro předchozí pracovní postup.

|Událost                   |Transakce 1                 |Role transakce 1 |Typ transakce 1       |Transakce 2          |Role transakce 2 |Typ transakce 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Odeslání časového záznamu   |GUID řádku deníku (prodej)     |Nefakturovaný prodej |msdyn_journalline            |GUID řádku deníku (náklady)     |Náklady            |msdyn_journalline  |
|Schválení času           |GUID skutečné nefakturované hodnoty (prodej)  |Nefakturovaný prodej |msdyn_actual                 |GUID skutečné hodnoty nákladů (náklady)       |Náklady            |msdyn_actual       |
|Vytvoření faktury        |GUID podrobnosti řádku faktury      |Fakturovaný prodej   |msdyn_invoicelinetransaction |GUID skutečné hodnoty nefakturovaného prodeje   |Nefakturovaný prodej  |msdyn_actual       |
|Potvrzení faktury    |GUID stornování skutečné hodnoty         |Stornování      |msdyn_actual                 |GUID původního nefakturovaného prodeje |Původní        |msdyn_actual       |
|                        |GUID fakturovaného prodeje             |Fakturovaný prodej   |msdyn_actual                 |GUID skutečné hodnoty nefakturovaného prodeje   |Nefakturovaný prodej  |msdyn_actual       |
|Oprava konceptu faktury |GUID transakce řádku faktury|Nahrazení      |msdyn_invoicelinetransaction |GUID fakturovaného prodeje            |Původní        |msdyn_actual       |
|Potvrdit opravu faktury|GUID storna fakturovaného prodeje  |Stornování      |msdyn_actual                 |GUID fakturovaného prodeje            |Původní        |msdyn_actual       |
|                        |GUID nového nefakturovaného prodeje |Nahrazení            |msdyn_actual                 |GUID fakturovaného prodeje            |Původní        |msdyn_actual       |


Následující obrázek ukazuje vazby, které jsou vytvořeny mezi různými typy skutečných hodnot při různých událostech, na příkladu časových záznamů v Project Operations.

> ![Jak jsou skutečná data různých typů vzájemně propojena v Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
