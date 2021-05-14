---
title: Použití kategorie transakce jako cenové dimenze
description: Toto téma obsahuje informace o použití pole Kategorie transakce jako cenové dimenze.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c84d3aaf7cd7577dcd15311f225c82b538586445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274585"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Použití kategorie transakce jako cenové dimenze


_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


Toto téma vysvětluje, jak používat pole **Kategorie transakce** jako cenovou dimenzi. 

## <a name="prerequisites"></a>Požadavky
Než dokončíte postupy v tomto tématu, musíte mít ve své organizaci nové řešení dimenze cen. Pokud jste si ještě žádný nevytvořili, podívejte se na [Vytvořte vlastní pole a entity jako cenové dimenze](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Přidání pole Kategorie transakcí do formulářů a zobrazení
Chcete-li, aby pole **Kategorie transakcí** bylo viditelné v řešení dimenze cen, musíte pole přidat do všech formulářů a pohledů jako entitu.

V následující tabulce jsou uvedeny všechny předpřipravené formuláře a zobrazení podle entit. Také budete muset přidat nové pole do všech dalších formulářů nebo zobrazení ve vašich přizpůsobených entitách.

|  Entity        | Formuláře     |Zobrazení        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena role| Informační |- Aktivní ceny kategorií zdrojů<br> - Přidružené ceny kategorií zdrojů |
|  Přirážka ceny role| Informační|- Aktivní přirážky ceny role<br>- Přidružené přirážky cen rolí |
|  Podrobnosti řádku nabídky|- Informace o projektu<br>- Rychlé vytvoření projektu| - Aktivní podrobnosti řádků nabídek<br>- Sloučené podrobnosti řádků objednávek<br>- Přidružené podrobnosti řádků nabídek |
|  Podrobnosti řádku projektové smlouvy|- Informace o projektu<br>- Rychlé vytvoření projektu|- Sloučené podrobnosti řádků smluv<br>- Aktivní podrobnosti řádků smluv<br>- Přidružené podrobnosti řádků smluv |
|  Projektový úkol|- informace<br>- Nový formulář| &nbsp; |
|  Člen projektového týmu|- informace<br>- Nový formulář|- Aktivní členové projektových týmů<br>- Členové projektových týmů<br>- Přidružení členové projektových týmů |
|  Časový záznam|- informace<br>- Vytvořit časový záznam|- Moje časové záznamy podle data<br>- Moje časové záznamy za tento týden<br>- Časové záznamy ke schválení|
|  Řádek deníku|- informace<br>- Rychlé vytvoření|- Aktivní řádky deníků<br>- Přidružené řádky deníků|
|  Podrobnosti řádku faktury|- informace<br>- Rychlé vytvoření|- Aktivní podrobnosti řádků faktur<br>- Účtovatelné fakturační transakce<br>- Neplacené fakturační transakce<br>- Přidružené podrobnosti řádků faktur <br>- Neúčtovatelné fakturační transakce|
|  Skutečnost|- informace<br>- Aktivní skutečnosti| - Přidružené skutečnosti |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Nastavení pole Kategorie transakce jako cenové dimenze

1. Přejděte na **Nastavení** > **Parametry**. 
2. Na stránce **Parametry** na kartě **Cenové dimenze založené na částce** ověřte, že mřížka zobrazuje záznamy v entitě **Cenové dimenze**.
3. Do tohoto seznamu přidejte **Kategorii transakce** a nastavte pole **Použitelné na náklady** a **Použitelné na prodej** na **Ano**.
4. V poli **Typ dimenze** vyberte možnost **Založeno na částce** a pak vyberte prioritu pro **Kategorii transakce**, jelikož souvisí s náklady a prodejem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]