---
title: Důležité informace o upgradu pro strukturovaný rozpis prací
description: Toto téma obsahuje informace o upgradu strukturovaného rozpisu prací z verze Project Service Automation 2.x na 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: a067521410f0fe0d8f5d4c510a35f2a3b018dce3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281740"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Důležité informace o upgradu pro strukturovaný rozpis prací

[!include [banner](../includes/psa-now-project-operations.md)]

Toto téma obsahuje informace o upgradu strukturovaného rozpisu prací z verze Project Service Automation 2.x na 3.x. Toto téma definuje zdravý stav projektu v aplikaci Project Service Automation (PSA), který je nutný pro úspěšný upgrade. Obsahuje také informace o běžných blokovacích podmínkách, které způsobí selhání upgradu. Další informace o definování úkolů projektu a jejich funkcích v rámci plánu projektu naleznete v tématu [Projektové plány](project-creating.md).

## <a name="key-entities"></a>Klíčové entity
Pro přesný strukturovaný rozpis prací, ve kterém jsou již načteny zdroje, jsou vyžadovány následující entity:

- [Projekt](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projektový tým](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projektový úkol](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Přiřazení zdrojů](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Závislost projektového úkolu](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Rezervovatelné zdroje](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Chcete-li definovat strukturovaný rozpis prací s načtenými zdroji, je třeba provést následující kroky:

1. Vytvořte nový projekt. Další informace o vytvoření nového projektu naleznete v tématu [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Vytvořte jeden nebo více úkolů. Další informace o vytvoření nového úkolu naleznete v tématu [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definujte závislosti mezi úkoly. Další informace viz [Závislost projektového úkolu](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Přiřaďte členy projektového týmu k projektu. Další informace naleznete v tématu [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Přiřaďte členy projektového týmu k úkolům. Další informace naleznete v tématu [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Vztahy v projektovém týmu

Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:
- Všem členům projektového týmu musí být přiřazen rezervovatelný zdroj.
- Všichni členové projektového týmu musí být přiřazeni ke stejnému projektu. 

## <a name="project-task-relationships"></a>Vztahy úkolu projektu
Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:

- Všechny související úkoly musí být přiřazeny ke stejnému projektu.
- Každý úkol na řádku musí mít nadřazený úkol.
- Každý úkol musí mít nadřazený projekt.

### <a name="valid-conditions"></a>Platné podmínky

- Všechny doby trvání úkolů musí být větší nebo rovny (>=) jedné hodině a menší než 1 800 000 minut (1 250 dní).*
- Všechny úkoly musí mít počáteční datum nejdříve 1. 1. 2000.*
- Všechny úkoly musí mít počáteční datum nejpozději 17 let od dnešního dne.*
- Všechny úkoly musí mít počáteční datum dřívější nebo shodné s datem dokončení.
- Všechny typy transakcí v klasifikacích (výdaje, materiál, daň a čas) musí mít hodnoty pro **Výchozí jednotku** a **Skupinu jednotek**.
- Je třeba se vyhnout formátům data s písmeny.

### <a name="potential-mitigation-steps"></a>Potenciální postup zmírnění
- Pomocí rozšířeného hledání lze identifikovat projektové úkoly, které neobsahují ID projektu.
- Pomocí rozšířeného hledání lze identifikovat projektové úkoly, u nichž je plánované trvání delší než> 1 800 000.
- Před provedením jakýchkoli změn dat byste měli prozkoumat všechna vlastní nastavení spojená s entitou, která mohla vést k tomu, že se data dostanou do špatného stavu. Tato vlastní nastavení by měla být vyřešena před provedením jakékoli aktualizace týkající se dat.
- U identifikovaných úkolů, které jsou osiřelé, zvažte odstranění těchto úkolů, pokud nejsou potřeba nebo pokud by měly být přidruženy ke správnému nadřazenému projektu.
- U všech úkolů, jejichž trvání je delší než 1 250 dní, zvažte přidání více úkolů, které představují celkové trvání, pokud je to možné.

> [!NOTE]
> Položky označené hvězdičkou (\*) mají limity, které jsou způsobeny skutečností, že správa vztahů se zákazníky (CRM) podporuje pouze 7 320 rozšíření opakování. Musíte zůstat pod tímto limitem.

## <a name="resource-assignment-relationships"></a>Vztahy přiřazení zdroje
Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:

- Všechna přiřazení zdrojů ve strukturovaném rozpisu prací musí souviset se stejným projektem.
- Všechna přiřazení zdrojů ve strukturovaném rozpisu prací musí být přiřazeny členům projektového týmu ve stejném projektu.

### <a name="potential-mitigation-steps"></a>Potenciální postup zmírnění
- Určete všechny úkoly, které nespadají do výše popsaných podmínek.  
- Všechna přiřazení zdrojů, která již nejsou platná, by měla být odstraněna.

## <a name="project-task-dependency-relationships"></a>Vztahy závislosti úkolů projektu
Aby bylo možné zajistit úspěšný upgrade, je nutné správně udržovat následující vztahy:

- Všechny závislosti úkolů projektu musí souviset se stejným projektem.
- Úkol nesmí mít stejnou závislost odkazovanou více než jednou.


[!INCLUDE[footer-include](../includes/footer-banner.md)]