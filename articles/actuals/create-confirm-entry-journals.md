---
title: Vytváření a potvrzení deníků záznamů
description: Tento článek poskytuje informace o tom, jak vytvářet a potvrzovat deníky záznamů v aplikaci Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912324"
---
# <a name="create-and-confirm-entry-journals"></a>Vytváření a potvrzení deníků záznamů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Deníky záznamů používáte k zaznamenávání skutečných hodnot přímo v aplikaci Microsoft Dynamics 365 Project Operations. Když používáte deníky záznamů, nemusíte zadávat protokoly času, výdajů a využití materiálu v Project Operations.

Jediný deník záznamů vám umožňuje vytvořit více řádků deníku. Když je deník potvrzen, řádek deníku záznamu obsahuje skutečné hodnoty pro následující podrobnosti:

- Náklady nebo výnosy v závislosti na typu transakce, který byl vybrán.
- Vybraná třída transakce. Dostupné třídy jsou **Čas**, **Výdaj**, **Materiál**, **Záloha**, **Milník** a **Daň**.
- Projekt a/nebo úkol, který je vybrán v řádku deníku.

Chcete-li vytvořit deník záznamů v Project Operations, postupujte takto.

1. Přejděte do nabídky **Prodej** \> **Transakce** \> **Deníky**.
2. Na stránce seznamu **Deníky záznamů** v podokně akcí vyberte příkaz **Nový** a vytvořte deník.
3. Na stránce **Nový deník** v poli **Popis** zadejte popis deníku.
4. Zkontrolujte, zda je pole **Typ deníku** nastaveno na **Záznam** a poté vyberte **Uložit**. Po uložení nového deníku záznamů by se na stránce deníku měla objevit karta **Řádky deníku** .
5. Na kartě **Řádky deníku** vyberte na panelu nástrojů nad mřížkou příkaz **Nový** a vytvořte řádek deníku záznamů.
6. V dialogovém okně **Rychlé vytvoření** pro vytvoření řádku deníku záznamů nastavte pole podle popisu v následující tabulce.

    | Pole | Description | Funkční dopad |
    | --- | --- | --- |
    | Třída transakce | Řádek deníku lze zařadit do jedné ze šesti tříd transakcí: **Čas**, **Výdaj**, **Materiál**, **Záloha**, **Milník** nebo **Daň**. | Transakční třída **Daň** byla v Project Operations označena jako zastaralá. <br> Pokud vytvoříte transakční třídu **Daň**, nebude zpracována fakturací ani při kalkulacích nákladů či výnosů. **Milník** je třída transakcí pouze pro výnosy. <br>Transakční třída **Záloha** představuje zálohu, která byla přijata od zákazníka. Vždy by měl být vytvořena jako dvojice řádků deníku vyúčtovaných prodejů a nevyúčtovaných prodejů. |
    | Typ transakce | Transakční třídy **Náklady**, **Mezipodnikový prodej** a **Jednotkové náklady zdroje** by se měly používat pro zaznamenávání nákladů.<br> Transakční třídy **Nevyfakturovaný prodej** a **Fakturovaný prodej** by se měly používat k evidenci výnosů. | Transakční třída **Záloha** funguje pouze s typy transakcí **Nevyfakturovaný prodej** a **Fakturovaný prodej**.<br> Transakční třída **Milník** funguje pouze s typem transakce **Fakturovaný prodej**. <br>Typy transakcí **Mezipodnikový prodej** a **Jednotkové náklady zdroje** jsou použitelné pouze u transakční třídy **Čas** a jsou dostupné pouze v denících záznamů ve scénáři omezeného nasazení a nikoli při nasazování Project Operations ve scénářích založených na zdrojích/položkách, které nejsou na skladě. |
    | Vybrat produkt | Když je vybrána třída transakce **Materiál**, toto pole vám umožňuje určit, zda je materiálová transakce, pro kterou vytváříte řádek deníku, existujícím produktem nebo produktem nezahrnutým do katalogu. | Pokud vyberete **Produkt nezahrnutý do katalogu**, můžete zadat název produktu. |
    | Produkt | Odkaz na produkt z katalogu. | |
    | Description | Popis řádku deníku, který usnadní jeho identifikaci. | U řádků deníku nevyfakturovaných prodejů bude hodnota použita jako popis při vytváření podrobností řádku faktury. |
    | Externí popis | Popis řádku deníku, který lze použít pro sdílení s externími zainteresovanými stranami. | U řádků deníku nevyfakturovaných prodejů bude hodnota použita jako externí popis při vytváření podrobností řádku faktury. Může se objevit i na faktuře zaslané zákazníkovi. |
    | Typ fakturace | Hodnota, která udává, zda bude řádek deníku započítán jako účtovatelná, doplňková nebo neúčtovatelná součást projektu. | V typickém toku je typ fakturace odvozen od dohodnutých podmínek, které jsou nastaveny ve smlouvě. Když však zaznamenáte řádek deníku, můžete do tohoto pole zadat hodnotu. |
    | Datum dokumentu | Použijte datum, kdy k transakci došlo. | |
    | Počáteční datum | Použijte datum, kdy k transakci došlo. | Toto pole se používá pro porovnání s datem vytvoření faktury u transakcí typu **Nevyfakturovaný prodej**. Toto srovnání vám pomůže rozhodnout, zda je transakce datovaná do budoucnosti nebo minulosti. Na fakturu budou přidány pouze transakce s uplynulým datem. |
    | Datum ukončení | Použijte datum, kdy k transakci došlo. | |
    | Datum účtování | Použijte datum, kdy bude zaznamenán účetní dopad. | |
    | Zákazník řádku smlouvy | Pokud má řádek smlouvy pouze jednoho zákazníka, je toto pole standardně nastaveno na zákazníka z řádku smlouvy, když je řádek deníku uložen. Pokud má řádek smlouvy více zákazníků, vyberte správného zákazníka v řádku smlouvy. | Pokud systém nemůže určit zákazníka řádku smlouvy na řádku deníku a pokud je prázdný ve skutečné hodnotě typu **Nevyfakturovaný prodej**, který je vytvořen z řádku deníku, skutečná hodnota nebude fakturována. |
    | Project | Vyberte projekt, do kterého chcete zaznamenat skutečnou hodnotu. | Na základě vybraného projektu, transakční třídy a úkolu se systém pokusí určit smlouvu, řádek smlouvy a zákazníka řádku smlouvy. |
    | Úloha | Vyberte úkol, do kterého chcete zaznamenat skutečnou hodnotu. | Pokud jste při nastavování smlouvy přiřadili úkoly k řádkům smlouvy, systém použije vybraný úkol spolu s třídou projektu a transakce k určení smlouvy, řádku smlouvy a zákazníka řádku smlouvy. |
    | Kategorie transakce | Vyberte kategorii transakce, do které chcete zaznamenat skutečnou hodnotu. | U výdajů určuje vybraná kategorie transakce výchozí cenu, která bude zapsána na řádek deníku při jeho uložení. |
    | Role | Toto pole je relevantní pro řádky časového deníku. Vyberte roli zdroje, který strávil čas na projektu a/nebo úkolu. | Pokud u řádků časového deníku použijete vestavěnou konfiguraci pro zadání výchozích nákladů na zdroje a fakturačních sazeb, vybraná role se použije společně s jednotkou zdrojů k určení výchozí ceny, která bude zadána na řádku deníku, když je uložen. Pokud pro zadávání výchozích cen používáte vlastní konfiguraci, měli byste tuto konfiguraci zkontrolovat a určit, zda se pole **Role** používá k zadání výchozích cenových hodnot. |
    | Subdodávka | Pokud řádek deníku představuje subdodavatelskou kapacitu nebo subdodavatelské náklady či materiály, vyberte příslušnou subdodávku. | Když jsou zaznamenány řádky nákladového deníku, vybraná subdodávka určí ceník, který se použije pro zadání výchozích jednotkových nákladů. |
    | Řádek subdodávky | Pokud řádek deníku představuje subdodavatelskou kapacitu nebo subdodavatelské náklady či materiály, vyberte příslušný řádek subdodávky. | Když jsou zaznamenány řádky nákladového deníku, vybraný subdodavatelský řádek zajistí, že výpočty dostupné kapacity na subdodavatelském řádku budou správné. |
    | Metoda výpočtu částky | Ve výchozím nastavení je toto pole nastaveno na **Vynásobit množství cenou** . Při použití této metody se částka vypočítá jako *Množství* × *Cena*. Další podporovanou metodou je **Pevná cena**. Při použití této metody bude cena nastavena na částku, a množství se při výpočtu nepoužije. | |
    | Rozpis jednotky a jednotka | Rozpis jednotky a jednotka společně identifikují jednotku množství. | Kombinace jednotky a kategorie transakce se používá k zadání výchozích cen u výdajů. Ve výchozí konfiguraci Project Operations se k zadání výchozích cen za čas používá kombinace jednotky, role a jednotky zdrojů. Pokud máte vlastní konfiguraci pro zadání výchozích cen, bude použita společně s jednotkou. Kombinace produktu a jednotky se používá k zadání výchozích cen u materiálů. |
    | Množství | Zadejte množství. | |
    | Cena | Pokud při vytváření řádku deníku zůstane cena prázdná, použijí se příslušné hodnoty pro zadání výchozích cen v závislosti na třídě transakce. Pokud je při vytváření řádku deníku zadána cena, použije se tato cena. | |
    | Daň | Zadejte libovolnou částku daně. | V závislosti na zadané výši daně se rozšířená částka vypočítá jako *Množství* + *Daň*. |

## <a name="confirm-an-entry-journal"></a>Potvrzení deníku záznamů

Poté, co zadáte všechny řádky do deníku záznamů, můžete deník potvrdit. Tento proces zaznamená každý řádek deníku jako skutečné hodnoty v příslušných projektech.

Poté, co je deník potvrzen, už nemůžete upravovat ani deník, ani žádný z jeho řádků.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Skutečné hodnoty vytvořené potvrzením deníku záznamů

Existuje několik klíčových rozdílů mezi skutečnými hodnotami, které jsou vytvářeny potvrzením deníku záznamů, a skutečnými hodnotami, které jsou vytvářeny během schvalování protokolů využití času, nákladů a materiálu a potvrzení faktury v Project Operations:

- Deníky záznamů nepoužívají připojení transakcí k propojení skutečných nákladů se skutečnými nevyfakturovanými prodeji. Skutečné hodnoty, které jsou vytvořeny při schválení protokolů využití času, výdajů a materiálu, vždy používají připojení transakcí k propojení skutečných nákladů a nevyfakturovaných prodejů.
- Deníky záznamů nepoužívají původy transakcí k propojení skutečných nákladů a skutečných nevyfakturovaných prodejů k libovolnému původnímu záznamu. Skutečné hodnoty, které jsou vytvořeny při schválení protokolů využití času, výdajů a materiálu, vždy používají původy transakcí k propojení skutečných nákladů a nevyfakturovaných prodejů k původnímu časovému záznamu.
- Když jsou fakturovány skutečné nevyfakturované prodeje vytvořené potvrzením deníku záznamů, jsou skutečné vyúčtované prodeje vytvořené během potvrzení faktury propojeny se skutečnými nevyfakturovanými prodeji podobným způsobem, jako skutečné nevyfakturované prodeje, které se vytvářejí při schválení protokolů využití času, výdajů a materiálu.
- Řádky deníku záznamů, které jsou vytvořeny pro čas, který je zadán meziorganizačními zdroji, nezpůsobí automatické vytvoření skutečných hodnot typu **Jednotkové náklady zdroje** a **Mezipodnikový prodej**. Tyto skutečné hodnoty musejí být vytvořeny ručně. Toto chování se liší od chování u časových položek, které jsou zaznamenány meziorganizačními zdroji. V takovém případě, když je čas schválen, aplikace automaticky vytvoří skutečné hodnoty typu **Náklady** u projektu a skutečné hodnoty typů **Jednotkové náklady zdroje** a **Mezipodnikový prodej** u divize vlastnící zaměstnance. Poté použije transakční připojení k propojení těchto skutečných hodnot a původy transakcí k jejich propojení s původním časovým záznamem.
- Když jsou deníky záznamů potvrzeny, vytvoří skutečné hodnoty. Deníky oprav však nelze použít k opravě těchto skutečných hodnot. Toto chování se liší od chování u skutečných hodnot, které se vytvářejí při schválení protokolů využití času, výdajů a materiálu. V takovém případě vám aplikace umožňuje používat deníky oprav k opravě skutečných hodnot, aby se opravily případné chyby, za předpokladu, že tyto skutečnosti ještě nebyly fakturovány. Pokud již byly vyfakturovány, můžete stále skutečnou hodnotu opravit, pokud zpracujete plný dobropis této skutečné hodnoty zákazníkovi.

> [!NOTE]
> Deníky záznamů nevynucují přísná pravidla výchozích hodnot. Proto používejte tyto deníky záznamů co nejméně a buďte opatrní, abyste zajistili, že ve svém systému nevytvoříte poškozená finanční data. Kdykoli je to možné, použijte k vytváření skutečných hodnot místo deníků záznamů protokoly využití času, výdajů a materiálu, nastavení milníku a záloh v projektových smlouvách a proces potvrzení projektové faktury.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
