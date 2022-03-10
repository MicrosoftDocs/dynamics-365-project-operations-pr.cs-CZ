---
title: Výchozí hodnoty finanční dimenze
description: Tohle téma poskytuje informace, jak nastavit výchozí finanční dimenze.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922930"
---
# <a name="financial-dimension-defaults"></a>Výchozí hodnoty finanční dimenze

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations používá rámec [Finanční dimenze](/dynamics365/finance/general-ledger/financial-dimensions) v Dynamics 365 Finance, aby bylo možné poskytnout další informace o transakcích dílčí hlavní knihy a hlavní knihy.

Výchozí finanční dimenze lze nastavit pro zákazníka, zdroj financování projektu, milník, řádek smlouvy projektu nebo projekt.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definování výchozích finančních dimenzí pro zákazníka

Výchozí dimenze zákazníka jsou specifikovány v řešení Finance. Chcete-li nastavit výchozí hodnoty dimenze, postupujte takto.

1. Přejděte na **Pohledávky** > **Zákazníci** > **Všichni zákazníci**.
2. Na kartě **Zákazníci** na kartě **Finanční dimenze** nastavte hodnoty finanční dimenze pro konkrétního zákazníka.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definování výchozích finančních dimenzí pro projektové smlouvy

Projektové smlouvy jsou vytvářeny a spravovány v Common Data Service (CDS). Atributy účetnictví pro projektové smlouvy jsou nastaveny v modulu **Řízení projektů a účetnictví** ve Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Nastavení finančních dimenzí pro zdroj financování projektu

1. Přejděte do nabídky **Řízení projektů a účetnictví** > **Projekty** > **Projektové smlouvy**.
2. Vyberte záznam, který chcete aktualizovat, a na kartě **Projektová smlouva** vyberte **Zobrazit výchozí účetnictví**.
3. Rozbalte **Související informace** a vyberte kartu **Zdroje financování**.
4. Nastavte výchozí hodnoty finanční dimenze. Všimněte si, že finanční dimenze vychází z účtu zákazníka.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Nastavení finančních dimenzí pro řádek projektové smlouvy

1. Přejděte do nabídky **Řízení projektů a účetnictví** > **Projekty** > **Projektové smlouvy**.
2. Vyberte záznam, který chcete aktualizovat, a na kartě **Projektová smlouva** vyberte **Zobrazit výchozí účetnictví**.
3. Rozbalte **Související informace** a vyberte kartu **Řádky smlouvy**.
4. Nastavte výchozí hodnoty finanční dimenze. Výchozí nastavení finanční dimenze jsou použitelná a lze je použít pouze u řádků smlouvy s pevnou cenou (milník).

Tyto výchozí hodnoty se používají u souvisejících projektových transakcí na účtu a na řádcích faktur.

## <a name="define-default-financial-dimensions-for-projects"></a>Definování výchozích finančních dimenzí pro projekty

Projekty jsou vytvářeny a spravovány v CDS. Atributy účetnictví pro projekty jsou nastaveny v modulu **Řízení projektů a účetnictví** ve Finance.

1. Přejděte do části **Správa projektů a účetnictví** > **Projekty** > **Všechny projekty**.
2. Vyberte záznam, který chcete aktualizovat, a na kartě **Projekt** vyberte **Zobrazit výchozí účetnictví**.
3. Rozbalte **Související informace** a vyberte kartu **Nastavení**.
4. Nastavte výchozí hodnoty finanční dimenze. Všimněte si, že finanční dimenze vychází z účtu zákazníka. Pokud je projekt přidružen k řádku smlouvy s více zákazníky projektové smlouvy, primární zákazník se použije k nastavení výchozích finančních dimenzí.

Výchozí finanční dimenze projektu se používají k nastavení výchozích hodnot řádků deníku pro transakce času, výdajů a poplatků v **Deníku integrace Project Operations** a na souvisejících řádcích faktury projektu.

## <a name="apply-financial-dimensions-for-project-time-entries"></a>Použití finančních dimenzí na časové záznamy projektu
Chcete-li použít finanční dimenze na časové položky projektu, mějte na paměti, že výchozí hodnota dimenze je založena na následujícím pořadí:

1. Prostředek
2. Project
3. Zdroj financování

Pokud je například výchozí dimenze zadaná u zdroje, použije se na výchozí hodnotu zadanou v projektu. Podobně bude použita výchozí dimenze projektu na výchozí, která je uvedena ve zdroji financování.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
