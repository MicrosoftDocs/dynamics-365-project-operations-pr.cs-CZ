---
title: Řádky subdodávky pro produkty
description: Toto téma vysvětluje, jak zaznamenávat řádky subdodávky pro produkty a pomocí různých polí nákup produktu od dodavatelů.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cda2db2b6beafb943738b35857d091f7ad17390d
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558539"
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

| Pole | Popis | Funkční dopad|
| ----- | ----------- | ----------- |
| Jméno | Název řádku subdodávky pro jeho identifikaci. |Toto se zobrazí jako první sloupec ve všech vyhledáváních podle řádků subdodávek.
| Popis | Stručný popis služeb a produktů, které jsou nakupovány na základě subdodávky. | Nic |
| Typ linky | Toto pole má výchozí hodnotu **Na základě množství**. |Nic |
| Fakturační metoda | Toto je sada možností, který představuje dva hlavní smluvní modely podporované aplikací Project Operations: **Pevná cena** a **Čas a materiál**. | Na základě vybrané metody fakturování je pro řádky subdodávky zpřístupněn plán faktur založený na milnících. |
| Třída transakce |Toto pole má výchozí hodnotu **Čas**. Chcete-li pro nákup produktů vytvářet řádky subdodávky, nastavte pole **Třída transakce** na **Materiál**.  | To znamená, že k zadání nákupu produktů, které mají být použity na projekty, se použije řádek subdodávky. |
| Vybrat produkt | Vyberte, zda je zakoupený produkt veden v katalogu produktů nebo jde o produkt nezahrnutý do katalogu. |Nic |
| Produkt | Vyberte aktivní produkt z katalogu. Toto pole je k dispozici pouze tehdy, když je pole **Vybrat produkt** nastaveno na **Existující**. |Kombinace **Produkt** a **Jednotka** bude použita jako výchozí nebo vypočítaná pro jednotkovou cenu pro řádek subdodávky.
| Produkt nezahrnutý do katalogu | Zadejte název produktu nezahrnutého do katalogu. Toto pole je k dispozici pouze tehdy, když je pole **Vybrat produkt** nastaveno na **Není v katalogu**.  |Nákupní cena nebude u zapisovaných produktů automaticky vyplněna.|
| Požadované datum dodávky | Zadejte požadované datum doručení produktů.| Toto datum je také použito k výběru ceníku projektu z ceníků projektu připojených k subdodávce. Náklady na produkt na řádku subdodávky jsou výchozí podle tohoto ceníku. |
| Smluvní datum dodávky | Zadejte datum, kdy je smluvně dohodnuto doručení produktů.  |Nic|
| Objednané množství | Zadejte množství produktu, které bylo zakoupeno od dodavatele.| Toto bude použito k zobrazení varování, když projektový manažer překročí toto množství.|
| Skupina jednotek | Tato hodnota je výchozí pouze pro katalogové produkty. |Když jsou vybrány **Produkt** a **Požadované datum dodání**, systém vybere příslušný ceník na základě data dodání. Pro odpovídající produkt jsou dotazovány související položky ceníku. Hodnoty jednotky a skupiny jednotek jsou výchozí z nastavení v záznamu položky ceníku. |
| Jednotka | Tato hodnota je výchozí pro jednotku nastavenou v záznamu položky ceníku. Podle potřeby můžete změnit na jinou jednotku.| Kombinace produktu a jednotky se používá k výchozímu nastavení jednotkové ceny na řádku subdodávky pro existující katalogové produkty. |
| Jednotková cena | Výchozí hodnota jednotkové ceny použitím kombinace produktu a jednotky z položek ceníku vztažených k ceníku projektu, která je použitelná pro požadované spuštění řádku subdodávky.  |Nic |
| Dílčí součet | Toto pole pouze pro čtení se vypočítá jako množství x jednotková cena, pokud mají obě pole zadané hodnoty. Pokud jsou pole **Množství**, **Jednotková cena** nebo obě pole prázdná, můžete do tohoto pole zadat hodnotu ručně.  |Nic |
| DPH | Zadejte částku prodejní daně. |Nic |
| Celková částka | Toto vypočítané pole ukazuje celkovou částku subdodávky po zahrnutí daní. Hodnota tohoto pole se počítá jako mezisoučet + daň. |Nic |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
