---
title: Projektujte prodejní objednávky pro časové a materiální projekty
description: Toto téma vysvětluje, jak vytvořit prodejní objednávky založené na projektech času a materiálu.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750289"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektujte prodejní objednávky pro časové a materiální projekty

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Toto téma popisuje, jak vytvořit prodejní objednávku pro projekt. Objednávky odběratele lze vytvořit pouze pro projekty typu **čas a materiál**.

Pokud má časový a věcný projekt na projektové smlouvě více zdrojů financování, musíte povolit **Povolit prodejní objednávky u projektů s více zdroji financování** parametr na stránce **Parametry řízení projektu a účetnictví**. 

> [!NOTE]
> - Podpora prodejních objednávek projektů s více zdroji financování je k dispozici od vydání aplikace 10.0.2 a vyšší.
> - Parametr umožňující podporu objednávek projektu s více zdroji financování bude odstraněn ve vlně vydání z dubna 2020, po které bude funkce vždy povolena.

Zakázky prodeje založené na projektu můžete vytvořit dvěma způsoby:

- Přejděte na projekt. V podokně akcí vyberte **Spravovat > Úkoly položek > Prodejní objednávka**. Informace o projektu budou výchozí pro prodejní objednávku z projektu. Pokud má projektová smlouva více než jeden zdroj financování, budete muset vybrat zdroj financování a nastavit zákazníka pro prodejní objednávku. Pokud pro projekt existuje pouze jeden zdroj financování, zákazník se nastaví automaticky.
- Přejděte na stránku seznamu **Všechny prodejní objednávky** a vytvořte novou prodejní objednávku. Budete muset vybrat projekt pro prodejní objednávku. Po výběru projektu bude zákazník nastaven ze zdroje financování, nebo budete muset vybrat zdroj financování, pokud má projektová smlouva více zdrojů financování.

