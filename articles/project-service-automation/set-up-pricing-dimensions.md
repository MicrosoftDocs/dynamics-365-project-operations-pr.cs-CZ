---
title: Nastavení vlastních polí jako cenových dimenzí
description: Toto téma obsahuje informace o nastavení vlastních cenových dimenzí.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: d5f59779-a6ed-4854-ab82-2810dace288f
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 8f19254acfc7f03ed7ccca95ed7e2b94cc199d3b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750305"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Nastavení vlastních polí jako cenových dimenzí 

Toto téma předpokládá, že než začněte, tak jste dokončili postupy v tématech [Vytvoření vlastních polí a entit](create-custom-fields-entities.md) a [Přidání vlastních polí do nastavení ceny a transakčních entit](field-references.md). Pokud jste tyto postupy nedokončili, vraťte se zpět, dokončete je a vraťte se k tomuto tématu. 

Toto téma obsahuje informace o nastavení vlastních cenových dimenzí. Karta **Cenové dimenze založené na částce** ve webovém rozhraní Project Service na stránce **Parametry** zobrazuje záznamy v entitách cenových dimenzí. Instalace Project Service vytváří ve výchozím nastavení 2 řádky v mřížce na této kartě:

- **msdyn_resourcecategory** (role)
- **msdyn_OrganizationalUnit** (organizační jednotka)

> [!IMPORTANT]
> Tyto řádky neodstraňujte. Pokud je však nepotřebujete, můžete je nastavit tak, aby byly v určitém kontextu nepoužitelné pomocí nastavení hodnoty všech možností **Použitelné na náklady**, **Použitelné pro prodej** a **Použitelné pro nákup** na **Ne**. Nastavení hodnot těchto atributů na **Ne** má stejný účinek, jako byste dané pole neměli k dispozici jako cenovou dimenzi.

Aby se pole stalo cenovou dimenzí, musí být:

- Vytvořeno jako pole v entitách **Cena role** a **Přirážka ceny role**. Další informace o tom, jak to udělat viz [Přidání vlastních polí do nastavení ceny a transakčních entit](field-references.md).
- Vytvořeno jako řádek v tabulce **Cenová dimenze**. Můžete například přidat řádky cenové dimenze, jak je znázorněno na následujícím obrázku. 

![Řádky cenové dimenze založené na částce](media/Amt-based-PD.png)

Všimněte si, že Pracovní doba zdroje (**msdyn_resourceworkhours**) byla přidána jako dimenze založená na přirážce a byla přidána do mřížky na kartě **Cenová dimenze založená na přirážce**.

![Řádky cenové dimenze založené na přirážce](media/Markup-based-PD.png)

> [!IMPORTANT]
> Jakákoli změna v datech cenové dimenze v této tabulce, existující nebo nová, se rozšíří do obchodní logiky ocenění Project Service až po aktualizaci mezipaměti. Doba aktualizace mezipaměti může trvat až 10 minut. Povolit tuto dobu zobrazení změn v logice pro výchozí cenu, která musí být výsledkem změn v datech cenové dimenze.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributy tabulky cenových dimenzí
Následující části obsahují informace o různých atributech v tabulce **Cenové dimenze**.

### <a name="pricing-dimension-name"></a>Název cenové dimenze
Tato hodnota by měla být shodná s názvem schématu pole, které je přidáno do tabulky **Cena role** pro vlastní cenové dimenze. Další informace o přidávání polí do tabulky **Cena role** viz [Přidání vlastních polí do nastavení ceny a transakčních entit](field-references.md)

### <a name="type-of-dimension"></a>Typ dimenze
Existují dva typy cenových dimenzí:
  
  - **Dimenze založené na částce**: hodnoty dimenze ze vstupního kontextu jsou spárovány s hodnotami dimenze na řádku **Cena role** a výchozí hodnota ceny/nákladů se převezme přímo z tabulky **Cena role**.
  - **Dimenze založené na přirážce**: jedná se o dimenze, kde služba Project Service přijme následující 3stupňový proces pro získání ceny/nákladů
 
    1. Služba Project Service spáruje hodnoty dimenze, která není založena na přirážce, ze vstupního kontextu s řádkem Cena role, aby získala základní sazbu.
    2. Služba Project Service spáruje všechny hodnoty dimenze ze vstupního kontextu s řádkem **Přirážka ceny role**, aby získala procento přirážky.
    3. Služba Project Service použije procento přirážky ze druhého kroku k základní sazbě získané z tabulky **Cena role** v prvním kroku k dosažení konečné ceny/nákladů.
   
   V následující tabulce je znázorněn výpočet přirážek ceny.
  
| Role        | Organizační jednotka    |Místo výkonu práce      |Standardní funkce      |Pracovní doba zdroje      |  Přirážka|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|U zákazníka            |                    |Přesčas                 |15     |
|             | Contoso India|Místní             |                    |Přesčas                 |10     |
|             | Contoso US   |Místní             |                    |Přesčas                 |20     |


Pokud zdroj ze společnosti Contoso India, jehož základní sazba je 100 USD, pracuje u zákazníka a zaznamenává do časového záznamu 8 hodin pravidelného času a 2 hodiny přesčasu, použije modul ocenění Project Service k zaznamenání 800 USD základní sazbu 100 za 8 hodin. Pro dobu 2 hodin přesčasové práce se na základní sazbu 100 použije přirážka ve výši 15 % pro získání jednotkové ceny 115 USD a zaznamenají se celkové náklady na 230 USD.

### <a name="applicable-to-cost"></a>Použitelné na náklady 
Pokud je toto nastaveno na **Ano**, znamená to, že hodnota dimenze ze vstupního kontextu by měla být použita ke spárování s **Cenou role** a **Přirážkou ceny role** při načítání sazeb nákladů a přirážky.

### <a name="applicable-to-sales"></a>Použitelné na prodej
Pokud je toto nastaveno na **Ano**, znamená to, že hodnota dimenze ze vstupního kontextu by měla být použita ke spárování s **Cenou role** a **Přirážkou ceny role** při načítání fakturační sazby a sazby přirážky.

### <a name="applicable-to-purchase"></a>Použitelné na nákup
Pokud je toto nastaveno na **Ano**, znamená to, že hodnota dimenze ze vstupního kontextu by měla být použita ke spárování s **Cenou role** a **Přirážkou ceny role** při načítání nákupní ceny. V současnosti služba Project Service nepodporuje scénáře subdodavatelů, takže toto pole není použito. 

### <a name="priority"></a>Priorita
Nastavení priority dimenze pomáhá službě Project Service při tvorbě ceny, a to i v případě, že nelze nalézt přesnou shodu mezi hodnotami vstupních dimenzí a hodnotami z tabulek **Cena role** nebo **Přirážka ceny role**. V tomto scénáři bude služba Project Service používat hodnoty null pro nespárované hodnoty dimenzí vážením dimenzí v pořadí podle jejich priority.

- **Priorita nákladů**: hodnota priority nákladů dimenze bude označovat váhu této dimenze při párování s nastavením nákladových cen. Hodnota **Priorita nákladů** musí být jedinečná v rámci dimenzí, které jsou **Použitelné na náklady**.
- **Priorita prodeje**: hodnota priority prodeje dimenze bude označovat váhu této dimenze při párování s nastavením prodejních cen nebo fakturačních sazeb. Hodnota **Priorita prodeje** musí být jedinečná v rámci dimenzí, které jsou **Použitelné na náklady**.
