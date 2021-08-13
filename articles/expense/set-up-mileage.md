---
title: Nastavení najetých kilometrů pomocí úrovní najetých kilometrů
description: Tento téma poskytuje informace o najetých kilometrech a úrovních najetých kilometrů.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083663"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Nastavení najetých kilometrů pomocí úrovní najetých kilometrů

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Když je vykázán výdaj a je zvolená kategorie výdajů **Najeté kilometry**, částka pro daný výdajový řádek se vypočítá podle částky *sazba za kilometr*. Tato částka je určena pomocí definovaných úrovní počtu ujetých kilometrů nebo, pokud nejsou nastaveny žádné úrovně počtu ujetých kilometrů, podle standardní sazby počtu ujetých kilometrů. 

Úrovně sazby najetých kilometrů lze nastavit přechodem na **Správa výdajů** > **Nastavení** >  **Všeobecné** > **Kategorie výdajů** > **Najeto** > **Nastavení kategorie**.

Po upgradu na verzi 10.0.18, pokud vaše organizace používá kategorii výdajů za ujeté kilometry, zvažte kontrolu funkce ujetých kilometrů po kontrole návrhových změn níže. 

Nový design úrovní rychlosti najetých kilometrů ovlivňuje, jak se hodnota v poli **Množství** zpracuje. Před vydáním 10.0.18 byla hodnota v poli **Množství** považována za spodní hranici. Když akumulace překročila tuto hodnotu, byla použita odpovídající sazba.  Od verze 10.0.18 je hodnota v poli **Množství** považována za horní limit. Odpovídající sazba se použije, když je počet najetých kilometrů menší než hodnota v poli **Množství**.  Nový model pro počet ujetých kilometrů pomáhá s konzistencí napříč najetými kilometry a lepší použitelností.   

Všechny schválené výkazy výdajů budou během zaúčtování přepočítány podle nového designu.

## <a name="example"></a>Příklad
 
### <a name="before-version-10018"></a>Před verzí 10.0.18
Se dvěma úrovněmi rychlosti najetých kilometrů pole **Množství** v každé úrovni představuje spodní limit počtu kilometrů. V současné době má první úroveň hodnotu nula (0) a sazbu 0,45 a druhá úroveň má hodnotu 1000 a sazbu 0,25. Pokud nashromážděné míle nebo kilometry překročí hodnotu v poli, použije se související sazba. Pokud neexistuje žádný řádek s nulovým množstvím, systém použije sazbu najetých kilometrů, která je definována ve správě výdajů. 
 
Pokud zaměstnanec předloží výkaz výdajů s 1500 kilometr, dva řádky ujetých kilometrů v zaúčtovaném výkazu výdajů budou: 1000 (sazba 0,45) + 500 (sazba 0,25) = 575,00.

### <a name="after-version-10018"></a>Po verzi 10.0.18
Ve verzi 10.0.18 pole **Množství** pole v každé úrovni představuje horní hranici úrovně. V současné době má první úroveň hodnotu 999 a sazbu 0,45 a druhá úroveň má hodnotu 999 999 999,00 a sazbu 0,25. Pokud nashromážděné míle nebo kilometry překročí hodnotu v poli **Množství**, použije se související sazba. Pokud jsou překročeny všechny horní limity, systém použije sazbu najetých kilometrů, která je definována ve správě výdajů. 
 
Chcete-li správně vypočítat stejný scénář, je třeba změnit nastavení úrovně. Pole **Množství** v první vrstvě má hodnotu 999,00 a hodnotu 999 999 999,00 v druhé vrstvě. Pokud zaměstnanec překročí celkové množství mil nebo kilometrů na první úrovni, systém použije sazbu najetých kilometrů, která je definována ve správě výdajů. 
  
Pokud zaměstnanec předloží výkaz výdajů s 1500 kilometry, dva řádky ujetých kilometrů v zaúčtovaném výkazu výdajů budou: 1000 (sazba 0,45) + 500 (sazba 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Aktivace výpočtu počtu kilometrů u více úrovní najetých kilometrů se stejnou sazbou

Funkce **výpočtu počtu kilometrů u více úrovní najetých kilometrů se stejnou sazbou** zlepšuje výpočet sazby ujetých kilometrů. Chcete-li povolit tuto funkci, proveďte následující kroky.

1. Přejděte na **Pracovní prostory** > **Správa funkcí**. 
2. V seznamu vyhledejte a vyberte **Výpočet počtu kilometrů pro více úrovní najetých kilometrů se stejnou sazbou** a potom vyberte **Aktivovat**.

Po aktivaci této funkce resetujte úrovně najetých kilometrů, aby správně odrážely hodnotu pole **Množství**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]