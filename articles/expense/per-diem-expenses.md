---
title: Výdaje na denní diety
description: Tento článek obsahuje informace o způsobu práce s výdaji na denní diety.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923180"
---
# <a name="per-diem-expenses"></a>Výdaje na denní diety

> [!IMPORTANT] 
> Funkce popisovaná v tomto článku je k dispozici cílovým uživatelům jako součást verze Preview.

Denní diety jsou pevná, předem stanovená denní náhrada, kterou společnost vyplácí svým zaměstnancům za ubytování (hotely), stravování a vedlejší výdaje, které tito zaměstnanci vynaloží při cestování za prací. Společnost vyplácí tuto náhradu zaměstnancům namísto úhrady skutečných cestovních nákladů. Zaměstnanci mohou využít své **Vedlejší/jiné** diety na pokrytí spropitného, pokojových služeb, praní nebo chemického čištění při důležitých obchodních jednáních. Sazba denních diet se může lišit v závislosti na tom, zda se zaměstnavatel rozhodne proplácet kombinované náklady na ubytování a stravování, nebo pouze náklady na stravování a vedlejší výdaje.

Sazby denních diet mohou být založeny na ročním období, místě cesty nebo na obou kritériích. Při vytvoření pravidla denní diety můžete zadat, aby bylo procento denní diety strženo, pokud zaměstnanec bude mít zajištěno náhradní stravování nebo jiné služby. Můžete také nastavit minimální a maximální počet hodin, kdy může být denní sazba aplikována na cestu zaměstnance.

Diety se vypočítávají jako celkový příspěvek za den minus srážky za stravné (náklady na doplňkové jídlo), které je zaměstnanci poskytováno.

## <a name="configure-per-diems"></a>Konfigurace denních diet

Chcete-li konfigurovat výdaje na denní diety, postupujte takto.

1. Přejděte do nabídky **Řízení výdajů** \> **Nastavení** \> **Všeobecné** \>**Parametry správy výdajů**.
2. Na kartě **Denní diety** v poli **Vypočítat srážku za stravné pomocí** vyberte způsob výpočtu diet:

    - **Typ stravy podle cesty** – Vypočítejte denní diety na základě typu zadaného jídla (snídaně, oběd nebo večeře) a na základě srážky za stravné, která je zadána pro každý druh jídla v rámci denních diet po dobu trvání cesty.
    - **Typ stravy podle dne** – Vypočítejte denní diety na základě typu zadaného jídla a na základě krácení stravného, které je zadáno pro každý druh jídla v rámci denních diet na jeden den.
    - **Počet jídel za den** – Vypočítejte diety na základě počtu zadaných jídel za den a srážky za stravné počítané za jídla, která jsou každý den poskytnuta.

3. Přejděte do nabídky **Řízení výdajů** \> **Nastavení** \> **Výpočty a kódy** \> **Umístění denních diet**.
4. Přidejte místa, kde lze denní diety použít.
5. Pro každé přidané umístění vyberte na kartě **Denní diety** denní sazbu a měnu, které jsou platné mezi konkrétními daty zahájení a ukončení pro ubytování, stravování a další výdaje. Chcete-li konfigurovat denní sazby a měny, přejděte na **Řízení výdajů** \> **Nastavení** \> **Výpočty a kódy** \> **Denní diety**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Denní diety v přepracovaném rozhraní výdajů

Funkce denních diet je podporována v přepracovaném pracovním prostoru **Řízení nákladů** v Microsoft Dynamics 365 Finance verze 10.0.25 a novější.

Při povolení denních diet postupujte následovně.

1. V pracovním prostoru **Správa funkcí** vyhledejte a vyberte funkci **Nová verze vyúčtování výdajů** v seznamu a poté vyberte **Povolit nyní**.
2. Vyhledejte a vyberte funkci **Přepracované rozhraní sestavy výdajů za denní diety** v seznamu a poté vyberte **Povolit nyní**.

## <a name="how-the-feature-works"></a>Jak funkce funguje

Tato část obsahuje příklady tří scénářů konfigurace. V každém příkladu je pole **Vypočítat srážku za stravné pomocí** nastaveno na jinou hodnotu. U všech tří příkladů je celková splatná částka stejná, dokud není uplatněna srážka za stravné. Po tomto okamžiku se celková splatná částka pro každý příklad liší.

Chcete-li vytvořit výdaje na diety, které se používají pro všechny tři příklady, postupujte takto.

1. Přejděte do nabídky **Pracovní prostory** \> **Správa výdajů**.
2. Vyberte **Nová sestava výdajů** nebo vyberte existující vyúčtování výdajů v seznamu.
3. Přidejte nový výdaj. V poli **Kategorie** vyberte **Denní diety**. Vyberte místo a datum začátku a konce cesty. Denní diety za ubytování, stravu a vedlejší výdaje (jiné výdaje) se vypočítávají na základě denní dávky, která je nastavena pro vybrané umístění.

    Vyberte například **Redmond (USA)** jako umístění. Denní náhrada pro toto umístění je 150 amerických dolarů (150 USD) na ubytování, 75 USD na jídlo a 5 USD na vedlejší výdaje. Datum zahájení cesty je 10. ledna a datum ukončení 14. ledna. Vybraná doba trvání je tedy pět dní, pokud je zvolena konfigurace kalendářních dnů s časem, a vybraný čas začíná a končí ve 00:00 v datech zahájení a ukončení. Takto vypadají výpočty:

    - Celková splatná částka = 5 × (150 + 75 + 5) = 5 × 230 = 1 150 USD
    - Stravování a vedlejší část z celkového množství = 5 × (75 + 5) = 400 USD

Pokud byla během cesty poskytnuta snídaně, oběd a večeře, musí být tato jídla započtena jako srážka za stravné.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Příklad 1: Denní diety, kde jsou srážky za stravné založeny na typu jídla na cestu

V tomto příkladu je srážka za stravné o 30 procent u snídaně, 30 procent u oběda a 40 procent u večeře. Na stránce **Parametry správy výdajů** je pole **Vypočítat srážku za stravné pomocí** nastaveno na **Typ stravy podle cesty**. Zde jsou výpočty pro případ, kdy byly zaměstnanci poskytnuty tři snídaně, dva obědy a nula večeří:

- Srážky za stravné = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Stravování a vedlejší výdaje = 400 – 112,50 = 287,50 USD
- Celková splatná částka = Celková náhrada – Srážky za stravné = 1 150 – 112,50 = 1 037,50 USD

![Výdaje na denní diety, kde jsou srážky za stravné založeny na typu jídla na cestu.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Příklad 2: Denní diety, kde je srážka za stravné založena na typu jídla na den

V tomto příkladu je srážka za stravné o 30 procent u snídaně, 30 procent u oběda a 40 procent u večeře. Na stránce **Parametry správy výdajů** je pole **Vypočítat srážku za stravné pomocí** nastaveno na **Typ stravy podle dne**. V tomto případě v mřížce **Jídlo** v dialogovém okně **Upravit výdaj** zrušte zaškrtnutí políček, abyste vyjádřili, která jídla vám byla během cesty poskytnuta.

Zde jsou například výpočty, pokud byla snídaně poskytnuta první tři dny cesty:

- Srážky za stravné pro každý z prvních tří dnů = 75 × 30 % = 22,50 USD
- Celková srážka za stravné = 3 × 22,50 = 67,50 USD
- Stravné a vedlejší výdaje za dny 1 až 3 = 75 – 22,50 = 57,50 USD
- Celkové stravné a vedlejší výdaje = součet jídel a vedlejších výdajů za pět dní = 400 – 67,50 = 332,50 USD
- Celková splatná částka = Celková částka – Srážky za stravné = 1 150 – 67,50 = 1 082,50 USD

![Výdaje na denní diety, kde jsou srážky za stravné založeny na typu jídla na den.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Příklad 3: Denní diety, kde je srážka za stravné založena na počtu jídel na den

V tomto příkladu je srážka za stravné vypočítána na základě počtu jídel, která byla poskytnuta za den (tj. pole **Vypočítat srážku za stravné pomocí** na stránce **Parametry správy výdajů** je nastaveno na **Počet jídel za den**). V mřížce **Jídlo** v dialogovém okně **Upravit výdaj** zrušte zaškrtnutí políček, abyste vyjádřili, která jídla vám byla poskytnuta.
V tomto případě je srážka za stravné založena pouze na počtu poskytnutých jídel, nikoli na typu poskytovaného jídla (snídaně/oběd/večeře).

Zde jsou výpočty denních diet, když je denní náhrada 150 USD na ubytování, 75 USD na jídlo a 5 USD na vedlejší výdaje:

- **Celková splatná částka** = 5 × (150 + 75 + 5) = 5 × 230 = 1 150 USD
- **Jedno jídlo:** Srážka za stravné = 20 % = 15 USD
- **Dvě jídla:** Srážka za stravné = 50 % = 37,50 USD
- **Tři jídla:** Srážka za stravné = 100 % = 75 USD

Zde jsou výpočty **náhrady za stravné a vedlejší výdaje**, které obsahují 5 USD pro vedlejší výdaje:

- Den 1 – zajištěna dvě jídla = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Den 2 – zajištěna dvě jídla = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Den 3 – zajištěno jedno jídlo = (75 – 15) + 5 = 60 + 5 = 65 USD
- Den 4 – nezajištěno žádné jídlo = (75 – 0) + 5 = 75 + 5 = 80 USD
- Den 5 – zajištěna tři jídla = (75 – 75) + 5 = 0 + 5 = 5 USD

- Celkový počet jídel a vedlejších výdajů = jídla a vedlejší výdaje za den 1 + den 2 + den 3 + den 4 + den 5 = 235 USD
- Celková srážka za stravné = srážka za stravné za den 1 + den 2 + den 3 + den 4 + den 5 = 37,5 + 37,5 + 15 + 0 + 75 = 165 USD
- Celková splatná částka = Celková náhrada – Celková srážka za stravné = 1 150 – 165 = 985 USD

![Výdaje na denní diety, kde jsou srážky za stravné založeny na počtu jídel na den.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Od verze Finance 10.0.23, pokud používáte přepracované rozhraní výdajů, nemůžete vytvářet výdaje na denní diety, u kterých se překrývají kalendářní data. Pokud se o to pokusíte, zobrazí se chybová zpráva.
