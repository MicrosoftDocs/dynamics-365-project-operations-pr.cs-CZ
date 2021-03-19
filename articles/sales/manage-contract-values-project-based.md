---
title: Práce s řádky smlouvy založené na projektu
description: Tohle téma poskytuje informace o řádcích smlouvy na základě projektu.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2b856e280ac56c1cedd7d4966aca7e7f234bc520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278095"
---
# <a name="work-with-projectbased-contract-lines"></a>Práce s řádky smlouvy založené na projektu

Řádky smlouvy na základě projektu v Dynamics 365 Project Operations jsou navrženy tak, aby obsahovaly odhad a řešení fakturace pro konkrétní součásti projektové práce na aktivitě. Struktura řádku smlouvy na základě projektu je rozšířena pro odhady projektu a scénáře fakturace o následující koncepty:

- Způsob fakturace
- Projekt a mapování úkolů
- Zahrnuté třídy transakcí
- Nepřekročitelný limit
- Nastavení účtovatelnosti
- Odhady pomocí podrobností řádku smlouvy
- Zákazníci řádku smlouvy

Následující pole jsou na kartě **Obecné** pro řádky smlouvy na základě projektu. Tato pole pomáhají připravit základ pro podrobný odhad a řešení fakturací pro práci na bázi projektu.

| Pole | Popis | Dopad na následné složky |
| --- | --- | --- |
| **Jméno** | Název řádku smlouvy, který identifikuje diskrétní složku smlouvy, která se odhaduje. U smlouvy projektu vytvořené z nabídky je tato hodnota zkopírována z odpovídající hodnoty řádku nabídky na základě projektu. | Tato hodnota pole je zkopírována do řádku faktury projektu, který je vytvořen z tohoto řádku smlouvy při vytváření faktury. |
| **Způsob fakturace** | U smlouvy projektu vytvořené z nabídky je tato hodnota zkopírována z odpovídajícího pole na řádku nabídky. Toto je sada možností, která představuje dva hlavní smluvní modely podporované v Project Operations:</br>- **Pevná cena**</br>- **Čas a materiál** | Na základě způsobu fakturace odkazované řádky smlouvy bude zpracována samotná transakce. Pokud má řádka smlouvy odkazovaná skutečnou hodnotou metodu fakturace času a materiálu, vytvoří se záznam skutečných nákladů a nefakturovaného prodeje. Pokud má řádek smlouvy, na který odkazuje skutečná hodnota, způsob fakturace s pevnou cenou, vytvoří se pouze skutečné náklady. |
| **Project** | Toto pole použijte k identifikaci projektu, který bude použit k provedení práce na této aktivitě. | Hodnota v tomto poli se používá v souvislosti s poli **Zahrnuté úkoly** a **Zahrnuté třídy transakcí** ke čtení odkazu na řádek smlouvy v záznamu skutečného nebo odhadovaného řádku. |
| **Zahrnout čas** | Příznak označuje, zda jsou na tomto řádku smlouvy zahrnuty časové transakce nebo mzdové náklady u vybraného projektu. Hodnota **Ne** označuje, že časové transakce nebo mzdové náklady nebudou zahrnuty do tohoto řádku smlouvy. Hodnota **Ano**, znamená že ano. | Tato hodnota pole se používá ve spojení s projektem ke čtení odkazu na řádek smlouvy v záznamu skutečného nebo odhadovaného řádku. |
| **Zahrnout výdaj** | Příznak označuje, zda budou na tomto řádku smlouvy zahrnuty výdajové náklady u vybraného projektu. Hodnota **Ne** označuje, že výdajové náklady nebudou zahrnuty do tohoto řádku smlouvy. Hodnota **Ano**, znamená že ano. | Tato hodnota pole se používá ve spojení s projektem ke čtení odkazu na řádek smlouvy v záznamu skutečného nebo odhadovaného řádku. |
| **Zahrnout poplatek** | Příznak označuje, zda budou na tomto řádku smlouvy zahrnuty poplatky u vybraného projektu. Hodnota **Ne** označuje, že poplatky nebudou zahrnuty do tohoto řádku smlouvy. Hodnota **Ano**, znamená že ano. | Tato hodnota pole se používá ve spojení s projektem ke čtení odkazu na řádek smlouvy v záznamu skutečného nebo odhadovaného řádku. |
| **Nasmlouvaná částka** | Na řádku smlouvy s pevnou cenou se jedná o dohodnutou hodnotu, která bude zákazníkovi fakturována za všechny součásti práce přidružené k tomuto řádku smlouvy. Na řádku smlouvy času a materiálu je tato částka odhadnutá hodnota, co bude zákazníkovi fakturováno za všechny součásti práce přidružené k tomuto řádku smlouvy. U smlouvy projektu vytvořené z nabídky je tato hodnota zkopírována z odpovídajícího pole na řádku nabídky. Pokud má řádek smlouvy na základě projektu podrobnosti, je toto pole uzamčeno pro úpravy a shrnuto z částky v podrobnostech řádku smlouvy. | Pokud řádek smlouvy obsahuje podrobnosti, lze tuto hodnotu upravit změnou částek v podrobnostech řádku. Na řádku smlouvy s pevnou cenou se tato hodnota používá ke generování částky před daní z milníků periodické fakturace. |
| **Odhad daně** | Uživatel může toto pole upravit a zadat odhadovanou částku daně na řádku smlouvy. Pokud má řádek smlouvy na základě projektu podrobnosti, je toto pole uzamčeno pro úpravy a shrnuto z částky daně v podrobnostech řádku smlouvy. | Pokud řádek smlouvy obsahuje podrobnosti, lze tuto hodnotu upravit změnou částek daně v podrobnostech řádku. Na řádku smlouvy s pevnou cenou se tato hodnota používá ke generování daně z milníků periodické fakturace. |
| **Nasmlouvaná částka včetně daně** | Řádka smlouvy s částkou včetně daně Toto pole je jen pro čtení a počítá se jako **Nasmlouvaná částka + daň**. | Na řádku smlouvy s pevnou cenou se tato hodnota používá ke generování milníků periodické fakturace. |
| **Nepřekročitelný limit** | Uživatel může toto pole upravit a je k dispozici pouze na řádcích smlouvy založené na projektu s metodou fakturace času a materiálu. | Uživatel může toto pole upravit. Když skutečný čas nebo výdaj odkazuje na tento řádek smlouvy pro čas a materiál, skutečná částka je vyhodnocena vůči nepřekročitelnému limitu na tomto řádku smlouvy po zaúčtování již vynaložených a potvrzených částek. |
| **Rozpočet zákazníka** | Toto pole je upravitelné a je zkopírováno z odpovídajícího pole na řádku nabídky, pokud byla smlouva vytvořena z nabídky. | Toto pole slouží pouze pro informaci a nemá žádný následný význam. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Pravidlo ověření pro možnosti na kartě Obecné pro řádky smlouvy založené na projektu

Pravidlo: Projekt a určitou třídu transakcí lze do smlouvy zahrnout pouze na jednom řádku smlouvy na základě projektu.

| Smlouva | Řádek smlouvy | Project | Zahrnout čas | Zahrnout výdaj | Zahrnout poplatek | Platné/neplatné | Důvod                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S1       | ŘS1           | O1      | Ano          | Ano             | Ano         | Neplatný       | Porušuje pravidlo. Čas, výdaje a poplatky za projekt P1 jsou zahrnuty v obou řádcích smluv ŘS1 a ŘS2.                                                                                       |
| S1       | ŘS2           | O1      | Ano          | Ano             | Ano         | Neplatný       | Porušuje pravidlo. Čas, výdaje a poplatky za projekt P1 jsou zahrnuty v obou řádcích smluv ŘS1 a ŘS2.                                                                                       |
| S1       | ŘS1           | O1      | Ano          | No              | Ano         | Neplatný       | Porušuje pravidlo. Čas,a poplatky za projekt P1 jsou zahrnuty v obou řádcích smluv ŘS1 a ŘS2.                                                                                                   |
| S1       | ŘS2           | O1      | Ano          | Ano             | Ano         | Neplatný       | Porušuje pravidlo. Čas,a poplatky za projekt P1 jsou zahrnuty v obou řádcích smluv ŘS1 a ŘS2.                                                                                                   |
| S1       | ŘS1           | O1      | Ano          | No              | Ano         | Platná           | Čas a poplatky v projektu P1 jsou zahrnuty na řádku ŘS1. Výdaje v projektu P1 jsou zahrnuty na řádku ŘS2. </br>   Neexistuje žádné překrývání toho, co je zahrnuto na každém řádku smlouvy, a proto je platné.  |
| S1       | ŘS2           | O1      | No           | Ano             | No          | Platná           | Čas a poplatky v projektu P1 jsou zahrnuty na řádku ŘS1. Výdaje v projektu P1 jsou zahrnuty na řádku ŘS2. </br>   Neexistuje žádné překrývání toho, co je zahrnuto na každém řádku smlouvy, a proto je platné.  |
| S1       | ŘS1           | O1      | Ano          | Ano             | Ano         | Neplatný       | Porušuje pravidlo. Čas, výdaje a poplatky za projekt P1 jsou zahrnuty v řádcích dvou smluv.                                                                                               |
| ŘS2      | ŘS2           | O1      | Ano          | Ano             | Ano         | Neplatný       | Porušuje pravidlo. Čas, výdaje a poplatky za projekt P1 jsou zahrnuty v řádcích dvou smluv.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]