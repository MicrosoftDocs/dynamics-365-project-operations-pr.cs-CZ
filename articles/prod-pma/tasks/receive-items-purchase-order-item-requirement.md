---
title: Příjem položek na nákupní objednávce z požadavku na položku.
description: Tento článek vysvětluje, jak přijmout položky na nákupní objednávce z požadavku na položku.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbe15fac325ad00bdd2f2fc6ddf3ae15df45271
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929528"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Příjem položek na nákupní objednávce z požadavku na položku.

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak přijmout položky na nákupní objednávce z požadavku na položku.

Použitím požadavku na položku namísto transakce s položkou můžete naplánovat dodávku těsně před skutečným použitím zboží, vytvořit nákupní objednávku, zahrnout položku do rámce obchodní dohody a zahrnout požadavek na položku do plánování výroby. 

Tento úkol používá datovou sadu USSI.

1. V navigačním podokně přejděte na **Moduly > Řízení projektů a účetnictví > Projekty > Všechny projekty**.
2. V seznamu vyberte odkaz v požadovaném řádku.
3. V podokně akcí vyberte **Plán**.
4. Vyberte **Požadavky na položku**.
5. Vyberte **Nové**.
6. V novém řádku zadejte nebo vyberte hodnotu v poli **Číslo položky**.
7. Do pole **Množství** zadejte číslo.
8. Zvolte **Uložit**.
9. V podokně akcí vyberte **Spravovat**.
10. Vyberte **Funkce**.
11. Vyberte **Vytvoření nákupní objednávky**.
12. Klikněte na tlačítko **Zahrnout vše**.
13. V poli **Účet dodavatele** zadejte nebo vyberte hodnotu.
14. Vyberte **OK**.
15. V navigačním podokně přejděte na **Moduly > Závazky > Nákupní objednávky > Všichni nákupní objednávky**.
16. V seznamu vyberte odkaz v požadovaném řádku.
17. V podokně akcí vyberte **Koupit**.
18. Vyberte **Potvrdit**.
19. V podokně akcí vyberte **Získat**.
20. Vyberte **Účtenka produktu**.
21. Do pole **Účtenka produktu** zadejte hodnotu.
22. Vyberte **OK**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]