---
title: Granty projektu
description: Toto téma vysvětluje, jak vytvořit nebo upravit grant.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
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
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073961"
---
# <a name="project-grants"></a>Granty projektu

[!include [banner](../includes/banner.md)]

Grant je dar peněz na konkrétní účel nebo projekt. Obvykle existují omezení, jak lze grant použít. V části Řízení projektů a účetnictví můžete granty zadávat a sledovat, a definovat jejich vztahy k projektům a projektovým smlouvám. Můžete například provádět následující úlohy.

- Přidružte granty k projektům a zdrojům financování prostřednictvím odkazů na stránky **Projekt** a **Podrobnosti o projektové smlouvě**.
- Zadejte a sledujte změny grantu při jeho přechodu z jednoho stavu do druhého.
- Zadejte a sledujte náklady, požadované částky a přidělené částky.
- Vytvořte hlavní granty a přidružte k nim dílčí granty.

Grant můžete vytvořit zadáním všech podrobností v novém záznamu, nebo můžete zkopírovat podrobnosti z existujícího grantu a poté je aktualizovat.

## <a name="create-a-new-grant"></a>Vytvoření nového grantu

1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Granty** \> **Granty**.
2. Vyberte příkaz **Nový** \> **Grant**.
3. Na stránce s podrobnostmi o grantu na pevné záložce **Všeobecné** zapište v poli **ID grantu** alfanumerický identifikátor grantu.
4. V poli **Název grantu** zadejte název nového grantu.
5. V poli **Popis** přidejte podrobnosti o novém grantu.

    Většina ostatních polí na stránce je volitelná a můžete v nich zadat tolik informací, kolik chcete.

    Následující seznam popisuje informace, které jsou uvedeny na každé pevné záložce stránky s podrobnostmi o grantu:

    - **Všeobecné** – Zadejte název grantu, stav, popis, účel a částku.
    - **Kontaktní informace** – Zadejte podrobnosti o zaměstnancích, oddělení, které spravuje grant, a zdroji grantu (zákazníkovi nebo organizaci). Můžete také určit, že vaše organizace je předávací entitou, která obdrží grant, a poté jej předá jinému příjemci. Vyberte **Přidat** a přidejte kontaktní informace, jako jsou telefonní čísla a e-mailové adresy organizace, která poskytuje grant.
    - **Data a termíny** – Zadejte data, která se vztahují k grantu a žádosti o grant. Mezi příklady patří koncové datum žádosti, datum podání a datum schválení nebo zamítnutí grantu.
    - **Přidružené projekty a projektové smlouvy** – Na této pevné záložce můžete zadat informace, pouze pokud je pole **Stav udělení** na pevné záložce **Všeobecné** nastaveno na **Aktivní** nebo **Přidělený**. Vyberte jednu z následujících možností k dokončení související úlohy:

        - **Přidat zdroj financování** – Přidejte nový zdroj financování grantu. Nyní můžete zadat všechny podrobnosti nebo můžete použít výchozí informace a později je aktualizovat.
        - **Přidat projektovou smlouvu** – Přidejte nebo aktualizujte informace o projektové smlouvě.
        - **Přidat projekt** - Přidejte nebo aktualizujte podrobnosti projektu.

    - **Nastavení** – Zadejte podrobnosti o odpovídajících fondech, pokud jsou tyto informace vyžadovány. Mnoho organizací, které udělují granty, vyžaduje, aby příjemci utratili konkrétní částku svých vlastních peněz nebo zdrojů, která má odpovídat částce udělené v grantu. V poli **Místní projekt nebo ID sledování** můžete zadat identifikátor, který se liší od identifikátoru projektu.

        > [!NOTE]
        > Pokud bude část grantu udělena jiné organizaci, nastavte možnost **Další poskytovatel grantu** na **Ano**. U grantů, které se udělují ve Spojených státech, můžete určit, zda bude grant udělen na základě státního nebo federálního mandátu.

    - **Podrobnosti o čerpání** – Přidejte nebo aktualizujte informace o tom, jak často lze prostředky z grantu vybírat, účtovat nebo utrácet.

## <a name="create-a-new-grant-from-a-copy"></a>Vytvoření nového grantu z kopie

1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Granty** \> **Granty**.
2. Vyberte příkaz **Nový** \> **Kopírovat z grantu**.
3. Zadejte alfanumerický identifikátor a název nového grantu a poté vyberte **OK**.
4. Na stránce s podrobnostmi o grantu zkontrolujte detaily zkopírovaného grantu a proveďte potřebné změny. Většina polí na stránce je volitelná.

## <a name="view-or-modify-grant-details"></a>Zobrazení nebo úprava podrobností grantu

1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Granty** \> **Granty**.
2. Vyberte grant, který chcete upravit.
3. V podokně akcí na kartě **Grant** vyberte ve skupině **Udržovat** příkaz **Upravit**.
4. Zkontrolujte podrobnosti o grantu a proveďte potřebné změny.
