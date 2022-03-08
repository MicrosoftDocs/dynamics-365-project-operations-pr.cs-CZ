---
title: Vratka DPH
description: Toto téma vysvětluje, jak získat zpět vratky u transakcí s DPH.
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76706fd8ced58063b05bc8ebe4b25c1dddbf0890e72e9c7194d17ff2937dc8ca
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986033"
---
# <a name="vat-recovery"></a>Vratka DPH 

Aby společnost nebo organizace mohla dostávat vrácené částky za způsobilé transakce k dani z přidané hodnoty (DPH), musí identifikovat, shromažďovat, ověřovat a odesílat přesné informace. Tento proces zahrnuje více úkolů a v závislosti na velikosti vaší společnosti může zahrnovat několik zaměstnanců nebo rolí.

Chcete-li získat zpět DPH pomocí modulu Správa výdajů, musí být splněny následující předpoklady:

- Kódy daně musí být vytvořeny pro země / oblasti, které jsou přiděleny do kategorií výdajů.
- Pro každý daňový zákon musí být vytvořena skupina DPH.
- Pro každou skupinu DPH musí být vytvořen kód DPH položky.

Po splnění nezbytných předpokladů zaměstnanci musejí provést následující kroky k vyžádání vratek za transakce s DPH.

1. Ve vyúčtování výdajů zadejte daňové údaje o transakcích kreditní kartou, abyste identifikovali nároky na vrácení DPH.
2. Ujistěte se, že jsou všechny daňové údaje úplné, a poté odešlete vyúčtování výdajů.
3. Zpracujte výdaje, které jsou způsobilé pro mezinárodní vratky DPH.
4. Zašlete údaje o vratkách DPH prodejci třetí strany a podejte mezinárodní přiznání k vrácení.
5. Zpracujte výdaje na tuzemské vrácení DPH.

V následujících částech jsou uvedeny příklady, které ukazují, jak zaměstnanci Contoso provádějí jednotlivé kroky.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Ve vyúčtování výdajů zadejte daňové údaje o transakcích kreditní kartou, abyste identifikovali nároky na vrácení DPH

Petra, obchodní zástupkyně Contoso se sídlem v USA, se nedávno vrátila z prodejní cesty do Velké Británie. Během výletu jí vznikly nějaké soukromé výdaje na kreditní kartě za jídlo. Nancy nyní musí vytvořit vyúčtování výdajů, aby sesouhlasila její výdaje.

Když Nancy zadá informace ve svém vyúčtování výdajů, vybere v poli **Země/region** na stránce **Upravit vyúčtování výdajů** možnost **Spojené království**. Seznam skupin DPH je poté filtrován, takže zobrazuje pouze skupiny, které se vztahují na Spojené království. Nancy vybere skupinu DPH **Spojené království 001** a poté vybere skupinu DPH **Jídla**. Poté přidá novou transakci za její ubytování. Protože pro ubytování ve Spojeném království existuje pouze jedna skupina DPH a skupina daně z prodeje zboží, tyto informace se automaticky vyplní v Nancyně vyúčtování výdajů.

Podle zásad Contoso musí mít všechny výdaje odpovídající potvrzení. Když tedy Nancy uloží své vyúčtování výdajů, obdrží zprávu, která uvádí, že musí připojit potvrzení o každé transakci, kterou uvedla ve svém vyúčtování výdajů. Nancy ověří, že ke svému vyúčtování výdajů připojila digitální snímek potvrzení každé transakce, a poté odešle vyúčtování ke schválení. Poté odešle papírové příjemky týmu zpracování back-office. Tento tým odešle údaje o vrácení DPH dodavateli třetí strany, který podává mezinárodní přiznání k vrácení DPH za Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Ujistěte se, že jsou všechny daňové údaje úplné, a poté odešlete vyúčtování výdajů

April, koordinátorka závazků pro Contoso, před odesláním přehledu musí zadat všechny daňové údaje, které v sestavě výdajů chybí. Otevře stránku **Podrobnosti vyúčtování výdajů** a uvidí schválené vyúčtování výdajů Nancy. April poté otevře vyúčtování výdajů a zobrazí podrobnosti transakcí. Vidí, že Nancy pro jednu z transakcí nezadala skupinu DPH. Protože tyto informace nejsou poskytnuty, April nemůže zaúčtovat vyúčtování výdajů. Proto April přejde na stránku **Daňové konfigurace** v okně Správa výdajů a najde příslušnou skupinu DPH pro danou zemi / region a typ transakce. April nyní může zaúčtovat vyúčtování výdajů do hlavní knihy.

Když April zaúčtuje vyúčtování výdajů, vytvoří se pracovní položka s možností vrácení DPH. Tato pracovní položka je přiřazena členovi týmu zpracování back-office. April obdrží zprávu, která potvrzuje, že zaúčtování bylo úspěšné. Tato zpráva také uvádí počet transakcí s DPH, které byly identifikovány k vrácení.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Zpracování výdajů, které jsou způsobilé pro mezinárodní vratky DPH

Arnie, člen kancelářského týmu zpracování Contoso, je odpovědný za potvrzení, že všechny požadované informace pro vrácení DPH jsou zahrnuty ve výkazech výdajů. Otevře stránku **Vratka daně z výdajů** a vybere vyúčtování výdajů, které Nancy odeslala. Arnie ověří, zda jsou připojeny všechny požadované příjemky a zda byly zadány správné kódy skupiny DPH a položky DPH.

Když Arnie obdrží papírové příjemky od Nancy, ověří papírové příjemky vůči digitálním příjemkám a poté změní stav vyúčtování výdajů na **Připraveno k vratce**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Zašlete údaje o vratkách DPH prodejci třetí strany a podejte mezinárodní přiznání k vrácení

Když je Arnie připraven odeslat data vyúčtování výdajů prodejci třetí strany, který bude podávat přiznání k vrácení DPH, otevře stránku **Vrácení daně z výdajů**. Filtruje stránku tak, aby zobrazovala pouze vyúčtování výdajů, která jsou označena jako **Připraveno k vrácení**. Arnie pak vybere **Soubor** &gt; **Exportovat do aplikace Excel**. Informace o DPH z vyúčtování výdajů se exportují do listu aplikace Microsoft Excel. Arnie odešle tento list prodejci třetí strany a přidá zprávu, která uvádí, že papírové stvrzenky byly odeslány kurýrem.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Zpracování výdajů na tuzemské vrácení DPH

Arnie musí ověřit, že transakce vyúčtování výdajů jsou způsobilé k vrácení DPH a že digitální příjmy jsou připojeny k vyúčtováním. Aby mohl začít zpracovávat způsobilé výdaje k domácímu vymáhání, otevře Arnie stránku **Vrácení daně z výdajů** a vybere vyúčtování výdajů, který vyžaduje ověření. Ověří, že příjmy jsou zadány jménem společnosti a nikoli zaměstnance. Pro vrácení DPH musí být příjemky vystaveny na název společnosti. Arnie poté potvrdí, že byly použity správné kódy skupiny DPH a položky DPH.

Když Arnie obdrží papírové stvrzenky, změní stav vyúčtování výdajů na **Připraveno k vratce**. Poté může podat přiznání u příslušného daňového úřadu. V tomto případě je příslušným daňovým úřadem v USA Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]