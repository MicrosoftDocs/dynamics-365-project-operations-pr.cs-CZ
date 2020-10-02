---
title: Jednotky a skupiny jednotek
description: Tento téma poskytuje informace o tom, jak vytvořit jednotky a skupiny jednotek v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898748"
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
