---
title: Skutečné hodnoty
description: Tento článek poskytuje informace o tom, jak pracovat se skutečnými hodnotami v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924790"
---
# <a name="actuals"></a>Skutečné hodnoty

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Skutečné hodnoty představují zkontrolovaný a schválený finanční a časový plán postupu v projektu. Jsou vytvořeny, když jsou schváleny záznamy o čase, výdajích a spotřebě materiálu, záznamy v deníku a faktury.

> [!IMPORTANT]
> Skutečné hodnoty by neměly být upravovány ani odstraňovány ze systému. V opačném případě může být nepříznivě ovlivněna finanční integrita a jakákoli integrace s jinými finančními a účetními systémy. Microsoft Dynamics 365 Project Operations umožňuje použít stornování a nahrazení skutečných hodnot k úpravě skutečných hodnot v různých bodech životního cyklu obchodních procesů vašich projektů.

## <a name="recording-actuals-based-on-project-events"></a>Záznam skutečných hodnot na základě událostí projektu

Aplikace Project Operations zaznamenává finanční transakce, ke kterým dojde během životního cyklu projektové zakázky, jako skutečné hodnoty. Vytváření skutečných hodnot při různých událostech v životním cyklu se liší v závislosti na tom, zda projektové zapojení používá model účtování podle času a materiálu nebo model účtování s pevnou cenou a zda je ve fázi předprodeje nebo jde o interní projekt.

Následující články vysvětlují dopad na tabulku Skutečné hodnoty u různých událostí pro různé varianty:

- [Dopad na skutečné hodnoty u časového a materiálového zapojení](ActualsonTM.md)
- [Dopad na skutečné hodnoty u zapojení s pevnou cenou](ActualonFP.md)
- [Dopad na skutečné hodnoty během předprodejní fáze zapojení](ActualonPreSales.md)
- [Dopad na skutečné hodnoty u interního projektu](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
