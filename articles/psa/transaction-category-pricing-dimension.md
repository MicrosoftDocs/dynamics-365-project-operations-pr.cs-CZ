---
title: Použití kategorie transakce jako cenové dimenze
description: Toto téma obsahuje informace o použití kategorie transakce jako cenové dimenze.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ce878665384b75fc44bba2d413217857e0ee467c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281875"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Použití kategorie transakce jako cenové dimenze

[!include [banner](../includes/psa-now-project-operations.md)]

Toto téma ukazuje, jak používat kategorii transakce jako cenovou dimenzi. Než začnete, pokud jste ještě nevytvořili řešení cenové dimenze, bude nutné vytvořit novou. Pokud již máte řešení cenové dimenze, můžete provést změny v tomto řešení. Pokud jste pro organizaci nevytvořili nové řešení cenové dimenze, dokončete postupy v tématu [Vytvoření vlastních polí a entit](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Přidání kategorie transakce do formulářů a zobrazení
Chcete-li, aby byla kategorie transakce viditelná v uživatelském rozhraní v řešení cenové dimenze, musíte projít všechny formuláře a zobrazení klíčových entit a přidat tato pole do formulářů a zobrazení těchto entit.
Následující tabulka obsahuje úplný seznam připravených formulářů a zobrazení, uvedených podle entity, kterou bude nutné pomocí těchto nových polí aktualizovat. Pokud vaše vlastní nastavení těchto entit obsahují další zobrazení nebo formuláře, přidejte do nich tato nová pole také.

|  Entita        | Formuláře     |Zobrazení        |
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

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Nastavení kategorie transakce jako cenové dimenze

1. Ve webovém rozhraní přejděte na položky **Project Service** > **Nastavení** > **Parametry**. 
2. Na stránce **Parametry** na kartě **Cenové dimenze založené na částce** si všimněte, že mřížka na této kartě zobrazuje záznamy v entitě **Cenové dimenze**.
3. Do tohoto seznamu přidejte **Kategorii transakce** a pole **Použitelné na náklady** a **Použitelné na prodej** nastavte na **Ano**
4. V poli **Typ dimenze** vyberte možnost **Založeno na částce** a pak vyberte prioritu pro **Kategorii transakce** související s náklady a prodejem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]