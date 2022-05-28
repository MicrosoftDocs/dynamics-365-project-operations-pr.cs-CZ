---
title: Zrušení schválení dříve schválených záznamů
description: Toto téma vysvětluje, jak může projektový manažer zrušit schválení dříve schválených záznamů o čase, výdajích nebo spotřebě materiálu.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584772"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Zrušení schválení dříve schválených záznamů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Projektový manažer nebo schvalovatel, který schválil záznamy o čase, výdajích nebo spotřebě materiálu, může schválení těchto záznamů zrušit. 

Chcete-li zrušit schválení již schváleného záznamu o čase, výdajích nebo spotřebě materiálu, postupujte následujícím způsobem.

1. Přejděte do **Projekty** \> **Úkoly** \> **Schválení**.
2. Stránka **Schválení** vypisujte všechny časové záznamy, které čekají na schválení. Změňte zobrazení na **Moje minulá schválení**.
3. Vyberte schválení času, výdajů nebo materiálu, které chcete zrušit. Poté v podokně akcí vyberte možnost **Zrušit schválení**.
4. V potvrzovacím okně, které se zobrazí, vyberte **OK** pro potvrzení operace.

> [!IMPORTANT]
> Nemůžete zrušit schválení dříve schváleného záznamu o čase, výdajích a spotřebě materiálu, který již byl zákazníkovi fakturován. Pokud to zkusíte, zobrazí se zpráva, že schválení nelze zrušit, protože již bylo vyfakturováno. V tomto případě můžete zrušit schválení pouze v případě, že je použita opravná faktura pro vystavení plného dobropisu nebo vrácení peněz zákazníkovi k původní faktuře.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Dopad zrušení schválení dříve schváleného záznamu

Pokud je schválení zrušeno, existuje jak provozní dopad, tak i finanční dopad.

### <a name="operational-impact"></a>Provozní dopad

Pokud je schválení zápisu zrušeno, je záznam o schválení označen jako **Odesláno**. Stav záznamu se změní na **Odesláno**. V této fázi může člen projektového týmu odvolat položku bez odeslání žádosti o odvolání.

Schvalovatel může změnit **Fakturovatelné množství** a **Typ fakturace** a poté položku ještě jednou schválit.

### <a name="financial-impact"></a>Finanční dopad

Pokud je schválení záznamu zrušeno, tak se skutečné hodnoty nákladů a prodeje aktualizují následujícím způsobem:

- Pole **Stav úpravy** se aktualizuje na **Upraveno**.
- Pole **Stav fakturace** se aktualizuje na **Zrušeno**.

Dále se v tabulce Skutečné hodnoty vytvoří záznamy storna. Chcete-li vytvořit záznamy storna, systém zkopíruje hodnoty tohoto pole z původních skutečných hodnot. Jedinými hodnotami, které nejsou kopírovány, jsou hodnoty množství. Tyto hodnoty jsou naopak stornovány. Stornované skutečné hodnoty se vytvoří pro skutečné hodnoty **Nákladů** a **Nefakturovaného prodeje**. Pole **Stav úpravy** je u stornovaných skutečných hodnot nastaveno na **Neupravitelné** a pole **Stav fakturace** je nastaveno na **Zrušeno**. Kvůli těmto změnám už nebudou zaznamenané výdaje a nedokončené výnosy v projektu dále odpovídat částkám, které tyto skutečné hodnoty představují.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
