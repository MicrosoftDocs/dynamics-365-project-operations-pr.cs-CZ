---
title: Záhlaví příležitosti
description: Toto téma popisuje celkové informace o obchodech založených na projektu a řádcích příležitostí založených na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073708"
---
# <a name="opportunity-header"></a>Záhlaví příležitosti

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Záhlaví příležitosti zachycuje celkové informace o obchodu založeném na projektu, které platí pro všechny řádky příležitosti založené na projektu.

Příležitosti založené na projektu v Dynamics 365 Project Operations jsou rozšířením příležitostí v aplikaci Dynamics 365 Sales. Tato rozšíření poskytují další funkce, které jsou specifické a vyžadované u příležitostí založených na projektu. Tato rozšíření mohou zahrnovat nová pole a akce pásu karet, které jsou dostupné v příležitostech založených na projektu. Některá pole, funkčnost nebo výchozí logika, která je k dispozici v Sales, nemusí být dostupná v aplikaci v Project Operations.

Následující tabulka obsahuje pole v příležitosti založené na projektu, která jsou buď jedinečná pro aplikaci Project Operations, nebo se jejich chování významně liší od chování příležitostí v aplikaci Sales.

| **Pole** | **Umístění** | **Relevance, účel a vedení** | **Dopad na následné složky** |
| --- | --- | --- | --- |
| Typ | Karta Obecné (skrytá) | Toto pole sady možností obsahuje následující možnosti:</br>- Na základě práce (k dispozici pouze v Project Operations)</br>- Na základě zboží (k dispozici pouze v případě, že jsou nainstalovány aplikace Project Operations a Sales)</br>- Na základě servisní údržby (k dispozici, když je nainstalována služba Field Service) | Když použijete aplikaci Project Operations, hodnota tohoto pole se automaticky nastaví na **Na základě práce** , takže příležitost je klasifikována jako projektová. Příležitost by měla být založená na projektu, aby byla povolena všechna rozšíření a funkce specifické pro projekt v procesu následného prodeje pro tento obchod. |
| Kontakt | Karta Obecné | Odkaz na primární kontakt zákazníka pro tento obchod. | |
| Účet | Karta Obecné | Odkaz na záznam společnosti nebo účtu zákazníka. | |
| Manažer obchodních vztahů | Karta Obecné | Jméno správce účtu pro tuto příležitost založenou na projektu. | Manažer obchodních vztahů je zodpovědný za řízení vztahu se zákazníkem až do dokončení tohoto projektu. Smluvní jednotka je nastavena na výchozí hodnoty na základě záznamu rezervovatelného zdroje svázaného se správcem účtu. |
| Smluvní jednotka | Karta Obecné | Organizační jednotka, která je odpovědná za realizaci projektu či projektů asociovaných s tímto obchodem. | Smluvní jednotka je divize společnosti, která dokončí projekty po uzavření obchodu. Každá smluvní jednotka má měnu a tato měna se používá k vykazování odhadovaných a skutečných nákladů vzniklých během projektu. |

Další informace o všech ostatních polích a sekcích na kartě **Souhrn** příležitosti najdete v tématu [Vytváření nebo úprava příležitostí (Sales a Centrum prodeje)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).
