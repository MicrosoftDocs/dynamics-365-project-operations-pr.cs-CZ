---
title: Rozpis výdajů
description: Toto téma vysvětluje, jak rozepisovat výdaje pomocí přepracovaného pracovního prostoru Výdaje.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b2077b77af036ce64aad203f52b03cacca8c4099
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944117"
---
# <a name="expense-itemization"></a>Rozpis výdajů

[!include [banner](../includes/banner.md)]

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Organizace často vyžadují, aby zaměstnanci poskytli podrobný rozpis výdajů vzniklých během služebních cest. Například hotelový záznam může obsahovat několik rozepsaných řádků pro sazbu za pokoj, daň, parkování a další různé výdaje vzniklé každý den během trvání pobytu. Nebo u nákladů na jídlo lze vyžadovat, abyste poskytli podrobnější rozpis snídaně, oběda nebo večeře. Bez ohledu na potřeby organizace lze každou kategorii výdajů nastavit tak, aby odrážela podkategorie nebo řádkové položky, které tvoří výdaje. Rozpis byl v **Řízení výdajů** sice vždy podporován, pracovní prostor **Přepracovaný výdaj** umožňuje efektivnější vytváření rozpisů, když je zapnuta funkce **Schopnost rychle rozepsat opakující se výdaje**.  

## <a name="enable-quick-itemization"></a>Povolení rychlého rozpisu 

Funkci **Schopnost rychle rozepsat opakující se výdaje** můžete použít k rychlému rozepsání opakujících se výdajů, a to bez nutnosti zadávat denní výdaje pokaždé po celou dobu pobytu. Chcete-li povolit rychlý rozpis, proveďte následující kroky.

1. Přejděte do pracovního prostoru **Správa funkcí** a v seznamu funkcí vyhledejte a vyberte **Sestavy výdajů v nové podobě**. 
2. Vyberte **Povolit nyní**. 
3. V seznamu funkcí vyhledejte a vyberte **Schopnost rychle rozepsat opakující se výdaje**.
4. Vyberte **Povolit nyní**. 

## <a name="itemization-grid"></a>Mřížka rozpisu 

Pokud má kategorie výdajů podkategorie nebo různé součásti, které tvoří tento výdaj, lze ji rozdělit na položky. Chcete-li rozepsat výdaj, vyberte řádek výdaje v sestavě výdajů a v podoknu **Podrobnosti výdaje** vyberte **Akce** > **Rozepsat**. Posuvník **Rozpis** zobrazí mřížku s poli. Následující tabulka uvádí příklad polí v mřížce a způsob, jakým je pole vykresleno v sestavě výdajů. 

|     Pole          |     Description                                                                                  |     Příklad              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Podkategorie    |     Seznam podkategorií konfigurovaných pod typem kategorie výdajů **Hotel**.             |     Denní sazba za pokoj      |
|     Počáteční datum     |     Datum, kdy byla nákladová položka poprvé vynaložena.                                           |     13. 9. 2021           |
|     Denní sazba     |     Částka vynaložená na nákladovou položku.                                                    |     200                  |
|     Množství       |     Počet opakování platby v souvislém období.                       |     3                    |

![Rozepište výdaje.](media/Itemization%20screen%201.png)

Když uložíte rozpis, uvidíte samostatný řádek položky pro množství zadané v mřížce rozpisu. Každý řádek začíná datem uvedeným v mřížce.

![Rozepsaná sestava.](media/Itemization%20screen%202.png)

