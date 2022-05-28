---
title: Eliminace odhadu projektu
description: Tento téma poskytuje informace o eliminaci odhadu projektu po jeho dokončení.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 267b5ffab7ef3a6776c31100deea81fb523752b6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684082"
---
# <a name="eliminate-a-project-estimate"></a>Eliminace odhadu projektu

[!include [banner](../includes/banner.md)]

Projektové odhady poskytují finanční přehled odhadované a plánované práce na projektu. Chcete-li pracovat s odhady projektu, musíte projekt připojit k projektu odhadu. Projekt odhadu je vždy založen na existujícím projektu, na jeden projekt odhadu však může odkazovat více projektů. K projektům odhadu lze připojit pouze investiční projekty s pevnou cenou a tyto projekty musí patřit do stejné skupiny projektů jako projekt odhadu.

Chcete-li eliminovat projekt odhadu, musí být hotový. Následující kroky vysvětlují, jak eliminovat odhad.

1. Přejděte do části **Řízení projektů a účetnictví** > **Všechny projekty** a otevřete projekt. 
2. Na kartě **Spravovat** vyberte **Odhady** a na stránce **Odhad** vyberte **Eliminovat**.
3. Na stránce **Eliminovat odhad** stránka na kartě **Obecné** nastavte následující možnosti:

   - **Kód období**: Vyberte kód období a vyberte příslušné projekty odhadu. 
   - **Datum odhadu**: Vyberte příslušné datum odhadu pro eliminaci.
   - **Eliminovat s varováními WIP**: Tuto možnost povolte, chcete-li uvádět oznámení, když bude eliminován odhad, který je spojen s nedokončenou prací (WIP). Pokud tato možnost není povolena, eliminace nemůže pokračovat, pokud existují neodhadnuté transakce. 
   > [!NOTE]
   > Tato možnost je k dispozici pouze v případě, že je na projekt odhadu použita eliminace. Není k dispozici, pokud používáte pravidelné zveřejňování účtování. Toto nastavení funguje s nastavením na kartě **Odhad** na stránce **Parametry projektu** ve skupině polí **Povolit eliminaci, když existují neodhadnuté transakce**.
   - **Nastavit fázi na Dokončeno**: Povolením této možnosti nastavíte fázi odhadu projektu na **Hotovo** po spuštění eliminace.
   - **Vytisknout seznam odhadů**: Vyberte informace, které mají být zahrnuty při tisku seznamu odhadů.
   - **Zobrazit Infolog**: Povolením této možnosti zobrazíte Infolog.
   - **Datum zaúčtování**: Vyberte datum zaúčtování odhadu do hlavní knihy.

4.  Vyberte **OK**.
5. Po dokončení procesu eliminace se zobrazí eliminovaný projekt odhadu se zápornou hodnotou. 

Pokud jste neměli v úmyslu odhad eliminovat, můžete vybrat eliminovat odhad a vybrat **Vrátit eliminaci**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]