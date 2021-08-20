---
title: Novinky a změny v aplikaci Project Service Automation verze 3
description: Tohle téma poskytuje informace o novinkách a změnách v aplikaci Project Service Automation verze 3.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: afce9cd2d4b3920dc5de5d3deab8920a7f51f275a73918a84db300739b1b4feb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987068"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Novinky a změny v aplikaci Project Service Automation verze 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma poskytuje informace o změnách uživatelského rozhraní (UI), funkčnosti a terminologie v aplikaci Project Service Automation mezi verzemi 2 nebo 1 a verzí 3.

## <a name="project-scheduling"></a>Plánování projektu
Plán projektu, v předchozích verzích označovaný jako strukturovaný rozpis prací, byl přejmenován na plán a je přístupný kliknutím na záložku **Plán**. 

![Plán projektu.](media/psa-schedule-01.png)

Plán má nyní nový vzhled pro interakci, který je moderní a přístupný. Základní plánovací modul aplikace Project Service Automation se však nezměnil. Ovládací tlačítka na pásu karet mřížky plánu umožňují interakci s plánem podobně jako v předchozí verzi Project Service Automation. Další změny plánu zahrnují:

- **Ganttův diagram** – Ganttův diagram již není přítomen. V budoucí aktualizaci se vrátí nová Ganntova vizualizace.
- **Záhlaví sloupců** – Záhlaví sloupců můžete v mřížce skrýt kliknutím na šipku dolů vedle nadpisu sloupce. 
- **Sloupce** – Skryté sloupce můžete zobrazit kliknutím na tlačítko **Přidat sloupec**. 
- **Kategorie transakce** – Vyhledávání **Kategorie transakce** bylo přidáno do mřížky plánu a ve výchozím nastavení je zobrazeno. 
 
## <a name="project-templates"></a>Šablony projektu
Ve funkcích šablony projektu byly provedeny následující změny.

### <a name="create-a-project-template"></a>Vytvoření šablony projektu 
Šablonu projektu můžete vytvořit ve verzi 3 podobně jako v předchozích verzích Project Service Automation. Šablona může obsahovat pouze plán a plán může zahrnovat přiřazení, ale ta nejsou povinná. Pokud má plán přiřazení, mohou být pouze pro obecné zdroje. Je možné generovat požadavky na zdroje pro obecné zdroje, ale nelze je rezervovat se skutečnými zdroji v šabloně. Do týmu v šabloně nelze rezervovat skutečný zdroj. 

### <a name="create-a-template-from-an-existing-template"></a>Vytvoření šablony z existující šablony
Když vytvoříte novou šablonu projektu z existující šablony v aplikaci Project Service Automation verze 3, dojde k následujícímu: 

- Plán zdrojového projektu bude zkopírován do šablony. 
- Obecné zdroje budou zkopírovány do týmu a všechna přiřazení obecných zdrojů budou zkopírována. Požadavky na obecné zdroje nebudou zkopírovány. 

### <a name="create-a-template-from-an-existing-project"></a>Vytvoření šablony z existujícího projektu
Když vytvoříte novou šablonu projektu z existujícího projektu ve verzi PSA 3, dojde k následujícímu: 

- Plán zdrojového projektu bude zkopírován do šablony. 
- Obecné zdroje budou zkopírovány do týmu a všechna přiřazení obecných zdrojů budou zachována. Požadavky na obecné zdroje nebudou zkopírovány.    
- Pojmenované zdroje, přiřazené nebo nepřiřazené, budou z týmu odebrány a nahrazeny obecnými zdroji.
- Pokud existují, informace o odběrateli budou odebrány. 
- Pokud existují, odkazy na nabídky a smlouvy budou odebrány. 

### <a name="create-a-project-from-a-template"></a>Vytvoření projektu ze šablony
Když vytvoříte nový projekt ze šablony v aplikaci Project Service Automation verze 3, dojde k následujícímu:

- Plán, tým a přiřazení se zkopírují do nového projektu.   
- Počáteční datum bude buď datum kopírování nebo datum vybrané uživatelem.   
- Pro všechny obecné členy týmů s požadavky na zdroje v šabloně nebudou požadavky zkopírovány ani automaticky vygenerovány. Bude nutné je vygenerovat. 

## <a name="copy-a-project"></a>Zkopírovat projekt
Při kopírování projektu v aplikaci Project Service Automation verze 3 dojde k následujícímu: 

- Odhadované počáteční datum se zkopíruje, ale bude možné je změnit.  
- Bude zkopírován plán projektu a úkoly. 
- Zkopírují se obecné zdroje a jejich přiřazení. Požadavky na obecné zdroje nebudou zkopírovány. Bude nutné je znovu vygenerovat. 
- Skutečné zdroje a jejich přiřazení se nezkopírují. Místo toho budou nahrazeny obecnými zdroji. 
- Skutečnosti se do nového projektu nezkopírují. 

## <a name="move-a-scheduled-project"></a>Přesunutí plánovaného projektu
Pokud přesunete plán existujícího projektu vpřed, dojde k následujícímu: 

- Data úkolů budou automaticky přesunuta tak, aby odpovídala období přesunu. 
- Přiřazené obecné zdroje zůstanou přiřazeny.   
- Pokud jsou vygenerovány před tím, než bude projekt přesunut, zůstanou požadavky na obecný zdroj stejné a nebudou automaticky znovu vygenerovány. Budete je muset vygenerovat znovu, aby odrážely nová přiřazení z důvodu přesunu úkolu. 
- Přiřazení skutečných zdrojů se změní v souladu s přesunem data úkolu. Rezervace skutečných zdrojů se nezmění. Rezervace bude nutné upravit pomocí zobrazení vyrovnání. 
- Týmové zdroje s rezervacemi, ale bez přiřazení se nezmění. 
- Skutečnosti nebudou přesunuty. 

## <a name="estimates"></a>Odhady
Odhady byly rozděleny na dvě karty, **Přiřazení zdroje** a **Odhady**. Záložka **Přiřazení zdroje** obsahuje odhady intenzity a zobrazuje přiřazení zdrojů pro úkoly v zobrazení s časovým uspořádáním. Odhady můžete upravit na základě toho, co modul plánování vygeneroval.

![Karta Přiřazení zdrojů, která zobrazuje odhady intenzity a přiřazení zdrojů pro úkoly.](media/resource-assignments-tab-02.png)

Karta **Odhady** zobrazuje částky nákladů a prodeje pro přiřazení zdrojů. Částky jsou jen pro čtení. Ceny nákladů a prodeje jsou nyní řízeny z přiřazení členů týmu podle plánu. To znamená, že pokud máte úkol bez přiřazení, úkol se zobrazí pod nepřidělený kbelík. To také znamená, že bez **Role**, což je výchozí cenová dimenze, nebudou k dispozici žádné odhadované náklady nebo prodeje, pokud máte zákazníka nebo smlouvu/nabídku spojenou s projektem. 

![Karta Odhady, která zobrazuje částky nákladů a prodeje.](media/estimates-tab-03.png)
  
Kategorie je podporována také u úkolů v zobrazení plánu. Seskupení podle kategorie v zobrazení odhadů s časovým uspořádáním poskytuje lepší možnosti, zejména pokud máte v projektu také odhady výdajů. Odhady výdajů se zapisují pomocí mřížky na samostatné kartě. 

Odhady výdajů lze zapsat do mřížky na kartě **Odhady výdajů**. 

![Karta Odhady výdajů, která zobrazuje mřížku odhadů výdajů.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Správa zdrojů
V aplikaci Project Service Automation verze 3, s novým uživatelským rozhraním jednotného klienta a změnami ve vztahu mezi rezervacemi a přiřazeními, se personální obsazení projektu s obecnými nebo skutečnými zdroji výrazně liší od verze 2 a 1. Koncepce rezervovatelných zdrojů, **skutečné** i **obecné**, však zůstávají stejné stejně jako členové týmu, požadavky, přiřazení a rezervace.   

![Používání výběru zdrojů.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Přiřazení skutečného rezervovatelného zdroje 
V aplikaci Project Service Automation verze 3 nejsou rezervace a přiřazení úkolů tak úzce propojeny jako v předchozích verzích automatizace Project Service Automation. Pomocí mřížky týmu můžete rezervovat **skutečného** člena týmu, podobně jako na trhu.

Pomocí výběru zdrojů v plánu můžete vybrat člena týmu vytvořeného v týmovém zobrazení a přiřadit ho k úkolům. Můžete mu i nadále přiřazovat úkoly, a to i po jeho rezervaci. Pomocí karty **Vyrovnání** lze vyrovnat členy týmu, kteří mají rozdíly v rezervacích a přiřazeních.

Výběr zdrojů zobrazí členy týmu pro daný projekt. Pomocí výběru zdroje můžete také vyhledat a vybrat další rezervovatelné zdroje, které nejsou součástí projektového týmu. Můžete je přiřadit k úkolu a stanou se součástí projektového týmu. Budete je muset rezervovat pomocí karty **Plánovací vývěska** nebo **Vyrovnání**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Přiřazení obecného zdroje pro úkol a projektový tým a následné vyplnění pomocí skutečného zdroje prostřednictvím plánovací vývěsky 
V aplikaci Project Service Automation verze 3 se funkce generování týmu nepoužívá pro obecné zdroje. Místo toho můžete vytvořit a přímo přiřadit obecný zdroj z plánu zadáním názvu pozice obecného zdroje do buňky zdroje v plánu. Nebo vyberte ikonu zdroje v buňce a poté pomocí výběru zdroje zadejte název obecného zdroje, který chcete vytvořit. Otevře se panel pro rychlé vytvoření, který vám umožní nastavit roli a organizační jednotku člena týmu obecného zdroje. Po vytvoření zdroje bude tento zdroj přiřazen k úkolu a můžete i nadále přiřazovat tento obecný zdroj k jiným úkolům v plánu.    
 
Pokud jste přiřadili zdroj ke všem příslušným úkolům, můžete vygenerovat požadavek na zdroj a poté jej vyplnit přímou rezervací pomocí **plánovací vývěsky** nebo odesláním žádosti o zdroj. Obecné zdroje můžete také přidat přímo do mřížky členů týmu. 

Obecné zdroje jsou přidány do projektového týmu bez požadavků na zdroje a s počátečními/koncovými daty projektu, dokud nebude vygenerován požadavek na zdroj. Chcete-li vygenerovat požadavek, vyberte obecný zdroj a klikněte na možnost **Vygenerovat**. Odkaz na požadavek se nyní zobrazí a požadované hodiny budou vyplněny přiřazenými hodinami. Kliknutím na odkaz můžete požadavek otevřít a aktualizovat.
  
Pokud je rezervace dokončena a zcela vyplněna pojmenovaným zdrojem, bude obecný zdroj nahrazen pojmenovaným zdrojem a přiřazení v plánu bude aktualizováno pomocí pojmenovaného zdroje. 

Navržené zdroje pro požadavky jsou nyní uloženy na kartě namísto samostatné sekce.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Vyplnění obecného zdroje pomocí několika pojmenovaných zdrojů
Pokud je požadavek vyplněn s více zdroji, zůstane obecný zdroj v týmu a přiřazen k úkolu. Pojmenovaní členové týmu, kteří jsou rezervováni, nejsou přiřazeni jako součást pozice. Projektový manažer může přiřadit požadovanou práci skutečným zdrojům.  Zobrazení **Vyrovnání** nabízí rozpis rezervací mezi více zdrojů pro více přiřazení úkolů. Není to prováděno automaticky, protože ve složitějších scénářích, jako například v případě, kdy máte balík úkolů, které tvoří požadavek, musí být vypočten záměr, jak chce projektový manažer přiřazení provést. Protože systém nedokáže pochopit záměr, je pravděpodobné, že předpoklady budou jiné, než je zamýšleno, a dojde k nesprávnému nebo nepředvídatelnému výsledku. Předvídatelným výsledkem je, že obecný zdroj zůstává přiřazen, dokud projektový manažer záměrně nepřiřadí zdroje pomocí zobrazení **Vyrovnání**.

### <a name="reconciliation"></a>Vyrovnání
Karta **Vyrovnání** zobrazuje rezervace a všechna přiřazení pro každého člena projektového týmu. Zobrazení znázorňuje hodiny v buňkách, které mohou reprezentovat časové body od měsíců po dny. Toto zobrazení umožňuje projektovým manažerům vyrovnat rezervace a přiřazení jednotlivých členů týmu pro daný projektový tým. To je užitečné, protože rezervace a přiřazení úkolů nejsou úzce spjaty, což umožňuje větší flexibilitu při plánování projektu. 

![Karta Vyrovnání, který zobrazuje rezervace a přiřazení pro každého člena projektového týmu.](media/resource-reconciliation-tab-06.png)

Pro každý zdroj je v zobrazení uveden rozdíl mezi rezervacemi člena týmu a souhrnnými přiřazeními úkolů a zobrazují se následující dva rozdíly, které mohou nastat u rezervací a přiřazení v projektu: 

- **Nedostatečná rezervace** – V případě, že zdroj obsahuje více přiřazení než rezervací, dojde k nedostatečné rezervaci. Vzhledem k tomu, že tato kapacita nebyla rezervována, může projektový manažer tento stav napravit rozšířením rezervací zdroje tak, aby pokryly deficit. 
- **Nadbytečné rezervace** – K nadměrným rezervacím dochází, pokud byl zdroj rezervován do projektu, ale nebyl přiřazen k úkolům.  To může být přijatelný výskyt, například pokud byl zdroj před přiřazením úkolu rezervován. V jiných případech však nemusí být zdroj naplánován k přiřazení a projektový manažer by měl zvážit zrušení rezervací zdroje, aby bylo možné využít kapacitu pro jiný projekt. 

Pokud máte přiřazení úkolů pro zdroj bez rezervací (nedostatečná rezervace), můžete vybrat souhrnné nedostatečné rezervace a kliknout na možnost **Prodloužit rezervaci**. Zde si můžete prohlédnout rezervaci potřebnou k vyřešení nedostatku zdrojů a jejich dostupnosti. 
 
## <a name="time-and-expense"></a>Čas a výdaje
Tato část obsahuje informace o změnách času, výdajů a schválení ve verzi 3 aplikace Project Service Automation. Jako součást řešení Dynamics 365 Project Service Automation byla obnovena funkce zadání **Časový záznam**, aby bylo možné využít architekturu Sjednoceného rozhraní. Díky tomu je možné poskytovat konzistentní, jednotné uživatelské rozhraní, které se řídí zásadami přizpůsobivého návrhu na libovolné velikosti obrazovky nebo v libovolném zařízení. 

### <a name="landing-page"></a>Cílová stránka
Ve verzi 3 se již nerozšiřitelné prostřední vlastního časového záznamu nepoužívá. Místo toho se zde používá rozšiřitelná a přístupná nativní mřížka. Funkci časového záznamu můžete používat pomocí mapy webu vlevo. Díky této změně již nebudete moci zadávat čas vždy na jeden týden. Místo toho bude nutné vytvořit časový záznam pro každý den v mřížce. Po vytvoření několika časových záznamů mohou uživatelé hromadně vytvářet časové záznamy pomocí funkce **Kopírovat** vysvětlené později v tomto tématu. 

![Úvodní stránka časového záznamu.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Vytvoření nových časových záznamů 
Kliknutím na možnost **Nový** na pásu karet otevřete stránku pro rychlé vytváření pro časový záznam, kde můžete zadat dobu trvání v minutách, hodinách nebo dnech. Chcete-li to provést, začněte psát h, m nebo d spolu s množstvím.  

![Rychlé vytvoření časového záznamu.](media/quick-create-time-entry-08.png)

Vyhledávací pole jsou podložena systémovými zobrazeními. Pokud například zadáte informace o projektu, bude pole **Projektový úkol** ve výchozím nastavení nastaveno na zobrazení **Moje otevřené projektové úkoly**. Chcete-li vytvořit časové záznamy pro úkoly, které nejsou přiřazeny uživateli, klikněte na možnost **Změnit zobrazení** ve vyhledávání a vyberte zobrazení **Všechny aktivní projektové úkoly**. Po vytvoření časového záznamu a jeho zobrazení v mřížce můžete upravit všechny hodnoty na řádku přímo v mřížce.  

### <a name="bulk-createcopy"></a>Hromadné vytvoření/kopírování 
Po vytvoření několika časových záznamů můžete pomocí funkce kopírování hromadně vytvořit další časové záznamy. Kliknutím na tlačítko **Kopírovat** otevřete dialogové okno **Kopírovat**. V poli **Od období: Počáteční datum** nastavte rozsah dat, ze kterého musí být časová období zkopírována. V poli **Do období: Počáteční datum** zadejte datum, pro které musí být vytvořeny časové záznamy. Kliknutím na možnost **Kopírovat** zkopírujte časové záznamy do odpovídajícího dne v týdnu uvedeného v poli **Do období**. Například pondělní časový záznam z minulého týdne bude zkopírován do pondělí týdne uvedeného v poli **Do období**. 

![Hromadné kopírování časových záznamů.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importovat data 
Přiřazení a výměna se řídí stejným vzorem uživatelského rozhraní, což uživateli umožňuje specifikovat rozsah dat od okamžiku, kdy je třeba importovat rezervace. Pak je třeba explicitně vybrat rezervace, které by měly být zkopírovány do časových záznamů ve stavu **Koncept**. Ve verzi 3 již není možné zobrazit vzor časových záznamů ve stavu **Navrženo** v mřížce a kalendáři.  

### <a name="change-in-calendar-control"></a>Změna v ovládacím prvku kalendáře
Ve verzi 3 jsme zrušili vlastní ovládací prvek kalendáře a nyní používáme kalendář UC k zobrazení časových záznamu pro daný týden. Pomocí tohoto kalendáře můžete zobrazit den, týden a měsíc. 

> [!NOTE]
> Omezení kalendáře spočívá v tom, že tento ovládací prvek nepodporuje akce u jednotlivých položek kalendáře. Nebude například možné vybrat jednu nebo více položek kalendáře a odeslat nebo odstranit tyto položky. Kliknutím na položku kalendáře otevřete stránku **Entita Časový záznam** pro další akce. 

### <a name="extensibility"></a>Rozšiřitelnost
**Zachycení dat ve vlastních polích pouze pro entity časových a výdajových položek** – Časový záznam používá upravitelnou mřížku, mřížku jen pro čtení a ovládací prvky kalendáře z platformy. Všechny tyto ovládací prvky jsou nativní, a proto budou podporovat vlastní nastavení. V aplikaci Project Service Automation verze 3 můžete přidat další vlastní pole, nastavit vyhledávací pole a zálohovat je pomocí vlastních zobrazení. Můžete také nastavit vlastní obchodní logiku založenou na vybraných hodnotách ve vlastních polích.  

**Zachycení dat ve vlastních polích v časových a výdajových položkách a jejich šíření prostřednictvím entit podporujících tok odesílání a schvalování** – Typické zpracování časových záznamů je znázorněno v následujícím diagramu.

![Zpracování toku časového záznamu.](media/process-time-entries-10.png)

Pokud obchodní požadavky stanoví, že časové a výdajové entity musí zachycovat vlastní cenové dimenze a šířit hodnoty, které jsou nastaveny časovým a vstupním zdrojem ve vlastní cenové dimenzi prostřednictvím všech entit v předchozí grafice, najdete informace v části [Nastavení vlastních polí jako cenových dimenzí](set-up-pricing-dimensions.md).

Aby bylo možné podporovat obchodní požadavky v případech, kdy musí časové a výdajové entity zachycovat vlastní jiné než cenové dimenze a šířit hodnoty, můžete použít nastavení cenových dimenzí a vyjádřit vlastní dimenze jako cenové dimenze bez nákladů nebo fakturační sazby. Dalším scénářem je přidání vlastního pole do každé entity pomocí stejného názvu pole ve všech entitách. Vlastní moduly plug-in mohou být vytvořeny tak, aby propojily záznamy v entitách, které se účastní toku odeslání nebo schválení, pomocí entit původu transakce a připojení transakce.  

### <a name="delegate-time-and-expense-entry"></a>Delegování časových a výdajových položek
Platforma Common Data Service nepodporuje zosobnění jednoho uživatele druhým, což znamená, že v aplikaci Project Service Automation verze 3 neexistuje podpora pro delegované časové a výdajové položky. Partneři a zákazníci však mohou využít řešení, které umožní podporu pro prostředí s delegovaným časovým záznamem ve verzi 3. Jedná se pouze o zástupné řešení, nikoli o úplné řešení, takže je důležité chápat omezení a použít tento přístup pouze v případě, že jsou tato omezení přijatelná. 

> [!IMPORTANT]
> Tyto informace by měly být považovány pouze za doporučené pokyny pro vlastní implementaci ze strany partnera/zákazníka. Produktový tým nebude nabízet formální podporu pro tuto funkci prostřednictvím žádného z našich kanálů podpory.

### <a name="customization-details"></a>Podrobnosti vlastního nastavení 
Vlastní nastavení umožňuje přidat **Rezervovatelný zdroj** do prostředí pro vytváření a úpravy, což uživateli umožní vystupovat jako delegát změnou pole **Rezervace zdroje** na jiného uživatele, pro kterého je třeba zaznamenat časové a výdajové položky. Následující kroky se týkají delegování časového záznamu. Stejné informace platí pro delegování výdajové položky. 
 
1.  Zajistěte, aby měl delegovaný uživatel globální přístup zabezpečení pro projekty a projektové úkoly. 
1.  Protože **Rezervovatelný zdroj**, což je pole v entitě **Časový záznam**, není na stránce **Vytvořit** uveden, je třeba jej přidat.

    nebo

    Vytvořte vlastní zobrazení, které obsahuje sloupec **Rezervovatelný zdroj**, chcete-li zobrazovat pouze časové záznamy, které jsou pro daný zdroj vytvořeny. Publikujte vlastní nastavení v návrháři modulu aplikace pro toto zobrazení, které se zobrazí pod **výběrem zobrazení** na stránce **Časové záznamy**. Existují dva moduly plug-in, které zpracovávají nastavení manažera pro časové záznamy mimo projekt:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Vytvořte nový modul plug-in, který přepíše pole **Manažer** na manažera uživatele přiřazeného v poli **Rezervovatelný zdroj**. Použijte stejnou **fázi provádění** jako samostatný (OOB) modul plug-in (předběžné ověření) a použijte **pořadí provádění** vyšší než moduly plug-in OOB (větší než 1). Tím zajistíte, že vlastní modul plug-in bude spuštěn po modulech plug-in OOB.  
 
### <a name="end-user-experience"></a>Prostředí koncového uživatele
1.  Když na stránce pro vytvoření vytvoříte časový záznam, zadejte podrobnosti projektu a projektového úkolu a pak vyberte uživatele v poli **Rezervovatelný zdroj**, pro který je nutné zaznamenat časový záznam. 
2.  Ve výchozím nastavení je toto pole přihlášeným uživatelem, avšak vzhledem k tomu, že uživatel toto pole přepsal, bude nyní vytvořen časový záznam pro zvolený **Rezervovatelný zdroj**.
3.  Když odešlete časové záznamy, které jste vytvořili pro tyto záznamy, budou zařazeny do fronty pro schvalovatele v projektu očekávaným způsobem. 
4.  Když odvoláte časové záznamy vytvořené pro jiného uživatele, budou vráceny do stavu **Koncept** s polem **Rezervovatelný zdroj** nastaveným na jiného uživatele. 
5.  Volitelně můžete přepnout na vlastní zobrazení a filtrovat časové záznamy vytvořené pro jiného uživatele. 
 
### <a name="limitations"></a>Omezení
Funkce **Kopírovat** a **Importovat** funguje pouze v kontextu přihlášeného uživatele. To znamená, že není možné kopírovat nebo importovat časové záznamy, které byly vytvořeny pro uživatele, který je přihlášen jako rezervovatelný zdroj.

Časové záznamy, které nejsou určeny pro projekt, budou směrovány ke schválení manažerovi rezervovatelného zdroje, pouze pokud byl dokončen krok 4 v části **Podrobnosti vlastního nastavení**. V opačném případě budou časové záznamy mimo projekt pro jiného uživatele nesprávně směrovány manažerovi přihlášeného uživatele. 

### <a name="other-changes"></a>Další změny 
Funkce **Rezervace a úkoly** byla odebrána. 

## <a name="multidimensional-pricing"></a>Multidimenzionální ceny
Pro maximalizaci flexibility a splnění různých obchodních požadavků podporuje verze 3 aplikace Project Service Automation samostatné použití sad cenových dimenzí na nákladové a fakturační sazby. Hodnoty dimenzí lze nastavit jako výchozí a poté je šířit v průběhu výpočtu nákladů a cen od profilování zdrojů až po zadání času do skutečností projektu. Konfigurace a úprava nebo rozšířené specifické pro zákazníka využívají standardní infrastrukturu přizpůsobení.

Aplikace Project Service Automation je dodávána s výchozí sadou cenových dimenzí a rolí a jednotek zdrojů a umožňuje nastavení cen a nákladů pro každou kombinaci role a organizační jednotky.

Pro zákazníky aplikace Project Service Automation, kteří chtějí nadále používat tato předem připravená pole jako cenové dimenze ve verzi 3, neproběhnou žádné zjistitelné změny. Službu Project Service Automation můžete nadále používat obvyklým způsobem. Pokud však potřebujete určit cenu nebo náklady pro zdroje pomocí jiných dalších atributů, verze 3 umožňuje přidat do aplikace Project Service Automation vlastní cenové dimenze. Rozšíření vlastních cenových dimenzí je složitá akce konfigurace. 

## <a name="quotes-and-contracts"></a>Nabídky a smlouvy
Ve verzi 3 aplikace Project Service Automation se změnily aspekty nastavení a správy pro nabídky a smlouvy. Podrobnější informace jsou uvedeny v následujících částech.

### <a name="set-up-chargeability-options"></a>Možnosti nastavení účtovatelnosti
Ve verzích 1 a 2 bylo provedeno nastavení možností účtovatelnosti pro role a kategorie pro konkrétní nabídky a smlouvy pomocí zobrazení **Účtovatelnost**, které bylo v horní navigační oblasti řádku nabídky nebo řádku smlouvy. Zde také můžete nastavit ceny pro tyto role a kategorie výdajů.

Od verze 3 se nastavení možností účtovatelnosti podle role a kategorie výdajů provádí na úrovni řádku nabídky nebo řádku smlouvy. Nastavení cen je oddělené od nastavení účtovatelnosti. **Účtovatelné role** a **Účtovatelné kategorie** budete moci najít jako karty na **řádku nabídky** a stránkách **řádku smlouvy** bez nutnosti použití horní navigační oblasti.

![Účtovatelné role.](media/chargeable-12.png)
 
Nastavení účtovatelných rolí a účtovatelných kategorií také využívá předem připravené ovládací prvky upravitelné mřížky. U každé role a kategorie zůstávají podporované možnosti pro typ fakturace během fáze vytvoření nabídky a smlouvy beze změny od předchozích verzí jako **Účtovatelné** a **Neúčtovatelné**. **Neplacené** není podporovaný typ během fáze vytvoření nabídky nebo smlouvy. **Bezplatné** je podporovaný typ pouze během schválení času nebo výdajů.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Vytvoření a úprava vlastních cen pro nabídku a projektovou smlouvu Project Service Automation
Ve verzích 1 a 2 bylo použití vlastního ceníku pro specifické nabídky a smlouvy provedeno pomocí funkce **Upravit ceny** v zobrazení **Účtovatelnost**. Zobrazení **Účtovatelnost** bylo umístěno v horní navigační oblasti řádku nabídky nebo řádku smlouvy. Zde také bylo možné nastavit možnosti účtovatelnosti pro role nebo kategorie výdajů.

Od verze 3 bylo vytvoření a použití vlastního ceníku projektu v nabídce a projektové smlouvě Project Service Automation odděleno od nastavení účtovatelnosti. Nabídka a projektové smlouvy Project Service Automation mají novou záložku nazvanou **Projektové ceníky**. Na této kartě se zobrazí přidružené zobrazení všech projektových ceníků, které jsou připojeny k nabídce nebo projektové smlouvě Project Service Automation. Chcete-li vytvořit vlastní ceník z existujícího ceníku, který je již přidružen k nabídce nebo smlouvě projektu, klikněte na možnost **Vytvořit vlastní ceny**. Tím vytvoříte kopii všech přidružených ceníků a připojíte je k nabídce nebo ke smlouvě. Nyní můžete otevřít ceník a upravit cenu role nebo kategorie výdajů tak, aby se tyto změny cen projevily pouze u této nabídky nebo smlouvy. 
  
Následující obrázek je ze chvíle před vytvořením vlastních ceníků.

![Před vlastními ceníky.](media/before-custom-price-lists-13.png)

Následující obrázek je ze chvíle po vytvoření vlastních ceníků.

![Po vlastních cenících.](media/after-custom-price-lists-14.png)

> [!NOTE]
> Může dojít ke krátké prodlevě mezi kliknutím na tlačítko **Vytvořit vlastní ceny** a vytvořením vlastního ceníku. Místo opakovaného kliknutí doporučujeme aktualizovat mřížku. Vlastní ceník byl vytvořen v případě, že název přidruženého ceníku má připojen název nabídky nebo název smlouvy o projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]