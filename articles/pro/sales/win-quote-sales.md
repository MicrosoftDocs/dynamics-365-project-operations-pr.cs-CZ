---
title: Uzavření nabídek
description: Toto téma poskytuje informace o uzavření nabídky v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073701"
---
# <a name="close-quotes"></a>Uzavření nabídek 

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Nabídku projektu lze uzavřít jako Získanou nebo Ztracenou. Operace Aktivovat and Revidovat v nabídkách nejsou v Microsoft Dynamics 365 Project Operations podporovány, takže lze koncept nabídky uzavřít.

## <a name="close-a-quote-as-won"></a>Uzavření nabídky jako získané

Uzavření nabídky projektu jako získané zavře nabídku se stavem nastaveným na Uzavřeno a důvodem stavu nastaveným na Získáno. Uzavřením se nabídka projektu nastaví jako jen pro čtení a vytvoří se návrh smlouvy o projektu, který obsahuje informace o nabídce. Protože uzavřenou nabídku nelze znovu otevřít, zobrazí se potvrzovací dialog Před provedením změn existuje potvrzovací dialog, protože uzavřenou nabídku nelze znovu otevřít a změny jsou nevratné.

Pokud je nabídka připojena k příležitosti, jakékoli jiné projektové nabídky příležitosti budou automaticky uzavřeny jako Ztraceno.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finanční dopad uzavření nabídky jako získané

Pokud na projektu byly zaznamenané nějaké skutečné hodnoty v době, kdy je ještě připojený ke konceptu nabídky, zaznamenají se pouze náklady na čas nebo výdaje. Po uzavření nabídky jako získané aplikace refaktoruje náklady obrácením starších údajů o nákladech a opětovným vytvořením nových údajů o nákladech. Aplikace zpracuje tyto údaje o nákladech na základě metody fakturace příslušného řádku smlouvy projektu. Pokud skutečná cena odkazuje na řádek smlouvy o čase a materiálu, systém automaticky vytvoří odpovídající nevyfakturované prodejní skutečné hodnoty, když je nabídka uzavřena a je vytvořena smlouva o projektu. Pokud skutečné náklady odkazují na řádek smlouvy s pevnou cenou, aplikace přestane přepracovávat skutečné náklady na základě pravidel rozdělené fakturace pro zákazníky smlouvy o projektu.

## <a name="closing-a-quote-as-lost"></a>Uzavření nabídky jako ztracené:

Uzavřením nabídky projektu jako ztracené nastavíte stav na Zavřeno a důvod stavu na Ztraceno. Uzavřením se nabídka projektu nastaví jako jen pro čtení. Protože uzavřenou nabídku nelze znovu otevřít, před uzavřením nabídky jsou změny potvrzeny v potvrzovacím dialogu.

Pokud má projektová nabídka, která je uzavřená jako ztracená, obsahuje na některé z řádků odkazovaný projekt, je tento projekt také označený jako uzavřený a veškeré rezervace zdrojů od daného dne dále jsou zrušeny.

> [!NOTE]
> V Project Operations nebude mít uzavření nabídky jako získané nebo ztracené vliv na tento stav příležitosti, která zůstane otevřená, dokud nebude ručně uzavřena.
