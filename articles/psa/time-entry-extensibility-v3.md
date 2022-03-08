---
title: Přizpůsobení týdenních časových záznamů
description: Toto téma obsahuje informace o způsobu implementace vlastních obchodních pravidel, která podporují postupy organizace.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
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
ms.openlocfilehash: fa2ef927e0234919ee4777f24c60569fb33a8570f6d48be6aef356df4f08a6e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002278"
---
# <a name="customize-weekly-time-entry"></a>Přizpůsobení týdenních časových záznamů 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V aplikaci Microsoft Dynamics 365 Project Service Automation verze 3.3 společnost Microsoft zavedla moderní mřížku, která projektovým zdrojům umožňuje rychle zadávat čas současně až pro jeden týden. Nový mřížka pro týdenní zadávání času může zobrazovat součty položek podle data, řádku nebo týdne. Zdroje mohou vytvářet kopie časových záznamů během týdne a také hromadně kopírovat z předchozích týdnů. Úpravci systému mohou přizpůsobit zobrazení přidáním polí, přidáním vyhledávání do jiných entit a implementací vlastních obchodních pravidel pro podporu postupů jejich organizace.

K zadání času a nové týdenní časové mřížce se přistupuje prostřednictvím mapy webu. Nerozšiřitelné vlastní prostřední pro zadávání času, které bylo součástí dřívějších verzí PSA, bylo nahrazeno rozšiřitelnou mřížkou týdenního zadávání času a také alternativním prostředím v mřížce a kalendáři jen ke čtení. Z důvodu této změny mohou uživatelé zadávat čas v týdenních množstvích.

## <a name="page-layout"></a>Rozložení stránky
Nová mřížka pro týdenní zadávání času je vlastní ovládací prvek, který obsahuje panel nástrojů a dvě hlavní části **Dimenze** a **Doba trvání**. Panel nástrojů obsahuje tlačítko, které je použitelné pouze pro tento vlastní ovládací prvek pro mřížku zadávání času. Naproti tomu tlačítka v podokně akcí v horní části stránky jsou použitelná na tři typy ovládacích prvků, které jsou podporovány pro zadávání času: ovládací prvek týdenního zadávání času, ovládací prvek jen ke čtení a ovládací prvek kalendáře.

### <a name="dimensions"></a>Dimenze
Část **Dimenze** znázorňuje všechny dimenze, pro které lze zadat čas, jako hlavičky sloupců. Následující dimenze jsou podporovány ve výchozím nastavení:

- Projekt
- Projektový úkol
- Role
- Typ
- Stav záznamu

Část **Dimenze** neumožňuje úpravy na řádku. Tato část je podložena zobrazením, které umožňuje přidat vlastní pole do mřížky pro týdenní zadávání času. Informace o přidávání vlastních polí naleznete dále v tomto tématu v části „Rozšiřitelnost“.

### <a name="duration"></a>Doba trvání
Část Doba trvání zobrazuje dny v týdnu jako záhlaví sloupců. Tato část umožňuje úpravy na řádku. Po vytvoření časového záznamu, který má odpovídající dimenze, mohou uživatelé rychle zadat na řádku množství času stráveného v těchto dimenzích.

## <a name="create-a-new-time-entry"></a>Vytvoření nového časového záznamu
Chcete-li v mřížce zadávání času vytvořit nový časový záznam, vyberte možnost **Nový**. Zobrazí se dialogové okno **Rychlé vytvoření časového záznamu**. V tomto dialogovém okně mohou uživatelé vybrat datum časového záznamu a poté zadat data pro dimenze **Projekt**, **Úkol**, **Role** a **Doba trvání** v minutách, hodinách nebo dnech zadáním písmene **h**, **m** nebo **d** spolu s číslem. Uživatelé mohou pro časový záznam zadat také popis a komentáře, které lze externě sdílet. Jakmile uživatelé uloží změny, zobrazí se hodnoty zadané pro dimenze v části **Dimenze**. Informace o době trvání zadané do pole **Doba trvání** se zobrazí k datu, pro které byl časový záznam vytvořen.

Vyhledávací pole jsou zálohována systémovými zobrazeními. Například poté, co uživatel zadá projekt, bude pole **Projektový úkol** ve výchozím nastavení nastaveno na zobrazení **Kopie**. Chcete-li vytvořit časové záznamy pro úkoly, které nejsou přiřazeny uživateli, vyberte možnost **Změnit zobrazení** v dialogovém okně vyhledávání a pak vyberte zobrazení **Všechny aktivní projektové úkoly**.

## <a name="edit-a-time-entry"></a>Úprava časového záznamu
Podrobnosti z některých polí na stránce zadávání času, například **Popis** a **Externí komentáře**, nejsou zobrazeny v mřížce týdenního zadávání času. Místo toho se v buňkách doby trvání, které mají tyto další podrobnosti, zobrazí malý trojúhelníkový ukazatel. Vyberte buňku a potom výběrem možnosti **Upravit podrobnosti** zobrazte data v podokně **Rychlá úprava**. Chcete-li upravit nebo aktualizovat podrobnosti pro konkrétní časový záznam, který není součástí mřížky týdenního zadávání času, musí uživatelé otevřít podokno **Rychlá úprava**.

## <a name="copy-a-time-entry-row"></a>Kopírování řádku časového záznamu
Po vytvoření prvního řádku pro zadání času mohou uživatelé vybrat možnost **Kopírovat řádek** a zkopírovat celý řádek do nového řádku. Po zkopírování řádku tímto způsobem budou zkopírovány také dimenze a doby trvání. Uživatelé mohou také vybrat možnost **Upravit řádek** a aktualizovat hodnoty dimenzí a dob trvání na řádku v části **Doba trvání**.

## <a name="open-a-time-entry"></a>Otevření časového záznamu
Pro podporu optimálního a rychlého zadávání do nejvýraznějších polí se v mřížce týdenního zadávání času zobrazuje podmnožina vybraných dimenzí a dob trvání. Chcete-li zobrazit všechny podrobnosti o jednom časovém záznamu, v části **Upravit záznam** vyberte možnost **Otevřít**.

## <a name="submit-a-time-entry"></a>Odeslání časového záznamu
Uživatelé mohou odeslat jeden časový záznam nebo skupinu časových záznamů výběrem bloku buněk nebo celého řádku časového záznamu a následným výběrem příkazu **Odeslat**. Odeslané časové záznamy se zobrazí jako položky čekající na schválení na stránce **Schválení** schvalovatelů. Po úspěšném odeslání časových záznamů je nelze upravit.

## <a name="recall-a-time-entry"></a>Odvolání časového záznamu
Časové záznamy, které jste odeslali, můžete odvolat. Můžete odvolat jeden časový záznam, blok časových záznamů nebo celý řádek časových záznamů. Zdroje mohou odvolané časové záznamy upravovat.

## <a name="time-entry-status"></a>Stav časového záznamu
Novým časovým záznamům je automaticky přiřazen stav **Koncept**. Po odeslání časového záznamu je stav aktualizován na **Odesláno**. Po schválení časového záznamu je stav aktualizován na **Schváleno**. Pokud je časový záznam zamítnut, bude jeho stav aktualizován na **Vráceno** a záznam bude dostupný pro opravu a opětovné odeslání. Odstranit lze pouze časové záznamy, které mají stav **Koncept**.

## <a name="view-rejection-comments"></a>Zobrazení komentářů k zamítnutí
Pokud je časový záznam zamítnut schvalovatelem, může schvalovatel přidat komentáře k zamítnutí, které pomohou zdroji porozumět důvodu zamítnutí. Chcete-li zobrazit komentáře k zamítnutí časového záznamu, vyberte možnost **Otevřít záznam**. Komentáře k zamítnutí budou zobrazeny na časové ose. Na časové ose může zdroj odpovědět na komentáře k zamítnutí dříve, než záznam znovu odešle.

## <a name="copy-week"></a>Kopírovat týden
Po vytvoření několika časových záznamů mohou uživatelé vybrat možnost **Kopírovat týden** pro hromadné vytvoření dalších časových záznamů. Zobrazí se dialogové okno **Kopírovat**. V části **Od období** použijte pole **Počáteční datum** a **Koncové datum** k definování rozsahu dat, ze kterého budou zkopírovány časové záznamy. V části **Do období** v poli **Počáteční datum** zadejte datum, pro které chcete vytvořit časové záznamy. Poté vyberte položku **Kopírovat**. Pro zadané datum v období „Do“ se vytvoří kopie časových záznamů pro odpovídající den v týdnu v období „Od“. Například pondělní časový záznam z minulého týdne bude zkopírován do pondělí týdne, který je zadán jako období „Do“.

## <a name="import"></a>Import
Stejný základní postup se používá k importu z rezervací, přiřazení a výměn. Uživatelé mohou určit rozsah dat, ze kterého budou rezervace importovány. Pak musí explicitně vybrat rezervace, které by měly být zkopírovány do časových záznamů ve stavu Koncept. V předchozí verzi se navrhované časové záznamy objevily v mřížce a v kalendáři a po aktualizace relace byly ztraceny.

## <a name="extensibility"></a>Rozšiřitelnost
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Přidání vlastních polí s vyhledáváním do jiných entit
Přidání vlastního pole do mřížky týdenního zadávání času zahrnuje tři hlavní kroky.

1.  Přidejte vlastní pole do dialogového okna pro vytvoření záznamu.
2.  Nakonfigurujte mřížku pro zobrazení vlastního pole.
3.  Podle potřeby přidejte vlastní pole do toku úkolu pro úpravu řádku nebo do toku úkolu pro úpravu buňky.

Je také nutné zajistit, aby nové pole mělo požadovaná ověření v toku úlohy pro úpravu řádku nebo buňky. V rámci tohoto kroku je nutné pole uzamknout na základě stavu časového záznamu.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Přidání vlastní pole do dialogového okna pro vytvoření záznamu
Vlastní pole je nutné přidat do dialogového okna Rychlé vytvoření časového záznamu, aby uživatelé mohli zadat hodnotu, když přidávají časové záznamy pomocí tlačítka **Nový**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurace mřížky pro zobrazení vlastního pole
Vlastní pole lze do mřížky týdenního zadávání času zadat dvěma způsoby. První možností je přizpůsobit zobrazení **Moje týdenní časové záznamy** a přidat do něj vlastní pole. Můžete zvolit umístění a velikost vlastního pole v mřížce úpravou těchto vlastností v zobrazení.

Druhou možností je vytvořit nové vlastní zobrazení časového záznamu a nastavit je jako výchozí zobrazení. Toto zobrazení by mělo obsahovat kromě sloupců, které mají být v mřížce, také pole **Popis** a **Externí komentáře**. Můžete zvolit umístění, velikost a výchozí pořadí řazení v mřížce úpravou těchto vlastností v zobrazení. Dále nakonfigurujte vlastní ovládací prvek pro toto zobrazení tak, aby se jednalo o ovládací prvek **Mřížka časových záznamů**. Přidejte tento ovládací prvek do zobrazení a vyberte jej pro web, telefon a tablet. Dále nakonfigurujte parametry pro tabulku týdenního zadávání času. Nastavte pole **Počáteční datum** na **msdyn_date**, pole **Doba trvání** na **msdyn_duration** a pole **Stav** na **msdyn_entrystatus**. U výchozího zobrazení je pole **Seznam stavů jen pro čtení** nastaveno na hodnotu **192350002,192350003,192350004**, pole **Tok úlohy úpravy řádku** na hodnotu **msdyn_timeentryrowedit** a pole **Tok úlohy úpravy buňky** na hodnotu **msdyn_timeentryedit**. Tato pole můžete upravit a přidat nebo odebrat stav jen ke čtení nebo použít jiné prostředí založené na úlohách (TBX) pro úpravy řádků nebo buněk. Tato pole by měla být vázána na statickou hodnotu.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Přidání vlastního pole do příslušného toku úlohy úprav
Stránky TBX, které se používají pro úpravy, lze nalézt v části **Procesy**. Výchozí stránky jsou **Project Service – Úprava řádku časového záznamu** a **Project Service – Úprava časového záznamu**. Můžete buď upravit tyto výchozí stránky nebo vytvořit nové vlastní stránky TBX.

> [!NOTE] 
> Obě možnosti odstraní některé připravené filtry pro entity **Projekt** a **Projektový úkol**, takže všechna zobrazení vyhledávání entit budou viditelná. Viditelná jsou pouze připravená příslušná zobrazení vyhledávání.

Je nutné určit příslušný tok úlohy pro vlastní pole. Pokud jste pole přidali do mřížky, mělo by přejít do toku úlohy úprav řádku, který se používá pro pole, která se vztahují na celý řádek časových záznamů. Má-li vlastní pole jedinečnou hodnotu každý den, například vlastní pole pro **Koncový čas**, mělo by přejít do toku úlohy úprav buňky.

Chcete-li přidat vlastní pole do toku úlohy, přetáhněte prvek **Pole** na příslušné místo na stránce a nastavte jeho vlastnosti. Nastavte vlastnost **Zdroj** na možnost **Časový záznam** a vlastnost **Datové pole** na vlastní pole. Vlastnost **Pole** určuje zobrazovaný název na stránce TBX. Výběrem možnosti **Použít** uložte změny pole. Poté výběrem možnosti **Aktualizovat** uložte změny na stránce.

Chcete-li místo toho použít novou vlastní stránku TBX, vytvořte nový proces. Nastavte kategorii na **Tok obchodního procesu**, entitu na **Časový záznam** a typ obchodního procesu na **Spustit proces jako tok úlohy**. V části **Vlastnosti** by měla být vlastnost **Název stránky** nastavena na zobrazovaný název stránky. Přidejte všechna příslušná pole na stránku TBX. Uložte a aktivujte proces a potom aktualizujte vlastnost vlastního ovládacího prvku pro příslušný tok úlohy na hodnotu **Název** v procesu.

### <a name="add-new-option-set-values"></a>Přidání nových hodnot sady možností
Chcete-li přidat hodnoty sady možností do připraveného pole, otevřete stránku pro úpravy pole a potom v části **Typ** vyberte možnost **Upravit** vedle sady možností. Dále přidejte novou možnost, která má vlastní popisek a barvu. Chcete-li přidat nový stav časového záznamu, bude připravené pole pojmenováno **Stav záznamu**, nikoli **Stav**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Určení nového stavu časového záznamu jako jen ke čtení
Chcete-li určit nový stav časového záznamu jako jen ke čtení, přidejte novou hodnotu časového záznamu (číslo, nikoli popisek) do vlastnosti **Seznam stavů jen pro čtení**. Upravitelná část mřížky pro zadávání času bude uzamčena pro řádky, které mají nový stav.
Dále přidejte obchodní pravidla pro uzamknutí všech polí na stránkách TBX **Úprava řádku časového záznamu** a **Úprava časového záznamu**. K obchodním pravidlům pro tyto stránky můžete přejít otevřením editoru toku obchodního procesu pro stránku a následným výběrem možnosti **Obchodní pravidla**. Nový stav můžete přidat do podmínky ve stávajících obchodních pravidlech nebo můžete přidat nové obchodní pravidlo pro nový stav.

### <a name="add-custom-validation-rules"></a>Přidávání vlastních ověřovacích pravidel
Existují dva typy ověřovacích pravidel, která lze přidat pro mřížku týdenního zadávání času: • Obchodní pravidla na straně klienta, která fungují v dialogových oknech pro rychlé vytváření a na stránkách TBX • Ověření modulu plug-in na straně serveru, která se vztahují na všechny aktualizace časových záznamů

#### <a name="business-rules"></a>Obchodní pravidla
Pomocí obchodních pravidel můžete zamknout a odemknout pole, zadat výchozí hodnoty do polí a definovat ověření, která vyžadují informace pouze z aktuálního záznamu o zadání času. K obchodním pravidlům pro stránku TBX můžete přejít otevřením editoru toku obchodního procesu pro stránku a následným výběrem možnosti **Obchodní pravidla**. Poté můžete upravit existující obchodní pravidla nebo přidat nové obchodní pravidlo. Pro ještě více přizpůsobené ověřování můžete použít obchodní pravidlo pro spuštění JavaScriptu.

#### <a name="plug-in-validations"></a>Ověření modulů plug-in
Ověření modulu plug-in byste měli použít pro jakákoli ověření vyžadující více kontextu, než jaký je k dispozici v jediném časovém záznamu, nebo pro jakákoli ověření, která chcete spustit v aktualizacích na řádku v mřížce. Chcete-li dokončit ověřování, vytvořte v entitě **Časový záznam** vlastní modul plug-in.

> [!IMPORTANT] 
> V současné době je známý problém na stránkách TBX, který uživatelům brání v opravě informací a opětovném výběru položky Hotovo v případě, že aktualizace selže při ověřování modulu plug-in. Tento problém odstraníte, pokud nastavíte ověřování obchodních pravidel tak, aby této situaci v maximální možné míře zabránilo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]