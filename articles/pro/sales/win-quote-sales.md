---
title: Uzavření nabídky – omezené
description: Toto téma poskytuje informace o uzavření nabídky v aplikaci Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764856"
---
# <a name="close-a-quote---lite"></a>Uzavření nabídky – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Nabídku projektu lze uzavřít jako Získanou nebo Ztracenou. Koncept nabídky lze uzavřít, protože operace Aktivace a Revize nabídek nejsou v Microsoft Dynamics 365 Project Operations podporovány.

## <a name="close-a-quote-as-won"></a>Uzavření nabídky jako získané

Když zavřete nabídku projektu jako vyhraná, stav je nastaven na uzavřeno a důvod stavu je vyhraná. Uzavřením se nabídka projektu nastaví jako jen pro čtení a vytvoří se návrh smlouvy o projektu, který obsahuje informace o nabídce. Protože uzavřenou nabídku nelze znovu otevřít, potvrzovací dialog potvrdí vaše změny.

Pokud je nabídka připojena k příležitosti, jakékoli jiné projektové nabídky příležitosti budou automaticky uzavřeny jako Ztraceno.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finanční dopad uzavření nabídky jako získané

Pokud jsou na projektu nějaké skutečné údaje, zatímco je stále připojen ke konceptu nabídky, zaznamenají se pouze náklady na čas nebo výdaj. Po uzavření nabídky jako získané aplikace refaktoruje náklady obrácením starších údajů o nákladech a opětovným vytvořením nových údajů o nákladech. Aplikace zpracuje tyto údaje o nákladech na základě metody fakturace příslušného řádku smlouvy projektu. Pokud skutečná cena odkazuje na řádek smlouvy času a materiálu, vytvoří se odpovídající nevyfakturované prodejní skutečné hodnoty, když je nabídka uzavřena a je vytvořena smlouva o projektu. Pokud skutečné náklady odkazují na řádek smlouvy s pevnou cenou, aplikace přestane přepracovávat skutečné náklady, které jsou založeny na pravidlech rozdělené fakturace pro zákazníky smlouvy o projektu.

## <a name="closing-a-quote-as-lost"></a>Uzavření nabídky jako ztracené:

Když zavřete nabídku projektu jako prohraná, stav je nastaven na uzavřeno a důvod stavu je prohraná. Uzavřením se nabídka projektu nastaví jako jen pro čtení. Protože uzavřenou nabídku nelze znovu otevřít, před uzavřením nabídky jsou změny potvrzeny v potvrzovacím dialogu.

Pokud nabídka projektu, která je uzavřena jako Prohraná, odkazuje na projekt na kterémkoli z jejích řádků, je tento projekt také označen jako Uzavřený. Veškeré rezervace zdrojů od daného dne budou zrušeny.

> [!NOTE]
> V Project Operations nebude mít uzavření nabídky jako získané nebo ztracené vliv na tento stav příležitosti, která zůstane otevřená, dokud nebude ručně uzavřena.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]