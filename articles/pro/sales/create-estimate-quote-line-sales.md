---
title: Odhad na řádku nabídky založené na projektu
description: Toto téma poskytuje informace o tom, jak vytvořit odhad na řádku nabídky založené na projektu.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a29cf20fe95ee5bfb189defded4f06aadb75a841
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598342"
---
# <a name="estimating-a-project-based-quote-line"></a>Odhad na řádku nabídky založené na projektu

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Řádek nabídky založené na projektu obsahuje podrobnosti, které pomáhají odhadnout náklady a potenciální výnosy z práce spojené s dodáním řádku nabídky.

Chcete-li odhadnout řádek nabídky na základě projektu, na řádku nabídky na základě projektu vyberte kartu **Podrobnosti řádku nabídky**. Existují dva způsoby, jak vytvořit odhad na řádku nabídky na základě projektu:

- Ručně vytvořte odhad přímo na řádku nabídky pomocí podrobností řádku nabídky. 
- Vytvořte projekt a plán projektu a poté přidružte projekt a úkoly v projektu k řádku nabídky. Bude povolen proces importu odhadů plánu projektu na řádku nabídky na základě informací, které jste poskytli.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Vytvoření odhadů přímo na řádku nabídky založené na projektu

Chcete-li vytvořit odhad na řádku nabídky na základě projektu, vyberte kartu **Podrobnosti na řádku nabídky**. Položka řádku, kterou vytvoříte na této kartě, shrnuje hodnotu nabídky pro tento řádek nabídky. 

Chcete-li vytvořit podrobnosti řádku nabídky, vyberte **Nové podrobnosti řádku nabídky** v podmřížce **Podrobnosti řádku nabídky**. Otevře se posuvník pro rychlé vytvoření. Následující tabulka poskytuje informace o polích na stránce **Údaj řádku nabídky** a jak hodnoty ovlivňují funkčnost.

| **Pole** | **Místo** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- | --- |
| Popis | Vytvořit | Popis konkrétního odhadu. | Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Třída transakce | Vytvořit | Tento rozevírací seznam poskytuje třídy transakcí, které jsou zahrnuty na kartě **Všeobecné** řádku nabídky na základě projektu.  | Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Vybrat produkt | Vytvořit | Platí, když je třída transakce **Materiál**. Můžete vybrat, zda je tento řádek odhadu pro **existující** (katalogový) produkt nebo **zapsaný** produkt. | Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Produkt | Vytvořit | ID produktu z katalogu produktů. Toto pole je k dispozici pouze, když vyberete **Existující** v poli **Vybrat produkt**. ID se používá k načtení prodejní ceny z ceníku projektu na cenové nabídce. | Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Produkt nezahrnutý do katalogu | Vytvořit | Textové pole pro zadání názvu produktu. Toto pole je k dispozici pouze, když vyberete produkt **nezahrnutý do katalogu** v poli **Vybrat produkt**.| Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Role | Vytvořit | Role osoby, která bude tuto práci vykonávat nebo jí vzniknou náklady. | Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Kategorie | Vytvořit | Kategorie práce nebo výdajů. | Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Počáteční datum | Vytvořit | Počáteční datum práce | Toto pole je výchozí pro údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Koncové datum | Vytvořit | Koncové datum práce | Toto pole je výchozí pro údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Jednotka zdroje | Vytvořit | Zdrojová jednotka, které vznikají tyto náklady a poskytuje prostředek pro práci na ní. | Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny, a používá se v načtení nákladové ceny. |
| Plán jednotky | Vytvořit | Skupina jednotek práce, produktu nebo výdajů. Jednotky patří do plánu jednotek nebo do skupiny jednotek. Například míle a kilometry jsou jednotky, které patří do skupiny jednotek popisujících vzdálenost. | Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Jednotka | Vytvořit | Jednotka práce, produktu nebo výdajů. | Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Množství | Vytvořit | Množství práce, produktu nebo výdajů. | Tato hodnota je výchozí pro související údaje řádku cenové nabídky pro náklady, které jsou automaticky vytvořeny. |
| Jednotková cena | Rychlé vytvoření |Fakturační sazba role, která vykonává práci, jednotková cena produktu nebo prodejní cena produktu nebo kategorie výdajů. Pro toto pole je výchozí **Čas** na základě kombinace hodnot cenových dimenzí v řádku ceny role v ceníku projektu, který je účinný pro počáteční datum. U **výdajů** výchozí hodnota vychází z nastavení ceny pro kategorii transakcí v projektovém ceníku, která je platná pro počáteční datum. Pokud metoda stanovení cen pro kategorii transakcí není cena za jednotku, neexistuje žádná výchozí hodnota a toto pole zůstane prázdné. U produktů je výchozí hodnota založena na řádku **Položka ceníku** v ceníku projektu, který je platný v počátečním datu.| Nákladová sazba role, která vykonává práci, nebo náklad na jednotku kategorie výdajů nebo jednotková cena produktu. Pro toto pole je výchozí **Čas** na základě kombinace hodnot cenových dimenzí v řádku ceny role v ceníku projektu, který je účinný pro počáteční datum. U **výdajů** výchozí hodnota vychází z nastavení ceny pro kategorii transakcí v projektovém ceníku, která je platná pro počáteční datum. Pokud metoda stanovení cen pro kategorii transakcí není cena za jednotku, neexistuje žádná výchozí hodnota a toto pole zůstane prázdné. U produktů je výchozí hodnota založena na řádku **Položka ceníku** v ceníku projektu, který je platný v počátečním datu.|
| Odhad daně | Vytvořit | Odhadovanou daň za tuto práci nebo výdaj můžete zadat ručně. | Neexistuje žádný následný dopad na toto pole. |
| Množství | Vytvořit | Do tohoto pole můžete ručně zadat informace, pokud jsou pole **Množství** a **Cena** ponechána prázdná. Pokud tato pole nejsou prázdná, stane se toto pole pouze pro čtení a bude vypočítáno jako (Množství \* Jednotková cena) + daň. | Neexistuje žádný následný dopad na toto pole. |


## <a name="update-prices-on-quote-line-details"></a>Aktualizujte ceny v podrobnostech řádku nabídky

Pokud jste změnili ceny v ceníku projektu, který je připojen k nabídce, nebo v ceníku nákladů smluvní jednotky, můžete vybrat **Přepočítat** na stránce **Cenová nabídka**, aby se obnovily ceny v údajích jednotlivých nabídek, aby se tato změna promítla. Když vyberete **Přepočítat**, zobrazí se varování, které vás informuje, že ceny údajích řádku cenové nabídky pro všechny řádky cenové nabídky na této cenové nabídce budou resetovány. Vyberte **Ano** k aktualizaci cen prodejních i nákladových podrobností řádku nabídky.

## <a name="access-quote-line-details-for-cost"></a>Přístup k podrobnostem řádku nabídky za cenu

Na kartě **Podrobnosti řádku nabídky** vyberte řádek v mřížce, čímž povolíte některé akce na panelu nástrojů podmřížky. První akce na panelu nástrojů podmřížky, když je vybrán detail řádku nabídky, je **Otevřít podrobnosti nákladů**. Vyberte **Otevřít podrobnosti nákladů**, chcete-li zobrazit související sazbu nákladů a částku pro tento řádek nabídky.

> [!NOTE]
> Změna hodnoty jednotky zdroje, množství, data, role nebo kategorie v detailu řádku nabídky pro náklady změní odpovídající hodnoty v podrobnostech nabídky řádku pro prodej.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Měna v podrobnostech řádku nabídky pro náklady a prodej

Měna v detailu řádku nabídky pro výchozí prodeje z ceníku projektu, který je platný pro datum zahájení podrobností řádku nabídky.

Měna v podrobnostech řádku nabídky pro výchozí náklady z ceníku projektu smluvní jednotky nabídky, který je platný pro datum zahájení podrobností řádku nabídky pro náklady.

Výpočty ziskovosti převádějí částku v podrobnostech řádku nabídky pro náklady a prodej do na základní měnu prostředí a vykazují celkovou odhadovanou marži nabídky.

> [!POZNÁMKA
> > Mohou se vyskytnout chyby při zaokrouhlování měn a změněné marže z důvodu chybějících směnných kurzů k platnému datu. Tyto výpočty používejte pouze u smluv o projektu, protože se jedná o přibližné údaje a nejsou určeny pro skutečné statutární nebo jiné zprávy, které vyžadují vyšší přesnost zaokrouhlování a povědomí o datu platnosti pro směnné kurzy.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
