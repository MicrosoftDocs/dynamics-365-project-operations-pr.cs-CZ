---
title: Odhadněte tržby a náklady projektu, když rezervovatelný zdroj plní více rolí v projektu
description: Tento téma vysvětluje, jak používat cenové dimenze k podpoře odhadů cen a nákladů pro zdroj, který v projektu plní více rolí.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7ef9765b7db1c6650fb0599bf5fb4b4b6304be69
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013658"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Odhadněte tržby a náklady projektu, když rezervovatelný zdroj plní více rolí v projektu 

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení – od obchodu po proforma fakturaci a Project Operations pro scénáře založené na skladovém materiálu / výrobě_ 

Projektové společnosti často potřebují, aby jeden zdroj zaplnil více rolí v projektu. Každá role může být oceněna a oceněna odlišně. To znamená, že čas stejného zdroje na projektu by mohl získat jiný finanční odhad v závislosti na faktuře a nákladových sazbách pro každou roli. Můžete nastavit hodnoty v záznamu člena týmu pro pojmenovaný prostředek s různými přepisy u každé z úkolů, ke kterým je člen týmu přiřazen.

Následující příklad vás provede tím, jak jednoduché přepsání hodnoty umožňuje, aby měl prostředek v projektu více rolí s různými náklady a sazbami faktur.

## <a name="create-tasks"></a>Vytvoření úkolů
Chcete-li vytvořit úkoly, musíte přidat úkoly a souhrnné úkoly, po kterých je třeba úkol přiřadit, než přidáte dobu trvání úkolu. 

### <a name="add-tasks-and-summary-tasks"></a>Přidejte úkoly a souhrnné úkoly
Chcete-li přidat úkol, postup dle následujících instrukcí.

1. Přejděte na **Projekty** a otevřete projekt, do kterého chcete přidat úkoly.
2. Vyberte **Přidat nový úkol**. Pojmenujte úkol a stiskněte **Enter**.
3. Zadejte název jiného úkolu a stiskněte **Enter**. Tento postup opakujte, dokud nebudete mít úplný seznam úkolů.
3. Chcete-li odsadit úkoly pod **Souhrnné** úkoly, vyberte tři svislé tečky podle názvu úkolu a poté vyberte **Vytvořit dílčí úkol**. 

  > [!TIP]
  > Chcete-li vybrat více než jeden úkol, vyberte úkol, stiskněte a podržte **Ctrl** a poté vyberte jiný úkol.
  >
  > Můžete si také vybrat **Zvýšit úroveň dílčího úkolu**, chcete-li přesunout úkoly mimo **Souhrnné** úkoly.

### <a name="assign-tasks"></a>Přiřadit úkoly

Chcete-li přiřadit úkol, postupujte dle následujících instrukcí.

1. Ve sloupci **Přiřazeno** pro úkol vyberte ikonu osoby.
2. Vyberte člena týmu ze seznamu nebo zadejte text a vyhledejte jméno.

### <a name="add-task-duration-and-columns"></a>Přidejte trvání úkolu a sloupce

Často je nejjednodušší zahájit konstrukci projektu s dobou trvání. Chcete-li přidat trvání úkolu, postupujte dle následujících instrukcí.

1. Ve sloupci **Doba trvání** pro úkol zadejte počet dní, které si myslíte, že bude trvat splnění úkolu. Pokud chcete použít jinou jednotku času, zadejte číslo plus slovo **hodin**, **týdnů** nebo **měsíců**.
2. Pokud chcete, aby se váš úkol objevil jako milník ve tvaru diamantu v zobrazení **Časová osa**, do sloupce **Doba trvání** zadejte **0 dní**.
3. Stiskněte **Enter** a přejděte na další úkol, kde v poli **Doba trvání** pokračujte v zadávání dob trvání.

  > [!NOTE]
  > Nelze zadat dobu trvání souhrnných úkolů.

Do projektu můžete přidat sloupce a poskytnout další podrobnosti. Chcete-li to provést, vyberte **Přidat sloupec**. 

Další informace najdete v části [Vytvoření projektu](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Nastavte roli a organizační jednotku pro člena obecného projektového týmu
Pomocí následujících kroků můžete nastavit roli a organizační jednotku pro generického člena týmu.

1. Na stránce **Úkoly** vyberte řádek **Úkol** pro **Úkol A**. 
2. V **Přiřazeno** vyberte **Přidat obecný zdroj**. Tím se otevře stránka **Rychlé vytvoření člena týmu**.
3. Na stránce **Rychlé vytvoření člena týmu** zadejte atributy obecného člena týmu, který může tento úkol provádět.
4. Vyberte příslušnou roli a organizační jednotku a poté vyberte **Uložit a zavřít**. Je vytvořen obecný člen týmu a přiřazen k tomuto úkolu. 
5. Opakujte kroky 1-4 pro **Úkol B**. Nicméně, **Úkol B** musí mít pro obecného člena týmu přiřazenu jinou roli a organizační jednotku než **Úkol A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Nastavte roli a organizační jednotku pro úkol projektu
Pomocí následujících kroků můžete nastavit roli a organizační jednotku pro úkol.

1. Poté, co vytvoříte **Úkol A**, vyberte úkol a poté vyberte ikonu **i** pro otevření podokna **Podrobnosti úkolu**. 
2. V podokně **Podrobnosti úkolu** přejděte dolů a vyberte **Zobrazit podrobnosti**, čímž otevřete stránku **Podrobnosti úkolu**.
3. Na stránce **Podrobnosti úkolu** v možnosti **Role** a **Organizační jednotka** přidejte hodnoty, které jsou vyžadovány k provedení této úlohy pro prostředek. 

  > [!NOTE]
  > Pokud dokončíte tento scénář pomocí ukázkových dat Project Operations, vyberte **Poradenský vedoucí** jako toli a **Fabrikam USA** jako organizační jednotku.

4. Vyberte **Úkol B** a potom vyberte úkol.
5. Vyberte ikonu **i** a otevřete podokno **Podrobnosti úkolu**. 
6. V podokně **Podrobnosti úkolu** přejděte dolů a vyberte **Zobrazit podrobnosti**, čímž otevřete stránku **Podrobnosti úkolu**.
7. Na stránce **Podrobnosti úkolu** v možnosti **Role** a **Organizační jednotka** přidejte hodnoty, které jsou vyžadovány k provedení této úlohy pro prostředek. Hodnoty v **Rolei** a **Organizační jednotce** pro **Úkol B** musí být jiné než pro **Úkol A**. 

  > [!NOTE]
  > Pokud dokončíte tento scénář pomocí ukázkových dat Project Operations, vyberte **Síťový technik** jako toli a **Fabrikam USA** jako organizační jednotku.

8. Uložte a zavřete stránku **Podrobnosti úkolu**. 

## <a name="team-member-and-estimates-behavior"></a>Člen týmu a odhady chování 
Chcete-li porozumět chování v mřížce **Člen týmu** a odhadů, proveďte následující kroky.

1. V mřížce **Člen týmu** vyberte dva obecné členy týmu a poté vyberte **Generovat požadavky**. Tím se vygenerují požadavky na zdroje. 
2. Vyberte řádek člena týmu pro **Poradenský vedoucí** a poté vyberte **Rezervovat**. Otevře se plánovací vývěska se seznamem zdrojů. Vyberte zdroj a poté vyberte **Rezervovat**, chcete-li rezervovat zdroj podle tohoto požadavku.
3. Vyberte řádek člena týmu pro **Síťového technika** a poté vyberte **Rezervovat**. Otevře se plánovací vývěska se seznamem zdrojů. Vyberte stejný zdroj jako výše a poté vyberte **Rezervovat**, chcete-li rezervovat zdroj podle tohoto požadavku.

### <a name="team-member-grid"></a>Mřížka členů týmu 

V mřížce **Člen týmu** dva obecné záznamy členů týmu jsou odstraněny a nahrazeny pouze jedním prostředkem. Pro tento prostředek existuje jedna sada hodnot, které jsou výchozí sadou hodnot pro **Roli** a **Organizační jednotku**.

Když rozbalíte řádek pro daný záznam člena týmu, uvidíte v záznamu člena týmu pro obě úlohy odlišná přiřazení. Každý řádek přiřazení má specifické hodnoty úkolu pro **Roli** a **Organizační jednotku**. 

### <a name="estimates-grid"></a>Mřížka odhadů 

V mřížce **Odhady** obě přiřazení stejného zdroje jsou oceněny odlišně. Cena za přiřazení zdroje na **úkolu A** je stanovena pomocí hodnoty atributu **Role** položky **Poradenský vedoucí**. Cena za přiřazení stejného zdroje na **úkolu B** je stanovena pomocí hodnoty atributu **Role** položky **Síťový technik**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]