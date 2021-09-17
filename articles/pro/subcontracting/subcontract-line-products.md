---
title: Řádky subdodávky pro produkty
description: Toto téma vysvětluje, jak zaznamenávat řádky subdodávky pro produkty a pomocí různých polí nákup produktu od dodavatelů.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323678"
---
# <a name="subcontract-lines-for-products"></a>Řádky subdodávky pro produkty

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Subdodavatel v Dynamics 365 Project Operations může mít řádek subdodávky pro produkty. Tyto řádky umožňují manažerovi projektu nakupovat produkty od dodavatelů, které mohou použít při plnění úkolů projektu.

Chcete-li vytvořit řádek subdodávky pro kategorie výdajů v Project Operations, proveďte následující kroky.

1. V navigačním podokně vyberte **Subdodávky** a otevřete subdodávku, na které chcete pracovat. 
2. Na kartě **Řádky subdodávky** vybráním **Nový** vytvořte nový řádek.
3. Na stránce **Rychlé vytvoření** v poli **Transakční třída** vyberte **Materiál** a zadejte nebo vyberte jakékoli další požadované informace pro pole. 
4. Zvolte **Uložit**.

Následující tabulka poskytuje informace o polích na stránce s podrobnostmi **Řádky subdodávky** a stránce **Rychlé vytvoření**.

| Pole | Popis |
| ----- | ----------- |
| Jméno | Název řádku subdodávky. |
| Popis | Stručný popis služeb a produktů, které jsou nakupovány na základě subdodávky. |
| Typ linky | Toto pole má výchozí hodnotu **Na základě množství**. |
| Fakturační metoda |  Fakturační metoda řádku subdodávky. Pro způsoby účtování s pevnou cenou je k dispozici plán faktur založený na milníku. |
| Třída transakce | Toto pole má výchozí hodnotu **Čas**. Chcete-li pro nákup produktů vytvářet řádky subdodávky, v poli **Transakční třída** vyberte **Materiál**. Tento výběr označuje, že se řádek subdodávky používá k záznamu nákupu produktů, které mají být použity pro projekty. |
| Vybrat produkt | Vyberte, zda je zakoupený produkt veden v katalogu produktů nebo jde o produkt nezahrnutý do katalogu. |
| Produkt | Vyberte aktivní produkt z katalogu. Toto pole je k dispozici pouze tehdy, když je pole **Vybrat produkt** nastaveno na **Existující**. |
| Produkt nezahrnutý do katalogu | Zadejte název produktu nezahrnutého do katalogu. Toto pole je k dispozici pouze tehdy, když je pole **Vybrat produkt** nastaveno na **Není v katalogu**.  |
| Požadované datum dodávky | Vyberte požadované datum dodání produktů. Toto datum je také použito k výběru ceníku projektu z ceníků projektu připojených k subdodávce. Náklady na produkt na řádku subdodávky jsou výchozí podle tohoto ceníku. |
| Smluvní datum dodávky | Vyberte datum, kdy jsou produkty smluvně dohodnuty na dodání.  |
| Objednané množství | Zadejte množství produktu, které bylo zakoupeno od dodavatele. Když projektový manažer přečerpá z tohoto množství, dojde k varování. |
| Skupina jednotek | Tato hodnota je výchozí pouze pro katalogové produkty. Když jsou vybrány **Produkt** a **Požadované datum dodání**, systém vybere příslušný ceník na základě data dodání. Pro odpovídající produkt jsou dotazovány související položky ceníku. Hodnoty jednotky a skupiny jednotek jsou výchozí z nastavení v záznamu položky ceníku. |
| Jednotka | Tato hodnota je výchozí pro nastavení jednotky v záznamu položky ceníku. Podle potřeby můžete změnit na jinou jednotku. Kombinace produktu a jednotky se používá k výchozímu nastavení jednotkové ceny na řádku subdodávky pro existující katalogové produkty. |
| Jednotková cena | Výchozí hodnota jednotkové ceny použitím kombinace produktu a jednotky z položek ceníku vztažených k ceníku projektu, která je použitelná pro požadované spuštění řádku subdodávky.  |
| Dílčí součet | Toto pole pouze pro čtení se vypočítá jako množství x jednotková cena, pokud mají obě pole zadané hodnoty. Pokud jsou pole **Množství**, **Jednotková cena** nebo obě pole prázdná, můžete do tohoto pole zadat hodnotu ručně.  |
| DPH | Zadejte částku prodejní daně. |
| Celková částka | Toto vypočítané pole ukazuje celkovou částku subdodávky po zahrnutí daní. Hodnota tohoto pole se počítá jako mezisoučet + daň. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
