---
title: Práce s datovým modelem Project Service Automation
description: Toto téma obsahuje informace o způsobu práce s datovým modelem.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8d63a1b36abe0a154c43e99738340f32f28c2f5e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120265"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Práce s datovým modelem Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation rozšiřuje další entity aplikace a zavádí vlastní entity v datovém modelu Common Data Service. Toto téma popisuje některé entity, se kterými se setkáte v typických scénářích vytváření sestav PSA.

## <a name="reporting-on-opportunities"></a>Podávání zpráv o příležitostech

Project Service Automation rozšiřuje entitu **Příležitost** aplikace Dynamics 365 Sales přidáním polí, která umožňují scénáře založené na projektech. Tato pole jsou označena názvem schématu, který má předponou **msdyn\_** Jedním novým polem, které je důležité pro vykazování příležitostí PSA, je **Typ objednávky**. Hodnota **Na základě práce** pro toto pole označuje, že je tato příležitost příležitostí PSA. Mezi další pole, která byla do entity přidána, patří **Smluvní organizace**, které zaznamenává organizaci, jenž příležitost obsahuje, a **Manažer obchodních vztahů**, které zaznamenává jméno manažera obchodních vztahů, který je za příležitost zodpovědný.

Entita **Řádek příležitosti** obsahuje i pole, která souvisejí s aplikací Project Service. **Způsob fakturace** označuje, zda má být řádek příležitosti fakturován na základě času a materiálu nebo na základě pevné ceny a **Projekt** zaznamenává název projektu, který příležitost podporuje. Další pole, která lze vykazovat u částek zachycených nákladů a rozpočtů zákazníka pro položku řádku.

## <a name="reporting-on-quotes"></a>Vykazování v nabídkách

PSA rozšiřuje entitu prodeje **Nabídka** přidáním polí souvisejících s projektem. **Typ objednávky** rozlišuje nabídky PSA a nabídky, které nepocházejí z PSA. Hodnota **Na základě práce** pro toto pole označuje, že je tato nabídka nabídkou PSA. Další pole, která mohou být relevantní pro vykazování v nabídkách PSA, zahrnují pole částek, jako jsou např. **Účtovatelné náklady**, **Nečtovatelné náklady**, **Hrubá marže**, **Odhady** a **Rozpočet**. Další užitečná pole označují, zda je nabídka zisková, zda bude dokončena podle plánu a zda splňuje očekávání rozpočtu zákazníka.

PSA také rozšiřuje entitu prodeje **Řádek nabídky**. Jedno pole, které PSA přidává, je **Způsob fakturace**, toto pole označuje, jak bude řádek nabídky fakturován (čas a materiál nebo pevná cena). Další pole, která byla přidána do entity, zaznamenávají související projekt, který podporuje řádek nabídky, fakturaci, náklady a rozpočet.

PSA datového modelu Dynamics 365 také přidává nové entity související s nabídkou. Zde je uvedeno několik příkladů:

- **Podrobnosti řádku nabídky** – tato entita obsahuje podrobnosti o odhadu projektu na řádku nabídky. Obsahuje dva záznamy pro každý řádek nabídky. V jednom záznamu jsou uloženy náklady a podrobnosti nákladů řádku nabídky a druhý záznam uchovává prodejní částku a podrobnosti prodeje řádku nabídky.
- **Rozpis faktury řádku nabídky** – tato entita obsahuje plán fakturace pro řádek nabídky. Tento plán je generován na základě četnosti fakturace, která je přiřazena k řádku nabídky.
- **Milník řádku nabídky** – tato entita obsahuje fakturační milníky pro řádky nabídky s pevnou cenou.
- **Analytický rozpis řádku objednávky** – tato entita obsahuje finanční podrobnosti řádku nabídky. Tyto podrobnosti mohou být užitečné pro vykazování částek nabízeného prodeje a odhadovaných nákladů podle různých dimenzí.

Dalšími entitami, které PSA do nabídek přidává, jsou **Projektový ceník řádku nabídky**, **Kategorie zdroje řádku nabídky** a **Kategorie transakce řádku nabídky**.

![Diagram zobrazující nabídku, řádek nabídky a vztahy projektů](media/PS-Reporting-image2.png "Diagram zobrazující nabídku, řádek nabídky a vztahy projektů")

## <a name="reporting-on-project-contracts"></a>Podávání zpráv o projektových smlouvách

PSA rozšiřuje entitu prodeje **Objednávka**, která se používá při záznamu projektových smluv. Přidá nové důležité pole **Typ objednávky**, které označuje smlouvu jako projektovou smlouvu PSA namísto prodejní objednávky. Hodnota **Na základě práce** pro toto pole označuje, že je tato objednávka projektovou smlouvou PSA. Další nová pole přidaná do entity **Objednávka** zaznamenávají podrobnosti o nákladech, stavu smlouvy PSA a organizaci, která smlouvu vlastní.

PSA také rozšiřuje entitu **Řádek prodejní objednávky**. Mezi pole, která jsou přidána, patří pole, která zaznamenávají způsob fakturace (čas a materiál nebo pevnou cenu), částky rozpočtu zákazníka a podkladový projekt.

PSA také přidává nové entity, které jsou navrženy pro projektové smlouvy. Zde je uvedeno několik příkladů:

- **Podrobnosti řádku projektové smlouvy** – tato entita obsahuje podrobnosti na úrovni řádku, které jsou zahrnuty do částky řádku smlouvy. Mohou být stejně podrobné jako položky řádku, které jsou generovány z plánu projektu na úrovni úkolu.
- **Rozpis faktury řádku smlouv** – tato entita obsahuje plán fakturace, který je generován na základě četnosti faktury přiřazené k řádku smlouvy.
- **Milník smlouvy** – tato entita obsahuje fakturační milníky pro řádky smlouvy, které obsahují požadavek na fakturaci s pevnou cenou.

Dalšími entitami, které PSA do smluv přidává, jsou **Projektový ceník řádku projektové smlouvy**, **Kategorie zdroje řádku projektové smlouvy** a **Kategorie transakce řádku projektové smlouvy**.

![Diagram zobrazující objednávku, řádek objednávky a vztahy projektů](media/PS-Reporting-image3.png "Diagram zobrazující objednávku, řádek objednávky a vztahy projektů")

## <a name="reporting-on-projects"></a>Podávání zpráv o projektech

Entita **Projekty** a související entity jsou výhradní pro PSA. **Projekt** je entita nejvyšší úrovně, která slouží k zachycení operací na straně práce a nákladů. Zde je seznam souvisejících entit:

- **Člen projektového týmu** – tato entita obsahuje podrobnosti o rezervovatelných zdrojích, které jsou k projektu přiřazeny. Tyto zdroje mohou být obecnými rezervovatelnými zdroji nebo mohou být pojmenovanými zdroji, které buď zadá projektový manažer, nebo jsou generovány z plánu projektu.
- **Projektový úkol** – tato entita obsahuje úkoly, které tvoří plán projektu nebo harmonogram.
- **Přiřazení zdroje** – tato entita obsahuje přiřazení úkolu k rezervovatelnému zdroji.
- **Požadavek na zdroj** – tato entita obsahuje požadavky na libovolné obecné zdroje členů týmu.
- **Odhad** a **Řádek odhadu** – tyto entity mají vztah záhlaví/řádek a obsahují odhady výdajů pro projekt. Odhady úkolů jsou uloženy v entitě **Odhad zdroje**.

![Diagram zobrazující požadavek na zdroj a vztahy projektů](media/PS-Reporting-image4.png "Diagram zobrazující požadavek na zdroj a vztahy projektů")

## <a name="reporting-on-resources"></a>Podávání zpráv o zdrojích

Zdroje projektu používají entity **Rezervovatelný zdroj** z aplikace Universal Resource Scheduling (URS), které jsou sdíleny s dalšími aplikacemi, jako je např. Microsoft Dynamics 365 Field Service. Zde je seznam entit, které budete pravděpodobně muset použít při vykazování zdrojů projektu:

- **Rezervovatelný zdroj** – tato entita představuje uživatele, kontakt, obecný zdroj, obchodní vztah, skupinu nebo vybavení, které se používají v projektovém týmu.
- **Charakteristiky rezervovatelného zdroje** – tato entita zahrnuje dovednosti, certifikace nebo vzdělání zdroje. Charakteristiky mohou obsahovat hodnoty hodnocení, které jsou definovány modelem hodnocení.
- **Kategorie rezervovatelného zdroje** – tato entita představuje roli rezervovatelného zdroje.
- **Rezervace rezervovatelného zdroje** – tato entita představuje čas, který je v projektech rezervovaný pro daný zdroj. Každá rezervace obsahuje jak entitu záhlaví, tak entity řádků a každý řádek obsahuje stav, který představuje stav rezervace.

![Diagram ukazující vztahy rezervovatelných charakteristik zdroje](media/PS-Reporting-image5.png "Diagram ukazující vztahy rezervovatelných charakteristik zdroje")

## <a name="reporting-on-actual-transactions"></a>Vykazování skutečných transakcí

Pokud v PSA schvalujete časový rozvrh nebo výdaj nebo fakturujete smlouvu, je obchodní transakce zachycena ve entitě **Skutečnost**. Tato entita může sloužit jako základ pro téměř všechny sestavy týkající se financí v rámci PSA. Entita **Skutečnost** zachycuje nákladové a prodejní transakce pro obchodní událost. Zachycuje také mnoho relevantních atributů.

Při práci s entitou **Skutečnost** je důležité porozumět, jaká transakce nebo jaké transakce jsou v entitě zaznamenány a kdy jsou transakce zaznamenány. Zde je typický tok při práci s časovými záznamy (tok výdajových záznamů je podobný):

1. Po uložení časového záznamu se v entitě **Skutečnost** nevytvoří žádné záznamy.
2. Po odeslání časového záznamu se v entitě **Skutečnost** nevytvoří žádné záznamy.
3. Po schválení časového záznamu se v entitě **Skutečnost** vytvoří jeden záznam a může se vytvořit i druhý záznam. První záznam uchovává náklady časového záznamu. Druhý záznam uchovává částku nefakturovaného prodeje časového záznamu. Druhý záznam závisí na tom, zda je k projektu přiřazen zákazník, nabídka, nebo řádek smlouvy.

    | Datum dokumentu | Typ transakce | Třída transakce | Zákazník         | Contract   | Zdroj     | Role zdroje | Typ fakturace | Množství | Cena za jednotku | Částka |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Náklady             | Time              | Alpine ski house | Alpine CRM | Dagmar Stejskalová | Projektový manažer   | Účtovatelné   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Nefakturovaný prodej   | Time              | Alpine ski house | Alpine CRM | Dagmar Stejskalová | Projektový manažer   | Účtovatelné   | 8.0      | 100.00     | 800.00 |

    Tyto dva záznamy jsou oddělené, ale související záznamy. Nejsou ani debetní, ani kreditní.

4. Je-li smlouva přidružena k projektu, vytvoří se v entitě **Skutečnost** při fakturaci časového záznamu další dva záznamy. Nejprve je vytvořena záporná částka pro záznam nefakturovaného prodeje. Tento záznam v podstatě stornuje nefakturovaný prodej. Poté se vytvoří transakce pro fakturovaný prodej. Tyto záznamy jsou opět oddělené, ale související záznamy, ani debetní, ani kreditní.

    | Datum dokumentu | Typ transakce | Třída transakce | Zákazník         | Contract   | Zdroj     | Role zdroje | Typ fakturace | Množství | Cena za jednotku | Částka   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Nefakturovaný prodej   | Time              | Alpine ski house | Alpine CRM | Dagmar Stejskalová | Projektový manažer   | Účtovatelné   | - 8,0    | 100.00     | - 800,00 |
    | 2/4/18        | Fakturovaný prodej     | Time              | Alpine ski house | Alpine CRM | Dagmar Stejskalová | Projektový manažer   | Účtovatelné   | 8.0      | 100.00     | 800.00   |

Entita **Původ transakce** zaznamenává původ záznamu **Skutečnost** a entita **Propojení transakce** zaznamenává související záznamy pro záznam **Skutečnost**. Záznam **Skutečnost** dále obsahuje odkazy na projekt, projektovou smlouvu (objednávky), rezervovatelné prostředky a zákazníka.

![Diagram zobrazující transakční připojení, původ a skutečné vztahy](media/PS-Reporting-image6.png "Diagram zobrazující transakční připojení, původ a skutečné vztahy")
