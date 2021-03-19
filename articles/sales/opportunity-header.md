---
title: Záhlaví/souhrn příležitosti
description: Toto téma poskytuje informace o obchodech založených na projektu a řádcích příležitostí založených na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c58c3696ae03e8a33a25a9483825a4b7cbf850be
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277690"
---
# <a name="opportunity-settings"></a>Nastavení příležitosti

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_


Záhlaví nebo souhrn příležitosti zachycuje celkové informace o obchodu založeném na projektu, které platí pro všechny řádky příležitosti založené na projektu.

Příležitosti založené na projektu v Dynamics 365 Project Operations jsou rozšíření příležitostí v Dynamics 365 Sales. Tato rozšíření poskytují další funkce, které jsou specifické a vyžadované u příležitostí založených na projektu. Tato rozšíření mohou zahrnovat nová pole a akce pásu karet, které jsou dostupné v příležitostech založených na projektu. Některá pole, funkčnost nebo výchozí logika, která je k dispozici v Sales, nemusí být dostupná v aplikaci v Project Operations.

Následující tabulka obsahuje pole v příležitosti založené na projektu, která jsou buď jedinečná pro aplikaci Project Operations, nebo se jejich chování významně liší od chování příležitostí v aplikaci Sales.

| **Pole** | **Umístění** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- | --- |
| Typ | Karta Obecné (skrytá) | Toto pole sady možností obsahuje následující možnosti:</br>- Na základě práce (k dispozici pouze v Project Operations)</br>- Na základě zboží (k dispozici pouze v případě, že jsou nainstalovány aplikace Project Operations a Sales)</br>- Na základě servisní údržby (k dispozici, když je nainstalována služba Field Service) | Když použijete aplikaci Project Operations, hodnota tohoto pole se automaticky nastaví na **Na základě práce**, takže příležitost je klasifikována jako projektová. Příležitost by měla být založená na projektu, aby byla povolena všechna rozšíření a funkce specifické pro projekt v procesu následného prodeje pro tento obchod. |
| Vlastnící společnost | Karta Obecné | Toto je společnost nebo právnická osoba, která dodá projekt zákazníkovi. | Informace v tomto poli budou zkopírovány do odpovídajícího pole v projektové nabídce, která je vytvořena z této příležitosti. |
| Kontakt | Karta Obecné | Odkaz na primární kontakt zákazníka pro tento obchod. | |
| Účet | Karta Obecné | Odkaz na záznam společnosti nebo účtu zákazníka. | |
| Manažer obchodních vztahů | Karta Obecné | Jméno správce účtu pro tuto příležitost založenou na projektu. | Manažer obchodních vztahů je zodpovědný za řízení vztahu se zákazníkem až do dokončení tohoto projektu. Smluvní jednotka je nastavena na výchozí hodnoty na základě záznamu rezervovatelného zdroje svázaného se správcem účtu. |
| Smluvní jednotka | Karta Obecné | Organizační jednotka, která je odpovědná za realizaci projektu či projektů asociovaných s tímto obchodem. | Smluvní jednotka je divize společnosti, která dokončí projekty po uzavření obchodu. Každá smluvní jednotka má měnu a tato měna se používá k vykazování odhadovaných a skutečných nákladů vzniklých během projektu. |

Další informace o všech ostatních polích a sekcích na kartě **Souhrn** příležitosti najdete v tématu [Vytváření nebo úprava příležitostí (Sales a Centrum prodeje)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).


[!INCLUDE[footer-include](../includes/footer-banner.md)]