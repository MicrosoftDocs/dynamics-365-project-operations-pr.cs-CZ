---
title: Sady schválení
description: Tento článek vysvětluje, jak pracovat se sadami schválení, požadavky a podmnožinami těchto operací.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524908"
---
# <a name="approval-sets"></a>Sady schválení

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Sady schválení seskupují požadavky na schválení společně do menších podmnožin operací. Toto seskupení umožňuje zpracování schválení podle projektu v konkrétním pořadí a umožňuje opakování a sekvenování. Seskupení žádostí o schválení dohromady zvyšuje spolehlivost a sledovatelnost zpracování schválení pro velké objemy schválení.

Sady schválení označují celkový stav zpracování souvisejících záznamů. Když je záznam schválení zpracován pomocí sady schválení, záznam se přesune z **Odesláno** na **Schválený**, a již není propojen se sadou schválení. Pokud záznam selže při odeslání ke schválení, zůstane ve stavu **Odesláno** a sada schválení je označena jako neúspěšná. Sada schválení zaznamená chybovou zprávu o selhání.

## <a name="processing-approvals-and-approval-sets"></a>Zpracování schválení a sad schválení
Schválení, která jsou zařazena do fronty ke zpracování, jsou viditelná v pohledu **Zpracování schválení**. Systém zpracovává všechny položky vícekrát asynchronně, včetně opakování schválení, pokud předchozí pokusy selhaly.

Pole **Životnost sady schválení** zaznamenává počet pokusů zbývajících ke zpracování sady, než bude označena jako neúspěšná.

Sady schválení jsou zpracovávány prostřednictvím periodické aktivace na základě **cloudového toku** s názvem **Project Service - Souběžně naplánovat sady schválení projektu**. Ten se nachází v **řešení** s názvem **Project Operations**. 

Ujistěte se, že je tok aktivován, provedením následujících kroků.

1. Jako správce se přihlaste na webu [flow.microsoft.com](https://powerautomate.microsoft.com).
2. V pravém horním rohu se přepněte do prostředí, které používáte pro Dynamics 365 Project Operations.
3. Výběrem položky **Řešení** vypište seznam řešení, která jsou nainstalována v prostředí.
4. V seznamu řešení vyberte položku **Project Operations**.
5. Změňte filtr z **Vše** na **Cloudové toky**.
6. Zkontrolujte, že je tok **Project Service - Souběžně naplánovat sady schválení projektu** nastaven na **Zapnuto**. Pokud tomu tak není, vyberte tok a poté vyberte **Zapnout**.
7. Zkontrolujte, zda ke zpracování dochází každých pět minut, a to kontrolou seznamu **Systémové úlohy** v oblasti **Nastavení** vašeho prostředí Project Operations v Dataverse.

## <a name="failed-approvals-and-approval-sets"></a>Neúspěšná schválení a sady schválení
Zobrazení **Neúspěšná schválení** obsahuje všechna schválení, která vyžadují zásah uživatele. Otevřete související protokoly sady schválení a zjistěte příčinu selhání.
Výběr možnosti **Opakovat** zvýší celkový počet sady schválení, přesune sadu schválení zpět do stavu **Zpracovává se** a pokusí se zpracovat zbývající záznamy.

## <a name="configure-approval-sets"></a>Konfigurace sad schválení

### <a name="enable-the-approval-sets-feature"></a>Aktivace funkce sad schválení
Než aktivujete funkci sad schválení, ověřte, zda v současné době nejsou zpracovávána žádná schválení. Po povolení této funkce ji nelze zakázat.

- Přejděte na stránku **Parametry projektu** stránku a vyberte **Ovládání funkcí** > **Aktivovat moderní schválení**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurace asynchronního prahu 
Když jsou vytvořeny sady schválení, zpracování se přesune na pozadí, když vybraný počet záznamů ke schválení překročí uvedenou prahovou hodnotu. Použijte pole **Asynchronní prahová hodnota** pro konfiguraci, kdy má být zpracování schválení spuštěno synchronně nebo asynchronně. Vyberte jednu z následujících hodnot:

  - Nula: Všechny požadavky by měly být zpracovávány asynchronně. 
  - Čísla větší než nula: Schválení se zpracovávají asynchronně, pouze pokud zadaný počet schválení překročí tuto hodnotu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
