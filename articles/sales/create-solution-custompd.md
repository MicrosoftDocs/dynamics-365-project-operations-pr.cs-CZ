---
title: Vytvoření řešení pro vlastní cenové dimenze
description: Toto téma obsahuje informace o vytvoření řešení vlastních cenových dimenzí.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513969"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Vytvoření řešení pro vlastní cenové dimenze

 _**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_ 

>[!IMPORTANT]
>Všechny změny vlastních cenových dimenzí by měly být v samostatném řešení. Tento důležitý osvědčený postup umožňuje flexibilitu při aktualizaci nebo odebrání změn podle potřeby, pomůže při opětovném použití vaší práce a usnadní portování těchto změn na jiné instance. Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované** řešení a pak jej importujte do jiných instancí za účelem znovupoužití.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Vytvoření řešení pro vlastní cenové dimenze

1.  Vyberte **Nastavení** > **Řešení** a pak vyberte **Nový**.
2.  Pojmenujte řešení *Cenové dimenze <your organization name>*.
3. Zadejte zbývající požadované informace a zvolte **Uložit**.

  ![Vytvoření řešení pro vlastní cenové dimenze](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Přidání všech požadovaných entit a souvisejících komponent do řešení cenové dimenze

Přidejte do svého cenového řešení následující entity Project Service, abyste mohli provést důležité změny schématu v cenovém řešení. Po dokončení tohoto postupu entity rozpoznají nové dimenze cen.

1.  Vyberte **Nastavení** > **Řešení** a potom klikněte dvakrát na **<*název vaší organizace*> cenové dimenze**.
2.  V Průzkumníku řešení vyberte v levém navigačním podokně **Přidat existující** > **Entity**.
3.  V dialogovém okně **Součásti řešení** vyberte následující entity:
 
   - **Skutečnost**
   - **Rezervovatelný zdroj**
   - **Řádek odhadu**
   - **Projektový úkol**
   - **Podrobnosti řádku faktury**
   - **Řádek deníku**
   - **Podrobnosti řádku projektové smlouvy**
   - **Člen projektového týmu**
   - **Podrobnosti řádku nabídky**
   - **Přirážka ceny role**
   - **Cena role**
   - **Časový záznam**
 
   ![Přidat existující entity k vlastnímu řešení cenových dimenzí](./media/Existing-entities-to-PD-solution.png)
 
 4. U každé entity zkontrolujte přidávané komponenty a konečný seznam prostředků entit pro každou entitu. 

   >[!NOTE]
   > Zahrňte všechny formuláře a zobrazení pro všechny vybrané entity.

  ![Přidané entity](./media/solution-component-selection.png)


5.  Po zobrazení výzvy k zahrnutí jakýchkoli závislých entit pro vybrané entity vyberte **Ne, nezahrnovat požadované součásti.**

    ![Včetně závislých entit](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]