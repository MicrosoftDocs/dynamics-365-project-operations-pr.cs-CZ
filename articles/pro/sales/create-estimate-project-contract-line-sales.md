---
title: Odhad řádku smlouvy na základě projektu – omezené
description: Tohle téma poskytuje informace o odhadech na řádku smlouvy na základě projektu.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bf7941a627375604dca778ab293756bed2536049
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858069"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Odhad řádku smlouvy na základě projektu – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V Dynamics 365 Project Operations má řádek smlouvy na základě projektu podrobnosti, které pomáhají odhadnout náklady a potenciální výnosy z práce spojené s dodáním řádky smlouvy.

Chcete-li odhadnout řádek smlouvy na základě projektu, přejděte na kartu **Podrobnost řádku smlouvy** pro **Řádek smlouvy** na základě projektu.  Existují dva způsoby, jak vytvořit odhad řádku smlouvy na základě projektu:

   - Vytvořte odhad přímo na řádku smlouvy ručním přidáním podrobností řádku smlouvy.
   - Vytvořte projekt a plán projektu a poté přidružte projekt a úkoly k řádku projektové smlouvy. Tím spustíte proces, pomocí kterého můžete importovat odhad plánu projektu do řádku smlouvy na základě komponent zahrnutých na řádku smlouvy.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Vytvoření odhadu přímo na řádku smlouvy na základě projektu

Chcete-li vytvořit odhad přímo na projektovém řádku smlouvy, postupujte takto:

1. Přejděte na řádek smlouvy a vyberte kartu **Podrobnost řádku smlouvy**. Řádky, které vytvoříte na této kartě, jsou shrnuty a zobrazeny jako **Smluvní hodnota** pro tento **Řádek smlouvy**. 
2. V podmřížce **Údaje řádku smlouvy** vyberte **Nový údaj řádku smlouvy**. Otevře se posuvník pro rychlé vytvoření. Následující pole jsou k dispozici na stránce **Údaje řádku smlouvy**.

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| **Popis** | **Rychlé vytvoření** | Popis konkrétního odhadu. | Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny. |
| **Třída transakce** | **Rychlé vytvoření** | Toto je seznam transakčních tříd obsažených na kartě **Všeobecné** řádku smlouvy na základě projektu. | Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny. |
| **Vybrat produkt** | **Vytvořit** | Platí, když je třída transakce **Materiál**. Můžete určit, zda je tento řádek odhadu pro **existující** (katalogový) produkt nebo **zapsaný** produkt. | Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny. |
| **Produkt** | **Vytvořit** | ID produktu z katalogu produktů. Toto pole je k dispozici pouze, když vyberete **Existující produkt** v poli **Vybrat produkt**. ID se používá k načtení prodejní ceny z ceníku projektu na smlouvě. | Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny. |
| **Produkt nezahrnutý do katalogu** | **Vytvořit** | Textové pole pro zadání názvu produktu. Toto pole je k dispozici pouze, když vyberete produkt **nezahrnutý do katalogu** v poli **Vybrat produkt**.| Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny. |
| **Role** | **Rychlé vytvoření** | Role osoby, která vykonává tuto práci nebo účtuje tyto výdaje. | Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny.|
| **Kategorie** | **Rychlé vytvoření** | Kategorie práce nebo výdajů. |Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny.|
| **Počáteční datum** | **Rychlé vytvoření** | Počáteční datum práce | Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny. |
| **Koncové datum** | **Rychlé vytvoření** | Koncové datum práce | Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny. |
| **Jednotka zdroje** | **Rychlé vytvoření** | Zdrojová jednotka, které vznikají tyto náklady a poskytuje prostředek pro práci na ní. |Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny, a používá se v načtení nákladové ceny. |
| **Plán jednotky** | **Vytvořit** | Skupina jednotek práce, produktu nebo výdajů. Jednotky patří do plánu jednotek nebo do skupiny jednotek. Například *míle* a *kilometry (km)* jsou jednotky, které patří do skupiny jednotek popisujících vzdálenost. | Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny. |
| **Jednotka** | **Rychlé vytvoření** | Jednotka práce, produktu nebo výdajů. | Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny. |
| **Množství** | **Rychlé vytvoření** | Množství práce, produktu nebo výdajů. | Tato hodnota je výchozí pro související údaje řádku smlouvy pro náklady, které jsou automaticky vytvořeny. |
| **Cena za jednotku** | **Rychlé vytvoření** | Fakturační sazba role, která vykonává práci, jednotková cena produktu nebo prodejní cena produktu nebo kategorie výdajů. Pro toto pole je výchozí **Čas** na základě kombinace hodnot cenových dimenzí v řádku ceny role v ceníku projektu, který je účinný pro počáteční datum. U **výdajů** výchozí hodnota tohoto pole vychází z nastavení ceny pro kategorii transakcí v projektovém ceníku, která je platná pro počáteční datum. Pokud metoda stanovení cen pro kategorii transakcí není **cena za jednotku**, neexistuje žádná výchozí hodnota a toto pole zůstane prázdné. U produktů je výchozí hodnota tohoto pole založena na řádku **Položka ceníku** v ceníku projektu, který je platný v počátečním datu.| Nákladová sazba role, která vykonává práci, nebo náklad na jednotku kategorie výdajů nebo jednotková cena produktu. Pro toto pole je výchozí **Čas** na základě kombinace hodnot cenových dimenzí v řádku ceny role nákladového ceníku připojeného ke smluvní jednotce, který účinný pro počáteční datum. U výdajů výchozí hodnota tohoto pole vychází z řádku kategorie ceny nákladového ceníku, který je připojen ke smluvní jednotce, která je platná pro počáteční datum. Pokud metoda stanovení cen pro kategorii transakcí není cena za jednotku, neexistuje žádná výchozí hodnota a toto pole zůstane prázdné. U produktů je výchozí hodnota tohoto pole založena na řádku **Položka ceníku** v nákladového ceníku připojeného ke smluvní jednotce, který je platný v počátečním datu.|
| **Odhad daně** | **Rychlé vytvoření** | Odhadovaná daň za tuto práci nebo výdaj. | Odhadovaná daň za tuto práci nebo výdaj. |
| **Množství** | **Rychlé vytvoření** | Hodnotu do tohoto pole můžete přidat, pokud pole **Množství** a **Cena** jsou ponechána prázdná. Pokud jsou vyplněny hodnoty **Množství** a **Cena**, pole **Množství** je jen pro čtení a počítá se jako **(Množství \* Cena za jednotku) + Daň**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Aktualizace cen v podrobnostech řádku smlouvy

Pokud změníte ceny projektového ceníku, který je připojen ke smlouvě, nebo nákladový ceník smluvní jednotky, můžete ceny aktualizovat v podrobnostech jednotlivých řádků smlouvy tak, aby odpovídaly změnám. Na stránce **Smlouva** vyberte **Přepočítat**. Zobrazí se varování, které vás informuje, že ceny pro všechny řádky smlouvy v této smlouvě jsou resetovány. Volbou **Ano** aktualizujete ceny u podrobností prodejních i nákladových řádků smlouvy.

## <a name="access-contract-line-details-for-cost"></a>Přístup k podrobnostem řádku smlouvy pro náklady

Na kartě **Podrobnosti řádku smlouvy** vyberte řádek v mřížce, čímž zobrazíte akce na panelu nástrojů podmřížky. První akce na panelu nástrojů podmřížky je **Otevřít podrobnost nákladů**. Chcete-li zobrazit související nákladovou sazbu a částku pro tento detail řádku smlouvy, vyberte **Otevřít podrobnost nákladů**. 

> [!NOTE]
> Změna společnosti poskytující zdroje, jednotky zdroje, množství, dat, role nebo hodnot kategorií v podrobnosti řádku smlouvy pro **Náklady** také změní odpovídající hodnoty v detailu řádku smlouvy pro **Prodej**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Měna v podrobnostech řádku smlouvy pro náklady a prodej

Podrobnosti řádku smlouvy pro **Prodej** nastaví výchozí měnu z projektového ceníku, která je účinná pro počáteční datum podrobností řádku smlouvy.

Podrobnosti řádku smlouvy pro **Náklady** nastaví výchozí měnu z ceníku smluvní jednotky dané smlouvy, která je účinná pro počáteční datum podrobností řádku smlouvy pro **Náklady**.

Výpočty ziskovosti převádějí částky pro podrobnosti řádku smlouvy pro **Náklady** a **Prodej** na základní měnu prostředí k vykázání celkových skutečných a odhadovaných marží smlouvy.

> [!NOTE]
> Mohou se vyskytnout chyby při zaokrouhlování měn a změněné marže z důvodu chybějících směnných kurzů k platnému datu. Tyto výpočty používejte pouze u smluv o projektu, protože se jedná o přibližné údaje a nejsou určeny pro skutečné statutární nebo jiné zprávy, které vyžadují vyšší přesnost zaokrouhlování a povědomí o datu platnosti pro směnné kurzy.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
