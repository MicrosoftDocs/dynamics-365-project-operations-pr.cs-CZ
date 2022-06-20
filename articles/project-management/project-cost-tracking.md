---
title: Sledování projektových nákladů
description: Tento článek poskytuje informace o tom, jak Project Operations sleduje průběh vůči mzdovým nákladům a výdajům na projekt.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c069a28c6dc546e5e632c4dff29686dc7965f23e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923732"
---
# <a name="labor-cost-tracking-on-projects"></a>Sledování pracovních nákladů na projektech

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations sleduje odhady pracovní síly a výdaje na nejnižší požadované úrovni členění v projektovém plánu. Finanční odhad pracovních nákladů je založen na plánovaném úsilí a obecných nebo pojmenovaných zdrojích, které jsou přiřazeny ke každému úkolu uzlu typu list v projektovém plánu. Když projekt začne a lidé začnou vykazovat čas strávený na různých projektových úkolech, jsou skutečné výdaje na práci shrnuty a začíná výpočet projekcí.

## <a name="labor-cost-tracking-view"></a>Zobrazení Sledování pracovních nákladů

Na stránce **Projekty** na kartě **Sledování** otevřete výběrem nabídky **Sledování** > **Náklady** zobrazení **Sledování nákladů**, kde uvidíte postup práce vynaložené na každý úkol v projektovém plánu. Tento pohled také porovnává skutečné pracovní náklady vynaložené na úkol s plánovanými pracovními náklady. Project Operations používá k výpočtu metrik pracovních nákladů následující vzorce:

- **Plánované náklady**: Odhadované náklady na všechna přiřazení zdrojů u každého úkolu uzlu typu list
- **Skutečné náklady**: Součet všech skutečných nákladů za čas zaznamenaný na úkolu
- **Procento spotřeby nákladů**: Skutečné náklady ÷ odhad nákladů při dokončení
- **Zbývající náklady**: Odhad nákladů při dokončení – skutečné náklady
- **Náklady při dokončení**: Zbývající náklady + skutečné náklady
- **Odchylka nákladů**: Plánované náklady – odhad nákladů při dokončení

U každého úkolu je zobrazen odhad odchylky nákladů. Pokud je odhad nákladů při dokončení větší než plánované náklady, předpokládá se, že úkol překročí rozpočet. Pokud je odhad nákladů při dokončení menší než plánované náklady, předpokládá se, že úkol nevyčerpá rozpočet.

>[!NOTE]
> Project Operations zobrazuje pouze pracovní náklady na stránce **Projekt** na kartě **Sledování**. I když materiály a výdaje lze odhadnout a sledovat jejich spotřebu, tyto náklady nejsou zahrnuty v nákladech uvedených na kartě **Sledování**. Tato karta je navržena tak, aby pouze opětovné promítala pracovní náklady na základě opětovného promítnutí úsilí.
Všechny zobrazené částky nákladů jsou převedeny na projektovou měnu nákladů z měny projektové ceny nákladů použité k určení míry nákladů. Měna nákladů projektu je měna smluvní jednotky projektu. Odhadované hodnoty nákladů za čas, které jsou uvedeny na kartě **Odhady** na stránce **Projekt**, nemusí přispívat k plánovaným nákladům na kartě **Sledování**. Důvodem tohoto rozdílu jsou rozdíly v tom, jak jsou odhadované náklady shrnuty v mřížce **Odhady** a způsobu výpočtu plánovaných nákladů v mřížce **Sledování**. 
>
> - **Karta Odhady** vypočítá odhadované náklady s použitím stejné měny sazby nákladů v ceníku. Poté se odhadovaná cena v měně ceníku převede na odhadovanou cenu v projektové měně nákladů. Odhadovaná cena v projektové měně se zobrazuje zaokrouhlená na 2 desetinná místa. Během tohoto převodu není nikdy použita přesnost měny. 
> - Na kartě **Sledování** dodržuje plánovaná kalkulace nákladů mírně odlišné pořadí výpočtu, které zahrnuje použití přesnosti měny ve dvou fázích: 
   ><ol>
   ><li>Odhadovaná částka nákladů v měně ceníku se převede na základní měnu (převod 1).</li>
   ><li>Odhadovaná částka nákladů v základní měně se převede na projektovou měnu nákladů (převod 2). </li>
   ></ol>
   >Přesnost měny se v obou krocích použije k získání plánovaných nákladů (na kartě **Sledování**), které se mírně odchylují od odhadovaných nákladů (v zobrazení **Časové uspořádání** na kartě **Odhady**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Přeprojektování nákladů u úkolů v uzlech typu list

Pracovní náklady u úkolu uzlu typu list nelze přímo promítnout na kartě **Sledování** na **stránce Projekt**. Můžete však použít zobrazení **Sledování úsilí** a v něm přeprojektovat zbývající úsilí na úkol. To způsobí přepočet zbývajících nákladů na úkol. Následuje popis toho, jak to funguje.

1. Manažer projektu může přeprojektovat úsilí uplatněné na úkoly aktualizací výchozí hodnoty v poli **Zbývající úsilí** za nový odhad zbývajícího úsilí na úkolu. Přeprojektování způsobí přepočet odhadu úsilí na úkol při dokončení (EAC), procenta pokroku a očekávané odchylky úsilí na úkolu. Rovněž se přepočítají hodnoty EAC, odhad do dokončení (ETC) a procento pokroku souhrnných úkolů, a vytvoří se nová projekce odchylky úsilí.
2. Na základě nové hodnoty zbývajícího úsilí na úkolu systém vypočítá zbývající náklady v zobrazení **Sledování nákladů**. Chcete-li vypočítat zbývající náklady na základě zbývajícího úsilí, systém nejprve vypočítá průměrné náklady na jednu hodinu úsilí na úkolu jako plánované náklady nebo plánované úsilí. Plánované náklady jsou součtem nákladů na všechna přiřazení zdrojů k úkolu. Průměrné náklady na hodinu se používají k výpočtu zbývajících nákladů u nově projektovaného zbývajícího úsilí na úkol.
3. Náklady při dokončení a procento spotřeby nákladů na úkol v uzlu typu list jsou přepočítány.
4. Přepočítají se hodnoty nákladů při dokončení souhrnných úkolů až ke kořenovému uzlu.

## <a name="reprojecting-costs-on-summary-tasks"></a>Přeprojektování nákladů u souhrnných úkolů

Projektové náklady můžete přeprojektovat u souhrnných úkolů nebo kontejnerových úkolů. Nemůžete však přímo přeprojektovat pracovní náklady u souhrnného projektového úkolu na kartě **Sledování** na stránce **Projekt**. Podobně jako u úkolů s uzly typu list lze reprojekce souhrnných a kontejnerových úkolů provádět v zobrazení **Sledování úsilí**. V tomto zobrazení můžete přeprojektovat zbývající úsilí na souhrnný úkol a vyvolat tak přepočet zbývajících nákladů na souhrnný úkol. Následuje popis toho, jak to funguje.

1. Manažer projektu může přeprojektovat úsilí uplatněné na souhrnné úkoly aktualizací výchozí hodnoty zbývajícího úsilí za nový odhad pro úkol. Tato aktualizace způsobí přepočet odhadu úsilí na souhrnný úkol při dokončení (EAC), procenta pokroku a očekávané odchylky úsilí na úkolu. Rovněž se přepočítají hodnoty EAC, ETC a procento pokroku souhrnných úkolů a vytvoří se nová projekce odchylky úsilí.
2. Na základě nové hodnoty zbývajícího úsilí na souhrnný úkol systém vypočítá zbývající náklady v zobrazení **Sledování nákladů**. Chcete-li vypočítat zbývající náklady na základě zbývajícího úsilí, systém nejprve vypočítá průměrné náklady na jednu hodinu úsilí na souhrnný úkol jako plánované náklady nebo plánované úsilí. Průměrné náklady na hodinu se používají k výpočtu nákladů u nově projektovaného zbývajícího úsilí na souhrnný úkol.
3. Náklady při dokončení a procento spotřeby nákladů na souhrnný úkol jsou přepočítány.
4. Nová hodnota nákladů při dokončení se na podřízené úkoly rozdělí ve stejném poměru jako původní plánované náklady úkolu.
5. Dojde k výpočtu nové hodnoty nákladů při dokončení u jednotlivých úkolů, až po úkoly uzlů typu list. Na základě této hodnoty budou u ovlivněných podřízených úkolů až do uzlů typu list přepočítány jejich zbývající náklady a procento spotřeby nákladů na základě hodnoty nákladů při dokončení. Výsledkem je nový odhad odchylky nákladů na úkol. 


Pole **Plnění nákladů** lze nastavit ze sledovacích údajů. Když je odchylka nákladů pro kořenový uzel v zobrazení **Sledování nákladů** záporná, můžete toto pole nastavit na **Nevyčerpaný rozpočet**. Když je odchylka nákladů pro kořenový uzel kladná, můžete tuto hodnotu nastavit na **Překročený rozpočet**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
