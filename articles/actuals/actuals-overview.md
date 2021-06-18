---
title: Skutečné hodnoty
description: Tento téma poskytuje informace o tom, jak pracovat s aktuálními údaji v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996603"
---
# <a name="actuals"></a>Skutečné hodnoty 

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Skutečné hodnoty představují zkontrolovaný a schválený finanční a časový plán postupu v projektu. Jsou vytvářeny na základě schválení času, výdajů, záznamů o použití materiálu a záznamů faktur a deníku.

## <a name="journal-lines-and-time-submission"></a>Řádky deníku a časové záznamy

Další informace o časových záznamech najdete v části [Přehled časových záznamů](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Čas a materiál

Když je zadaný časový údaj propojen s projektem, který je namapován na řádek kontraktu času a materiálů, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.

### <a name="fixed-price"></a>Pevná cena

Při odeslání časového záznamu propojeného s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku pro náklady.

### <a name="default-pricing"></a>Výchozí cena

Logika pro vytváření výchozích cen je umístěna na řádku deníku. Hodnoty polí z časového záznamu jsou zkopírovány do řádku deníku. Tyto hodnoty obsahují datum transakce, řádek smlouvy, na který je projekt namapován, a výsledek měny v příslušném ceníku.

Pole, která ovlivňují výchozí ceny, jako jsou **Role** a **Jednotka prostředků** se používají k určení odpovídající ceny na řádku deníku. K časovému záznamu můžete přidat vlastní pole. Pokud chcete, aby se hodnota pole rozšířila na skutečné hodnoty, vytvořte pole v tabulkách **Skutečné hodnoty** a **Řádek deníku**. Pomocí vlastního kódu můžete šířit vybranou hodnotu pole z položky Zadání na Skutečné hodnoty prostřednictvím řádku deníku pomocí původů transakcí. Další informace o původu transakcí a propojení najdete v tématu [Propojení skutečných hodnot s původními záznamy](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Řádky deníku a zadávání základních výdajů

Další informace o záznamech o výdajích najdete v části [Přehled výdajů](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Čas a materiál

Když je zadaný záznam základního výdaje propojen s projektem, který je namapován na řádek kontraktu času a materiálů, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.

### <a name="fixed-price"></a>Pevná cena

Když je odeslaný záznam základního výdaje spojen s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku na náklad.

### <a name="default-pricing"></a>Výchozí cena

Logika pro zadávání výchozích cen výdajů je založena na kategorii výdajů. Datum transakce, řádek smlouvy, na který je projekt namapován, a měna jsou použity k určení příslušného ceníku. Pole, která ovlivňují výchozí ceny, jako jsou **Kategorie transakce** a **Jednotka prostředků** se používají k určení odpovídající ceny na řádku deníku. To však funguje pouze v případě, že cenová metoda v ceníku je **Cena za jednotku**. Pokud je způsob stanovení cen **Za cenu** nebo **Přirážka nad náklady**, pro náklady se použije cena zadaná při vytvoření položky výdajů a cena na řádku prodejního deníku se vypočítá na základě metody stanovení cen. 

K záznamu výdajů můžete přidat vlastní pole. Pokud chcete, aby se hodnota pole rozšířila na skutečné hodnoty, vytvořte pole v tabulkách **Skutečné hodnoty** a **Řádek deníku**. Pomocí vlastního kódu můžete šířit vybranou hodnotu pole z položky Zadání na Skutečné hodnoty prostřednictvím řádku deníku pomocí původů transakcí. Další informace o původu transakcí a propojení najdete v tématu [Propojení skutečných hodnot s původními záznamy](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Řádky deníku a odeslání protokolu o použití materiálu

Další informace o zadávání výdajů najdete v části [Protokol použití materiálu](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Čas a materiál

Když je zadaná položka protokolu o použití materiálu propojena s projektem, který je mapován na řádek smlouvy o čase a materiálech, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.

### <a name="fixed-price"></a>Pevná cena

Když je odeslaný záznam protokolu využití materiálu spojen s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku na náklad.

### <a name="default-pricing"></a>Výchozí cena

Logika pro zadání výchozích cen materiálu je založena na kombinaci produktu a jednotky. Datum transakce, řádek smlouvy, na který je projekt namapován, a měna jsou použity k určení příslušného ceníku. Pole, která ovlivňují výchozí ceny, jako jsou **ID produktu** a **Jednotka prostředků** se používají k určení odpovídající ceny na řádku deníku. To však funguje pouze u katalogových produktů. U produktů, které nejsou v katalogu, se pro náklady a prodejní cenu na řádcích deníku použije cena zadaná při vytvoření položky protokolu o použití materiálu. 

K záznamu **Protokol využití materiálu** můžete přidat vlastní pole. Pokud chcete, aby se hodnota pole rozšířila na skutečné hodnoty, vytvořte pole v tabulkách **Skutečné hodnoty** a **Řádek deníku**. Pomocí vlastního kódu můžete šířit vybranou hodnotu pole z položky Zadání na Skutečné hodnoty prostřednictvím řádku deníku pomocí původů transakcí. Další informace o původu transakcí a propojení najdete v tématu [Propojení skutečných hodnot s původními záznamy](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Použití deníků k zaznamenání nákladů

Deníky záznamů můžete použít a zaznamenávat náklady nebo výnosy do tříd materiálu, poplatků, času, výdajů nebo daňových transakcí. Deníky lze použít k následujícím účelům:

- Skutečné hodnoty transakcí z jiného systému je nutné přesunout do Microsoft Dynamics 365 Project Operations.
- Zaznamenejte náklady, ke kterým došlo v jiném systému. Tyto náklady mohou zahrnovat náklady na pořízení nebo subdodávky.

> [!IMPORTANT]
> Aplikace neověřuje typ řádku deníku ani související ceny, které jsou zadány na řádku deníku. Proto by měl k vytváření skutečných hodnot používat deníky pouze uživatel, který si je plně vědom účetního dopadu skutečných hodnot na projekt. Z důvodu dopadu tohoto typu deníku byste měli pečlivě zvolit, kdo má přístup k vytváření deníků záznamů.

## <a name="record-actuals-based-on-project-events"></a>Záznam skutečných hodnot na základě událostí projektu

Project Operations zaznamenává finanční transakce, které nastanou během projektu. Tyto transakce jsou zaznamenány jako skutečné hodnoty. V následujících tabulkách jsou zobrazeny různé typy skutečných hodnot, které jsou vytvořeny v závislosti na tom, zda je projekt časově materiálovým projektem nebo projektem s pevnou cenou, je v předprodejní fázi nebo jde o interní projekt.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Zdroj patří do stejné organizační jednotky jako smluvní jednotka projektu

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

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Zdroj patří do organizační jednotky, která se liší od smluvní jednotky projektu

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
