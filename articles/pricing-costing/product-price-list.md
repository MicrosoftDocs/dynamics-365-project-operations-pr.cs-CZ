---
title: Produktové ceníky
description: Tento článek poskytuje informace o cenících v katalogových cenách používaných v projektových nabídkách a smlouvách.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 68203f5adf7bf41d97e662e335d481ccac959ed6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917614"
---
# <a name="product-price-lists"></a>Produktové ceníky

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

 V Project Operations podporují **Ceníky produktů** a související entity položek ceníku funkčnost pro oceňování produktů na základě řádků nabídek a smluv založených na produktu. U produktů použitých na projektech se používají záznamy položek ceníku pro projektové ceníky. 

Produkty by měly být nastaveny tak, aby měly v katalogu produktů výchozí nákladové ceníky a ceníky. Ke konfiguraci výchozích nákladových cen a ceníků použijte ceníkovou cenu, standardní cenu a aktuální cenu. Výchozí ceníky se používají na řádku nabídky nebo řádku projektové smlouvy pouze v případě, že systém nemůže pro tento produkt najít řádek ceníku v produktovém ceníku pro nabídku nebo projektovou smlouvu.

Nákladová cena řádků katalogu produktů může být změněna mezi nabídkami. Tato možnost je důležitá, protože pokud přesně nesledujete náklady, nemůžete u učastí na projektu určit provozní zisky. Ve výchozím nastavení se standardní cena produktu používá jako nákladová cena. Výchozí nákladovou cenu je však možné na řádku nabídky aktualizovat, pokud pro tuto nabídku existuje jiná nákladová cena.

## <a name="price-list-items"></a>Položky ceníku

Produkty z katalogu produktů můžete přidat do různých ceníků. Řádky ceníku pro produkty vždy odkazují na určitou jednotku. Ocenění produktu v položkách ceníku lze konfigurovat jako částku v měně. Alternativně může být nakonfigurována jako funkce ceníku, aktuální ceny nebo standardní ceny.

Funkčnost ocenění podporuje různé možnosti zaokrouhlení, pokud jsou ceny produktů konfigurovány jako funkce ceníku, standardní ceny nebo aktuální ceny. Kromě využití více způsobů ocenění a možností zaokrouhlení můžete k položkám ceníku přidružit seznamy slev. 

 
## <a name="default-product-price-list"></a>Výchozí ceník produktu
Každý záznam zákazníka obsahuje pole **Výchozí ceník**, ve kterém můžete určit ceník, který odpovídá měně zákazníka. Do tohoto pole nevloží automaticky výchozí hodnota. Pokud existuje vlastní cenová dohoda s určitým zákazníkem, můžete toto pole použít k přidružení ceníku k tomuto zákazníkovi.

Entity Příležitost, Nabídka a Projektová smlouva používají k zadávání výchozích ceníků produktů následující pořadí. Stejné pořadí se používá pro projektové ceníky.

1.  Nabídka
2.  Příležitost
3.  Zákazník
4.  Globální nastavení 

Ve výchozím nastavení uvádí pole **Produkt** na řádku nabídky všechny aktivní produkty v ceníku produktu nabídky. Pokud byl produkt inaktivován nebo pokud se jedná o koncept produktu, není v seznamu uveden, i když je v ceníku. 

Řádky katalogu produktů jsou přidány jako řádky faktury v první faktuře, která je vytvořena pro projektovou smlouvu. Tyto řádky faktury lze v konceptu faktury odstranit. V takovém případě se řádky objeví na následující faktuře, dokud nebudou fakturovány nebo dokud nebude faktura odeslána zákazníkovi. Nelze fakturovat částečné množství z řádku faktury za produkt. Při fakturaci řádků produktu z projektové smlouvy se vytvoří skutečné hodnoty. Tyto skutečné hodnoty však nejsou propojeny se související entitou projektu. Jinými slovy, řádky projektové smlouvy založené na produktu jsou nezávislé na jakémkoli použití založeném na projektu. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
