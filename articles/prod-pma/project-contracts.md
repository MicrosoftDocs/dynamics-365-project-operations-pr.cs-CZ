---
title: Projektové smlouvy
description: Toto téma poskytuje příklady projektových smluv, které můžete vytvořit pro různé typy projektů a zdrojů financování, a příklady správy smluv a fakturace zákazníkům projektu.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b92668c38071e8b1afdee9a79fd4a25190248ada30380bfb79054a6dc587f95
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001018"
---
# <a name="project-contracts"></a>Projektové smlouvy

[!include [banner](../includes/banner.md)]

Tento článek poskytuje příklady projektových smluv, které můžete vytvořit pro různé typy projektů a zdrojů financování, a příklady správy smluv a fakturace zákazníkům projektu.

Typ projektu, který vytvoříte pro projektovou smlouvu, určuje metodu, která se používá k fakturaci zákazníků projektu. Projektovou smlouvu a související projekt můžete změnit, ale nemůžete změnit typ projektu. 

Pomocí projektové smlouvy můžete fakturovat jeden nebo více projektů současně. Projektová smlouva také pomáhá zaručit konzistentní postup fakturace pro každý dílčí projekt ve struktuře projektu. 

Každý projekt, který bude fakturován, musí být spojen s projektovou smlouvou. Nastavení pro projektovou smlouvu se vztahuje na všechny projekty a dílčí projekty, které jsou spojeny s touto projektovou smlouvou. 

Projektová smlouva může stanovit jeden nebo více zdrojů financování. Proto můžete rozdělit fakturaci mezi více poskytovatelů financování, nastavit limity financování tak, aby ze zdrojů financování byla fakturována maximálně určená částka, a konfigurovat pravidla financování pro účtování výdajů.

## <a name="funding-for-project-contracts"></a>Financování projektových smluv
Některé projektové smlouvy stanoví, že odpovědnost za financování nákladů projektu sdílí více stran. Zde je uvedeno několik příkladů:

-   Velký zákazník s několika divizemi požaduje, aby bylo financování projektu rozděleno podle divizí.
-   Vaše společnost sdílí náklady na velký projekt s externí organizací.
-   Silniční projekt je spolufinancován dvěma obcemi.
-   Projekt stavby mostu je financován z vládního grantu a soukromou společností.

V Dynamics 365 Finance můžete rozdělit fakturaci za jednu transakci nebo celý projekt mezi více zákazníků, grantů nebo organizací. 

V projektech, které mají více poskytovatelů financování, se všechny strany, které přispívají na financování projektu s rozšířeným financováním, nazývají zdroje financování. Poté, co je zákazník, organizace nebo grant definován jako zdroj financování, jej lze přiřadit k jednomu nebo více pravidlům financování. Pravidla financování obsahují kritéria, která určují, jak jsou alokovány poplatky k různým zdrojům financování projektu. 

Vzhledem k tomu, že položky na skladě – například ty, které se objevují na nákupních požadavcích a objednávkách – nelze rozdělit, částku nákladů nelze v době distribuce rozdělit mezi více zdrojů financování. Proto zůstane hodnota zdroje financování 0 (nula), dokud nebude zaúčtována emise zásob. Když se zaúčtuje emise zásob, částka nákladů se rozdělí podle pravidel distribuce účtu pro projekt.

Zde je několik kroků, které můžete podniknout, abyste usnadnili rozdělení fakturace mezi více zdrojů financování:

-   Určete, že všechny transakce zadané pro projekt používají stejnou měnu prodeje jako projektová smlouva.
-   Nastavte limity financování tak, aby zdroj financování nebyl fakturován více než stanovenou částkou na projekt.
-   Konfigurujte pravidla financování a limity financování pro každého pracovníka, položku, kategorii, skupinu kategorií a typ transakce (nebo pro všechny typy transakcí).
-   Vyberte nepovinné počáteční a koncové datum a definujte tak období platnosti každého pravidla financování.
-   Uveďte procento, za které je každý zdroj financování odpovědný.
-   Určete, který zdroj financování je zodpovědný za zaokrouhlování rozdílů, které jsou způsobeny výpočty alokace financování.
-   Nastavte pravidla, která určují, jak jsou náklady na projekt fakturovány externím zákazníkům a účtovány interním organizacím.
-   Zaznamenávejte transakce na účtu pozastaveného financování, dokud nebude možné získat další financování nebo dokud se nerozhodnete nést náklady interně.

V projektu se vyhledá přiřazení daňové skupiny, aby bylo možné určit, která daňová skupina se má k transakci přidružit. Pokud na úrovni projektu nebylo provedeno žádné přiřazení daňové skupiny, prohledá se projektová smlouva.

### <a name="example-multiple-funding-sources-simple"></a>Příklad: Více zdrojů financování (jednoduchý)

Následující tabulka poskytuje scénáře pro správu alokace financování mezi více zdroji financování. Tyto scénáře jsou založeny na následujících předpokladech:

-   Nastavení priorit se zohledňuje v alokaci finančních prostředků před uplatněním dalšího kritéria pravidla financování.
-   Nebylo zadáno žádné časové období k definování období d, kdy je pravidlo financování platné.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scénář</strong></td>
<td><strong>Zdroj financování</strong></td>
<td><strong>Procento alokace</strong></td>
<td><strong>Priorita přidělení</strong></td>
</tr>
<tr class="even">
<td>Chcete přidělit náklady jednomu zdroji financování, dokud nebudou vyčerpány jeho prostředky, přidělit náklady druhému zdroji financování, dokud nebudou vyčerpány jeho prostředky, a nakonec přidělit zbývající náklady třetímu zdroji financování.</td>
<td><ul>
<li>Zdroj　financování　1</li>
<li>Zdroj　financování　2</li>
<li>Zdroj　financování　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Chcete přidělit 75 procent nákladů jednomu zdroji financování a 25 procent druhému zdroji financování. Když je některý z těchto zdrojů financování vyčerpán, chcete uhradit zbývající náklady z třetího zdroje financování.</td>
<td><ul>
<li>Zdroj　financování　1</li>
<li>Zdroj　financování　2</li>
<li>Zdroj　financování　3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>0</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Chcete přidělit 75 procent nákladů jednomu zdroji financování a 25 procent druhému zdroji financování. Když je některý z těchto zdrojů financování vyčerpán, chcete rozdělit zbývající náklady mezi třetí a čtvrtý zdroj financování.</td>
<td><ul>
<li>Zdroj　financování　1</li>
<li>Zdroj　financování　2</li>
<li>Zdroj　financování　3</li>
<li>Zdroj　financování　4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>0</li>
<li>0</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Chcete přidělit prvních 25 procent nákladů jednomu zdroji financování a zbytek druhému zdroji financování.</td>
<td><ul>
<li>Zdroj　financování　1</li>
<li>Zdroj　financování　2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Příklad: Více zdrojů financování (složitý)

Máte tři zdroje financování, které chcete použít v následujícím pořadí:

1.  Používejte zdroj financování 2 a zdroj financování 3 rovnoměrně, dokud nebude vyčerpán zdroj financování 2.
2.  Pokračujte v používání zdroje financování 3, dokud nebude vyčerpán.
3.  Po vyčerpání zdroje financování 3 použijte zdroj financování 1.

K dosažení tohoto cíle musíte provést následující postup:

-   Nastavte limity financování pro zdroj financování 2 a zdroj financování 3 na jejich odpovídající částky.
-   Vytvořte následující pravidla financování:
    -   Pravidlo 1 (Priorita 1): Přidělte 50 procent transakcí zdroji financování 2 a 50 procent zdroji financování 3.
    -   Pravidlo 2 (Priorita 2): Přidělte 100 procent transakcí zdroji financování 3.
    -   Pravidlo 3 (Priorita 3): Přidělte 100 procent transakcí zdroji financování 1.

Toto nastavení funguje, protože transakce jsou prověřovány na základě pravidel a limitů, aby se určilo, zda se na transakci vztahuje některé pravidlo nebo limit. Pokud se na transakci nevztahují žádná konkrétní pravidla nebo limity, použije se pravidlo Všechny transakce. Pravidlo Všechny transakce odpovídá všem transakcím. 

Pokud je nalezeno pravidlo, které odpovídá transakci, použije se nejprve procento, které bylo přiděleno v tomto pravidle, ale až poté, co jsou shody porovnány s nastavenými limity. Pokud byl limit splněn a prostředky zdroje financování jsou vyčerpány, pravidlo financování spojené s limitem financování bude ignorováno a program hledá další platné pravidlo. 

V některých případech lze podle pravidla přidělit pouze část transakce. K tomu může dojít, protože při alokaci transakce je dosaženo limitu. V tomto případě je podle tohoto pravidla přidělena pouze určitá částka, například 50 procent na každý zdroj financování. To je případ pravidla 1, které je popsáno dříve v této části. Zbytek je přidělen podle dalšího pravidla v pořadí. 

Následující tabulka zkoumá tento scénář podrobněji.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Zaměření</strong></td>
<td><strong>Podrobnosti</strong></td>
</tr>
<tr class="even">
<td>Pravidla financování</td>
<td><ul>
<li>Pravidlo 1 (Priorita 1): Všechny transakce. Přidělte zdroj financování 2 s 50 % a zdroj financování 3 s 50 %.</li>
<li>Pravidlo 2 (Priorita 2): Všechny transakce. Přidělte zdroj financování 3 se 100 %.</li>
<li>Pravidlo 3 (Priorita 2): Všechny transakce. Přidělte zdroj financování 1 se 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Limity financování</td>
<td><ul>
<li>Limit zdroje financování 1 = 10 000,00</li>
<li>Limit zdroje financování 2 = 500,00</li>
<li>Limit zdroje financování 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transakce 1</td>
<td><strong>Částka transakce:</strong> 100,00<strong>Financování:</strong> Transakce se vyplácí pouze podle pravidla 1, protože transakce je plně zaplacena po uplatnění pravidla 1. Transakce je financována rovnoměrně mezi zdrojem financování 2 a zdrojem financování 3.
<ul>
<li>Zdroj financování 2: 50,00</li>
<li>Zdroj financování 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transakce 2</td>
<td><strong>Částka transakce</strong> 5 000,00<strong>Financování:</strong> Transakce se vyplácí podle všech tří pravidel. <strong>Pravidlo 1</strong>
<ul>
<li>Zdroj financování 2: 450,00</li>
<li>Zdroj financování 3: 450,00</li>
</ul>
<strong>Pravidlo 2</strong>
<ul>
<li>Zdroj financování 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Pravidlo 3</strong>
<ul>
<li>Zdroj financování 1: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Celkové prostředky, které jsou rozděleny pro každý zdroj financování</td>
<td><ul>
<li>Zdroj financování 1: 3.850,00</li>
<li>Zdroj financování 2: 500,00</li>
<li>Zdroj financování 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Pravidla fakturace
Když sjednáváte projektovou smlouvu se zákazníkem, definujete, jak a kdy můžete zákazníkovi fakturovat práci na projektu. Poté, co nastavíte projektovou smlouvu a projekt, můžete nastavit pravidla fakturace pro projekt. Pravidla fakturace jsou založena na smluvních podmínkách projektu, které jsou uvedeny ve smlouvě o projektu. Pravidla fakturace, která můžete vytvořit, závisí na smluvních podmínkách projektové smlouvy a typu projektu, jako je Čas a materiál nebo Pevná cena, který přidružíte k pravidlu fakturace. Pro projektovou smlouvu můžete vytvořit více než jedno fakturační pravidlo. Pravidlo fakturace můžete také přiřadit několika projektům, které jsou spojeny se stejnou projektovou smlouvou a mají podobné fakturační podmínky. 

Můžete nastavit následující typy pravidel fakturace:

-   **Jednotka dodávky** – Fakturujte zákazníka, když dokončíte jednotku dodávky. Jednotky dodávky definujete ve smlouvě.
-   **Pokrok** – Fakturujte zákazníka, když dokončíte stanovené procento projektu. Můžete nastavit pravidlo fakturace, které automaticky vypočítá procento dokončené práce, nebo můžete ručně vypočítat procento dokončené práce a částku fakturovanou zákazníkovi.
-   **Milník** – Fakturujte zákazníkovi celou částku milníku projektu, když je milníku dosaženo.
-   **Poplatek** – Fakturujte zákazníkovi své služby plus poplatek za správu, což je obvykle procento z ceny služeb.
-   **Čas a materiál** – Fakturujte zákazníkovi hodnotu času a materiálů použitých na projektu.

U všech typů pravidel fakturace můžete určit retenční procento, které se odečte od faktur zákazníka, dokud projekt nedosáhne dohodnuté fáze. Procento zadržení platby je uvedeno v projektové smlouvě. Částka se vypočítá na základě celkové hodnoty řádků ve faktuře zákazníka, od které bude odečtena. 

U pravidel fakturace **Čas a materiál** a **Pokrok** můžete přiřadit zpoplatněné kategorie. Zpoplatněné kategorie označují transakce, které by měly být zahrnuty do faktur zákazníka. 

Když jste připraveni fakturovat zákazníkovi, vypočítá se fakturovaná částka za projekt na základě pravidel fakturace a vygeneruje se návrh faktury projektu. 

V následujících částech jsou uvedeny příklady, které ukazují, jak nastavit a spravovat pravidla fakturace pro projekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Příklad: Vytvořte fakturační pravidlo, které je založeno na počtu dodaných jednotek.

Vaše organizace uzavře dohodu o realizaci celkem pěti školení pro zaměstnance zákazníka s cenou 10 000 za jedno školení. Zákazníkovi zašlete fakturu po každém školení. 

Když nastavíte pravidla fakturace pro smlouvu, použijete následující hodnoty:

-   Jednotkou dodávky je jedno školení.
-   Jednotková cena je 10 000 za školení.
-   Celkový počet jednotek je pět školení.

Po absolvování jednoho školení můžete vytvořit fakturu s částkou 10 000 za první dodanou jednotku a odeslat fakturu zákazníkovi.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Příklad: Vytvořte fakturační pravidlo založené na zadaném procentu dokončení projektu (ruční výpočet)

Vaše organizace – softwarová poradenská firma – uzavírá se zákazníkem dohodu o vývoji části produktu, který zákazník vyvíjí. Vaše organizace souhlasí s dodáním softwarového kódu během šesti měsíců. Zákazník se zavazuje zaplatit vaší organizaci za práci celkem 100 000. Vytvoříte fakturační pravidlo pro fakturaci zákazníkovi na základě procenta práce dokončené na projektu, jak je uvedeno ve smlouvě.

-   Na konci prvního měsíce dojde ke schůzce se zákazníkem, abyste určili procento dokončené práce. Poté, co vy a zákazník zkontrolujete projekt, se rozhodnete, že je projekt dokončen na 15 procent.
-   Vytvoříte fakturu s částkou 15 000 (15 procent ze 100 000) a odešlete ji zákazníkovi.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Příklad: Vytvořte fakturační pravidlo založené na zadaném procentu dokončení projektu (automatický výpočet)

Vaše organizace – zabývající se vývojem softwaru – souhlasí s vytvořením balíčku mzdového účetnictví pro zákazníka za 30 000. Zákazník se zavazuje zaplatit vaší organizaci na základě procenta dokončené práce. Odhadujete, že náklady na projekt budou 20 000. Projektová smlouva určuje kategorie prací, které používáte v procesu fakturace. Nastavíte pravidla fakturace, která automaticky vypočítají částky faktury pro procento práce dokončené v každé kategorii. Nastavíte rozpočet pro každou kategorii:

-   **Vývoj** - Náklady 15 000 a výnosy 20 000
-   **Instalace** - Náklady 5 000 a výnosy 10 000

Když vytvoříte fakturu zákazníka poprvé, částka faktury se automaticky vypočítá na základě následujících informací:

-   Po měsíci pracovník projektu odešle časový rozvrh prací na projektu. Náklady na odpracované hodiny jsou 5 000 za vývoj a 1 000 za instalaci. Vývojové práce jsou dokončeny z 33 procent (5 000 skutečných nákladů / 15 000 rozpočtových nákladů) a instalační práce jsou dokončeny z 20 procent (1 000 skutečných nákladů / 5 000 rozpočtových nákladů).
-   Automaticky se vypočítá fakturovaná částka 8 667 (33 procent z 20 000 + 20 procent z 10 000).
-   Vytvoříte fakturu s částkou 8 667 a odešlete ji zákazníkovi.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Příklad: Vytvořte fakturační pravidlo založené na dohodnutých milnících

Vaše organizace – poradenská společnost pro management – souhlasí s provedením průzkumu trhu pro spotřební výrobek, který zákazník hodlá prodávat. Zákazník souhlasí s používáním vašich služeb po dobu tří měsíců, počínaje březnem, a zavazuje se zaplatit vaší organizaci 50 000. Projekt má tři milníky:

-   Milník 1: Shromažďování údajů o spotřebitelích - 31. března
-   Milník 2: Analýza spotřebitelských dat - 30. dubna
-   Milník 3: Představení návrhu životaschopnosti produktu - 31. května

Zákazník souhlasí, že vaší organizaci zaplatí 10 000 za první milník, 20 000 za druhý milník a 20 000 za třetí milník. 

Když nastavujete projektovou smlouvu, souhlasíte s fakturací zákazníkovi na základě milníku, který byl dokončen. Nastavení pravidla fakturace zahrnuje následující kroky:

-   Definujte milníky projektu.
-   Definujte částku, která bude zákazníkovi fakturována po dokončení každého milníku.

Když je první milník dokončen 31. března, označíte milník jako dokončený a poté vytvoříte fakturu s částkou 10 000 a odešlete ji zákazníkovi. Fakturu za milník nemůžete vytvořit, dokud milník neoznačíte jako dokončený.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Příklad: Vytvořte fakturační pravidlo založené na službách plus poplatek za správu

Vaše organizace – poradenská firma pro management – souhlasí s provedením průzkumu trhu, jehož cílem je vyhodnocení životaschopnosti produktu, který vyvíjí maloobchodní společnost zákazníka. Podmínky smlouvy upřesňují, že budete poskytovat služby vašim třem nejlepším konzultantům v oblasti managementu, kteří budou provádět výzkum na základě časových a materiálových podkladů. Zákazník souhlasí s tím, že zaplatí 100 za hodinu plus 10% poplatek za správu za konzultační hodiny účtované projektu. 

Když připravujete projektovou smlouvu, vytvořte fakturační pravidlo a přidejte 10% poplatek za správu ke konzultačním hodinám účtovaným projektu. 

Když vytvoříte fakturu pro zákazníka, bude zákazníkovi účtován poplatek za správu ve výši 10 procent plus náklady na konzultační hodiny. Například pokud tři konzultanti na projektu pracovali celkem 200 hodin, vytvoří se faktura za 22 000 na základě následujícího výpočtu:

-   200 hodin s cenou 100 za hodinu = 20 000
-   10% poplatek za správu = 2 000
-   Celková částka faktury = 22 000

Pokud jsou poplatky zdanitelné zákazníkovi a v projektové smlouvě vyberete skupinu daně z obratu, zadá se skupina daně z obratu automaticky do pravidla fakturace poplatků.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Příklad: Vytvořte fakturační pravidlo pro cenu času a materiálů

Vaše organizace – softwarová poradenská společnost – souhlasí s poskytnutím pěti technických konzultantů pro práci na projektu vývoje softwaru pro zákazníka na příštích šest měsíců. Zákazník souhlasí se zaplacením 150 za každou konzultační hodinu plus náklady na kancelářské potřeby. Vaše organizace pošle zákazníkovi fakturu na konci každého měsíce. 

Při uzavírání projektové smlouvy souhlasíte, že budete zákazníkovi každý měsíc fakturovat čas a materiály týkající se projektu. Vytvoříte fakturační pravidlo, které obsahuje následující informace:

-   Smluvní období je šest měsíců.
-   Konzultační čas se vypočítá sazbou 150 za hodinu.
-   Kancelářské potřeby jsou fakturovány v jejich ceně a celkové náklady na projekt nesmí překročit 10 000.
-   Zákaznickou fakturu vytvoříte na konci každého kalendářního měsíce během projektu.

Během prvního měsíce konzultanti projektu odpracovali celkem 800 hodin. Náklady na kancelářské potřeby účtované projektu jsou 2 000. Na konci měsíce tedy vytvoříte fakturu s částkou 122 000, která se počítá jako 800 hodin krát 150 za hodinu, plus 2 000 za kancelářské potřeby.





[!INCLUDE[footer-include](../includes/footer-banner.md)]