---
title: Synchronizace kapacity zdroje
description: Toto téma poskytuje informace o tom, jak synchronizovat kapacitu zdroje napříč kalendáři a projekty.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288551"
---
# <a name="synchronize-resource-capacity"></a>Synchronizace kapacity zdroje

[!include [banner](../includes/banner.md)]

Procesy pro synchronizaci zdrojů pomáhají zaručit, že informace kalendáře a základního kalendáře se postupně dostávají do plánování zdrojů projektu. Pokud se kalendář změní, procesy provedou požadované aktualizace plánování projektových zdrojů. Procesy také pomáhají zlepšit výkon, protože informace o zdrojích kalendáře jsou synchronizovány předem. Aktualizace informací o plánování prostředků proto probíhají rychleji. Doporučujeme naplánovat spouštění procesů v dávce namísto po jednom. V opačném případě existuje riziko, že někdo zapomene hraniční datumy období, kdy byly informace naposledy synchronizovány. Pokud se nepoužívají správné hraniční datumy, mohou se během synchronizace datumů objevit mezery.

![Synchronizace kalendáře](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synchronizace souhrnů kapacity zdrojů

Proces synchronizace je navržen tak, aby synchronizoval všechny informace kalendáře zdrojů. Tyto informace zahrnují informace základního kalendáře o všech změnách v tabulce kapacity kalendáře zdrojů projektu. Pokud jsou do projektu přidány nové zdroje, synchronizace pomáhá zaručit, že jsou k dispozici aktualizované informace kalendáře. Tuto synchronizaci lze provést kdykoli.

Doporučujeme vám použít dávkovou aktualizaci. Možnosti jsou k dispozici během synchronizace rezervací kapacity.

1. Vyberte **Správa projektů a účetnictví** &gt; **Periodické** &gt; **Synchronizace kapacity** &gt; **Synchronizace souhrnů kapacity zdrojů**.
2. Nastavte možnosti v následující tabulce.

    | Možnost      | Popis |
    |-------------|-------------|
    | Kód období | Volitelně vyberte kód intervalu datumů hlavní knihy a nastavte tak počáteční a konečné datum procesu synchronizace souhrnů kapacity zdrojů. |
    | Počáteční datum  | Zadejte počáteční datum procesu synchronizace souhrnů kapacity zdrojů. |
    | Koncové datum    | Zadejte koncové datum procesu synchronizace souhrnů kapacity zdrojů. |

[![Proces synchronizace](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]