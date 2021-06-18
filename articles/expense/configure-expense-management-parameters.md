---
title: Konfigurace parametrů správy výdajů
description: Toto téma popisuje parametry, které řídí obecné chování ve správě výdajů.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1e1181467c51384c4de7dcda2de29ed531360a0a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995433"
---
# <a name="configure-expense-management-parameters"></a>Konfigurace parametrů správy výdajů

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma popisuje parametry, které řídí obecné chování ve správě výdajů.

## <a name="general"></a>Obecná

| Pole                                                    | Popis |
|----------------------------------------------------------|-------------|
| Standardní sazba za ujeté kilometry                                 | Zadejte sazbu náhrady za výdaje za ujeté kilometry. Tato sazba se vynásobí počtem najetých kilometrů, který je zadán u výdajů pro výpočet částky, která je proplácena za cestovní výdaje. |
| Ověřit účel výdajů                                 | Tuto možnost zapněte, chcete-li omezit uživatele na existující sadu hodnot, která je nakonfigurována v poli **Účel výkazu výdajů**, když vytvářejí výkazy výdajů. |
| Osobní výdaje hrazené                                | Vyberte, kdo je odpovědný za výplatu všech částek transakcí kreditní kartou, které jsou kategorizovány jako osobní. |
| Zobrazit celou zprávu o výdajích při vrácení zpět               | Vyberte tuto možnost, chcete-li zobrazit všechny výdaje na výkazu výdajů, když jsou zobrazeny podrobnosti původního dokumentu pro konkrétní doklad, který byl vygenerován při zaúčtování výkazu výdajů. |
| Předběžná autorizace cesty je povinná                 | Tuto možnost vyberte, pokud chcete, aby zaměstnanec mohl odeslat výkaz výdajů, aby byla odeslána a schválena cestovní žádost. |
| Před zveřejněním povolte úpravy distribucí            | Vyberte, zda lze distribuce sestavy výdajů upravit před jejím zveřejněním. |
| Vyhodnoťte zásady řízení výdajů                     | Vyberte, kdy se mají vyhodnocovat výdaje, a určete, zda došlo k porušení zásad výdajů. Výdaje lze vyhodnotit z hlediska porušení, když je zadán a uložen záznam výdajů, nebo když je výdaj předložen ke schválení. Při uložení řádku výdajů budou vyhodnocena pravidla zásad pro požadované příjmy. |
| Povolit mezipodnikové výdajové řádky                         | Vyberte, zda lze do výkazu výdajů zadat výdaje za jiné právnické osoby. |
| Povolte úpravy směnného kurzu pro výdaje na kreditní karty | Vyberte tuto možnost, abyste uživateli umožnili upravit směnný kurz pro importované výdaje na kreditní karty. |
| Pole víceúrovňové hierarchie k zobrazení                  | Vyberte, která pole schvalovatele se zobrazují, když je typ přiřazení pracovního toku nastaven na hierarchii, a výběr **Hierarchie** je nastaven na použití hierarchie schválení, víceúrovňové schválení výdajů. Když se pro pracovní postup použije víceúrovňová schvalovací hierarchie, vybraná pole se zobrazí v sestavě výdajů a lze je upravit. |
| Zadejte číslo kreditní karty zaměstnance                        | Vyberte, zda lze zadat a uložit 15místné nebo 16místné číslo do pole **ID karty** na stránce **Kreditní karty** pro zaměstnance. |
| Ověření účel cestovní žádosti                      | Tuto možnost zapněte, chcete-li omezit uživatele na existující sadu hodnot, která je nakonfigurována v poli **Účel výkazu výdajů**, když vytvářejí cestovní žádanky. |

## <a name="financial"></a>Finanční služby

| Pole                                                                                    | Popis |
|------------------------------------------------------------------------------------------|-------------|
| Název deníku účetní knihy                                                                | Vyberte název deníku účetní knihy, do kterého se zaúčtují schválené výkazy výdajů. |
| Povolit vymáhání daní z výdajů                                                        | Tuto možnost vyberte, pokud chcete povolit vrácení daně z výdajů pro způsobilé výdaje. Tuto možnost nelze vybrat, pokud je povolena DPH a daň z užívání v USA. |
| Okamžitě zaúčtovat hotovostní zálohy                                                           | Vyberte tuto možnost, chcete-li po dokončení procesu platby a převodu zaúčtovat schválenou hotovostní zálohu. Pokud tato možnost není vybrána, proces platby a převodu vygeneruje nezaúčtovaný obecný deník. |
| Opravit účetní datum během účtování                                                   | Tuto možnost vyberte, chcete-li aktualizovat účetní datum při zaúčtování výdajů, pokud je aktuální období pozastaveno nebo uzavřeno. Účetní datum bude nastaveno na další otevřené období. |
| Povolit seskupování transakcí na základě offsetového účtu uvedeného v platební metodě       | Vyberte tuto možnost, chcete-li shrnout transakce výdajů pro výkaz výdajů na základě offsetového účtu, který je zadán v platební metodě výdajů. |
| Včetně daně                                                                             | Vyberte tuto možnost, chcete-li do částky výdajů ve výchozím nastavení zahrnout DPH. |
| Uvolněte břemena při uzavírání cestovních požadavků                                      | Vyberte tuto možnost, abyste uvolnili zatížené prostředky, když je schválená cestovní žádost uzavřena. |
| Povolit odeslání cestovní žádanky při překročení rozpočtu pro registr rozpočtu a rozpočet projektu | Tuto možnost vyberte, pokud chcete zaměstnancům umožnit odeslat cestovní žádanky ke schválení, přestože překračují buď povolený rozpočet, který je nastaven v registru rozpočtu, nebo povolený rozpočet pro projekt. |
| Povolit odeslání sestavy výdajů při překročení rozpočtu pro registr rozpočtu a rozpočet projektu     | Tuto možnost vyberte, pokud chcete zaměstnancům umožnit odeslat sestavu výdajů ke schválení, přestože překračují buď povolený rozpočet, který je nastaven v registru rozpočtu, nebo povolený rozpočet pro projekt. |
| Povolit schválení sestavy výdajů při překročení rozpočtu pouze pro registr rozpočtu.                 | Vyberte tuto možnost, chcete-li povolit schvalovatelům schvalovat výkazy výdajů, které překračují povolený rozpočet nastavený v registru rozpočtu. |

## <a name="per-diem"></a>Denní diety

| Pole                                 | Popis |
|---------------------------------------|-------------|
| Minimální počet hodin denně            | Zadejte výchozí minimální počet hodin, které musí zaměstnanec za den odpracovat, aby měl nárok na denní diety za cestovní výdaje. Tato hodnota se používá jako výchozí hodnota pouze pro pole **Minimální počet hodin** pole pro úrovně denních diet. |
| Procento jídla                          | Zadejte výchozí procento stravného, které se použije v první a poslední den výdajů souvisejících s cestováním, když je pole **Vypočítejte snížení jídla o** nastaveno na **Typ jídla za den** nebo **Počet jídel za den**. Pracovní den v první a poslední den může být kratší než standardní pracovní den. Proto se částka stravného v těchto dnech může lišit od standardní částky. Pokud je procento nastaveno na **0** (nula), odpočty za první a poslední den budou 0,00. |
| Procento hotelu                         | Zadejte výchozí procento stravného pro hotely, které se použije první a poslední den výdajů souvisejících s cestováním. Pracovní den v první a poslední den může být kratší než standardní pracovní den. Proto se částka stravného v těchto dnech může lišit od standardní částky. Pokud je procento nastaveno na **0** (nula), odpočty za první a poslední den budou 0,00. |
| Ostatní procenta                         | Zadejte výchozí procento stravného pro různé výdaje, které se použije první a poslední den výdajů souvisejících s cestováním. Pracovní den v první a poslední den může být kratší než standardní pracovní den. Proto se částka stravného v těchto dnech může lišit od standardní částky. Pokud je procento nastaveno na **0** (nula), odpočty za první a poslední den budou 0,00. |
| Snížení procenta na snídani | Zadejte částku, o kterou je dieta sníženo o snídani. Například pokud zaměstnanec obdrží snídani zdarma, možná budete chtít snížit částku dieta o 10 procent. |
| Snížení procenta na oběd     | Zadejte částku, o kterou je dieta sníženo o oběd. Například pokud zaměstnanec obdrží oběd zdarma, možná budete chtít snížit částku dieta o 15 procent. |
| Snížení procenta na večeři    | Zadejte částku, o kterou je dieta sníženo o večeři. Například pokud zaměstnanec obdrží večeři zdarma, možná budete chtít snížit částku dieta o 25 procent. |
| Vypočítejte snížení jídla o           | Určete, jak má systém vypočítat snížení denního jídla výběrem, zda je snížení založeno na typu jídla na cestu nebo na den, nebo zda je založeno na počtu povolených jídel denně. |
| Zaokrouhlování denních diet                     | Vyberte typ zaokrouhlování, který se používá pro výdaje na denní diety. Pokud vyberete normální zaokrouhlování, všechny výdaje za denní diety, které mají částku 0,50, se zaokrouhlí nahoru na 1,00 a všechny diety, které mají částku menší než 0,50, se zaokrouhlí dolů na 0,00. |
| Výpočet základu denních diet dne          | Vyberte, zda částka za denní diety závisí na kalendářním dni nebo 24hodinovém období. |

## <a name="fax-cover-pages"></a>Titulní stránky faxu

| Pole                          | Popis |
|--------------------------------|-------------|
| Pokyny                   | Zadejte pokyny, které musí zaměstnanci dodržovat, když vytvářejí titulní stránku pro fax, který se používá k odesílání účtenek souvisejících se sestavou výdajů. Chcete-li zadat text specifický pro jazyk, který se zobrazí, na základě uživatelského jazyka vyberte **Překlady**. |
| ID uživatele (informace o čárovém kódu) | Tuto možnost vyberte, pokud chcete uložit jedinečný identifikátor zaměstnance do čárového kódu, který se používá na titulní stránce faxu. |
| Čárový kód                       | Vyberte čárový kód, který se použije na titulní stránce faxu. Ve správě výdajů jsou podporovány čárové kódy 39 a 128. |

## <a name="anti-corruption"></a>Protikorupční

| Pole                                 | Popis |
|---------------------------------------|-------------|
| Zobrazit protikorupční osvědčení   | Vyberte tuto možnost, chcete-li zobrazit protikorupční text při vytváření výkazu výdajů. Poté lze povolit konkrétní kategorie výdajů, které budou vyžadovat, aby bylo ve výkazu výdajů vybráno protikorupční osvědčení. Například kategorie dárků, která souvisí s výdaji státních úředníků, může vyžadovat, aby zaměstnanec potvrdil, že výdaj splňuje zásady společnosti související s vládními úředníky. |
| Protikorupční zpráva pro zadavatele | Zadejte text, který se má zobrazit zaměstnanci, který vytváří sestavu výdajů. Chcete-li zadat text specifický pro jazyk, který se zobrazí, na základě uživatelského jazyka vyberte **Překlady**. |
| Protikorupční zpráva pro schvalovatele  | Zadejte text, který se má zobrazit schvalovateli při vytváření sestavy výdajů. Chcete-li zadat text specifický pro jazyk, který se zobrazí, na základě uživatelského jazyka vyberte **Překlady**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]