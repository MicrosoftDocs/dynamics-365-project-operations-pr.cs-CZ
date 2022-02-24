---
title: Vytvoření modelů prognóz pro rozpočty projektů
description: Tento téma popisuje, jak vytvořit model prognózy pro zbývající rozpočty.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271030"
---
# <a name="create-forecast-models-for-project-budgets"></a>Vytvoření modelů prognóz pro rozpočty projektů 

[!include [banner](../includes/banner.md)]

Tento téma popisuje, jak vytvořit model prognózy pro zbývající rozpočty. Projekt, který podléhá kontrole rozpočtu, používá dva typy rozpočtů: původní a zbývající. Když vytváříte rozpočet projektu, musíte určit původní a zbývající modely prognózy rozpočtu, které byly vytvořeny na stránce **Předpovědní modely**. Rozpočty projektu založené na zadaných modelech se vytvářejí při potvrzení rozpočtu projektu.

> [!NOTE]
> Model předpovědi, který se používá pro kontrolu rozpočtu, nemůže mít podmodel ani jej nelze použít jako podmodel.

1. Vyberte možnost **Řízení projektů a účetnictví** > **Nastavení** > **Prognózy**  > **Předpovědní modely**.
2. Vybráním možnosti **Nový** vytvořte nový model předpovědi a poté zadejte identifikační číslo modelu a název nového modelu. 
3. Nastavte možnost **Zastaveno** na **Ano**, abyste zabránili jakýmkoli změnám v řádcích prognózy pro předpovědní model. 
4. Pokud by řádky prognózy, ke kterým je model přidružen, měly generovat prognózy peněžních toků v hlavní knize, nastavte možnost **Zahrnout do prognóz peněžních toků** na **Ano**. 
5. Chcete-li jako datum faktury použít datum projektu, nastavte **Datum faktury předpovědi** na **Ano**. 
6. V poli **Typ rozpočtu** vyberte jeden z následujících typů modelů:

   - **Původní rozpočet**: Použijte původní částky rozpočtu, které jsou přiděleny, když je vytvořen a schválen původní rozpočet.
   - **Zbývající rozpočet**: Použijte zbývající částky rozpočtu během doby trvání projektu. Zůstatky v tomto modelu prognózy se snižují o skutečné transakce a zvyšují nebo snižují revize rozpočtu.
   - **Převádět**: Použijte částky převedeného rozpočtu pro projekt. Převedení je volitelný proces, který lze spustit a převést nevyužité částky rozpočtu z jednoho fiskálního roku do druhého.

7. Nastavte následující možnosti podle potřeby:

   - Chcete-li jako datum faktury použít datum projektu, zapněte **Datum faktury předpovědi**.
   - Zapněte možnost **Předpověď s WIP**, chcete-li předpovídat na základě nedokončené výroby (WIP) a poté vyberte typ WIP. 
   - Můžete ponechat výchozí **Typ rozpočtu** jako **Žádný** nebo zadat nový typ. Po změně záznamu nelze typ rozpočtu změnit.     
    > [!NOTE]
    > Pokud změníte výchozí typ rozpočtu, nebudou pro aktualizace k dispozici všechny ostatní možnosti a nebudete moci tento předpovědní model znovu použít. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]