---
title: Dopad na skutečné hodnoty u zapojení s pevnou cenou
description: Tento téma poskytuje informace o dopadu na tabulku Skutečné hodnoty při různých událostech během životního cyklu zapojení s pevnou cenou v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579220"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Dopad na skutečné hodnoty u zapojení s pevnou cenou

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V následující tabulce jsou uvedeny skutečné hodnoty různých typů transakcí, které se vytvářejí při různých událostech v rámci zapojení s pevnou cenou.

| Zvláštní událost | Skutečné náklady | Skutečný nefakturovaný prodej | Skutečný fakturovaný prodej | Příklad |
|---|---|---|---|---|
| Je vytvořen čas. | Nelze použít | Nelze použít | Nelze použít | <p>Bob Kozack z organizační jednotky Fabrikam US, který stojí 100 USD za hodinu, pracuje na projektu s názvem „Instalace ARM ve společnosti Adatum“. Tento projekt je v řádku smlouvy namapován na metodu účtování s pevnou cenou. Zde je ukázkový časový záznam za uživatele Bob Kozak:</p><p>Bob Kozack - 8 hodin</p> |
| Čas je odeslán. | Nelze použít | Nelze použít | Nelze použít | Pro časový záznam se vytvoří řádek nákladového deníku. Výchozí nákladová sazba se zadá do deníkového záznamu. |
| Zadaný čas je před schválením odvolán. | Nelze použít | Nelze použít | Nelze použít | |
| Čas je schválen. | Vytvoří se skutečná cena. | Nelze použít | Nelze použít | <p>Nová skutečná hodnota, která je vytvořena:</p><ul><li>**Skutečná cena:** Bob Kozack, 8 hodin, 800 USD</li></ul> |
| Schválení času je zrušeno. | <p>Stav úpravy původních skutečných nákladů se aktualizuje na **Upraveno**.</p><p>Vytvoří se storno skutečné ceny, která má stav úpravy **Neupravitelné**.</p> | Nelze použít | Nelze použít | <p>Stávající skutečná cena, která je aktualizována:</p><ul><li>**Skutečná cena**: Bob Kozack, 8 hodin, 800 USD, *Upraveno*</li></ul><p>Nová skutečná hodnota, která je vytvořena pro storno předchozího finančního dopadu:</p><ul><li>**Skutečná cena**: Bob Kozack, (8 hodin), (800 USD), *Neupravitelné*</li></ul> |
| Zadaný čas je po schválení odvolán. | <p>Stav úpravy původních skutečných nákladů se aktualizuje na **Upraveno**.</p><p>Vytvoří se storno skutečné ceny, která má stav úpravy **Neupravitelné**.</p> | Nelze použít | Nelze použít | <p>Stávající skutečná cena, která je aktualizována:</p><ul><li>**Skutečná cena**: Bob Kozack, 8 hodin, 800 USD, *Upraveno*</li></ul><p>Nová skutečná hodnota, která je vytvořena pro storno předchozího finančního dopadu:</p><ul><li>**Skutečná cena**: Bob Kozack, (8 hodin), (800 USD), *Neupravitelné*</li></ul> |
| Smlouva není potvrzená. | <p>Stav úpravy starých skutečných nákladů se aktualizuje na **Upraveno**.</p><p>Vytvoří se storna skutečné ceny, která mají stav úpravy **Neupravitelné**.</p><p>Po přehodnocení smluvních pravidel se vytvoří nová skutečná cena.</p> | Nelze použít | Nelze použít | <p>Stávající skutečná cena, která je aktualizována:</p><ul><li>**Skutečná cena**: Bob Kozack, 8 hodin, 800 USD, *Upraveno*</li></ul><p>Nová skutečná hodnota, která je vytvořena pro storno předchozího finančního dopadu:</p><ul><li>**Skutečná cena**: Bob Kozack, (8 hodin), (800 USD), *Neupravitelné*</li></ul><p>Nová skutečná hodnota, která je vytvořena pro přehodnocený finanční dopad:</p><ul><li>**Skutečná cena:** Bob Kozack, 8 hodin, 800 USD</li></ul> |
| Faktura je vytvořena. | Nelze použít | Nelze použít | Nelze použít | |
| Faktura je potvrzena milníkem. | Nelze použít | Nelze použít | Jsou vytvořeny nové skutečné fakturované prodeje založené na milníku. | <p>Stávající skutečná hodnota, která zůstává nezměněna:</p><ul><li>**Skutečná cena:** Bob Kozack, 8 hodin, 800 USD</li></ul><p>Nová skutečná hodnota, která je vytvořena pro zaznamenání hodnot fakturovaného prodeje:</p><ul><li>**Skutečný fakturovaný prodej:** milník, 5 000 USD</li></ul> |
| Faktura je opravena pro připsání milníku. | Nelze použít | Nelze použít | Vytvoří se storno skutečného fakturovaného prodeje. | <p>Stávající skutečná hodnota, která zůstává nezměněna:</p><ul><li>**Skutečná cena:** Bob Kozack, 8 hodin, 800 USD</li></ul><p>Stávající skutečná cena, která je aktualizována:</p><ul><li>**Skutečný fakturovaný prodej**: milník, 5 000 USD, *Upraveno*</li></ul><p>Nová skutečná hodnota, která je vytvořena pro storno předchozích hodnot fakturovaného prodeje:</p><ul><li>**Skutečný fakturovaný prodej**: milník, (5 000 USD), *Neupravitelné*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
