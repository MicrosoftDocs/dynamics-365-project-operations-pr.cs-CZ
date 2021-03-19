---
title: Vytvoření vlastních polí a entit
description: Toto téma vysvětluje, jak vytvořit sady možností a entity ve vlastním řešení na platformě Power Apps.
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
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290520"
---
# <a name="create-custom-fields-and-entities"></a>Vytvoření vlastních polí a entit 

[!include [banner](../includes/psa-now-project-operations.md)]

Následující kroky proveďte pokaždé, když chcete na platformě Power Apps vytvořit vlastní sadu možností nebo entitu.  
Postupy v tomto tématu by měly být prováděny prostřednictvím webového rozhraní Project Service Automation (PSA).

> [!IMPORTANT]
> Doporučujeme provést všechny změny cenových dimenzí v samostatném řešení. Tento důležitý osvědčený postup poskytuje v budoucnosti flexibilitu pro aktualizaci nebo odebrání změn podle potřeby, pomůže při opětovném použití vaší práce a usnadní portování těchto změn na jinou instanci. Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované řešení** a importujte ho do jiných instancí za účelem znovupoužití vašeho nastavení cen.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Vytvoření vlastních polí a sad možností v řešení cenové dimenze

Cenová dimenze může být sada možností nebo entita. Obojí musí být vytvořeno ve vašem řešení ocenění. Kroky v tomto postupu vysvětlují, jak vytvořit dimenze založené na entitě a dimenze založené na sadě možností.

### <a name="entity-based-dimensions"></a>Dimenze založené na entitě

1. V PSA klikněte na **Nastavení** > **Řešení** a pak dvakrát klikněte na **\<your organization name> cenové dimenze**.
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Entity**.
3. Kliknutím na **Nová** vytvoříte novou entitu nazvanou **Standardní funkce**. Zadejte zbývající požadované informace a klikněte na **Uložit**.

> ![Definice entity Standardní funkce](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimenze založené na sadě možností 
Můžete vytvořit dvě dimenze založené na sadě možností. Ke sledování ceny práce v místě **Domácí** a práce **U zákazníka** použijte **Místo výkonu práce zdroje** a chcete-li po dokončení práce použít přirážku, použijte **Pracovní dobu zdroje** s hodnotami **Normální** a **Přesčas**.


1. V PSA klikněte na **Nastavení** > **Řešení** a pak dvakrát klikněte na **\<your organization name> cenové dimenze**. 
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Sady možností**. 
3. Kliknutím na **Nový** vytvořte novou sadu možností, zadejte zbývající požadované informace a poté klikněte na **Uložit**.

> ![Cenová dimenze založená na sadě možností s názvem Místo výkonu práce zdroje ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Cenová dimenze založená na sadě možností s názvem Pracovní doba zdroje ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Vytvoření dat pro dimenze založené na entitě

Data lze pro dimenze založené na entitě vytvořit ručně nebo pomocí importu aplikace Microsoft Excel nebo volání služby. Pomocí kroků v tomto postupu můžete z dimenze **Standardní funkce**, která je založena na entitě, vytvořit dvě standardní funkce, **Systémový technik** a **Hlavní systémový technik**. Pokud jsou data, která chcete vytvořit, malá, jako v následujícím příkladu, můžete použít standardní formulář.

1. Klikněte v PSA na **Rozšířené hledání**. Vyberte entitu **Standardní funkce** a poté klikněte na **Výsledky**. Zobrazí se všechny řádky v entitě **Standardní funkce**.
2. Klikněte na **Nový**. Do pole **Název** zadejte „Systémový technik” a poté klikněte na **Uložit**.
3. Zavřete formulář. 
4. Opakováním kroků 1–3 vytvořte další standardní funkci pro „Hlavního systémového technika”.

> ![Ukázková data pro entitu Standardní funkce ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]