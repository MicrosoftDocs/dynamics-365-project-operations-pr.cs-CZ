---
title: Správa časových pásem
description: Když je projekt vytvořen, jeho časové pásmo je založeno na časovém pásmu definovaném v použité šabloně pracovní doby.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c3feb05e1b2e81add1b0df886a5a69ced229eb72
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578516"
---
# <a name="manage-time-zones"></a>Správa časových pásem

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


## <a name="projects"></a>Projekty

Když je projekt vytvořen, časové pásmo je založeno na časovém pásmu definovaném v použité šabloně pracovní doby. Na kartě **Projekt** jsou datumy jsou vždy relativní k časovému pásmu uživatele, který je přihlášen na každé kartě, kromě karty **Úkol**. Při prohlížení strukturovaného rozpisu prací se datumy vždy zobrazí v časovém pásmu projektu.

## <a name="tasks"></a>Úlohy

Když je úkol vytvořen, čas zahájení, čas ukončení a počet hodin/den se řídí pracovní dobou projektu. Například pokud je úkol vytvořen s projektem, jehož časové pásmo je -8 PST a má následující pracovní dobu: 9:00–17:00 od pondělí do pátku, jakýkoli úkol vytvořený bez přiřazení bude respektovat počáteční čas a čas ukončení kalendáře projektu.

## <a name="manage-resources-with-time-zones"></a>Správa zdrojů pomocí časových pásem

Pro přesné a předvídatelné výsledky při používání funkce **Prodloužit rezervaci** musí být splněny dva klíčové předpoklady:  

- Uživatel musí konfigurovat časové pásmo svého zařízení tak, aby odpovídalo časovému pásmu definovanému v systémové možnosti **Nastavení přizpůsobení**.
 
  ![Nastavení časového pásma v systému Windows 10.](media/reconcile-assignments-03.png)

  ![Nastavení časového pásma v nastavení personalizace.](media/reconcile-assignments-04.png)
 
- Rezervovatelný zdroj musí mít alespoň jednu minutu pracovní doby, která se překrývá s průběhovými křivkami, které slouží k definování požadovaného rozšíření. Například následující zdroje s pracovní dobou, která spadá mezi 9:00 a 19:00. 

  ![Porovnání průběhových křivek zdroje.](media/reconcile-assignments-05.png)

Následující tabulka znázorňuje:

- Šablona kalendáře projektu
- Zdroj A: Tento zdroj má stejný kalendář a je ve stejném časovém pásmu jako projekt. Čas zahájení rezervace bude 9:00.
- Zdroj B: Tento prostředek se nachází v jiném časovém pásmu než projekt a začíná v 7:00 v jejich časovém pásmu. Rezervace však začnou v 9:00, protože to je nejčasnější počáteční čas průběhové křivky přiřazení.
- Zdroje C a D: Zdroje jsou umístěny v různých časových pásmech, která se liší navzájem a také vůči projektu, a jejich rezervace začínají nejdříve v příslušných dostupných počátečních časech.

|Entity  |Kalendář  |
|-|-|
|Šablona kalendáře projektu   | ![kalendář projektu.](media/reconcile-assignments-06.png) |
|Zdroj A  | ![Kalendář zdroje A.](media/reconcile-assignments-06.png) |
|Zdroj B  |  ![Kalendář zdroje B.](media/reconcile-assignments-07.png) |
|Zdroj C  |  ![Kalendář zdroje C.](media/reconcile-assignments-08.png) |
|Zdroj D  | ![Kalendář zdroje D.](media/reconcile-assignments-09.png)  |
 
Když přejdete na zobrazení **Vyrovnání**, zobrazí se přiřazení zdrojů a přidružené nedostatečné rezervace.

![Zobrazení odsouhlasení před rozšířením.](media/reconcile-assignments-10.png)

Poté, co byla u každého zdroje použita funkce rozšířené rezervace, jsou rezervace úspěšně rozšířeny u každého zdroje, protože pracovní doba každého zdroje se překrývala s průběhovými křivkami nedostatečné rezervace.

![Zobrazení odsouhlasení po prodloužení rezervace.](media/reconcile-assignments-11.png) 

Všimněte si, že při detailnějším pohledu na podrobnosti rezervací se ukážou rozdíly v počátečním čase rezervací. Rezervace začínají nejdříve v počátečním čase průběhové křivky přiřazení a nejdříve v dostupném počátečním čase zdroje.

![Nové rezervace zdrojů na plánovací vývěsce.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]