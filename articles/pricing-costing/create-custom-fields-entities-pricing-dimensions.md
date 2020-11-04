---
title: Vytvoření vlastních polí a entit jako cenových dimenzí
description: Toto téma poskytuje informace o tom, jak vytvořit vlastní sady možností nebo entity.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073818"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Vytvoření vlastních polí a entit jako cenových dimenzí

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Následující kroky proveďte pokaždé, když chcete vytvořit vlastní sadu možností nebo entitu.

> [!IMPORTANT]
> Doporučujeme provést všechny změny cenových dimenzí v samostatném řešení. Tento důležitý osvědčený postup poskytuje v budoucnosti flexibilitu pro aktualizaci nebo odebrání změn podle potřeby, pomůže při opětovném použití vaší práce a usnadní portování těchto změn na jinou instanci. Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované řešení** a importujte ho do jiných instancí za účelem znovupoužití vašeho nastavení cen.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Vytvoření vlastního řešení pro cenové dimenze
1. Přejděte na **Nastavení** > **Řešení** a pak zvolte **Nové** a vytvořte nové řešení. 
2. Řešení nazvěte **\<your organization name> cenové dimenze** , zadejte zbývající požadované informace a poté vyberte **Uložit**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Vytvoření vlastních polí a sad možností v řešení cenové dimenze

Cenová dimenze může být sada možností nebo entita. Obojí musí být vytvořeno ve vašem řešení ocenění. Kroky v tomto postupu vysvětlují, jak vytvořit dimenze založené na entitě a dimenze založené na sadě možností.

### <a name="entity-based-dimensions"></a>Dimenze založené na entitě

1. Přejděte na **Nastavení** > **Řešení** a potom dvakrát klikněte na **\<your organization name> cenové dimenze**.
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Entity**.
3. Zvolte **Nová** a vytvořte novou entitu nazvanou **Standardní funkce**. 
4. Zadejte zbývající požadované informace a zvolte **Uložit**.


### <a name="option-set-based-dimensions"></a>Dimenze založené na sadě možností 
Můžete vytvořit dvě dimenze založené na sadě možností. Ke sledování ceny práce v místě **Domácí** a práce **U zákazníka** použijte **Místo výkonu práce zdroje** a chcete-li po dokončení práce použít přirážku, použijte **Pracovní dobu zdroje** s hodnotami **Normální** a **Přesčas**.


1. Přejděte na **Nastavení** > **Řešení** a dvakrát klikněte na **\<your organization name> cenové dimenze**. 
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Sady možností**. 
3. Vyberte **Nový** vytvořte novou sadu možností, zadejte zbývající požadované informace a poté zvolte **Uložit**.

## <a name="create-data-for-entity-based-dimensions"></a>Vytvoření dat pro dimenze založené na entitě

Data lze pro dimenze založené na entitě vytvořit ručně nebo pomocí importu aplikace Microsoft Excel nebo volání služby. Pomocí kroků v tomto postupu můžete z dimenze **Standardní funkce** , která je založena na entitě, vytvořit dvě standardní funkce, **Systémový technik** a **Hlavní systémový technik**. Pokud jsou data, která chcete vytvořit, malá, jako v následujícím příkladu, můžete použít standardní formulář.

1. Vyberte **Pokročilé hledání** , vyberte entitu **Standardní funkce** a potom vyberte **Výsledky**. Zobrazí se všechny řádky v entitě **Standardní funkce**.
2. Vyberte **Nový** a v poli **Název** vyberte "Systémový inženýr" a pak zvolte **Uložit**.
3. Zavře formulář. 
4. Opakováním kroků 1–3 vytvořte další standardní funkci pro „Hlavního systémového technika”.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Přidání všech požadovaných entit a souvisejících komponent do řešení cenové dimenze
K vašemu řešení cen bude nutné přidat následující entity. Pomocí kroků v tomto postupu můžete provést některé důležité změny schématu v řešení ocenění, aby si entity všimly nových cenových dimenzí.

1. Zvolte **Nastavení** > **Řešení** a dvakrát klikněte na **\<your organization name> cenové dimenze**. 
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


> [!NOTE]
> Nezapomeňte zahrnout všechny formuláře a zobrazení pro všechny vybrané entity.

4. Při zobrazení výzvy k zahrnutí všech závislých entit do výše vybraných entit zvolte **Ne**.

