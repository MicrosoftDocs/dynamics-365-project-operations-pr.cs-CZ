---
title: Projektové náklady a výnosy
description: Toto téma obsahuje informace o odhadování projektových nákladů a výnosů.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fe51af8adb7c3831a57494b8359def2a0176b552efe16feb53a2a265f5ffcb0c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002548"
---
# <a name="project-costs-and-revenue"></a>Projektové náklady a výnosy

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektové odhady poskytují finanční přehled odhadované a plánované práce v plánu projektu. Karta **Odhady** na stránce **Projekty** zobrazuje dopad nákladů a výnosů plánované práce. Poskytuje také informace o mnoha předdefinovaných dimenzích. 

> ![Karta Odhady.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Nákladová a prodejní hodnota projektu

Ceníky definují nákladovou a fakturační sazbu pro role v projektu. Na základě rolí spojených s názvem pozice a pojmenovaným zdrojem přiřazeným k úkolu můžete určit dopad nákladů a výnosů práce. Pokud existují úkoly, které nemají přiřazení (obecné nebo pojmenované), nelze získat odhady nákladů nebo prodejů. Hodnoty nákladů a prodeje berou v úvahu datum, které je definováno v ceníku.

### <a name="default-cost-price"></a>Výchozí nákladová cena  

Každý projekt patří k organizaci. Tato organizace je uvedena v poli **Smluvní jednotka** v projektu. Ceník, který je přidružený ke smluvní jednotce, se používá k určení jednotkové nákladové ceny. Chcete-li u rolí určit správné nákladové ceny pro datum, které je definováno na řádcích odhadu, hledejte v nákladovém ceníku kombinaci role, jednotky a organizační jednotky. 

Aby bylo možné jejich nákladové ceny vypočítat, musí být ke zdroji přiřazeny všechny úkoly. Jakékoli nepřiřazené úkoly budou mít nákladovou cenu 0,00.

Pokud kombinace role, jednotky a organizační jednotky nevrátí nákladovou cenu z ceníku smluvní jednotky, systém jednotku ignoruje. Místo toho vyhledává kombinaci pouze role a organizační jednotky. Pokud je nákladová cena nalezena, použijí se k jejímu převodu na jednotku, kterou jste vybrali na řádku odhadu, koeficienty převodu.

Pokud kombinace role, jednotky a organizační jednotky nevrátí nákladovou cenu, systém organizační jednotku ignoruje. Místo toho hledá kombinaci role a jednotky k nastavení výchozí ceny (po použití jakéhokoli převodu).

Pokud systém nenajde cenu pro roli, nastaví se nákladová cena na řádku odhadu na výchozí hodnotu **0,00**. Všechny částky nákladů na řádcích odhadu nákladů projektu jsou zaznamenány v měně smluvní jednotky.

> [!NOTE]
> Microsoft Dynamics 365 ve výchozím nastavení ukládá částky nákladů v základní měně. Částky nákladů, které jsou zobrazeny na kartě **Odhady**, jsou však v měně smluvní jednotky.  

### <a name="default-sales-price"></a>Výchozí prodejní cena 

Prodejní ceník je určen buď prodejní entitou, ke které je projekt připojen, nebo zákazníkem projektu. Pokud je prodejní entita, například příležitost, nabídka nebo smlouva, přidružena k projektu, je prodejní cena prodejní entity určena ceníkem, který je spojen s nabídkou nebo smlouvou. Pokud má nabídka nebo smlouva vlastní ceník, tak se tento ceník použije jako výchozí prodejní ceník pro odhady projektu. Pokud neexistuje žádné spojení s prodejními entitami, použije se jako výchozí prodejní ceník prodejní ceník z parametrů, který odpovídá měně zákazníka definované v projektu.

Každý řádek odhadu obsahuje jednotku zdroje, která je k němu přidružena. Jednotka zdroje označuje organizační jednotku, ze které jsou zdroje pro dokončení úkolu rezervovány. Chcete-li určit prodejní cenu přidružených rolí, vyhledejte kombinaci role, jednotky, jednotky zdroje v prodejním ceníku. Pokud pro úkol neexistují žádná přiřazení, prodejní cena pro tento úkol je 0,00.

Pokud kombinace role, jednotky a jednotky zdroje nevrátí prodejní cenu z prodejního ceníku, systém jednotku ignoruje. Místo toho vyhledává kombinaci pouze role a jednotky zdroje. Pokud je prodejní cena nalezena, použijí se k jejímu převodu na jednotku, kterou jste vybrali na řádku odhadu prodeje, koeficienty převodu. 

Pokud kombinace role a jednotky zdroje nevrátí prodejní cenu z prodejního ceníku, systém jednotku zdroje ignoruje. Místo toho hledá kombinaci role a jednotky k nastavení výchozí ceny (po použití jakéhokoli převodu).

Pokud systém nenajde cenu pro roli, nastaví se prodejní cena na řádku odhadu na výchozí hodnotu **0,00**.

Karta **Odhady** obsahuje tabulkové zobrazení, které zobrazuje řádky odhadu. Mřížka obsahuje sloupce pro jednotku, celkovou nákladovou cenu a celkovou prodejní cenu, jak je znázorněno na následujícím obrázku. 

> ![Zobrazení mřížky na kartě Odhady.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Zobrazení časového uspořádání odhadů projektu

Zobrazení odhadů projektu s časovým uspořádáním zobrazuje data odhadu ze zobrazení mřížky na časové ose v časovém měřítku, které vyberete. Ve výchozím nastavení jsou data odhadu uspořádána dle dimenze **Role**.

> ![Zobrazení časového uspořádání odhadů projektu.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Přidělení odhadu úsilí na základě režimu úkolu

V zobrazení časového uspořádání je celkové úsilí odhadované pro úkol distribuováno přidělením hodin úsilí na jednotku časového období ve zvoleném časovém měřítku. Režim úkolu určuje, jak bude úsilí přiděleno v rámci celé doby trvání úkolu. Používají se dva druhy přidělení – **Rovnoměrné** a **Na základě pracovní doby**.

### <a name="work-hours-based-allocation"></a>Přidělení na základě pracovní doby
 
V režimu automatického plánování jsou denní výchozí hodiny pro zdroje úkolů nastaveny na celou pracovní hodinovou sazbu. Toto chování platí při přidělování úsilí jeho rozdělením na celou dobu trvání úkolů v zobrazení časového uspořádání. Pokud například odhadnete, že úkol dokončí jeden zdroj v časovém měřítku **Den**, tak úsilí, které je přiděleno na den, nesmí přesáhnout pracovní dobu za den, která je definována v projektovém kalendáři. Proto přidělení úsilí vždy zajišťuje odhad, že prostředky budou využity po celý den.

### <a name="even-allocation"></a>Rovnoměrné přidělení

V režimu ručního plánování úkolu není použita pracovní doba z projektového kalendáře. Plán úkolu je místo toho založen na zadání uživatele. Pro tyto úkoly nemá přidělení úsilí na jednotku časového období ve zvoleném časovém měřítku žádné omezující faktory. Celkové úsilí úkolu je rovnoměrně rozděleno a přiděleno pro každou jednotku časového období ve zvoleném časovém měřítku. Proto režim úkolu definovaný v úkolu určuje rozdělení úsilí nebo přidělení úsilí na jednotku časového období v časovém uspořádání odhadů.

## <a name="grouping-and-time-phasing-options"></a>Možnosti seskupení a časového uspořádání

Časově uspořádané zobrazení zobrazuje rozložení odhadů úsilí, nákladů a prodeje za den, týden, měsíc nebo rok. Ve výchozím nastavení jsou data odhadu uspořádána dle dimenze **Role**. Pomocí možnosti **Seskupit podle** však můžete kontingenční tabulky použít u dvou dalších dimenzí: **Kategorie** a **Zdroj**.

V zobrazení tabulky i v zobrazení časového uspořádání můžete vybrat, která pole budou zobrazena. Součty pro každý časový blok jsou zobrazeny v dolní části projektu. Zobrazují celkové odhadované úsilí, náklady a prodej za den, týden, měsíc nebo rok. Výchozí nákladová cena a prodejní cena jsou platné podle data. Jinými slovy, pro každý zdroj se změní na základě časově uspořádaného zobrazení, které jste vybrali.

## <a name="expense-estimates"></a>Odhady výdajů

Tlačítko **Přidat nový odhad výdajů** v zobrazení tabulky umožňuje zaznamenat veškeré výdaje vzniklé v projektu, které však nesouvisejí přímo s prací. Můžete zaznamenat odhady výdajů pro určitý úkol nebo pro celý projekt. Vyberte kategorie výdajů a nezávazné datum očekávaného vzniku výdaje. Pokud přidružené nákladové a prodejní ceníky obsahují výchozí ceny (nebo pokud jsou procenta přirážky definována pro kategorie výdajů), budou automaticky zadány na řádku odhadu při vzniku přidružení.


[!INCLUDE[footer-include](../includes/footer-banner.md)]