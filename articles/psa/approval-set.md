---
title: Sady schválení v Project Service Automation
description: Tento téma poskytuje informace o sadě schválení, požadavcích a podmnožinách těchto operací.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9a7a9efbd8615f4923c6795a16c9cf98a40362b6
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323543"
---
# <a name="approval-sets-in-project-service-automation"></a>Sady schválení v Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sady schválení seskupují požadavky na schválení společně do menších podmnožin operací. Toto seskupení umožňuje zpracování schválení v pořadí podle projektu a umožňuje opakování a řazení. Seskupení zlepšuje spolehlivost a sledovatelnost zpracování schválení pro velké objemy schválení.

Sady schválení označují celkový stav zpracování souvisejících záznamů. Když je záznam o schválení zpracován pomocí sady schválení, záznam se přesune z **Odesláno** na **Schváleno** a je odpojen od sady schválení. Pokud záznam selže při odeslání ke schválení, zůstane ve stavu **Odesláno** a sada schválení je označena jako neúspěšná. Sada schválení zaznamená chybovou zprávu o selhání.

## <a name="processing-approvals-and-approval-sets"></a>Zpracování schválení a sad schválení
Schválení, která jsou zařazena do fronty ke zpracování, jsou viditelná v pohledu **Zpracování schválení**. Systém se pokusí zpracovat všechny položky několikrát asynchronně, včetně opakování pokusu o schválení, pokud předchozí pokusy selhaly.

Pole **Životnost sady schválení** zaznamenává počet pokusů zbývajících ke zpracování sady, než bude označena jako neúspěšná.

## <a name="failed-approvals-and-approval-sets"></a>Neúspěšná schválení a sady schválení
Zobrazení **Neúspěšná schválení** obsahuje seznam všech schválení, která vyžadují zásah uživatele. Otevřete související protokoly sady schválení a zjistěte příčinu selhání.
Výběr možnosti **Opakovat** zvýší celkový počet sady schválení, přesune sadu schválení zpět do stavu **Zpracovává se** a pokusí se zpracovat zbývající záznamy.

## <a name="configure-approval-sets"></a>Konfigurace sad schválení

###  <a name="enable-the-approval-sets-feature"></a>Aktivace funkce sad schválení
Než aktivujete funkci sad schválení, ověřte, zda v současné době nejsou zpracovávána žádná schválení.

- Přejděte na stránku **Parametry projektu** stránku a vyberte **Ovládání funkcí** > **Aktivovat moderní schválení**.

### <a name="turn-off-the-approval-sets-feature"></a>Vypnutí funkce sad schválení
Než vypnete funkci sad schválení, ověřte, zda v současné době nejsou zpracovávána žádná schválení.

- Přejděte na stránku **Parametry projektu** stránku a vyberte **Ovládání funkcí** > **Deaktivovat moderní schválení**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurace asynchronního prahu 
Když jsou vytvořeny sady schválení, zpracování se přesune na pozadí, když vybraný počet záznamů ke schválení překročí uvedenou prahovou hodnotu. Použijte pole **Asynchronní prahová hodnota** pro konfiguraci, kdy má být zpracování schválení spuštěno synchronně nebo asynchronně.
Platné hodnoty jsou:

  - Nula: Všechny požadavky by měly být zpracovávány asynchronně. 
  - Čísla větší než nula: Schválení se zpracovávají asynchronně, pouze pokud zadaný počet schválení překročí tuto hodnotu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
