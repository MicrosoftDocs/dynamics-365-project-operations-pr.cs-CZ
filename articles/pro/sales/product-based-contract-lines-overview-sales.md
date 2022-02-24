---
title: Přehled řádků smlouvy založené na produktu – omezený
description: Toto téma poskytuje informace o řádcích smlouvy založených na produktu.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272650"
---
# <a name="product-based-contract-lines-overview---lite"></a>Přehled řádků smlouvy založené na produktu – omezený

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V aplikaci Dynamics 365 Project Operations můžete vytvořit řádky smlouvy založené na produktu. Řádky smlouvy založené na produktu mohou vytvořené ručně nebo mohou být položkami z katalogu produktů.

## <a name="product-catalog"></a>Katalog produktů

Produkty v katalogu produktů aplikace mají výchozí jednotku a skupinu jednotek. Pokud několik produktů sdílí stejnou sadu atributů, můžete vytvořit produktovou řadu, která má také tyto atributy. Všechny produkty v jedné produktové řadě dědí stejnou sadu atributů.

Společnost například prodává předplacené licence pro různé druhy softwaru. Veškerý předplacený software má následující dva atributy:

- Počet uživatelů
- Doba trvání předplatného (v měsících)

Chcete-li udržovat tento typ katalogu, vytvořte produktovou řadu **Předplacený software**. Přidejte do produktové řady atributy **Počet uživatelů** a **Délka předplatného**. Poté přidejte jednotlivé produkty do produktové řady **Předplacený software**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Přidání položek katalogu produktů do projektové smlouvy

Projektové smlouvy mají oddíly pro dva typy řádků: řádky založené na projektu a řádky založené na produktu. Řádky založené na produktu zahrnují všechny produkty a jednotky uvedené v ceníku produktů ve smlouvě. Můžete také přidat produkty, které nejsou součástí ceníku produktů smlouvy.

Produkty můžete vybrat z jiných ceníků nebo přímo z katalogu produktů. Vyberete-li produkt přímo z katalogu produktů, prodejní cena produktu se vybere z výchozího ceníku produktu. Pokud není nastaven výchozí ceník, je cena nastavena na 0 (nulu).

Pokud je řádek smlouvy založen na katalogu produktů, můžete přepsat prodejní cenu přímo v řádku. Řádek smlouvy má pole **Ocenění** pole se dvěma hodnotami:

- **Přepsat ocenění**
- **Použít výchozí**

Pokud pole **Ocenění** nastavíte na **Přepsat ocenění**, není výchozí cena nastavena. Zadejte cenu produktu v řádku smlouvy. Pokud nastavíte pole na hodnotu **Použít výchozí**, použije se výchozí prodejní cena a pole nelze upravit.

Po instalaci Project Operations jsou do řádků smlouvy založených na produktu vloženy výchozí prodejní ceny. Pole **Ocenění** je pak nastaveno na **Přepsat ocenění**, takže můžete upravit výchozí cenu na řádcích smlouvy. Toto přepsání chování řádků založených je specifické pro Project Operations a odlišné vůči aplikaci Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]