---
title: Nastavení nákladových a prodejních sazeb pro katalogové produkty
description: Toto téma poskytuje informace o tom, jak nastavit nákladové a prodejní sazby u položek v katalogu produktů.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073847"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Nastavení nákladových a prodejních sazeb pro katalogové produkty

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_


Stanovení cen u položek v katalogu produktů v Dynamics 365 Project Operations je stejné jako v Dynamics 365 Sales.

Protože produkty nelze odhadnout ani použít v projektech Project Operations, není nutné nastavovat katalogové ceny produktů v projektových cenících pro nabídky a smlouvy.

Katalogové ceny produktů by měly být stanoveny v poli **Cena produktu** nabídky, smlouvy nebo účtu. Nenastavujte katalogové ceny produktů v projektových cenících pro tyto entity. Projektové ceníky jsou exkluzivní funkcí aplikace Project Operations. Existuje obchodní logika pro konkrétní aplikaci, která kopíruje ceníky z nabídky do smlouvy. Výsledkem je projektový ceník pro určitou smlouvu. Operace kopírování může zpozdit proces vyhrání nabídky, pokud bude projektový ceník nabídky příliš velký. Produktové ceníky se nekopírují, aby vytvořily vlastní ceníky ve smlouvách. To znamená, že produktové ceníky nemají vliv na výkon procesu vyhrání nabídky.
