---
title: Vytvoření vlastních řešení pro cenové dimenze
description: Tento článek vysvětluje, jak vytvořit vlastní řešení při vytváření vlastních cenových dimenzí.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 0df6728634b169c8a1a128aba1555d79fee5719f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929022"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Vytvoření vlastních řešení pro cenové dimenze

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Všechny změny vlastních cenových dimenzí by měly být v samostatném řešení. Tento důležitý osvědčený postup poskytuje v budoucnosti flexibilitu pro aktualizaci nebo odebrání změn podle potřeby, pomůže při opětovném použití vaší práce a usnadní portování těchto změn na jinou instanci. Po provedení všech požadovaných změn exportujte toto řešení jako **Spravované řešení** a importujte ho do jiných instancí za účelem znovupoužití vašeho nastavení cen.

1. Vyberte **Nastavení** > **Řešení** a pak vyberte **Nový**. 
2. Řešení nazvěte **\<your organization name> cenové dimenze**, zadejte zbývající požadované informace a poté vyberte **Uložit**.

> ![Vytvoření vlastního řešení pro cenové dimenze.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Přidání všech požadovaných entit a souvisejících komponent do řešení cenové dimenze
K vašemu řešení ocenění bude nutné přidat následující entity Project Service. Provedením kroků v tomto postupu můžete provést některé důležité změny schématu v řešení ocenění, aby si entity všimly nových cenových dimenzí.

1. Zvolte **Nastavení** > **Řešení** a pak dvakrát klikněte na **\<your organization name> cenové dimenze**. 
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Přidat existující** > **Entity**.
3. V dialogovém okně **Součásti řešení** vyberte následující entity:

- Skutečnost
- Rezervovatelný zdroj
- Řádek odhadu
- Projektový úkol
- Podrobnosti řádku faktury
- Řádek deníku
- Podrobnosti řádku projektové smlouvy
- Člen projektového týmu
- Podrobnosti řádku nabídky
- Přirážka ceny role
- Cena role 
- Časový záznam 

> ![Přidat existující entity k řešení cenových dimenzí.](media/Existing-entities-to-PD-solution.png)

> ![Vybrat součásti řešení.](media/Dimension-Components.png)

> [!NOTE]
> Nezapomeňte zahrnout všechny formuláře a zobrazení pro všechny vybrané entity.

4. Při zobrazení výzvy k zahrnutí všech závislých entit do vybraných entit zvolte **Ne**.

> ![Nezahrnovat všechny související komponenty.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
