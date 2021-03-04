---
title: Skupiny jednotek a jednotky
description: Toto téma poskytuje informace o skupinách jednotek a jednotkách.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145575"
---
# <a name="unit-groups-and-units"></a>Skupiny jednotek a jednotky

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Skupiny jednotek a jednotky jsou základními entitami v Microsoft Dynamics 365. Jednotka je jedna měrná jednotka a více jednotek lze seskupit do skupin jednotek. Skupina jednotek se v uživatelském rozhraní (UI) aplikace Dynamics 365 někdy označuje jako rozpis jednotky. 

Zde je několik příkladů jednotek a skupin jednotek:
 
- **Skupina jednotek**: Vzdálenost 
    - **Jednotky**: míle, kilometr a tak dál.
- **Skupina jednotek**: Čas
    - **Jednotky**: hodina, den, týden atd. 

Pokud nastavíte více jednotek ve skupině jednotek, musíte také nastavit koeficient převodu tak, že určíte první jednotku, kterou nastavíte jako výchozí nebo primární jednotku pro skupinu jednotek. 

Pokud například ve skupině jednotek **Čas** nastavíte jako první jednotku **Hodina**, systém označí **Hodinu** jako výchozí jednotku. Pokud je následující jednotka, kterou nastavíte, **Den**, musíte nastavit koeficient převodu pro **Den** na **Hodinu.** Pokud potom jako třetí jednotku přidáte **Týden**, musíte nastavit koeficient převodu pro **Týden** podle **Dnů** nebo **Hodin**. 

Následující obrázek znázorňuje příklad nastavení pro jednotku **Den**, kde pole **Množství** zobrazuje počet hodin v rámci dne a **Týdne**, kde pole **Množství** zobrazí počet dnů v týdnu.

> ![Skupina jednotek: Stránka s informacemi](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Použití jednotek a skupin jednotek

Dynamics 365 Project Service Automation používá jednotky a skupiny jednotek ke zpracování odhadů a položek pro náklady i čas. 

U výdajů má každá kategorie výdajů výchozí skupinu jednotek a jednotku. Tyto hodnoty jsou zadány jako výchozí hodnoty pro položky ceníku pro kategorie výdajů. 

Máte například kategorii výdajů s názvem **Mílovné**. Obsahuje skupinu jednotek pojmenovanou **Vzdálenost** a výchozí jednotku pojmenovanou **Míle**. Nastavíte-li skupinu jednotek **Vzdálenost** tak, aby obsahovala dvě jednotky (**Míle** a **Kilometr**), můžete nastavit dvě ceny pro kategorii **Mílovné** v jednom ceníku: cena za míli a cena za kilometr.

| Kategorie výdaje  | Skupina jednotek  | Jednotka      | Způsob ocenění  | Cena za jednotku  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Mílovné           | Vzdálenost      | Míle      | Cena za jednotku    | 10 USD            |
| Mílovné           | Vzdálenost      | Kilometr | Cena za jednotku    |  6 USD            |

Když zadáte výdaj do projektu, systém určí cenu pomocí kombinace kategorie a jednotky na náklady. 

| Popis výdaje        | Kategorie výdaje  | Jednotka  | Množství  | Cena za jednotku   |
|----------------------------|---------------------|-------|-----------|----------------|
| Cesta do umístění klienta | Mílovné             | Míle  | 10        | 10 USD         |

Každá hlavička ceníku má pro čas pole **Výchozí časová jednotka**. Tato hodnota se nastavuje při vytváření záhlaví ceníku. Tato jednotka se pak používá k nastavení všech cen na základě rolí na tomto ceníku.

Řádky odhadu pro pole **Čas na nabídce** lze vyjádřit v libovolné časové jednotce. Řádky odhadu v projektech a časových položkách pro projekty však mohou používat pouze jednotku času **Hodina**. Pokud jednotka v řádku časového záznamu nebo odhadu neodpovídá jednotce na řádku ceníku pro tuto roli, převede systém cenu na jednotky definované v odhadu projektu nebo skutečné transakci projektu.

Následující příklad ukazuje, jak PSA používá skupinu jednotek, jednotky a koeficienty převodu.
- Jednotky

   - **Skupina jednotek**: Čas 
   - **Jednotky**: Hodina 
    
    - **Den** – koeficient převodu: 8 hodin       
    - **Týden** – koeficient převodu: 40 hodin  
        
- Nastavení ceníku na projektu A:

    - **Název**: prodejní ceny UK 2016 
    - **Výchozí časová jednotka**: Den 
    - **Měna**: GBP

| Role      | Skupina jednotek | Jednotka | Organizační jednotka | Cena   |
|-----------|------------|------|---------------------|---------|
| Vývojář | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Časový záznam

Následující tabulka zobrazuje výsledné transakce na straně prodeje vytvořené pomocí PSA pro tříhodinový projekt.


| Projekt   | Task    | Role      | Množství | Jednotka  | Cena za jednotku | Nefakturovaná prodejní částka |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekt A | Návrh  | Vývojář | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Nejčastější dotazy k časové jednotce

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Převádí se PSA na různé jednotky v případě výdajů?
Č. Převod jednotek funguje pouze pro čas. V případě výdajů, pokud systém nemůže najít cenu pro kombinaci kategorie výdajů a jednotky, je ve výchozím nastavení cena nastavena na 0,00.

### <a name="why-does-psa-convert-time-units"></a>Proč PSA převádí časové jednotky?
V některých zemích nebo oblastech existuje právní požadavek, aby byly fakturační sazby nastaveny ve dnech. Sjednání ceny a slevy během cyklu nabídky se provádí pomocí denních sazeb pro každou fakturovatelnou roli. Odhad plánu a časový záznam se provádí v hodinách. Pro podporu tohoto rozdílu v časových jednotkách převádí PSA časové jednotky.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Lze změnit časové jednotky v odhadech projektu?
Č. Odhad plánu je nyní omezen na hodiny a nelze jej změnit.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Lze jednotky a skupiny jednotek upravit, odstranit a přidat?
Ano. S výjimkou skupiny jednotek **Čas** a jednotky **Hodina** lze všechny jednotky odstranit nebo upravit a přidat nové jednotky. V PSA nelze skupinu jednotek **Čas** a jednotku **Hodina** odstranit. Lze je však aktualizovat pomocí přeloženého textu pro pole **Název**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]