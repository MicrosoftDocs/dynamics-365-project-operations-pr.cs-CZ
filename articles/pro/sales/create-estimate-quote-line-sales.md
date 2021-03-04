---
title: Odhad na řádku nabídky založené na projektu
description: Toto téma poskytuje informace o tom, jak vytvořit odhad na řádku nabídky založené na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 56892a134c0c739958f7f939214930631dea7420
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180364"
---
# <a name="estimating-a-project-based-quote-line"></a>Odhad na řádku nabídky založené na projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Řádek nabídky založené na projektu obsahuje podrobnosti, které pomáhají odhadnout náklady a potenciální výnosy z práce spojené s dodáním řádku nabídky.

Chcete-li odhadnout řádek nabídky na základě projektu, na řádku nabídky na základě projektu vyberte kartu **Podrobnosti řádku nabídky**. Existují dva způsoby, jak vytvořit odhad na řádku nabídky na základě projektu:

- Ručně vytvořte odhad přímo na řádku nabídky pomocí podrobností řádku nabídky 
- Vytvořte projekt a plán projektu a poté přidružte projekt a úkoly v projektu k řádku nabídky. Bude povolen proces importu odhadů plánu projektu na řádku nabídky na základě informací, které jste poskytli.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Vytvoření odhadů přímo na řádku nabídky založené na projektu

Chcete-li vytvořit odhad na řádku nabídky na základě projektu, vyberte kartu **Podrobnosti na řádku nabídky**. Položka řádku, kterou vytvoříte na této kartě, shrnuje hodnotu nabídky pro tento řádek nabídky. 

Chcete-li vytvořit podrobnosti řádku nabídky, vyberte **+ Nové podrobnosti řádku nabídky** v podmřížce **Podrobnosti řádku nabídky**. Otevře se posuvník pro rychlé vytvoření. Následující pole na formuláři **Řádek nabídky**:

| **Pole** | **Umístění** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- | --- |
| Popis | Vytvořit | Popis konkrétního odhadu. | Toto pole má výchozí hodnotu souvisejícího řádku nabídky pro náklady, které se vytvářejí automaticky. |
| Třída transakce | Vytvořit | Tento rozevírací seznam poskytuje třídy transakcí, které jsou zahrnuty na kartě **Všeobecné** nabídky na základě projektu.  | Toto pole má výchozí hodnotu souvisejícího řádku nabídky pro náklady, které se vytvářejí automaticky. |
| Role | Vytvořit | Osoba, která bude tuto práci vykonávat nebo jí vzniknou náklady. | Toto pole má výchozí hodnotu souvisejícího řádku nabídky pro náklady, které se vytvářejí automaticky. |
| Kategorie | Vytvořit | Kategorie práce nebo výdajů. | Toto pole má výchozí hodnotu souvisejícího řádku nabídky pro náklady, které se vytvářejí automaticky. |
| Počáteční datum | Vytvořit | Datum zahájení práce. | Toto pole má výchozí hodnotu souvisejícího řádku nabídky pro náklady, které se vytvářejí automaticky. |
| Koncové datum | Vytvořit | Datum ukončení práce. | Toto pole má výchozí hodnotu souvisejícího řádku nabídky pro náklady, které se vytvářejí automaticky. |
| Jednotka zdroje | Vytvořit | Jednotka zdroje, které vzniknou tyto náklady a poskytne zdroj pro práci na ní. | Toto pole má výchozí hodnotu souvisejícího řádku nabídky pro náklady, které se vytvářejí automaticky. Toto pole se také používá při načítání nákladové ceny. |
| Plán jednotky | Vytvořit | Skupina jednotek práce nebo výdajů. Jednotky patří do plánu jednotek nebo do skupiny jednotek. Například míle a kilometry jsou jednotky, které patří do skupiny jednotek popisujících vzdálenost. | Toto pole má výchozí hodnotu souvisejícího řádku nabídky pro náklady, které se vytvářejí automaticky. |
| Jednotka | Vytvořit | Jednotka práce nebo výdajů. | Toto pole má výchozí hodnotu souvisejícího řádku nabídky pro náklady, které se vytvářejí automaticky. |
| Množství | Vytvořit | Množství práce nebo výdajů. | Toto pole má výchozí hodnotu souvisejícího řádku nabídky pro náklady, které se vytvářejí automaticky. |
| Cena za jednotku | Vytvořit | Fakturační sazba role, která vykonává práci, nebo prodejní cena kategorie výdajů. Toto pole je výchozí pro Čas na základě kombinace rolí a zdrojů v ceníku projektu, který je platný pro počáteční datum. U výdajů je v tomto poli výchozí nastavení ceny pro kategorii transakcí v ceníku projektu, který je platný pro počáteční datum. Pokud metoda stanovení cen pro kategorii transakcí není cena za jednotku, neexistuje žádná výchozí hodnota a toto pole zůstane prázdné. | Sazba nákladů role, která vykonává práci, nebo náklady na jednotku kategorie výdajů. Toto pole je výchozí pro Čas na základě kombinace rolí a jednotky zdroje v ceně smluvní jednotky ceníku projektu nabídky, který je platný pro počáteční datum. U výdajů je v tomto poli výchozí nastavení ceny pro kategorii transakcí v ceníku nákladů smluvní jednotky, který je platný pro počáteční datum. Pokud metoda stanovení cen pro kategorii transakcí není cena za jednotku, neexistuje žádná výchozí hodnota a toto pole zůstane prázdné. |
| Odhad daně | Vytvořit | Odhadovanou daň za tuto práci nebo výdaj můžete zadat ručně. | Toto pole nemá žádný následný dopad. |
| Množství | Vytvořit | Do tohoto pole můžete ručně zadat informace, pokud jsou pole **Množství** a **Cena** ponechána prázdná. Pokud tato pole nejsou prázdná, stane se toto pole pouze pro čtení a bude vypočítáno jako (Množství \* Jednotková cena) + daň. | Toto pole nemá žádný následný dopad. |

## <a name="update-prices-on-quote-line-details"></a>Aktualizujte ceny v podrobnostech řádku nabídky

Pokud jste změnili ceny v ceníku projektu, který je připojen k nabídce, nebo v ceníku nákladů smluvní jednotky, můžete vybrat **Přepočítat** na stránce **Nabídka**, chcete-li aktualizovat ceny v podrobnostech jednotlivých nabídek, aby se tato změna promítla. Když vyberete **Přepočítat**, objeví se varování, které vás informuje, že ceny v podrobnostech řádku nabídky pro všechny řádky nabídky v této nabídce budou resetovány. Vyberte **Ano** k aktualizaci cen prodejních i nákladových podrobností řádku nabídky.

## <a name="access-quote-line-details-for-cost"></a>Přístup k podrobnostem řádku nabídky za cenu

Na kartě **Podrobnosti řádku nabídky** vyberte řádek v mřížce, čímž povolíte některé akce na panelu nástrojů podmřížky. První akce na panelu nástrojů podmřížky, když je vybrán detail řádku nabídky, je **Otevřít podrobnosti nákladů**. Vyberte **Otevřít podrobnosti nákladů**, chcete-li zobrazit související sazbu nákladů a částku pro tento řádek nabídky.

> [!NOTE]
> Změna hodnoty jednotky zdroje, množství, data, role nebo kategorie v detailu řádku nabídky pro náklady změní odpovídající hodnoty v podrobnostech nabídky řádku pro prodej.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Měna v podrobnostech řádku nabídky pro náklady a prodej

Měna v detailu řádku nabídky pro výchozí prodeje z ceníku projektu, který je platný pro datum zahájení podrobností řádku nabídky.

Měna v podrobnostech řádku nabídky pro výchozí náklady z ceníku projektu smluvní jednotky nabídky, který je platný pro datum zahájení podrobností řádku nabídky pro náklady.

Výpočty ziskovosti převádějí částku v podrobnostech řádku nabídky pro náklady a prodej do na základní měnu prostředí a vykazují celkovou odhadovanou marži nabídky.

To by mohlo mít za následek chyby zaokrouhlování měn a změnu marží z důvodu neexistence směnných kurzů platných pro daný den. Tyto výpočty použijte v nabídkách projektu pouze jako přibližné hodnoty a nikoli jako skutečné statutární nebo jiné sestavy, které vyžadují vyšší přesnost zaokrouhlování a směnné kurzy platné pro patřičný den.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]