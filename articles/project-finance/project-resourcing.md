---
title: Zajišťování zdrojů pro projekt
description: Toto téma obsahuje informace o zajišťování zdrojů pro projekt.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750271"
---
# <a name="project-resourcing"></a>Zajišťování zdrojů pro projekt

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o zajišťování zdrojů pro projekt.

Náročným úkolem ve fázi plánování projektu pro projektové manažery a manažery zdrojů je alokace zdrojů, kdy musí určit a rezervovat správný zdroj pro práci na projektu. V Dynamics 365 Finance vám funkce zajišťování zdrojů pro projekty umožňuje definovat role, které jsou považovány za dočasné zdroje a které mohou být rezervovány pro konkrétní zakázku nebo část zakázky. Tento typ financování umožní projektovým manažerům a manažerům zdrojů dokončit následující úkoly:

- Definovat roli, která má požadované kompetence, aby bylo snadné dát dohromady potřebné zdroje.
- Pomocí rolí můžete definovat počáteční plán zakázky, který je založen na rezervovaných zdrojích.
- Odhadněte náklady a určete počáteční rozpočet na základě přiřazených rolí a zdrojů pro projekt.
- Pomocí rolí můžete odhadnout počet rezervací zdrojů, které jsou vyžadovány pro každou zakázku.
- Odhadněte počet zdrojů, které jsou potřebné pro celý životní cyklus projektu.
- Navrhněte strukturovaný rozpis prací (WBS) s využitím počátečních přiřazení zdrojů.

[![Životní cyklus projektu](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

V průběhu plánování projektu lze plánované zdroje nahradit personálními zdroji. Vedoucí projektu se může také vrátit zpět a aktualizovat rezervace zdrojů během kterékoli fáze projektu.

## <a name="set-up-project-resources"></a>Nastavení projektových zdrojů
Musíte nastavit kalendář a přidružit jej k zaměstnanci nebo pracovníkovi. Kalendář se používá k naplánování projektu a pracovní doby zdrojů, které jsou pro projekt rezervovány. Během přípravy kalendáře mohou projektoví manažeři provádět vyrovnávání zdrojů jako součást jejich optimalizace. Na základě harmonogramu kalendáře lze zdroje omezit. Kalendář můžete nastavit na straně **Kalendáře**.

Když nastavujete pracovníka jako zdroj projektu, můžete vybírat z pracovníků, kteří pracují ve společnosti, pro kterou nastavujete prostředky. Případně můžete vybrat pracovníky z jiných společností ve vaší organizaci. Tito pracovníci jsou označování jako mezipodnikové zdroje.

Následující postupy vysvětlují, jak nastavit pracovníka jako projektový zdroj ve vaší společnosti a jak nastavit mezipodnikový projektový zdroj.

### <a name="set-up-a-worker-as-a-project-resource"></a>Nastavení pracovníka jako projektový zdroj

1. Na stránce **Pracovníci** vyberte v seznamu **Pracovníci** toho pracovníka, kterého přidáváte jako projektový zdroj, a otevřete záznam pracovníka.
2. V podokně akcí vyberte **Projekt** &gt; **Nastavení** &gt; **Nastavení projektu**.
3. Vyberte kalendář a poté stránku zavřete.

Můžete také určit výchozí projekty pro zdroj jako typ předběžného přiřazení. Předběžné přiřazení lze použít, pokud manažer prostředků nebo projektový manažer předem ví, na kterých projektech bude prostředek pracovat. Předběžná přiřazení mohou být také založena na požadavku sponzora projektu nebo zákazníka. Chcete-li předem přiřadit projekt, vyberte příslušný projekt na stránce **Přiřadit projekty** na kartě **Projekty** v seznamu **Zbývající projekty**.

### <a name="set-up-an-intercompany-resource"></a>Nastavení mezipodnikového zdroje

Když nastavíte pracovníka jako mezipodnikový zdroj, musíte dokončit nastavení jak ve společnosti poskytující půjčku, tak ve společnosti, která si zdroj půjčuje.

**Ve společnosti poskytující půjčku**

1. V aplikace Finance ověřte, zda je vybrána společnost poskytující půjčku, a poté dokončete postup v předchozí části „Nastavení pracovníka jako projektový zdroj“.
2. Na stránce **Mezipodnikové účetnictví** vyberte možnost **Nový**.
3. V poli **ID právnické osoby** vyberte společnost poskytující půjčku. Vyplňte zbývající pole podle potřeby a poté vyberte příkaz **Uložit**.
4. Na stránce **Cena za převod** vyberte možnost **Nová**.
5. V poli **Půjčující si subjekt** vyberte příslušnou společnost.
6. Chcete-li půjčující si společnosti zapůjčit pouze zdroj, který jste vytvořili na začátku této části, vyberte v poli **Zdroj** název zdroje, který jste vytvořili. Chcete-li půjčující si společnosti zpřístupnit všechny zdroje společnosti poskytující půjčku, ponechte pole **Zdroj** prázdné.
7. Na stránce **Parametry správy projektu a účetnictví** nastavte na kartě **Mezipodnikové** možnost **Povolit mezipodnikové plánování zdrojů a časové rozvrhy** na **Ano**.

**V půjčující si společnosti**

- Na stránce **Seznam zdrojů** ve filtru vyhledávání zadejte název zdroje, který jste vytvořili pro společnost poskytující půjčku, abyste ověřili, zda je název zahrnut do seznamu prostředků pro půjčující si společnost.

## <a name="manage-resource-competencies"></a>Správa kompetencí zdrojů
Kompetence zdrojů jsou podstatnou součástí správy zdrojů. Kompetence lze použít jako základ pro určení zdrojů, které mají správnou rovnováhu dovedností, vzdělání, certifikace a projektových zkušeností. Tyto informace byste měli nastavit pro každý zdroj a pravidelně je aktualizovat. Tímto způsobem můžete maximalizovat schopnosti, když se během přiřazování projektových zdrojů shodují konkrétní kompetence zdrojů.

[![Příklady dovedností, certifikací, vzdělání a projektových zkušeností](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Následující postupy vysvětlují, jak nastavit některé kompetence pro zdroj.

K nastavení kompetencí pro pracovníka můžete použít buď stránku seznamu **Pracovníci** v oblasti Lidské zdroje nebo stránku seznamu **Zdroje** v části Správa projektů a účetnictví. U následujících postupů se používá stránka se seznamem **Pracovníci** v oblasti Lidské zdroje.

### <a name="set-up-competencies-certificates"></a>Nastavení kompetencí: Certifikáty

1. Na stránce se seznamem **Pracovníci** vyberte řádek pracovníka, pro kterého přidáte informace certifikátu.
2. V podokně akcí na kartě **Pracovník** vyberte ve skupině **Kompetence** hodnotu **Certifikáty**.
3. Vyberte **Nový** a poté v poli **Typ certifikátu** vyberte hodnotu **PMP**.
4. V poli **Počáteční datum** vyberte **1. 10. 2015** a vyberte příkaz **Uložit**.

### <a name="set-up-competencies-skills"></a>Nastavení kompetencí: Dovednosti

1. Na stránce se seznamem **Pracovníci** zkontrolujte, zda je stále vybrán pracovník, kterého jste použili v předchozím postupu. Poté v podokně akcí na kartě **Pracovník** vyberte ve skupině **Kompetence** hodnotu **Dovednosti**.
2. Vyberte **Nové**.
3. V poli **Dovednost** vyberte **Správa projektů**.
4. V poli **Úroveň** vyberte **5 Expert**.
5. V poli **Datum úrovně** vyberte **14. 1. 2014**.
6. V poli **Roky zkušeností** zadejte **10**.
7. Vyberte tlačítko **Uložit** a potom zavřete stránku.

## <a name="create-a-new-project"></a>Vytvoření nového projektu
1. Na stránce **Správa projektu** vyberte **Nový projekt** a zadejte následující hodnoty:

    - **Typ projektu:** Čas a materiál
    - **Název projektu:** Fáze 2 upgradu XYZ
    - **Projektová skupina:** TM\_WIP
    - **ID projektové smlouvy:** 00000002

2. Vyberte příkaz **Vytvořit projekt**.

### <a name="assign-a-resource-to-a-project"></a>Přiřazení zdroje k projektu

1. Na stránce **Pracovníci** vyberte v seznamu **Pracovníci** záznam pro toho pracovníka, kterému jste předtím přiřadili kompetence, a otevřete záznam pracovníka.
2. V podokně akcí na kartě **Projekt** vyberte ve skupině **Nastavení** příkaz **Přiřadit projekty**.
3. Na stránce **Přiřazení projektů ověření prostředku** na kartě **Projekty** v poli **Přidat projekt k vybraným projektům** filtrujte podle projektu **Fáze 2 upgradu XYZ**.
4. V podokně **Zbývající projekty** vyberte projekt a poté jej kliknutím na tlačítko se šipkou přidejte do podokna **Vybrané projekty**.

Můžete také podle potřeby přiřadit kategorie ke zdroji. Typ kategorie je buď **Náklady** nebo **Výnosy**. Typ kategorie určuje vaše organizace. Pokud zdroji nejsou přiřazeny žádné kategorie, vyhledá Finance výchozí kategorii na základě hodinových cen nákladů a výnosů.

### <a name="set-up-project-resource-and-role-characteristics"></a>Nastavení charakteristik projektového zdroje a role

Manažer projektu může použít funkci projektového zajišťování zdrojů k vytvoření rolí, které jsou pro projekt vyžadovány. Role lze použít, pokud jsou potvrzené zdroje stále neznámé, když probíhá rezervace zdrojů. Role lze dočasně rezervovat jako plánované zdroje, abyste mohli pokračovat ve fázích plánování projektu.

[![Příklad role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scénář:** Společnost Contoso byla najata, aby dokončila projekt Čas a materiál, který má schválenou chartu projektu. Nižší projektový manažer stále dokončuje rozsah projektu. Správce prostředků aktuálně identifikuje konkrétní zdroje, které budou vyhrazeny pro práci na novém projektu. Vzhledem ke kritické povaze projektu si sponzor projektu požádal o přidělení role vyššího projektového manažera. Správce zdrojů musí získat nový zdroj a definovat roli v systému v případě, že nižší projektový manažer vyžaduje během plánování projektu informace o zdroji.

Následující kroky ukazují, jak může správce zdrojů nastavit roli vyššího projektového manažera a asociovat s ním charakteristiky zdrojů. Později lze roli použít k vyhledání dostupných zdrojů, které odpovídají požadovaným kompetencím zdrojů.

1. Na stránce **Nastavení rolí** vyberte **Nová** a zadejte následující hodnoty:

    - **ID role:** Vyšší projektový manažer
    - **ID role:** Vyšší projektový manažer

2. Vyberte **Vytvořit**.
3. Vyberte roli **Vyšší projektový manažer** a poté vyberte **Konfigurovat charakteristiky**.
4. V poli **Typ charakteristiky** vyberte **Dovednost**.
5. V poli **Dostupné charakteristiky** zadejte hledanou dovednost.
6. V poli **Typ charakteristiky** vyberte **Certifikát**.
7. V poli **Dostupné charakteristiky** zadejte hledaný typ certifikátu.

### <a name="assign-a-project-resource-to-a-project"></a>Přiřazení projektového zdroje k projektu

1. Na stránce **Všechny projekty** vyberte projekt **Fáze 2 upgradu XYZ**.
2. Na kartě **Projektový tým a plánování** vyberte možnost **Přidat**.
3. V poli **Role** vyberte **Člen týmu**.
4. Vyberte **Rezervovat z kalendáře**.
5. Na stránce **Dostupnost zdrojů** vyberte možnost **Nastavení zobrazení**.
6. Na stránce **Upravit nastavení zobrazení** zadejte následující hodnoty:

    - **Formát pro zobrazení rozsahu dat:** Den
    - **Zobrazit popisy dostupnosti:** Ano
    - **Zobrazit zbývající kapacitu:** Ano

7. V seznamu zdrojů vyberte zdroj.
8. Vyberte **Závazná rezervace** a **Plná kapacita**.


### <a name="assign-a-resource-to-a-default-role"></a>Přiřazení zdroje k výchozí roli

Chcete-li pomoci správcům projektů nebo zdrojů s procházením hierarchie zdrojů, které lze pro projekt rezervovat. Můžete přiřadit výchozí roli k existujícímu zdroji nebo nově získanému zdroji. Například když byl Daniel najat, měl zkušenosti a dovednosti, aby mohl plnit roli obchodního analytika. Správce zdrojů přidělil tuto Danielovi jako výchozí. Proto správce zdrojů přidal Daniela do fondu obchodních analytiků, kteří jsou k dispozici pro práci na projektech.

Během rezervace zdrojů mohou projektoví manažeři filtrovat zdroje rolí, které jsou k dispozici pro práci na projektech. Tuto informaci mohou použít jako jedno z kritérií při provádění multikriteriální rozhodovací analýzy během plnění zdrojů. Mohou také přidat do filtru další charakteristiky zdrojů, aby vyhledali zdroje, které mají specifické dovednosti, vzdělání a zkušenosti pro daný projekt.

**Scénář:** Byl zahájen schválený projekt a role vyššího projektového manažera byla rezervována jako plánovaný zdroj během fáze plánování projektu. Správce prostředků nyní získal zdroj ke splnění role vyššího projektového manažera.

1. Na stránce **Seznam zdrojů** vyberte položku **Daniel Goldschmidt**.
2. Na stránce **Role zdroje** vyberte **Nová** a zadejte následující hodnoty:

    - **Platí od:** Zadejte aktuální datum.
    - **Vypršení platnosti:** Zadejte **Nikdy**.
    - **Role:** Zadejte **Vyšší projektový manažer**.

3. Vyberte tlačítko **Uložit** a potom zavřete stránku.
4. Na kartě **Kompetence** přidejte dovednost **Správa projektu** a certifikát **PMP**.

## <a name="set-up-role-based-pricing"></a>Nastavení určování cen založeného na rolích
Pro role lze nastavit všechny nákladové, prodejní a vnitropodnikové ceny.

1. Na stránce **Prodejní cena (hodina)** vyberte možnost **Nová** a zadejte datum začátku platnosti.
2. Ve sloupci **Role** vyberte roli.
3. Ve sloupci **Ceny** zadejte cenu pro vybranou roli zdroje.

## <a name="form-a-project-team"></a>Sestavení projektového týmu
Chce-li použít role, které byly předtím nastaveny v projektu, musí projektový manažer přidružit role k projektu. Projektu lze přiřadit více rolí. Aby nedocházelo k nejasnostem, jsou tyto role během rezervace automaticky označeny. Například pokud projektový manažer vyžaduje tři softwarové inženýry, jsou automaticky generovány tři role softwarového inženýra, které jsou označeny štítky **softwarový inženýr 1**, **softwarový inženýr 2** a **softwarový inženýr 3**. Pokud již byly charakteristiky rolí nastaveny pro roli, použijí se jako filtr během hledání zdrojů. Podle potřeby lze přidat další charakteristiky k dalšímu upřesnění vyhledávání.

Nastavení zobrazení lze také přizpůsobit tak, aby poskytovalo lepší přehled o dostupnosti zdrojů. K dispozici jsou možnosti zobrazení hodinové, denní, týdenní, měsíční, čtvrtletní a roční dostupnosti. K dispozici je také možnost zobrazit dostupnou a zbývající kapacitu zdrojů. Tato možnost je užitečná pro správu času, když odhadujete dostupný čas pro aktivity nebo dostupnost zdrojů.

Projektový manažer může vybrat roli na stránce a poté, pokud existuje dostupný zdroj vyhovující požadavku, vybere rezervaci prostředku, aby naplnil roli. Všimněte si, že zdroje nemusí být rezervovány v tomto okamžiku ve fázi plánování. Když vytvoříte strukturovaný rozpis prací, můžete role nahradit personálními zdroji pro projekt. Pokud jsou role nahrazeny personálními zdroji ve strukturovaném rozpisu prací, nastavení prostředků automaticky aktualizuje seznam a plánování projektového týmu.

[![Seznam projektového týmu, který zahrnuje role i skutečné zdroje](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektový manažer má různé možnosti rezervace zdroje pro projekt, například **Zbývající kapacita**, **Plná kapacita**, **Procento kapacity** a **Zadat hodiny**. Tyto možnosti rezervace lze kdykoli zrušit, pokud se změní přiřazení zdrojů. Podporovány jsou dva typy rezervací:

- **Závazná rezervace** – Rezervace zdroje byla schválena a potvrzena pro práci na zakázce po stanovenou dobu.
- **Předběžná rezervace** – Rezervace zdrojů byly pro práci na zakázce po stanovenou dobu nastaveny předběžně.

Následující procedura vysvětluje, jak vytvořit projektový tým:

### <a name="create-a-project-team"></a>Vytvoření projektového týmu

1. Na stránce se seznamem **Všechny projekty** vyberte projekt a poté vyberte možnost **Upravit**.
2. Na kartě **Projektový tým a plánování** zadejte v poli **Naplánovat koncové datum** datum zahájení plánu plus jeden měsíc. Pokud je například datum zahájení plánu 24. června 2017 (24. 6. 2017), zadejte **24. 7. 2017**.
3. Vyberte **Přidat**.
4. V podokně **Přidat role do projektu** vyberte v poli **Role** hodnotu **Vyšší projektový manažer**.
5. Vyberte **Požadované kompetence**.
6. Na stránce **Vyberte charakteristiky** jsou ve výchozím nastavení vybrány charakteristiky, které jste předtím nastavili pro roli Vyšší projektový manažer. Vyberte **OK**.
7. Na stránce **Přidat role do projektu** zadejte v poli **Počet zdrojů** číslo **1**.
8. V poli **Zdroj** vyhledávání zobrazí všechny zdroje, které mají požadované kompetence. Vyberte položku **Daniel Goldschmidt**a potom vyberte **Vytvořit**.
9. Na stránce **Projekt** vyberte příkaz **Přidat**.
10. V podokně **Přidat role do projektu** vyberte v poli **Role** hodnotu **Člen týmu**. V poli **Počet zdrojů** zadejte **5**.
11. Vyberte **Vytvořit**.
12. Na stránce **Projekty** vyberte **Splnit prostředek**.

## <a name="resource-capacity-synchronization"></a>Synchronizace kapacity zdroje
Procesy pro synchronizaci zdrojů pomáhají zaručit, že informace kalendáře a základního kalendáře se postupně dostávají do plánování zdrojů projektu. Pokud se kalendář změní, procesy provedou požadované aktualizace plánování projektových zdrojů. Procesy také pomáhají zlepšit výkon, protože informace o zdrojích kalendáře jsou synchronizovány předem. Aktualizace informací o plánování prostředků proto probíhají rychleji. Doporučujeme naplánovat spouštění procesů v dávce namísto po jednom. V opačném případě existuje riziko, že někdo zapomene hraniční datumy období, kdy byly informace naposledy synchronizovány. Pokud se nepoužívají správné hraniční datumy, mohou se během synchronizace datumů objevit mezery.

![Synchronizace kalendáře](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synchronizace souhrnů kapacity zdrojů

Proces synchronizace je navržen tak, aby synchronizoval všechny informace kalendáře zdrojů. Tyto informace zahrnují informace základního kalendáře o všech změnách v tabulce kapacity kalendáře zdrojů projektu. Pokud jsou do projektu přidány nové zdroje, synchronizace pomáhá zaručit, že jsou k dispozici aktualizované informace kalendáře. Tuto synchronizaci lze provést kdykoli.

Doporučujeme vám použít dávkovou aktualizaci. Možnosti jsou k dispozici během synchronizace rezervací kapacity.

1. Vyberte **Správa projektů a účetnictví** &gt; **Periodické** &gt; **Synchronizace kapacity** &gt; **Synchronizace souhrnů kapacity zdrojů**.
2. Nastavte možnosti v následující tabulce.

    | Možnost      | Popis |
    |-------------|-------------|
    | Kód období | Volitelně vyberte kód intervalu datumů hlavní knihy a nastavte tak počáteční a konečné datum procesu synchronizace souhrnů kapacity zdrojů. |
    | Počáteční datum  | Zadejte počáteční datum procesu synchronizace souhrnů kapacity zdrojů. |
    | Koncové datum    | Zadejte koncové datum procesu synchronizace souhrnů kapacity zdrojů. |

[![Proces synchronizace](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Nastavení rolí v šablonách strukturovaného rozpisu prací
Projektoví manažeři mohou nastavit šablony strukturovaného rozpisu prací, které mohou použít při vytváření strukturovaného rozpisu prací pro nové projekty. Projektoví manažeři mohou při vytváření šablony přidávat role. Pomocí následujícího postupu přiřadíte roli šabloně strukturovaného rozpisu prací.

1. Vyberte **Správa projektu a účetnictví** &gt; **Nastavení** &gt; **Projekty** &gt; **Šablony strukturovaného rozpisu prací**.
2. Vyberte položku **Detaily** pro vybranou šablonu strukturovaného rozpisu prací.
3. Vyberte úkol v seznamu a poté v poli **Role** vyberte roli, kterou chcete k úkolu přiřadit.

### <a name="work-with-a-wbs"></a>Práce se strukturovaným rozpisem prací

Můžete vytvořit nový strukturovaný rozpis prací nebo můžete zkopírovat rozpis z existující šablony strukturovaného rozpisu prací. Projektový manažer může snadno spravovat zdroje přiřazením rolí k novým úkolům ve strukturovaném rozpisu prací. Role lze vyměnit buď po získání zdroje, nebo po identifikaci potvrzeného zdroje pro práci na úkolu. Tato flexibilita umožňuje projektovým manažerům provádět následující úkoly:

- Určit počet zdrojů, které jsou vyžadovány pro pracovní balíčky strukturovaného rozpisu prací.
- Odhadovat projektové náklady.
- Určit předběžný rozpočet.
- Odhadnout trvání aktivity na základě rolí a zdrojů.
- Vypracovat některé plány správy projektů na základě dostupných informací o projektu.

Do strukturovaného rozpisu prací byly přidány další možnosti pro lepší využití funkce zajišťování zdrojů.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Možnost</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Přiřazení zdrojů</td>
<td>Zobrazit přiřazené zdroje, datumy, počet hodin a typ rezervace pro úkoly na strukturovaném rozpisu prací.</td>
</tr>
<tr class="even">
<td>Automaticky vygenerovat tým</td>
<td>Automaticky přidávat plánované prostředky pomocí rolí, které jsou přidruženy k úkolu. Aplikace Finance automaticky navrhne plánované zdroje pomocí multikriteriální rozhodovací analýzy založené na rolích. Po nastavení rolí a úsilí (v hodinách) pro úkoly ve WBS a po uvolnění struktury vyberte příkaz <strong>Automaticky generovat tým</strong>. Požadovaný počet plánovaných zdrojů je přidán do strukturovaného rozpisu prací a na kartu <strong>Plánování projektu a týmu</strong>.</td>
</tr>
<tr class="odd">
<td>Zdroj (rozevírací seznam)</td>
<td>Na stránce <strong>Spustit přiřazení prostředku</strong> můžete vybrat zdroje pro závaznou nebo předběžnou rezervaci na základě zadané doby trvání. Můžete upravit nastavení zobrazení, abyste viděli a nastavili dobu trvání aktivit zdrojů. Zdroje můžete vybrat a přiřadit na úrovni pracovního balíčku pomocí následujících možností:
<ul>
<li><strong>Přijmout</strong> – Potvrďte změny zdroje, který je přiřazen k úkolu.</li>
<li><strong>Zrušit</strong> – Zrušte změny zdroje, který je přiřazen k úkolu.</li>
<li><strong>Přiřadit automaticky</strong> – Dostupný personální zdroj, který má odpovídající roli, je automaticky vybrán a přiřazen k vybranému úkolu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stránce **Všechny projekty** vyberte projekt **Fáze 2 upgradu XYZ**.
2. Vyberte **Plán** &gt; **Aktivity** &gt; **Strukturovaný rozpis prací**.
3. Výběrem možnosti **Nový** přidáte do strukturovaného rozpisu prací následující aktivity první úrovně:

    - Spouštěcí
    - Plánování
    - Spouštění
    - Monitorování a řízení
    - Uzavřeno

4. Nastavte data a úsilí (v hodinách), jak je znázorněno na následujícím obrázku.

    [![Nastavení dat a úsilí](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Vyberte řádek úlohy **Spouštěcí** a poté v poli **Role** vyberte **Vyšší projektový manažer**.
6. Vyberte **Publikovat**.
7. Na stejném řádku vyberte v poli **Zdroj** položku **Daniel Goldschmidt** a potom vyberte **Přijmout**.
8. Vyberte řádek úlohy **Plánování** a poté v poli **Role** vyberte položku **Obchodní analytik**.
9. Vyberte příkaz **Publikovat** a potom vyberte **Automaticky generovat tým**.
10. V okně se zprávou, které se objeví, vyberte **Ano**.
11. V poli **Zdroj** ověřte, zda je v něm hodnota **Obchodní analytik 1**.
12. Pro zdroj **Obchodní analytik 1** otevřete vyhledávání a vyberte možnost **Spustit přiřazení zdrojů**. Poté vyberte pracovníka pro úkol.
13. Vyberte možnost **Předběžně přiřadit** &gt; **Plná kapacita**.

    > [!NOTE] 
    > Neobdržíte varování, že zadaný zdroj je nyní 2, protože počet zdrojů zůstává 1.

14. Na stránce **Strukturovaný rozpis prací** ověřte přiřazení zdrojů ve strukturovaném rozpisu prací a poté vyberte příkaz **Uložit**.

## <a name="resource-fulfillment-for-planned-resources"></a>Plnění zdrojů pro plánované zdroje
Manažer projektu může naplánovat požadované role zdrojů pro projekt. Správce zdrojů uvidí tyto plánované zdroje jako požadavky na stránce **Plnění zdrojů** a může přiřadit skutečné zdroje.

1. Na stránce **Všechny projekty** vyberte projekt **Fáze 2 upgradu XYZ**.
2. Vyberte položku **Projekt** a poté vyberte příkaz **Upravit**.
3. Na kartě **Projektový tým a plánování** vyberte možnost **Přidat**.
4. V dialogovém okně **Přidat role** vyberte roli **Vývojář softwaru**.
5. Vyberte příkaz **Vytvořit** a poté zavřete stránku projektu.
6. Na stránce **Plnění zdrojů** vyberte položku **Softwarový vývojář 1** pro projekt **Fáze 2 projektu Upgrade XYZ**.
7. Vyberte pracovníka a poté zvolte **Přiřadit**.
8. Ověřte, zda byl řádek pro **Softwarového vývojáře 1** odstraněn u projektu **Fáze 2 projektu Upgrade XYZ**.
9. Na kartě **Projektový tým a plánování** u projektu **Fáze 2 projektu Upgrade XYZ** ověřte, že pracovník vybraný v předchozím kroku byl přidán jako **Softwarový vývojář**.

## <a name="requests-for-project-resources"></a>Žádosti o projektové zdroje
Funkce pro plánování projektových zdrojů slouží pouze k tomu, aby manažeři zdrojů distribuovali personální zdroje na zakázkách nebo projektech. Chcete-li povolit tuto funkci, proveďte následující úkoly nebo ověřte, že byly dokončeny:

- Nastavte číselné řady.
- Nastavte pracovní postupy pro správu projektů a účetnictví.
- Povolte pracovní postupy žádostí o zdroje.

Po dokončení předchozích úkolů můžete podle potřeby dokončit následující úkoly:

- Vytvořte požadavek na zdroj z předběžně rezervovaného personálního zdroje.
- Monitorujte žádosti o zdroje.
- Vyřizujte žádosti o zdroje.
- Požádejte o personální zdroj ze strukturovaného rozpisu prací.
- Rezervujte si zdroje do projektu bez požadavku na personální zdroj.

## <a name="monitor-project-teams"></a>Monitorování projektových týmů
1. Na stránce **Všechny projekty** vyberte odkaz **ID projektu** pro projekt **Fáze 2 upgradu XYZ**.
2. Na kartě **Projektový tým a plánování** ověřte, zda jsou projektové zdroje v seznamu správné.
