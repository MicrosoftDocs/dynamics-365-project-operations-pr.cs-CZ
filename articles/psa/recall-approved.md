---
title: Odvolání schválených časových nebo výdajových záznamů
description: Toto téma obsahuje informace o tom, jak odvolat dříve schválený čas nebo výdajovou transakci.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7bacd70881a6c463cc449a365173da5338a3d3fc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073827"
---
# <a name="recall-approved-time-or-expense-entries"></a>Odvolání schválených časových nebo výdajových záznamů

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Člen projektového týmu nebo jiná osoba, která odesílá časový nebo výdajový záznam, může tento časový nebo výdajový záznam po schválení odvolat. Proces odvolání časového nebo výdajového záznamu má dva kroky:

1. Odesílatel požádá o odvolání.
2. Schvalovatel schválí odvolání.

## <a name="request-a-recall"></a>Žádost o odvolání

Chcete-li odvolat dříve schválený časový nebo výdajový záznam, postupujte následujícím způsobem.

1. V případě časových záznamů přejděte do **Projekty** \> **Úkoly** \> **Časový záznam**.

    –nebo–

    V případě výdajových záznamů přejděte do **Projekty** \> **Úkoly** \> **Výdaje**.

2. U časových záznamů vyberte všechny časové záznamy pro konkrétní kombinaci projektu a úkolu. Alternativně vyberte v mřížce jednotlivé buňky pro čas u určitého data pro konkrétní projekt.

    –nebo–

    U výdajových záznamů vyberte řádek výdajového záznamu, který chcete odvolat.

3. Vyberte **Odvolat**. Zobrazí se dialogové okno s potvrzením Pokud byly vybrané časové a výdajové záznamy již schváleny, budete vyzváni k zadání důvodu odvolání.
4. Zadejte důvod odvolání a výběrem **OK** operaci potvrďte. Systém zašle osobě, která položky schválila, žádost o schválení odvolání.

> [!NOTE]
> Přestože lze schválené časové a výdajové záznamy odvolat, pokud již byl zákazníkovi schválený časový nebo výdajový záznam fakturován, nelze žádost o odvolání vytvořit. Uživatel, který se pokusí vytvořit žádost o odvolání, obdrží zprávu, že časový nebo výdajový záznam nelze odvolat, protože už byl fakturován.

## <a name="approve-or-reject-a-recall-request"></a>Schválení nebo zamítnutí žádosti o odvolání

Chcete-li žádost o odvolání schválit nebo zamítnout, postupujte podle následujících kroků.

1. Přejděte do **Projekty** \> **Úkoly** \> **Schválení**.
2. Na stránce se seznamem **Schválení** změňte zobrazení na **Odvolat žádosti o schválení**. Zobrazí se seznam odeslaných žádostí o odvolání.
3. Vyberte jeden nebo více záznamů a pak vyberte buď **Schválit** nebo **Zamítnout**.
4. Pokud jste zvolili **Schválit** , obdržíte varovnou zprávu s vysvětlením dopadu schválení. Výběrem **OK** operaci potvrďte. Žádost o odvolání je schválena.

    –nebo–

    Pokud jste vybrali **Zamítnout** , je žádost o odvolání zamítnuta.

> [!NOTE]
> Stejně jako při žádosti o odvolání systém při schválení odvolání u časových nebo výdajových záznamů kontroluje jakoukoli fakturační činnost. Pokud byl záznam již fakturován nebo pokud je na konceptu faktury, zobrazí se schvalovateli chybová zpráva, že odvolání časového nebo výdajového záznamu nelze schválit, protože již byl fakturován.

## <a name="impact-of-a-recall-request"></a>Dopad žádosti o odvolání

Pokud je schválení odvoláno, existuje jak provozní dopad, tak i finanční dopad.

### <a name="operational-impact"></a>Provozní dopad

Je-li žádost o odvolání schválena, označí se záznam o schválení jako **Zamítnutý**. Stav záznamu se změní buď na **Vráceno** , nebo **Zamítnuto** , v závislosti na tom, zda se jedná o časový nebo výdajový záznam.

Člen projektového týmu může záznamy zobrazit, upravit a poté je znovu odeslat nebo zcela odstranit.

Pokud je žádost o odvolání zamítnuta, stav záznamu zůstane **Schváleno** a člen týmu nebo schvalovatel projektu ho nemůže upravit.

### <a name="financial-impact"></a>Finanční dopad

Pokud je žádost o odvolání schválena, tak se skutečné hodnoty nákladů a prodeje nejprve aktualizují následujícím způsobem:

- Pole **Stav úpravy** se aktualizuje na **Upraveno**.
- Pole **Stav fakturace** se aktualizuje na **Zrušeno**.

Dále se v tabulce Skutečné hodnoty vytvoří záznamy storna. Chcete-li vytvořit záznamy storna, systém zkopíruje hodnoty tohoto pole z původních skutečných hodnot. Jedinými hodnotami, které nejsou kopírovány, jsou hodnoty množství. Tyto hodnoty jsou naopak stornovány. Stornované skutečné hodnoty se vytvoří pro skutečné hodnoty **Nákladů** a **Nefakturovaného prodeje**. Pole **Stav úpravy** je u stornovaných skutečných hodnot nastaveno na **Neupravitelné** a pole **Stav fakturace** je nastaveno na **Zrušeno**. Kvůli těmto změnám už nebudou zaznamenané výdaje a nedokončené výnosy v projektu dále odpovídat částkám, které tyto skutečné hodnoty představují.

Je-li žádost o odvolání zamítnuta, tak to na projekt nemá žádný finanční dopad.

## <a name="changes-to-time-entry-records"></a>Změny časových záznamů

Následující obrázek zobrazuje změny, ke kterým dojde u schválených časových záznamů při jejich odvolání.

![Stavové přechody časových záznamů](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Změny výdajových záznamů

Následující obrázek zobrazuje změny, ke kterým dojde u schválených výdajových záznamů při jejich odvolání.

![Stavové přechody výdajových záznamů](media/ExpenseEntryStateTransitions.png)
