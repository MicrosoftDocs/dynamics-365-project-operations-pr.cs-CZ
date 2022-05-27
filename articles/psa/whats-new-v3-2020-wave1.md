---
title: Novinky a změny v aplikaci Project Service Automation verze 3.x vlny 1 2020
description: Tohle téma poskytuje informace o novinkách a změnách v aplikaci Project Service Automation verze 3 vlny 1 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 073b70b4ae02d943eb0794b51e888815ee16f438
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577872"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novinky a změny v aplikaci Project Service Automation verze 3 vlny 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Téma zdůrazňuje klíčové aspekty upgradu při přechodu na nejnovější vydání aplikace Project Service Automation (PSA) verze 3.x vlny 1 2020.

## <a name="time-entry"></a>Časový záznam
Možnosti práce s časovým záznamem byly rozšířeny, takže umožňují rozšíření časového záznamu do více zákaznických scénářů. To zahrnuje možnost přidat typy záznamů, které nyní řídí specifické chování na základě názvu schématu pole **Nastavení časového záznamu**, zobrazených jako **Časový zdroj**. Na podporu této funkce bylo přidáno nové řešení Time, Expense, Statusing, and Approvals (TESA).

### <a name="upgrade-consideration"></a>Důležité informace o upgradu
Pro podporu této funkce byly role v rámci PSA aktualizovány, aby zahrnovaly nová oprávnění. Tato oprávnění udělují přístup pro čtení k nové entitě, **Nastavení časového záznamu**.

Uživatelům, kteří potřebují protokolovat čas, by měla být udělena role **Uživatel časového záznamu** navíc ke stávajícím rolím. Tato role zahrnuje novou funkci a zajišťuje, že časový záznam bude nadále fungovat.

Pokud navíc máte jakékoli vlastní moduly aplikace, které zahrnují všechny formuláře pro entitu časového zadání, budete muset odebrat **formulář pro rychlé vytvoření zadání času TESA** z modulu.

### <a name="currently-extended-time-entry-changes"></a>Aktuálně změny rozšířeného časového záznamu
Aby se minimalizoval dopad na současné uživatele časového záznamu, je tato změna role jediným základním požadavkem nezbytným pro pokračování ve časového záznamu. Pokud jste vytvořili vlastní zobrazení nebo oddělené časové záznamy, musíte nastavit pole **Nastavení časového záznamu** na správnou hodnotu PSA.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
