---
title: Určení odhadu nákladů a výnosů projektu
description: Postup určení odhadu nákladů a výnosů projektu v Project Service
author: ruhercul
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 38de99680f4ba67b8eb593ec575c2a796fcfb59436fea5323dd1d86d7cf3d797
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002593"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Určení odhadu nákladů a výnosů projektu 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Odhady projektů poskytují finanční přehled odhadované a plánované práce ve struktuře rozpisu práce projektu. Zobrazení odhadů informuje o vlivu nákladů a výnosů plánované práce. Zobrazení odhadů poskytuje nástroj pro zobrazení informací o řadě předem definovaných dimenzí, které nejlépe informují o finančním dopadu projektu.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Nákladová a prodejní hodnota projektu  
Ceníky [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] definují nákladovou a fakturační sazbu pro role, které projekty používají. Na základě rolí přidružených k úkolům ve struktuře rozpisu práce projektu lze určit dopad nákladů a výnosů provedené práce.  
  
## <a name="cost-price-defaulting"></a>Výchozí nastavení nákladové ceny  
Každý projekt patří k organizaci (v části **Vlastnící jednotka** v projektu). Ceník přidružený k vlastnící organizační jednotce určuje nákladovou cenu jednotky. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] určují nákladové ceny pro role prostřednictvím hledání kombinace role, jednotky a organizační jednotky v nákladovém ceníku za účelem získání správné nákladové ceny pro datum platnosti řádků odhadu.  
  
Pokud kombinace role, jednotky a organizační jednotky nevede ke zjištění nákladové ceny z ceníku vlastnící jednotky, bude jednotka ignorována ve prospěch kombinace role a organizační jednotky. Existuje-li nákladová cena, tato cena je převedena na jednotku, kterou jste zvolili na řádku odhadu.  
  
Pokud kombinace rolí a organizační jednotky nevede ke zjištění nákladové ceny, bude organizační jednotky ignorována ve prospěch kombinace role a jednotky a cena bude v případě potřeby převzata po použití převodu.  
  
 Pokud není určena cena pro roli, výchozí nákladová cena na řádku odhadu bude 0,00.  
  
 Všechny částky nákladů na řádcích odhadu nákladů projektu jsou v měně vlastnící organizační jednotky.  
  
## <a name="sales-price-defaulting"></a>Výchozí nastavení prodejní ceny  
Prodejní ceník vychází z entity prodeje, ke které je projekt připojen. Prodejní ceník přidružený k nabídce nebo smlouvě určuje prodejní cenu jednotky. Pokud má nabídka nebo smlouva vlastní ceník, jedná se o výchozí prodejní ceník pro odhady projektu. Pokud neexistuje žádné přidružení entity prodeje, výchozí prodejní ceník konfigurovaný v nastavení parametrů bude výchozím prodejním ceníkem pro projekt. Každý řádek odhadu má přidruženu organizační jednotku zdroje, čímž značí organizační jednotku, ze které budou zdroje rezervovány pro dokončení úkolu. Prodejní cena pro přidružené role je určena prostřednictvím hledání kombinace role, jednotky a organizační jednotky zdroje v prodejním ceníku za účelem získání správné prodejní ceny pro datum platnosti řádků odhadu.  
  
Pokud kombinace role, jednotky a organizační jednotky zdroje nevede ke zjištění prodejní ceny z prodejního ceníku, systém nebude brát v úvahu jednotku a vyhledá kombinaci role a organizační jednotky zdroje. Pokud je zjištěna prodejní cena, bude převedena na jednotku, kterou jste zvolili na řádku odhadu prodeje.  
  
Pokud systém nenajde cenu pro roli, výchozí prodejní cena na řádku odhadu bude 0,00.  
  
Zobrazení odhadů má zobrazení mřížky, které zobrazuje plochou mřížku řádků odhadu s jednotkou a celkovými náklady a prodejní cenou.  
  
## <a name="time-phased-view-of-project-estimates"></a>Zobrazení časového uspořádání odhadů projektu  
V zobrazení časového uspořádání pro odhady projektů jsou data odhadů ze zobrazení mřížky ve výchozím nastavení uspořádána dle role a zobrazují šíření dat odhadu podél časové osy ve vybraném časovém období.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Přidělení odhadu úsilí na základě režimu úkolu  
V zobrazení časového uspořádání je celkové úsilí odhadované pro úkol distribuováno přidělením určitého počtu hodin úsilí na jednotku časového období zvoleného časového období. V projektových službách režim úkolu určuje, jak bude úsilí přiděleno v rámci celé doby trvání úkolu. Používají se dva druhy přidělení – rovnoměrné přidělení a přidělení na základě pracovní doby. 
  
## <a name="work-hours-based-allocation"></a>Přidělení na základě pracovní doby  
Režim automatického plánování úkolu určuje, že pro počet zdrojů odhadovaných pro úkol se odhaduje, že budou využity po celou pracovní dobu za den. To platí také při přidělování úsilí jeho rozdělením na celou dobu trvání úkolů v zobrazení časového uspořádání. Například pro časové měřítko „Den“ platí, že pro úkol, u kterého se očekává dokončení jedním zdrojem, nesmí úsilí přidělené na den překročit pracovní dobu za den definovanou v kalendáři projektu. Proto přidělení úsilí vždy zajišťuje odhad, že prostředky budou využity po celý den.  
  
## <a name="even-distribution"></a>Rovnoměrné přidělení  
Režim ručního plánování úkolu neřeší pracovní dobu, kalendář projektu ani počet zdrojů, které jsou definovány pro úkol. Plán úkolu je založen na zadání uživatele. Pro takové úkoly nemá přidělení úsilí na jednotku zvoleného časového období žádné omezující faktory. Celkové úsilí úkolu je rovnoměrně rozděleno a přiděleno pro každou jednotku časového období na vybrané časové ose.  
  
Tímto způsobem režim úkolu definovaný v úkolu určuje rozdělení úsilí nebo přidělení úsilí na jednotku časového období do časovém uspořádání odhadů.  
  
## <a name="grouping-and-time-phasing-options"></a>Možnosti seskupení a časového uspořádání  
Toto zobrazení vám pomáhá pochopit rozložení odhadů úsilí, nákladů a prodeje za den, týden, měsíc nebo rok. Možnost Seskupit podle umožňuje uspořádání dat odhadů do dvou různých dimenzích: kategorie a zdroje. V zobrazení mřížky a zobrazení časového uspořádání lze vybrat pole, která chcete zobrazit. Součty pro jednotlivé časové úseky se zobrazí v dolní části a značí celkové odhadované úsilí, náklady a prodeje za den, týden, měsíc nebo rok.  
  
Výchozí nákladová cena a prodejní cena jsou platné podle data. Když se změní sazby pro role, bude přehlednější v zobrazení časového uspořádání při zobrazování dat odhadu uspořádaných dle „zdroje“ a časového uspořádání dle týdně.  
  
## <a name="expense-estimates"></a>Odhady výdajů  
Veškeré výdaje, které vzniknou v projektu a které nesouvisí přímo s vykonanou prací, lze zaznamenat do odhadů projektu v zobrazení mřížky. To lze provést pomocí možnosti **Přidat odhad výdajů** v zobrazení mřížky. Je možné zaznamenat odhady výdajů pro určitý úkol nebo pro celý projekt. Na těchto řádcích můžete vybrat kategorie výdajů a zvolit předběžné datum, kdy se očekává vznik výdajů. Pokud přidružené nákladové a prodejní ceníky mají výchozí ceny nebo procenta přirážky definované pro kategorie výdajů, budou tyto hodnoty při přidružení uvedeny na řádku odhadu.  
  
### <a name="see-also"></a>Viz také  
 [Příručka pro projektového manažera](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]