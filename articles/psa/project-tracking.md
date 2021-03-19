---
title: Průběh projektu a spotřeba nákladů
description: Toto téma obsahuje informace o sledování průběhu projektu a spotřeby nákladů.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283630"
---
# <a name="project-progress-and-cost-consumption"></a>Průběh projektu a spotřeba nákladů

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Potřeba sledovat pokrok oproti plánu se liší podle odvětví. Některá odvětví sledují pokrok podrobně, zatímco jiná odvětví ho sledují na vyšší úrovni. Toto téma ukazuje, jak plánovat, abyste vyhověli požadavkům vaší organizace.

## <a name="effort-tracking-view"></a>Zobrazení sledování úsilí

Zobrazení **Sledování úsilí** sleduje pokrok úkolů v plánu. Porovnává skutečné úsilí (v hodinách) doposud vynaložené na úkol oproti úsilí (v hodinách) plánovanému pro úkol. Project Service Automation pro výpočet metrik sledování používá následující vzorce:

Nejprve při vytváření úkolu: Plánované náklady budou nastaveny na Odhadované náklady po dokončení. Jakmile jsou u úkolu zaznamenána skutečná data, bude v zobrazení Sledování úsilí následující výpočet

- Procento pokroku = skutečné úsilí vynaložené doposud + Odhad při dokončení (EAC) 
- Odhad na dokončení (ETC) = Odhad na dokončení (EAC) - skutečné vynaložené úsilí k dnešnímu dni 
- EAC = zbývající úsilí + skutečné úsilí vynaložené doposud 
- Očekávaná odchylka úsilí = plánované úsilí – EAC

Project Service Automation u daného úkolu zobrazuje očekávanou odchylku úsilí. Je-li EAC větší než plánované úsilí, předpokládá se, že úkol zabere více času, než bylo původně plánováno. Proto je pozadu za plánem. Je-li EAC menší než plánované úsilí, předpokládá se, že úkol zabere méně času, než bylo původně plánováno. Proto je před plánem v předstihu.

## <a name="reprojecting-effort"></a>Přeplánování úsilí

Je běžné, že projektový manažer reviduje původní odhady úkolu. Předpovědi projektu jsou vnímání odhadů projektového manažera podle aktuálního stavu projektu. Nedoporučujeme však, aby projektoví manažeři směrná čísla měnili, protože směrný plán projektu představuje stanovený zdroj pravdy pro odhady plánů a nákladů projektu a všichni účastníci projektu se na něm shodli.

Projektový manažer může předpovědět úsilí na úkoly dvěma způsoby:

- Přepsat výchozí hodnotu ETC novým odhadem skutečně zbývajícího úsilí na úkol. 
- Přepsat výchozí procento pokroku novým odhadem skutečného pokroku u úkolu.

Každý z těchto přístupů způsobuje přepočet hodnot ETC, EAC a procenta pokroku a očekávané odchylky úsilí daného úkolu. Rovněž se přepočítají hodnoty EAC, ETC a procento pokroku souhrnných úkolů a vytvoří se nová projekce odchylky úsilí.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Přeplánování úsilí na souhrnné úkoly

Úsilí na souhrnné úkoly nebo úkoly kontejneru je možné přeplánovat. Bez ohledu na to, zda uživatel provede přeplánování pomocí zbývajícího úsilí nebo procenta pokroku souhrnných úkolů, spustí se následující sada výpočtů:

- Vypočítá se hodnota EAC, ETC a procento pokroku úkolu.
- Nová hodnota EAC se na podřízené úkoly rozdělí ve stejném poměru jako původní EAC úkolu.
- Dojde k výpočtu nové hodnoty EAC u jednotlivých úkolů, až po úkoly uzlů typu list. 
- Ovlivněné podřízené úkoly směrem k úkolům uzlů typu list mají hodnotu ETC a procentuální hodnotu pokroku přepočítány na základě hodnoty EAC. Výsledkem je nový odhad odchylky úsilí na úkol. 
- Přepočítají se hodnoty EAC souhrnných úkolů všech cest ke kořenovému uzlu.

### <a name="cost-tracking-view"></a>Zobrazení Sledování nákladů 

Zobrazení **Sledování nákladů** porovnává skutečné náklady, které byly vynaloženy na úkol, s plánovanými náklady. 

> [!NOTE]
> Toto zobrazení ukazuje pouze náklady práce a nezahrnuje náklady z odhadů výdajů. 

Project Service Automation pro výpočet metrik sledování používá následující vzorce:

Po vytvoření úkolu se plánované náklady rovnají odhadovaným nákladům při dokončení. Jakmile jsou u úkolu zaznamenána skutečná data, bude v zobrazení **Sledování** pro náklady následující výpočet:

 - Procento spotřebovaných nákladů = skutečné náklady vynaložené doposud ÷ odhadované náklady při dokončení na úkol
 - Náklady na dokončení (CTC) = odhadované náklady při dokončení – skutečné náklady vynaložené doposud
 - Odhadované náklady při dokončení = (CTC) + skutečné náklady vynaložené doposud
 - Očekávaná odchylka nákladů = plánované náklady - odhadované náklady při dokončení

U úkolu je zobrazen odhad odchylky nákladů. Josu-li odhadované náklady při dokončení větší než plánované náklady, předpokládá se, že náklady na úkol budou vyšší, než bylo původně plánováno. Proto vykazuje vývoj trendu nad rozpočet. Josu-li odhadované náklady při dokončení nižší než plánované náklady, předpokládá se, že náklady na úkol budou nižší, než bylo původně plánováno a vykazují vývoj trendu pod rozpočtem.

## <a name="project-managers-reprojection-of-cost"></a>Přeplánování nákladů projektového manažera

Při nové předpovědi úsilí se hodnoty CTC, odhadované náklady při dokončení, procento spotřebovaných nákladů a očekávaná odchylka nákladů přepočítají v zobrazení **Sledování nákladů**.

## <a name="project-status-summary"></a>Souhrn stavu projektu

Sledování dat v zobrazeních **Sledování úsilí** a **Sledování nákladů** znázorňuje pokrok a spotřebu nákladů na úrovni kořenového uzlu projektu, souhrnných úkolů a úkolů na úrovni uzlů typu list. Část **Stav** na stránce **Entita projektu** zobrazuje souhrn stavu na úrovni projektu.

## <a name="status-summary-fields"></a>Souhrnná pole stavu

Pole **Celkový stav projektu** je upravitelné pole, které zobrazuje celkový stav projektu. K označení zvyšujících se rizik používá barevné označení, například zelené, žluté a červené. Pole **Komentáře** umožňuje projektovému manažerovi zadat konkrétní komentáře o stavu. Pole **Datum aktualizace stavu** nelze upravit a tato hodnota je časové razítko, které označuje, kdy byl stav naposledy aktualizován.

Pole **Plnění plánu** a **Plnění nákladů** jsou nastavena od data sledování. Pokud jsou odchylky plánu a nákladů kořenového uzlu v zobrazení **Sledování úsilí** kladné, můžete tato pole nastavit na **V předstihu**. Pokud jsou odchylky plánu a nákladů kořenového uzlu záporné, můžete je nastavit na **Ve skluzu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]