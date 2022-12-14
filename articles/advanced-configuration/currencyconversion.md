---
title: Nastavení převodu měny pro výpočet prodejních cen z nákladových sazeb
description: Tento článek vysvětluje, jak nakonfigurovat chování při převodu měny, které bude použito v Microsoft Dynamics 365 Project Operations, když jsou prodejní transakce generovány z nákladových transakcí.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816661"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Nastavení převodu měny pro výpočet prodejních cen z nákladových sazeb

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

V Microsoft Dynamics 365 Project Operations lze prodejní ceny pro kategorie výdajů nastavit jako číselné hodnoty nebo je lze nastavit tak, aby se vypočítaly na základě vynaložených nákladů.

Když jsou nastaveny tak, aby se vypočítaly na základě vzniklých nákladů, jsou k dispozici následující možnosti:

- Podle nákladů
- Připočtení procenta nad náklady

Ve scénářích, kde jsou náklady vynaloženy v měně, která se liší od měny prodeje pro smlouvu projektu, je pro výpočet prodejní ceny na základě nákladů vyžadován převod měny.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Chování při převodu měn, které využívá nativní směnné kurzy Dataverse

Ve výchozím nastavení používá Project Operations směnné kurzy, které jsou uloženy v tabulce Měna v Dataverse. Chcete-li nakonfigurovat Project Operations tak, aby k výpočtu prodejních cen z nákladů používaly nativní směnné kurzy, postupujte takto.

1. Přejděte do **Project Operations \> Nastavení \> Parametry**.
1. Otevřete stránku s podrobnostmi **Parametr projektu**.
1. Nastavte pole **Logika převodu měny** na prázdnou hodnotu.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Chování při převodu měn, které využívá směnné kurzy z finančních a provozních aplikací

Směnné kurzy v tabulce Měna, které jsou nativně dostupné v Dataverse, nejsou platné k datu. Proto nemusí být vždy přizpůsobeny požadavkům, které máte pro výpočet prodejních cen z nákladových sazeb.

K výpočtu prodejní ceny v prodejní měně z nákladového kurzu v nákladové měně můžete použít směnné kurzy z finančního a provozního prostředí. Chcete-li nakonfigurovat toto chování převodu měny, postupujte takto.

1. Na stránce **Parametry projektu** přidejte pole **Logika převodu měny**. Poté vlastní nastavení uložte a publikujte.
1. Přejděte do **Project Operations \> Nastavení \> Parametry**.
1. Otevřete stránku s podrobnostmi **Parametr projektu**. 
1. Nastavte pole **Chování při převodu měn** na hodnotu **Rozšířeno s nouzovým nastavením na výchozí**.
1. Udělte roli zabezpečení **Uživatel aplikace s duálním zápisem** oprávnění **Globální čtení** k následujícím tabulkám:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. Ve svém finančním a provozním prostředí spusťte následující mapy duálního zápisu s počáteční synchronizací:

    - Typ směnného kurzu (msdyn\_exchangeratetypes)
    - Pár měny směnného kurzu (msdyn\_currencyexchangeratepairs)
    - Směnné kurzy CDS (msdyn\_currencyexchangerates)

Po provedení těchto změn duální zápis zpřístupní směnné kurzy z finančního a provozního prostředí v Dataverse. Project Operations pak použije tyto směnné kurzy k převodu nákladových sazeb na prodejní měnu smlouvy.

> [!NOTE]
> Toto chování při převodu měn se vztahuje pouze na výpočet prodejních cen z nákladových sazeb. Nebude se používat k obecnému výpočtu hodnot základní měny. Hodnoty základní měny budou vždy používat nativní směnné kurzy Dataverse bez ohledu na to, zda tento postup provedete.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
