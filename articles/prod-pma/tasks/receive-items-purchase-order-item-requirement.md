---
title: Příjem položek na nákupní objednávce z požadavku na položku.
description: Tento téma vysvětluje, jak přijímat položky na nákupní objednávce z požadavku na položku.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2083516ff929113fd6db377acfe5aeb104666dd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288220"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Příjem položek na nákupní objednávce z požadavku na položku.

[!include [banner](../../includes/banner.md)]

Tento téma vysvětluje, jak přijímat položky na nákupní objednávce z požadavku na položku.

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