---
title: Aktualizace atributů modulů plug-in o nové cenové dimenze
description: Toto téma obsahuje informace o aktualizaci atributů modulů plug-in o cenové dimenze.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 54b87a993929edbf89ef48741ba0a06c6c42ec4e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004613"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Aktualizace atributů modulů plug-in o nové cenové dimenze

Toto téma obsahuje informace o aktualizaci atributů modulů plug-in o cenové dimenze.

> [!NOTE]
> Toto téma se vztahuje pouze na funkce nabídek a smluv v Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Požadavky
Než dokončíte kroky v tomto téma, musíte mít dokončené postupy v následujících tématech:

  - [Vytvoření vlastních polí a entit](create-custom-fields-entities-pricing-dimensions.md) 
  - [Přidání vlastních polí do nastavení ceny a transakčních entit ](add-custom-fields-price-setup-transactional-entities.md)
  - [Nastavení vlastních polí jako cenových dimenzí ](set-up-custom-fields-pricing-dimensions.md). 
  
Pokud jste tyto postupy nedokončili, dokončete je a vraťte se k tomuto tématu.

## <a name="register-a-plug-in"></a>Registrace modulů plug-in
Když je vytvořen detail řádku nabídky na stránce **Řádek nabídky** pro řádek nabídky projektu, systém vytvoří dva řádky odhadu. Jeden řádek je na straně nákladů odhadu a druhý řádek na straně prodeje. To je stejné pro řádky projektové smlouvy.

Pokud změníte množství nebo pole na straně nákladů, tato změna se projeví i na straně prodeje. To je možné, protože moduly plug-in PreOperation na Quotelinedetail a entity podrobností řádků smlouvy spojují konkrétní atributy na straně nákladů s prodejní stranou transakce. Pokud potřebujete provést změny hodnot cenové dimenze na prodejní straně i na straně nákladů, je nutné po provedení změn cenové dimenze znovu zaregistrovat následující doplňky.

Následujcí moduly plug-in je třeba aktualizovat a znovu registrovat:

- PreOperationContractLineDetailUpdate – Aktualizujte **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – Aktualizujte **msdyn_quotelinetransaction**.

Pomocí následujících kroků aktualizujte a znovu zaregistrujte moduly plug-in.

1. Ortevřete **PluginRegistrationTool** a připojte se ke svému prostředí Project Operations Dataverse.
2. Vyberte **Vyhledávání** a zadejte několik prvních písmen pluginu, který má být aktualizován.
3. Po nalezení modulu plug-in jej vyberte a vyberte **Vybrat v hlavním formuláři**.
4. Vyberte krok **Aktualizujte msdyn_orderlinetransaction**, klikněte pravým tlačítkem myši a vyberte **Aktualizovat**.
5. V dialogovém okně **Aktualizovat** vyberte tři tečky (**...**) v atributech filtrování.
6. Otevře se okno filtrování atributů a poskytuje seznam všech atributů v entitě a dimenzích cen. Zaškrtněte políčka u atributů dimenze cen.
7. Výběrem **OK** zavřete stránku a pak vyberte možnost **Aktualizovat krok**.
8. Opakujte kroky 2 až 7 pro druhý modul plug-in **PreOperationQuoteLineDetail**. Pro tento modul plug-in musíte aktualizovat krok **Aktualizujte msdyn_quotelinetransaction**.
9. Zavřete **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]