---
title: Zobrazení fakturovatelného využití zdrojů
description: Tento článek obsahuje informace o zobrazení využití zdrojů.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 57203ecff99ab4434dacdded04245435d31bc8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921846"
---
# <a name="view-chargeable-utilization-for-resources"></a>Zobrazení fakturovatelného využití zdrojů

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Zobrazení využití** na stránce **Využití zdrojů v Project Service** zobrazuje fakturovatelné využití pro každý rezervovatelný zdroj. Protože je zobrazení založeno na plánovací vývěsce, naleznete tam mnoho stejných funkcí.

> ![Obrazovka Zobrazení využití.](media/FAQ-utilization-1.png)
 

Výpočet fakturovatelného využití probíhá takto:

   Fakturovatelné využití = (skutečné fakturovatelné hodiny) / (kapacita zdroje)

Buňky představují vypočítané fakturovatelné využití za vybrané období (dny, týdny nebo měsíce).

Barvy v každé buňce zobrazují fakturovatelné využití zdroje ve srovnání s jejich cílovým fakturovatelným využitím. 

Cílové využití může být nastaveno na výchozí roli zdroje nebo na samotném jednotlivém zdroji. Výpočet pohlíží nejdříve na jednotlivé pro cíl, a pak na výchozí roli zdroje.

## <a name="set-target-on-a-resource"></a>Nastavení cíle u zdroje

1. Přejděte na **Zdroje** \> **Zdroje**. 
2. Vyberte zdroj pro otevření záznamu. 
3. Na kartě **Project Service** můžete nastavit cílové využití zdroje.

> ![Snímek obrazovky s použitím karty Project Service pro nastavení cílového využití.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Nastavení cílového využití u role

1. Přejděte na **Zdroje** \> **Role zdrojů**. 
2. Vyberte roli a otevřete záznam. 
3. Nastavte cílové využití pro roli.

> ![Snímek obrazovky s použitím možnosti Role zdroje pro nastavení cílového využití.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Výpočet fakturovatelného využití zdroje

Pro výpočet fakturovatelného využití zdroje budete muset splnit některé předpoklady. 

### <a name="set-default-role-for-individual-resource"></a>Nastavení výchozí role pro individuální zdroj

Za prvé, cílové využití musí být nastaveno buď na jednotlivý zdroj nebo na role zdroje. Pokud používáte role zdroje pro cíle, musí mít každý jednotlivý zdroj výchozí roli. 

1. Pro toto nastavení přejděte na **Zdroje** \> **Zdroje**. 
2. Vyberte zdroj, otevřete záznam a pak vyberte kartu služba **Project Service**. 
3. V mřížce **Role zdroje** se ujistěte, že pro daný zdroj existuje jedna role a **Je výchozí** je nastaveno na **Ano**.
 
### <a name="change-billing-type-for-resource-role"></a>Změna typu fakturace pro roli zdroje

Role zdroje musí být nastaveny tak, aby měly typ fakturace **Účtovatelný**. 

1. Přejděte na **Zdroje** \> **Role zdrojů**. 
2. Otevřete záznam, který chcete aktualizovat a poté nastavte výchozí typ fakturace na **Účtovatelný**.

### <a name="set-working-hours-for-resource-role"></a>Nastavení pracovní doby pro roli zdroje
 
Zdroj musí mít pracovní dobu pro výpočet kapacity. 

1. Přejděte na **Zdroje** \> **Zdroje**. 
2. Vyberte zdroj pro otevření záznamu a pak vyberte **Zobrazit pracovní dobu**. 
3. Je možná hromadná aktualizace seznamu zdrojů použitím **Šablony pracovní doby** ze zobrazení **Seznam zdrojů**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Poradce při potížích se skutečnými fakturovatelnými hodinami

Skutečné fakturovatelné hodiny pocházejí z entity **Skutečné hodnoty**. Skutečné hodnoty s typem fakturace **Účtovatelné** jsou zahrnuty do výpočtu a z tohoto důvodu musíte mít projekty, kde jsou skutečné hodnoty účtovatelné.

Pokud nevidíte fakturovatelné využití, zde je několik věcí, které můžete zkontrolovat:

- Zdroj má definovanou pracovní dobu pro kapacitu.
- Zdroj má buď individuálně definovaný cíl využití nebo má k němu přiřazenou výchozí roli. Role má definován cíl využití.
- Skutečné hodnoty mají pro období, pro které očekáváte výpočet využití, typ fakturace **Účtovatelné**. Pokud se skutečné hodnoty zobrazují s jinými typy fakturace než účtovatelné, zkontrolujte následující:

  - Role použitá pro skutečné hodnoty má výchozí typ fakturace jiný než fakturovatelný.
  - Role na řádku smlouvy projektu byla nastavena na nefakturovatelnou.
  - Projekt nemá přidružený řádek smlouvy.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
