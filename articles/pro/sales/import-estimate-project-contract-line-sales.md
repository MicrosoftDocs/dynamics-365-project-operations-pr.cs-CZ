---
title: Import odhadu do řádku smlouvy na základě projektu – omezené
description: Toto téma poskytuje informace o importu finančních odhadů z projektu na řádek smlouvy.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b462af163fef1bfcbbc4f945df722d4e8a71fb1a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177458"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Import odhadu do řádku smlouvy na základě projektu – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V Dynamics 365 Project Operations můžete importovat odhady z projektu na řádek smlouvy na základě projektu.

1. Ověřte, že pole **Projekt** bylo vyplněno na řádku smlouvy na základě projektu.
2. Na kartě **Podrobnosti řádku smlouvy** na podmřížce vyberte **Import z odhadu projektu**. Otevře se dialogové okno s možnostmi shrnutí. Dostupné možnosti shrnutí jsou **Třída transakce**, **Kategorie**, **Role** a **Projektový úkol**.
3. Na základě výběru shrnutí se zkopíruje odhad z projektu pro všechny třídy transakcí a úlohy zahrnuté v tomto řádku smlouvy. Chcete-li zkontrolovat, které třídy transakcí jsou zahrnuty, na kartě **Obecné** na řádku smlouvy na základě projektu zkontrolujte hodnoty v polích **Zahrnout čas**, **Zahrnout výdaje** a **Zahrnout poplatky**. 
4. Chcete-li zjistit, jaké úkoly jsou zahrnuty, vyberte kartu **Účtovatelné úkoly** na řádku smlouvy. Na základě přidružených úkolů, které mají pole **Zahrnuté třídy transakcí** nastaveno na **Ano**, všechny odhady pro tyto kombinace úkolů a tříd transakcí se importují do řádku smlouvy.

Když importujete odhady, systém nastaví výchozí cenu na základě ceníků projektu připojených ke smlouvě a typu fakturace nastaveného na řádku smlouvy založeného na projektu. Pokud je úloha, role nebo kategorie nastavena na řádku smlouvy jako neúčtovatelná, importovaný řádek odhadu se nastaví jako neúčtovatelný a nepřidá se ke smluvní hodnotě řádku smlouvy.

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
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Když se uživatel rozhodne provést sumarizaci podle **třídy transakce** a **kategorie**, importují se následující informace:

| Úloha | Kategorie | Datum | Množství | Cena za jednotku | Množství |
| --- | --- | --- | --- | --- | --- |
| Úkol A | Letenky | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 10/1/2020 | 6 | 200 | 1200 |

Když se uživatel rozhodne provést sumarizaci podle **třídy transakce**, **kategorie** a **úkol uzlu typu list**, importuje se následující. Všimněte si, že tento výsledek je stejný jako výsledek projektu:

| Úloha | Kategorie | Datum | Množství | Cena za jednotku | Množství |
| --- | --- | --- | --- | --- | --- |
| Úkol A | Letenky | 10/1/2020 | 4 | 400 | 1600 |
| Úkol B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Úkol C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]