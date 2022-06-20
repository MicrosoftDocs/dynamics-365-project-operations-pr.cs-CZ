---
title: Sledování projektového úsilí
description: Tento článek obsahuje informace o způsobu sledování projektového úsilí a průběhu prací.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c41dbc138f6fc92a9586de173ba5dfc89c7e44e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929252"
---
# <a name="project-effort-tracking"></a>Sledování projektového úsilí

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Potřeba sledovat pokrok oproti plánu se liší podle odvětví. Některá odvětví sledují pokrok podrobně, zatímco jiná odvětví ho sledují na vyšší úrovni. Tento článek ukazuje, jak plánovat, abyste vyhověli požadavkům vaší organizace.

## <a name="effort-tracking-view"></a>Zobrazení sledování úsilí

Zobrazení **Sledování úsilí** sleduje průběh úkolů v plánu porovnáním skutečných hodin úsilí vynaložených na úkol s hodinami plánovaného úsilí. Dynamics 365 Project Operations pro výpočet metrik sledování používá následující vzorce:

- **Procento pokroku**: Skutečné úsilí vynaložené doposud ÷ Odhad při dokončení (EAC) 
- **Zbývající úsilí**: Odhadované úsilí při dokončení – skutečné doposud vynaložené úsilí 
- **Odhad nákladů při dokončení (EAC)**: Zbývající úsilí + Skutečné úsilí vynaložené doposud 
- **Očekávaná odchylka úsilí**: Plánované úsilí – EAC

Project Operations u daného úkolu zobrazuje očekávanou odchylku úsilí. Je-li EAC větší než plánované úsilí, předpokládá se, že úkol zabere více času, než bylo původně plánováno a je pozadu za plánem. Je-li EAC menší než plánované úsilí, předpokládá se, že úkol zabere méně času, než bylo původně plánováno a je před plánem v předstihu.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Přeprojektování úsilí u úkolů v uzlech typu list

Projektoví manažeři často revidují původní odhady u úkolu. Předpovědi projektu jsou vnímání odhadů projektového manažera podle aktuálního stavu projektu. Nedoporučujeme však projektovým manažerům měnit plánovaná čísla úsilí. A to proto, že plánované projektové úsilí představuje zavedený zdroj pravdivých údajů pro harmonogram projektu a odhad nákladů, a všichni účastníci projektu s ním souhlasili.

Manažer projektu může přeprojektovat úsilí uplatněné na úkoly aktualizací výchozí hodnoty pole **Zbývající úsilí** za nový odhad pro úkol. Tato aktualizace způsobí přepočet odhadu úsilí na úkol při dokončení (EAC), procenta pokroku a očekávané odchylky úsilí na úkolu. Rovněž se přepočítají hodnoty EAC, ETC a procento pokroku souhrnných úkolů a vytvoří se nová projekce odchylky úsilí.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Přeplánování úsilí na souhrnné úkoly

Úsilí na souhrnné úkoly nebo úkoly kontejneru je možné přeplánovat. Vedoucí projektů mohou aktualizovat zbývající úsilí u souhrnných úkolů. Aktualizace zbývajícího úsilí spustí v aplikaci následující sadu výpočtů:

- Vypočítá se hodnota EAC a procento pokroku na úkolu.
- Nová hodnota EAC se na podřízené úkoly rozdělí ve stejném poměru jako původní EAC úkolu.
- Dojde k výpočtu nové hodnoty EAC u jednotlivých úkolů, až po úkoly uzlů typu list. 
- Ovlivněné podřízené úkoly směrem k úkolům uzlů typu list mají zbývající úsilí a procentuální hodnotu pokroku přepočítány na základě hodnoty EAC. Výsledkem je nový odhad odchylky úsilí na úkol. 
- Přepočítají se hodnoty EAC souhrnných úkolů všech cest ke kořenovému uzlu.
- Schválené úsilí u souhrnného úkolu je součtem schváleného úsilí u všech podřízených úkolů plus schváleného úsilí u souhrnného úkolu.
- Zbývající úsilí u souhrnného úkolu je součtem zbývajícího úsilí u všech podřízených úkolů minus schválené úsilí u souhrnného úkolu.

## <a name="project-status-summary"></a>Souhrn stavu projektu

Sledování dat v zobrazeních **Sledování úsilí** a **Sledování nákladů** znázorňuje pokrok a spotřebu nákladů na úrovni kořenového uzlu projektu, souhrnných úkolů a úkolů na úrovni uzlů typu list. Část **Stav** na stránce **Entita projektu** zobrazuje souhrn stavu na úrovni projektu.

## <a name="status-summary-fields"></a>Souhrnná pole stavu

Pole **Celkový stav projektu** je upravitelné pole, které zobrazuje celkový stav projektu. K označení zvyšujících se rizik používá barevné označení, například zelené, žluté a červené. Pole **Komentáře** umožňuje projektovému manažerovi zadat konkrétní komentáře o stavu. Pole **Datum aktualizace stavu** nelze upravit a tato hodnota je časové razítko, které označuje, kdy byl stav naposledy aktualizován.

Pole **Plnění plánu** a **Plnění nákladů** jsou nastavena od data sledování. Pokud jsou odchylky plánu a nákladů kořenového uzlu v zobrazení **Sledování úsilí** kladné, můžete tato pole nastavit na **V předstihu**. Pokud jsou odchylky plánu a nákladů kořenového uzlu záporné, můžete je nastavit na **Ve skluzu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
