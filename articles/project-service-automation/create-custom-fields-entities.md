---
title: Vytvoření vlastních polí a entit
description: Toto téma vysvětluje, jak vytvořit sady možností a entity ve vlastním řešení na platformě Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750400"
---
# <a name="create-custom-fields-and-entities"></a>Vytvoření vlastních polí a entit 

Následující kroky proveďte pokaždé, když chcete na platformě Power Apps vytvořit vlastní sadu možností nebo entitu.  
Postupy v tomto tématu by měly být prováděny prostřednictvím webového rozhraní Project Service Automation (PSA).

> [!IMPORTANT]
> Doporučujeme provést všechny změny cenových dimenzí v samostatném řešení. Tento důležitý osvědčený postup poskytuje v budoucnosti flexibilitu pro aktualizaci nebo odebrání změn podle potřeby, pomůže při opětovném použití vaší práce a usnadní portování těchto změn na jinou instanci. Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované řešení** a importujte ho do jiných instancí za účelem znovupoužití vašeho nastavení cen.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Vytvoření vlastního řešení pro cenové dimenze
1. V PSA klikněte na **Nastavení** > **Řešení** a pak kliknutím na **Nové** vytvořte nové řešení. 
2. Řešení nazvěte **\<název vaší organizace> cenové dimenze**, zadejte zbývající požadované informace a poté klikněte na **Uložit**.

> ![Vytvoření vlastního řešení pro cenové dimenze](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Vytvoření vlastních polí a sad možností v řešení cenové dimenze

Cenová dimenze může být sada možností nebo entita. Obojí musí být vytvořeno ve vašem řešení ocenění. Kroky v tomto postupu vysvětlují, jak vytvořit dimenze založené na entitě a dimenze založené na sadě možností.

### <a name="entity-based-dimensions"></a>Dimenze založené na entitě

1. V PSA klikněte na **Nastavení** > **Řešení** a potom klikněte dvakrát na **\<název vaší organizace> cenové dimenze**.
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Entity**.
3. Kliknutím na **Nová** vytvoříte novou entitu nazvanou **Standardní funkce**. Zadejte zbývající požadované informace a klikněte na **Uložit**.

> ![Definice entity Standardní funkce](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimenze založené na sadě možností 
Můžete vytvořit dvě dimenze založené na sadě možností. Ke sledování ceny práce v místě **Domácí** a práce **U zákazníka** použijte **Místo výkonu práce zdroje** a chcete-li po dokončení práce použít přirážku, použijte **Pracovní dobu zdroje** s hodnotami **Normální** a **Přesčas**.


1. V PSA klikněte na **Nastavení** > **Řešení** a potom klikněte dvakrát na **\<název vaší organizace> cenové dimenze**. 
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

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Přidání všech požadovaných entit PSA a souvisejících komponent do Řešení cenové dimenze
K vašemu řešení ocenění bude nutné přidat následující entity Project Service. Pomocí kroků v tomto postupu můžete provést některé důležité změny schématu v řešení ocenění, aby si entity všimly nových cenových dimenzí.

1. V PSA klikněte na **Nastavení** > **Řešení** a potom klikněte dvakrát na **\<název vaší organizace> cenové dimenze**. 
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Přidat existující** > **Entity**.
3. V dialogovém okně **Součásti řešení** vyberte následující entity:

- Skutečnost
- Rezervovatelný zdroj
- Řádek odhadu
- Podrobnosti řádku faktury
- Řádek deníku
- Podrobnosti řádku projektové smlouvy
- Člen projektového týmu
- Podrobnosti řádku nabídky
- Přirážka ceny role
- Cena role 
- Časový záznam 

> ![Přidat existující entity k řešení cenových dimenzí](media/Existing-entities-to-PD-solution.png)

> ![Vybrat součásti řešení](media/Dimension-Components.png)

> [!NOTE]
> Nezapomeňte zahrnout všechny formuláře a zobrazení pro všechny vybrané entity.

4. Při zobrazení výzvy k zahrnutí všech závislých entit do výše vybraných entit klikněte na **Ne**.

> ![Nezahrnovat všechny související komponenty](media/Do-not-include-required.png)


