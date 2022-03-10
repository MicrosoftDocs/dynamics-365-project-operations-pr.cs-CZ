---
title: Správa nedokončené fakturace produktů
description: Tento téma poskytuje informace o různých pohledech, které jsou k dispozici při správě nevyřízených fakturací u projektů.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 27ef2ae90778394d15b979a13215c8f5af483cda0312682e9fc7256b8282b999
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988283"
---
# <a name="manage-project-billing-backlog"></a>Správa nedokončené fakturace produktů 

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Dynamics 365 Project Operations má vyhrazená zobrazení, která pomáhají spravovat nedokončené fakturace. Chcete-li spravovat nedokončené fakturace, vyberte odkazy v oblasti **Prodej** v části **Fakturace**. 

K dispozici jsou následující zobrazení:

- Zálohy
- Dostupné zálohy
- Milníky s pevnou cenou
- Nedokončená fakturace produktů
- Nedokončená fakturace času a materiálu

## <a name="retainers-and-advances"></a>Zálohy

Zobrazení **Zálohy** obsahuje seznam všech záloh ve všech smlouvách projektu v systému. Po fakturaci zálohy bude částka zálohy k dispozici k použití.

## <a name="available-retainers-and-advances"></a>Dostupné zálohy

Zobrazení **Dostupné zálohy** obsahuje seznam všech dostupných záloh ve všech smlouvách projektu v systému. Po fakturaci zálohy bude částka zálohy k dispozici k použití a je přidána do seznamu. Poté, co je částka zálohy zcela vyčerpána, je odstraněna ze seznamu.

## <a name="fixed-price-milestones"></a>Milníky s pevnou cenou

Zobrazení **Milníky s pevnou cenou** obsahuje všechny milníky s pevnou cenou napříč všemi řádky smlouvy projektu v systému. Jeden nebo více milníků lze označit jako **Připraveno k fakturaci** nebo **Nepřipraveno k fakturaci** z tohoto zobrazení. Označení milníku jako **Připraveno k fakturaci** jej zpřístupňuje k zařazení do konceptu faktury.

Když mají řádky smlouvy pro více zákazníků metodu fakturace s pevnou cenou, vytvoří se milník pro každého zákazníka na řádku smlouvy. Milník může být vytvořen a poté rozdělen do jednotlivých záznamů milníků specifických pro zákazníka. Toto rozdělení je interní a v souladu s rozdělením fakturačního procenta definovaným pro každého zákazníka na řádku smlouvy. V zobrazení **Milníky s pevnou cenou** uvidíte jednotlivé záznamy milníků konkrétních zákazníků. Každý z těchto milníků lze označit jako **Připraveno k fakturaci** odděleně z tohoto zobrazení. Když je jeden nebo více souvisejících milníků rozděleno jako **Připraveno k fakturaci**, je stav záhlaví aktualizován na **Probíhá** z **Nezahájeno**. Když jsou fakturovány všechna rozdělení milníků, je stav milníku záhlaví aktualizován na **Dokončeno**.

V tomto zobrazení se zobrazuje milník v konceptu faktury se stavem fakturace **Zákaznická faktura vytvořena**. Po potvrzení konceptu faktury se stav fakturace v záznamu aktualizuje na **Faktura zákazníka zaúčtována**. Neaktualizujte tuto hodnotu stavu pomocí vlastního kódu. Pokud jsou tyto hodnoty stavu aktualizovány pomocí vlastního kódu, Project Operations nefunguje správně.

## <a name="product-billing-backlog"></a>Nedokončená fakturace produktů

Zobrazení **Nedokončená fakturace produktů** obsahuje seznam všech řádků smlouvy na základě produktu napříč všemi smlouvami projektu v systému. Jeden nebo více řádek smlouvy na základě produktu lze označit jako **Připraveno k fakturaci** nebo **Nepřipraveno k fakturaci** z tohoto zobrazení. Označení řádku smlouvy na základě produktu jako **Připraveno k fakturaci** jej zpřístupňuje k zařazení do konceptu faktury.

Řádek smlouvy na základě produktu, který je v konceptu faktury, je zobrazen v tomto zobrazení se stavem fakturace **Faktura zákazníka vytvořena**. Po potvrzení konceptu faktury se stav fakturace v tomto záznamu aktualizuje na **Faktura zákazníka zaúčtována**. Neaktualizujte tuto hodnotu stavu pomocí vlastního kódu. Pokud jsou tyto hodnoty stavu aktualizovány pomocí vlastního kódu, Project Operations nefunguje správně.

## <a name="time-and-material-billing-backlog"></a>Nedokončená fakturace času a materiálu

Zobrazení **Nedokončená fakturace času a materiálu** obsahuje seznam všech nefakturovaných skutečných prodejů napříč všemi smlouvami projektu v systému, které nebyly fakturovány. Jeden nebo více nevyfakturovaných skutečných prodejů lze označit jako **Připraveno k fakturaci** nebo **Není připraveni na fakturaci** z tohoto pohledu. Označení nevyfakturovaného skutečného prodeje jako **Připraveno k fakturaci** ho zpřístupňuje k zařazení na koncept faktury.

Nefakturované skutečné prodeje se stavem **Nepřekročitelné** s hodnotou **Chyba** nelze označit jako **Připraveno k fakturaci**. Pokud je třeba skutečné prodeje označit jako **Připraveno k fakturaci**, obnovte stav u ostatních skutečných prodejů na řádku smlouvy, které jsou potvrzeny. a poté znovu vyhodnoťte stav **Nepřekročitelné**.

Pokud řádky smlouvy pro více zákazníků mají metodu fakturace času a materiálu, je po schválení času a výdajů vytvořen jeden nefakturovaný skutečný prodej pro každého zákazníka na řádku smlouvy podle procentuálního rozdělení fakturace definovaného pro každého ze zákazníků. V zobrazení **Nedokončená fakturace času a materiálu** vidíte tyto nefakturované skutečné prodeje pro jednotlivé konkrétní zákazníky. Každý z nevyfakturovaných skutečných prodejů lze označit jako **Připraveno k fakturaci** odděleně z tohoto zobrazení.

Nefakturovaný skutečný prodej, který je v konceptu faktury, je zobrazen v tomto zobrazení se stavem fakturace **Faktura zákazníka vytvořena**. Po potvrzení konceptu faktury se stav fakturace v tomto záznamu aktualizuje na **Faktura zákazníka zaúčtována**. Neaktualizujte tuto hodnotu stavu pomocí vlastního kódu. Pokud jsou tyto hodnoty stavu aktualizovány pomocí vlastního kódu, Project Operations nefunguje správně.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
