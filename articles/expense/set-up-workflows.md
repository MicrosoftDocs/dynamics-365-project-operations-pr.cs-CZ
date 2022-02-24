---
title: Nastavení pracovních postupů pro správu výdajů
description: Můžete nastavit proces pracovního postupu, který se používá ke kontrole a schvalování cestovních a výdajových dokladů.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127690"
---
# <a name="set-up-workflows-for-expense-management"></a>Nastavení pracovních postupů pro správu výdajů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Můžete nastavit proces pracovního postupu ke kontrole a schvalování cestovních a výdajových dokladů. Můžete definovat pracovní postupy pro výkazy výdajů, cestovní žádanky a žádosti o hotovostní zálohy.

Pracovní postup představuje obchodní proces a definuje, jak doklad protéká systémem. Pracovní postup také označuje, kdo musí dokončit úkol nebo schválit dokument. Existuje několik výhod používání systému pracovního postupu ve vaší organizaci:

- **Konzistentní procesy**: Můžete definovat proces schvalování pro konkrétní doklady, jako jsou nákupní žádanky a výkazy výdajů. Používání systému pracovního postupu pomáhá zajistit, aby dokumenty byly zpracovávány a schvalovány konzistentním a efektivním způsobem.
- **Viditelnost procesu**: Můžete sledovat stav, historii a metriky výkonu konkrétní instance pracovního postupu. To vám pomůže určit, zda je třeba provést změny v pracovním postupu, aby se zlepšila účinnost.
- **Centralizovaný pracovní seznam**: Uživatelé si mohou prohlížet centralizovaný pracovní seznam a zobrazit úkoly pracovního toku a schválení, která jim byla přidělena. 

## <a name="workflow-types"></a>Typy pracovního postupu

Následující tabulka obsahuje typy pracovních postupů, které můžete vytvářet ve **správě výdajů**.


|              <strong>Typ</strong>              |                   <strong>Použít tento typ k</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Automatické schválení výkazů výdajů</strong> |            Vytvořte pracovní postupy schválení pro výkazy výdajů.             |
|  <strong>Automatické zaúčtování výkazů výdajů</strong>   |        Vytvořte pracovní postupy automatického zaúčtování pro výkazy výdajů.        |
|       <strong>Položka řádku výdajů</strong>        |     Vytvořte pracovní postupy schválení pro položky řádků na výkazech výdajů.      |
| <strong>Automatické zaúčtování položek řádku výdajů</strong> | Vytvořte pracovní postupy automatického zaúčtování pro položky řádků na výkazech výdajů. |
|       <strong>Cestovní žádanka</strong>       |          Vytvořte pracovní postupy schválení pro cestovní žádanky.           |
|      <strong>Požadavek na hotovostní zálohu</strong>      |         Vytvořte pracovní postupy schvalování požadavků na hotovostní zálohu.          |
|        <strong>Vratka DPH</strong>        | Vytvořte pracovní postupy schválení pro vratku daně z přidané hodnoty (DPH).  |
