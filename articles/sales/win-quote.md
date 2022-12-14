---
title: Uzavření nabídek na základě projektu
description: Tento článek poskytuje informace o tom, jak zavírat nabídky v Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b35417d4258a1e837fdf7a61bbcc303ec04a900
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824208"
---
# <a name="close-project-based-quotes"></a>Uzavření nabídek na základě projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Nabídku projektu lze uzavřít jako **získanou** nebo **ztracenou**. 

## <a name="close-a-quote-as-won"></a>Uzavření nabídky jako získané

Uzavření nabídky projektu jako získané nastaví stav nabídky na **Uzavřená** a důvod stavu na **Získaná**. Uzavřením se nabídky projektu nastaví jako jen pro čtení a vytvoří se návrh smlouvy o projektu, který obsahuje všechny informace o nabídce. Protože uzavřenou nabídku nelze znovu otevřít, před uzavřením nabídky jsou změny potvrzeny v potvrzovacím dialogu.

Smlouva o projektu vytvořená z nabídky projektu je také k dispozici v části Řízení projektů a účetnictví modulu Project Operations. Pokud smlouva o projektu není namapována na projekt na žádném z jeho řádků, je tato smlouva o projektu zpřístupněna jako neaktivní smlouva o projektu a stane se aktivní, jakmile je projekt namapován na alespoň jednu ze svých řádků smlouvy.

Pokud je nabídka připojena k příležitosti, jakékoli jiné projektové nabídky příležitosti budou automaticky uzavřeny jako Ztraceno.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finanční dopad uzavření nabídky jako získané

Pokud na projektu byly zaznamenané nějaké skutečné hodnoty v době, kdy je ještě připojený ke konceptu nabídky, zaznamenají se pouze náklady na čas nebo výdaje. Po uzavření nabídky jako získané aplikace refaktoruje náklady obrácením starších údajů o nákladech a opětovným vytvořením nových údajů o nákladech. Aplikace zpracuje tyto údaje o nákladech na základě metody fakturace příslušného řádku smlouvy projektu. Pokud skutečná cena odkazuje na řádek smlouvy o čase a materiálu, systém automaticky vytvoří odpovídající nevyfakturované prodejní skutečné hodnoty, když je nabídka uzavřena a je vytvořena smlouva o projektu. Pokud skutečné náklady odkazují na řádek smlouvy s pevnou cenou, aplikace přestane přepracovávat skutečné náklady na základě pravidel rozdělené fakturace pro zákazníky smlouvy o projektu.

Všechny přepracované skutečné hodnoty jsou k dispozici v modulu Řízení projektu a účetnictví pro účetního, který je může zkontrolovat, aktualizovat a zaúčtovat do hlavní knihy. 

## <a name="close-a-quote-as-lost"></a>Uzavření nabídky jako ztracené

Uzavřením nabídky projektu jako ztracené nastavíte stav na **Zavřeno** a důvod stavu na **Ztraceno**. Uzavřením se nabídka nastaví jako jen pro čtení. Protože uzavřenou nabídku nelze znovu otevřít, před uzavřením nabídky jsou změny potvrzeny v potvrzovacím dialogu.

Pokud má projektová nabídka, která je uzavřená jako ztracená, obsahuje na některé z řádků odkazovaný projekt, je tento projekt také označený jako uzavřený a veškeré rezervace zdrojů od daného dne dále jsou zrušeny.

> [!NOTE]
> V Project Operations nebude mít uzavření nabídky jako získané nebo ztracené vliv na tento stav příležitosti, která zůstane otevřená, dokud nebude ručně uzavřena.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
