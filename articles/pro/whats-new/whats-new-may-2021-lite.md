---
title: Co je nového, květen 2021 – omezené nasazení Project Operations
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z května 2021 pro omezené nasazení.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a5d67159b732e0309e03c64fb6dadcc7b8cbff51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934174"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Co je nového, květen 2021 – omezené nasazení Project Operations

_Platí pro: Omezené nasazení – od obchodu po pro forma fakturaci_

Tento článek se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

   - Project Operations v prostředí Dataverse verze 4.10.0.186.

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

V této vydané verzi jsou zahrnuty následující funkce:

- [Režimy plánování](../../project-management/scheduling-modes.md): Projektoví manažeři nyní mohou definovat, zda by měl být projekt řízen pomocí fixního trvání, pevné práce nebo režimu plánování pevných jednotek.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| Fakturace a ceny | 2224568 | Přidaná logika povolující přizpůsobení, která zahrnuje vyvolání doplňku pro potvrzení faktury. |
| Fakturace a ceny | 2101098 | Vylepšena logika výchozích polí proforma faktury. Mezi tato pole patří **Fakturační adresa**, **Fakturační jméno** a **Platební podmínky**. Pole mají nyní výchozí hodnotu z příslušného záznamu zákazníka smlouvy o projektu. |
| Fakturace a ceny | 2021413 | Aktualizována pole **Skutečná cena** a **Prodeje** u entity **Úkol**, která nově zahrnují hodnoty prodeje z nevyfakturovaných a fakturovaných výdajů na úkoly. |
| Fakturace a ceny | 2182110 | Při kopírování projektové smlouvy se ID řádku smlouvy znovu vygeneruje v cílové projektové smlouvě, aby se zajistilo, že je jedinečné. |
| Správa příležitostí | 2186741 | Přidaná ověření, která zajišťují, že u polí **Původ** a typ transakce nelze aktualizovat existující podrobnosti řádku nabídky. |
| Správa příležitostí | 2191353 | Vytváření milníků nesmí být povoleno na řádku smlouvy s časem a materiálem. |
| Správa příležitostí | 2216956 | Opraveny problémy ve funkci **Aktualizovat ceny**. |
| Plánování a sledování | 2182979 | Vylepšena funkce kopírování projektu, aby bylo zajištěno, že řádky odhadu výdajů budou zkopírovány z původního projektu. |
| Plánování a sledování | 2184144 | Vylepšena funkce kopírování projektu, aby bylo zajištěno, že název pozice zdroje bude zkopírován z původního projektu. |
| Plánování a sledování | 2184799 | Zpřísněna kontrola při kopírování projektu zajišťující, že odhadované datum zahájení nelze během kopírování změnit. |
| Plánování a sledování | 2185134 | Během kopírování projektu odhadované datum zahájení cílového projektu je nastaveno na dnešní datum. |
| Plánování a sledování | 2196373 | Zajištění, aby záznamy projektového manažera a člena týmu nebyly v projektovém týmu duplikovány při kopírování projektu. |
| Plánování a sledování | 2211833 | Přiřazení zdrojů se zkopírují z úlohy zdrojového projektu do cílového projektu. |
| Plánování a sledování | 2186541 | Opraveny problémy v mřížce **Odhady** při seskupování podle **Zdroje**. |
| Plánování a sledování | 2166906 | Kategorie transakcí z úkolu musí být zkopírována do entity **Přiřazení zdrojů**. |
| Správa zdrojů | 2125362 | Opraveny problémy při vytváření obecného člena týmu pomocí metody přidělování podle hodin. |
| Čas a výdaje | 2113603 | Opraven problém související s přizpůsobením při odstraňování atributů ze stránky **Zadání času**. Systém nyní před přístupem k atributu s využitím skriptu zkontroluje, zda atribut na stránce existuje. |
| Čas a výdaje | 2204377 | Zkopírované časové rozvrhy se musí automaticky zobrazit, když vyberete možnost **Kopírovat týden**. |
| Čas a výdaje | 2209059 | Pole **Stav** lze u časových údajů Dynamics 365 Field Service upravit. |
