---
title: Přehled řádků nabídky založené na produktu – omezený
description: Tohle téma poskytuje informace o práci s řádky nabídky na základě projektu.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369773"
---
# <a name="product-based-quote-lines-overview---lite"></a>Přehled řádků nabídky založené na produktu – omezený

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V aplikaci Dynamics 365 Project Operations můžete vytvořit řádky nabídky založené na produktu. Řádky nabídky založené na produktu mohou být ručně přidané nebo mohou být položkami z katalogu produktů.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]