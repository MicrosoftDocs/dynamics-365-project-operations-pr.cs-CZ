---
title: Dopad na skutečné hodnoty u interního projektu
description: Tento článek poskytuje informace o dopadu na tabulku Skutečné hodnoty při různých událostech pro interní projekt v Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921340"
---
# <a name="actuals-impact-for-an-internal-project"></a>Dopad na skutečné hodnoty u interního projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V následující tabulce jsou uvedeny skutečné hodnoty různých typů transakcí, které se vytvářejí při různých událostech v rámci zapojení interního projektu.

| Zvláštní událost | Skutečné náklady | Příklad |
|---|---|---|
| Je vytvořen čas. | Nelze použít | <p>Bob Kozack z organizační jednotky Fabrikam US, který stojí 100 USD za hodinu, pracuje na projektu s názvem „Instalace ARM ve společnosti Adatum“. Tento projekt je v řádku smlouvy namapován na metodu účtování s pevnou cenou. Zde je ukázkový časový záznam za uživatele Bob Kozak:</p><p>Bob Kozack - 8 hodin</p> |
| Čas je odeslán. | Nelze použít | Pro časový záznam se vytvoří řádek nákladového deníku. Výchozí nákladová sazba se zadá do deníkového záznamu. |
| Zadaný čas je před schválením odvolán. | Nelze použít | |
| Čas je schválen. | Vytvoří se skutečná cena. | <p>Nová skutečná hodnota, která je vytvořena:</p><ul><li>**Skutečná cena:** Bob Kozack, 8 hodin, 800 USD</li></ul> |
| Schválení času je zrušeno. | <p>Stav úpravy původních skutečných nákladů se aktualizuje na **Upraveno**.</p><p>Vytvoří se storno skutečné ceny, která má stav úpravy **Neupravitelné**.</p> | <p>Stávající skutečná cena, která je aktualizována:</p><ul><li>**Skutečná cena**: Bob Kozack, 8 hodin, 800 USD, *Upraveno*</li></ul><p>Nová skutečná hodnota, která je vytvořena pro storno předchozího finančního dopadu:</p><ul><li>**Skutečná cena**: Bob Kozack, (8 hodin), (800 USD), *Neupravitelné*</li></ul> |
| Zadaný čas je po schválení odvolán. | <p>Stav úpravy původních skutečných nákladů se aktualizuje na **Upraveno**.</p><p>Vytvoří se storno skutečné ceny, která má stav úpravy **Neupravitelné**.</p> | <p>Stávající skutečná cena, která je aktualizována:</p><ul><li>**Skutečná cena**: Bob Kozack, 8 hodin, 800 USD, *Upraveno*</li></ul><p>Nová skutečná hodnota, která je vytvořena pro storno předchozího finančního dopadu:</p><ul><li>**Skutečná cena**: Bob Kozack, (8 hodin), (800 USD), *Neupravitelné*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
