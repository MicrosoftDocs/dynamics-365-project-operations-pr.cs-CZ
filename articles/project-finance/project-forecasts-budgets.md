---
title: Projektové předpovědi a rozpočty
description: Microsoft Dynamics 365 Finance poskytuje projektové předpovědi a rozpočty pro správu a řízení vašich projektů.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85a5577968024bf42449c50d72a11414f9207eec
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750360"
---
# <a name="project-forecasts-and-budgets"></a>Projektové předpovědi a rozpočty

[!include [banner](../includes/banner.md)]

Projekty můžete spravovat a řídit dvěma způsoby: pomocí projektových předpovědí nebo rozpočtů. 

Pokud má vaše organizace provozní perspektivu a pokud se zaměřuje na výnosy a náklady odvozené z konkrétních transakcí, použijte projektové předpovědi. Pokud se vaše organizace více zaměřuje na finanční částky, použijte rozpočtování projektů. 

Projektové předpovědi i rozpočty používají modely předpovědí k uchovávání předpokládaných částek transakcí. 

Každá metoda má svoje výhody. Než vyberete metodu pro vaši organizaci, měli byste zvážit následující body.

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **Projektové předpovědi**                  | **Rozpočtování projektů**                              |
| **Přidělení období**     | Transakce nelze explicitně přidělit v rámci fiskálního období. Místo toho je předpověď a její řízení založena na životnosti projektu. Předpovědi jsou založeny na konkrétním datu, a proto musíte použité období odvodit od tohoto data. | Transakce můžete přidělit za celý projekt nebo fiskální období. Pokud přidělíte za celé období, můžete nevyužité částky převést do dalšího fiskálního období. |
| **Prohlížení transakcí**  | Transakce můžete zobrazit ve formulářích předpovědí, kde vidíte předpovědi za celou společnost a všechny projekty bez ohledu na jejich hierarchii. Chcete-li se zaměřit na konkrétní projekt, musíte filtrovat data.                                       | Rozpočtované transakce můžete zobrazit pro jednu hierarchii projektu. Proto můžete zobrazit podrobnosti transakce u nadřazeného projektu nebo jeho dílčích projektů.                 |
| **Transakční proměnné** | Když zadáváte transakce předpovědi, můžete použít všechny atributy, které existují pro skutečnou transakci. To umožňuje vyšší míru podrobností v předpovědi. Můžete například zadat podrobnosti o množství, pracovnících, položkách nebo vlastnostech výrobních linek.         | Když zadáváte podrobnosti o rozpočtu, můžete použít pouze částky, kategorie a aktivity.                    |
| **Zabezpečení**              | Prognózování je založeno na transakcích, které zadáte do formulářů předpovědi, a nezahrnuje žádný mechanismus řízení procesu. Kterýkoli pracovník, který má oprávnění k formuláři předpovědi, může revidovat informace, aniž by bylo nutné schválení úprav.                                        | Rozpočtování využívá systém pracovních postupů, který povoluje správu změn a umožňuje vám udržovat historii revizí.         |
| **Typy položek**           | Položky transakce předpovědi jsou založeny na počtu jednotek a na nákladových a prodejních jednotkových cenách.  | Podrobnosti rozpočtu jsou založeny na částkách, které jsou rozděleny mezi náklady a výnosy.                                          |
| **Modely předpovědí**       | Protože každá předpověď musí být přidružena k modelu, můžete vytvořit více modelů předpovědí a také nastavit dílčí modely.           | Projektové rozpočtování omezuje modely předpovědí, které se používají pro rozpočtování. Menší počet modelů předpovědí může pomoci zvýšit konzistenci projekcí.                           |
| **Překročení nákladů**         | Zadávání transakcí, které způsobí překročení nákladů, můžete pouze povolit nebo zakázat.   | Rozpočtování projektů poskytuje uživatelům další možnosti řízení. Můžete povolit varování a překročení.                    |
| **Ovládací prvek**               | Řízení předpovědi se provádí pomocí redukce předpovědi. Skutečné částky jsou odečteny od zůstatků transakcí předpovědí bez jakékoli záznamu pro audit. To může ztížit dohledání, kde došlo ke skutečným transakcím.                   | Při řízení projektového rozpočtu se skutečné částky odečítají od částek ve zbývajícím rozpočtu. To umožňuje vytvářet přehlednější záznam pro audit.                                   |

## <a name="project-forecasts"></a>Projektové předpovědi
Když používáte projektové předpovědi, můžete zadat transakce předpovědí do formulářů předpovědi pro každý typ transakce. Každý atribut, který je k dispozici pro skutečnou transakci, lze použít pro transakci předpovědi – například ziskovost linky, atributy linky, pracovníky nebo popisy. Můžete také plánovat, jak dlouho po vzniku nákladů budete zákazníkovi fakturovat. 

Transakce prognózování projektů jsou založeny na jednotkách a částkách. 

Každou projektovou předpověď musíte spojit s modelem předpovědi. Když zadáte transakci předpovědi, automaticky se navrhne model předpovědi. Model předpovědi funguje jako kontejner pro transakce předpovědi. 

Modely předpovědi můžete označit jako dílčí modely určitého modelu. To vám umožní předpovídat podle regionu, časového období nebo oddělení. Transakce předpovědi můžete zkopírovat do modelu a vytvořit nový model. Transakce můžete také převést do hlavní knihy. Protože mezi předpovědí a modelem existuje vztah jedna k jedné, každý model předpovědi vytváří samostatný rozpočet pro projekt. 

Modely předpovědí mohou používat redukci předpovědi jako kontrolní mechanismus pro projekty. Při redukci předpovědi snižují skutečné transakce zůstatky transakcí předpovědi. Protože se však redukce předpovědi použije na nejvyšší projekt v hierarchii, poskytuje omezený pohled na změny v předpovědi. Například pokud je pracovník přidružen k dílčímu projektu, skutečné transakce pro pracovníka jsou zaúčtovány do nadřazeného projektu. To může ztěžovat sledování změn, protože nemůžete snadno určit, která transakce ve kterém dílčím projektu způsobila snížení částky předpovědi. Proto je vhodné vytvořit kopii modelu předpovědi, na kterou použijete redukci předpovědi. Poté můžete pomocí sestav zobrazit, co bylo původně předpovězeno. 

Projektové předpovědi můžete revidovat, kopírovat, mazat nebo přenášet do rozpočtu hlavní knihy. Neexistuje však žádné řízení procesu. Kterýkoli pracovník, který má oprávnění k formuláři předpovědi, může provádět revize bez jejich následné kontroly.

-   **Revidovat** – Předpověď transakce můžete revidovat ve stejných formulářích, kde byly vytvořeny původní záznamy.
-   **Kopírovat nebo odstranit** – Když kopírujete transakce předpovědí, kopírujete řádky transakcí jednoho modelu prognózy do jiného modelu prognózy. Když odstraníte předpověď, odstraníte transakce předpovědi z modelu předpovědi. Chcete-li omezit transakce předpovědi, které se kopírují nebo odstraňují, vyberte konkrétní typy transakcí a data. To vám umožní kopírovat nebo mazat pouze konkrétní části předpovědi.
-   **Převod** – Když převedete projektovou předpověď do rozpočtu hlavní knihy, převedete transakce předpovědi modelu předpovědi do rozpočtu hlavní knihy. Veškeré dříve převedené transakce můžete přepsat v rozpočtu hlavní knihy, do kterého přenesete projektovou předpověď.

## <a name="project-budgets"></a>Projektové rozpočty
Projektové rozpočty jsou jednodušší metodou než předpovědi, ačkoli se integrují do modelů předpovědí. Rozpočet používá jediný vstupní formulář pro původní podrobnosti rozpočtu a revize, a umožňuje projekce založené pouze na částce, kategorii nebo aktivitě. 

V rozpočtování projektu musí být všechny původní rozpočty a revize odeslány do pracovního postupu projektu ke schválení. Pracovní postupy vám dávají větší kontrolu nad procesem a vytvářejí záznam historie změn. 

Rozpočtování projektů se podobá rozpočtu hlavní knihy, ale jeho nastavení je rychlejší a snazší. Mnohé možnosti v rozpočtování hlavní knihy, například číselné řady nebo měna, nemusí být pro projekty nastaveny samostatně.

Projektové rozpočty jsou automaticky spojeny se dvěma modely předpovědi, jedním pro původní rozpočet a druhým pro zbývající rozpočet. Proto mohou sestavy založené na modelech předpovědí využívat data rozpočtu. Když je projektový rozpočet přijat, systém vytvoří transakce předpovědi na základě přidružených modelů, které se používají pro účely vykazování a řízení.

## <a name="forecast-models"></a>Modely předpovědí
Modely předpovědí mají jednovrstvou hierarchii. To znamená, že jedna projektová předpověď musí být spojena s jedním modelem předpovědi.

Pokud používáte projektové předpovědi, můžete modely identifikovat jako dílčí modely. To vám umožní poté předpovídat podle regionu, časového období nebo oddělení. Můžete například vytvořit model předpovědi na rok a poté vytvořit dílčí modely pro regionální předpovědi Severovýchod, Jihovýchod, Severozápad a Jihozápad, které přijímají regionální manažeři. Výběrem různých možností v dostupných sestavách můžete zobrazit informace podle celkové předpovědi nebo podle dílčího modelu.



