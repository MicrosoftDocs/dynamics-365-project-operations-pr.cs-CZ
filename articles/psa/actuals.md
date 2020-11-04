---
title: Přehled skutečných hodnot
description: Toto téma poskytuje informace o skutečných hodnotách projektu.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073978"
---
# <a name="actuals-overview"></a>Přehled skutečných hodnot

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Skutečné hodnoty jsou množství práce dokončené v projektu. Skutečné hodnoty projektu lze sledovat zpět do jejich zdrojových dokumentů. Tyto zdrojové dokumenty obsahují čas, výdaje, položky deníku a také faktury.

![Způsob sledování skutečných hodnot projektu do zdrojových dokumentů](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Odeslání časového záznamu.

V PSA se při odeslání časového záznamu pro projekt, který je namapovaný na řádek smlouvy s časem a materiálem, vytvoří dva řádky deníku. Jeden řádek je pro náklady a druhý řádek je pro nefakturované prodeje. Při odeslání časového záznamu pro projekt, který je namapovaný na řádek smlouvy s pevnou cenou, se vytvoří pouze řádek deníku pro náklady. 

Logika pro zadávání výchozích cen je umístěna na řádku deníku. Všechny hodnoty polí z časového záznamu jsou zkopírovány do řádku deníku. Tato pole obsahují datum transakce, řádek smlouvy, na který je projekt namapován, a výsledek měny v příslušném ceníku. 

Pole, která ovlivňují výchozí ceny, jako jsou **Role** a **Organizační jednotka** , způsobí, že ve výchozím nastavení bude do řádku deníku zadána odpovídající cena. Přidáte-li do časového záznamu vlastní pole a chcete, aby byla hodnota pole přenesena do skutečných hodnot, vytvořte v entitě Skutečnost pole a pomocí mapování polí zkopírujte pole z časového záznamu do skutečného záznamu.

## <a name="submitting-an-expense-entry"></a>Odeslání výdajové položky

V PSA se při odeslání výdajové položky pro projekt, který je namapovaný na řádek smlouvy s časem a materiálem, vytvoří dva řádky deníku. Jeden řádek je pro náklady a druhý řádek je pro nefakturované prodeje. Při odeslání výdajové položky pro projekt, který je namapovaný na řádek smlouvy s pevnou cenou, se vytvoří pouze řádek deníku pro náklady.

Logika pro zadávání výchozích cen pro výdaje je založena na kategorii výdajů, která je vybrána na stránce **Výdajová položka**. Datum transakce, řádek smlouvy, na který je projekt namapován, a měna jsou použity k určení příslušného ceníku. Avšak pro samotnou cenu je částka, kterou uživatel zadal, nastavena přímo na souvisejících výdajových řádcích deníku pro náklady a prodej ve výchozím nastavení.

V aktuální verzi PSA není k dispozici položka založená na kategoriích výchozích jednotkových cen na výdajových položkách.

## <a name="using-entry-journals-to-record-costs"></a>Použití deníků položek k zaznamenání nákladů

V PSA vám deníky položek umožňují zaznamenávat náklady nebo výnosy do tříd materiálu, poplatků, času, výdajů nebo daňových transakcí. Deník obsahuje hlavičku, řádky a akci **Potvrzení**. Zde jsou některé scénáře, ve kterých můžete použít deník:

- Do projektu je nutné zaznamenat skutečné náklady na materiál a prodej.
- Skutečné hodnoty transakcí z jiného systému je nutné přesunout na PSA.
- Je nutné zaznamenat náklady, které se vyskytly v jiném systému, například náklady na nákup nebo subdodavatele.

> [!IMPORTANT]
> Používání deníků položek k vytváření skutečných hodnot by měl provádět pouze uživatel, který si je plně vědom účetního dopadu skutečných hodnot na projekt. Důvodem je, že aplikace neověřuje typ řádku deníku nebo související ceny, které jsou zadány na řádku deníku. Vzhledem k dopadům tohoto typu deníku věnujte dostatečnou pozornost tomu, komu je povolen přístup k tvorbě vstupních časopisů.     


## <a name="recording-actuals-based-on-project-events"></a>Záznam skutečných hodnot na základě událostí projektu

PSA zaznamenává finanční transakce, které nastanou během projektu. Tyto transakce jsou zaznamenány jako **skutečné hodnoty**. V následujících tabulkách jsou zobrazeny různé typy skutečných hodnot, které jsou vytvořeny v závislosti na tom, zda je projekt časově materiálovým projektem nebo projektem s pevnou cenou, je v předprodejní fázi nebo jde o interní projekt.

**Zdroj patří do stejné organizační jednotky jako smluvní jednotka projektu**

<table>
<thead>
<tr>
<th rowspan="3">Událost</th>
<th colspan="4">Fakturovatelný nebo prodaný projekt</th>
<th rowspan="3">Projekt v předprodejní fázi</th>
<th rowspan="3">Interní projekt</th>
</tr>
<tr>
<th colspan="2">Čas a materiál</th>
<th colspan="2">Pevná cena</th>
</tr>
<tr>
<th>Skutečnost</th>
<th>Měna transakce</th>
<th>Pevná cena</th>
<th>Měna transakce</th>
</tr>
</thead>
<tbody>
<tr>
<td>Je vytvořen časový záznam,</td>
<td colspan="6">V entitě Skutečné hodnoty není žádná aktivita</td>
</tr>
<tr>
<td>Je odeslán časový záznam.</td>
<td colspan="6">V entitě Skutečné hodnoty není žádná aktivita</td>
</tr>
<tr>
<td rowspan="2">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</td>
<td>Skutečné náklady</td>
<td>Měna smluvní jednotky</td>
<td rowspan="2">Skutečné náklady</td>
<td rowspan="2">Měna smluvní jednotky
<td rowspan="2">Skutečné náklady</td>
<td rowspan="2">Skutečné náklady</td>
</tr>
<tr>
<td>Nefakturované skutečné prodeje – účtovatelné</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td rowspan="3">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</td>
<td>Skutečné náklady</td>
<td>Měna smluvní jednotky</td>
<td rowspan="3">Skutečné náklady</td>
<td rowspan="3">Měna smluvní jednotky</td>
<td rowspan="3">Skutečné náklady</td>
<td rowspan="3">Skutečné náklady</td>
</tr>
<tr>
<td>Skutečný nefakturovaný prodej – účtovatelný pro nové množství</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td>Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td rowspan="2">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</td>
<td>Storno nefakturovaného prodeje</td>
<td>Měna projektové smlouvy</td>
<td rowspan="2">Fakturovaný prodej pro milník</td>
<td rowspan="2">Měna projektové smlouvy</td>
<td rowspan="2">Nelze použít</td>
<td rowspan="2">Nelze použít</td>
</tr>
<tr>
<td>Fakturovaný prodej</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td rowspan="3">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</td>
<td>Storno nefakturovaného prodeje</td>
<td>Měna projektové smlouvy</td>
<td rowspan="3">Nelze použít</td>
<td rowspan="3">Nelze použít</td>
<td rowspan="3">Nelze použít</td>
<td rowspan="3">Nelze použít</td>
</tr>
<tr>
<td>Fakturovaný prodej – účtovatelný pro nové množství</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td>Fakturovaný prodej – neúčtovatelný pro rozdíl</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td rowspan="2">Faktura je opravena za účelem zvýšení účtovatelného množství.</td>
<td>Fakturovaný prodej – storno</td>
<td>Měna projektové smlouvy</td>
<td rowspan="5">
<ul>
<li>Storno fakturovaného prodeje pro milník</li>
<li>Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></li>
</ul>
</td>
<td rowspan="5">Měna projektové smlouvy</td>
<td rowspan="5">Nelze použít</td>
<td rowspan="5">Nelze použít</td>
</tr>
<tr>
<td>Fakturovaný prodej</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td rowspan="3">Faktura je opravena za účelem snížení účtovatelného množství.</td>
<td>Fakturovaný prodej – storno</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td>Fakturovaný prodej pro nové množství</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td>Nefakturovaný prodej – účtovatelný pro rozdíl</td>
<td>Měna projektové smlouvy</td>
</tr>
</tbody>
</table>

**Zdroj patří do organizační jednotky, která se liší od smluvní jednotky projektu**

<table>
<thead>
<tr>
<th rowspan="3">Událost</th>
<th colspan="4">Fakturovatelný nebo prodaný projekt</th>
<th rowspan="3">Projekt v předprodejní fázi</th>
<th rowspan="3">Interní projekt</th>
</tr>
<tr>
<th colspan="2">Čas a materiál</th>
<th colspan="2">Pevná cena</th>
</tr>
<tr>
<th>Skutečnost</th>
<th>Měna transakce</th>
<th>Pevná cena</th>
<th>Měna transakce</th>
</tr>
</thead>
<tbody>
<tr>
<td>Je vytvořen časový záznam,</td>
<td colspan="6">V entitě Skutečné hodnoty není žádná aktivita</td>
</tr>
<tr>
<td>Je odeslán časový záznam.</td>
<td colspan="6">V entitě Skutečné hodnoty není žádná aktivita</td>
</tr>
<tr>
<td rowspan="4">Čas je schválen a během schvalování nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</td>
<td>Skutečné náklady</td>
<td>Měna smluvní jednotky</td>
<td rowspan="4">Skutečné náklady</td>
<td rowspan="4">Měna smluvní jednotky</td>
<td rowspan="4">Skutečné náklady</td>
<td rowspan="4">Skutečné náklady</td>
</tr>
<tr>
<td>Nefakturované skutečné prodeje – účtovatelné</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td>Jednotkové náklady zdroje</td>
<td>Měna jednotky zdroje</td>
</tr>
<tr>
<td>Vnitropodnikový prodej</td>
<td>Měna smluvní jednotky</td>
</tr>
<tr>
<td rowspan="5">Čas je schválen a během schvalování dojde ke snížení fakturovatelných hodin.</td>
<td>Skutečné náklady</td>
<td>Měna smluvní jednotky</td>
<td rowspan="5">Skutečné náklady</td>
<td rowspan="5">Měna smluvní jednotky</td>
<td rowspan="5">Skutečné náklady</td>
<td rowspan="5">Skutečné náklady</td>
</tr>
<tr>
<td>Jednotkové náklady zdroje</td>
<td>Měna jednotky zdroje</td>
</tr>
<tr>
<td>Vnitropodnikový prodej</td>
<td>Měna smluvní jednotky</td>
</tr>
<tr>
<td>Skutečný nefakturovaný prodej – účtovatelný pro nové množství</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td>Skutečný nefakturovaný prodej – neúčtovatelný pro rozdíl</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td rowspan="2">Faktura je potvrzena a nedojde k žádným změnám nebo nárůstu fakturovatelných hodin.</td>
<td>Storno nefakturovaného prodeje</td>
<td>Měna projektové smlouvy</td>
<td rowspan="2">Fakturovaný prodej pro milník</td>
<td rowspan="2">Měna projektové smlouvy</td>
<td rowspan="2">Nelze použít</td>
<td rowspan="2">Nelze použít</td>
</tr>
<tr>
<td>Fakturovaný prodej</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td rowspan="3">Faktura je potvrzena a dojde ke snížení fakturovatelných hodin.</td>
<td>Storno nefakturovaného prodeje</td>
<td>Měna projektové smlouvy</td>
<td rowspan="3">Nelze použít</td>
<td rowspan="3">Nelze použít</td>
<td rowspan="3">Nelze použít</td>
<td rowspan="3">Nelze použít</td>
</tr>
<tr>
<td>Fakturovaný prodej – účtovatelný pro nové množství</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td>Fakturovaný prodej – neúčtovatelný pro rozdíl</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td rowspan="2">Faktura je opravena za účelem zvýšení účtovatelného množství.</td>
<td>Fakturovaný prodej – storno</td>
<td>Měna projektové smlouvy</td>
<td rowspan="5">
<ul>
<li>Storno fakturovaného prodeje pro milník</li>
<li>Změna stavu milníku z <strong>fakturováno</strong> na <strong>Připraveno pro fakturu</strong></li>
</ul>
</td>
<td rowspan="5">Měna projektové smlouvy</td>
<td rowspan="5">Nelze použít</td>
<td rowspan="5">Nelze použít</td>
</tr>
<tr>
<td>Fakturovaný prodej</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td rowspan="3">Faktura je opravena za účelem snížení účtovatelného množství.</td>
<td>Fakturovaný prodej – storno</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td>Fakturovaný prodej pro nové množství</td>
<td>Měna projektové smlouvy</td>
</tr>
<tr>
<td>Nefakturovaný prodej – účtovatelný pro rozdíl</td>
<td>Měna projektové smlouvy</td>
</tr>
</tbody>
</table>
