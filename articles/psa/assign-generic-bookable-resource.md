---
title: Přiřaďte k úkolu a projektovému týmu obecné rezervovatelné zdroje
description: Toto téma obsahuje informace o rezervaci obecných zdrojů pro úkoly a projektové týmy.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: a1e22337d3fd3e7ff4147a9547fd3c272f4185d3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009383"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Přiřaďte k úkolu obecný rezervovatelný zdroj a vygenerujte požadavky na zdroj 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kromě rezervace a přiřazování pojmenovaných nebo skutečných zdrojů pro váš projekt můžete k projektovým úkolům přiřadit obecné zdroje. Tyto zdroje mohou sloužit jako zástupné symboly pro pojmenované zdroje, dokud nebudete připraveni k obsazení vašeho projektu pojmenovanými zdroji. 

1. V Project Service Automation (PSA) otevřete stránku **Projekt** a na kartě **Plán** zadejte do buňky plánu **Zdroj** název pozice obecného zdroje. Nebo klepnutím na ikonu **Zdroje** v buňce otevřete okno pro výběr zdroje a zadejte název obecného zdroje, který chcete vytvořit.

![Vytvoření a přiřazení obecného člena týmu](media/RM-how-to-9.png)

Otevře se panel **Vytvořit: Člen projektového týmu**. 

2. Zadejte roli a organizační jednotku obecného zdroje člena týmu a pak klepněte na **Uložit**.

![Vytvoření obecného člena týmu](media/RM-how-to-10.png)

3. Poté, co jste vytvořili nový obecný zdroj člena týmu, je přiřazen k úkolu. Tento obecný zdroj můžete dále přiřadit k dalším úkolům v plánu úkolů.

![Přiřazení existujícího obecného člena týmu k úkolům](media/RM-how-to-11.png)

4. Po přiřazení obecného zdroje můžete vygenerovat požadavek na zdroj a splnit ji přímou rezervací nebo odesláním žádosti o zdroj správci zdrojů.

![Generování požadavku na obecného člena týmu](media/RM-how-to-12.png)

V mřížce člena týmu můžete kromě toho, že budete moci použít výběr zdroje výše uvedeným způsobem, přidat obecné zdroje přímo. Zdroje jsou přidávány prostřednictvím požadavku na zdroj, který je založen na počátečních a koncových datech a metodě přidělení určené v panelu **Vytvořit: Člen projektového týmu**.

Rozdíl můžete vidět, pokud přidáte obecného člena týmu přímo a potom k tomuto obecnému zdroji přiřadíte více úkolů, než je počet hodin potřebný k pokrytí. Chcete-li vygenerovat požadavek na vyrovnání požadovaných hodin oproti přiřazením, klikněte na **Generovat požadavek**.

Můžete také kliknout na odkaz **Požadavek na zdroj** v mřížce týmu a tím otevřít požadavek a přidat dovednosti, upřednostňované zdroje atd.

![Požadavek na zdroj](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]