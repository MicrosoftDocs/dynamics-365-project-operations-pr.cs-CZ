---
title: Mezipodniková fakturace
description: Tento článek poskytuje informace a příklady mezipodnikové fakturace pro projekty.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073806"
---
# <a name="intercompany-invoicing"></a>Mezipodniková fakturace

[!include [banner](../includes/banner.md)]

Tento článek poskytuje informace a příklady mezipodnikové fakturace pro projekty.

Vaše organizace může mít více divizí, dceřiných společností a dalších právnických subjektů, které si navzájem přenášejí produkty a služby pro účely projektů. Právnická osoba, který poskytuje službu nebo produkt, se nazývá *Právnická osoba poskytující půjčku* , a právnická osoba, která přijímá službu nebo produkt, se nazývá *Právnická osoba přijímající půjčku*. 

Následující obrázek ukazuje typický scénář, kdy dvě právnické osoby, SI FR (Právnická osoba přijímající půjčku) a SI USA (Právnická osoba poskytující půjčku) sdílejí prostředky na dodání projektu pro zákazníka A. V tomto scénáři je SI FR nasmlouvána, aby dodala práci pro zákazníka A. 

[![Příklad mezipodnikové fakturace](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Cílem je učinit kontrolu nákladů, uznání výnosů, daně a cenu převodu u transakcí mezi společnostmi flexibilnější a výkonnější. Kromě toho jsou k dispozici následující funkce:

-   Vytvářejte faktury zákazníků proti projektu v právnické osobě přijímající půjčku pomocí mezipodnikových časových výkazů, výdajů a faktur dodavatele v právnické osobě poskytující půjčku.
-   Podpora výpočtů daní a nepřímých nákladů.
-   Odložte uznání výnosů v právnické osobě poskytující půjčku a když by měla právnická osoba přijímající půjčku uznat náklady.
-   Poměrně rozložte zisky z probíhající práce (WIP) v právnické osobě poskytující půjčku.
-   Nastavte převodní ceny, které mohou vycházet z různých cenových modelů. Zde je uvedeno několik příkladů:
    -   **Množství** - Částka, kterou zadáte do pole **Ceny** , je skutečná cena za množství nebo jednotku.
    -   **Výše poplatků** - Cena / cena za transakci plus částka poplatků, kterou zadáte do pole **Ceny**.
    -   **Procento poplatků** - Cena za převod je cena / cena za transakci vynásobená procentem poplatků, které zadáte do pole **Ceny**.
    -   **Procento prodejní ceny** - Procento prodejní ceny, které je převedeno na právnickou osobu poskytující půjčku.
    -   **Částka pod prodejní cenou** - Částka, kterou právnická osoba přijímající půjčku zadržuje z prodejních cen před převodem na právnickou osobu poskytující půjčku.
    -   **Poměr příspěvků** - Číslo, které zadáte do pole **Ceny** , je poměr příspěvků, který je vyjádřen jako procento z prodejní ceny.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Příklad 1: Nastavení parametrů pro mezipodnikovou fakturaci
V tomto příkladu je USSI právnická osoba poskytující půjčku a její zdroje vykazují čas vůči právnické osobě přijímající půjčku, FRSI, která vlastní smlouvu s koncovým zákazníkem. Hodiny a výdaje, které vykazují zaměstnanci USSI, lze zahrnout do faktury projektu, kterou generuje FRSI. Kromě toho existuje třetí zdroj transakcí, které mohou pocházet od právnické osoby poskytující půjčku (v tomto příkladu USSI), když poskytuje služby sdílených prodejců dceřiným společnostem (například FRSI) a poté tyto náklady přenáší na projekty v rámci těchto dceřiných společností. Všechny odpovídající fakturační dokumenty a výpočty daně jsou dokončeny modulem Finance. 

V tomto příkladu musí být FRSI zákazníkem v právnické osobě USSI a USSI musí být dodavatelem v právnické osobě FRSI. Poté můžete nastavit mezipodnikový vztah mezi těmito dvěma právnickými osobami. Následující postup ukazuje, jak nastavit parametry tak, aby se obě právnické osoby mohly podílet na mezipodnikové fakturaci.

1. Nastavte FRSI jako zákazníka v právnické osobě USSI a USSI jako dodavatele v právnické osobě FRSI. Existují tři vstupní body pro kroky, které jsou pro tento úkol nutné.

   | Krok |                                                       Vstupní bod                                                        |                                                                                                                                                                                               Popis                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | V USSI klikněte na <strong>Pohledávky</strong> &gt; <strong>Zákazníci</strong> &gt; <strong>Všichni zákazníci</strong>. |                                                                                                                                                                  Vytvořte nový záznam o zákazníkovi pro FRSI a vyberte skupinu zákazníků.                                                                                                                                                                  |
   |  T   |    Ve FRSI klikněte <strong>Závazky</strong> &gt; <strong>Dodavatelé</strong> &gt; <strong>Všichni dodavatelé</strong>.     |                                                                                                                                                                    Vytvořte nový záznam o dodavateli pro USSI a vyberte skupinu dodavatelů.                                                                                                                                                                    |
   |  C   |                                  Ve FRSI otevřete záznam dodavatele, který jste právě vytvořili.                                  | V podokně akcí na kartě <strong>Obecné</strong> klikněte ve skupině <strong>Nastavení</strong> na <strong>Mezipodnikové</strong>. Na stránce <strong>Mezipodnikové</strong> na kartě <strong>Obchodní vztah</strong> nastavte posuvník <strong>Aktivní</strong> na <strong>Ano</strong>. V poli <strong>Společnost zákazníka</strong> vyberte záznam zákazníka, který jste vytvořili v kroku A. |


2. Klikněte na **Řízení projektů a účetnictví** &gt; **Nastavení** &gt; **Parametry účetnictví řízení produktů** a potom klikněte na kartu **Mezipodniková**. Způsob, jakým nastavíte parametry, závisí na tom, zda jste právnickou osobou přijímající půjčku nebo právnickou osobou poskytující půjčku.
   -   Pokud jste právnickou osobou přijímající půjčku, vyberte kategorii nákupu, která by se měla použít k porovnání faktur dodavatele, které se generují automaticky.
   -   Pokud jste právnickou osobou poskytující půjčku, vyberte pro každou právnickou osobu přijímající půjčku výchozí kategorii projektu pro každý typ transakce. Kategorie projektu se používají pro konfiguraci daně, když fakturovaná kategorie v mezipodnikových transakcích existuje pouze v právnické osobě přijímající půjčku. Můžete si vybrat, zda časově rozložit výnosy z mezipodnikových transakcí. Toto časové rozlišení se provádí při zaúčtování transakcí a poté je zrušeno při zaúčtování mezipodnikové faktury.

3. Klikněte na **Řízení projektů a účetnictví** &gt; **Nastavení** &gt; **Ceny** &gt; **Poplatek za převod**.
4. Vyberte měnu, typ transakce a model ceny převodu. Měna, která se používá na faktuře, je měna, která je nakonfigurována v záznamu zákazníka pro právnickou osobu přijímající půjčku v právnické osobě poskytující půjčku. Měna se používá ke spárování položek v tabulce převodních cen.
5. Klikněte na **Hlavní kniha** &gt; **Nastavení zaúčtování** &gt; **Mezipodnikové účetnictví** a nastavte vztah USSI a FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Příklad 2: Vytvoření a zveřejnění mezipodnikového časového výkazu
USSI, právnická osoba poskytující půjčku, musí vytvořit a zaúčtovat časový rozvrh projektu od FRSI, právnické osoby přijímající půjčku. Existují dva vstupní body pro kroky, které jsou pro tento úkol nutné.

| Krok | Vstupní bod                                                                       | Popis                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Řízení projektů a účetnictví** &gt; **Časové výkazy** &gt; **Všechny časové výkazy** | Vytvoření nového časového výkazu Na řádku časového rozvrhu v poli **Právnická osoba** vyberte **FRSI**. V poli **ID projektu** vyberte projekt ve FRSI. Zadejte hodiny pro každý den v týdnu. |
| T    | Strana **Časový výkaz**                                                                | Po spuštění pracovního postupu odešlete časový výkaz a poznamenejte si číslo dokladu.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Příklad 3: Vytvoření a zveřejnění mezipodnikové faktury dodavatele
USSI, právnická osoba poskytující půjčku, musí vytvořit a zaúčtovat mezipodnikovou fakturu dodavatele pro projekt od FRSI, právnické osoby přijímající půjčku. Tato faktura dodavatele představuje outsourcovanou práci a výdaje, které provedli dodavatelé a které platí USSI. Existují dva vstupní body pro kroky, které jsou pro tento úkol nutné.

| Krok | Vstupní bod                                                                                      | Popis                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Závazky** &gt; **Faktury** &gt; **Otevřené faktury dodavatele** &gt; **Nová faktura dodavatele** | Vytvořte novou fakturu dodavatele a zadejte služby, které byly pořízeny jménem projektu FRSI.                                                                                                                                                                                  |
| T    | Stránka **Faktura dodavatele**                                                                      | Zadejte řádky, které představují outsourcované služby jménem FRSI. Na pevné záložce **Podrobnosti řádku** na kartě **Projekt** řádku faktury v poli **Společnosti projektu** zadejte **FRSI**. Zadejte projekt a odpovídající informace. Poté zaúčtujte fakturu dodavatele. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Příklad 4: Vytvoření a zaúčtování mezipodnikové faktury
USSI, právnická osoba poskytující půjčku, musí vytvořit a zaúčtovat mezipodnikovou fakturu. Existují dva vstupní body pro kroky, které jsou pro tento úkol nutné.

| Krok | Vstupní bod                                                                                             | Popis                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Řízení projektů a účetnictví** &gt; **Faktury projektu** &gt; **Mezipodniková faktura zákazníka**  | Kliknutím na **Nový** otevřete stránku **Vytvořit mezipodnikovou fakturu**.                                                                                  |
| T    | **Řízení projektů a účetnictví** &gt; **Faktury projektu** &gt; **Mezipodnikové faktury zákazníka** | Na stránce **Vytvořit mezipodnikovou fakturu** zadejte právnickou osobu, zadejte transakci, která má být zahrnuta, a klikněte na **Vyhledat**. |
| C    | **Řízení projektů a účetnictví** &gt; **Faktury projektu** &gt; **Mezipodnikové faktury zákazníka** | Vyberte transakce, které chcete fakturovat, nebo klikněte na **Vybrat vše** k fakturaci všech transakcí ze seznamu. Pak klikněte na **OK**.                  |
| D    | Stránka **Mezipodniková faktura**                                                                       | Zobrazí se návrh mezipodnikové faktury zákazníka.                                                                                             |
| E    | Stránka **Mezipodniková faktura**                                                                       | Klikněte na **Zaúčtovat**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Příklad 5: Zaúčtování faktury dodavatele a fakturace zákazníka
Když právnická osoba poskytující půjčku, USSI, zaúčtuje mezipodnikovou fakturu zákazníka, vytvoří se v právnické osobě přijímající půjčku, FRSI odpovídající nevyřízená faktura dodavatele. Po zaúčtování této faktury dodavatele FRSI také fakturuje zákazníkovi projektu hodiny, které zadala USSI. Existují tři vstupní body pro kroky, které jsou pro tento úkol nutné.

| Krok | Vstupní bod                                                                                        | Popis                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Závazky** &gt; **Faktury** &gt; **Nevyřízené faktury dodavatele**                            | Zkontrolujte fakturu a ověřte, zda jsou zahrnuty hodnoty časového rozvrhu, a poté odešlete fakturu dodavatele.                  |
| T    | **Řízení projektů a účetnictví** &gt; **Faktury projektu** &gt; **Návrhy faktury projektu** | Vytvořte pro projekt novou fakturu projektu a ověřte, zda se zobrazily hodinové transakce, které byly zaúčtovány.            |
| C    | Stránka **Faktura projektu**                                                                       | Vyberte fakturu projektu a poté klikněte na **Zobrazit podrobnosti** ke kontrole nákladů a částky prodeje. Poté zaúčtujte fakturu. |


Další informace viz [Konfigurace mezipodnikové fakturace projektu](tasks/configure-intercompany-project-invoicing.md).


