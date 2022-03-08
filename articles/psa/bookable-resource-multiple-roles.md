---
title: Odhad tržeb a nákladů projektu, když rezervovatelný zdroj plní více rolí v projektu
description: Tento téma obsahuje informace, jak používat cenové dimenze k podpoře vytváření cen a nákladů pro zdroj, který v projektu plní více rolí.
author: rumant
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
ms.openlocfilehash: be24bb3bdf2f3c8351fc396ae67457b5213e1cd800e9d2ad23d59d0d038f22b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987473"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Odhad tržeb a nákladů projektu, když rezervovatelný zdroj plní více rolí v projektu 

[!include [banner](../includes/psa-now-project-operations.md)]

Projektové společnosti často potřebují, aby jeden zdroj prováděl více rolí v projektu. Každá z těchto rolí by mohla jinou cenu a náklady, což znamená, že čas stejného zdroje na projektu by mohl získat jiný finanční odhad v závislosti na sazbách fakturace a nákladových sazbách pro každou z rolí. Project Service Automation umožňuje nastavení hodnot v záznamu člena týmu pro pojmenovaný zdroj a umožňuje různé přepsání každého z úkolů, ke kterým je člen týmu přiřazen.

Následující příklad vysvětluje, jak jednoduché přepsání této hodnoty umožňuje, aby měl prostředek v projektu více rolí s různými sazbami fakturace a nákladovými sazbami.

## <a name="create-tasks"></a>Vytvoření úkolů
Vytvořte dva projektové úkoly na 40 hodin, úkol A a úkol B. Vyberte úkol A jako předchůdce úlohy B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Nastavte roli a organizační jednotku pro člena obecného projektového týmu

1. Na stránce **Plán** vyberte řádek **Úkol** pro úkol A. 
2. V poli **Zdroje** vyberte **Vytvořit** v rozevíracím seznamu.
3. Na stránce **Rychlé vytvoření člena týmu** zadejte atributy obecného člena týmu, který může tento úkol provádět.
4. Vyberte příslušnou roli a organizační jednotku a poté vyberte **Uložit a zavřít**. Je vytvořen obecný člen týmu a přiřazen k tomuto úkolu. 

Opakujte tyto kroky pro úkol B a ujistěte se, že role a organizační jednotka člena obecného týmu vytvořeného pro úkol B se liší od úlohy A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Nastavte roli a organizační jednotku pro projektový úkol

1. Po vytvoření úlohy A vyberte úkol a poté vyberte **Upravit úkol**.
2. Na stránce **Podrobnosti úkolu** najděte pole **Role** a **Organizační jednotka**, přidejte hodnoty požadované u zdroje, který by tuto úlohu provedl. 

  > [!NOTE]
  > Pokud dokončujete tyto scénáře pomocí ukázkových dat Project Service Automation, vyberte **Poradenský vedoucí** jako roli a **Fabrikam USA** jako organizační jednotku.

3. Vyberte úkol B a potom vyberte položku **Upravit úkol**.
4. Na stránce **Podrobnosti úkolu** najděte pole **Role** a **Organizační jednotka**, přidejte hodnoty požadované u zdroje, který by tuto úlohu provedl. Ujistěte se, že hodnoty v polích **Role** a **Organizační jednotka** se liší pro úkol B od hodnot pro úkol A. 

  > [!NOTE]
  > Pokud dokončujete tyto scénáře pomocí ukázkových dat Project Service Automation, vyberte **Síťový technik** jako roli a **Fabrikam USA** jako organizační jednotku.

5. Uložte a zavřete stránku **Podrobnosti úkolu**. 

## <a name="team-member-and-estimates-behavior"></a>Člen týmu a odhady chování 

1. Na stránce **Podrobnosti úkolu** u **Člena týmu** vyberte dva obecné členy týmu a poté vyberte **Generovat požadavky**. 
2. Vyberte řádek člena týmu pro **Poradenský vedoucí** a poté vyberte **Rezervovat**. Otevře se plánovací vývěska a rezervuje zdroj k tomuto požadavku.
3. Vyberte řádek člena týmu pro **Síťového technika** a poté vyberte **Rezervovat**. Otevře se plánovací vývěska a rezervuje stejný zdroj k tomuto požadavku.

### <a name="team-member-grid"></a>Mřížka členů týmu 
V mřížce **Člen týmu** si všimněte, že dva obecné záznamy členů týmu jsou odstraněny a byly nahrazeny jedním prostředkem. Pro tento zdroj existuje jedna sada hodnot, která zobrazuje výchozí sadu hodnot pro **Roli** a **Organizační jednotku**.
Když rozbalíte řádek daného záznamu člena týmu, uvidíte v záznamu člena týmu odlišná přiřazení pro obě tyto úlohy. Každý řádek přiřazení má specifické hodnoty úkolu pro **Roli** a **Organizační jednotku**. 

### <a name="estimates-grid"></a>Mřížka odhadů 
Když přejdete na mřížku **Odhady**, všimnete si, že obě přiřazení stejného zdroje jsou oceněny odlišně.
Cena za přiřazení zdroje na úkolu A je stanovena pomocí hodnoty atributu **Role** položky **Poradenský vedoucí**. Cena za přiřazení stejného zdroje na úkolu B je stanovena pomocí hodnoty atributu **Role** položky **Síťový technik**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]