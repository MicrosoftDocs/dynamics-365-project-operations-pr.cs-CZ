---
title: Co je nového, březen 2022 - omezené nasazení Project Operations
description: Toto téma poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z března 2022 pro omezené nasazení.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583742"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Co je nového, březen 2022 - omezené nasazení Project Operations

_Platí pro: Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.30.0.99

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

- Subdodávky: Tvorba dodavatelských faktur a zkušenosti s párováním

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Čas a výdaje | 2388011 | Při hromadném schvalování zobrazit předkladatelům zadání času komentáře k zamítnutí. |
| Plánování a sledování projektu | 2495294 | Podrobnosti projektu nesmí být upravitelné na stránce **Podrobnosti úkolu**. |
| Fakturace a ceny | 2499605 | Milníky smlouvy, které jsou vytvořeny z milníků nabídek, jsou nesprávně označeny jako pouze pro čtení. |
| Plánování a sledování projektu | 2506050 | Pokud nedojde k žádné změně k uložení, sada operací zůstane nevyřízená po dobu jedné hodiny. Sada je pak nesprávně označena jako **Nezdařilo se**, přičemž by měla být dokončena okamžitě. |
| Fakturace a ceny | 2507401 | Výchozí smluvní jednotky jsou v projektech nesprávně zadány z důvodu nesprávného ukládání do mezipaměti. |
| Fakturace a ceny | 2541660 | **Ověření vytvoření prodejní objednávky** v duálním zápisu by mělo být pouze pro zakázky založené na projektu. |
| Fakturace a ceny | 2552745 | Daň se nerozděluje mezi zákazníky, kteří si nastavili pravidla rozdělené fakturace. |
| Fakturace a ceny | 2558859 | Vylepšené chybové zprávy při nastavování dimenzí cen. |
| Fakturace a ceny | 2558933 | **Import z odhadů projektu** selže, když **msdyn\_projekt** je přidáno jako cenová dimenze. |
| Fakturace a ceny | 2559101 | Smazání parametru projektu není blokováno a způsobuje problémy. |
| Správa příležitostí | 2570390 | Zásuvný modul pro duální zápis vynucuje typ účtu u nabídek, objednávek a příležitostí **Zákazník**, i když tento typ účtu není správný. |
| Fakturace a ceny | 2586097 | Skutečné hodnoty rozdělených fakturovaných nákladů nejsou stornovány, když je projekt odstraněn z řádku projektové smlouvy. |
| Fakturace a ceny | 2589619 | Daň ze zapsaného materiálu se přenáší do nevyfakturovaných skutečných prodejů a faktury. |
| Správa příležitostí | 2594015 | Cenovou nabídku nelze uzavřít jako vyhranou pro zákazníky, kteří mají platební podmínky **Net60**. |
| Plánování a sledování projektu | 2595841 | V aplikaci Project for the Web uživatelé obdrží chybovou zprávu o chybějící **msdyn\_actualstart**, když vytvoří nový požadavek na zdroj. |
| Čas a výdaje | 2602511 | Pole **Odmítnuto uživatelem** pro zadání času ukazuje **Systém** místo pojmenovaného uživatele jako odmítajícího. |
| Čas a výdaje | 2602528 | Schvalovatel projektu může schvalovat čas na projektech, kde není uveden jako schvalovatel. |
| Fakturace a ceny | 2608550 | Opravnou fakturu lze potvrdit i v případě, že nedošlo k žádným změnám oproti originálu. |

## <a name="removed-and-deprecated-features"></a>Odstraněné a zastaralé funkce

Téma [Odebrané nebo zastaralé funkce v Project Operations](../../whats-new/removed-depreciated-features-project.md) popisuje funkce, které byly odstraněny nebo které byly zastaralé pro Dynamics 365 Project Operations.

- Odebraná funkce již v produktu není k dispozici.
- Zastaralá funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Oznámení o zastarání se objeví v tématu [Odebrané nebo zastaralé funkce v Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 měsíců před odebráním funkce z produktu.
