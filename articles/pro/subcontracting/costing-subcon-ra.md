---
title: Odhad nákladů na přidělení zdrojů subdodávky
description: Tento článek vysvětluje, jak Microsoft Dynamics 365 Project Operations vypočítává odhad nákladů na přidělení zdrojů subdodávky.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262051"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Odhad nákladů na přidělení zdrojů subdodávky

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Přiřazení úkolů členům projektového týmu subdodávky je kalkulováno pomocí ceníku **Nákup**, který je připojen k subdodávce na příslušném záznamu člena týmu. To se liší od způsobu výpočtu přiřazení zaměstnanců, kde se přiřazení úkolů zaměstnancům počítá pomocí ceníku **Náklady**, který je přílohou smluvní jednotky projektu. 

U členů obecného projektového týmu, který je řešen jako subdodávka, je přidělení počítáno pomocí nastavení ceny na základě rolí v nákupním ceníku, který je připojen k subdodávce. Nákupní ceny lze také nastavit specificky pro každý zdroj. Tyto ceny specifické pro zdroj budou upřednostněny, když jsou přiřazení úkolů ocenění u členů uvedeného projektového týmu smluvními pracovníky. 

Priorita použití kupní ceny specifické pro určitou roli oproti použití ceny specifické pro zdroj je řízena nastavením priority cenové dimenze v okně **Parametry > Cenové dimenze založené na částce**.

Tato funkce dynamického odvozování cen na základě nastavení dimenzí pro nákupní ceny subdodavatelů je podobná tomu, jak se odvozují nákladové a fakturační sazby u zaměstnanců na plný úvazek. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Vytváření přiřazení úkolů pro získání odhadů nákladů na zdroje subdodavatelů

Přiřazení úkolů pro subdodavatele lze vytvořit dvěma způsoby: 
- Na kartě **Úkoly**.
- Na kartě **Tým**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Vytváření přiřazení zdrojů pomocí karty Úkoly
S využitím seznamu **Zdroje** na kartě **Úkoly** pro konkrétní úkol můžete vytvořit přiřazení úkolu pro pojmenovaný zdroj nebo obecný zdroj. Pokud vyberete pojmenovaný zdroj v rozbalovacím seznamu **Přidělené zdroje** u úkolu a tento zdroj je smluvní pracovník, pojmenovaný zdroj je přiřazen k úkolu a je vytvořen odpovídající záznam člena projektového týmu s typem pracovníka nastaveným na **Smluvní pracovník** a **Platností** nastavenou na **Neplatný**. Jako další krok budete muset otevřít záznam člena projektového týmu a vybrat subdodávku a řádek subdodávky. Tím se aktualizuje přiřazení úkolu tak, aby obsahovalo odkaz na subdodávku a řádek subdodávky, a také se aktualizuje stav člena týmu na **Platný**.

Pokud se rozhodnete vytvořit obecného člena týmu z rozbalovacího seznamu **Přidělené zdroje** u úkolu, dialog **Vytvoření obecného člena týmu** vám umožní vybrat subdodávku a řádek subdodávky. Když je k úkolu přiřazen obecný zdroj a je vytvořen odpovídající záznam člena projektového týmu, všimnete si, že záznam člena projektového týmu je vytvořen s typem pracovníka nastaveným na **Smluvní pracovník** a **Platnost** je nastavena na **Platný**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Vytváření členů projektového týmu pomocí karty Tým
Na kartě Tým v projektu můžete vytvořit obecného nebo pojmenovaného člena týmu. Při vytváření člena týmu můžete vybrat subdodávku a řádek subdodávky. Po vytvoření člena týmu budete muset člena týmu přiřadit k úkolu pomocí rozbalovací nabídky **Přidělené zdroje** u úkolu. 

## <a name="updating-estimates"></a>Aktualizace odhadů
Po přiřazení členů projektového týmu k úkolům budete muset přejít na kartu **Odhady** projektu a vybrat příkaz **Aktualizovat ceny**, aby bylo zajištěno, že nákladové sazby přidělení zdrojů subdodávky jsou aktualizovány na základě nákupního ceníku připojeného k subdodávce. Pro nepřiřazené úkoly se v Microsoft Dynamics 365 Project Operations negenerují odhady. V důsledku toho budete muset vytvořit přiřazení úkolů k ceně a ocenit různé úkoly ve vašem projektu. 

> [POZNÁMKA!] Členové projektového týmu, kteří mají **Typ pracovníka** nastaven na **Smluvní pracovník**, ale nemají odkaz na subdodávku, jsou označeni jako **Neplatný** v mřížce **Členové projektového týmu**. Pokud existují členové projektového týmu s tímto stavem, otevřete záznam člena projektového týmu a ručně aktualizujte pole subdodávky a řádku subdodávky, aby odhad finančních nákladů přesně odrážel náklady subdodavatele na kartě **Odhady**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
