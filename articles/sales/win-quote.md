---
title: Uzavření nabídky
description: Tento článek poskytuje informace o tom, jak zavírat nabídky v Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 45bdfe5fb9eddb8f96ed1bc017596c8fe436245e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931874"
---
# <a name="close-a-quote"></a>Uzavření nabídky

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Nabídku projektu lze uzavřít jako Získanou nebo Ztracenou. Koncept nabídky lze uzavřít, protože funkce Aktivace a Revize nabídek nejsou v Microsoft Dynamics 365 Project Operations podporovány.

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