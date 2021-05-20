---
title: Výchozí hodnoty finanční dimenze
description: Tohle téma poskytuje informace, jak nastavit výchozí finanční dimenze.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950121"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]