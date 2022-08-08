---
title: Deník integrace v Project Operations
description: Tento článek poskytuje informace o práci s deníkem integrace v Project Operations.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106267"
---
# <a name="integration-journal-in-project-operations"></a>Deník integrace v Project Operations

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Položky času, výdajů, poplatků a materiálu vytvářejí **Skutečné** transakce, které představují provozní zobrazení práce provedenou v rámci projektu. Dynamics 365 Project Operations poskytuje účetním nástroj pro kontrolu transakcí a úpravu účetních atributů podle potřeby. Po dokončení kontroly a úprav jsou transakce zaúčtovány do dílčí hlavní knihy a hlavní knihy projektu. Účetní může tyto činnosti provádět pomocí deníku **Integrace Project Operations** (**Dynamics 365 Finance** > **Řízení projektů a účetnictví** > **Deníky** > deník **Integrace Project Operations**.

![Tok deníku integrace.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Vytvoření záznamů v deníku integrace Project Operations

Záznamy v deníku integrace Project Operations jsou vytvářeny pomocí periodického procesu **Import z pracovní tabulky**. Tento proces můžete spustit přechodem na **Dynamics 365 Finance** > **Řízení a účetnictví projektů** > **Periodické** > **Integrace Project Operations** > **Import z tabulky fázování**. Proces můžete spustit interaktivně nebo jej nakonfigurovat tak, aby běžel na pozadí podle potřeby.

Když se periodický proces spustí, budou nalezeny všechny skutečné hodnoty, které ještě nejsou přidány do deníku integrace Project Operations. Vytvoří se řádek deníku pro každou transakci skutečné hodnoty.
Systém seskupí řádky deníku do samostatných deníků na základě hodnoty vybrané v poli **Jednotka období v deníku integrace Project Operations** (**Finance** > **Řízení a účetnictví projektů** > **Nastavení** > **Parametry modulu Řízení a účetnictví projektu**, karta **Project Operations v Dynamics 365 Customer Engagement**). Možné hodnoty pro toto pole zahrnují:

  - **Dny**: Skutečné hodnoty jsou seskupeny podle data transakce. Pro každý den se vytvoří samostatný deník.
  - **Měsíce**: Skutečné hodnoty jsou seskupeny podle kalendářních měsíců. Pro každý měsíc se vytvoří samostatný deník.
  - **Roky**: Skutečné hodnoty jsou seskupeny podle kalendářních let. Pro každý rok se vytvoří samostatný deník.
  - **Vše**: Všechny skutečné transakce jsou zahrnuty ve stejném deníku integrace. Pokud deník není k dispozici při spuštění periodického procesu, například pokud je deník v procesu účtování transakcí, vytvoří se nový deník.

Řádky deníku jsou vytvářeny na základě skutečných hodnot projektu. Následující seznam obsahuje některá z nejvýznamnějších výchozích pravidel a pravidel transformace:

  - Každá skutečná transakce projektu má řádek v deníku integrace Project Operations. Náklady a nefakturované prodejní transakce pro typ fakturace času a materiálu jsou zobrazeny na samostatných řádcích.
  - Pole **Datum** představuje datum transakce. Pole **Datum účtování** představuje datum, kdy je transakce zaznamenána do hlavní knihy. Pokud je datum účtování v [uzavřeném finanční období](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) a parametr **Automaticky nastavit datum účtování na otevřené období hlavní knihy** je nastaven na kartě **Finanční služby** na stránce **Parametry řízení projektů a účetnictví**, systém upraví datum účtování transakce na první datum v příštím otevřeném období hlavní knihy.
  - Pole **Poukaz** pole zobrazuje číslo poukazu pro každou skutečnou transakci. Pořadí čísel poukazů je definováno na kartě **Číselné řady** na stránce **Parametry řízení projektů a účetnictví**. Každému řádku je přiřazeno nové číslo. Po odeslání poukazu můžete zobrazit, jak souvisí cena a nefakturovaná prodejní transakce, výběrem možnosti **Související poukazy** na stránce **Transakce poukazů**.
  - Pole **Kategorie** představuje transakci projektu a výchozí hodnoty na základě kategorie transakcí pro související skutečnou hodnotu projektu.
    - Pokud je **Kategorie transakce** nastavena ve skutečné hodnotě projektu a existuje související **Kategorie projektu** v dané právnické osobě, kategorie se automaticky nastaví na kategorii tohoto projektu.
    - Pokud **Kategorie transakce** není nastavena ve skutečných hodnotách projektu, systém použije hodnotu nastavenou v poli **Výchozí kategorie projektu** na kartě **Project Operations v Dynamics 365 Customer Engagement** na stránce **Parametry modulu Řízení a účetnictví projektu**.
  - Pole **Zdroj** představuje zdroj projektu související s touto transakcí. Zdroj se používá jako odkaz v návrzích faktur projektu pro zákazníky.
  - Pole **Směnný kurz** přebírá výchozí hodnoty ze **Směnného kurzu měny** nastaveného v Dynamics 365 Finance. Pokud nastavení směnného kurzu chybí, periodický proces **Import z pracovní tabulky** nepřidá záznam do deníku a do protokolu o spuštění úlohy bude přidána chybová zpráva.
  - Pole **Vlastnost řádku** představuje typ fakturace ve skutečných hodnotách projektu. Vlastnost řádku a mapování typu účtování jsou definovány na kartě **Project Operations v Dynamics 365 Customer Engagement** na stránce **Parametry modulu Řízení a účetnictví projektu**.

V řádcích deníku integrace Project Operations lze aktualizovat pouze následující účetní atributy:

- **Fakturační skupina prodejní daně** a **Fakturační skupina prodejní daně položky**
- **Finanční dimenze** (za použití akce **Rozdělit částky**)

Řádky deníku integrace lze odstranit. Všechny nezaúčtované řádky se však do deníku vloží znovu po opětovném spuštění periodického procesu **Import z pracovní tabulky**.

### <a name="post-the-project-operations-integration-journal"></a>Zaúčtovat deník integrace Project Operations

Když zaúčtujete deník integrace, vytvoří se transakce dílčí hlavní knihy a hlavní knihy. Tyto transakce se používají při následné fakturaci zákazníků, uznání výnosů a finančním výkaznictví.

Vybraný deník integrace Project Operations lze zaúčtovat pomocí **Zaúčtovat** na stránce deníku integrace Project Operations. Všechny deníky lze automaticky zaúčtovat spuštěním procesu na **Periodika** > **Integrace Project Operations** > **Zaúčtovat deník integrace Project Operations**.

Účtování lze provádět interaktivně nebo hromadně. Všimněte si, že všechny deníky, které mají více než 100 řádků, budou automaticky zaúčtovány v dávce. Pro lepší výkon, když jsou deníky, které mají mnoho řádků, zaúčtovány v dávce, povolte funkci **Zaúčtovat deník integrace Project Operations pomocí více dávkových úloh** v pracovním prostoru **Správa funkcí**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Přeneste všechny řádky s chybami účtování do nového deníku

> [!NOTE]
> Chcete-li použít tuto funkci, povolte funkci **Přeneste všechny řádky s chybami zaúčtování do nového deníku integrace Project Operations** v pracovním prostoru **Správa funkcí**.

Během zaúčtování do deníku integrace Project Operations systém ověří každý řádek v deníku. Systém zaúčtuje všechny řádky, které nemají žádné chyby, a vytvoří nový deník pro všechny řádky, které mají chyby zaúčtování. Chcete-li zkontrolovat deníky, které obsahují řádky s chybami zaúčtování, přejděte na **Projektové řízení a účetnictví** > **Deníky** > **Deník integrace Project Operations** a filtrujte deníky pomocí pole **Původní deník**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
