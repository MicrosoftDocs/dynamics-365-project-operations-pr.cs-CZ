---
title: Příjem položek na nákupní objednávce z požadavku na položku.
description: Tento téma vysvětluje, jak přijímat položky na nákupní objednávce z požadavku na položku.
author: KimANelson
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
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750270"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Příjem položek na nákupní objednávce z požadavku na položku.

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

