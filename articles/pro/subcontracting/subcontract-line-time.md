---
title: Řádky subdodávky pro čas
description: Toto téma vysvětluje, jak zaznamenávat řádky subdodávky pro čas a pomocí polí zaznamenávat čas nákupu od dodavatelů.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547236"
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
