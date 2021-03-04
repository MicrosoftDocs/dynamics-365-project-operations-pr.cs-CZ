---
title: Výkon plánování zdrojů projektu
description: Toto téma poskytuje informace o tom, jak zlepšit výkon plánování zdrojů u velkého počtu projektů.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073763"
---
# <a name="project-resource-scheduling-performance"></a>Výkon plánování zdrojů projektu

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Problémy s výkonem u plánování zdrojů mohou nastat, když počet projektů dosáhne tisíců. Chcete-li zlepšit výkon plánování zdrojů, je k dispozici funkce, která uživatelům umožňuje zkrátit čas potřebný ke spuštění formuláře dostupnosti zdrojů. Konkrétně dojde k odebrání procesu synchronizace shrnutí kapacity zdrojů a použije se tabulka **ResProjectResource** k urychlení vyhledávání zdrojů. Poznámka: tabulka **ResRollup** již nebude použita.

> [!IMPORTANT]
> Pokud existuje závislost buď na procesu synchronizace shrnutí kapacity zdrojů, nebo na tabulce **ResProjectResource** , nepoužívejte tuto funkci.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Jak povolit vylepšení výkonu plánování zdrojů
Chcete-li povolit vylepšený výkon při plánování zdrojů, proveďte následující kroky.

1. Přejděte do nabídky **Správa funkcí** > **Vše** a v seznamu funkcí vyhledejte položku **Povolit funkci vylepšení výkonu plánování zdrojů projektu**.
2. Vyberte **Povolit nyní**.

> [!NOTE]
> Pokud nemůžete najít funkci v seznamu, aktualizujte seznam výběrem položky **Kontrola aktualizací**.

3. Aktualizujte okno prohlížeče a přejděte na **Řízení projektů a účetnictví** > **Periodické** > **Zdroje projektu** > **Synchronizovat kapacitu kalendářů zdrojů ve všech společnostech**.
4. Nastavením položky **Odebrat existující záznamy o kapacitě** na **Ano** odstraníte předchozí data. Pokud chcete generovat přírůstková data, nastavte tuto položku na **Ne**.
5. V poli **Kód období** vyberte období, ve kterém mají být data generována. Když vyberete kód období, není nutné definovat počáteční a koncové datum.
6. Když necháte pole **Kód období** prázdné, vyberte konkrétní data zahájení a ukončení pro generování dat.
7. Vyberte **OK**.

 > [!NOTE]
 > Tato akce bude distribuovat obecná data do tabulky **ResCalendarCapacity** napříč všemi společnostmi ve vašem prostředí, takže dávkovou úlohu je třeba spustit pouze v jedné právnické osobě. Data v této dávkové úloze jsou potřebná k výpočtu kapacity zdrojů prostřednictvím přidruženého kalendáře.

8. Přejděte do nabídky **Řízení projektů a účetnictví** > **Periodické** > **Zdroje projektu** > **Naplnit zdroje projektu napříč všemi společnostmi** a poté vyberte **OK**. Toto je skript pro aktualizaci obecných dat v tabulkách **ResProjectResource** , **ResCalendarDateTimeRange** a **ResEffectiveDateTimeRange**. Hodnoty pro pole **PSAPRojSchedRole.RootActivity** se také aktualizují. Pokud tato akce není spuštěna, obdržíte varování, když se pokusíte provést operace plánování zdrojů.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Jak vypnout vylepšení výkonu plánování zdrojů

1. Přejděte do nabídky **Správa funkcí** > **Vše** a vyhledejte položku **Povolit funkci vylepšení výkonu plánování zdrojů projektu**.
2. Vyberte funkci a poté klikněte na tlačítko **Zakázat**.
3. Aktualizujte okno prohlížeče.
4. Přejděte do nabídky **Řízení projektů a účetnictví** > **Periodické** > **Synchronizace kapacity** > **Synchronizace shrnutí kapacity pro prostředek**.
5. Na stránce **Synchronizace shrnutí kapacity** nastavením položky **Odebrat existující záznamy o kapacitě** na **Ano** odstraníte předchozí data. Pokud chcete generovat přírůstková data, nastavte tuto položku na **Ne**.
6. V poli **Kód období** vyberte období, ve kterém mají být data generována. Když vyberete kód období, není nutné definovat počáteční a koncové datum.
7. Když necháte pole **Kód období** prázdné, vyberte konkrétní data zahájení a ukončení pro generování dat.
8. Vyberte **OK**.

> [!NOTE]
> Tato akce bude distribuovat obecná data do tabulky **ResRollup** napříč všemi společnostmi ve vašem prostředí, takže dávkovou úlohu je třeba spustit pouze v jedné právnické osobě. Tato dávková úloha je nutná pro všechny pohledy **Dostupnost zdrojů**. Pokud tato dávková úloha není spuštěna, data tabulky **ResRollup** budou generována za chodu, což může chvíli trvat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]