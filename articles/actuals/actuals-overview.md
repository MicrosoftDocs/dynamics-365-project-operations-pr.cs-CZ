---
title: Skutečné hodnoty
description: Tento téma poskytuje informace o práci se skutečnými hodnotami v Microsoft Dynamics 365 Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073770"
---
# <a name="actuals"></a>Skutečné hodnoty 

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Skutečné hodnoty jsou množství práce dokončené v projektu. Jsou vytvářeny jako výsledek časových a výdajových záznamů, záznamů deníku a faktur.

## <a name="journal-lines-and-time-submission"></a>Řádky deníku a časové záznamy

Další informace o časových záznamech najdete v části [Přehled časových záznamů](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Čas a materiál

Když je zadaný časový údaj propojen s projektem, který je namapován na řádek kontraktu času a materiálů, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.

### <a name="fixed-price"></a>Pevná cena

Při odeslání časového záznamu propojeného s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku pro náklady.

### <a name="default-pricing"></a>Výchozí cena

Logika pro vytváření výchozích cen je umístěna na řádku deníku. Hodnoty polí z časového záznamu jsou zkopírovány do řádku deníku. Tyto hodnoty obsahují datum transakce, řádek smlouvy, na který je projekt namapován, a výsledek měny v příslušném ceníku.

Pole, která ovlivňují výchozí ceny, jako jsou **Role** a **Organizační jednotka** se používají k tomu, aby byla do řádku deníku zadána odpovídající cena. K časovému záznamu můžete přidat vlastní pole. Pokud chcete, aby byla hodnota pole přenesena do skutečných hodnot, vytvořte v entitě Skutečnost pole a pomocí mapování polí zkopírujte pole z časového záznamu do skutečného záznamu.

## <a name="journal-lines-and-basic-expense-submission"></a>Řádky deníku a zadávání základních výdajů

Další informace o záznamech o výdajích najdete v části [Přehled výdajů](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Čas a materiál

Když je zadaný záznam základního výdaje propojen s projektem, který je namapován na řádek kontraktu času a materiálů, systém vytvoří dva řádky deníku, jeden pro náklady a druhý pro nevyfakturované prodeje.

### <a name="fixed-price"></a>Pevná cena

Při odeslání základního záznamu o výdajích propojeného s projektem, který je namapovaný na řádek smlouvy s pevnou cenou, systém vytvoří jeden řádek deníku pro náklady.

### <a name="default-pricing"></a>Výchozí cena

Logika pro zadávání výchozích cen výdajů je založena na kategorii výdajů. Datum transakce, řádek smlouvy, na který je projekt namapován, a měna jsou použity k určení příslušného ceníku. Avšak ve výchozím nastavení je zadaná částka pro samotnou cenu nastavena přímo na souvisejících výdajových řádcích deníku pro náklady a prodej ve výchozím nastavení.

Položka založená na kategoriích výchozích jednotkových cen na výdajových položkách.

## <a name="use-entry-journals-to-record-costs"></a>Použití deníků k zaznamenání nákladů

Deníky záznamů můžete použít a zaznamenávat náklady nebo výnosy do tříd materiálu, poplatků, času, výdajů nebo daňových transakcí. Deníky lze použít k následujícím účelům:

- Záznam skutečných nákladů na materiál a prodej projektu.
- Přesunout dkutečné hodnoty transakcí z jiného systému do Microsoft Dynamics 365 Project Operations.
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
