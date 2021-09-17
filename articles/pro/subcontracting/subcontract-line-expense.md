---
title: Řádky subdodávky pro kategorie výdajů
description: Toto téma vysvětluje, jak zaznamenávat řádky subdodávky pro výdaje a pomocí polí zaznamenávat čas nákupu od dodavatelů.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323813"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Řádky subdodávky pro kategorie výdajů

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Subdodavatel v Dynamics 365 Project Operations může mít řádek pro kategorie výdajů. Řádky subdodávek pro kategorie výkladů umožňují vedoucímu projektu nakupovat nákupní kategorie služeb nebo produktů od dodavatelů, které mohou být účtovány na projekt.

Chcete-li vytvořit řádek subdodávky pro kategorie výdajů v Project Operations, proveďte následující kroky.

1. V navigačním podokně vyberte **Subdodávky** a otevřete subdodávku, na které chcete pracovat.
2. Na kartě **Řádky subdodávky** vybráním **Nový** vytvořte nový řádek.
3. Na stránce **Rychlé vytvoření** v poli **Transakční třída**  vyberte **Výdaje** a zadejte nebo vyberte jakékoli další požadované informace pro pole.

Následující tabulka poskytuje informace o polích na stránce s podrobnostmi **Řádky subdodávky** a stránce **Rychlé vytvoření**.

| **Pole** |  **Popis** |
| ----------| ---------------- |
| Jméno | Název řádku subdodávky. |
| Popis | Stručný popis služeb a kategorií produktů, které jsou nakupovány na řádku subdodávky. |
| Typ linky | Toto pole má výchozí hodnotu **Na základě množství**.  |
| Fakturační metoda | Fakturační metoda řádku subdodávky. Na základě fakturační metody řádku je pro fakturační metodu s pevnou cenou k dispozici plán faktur založený na milníku.  |
| Třída transakce | Toto pole má výchozí hodnotu **Čas**. Chcete-li pro nákup produktů vytvářet řádky subdodávky, nastavte pole **Transakční třída** na **Výdaje**. Tato hodnota pole označuje, že se řádek subdodávky používá k záznamu nákupu kategorie produktů nebo služeb, které mají být použity pro projekty. |
| Kategorie transakce | Vyberte kategorii transakce. |
| Požadované počáteční datum | Datum, kdy musejí být kategorie nákupu k dispozici u dodavatele. Požadovaný začátek slouží k výběru ceníku projektu z ceníků projektu připojených k subdodávce. Náklady na kategorii na řádku subdodávky jsou výchozí podle tohoto ceníku. |
| Požadované koncové datum | Datum, kdy kategorie nákupů již nejsou potřeba. Toto datum vyvolá upozornění, když vedoucí projektu přidruží tento řádek subdodávky ke konkrétním odhadům výdajů na projekty, které jsou datovány po tomto datu. |
| Objednané množství | Množství kategorie, které bylo zakoupeno od dodavatele. Když projektový manažer přečerpá ze zakoupeného množství, dojde k varování.  |
| Skupina jednotek | Tato hodnota pole je výchozí na základě výchozí skupiny jednotek, která je nastavena pro vybranou kategorii. |
| Jednotka | Tato hodnota pole je výchozí na základě výchozí skupiny jednotek, která je nastavena pro vybranou kategorii. Kombinace kategorie a jednotky se používá k výchozímu nastavení jednotkové ceny na řádku subdodávky. |
| Jednotková cena | Hodnota pole jednotkové ceny je výchozí jako kombinace kategorie a jednotky z cen kategorie vztažených k ceníku projektu, který je použitelný pro požadované spuštění řádku subdodávky.  |
| Dílčí součet | Toto pole pouze pro čtení se automaticky vypočítá jako jednotková cena množství, pokud jsou zadány hodnoty množství i jednotkové ceny. Pokud je jedno nebo obě pole prázdná, můžete do tohoto pole zadat hodnotu ručně.  |
| DPH | Zadejte částku prodejní daně.  |
| Celková částka | Celkové množství řádku subdodávky včetně daní. Toto pole se počítá jako mezisoučet + daň z obratu.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
