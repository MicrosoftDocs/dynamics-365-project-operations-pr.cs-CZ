---
title: Měna
description: Tento téma poskytuje informace o tom, jak přidávat a odebírat typy měn v Project Operations.
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
ms.openlocfilehash: 7368dc5d4901e8083f15b0174b7cc58a6b6dbd91
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277465"
---
# <a name="currency"></a>Měna

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Měny určují ceny produktů, které obsahuje katalog produktů, a náklady na transakce, jako jsou prodejní objednávky. Pokud se vaši zákazníci nacházejí v různých zeměpisných oblastech, přidejte jejich měny, aby bylo možné spravovat transakce. Přidejte měny, které jsou nejvhodnější pro vaše současné i budoucí obchodní potřeby.  

> [!NOTE]
> Pokud je vaše prostředí Common Data Service, jste v centru pro správu Power Platform a vyberete stránku **Měny** (**Prostředí** > [vyberte prostředí]> **Nastavení** > **Obchodování** > **Měny**), stránka bude prázdná. Důvodem je, že nastavení měny není podporováno v prostředích Common Data Service.

## <a name="add-a-currency"></a>Přidání měny  
Než zahájíte tento postup, ověřte, zda vaše role zabezpečení obsahuje oprávnění správce systému. 

1. V centru pro správu Power Platform vyberte prostředí. 
2. Vyberte **Nastavení** > **Obchodní**.
3. Vyberte **Měny**.  
4. Vyberte **Nové**.  
5. Podle potřeby doplňte odpovídající informace.  


   |          Pole          |                                                                                                                                                                                                                                                                                                                                                                            Popis                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Typ měny**    | - **Systém** – Tuto možnost vyberte, pokud chcete používat měny dostupné v modelem řízených aplikacích v Dynamics 365. Výběrem tlačítka **Vyhledávání** můžete měnu vyhledat. Když vyberete kód měny, pro vybrané měny se automaticky přidají **Název měny** a **Symbol měny**.<br />- **Vlastní** – Tuto možnost vyberte, pokud chcete přidat měnu, která není dostupná v modelem řízených aplikacích v Dynamics 365. V tomto případě je nutné ručně zadat hodnoty pro položky **Kód měny**, **Přesnost měny**, **Název měny**, **Symbol měny** a **Převod měny**. |
   |    **Kód měny**    |                                                                                                                                                                                                                                                                                                                                            Zkratka měny. Například **USD** pro americký dolar.                                                                                                                                                                                                                                                                                                                                            |
   | **Přesnost měny**  |                                                                                                                                                                                  Zadejte počet desetinných míst, jež chcete použít pro tuto měnu.  Můžete přidat hodnotu mezi 0 a 4. **Poznámka:** Pokud jste nastavili hodnotu přesnosti v dialogovém okně **Nastavení systému**, tato hodnota se zde zobrazí.                                                                                                                                                                                  |
   |    **Název měny**    |                                                                                                                                                                                                                                         Pokud jste vybrali kód měny ze seznamu dostupných měn v modelem řízených aplikacích v Dynamics 365, zobrazí se zde název měny pro vybraný kód. Pokud jste vybrali jako typ měny položku **Vlastní**, zadejte název měny.                                                                                                                                                                                                                                          |
   |   **Symbol měny**   |                                                                                                                                                                                                                                                                      Pokud jste vybrali kód měny ze seznamu dostupných měn, zobrazí se zde symbol pro vybranou měnu. Pokud jste vybrali jako typ měny položku **Vlastní**, zadejte symbol nové měny.                                                                                                                                                                                                                                                                       |
   | **Převod měny** |                                                                                                                                                                                                                                     Zadejte hodnotu vybrané měny vzhledem k jednomu americkému dolaru. Jedná se o částku, pomocí které se vybraná měna převádí na základní měnu. **Důležité:** Nazapomeňte tuto hodnotu často aktualizovat, aby se zabránilo nepřesným výpočtům v transakcích.                                                                                                                                                                                                                                      |


6. Jakmile budete hotovi, na panelu příkazů vyberte tlačítko **Uložit** nebo **Uložit a zavřít**.  

   > [!TIP]
   >  Chcete-li měnu upravit, vyberte měnu a poté zadejte nebo vyberte nové hodnoty.  

## <a name="delete-a-currency"></a>Odstranění měny  

1. V centru pro správu Power Platform vyberte prostředí. 
2. Vyberte **Nastavení** > **Obchodní**.
3. Vyberte **Měny**.  
4. Ze zobrazeného seznamu měn vyberte měnu, kterou chcete odstranit.  
5. Vyberte **Odstranit**.  
6. Potvrďte odstranění.  

> [!IMPORTANT]
>  Nelze odstranit měny, které se používají v jiných záznamech. Můžete je pouze deaktivovat. Při deaktivaci záznamů měny nedojde k odebrání informací o měně uložených v existujících záznamech, například příležitostech nebo objednávkách. Deaktivovanou měnu však nebudete moci vybrat pro nové transakce.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]