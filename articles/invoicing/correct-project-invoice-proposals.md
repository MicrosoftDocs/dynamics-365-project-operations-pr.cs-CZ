---
title: Oprava účtování návrhů konceptů faktur projektu
description: Tento téma vysvětluje, jak upravit informace související s účetnictvím u návrhu konceptu faktury.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999308"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Oprava účtování návrhů konceptů faktur projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

*Provozní podrobnosti* pro projektové faktury vede projektový manažer na proforma faktuře. Mezi tyto podrobnosti patří rozhodnutí o hodinách, výdajích, materiálech nebo milnících, které musí být fakturovány, sazbách a použití záloh a zadržených částek. Po potvrzení původní proforma faktury můžete upravit provozní podrobnosti vytvořením a potvrzením [opravné proforma faktury](../proforma-invoicing/corrective-invoices.md).

*Účetní údaje* pro projektové faktury jsou uchovávány v dokumentu faktury orientované na zákazníka. Mezi tyto podrobnosti patří výpočet DPH a finanční dimenze použité na faktuře. Tento téma poskytuje podrobnosti o tom, jak lze tyto účetní podrobnosti upravit v návrhu faktury konceptu projektu.

## <a name="adjust-sales-tax"></a>Úprava DPH

Výchozí fakturační skupiny DPH a položkové skupiny DPH lze upravit přímo v dokumentu návrhu faktury. Chcete-li tyto skupiny upravit, vyberte **Upravit** a poté na každém řádku návrhu faktury projektu zadejte novou hodnotu do pole **Skupina DPH** nebo **Skupina DPH položek**.

## <a name="adjust-financial-dimensions"></a>Úprava finančních dimenzí

Finanční dimenze nelze upravit přímo na řádku návrhu faktury projektu. Místo toho postupujte podle těchto kroků a upravte finanční dimenze v návrhu faktury projektu.

1. Na návrhu faktury projektu vyberte **Smazat všechny**, chcete-li odebrat řádky návrhu faktury projektu.

    > [!NOTE]
    > Tlačítko **Smazat všechny** je k dispozici pouze poté, co správce systému povolí funkci **Odstranit řádky návrhu faktury při použití Project Operations pro scénáře se zdroji bez skladových materiálů** v pracovním prostoru **Správa funkcí**.

2. Úprava finančních dimenzí:

    - **Transakce na účet (milníky fakturace):** přejděte na **Všechny projekty** \> **Spravovat** \> **Transakce na účet** a vyberte milník, který vyžaduje úpravu. Pak na kartě **Finanční dimenze** aktualizujte hodnoty podle potřeby.
    - **Časové, výdajové a materiální transakce:** Na stránce **Zaúčtované transakce projektu** vyberte **Upravte účetnictví**, chcete-li aktualizovat finanční dimenze.

3. Po dokončení úpravy hodnot finanční dimenze přejděte na **Řízení projektů a účetnictví** \> **Periodické** \> **Integrace Project Operations** a vyberte **Import z pracovní tabulky**, chcete-li spustit periodický proces. Tento proces používá aktualizované hodnoty finančních dimenzí k opětovnému vytvoření řádků návrhu faktury projektu. Aktualizované hodnoty se poté použijí v podřízené účetní knize projektu a hlavní knize při zaúčtování faktury projektu.
