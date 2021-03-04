---
title: Vytvoření časových záznamů
description: Toto téma obsahuje informace o způsobu vytvoření časových záznamů.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149670"
---
# <a name="create-time-entries"></a>Vytvoření časových záznamů

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V předchozích verzích Dynamics 365 Project Service Automation byly časové záznamy zadány týdně. Ve verzi 3 Project Service Automation se časové záznamy zadávají denně. Po vytvoření několika časových záznamů však tyto položky můžete hromadně vytvořit nebo zkopírovat.

## <a name="create-a-time-entry"></a>Vytvoření časového záznamu

Chcete-li vytvořit časový záznam, postupujte takto.

1. Na stránce **Časové záznamy** vyberte **Nový**.
2. V dialogovém okně **Vytvořit: Časový záznam** zadejte dobu trvání časového záznamu v minutách, hodinách nebo dnech. Doba trvání musí být zadána v následujícím formátu: *x* minut, *x* hodin nebo *x* dnů. Hodiny a dny lze také zadávat jako desetinná čísla, například *x.x* hodin nebo *x.x* dnů.
3. Vyberte typ časového záznamu a projekt, pro který tento časový záznam zadáváte.
4. V poli **Projektový úkol** najděte úkol pro tento časový záznam.

    > [!NOTE]
    > Pokud vytváříte časový záznam pro úkol, který není přiřazen uživateli, vyberte v poli **Projektový úkol** tlačítko **Hledat**, vyberte **Změnit zobrazení** a pak vyberte **Všechny aktivní projektové úkoly** pro zobrazení seznamu všech úkolů.

5. Zadejte popis, pokud je vyžadován popis, a pak vyberte **Uložit a zavřít**.

Jakmile je časový záznam vytvořen a uložen, můžete ho upravit v mřížce časového záznamu. Mřížka časového záznamu podporuje dva formáty:

- Časové záznamy lze zadat ve formátu **hh: mm**. Tento formát je pak převeden na hodiny a zlomky.
- Hodiny a zlomky můžete zadat přímo.

Všimněte si, že zlomky hodiny nejsou minuty. Proto 1,5 hodiny představuje 1 hodinu a 30 minut. Stejné pravidlo platí pro zlomky dne. Jeden den je 24 hodin a 0,5 dne představuje 12 hodin.

## <a name="bulk-create-time-entries"></a>Hromadné vytvoření časových záznamů

Po vytvoření několika časových záznamů je můžete pomocí funkce kopírování kopírovat za účelem hromadného vytvoření dalších záznamů.

1. Na stránce **Časové záznamy** vyberte **Kopírovat týden**.
2. Ve skupině polí **Od období** definujte v polích **Počáteční datum** a **Koncové datum** rozsah dat, ze kterého se má zkopírovat časový záznam.
3. Ve skupině polí **Do období** v poli **Počáteční datum** zadejte datum, pro které chcete vytvořit časové záznamy.
4. Chcete-li vytvořit kopii časových záznamů, které odpovídají dnu v týdnu určenému ve skupině polí **Do období**, klikněte na **Kopírovat**. Například pondělní časový záznam z minulého týdne bude zkopírován do pondělí týdne, který je zadán ve skupině polí jako **Do období**.

## <a name="import-data-for-time-entries"></a>Importovat data pro časové záznamy

Můžete importovat data z rezervací projektů a přiřazení. Při importu dat můžete určit rozsah kalendářních dat rezervací, které chcete importovat, a pak explicitně vybrat rezervace, které mají být vytvořeny jako **Koncept** časových záznamů.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Funkce seskupit podle, třídit, hledat a filtrovat

Časové záznamy lze seskupit a filtrovat podle dimenzí zadaných ve sloupcích. V poli **Seskupit podle** vyberte dimenzi, kterou chcete použít k filtrování časových záznamů. Záznamy s položkami času lze také řadit vzestupně nebo sestupně pomocí šipky řazení v záhlavích sloupců. Tyto záznamy lze zobrazit nebo skrýt výběrem tlačítka **Filtrovat** v záhlavích sloupců a potom do políčka **Hledat** zadáním textu, který má být použit k hledání časových položek podle názvu projektu, úkolu projektu, času položku nebo zdroj.
