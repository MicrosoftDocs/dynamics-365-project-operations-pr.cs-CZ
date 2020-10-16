---
title: Importovat odhady projektu do řádku nabídky založené na projektu
description: Toto téma poskytuje informace o importu odhadů z projektu na řádek nabídky.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907985"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importovat odhady projektu do řádku nabídky založené na projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


Pokud je projekt vytvořen během fáze předprodeje, můžete vybrat import finančního odhadu z projektu do řádku nabídky na základě projektu.

1. Ujistěte se, že řádek nabídky na základě projektu obsahuje informace o projektu v poli **Projekt**.
2. Na kartě **Podrobnosti řádku nabídky** vyberte **Import z odhadu projektu**.
3. V dialogovém okně vyberte jednu z následujících možností sumarizace.

  - **Třída transakce**
  - **Kategorie**
  - **Role** 
  - **Projektový úkol**

Na základě vašeho výběru se zkopíruje odhad z projektu pro všechny třídy transakcí zahrnutých v tomto řádku nabídky. Chcete-li zkontrolovat, které třídy transakcí jsou zahrnuty, vyberte kartu **Všeobecné** na řádku nabídky na základě projektu a zkontrolujte hodnoty pro **Zahrnout čas**, **Zahrnout výdaje** a **Zahrnout poplatky**.

Když importujete odhady, systém nastaví výchozí cenu na základě ceníků projektu připojených k nabídce a typu fakturace nastaveného na řádku nabídky založeného na projektu. Pokud je role nebo kategorie nastavena na řádku nabídky založeného na projektu jako neúčtovatelná, importovaný řádek odhadu se nastaví jako neúčtovatelný a nepřidá se k hodnotě nabídky řádku nabídky.

Pokud řádek nabídky obsahuje podrobnosti řádku, pole **Hodnota nabídky** a **Odhadovaná daň** na řádku nabídky jsou shrnuta a nelze je upravovat.

Když je vybráno více možností sumarizace, pokusí se sumarizace shrnout všechny vybrané možnosti. To znamená, že výstup importovaných řádků nabídek bude větší, než kdybyste vybrali pouze jednu možnost shrnutí.

Například pokud má projekt následující řádky odhadu výdajů.

| Úloha | Kategorie | Datum | Množství | Cena za jednotku | Množství |
| --- | --- | --- | --- | --- | --- |
| Úkol A | Letenky | 10/1/2020 | 4 | 400 | 1600 |
| Úkol B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Úkol C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Když se uživatel rozhodne provést sumarizaci podle třídy transakce, importují se následující informace.

| Úloha | Kategorie | Datum | Množství | Cena za jednotku | Množství |
| --- | --- | --- | --- | --- | --- |
| | | 10/1/2020 | 3.34 | 840 | 2800 |

Když se uživatel rozhodne provést sumarizaci podle třídy transakce a kategorie, importují se následující informace.

| Úloha | Kategorie | Datum | Množství | Cena za jednotku | Množství |
| --- | --- | --- | --- | --- | --- |
| Úkol A | Letenky | 10/1/2020 | 4 | 400 | 1600 |
| | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Když se uživatel rozhodne provést sumarizaci podle třídy transakce, kategorie a úkol uzlu typu list, importují se následující informace. Všimněte si, že tento výsledek je stejný jako výsledek projektu.

| Úloha | Kategorie | Datum | Množství | Cena za jednotku | Množství |
| --- | --- | --- | --- | --- | --- |
| Úkol A | Letenky | 10/1/2020 | 4 | 400 | 1600 |
| Úkol B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Úkol C | Hotel | 11/1/2020 | 2 | 200 | 400 |