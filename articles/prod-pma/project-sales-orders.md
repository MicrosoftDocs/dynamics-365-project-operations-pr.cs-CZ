---
title: Projektujte prodejní objednávky pro časové a materiální projekty
description: Tento článek vysvětluje, jak vytvářet prodejní objednávky na základě projektů určených časem a materiálem.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3a040de6d22b626b9e3d462272f43c5763b5b90f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933806"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektujte prodejní objednávky pro časové a materiální projekty

[!include[banner](../includes/banner.md)]

Tento článek popisuje způsob vytvoření prodejní objednávky pro projekt. Objednávky odběratele lze vytvořit pouze pro projekty typu **čas a materiál**.

Pokud má časový a věcný projekt na projektové smlouvě více zdrojů financování, musíte povolit **Povolit prodejní objednávky u projektů s více zdroji financování** parametr na stránce **Parametry řízení projektu a účetnictví**. 

> [!NOTE]
> - Podpora prodejních objednávek projektů s více zdroji financování je k dispozici od vydání aplikace 10.0.2 a vyšší.
> - Parametr umožňující podporu objednávek projektu s více zdroji financování bude odstraněn ve vlně vydání z dubna 2020, po které bude funkce vždy povolena.

Zakázky prodeje založené na projektu můžete vytvořit dvěma způsoby:

- Přejděte na projekt. V podokně akcí vyberte **Spravovat > Úkoly položek > Prodejní objednávka**. Informace o projektu budou výchozí pro prodejní objednávku z projektu. Pokud má projektová smlouva více než jeden zdroj financování, budete muset vybrat zdroj financování a nastavit zákazníka pro prodejní objednávku. Pokud pro projekt existuje pouze jeden zdroj financování, zákazník se nastaví automaticky.
- Přejděte na stránku seznamu **Všechny prodejní objednávky** a vytvořte novou prodejní objednávku. Budete muset vybrat projekt pro prodejní objednávku. Po výběru projektu bude zákazník nastaven ze zdroje financování, nebo budete muset vybrat zdroj financování, pokud má projektová smlouva více zdrojů financování.



[!INCLUDE[footer-include](../includes/footer-banner.md)]