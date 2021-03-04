---
title: Přiřazení zdroje k úkolu
description: Toto téma obsahuje informace o způsobu přiřazení zdrojů k úkolům.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
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
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149985"
---
# <a name="assign-a-resource-to-a-task"></a>Přiřazení zdroje k úkolu

[!include [banner](../includes/psa-now-project-operations.md)]

Existují tři způsoby, jak přiřadit zdroj k úkolu v Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervace zdroje jako člena týmu a následné přiřazení zdroje k úkolu

Můžete přidat zdroj do projektového týmu a poté přiřadit zdroj k úkolům v plánu projektu.

1. Na kartě **Člen týmu** přidejte nového člena týmu výběrem možnosti **Nový**. 

2. Otevře se panel **Rychlé vytvoření člena týmu**, kde můžete zvolit název rezervovatelného zdroje a nastavit roli. 

    Vyberte jednu z následujících metod přidělení pro rezervaci zdroje:

    - **Plná kapacita** rezervuje plnou kapacitu zdroje pro zadaná počáteční a koncová data.
    - **Procentuální kapacita** rezervuje zdroj pro procento kapacity zdroje pro daná počáteční a koncová data.
    - **Rovnoměrně rozdělit podle hodin** rezervuje zdroj pro určený počet hodin a distribuuje ho rovnoměrně každý den v období od počátečního do koncového data.
    - **Vytížení na začátku podle hodin** rezervuje zdroj pro určený počet hodin s vytížením na začátku každý den v období od počátečního do koncového data.
    - **Žádné** přidá zdroj k týmu, ale nevytvoří žádné rezervace, které absorbují kapacitu zdroje.

3. Na mřížce **Plán** zvolte pro úkol ikonu **Zdroj** v buňce zdroje a pak v části **Členové týmu** vyberte člena týmu, kterého jste právě přidali. 

> [!NOTE]
> Na kartách **Člen týmu** a **Vyrovnání** se u zdroje zobrazují rezervované a přiřazené hodiny. Tyto hodiny by měly být stejné, ale není to nutné, protože rezervace a přiřazení nejsou pevně spjaty. Karta **Vyrovnání** uvádí podrobnosti, pokud jsou odlišné, například při přiřazení více hodin zdroji, než jste rezervovali. Tyto informace můžete v případě potřeby opravit rozšířením rezervací zdroje nebo změnou přiřazení.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Vytvoření obecného člena týmu prostřednictvím přiřazení úkolu

Pokud pomocí přiřazení úkolu vytvoříte obecného člena týmu, vytvoříte zástupce nebo obecný zdroj, který popisuje vlastnosti pojmenovaného zdroje, u kterého chcete, aby pracoval na úkolech. Potom vygenerujete požadavek (nebo odešlete žádost pomocí požadavku), který slouží k vyhledávání a rezervaci pojmenovaného zdroje.

1. V mřížce **Plán** vyberte pro daný úkol ikonu **Zdroj** v buňce zdroje.

2. Zadejte název sloužící jako zástupný text názvu zdroje. Například Programový manažer.

3. Vyberte **Vytvořit** a v poli **Rychlé vytvoření člena týmu** nastavte roli pro obecný zdroj.

4. Můžete pokračovat k přiřazení úkolů tomuto zástupnému zdroji výběrem tohoto zdroje ve **Výběru zdrojů** pro daný úkol. Jsou uvedeny pod položkou **Členové týmu**.

5. Po dokončení přiřazování obecného zdroje vyberte obecný zdroj na kartě **Tým** a poté vyberte **Vygenerovat požadavek** pro vytvoření požadavku na zdroj pro obecný zdroj.

6. Vyberte **Rezervovat** pro obecný zdroj. Poté můžete použít Plánovací vývěsku k vyhledání a rezervaci skutečného zdroje. Je také možné odeslat požadavek na splnění manažerem zdrojů.

7. Když je obecný zdroj naplněn pojmenovaným zdrojem, obecný zdroj je odebrán z týmu a přiřazení úkolů pro obecný zdroj jsou přiřazena k pojmenovanému zdroji, který splnil požadavek na zdroj obecného zdroje.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Přiřazení pojmenovaného zdroje ze seznamu všech rezervovatelných zdrojů

Můžete použít vyhledávací pole ve **Výběru zdrojů** pro vyhledání všech rezervovatelných zdrojů a přiřadit je k úkolu.

Zdroje přiřazené tímto způsobem jsou do týmu přidány bez jakýchkoli rezervací. To je podobné jako přidání člena týmu a vybrání metody přidělení Žádná. Zdroj se zobrazí se na kartách **Tým** a **Vyrovnání** jako zdroj pouze s přiřazením a nedostatečnou rezervací. Zarezervujte je, pokud chcete použít jejich dostupnost.

1. V mřížce **Plán** vyberte pro daný úkol ikonu **Zdroj** v buňce zdroje.

2. Začněte psát název. Výsledky vyhledání názvu se zobrazí ve **Výběru zdrojů** v části **Další zdroje**.

3. Vyberte zdroj, který chcete k úkolu přiřadit.



[!INCLUDE[footer-include](../includes/footer-banner.md)]