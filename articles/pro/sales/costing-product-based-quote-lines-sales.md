---
title: Nákladové řádky nabídky založené na produktu
description: Toto téma poskytuje informace o použití nákladové ceny na řádku nabídky založené na produktu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c08ac3b0f24dda19489bad6e667a50b67b8ce3ec
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273640"
---
# <a name="costing-product-based-quote-lines"></a>Nákladové řádky nabídky založené na produktu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


Produktové řádky nabídek v Dynamics 365 Project Operations mají také pole také **Ceník**. Toto pole se používá ke sledování nákladové ceny produktu na řádku nabídky a pro výpočty následné ziskovosti.

Když je pro katalogový produkt vytvořen řádek nabídky založené na produktu, náklady na řádek nabídky založené na produktu jsou ve výchozím stavu přebírány z pole **Standardní náklady** v katalogu produktů. Pole standardních nákladů v katalogu produktů je nastaveno v základní měně organizace. Výchozí jednotková cena na řádku nabídky na základě produktu se převede na měnu prodeje v nabídce.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Jednotková cena na řádku nabídky na produktu

Účelem jednotkových nákladů na produktové nabídce je umožnit různé náklady na produkt pro každý prodej. Toto není typický scénář, ale někdy může dodavatel snížit cenu produktu v závislosti na zákazníkovi konečného prodeje.

Příklad:

Fabrikam Robotics instaluje robotická ramena na montážní linky společnosti A Datum Corporation. Fabrikam poskytuje instalační služby, ale robotická ramena jsou získávána z Trey Robotics. Pokud instalace robotických ramen ve společnosti A Datum Corporation otevře novou průmyslovou vertikálu pro robotická ramena společnosti Trey, mohl by Trey poskytnout speciální slevu na tento kontrakt společnosti Fabrikam.

V tomto případě Fabrikam vytvoří produktovou nabídku pro robotická ramena a pro tuto nabídku zadá speciální cenu za jednotku. Tato cena se liší od standardní ceny společnosti Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]