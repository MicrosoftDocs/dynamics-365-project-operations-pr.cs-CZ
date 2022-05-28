---
title: Správa nedokončené fakturace
description: Toto téma poskytuje informace o tom, jak zobrazovat nedokončenou fakturaci a pracovat s ní v aplikaci Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9837af0d3c0b2476edab35a53092cf95a44e5244
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599970"
---
# <a name="manage-billing-backlog"></a>Správa nedokončené fakturace

_ **Platí pro:** Project Operations u scénářů založených na zdrojích / položkách, které nejsou na skladě

Dynamics 365 Project Operations má vyhrazená zobrazení, která pomáhají spravovat nedokončené fakturace. Chcete-li spravovat nedokončené fakturace, vyberte odkazy v oblasti **Prodej** v části **Fakturace**. 

K dispozici jsou následující zobrazení:

- Zálohy
- Dostupné zálohy
- Milníky s pevnou cenou
- Nedokončená fakturace času a materiálu

## <a name="retainers-and-advances"></a>Zálohy

Zobrazení **Zálohy** obsahuje seznam záloh ve všech smlouvách projektu. Po fakturaci zálohy bude částka zálohy k dispozici k použití.

## <a name="available-retainers-and-advances"></a>Dostupné zálohy

Zobrazení **Dostupné zálohy** obsahuje seznam všech dostupných záloh ve všech smlouvách projektu. Po fakturaci zálohy bude částka zálohy k dispozici k použití a je přidána do seznamu. Jakmile je částka zálohy zcela vyčerpána, je odstraněna ze seznamu.

## <a name="fixed-price-milestones"></a>Milníky s pevnou cenou

Zobrazení **Milníky pevné ceny** obsahuje seznam všech milníků pevné ceny napříč všemi řádky smlouvy projektu. Z tohoto pohledu lze označit jeden nebo více milníků jako **Připraveno k fakturaci** nebo **Není připraveno k fakturaci**. Označení milníku jako **Připraveno k fakturaci** jej zpřístupňuje k zařazení do konceptu faktury.

Když mají řádky smlouvy pro více zákazníků metodu fakturace s pevnou cenou, vytvoří se milník pro každého zákazníka na řádku smlouvy. Milník může být vytvořen a poté rozdělen do jednotlivých záznamů milníků specifických pro zákazníka. Toto rozdělení je interní a v souladu s rozdělením fakturačního procenta definovaným pro každého zákazníka na řádku smlouvy. V zobrazení **Milníky s pevnou cenou** uvidíte jednotlivé záznamy milníků konkrétních zákazníků. Každý z těchto milníků lze označit jako **Připraveno k fakturaci** odděleně z tohoto zobrazení. Když je jedno nebo více rozdělení souvisejících milníků označeno jako **Připraveno k fakturaci**, stav záhlaví se aktualizuje na **Probíhá** z **Nezahájeno**. Když jsou fakturovány všechna rozdělení milníku, stav milníku záhlaví se aktualizuje na **Dokončeno**.

V tomto zobrazení se zobrazuje milník v konceptu faktury se stavem fakturace **Zákaznická faktura vytvořena**. Po potvrzení konceptu faktury se stav fakturace v záznamu aktualizuje na **Faktura zákazníka zaúčtována**. 

> [!NOTE] 
> Neaktualizujte tuto hodnotu stavu pomocí vlastního kódu. Pokud jsou tyto hodnoty stavu aktualizovány pomocí vlastního kódu, Project Operations nefunguje správně.

## <a name="time-and-material-billing-backlog"></a>Nedokončená fakturace času a materiálu

Zobrazení **Nedokončená fakturace času a materiálu** obsahuje seznam všech nefakturovaných skutečných prodejů napříč všemi smlouvami projektu v systému, které nebyly fakturovány. Jeden nebo více nevyfakturovaných skutečných prodejů lze označit jako **Připraveno k fakturaci** nebo **Není připraveni na fakturaci** z tohoto pohledu. Označení nevyfakturovaného skutečného prodeje jako **Připraveno k fakturaci** ho zpřístupňuje k zařazení na koncept faktury.

Nefakturované skutečné prodeje se stavem **Nepřekročitelné** s hodnotou **Chyba** nelze označit jako **Připraveno k fakturaci**. Pokud je třeba údaje označit jako **Připraveno k fakturaci**, resetujte stav u ostatních skutečných hodnot na řádku smlouvy, které jsou potvrzeny, a poté znovu vyhodnoťte stav **Nepřekračovat**.

Pokud řádky smlouvy pro více zákazníků mají metodu fakturace času a materiálu, je po schválení času a výdajů vytvořen jeden nefakturovaný skutečný prodej pro každého zákazníka na řádku smlouvy podle procentuálního rozdělení fakturace definovaného pro každého ze zákazníků. V zobrazení **Nedokončená fakturace času a materiálu** vidíte tyto nefakturované skutečné prodeje pro jednotlivé konkrétní zákazníky. Každý z nevyfakturovaných skutečných prodejů lze označit jako **Připraveno k fakturaci** odděleně z tohoto zobrazení.

Skutečný nevyfakturovaný prodej, který je na konceptu faktury, se zobrazuje v tomto zobrazení se stavem fakturace **Zákaznická faktura vytvořena**. Po potvrzení konceptu faktury se stav fakturace v tomto záznamu aktualizuje na **Faktura zákazníka zaúčtována**. 

> [!NOTE] 
> Neaktualizujte tuto hodnotu stavu pomocí vlastního kódu. Pokud jsou tyto hodnoty stavu aktualizovány pomocí vlastního kódu, Project Operations nefunguje správně.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
