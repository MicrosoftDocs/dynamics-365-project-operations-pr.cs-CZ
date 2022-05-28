---
title: Přehled struktur rozpisu prací
description: Struktura rozpisu práce (WBS) je popis práce, která bude pro projekt provedena. Je to hierarchie úkolů, která představuje pochopení projektového týmu ohledně složení práce a velikosti, nákladů a doby trvání každé komponenty nebo úkolu.
author: Yowelle
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1e69d7cc97e3a7a59bdba387282fe19d12f5780
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683392"
---
# <a name="work-breakdown-structures-overview"></a>Přehled struktur rozpisu prací

[!include [banner](../includes/banner.md)]

Struktura rozpisu práce (WBS) je popis práce, která bude pro projekt provedena. Je to hierarchie úkolů, která představuje pochopení projektového týmu ohledně složení práce a velikosti, nákladů a doby trvání každé komponenty nebo úkolu. WBS má tři hlavní účely:

-   Popsání rozdělení nebo složení práce v úkolech.
-   Plánování práce na projektu.
-   Odhadněte náklady na každý úkol.

Stupeň podrobností ve WBS závisí na úrovni přesnosti, která je požadována v odhadech, a na úrovni sledování, která je požadována oproti těmto odhadům. Projekty, které mají velmi nízkou toleranci skluzů v harmonogramu nebo nákladech, obvykle vyžadují podrobnější strukturovaný rozpis prací a pečlivé sledování postupu práce a nákladů oproti tomuto rozpisu. Tento druh projektu je běžný ve stavebnictví a strojírenství. 

Naproti tomu projekty v průmyslových odvětvích, jako jsou média a reklama, software IT infrastruktura, bývají svého druhu a produktivita je relativní ke zkušenostem a kompetencím jednotlivce, který tento úkol plní. Proto tato odvětví používají strukturovaný rozpis prací k získání přibližné velikosti projektu, nikoli k podrobnému sledování postupu tohoto projektu. 

Budování strukturovaného rozpis prací je intenzivní proces, který se obvykle provádí po dlouhou dobu a který vyžaduje spolupráci a informace od nejrůznějších lidí. Toho téma popisuje, jak můžete pomocí vylepšení strukturovaného rozpisu prací splnit své požadavky na odhady a sledování.

## <a name="prerequisites-for-creating-a-wbs"></a>Požadavky na vytvoření strukturovaného rozpisu prací
Chcete-li vytvořit strukturovaný rozpis prací, musíte být schopni vytvořit pracovní plán a odhadnout cenu práce.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Předpoklady pro vytvoření pracovního plánu

Chcete-li využít možnosti úplného plánování funkcí strukturovaného rozpisu prací, proveďte následující nastavení:

1.  Nastavení výchozího kalendáře a kalendáře projektu:
    1.  Klikněte na **Správa projektů a účetnictví** &gt; **Nastavení** &gt; **Parametry správy projektů a účetnictví** &gt; **Plánování**. V poli **Výchozí pracovní kalendář** zadejte výchozí kalendář. Toto bude výchozí pracovní kalendář pro každý nový projekt, který je vytvořen.
    2.  Můžete změnit výchozí kalendář pro konkrétní projekt. Klikněte na stránku s podrobnostmi o projektu a poté na pevnou kartu **Projektový tým a plánování** a aktualizujte **Plánovací kalendář** výběrem jiného kalendáře.

2.  Nastavte standardní pracovní dny a pracovní dobu. Kalendář, který nastavíte jako pracovní kalendář pro svůj projekt, bude použit v strukturovaném rozpisu prací k určení následujících informací:

-   Pracovní dny a svátky
-   Počet pracovních hodin za den

Chcete-li nastavit pracovní dny a pracovní dobu pro kalendář nebo vytvořit nový kalendář, klikněte na **Správa organizace** &gt; **Společné** &gt; **Kalendáře**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Předpoklady pro odhad nákladů na práci

Chcete-li použít funkce WBS pro odhad celých nákladů, měli byste nastavit náklady a prodejní ceny pro pracovníky, kategorie práce, výdaje a poplatky a položky.

-   Chcete-li nastavit kategorie nákladů a prodejních cen práce, výdajů a poplatků, klikněte na **Řízení projektů a účetnictví** &gt; **Nastavení** &gt; **Ceny**.
-   Chcete-li nastavit náklady a prodejní cenu položek, použijte stránku **Obchodní dohody** pro každou položku na stránce **Vydané produkty** ve správě informací o produktu.

## <a name="creating-a-wbs"></a>Vytváření WBS
Vytvoření strukturovaného rozpisu prací zahrnuje tři aktivity:

1.  **Rozklad práce** - Vytvořte rozdělení práce na zvládnutelné bloky nebo úkoly.
2.  **Pracovní rozvrh** - Odhadněte čas potřebný k dokončení úkolu, nastavte vzájemné závislosti úkolu a vyberte počáteční a konečné datum úkolu.
3.  **Přibližná cena** - Odhad nákladů na každý úkol.

Následující části pojednávají o tom, jak mohou funkce strukturovaného rozpisu prací pomoci s každou z těchto aktivit.

### <a name="work-decomposition"></a>Rozklad práce

Vytvoření rozpisu nebo rozkladu práce je obvykle prvním krokem v procesu vytváření strukturovaného rozpisu prací. Funkce strukturovaného rozpisu prací podporuje následující základní konstrukce pro rozpis nebo rozklad práce. 

**Projektovat kořenový úkol** Kořenová úloha projektu je souhrnný úkol nejvyšší úrovně pro projekt. Všechny ostatní úkoly projektu jsou vytvořeny pod ním. Název kořenového úkolu je vždy nastaven na název projektu. Úsilí, data a doba trvání kořenového uzlu shrnují hodnoty úkolů pod kořenovou úlohou. Nelze upravit vlastnosti kořenového uzlu ani odstranit kořenový uzel.

**Souhrnné nebo kontejnerové úkoly** Souhrnný úkol je úkol, který má pod sebou dílčí úkoly. Souhrnný úkol nemá žádné vlastní úsilí nebo své vlastní náklady. Místo toho je pracovní úsilí a cena souhrnného úkolu součtem pracovního úsilí a nákladů na jednotlivé úkoly. Nejdřívější počáteční datum dílčího úkolu je datum zahájení úkolů kontejneru a poslední koncové datem dílčích úloh je použito jako koncové datum. Název souhrnného úkolu lze upravit, ale vlastnosti plánování (úsilí, data a dobu trvání) nelze upravit. Odstraníte-li souhrnný úkol, odstraníte také všechny jeho dílčí úkoly. 

**Úkoly uzlu listu** Úloha listového uzlu představuje nejpodrobnější pracovní balíček na projektu. Uzel typu list má odhadnuté úsilí, plánovaný počet prostředků, plánované datum zahájení a ukončení a dobu trvání. 

Můžete dokončit následující operace hierarchie, abyste povolili vytvoření pracovní hierarchie nebo rozkladu projektu. 

**Nová úloha** Jakýkoli nový úkol, který vytvoříte, se automaticky přidá pod kořenový uzel a úkolu se automaticky přidělí číslo strukturovaného rozpisu prací. Číslo strukturovaného rozpisu prací představuje úroveň úkolu v hierarchii. U úkolů na první úrovni pod kořenovým úkolem projektu se používá schéma číslování 1, 2, 3 atd. U úkolů které jsou pod první úrovní se používá schéma číslování 1.1, 1.2, 1.3 atd. Pro každou úroveň, která je přidána pod předchozí úroveň, je přidána nová tečkovaná řada čísel. 

V současné době nemůžete přizpůsobit číslování strukturovaného rozpisu prací. 

**Odsadit úkol** Když úkol odsadíte, stane se podřízeným úkolu, který mu předchází. Číslo strukturovaného rozpisu prací nové podřízené úlohy se automaticky přepočítá na základě čísla strukturovaného rozpisu prací jeho nového rodiče. Nadřazený úkol je nyní souhrnný nebo kontejnerový úkol, a proto se stává souhrnem jeho základních úkolů. 

> [!NOTE] 
> Když odsadíte úkoly pod úkolem, který byl před operací odsazení listovým uzlem, ztratí nově vytvořený souhrnný úkol svá vlastní data, úsilí a počet prostředků. Nyní používá souhrn hodnot svých nových základních úkolů. 

**Zmenšit odsazení úkolu** Když zmenšíte odsazení úkolu, přestane být základním úkolem jeho rodiče. Číslo strukturovaného rozpisu prací tohoto úkolu se automaticky přepočítá tak, aby odráželo novou úroveň úkolu v hierarchii. Úsilí, náklady a data předchozího nadřazeného úkolu jsou přepočítány tak, aby nezahrnovaly tento úkol. 

**Posunout nahoru a Posunout dolů** kliknutím na **Posunout nahoru** a **Posunout dolů** změníte pozici úkolu v hierarchii jeho rodiče. Umístění úkolu neovlivňuje úsilí, náklady, data ani dobu trvání úkolu. Číslo strukturovaného rozpisu prací tohoto úkolu se ovšem automaticky přepočítá tak, aby odráželo novou pozici úkolu.

### <a name="schedule-estimation"></a>Odhad plánu

Odhad harmonogramu je obvykle druhým krokem při vytváření strukturovaného rozpisu prací. Jako nejlepší postup byste měli po vytvoření úkolů dokončit odhad plánu. Stranka **Struktura členění práce** ve Finance má dvě sekce. Horní podokno je určeno pro odhad plánu a spodní podokno obsahuje záložku **Odhadované náklady a výnosy**, kterou můžete použít pro odhad nákladů. 
**Závislosti úkolů** Ve strukturovaném rozpisu prací můžete vytvořit předchůdce vztah mezi úkoly. Když k úkolu přiřadíte úkoly předchůdců, lze tento úkol zahájit pouze v případě, že byly dokončeny všechny úkoly typu předchůdce. Plánované datum zahájení úkolu se automaticky nastaví na nejnovější datum všech jeho předchůdců. 

**Plánování úkolů** Následující faktory určují plánování úloh listového uzlu:

-   Předchůdci
-   Úsilí
-   Počet zdrojů
-   Počáteční a koncová data

Počáteční datum úkolu uzlu typu list, který nemá předchůdce, bude automaticky nastaven na výchozí datum zahájení plánování projektu. Doba trvání úkolu uzlu typu list se vždy počítá jako počet pracovních dnů mezi jeho počátečním a koncovým datem. 

*<strong><em>Pravidla plánování</em></strong>* Když je zapnuta automatická pomoc s plánováním, platí pro plánování úkolů pro úkoly uzlů listu následující pravidla:

-   Datum zahájení a ukončení úkolu musí být podle plánovacího kalendáře projektu pracovní dny
-   Datum zahájení úkolu, který má předchůdce, bude automaticky nastaveno na poslední koncové datum jeho předchůdců.
-   Úsilí pro úkol se automaticky vypočítá takto:

Počet osob × doba trvání × hodiny ve standardní pracovní den kalendáře projektu 

V některých případech se můžete chtít od těchto pravidel odchýlit. Můžete vypnout automatické plánování, abyste zabránili tomu, aby Finance automaticky nastavovalo nebo opravovalo jakékoli vlastnosti úkolů uzlů v křídlech. Když zadáte informace o úkolu, který způsobí porušení jakýchkoli pravidel plánování, zobrazí se u úlohy ikona chyby plánování. Pokud si nepřejete, aby se zobrazovaly chyby plánování, klikněte na **Zobrazit chyby plánování** pro vypnutí této funkce. 

> [!NOTE] 
> Hodnoty souhrnné nebo kontejnerové úlohy se nadále počítají jako součet hodnot základních úkolů, bez ohledu na to, zda je zapnuta nebo vypnuta automatická plánovací pomoc. 

**Oprava chyb v plánování** Když je zapnuta automatická podpora plánování, pravděpodobně nedojde k chybám plánování. Pokud však vypnete pomoc s automatickým plánováním a později ji znovu zapnete, mohou se ve službě strukturovaného rozpisu prací zobrazit ikony chyb plánování. 

**Oprava chyb v plánování podle úkolu** Když dvakrát kliknete na ikonu chyby plánu pro konkrétní úkol, zobrazí se v dialogovém okně všechny chyby plánování pro daný úkol. Můžete se rozhodnout, které chyby plánování naplánovat pro daný úkol. 

**Oprava všech chyb plánování** Pokud chcete, aby Finance opravilo všechny chyby plánování ve strukturovaném rozpisu prací, v podokně akcí klikněte na **Opravit všechny nesrovnalosti v plánování**. 

> [!NOTE] 
> Tato funkce může způsobit významné úpravy strukturovaného rozpisu prací. Chyby jsou opraveny v následujícím pořadí:

1.  Odhadované úsilí je u všech úkolů upraveno tak, aby se rovnalo kapacitě definované v kalendáři projektu.
2.  Datum zahájení každého úkolu se upraví tak, aby se úkol spustil po dokončení všech úkolů předchůdce.
3.  Datum zahájení každého úkolu se upraví tak, aby se odstranily mezery v datech zahájení úkolů předchůdců.

### <a name="cost-estimation"></a>Odhadované náklady

Jak již bylo zmíněno dříve v tomto dokumentu, odhad nákladů pro každou úlohu uzlu listu se zadává pomocí karty **Odhadované náklady a výnosy** ve spodním panelu stránky **Struktura členění práce**. 

> [!NOTE] 
> Pro souhrnnou nebo kontejnerovou úlohu nemůžete upravit odhad nákladů. Odhad nákladů na souhrnný úkol se rovná součtu odhadu nákladů na úkoly jeho listového uzlu. Odhadované celkové náklady pro každý úkol se počítají jako součet odhadovaných částek nákladů pro následující typy transakcí:

-   Práce
-   Položka nebo materiál
-   Výdaje

Typ transakce **Poplatek** se používá k odhadu výnosů založených na poplatcích. Tento typ transakce nemá nákladovou složku, a proto se při odhadování nákladů nezohledňuje. 

Typ transakce **Na účet** se používá k zaznamenávání sjednané hodnoty prodeje v projektu s pevnou hodnotou. Tento typ transakce se také při odhadování nákladů nezohledňuje. 

Když odhadujete náklady na práci, materiál a výdaje pro každý úkol, musíte k odhadované ceně přiřadit kategorii projektu. 

**Odhad nákladů práce** Ke každému úkolu uzlu listu přiřadíte pracovní úsilí v hodinách a výchozí kategorii. Proto když nastavíte plán úkolu, odhad nákladů práce pro tento úkol se automaticky přidá do výchozí kategorie pro práci. Tento odhad nákladů je zobrazen na záložce **Odhadované náklady a výnosy** v mřížce **Podrobnosti řádku** pro ten úkol. Pokud požadujete více odhadů nákladů práce, můžete je přidat na této kartě. Pokud zvýšíte nebo snížíte počet hodin v odhadu nákladů práce, plán úlohy se automaticky přepočítá. 

**Odhad nákladů a nákladů na materiál** Záložka **Odhadované náklady a výnosy** také umožňuje odhadnout náklady a náklady na materiál pro úlohu, pokud požadujete odhady. 

Cena a prodejní cena pro každý řádek odhadu práce nebo výdajů jsou založeny na nastavení, které je definováno pro každou kategorii v cenových tabulkách v **Řízení projektů a účetnictví** &gt; **Nastavení** &gt; **Ceny**. Pro položky, náklady a prodejní cenu položek jsou přidány automaticky z položkových nebo obchodních dohod na stránce **Vydané produkty** ve správě informací o produktu.

## <a name="tracking-progress-on-the-wbs"></a>Sledování pokroku ve strukturovaném rozpisu prací
Některá odvětví sledují pokrok projektu oproti strukturovanému rozpisu prací na velmi podrobné úrovni, zatímco jiná sledují pokrok na vyšší úrovni strukturovaného rozpisu prací. Tato část popisuje, jak můžete použít sledování strukturovaného rozpisu prací pro požadavky projektu. 

Finance má pro strukturovaný rozpis prací projektu tři zobrazení: Zobrazení plánování, Zobrazení sledování úsilí a Zobrazení sledování nákladů.

### <a name="planning-view"></a>Zobrazení plánování

Zobrazení Plánování zobrazuje plánovaný nebo základní odhad plánu a informací o nákladech. Ačkoli neexistují žádné funkce pro sledování verze a základní úroveň pro projekt strukturovaného rozpisu prací, hodnoty v tomto zobrazení jsou určeny k představení verze v základní úrovni. Oddíly Odhad plánu a Odhad nákladů tohoto téma popisují toto zobrazení a způsob, jakým se používá k vytvoření strukturovaného rozpisu prací.

### <a name="effort-tracking-view"></a>Zobrazení sledování úsilí

Zobrazení Sledování úsilí zobrazuje pokrok úkolů ve strukturovaném rozpisu prací. Porovnává nashromážděné skutečné hodiny úsilí pro úkol s plánovanými hodinami úsilí. Následující vzorce poskytují hodnoty v zobrazení Sledování úsilí:

-   Procento pokroku = skutečné úsilí vynaložené doposud ÷ plánované úsilí na úkol
-   Zbývající úsilí (známé také jako odhad dokončení \[ETC\]) = plánované úsilí - skutečné dosavadní úsilí
-   Odhad při dokončení (EAC) = zbývající úsilí + skutečné úsilí vynaložené doposud
-   Očekávaná odchylka úsilí = plánované úsilí – EAC

Zobrazení Sledování úsilí zobrazuje projekci rozptylu intenzity úkolu na základě toho, zda je EAC větší nebo menší než plánované úsilí:

-   Je-li EAC větší než plánované úsilí, předpokládá se, že úkol zabere více času, než bylo původně plánováno a je pozadu za plánem.
-   Je-li EAC menší než plánované úsilí, předpokládá se, že úkol zabere méně času, než bylo původně plánováno a je před plánem v předstihu.

**Nová předpověď úsilí projektového manažera** Občas bude muset projektový manažer nebo jiná osoba, která sleduje postup projektu, revidovat původní odhady úkolu. Úloha může z různých důvodů probíhat rychleji nebo pomaleji, než se původně očekávalo. Například byl omezen rozsah nebo mají pracovníci méně zkušeností, než se původně plánovalo. Předpovědi jsou vnímání odhadů projektového manažera podle aktuálního stavu projektu. Nedoporučujeme měnit směrná čísla, protože směrný plán projektu představuje dobře publikovaný dokument pro odhady plánů a nákladů projektu, na nichž se shodli všichni účastníci projektu. 

Projektoví manažeři mohou upravit úsilí na úkoly dvěma způsoby:

-   Upravit zbývající úsilí, které je automaticky nastaveno pro aktualizaci skutečného zbývajícího úsilí v úkolu.
-   Upravit procento pokroku, které je automaticky nastaveno pro aktualizaci skutečného pokroku v úkolu.

Oba přístupy způsobují přepočet hodnot ETC, EAC a procenta pokroku a očekávaných odchylek úsilí daného úkolu. Rovněž se přepočítají hodnoty EAC, ETC a procento pokroku souhrnných úkolů a jejich předpokládané odchylky úsilí jsou aktualizovány. 

**Upravené úsilí souhrnných úkolů** Můžete upravit úsilí u souhrnných nebo kontejnerových úkolů. Bez ohledu na to, zda upravíte tyto hodnoty pomocí zbývajícího úsilí nebo procenta pokroku souhrnných úkolů, spustí se automaticky následující sada výpočtů v tomto pořadí:

1.  Vypočítá se hodnota EAC, ETC a procento pokroku úkolu.
2.  Nová hodnota EAC se na podřízené úkoly rozdělí ve stejném poměru jako původní množství EAC.
3.  Vypočítá se nová EAC pro každou úlohu uzlu listu.
4.  Zbývající úsilí a procento pokroku se přepočítají pro všechny ovlivněné podřízené úkoly na základě nové hodnoty EAC. Přepočítá se také rozptyl úsilí úkolů.
5.  EAC souhrnných úkolů se také přepočítá z uzlů listu.

Klikněte na **Rozbalte na úroveň** v zobrazení Sledování úsilí k nastavení úrovně, na které bude váš strukturovaný rozpis prací sledován a udržován. Strukturovaný rozpis prací se automaticky rozbalí na tuto úroveň v zobrazení Sledování úsilí, kdykoli jej otevřete.

### <a name="cost-tracking-view"></a>Zobrazení Sledování nákladů

Zobrazení Sledování nákladů zobrazuje sledování spotřeby nákladů na úkol. V tomto zobrazení jsou skutečné náklady, které byly dosud vynaloženy na úkol, porovnány s plánovanými náklady na úkol. Následující vzorce poskytují hodnoty v zobrazení Sledování nákladů:

-   Procento spotřebovaných nákladů = skutečné náklady vynaložené doposud ÷ plánované náklady na úkol
-   Náklady na dokončení (CTC) = plánované náklady – skutečné náklady vynaložené doposud
-   Náklady na dokončení (EAC) = CTC + skutečné náklady doposud
-   Očekávaná odchylka nákladů = plánované náklady – EAC

Zobrazení Sledování nákladů zobrazuje projekci rozptylu nákladů úkolu na základě toho, zda je EAC větší nebo menší než plánované náklady:

-   Je-li EAC větší než plánované náklady, předpokládá se, že úkol zabere více nákladů, než bylo původně plánováno a je nad rozpočtem.
-   Je-li EAC menší než plánované náklady, předpokládá se, že úkol zabere méně nákladů, než bylo původně plánováno a je pod rozpočtem.

**Nová předpověď nákladů projektového manažera** Projektoví manažeři musí použít CTC k revizi původního odhadu nákladů na úkol. Projektový manažer může upravit hodnotu CTC na náklady, které jsou nutné k dokončení úkolu. Pokud upravíte hodnotu CTC, přepočítají se CTC, EAC a procento spotřebovaných nákladů úkolu a promítnutá odchylka nákladů úkolu. Rovněž se přepočítají hodnoty EAC, ETC a vynaložené náklady souhrnných úkolů a jejich předpokládané odchylky nákladů jsou aktualizovány. 

> [!NOTE] 
> Když opravíte úsilí pro úkol WBS v pohledu Sledování úsilí, CTC, EAC úkolu, procento spotřebovaných nákladů a promítnutá odchylka nákladů se přepočítají v zobrazení Sledování nákladů. Oprava nákladů však neovlivní hodnoty v zobrazení Sledování úsilí, protože náklady podle typu transakce (práce, materiály nebo výdaje) nebo kategorie projektu nejsou revidovány. 

**Revize projekce nákladů na souhrnné úkoly** Můžete opravit náklady na souhrnné úkoly a výpočty se provádějí automaticky v následujícím pořadí:

1.  EAC, CTC a procento nákladů spotřebovaných na úkol se přepočítají.
2.  Nová hodnota EAC se na podřízené úkoly rozdělí ve stejném poměru jako v původních EAC úkolů.
3.  Vypočítá se nový EAC pro každý úkol.
4.  CTS a procento spotřebovaných nákladů jsou přepočítány pro ovlivněné podřízené úkoly na základě hodnoty EAC. Přepočítá se také rozptyl nákladů úkolů.
5.  Na základě této změny se EAC pro všechny souhrnné úkoly přepočítá.

Klikněte na **Rozbalte na úroveň** v zobrazení Sledování nákladů k nastavení úrovně, na které bude váš strukturovaný rozpis prací sledován a udržován. Strukturovaný rozpis prací se rozbalí na tuto úroveň v zobrazení Sledování nákladů, kdykoli jej otevřete.

### <a name="earned-value-management"></a>Správa vydělané hodnoty

Ke sledování postupu projektu můžete použít metodu vydělané hodnoty (EVM). Metriky vydělané hodnoty si můžete prohlédnout v Centru rolí projektového manažera. Komponenta grafu vydělané hodnoty zobrazuje časově rozložené hodnoty plánované hodnoty a skutečných nákladů. Získaná hodnota k aktuálnímu datu se zobrazuje jako bod. Časově odstupňovaná data pro získanou hodnotu nejsou aktuálně k dispozici. 

Časová fáze v grafu vydělané hodnoty se zobrazuje podle týdne nebo měsíce. Tato část popisuje tři pilíře EVM: plánovanou hodnotu, získanou hodnotu a skutečné náklady. 

**Plánovaná hodnota** Teorie EVM uvádí, že plánovaná hodnota představuje rychlost, jakou tým projektu plánoval vydělat na projektu hodnotu. 

Finance používá pravidlo výdělku 0:100, když vykresluje plánovanou hodnotu. Podle tohoto pravidla se hodnota úkolu zaúčtuje k úkolu k datu jeho ukončení. Žádná hodnota se nezveřejní, dokud úkol není 100% dokončen. 

V části Správa projektů a účetnictví zadáte datum ukončení uzlů listu a plánované náklady na něj. Když je graf plánované hodnoty zobrazen podle týdne, je plánovaná hodnota shrnuta podle týdne pro všechny úkoly v listovém uzlu po dobu trvání projektu. 

**Vydělaná hodnota** Teorie EVM uvádí, že vydělaná hodnota představuje rychlost, jakou tým projektu ve skutečnosti vydlává na projektu hodnotu. 

Finance používá pravidlo výdělku 0:100, když vykresluje vydělanou hodnotu. Podle tohoto pravidla se hodnota úkolu zaúčtuje k úkolu k datu jeho ukončení. Žádná hodnota se nezveřejní, dokud úkol není 100% dokončen. 

Když se vypočítá vydělaná hodnota, zohlední se procento pokroku každého úkolu. Podle pravidla výdělku 0:100 se pro výpočet získané hodnoty ke konci daného období berou v úvahu pouze úkoly, které jsou dokončeny v daném období. Získaná hodnota v projektu se vypočítá pro všechny úkoly, které byly dokončeny při vytváření grafu. 

> [!NOTE] 
> V současné době systém pro sledování strukturovaného rozpisu prací nemá datové struktury, které by ukládaly historická procenta pokroku u každého úkolu. Získanou hodnotu lze tedy vykazovat pouze od doby zpracování krychle. Pravidelně zpracovávejte krychli, abyste aktualizovali data o vydělané hodnotě, která se zobrazují v Centru rolí. 

**Aktuální cena** Teorie EVM uvádí, že graf skutečných nákladů představuje míru, s jakou jsou peníze utráceny. 

Transakce, které jsou zaúčtovány do projektu, se používají k vykreslení řádku skutečných nákladů. Náklady jsou shrnuty podle data. Tato data se poté použijí k vytvoření grafu skutečných nákladů podle týdne nebo měsíce v grafu vydělané hodnoty.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Jak používat koncepty plánované hodnoty, vydělané hodnoty a skutečných nákladů

**Odchylka v plánu** Během plánování vytvoříte prognózu pro práci na časové ose. Plánovaná hodnota je tedy míra, s jakou plánovači projektu považovali práci na projektu za dokončenou. Po dokončení projektu je práce dokončena a projekt získává hodnotu. Porovnáním plánované hodnoty se získanou hodnotou můžete zobrazit, jak práce na projektu pokračuje. Výsledek tohoto srovnání se nazývá rozptyl plánu. 

Pokud je plánovaná hodnota za období větší než vydělaná hodnota, je množství práce, které bylo na projektu provedeno, menší než to, co bylo plánováno. Proto je projekt pozadu. Protože plánovaná hodnota a vydělaná hodnota jsou vyjádřeny v peněžním vyjádření, je časovému zpoždění na projektu dána také peněžní hodnota. 

Pokud je plánovaná hodnota za období menší než vydělaná hodnota, je množství práce, které bylo na projektu provedeno, větší než to, co bylo plánováno. Proto je projekt v předstihu. Tato doba realizace také získá peněžní hodnotu.

**Rozptyl nákladů** Protože vydělaná hodnota používá jako násobitel cenu nákladů, vydělaná hodnota označuje cenu práce, která se na projektu provádí. Jak projekt postupuje, protokol transakcí poskytuje záznam o penězích, které jsou skutečně vynaloženy na tento projekt. Porovnáním vydělané hodnoty se skutečnými náklady můžete zobrazit částku utracených peněz versus vydělanou hodnotu. Výsledek tohoto srovnání se nazývá rozptyl nákladů. 

Pokud jsou skutečné náklady vynaložené na určité období vyšší než vydělaná hodnota, bylo utraceno více peněz než vyděláno. Proto je projekt nad rozpočtem. 

Pokud jsou skutečné náklady vynaložené na určité období menší než vydělaná hodnota, bylo vyděláno více peněz než utraceno. Proto je projekt pod rozpočtem.

## <a name="wbs-templates"></a>Šablony pro strukturovaný rozpis prací
Funkci šablon strukturovaného rozpisu prací můžete použít k vytvoření standardních šablon pro projekty. Pokud projekty, které vaše společnost nabízí, zahrnují hodně opakovatelné práce, měli byste zvážit vytvoření šablony strukturovaného rozpisu prací. 

Šablonu strukturovaného rozpisu prací můžete vytvořit ze strukturovaného rozpisu prací existujícího projektu, aby znalosti a osvědčené postupy, které jste získali během plánování daného projektu, mohli být v budoucnu na podobných projektech znovu použity. Někdy však nemusí mít smysl uložit celý strukturovaný rozpis prací jako šablonu. Proto můžete také vytvořit šablony z částí strukturovaného rozpisu prací pro projekt.

### <a name="saving-a-projects-wbs-as-a-template"></a>Uložení strukturovaného rozpisu prací projektu jako šablony

Jakmile vytvoříte šablonu, můžete ji importovat do strukturovaného rozpisu prací nového projektu pod kořenovým uzlem nebo pod jakoukoli úlohu v strukturovaném rozpisu prací projektu.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Import šablony strukturovaného rozpisu prací do strukturovaného rozpisu prací projektu

Při importu úkolů jsou úkoly v šabloně uspořádány podle data zahájení úkolu, pod kterým jsou importovány. Během importu se vztahy předchůdců u úkolů šablony používají k výpočtu počátečních dat pro importované úkoly. Standardní pracovní kalendář cílového projektu se použije k výpočtu konečných dat importovaných úkolů, takže zůstanou zachovány pracovní dny a standardní pracovní doba, které jsou definovány v pracovním kalendáři aktuálního projektu. 

Výdajové náklady a prodejní ceny na řádcích odhadu se používají k zajištění toho, že ceny specifické pro projekt nebo projektovou smlouvu mají platná data.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Rozdíly mezi strukturovaným rozpisem nákladů projektu a šablonou strukturovaného rozpisu úkolů

-   Úkoly v šablonách strukturovaného rozpisu prací nemají počáteční a koncová data.

Pracovní a nepracovní dny nejsou pro šablony strukturovaného rozpisu prací nastaveny.

-   Šablony strukturovaného rozpisu prací vždy používají plánovací kalendář, který je nastaven jako výchozí kalendář pro všechny projekty.

Výchozí plánovací kalendář se používá pouze ke zjištění hodin ve standardní pracovní den.

-   Vztahy předchůdců se nekopírují do šablony strukturovaného rozpisu prací.

Protože šablony strukturovaného rozpisu prací neobsahují data, logika počátečního data, která je založena na datu ukončení předchůdce, se nevyžaduje.

-   Řádek odhadu nákladů práce se automaticky vytvoří při vytvoření úkolu v šabloně strukturovaného rozpisu prací. Prodejní cena a částka nákladů jsou zkopírovány z vybraného pracovníka.

Náklady a náklady na položky lze vytvořit ručně, stejně jako je to možné ve strukturovaném rozpisu prací projektu.

-   Chyby plánování se zobrazují, když existují odchylky od následujícího vzorce:

Úsilí = počet zdrojů × doba trvání × počet hodin za standardní pracovní den 

Všechny chyby plánování můžete opravit současně kliknutím na tlačítko **Opravit všechny chyby plánování**. 

Případně můžete opravit chyby plánování jednotlivě kliknutím na ikonu varování u každého úkolu.





[!INCLUDE[footer-include](../includes/footer-banner.md)]