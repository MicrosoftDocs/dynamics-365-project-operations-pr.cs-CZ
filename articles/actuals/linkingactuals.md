---
title: Původy transakcí – Propojte skutečné hodnoty s jejich zdrojem
description: Tento článek vysvětluje, jak se koncept původu transakcí používá k propojení skutečných hodnot s původními zdrojovými záznamy, jako je záznam času, záznam výdajů nebo protokoly využití materiálu.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921294"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Původy transakcí – Propojte skutečné hodnoty s jejich zdrojem

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Záznamy o původu transakcí se vytvářejí za účelem propojení skutečných hodnot s jejich zdrojem, jako jsou časové záznamy, záznamy o výdajích, protokoly využití materiálu a projektové faktury.

Následující příklad ukazuje typické zpracování časových záznamů v životním cyklu projektu Project Operations.

> ![Zpracování časových záznamů v Project Operations.](media/basic-guide-17.png)
 
1. Odeslání časového záznamu způsobí vytvoření dvou řádků deníku: jednoho pro náklady a jednoho pro nefakturovaný prodej.
2. Případné schválení časového záznamu způsobí vytvoření dvou skutečných hodnot: jedné pro náklady a jedné pro nefakturovaný prodej.
3. Když uživatel vytvoří projektovou fakturu, transakce řádku faktury se vytvoří pomocí dat z nefakturovaného skutečného prodeje.
4. Po potvrzení faktury se vytvoří dvě nové skutečné hodnoty: storno nefakturovaného prodeje a skutečný fakturovaný prodej.

Každá událost v tomto pracovním postupu zpracování spouští vytvoření záznamů v entitě Původ transakce, aby pomohla vytvořit trasování vztahů mezi těmito záznamy, které byly vytvořeny napříč časovým záznamem, řádkem deníku, skutečnými hodnotami a podrobnostmi řádku faktury.

Následující tabulka zobrazuje záznamy v entitě Původ transakce pro předchozí pracovní postup.

| Událost                        | Zdroj                   | Typ původu                       | Transakce                       | Typ transakce         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Odeslání časového záznamu        | GUID záznamu časového záznamu   | Časový záznam                        | GUID záznamu řádku deníku (náklady)   | Řádek deníku             |
| GUID záznamu časového záznamu       | Časový záznam               | GUID záznamu řádku deníku (prodej)  | Řádek deníku                      |                          |
| Schválení času                | GUID záznamu řádku deníku | Řádek deníku                      | GUID záznamu nefakturovaného prodeje        | Skutečnost                   |
| GUID záznamu časového záznamu       | Časový záznam               | GUID záznamu nefakturovaného prodeje        | Skutečnost                            |                          |
| GUID záznamu řádku deníku     | Řádek deníku             | GUID záznamu skutečné hodnoty nákladů           | Skutečnost                            |                          |
| GUID záznamu časového záznamu       | Časový záznam               | GUID záznamu skutečné hodnoty nákladů           | Skutečnost                            |                          |
| Vytvoření faktury             | GUID záznamu časového záznamu   | Časový záznam                        | GUID transakce řádku faktury     | Transakce řádku faktury |
| GUID záznamu řádku deníku     | Řádek deníku             | GUID transakce řádku faktury     | Transakce řádku faktury          |                          |
| Potvrzení faktury         | GUID řádku faktury        | Řádek faktury                      | GUID záznamu fakturovaného prodeje          | Skutečnost                   |
| GUID faktury                 | Faktura                  | GUID záznamu fakturovaného prodeje          | Skutečnost                            |                          |
| GUID podrobnosti řádku faktury     | Podrobnosti řádku faktury      | GUID záznamu fakturovaného prodeje          | Skutečnost                            |                          |
| GUID záznamu časového záznamu       | Časový záznam               | GUID záznamu fakturovaného prodeje          | Skutečnost                            |                          |
| GUID záznamu řádku deníku     | Řádek deníku             | GUID záznamu fakturovaného prodeje          | Skutečnost                            |                          |
| GUID záznamu časového záznamu       | Časový záznam               | GUID storna nefakturovaného prodeje      | Skutečnost                            |                          |
| GUID záznamu řádku deníku     | Řádek deníku             | GUID storna nefakturovaného prodeje      | Skutečnost                            |                          |
| Oprava konceptu faktury     | GUID starých PŘF             | Transakce řádku faktury          | GUID opravných PŘF               | Transakce řádku faktury |
| GUID starého ŘF                  | Řádek faktury             | GUID opravných PŘF               | Transakce řádku faktury          |                          |
| GUID staré faktury             | Faktura                  | GUID opravných PŘF               | Transakce řádku faktury          |                          |
| GUID záznamu časového záznamu       | Časový záznam               | GUID opravných PŘF               | Transakce řádku faktury          |                          |
| GUID záznamu řádku deníku     | Řádek deníku             | GUID opravných PŘF               | Transakce řádku faktury          |                          |
| Oprava potvrzené faktury | GUID starých PŘF             | Transakce řádku faktury          | GUID skutečné hodnoty stornovaného fakturovaného prodeje | Skutečnost                   |
| GUID starého ŘF                  | Řádek faktury             | GUID skutečné hodnoty stornovaného fakturovaného prodeje | Skutečnost                            |                          |
| GUID staré faktury             | Faktura                  | GUID skutečné hodnoty stornovaného fakturovaného prodeje | Skutečnost                            |                          |
| GUID záznamu časového záznamu       | Časový záznam               | GUID skutečné hodnoty stornovaného fakturovaného prodeje | Skutečnost                            |                          |
| GUID záznamu řádku deníku     | Řádek deníku             | GUID skutečné hodnoty stornovaného fakturovaného prodeje | Skutečnost                            |                          |
| GUID starých PŘF                 | Transakce řádku faktury | GUID skutečné hodnoty nového nefakturovaného prodeje    | Skutečnost                            |                          |
| GUID starého ŘF                  | Řádek faktury             | GUID skutečné hodnoty nového nefakturovaného prodeje    | Skutečnost                            |                          |
| GUID staré faktury             | Faktura                  | GUID skutečné hodnoty nového nefakturovaného prodeje    | Skutečnost                            |                          |
| GUID záznamu časového záznamu       | Časový záznam               | GUID skutečné hodnoty nového nefakturovaného prodeje    | Skutečnost                            |                          |
| GUID záznamu řádku deníku     | Řádek deníku             | GUID skutečné hodnoty nového nefakturovaného prodeje    | Skutečnost                            |                          |
| GUID opravných PŘF          | Transakce řádku faktury | GUID skutečné hodnoty nového nefakturovaného prodeje    | Skutečnost                            |                          |
| GUID opravného ŘF           | Řádek faktury             | GUID skutečné hodnoty nového nefakturovaného prodeje    | Skutečnost                            |                          |
| GUID opravné faktury      | Faktura                  | GUID skutečné hodnoty nového nefakturovaného prodeje    | Skutečnost                            |                          |


Následující obrázek ukazuje vazby, které jsou vytvořeny mezi skutečnými hodnotami a jejich zdroji při různých událostech, na příkladu časových záznamů v Project Operations.

> ![Jak jsou skutečné hodnoty propojeny se zdrojovými záznamy v Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
