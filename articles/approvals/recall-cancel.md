---
title: Odvolání dříve schválených položek
description: Toto téma vysvětluje, jak může člen projektového týmu požádat o odvolání dříve předložených a schválených záznamů o čase, výdajích a použití materiálu, a jak může projektový manažer schválit nebo zamítnout žádosti o stažení.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586566"
---
# <a name="recall-previously-approved-entries"></a>Odvolání dříve schválených položek

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Člen projektového týmu, který odesílá záznam o čase, výdajích nebo spotřebě materiálu, může tento záznam po schválení odvolat. Proces odvolání tvoří dva hlavní kroky:

1. Odesílatel požádá o odvolání.
2. Schvalovatel schválí žádost o odvolání.

## <a name="request-a-recall"></a>Žádost o odvolání

Chcete-li odvolat dříve schválený záznam o čase, výdajích nebo spotřebě materiálu, postupujte následujícím způsobem.

1. V závislosti na typu záznamu, který chcete odvolat, proveďte jeden z těchto kroků:

    - U časových záznamů přejděte do nabídky **Projekty** \> **Má práce** \> **Časový záznam** a vyberte všechny časové záznamy pro konkrétní kombinaci projektu a úkolu. Alternativně vyberte v mřížce jednotlivé buňky pro čas u určitého data pro konkrétní projekt.
    - U výdajových záznamů přejděte do nabídky **Projekty** \> **Má práce** \> **Výdaje** a vyberte řádek výdajového záznamu, který chcete odvolat.
    - U záznamů o spotřebě materiálu přejděte do nabídky **Projekty** \> **Má práce** \> **Protokol využití materiálu** a vyberte řádek záznamu o spotřebě materiálu, který chcete odvolat.

2. Vyberte **Odvolat**. Zobrazí se dialogové okno s potvrzením Pokud byly vybrané záznamy o čase, výdajích nebo spotřebě materiálu již schváleny, budete vyzváni k zadání důvodu odvolání.
3. Zadejte důvod odvolání a výběrem **OK** operaci potvrďte. Systém zašle osobě, která položky schválila, žádost o schválení odvolání.

> [!IMPORTANT]
> Nemůžete vytvořit žádost o zrušení záznamu o čase, výdajích a spotřebě materiálu, který již byl zákazníkovi fakturován. Pokud se o to pokusíte, uvidíte zprávu, že záznam o čase, výdajích nebo spotřebě materiálu nelze odvolat, protože už byl fakturován. V tomto případě můžete požádat o odvolání záznamu pouze v případě, že je použita opravná faktura pro vystavení plného dobropisu nebo vrácení peněz zákazníkovi k původní faktuře.

## <a name="approve-or-reject-a-recall-request"></a>Schválení nebo zamítnutí žádosti o odvolání

Chcete-li žádost o odvolání schválit nebo zamítnout, postupujte podle následujících kroků.

1. Přejděte do **Projekty** \> **Úkoly** \> **Schválení**.
2. Na stránce se seznamem **Schválení** změňte zobrazení na **Odvolat žádosti o schválení**. Zobrazí se seznam odeslaných žádostí o odvolání.
3. Vyberte jeden nebo více záznamů a pak vyberte buď **Schválit** nebo **Zamítnout**.
4. Pokud jste zvolili **Schválit**, obdržíte varovnou zprávu s vysvětlením dopadu schválení. Výběrem **OK** operaci potvrďte. Žádost o odvolání je schválena.

    –nebo–

    Pokud jste vybrali **Zamítnout**, je žádost o odvolání zamítnuta.

> [!IMPORTANT]
> Když je odvolání schváleno, stejně jako při žádosti o odvolání systém přitom zkontroluje jakoukoli fakturační činnost u záznamů o čase, výdajích nebo spotřebě materiálu. Pokud byl záznam již fakturován nebo pokud je na konceptu faktury, zobrazí se schvalovateli chybová zpráva, že odvolání časového nebo výdajového záznamu nelze schválit, protože již byl fakturován. V tomto případě může schvalovatel schválit odvolání záznamu pouze v případě, že je použita opravná faktura pro vystavení plného dobropisu nebo vrácení peněz zákazníkovi k původní faktuře.

## <a name="impact-of-a-recall-request"></a>Dopad žádosti o odvolání

Pokud je schválení odvoláno, existuje jak provozní dopad, tak i finanční dopad.

### <a name="operational-impact"></a>Provozní dopad

Je-li žádost o odvolání schválena, označí se záznam o schválení jako **Zamítnutý**. Stav záznamu se změní buď na **Vráceno**, nebo **Zamítnuto**, v závislosti na tom, zda se jedná o záznam o čase, výdajích nebo spotřebě materiálu .

Člen projektového týmu může záznamy zobrazit, upravit a poté je znovu odeslat nebo zcela odstranit.

Pokud je žádost o odvolání zamítnuta, stav záznamu zůstane **Schváleno** a člen týmu nebo schvalovatel projektu ho nemůže upravit.

### <a name="financial-impact"></a>Finanční dopad

Pokud je žádost o odvolání schválena, tak se skutečné hodnoty nákladů a prodeje nejprve aktualizují následujícím způsobem:

- Pole **Stav úpravy** se aktualizuje na **Upraveno**.
- Pole **Stav fakturace** se aktualizuje na **Zrušeno**.

Dále se v tabulce Skutečné hodnoty vytvoří záznamy storna. Chcete-li vytvořit záznamy storna, systém zkopíruje hodnoty tohoto pole z původních skutečných hodnot. Jedinými hodnotami, které nejsou kopírovány, jsou hodnoty množství. Tyto hodnoty jsou naopak stornovány. Stornované skutečné hodnoty se vytvoří pro skutečné hodnoty **Nákladů** a **Nefakturovaného prodeje**. Pole **Stav úpravy** je u stornovaných skutečných hodnot nastaveno na **Neupravitelné** a pole **Stav fakturace** je nastaveno na **Zrušeno**. Kvůli těmto změnám už nebudou zaznamenané výdaje a nedokončené výnosy v projektu dále odpovídat částkám, které tyto skutečné hodnoty představují.

Je-li žádost o odvolání zamítnuta, tak to na projekt nemá žádný finanční dopad.

## <a name="changes-to-time-entry-records"></a>Změny časových záznamů

Následující obrázek zobrazuje změny, ke kterým dojde u schválených časových záznamů a odpovídajících záznamů schválení při jejich odvolání.

![Stavové přechody časových záznamů.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Změny výdajových záznamů a záznamů o spotřebě materiálu

Následující obrázek zobrazuje změny, ke kterým dojde u schválených výdajových záznamů a záznamů o spotřebě materiálu a odpovídajících záznamů schválení při jejich odvolání.

![Stavové přechody výdajových záznamů.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
