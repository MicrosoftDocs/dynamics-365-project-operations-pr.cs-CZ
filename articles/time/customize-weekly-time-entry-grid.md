---
title: Rozšíření časových záznamů
description: Tento téma poskytuje informace o tom, jak jsou vývojáři schopni rozšířit řízení časových záznamů.
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d9c14f0550d4429ac794607a3fb61717566207e4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124630"
---
# <a name="extending-time-entries"></a>Rozšíření časových záznamů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations zahrnuje rozšiřitelný vlastní ovládací prvek pro časové záznamy. Tento ovládací prvek obsahuje následující funkce:

- Zadávání času horizontálně přes týden
- Součty za den, řádek nebo týden
- Kopírování řádků nebo týdnů
- Zadání času prostřednictvím HH: mm nebo HH.hh (automaticky se převede na HH.hh)
- Importujte z úkolů, rezervací nebo schůzek

Prodloužení časových záznamů je možné ve dvou oblastech:
- [Přidejte vlastní časové záznamy pro vlastní potřebu](#add)
- [Přizpůsobení týdenního ovládacího prvku časových záznamů](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Přidejte vlastní časové záznamy pro vlastní potřebu

Časové položky jsou základní entitou používanou ve více scénářích. V dubnové vlně 1 2020 bylo představeno základní řešení TESA. TESA poskytuje a entitu **Nastavení** a novou roli zabezpečení **Uživatel zadání času**. Nová pole **msdyn_start** a **msdyn_end**, které mají přímý vztah k **msdyn_duration**, byly také zahrnuty. Nová entita role zabezpečení a pole umožňují jednotnější přístup k času napříč více produkty.


### <a name="time-source-entity"></a>Entita časového zdroje
| Pole | Popis | 
|-------|------------|
| Jméno  | Název záznamu Časový zdroj použitý jako hodnota výběru během vytváření časových položek. |
| Výchozí časový zdroj [Časový zdron: isdefault] | Ve výchozím nastavení může být u výchozího zdroje času označen pouze jeden zdroj času. To umožňuje, aby položky měly výchozí zdroj času, pokud není zadán. |
|Typ zdroje času [Zdroj času: sourcetype] | Typ zdroje je možnost (Typ zdroje časového záznamu), která umožňuje přidružení zdroje času k aplikaci. Společnost Microsoft si vyhrazuje hodnoty vyšší než 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Časové záznamy a entita zdroje času
Každý časový záznam je přidružen k záznamu zdroje času. Tento záznam určuje, jak a které aplikace by měly zpracovat časový záznam.

Časové záznamy jsou vždy jeden souvislý časový blok s propojeným začátkem, koncem a dobou trvání.

Logika automaticky aktualizuje záznam zadání času v následujících situacích:

- Pokud jsou k dispozici dvě ze tří následujících polí, automaticky se vypočítá třetí: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Pole **msdyn_start** a **msdyn_end** berou v potaz časové pásmo.
- Časové položky vytvořené pouze se zadanými hodnotami **msdyn_date** a **msdyn_duration** začnou o půlnoci. Pole **msdyn_start** a **msdyn_end** se odpovídajícím způsobem aktualizují.

#### <a name="time-entry-types"></a>Typy časových záznamů

Časové záznamy mají přidružený typ, který definuje chování v toku odesílání pro přidruženou aplikaci.

|Štítek | Hodnota|
|-----|-----|
|Přestávka   |192,355,000|
|Cesta | 192,355,001|
|Přesčas   | 192,354,320|
|Práce   | 192,350,000|
|Absence    | 192,350,001|
|Dovolená   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Přizpůsobení týdenního ovládacího prvku časových záznamů
Vývojáři mohou přidat další pole a vyhledávání do dalších entit a implementovat vlastní obchodní pravidla pro podporu svých obchodních scénářů.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Přidání vlastních polí s vyhledáváním do jiných entit
Přidání vlastního pole do mřížky týdenního zadávání času zahrnuje tři hlavní kroky.

1. Přidejte vlastní pole do dialogového okna pro vytvoření záznamu.
2. Nakonfigurujte mřížku pro zobrazení vlastního pole.
3. Přidejte vlastní pole do toku úkolu pro úpravu řádku nebo do toku úkolu pro úpravu buňky.

Zajistěte, aby nové pole mělo požadovaná ověření v toku úlohy pro úpravu řádku nebo buňky. V rámci tohoto kroku je nutné pole uzamknout na základě stavu časového záznamu.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Přidání vlastní pole do dialogového okna pro vytvoření záznamu
Přidejte vlastní pole přidat do dialogového okna **Rychlé vytvoření časového záznamu**. Pak je možné zadat hodnotu při přidání časových údajů výběrem **Nový**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurace mřížky pro zobrazení vlastního pole
Vlastní pole lze do mřížky týdenního zadávání času zadat dvěma způsoby:

  - Přizpůsobte zobrazení a přidejte vlastní pole
  - Vytvoření nového výchozího časového záznamu 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Přizpůsobte zobrazení a přidejte vlastní pole

Můžete přizpůsobit zobrazení **Moje týdenní časové záznamy** a přidat do něj vlastní pole. Můžete zvolit umístění a velikost vlastního pole v mřížce úpravou těchto vlastností v zobrazení.

#### <a name="create-a-new-default-custom-time-entry"></a>Vytvoření nového výchozího časového záznamu

Toto zobrazení by mělo obsahovat kromě sloupců, které mají být v mřížce, také pole **Popis** a **Externí komentáře**. 

1. Vyberte umístění, velikost a výchozí pořadí řazení v mřížce úpravou těchto vlastností v zobrazení. 
2. Nakonfigurujte vlastní ovládací prvek pro toto zobrazení tak, aby se jednalo o ovládací prvek **Mřížka časových záznamů**. 
3. Přidejte tento ovládací prvek do zobrazení a vyberte jej pro web, telefon a tablet. 
4. Nakonfigurujte parametry pro tabulku týdenního zadávání času. 
5. Nastavte pole **Počáteční datum** na **msdyn_date**, pole **Doba trvání** na **msdyn_duration** a pole **Stav** na **msdyn_entrystatus**. 
6. Pro výchozí zobrazení je pole **Seznam stavů jen pro čtení** pole je nastaveno na **192350002,192350003,192350004**. Pole **Průběh úlohy úpravy řádku** je nastaveno na **msdyn_timeentryrowedit**. Pole **Průběh úlohy úpravy buňky** je nastaveno na **msdyn_timeentryedit**. 
7. Tato pole můžete upravit a přidat nebo odebrat stav jen ke čtení nebo použít jiné prostředí založené na úlohách (TBX) pro úpravy řádků nebo buněk. Tato pole jsou nyní vázána na statickou hodnotu.


> [!NOTE] 
> Obě možnosti odstraní některé připravené filtry pro entity **Projekt** a **Projektový úkol**, takže všechna zobrazení vyhledávání entit budou viditelná. Viditelná jsou pouze připravená příslušná zobrazení vyhledávání.

Určete příslušný tok úlohy pro vlastní pole. Pokud jste pole přidali do mřížky, mělo by přejít do toku úlohy úprav řádku, který se používá pro pole, která se vztahují na celý řádek časových záznamů. Má-li vlastní pole jedinečnou hodnotu každý den, například vlastní pole pro **Koncový čas**, mělo by přejít do toku úlohy úprav buňky.

Chcete-li přidat vlastní pole do toku úlohy, přetáhněte prvek **Pole** na příslušné místo na stránce a nastavte vlastnosti pole. Nastavte vlastnost **Zdroj** na možnost **Časový záznam** a vlastnost **Datové pole** na vlastní pole. Vlastnost **Pole** určuje zobrazovaný název na stránce TBX. Vyberte **Použít** a uložte změny do pole a poté vyberte **Aktualizovat** pro uložení změn na stránku.

Chcete-li místo toho použít novou vlastní stránku TBX, vytvořte nový proces. Nastavte kategorii na **Tok obchodního procesu**, entitu na **Časový záznam** a typ obchodního procesu na **Spustit proces jako tok úlohy**. V části **Vlastnosti** by měla být vlastnost **Název stránky** nastavena na zobrazovaný název stránky. Přidejte všechna příslušná pole na stránku TBX. Proces uložte a aktivujte. Aktualizujte vlastnost vlastního ovládacího prvku pro příslušný tok úlohy na hodnotu **Název** v procesu.

### <a name="add-new-option-set-values"></a>Přidání nových hodnot sady možností
Chcete-li přidat hodnoty sady možností do připraveného pole, otevřete stránku pro úpravy pole a potom v části **Typ** vyberte možnost **Upravit** vedle sady možností. Přidejte novou možnost, která má vlastní popisek a barvu. Chcete-li přidat nový stav časového záznamu, bude připravené pole pojmenováno **Stav záznamu**, nikoli **Stav**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Určení nového stavu časového záznamu jako jen ke čtení
Chcete-li určit nový stav časového záznamu jako jen ke čtení, přidejte novou hodnotu časového záznamu do vlastnosti **Seznam stavů jen pro čtení**. Upravitelná část mřížky pro zadávání času bude uzamčena pro řádky, které mají nový stav.
Dále přidejte obchodní pravidla pro uzamknutí všech polí na stránkách TBX **Úprava řádku časového záznamu** a **Úprava časového záznamu**. K obchodním pravidlům pro tyto stránky můžete přejít otevřením editoru toku obchodního procesu pro stránku a následným výběrem možnosti **Obchodní pravidla**. Nový stav můžete přidat do podmínky ve stávajících obchodních pravidlech nebo můžete přidat nové obchodní pravidlo pro nový stav.

### <a name="add-custom-validation-rules"></a>Přidávání vlastních ověřovacích pravidel
Existují dva typy pravidel ověření, které můžete přidat pro týdenní mřížku pro zadávání času:

- Obchodní pravidla na straně klienta, která fungují v dialogových oknech pro rychlé vytvoření a na stránkách TBX.
- Ověření plug-inů na straně serveru, které se vztahují na všechny aktualizace časových vstupů.

#### <a name="business-rules"></a>Obchodní pravidla
Pomocí obchodních pravidel můžete zamknout a odemknout pole, zadat výchozí hodnoty do polí a definovat ověření, která vyžadují informace pouze z aktuálního záznamu o zadání času. K obchodním pravidlům pro stránku TBX můžete přejít otevřením editoru toku obchodního procesu pro stránku a následným výběrem možnosti **Obchodní pravidla**. Poté můžete upravit existující obchodní pravidla nebo přidat nové obchodní pravidlo. Pro ještě více přizpůsobené ověřování můžete použít obchodní pravidlo pro spuštění JavaScriptu.

#### <a name="plug-in-validations"></a>Ověření modulů plug-in
Ověření modulu plug-in použijte pro jakákoli ověření vyžadující více kontextu, než jaký je k dispozici v jediném časovém záznamu, nebo pro jakákoli ověření, která chcete spustit v aktualizacích na řádku v mřížce. Chcete-li dokončit ověřování, vytvořte v entitě **Časový záznam** vlastní modul plug-in.

### <a name="copying-time-entries"></a>Kopírování časových záznamů
Použijte pohled **Kopírování sloupců pro zadání času** k definování seznamu polí ke kopírování během zadávání času. **Datum** a **Doba trvání** jsou povinná pole a nesmí být ze zobrazení odstraněna.


[!INCLUDE[footer-include](../includes/footer-banner.md)]