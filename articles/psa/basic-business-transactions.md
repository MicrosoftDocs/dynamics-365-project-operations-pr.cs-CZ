---
title: Obchodní transakce
description: Toto téma poskytuje informace o obchodních transakcích.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 28555f29e65c11255c8966f3d4b900512aa01c30fef0a9cef3a3794edaf92a0b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987518"
---
# <a name="business-transactions"></a>Obchodní transakce

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V Dynamics 365 Project Service Automation *je obchodní transakce* abstraktní koncept, který není reprezentován žádnou entitou. Některá společná pole a procesy v entitách jsou však navrženy tak, aby používaly koncept obchodních transakcí. Následující entity používají tuto abstrakci:

- Podrobnosti řádku nabídky
- Podrobnosti řádku smlouvy
- Řádky odhadu
- Řádky deníku
- Skutečnost

Z těchto entit jsou na fázi odhadu v životním cyklu projektu mapovány Podrobnosti řádku nabídky, Podrobnosti řádku smlouvy a Řádky odhadu. Entity Řádky deníku a Skutečné hodnoty jsou mapovány na fázi spuštění v životním cyklu projektu.

PSA zachází se záznamy v těchto pěti entitách jako s obchodními transakcemi. Jediným rozdílem je, že záznamy v entitách, které jsou mapovány na fázi odhadu, jsou považovány za finanční prognózy, zatímco záznamy v entitách, které jsou mapovány na fázi spuštění, jsou považovány za finanční fakty, které již nastaly.

Další informace viz [Odhady](estimates.md) a [Skutečné hodnoty](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepty, které jsou jedinečné pro obchodní transakce
Následující koncepty jsou jedinečné pro koncept obchodních transakcí:

- Typ transakce
- Třída transakce
- Původ transakce
- Propojení transakce

### <a name="transaction-type"></a>Typ transakce

Typ transakce představuje načasování a kontext finančního dopadu na projekt. Je reprezentován sadou možností, která má v PSA následující podporované hodnoty:
- Náklady
- Projektová smlouva
- Nefakturovaný prodej
- Fakturovaný prodej
- Vnitropodnikový prodej
- Jednotkové náklady zdroje

### <a name="transaction-class"></a>Třída transakce

Třída transakce představuje různé typy nákladů vynaložených na projekty. Je reprezentován sadou možností, která má v PSA následující podporované hodnoty:

- Time
- Výdaj
- Materiál
- Poplatek
- Milník
- Daň

Hodnotu **Milníku** obvykle používá obchodní logika v PSA pro fakturaci s pevnou cenou.

### <a name="transaction-origin"></a>Původ transakce

Původ transakce je entita, která ukládá původ každé obchodní transakce. Jak probíhá provádění projektu, každá obchodní transakce povede k další obchodní transakci, která zase vytvoří další a tak dále. Entita původu transakce byla navržena tak, aby ukládala data o původu každé transakce a pomohla tak vykazování a sledovatelnosti. 

### <a name="transaction-connection"></a>Propojení transakce

Propojení transakce je entita, která uchovává vztah mezi dvěma podobnými obchodními transakcemi, jako jsou např. náklady a související skutečné hodnoty prodeje nebo storna transakcí, které jsou spouštěny fakturačními aktivitami, jako jsou např. potvrzení faktury nebo opravy faktury.

Původ transakce a Propojení transakce vám společně pomáhají udržet přehled o vztazích mezi obchodními transakcemi a akcemi, které vedly k vytvoření specifické obchodní transakce.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Příklad: Jak funguje Původ transakce s Propojením transakce

Následující příklad ukazuje typické zpracování časových záznamů v životním cyklu projektu PSA.

> ![Zpracování časových záznamů v životním cyklu aplikace Project Service.](media/basic-guide-17.png)
 
1. Odeslání časového záznamu způsobí vytvoření dvou řádků deníku: jeden pro náklady a jeden pro nefakturovaný prodej.
2. Případné schválení časového záznamu způsobí vytvoření dvou skutečných hodnot: jedna pro náklady a jedna pro nefakturovaný prodej.
3. Když uživatel vytvoří projektovou fakturu, transakce řádku faktury se vytvoří pomocí dat z nefakturovaného skutečného prodeje. 
4. Po potvrzení faktury se vytvoří dvě nové skutečné hodnoty: storno nefakturovaného prodeje a skutečný fakturovaný prodej.

Každá z těchto událostí spouští vytvoření záznamů v entitách Původ transakce a Propojení transakce, aby pomohla vytvořit trasování vztahů mezi těmito záznamy, které byly vytvořeny napříč časovým záznamem, řádkem deníku, skutečnými hodnotami a podrobnostmi řádku faktury.

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

Následující tabulka zobrazuje záznamy v entitě Propojení transakce pro předchozí pracovní postup.

| Událost                          | Transakce 1                 | Role transakce 1 | Typ transakce 1           | Transakce 2                | Role transakce 2 | Typ transakce 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Odeslání časového záznamu          | GUID řádku deníku (prodej)     | Nefakturovaný prodej     | msdyn_journalline            | GUID řádku deníku (náklady)     | Náklady               | msdyn_journalline  |
| Schválení času                  | GUID skutečné nefakturované hodnoty (prodej)  | Nefakturovaný prodej     | msdyn_actual                 | GUID skutečné hodnoty nákladů (náklady)       | Náklady               | msdyn_actual       |
| Vytvoření faktury               | GUID podrobnosti řádku faktury      | Fakturovaný prodej       | msdyn_invoicelinetransaction | GUID skutečné hodnoty nefakturovaného prodeje   | Nefakturovaný prodej     | msdyn_actual       |
| Potvrzení faktury           | GUID stornování skutečné hodnoty         | Stornování          | msdyn_actual                 | GUID původního nefakturovaného prodeje | Původní           | msdyn_actual       |
| GUID fakturovaného prodeje              | Fakturovaný prodej                  | msdyn_actual       | GUID skutečné hodnoty nefakturovaného prodeje   | Nefakturovaný prodej               | msdyn_actual       |                    |
| Oprava konceptu faktury       | GUID transakce řádku faktury | Nahrazení          | msdyn_invoicelinetransaction | GUID fakturovaného prodeje            | Původní           | msdyn_actual       |
| Potvrdit opravu faktury     | GUID storna fakturovaného prodeje    | Stornování          | msdyn_actual                 | GUID fakturovaného prodeje            | Původní           | msdyn_actual       |
| GUID skutečné hodnoty nového nefakturovaného prodeje | Nahrazení                     | msdyn_actual       | GUID fakturovaného prodeje            | Původní                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]