---
title: Použití rezervovatelného zdroje jako cenové dimenze
description: Tento článek obsahuje informace o používání rezervovatelného zdroje jako cenové dimenze.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c467c45885bbd8931eccc75862f537c0f46433ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914808"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Použití rezervovatelného zdroje jako cenové dimenze

 _**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_ 

Tento článek obsahuje informace o používání rezervovatelného zdroje jako cenové dimenze. Pokud je vaše cenová strategie nastavena tak, že každý rezervovatelný zdroj musí mít konkrétní cenu nebo míru nákladů, použijte rezervovatelný zdroj jako cenovou dimenzi.

## <a name="prerequisites"></a>Předpoklady
Než dokončíte postupy v tomto článku, musíte mít pro svou organizaci nové řešení dimenze cen. Pokud jste si ještě žádný nevytvořili, podívejte se na [Vytvořte vlastní pole a entity](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Přidat do formulářů a zobrazení pole Rezervovatelný zdroj
Chcete-li, aby pole **Rezervovatelný zdroj** bylo viditelné v řešení dimenze cen, musíte pole přidat do všech formulářů a pohledů jako entitu.

V následující tabulce jsou uvedeny všechny předpřipravené formuláře a zobrazení podle entit. Také budete muset přidat nové pole do všech dalších formulářů nebo zobrazení ve vašich přizpůsobených entitách.

|   Entity        | Formuláře   |Zobrazení        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena role| Informační | - Aktivní ceny kategorií zdrojů<br> - Přidružené ceny kategorií zdrojů |
|  Přirážka ceny role| Informační| - Aktivní přirážky ceny role<br>- Přidružené přirážky cen rolí |
|  Podrobnosti řádku nabídky| - Informace o projektu<br>- Rychlé vytvoření projektu| - Aktivní podrobnosti řádků nabídek<br>- Sloučené podrobnosti řádků objednávek<br>- Přidružené podrobnosti řádků nabídek |
|  Podrobnosti řádku projektové smlouvy| - Informace o projektu<br>- Rychlé vytvoření projektu| - Sloučené podrobnosti řádků smluv<br>- Aktivní podrobnosti řádků smluv<br>- Přidružené podrobnosti řádků smluv |
|  Projektový úkol| - informace<br>- Nový formulář| &nbsp; |
|  Člen projektového týmu| - informace<br>- Nový formulář| - Aktivní členové projektových týmů<br>- Členové projektových týmů<br>- Přidružení členové projektových týmů |
|  Časový záznam| - informace<br>- Vytvořit časový záznam| - Moje časové záznamy podle data<br>- Moje časové záznamy za tento týden<br>- Časové záznamy ke schválení|
|  Řádek deníku| - informace<br>- Rychlé vytvoření| - Aktivní řádky deníků<br>- Přidružené řádky deníků |
|  Podrobnosti řádku faktury| - informace<br>- Rychlé vytvoření| - Aktivní podrobnosti řádků faktur<br>- Účtovatelné fakturační transakce<br>- Neplacené fakturační transakce<br>- Přidružené podrobnosti řádků faktur <br>- Neúčtovatelné fakturační transakce|
|  Skutečnost| - informace<br>- Aktivní skutečnosti| Přidružené skutečnosti |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Nastavení rezervovatelného zdroje jako cenové dimenze
Chcete-li nastavit rezervovatelný zdroj jako cenovou dimenzi, postupujte následovně:

1. Přejděte na **Nastavení** > **Parametry**. 
2. Na stránce **Parametr** na kartě **Cenové dimenze založené na částce** ověřte, že mřížka zobrazuje záznamy v entitě **Cenové dimenze**. 
2. Přidat **Rezervovatelný zdroj** do tohoto seznamu cenových dimenzí jako **msdyn_bookableresource**. 
3. V **Platí pro náklady** a **Platí pro prodej** vyberte hodnotu.
4. V **Typu dimenze** vyberte **Založeno na částce**. 
5. Vyberte prioritu nákladů a prodeje pro rezervovatelný zdroj. Pokud je zahrnut jako cenová dimenze, má rezervovatelný zdroj obvykle nejvyšší prioritu. Nastavte prioritu na **1** (nebo **0** v závislosti na tom, jak počítáte prioritu) k zajištění tohoto chování.

## <a name="set-up-pricing-dimension-field-names"></a>Nastavení názvů polí cenových dimenzí

Pokud je název pole cenové dimenze v tabulce **Cena role** odlišný od jeho názvu pole v jakýchkoli jiných entitách, kde se používá výchozí cena, musí být záznam cenové dimenze s těmito odlišnými názvy obeznámen.  

Entita **Členové projektových týmů** má pro rezervovatelný zdroj mírně odlišný název pole od názvu v entitě **Cena role**: 

 - Entita **Členové projektového týmu** = **msdyn_bookableresourceid**
 - Entita **Cena role** = **msdyn_bookableresource**

Záznam cenové dimenze pro **msydn_bookableresource** s musí být o tomto rozdílu obeznámen.

1. Dvakrát klikněte na řádek v mřížce **Cenové dimenze**, aby se otevřela stránka dimenze **msdyn_bookableresource**.
2. Na stránce dimenze na kartě **Související** vyberte **Názvy polí cenových dimenzí**.

  ![Karta Názvy polí cenových dimenzí.](media/PD-fieldname.png)

3. V přidruženém zobrazení, které se otevře, vyberte **Přidat nový název pole cenové dimenze**.

  ![Přidat nové názvy polí cenové dimenze.](media/Add-NewPD-fieldname.png)

  Otevře se stránka **Nový název pole cenové dimenze** pro **msdyn_bookableresource**. 

4. Na stránce **Název nového pole dimenze cen** přidejte **msdyn_projectteam** k **Logickému názvu entity**.
5. Přidejte **msdyn_bookableresourceid** k **Názvu pole**.

 ![Nový formulář názvu pole cenové dimenze.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]