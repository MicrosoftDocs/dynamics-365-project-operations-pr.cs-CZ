---
title: Nákladové řádky smlouvy založené na produktu – omezené
description: Tento článek obsahuje informace o vytváření
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a63ad12c081d19efde02303bf626184f8586d4a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922904"
---
# <a name="cost-product-based-contract-lines---lite"></a>Nákladové řádky smlouvy založené na produktu – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_


Řádky smlouvy na základě produktu v Dynamics 365 Project Operations obsahují pole **Nákladová cena**, které ukládá nákladovou cenu produktu pro následné výpočty ziskovosti.

Když je pro katalogový produkt vytvořena produktový řádek smlouvy, náklady na řádek mají výchozí hodnoty z pole **Standardní náklady** v katalogu produktů. Pole **Standardní náklad** v katalogu produktů je nastaveno v základní měně organizace. Když jsou na řádku smlouvy výchozí jednotkové náklady, převedou se na měnu prodeje na smlouvě.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jednotková cena na řádku smlouvy na základě produktu

Mít jednotkový náklad na řádku smlouvy na základě produktu umožňuje různé náklady na produkt pro každou jednotku. I když to není vždy nutné, existují určité scénáře, kdy dodavatel může pro zákazníka zlevnit náklady na produkt. Zvažte následující scénář:

Fabrikam Robotics instaluje robotická ramena na montážní linky společnosti Adatum Corporation. Fabrikam poskytuje instalační služby, ale robotická ramena pocházejí od společnosti Trey Research. Pokud instalace robotických ramen ve společnosti Adatum Corporation otevře novou průmyslovou vertikálu pro robotická ramena společnosti Trey Research, může poskytnout speciální slevu na tento kontrakt společnosti Fabrikam. V tomto případě Fabrikam vytvoří produktovou smlouvu pro Robotic Arms. U této smlouvy se zadává jednotková cena. Cena se liší od nákladů na robotická ramena od společnosti Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]