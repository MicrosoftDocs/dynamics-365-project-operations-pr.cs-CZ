---
title: Import odhadu do řádku smlouvy na základě projektu
description: Toto téma poskytuje informace o importu odhadu z projektu na řádek smlouvy.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f2b9cbb4cce1691f262c85d95849e01f1a812d51
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2020
ms.locfileid: "4074015"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Import odhadu do řádku smlouvy na základě projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

V Dynamics 365 Project Operations můžete importovat odhady z projektu na řádek smlouvy na základě projektu.

1. Ověřte, že pole **Projekt** bylo vyplněno na řádku smlouvy na základě projektu.
2. Na kartě **Podrobnosti řádku smlouvy** na podmřížce vyberte **Import z odhadu projektu**. Otevře se dialogové okno s možnostmi shrnutí. Dostupné možnosti shrnutí jsou **Třída transakce**, **Kategorie**, **Role** a **Projektový úkol**. Na základě výběru shrnutí se zkopíruje odhad z projektu pro všechny třídy transakcí zahrnuté v tomto řádku smlouvy. 
3. Chcete-li zkontrolovat, které třídy transakcí jsou zahrnuty, na kartě **Obecné** na řádku smlouvy zkontrolujte hodnoty v polích **Zahrnout čas**, **Zahrnout výdaje** a **Zahrnout poplatky**.

Když importujete odhady, aplikace nastaví výchozí cenu na základě ceníků projektu připojených ke smlouvě a typu fakturace nastaveného na řádku smlouvy založeného na projektu. Pokud je úloha, role nebo kategorie nastavena na řádku smlouvy jako neúčtovatelná, importovaný řádek odhadu pro danou roli a kategorii se nastaví jako neúčtovatelný a nepřidá se ke smluvní hodnotě řádku smlouvy.

Pokud řádek smlouvy obsahuje podrobnosti řádku, pole **Hodnota smlouvy** a **Odhadovaná daň** na řádku smlouvy jsou shrnuta a nelze je upravovat.

Když je vybráno více možností sumarizace, pokusí se systém shrnout všechny vybrané možnosti. Výsledek shrnutí má za následek více importovaných řádků smlouvy, než když vyberete pouze jednu možnost shrnutí.

Například pokud má projekt následující řádky odhadu výdajů:

| Úloha | Kategorie | Datum | Množství | Cena za jednotku | Množství |
| --- | --- | --- | --- | --- | --- |
| Úkol A | Letenky | 10/1/2020 | 4 | 400 | 1600 |
| Úkol B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Úkol C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Když se uživatel rozhodne provést sumarizaci podle **třídy transakce**, importují se následující informace:

| Úloha | Kategorie | Datum | Množství | Cena za jednotku | Množství |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10/1/2020 | 3.34 | 840 | 2800 |

Když se uživatel rozhodne provést sumarizaci podle **třídy transakce** a **kategorie**, importují se následující informace:

| Úloha | Kategorie | Datum | Množství | Cena za jednotku | Množství |
| --- | --- | --- | --- | --- | --- |
| Úkol A | Letenky | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Když se uživatel rozhodne provést sumarizaci podle **třídy transakce**, **kategorie** a **úkol uzlu typu list**, importuje se následující. Všimněte si, že tento výsledek je stejný jako výsledek projektu:

| Úloha | Kategorie | Datum | Množství | Cena za jednotku | Množství |
| --- | --- | --- | --- | --- | --- |
| Úkol A | Letenky | 10/1/2020 | 4 | 400 | 1600 |
| Úkol B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Úkol C | Hotel | 11/1/2020 | 2 | 200 | 400 |
