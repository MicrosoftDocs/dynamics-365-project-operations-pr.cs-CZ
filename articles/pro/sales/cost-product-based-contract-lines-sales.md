---
title: Nákladové řádky smlouvy založené na produktu – omezené
description: Toto téma poskytuje informace o vytváření
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003533"
---
# <a name="cost-product-based-contract-lines---lite"></a>Nákladové řádky smlouvy založené na produktu – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_


Řádky smlouvy na základě produktu v Dynamics 365 Project Operations obsahují pole **Nákladová cena**, které ukládá nákladovou cenu produktu pro následné výpočty ziskovosti.

Když je pro katalogový produkt vytvořena produktový řádek smlouvy, náklady na řádek mají výchozí hodnoty z pole **Standardní náklady** v katalogu produktů. Pole **Standardní náklad** v katalogu produktů je nastaveno v základní měně organizace. Když jsou na řádku smlouvy výchozí jednotkové náklady, převedou se na měnu prodeje na smlouvě.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jednotková cena na řádku smlouvy na základě produktu

Mít jednotkový náklad na řádku smlouvy na základě produktu umožňuje různé náklady na produkt pro každou jednotku. I když to není vždy nutné, existují určité scénáře, kdy dodavatel může pro zákazníka zlevnit náklady na produkt. Zvažte následující scénář:

Fabrikam Robotics instaluje robotická ramena na montážní linky společnosti Adatum Corporation. Fabrikam poskytuje instalační služby, ale robotická ramena pocházejí od společnosti Trey Research. Pokud instalace robotických ramen ve společnosti Adatum Corporation otevře novou průmyslovou vertikálu pro robotická ramena společnosti Trey Research, může poskytnout speciální slevu na tento kontrakt společnosti Fabrikam. V tomto případě Fabrikam vytvoří produktovou smlouvu pro Robotic Arms. U této smlouvy se zadává jednotková cena. Cena se liší od nákladů na robotická ramena od společnosti Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]