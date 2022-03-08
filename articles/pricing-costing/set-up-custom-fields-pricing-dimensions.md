---
title: Nastavení vlastních polí jako cenových dimenzí
description: Toto téma obsahuje informace o tom, jak nastavit cenové dimenze pomocí vlastních polí.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e40f0336d98cd8452642eb582c4d9daf2304ceb2532ef75ce9d03a0fa4bd8e8b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003583"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Nastavení vlastních polí jako cenových dimenzí

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Toto téma předpokládá, že než začněte, tak jste dokončili postupy v tématech [Vytvoření vlastních polí a entit](create-custom-fields-entities-pricing-dimensions.md) a [Přidání požadovaných vlastních polí do nastavení ceny a transakčních entit](add-custom-fields-price-setup-transactional-entities.md). Pokud jste tyto postupy nedokončili, vraťte se zpět, dokončete je a vraťte se k tomuto tématu. 

Toto téma obsahuje informace o nastavení vlastních cenových dimenzí. Na stránce **Parametry** na kartě **Cenové dimenze založené na částce** se zobrazují záznamy v entitách cenové dimenze. Ve výchozím nastavení jsou na této kartě v mřížce dva řádky:

- **msdyn_resourcecategory** (role)
- **msdyn_OrganizationalUnit** (organizační jednotka)

> [!IMPORTANT]
> Tyto řádky neodstraňujte. Pokud je však nepotřebujete, můžete je nastavit tak, aby byly v určitém kontextu nepoužitelné pomocí nastavení hodnoty všech možností **Použitelné na náklady**, **Použitelné pro prodej** a **Použitelné pro nákup** na **Ne**. Nastavení hodnot těchto atributů na **Ne** má stejný účinek, jako byste dané pole neměli k dispozici jako cenovou dimenzi.

Aby se pole stalo cenovou dimenzí, musí být:

- Vytvořeno jako pole v entitách **Cena role** a **Přirážka ceny role**. Další informace o tom, jak to udělat viz [Přidání vlastních polí do nastavení ceny a transakčních entit](add-custom-fields-price-setup-transactional-entities.md).

- Vytvořeno jako řádek v tabulce **Cenová dimenze**. Můžete například přidat řádky cenové dimenze, jak je znázorněno na následujícím obrázku. 

![Řádky cenové dimenze založené na částce.](media/Amt-based-PD.png)

Pracovní doba zdroje (**msdyn_resourceworkhours**) je přidána jako dimenze založená na přirážce a byla přidána do mřížky na kartě **Cenová dimenze založená na přirážce**.

![Řádky cenové dimenze založené na přirážce.](media/Markup-based-PD.png)


> [!IMPORTANT]
> Jakákoli změna v datech cenové dimenze v této tabulce, existující nebo nová, se rozšíří do obchodní logiky ocenění až po aktualizaci mezipaměti. Doba aktualizace mezipaměti může trvat až 10 minut. Povolit tuto dobu zobrazení změn v logice pro výchozí cenu, která musí být výsledkem změn v datech cenové dimenze.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributy tabulky cenových dimenzí
Následující části obsahují informace o různých atributech v tabulce **Cenové dimenze**.

### <a name="pricing-dimension-name"></a>Název cenové dimenze
Tato hodnota by měla být shodná s názvem schématu pole, které je přidáno do tabulky **Cena role** pro vlastní cenové dimenze. Další informace o přidávání polí do tabulky **Cena role** viz [Přidání vlastních polí do nastavení ceny a transakčních entit](add-custom-fields-price-setup-transactional-entities.md)

### <a name="type-of-dimension"></a>Typ dimenze
Existují dva typy cenových dimenzí:
  
  - **Dimenze založené na částce**: hodnoty dimenze ze vstupního kontextu jsou spárovány s hodnotami dimenze na řádku **Cena role** a výchozí hodnota ceny/nákladů se převezme přímo z tabulky **Cena role**.
  - **Dimenze založené na přirážce**: jedná se o dimenze, kde se použije následující 3stupňový proces pro získání ceny/nákladů:
 
    1. Hodnoty dimenze, která není založena na přirážce, ze vstupního kontextu se spárují s řádkem Cena role, aby se získala základní sazba.
    2. Hodnoty dimenze ze vstupního kontextu se sprárují s řádkem **Přirážka ceny role**, aby se získalo procento přirážky.
    3. Procento přirážky ze druhého kroku se použije na základní sazbu získanou z tabulky **Cena role** v prvním kroku k dosažení konečné ceny/nákladů.
   
   V následující tabulce je znázorněn výpočet přirážek ceny.
  
| Role        | Organizační jednotka    |Místo výkonu práce      |Standardní funkce      |Pracovní doba zdroje      |  Přirážka|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|U zákazníka            |                    |Přesčas                 |15     |
|             | Contoso India|Místní             |                    |Přesčas                 |10     |
|             | Contoso (USA)   |Místní             |                    |Přesčas                 |20     |


Pokud zdroj ze společnosti Contoso India, jehož základní sazba je 100 USD, pracuje u zákazníka a zaznamenává do časového záznamu 8 hodin pravidelného času a 2 hodiny přesčasu, použije modul ocenění k zaznamenání 800 USD základní sazbu 100 za 8 hodin. Pro dobu 2 hodin přesčasové práce se na základní sazbu 100 použije přirážka ve výši 15 % pro získání jednotkové ceny 115 USD a zaznamenají se celkové náklady na 230 USD.

### <a name="applicable-to-cost"></a>Použitelné na náklady 
Pokud je toto nastaveno na **Ano**, znamená to, že hodnota dimenze ze vstupního kontextu by měla být použita ke spárování s **Cenou role** a **Přirážkou ceny role** při načítání sazeb nákladů a přirážky.

### <a name="applicable-to-sales"></a>Použitelné na prodej
Pokud je toto nastaveno na **Ano**, znamená to, že hodnota dimenze ze vstupního kontextu by měla být použita ke spárování s **Cenou role** a **Přirážkou ceny role** při načítání fakturační sazby a sazby přirážky.

### <a name="applicable-to-purchase"></a>Použitelné na nákup
Pokud je toto nastaveno na **Ano**, znamená to, že hodnota dimenze ze vstupního kontextu by měla být použita ke spárování s **Cenou role** a **Přirážkou ceny role** při načítání nákupní ceny. Scénáře subdodávek nejsou podporovány, takže toto pole se nepoužívá. 

### <a name="priority"></a>Priorita
Nastavení priority dimenze pomáhá při tvorbě ceny, a to i v případě, že nelze nalézt přesnou shodu mezi hodnotami vstupních dimenzí a hodnotami z tabulek **Cena role** nebo **Přirážka ceny role**. V tomto scénáři se použijí hodnoty null pro nespárované hodnoty dimenzí vážením dimenzí v pořadí podle jejich priority.

- **Priorita nákladů**: hodnota priority nákladů dimenze bude označovat váhu této dimenze při párování s nastavením nákladových cen. Hodnota **Priorita nákladů** musí být jedinečná v rámci dimenzí, které jsou **Použitelné na náklady**.
- **Priorita prodeje**: hodnota priority prodeje dimenze bude označovat váhu této dimenze při párování s nastavením prodejních cen nebo fakturačních sazeb. Hodnota **Priorita prodeje** musí být jedinečná v rámci dimenzí, které jsou **Použitelné na náklady**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]