---
title: Vratka DPH ve správě výdajů
description: Toto téma vysvětluje, jak získat vrácení peněz za transakce způsobilé k dani z přidané hodnoty (DPH).
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1c7bd2cb3b200ef3be735484d4e831a7a5793d58
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275935"
---
# <a name="vat-recovery-in-expense-management"></a>Vratka DPH ve správě výdajů

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Aby společnost nebo organizace mohla dostávat vrácené částky za způsobilé transakce k dani z přidané hodnoty (DPH), musí identifikovat, shromažďovat, ověřovat a odesílat přesné informace. Tento proces zahrnuje více úkolů a v závislosti na velikosti vaší společnosti může zahrnovat několik zaměstnanců nebo rolí.

Chcete-li získat zpět DPH v modulu **Správa výdajů**, musí být splněny následující předpoklady:

- Kódy daně musí být vytvořeny pro země / oblasti, které jsou přiděleny do kategorií výdajů.
- Pro každý daňový zákon musí být vytvořena skupina DPH.
- Pro každou skupinu DPH musí být vytvořen kód DPH položky.

Po splnění nezbytných předpokladů je třeba provést následující kroky k vyžádání vrácení peněz za transakce s DPH.

1. Ve vyúčtování výdajů zadejte daňové údaje o transakcích kreditní kartou, abyste identifikovali nároky na vrácení DPH.
2. Ověřte, zda jsou všechny daňové údaje úplné, a poté odešlete vyúčtování výdajů.
3. Zpracujte výdaje, které jsou způsobilé pro mezinárodní vratky DPH.
4. Zašlete údaje o vratkách DPH prodejci třetí strany a podejte mezinárodní přiznání k vrácení.
5. Zpracujte výdaje na tuzemské vrácení DPH.

V následujících částech jsou uvedeny příklady, které ukazují, jak zaměstnanci společnosti Contoso dokončují jednotlivé kroky.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Zadejte daňové údaje o transakcích kreditní kartou, abyste identifikovali nároky na vrácení DPH.

Nancy, obchodní zástupkyně společnosti Contoso se sídlem ve Spojených státech, se nedávno vrátila z obchodní cesty do Spojeného království. Během výletu Nancy vznikly nějaké soukromé výdaje na kreditní kartě za jídlo. Nancy nyní musí vytvořit vyúčtování výdajů, aby sesouhlasila výdaje.

Když Nancy zadá informace ve vyúčtování výdajů, vybere v poli **Země/region** na stránce **Upravit vyúčtování výdajů** možnost **Spojené království**. Seznam skupin DPH je poté filtrován, takže zobrazuje pouze skupiny, které se vztahují na Spojené království. Nancy vybere skupinu DPH **Spojené království 001** a poté vybere skupinu DPH **Jídla**. Dále Nancy přidá novou transakci pro ubytování. Protože pro ubytování ve Spojeném království existuje pouze jedna skupina DPH a jedna skupina daně z prodeje zboží, tyto informace se automaticky vyplní v Nancyně vyúčtování výdajů.

Podle zásad společnosti Contoso musí mít všechny výdaje odpovídající potvrzení. Když tedy Nancy uloží vyúčtování výdajů, obdrží zprávu, která uvádí, že musí připojit potvrzení o každé transakci, kterou uvedla ve svém vyúčtování výdajů. Nancy ověří, že ke svému vyúčtování výdajů připojila digitální snímek potvrzení každé transakce, a poté odešle vyúčtování ke schválení. Poté odešle papírové příjemky týmu zpracování back-office. Tento tým odešle údaje o vratce DPH dodavateli třetí strany, který pro společnost Contoso podává mezinárodní přiznání k vrácení DPH.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Ověření daňových údajů a zaúčtování vyúčtování výdajů

Než bude moci April, koordinátorka účtů pro společnost Contoso zaúčtovat vyúčtování výdajů, musí zadat všechny daňové informace, které v něm chybí. Otevře stránku **Podrobnosti vyúčtování výdajů** a uvidí schválené vyúčtování výdajů Nancy. April poté otevře vyúčtování výdajů a zobrazí podrobnosti transakcí. Vidí, že Nancy pro jednu z transakcí nezadala skupinu DPH. Protože tyto informace nejsou poskytnuty, April nemůže zaúčtovat vyúčtování výdajů. Proto přejde na stránku **Daňové konfigurace** v okně Správa výdajů a najde příslušnou skupinu DPH pro danou zemi / region a typ transakce. April nyní může zaúčtovat vyúčtování výdajů do hlavní knihy.

Když April zaúčtuje vyúčtování výdajů, vytvoří se pracovní položka s možností vrácení DPH. Tato pracovní položka je přiřazena členovi týmu zpracování back-office. April obdrží zprávu, která potvrzuje, že zaúčtování bylo úspěšné. Tato zpráva také uvádí počet transakcí s DPH, které byly identifikovány k vrácení.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Zpracování výdajů, které jsou způsobilé pro mezinárodní vratky DPH

Arnie, člen týmu pro zpracování back-office společnosti Contoso, je odpovědný za ověření, zda jsou ve vyúčtováních výdajů zahrnuty všechny požadované informace pro vrácení DPH. Otevře stránku **Vratka daně z výdajů** a vybere vyúčtování výdajů, které Nancy odeslala. Arnie poté ověří, zda jsou připojeny všechny požadované příjemky a zda byly zadány správné kódy skupiny DPH a položky DPH.

Když Arnie obdrží papírové příjemky od Nancy, ověří je proti digitálním stvrzenkám a poté změní stav vyúčtování výdajů na **Připraveno k vratce**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Odeslání údajů o vratce DPH dodavateli třetí strany

Když je Arnie připraven odeslat data vyúčtování výdajů prodejci třetí strany, který bude podávat přiznání k vrácení DPH, otevře stránku **Vrácení daně z výdajů**. Filtruje stránku tak, aby zobrazovala pouze vyúčtování výdajů, která jsou označena jako **Připraveno k vrácení**. Arnie pak vybere **Soubor** &gt; **Exportovat do aplikace Excel**. Informace o DPH z vyúčtování výdajů se exportují do listu aplikace Microsoft Excel. Arnie odešle tento list prodejci třetí strany a přidá zprávu, která uvádí, že papírové stvrzenky byly odeslány kurýrem.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Zpracování výdajů na tuzemské vrácení DPH

Arnie musí ověřit, že transakce vyúčtování výdajů jsou způsobilé k vrácení DPH a že digitální příjmy jsou připojeny k vyúčtováním. Aby mohl začít zpracovávat způsobilé výdaje k domácímu vymáhání, otevře Arnie stránku **Vrácení daně z výdajů** a vybere vyúčtování výdajů, který vyžaduje ověření. Ověří, že příjmy jsou zadány jménem společnosti a nikoli zaměstnance. (Při vratkách DPH musí být příjmy zadány jménem společnosti.) Arnie poté ověří, zda jsou připojeny všechny požadované příjemky a zda byly zadány správné kódy skupiny DPH a položky DPH.

Když Arnie obdrží papírové stvrzenky, změní stav vyúčtování výdajů na **Připraveno k vratce**. Poté může podat přiznání u příslušného daňového úřadu. V tomto případě je příslušným daňovým úřadem ve Spojených státech Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]