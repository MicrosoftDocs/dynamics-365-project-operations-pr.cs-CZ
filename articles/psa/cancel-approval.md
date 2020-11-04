---
title: Zrušit dříve schválené časové a výdajové záznamy
description: Toto téma obsahuje informace o tom, jak zrušit schválený čas projektu a výdajovou transakci.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 0ea816040570cc8f6ddf3c5ec8a74ac092fc68b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073955"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Zrušit dříve schválené časové nebo výdajové záznamy

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V nejnovější verzi Dynamics 365 Project Service Automation mohou schvalující zrušit časové nebo výdajové záznamy, které dříve schválili.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Zrušit dříve schválený časový nebo výdajový záznam

Chcete-li zrušit dříve schválený časový nebo výdajový záznam, postupujte následujícím způsobem.

1. Přejděte do **Projekty** \> **Úkoly** \> **Schválení**.
2. Na stránce se seznamem **Schválení** změňte zobrazení na **Moje předchozí schválení**. Zobrazí se seznam časových a výdajových záznamů, které jste dříve schválili.
3. Vyberte jeden nebo více záznamů a pak vyberte **Zrušit schválení**. Zobrazí se varovná zpráva.
4. Pokud chcete schválení zrušit, vyberte **OK**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Porozumění vlivu zrušení schválení časového nebo výdajového záznamu

Pokud je schválení zrušeno, existuje jak provozní dopad, tak i finanční dopad.

### <a name="operational-impact"></a>Provozní dopad

Z provozního pohledu se stav záznamu při zrušení schválení obnoví na **Koncept** a schválení se již nezobrazuje v zobrazení **Moje předchozí schválení**. Zrušené schválení se místo toho zobrazí buď v zobrazení **Časové záznamy ke schválení** nebo v zobrazení **Výdajové záznamy ke schválení** , v závislosti na tom, zda se jednalo o časový záznam nebo výdajový záznam. Dále se stav souvisejícího časového nebo výdajového záznamu změní na **Odesláno** , takže související záznam je konzistentní se schváleními, která mají stav **Koncept**.

Jako schvalující můžete upravit některá pole schválení, která mají stav **Koncept**. Tato pole zahrnují **Typ fakturace** a **Fakturovatelné hodiny pro časové záznamy**. Po provedení změn můžete záznam znovu schválit. Záznam můžete také zamítnout. Pokud zamítnete schválení časového záznamu, změní se stav záznamu na **Vráceno**. Pokud zamítnete schválení výdajového záznamu, změní se stav záznamu na **Zamítnuto**. Funkčně se oba vrácené a zamítnuté záznamy chovají stejně jako záznam se stavem **Koncept**. Člen projektového týmu může buď provést požadované změny záznamu, a pak jej znovu odeslat ke schválení, nebo záznam zcela odstranit.

### <a name="financial-impact"></a>Finanční dopad

Projekt je při zrušení schválení ovlivněn také finančně. Odpovídající skutečné hodnoty nákladů a prodeje se nejprve aktualizují následujícím způsobem:

- Stav úpravy je nastaven na **Upraveno**.
- Stav fakturace je nastaven na **Zrušeno**.

Dále se v tabulce Skutečné hodnoty vytvoří záznamy storna. Chcete-li vytvořit záznamy storna, systém zkopíruje hodnoty tohoto pole z původních skutečných hodnot. Jedinými hodnotami, které nejsou kopírovány, jsou hodnoty množství. Tyto hodnoty jsou naopak stornovány. Stornované skutečné hodnoty se vytvoří pro skutečné hodnoty **Nákladů** a **Nefakturovaného prodeje**. Pole **Stav úpravy** je u stornovaných skutečných hodnot nastaveno na **Neupravitelné** a stav fakturace je nastaven na **Zrušeno**.

Po provedení těchto změn bude částka zaznamenaná jako utracená v projektu a nedokončené výnosy v projektu dále odpovídat částkám, které tyto skutečné hodnoty představují.
