---
title: Integrace projektové faktury
description: Toto téma poskytuje informace o integraci fakturaci zákazníka Project Operations s použitím duálního zápisu.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955723"
---
# <a name="project-invoice-integration"></a>Integrace projektové faktury

Toto téma poskytuje informace o integraci fakturaci zákazníka Project Operations s použitím duálního zápisu.

V Project Operations projektový manažer spravuje nevyřízené účty fakturace projektu a vytváří proforma fakturu pro zákazníka v Microsoft Dataverse. Na základě této proforma faktury vytvoří účetní pohledávek nebo účetní projektu zákaznickou fakturu. Integrace duálního zápisu zajišťuje synchronizaci údajů proforma faktury do aplikace Finance and Operations. Po zaúčtování faktury orientované na zákazníka systém aktualizuje příslušné skutečné hodnoty projektu Dataverse s údaji účetnictví. Následující obrázek poskytuje koncepční přehled této integrace na vysoké úrovni.

   ![Integrace projektové faktury](./media/DW5Invoicing.png)

Poté, co vedoucí projektu potvrdí proforma fakturu v Dataverse, údaje záhlaví proforma faktury se synchronizují do aplikace Finance and Operations pomocí mapu tabulky se duálním zápisem **Návrh faktury projektu V2 (faktury)**. Toto je jednosměrná integrace z Dataverse do aplikací Finance and Operations. Vytváření nebo mazání návrhů faktur projektu přímo v aplikacích Finance and Operations není podporováno.

Potvrzení faktury v Dataverse také spustí obchodní logiku k vytvoření záznamů souvisejících s fakturací v entitě **Skutečné hodnoty**. Tyto záznamy jsou synchronizovány do aplikací Finance and Operations pomocí mapy tabulky s duálním zápisem **Skutečné hodnoty integrace Project Operations (msdyn\_actuals)**. Další informace viz [Odhady a skutečné hodnoty projektu](resource-dual-write-estimates-actuals.md). 

Řádky návrhu faktury projektu jsou vytvářeny periodickým procesem **Import pracovního formuláře**. Tento proces je založen na údajích fakturovaných skutečných hodnot prodeje v tabulce **Skutečné pracovní hodnoty**. Další informace viz [Správa návrhů faktur projektu](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
