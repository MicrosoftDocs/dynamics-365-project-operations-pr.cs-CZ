---
title: Nastavení nákladových a prodejních sazeb pro produkty katalogu – omezené
description: Toto téma poskytuje informace o tom, jak nastavit nákladové a prodejní sazby u položek v katalogu produktů.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996023"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Nastavení nákladových a prodejních sazeb pro produkty katalogu – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_


Nastavení cen pro položky katalogu produktů v Dynamics 365 Project Operations je stejné jako v Dynamics 365 Sales.

V Project Operations nelze produkty odhadovat ani používat na projektech, takže není nutné nastavovat ceny katalogů produktů v cenících projektů pro nabídky a smlouvy.

Použijte pole **Cena produktu** pole nabídky, smlouvy nebo účtu k nastavení cen katalogu produktů. Nenastavujte ceny katalogů produktů v cenících projektů. Projektové ceníky jsou exkluzivní funkcí aplikace Project Operations. Obchodní logika pro konkrétní aplikaci kopíruje ceníky z nabídky do smlouvy. Výsledkem je projektový ceník pro určitou smlouvu. Operace kopírování může zpozdit proces vyhrání nabídky, pokud bude projektový ceník nabídky příliš velký. Produktové ceníky se nekopírují, aby vytvořily vlastní ceníky ve smlouvách. Protože se nejedná o žádné kopírování, není ovlivněn výkon procesu nabídky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]