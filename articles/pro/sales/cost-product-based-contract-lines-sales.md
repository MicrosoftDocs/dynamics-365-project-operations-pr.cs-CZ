---
title: Nákladové řádky smlouvy založené na produktu
description: Toto téma poskytuje informace o vytváření
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2020
ms.locfileid: "4074011"
---
# <a name="costing-product-based-contract-lines"></a>Nákladové řádky smlouvy založené na produktu

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_


Řádky smlouvy na základě produktu v Dynamics 365 Project Operations zahrnují pole **Nákladová cena** , kam se ukládá nákladová cena produktu pro následné výpočty ziskovosti.

Když je pro katalogový produkt vytvořen řádek smlouvy založené na produktu, náklady na řádek smlouvy založené na produktu jsou ve výchozím stavu přebírány z pole **Standardní náklady** v katalogu produktů. Pole **Standardní náklad** v katalogu produktů je nastaveno v základní měně organizace. Když jsou na řádku smlouvy výchozí jednotkové náklady, převedou se na měnu prodeje na smlouvě.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jednotková cena na řádku smlouvy na základě produktu

Mít jednotkový náklad na řádku smlouvy na základě produktu umožňuje různé náklady na produkt pro každou jednotku. I když to není vždy nutné, existují určité scénáře, kdy dodavatel může pro zákazníka zlevnit náklady na produkt. Zvažte následující scénář:

Fabrikam Robotics instaluje robotická ramena na montážní linky společnosti Adatum Corporation. Fabrikam poskytuje instalační služby, ale robotická ramena jsou získávána z Trey Research. Pokud instalace robotických ramen ve společnosti Adatum Corporation otevře novou průmyslovou vertikálu pro robotická ramena společnosti Trey Research, může poskytnout speciální slevu na tento kontrakt společnosti Fabrikam. V tomto případě Fabrikam vytvoří řádek smlouvy na základě produktu pro Robotic Arms a zadá jednotkové náklady na tuto smlouvu, které se liší od standardních nákladů na robotická ramena od Trey Research.
