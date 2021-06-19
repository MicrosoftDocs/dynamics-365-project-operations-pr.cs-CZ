---
title: Přenos projektových rozpočtů na konci fiskálního roku
description: Tento článek poskytuje informace o tom, jak převést zbývající částky rozpočtu do budoucích let a jak vytvořit podrobnosti registru rozpočtu.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: be3dc039b92e88cac6f6b3b7f72bc32ecf587539
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008033"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Přenos projektových rozpočtů na konci fiskálního roku

[!include [banner](../includes/banner.md)]

Při práci na víceletém projektu můžete mít na konci fiskálního roku zbývající rozpočet. Můžete převést zbývající částky rozpočtu do budoucího roku a vytvořit podrobnosti registru rozpočtu pro částky v přidružených účtech hlavní knihy. Než převedete zbývající částky, zkontrolujte a analyzujte zbývající částky rozpočtu.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Kontrola a analýza zbývajících částek rozpočtu

Proveďte následující kroky, abyste zkontrolovali částky rozpočtu na konci roku u projektů, ale částky nepřenášejte.

1. Přejděte do **Řízení projektů a účetnictví** > **Periodické** > **Rozpočty** > **Převést rozpočty do dalšího období**. 
2. Na stránce **Proces převedení projektového rozpočtu do dalšího období** na kartě **Možnosti na konci roku** ověřte, že není zapnuta možnost **Převést do dalšího období zbývající částky rozpočtu projektu**.
3. Na kartě **Parametry** v poli **Rozpočtový rok projektu** vyberte fiskální rok, u kterého chcete zobrazit zbývající částku rozpočtu. 
4. V poli **Počáteční fiskální rok** vyberte fiskální rok, u kterého chcete zobrazit zbývající částku rozpočtu. 
5. V poli **Z modelu prognózy** vyberte hodnotu **Zbývající rozpočet**. 
6. Chcete-li zahrnout projekty, které splňují vámi vybraná kritéria a nemají zbývající rozpočet, vyberte **Zobrazit nulový zůstatek**.  
7. Na kartě **Vyberte rozpočty** zvolte možnost **Načíst všechny rozpočty**, aby se načetly všechny rozpočty odpovídající vybraným kritériím, a poté vyberte **Zpracovat**. 
8. Chcete-li navrhnout databázový dotaz, který do podokna načte konkrétní sadu rozpočtů, vyberte možnost **Načíst vybrané rozpočty**.

Chcete-li další informace o konkrétním řádku v podokně, vyberte řádek a poté vyberte příkaz **Zobrazit podrobnosti rozpočtu** nebo **Zobrazit účty**.

## <a name="carry-forward-remaining-budget-amounts"></a>Převod zbývajících částek rozpočtu 

Při zpracování zbývajících částek rozpočtu můžete v hlavní knize vytvořit transakce pro částky, které přenášíte. Chcete-li vytvořit transakce hlavní knihy, proveďte kroky v části [Převod částek rozpočtu a vytvoření transakcí hlavní knihy](#carry-forward). 

> [!NOTE]
> Částky rozpočtu, které jsou převedeny, jsou přeneseny do modelu prognózy, který je vybrán na stránce **Modely prognóz** jako model prognózy převodu.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Převod částek rozpočtu a vytvoření transakcí hlavní knihy

1.  Vyberte položku nabídky **Řízení projektů a účetnictví** > **Periodické** > **Rozpočty** > **Převést rozpočty do dalšího období**. 
2. Na stránce **Proces převedení projektového rozpočtu do dalšího období** vyberte **Konec roku** a poté povolte možnosti **Převést zbývající částky rozpočtu projektu** a **Vytvořit položky registru rozpočtu v hlavní knize**. 
3. Na kartě **Parametry** ve skupině polí **Parametry projektu** vyberte následující:

   - **Rozpočtový rok projektu**: Vyberte začátek fiskálního roku, u kterého chcete zobrazit zbývající částky rozpočtu. 
   - **Zisk a ztráta**: Vytvořte transakce zisků a ztrát v hlavní knize. 
   -  **NV**: Vytvořte transakce probíhajících prací (nedokončené výroby) v hlavní knize.
   -  **Mzdy**: Vytvořte transakce přidělení mezd v hlavní knize. 

5. Ve skupině polí **Hlavní kniha** zadejte následující informace: 

   - V poli **Počáteční fiskální rok** vyberte fiskální rok, do kterého chcete přenést zbývající částky projektových rozpočtů. Výchozí hodnota je jeden rok po hodnotě v poli **Rozpočtový rok projektu**.
   -  V poli **Období převedení do dalšího období** vyberte období, pro které chcete vytvořit podrobnosti registru rozpočtu v hlavní knize. Jedná se obvykle o první období v úvodním fiskálním roku.

6. Ve skupině polí **Kopírovat z/do** zadejte následující informace:

   - V poli **Z modelu prognózy** vyberte model prognózy projektového rozpočtu spojený se zbývajícími částkami rozpočtu, které chcete pro projekty převést. 
   - V poli **Do rozpočtového modelu hlavní knihy** vyberte model rozpočtu hlavní knihy spojený s částkami rozpočtu, které chcete převést do hlavní knihy. 
   -  Vyberte příkaz **Převést prodejní měnu**, chcete-li použít prodejní měnu projektu pro transakce hlavní knihy, které se vytvoří při přenosu částek rozpočtu pro projekty. Pokud tato možnost není vybrána, transakce používají účetní měnu. 
   -  Vyberte možnost **Zobrazit nulový zůstatek**, chcete-li zahrnout projekty, které nemají žádné zbývající částky rozpočtu, ale splňují další kritéria, která vyberete v projektech zobrazených v dolním podokně.

7. Na kartě **Vyberte rozpočty** zvolte možnost **Načíst všechny rozpočty**, aby se načetly všechny rozpočty odpovídající vybraným kritériím. Dáváte-li přednost návrhu databázového dotazu, který do podokna načte konkrétní sadu projektových rozpočtů, vyberte možnost **Načíst vybrané rozpočty**.
8. U každého projektu, který chcete zpracovat, vyberte možnost na začátku řádku pro projekt.

    > [!TIP]
    > Chcete-li vybrat všechny nebo většinu projektů, zaškrtněte políčko v levém horním levém rohu. Chcete-li vyloučit nějaký projekt ze zpracování, vypněte zaškrtávací políčko pro tento projekt.

9. Chcete-li přenést zbývající částky rozpočtu pro vybrané projekty do vybraného fiskálního roku a vytvořit podrobnosti registru rozpočtu v hlavní knize, vyberte příkaz **Zpracovat**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Převod částek rozpočtu bez vytvoření transakcí hlavní knihy

1. Přejděte do **Řízení projektů a účetnictví** > **Periodické** > **Rozpočty** > **Převést rozpočty do dalšího období**.
2. Na stránce **Proces převedení projektového rozpočtu do dalšího období** na kartě **Možnosti na konci roku** zapněte možnost **Převést do dalšího období zbývající částky rozpočtu projektu**.
3. Ve skupině **Parametry** v poli **Rozpočtový rok projektu** vyberte fiskální rok, u kterého chcete zobrazit zbývající částky rozpočtu.
4. Ve skupině **Kopírovat z/do** zadejte následující informace:

   - V poli **Z modelu prognózy** vyberte model prognózy projektového rozpočtu, který je spojený se zbývajícími částkami rozpočtu, které chcete pro projekty převést. 
   - Chcete-li zahrnout projekty, které nemají zbývající rozpočtové částky, ale splňují jiná vámi vybraná kritéria, vyberte možnost **Zobrazit nulový zůstatek**.
   - Ve skupině **Vyberte rozpočty** zvolte možnost **Načíst všechny rozpočty**, aby se načetly všechny rozpočty odpovídající vybraným kritériím. Chcete-li navrhnout databázový dotaz, který do podokna načte konkrétní sadu projektových rozpočtů, vyberte možnost **Načíst vybrané rozpočty**.

5. U každého projektu, který chcete zpracovat, vyberte možnost na začátku řádku pro projekt. 
6. Výběrem příkazu **Zpracovat** převeďte zbývající částky rozpočtu pro vybrané projekty do vybraného fiskálního roku.



[!INCLUDE[footer-include](../includes/footer-banner.md)]