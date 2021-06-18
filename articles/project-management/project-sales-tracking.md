---
title: Sledování projektových prodejů
description: Tento téma poskytuje informace o tom, jak Project Operations sleduje vývoj pracovních výnosů u projektu.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f9873dc3e709453a56cb53273b35cc1cd312127
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996963"
---
# <a name="project-sales-tracking"></a>Sledování projektových prodejů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations sleduje odhady pracovní síly a výnosy na nejnižší požadované úrovni členění v projektovém plánu. Finanční odhad pracovních výnosů je založen na plánovaném úsilí a obecných nebo pojmenovaných zdrojích, které jsou přiřazeny ke každému úkolu uzlu typu list v projektovém plánu. Když projekt začne a lidé začnou vykazovat čas strávený na různých projektových úkolech, jsou skutečné výnosy na práci shrnuty a začíná výpočet projekcí.

## <a name="labor-revenue-tracking-view"></a>Zobrazení Sledování pracovních výnosů

Na stránce **Projekty** na kartě **Sledování** můžete výběrem nabídky **Sledování** > **Náklady** otevřít zobrazení **Sledování nákladů**. Nebo můžete výběrem nabídky **Použití** > **Fakturační sazba** otevřít zobrazení **Sledování výnosů**, které ukazuje vývoj pracovních výnosů u každého úkolu v projektovém plánu. Tento pohled také porovnává skutečné pracovní výnosy získanými u úkolu s plánovanými pracovními výnosy. Project Operations používá k výpočtu metrik pracovních výnosů následující vzorce:

- **Plánované výnosy**: Odhadované hodnoty prodejů na všechna přiřazení zdrojů u každého úkolu uzlu typu list
- **Skutečné výnosy**: Součet všech nefakturovaných skutečných prodejů za čas zaznamenaný na úkolu
- **Procento fakturovatelných výnosů**: Skutečné výnosy ÷ odhadované výnosy při dokončení
- **Zbývající výnosy**: Odhadované výnosy při dokončení – skutečné výnosy
- **Odhadované výnosy při dokončení**: Zbývající výnosy + skutečné výnosy
- **Odchylka výnosů**: Plánované výnosy – odhadované výnosy při dokončení


> [!NOTE]
> Project Operations zobrazuje pouze pracovní výnosy na stránce **Projekt** na kartě **Sledování**. I když materiály a výdaje lze odhadnout a sledovat jejich spotřebu, tyto výnosy nejsou zahrnuty ve výnosech uvedených na kartě **Sledování**. Tato karta je navržena tak, aby pouze přeprojektovala pracovní výnosy na základě přeprojekce úsilí.  
> Všechny zobrazené částky výnosů jsou převedeny na měnu nákladů projektu. Měna nákladů projektu je měna smluvní jednotky projektu. U projektů s pevnou cenou nejsou čísla výnosů v zobrazení **Sledování pracovních výnosů** relevantní, protože nevyfakturované skutečné prodeje se nezaznamenávají po schválení časových záznamů.
> Odhadované hodnoty prodeje za časové záznamy, které jsou uvedeny na kartě **Odhad** projektu nemusí přispívat k hodnotě plánovaných výnosů na kartě **Sledování**. Tato nesrovnalost je způsobena dvěma možnými důvody:
><ol>
   ><li> Karta <b>Odhady</b> zobrazuje odhadované výnosy v měně prodeje, zatímco karta <b>Sledování</b> zobrazuje plánované výnosy převedené na měnu nákladů. </li>
   ><li> Když jsou odhadované prodeje převedeny na smluvní měnu, jak je uvedeno na kartě <b>Odhady</b>, zahrnuje převod na projektovou měnu kroky, které by mohly vést ke ztrátě přesnosti: </li>
><ol>
><li> Odhadovaná částka prodejů ve smluvní měně se nejprve převede na základní měnu (převod 1).</li>
><li> Odhadovaná částka prodejů v základní měně se převede na projektovou měnu nákladů (převod 2). </li>
></ol>
></ol>
> Přesnost měny se aplikuje v obou krocích, což má za následek odchylku plánovaného výnosu v měně projektu od plánovaného prodeje ve smluvní měně.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Přeprojektování výnosů u úkolů v uzlech typu list

Pracovní výnosy u úkolu uzlu typu list nelze přímo promítnout na kartě **Sledování** na stránce **Projekt**. Můžete však použít zobrazení **Sledování úsilí** a v něm přeprojektovat zbývající úsilí na úkol. To způsobí přepočet zbývajících výnosů na úkol. Následuje popis toho, jak to funguje.

1. Manažer projektu může přeprojektovat úsilí uplatněné na úkoly aktualizací výchozí hodnoty v poli **Zbývající úsilí** za nový odhad zbývajícího úsilí na úkolu. Přeprojektování způsobí přepočet odhadu úsilí na úkol při dokončení (EAC), procenta pokroku a očekávané odchylky úsilí na úkolu. Rovněž se přepočítají hodnoty EAC, odhad do dokončení (ETC) a procento pokroku souhrnných úkolů, a vytvoří se nová projekce odchylky úsilí.
2. Na základě nové hodnoty zbývajícího úsilí na úkolu systém vypočítá zbývající výnosy v zobrazení **Sledování výnosů**. Chcete-li vypočítat zbývající výnosy na základě zbývajícího úsilí, systém nejprve vypočítá průměrné výnosy na jednu hodinu úsilí na souhrnný úkol jako plánované výnosy nebo plánované úsilí. Plánované jsou součtem výnosů na všechna přiřazení zdrojů k úkolu. Průměrné výnosy na hodinu se používají k výpočtu zbývajících výnosů u nově projektovaného zbývajícího úsilí na úkol.
3. Odhadované výnosy při dokončení a procento spotřeby výnosů na úkol v uzlu typu list jsou přepočítány.
4. Přepočítají se hodnoty výnosů při dokončení souhrnných úkolů až ke kořenovému uzlu.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Přeprojektování výnosů u souhrnných úkolů

Projektové výnosy můžete přeprojektovat u souhrnných úkolů nebo kontejnerových úkolů. Nemůžete však přímo přeprojektovat pracovní výnosy u souhrnného projektového úkolu na kartě **Sledování** na stránce **Projekt**. Podobně jako u úkolů s uzly typu list lze reprojekce souhrnných a kontejnerových úkolů provádět v zobrazení **Sledování úsilí**. V tomto zobrazení můžete přeprojektovat zbývající úsilí na souhrnný úkol a vyvolat tak přepočet zbývajících výnosů na souhrnný úkol. Následuje popis toho, jak to funguje.

1. Manažer projektu může přeprojektovat úsilí uplatněné na úkoly aktualizací výchozí hodnoty v poli **Zbývající úsilí** za nový odhad **zbývajícího úsilí** na úkolu. Přeprojektování způsobí přepočet odhadu úsilí na úkol při dokončení (EAC), procenta pokroku a očekávané odchylky úsilí na úkolu. Rovněž se přepočítají hodnoty EAC, ETC a procento pokroku souhrnných úkolů a vytvoří se nová projekce odchylky úsilí.
2. Na základě nové hodnoty v poli **Zbývající úsilí** na úkolu systém vypočítá zbývající výnosy v zobrazení **Sledování výnosů**. Chcete-li vypočítat zbývající výnosy na základě zbývajícího úsilí, systém nejprve vypočítá průměrné výnosy na jednu hodinu úsilí na souhrnný úkol jako plánované výnosy nebo plánované úsilí. Plánované jsou součtem výnosů na všechna přiřazení zdrojů k úkolu. Tento průměrný výnos na hodinu se poté použije k výpočtu výnosů u nově projektovaného zbývajícího úsilí na úkol.
3. Odhadované výnosy při dokončení a procenta spotřeby výnosů u souhrnného úkolu jsou přepočítány.
4. Nová hodnota odhadovaných výnosů při dokončení se na podřízené úkoly rozdělí ve stejném poměru jako původní plánované výnosy úkolu.
5. Dojde k výpočtu nových odhadovaných výnosů nákladů při dokončení u jednotlivých úkolů, až po úkoly uzlů typu list. Na základě této hodnoty budou u ovlivněných podřízených úkolů až do uzlů typu list přepočítány jejich zbývající výnosy a procento spotřeby výnosů na základě hodnoty výnosů při dokončení. Výsledkem je nový odhad odchylky výnosů na úkol. 
6. Přepočítají se hodnoty výnosů při dokončení souhrnných úkolů až ke kořenovému uzlu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

