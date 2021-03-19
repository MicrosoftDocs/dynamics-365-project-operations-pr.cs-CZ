---
title: Jednotky a skupiny jednotek
description: Toto téma obsahuje informace, jak vytvářet jednotky a skupiny jednotek v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277330"
---
# <a name="units-and-unit-groups"></a>Jednotky a skupiny jednotek

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Jednotky jsou množství nebo míry, ve kterých své produkty nebo služby prodáváte. Pokud například prodáváte zahradnické potřeby, můžete prodávat semena v jednotkách sáčky, krabice a palety. Skupina jednotek je kolekce těchto různých jednotek.

Chcete-li provést kroky v tomto tématu, ujistěte se, že vám byla přiřazena role správce systému nebo Sales Professional Manager nebo že máte ekvivalentní oprávnění.

## <a name="create-a-unit-group"></a>Vytvoření skupiny jednotek

1. V mapě webu vyberte **Jednotky**.
2. Zvolte **Nová** a v dialogovém okně **Vytvořit skupinu jednotky** zadejte název jednotky.
3. V poli **Primární jednotka** zadejte nejnižší běžnou měrnou jednotku, ve které bude produkt prodáván. Můžete například zadat „kus“ nebo „unce“.
4. Vyberte **OK**.

## <a name="add-units-to-a-unit-group"></a>Přidání jednotek do skupiny jednotek

1. Otevřete skupinu jednotek a na kartě **Související** vyberte **Jednotky**. Uvidíte, že primární jednotka je již přidána.
2. Vyberte **Přidat novou jednotku** a na stránce **Rychlé vytvoření: Jednotka** zadejte do pole **Název** název jednotky.
3. Do pole **Množství** zadejte množství, které bude jednotka obsahovat. Pokud například krabice obsahuje dva kusy, zadejte „2“. 
4. V poli **Základní jednotka** vyberte základní jednotku pro stanovení nejnižší měrné jednotky pro danou jednotku. Můžete například vybrat „Kus“.
5. Zvolte **Uložit**:


[!INCLUDE[footer-include](../includes/footer-banner.md)]