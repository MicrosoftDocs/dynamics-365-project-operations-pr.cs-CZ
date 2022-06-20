---
title: Řádky subdodávky pro kategorie výdajů
description: Tento článek vysvětluje, jak zaznamenat řádky subdodávek pro výdaje a jak pomocí polí zaznamenat nákup času od dodavatelů.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b02a8aa0fce7bcb52374c0755d4bb85db16dad3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921018"
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

| **Pole** | **Popis** | **Funkční dopad** |
| --- | --- | --- |
| Jméno | Název řádku subdodávky pro jeho identifikaci. | Toto se zobrazí jako první sloupec ve všech vyhledáváních podle řádků subdodávek. |
| Popis | Stručný popis kategorií nákladů, které jsou nakupovány na řádku subdodávky. | Nic |
|Typ linky | Toto pole má výchozí hodnotu **Na základě množství**. |Nic |
| Fakturační metoda | Toto je sada možností, který představuje dva hlavní smluvní modely podporované aplikací Project Operations: **Pevná cena** a **Čas a materiál**. | Pokud je vybrána metoda fakturování s pevnou cenou, pro řádky subdodávky je zpřístupněn plán faktur založený na milnících. |
| Třída transakce | Toto pole má výchozí hodnotu **Čas**. Chcete-li pro nákup produktů vytvářet řádky subdodávky, nastavte pole **Třída transakce** na **Výdaje**.  | To znamená, že k zadání nákupu v rámci kategorie výdajů, které mají být použity na projekty, se použije řádek subdodávky. |
| Kategorie transakce | Zobrazuje seznam aktivních kategorií transakcí v systému. |Nic |
| Požadované počáteční datum | Zadejte datum, kdy musí být od dodavatele dostupná kategorie nákupu. | Požadovaný začátek slouží k výběru ceníku projektu z ceníků projektu připojených k subdodávce. Náklady na kategorii na řádku subdodávky pocházejí z tohoto ceníku. |
| Požadovaný konec | Zadejte datum, kdy již nebudou potřeba kategorie nákupu. | Toto bude použito k zobrazení varování, když vedoucí projektu přidruží tento řádek subdodávky ke konkrétním odhadům výdajů projektu, které jsou vyžadovány po tomto datu. |
| Objednané množství | Množství kategorie nakupované od dodavatele. | Toto bude použito k zobrazení varování, když projektový manažer překročí toto množství.|
| Skupina jednotek | Výchozí hodnota je založena na výchozí skupině jednotek, která je nastavena pro vybranou kategorii. |Nic |
| Jednotka | Výchozí hodnota je založena na výchozí jednotce, která je nastavena pro vybranou kategorii.  | Kombinace **Kategorie** a **Jednotka** bude použita jako výchozí nebo vypočítaná pro jednotkovou cenu pro řádek subdodávky.  |
| Jednotková cena | Výchozí hodnota používá kombinaci **Kategorie** a **Jednotka** z cenových kategorií souvisejících s ceníkem projektu, který platí pro požadovaný začátek řádku subdodávky. |Nic |
| Dílčí součet | Toto pole je pouze pro čtení a počítá se jako jednotková cena množství X, pokud jsou zadány hodnoty množství i jednotkové ceny. Pokud je jedno nebo obě pole prázdná, můžete do tohoto pole zadat hodnotu. |Nic |
| DPH | Zadejte částku prodejní daně. |Nic |
| Celková částka | Celkové množství řádku subdodávky včetně daní. Toto pole se počítá jako mezisoučet + prodejní daň. |Nic |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
