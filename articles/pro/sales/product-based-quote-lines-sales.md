---
title: Přehled řádků nabídky založené na produktu – omezený
description: Tohle téma poskytuje informace o práci s řádky nabídky na základě projektu.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178180"
---
# <a name="product-based-quote-lines-overview---lite"></a>Přehled řádků nabídky založené na produktu – omezený

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V Dynamics 365 Project Operations můžete vytvořit řádky nabídky založené na produktu. Řádky nabídky založené na produktu mohou být ručně přidané nebo mohou být položkami z katalogu produktů.

## <a name="product-catalog"></a>Katalog produktů

Každý produkt v katalogu produktů má výchozí jednotku a skupinu jednotek. Pokud několik produktů sdílí stejnou sadu atributů, můžete vytvořit produktovou řadu, která sdílí tyto atributy. 

Společnost například prodává předplacené licence pro různé druhy softwaru. Veškerý předplacený software má následující dva atributy:

- Počet uživatelů
- Doba trvání předplatného měřená v měsících

Chcete-li udržovat tento typ katalogu, vytvořte produktovou řadu s názvem **Předplatné softwaru** a jako atributy přidejte počet uživatelů a dobu trvání předplatného. Dále můžete přidat jednotlivé produkty do produktové řady **Předplatné softwaru**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Přidání položek katalogu produktů do projektové nabídky

Stránky **Projektová nabídka** a **Projektová smlouva** mají oddíly pro řádky založené na projektu a řádky založené na produktu. V případě řádků založených na produktu zahrnuje rozevírací seznam na řádku nabídky nebo řádku projektové smlouvy všechny produkty a jednotky v produktovém ceníku. Můžete také přidat produkty, které nejsou součástí produktového ceníku.

Dále můžete vybrat produkty z jiných ceníků nebo přímo z katalogu produktů. Vyberete-li produkt přímo z katalogu produktů, použije se pro získání prodejní ceny produktu výchozí ceník tohoto produktu. Pokud není nastaven výchozí ceník, je cena nastavena na nulu (0).

Pokud je řádek nabídky založen na katalogu produktů, můžete přepsat prodejní cenu přímo na řádku nabídky. Řádek nabídky v poli **Ceny** se dvěma dostupnými hodnotami:

- **Přepsat cenu**
- **Použít výchozí**

Pokud vyberete **Přepsat cenu**, výchozí cena není nastavena. Místo toho musíte na řádku nabídky zadat cenu produktu. Pokud vyberete **Použít výchozí**, použije se výchozí prodejní cena a pole je uzamčeno pro úpravy.

Do řádků nabídky založených na produktu jsou vloženy výchozí prodejní ceny. Pole **Ceny** je pak nastaveno na **Přepsat cenu**, takže můžete upravit výchozí cenu na řádcích nabídky. Toto je přepsání přímo pro Project Operations pro chování řádků založených na produktu v Dynamics 365 Sales.
