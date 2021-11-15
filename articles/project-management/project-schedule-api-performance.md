---
title: Výkon rozhraní API projektového plánu
description: Toto téma poskytuje informace o výkonnostních testech API Plánu projektu a identifikuje nejlepší postupy pro optimální využití.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a1abadbae044ccbd40077c6937262f0f17387bad
ms.sourcegitcommit: 5c536cf05e2cbfc1d15982e4695d726064a074da
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2021
ms.locfileid: "7750594"
---
# <a name="project-schedule-api-performance"></a>Výkon rozhraní API projektového plánu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / neskladových položkých, nasazení Lite – řeší proforma fakturaci, Project for the Web_

Toto téma poskytuje informace o výkonnostních testech rozhraní API Plánu projektu a identifikuje nejlepší postupy pro optimální využití.

## <a name="project-scheduling-service"></a>Služba Plánování projektů
Služba Plánování projektů je služba pro více klientů, která běží v Microsoft Azure. Je navržena tak, aby zlepšila interakci poskytováním rychlého a plynulého zážitku, když uživatelé pracují na projektech. Tohoto zlepšení je dosaženo přijetím požadavků na změny, jejich zpracováním a následným okamžitým vrácením výsledku. Služba asynchronně uchovává data v Dataverse a nebrání uživateli provádět další operace.

Rozhraní API Plánu projektu spoléhají na službu Plánování projektů, která spouští požadavky, které jsou podrobněji popsány v dalších částech tohoto tématu.

Rozhraní API Plánu projektu jsou navržena tak, aby fungovala s následujícími entitami strukturovaného rozpisu prací (WBS):

  - Project
  - Projektový úkol
  - Závislost projektového úkolu
  - Člen projektového týmu
  - Přiřazení zdroje
  
Podporována jsou jak přednastavená, tak vlastní pole. Pokud není uvedeno jinak, jsou podporovány všechny běžné operace, jako je vytváření, aktualizace a odstraňování. Více informací najdete v tématu [Používání rozhraní API Plánu projektu k provádění operací a plánování entit](schedule-api-preview.md).

Jako součást rozhraní API Plánu projektu byl přidán vzor pracovní jednotky. Tento vzor je známý jako OperationSet (sada operací) a lze jej použít, když musí být v jedné transakci zpracováno několik požadavků.

Následující obrázek ukazuje tok, se kterým se partner setká při použití této funkce.

![Dataverse a tok služby Plánování projektů.](./media/dataverse-project-scheduling-service-flow.png)

**Krok 1**: Klient spustí volání API koncového bodu protokolu Open Data Protocol (OData) v Dataverse a vytvoří OperationSet.

**Krok 2**: Po vytvoření nového OperationSet je vrácena hodnota **OperationSetId**.

**Krok 3**: Klient použije hodnotu **OperationSetId** k vytvoření dalšího požadavku API Plánu projektu. Výsledkem je požadavek na vytvoření, aktualizaci nebo odstranění entity plánování. Po vytvoření tohoto požadavku se provede ověření metadat. Pokud ověření selže, požadavek je ukončen a je vrácena chyba.

**Kroky 4a–4c**: Tyto kroky představují fázi ACCEPT (přijetí). Klient volá rozhraní API **ExecuteOperationSetV1**, které odesílá všechny změny do služby Plánování projektů v jedné dávce. Služba Plánování projektu spouští vlastní ověření požadavků v dávce. Jakékoli selhání ověření zruší dávku a vrátí výjimku volajícímu. Pokud je dávka úspěšně přijata službou Plánování projektu, stav OperationSet se aktualizuje tak, aby odrážel skutečnost, že OperationSet je zpracovávána službou Plánování projektu.

**Krok 5**: Tento krok představuje fázi PERSIST (trvale uložit). Služba Plánování projektu asynchronně zapíše v transakci dávku do Dataverse. Pokud je operace zápisu úspěšná, je sada OperationSet označena jako **Dokončeno**. Jakékoli chyby vrátí transakci a dávku zpět a OperationSet je označena jako **Selhání**.

## <a name="performance-methodology"></a>Metodika měření výkonu
Doba provedení je definována jako doba od volání operace **ExecuteOperationSetV1** API do doby, kdy služba Plánování projektů dokončí zápis do Dataverse. Všechny operace proběhnou dohromady 2200krát a vykazována jsou měření doby provádění P99. Měří se operace s jedním záznamem a hromadné operace.

U operace s jedním záznamem obsahuje OperationSet jeden požadavek. U hromadných operací obsahuje 20, 50 nebo 100 požadavků. Každá velikost dávky se vykazuje samostatně.

Tyto operace běží na nasazení UR 15 Project Operations Lite v Severní Americe.

## <a name="results"></a>Výsledky
### <a name="create-operations"></a>Operace vytváření
#### <a name="single-record-create-operations"></a>Operace vytváření jednoho záznamu
Následující tabulka ukazuje doby provádění při vytvoření jednoho záznamu. Časy jsou v sekundách.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Typ&nbsp;&nbsp;&nbsp;záznamu</th>
    <th class="tg-0lax" colspan="2">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax">Povinná pole</th>
    <th class="tg-0lax">Všechna podporovaná pole</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Úloha</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Přiřazení</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Člen týmu</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Závislost</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operace hromadného vytváření
Následující tabulka ukazuje doby provádění při vytvoření více záznamů. Microsoft konkrétně měřil doby provádění při vytváření 20, 50 a 100 záznamů v jedné OperationSet. Časy jsou v sekundách.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Typ&nbsp;&nbsp;&nbsp;záznamu</th>
    <th class="tg-0lax" colspan="6">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 záznamů</th>
    <th class="tg-0lax" colspan="2">50 záznamů</th>
    <th class="tg-0lax" colspan="2">100 záznamů</th>
  </tr>
  <tr>
    <th class="tg-0lax">Povinná pole</th>
    <th class="tg-0lax">Všechna podporovaná pole</th>
    <th class="tg-0lax">Povinná pole</th>
    <th class="tg-0lax">Všechna podporovaná pole</th>
    <th class="tg-0lax">Povinná pole</th>
    <th class="tg-0lax">Všechna podporovaná pole</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Úloha</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Přiřazení</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Závislost</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Operace hromadného vytváření na entitách **Projekt** a **Člen týmu** nejsou v této tabulce obsaženy, protože modul runtime pro tyto operace se podobá modulu runtime, kdy je API pro vytvoření jednoho záznamu voláno vícekrát. Tato rozhraní API se spouštějí okamžitě v Dataverse.

Následující obrázek ukazuje graf časů provádění pro entity **Úkol**, **Přiřazení** a **Závislost**, kdy je vytvořeno 20, 50 a 100 záznamů a jsou použita všechna podporovaná pole.

![Graf doby provádění vytvoření záznamů.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operace aktualizace
#### <a name="single-record-update-operations"></a>Operace aktualizace jednoho záznamu
Následující tabulka ukazuje doby provádění při aktualizaci jednoho záznamu. Časy jsou v sekundách.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Typ&nbsp;&nbsp;&nbsp;záznamu</th>
    <th class="tg-0lax" colspan="2">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax">Povinná pole </th>
    <th class="tg-0lax">Všechna podporovaná pole</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Úloha</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Člen týmu</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operace aktualizace entit **Přiřazení zdrojů** a **Závislost projektového úkolu** nejsou podporovány.

#### <a name="bulk-update-operations"></a>Operace hromadné aktualizace
Následující tabulka ukazuje doby provádění při aktualizaci více záznamů. Microsoft konkrétně měřil doby provádění při aktualizaci 20, 50 a 100 záznamů v jedné OperationSet. Časy jsou v sekundách.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Typ&nbsp;&nbsp;&nbsp;záznamu</th>
    <th class="tg-0lax" colspan="6">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 záznamů</th>
    <th class="tg-0lax" colspan="2">50 záznamů</th>
    <th class="tg-0lax" colspan="2">100 záznamů</th>
  </tr>
  <tr>
    <th class="tg-0lax">Povinná pole</th>
    <th class="tg-0lax">Všechna podporovaná pole</th>
    <th class="tg-0lax">Povinná pole</th>
    <th class="tg-0lax">Všechna podporovaná pole</th>
    <th class="tg-0lax">Povinná pole</th>
    <th class="tg-0lax">Všechna podporovaná pole</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Úloha</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Člen týmu</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operace aktualizace entit **Přiřazení zdrojů** a **Závislost projektového úkolu** nejsou podporovány.

Následující obrázek ukazuje graf časů provádění pro entity Úkol a Člen týmu, kdy je aktualizováno 20, 50 a 100 záznamů a jsou použita všechna podporovaná pole.

![Graf doby provádění aktualizace záznamů.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operace odstranění
#### <a name="single-record-delete-operations"></a>Operace odstranění jednoho záznamu
Následující tabulka ukazuje doby provádění při odstranění jednoho záznamu. Časy jsou v sekundách.

| Typ záznamu | Čas  |
|-------------|-------|
| Úloha        | 20.12 |
| Přiřazení  | 10.86 |
| Člen týmu | 12.52 |
| Závislost  | 20.89 |

> [!NOTE]
> Operace odstranění entit **Projekt** nejsou podporovány.

#### <a name="bulk-delete-operations"></a>Operace hromadného odstranění
Následující tabulka ukazuje doby provádění při odstranění více záznamů. Microsoft konkrétně měřil doby provádění při odstranění 20, 50 a 100 záznamů v jedné OperationSet. Časy jsou v sekundách.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Typ&nbsp;&nbsp;&nbsp;záznamu</th>
    <th class="tg-0lax" colspan="3">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 záznamů</th>
    <th class="tg-0lax">50 záznamů</th>
    <th class="tg-0lax">100 záznamů</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Úloha</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Přiřazení</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Člen týmu</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Závislost</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operace odstranění entit **Projekt** nejsou podporovány.

Následující obrázek ukazuje graf časů provádění pro entity **Úkol**, **Přiřazení**, **Člen týmu** a **Závislost**, kdy je odstraněno 20, 50 a 100 záznamů.

![Graf doby provádění odstranění záznamů.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Postřehy
U každé operace záznamu trvá operaci **ExecuteOperationSet** rozhraní API asi 800 milisekund, než odešle požadavek službě Plánování projektu. Službě Plánování projektu pak trvá asi pět sekund, než zpracuje datovou část a volá Dataverse. Zbytek doby provádění je spuštěna obchodní logika a zápis dat do databáze v Dataverse.

Když je vytvořeno, aktualizováno nebo odstraněno 100 záznamů, trvá operaci **ExecuteOperationSet** rozhraní API asi tři sekundy, než odešle požadavek do služby Plánování projektu. Službě Plánování projektu pak trvá asi pět sekund, než zpracuje požadavky a volá Dataverse. Hromadné operace musí jednorázově zaplatit **daň služby Plánování projektů** pro všechny záznamy v OperationSet. Hromadné operace mají tedy výrazně nižší průměrnou dobu provádění než operace s jedním záznamem.

## <a name="scenarios"></a>Scénáře
Následující tabulka ukazuje doby provádění, když se rozhraní API Plánu projektu používají ke splnění konkrétních scénářů. Časy jsou v sekundách.

| Scénář                                                                   | Čas  |
|----------------------------------------------------------------------------|-------|
| Vytvoření projektu, který má 40 úkolů.                                      | 36.01 |
| Vytvoření projektu, který má 40 úkolů a 20 závislostí.                  | 38.11 |
| Vytvoření projektu, který má 40 úkolů a 30 přiřazení.                   | 60.17 |
| Vytvoření projektu, který má 40 úkolů, 20 závislostí a 30 přiřazení. | 60.27 |

## <a name="best-practices"></a>Osvědčené postupy
Na základě výsledků předchozího scénáře fungují rozhraní API lépe za následujících podmínek:

  - Je seskupeno co nejvíce operací dohromady. Průměrná doba běhu hromadných operací je lepší než průměrná doba běhu operací s jedním záznamem. Čím menší je počet používaných sad OperationSet, tím rychlejší bude průměrná doba provádění.
  - Nastavte pouze minimální počet atributů, které jsou nutné k provedení vašeho scénáře. Pečlivě volte typy nepovinných polí zahrnutých v požadavku OperationSet. Pole, která obsahují cizí klíče nebo souhrnná pole, negativně ovlivní výkon.
