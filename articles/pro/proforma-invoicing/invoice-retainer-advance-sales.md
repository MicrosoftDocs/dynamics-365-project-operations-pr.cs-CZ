---
title: Fakturace záloh
description: Toto téma poskytuje informace o fakturaci záloh v aplikaci Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 238b55e906fb66415cf46d3abc8827d85c174dd7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003983"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Fakturace záloh

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations podporuje smluvy na základě záloh a jednorázové zálohy. Na smlouvě o projektu můžete zaznamenat plán záloh nebo jednorázových zálohu. Nahrávání na úrovni smlouvy o projektu však okamžitě nezpřístupní zálohu pro použití. Chcete-li použít zálohu na faktuře, která zákazníkovi skutečně účtuje, je třeba nejdříve zálohu vyfakturovat.

Chcete-li vyfakturovat zálohu, postupujte následovně.

1. Vybrat **Prodej** > **Fakturace** > **Zálohy**. 
2. Na stránce **Zálohy** pomocí filtru vyberte konkrétní zálohu k fakturaci a označte ji jako **Připraveno k fakturaci**.
3. Vytvořte fakturu buď ručně ze seznamu **Smlouva o projektu** nebo stránky s podrobnostmi. Záloha je uvedena na konceptu faktury v části **Zálohy** na stránce **Faktura**.
4. Fakturu potvrďte. Díky tomu bude záloha k dispozici pro použití. Fakturu si můžete ověřit na stránce seznamu **Zálohy**. U fakturované zálohy se dostupná částka zobrazí v mřížce.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Vytvoření zálohy z mřížky faktury

Zálohu můžete vytvořit přímo na faktuře.

1. Na konceptu faktury na podmřížce **Zálohy** vyberte **Nová** k vytvoření nové zálohy. 
2. Na stránce **Rychlé vytvoření** přidejte potřebné informace a poté vyberte **Uložit**. Záloha je vytvořena na projektové smlouvě související s fakturou. Záloha je automaticky označena jako **Připraveno k fakturaci** a poté přidána do podmřížky **Zálohy** na stránce **Faktura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Vyrovnání fakturované zálohy

Po fakturaci zálohy ji lze použít nebo vyrovnat na faktuře s časem, výdaji, milníky nebo jinými poplatky na základě projektu. Zákazníkovi se částka faktury sníží o částku zálohy použitou na této faktuře.

Na každé faktuře, která je generována pro smlouvu o projektu, která fakturovala zálohy, Project Operation automaticky použije zálohy na faktuře.

To je vidět na mřížce **Použité zálohy** na stránce **Faktura**. Následující tabulka poskytuje informace o polích v mřížce **Použité zálohy** na stránce **Projektová faktura**.

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| Popis | Mřížka **Použité zálohy** na stránce **Projektová faktura**. |Toto pole jen pro čtení poskytuje popis zálohy použité na této faktuře. Tuto hodnotu nelze na faktuře změnit. Tuto hodnotu lze aktualizovat v podsíti na serveru **Projektová smlouva**. | Toto pole lze zákazníkovi zobrazit na vytištěné faktuře, aby bylo uvedeno, která záloha je na faktuře použita. |
| Datum dodání | Mřížka **Použité zálohy** na stránce **Projektová faktura**.  | Toto pole jen pro čtení poskytuje datum fakturace zálohy použité na této faktuře. Tuto hodnotu nelze na faktuře změnit. Tuto hodnotu lze aktualizovat v podsíti na serveru **Projektová smlouva**. | Toto pole lze zákazníkovi zobrazit na vytištěné faktuře, aby bylo uvedeno datum, kdy byla záloha zákazníkovi poprvé fakturována. |
| Množství | Mřížka **Použité zálohy** na stránce **Projektová faktura**.  | Toto pole jen pro čtení poskytuje částku zálohy použité na této faktuře. Tuto hodnotu nelze na faktuře změnit. Tuto hodnotu lze aktualizovat v podsíti na serveru **Projektová smlouva**. | Toto pole lze zákazníkovi zobrazit na vytištěné faktuře, aby byla uvedena původní částka zálohy, která byla zákazníkem zaplacena. |
| Použitá částka | Mřížka **Použité zálohy** na stránce **Projektová faktura**.  | Toto pole jen pro čtení poskytuje vypočtenou hodnotu, která shrnuje, kolik ze zálohy bylo použito. | Toto pole lze zákazníkovi zobrazit na vytištěné faktuře, aby byla uvedena částka této zálohy, která byla již použita. |
| Rozšířená částka | Mřížka **Použité zálohy** na stránce **Projektová faktura**.  | Toto upravitelné pole poskytuje částku zálohy, která se používá na projektové faktuře. Tato částka nemůže být vyšší než částka, která je k dispozici na zálohu. Systém to automaticky vypočítá jako rozdíl mezi poli **Množství** a **Použité množství** na mřížce. Tuto částku můžete snížit, abyste spotřebovali méně, než je k dispozici, ale nemůžete zvýšit částku, abyste použili více, než je k dispozici. | Toto pole lze zákazníkovi zobrazit na vytištěné faktuře, aby byla uvedena částka této zálohy, která se používá na faktuře. |
| Částka zůstatku zálohy. | Mřížka **Použité zálohy** na stránce **Projektová faktura**.  | Toto pole jen pro čtení poskytuje hodnotu toho, kolik rezervy nebo zálohy zbude po potvrzení faktury. | Toto pole lze zákazníkovi zobrazit na vytištěné faktuře, aby byla uvedena částka této zálohy, která bude ponechána z této zálohy po potvrzení a zaplacení faktury. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]