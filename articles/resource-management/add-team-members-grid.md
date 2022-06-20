---
title: Přidejte členy týmu z mřížky členů týmu
description: Tento článek obsahuje informace o způsobu správy zdrojů členů týmu.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3c0c277ca1fe2b709a6ff1c626f5ea7ec63705d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928562"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Přidejte členy týmu z mřížky členů týmu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations obsahuje řídicí panel Správce zdrojů, který poskytuje vizuální přehled o poptávce a využití zdrojů v celé organizaci. Grafy na tomto řídicím panelu můžete použít k vizualizaci následujících informací:

- **Poptávka po zdroji**: graf **Aktivní žádost o zdroj** zobrazuje zdroje, které byly odeslány. Zdroje jsou agregovány podle role nebo projektu.
- **Neodeslaná poptávka po zdroji**: graf **Nepřiřazená poptávka po zdroji** zobrazuje všechny požadavky na zdroje, které nebyly odeslány. Graf pomáhá správcům zdrojů Zobrazit poptávku, která není pevná a může být odeslána prostřednictvím žádosti o zdroj.
- **Fakturovatelné využití za minulý týden**: graf **Využití podle role** zobrazuje procentuální hodnotu skutečného fakturovatelného využití podle role v rámci organizace vzhledem k jejímu cílovému fakturovatelnému využití podle role.

    > [!NOTE]
    > Chcete-li graf **Využití podle role** zpřístupnit, vytvořte úlohu, která spustí pracovní postup **UpdateRoleUtilization**. Tato opakovaná úloha se spouští každých sedm dní pro výpočet fakturovatelného využití za předchozích sedm dní. Výsledky jsou agregovány podle role.

## <a name="manage-project-team-members"></a>Správa členů projektového týmu

Projektoví manažeři mohou pomocí řídicího panelu správce zdrojů spravovat zdroje na projektech. Mohou například přidat člena týmu přímo do projektu a rezervovat člena týmu, aby splnili požadavky na zdroje, které byly zachyceny obecným zdrojem.

### <a name="add-a-team-member-directly-to-a-project"></a>Přidání člena týmu přímo do projektu

Chcete-li přidat člena týmu přímo do projektu, vyberte ve formuláři **Projekty**, na kartě **Tým** **Nový**. Zobrazí se dialogové okno **Vytvořit: Člen projektového týmu**. V tomto dialogovém okně můžete provádět následující úkoly:

- **Rezervace pojmenovaného zdroje**: v poli zdroj **Rezervovatelný zdroj** vyberte název zdroje. Potom vyberte roli, nastavte období a vyberte metodu přidělení. Pojmenovaný zdroj, který jste vybrali, je přidán do projektu pomocí vybrané metody přidělení a kalendáře zdrojů.
- **Přidání obecného zdroje**: ponechte pole **Rezervovatelný zdroj** prázdné, a poté vyberte roli, nastavte období a vyberte upřednostňovanou metodu přidělení. Obecný zdroj je přidán do týmu jako zástupný symbol. Zástupný symbol obsahuje vzor poptávky, který se používá k rezervaci pojmenovaných zdrojů v týmu. Požadavek je proveden podle projektového kalendáře.
- **Přidání pojmenovaného zdroje do týmu bez spotřeby kapacity zdroje**: v poli **Rezervovatelný zdroj** vyberte zdroj. Vyberte období a potom jako metodu přidělení vyberte **Žádná**. Zdroj je přidán do týmu, ale kapacita zdroje není při rezervaci spotřebována.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezervace člena týmu za účelem splnění požadavků na zdroje pro obecný zdroj

V části Project Operations můžete rezervovat obecný prostředek v projektovém týmu. Můžete také určit roli, požadovanou kapacitu a způsob distribuce této kapacity. U požadavku na zdroj můžete zadat atributy, které jsou přidruženy k obecnému zdroji. Tyto atributy zahrnují požadované dovednosti, upřednostňovanou organizační jednotku a upřednostňované zdroje.

Chcete-li pro vývojáře zadat požadované dovednosti u obecného zdroje, proveďte následující kroky.

1. Chcete-li rezervovat obecný zdroj, ve formuláři **Projekty** na kartě **Tým** vyberte **Nový**.
2. V zobrazení **Všichni členové týmu**, ve sloupci **Požadavek na zdroj** vyberte odkaz pro přidání požadovaných požadovaných dovedností pro obecný zdroj.
3. Ve formuláři **Požadavek na zdroj** vyberte v mřížce **Dovednosti** výpustku (**…**) a pak vyberte **Přidat novou charakteristiku požadavku**, chcete-li přidat požadované dovednosti pro vývojáře.
4. V dialogovém formuláři **Vytvořit: Charakteristika požadavku**, které se zobrazí, vyberte v poli **Charakteristika** požadovanou dovednost.
5. V poli **Hodnota hodnocení** vyberte úroveň odborné způsobilosti pro tuto dovednost. 
6. V poli **Požadavek na zdroj** nastavte požadavek na zdrojové zdroje z organizačních jednotek nebo dokonce pojmenovaných zdrojů. Jakmile budete hotovi, zvolte tlačítko **Uložit**.
7. Chcete-li splnit požadavek na zdroj, vyberte ve formuláři **Požadavek na zdroj** **Rezervovat**. Můžete také vybrat obecný zdroj v mřížce **Všichni členové týmu** a pak vybrat **Rezervovat**.

    > [!NOTE]
    > V tomto příkladu je požadováno 40 hodin, ale žádné skutečné rezervované hodiny, protože obecné zdroje nemají rezervace. Navíc nejsou přiřazeny žádné hodiny, protože obecný zdroj byl přidán přímo do týmu místo toho, aby byl přidán pomocí přiřazení úkolu.

    Na formuláři **Pomocník plánování** můžete filtrovat dostupné zdroje podle požadavků, které jsou specifikovány u požadavku na zdroj. Zdroje jsou seřazeny podle parametrů řazení, které jsou specifikovány v Plánovací vývěsce.

   Mezi nejčastěji používané filtry patří:

    - **Vlastnosti společně s hodnocením**: filtr podle dovedností, certifikací a dalších vlastností zdroje, kromě hodnocení odbornosti.
    - **Role**: filtr podle výchozích rolí, které jsou přiřazeny k rezervovatelným zdrojům.
    - **Organizační jednotky**: filtr rezervovatelných zdrojů podle organizačních jednotek, ke kterým jsou přiřazeny.

8. Pokud nejste spokojeni s výsledky počátečního hledání požadavku, můžete kritéria filtru změnit. Chcete-li najít další zdroje, rozbalte podokno **Filtrovat zobrazení** a pak vyberte **Hledat**. Chcete-li změnit způsob řazení výsledků, vyberte **Řadit**.
9. Vyberte zdroje podle poptávky, která je určena u požadavku, jak je uvedeno v horní části mřížky. Výběr buněk v mřížce můžete vymazat a ponechat tuto kapacitu zdroje otevřenou. Jako rezervovaný lze najednou vybrat pouze jeden zdroj.
10. Chcete-li vybraný zdroj rezervovat, vyberte **Rezervovat** a ponechejte Plánovací vývěsku otevřenou, aby bylo možné vybrat další zdroje. Případně vyberte **Rezervovat a ukončit**, chcete-li rezervovat vybraný zdroj a zavřít Plánovací vývěsku.
11. Vraťte se do zobrazení **Všichni členové týmu**. V mřížce si všimněte, že obecný zdroj byl nahrazen pojmenovaným zdrojem, a že je u tohoto zdroje uvedeno 40 hodin jako rezervovaných.

    > [!NOTE]
    > Nejsou zobrazeny žádné přidělené hodiny, protože byly rezervováni přímo v týmu. Nebyli rezervováni pomocí přiřazení úkolu.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Přiřazení obecného zdroje k úkolům a vygenerování požadavků na zdroj

V Project Operations můžete vytvářet úkoly a poté k nim přiřazovat obecné zdroje. Poptávka po zdroji při odhadu vašeho plánu a finančních čísel pak může být představována zástupnými symboly. Poté můžete generovat požadavky na zdroje pro obecné zdroje a splnit je.

1. Chcete-li vytvořit úlohu, ve formuláři **Projekty** na kartě **Plán** vyberte **Přidat**.
2. V poli **Zdroje** vyberte symbol **Výběr zdroje**. Zobrazí se dialogové okno Výběr zdroje zobrazující existující členy týmu pro projekt.
3. Zadejte název nového obecného zdroje a pak vyberte **Vytvořit**.
4. V dialogovém okně **Vytvořit: Člen projektového týmu**, které se zobrazí, vyberte v poli **Role** roli obecného zdroje. 
5. V poli **Jednotka zdroje** vyberte organizační jednotku pro obecný zdroj. Pak vyberte **Uložit**. Obecný člen týmu je nyní přiřazen k úkolu.

   Na kartě **Tým** se zobrazí nový obecný člen týmu. Povšimněte si, že má přiřazené pouze hodiny. Tyto hodiny představují součet všech úkolů, které jsou přiřazeny k obecnému členu týmu. Obecný člen týmu ještě nemá požadované hodiny ani požadavek na zdroj.

6. Obecného člena týmu můžete nyní přiřadit k jiným úkolům pomocí symbolu Výběr zdroje.

   Po dokončení přiřazení obecného zdroje k úkolům můžete generovat požadavek na zdroj pro obecný zdroj.

7. Na kartě **Tým** vyberte obecný zdroj a pak vyberte **Generate Requirement**. Po vygenerování požadavku bude mít obecný člen týmu požadované hodiny a odkaz na požadavek na zdroj.

  Jakmile provedete rezervaci pojmenovaného zdroje, je obecný zdroj odebrán z týmu a nahrazen pojmenovaným zdrojem. Na kartě **Plán** jsou odebrána přiřazení obecných zdrojů a nahrazena pojmenovaným zdrojem.

  > [!NOTE]
  > K tomuto chování dochází pouze v případě, že je pojmenovaný zdroj plně rezervovaný pro obecný požadavek na zdroj. Pokud některý pojmenovaný zdroj částečně nahradí požadavek na obecný zdroj nebo více pojmenovaných zdrojů nahradí požadavek na obecný zdroj, zůstane obecný zdroj přiřazen k úkolu.

Project Operations nepřiřazuje k úkolu oba zdroje, protože toto chování by vyvolalo méně předvídatelný plán. V tomto jednoduchém příkladu je snadné rozdělit hodiny rovnoměrně mezi dva zdroje. Ve složitějších scénářích, které zahrnují více úkolů a více zdrojů, by však aplikace PSA musela učinit předpoklady, jak by měla rozdělit rezervace přijaté pro více zdrojů ve více úkolech.

Proto je v těchto scénářích za analýzu vícenásobných rezervací a jejich přiřazení podle potřeby zodpovědný projektový manažer. K rozdělení rezervací přiřadí vedoucí projektu úkoly z obecných zdrojů k pojmenovaným zdrojům a potom použije zobrazení **odsouhlasení**, aby se ujistil, že přidělení pracuje s rezervacemi.

### <a name="edit-a-resource-requirement"></a>Úprava požadavku na zdroj

Po vytvoření požadavku na zdroj může projektový manažer nebo správce zdrojů chtít upravit podrobnosti a upřesnit kritéria hledání při použití plánovací vývěsky. Chcete-li upravit požadavek na zdroj, postupujte následovně.

1. Ve formuláři **Projekty** vyberte na kartě **Tým** odkaz na libovolný požadavek na obecný zdroj.
2. Ve formuláři **Požadavek na zdroje**, který se zobrazí, zadejte potřebné informace o poli

   Ve formuláři **Požadavek na zdroje** projektový manažer nebo manažer zdrojů může také definovat dovednosti, role, preference zdrojů a preferovanou organizační jednotku.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Aktualizace rezervací zdrojů po jejich rezervaci do projektu

Po přidání obecného nebo pojmenovaného zdroje do projektového týmu můžete změnit rezervace zdrojů.

1. Ve formuláři **Projekty** vyberte na kartě **Tým** člena týmu a poté vyberte **Zachovat rezervace**.
 
   Zobrazí se Plánovací vývěska a zobrauje rezervace členů projektového týmu. Rozbalte záznam člena týmu a zobrazte hodiny, které byly zarezervovány pro tento projekt a další projekty, které spotřebovávají kapacitu tohoto člena týmu.

2. Výběrem a přetažením rezervace ji prodlouhujte nebo zkrátíte. Zobrazí se dialogové okno **Vytvořit rezervaci zdroje**, které vám umožní upravit rezervaci.
3. Klepněte na rezervaci pravým tlačítkem myši. Potom můžete pomocí místní nabídky provést následující akce:

    - Změna stavu rezervace
    - Upravit rezervaci.
    - Nahrazení zdroje v projektovém týmu

### <a name="change-the-booking-status"></a>Změna stavu rezervace

Můžete změnit libovolný výchozí nebo vlastní stav rezervace.

Následující stavy jsou k dispozici v Project Operations:

- **Zrušeno**: zruší rezervaci zdroje a uvolní kapacitu zdroje.
- **Závazné rezervace**: spotřebovávají kapacitu zdroje. Rezervace má obvykle tento stav, když otevřete **Zachovat rezervace** z mřížky **Všichni členové týmu** ve formuláři **Projekty**.
- **Předběžná rezervace**: přidá zdroj k týmu, ale nespotřebovává kapacitu zdroje. Tento stav označuje, že zdroj byl rezervován pro potenciální práci, ale stále má kapacitu, pokud je potřebný pro jiné práce. Vzhledem k celkové dostupnosti zdroje mají předběžné rezervace jiný stav než závazné rezervace.
- **Navrženo**: Představuje návrh správce zdroje nebo projektového manažera pro zdroj. Návrhy nespotřebovávají kapacitu zdroje a zdroj není přidán do projektového týmu. Chcete-li zdroj v týmu pevně rezervovat, musí projektový manažer tento návrh přijmout.

### <a name="submit-resource-requests"></a>Odeslání požadavků na zdroj

Požadavky na zdroj se používají k přenosu poptávky nebo požadavku na zdroj, která musí být splněna správcem zdroje. Pro obecný zdroj, který je již v týmu, můžete odeslat požadavek na zdroj přímo. Žádost o zdroj lze splnit dvěma způsoby:

- Správce zdroje přímo splní žádost. V tomto případě je obecný zdroj nahrazen závaznou rezervací, která obsahuje pojmenovaný zdroj.
- Správce zdroje navrhne zdroj projektovému manažerovi a projektový manažer navržený zdroj schválí nebo zamítne.

#### <a name="direct-fulfillment-of-resource-requests"></a>Přímé plnění žádostí o zdroje

Při generování požadavku na zdroj může projektový manažer odeslat žádost o zdroj pro obecný zdroj výběrem zdroje a následným výběrem **Odeslat žádost**. Komentáře ke zdroji mohou být poskytnuty správci zdroje, který požadavek plní. Po odeslání požadavku se pole **Stav** pro člena týmu změní na **Odesláno**. Jakmile správce prostředku splní požadavek, bude obecný člen týmu v mřížce **Všichni členové výmu** nahrazen pojmenovaným zdrojem.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Použití návrhu zdroje pro žádosti o zdroje

Namísto přímého rezervování zdroje na základě žádosti o zdroj může správce prostředku navrhnout zdroj projektovému manažerovi. Správce prostředku může tuto možnost použít, pokud není k dispozici přesná shoda požadavků. Když správce prostředku navrhne zdroj, projektový manažer uvidí, že je pole **Stav** pro obecného člena týmu změněno na **Potřebuje kontrolu**.

Můžete si prohlédnout navrhovaný zdroj společně s vizualizací účinku rezervace nabídky. 

1. Poklepejte na člena týmu, který má stav **Vyžaduje kontrolu**. 
2. Vyberte kartu **Navržené zdroje**.
3. Vyberte **Přijmout všechny návrhy**, abyste přijali všechny navržené zdroje nebo **Zamítnout všechny návrhy**, abyste je zamítli. Přijmete-li navržené zdroje, budou v projektu závazně zarezervovány jako členové týmu a nahradí obecné zdroje.

> [!NOTE]
> Všechny navržené zdroje musíte buď přijmout, nebo zamítnout. Nemůžete je částečně přijmout nebo zamítnout.

### <a name="substitute-a-resource-on-the-project-team"></a>Nahrazení zdroje v projektovém týmu

Projektový manažer někdy musí v projektu nahradit rezervovaného člena týmu.

1. Ve formuláři **Projekty** vyberte na kartě **Tým** zdroj, který vyžaduje náhradu a poté vyberte **Zachovat rezervace**.
2. Chcete-li zobrazit projekty, ke kterým je zdroj přiřazen, rozbalte ho.
3. Klepněte pravým tlačítkem myši na projekt a vyberte **Nahradit zdroj**.
4. Pokud znáte zdroj, kterým chcete nahradit aktuální zdroj, vyberte ho nebo zadejte jeho název a pak vyberte **Znovu přiřadit**.

Or. Pokud potřebujete vyhledat zdroj, proveďte následující kroky.

1. Vyberte **Najít náhradu**.

   Pomocník plánování vrátí seznam dostupných náhrad. V Pomocníkovi plánování můžete dále filtrovat dostupné zdroje a najít vhodnou náhradu.

2. Chcete-li nahradit zdroj, vyberte zdroj, který chcete a pak vyberte **Nahradit**.   

   Rezervace a přiřazení budou nahrazeny novým zdrojem.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Spárování rezervací a přiřazení člena týmu

Pro členy týmu jsou rezervace a přiřazení volně provázené. Jinými slovy, zdroje mohou obsahovat přiřazení, ale žádné rezervace, nebo mohou obsahovat rezervace, ale žádná přiřazení. V ideálním případě by měly být rezervace a přiřazení zarovnány, aby zdroje měly potvrzenou kapacitu k provádění přiřazení úkolů. Rezervace mohou být však založeny na dostupnosti a časování úkolů se může při pokračování projektu změnit. Volné spojení rezervací a přiřazení je proto flexibilní.

Project Operations obsahuje kartu **Vyrovnání** která projektovým manažerům umožňuje vyrovnat rezervace a přiřazení členů týmů pro projektové týmy.

Karta **Vyrovnání** zobrazuje rezervace a přiřazení až k úrovni jednotlivých přiřazení úkolů pro každého člena týmu. Zobrazuje hodiny v buňkách reprezentujících časová období od měsíců po dny.

Na kartě je také zobrazen celkový čistý součet pro projekt, spolu se sloupcem celkem.

Pro každý zdroj je na kartě vypočten rozdíl mezi rezervacemi člena týmu a souhrnnými přiřazeními člena týmu. V ideálním případě by tento rozdíl měl být 0 (nula). Jinými slovy, mezi rezervacemi a přiřazeními by neměl být žádný rozdíl. Rozdíly jsou barevné a stínované, aby upozornily na dva stavy:

- **Nedostatečná rezervace**: objeví se v případě, že zdroj obsahuje více přiřazení než rezervací. Vzhledem k tomu, že tato kapacita nebyla rezervována, může projektový manažer tento stav napravit rozšířením rezervací zdroje tak, aby pokryly deficit.
- **Nadbytečné rezervace**: Dochází, pokud byl zdroj rezervován do projektu, ale nebyl přiřazen k úkolům. Tento stav může být přijatelný v případech, kdy byl zdroj pro projekt rezervován předtím, než došlo k přiřazení úkolu. V jiných případech však není plánováno přiřazení zdroje k úkolům. V těchto případech by měl projektový manažer zvážit zrušení rezervací zdroje, aby bylo možné použít kapacitu pro jiný projekt.

Pokud v některých případech zobrazíte čas na vyšší úrovni než denní úroveň, například úroveň měsíce, můžete u zdroje vidět čistý nulový rozdíl. Jinými slovy, rezervace = přiřazení. Pokud však zobrazíte čas na úrovni týdne, můžete se setkat s tím, že v prvním týdnu jsou přiřazení ve výši nula hodin a rezervace 40 hodin, ale ve druhém týdnu jsou přiřazení 40 hodin a rezervace nula hodin. Celkově jsou rezervace a přiřazení vyrovnané, liší se však od jednoho týdne k dalšímu.

Když zobrazíte čas na vyšších úrovních, buňky na kartě **Vyrovnání** mají indikátor, který vás upozorní, že se na nižších úrovních vyskytují rozdíly. Dvojitým kliknutím do buňky můžete provést přiblížení a zobrazit rozdíl. Kliknutím pravým tlačítkem myši můžete zobrazení oddálit. Výběrem zdroje a následným výběrem ovládacího prvku **Další rozdíl** na panelu nástrojů mřížky můžete přejít na další rozdíl mezi rezervacemi a přiřazeními pro daný zdroj. Vyberte **Předchozí rozdíl** pro návrat. V **Nastavení** také můžete vypnout ukazatel rozdílu a chování navigace.

Pokud máte pro zdroj přiřazení úkolů, ale nemáte žádné rezervace, vyberte ve formuláři **Projekty**, na kartě **Vyrovnání** nedostatečnou rezervaci a pak vyberte **Prodloužit rezervaci**. Zobrazí se dialogové okno **Prodloužit rezervaci**, ve kterém je uvedena rezervace potřebná k vyřešení nedostatku zdroje. Dialogové okno také zobrazuje existující rezervace zdroje ve všech projektech nebo jiných plánovatelných entitách. Pokud vyberete **OK** pro vytvoření rezervace pro zdroj bez ohledu na dostupnost zdroje, můžete způsobit přerezervaci.

Projektový manažer nebo správce prostředku pak může pomocí Plánovací vývěsky spravovat všechny situace, ve kterých je zdroj přerezervovaný nad svoji kapacitu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]