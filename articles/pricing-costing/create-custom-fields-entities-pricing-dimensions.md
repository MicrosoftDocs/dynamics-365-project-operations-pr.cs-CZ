---
title: Vytvoření vlastních polí a entit jako cenových dimenzí
description: Toto téma poskytuje informace o tom, jak vytvořit vlastní sady možností nebo entity.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000518"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Vytvoření vlastních polí a entit jako cenových dimenzí

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Následující kroky proveďte, když chcete vytvořit vlastní sadu možností nebo entitu pro použití jako cenové dimenze. Další informace viz [Přehled cenových dimenzí](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Doporučujeme provést všechny změny cenových dimenzí v samostatném řešení. Tento důležitý osvědčený postup poskytuje v budoucnu flexibilitu pro aktualizaci nebo odstranění změn podle potřeby. To také pomůže s opětovným použitím vaší práce a usnadní přenos těchto změn do jiné instance. Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované řešení** a importujte jej do jiných instancí, abyste mohli znovu použít nastavení cen.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Vytvoření vlastních polí a sad možností v řešení cenové dimenze

Cenová dimenze může být sada možností nebo entita. Obojí musí být vytvořeno ve vašem řešení ocenění. Kroky v tomto postupu vysvětlují, jak vytvořit dimenze založené na entitě a dimenze založené na sadě možností.

### <a name="entity-based-dimensions"></a>Dimenze založené na entitě
Chcete-li vytvořit dimenze založené na entitách, postupujte takto:

1. Přejděte na **Nastavení** > **Řešení** a potom dvakrát klikněte na **\<your organization name> cenové dimenze**.
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Entity**.
3. Zvolte **Nová** a vytvořte novou entitu nazvanou **Standardní funkce**. 
4. Zadejte zbývající požadované informace a zvolte **Uložit**.

> ![Definice entity Standardní funkce](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimenze založené na sadě možností 
Můžete vytvořit dvě dimenze založené na sadě možností. 

- Použijte **Místo práce zdroje**, chcete-li sledovat cenu místa práce **Doma** a práce **U zákazníka**. 
- Použijte **Pracovní dobu zdroje** s hodnotami **Pravidelný** a **Přesčas** pro použití přirážky po dokončení práce.

Následující obrázek poskytuje zobrazení dimenze **Místo práce zdroje**. 

> ![Cenová dimenze založená na sadě možností s názvem Místo výkonu práce zdroje](media/Option-set-PD-called-Resource-Work-Location.png)

Následující obrázek poskytuje zobrazení dimenze **Pracovní doba zdroje**. 

> ![Cenová dimenze založená na sadě možností s názvem Pracovní doba zdroje](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Přejděte na **Nastavení** > **Řešení** a dvakrát klikněte na **\<your organization name> cenové dimenze**. 
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Sady možností**. 
3. Vyberte **Nový** vytvořte novou sadu možností, zadejte zbývající požadované informace a poté zvolte **Uložit**.

## <a name="create-data-for-entity-based-dimensions"></a>Vytvoření dat pro dimenze založené na entitě

Data lze pro dimenze založené na entitě vytvořit ručně nebo pomocí importu aplikace Microsoft Excel nebo volání služby. Pomocí kroků v tomto postupu můžete z dimenze **Standardní funkce**, která je založena na entitě, vytvořit dvě standardní funkce, **Systémový technik** a **Hlavní systémový technik**. Pokud jsou data, která chcete vytvořit, malá, jako v následujícím příkladu, můžete použít standardní formulář.

1. Vyberte **Rozšířené hledání**.
2. Vyberte entitu **Standardní funkce** a poté vyberte **Výsledky**. Zobrazí se všechny řádky v entitě **Standardní funkce**.
3. Vyberte **Nový** a v poli **Název** vyberte "Systémový inženýr" a pak zvolte **Uložit**.
4. Zavřete stránku. 
5. Opakováním kroků 1–3 vytvořte další standardní funkci pro „Hlavního systémového technika”.

> ![Ukázková data pro entitu Standardní funkce](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]