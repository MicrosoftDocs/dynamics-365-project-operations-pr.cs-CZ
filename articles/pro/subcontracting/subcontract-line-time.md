---
title: Řádky subdodávky pro čas
description: Toto téma vysvětluje, jak zaznamenávat řádky subdodávky pro čas a pomocí polí zaznamenávat čas nákupu od dodavatelů.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323858"
---
# <a name="subcontract-lines-for-time"></a>Řádky subdodávky pro čas

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Subdodavatel v Dynamics 365 Project Operations může mít řádek subdodávky pro čas. Řádky subdodávek pro čas umožňují manažerovi projektu nakoupit čas zdroje dodavatele na plnění úkolů projektu a požadavků na zdroje.

Chcete-li vytvořit řádek subdodávky pro čas v Project Operations, proveďte následující kroky.

1. V navigačním podokně vyberte **Subdodávky** a otevřete subdodávku.
2. Na kartě **Řádky subdodávky** vybráním **Nový** vytvořte nový řádek.
3. Na stránce **Rychlé vytvoření** v poli **Trankční třída** vyberte **Čas**.
4. Zadejte zbývající požadované informace a klikněte na **Uložit**.

  Následující tabulka poskytuje informace o polích na stránce s podrobnostmi **Řádky subdodávky** a stránce **Rychlé vytvoření**.

| **Pole** | **Popis** |
| --- | --- |
| Jméno | Název řádku subdodávky. |
| Popis | Stručný popis služeb, které jsou nakupovány na řádku subdodávky. | 
| Typ linky | Toto pole je výchozí hodnota.  |
| Fakturační metoda | Vyberte fakturační metodu. Na základě fakturační metody odkazovaného řádku subdodávky je k dispozici plán faktur založený na milníku, dostupný pro fakturační metodu s pevnou cenou. |
| Třída transakce | Toto pole je výchozí hodnota, která udává, zda se k záznamu nákupu času subdodavatele používá řádek subdodávky. |
| Role | Role zdrojů subdodávky, jejichž čas se nakupuje. Role přiřazená zdrojům subdodávky určuje náklady na nákup. |
| Požadované počáteční datum | Datum, kdy jsou zdroje subdodávky nutné k zahájení práce. Požadovaný začátek slouží k výběru ceníku projektu z ceníků projektu připojených k subdodávce. Náklady na roli na řádku subdodávky jsou potom výchozí podle tohoto ceníku. |
| Požadované koncové datum | Datum, kdy skončí přiřazení zdrojů subdodavatele. Toto datum se používá k zobrazení varování, když projektový manažer čerpá z této kapacity pro požadavky na zdroje, které nastanou po tomto datu. |
| Objednané množství | Množství hodin role, které bylo zakoupeno od dodavatele. Tato hodnota se používá k zobrazení varování, když projektový manažer čerpá z této kapacity pro požadavky na zdroje, které nastanou po tomto datu. |
| Skupina jednotek | Tato hodnota pole je výchozí pro skupinu jednotek času a nelze ji změnit.  |
| Jednotka | Toto pole je výchozí pro základní jednotku hodin ze skupiny jednotek času. Tuto hodnotu můžete změnit a koupit jakoukoli jednotku času skupiny časových jednotek, například den nebo týden. Kombinace role a jednotky se používá k výpočtu jednotkové ceny na řádek subdodávky. |
| Jednotková cena | Výchozí hodnoty jednotkové ceny z kombinace role a jednotky z ceníku projektu, který je použitelný pro požadované datum spuštění řádku subdodávky. Pokud má příslušný ceník projektu cenu nastavenu v jiné jednotce, než je jednotka na řádku subdodávky, systém použije přepočet jednotek k výpočtu jednotkové ceny. |
| Dílčí součet | Toto pole pouze pro čtení se automaticky vypočítá jako **jednotková cena x množství**, pokud jsou zadány hodnoty množství i jednotkové ceny. Pokud jsou množství, jednotková cena nebo obě prázdné, můžete do tohoto pole zadat hodnotu. |
| DPH |  Zadejte částku prodejní daně. |
| Celková částka | Celkové množství řádku subdodávky po zdanění je zahrnuto. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
