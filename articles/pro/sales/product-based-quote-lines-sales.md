---
title: Přehled řádků nabídky založené na produktu
description: Tento článek poskytuje informace o práci s řádky nabídek založených na produktu.
author: rumant
ms.date: 10/30/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a260c0f51cc2d958281dbc6f0f711347cab85a9a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826214"
---
# <a name="product-based-quote-lines-overview"></a>Přehled řádků nabídky založené na produktu

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
