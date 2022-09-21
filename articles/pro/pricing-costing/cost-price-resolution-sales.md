---
title: Určení nákladových sazeb pro odhady a skutečné hodnoty projektu
description: Tento článek poskytuje informace o tom, jak se určují nákladové sazby na odhady a skutečné hodnoty projektu.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475223"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Určení nákladových sazeb pro odhady a skutečné hodnoty projektu

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Když jsou určovány nákladové sazby na základě odhadů a skutečností v Microsoft Dynamics 365 Project Operations, systém nejprve použije datum a měnu v příchozím odhadu nebo skutečném kontextu k určení nákladového ceníku. Ve skutečném kontextu konkrétně systém používá pole **Datum transakce** pro určení, který ceník je použitelný. Hodnota **Datum transakce** příchozího odhadu nebo skutečné hodnoty se porovnává s hodnotami **Zahájení platnosti (nezávisle na časovém pásmu)** a **Konec platnosti (nezávisle na časovém pásmu)** v ceníku. Po určení ceníku nákladů systém určí nákladovou sazbu. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Určení nákladových sazeb v kontextu odhadu a skutečném kontextu pro čas

Kontext odhadu pro **Čas** odkazuje na:

- Údaje řádku nabídky pro **Čas**.
- Údaje řádku smlouvy pro **Čas**.
- Přiřazení zdroje k projektu.

Skutečný kontext pro **Čas** odkazuje na:

- Řádky deníku záznamů a oprav pro **Čas**.
- Řádky deníku, které se vytvoří při odeslání časového záznamu.

Po určení nákladového ceníku systém provede následující kroky a zadá výchozí nákladovou sazbu.

1. Systém spáruje pole **Role** a **Jednotka zdroje** v kontextu odhadu nebo skutečném odhadu pro **Čas** s řádky cen rolí v ceníku. Tato shoda předpokládá, že používáte standardní cenové dimenze mzdových nákladů. Pokud jste nakonfigurovali systém, aby pároval pole namísto polí **Role**, **Jednotka zdroje** nebo kromě nich, pak je použita k načtení odpovídajícího řádku ceny role jiná kombinace.
1. Pokud systém najde řádek ceny role, který má nákladovou sazbu pro kombinaci polí **Role** a **Jednotka zdroje**, pak je tato nákladová sazba použita jako výchozí.
1. Pokud systém nedokáže spárovat hodnoty polí **Role**, **Jednotka zdroje**, načte řádky cen rolí se shodným polem **Role**, ale s hodnotami null v poli **Jednotka zdroje**. Poté, co systém má odpovídající záznam ceny role, nákladová sazba podle tohoto záznamu bude použita jako výchozí.

> [!NOTE]
> Pokud jste konfigurovali jinou prioritu polí **Role** a **Jednotka zdroje** nebo pokud máte jiné dimenze s vyšší prioritou, předchozí chování se odpovídajícím způsobem změní. Systém načte záznamy cen rolí, které mají hodnoty, které odpovídají každé hodnotě dimenze cen v pořadí podle priority. Řádky, které mají pro tyto dimenze hodnoty null, jsou na posledním místě.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Určení nákladových sazeb v řádcích skutečností a odhadů pro výdaj

Kontext odhadu pro **Výdaj** odkazuje na:

- Údaje řádku nabídky pro **Výdaj**.
- Údaje řádku smlouvy pro **Výdaj**.
- Odhady výdajů na projekt.

Skutečný kontext pro **Výdaj** odkazuje na:

- Řádky deníku záznamů a oprav pro **Výdaj**.
- Řádky deníku, které se vytvoří při odeslání záznamu výdaje.

Po určení nákladového ceníku systém provede následující kroky a zadá výchozí nákladovou sazbu.

1. Systém spáruje pole **Kategorie** a **Jednotka** v kontextu odhadu nebo skutečném odhadu pro **Výdaj** s řádky cen kategorie v ceníku.
1. Pokud systém najde řádek ceny kategorie, který má nákladovou sazbu pro kombinaci polí **Kategorie** a **Jednotka**, pak je tato nákladová sazba použita jako výchozí.
1. Pokud systém není schopen spárovat hodnoty polí **Kategorie** a **Jednotka**, je výchozí cena nastavena na **0** (nula).
1. Pokud systém nedokáže v kontextu odhadu najít odpovídající cenový řádek kategorie, ale metoda stanovení cen není **Cena za jednotku**, je výchozí nákladová sazba nastavena na **0** (nula).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Určení nákladových sazeb na řádcích skutečností a odhadů pro materiál

Kontext odhadu pro **Materiál** odkazuje na:

- Údaje řádku nabídky pro **Materiál**.
- Údaje řádku smlouvy pro **Materiál**.
- Odhady materiálu v projektu.

Skutečný kontext pro **Materiál** odkazuje na:

- Řádky deníku záznamů a oprav pro **Materiál**.
- Řádky deníku, které se vytvoří při odeslání deníku využití materiálu.

Po určení nákladového ceníku systém provede následující kroky a zadá výchozí nákladovou sazbu.

1. Systém používá kombinaci polí **Produkt** a **Jednotka** v kontextu odhadu nebo skutečném kontextu pro **Materiál** s řádky položky ceníku v ceníku.
1. Pokud systém najde řádek položky ceníku, který má nákladovou sazbu pro kombinaci **Produkt** a **Jednotka**, použije se tato nákladová sazba jako výchozí nákladová sazba.
1. Pokud systém nedokáže spárovat hodnoty **Produkt** a **Jednotka**, výchozí nákladová jednotka je **0** (nula).
1. Pokud systém nedokáže v kontextu odhadu nebo skutečném kontextu najít odpovídající řádek položky ceníku, ale metoda stanovení cen není **Měna v jednotce**, je výchozí jednotková cena nastavena na **0** (nula). K tomuto chování dochází, protože Project Operations podporuje pouze metodu ceny **Částka měny** pro materiály, které se používají na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
