---
title: Oprava účtování návrhů konceptů faktur projektu
description: Tento článek vysvětluje, jak upravit informace související s účetnictvím v návrhu faktury.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921202"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Oprava účtování návrhů konceptů faktur projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

*Provozní podrobnosti* pro projektové faktury vede projektový manažer na proforma faktuře. Mezi tyto podrobnosti patří rozhodnutí o hodinách, výdajích, materiálech nebo milnících, které musí být fakturovány, sazbách a použití záloh a zadržených částek. Po potvrzení původní proforma faktury můžete upravit provozní podrobnosti vytvořením a potvrzením [opravné proforma faktury](../proforma-invoicing/corrective-invoices.md).

*Účetní údaje* pro projektové faktury jsou uchovávány v dokumentu faktury orientované na zákazníka. Mezi tyto podrobnosti patří výpočet DPH a finanční dimenze použité na faktuře. Tento článek poskytuje podrobnosti o tom, jak lze tyto účetní podrobnosti upravit v návrhu projektové faktury.

## <a name="adjust-sales-tax"></a>Úprava DPH

Výchozí fakturační skupiny DPH a položkové skupiny DPH lze upravit přímo v dokumentu návrhu faktury. Chcete-li tyto skupiny upravit, vyberte **Upravit** a poté na každém řádku návrhu faktury projektu zadejte novou hodnotu do pole **Skupina DPH** nebo **Skupina DPH položek**.

## <a name="adjust-financial-dimensions"></a>Úprava finančních dimenzí

### <a name="header-dimensions"></a>Dimenze záhlaví

Ve výchozím nastavení jsou finanční dimenze faktury odvozeny ze záznamů nevyfakturovaných transakcí projektu, které jsou fakturovány. Systémová nastavení však umožňují použít finanční dimenze v záhlaví návrhů projektových faktur k zaúčtování zůstatků zákazníků. Chcete-li tuto funkci povolit, zapněte možnost **Povolit aktualizace dimenzí projektu pro pohledávky** na kartě **Finance** ve stránce **Parametry modulu Řízení a účetnictví projektu**.

Finanční dimenze v záhlaví faktur lze upravit před zaúčtováním faktury. Na stránce **Návrh projektové faktury** se přepněte na zobrazení **Záhlaví** a poté upravte hodnoty na kartě **Finanční dimenze**.

Zobrazení **Záhlaví** je dostupné až poté, co správce systému zapne funkci **Použít návrh projektové faktury a formuláře deníku faktur se zobrazením Záhlaví a řádky** v pracovním prostoru **Správa funkcí**. Tato funkce vyžaduje aktualizaci Finance 10.0.25 nebo novější.

### <a name="line-dimensions"></a>Dimenze řádku

Finanční dimenze nelze upravit přímo na řádku návrhu faktury projektu. Místo toho postupujte podle těchto kroků a upravte finanční dimenze v návrhu faktury projektu.

1. Na návrhu faktury projektu vyberte **Smazat všechny**, chcete-li odebrat řádky návrhu faktury projektu.

    Tlačítko **Smazat všechny** je k dispozici pouze poté, co správce systému povolí funkci **Odstranit řádky návrhu faktury při použití Project Operations pro scénáře se zdroji bez skladových materiálů** v pracovním prostoru **Správa funkcí**.

2. Úprava finančních dimenzí:

    - **Transakce na účet (milníky fakturace):** přejděte na **Všechny projekty** \> **Spravovat** \> **Transakce na účet** a vyberte milník, který vyžaduje úpravu. Pak na kartě **Finanční dimenze** aktualizujte hodnoty podle potřeby.
    - **Časové, výdajové a materiální transakce:** Na stránce **Zaúčtované transakce projektu** vyberte **Upravte účetnictví**, chcete-li aktualizovat finanční dimenze.

3. Po dokončení úpravy hodnot finanční dimenze přejděte na **Řízení projektů a účetnictví** \> **Periodické** \> **Integrace Project Operations** a vyberte **Import z pracovní tabulky**, chcete-li spustit periodický proces. Tento proces používá aktualizované hodnoty finančních dimenzí k opětovnému vytvoření řádků návrhu faktury projektu. Aktualizované hodnoty se poté použijí v podřízené účetní knize projektu a hlavní knize při zaúčtování faktury projektu.
