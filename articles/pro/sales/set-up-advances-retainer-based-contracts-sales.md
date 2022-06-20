---
title: Zálohy a smlouvy na základě záloh
description: Tento článek poskytuje informace o smluvních modelech založených na zálohách a zálohách v Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 201dd1651b12614930f6a2c294156b31deceab0b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932472"
---
# <a name="advances-and-retainer-based-contracts"></a>Zálohy a smlouvy na základě záloh


_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations podporuje smlouvy na základě záloh. Smlouva založená na zálohách je sjednaná sada rovnoměrně distribuovaných plateb, které budou zákazníkovi fakturovány po celou dobu trvání projektu. Tento typ smlouvy se obvykle používá pro fakturační modely založené na čase a materiálu nebo spotřebě, kde je třeba zákazníkovi poskytnout předvídatelnou fakturu a plán plateb. Skutečné časově rozlišené výnosy v každém období jsou porovnány s platbami přijatými od zákazníka na začátku období. V souladu s konceptem fakturačního modelu Čas a materiál se časově rozlišené hodnoty výnosů v každém období mohou lišit podle vzniklých nákladů. Pokud je časově rozlišený výnos vyšší než částka přijatá na začátku období, mohla by společnost provádějící projekt:

- Fakturovat zákazníkovi pouze přebytek 
- Odložit odsouhlasení výnosů na další fakturační období a na konci projektu provést jedno závěrečné vyúčtování zbývajících nevyrovnaných výnosů

Hlavní rozdíl mezi smluvním modelem založeným na zálohách a smluvním modelem s pevnou cenou v Project Operations je ten, že u smluvního modelu s pevnou cenou není částka faktury spojena ani vázána na vzniklé náklady. Fakturace se řídí milníkovým přístupem, který je sladěn s náklady vzniklými za dané období. Ve smlouvě založené na zálohách se výnosy, které lze fakturovat, zaznamenávají na základě způsobu fakturace řádku smlouvy. Pokud se účtuje na základě času a materiálu, je fakturovatelný výnos vázán na náklady vzniklé v libovolném daném období a může se v jednotlivých obdobích lišit. Zákazníkovi je však fakturována pouze částka periodické zálohy. Systém používá další fakturu na konci období k vyrovnání fakturovatelných výnosů zaznamenaných během období vůči částce, která byla zákazníkovi fakturována na začátku období.

Výhodou této metody je to, že náklady zákazníka se stanou předvídatelnými v plánu záloh, na rozdíl od typického časového a materiálového modelu. Organizace doručující projekt má také určitý prostor k pokrytí rizika úhrady nákladů vzniklých v důsledku jakéhokoli zvýšení rozsahu prací, které by jim model s pevnou cenou neumožnil.

Kromě pravidelného plánu založeného na zálohách může Project Operations zaznamenat jednorázovou zálohu od zákazníka a porovnat ji s různými nákladovými složkami projektu.

Zálohu v Project Operations nelze použít, dokud nebude fakturována zákazníkovi. To naznačují následující pole v podmřížce pro zálohy.

| Pole | Popis | Dopad na následné složky |
| --- | --- | --- |
| Dostupná částka | Částka, která je k dispozici k použití v zálohovém záznamu. | Dokud nebude záloha vyfakturována, nebude možné ji použít, což znamená, že dostupná částka bude nulová. |
| Použitá částka | Částka, která je již použita v záloze. | Záloha může být částečně odsouhlasena na faktuře se skutečnými náklady, které budou mít některou část označenou jako již použitou nebo spotřebovanou. Zbytek částky zálohy je k dispozici k odsouhlasení na budoucí faktuře se skutečnými náklady. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]