---
title: Ceny v katalogu produktů
description: Toto téma obsahuje informace o tom, jak v Dynamics 365 Project Service Automation (PSA) fungují ceny v katalogu produktů.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 6cf50a09226bd6fdb803fd1fd379fec80838be75
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600642"
---
# <a name="product-catalog-pricing"></a>Ceny v katalogu produktů 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Ceníky a entity položek ceníku podporují oceněn v katalogu produktů. Tato funkce se většinou používá pro řádky založené na katalogu v nabídkách projektů a projektových smlouvách.

U řádků založených na projektu představuje smlouva dohodu po jejím získání. Vzhledem k tomu, že proces vyjednávání obvykle předchází získání, je ocenění připojené k nabídce vždy zkopírováno tak, jak je, do nového ceníku a připojeno ke smlouvě. Tento nový ceník nelze změnit mimo rozsah smlouvy. Toto omezení pomáhá chránit kartu se sazbami před jakýmikoli změnami cen, které se vyskytují v hlavním ceníku.

Produkty by měly být nastaveny tak, aby měly v katalogu produktů výchozí nákladové ceníky a ceníky. Ke konfiguraci výchozích nákladových cen a ceníků je nutné použít ceníkovou cenu, standardní cenu a aktuální cenu. Výchozí ceníky se používají na řádku nabídky nebo řádku projektové smlouvy pouze v případě, že systém nemůže pro tento produkt najít řádek ceníku v produktovém ceníku pro nabídku nebo projektovou smlouvu.

Nákladová cena řádků katalogu produktů může být změněna mezi nabídkami. Tato možnost je důležitá, protože pokud přesně nesledujete náklady, nemůžete u učastí na projektu určit provozní zisky. Ve výchozím nastavení se standardní cena produktu používá jako nákladová cena. Výchozí nákladovou cenu je však možné na řádku nabídky aktualizovat, pokud pro tuto nabídku existuje jiná nákladová cena.

## <a name="price-list-items"></a>Položky ceníku

Produkty z katalogu produktů můžete přidat do různých ceníků. Řádky ceníku pro produkty vždy odkazují na určitou jednotku. Ocenění produktu v položkách ceníku lze konfigurovat jako částku v měně. Alternativně může být nakonfigurována jako funkce ceníku, aktuální ceny nebo standardní ceny.

PSA podporuje různé možnosti zaokrouhlení, pokud jsou ceny konfigurovány jako funkce ceníku, standardní ceny nebo aktuální ceny. Kromě využití více způsobů ocenění a možností zaokrouhlení můžete k položkám ceníku přidružit seznamy slev. 

> ![Přidání produktů z katalogu do různých ceníků.](media/basic-guide-16.png)

Když vytvoříte nový vlastní ceník pro nabídku pomocí výběru **Vytvořit vlastní ceny** na stránce **Projektová nabídka**, PSA vytvoří kopii ceníku a pole **Entita** v záhlaví nového ceníku bude nastaveno na **Entita prodeje**. K názvu nového ceníku je připojen název nabídky a časové razítko. Název nového ceníku a název nabídky ve vlastních pracovních postupech můžete také použít k aktivaci další kontroly a schválení pro nabídky, které používají vlastní ceny.

 
## <a name="default-product-price-list"></a>Výchozí ceník produktu
Každý záznam zákazníka obsahuje pole **Výchozí ceník**, ve kterém můžete určit ceník, který odpovídá měně zákazníka. V PSA se do tohoto pole nevloží automaticky výchozí hodnota. Pokud existuje vlastní cenová dohoda s určitým zákazníkem, můžete toto pole použít k přidružení ceníku k tomuto zákazníkovi.

Entity Příležitost, Nabídka a Projektová smlouva používají k zadávání výchozích ceníků produktů následující pořadí. Stejné pořadí se používá pro projektové ceníky.

1.  Nabídka
2.  Příležitost
3.  Zákazník
4.  Globální nastavení pro PSA

Ve výchozím nastavení uvádí pole **Produkt** na řádku nabídky všechny aktivní produkty v ceníku produktu nabídky. Pokud byl produkt inaktivován nebo pokud se jedná o koncept produktu, není v seznamu uveden, i když je v ceníku. 

Řádky katalogu produktů jsou přidány jako řádky faktury v první faktuře, která je vytvořena pro projektovou smlouvu. Tyto řádky faktury lze v konceptu faktury odstranit. V takovém případě se řádky objeví na následující faktuře, dokud nebudou fakturovány nebo dokud nebude faktura odeslána zákazníkovi. V PSA nelze fakturovat částečné množství z řádku faktury za produkt. Při fakturaci řádků produktu z projektové smlouvy se vytvoří skutečné hodnoty. Tyto skutečné hodnoty však nejsou propojeny se související entitou projektu. Jinými slovy, řádky projektové smlouvy založené na produktu jsou nezávislé na jakémkoli použití založeném na projektu. PSA u projektů nesleduje spotřebu materiálu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
