---
title: Správa nedokončené fakturace
description: Toto téma poskytuje informace o tom, jak zobrazovat nedokončenou fakturaci a pracovat s ní v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bec6afe04a705d4f55ac3a7de93a64b47021fbb4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122335"
---
# <a name="manage-the-billing-backlog"></a>Správa nedokončené fakturace

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations má dva vyhrazené pohledy, které vám pomohou pracovat a spravovat nevyřízené položky fakturace. Jsou to **Milníky pevné ceny** a **Nevyřízená fakturace času a materiálu**. Chcete-li vybrat pohled, v oblasti **Prodej** v Project Operations na levé navigační stránce vyberte **Fakturace**. Jsou zde uloženy odkazy na nevyřízenou fakturaci.

## <a name="fixed-price-milestones"></a>Milníky s pevnou cenou

Toto zobrazení uvádí všechny milníky fixních cen ve všech řádcích smluv projektu v systému. Jeden nebo více milníků lze označit jako **Připraveno k fakturaci** nebo **Není připraveni na fakturaci** z tohoto pohledu. Když označíte milník jako **Připraveno k fakturaci**, milník bude k dispozici pro koncept faktury.

Pokud mají řádky smlouvy pro více zákazníků pevnou metodu fakturace, vytvoří se jeden milník pro každého zákazníka na řádce smlouvy. Uživatel vytvoří milník a tento milník se interně rozdělí na záznamy o zákaznících = specifické milníky podle rozdělení fakturačního procenta definovaného pro každého zákazníka na řádku smlouvy. V zobrazení **Milníky pevné ceny** uvidíte jednotlivé záznamy o milnících konkrétních zákazníků. Každý z těchto milníků lze označit jako **Připraveno k fakturaci** odděleně z tohoto zobrazení. Když je jeden nebo více souvisejících milníků rozděleno jako **Připraveno k fakturaci**, záhlaví se přesune do stavu **Probíhá** z **Nezahájeno**. Po fakturaci všech rozdělení milníku se stav milníku záhlaví stane **Dokončeno**.

V tomto zobrazení se zobrazuje milník v konceptu faktury se stavem fakturace **Zákaznická faktura vytvořena**. Po potvrzení konceptu faktury se stav fakturace v tomto záznamu aktualizuje na **Faktura zaúčtována**. Aktualizace této hodnoty stavu pomocí vlastního kódu se nedoporučuje. Pokud jsou tyto hodnoty stavu aktualizovány pomocí vlastního kódu, nebude Project Operations fungovat správně.

## <a name="time-and-material-billing-backlog"></a>Nedokončená fakturace času a materiálu

Toto zobrazení uvádí seznam všech nevyfakturovaných skutečných prodejů, které nebyly fakturovány napříč všemi smlouvami projektu v systému. Jeden nebo více nevyfakturovaných skutečných prodejů lze označit jako **Připraveno k fakturaci** nebo **Není připraveni na fakturaci** z tohoto pohledu. Označení nevyfakturovaného skutečného prodeje jako **Připraveno k fakturaci** ho zpřístupňuje k zařazení na koncept faktury.

Nevyfakturované údaje o prodeji, které mají stav **Nepřekračovat** **Selhalo** nelze označit jako **Připraveno k fakturaci**. Pokud je třeba tyto skutečné údaje označit jako takové, resetujte stav u ostatních skutečných hodnot na řádku smlouvy, které jsou potvrzeny, a poté vyhodnoťte stav **Nepřekračovat**.

V případě vícezákaznických řádků smlouvy, které mají metodu fakturace času a materiálu, se po schválení času a výdajů vytvoří nevyfakturovaná skutečná tržba pro každého zákazníka na řádce smlouvy podle procentuálního rozdělení fakturace definovaného pro každého zákazníka na řádku smlouvy. V zobrazení **Nevyřízena fakturace času a materiálu** uvidíte tyto jednotlivé nevyfakturované skutečné prodeje konkrétního zákazníka. Každý z nevyfakturovaných skutečných prodejů lze označit jako **Připraveno k fakturaci** odděleně z tohoto zobrazení.

V tomto zobrazení se zobrazuje nevyfakturovaný skutečný prodej v konceptu faktury se **stavem fakturace** **Zákaznická faktura vytvořena**. Po potvrzení konceptu faktury se stav fakturace v tomto záznamu aktualizuje na **Faktura zákazníka zaúčtována**. Aktualizace této hodnoty, když je v tomto stavu, pomocí vlastního kódu se nedoporučuje. Pokud jsou tyto hodnoty stavu aktualizovány pomocí vlastního kódu, nebude Project Operations fungovat správně.


[!INCLUDE[footer-include](../includes/footer-banner.md)]