---
title: Zpracování příjemek výdajů
description: Toto téma poskytuje informace o zpracování optického rozpoznávání znaků (OCR) pro účtenky. Tato funkce je navržena tak, aby zlepšila uživatelské prostředí při vytváření výkazů výdajů v Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271795"
---
# <a name="expense-receipt-processing"></a>Zpracování příjemek výdajů

Zadávání výdajů bylo vylepšeno zavedením zpracování optického rozpoznávání znaků (OCR) pro účtenky. Tato funkce je navržena tak, aby zlepšila uživatelské prostředí při vytváření výkazů výdajů.

## <a name="key-features"></a>Klíčové funkce

- Systém z účtenek extrahuje jméno obchodníka, datum a celkovou částku.
- Funkce se pokusí porovnat nepřipojené účtenky s nepřipojenými výdajovými transakcemi.
- Z účtenek může uživatel vytvořit ručně zadané výdajové transakce.

## <a name="usage-examples"></a>Příklady použití

Chcete-li automaticky připojit účtenky, které zahrnují transakce kreditní kartou, když je vytvořen výkaz výdajů, proveďte následující:

  1. Otevřete pracovní prostor **Správa výdajů**.
  2. Na kartě **Účtenky** ověřte, zda existují nepřipojené účtenky. Potvrzení můžete také odeslat na kartě **Účtenky**.
  3. Na kartě **Výdaje** ověřte, zda existují nepřipojené výdaje. Správce výdajů tyto náklady obvykle importuje od poskytovatele kreditní karty.
  4. Vyberte **Nový výkaz výdajů**. Všimněte si, že při vytváření výkazu výdajů můžete nyní zahrnout výdaje a účtenky. Pokud přidáte výdaje i účtenky, spustí se automatické párování účtenek s výdaji.

Chcete-li vytvořit výdaj nebo spárovat výdaj z účtenky, proveďte následující:

  1. Na výkazu výdajů na kartě **Účtenky** připojte účtenky volbou **Přidat účtenky**.
  2. Pod nahraným obrázkem účtenky si všimněte možností **Vytvořit** a **Párovat**.

      - Vyberte **Vytvořit** k vytvoření ručně zadané výdajové transakce a vyplnění hodnot, které jsou extrahovány z účtenky.
      - Pokud vyberete **Párovat**, systém se pokusí spárovat existující výdaj s účtenkou.

## <a name="installation"></a>Instalace

Tato funkce funguje v kombinaci s funkcí **Sestavy výdajů v novém**, která pomůže zjednodušit výdaje. Tato funkce je k dispozici pouze pro prostředí úrovně alespoň 2, která jsou Sandbox a provozní.

Chcete-li použít tyto pokročilé možnosti výdajů, nainstalujte si doplněk Služba správy výdajů pro Microsoft Dynamics 365 Finance a zapněte funkce ve vaší instanci. K doplňku můžete přistupovat ze svého projektu v Microsoft Dynamics Lifecycle Services (LCS).

1. Přihlaste se do LCS a otevřete požadované prostředí.
2. Přejděte na **Úplné podrobnosti**.
3. Vyberte **Udržovat**, nebo přejděte dolů záložku s náhledem **Doplňky prostředí**.
4. Vyberte **Nainstalovat nový doplněk**.
5. Zvolte **Služba správy výdajů**.
6. Postupujte podle instalačního průvodce a souhlaste s podmínkami.
7. Vyberte volbu **Instalovat**.

V pracovním prostoru **Správa funkcí** zapněte následující funkce:

- Nová verze výkazů výdajů
- Automatické spárování a vytváření výdajů z účtenek

Po zapnutí těchto funkcí dojde k následujícím akcím:

- Existující pracovní prostor **Správa výdajů** je nahrazen novým pracovním prostorem.
- Je přidána nová položka nabídky pro viditelnost pole výdajů.
- Stále můžete otevřít bývalou stránku **Výkazy výdajů** přechodem na **Správa výdajů> Moje výdaje> Výkazy výdajů**.
- Pracovní postupy a veškerá schválení vás stále budou zavádět na existujíc stránku s výkazy výdajů.
- Účtenky budou zpracovány prostřednictvím Microsoft Azure Cognitive Services a metadata budou extrahována a přidána.
- Přidá se možnost, která vám umožní vytvořit výkaz výdajů obsahující nespárované nepřipojené účtenky.
- Možnost, která je přidána do výkazů výdajů, vám umožní vytvořit řádek výdajů z účtenky nebo se pokusí spárovat existující účtenku s existujícím řádkem výdajů.

Další informace o funkci Sestavy výdajů v novém viz [Sestavy výdajů v novém ](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Nejčastější dotazy

**Používá Microsoft moje data pro své modely?**

Ne, společnost Microsoft vytvořila obecný model strojové učení pro svou službu zpracování účtenek. Tento model není založen na účtenkách, které nahrajete.

**Kde je tato funkce dostupná a zpracována?**

V současné době jsou podporovány Spojené státy.

**Kam jdou moje účtenky?**

Finance kontaktují Cognitive Services s cílem extrahovat data pole. Během zpracování bude služba Cognitive Services uchovávat kopii vašeho dokladu až 24 hodin. Po dokončení zpracování odebere Cognitive Services účtenku. Účtenky jsou stále uloženy v aplikaci Finance.

Další informace naleznete v tématu [Povolit porozumění účtenkám s novou funkcí rozpoznávání formulářů](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]