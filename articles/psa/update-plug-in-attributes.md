---
title: Aktualizace atributů modulů plug-in tak, aby zahrnovaly nové cenové dimenze
description: Toto téma obsahuje informace o aktualizaci atributů modulů plug-in pro cenové dimenze.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281785"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Aktualizace atributů modulů plug-in tak, aby zahrnovaly nové cenové dimenze

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Pokud nepoužíváte funkce Vypracování nabídky a Uzavírání smluv služby Project Service Automation (PSA), můžete toto téma přeskočit.

Toto téma předpokládá, že jste dokončili postupy v tématech [Vytvoření vlastních polí a entit](create-custom-fields-entities.md), [Přidání vlastních polí do nastavení ceny a transakčních entit](field-references.md) a [Nastavení vlastních polí jako cenových dimenzí](set-up-pricing-dimensions.md). Pokud jste tyto postupy nedokončili, vraťte se zpět, dokončete je a vraťte se k tomuto tématu.

Při vytvoření detailu řádku nabídky na stránce **Řádek nabídky** pro řádek nabídky projektu systém vytvoří dva řádky odhadu na pozadí – jeden řádek pro nákladovou stranu odhadu a jeden pro prodejní stranu. To je stejné pro řádky projektové smlouvy.

Pokud změníte množství nebo pole na straně nákladů, bude tato změna rozšířena na stranu prodeje. To je možné kvůli tomu, že následující moduly plug-in je nutné po změně cenových dimenzí znovu zaregistrovat.

- PreOperationContractLineDetailUpdate – Aktualizuje **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – Aktualizuje **msdyn_quotelinetransaction**.

Následující postup vysvětluje proces registrace modulů plug-in.

1. Otevřete **PluginRegistrationTool** a připojte se k online instanci.
2. Klikněte na tlačítko **Hledat** a vyhledejte modul plug-in, který chcete aktualizovat.

 ![Snímek obrazovky vyhledávacího stromu](media/PRT-1.png)

3. Po nalezení modulu plug-in jej vyberte a klikněte na tlačítko **Vybrat v hlavním formuláři**.

4. Vyberte krok modulu plug-in, který chcete aktualizovat, klikněte pravým tlačítkem myši a vyberte položku **Aktualizovat**.

 ![Snímek obrazovky modulu plug-in, který má být aktualizován](media/PRT-2.png)
 
5. V okně aktualizace klikněte na tři tečky (**...**) v atributech filtrování.

 ![Snímek obrazovky aktualizace existujících informací kroku konfigurace](media/PRT-3.png)
 
6. Zaškrtněte políčka atributu ceny.

 ![Snímek obrazovky zaškrtnutí políčka pro atributy ceny](media/PRT-4.png)

7. Kliknutím na tlačítko **OK** zavřete stránku a pak vyberte možnost **Aktualizovat krok**.

 ![Snímek obrazovky s tlačítkem „Aktualizovat krok“](media/PRT-5.png)
 
8. Tento postup zopakujte pro druhý modul plug-in **PreOperationQuoteLineDetail – Aktualizace msdyn_quotelinetransaction**.

9. Zavřete nástroj Plug-in Registration Tool.



[!INCLUDE[footer-include](../includes/footer-banner.md)]