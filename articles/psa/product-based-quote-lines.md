---
title: Řádky nabídky založené na produktu
description: Toto téma poskytuje informace o řádcích nabídky založených na produktu.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: 3cc2e8788ea699b57ef75903ec3771f2e66fe867a9b8b6328a55b484eb13ede4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008578"
---
# <a name="product-based-quote-lines"></a>Řádky nabídky založené na produktu

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


V aplikaci Dynamics 365 Project Service Automation můžete vytvořit řádky nabídky založené na produktu. Řádky nabídky založené na produktu mohou být řádky „nezahrnutými do katalogu” nebo mohou být položkami z katalogu produktů.

## <a name="product-catalog"></a>Katalog produktů

Produkty v katalogu produktů aplikace Dynamics 365 mají výchozí jednotku a skupinu jednotek. Pokud několik produktů sdílí stejnou sadu atributů, můžete vytvořit produktovou řadu, která má také tyto atributy. Všechny produkty v jedné produktové řadě dědí stejnou sadu atributů.

Společnost například prodává předplacené licence pro různé softwary. Veškerý předplacený software má následující dva atributy:

- Počet uživatelů 
- Doba trvání předplatného (v měsících)

Dobrým způsobem, jak udržovat tento typ katalogu, je vytvořit produktovou řadu s názvem **Předplatné softwaru**, která jako atributy obsahuje **Počet uživatelů** a **Doba trvání předplatného**. Poté můžete do produktové řady **Předplatné softwaru** přidat jednotlivé produkty, například **Dynamics 365 Sales** nebo **Dynamics 365 Field Service**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Přidání položek katalogu produktů do projektové nabídky

Stránky projektová nabídka a projektová smlouva mají oddíly pro dva typy řádků: řádky založené na projektu a řádky založené na produktu. Pro řádky založené na produktu se Dynamics 365 používá k přidávání položek z katalogu produktů do nabídky. Rozevírací seznam na řádku nabídky nebo řádku projektové smlouvy obsahuje všechny produkty a jednotky v ceníku produktů, který je připojený k nabídce nebo projektové smlouvě. Můžete také přidat produkty, které nejsou součástí ceníku produktů nabídky.

Dále můžete vybrat produkty z jiných ceníků nebo vybrat produkty přímo z katalogu produktů. Vyberete-li produkt přímo z katalogu produktů, použije se pro získání prodejní ceny produktu výchozí ceník tohoto produktu. Pokud není nastaven výchozí ceník, je cena nastavena na 0 (nulu).

Pokud je řádek poptávky založen na katalogu produktů, můžete přepsat prodejní cenu přímo na řádku nabídky. Všimněte si, že řádek nabídky v Dynamics 365 obsahuje pole **Ocenění**. K dispozici jsou dvě hodnoty:

- Přepsat ocenění  
- Použít výchozí

Pokud toto pole nastavíte na **Přepsat ocenění**, Dynamics 365 nenastaví výchozí cenu. Na řádku nabídky musíte zadat cenu produktu. Pokud toto pole nastavíte na **Použít výchozí**, Dynamics 365 použije výchozí prodejní cenu a uzamkne pole, aby nedošlo k úpravám.

Po instalaci PSA jsou do řádků na nabídce založených na produktu vloženy výchozí prodejní ceny. Pole **Ocenění** je pak nastaveno na **Přepsat ocenění**, takže můžete upravit výchozí cenu na řádcích nabídky.

> ![Nastavení přepisu ocenění.](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Množstevní faktory pro výrobky

PSA používá množstevní faktory pro podporu prodeje produktů založených na předplatném. U produktů založených na předplatném je množství v nabídce nebo na řádku projektové smlouvy vyjádřeno jako počet uživatelských měsíců.

Cena předplaceného softwaru je v katalogu obvykle uložena jako cena za uživatele za měsíc. Místo toho však můžete použít jiné popisy času. Během prodejního procesu je cena na řádku nabídky obvykle cena za uživatele za měsíc, která byla sjednána prodejním agentem IT a po uplatnění slevy. Každá dohoda má různý počet uživatelů a různý počet měsíců předplatného. Množství, které se používá k výpočtu částky řádku nabídky, je součin počtu uživatelů a počtu měsíců předplatného.

Za účelem podpory tohoto typu prodeje byl v PSA zaveden koncept množstevních faktorů. Množstevní faktory závisí na atributech produktu v Dynamics 365. Při konfiguraci určitých vlastností produktu umožňuje PSA označit podmnožinu těchto vlastností nebo všechny vlastnosti jako množstevní faktory.

PSA ověřuje, zda jsou jako množstevní faktory označeny pouze numerické vlastnosti nebo vlastnosti produktu, které mají číselný datový typ. Pokud je produkt, pro nějž jsou nakonfigurovány množstevní faktory, přidán k řádku nabídky, pole **Množství** na řádku nabídky se stane polem jen pro čtení. Po zadání hodnot vlastností produktu, které jsou množstevními faktory, vypočítá PSA množství řádku nabídky.

Dynamics 365 může mít například následující vlastnosti: 

- **Poč. uživatelů** – počet uživatelů 
- **Poč. měsíců** – počet měsíců předplatného
- **Jednotka SKU produktu** 

Vlastnosti **Poč. uživatelů** a **Poč. měsíců** lze pomocí úpravy vlastností řádku produktu označit jako množstevní faktory. 

> ![Označení vlastností Poč. uživatelů a Poč. měsíců jako množstevní faktory.](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]