---
title: Párování účtenky k výdajům pomocí OCR
description: Toto téma poskytuje informace o zpracování optického rozpoznávání znaků (OCR) pro účtenky.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124315"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Párování účtenky k výdajům pomocí OCR

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Zadávání výdajů bylo vylepšeno zavedením zpracování optického rozpoznávání znaků (OCR) pro účtenky. Tato funkce je navržena tak, aby zlepšila uživatelské prostředí při vytváření výkazů výdajů.

## <a name="key-features"></a>Klíčové funkce

- Systém z účtenek extrahuje jméno obchodníka, datum a celkovou částku.
- Systém se pokusí porovnat nepřipojené účtenky s nepřipojenými výdajovými transakcemi.
- Z účtenek můžete vytvořit ručně zadané výdajové transakce.

## <a name="attach-receipts-to-an-expense-report"></a>Připojení účtenek k výkazu výdajů

Chcete-li automaticky připojit účtenky, které zahrnují transakce kreditní kartou, když je vytvořen výkaz výdajů, proveďte následující kroky.

  1. Otevřete pracovní prostor **Správa výdajů**.
  2. Na kartě **Účtenky** ověřte, zda existují nepřipojené účtenky. Potvrzení můžete také odeslat na kartě **Účtenky**.
  3. Na kartě **Výdaje** ověřte, zda existují nepřipojené výdaje. Správce výdajů tyto náklady obvykle importuje od poskytovatele kreditní karty.
  4. Vyberte **Nový výkaz výdajů**. Všimněte si, že při vytváření výkazu výdajů můžete nyní zahrnout výdaje a účtenky. Pokud přidáte výdaje i účtenky, spustí se automatické párování účtenek s výdaji.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Vytvoření nebo párování účtenek s výkazy výdajů
Chcete-li vytvořit výdaj nebo spárovat výdaj z účtenky, proveďte následující kroky.

  1. Na výkazu výdajů na kartě **Účtenky** připojte účtenky volbou **Přidat účtenky**.
  2. Pod nahraným obrázkem účtenky si všimněte možností **Vytvořit** a **Párovat**.

      - Vyberte **Vytvořit** k vytvoření ručně zadané výdajové transakce a vyplnění hodnot, které jsou extrahovány z účtenky.
      - Pokud vyberete **Párovat**, systém se pokusí spárovat existující výdaj s účtenkou.

## <a name="installation"></a>Instalace

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

## <a name="frequently-asked-questions"></a>Nejčastější dotazy

**Používá Microsoft moje data pro své modely?**

Ne, společnost Microsoft vytvořila obecný model strojové učení pro svou službu zpracování účtenek. Tento model není založen na účtenkách, které nahrajete.

**Kde je tato funkce dostupná a zpracována?**

V současné době jsou podporovány Spojené státy.

**Kam jdou moje účtenky?**

Finance kontaktují Cognitive Services s cílem extrahovat data pole. Během zpracování bude služba Cognitive Services uchovávat kopii vašeho dokladu až 24 hodin. Po dokončení zpracování odebere Cognitive Services účtenku. Účtenky jsou stále uloženy v aplikaci Finance.

Další informace naleznete v tématu [Povolit porozumění účtenkám s novou funkcí rozpoznávání formulářů](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
