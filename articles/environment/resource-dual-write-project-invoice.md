---
title: Integrace projektové faktury
description: Tento článek poskytuje informace o integraci duálního zápisu Project Operations pro fakturaci zákazníků.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912094"
---
# <a name="project-invoice-integration"></a>Integrace projektové faktury

Tento článek poskytuje informace o integraci duálního zápisu Project Operations pro fakturaci zákazníků.

V Project Operations projektový manažer spravuje nevyřízené účty fakturace projektu a vytváří proforma fakturu pro zákazníka v Microsoft Dataverse. Na základě této proforma faktury vytvoří účetní pohledávek nebo účetní projektu zákaznickou fakturu. Integrace duálního zápisu zajišťuje synchronizaci podrobností proforma faktury s finančními a provozními aplikacemi. Po zaúčtování faktury orientované na zákazníka systém aktualizuje příslušné skutečné hodnoty projektu Dataverse s údaji účetnictví. Následující obrázek poskytuje koncepční přehled této integrace na vysoké úrovni.

   ![Integrace projektové faktury.](./media/DW5Invoicing.png)

Poté, co projektový manažer potvrdí proforma fakturu v Dataverse, informace záhlaví proforma faktury se synchronizují s finančními a provozními aplikacemi pomocí mapy tabulek s duálním zápisem **Návrh projektové faktury V2 (faktury)**. Jedná se o jednosměrnou integraci z Dataverse do finančních a provozních aplikací. Vytváření nebo odstraňování návrhů faktur projektu přímo ve finančních a provozních aplikacích není podporováno.

Potvrzení faktury v Dataverse také spustí obchodní logiku k vytvoření záznamů souvisejících s fakturací v entitě **Skutečné hodnoty**. Tyto záznamy jsou synchronizovány s finančními a provozními aplikacemi pomocí mapy tabulek s duálním zápisem **Skutečné hodnoty integrace Project Operations (msdyn\_actuals).** Další informace viz [Odhady a skutečné hodnoty projektu](resource-dual-write-estimates-actuals.md). 

Řádky návrhu faktury projektu jsou vytvářeny periodickým procesem **Import pracovního formuláře**. Tento proces je založen na údajích fakturovaných skutečných hodnot prodeje v tabulce **Skutečné pracovní hodnoty**. Další informace viz [Správa návrhů faktur projektu](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
