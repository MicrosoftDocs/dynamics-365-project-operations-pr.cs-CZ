---
title: Přehled sledování projektů
description: Toto téma obsahuje informace o způsobu sledování pokroku projektu a spotřeby nákladů.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073631"
---
# <a name="project-tracking-overview"></a>Přehled sledování projektů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Potřeba sledovat pokrok oproti plánu se liší podle odvětví. Některá odvětví sledují pokrok podrobně, zatímco jiná odvětví ho sledují na vyšší úrovni. Toto téma ukazuje, jak plánovat, abyste vyhověli požadavkům vaší organizace.

## <a name="effort-tracking-view"></a>Zobrazení sledování úsilí

Zobrazení **Sledování úsilí** sleduje průběh úkolů v plánu porovnáním skutečných hodin úsilí vynaložených na úkol s hodinami plánovaného úsilí. Aplikace Dynamics 365 Project Operations používá pro výpočet metrik sledování následující vzorce:

- **Procento pokroku** : Skutečné úsilí vynaložené doposud ÷ Odhad při dokončení (EAC) 
- **Odhad dokončení (ETC)** : Plánované úsilí – Skutečné úsilí vynaložené doposud 
- **Odhad nákladů při dokončení (EAC)** : Zbývající úsilí + Skutečné úsilí vynaložené doposud 
- **Očekávaná odchylka úsilí** : Plánované úsilí – EAC

Project Operations u daného úkolu zobrazuje očekávanou odchylku úsilí. Je-li EAC větší než plánované úsilí, předpokládá se, že úkol zabere více času, než bylo původně plánováno a je pozadu za plánem. Je-li EAC menší než plánované úsilí, předpokládá se, že úkol zabere méně času, než bylo původně plánováno a je před plánem v předstihu.

## <a name="reprojecting-effort"></a>Přeplánování úsilí

Projektoví manažeři často revidují původní odhady u úkolu. Předpovědi projektu jsou vnímání odhadů projektového manažera podle aktuálního stavu projektu. Nedoporučujeme však projektovým manažerům, aby změnili směrná čísla. Důvodem je to, že směrný plán projektu představuje stanovený zdroj pravdy pro odhady plánů a nákladů projektu a všichni účastníci projektu se na něm shodli.

Projektový manažer může předpovědět úsilí na úkoly dvěma způsoby:

- Přepsat výchozí hodnotu ETC novým odhadem skutečně zbývajícího úsilí na úkol. 
- Přepsat výchozí procento pokroku novým odhadem skutečného pokroku u úkolu.

Každý přístup způsobí přepočet hodnot ETC, EAC, procenta pokroku a očekávané odchylky úsilí daného úkolu. Rovněž se přepočítají hodnoty EAC, ETC a procento pokroku souhrnných úkolů a vytvoří se nová projekce odchylky úsilí.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Přeplánování úsilí na souhrnné úkoly

Úsilí na souhrnné úkoly nebo úkoly kontejneru je možné přeplánovat. Bez ohledu na to, zda uživatel provede přeplánování pomocí zbývajícího úsilí nebo procenta pokroku souhrnných úkolů, spustí se následující sada výpočtů:

- Vypočítá se hodnota EAC, ETC a procento pokroku úkolu.
- Nová hodnota EAC se na podřízené úkoly rozdělí ve stejném poměru jako původní EAC úkolu.
- Dojde k výpočtu nové hodnoty EAC u jednotlivých úkolů, až po úkoly uzlů typu list. 
- Ovlivněné podřízené úkoly směrem k úkolům uzlů typu list mají hodnotu ETC a procentuální hodnotu pokroku přepočítány na základě hodnoty EAC. Výsledkem je nový odhad odchylky úsilí na úkol. 
- Přepočítají se hodnoty EAC souhrnných úkolů všech cest ke kořenovému uzlu.

### <a name="cost-tracking-view"></a>Zobrazení Sledování nákladů 

Zobrazení **Sledování nákladů** porovnává skutečné náklady, které byly vynaloženy na úkol, s plánovanými náklady na úkol. 

> [!NOTE]
> Toto zobrazení ukazuje pouze náklady práce a nezahrnuje náklady z odhadů výdajů. Aplikace Project Operations používá pro výpočet metrik sledování následující vzorce:

- **Procento spotřebovaných nákladů** : Skutečné náklady vynaložené doposud ÷ Odhadované náklady při dokončení
- **Náklady na dokončení (CTC)** : Plánované náklady – Skutečné náklady vynaložené doposud
- **Odhad nákladů při dokončení (EAC)** : Zbývající náklady + Skutečné dosud vynaložené náklady
- **Očekávaná odchylka nákladů** : Plánované náklady – EAC

U úkolu je zobrazen odhad odchylky nákladů. Je-li EAC větší než plánované náklady, předpokládá se, že náklady na úkol budou vyšší, než bylo původně plánováno. Proto vykazuje vývoj trendu nad rozpočet. Je-li EAC menší než plánované náklady, předpokládá se, že náklady na úkol budou nižší, než bylo původně plánováno. Proto vykazuje vývoj trendu pod rozpočtem.

## <a name="project-managers-reprojection-of-cost"></a>Přeplánování nákladů projektového manažera

Při přeplánování úsilí se hodnoty CTC, EAC, procento spotřebovaných nákladů a očekávaná odchylka nákladů přepočítají v zobrazení **Sledování nákladů**.

## <a name="project-status-summary"></a>Souhrn stavu projektu

Sledování dat v zobrazeních **Sledování úsilí** a **Sledování nákladů** znázorňuje pokrok a spotřebu nákladů na úrovni kořenového uzlu projektu, souhrnných úkolů a úkolů na úrovni uzlů typu list. Část **Stav** na stránce **Entita projektu** zobrazuje souhrn stavu na úrovni projektu.

## <a name="status-summary-fields"></a>Souhrnná pole stavu

Pole **Celkový stav projektu** je upravitelné pole, které zobrazuje celkový stav projektu. K označení zvyšujících se rizik používá barevné označení, například zelené, žluté a červené. Pole **Komentáře** umožňuje projektovému manažerovi zadat konkrétní komentáře o stavu. Pole **Datum aktualizace stavu** nelze upravit a tato hodnota je časové razítko, které označuje, kdy byl stav naposledy aktualizován.

Pole **Plnění plánu** a **Plnění nákladů** jsou nastavena od data sledování. Pokud jsou odchylky plánu a nákladů kořenového uzlu v zobrazení **Sledování úsilí** kladné, můžete tato pole nastavit na **V předstihu**. Pokud jsou odchylky plánu a nákladů kořenového uzlu záporné, můžete je nastavit na **Ve skluzu**.
