---
title: Přehled mezipodnikové fakturace
description: Toto téma poskytuje informace a příklady o mezipodnikové fakturaci projektů.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595443"
---
# <a name="intercompany-invoicing-overview"></a>Přehled mezipodnikové fakturace

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Vaše organizace může mít více divizí, dceřiných společností a dalších právnických subjektů, které si navzájem přenášejí produkty a služby pro účely projektů. Právnická osoba, která poskytuje službu nebo produkt, se nazývá *půjčující právnická osoba*. Právnická osoba, která získává službu nebo produkt, se nazývá *vypůjčující právnická osoba*.

Následující obrázek ukazuje typický scénář, kdy dvé právnické osoby, Contoso Robotics USA (vypůjčující právnická osoba) a Contoso Robotics UK (půjčující právnická osoba), sdílejí prostředky na dodání projektu pro zákazníka Adventure Works. V tomto scénáři se společnost Contoso Robotics USA smluvně zavazuje dodat dílo do Adventure Works.

![Mezipodniková fakturace](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations používá následující tok ke zpracování mezipodnikových transakcí:

1. Zdroje z půjčující právnické osoby zaznamenávají mezipodnikové transakce času nebo výdajů tím, že rezervují čas a výdaje oproti projektům ve vypůjčující právnické osobě.
2. Časové a výdajové náklady se zaznamenávají v půjčující společnosti pomocí ceníku jednotkových nákladů vypůjčující společnosti.
3. Mezipodnikové nefakturované prodejní transakce se zaznamenávají v půjčující společnosti pomocí ceníku jednotkových nákladů vypůjčující společnosti.
4. Nevyfakturované výnosy se ve vypůjčující společnosti zaznamenávají pomocí ceníku smluvních prodejů. Zákazníkovi lze vystavit fakturu, když je zaznamenán nevyfakturovaný příjem. Zákazník nemusí čekat na dokončení zpracování mezipodnikové faktury.
5. Mezipodnikové faktury zákazníků se v půjčující společnosti vytvářejí pravidelně. Faktury jsou vytvářeny ručně nebo pomocí periodického automatizovaného procesu. Pro každou vypůjčující právnickou osobu lze vytvořit jednu fakturu nebo lze podle projektu vytvořit samostatné faktury.
6. Když je zaúčtována příslušná mezipodniková faktura zákazníka v půjčující právnické osobě, ve vypůjčující právnické osobě je vytvořena příslušná čekající faktura dodavatele. Po zaúčtování faktury budou náklady na čekající faktuře dodavatele zaznamenány do podřízené účetní knihy projektu.

Následující diagram ilustruje mezipodnikovou fakturaci, protože se týká účetních událostí a očekávaných zaúčtování do hlavní knihy.

![Mezipodnikový tok](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Další materiály

- [Konfigurace mezipodnikové fakturace](configure-intercompany-invoicing.md)
- [Zaznamenávání mezipodnikových transakcí](create-intercompany-transactions.md)
- [Vytváření mezipodnikových faktur zákazníků a dodavatelů](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]