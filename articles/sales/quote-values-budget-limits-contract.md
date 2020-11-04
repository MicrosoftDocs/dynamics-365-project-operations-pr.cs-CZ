---
title: Souhrnné informace o projektové nabídce
description: Toto téma poskytuje informace o údajích a nastaveních, která se vztahují na projektové nabídky a ovlivňují je.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6dde5305f179e9a4454bf97c44f1ebdf9986dd43
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073626"
---
# <a name="summary-information-on-a-project-quote"></a>Souhrnné informace o projektové nabídce

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_


Tento článek vysvětluje informace, které se vztahují k projektové nabídce. Tyto informace zahrnují nastavení, která mají dopad na všechny řádky nabídky, a informace o nabídce, které jsou shrnuty za všechny řádkové položky a řídí KPI projektové nabídky.

V následující tabulce jsou uvedena souhrnná informační pole projektové nabídky, která jsou jedinečná pro aplikaci Dynamics 365 Project Operations nebo se jejich chování významně odlišuje oproti nabídkám aplikace Dynamics 365 Sales.

| **Pole** | **Umístění** | **Relevance, účel a vedení** | **Dopad na následné složky** |
| --- | --- | --- | --- |
| Typ | Karta Souhrn (skrytá) | Toto pole sady možností obsahuje následující možnosti:</br>- Na základě práce (k dispozici pouze v případě, že je nainstalována aplikace Project Operations)</br>- Na základě zboží (k dispozici pouze v případě, že jsou nainstalovány aplikace Project Operations a Sales)</br>- Na základě servisní údržby (k dispozici, když je nainstalována služba Dynamics 365 Field Service) | Když použijete aplikaci Project Operations, hodnota tohoto pole se automaticky nastaví na **Na základě práce**. Toto klasifikuje nabídku jako nabídku založenou na projektu. Nabídka by měla být založená na projektu, aby povolila všechna rozšíření a funkce specifické pro projekt. |
| Vlastnící společnost | Souhrn | Právní subjekt, který bude odpovídat za náklady a výnosy plynoucí z tohoto projektu nebo projektů spojených s touto nabídkou. Když je nabídka vytvořena z příležitosti, zkopíruje se toto pole z odpovídajícího pole příležitosti. | Vlastnící společnost odpovídá konceptu právnické osoby v modulu **Řízení a účetnictví projektů** aplikace Project Operations. Všechny náklady a výnosy plynoucí z tohoto projektu budou zaúčtovány v hlavní knize vlastnící společnosti, |
| Potenciální zákazník | Karta Souhrn | Odkaz na záznam společnosti nebo účtu zákazníka. Platný odkazovaný zákazník v projektové nabídce musí být nastaven jako zákazník ve vlastnící společnosti nabídky. Vlastnící společnost zobrazuje seznam právnických osob, které jsou nastaveny v modulu **Řízení a účetnictví projektů** aplikace Project Operations. Když je nabídka vytvořena z příležitosti, zkopíruje se toto pole z odpovídajícího pole příležitosti. | Měna v projektové nabídce má výchozí hodnotu na základě měny zákazníka. Toto však lze změnit před uložením nabídky. |
| Manažer obchodních vztahů | Karta Souhrn | Jméno manažera obchodních vztahů pro tento obchod. Když je nabídka vytvořena z příležitosti, zkopíruje se toto pole z odpovídajícího pole příležitosti. | Manažer obchodních vztahů je zodpovědný za řízení vztahu se zákazníkem až do dokončení tohoto projektu. Výchozí hodnoty smluvní jednotky u projektové nabídky jsou nastaveny na základě záznamu rezervovatelného zdroje svázaného s manažerem obchodních vztahů.|
| Smluvní jednotka | Karta Souhrn | Organizační jednotka, která je odpovědná za realizaci projektu či projektů asociovaných s touto nabídkou. Když je nabídka vytvořena z příležitosti, zkopíruje se toto pole z odpovídajícího pole příležitosti. | Smluvní jednotka je divize společnosti, která bude realizovat projekty po uzavření obchodu. Každá smluvní jednotka má měnu a tato měna se používá k vykazování odhadovaných a skutečných nákladů vzniklých během provádění projektu. |
| Ceník produktů | Karta Souhrn | Toto je ceník, který se používá pro výchozí ceny v řádcích nabídek založených na produktu. Seznam možností pro toto pole zobrazuje seznam ceníků, kde měna ceníku odpovídá měně nabídky. Když je nabídka vytvořena z příležitosti, zkopíruje se toto pole z odpovídajícího pole příležitosti. Toto pole v příležitosti má výchozí hodnotu načtenou ze záznamu účtu, ale lze ji změnit. | Když je nabídka získána, hodnota pole je zkopírována do vytvářené projektové smlouvy. |
| Měna | Karta Souhrn | To označuje měnu, která bude použita pro hlášení hodnoty tohoto obchodu. Je to také měna, ve které bude zákazníkovi fakturován obchod, pokud bude získán. Když je nabídka vytvořena z příležitosti, zkopíruje se toto pole z odpovídajícího pole příležitosti. Toto pole v příležitosti má výchozí hodnotu načtenou ze záznamu účtu, ale uživatel ji může změnit.  | Po uložení nabídky již toto pole nelze upravovat. Používá se k určení výchozích hodnot ceníků produktů a projektů v nabídce. Měna této nabídky se musí shodovat s měnou ceníku. |
| Nepřekročitelný limit | Karta Souhrn | To označuje vyjednanou horní mez konečné hodnoty, se kterou zákazník u tohoto obchodu souhlasí. | Tato horní mez se vyhodnocuje během provádění a je použitelná ve všech řádkových položkách a projektech přidružených k tomuto obchodu. |
| Požadované datum dodávky | Karta Souhrn | Když je nabídka vytvořena z příležitosti, zkopíruje se toto pole z odpovídajícího pole příležitosti. | Toto datum se používá jako konečné datum pro generování rozpisů faktur. |

Níže jsou uvedeny karty a KPI dostupné v projektové nabídce, které jsou jedinečné pro aplikaci Project Operations, nebo se jejich chování významně liší od chování nabídek aplikace Sales.

| **Pole** | **Umístění** | **Relevance, účel a vedení** |
| --- | --- | --- |
| Analýza ziskovosti | Karta na nabídce | Karta zobrazuje následující metriky.</br>- Celkové účtovatelné náklady</br></br>- Celkové neúčtovatelné náklady</br>- Celkové výnosy</br>- Celkové výnosy (základní)</br>- Hrubá marže</br>- Upravená hrubá marže|
| Porovnání s očekáváními zákazníka | Karta na nabídce | Tato karta zobrazuje následující metriky.</br>- Odhadované dokončení</br>- Požadované dokončení</br>- Rozpočet zákazníka</br>- Hodnota nabídky |
| Analýza nabídky | Karta na nabídce | Tato karta shrnuje následující hlavní KPI pro projektovou nabídku</br>- Srovnání s očekáváním zákazníka ohledně rozpočtu a plánu</br>- Hrubá marže</br>- Upravená hrubá marže |
