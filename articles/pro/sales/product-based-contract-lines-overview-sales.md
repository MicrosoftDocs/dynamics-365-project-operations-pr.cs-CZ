---
title: Přehled řádků smlouvy založených na produktu
description: Toto téma poskytuje informace o řádcích smlouvy založených na produktu.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073707"
---
# <a name="product-based-contract-lines-overview"></a>Přehled řádků smlouvy založených na produktu

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V Dynamics 365 Project Operations můžete vytvářet řádky smluv založené na produktu. Řádky smlouvy založené na produktu mohou vytvořené ručně nebo mohou být položkami z katalogu produktů.

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

Pokud pole **Ocenění** nastavíte na **Přepsat ocenění** , není výchozí cena nastavena. Zadejte cenu produktu v řádku smlouvy. Pokud nastavíte pole na hodnotu **Použít výchozí** , použije se výchozí prodejní cena a pole nelze upravit.

Po instalaci Project Operations jsou do řádků smlouvy založených na produktu vloženy výchozí prodejní ceny. Pole **Ocenění** je pak nastaveno na **Přepsat ocenění** , takže můžete upravit výchozí cenu na řádcích smlouvy. Toto přepsání chování řádků založených je specifické pro Project Operations a odlišné vůči aplikaci Dynamics 365 Sales.
