---
title: Zálohy a smlouvy na základě záloh
description: Toto téma poskytuje informace o smluvních modelech založených na zálohách a zálohách v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ccf8ff4fa52fa6ff9fe534dfbe6736afc24ffba
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087853"
---
# <a name="advances-and-retainer-based-contracts"></a>Zálohy a smlouvy na základě záloh 


_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Dynamics 365 Project Operations podporuje smlouvy založené na zálohách. Smlouva založená na zálohách je sjednaná sada rovnoměrně distribuovaných plateb, které budou zákazníkovi fakturovány po celou dobu trvání projektu. Tento typ smlouvy se obvykle používá pro fakturační modely založené na čase a materiálu nebo spotřebě, kde je třeba zákazníkovi poskytnout předvídatelnou fakturu a plán plateb. Skutečné časově rozlišené výnosy v každém období jsou porovnány s platbami přijatými od zákazníka na začátku období. V souladu s konceptem fakturačního modelu Čas a materiál se časově rozlišené hodnoty výnosů v každém období mohou lišit podle vzniklých nákladů. Pokud je časově rozlišený výnos vyšší než částka přijatá na začátku období, mohla by společnost provádějící projekt:

- Fakturovat zákazníkovi pouze přebytek 
- Odložit odsouhlasení výnosů na další fakturační období a na konci projektu provést jedno závěrečné vyúčtování zbývajících nevyrovnaných výnosů

Hlavní rozdíl mezi smluvním modelem založeným na zálohách a smluvním modelem s pevnou cenou v Project Operations je ten, že u smluvního modelu s pevnou cenou není částka faktury spojena ani vázána na vzniklé náklady. Fakturace se řídí milníkovým přístupem, který je sladěn s náklady vzniklými za dané období. Ve smlouvě založené na zálohách se výnosy, které lze fakturovat, zaznamenávají na základě způsobu fakturace řádku smlouvy. Pokud se účtuje na základě času a materiálu, je fakturovatelný výnos vázán na náklady vzniklé v libovolném daném období a může se v jednotlivých obdobích lišit. Zákazníkovi je však fakturována pouze částka periodické zálohy. Systém používá další fakturu na konci období k vyrovnání fakturovatelných výnosů zaznamenaných během období vůči částce, která byla zákazníkovi fakturována na začátku období.

Výhodou této metody je to, že náklady zákazníka se stanou předvídatelnými v plánu záloh, na rozdíl od typického časového a materiálového modelu. Organizace doručující projekt má také určitý prostor k pokrytí rizika úhrady nákladů vzniklých v důsledku jakéhokoli zvýšení rozsahu prací, které by jim model s pevnou cenou neumožnil.

Kromě pravidelného plánu založeného na zálohách může Project Operations zaznamenat jednorázovou zálohu od zákazníka a porovnat ji s různými nákladovými složkami projektu.

Zálohu v Project Operations nelze použít, dokud nebude fakturována zákazníkovi. To naznačují následující pole v podmřížce pro zálohy.

| Pole | Relevance, účel a vedení | Dopad na následné složky |
| --- | --- | --- |
| Dostupná částka | Částka, která je k dispozici k použití v zálohovém záznamu. | Dokud nebude záloha vyfakturována, nebude možné ji použít, což znamená, že dostupná částka bude nulová. |
| Použitá částka | Částka, která je již použita v záloze. | Záloha může být částečně odsouhlasena na faktuře se skutečnými náklady, které budou mít některou část označenou jako již použitou nebo spotřebovanou. Zbytek částky zálohy je k dispozici k odsouhlasení na budoucí faktuře se skutečnými náklady. |
