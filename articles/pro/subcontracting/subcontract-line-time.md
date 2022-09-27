---
title: Řádky subdodávky pro čas
description: Tento článek vysvětluje, jak zaznamenat řádky subdodávek pro čas a zaznamenat nákup času od dodavatelů.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ba013dd7ad023acc4f0cf077099c8c2c8d5bcd8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522224"
---
# <a name="subcontract-lines-for-time"></a>Řádky subdodávky pro čas

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Subdodavatel v Dynamics 365 Project Operations může mít řádek subdodávky pro čas. Řádky subdodávek pro čas umožňují manažerovi projektu nakoupit čas zdroje dodavatele na plnění úkolů projektu a požadavků na zdroje.

Chcete-li vytvořit řádek subdodávky pro čas v Project Operations, proveďte následující kroky.

1. V navigačním podokně vyberte **Subdodávky** a otevřete subdodávku.
2. Na kartě **Řádky subdodávky** vybráním **Nový** vytvořte nový řádek.
3. Na stránce **Rychlé vytvoření** v poli **Trankční třída** vyberte **Čas**.
4. Zadejte zbývající požadované informace a klikněte na **Uložit**.

  Následující tabulka poskytuje informace o polích na stránce s podrobnostmi **Řádky subdodávky** a stránce **Rychlé vytvoření**.

| **Pole** | **Popis** | **Funkční dopad** |
| --- | --- | --- |
| Jméno | Název řádku subdodávky pro jeho identifikaci. | Toto se zobrazí jako první sloupec ve všech vyhledáváních podle řádků subdodávek. |
| Popis | Stručný popis služeb, které jsou nakupovány na řádku subdodávky. |Nic |
| Typ linky |   Toto pole má výchozí hodnotu **Na základě množství**.| Nic |
| Fakturační metoda | Toto je sada možností, který představuje dva hlavní smluvní modely podporované aplikací Project Operations: **Pevná cena** a **Čas a materiál**. | Na základě vybrané metody fakturování je pro řádky subdodávky zpřístupněn plán faktur založený na milnících. |
| Třída transakce | Výchozí hodnotou je **Čas**. | To znamená, že řádek subdodávky slouží k záznamu nákupu času subdodavatele. |
| Role | Vyberte roli zdrojů subdodavatele, jejichž čas se nakupuje. | Role vykonávaná zdroji subdodavatele určuje náklady na nákup. |
| Požadované počáteční datum | Zadejte datum, kdy jsou zdroje subdodavatele nutné k zahájení práce. | Toto slouží k výběru ceníku projektu z ceníků projektu připojených k subdodávce. Náklady na roli na řádku subdodávky pocházejí z tohoto ceníku. |
| Požadovaný konec | Zadejte datum, kdy skončí přiřazení zdroje subdodavatele. | Toto bude použito k zobrazení varování, když projektový manažer čerpá z kapacity pro požadavky na zdroje, ke kterým dochází po tomto datu. |
| Objednané množství | Zadejte počet hodin role kupované od dodavatele. | Toto bude použito k zobrazení varování, když projektový manažer přečerpá tuto kapacitu pro požadavky na zdroje. |
| Skupina jednotek | Výchozí hodnota je **Skupina časových jednotek**, kterou nelze změnit. | Nic|
| Jednotka | Výchozí hodnota pro toto pole je základní jednotka hodin ze **Skupina časových jednotek**. Tuto hodnotu můžete změnit a koupit jakoukoli jednotku času **skupiny časových jednotek**, například den nebo týden. | Kombinace **Role** a **Jednotka** bude použita jako výchozí nebo vypočítaná pro jednotkovou cenu pro řádek subdodávky. |
| Jednotková cena | Výchozí cenová jednotka používá kombinaci **Role** a **Jednotka** z ceníku projektu, který platí pro datum **Požadovaný začátek** na řádku subdodávky. | Pokud má příslušný ceník projektu cenu nastavenu v jiné jednotce, než je jednotka na řádku subdodávky, systém použije přepočet jednotek k výpočtu jednotkové ceny. |
| Dílčí součet |    Toto pole je pouze pro čtení a počítá se jako jednotková cena množství X, pokud jsou zadány hodnoty množství i jednotkové ceny. Pokud jsou množství, jednotková cena nebo obě prázdné, můžete do tohoto pole zadat hodnotu. | Nic|
| DPH |   Zadejte částku prodejní daně. |Nic |
| Celková částka | Celkové množství řádku subdodávky včetně daní. Toto pole se počítá jako mezisoučet + prodejní daň.|Nic |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
