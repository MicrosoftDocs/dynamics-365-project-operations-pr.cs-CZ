---
title: Použití rezervovatelného zdroje jako cenové dimenze
description: Tento článek obsahuje informace o použití rezervovatelného zdroje jako cenové dimenze.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: becb64bb137079422a765dd7cd61369297e1ffb1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916096"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Použití rezervovatelného zdroje jako cenové dimenze

[!include [banner](../includes/psa-now-project-operations.md)]

Tento článek obsahuje informace o použití rezervovatelného zdroje jako cenové dimenze. Než začnete, pokud jste ještě nevytvořili řešení cenové dimenze, bude nutné vytvořit novou. Pokud již máte řešení cenové dimenze, můžete provést změny v tomto řešení. Pokud jste pro organizaci nevytvořili nové řešení cenové dimenze, dokončete postupy v článku [Vytvoření vlastních polí a entit](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Přidat do formulářů a zobrazení rezervovatelný zdroj
Chcete-li, aby byla tato pole viditelná v uživatelském rozhraní v řešení cenové dimenze, musíte projít všechny formuláře a zobrazení klíčových entit Project Service a přidat tato pole do formulářů a zobrazení těchto entit.
Následující tabulka je úplným seznamem připravených formulářů a zobrazení, uvedených podle entity, kterou bude nutné aktualizovat. Pokud vaše vlastní nastavení těchto entit obsahují další zobrazení nebo formuláře, přidejte do nich tato nová pole také.
Otevřete Průzkumníka řešení pro řešení cenové dimenze a pak klepněte na **Publikovat všechna vlastní nastavení**.


|   Entita        | Formuláře   |Zobrazení        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena role|• Informace |• Aktivní ceny kategorií zdrojů<br> • Přidružené zobrazení cen kategorií zdrojů|
|  Přirážka ceny role|• Informace|• Aktivní přirážky ceny role<br>• Přidružené zobrazení přirážek ceny role|
|  Podrobnosti řádku nabídky|• Informace o projektu<br>• Vytvořit projekt|• Aktivní podrobnosti řádků nabídek<br>• Sloučené podrobnosti řádků objednávek<br>• Přidružené zobrazení podrobností řádků nabídek|
|  Podrobnosti řádku projektové smlouvy|• Informace o projektu<br>• Vytvořit projekt|• Sloučené podrobnosti řádků smluv<br>• Aktivní podrobnosti řádků smluv<br>• Přidružené zobrazení podrobností řádků smluv|
|  Projektový úkol|• Informace<br>• Nový formulář||
|  Člen projektového týmu|• Informace<br>• Nový formulář|• Aktivní členové projektových týmů<br>• Členové projektových týmů<br>• Přidružené zobrazení členů projektových týmů|
|  Časový záznam|• Informace<br>• Vytvořit časový záznam|• Moje časové záznamy podle data<br>• Moje časové záznamy za tento týden<br>• Časové záznamy ke schválení|
|  Řádek deníku|• Informace<br>• Vytvořit|• Aktivní řádky deníků<br>• Přidružené zobrazení řádků deníků|
|  Podrobnosti řádku faktury|• Informace<br>• Vytvořit|• Aktivní podrobnosti řádků faktur<br>• Účtovatelné fakturační transakce<br>• Neplacené fakturační transakce<br>• Přidružené zobrazení podrobností řádků faktur<br>• Neúčtovatelné fakturační transakce|
|  Skutečnost|• Informace<br>• Aktivní skutečnosti|• Přidružené zobrazení skutečností|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Nastavení rezervovatelného zdroje jako cenové dimenze

1. Ve webovém rozhraní přejděte na položky **Project Service** > **Nastavení** > **Parametry**. Na stránce **Parametr** na kartě **Cenové dimenze založené na částce** si všimněte, že mřížka na této kartě zobrazuje záznamy v entitě cenové dimenze. 
2. Přidat **Rezervovatelný zdroj** do tohoto seznamu cenových dimenzí jako **msdyn_bookableresource**. 
3. Označte kontext, ve kterém rezervovatelný zdroj pracuje, jako cenovou dimenzi, a nastavte hodnoty **Použitelné pro náklady** a **Použitelné pro prodej**.
4. V poli **Typ dimenze** vyberte **Založeno na částce**. 
5. Vyberte prioritu nákladů a prodeje pro rezervovatelný zdroj. Obvykle, pokud je rezervovatelný zdroj zahrnut jako cenová dimenze, má nejvyšší prioritu, takže její nastavení na **1** (nebo **0**, v závislosti na způsobu výpočtu priority) by zaručilo takové chování.

## <a name="set-up-pricing-dimension-field-names"></a>Nastavení názvů polí cenových dimenzí

Pokud je název pole cenové dimenze v tabulce **Cena role** odlišný od jeho názvu pole v jakýchkoli jiných entitách, kde musí fungovat výchozí cena, musí být záznam cenové dimenze s těmito odlišnými názvy obeznámen.    
Entita **Členové projektových týmů** má pro rezervovatelný zdroj mírně odlišný název pole (**msdyn_bookableresourceid**) od jeho názvu v entitě **Cena role** (**msdyn_bookableresource**). Záznam cenové dimenze pro **msydn_bookableresource** s tím musí být obeznámen. 
1. Chcete-li to provést, poklepejte na řádek v mřížce **Cenové dimenze**, aby se otevřela stránka dimenze **msdyn_bookableresource**.
2. Na stránce dimenze klikněte na kartě **Související** na **Názvy polí cenových dimenzí**.

 ![Karta Názvy polí cenových dimenzí.](media/PD-fieldname.png)

4. V přidruženém zobrazení, které se otevře, klikněte na **Přidat nový název pole cenové dimenze**.

 ![Přidat nové názvy polí cenové dimenze.](media/Add-NewPD-fieldname.png)


Otevře se stránka **Nový název pole cenové dimenze** pro **msdyn_bookableresource**. 

5. Do pole **Logický název entity** přidejte **msdyn_projectteam** a do pole **Název pole** **msdyn_bookableresourceid**. Uložte záznam.

 ![Nový formulář názvu pole cenové dimenze.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
