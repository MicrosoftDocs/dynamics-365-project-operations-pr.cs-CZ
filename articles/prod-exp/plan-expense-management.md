---
title: Konfigurace správy výdajů
description: Tento článek popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování před konfigurací oblasti Správa výdajů v aplikaci Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d919a26000b127dd6fb2fd8a49d79e3087f1c403
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8709961"
---
# <a name="configure-expense-management"></a>Konfigurace správy výdajů

Toto téma popisuje úvahy a rozhodnutí, která musíte udělat během procesu plánování, než nakonfigurujete správu výdajů. Ve správě výdajů můžete ukládat informace o platebních metodách, cestovních požadavcích, sestavách výdajů, zásadách atd.

Protože mnohá rozhodnutí, která uděláte při plánování konfigurace správy výdajů, jsou založena na hierarchii a finanční struktuře vaší organizace, musíte si přečíst plánovací dokumenty pro tyto oblasti.

## <a name="intercompany-expenses"></a>Mezipodnikové výdaje

Když povolíte mezipodnikové výdaje, umožníte právním subjektům a zaměstnancům nést náklady jménem jiné právnické osoby a inkasovat platby od právnické osoby zaměstnávající ve vaší organizaci. Například zaměstnanec v právnické osobě A dokončí projekt pro právnickou osobu B a v projektu vzniknou cestovní výdaje. Pokud jsou povoleny mezipodnikové výdaje, může zaměstnanec následně předložit sestavu výdajů, které zaúčtuje výdaj právnické osobě B, a výdaj musí poté uhradit právnická osoba A. Pokud vaše organizace nemá více právnických osob, nemusíte povolit mezipodnikové výdaje.

**Rozhodnutí:** Chcete povolit mezipodnikové výdaje?

## <a name="financial-management"></a>Finanční správa

Správa výdajů je úzce integrována do finančního řízení vaší organizace. Spousta vaší konfigurace pro správu výdajů bude založena na rozhodnutích, které jste přijali v oblasti financování vaší organizace. V následujících částech jsou popsány různé oblasti, které vyžadují plánování a rozhodování na základě finančních rozhodnutí vaší organizace a pokynů vašeho vedoucího týmu.

### <a name="per-diems"></a>Denní diety

Musíte definovat denní diety zaměstnanců, které vaše organizace poskytuje. Protože se denní diety obvykle používají k pokrytí výdajů, jako jsou stravování, ubytování a další vedlejší výdaje, můžete vytvořit pravidla pro denní diety, které vaše organizace nabízí. sazby denních diet mohou být založeny na ročním období, místě cesty nebo na obou kritériích. Když definujete pravidlo denní diety, můžete určit, že určité procento sazby diety bude zadrženo, pokud pracovník obdrží bezplatné jídlo nebo služby. Můžete také definovat úrovně denních diet a nastavit pomocí nich minimální a maximální počet hodin, které musí cesta pracovníka trvat, aby byla sazba denní diety použita.

**Rozhodnutí:**

- Výchozí pravidla denních diet pro první a poslední den:

    - Jaký je minimální počet hodin, který může zaměstnanec za den vykázat a přesto dostat denní dietu?
    - Dochází ke snížení částky nabízené za jídlo za první a poslední den? Pokud dojde ke snížení, jaké je jeho procento?
    - Dochází ke snížení částky nabízené za ubytování v hotelu za první a poslední den? Pokud dojde ke snížení, jaké je jeho procento?
    - Dochází ke snížení částky nabízené za jiné výdaje, ke kterým dojde v prvním a posledním dnu? Pokud dojde ke snížení, jaké je jeho procento?

- Výchozí pravidla denních diet:

    - Dochází k procentnímu snížení denní diety za každé jídlo, pokud je například jídlo bezplatné? Pokud dojde ke snížení, jaké je jeho procento za každé jídlo?
    - Je snížení za jídlo počítáno za den, za celou cestu nebo podle počtu jídel za den?
    - Mají být částky za diety zaokrouhleny běžným způsobem nebo zaokrouhleny nahoru?
    - Počítají se diety za 24 hodin nebo za kalendářní den?

- Pravidla denních diet, která jsou založena na umístění:

    - Liší se sazby denních diet podle umístění? Jaká umístění jsou zahrnuta?
    - Pokud se sazby denních diet liší podle umístění, jaká procentní částka pro každou lokalitu je poskytována pro následující typy výdajů:

        - Stravování
        - Hotel
        - Jiné výdaje

### <a name="expense-management-journals-and-accounts"></a>Deníky a účty pro správu výdajů

Správa výdajů vyžaduje, abyste používali více deníků a účtů. Musíte se například rozhodnout, zda se stejný účet používá pro hotovostní zálohy a spory o kreditní karty.

**Rozhodnutí:**

- Do kterého deníku hlavní knihy jsou schválené sestavy výdajů zaúčtovány?
- Který účet se používá pro hotovostní zálohy?
- Měly by být peněžní zálohy zaúčtovány okamžitě?

### <a name="payment-methods"></a>Způsoby platby

Pokud zaměstnancům umožníte, aby vytvářeli výdaje jménem vašeho podniku, musíte definovat způsoby platby, které mohou zaměstnanci používat. Například můžete zaměstnancům umožnit používat hotovost nebo firemní kreditní kartu. Můžete také umožnit zaměstnancům používat osobní kreditní karty a poté zaměstnancům vrátit peníze. U každého povoleného způsobu platby musíte učinit následující rozhodnutí.

**Rozhodnutí:**

- Jaké způsoby platby jsou povoleny?
- Kdo vlastní výdaje na způsob platby?
- Existuje typ offsetového účtu? Pokud existuje typ offsetového účtu, který to je?
- Pokud existuje typ offsetového účtu, který účet to je?
- Pokud je způsobem platby kreditní karta, měl by se tento způsob použít pouze u importovaných transakcí?

### <a name="expense-categories-and-shared-categories"></a>Kategorie výdajů a sdílené kategorie

Když zaměstnanci vytvářejí sestavu výdajů, musí být každý zaznamenaný výdaj přidružen ke kategorii výdajů. Kategorie výdajů jsou odvozeny ze sdílených kategorií, které lze sdílet mezi právnickými osobami ve vaší organizaci. Tyto kategorie lze také sdílet v Řízení projektů a účetnictví, v závislosti na způsobu, jakým je vaše organizace definována. Na základě definice vaší organizace a pokynů od implementačního týmu určete, zda kategorie, které se používají ve správě výdajů, budou použity pouze ve správě výdajů, nebo zda by měly být sdíleny mezi moduly Řízení projektů a účetnictví a Správa výdajů. Poznámka: tyto kategorie lze sdílet mezi moduly Projekty a Výdaje nebo mezi moduly Projekt a Výroba, ale ne mezi moduly Výdaje a Výroba. Pro každou kategorii výdajů musíte učinit následující rozhodnutí.

**Rozhodnutí:**

- Jaká je kategorie výdajů? Mezi příklady patří kategorie letů, hotelů nebo najetých kilometrů.
- Lze kategorii výdajů použít také v modulu Řízení a účetnictví projektů?
- Jaký je typ výdajů?
- Jaký je výchozí způsob platby pro kategorii výdajů?
- Musí být výdaje v kategorii výdajů rozepsány?
- Jaký je hlavní výchozí účet pro kategorii výdajů?
- Jaká je výchozí skupina daně z prodeje zboží pro kategorii výdajů?
- Jsou pro kategorii výdajů povoleny další způsoby platby? Jsou-li povoleny další způsoby platby, které to jsou?
- Existují v této kategorii výdajů podkategorie? Když existují podkategorie, musíte rovněž učinit následující rozhodnutí:

    - Jsou některé z podkategorií vyloučeny z vymáhání daní?
    - Jaká je skupina daně z prodeje zboží u podkategorií?

Pokud se kategorie výdajů používá také v Řízení projektů a účetnictví, odpovězte na zbývající otázky. V opačném případě přejděte k další části.

- Které nákladové účty budou použity pro následující výdaje?

    - Náklady
    - Přidělení mezd
    - Hodnota nákladů nedokončené práce
    - Náklady – položka
    - Nedokončená výroba – hodnota nákladů – položka
    - Časově rozlišená ztráta
    - NV – časově rozlišená ztráta

- Které účty výnosů budou použity pro následující položky?

    - Fakturované výnosy
    - Časově rozlišené výnosy – hodnota prodeje
    - NV – prodej
    - Časově rozlišené výnosy – výroba
    - NV – výroba
    - Časově rozlišené výnosy – zisk
    - NV – zisk
    - Časově rozlišené výnosy – předplatné
    - NV – předplatné

### <a name="taxes"></a>Daně

U daní souvisejících s výdaji musíte určit, co je zahrnuto nebo povoleno v sestavách výdajů.

**Rozhodnutí:**

- Je prodejní daň zahrnuta do částky výdajů?
- Mají být povoleny vratky daní u výdajů?

    > [!NOTE]
    > Pokud jste se při plánování hlavní knihy rozhodli použít prodejní daň v USA a použít daňová pravidla, nemůžete povolit vratky daní u výdajů. (Chcete-li použít prodejní daň v USA a použít daňová pravidla, nastavte možnost **Použít pravidla zdanění prodejní daně** na **Ano** .)

## <a name="policies"></a>Zásady

Vytvořením zásad sestav výdajů můžete pomoci vaší organizaci ušetřit čas a peníze, když zaměstnancům vzniknou náklady jejím jménem. Zásady pomáhají zaručit, že zaměstnanci nepřekročí rozpočet, dostanou všechny požadované informace a utratí peníze, pouze pokud je potřebují. Pro každou vytvořenou zásadu sestavy výdajů a každou zásadu schvalování sestavy výdajů musíte učinit následující rozhodnutí.

**Rozhodnutí:**

- Jaký je název zásady?
- K čemu zásada výdajů slouží?
- Pokud jste se dříve rozhodli povolit mezipodnikové výdaje, na které společnosti ve vaší organizaci se tato zásada bude vztahovat?
- Kdy začne zásada platit?
- Kdy platnost zásady skončí?
- Jaké je pravidlo zásady?
- Jaký je výstup pravidla zásady?


[!INCLUDE[footer-include](../includes/footer-banner.md)]