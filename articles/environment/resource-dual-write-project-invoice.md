---
title: Integrace projektové faktury
description: Toto téma poskytuje informace o integraci fakturaci zákazníka Project Operations s použitím duálního zápisu.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996558"
---
# <a name="project-invoice-integration"></a>Integrace projektové faktury

Toto téma poskytuje informace o integraci fakturaci zákazníka Project Operations s použitím duálního zápisu.

V Project Operations projektový manažer spravuje nevyřízené účty fakturace projektu a vytváří proforma fakturu pro zákazníka v Microsoft Dataverse. Na základě této proforma faktury vytvoří účetní pohledávek nebo účetní projektu zákaznickou fakturu. Integrace duálního zápisu zajišťuje synchronizaci údajů proforma faktury do aplikace Finance and Operations. Po zaúčtování faktury orientované na zákazníka systém aktualizuje příslušné skutečné hodnoty projektu Dataverse s údaji účetnictví. Následující obrázek poskytuje koncepční přehled této integrace na vysoké úrovni.

   ![Integrace projektové faktury](./media/DW5Invoicing.png)

Poté, co vedoucí projektu potvrdí proforma fakturu v Dataverse, údaje záhlaví proforma faktury se synchronizují do aplikace Finance and Operations pomocí mapu tabulky se duálním zápisem **Návrh faktury projektu V2 (faktury)**. Toto je jednosměrná integrace z Dataverse do aplikací Finance and Operations. Vytváření nebo mazání návrhů faktur projektu přímo v aplikacích Finance and Operations není podporováno.

Potvrzení faktury v Dataverse také spustí obchodní logiku k vytvoření záznamů souvisejících s fakturací v entitě **Skutečné hodnoty**. Tyto záznamy jsou synchronizovány do aplikací Finance and Operations pomocí mapy tabulky s duálním zápisem **Skutečné hodnoty integrace Project Operations (msdyn\_actuals)**. Další informace viz [Odhady a skutečné hodnoty projektu](resource-dual-write-estimates-actuals.md). 

Řádky návrhu faktury projektu jsou vytvářeny periodickým procesem **Import pracovního formuláře**. Tento proces je založen na údajích fakturovaných skutečných hodnot prodeje v tabulce **Skutečné pracovní hodnoty**. Další informace viz [Správa návrhů faktur projektu](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
