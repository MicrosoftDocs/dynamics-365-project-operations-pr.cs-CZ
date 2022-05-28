---
title: Rozšíření časových záznamů
description: Tento téma poskytuje informace o tom, jak jsou vývojáři schopni rozšířit řízení časových záznamů.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582978"
---
# <a name="extending-time-entries"></a>Rozšíření časových záznamů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations obsahuje rozšiřitelný vlastní vstupní ovládací prvek. Tento ovládací prvek obsahuje následující funkce:

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
Každý časový záznam je přidružen k záznamu zdroje času. Tento záznam určuje, které aplikace by měly zpracovat zadání času a jak.

Časové záznamy jsou vždy jeden souvislý časový blok s propojeným začátkem, koncem a dobou trvání.

Logika automaticky aktualizuje záznam zadání času v následujících situacích:

- Pokud jsou k dispozici dvě ze tří následujících polí, automaticky se vypočítá třetí: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Pole **msdyn_start** a **msdyn_end** berou ohled na časové pásmo.
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

1. Přidejte vlastní pole do dialogového okna **Rychlé vytvoření**.
2. Nakonfigurujte mřížku pro zobrazení vlastního pole.
3. Přidejte vlastní pole do stránky **Úprava řádku** nebo **Úprava časového záznamu** podle potřeby.

Zajistěte, aby nové pole mělo požadovaná ověření na stránce **Úprava řádku** nebo **Úprava časového záznamu**. V rámci tohoto úkolu uzamkněte pole na základě stavu časového záznamu.

Když přidáte vlastní pole do mřížky **Zadání času** a poté vytvoříte časové položky přímo v mřížce, vlastní pole pro tyto položky se automaticky nastaví tak, aby odpovídalo řádku. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Přidání vlastního pole do dialogového okna Rychlé vytvoření
Přidejte vlastní pole do dialogového okna **Rychlé vytvoření: Vytvoření časového záznamu**. Uživatelé pak mohou zadat hodnotu, když přidají časové údaje výběrem **Nový**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurace mřížky pro zobrazení vlastního pole
Vlastní pole lze do mřížky **Týdenní časový záznam** zadat dvěma způsoby.

- Můžete přizpůsobit zobrazení **Moje týdenní časové záznamy** a přidat do něj vlastní pole. Můžete určit umístění a velikost vlastního pole v mřížce úpravou vlastností v zobrazení.
- Vytvořte nové vlastní zobrazení časového záznamu a nastavte je jako výchozí zobrazení. Toto zobrazení by mělo obsahovat kromě sloupců, které mají být v mřížce, také pole **Popis** a **Externí komentáře**. Můžete určit umístění, velikost a výchozí pořadí řazení v mřížce úpravou vlastností v zobrazení. Dále nakonfigurujte vlastní ovládací prvek pro toto zobrazení tak, aby se jednalo o ovládací prvek **Mřížka časových záznamů**. Přidejte ovládací prvek do zobrazení a vyberte jej pro **Web**, **Telefon** a **Tablet**. Dále nakonfigurujte parametry pro mřížku **Týdenní časový záznam**. Nastavte pole **Počáteční datum** na **msdyn\_date**, pole **Doba trvání** na **msdyn\_duration** a pole **Stav** na **msdyn\_entrystatus**. Pole **Seznam stavů jen ke čtení** je nastaveno na **192350002 (Schváleno)**, **192350003 (Odesláno)** nebo **192350004 (Vyžádáno odvolání)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Přidání vlastního pole do příslušné stránky úprav
Stránky, které se používají k úpravě časového záznamu nebo řady časových záznamů, naleznete v části **Formuláře**. Tlačítko **Upravit záznam** v mřížce otevře stránku **Upravit záznam** a tlačítko **Upravit řádek** otevře stránku **Úprava řádku**. Tyto stránky můžete upravit tak, aby obsahovaly vlastní pole.

Obě možnosti odstraní některé připravené filtry pro entity **Projekt** a **Projektový úkol**, takže všechna zobrazení vyhledávání entit jsou viditelná. Viditelná jsou pouze připravená příslušná zobrazení vyhledávání.

Je nutné určit příslušnou stránku pro vlastní pole. Pokud jste pole přidali do mřížky, mělo by přejít do stránky **Úprava řádku**, který se používá u polí vztahujících na celý řádek časových záznamů. Má-li vlastní pole jedinečnou hodnotu v řádku každý den (například u vlastního pole pro koncový čas), mělo by přejít na stránku **Úprava časového záznamu**.

Chcete-li přidat vlastní pole do stránky, přetáhněte prvek **Pole** na příslušné místo na stránce a nastavte jeho vlastnosti.

### <a name="add-new-option-set-values"></a>Přidání nových hodnot sady možností
Chcete-li do vestavěného pole přidat hodnoty sady možností, postupujte takto.

1. Otevřete stránku pro úpravy pole a potom v části **Typ** vyberte možnost **Upravit** vedle sady možností.
2. Přidejte novou možnost, která má vlastní popisek a barvu. Chcete-li přidat nový stav časového záznamu, bude připravené pole pojmenováno **Stav záznamu**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Určení nového stavu časového záznamu jako jen ke čtení
Chcete-li určit nový stav časového záznamu jako jen ke čtení, přidejte novou hodnotu časového záznamu do vlastnosti **Seznam stavů jen pro čtení**. Nezapomeňte přidat číslo, nikoli popisek. Upravitelná část mřížky časového záznamu bude nyní uzamčena pro řádky, které mají nový stav. Chcete-li nastavit vlastnost **Seznam stavů jen pro čtení** jinak pro různá zobrazení **Časový záznam**, přidejte mřížku **Časový záznam** v sekci **Vlastní ovládací prvky** zobrazení a konfigurujte parametry podle potřeby.

Dále přidejte obchodní pravidla pro uzamknutí všech polí na stránkách **Úprava řádku** a **Úprava časového záznamu**. K obchodním pravidlům pro tyto stránky můžete přejít otevřením editoru formuláře pro každou stránku a následným výběrem možnosti **Obchodní pravidla**. Nový stav můžete přidat do podmínky ve stávajících obchodních pravidlech nebo můžete přidat nové obchodní pravidlo pro nový stav.

### <a name="add-custom-validation-rules"></a>Přidávání vlastních ověřovacích pravidel
Do prostředí mřížky **Týdenní časový záznam** můžete přidat dva typy ověřovacích pravidel:

- Obchodní pravidla na straně klienta, která fungují na stránkách
- Ověření modulů plug-in na straně serveru, které se vztahují na všechny aktualizace časových záznamů

#### <a name="client-side-business-rules"></a>Obchodní pravidla na straně klienta
Pomocí obchodních pravidel můžete zamknout a odemknout pole, zadat výchozí hodnoty do polí a definovat ověření, která vyžadují informace pouze z aktuálního záznamu o zadání času. K obchodním pravidlům pro stránku můžete přejít otevřením editoru formuláře a následným výběrem možnosti **Obchodní pravidla**. Poté můžete upravit existující obchodní pravidla nebo přidat nové obchodní pravidlo.

#### <a name="server-side-plug-in-validations"></a>Ověření modulů plug-in na straně serveru
Ověření modulu plug-in byste měli použít pro jakákoli ověření vyžadující více kontextu, než jaký je k dispozici v jediném časovém záznamu. Měli byste je také použít pro jakákoli ověření, která chcete spustit v aktualizacích na řádku v mřížce. Chcete-li dokončit ověřování, vytvořte v entitě **Časový záznam** vlastní modul plug-in.

### <a name="limits"></a>Limity
V současné době má mřížka **Časový záznam** limit velikosti 500 řádků. Pokud existuje více než 500 řádků, přebytečné řádky se nezobrazí. Tento limit velikosti nelze nijak zvýšit.

### <a name="copying-time-entries"></a>Kopírování časových záznamů
Použijte pohled **Kopírování sloupců pro zadání času** k definování seznamu polí ke kopírování během zadávání času. **Datum** a **Doba trvání** jsou povinná pole a nesmí být ze zobrazení odstraněna.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
