---
title: Úpravy projektu
description: Tento článek poskytuje informace o úpravách projektu.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788293"
---
# <a name="project-adjustments"></a>Úpravy projektu

_**Platí pro:** Project Operations pro scénáře založené na skladovém materiálu / výrobě_

## <a name="adjustments-overview"></a>Přehled úprav

Microsoft Dynamics 365 Project Operations můžete nakonfigurovat tak, aby uživatelé mohli provádět změny zaúčtovaných transakcí. Transakce projektu můžete upravovat po jedné nebo můžete vybrat ze seznamu všech transakcí projektu více transakcí najednou. Úpravy projektu se používají například k hromadné aktualizaci fakturovatelného stavu, přepočtu nákladů po změně konfigurace nebo aktualizaci zdrojů financování.

Uživatelé mohou přistupovat k funkci úprav projektu několika způsoby:

- Pomocí stránky **Upravit transakce** , která je přístupná z **Řízení projektu a účetnictví** \> **Nastavení**.
- Pomocí tlačítka **Úprava** na stránce **Zaúčtované transakce projektu** , na kterou se lze dostat z **Projektové řízení a účetnictví** \> **Transakce**.
- Pomocí tlačítka **Úprava** na stránce **Zaúčtované transakce projektu** v kontextu projektu. Tato stránka je přístupná z **Řízení projektů a účetnictví** \> **Všechny projekty**.

Chcete-li povolit úpravy, musíte zapnout jeden nebo více stavů transakce z **Řízení projektu a účetnictví** \> **Parametry řízení projektů a účetnictví** na stránce **Obecné** v sekci **Povolit úpravu stavu transakce**. Příklady stavů transakcí zahrnují zaúčtované transakce, fakturované transakce nebo eliminované transakce. Jakýkoli stav transakce, který je nastaven na **Ne** , bude mít transakce v tomto stavu, které se v procesu úpravy neobjeví jako volitelné pro úpravu.

Možnost konfigurace s názvem **Vždy vytvořit transakci úprav** je aktuálně dostupná v části Správa projektu a parametry účtování. Tuto možnost můžete deaktivovat a aktualizovat původní transakci namísto vytváření nových transakcí během úpravy v podmnožině scénářů. Bylo oznámeno, že tento parametr bude k 1. březnu 2023 ukončen. Po 1. březnu 2023 se bude systém vždy chovat, jako by byla tato možnost aktivována.

## <a name="adjustments-process-flow"></a>Tok procesu úprav

Následující kroky ukazují typický postup úprav zpracování.

1. Otevřete stránku **Úpravy projektu** .
2. Chcete-li vyhledat transakce, které splňují očekávaná kritéria pro úpravu, vyberte **Vybrat** .
3. V seznamu transakcí vyberte všechny transakce nebo podmnožinu transakcí pro úpravu.
4. Vyberte **Upravit** a upravte atributy na řádku. Alternativně, pokud byly hodnoty zadány ručně během zadávání transakce, můžete zvolit zadání výchozích systémových hodnot.
5. Vrátí se seznam transakcí a ve sloupci **Čeká na úpravu** se zobrazí zaškrtnutí, které označuje, kde byly provedeny změny. Veškeré úpravy, které mají nevyřízené změny, jsou zobrazeny v dolní polovině stránky. Zde můžete provést další podrobné změny nad rámec toho, co bylo zobrazeno na předchozí stránce.
6. Vyberte **Zaúčtovat** pro zaúčtování transakcí úprav.

V závislosti na konfiguraci se pro úpravu obvykle vytvářejí nové transakce.

- Pole **Stav úpravy** původní transakce je nastaven na **Upraveno**.
- Pro zrušení původní transakce je vytvořena stornovací transakce a pole **Stav** je nastaveno na **Upraveno**.
- Vytvoří se nová transakce se změnami, které byly provedeny během procesu úpravy.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Výběr více zaúčtovaných transakcí projektu najednou pro úpravy a dobropisy

Nová funkce, která byla představena ve verzi 10.0.30, umožňuje výběr více transakcí pro úpravu najednou na stránce **Zaúčtované transakce projektu**.

Než budete moci použít tuto funkci, musíte ji v systému zapnout. Správci mohou pomocí pracovního prostoru **Správa funkcí** zkontrolovat stav funkce a zapnout ji v případě potřeby. V pracovním prostoru **Správa funkcí** vyhledejte a vyberte **Vícenásobný výběr zaúčtovaných transakcí projektu pro úpravy a dobropisy** a poté vyberte **Zapnout**.

Tato funkce zapíná následující klíčové funkce:

- Lze k ní přistupovat ze stránky zaúčtované transakce v rámci projektu pomocí stávajícího tlačítka **Úprava**.
- Umožňuje ovládací prvek víceřádkového výběru na stránce **Zaúčtované transakce projektu**. Než začnete s úpravami, můžete na stránku seznamu použít filtry a vybrat své záznamy.
- Deaktivuje tlačítko **Úprava** , pokud nelze upravit jakoukoli jednotlivou transakci nebo pokud vyberete kombinaci dobropisů a deníků společně namísto jednotlivě.
- Kvůli přidání víceřádkového ovládacího prvku pro výběr již není odkaz **Potvrzené náklady** na pásu karet deaktivován, pokud je vybráno více řádků.
- Přidá následující varovnou zprávu: „Vybrali jste více než (vybraný počet) záznamů k úpravě. Provedení této akce může chvíli trvat. Opravdu chcete tuto akci provést?“

Tato funkce také odebere krok 2 z toku procesu, který byl popsán dříve v tomto článku. Proto všechny transakce, které byly vybrány před otevřením stránky **Upravit transakce** , budou zahrnuty do seznamu transakcí k úpravě. K jejich vyhledání nemusíte používat tlačítko **Vybrat**.

> [!NOTE] 
> I když je tato funkce deaktivována, stále můžete vybrat více záznamů pro úpravu. Pouze jeden záznam však *zůstane vybrán* a dialogové okno **Vybrat transakce** se zobrazí ihned poté, co vyberete možnost otevřít úpravy.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Stavy transakcí úprav, které lze aktivovat a deaktivovat pro úpravy

Následující stavy lze aktivovat a deaktivovat na kartě **Obecné** na stránce **Parametry řízení projektu a účetnictví**:

- Zaúčtováno
- Návrh faktury
- Fakturováno
- Odhadnuto
- Eliminováno
- Počáteční zůstatek (hodina)

## <a name="adjustment-parameters"></a>Parametry úprav

Tyto parametry jsou uvedeny na stránce **Projektové řízení a parametry účetnictví** na kartě **Obecné** pod skupinou **Úprava** a upraví chování pro způsob zpracování úprav. 

| Název parametru | Description |
|----------------|-------------
| Vždy vytvořit transakci úpravy | Pokud je tento parametr aktivován, proces úpravy vždy vytvoří novou transakci vrácení a novou upravenou transakci, pokud dojde k dopadu na finance nebo vykazování. Pokud je parametr deaktivován, proces úpravy aktualizuje původní transakci namísto vytvoření storna a nové transakce pro scénář, jako je aktualizace textu transakce. |
| Automaticky aktualizovat pole | Pokud je tento parametr aktivován, systém přepočítá nákladovou cenu a prodejní cenu. |
| Použít datum úpravy jako nový projekt | Tento parametr se používá k přesunutí transakcí do budoucího fiskální období, než systém tuto funkci podporoval. Nedoporučujeme ji používat, protože mění obchodní datum transakce a v budoucí verzi bude zastaralá. |
| Povolit uzavřené aktivity | Obvykle nelze vytvořit transakce pro uzavřené aktivity. Pokud je tento parametr aktivován, toto chování je potlačeno. K uzavřeným činnostem lze tedy vytvářet opravné položky. |
