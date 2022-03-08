---
title: Odhad řádku smlouvy na základě projektu
description: Tohle téma poskytuje informace o odhadech na řádku smlouvy na základě projektu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180454"
---
# <a name="estimate-a-projectbased-contract-line"></a>Odhad řádku smlouvy na základě projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_ 

V Dynamics 365 Project Operations má řádek smlouvy na základě projektu podrobnosti, které pomáhají odhadnout náklady a potenciální výnosy z práce spojené s dodáním řádky smlouvy.

Chcete-li odhadnout řádek smlouvy na základě projektu, přejděte na kartu **Podrobnost řádku smlouvy** pro **Řádek smlouvy** na základě projektu.  Existují dva způsoby, jak vytvořit odhad řádku smlouvy na základě projektu:

   - Vytvořte odhad přímo na řádku smlouvy ručním přidáním podrobností řádku smlouvy.
   - Vytvořte projekt a plán projektu a poté přidružte projekt a úkoly k řádku projektové smlouvy. Tím spustíte proces, pomocí kterého můžete importovat odhad plánu projektu do řádku smlouvy na základě komponent zahrnutých na řádku smlouvy.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Vytvoření odhadu přímo na řádku smlouvy na základě projektu

1. Přejděte na řádek smlouvy a vyberte kartu **Podrobnost řádku smlouvy**. Řádky, které vytvoříte na této kartě, jsou shrnuty a zobrazeny jako **Smluvní hodnota** pro tento **Řádek smlouvy**. 
2. V podmřížce **Podrobnosti řádku smlouvy** vyberte **+ Nová podrobnost řádku smlouvy**. Otevře se posuvník pro rychlé vytvoření. Následující pole jsou k dispozici ve formuláři **Podrobnosti řádku smlouvy**:

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| **Popis** | **Vytvořit** | Popis konkrétního odhadu. | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. |
| **Třída transakce** | **Vytvořit** | V tomto rozevíracím seznamu je seznam tříd transakcí obsažených na kartě **Obecné** pro řádek smlouvy na základě projektu. | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. |
| **Role** | **Vytvořit** | Role osoby, která vykonává tuto práci nebo účtuje tyto výdaje. | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. |
| **Kategorie** | **Vytvořit** | Kategorie práce nebo výdajů. | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. |
| **Počáteční datum** | **Vytvořit** | Počáteční datum práce | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. |
| **Koncové datum** | **Vytvořit** | Koncové datum práce | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. |
| **Společnost poskytující zdroje** | **Vytvořit** | Společnost nebo právnická osoba, která účtuje tyto náklady a poskytuje zdroje, aby na nich bylo možné pracovat. | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. Toto pole se také používá při načítání nákladové ceny. |
| **Jednotka zdroje** | **Vytvořit** | Jednotka zdroje, která účtuje tyto náklady a poskytuje zdroj, aby se na nich dalo pracovat. | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. Toto pole se také používá při načítání nákladové ceny. |
| **Plán jednotky** | **Vytvořit** | Skupina jednotek práce nebo výdajů. Jednotky patří do plánu jednotek nebo do skupiny jednotek. Například *míle* a *kilometry (km)* jsou jednotky, které patří do skupiny jednotek popisujících vzdálenost. | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. |
| **Jednotka** | **Vytvořit** | Jednotka práce nebo výdajů. | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. |
| **Množství** | **Vytvořit** | Množství práce nebo výdajů. | Toto pole standardně obsahuje podrobnost související s řádkem smlouvy pro náklady, které se vytvářejí automaticky. |
| **Cena za jednotku** | **Vytvořit** | Fakturační sazba role, která vykonává práci, nebo prodejní cena kategorie výdajů. Toto pole je výchozí pro **Čas** na základě kombinace rolí a zdrojů v ceníku projektu, který je platný pro počáteční datum. U výdajů výchozí hodnota tohoto pole vychází z nastavení ceny pro kategorii transakcí v projektovém ceníku, která je platná pro počáteční datum. Pokud metoda stanovení cen pro kategorii transakcí není **cena za jednotku**, neexistuje žádná výchozí hodnota a toto pole zůstane prázdné. | Nákladová sazba role, která vykonává práci, nebo náklady na jednotku kategorie výdajů. Výchozí hodnota tohoto pole vychází z hodnoty **Čas na základě role** a kombinace řádku ceny role nákladového ceníku připojeném ke smluvní jednotce platné pro počáteční datum. U výdajů výchozí hodnota tohoto pole vychází z řádku kategorie ceny nákladového ceníku, který je připojen ke smluvní jednotce, která je platná pro počáteční datum. Pokud metoda stanovení cen pro kategorii transakcí není cena za jednotku, neexistuje žádná výchozí hodnota a toto pole zůstane prázdné. |
| **Odhad daně** | **Vytvořit** | Odhadovaná daň za tuto práci nebo výdaj jako vstup uživatele. | Odhadovaná daň za tuto práci nebo výdaj jako vstup uživatele. |
| **Množství** | **Vytvořit** | Tuto hodnotu v tomto poli může uživatel přidat, pokud jsou pole **Množství** a **Cena** ponechána prázdná. Pokud jsou vyplněny hodnoty **Množství** a **Cena**, pole **Množství** je jen pro čtení a počítá se jako **(Množství \* Cena za jednotku) + Daň**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Aktualizace cen v podrobnostech řádku smlouvy

Pokud změníte ceny projektového ceníku, který je připojen ke smlouvě, nebo nákladový ceník smluvní jednotky, můžete ceny aktualizovat v podrobnostech jednotlivých řádků smlouvy tak, aby odpovídaly změnám. Na stránce **Smlouva** vyberte **Přepočítat**. Otevře se varování, které vás bude informovat, že ceny pro všechny řádky této smlouvy jsou obnoveny. Volbou **Ano** aktualizujete ceny u podrobností prodejních i nákladových řádků smlouvy.

## <a name="access-contract-line-details-for-cost"></a>Přístup k podrobnostem řádku smlouvy pro náklady

Na kartě **Podrobnosti řádku smlouvy** vyberte řádek v mřížce, čímž zobrazíte akce na panelu nástrojů podmřížky. První akce na panelu nástrojů podmřížky je **Otevřít podrobnost nákladů**. Chcete-li zobrazit související nákladovou sazbu a částku pro tento detail řádku smlouvy, vyberte **Otevřít podrobnost nákladů**. 

> [!NOTE]
> Změna společnosti poskytující zdroje, jednotky zdroje, množství, dat, role nebo hodnot kategorií v podrobnosti řádku smlouvy pro **Náklady** také změní odpovídající hodnoty v detailu řádku smlouvy pro **Prodej**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Měna v podrobnostech řádku smlouvy pro náklady a prodej

Podrobnosti řádku smlouvy pro **Prodej** nastaví výchozí měnu z projektového ceníku, která je účinná pro počáteční datum podrobností řádku smlouvy.

Podrobnosti řádku smlouvy pro **Náklady** nastaví výchozí měnu z ceníku smluvní jednotky dané smlouvy, která je účinná pro počáteční datum podrobností řádku smlouvy pro **Náklady**.

Výpočty ziskovosti převádějí částky pro podrobnosti řádku smlouvy pro **Náklady** a **Prodej** na základní měnu prostředí k vykázání celkových skutečných a odhadovaných marží smlouvy.

> [!NOTE]
> Mohou se vyskytnout chyby při zaokrouhlování měn a změněné marže z důvodu chybějících směnných kurzů k platnému datu. Tyto výpočty u projektových smluv používejte pouze jako přibližné hodnoty, nikoli pro skutečné statutární nebo jiné vykazování, které vyžaduje vyšší přesnost zaokrouhlování a vědomí o platnosti data pro směnné kurzy.
