---
title: Plánování projektu pomocí strukturovaného rozpisu prací
description: Postup plánování projektu pomocí strukturovaného rozpisu prací v Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a00e39f78890426721a49cd569ba8ce4accb30a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282685"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Plánování projektu se strukturou rozpisu práce (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Plán projektu uvádí, co je třeba udělat, které zdroje práci vykonají a časový rámec, ve kterém je třeba práci dokončit. Plán projektu odráží všechny práce související s dodáním projektu včas. Jedním z prvních kroků v počáteční fázi projektu je přijít s plánem projektu. K vytvoření plánu projektu je nutné vytvořit strukturovaný rozpis prací.  
  
 Vytvořte strukturu projektu pomocí strukturovaného rozpisu prací, což vám pomůže:  
  
- Rozdělit práci na zvládnutelné úkoly  
  
- Odhadnout čas potřebný k dokončení úkolu  
  
- Nastavit závislostí a dobu trvání úkolu  
  
- Určit role potřebné k dokončení každého úkolu  
  
  Plán projektu ve strukturovaném rozpisu prací má známý vzhled a chování, včetně interaktivního Ganttova diagramu.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Vytvoření strukturovaného rozpisu prací pro projekt  
 Vytvořte strukturovaný rozpis prací pro znázornění posloupnosti úkolů v projektu. Strukturovaný rozpis prací zahrnuje úkoly, požadavky na jednotlivé úkoly a informace o výnosech a nákladech. Ve strukturovaném rozpisu prací můžete přidat:  
  
-   Řadu úkolů v hierarchii  
  
-   Další úkoly, které je nutno dokončit před zahájením úkolu  
  
-   Počáteční datum, koncové datum a dobu trvání úkolu  
  
-   Počet hodin, které jsou potřebné pro daný úkol  
  
-   Jakékoli požadované dovednosti pracovníků a vzdělávání  
  
-   Pracovníci, kteří jsou přiřazeni k úkolu  
  
-   Odhadované výnosy a náklady  
  
## <a name="task-types"></a>Typy úkolů  
Při vytváření strukturovaného rozpisu prací budete používat následující typy úkolů:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Kořenový uzel projektu**. | Souhrnný úkol nejvyšší úrovně pro projekt. Všechny ostatní úkoly projektu jsou vytvořeny pod ním. Název kořenového úkolu je název projektu. Úsilí, data a doba trvání kořenového uzlu se zakládají na hodnotách v hierarchii pod ním. Nelze upravit vlastnosti kořenového uzlu ani odstranit kořenový uzel. | 
| **Souhrnné úkoly nebo úkoly kontejneru** | Souhrnný úkol je úkol, který má pod sebou dílčí úkoly. Souhrnný úkol nemá žádné vlastní úsilí nebo své vlastní náklady. Jeho pracovní úsilí a náklady jsou součtem jeho dílčích úkolů. Můžete změnit název souhrnného úkolu, ale nelze změnit úsilí, data a dobu trvání, protože ty jsou vypočteny automaticky. Odstraněním souhrnného úkolu odstraníte úkol a všechny jeho dílčí úkoly.|  
| **Úkoly uzlu typu list** | Úkol uzlu typu list představuje nejpodrobnější práci na projektu. Má odhadnuté úsilí, plánovaný počet prostředků, plánované datum zahájení a ukončení a dobu trvání.|

  
## <a name="task-hierarchy"></a>Hierarchie úkolů  
 Při vytváření hierarchie úkolů máte následující možnosti:  
  
- **Přidat úkol**.   Můžete přidat úkol do zvoleného umístění v hierarchii úkolů. Pokud nevyberete umístění, zobrazí se nový úkol na konci.  
  
- **Zvětšit odsazení úkolu**.   Zvětšením odsazení úkolu jej můžete nastavit jako podřízený úkol úkolu přímo nad ním.  
  
- **Zmenšit odsazení úkolu**.   Zmenšením odsazení úkolu již nebude dílčím úkolem jeho původního nadřazeného úkolu.  
  
- **Posunout nahoru a Posunout dolů**.   Přesune úkoly nahoru nebo dolů v hierarchii jejich nadřazeného úkolu. Přesunutí úkolu směrem nahoru nebo dolů nemá žádný vliv na jeho úsilí, náklady, data nebo dobu trvání.  
  
## <a name="task-attributes"></a>Atributy úkolu  
 Název úkolu popisuje práci, kterou je třeba vykonat. K popisu plánu a požadavků na pracovníky využijte různé atributy úkolu.  
  
### <a name="schedule-attributes"></a>Plánování atributů

 - Přiřaďte hodnoty k možnostem **Hodiny úsilí**, **Počet zdrojů**, **Datum zahájení**, **Datum ukončení** a **Doba trvání** a stanovte plán úkolu. 
 - **Úsilí** je odhadovaný počet hodin nutných k dokončení úkolu.
 - **Počet zdrojů** je odhad vedoucího projektu ohledně počtu osob, které jsou třeba pro nejlepší možný plán. 
 - **Doba trvání** (ve dnech) označuje počet pracovních dnů, které budou třeba k dokončení úkolu.  
  
### <a name="staffing-attributes"></a>Personální atributy

 - **Role**, **Organizační jednotka zdroje**, **Počet zdrojů**, a **Zdroje** popisují požadavky na personální obsazení úkolu. 
 - **Role** popisuje typ zdroje potřebný k provedení úkolu. 
 - **Organizační jednotka zdroje** označuje organizační jednotku, ze které je pro tento úkol třeba zajistit zdroje. To ovlivní také nákladové a prodejní odhady úkolu, protože je třeba vzít tyto hodnoty v úvahu při určování jednotkové prodejní ceny zdroje. 
 - **Zdroje** zahrnují obecné zdroje nebo pojmenované zdroje, pokud existují.  
  
## <a name="task-dependencies"></a>Závislosti úkolu  
 Můžete vytvořit vztahy mezi předchůdci pro jeden nebo více úkolů ve strukturovaném rozpisu prací. Můžete nastavit jednu nebo více hodnot pro pole předchůdce úkolů, čímž označíte úkoly, na kterých bude záviset. Když přiadíte hodnotu předchůdce k úkolu, můžete se úkol spustit pouze v případě, že byly dokončeny všechny úkoly typu předchůdce. Výsledkem nastavení této závislosti na úkolu bude přepočet plánovaného data zahájení úkolu až po ukončení všech jeho předchůdců. Vliv předchůdce na plán není omezen režimem úkolu definovaným v úkolu.  
  
## <a name="task-mode"></a>Režim úkolu  
 Režim úkolu je jedním z důležitých faktorů, které určují plánování úkolů uzlu typu list. Existují dva režimy úkolů pro každý úkol: režim automatického plánování a režim ručního plánování.  
  
-   **Automatické plánování**.   Při nastavení režimu úkolu na automatické plánování modul plánování úkolu používá pravidla plánování na následující atributy úkolu k určení plánu úkolu:  
  
    -   Předchůdci  
  
    -   Úsilí  
  
    -   Počet zdrojů  
  
    -   Počáteční a koncová data  
  
-   **Pravidla plánování**.   Počáteční datum úkolu uzlu typu list, který nemá předchůdce, bude nastaven na výchozí datum zahájení plánování projektu. Doba trvání úkolu uzlu typu list se vždy počítá jako počet pracovních dnů mezi jeho počátečním a koncovým datem. Když je úkol naplánován automaticky, plánovací modul postupujte podle následujících pravidel:  
  
    -   Datum zahájení a dokončení úkolu musí být vždy pracovní dny podle plánovacího kalendáře projektu  
  
    -   Datum zahájení úkolu, který má předchůdce, bude nastaveno na poslední koncové datum jeho předchůdců  
  
    -   Úsilí = počet osob * doba trvání * hodiny ve standardní pracovní den kalendáře projektu  
  
-   **Ruční plánování**.   V některých případech se můžete chtít od těchto pravidel odchýlit. V těchto případech můžete nastavit režim úkolu pro úkol na ruční plánování. Tím zabráníte plánovacímu modulu ve výpočtu hodnot z jiných atributů plánování. Nastavení předchůdců úkolů vždy ovlivňuje datum zahájení závislého úkolu.  
  
## <a name="create-a-work-breakdown-structure"></a>Vytvoření strukturovaného rozpisu prací  
  
1.  Přejděte do nabídky **Project Service > Projekty**.  
  
2.  Klepněte na projekt, na kterém chcete pracovat.  
  
3.  Na panelu v horní části obrazovky vyberte šipku dolů vedle názvu projektu a potom klikněte na možnost Strukturovaný rozpis prací.  
  
4.  Chcete-li přidat úkol, klikněte na tlačítko **Přidat úkol**. Vyplňte pole úkolu a klikněte na tlačítko **Uložit**.  
  
5.  Pokračujte v přidávání úkolů, dokud nebude strukturovaný rozpis prací dokončen. Při vytváření strukturovaného rozpisu prací můžete provést následující, chcete-li uspořádat úkoly:  
  
    -   Vyberte úkol a klikněte na tlačítko **Zvětšit odsazení**, chcete-li jej posunout pod jiný úkol, nebo na tlačítko Zmenšit odsazení, chcete-li jej přesunout na vyšší úroveň.  
  
    -   Vyberte úkol a klikněte na tlačítko **Posunout nahoru** nebo **Posunout dolů** , chcete-li úkol přesunout nahoru nebo dolů v seznamu.  
  
    -   Klikněte na tlačítko **Skrýt Ganttův diagram**, chcete-li skrýt Ganttům diagram, a na tlačítko **Zobrazit Ganttův diagram**, chcete-li jej znovu zobrazit.  
  
    -   Vyberte jinou dobu pro Ganttův diagram v poli **Časové měřítko**.  
  
6.  Chcete-li přidat role uvedené ve strukturovaném rozpisu prací ke členům týmu projektu, klikněte na tlačítko **Generovat projektový tým**.  
  
7.  Když jste s prováděním změn hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.  
  
### <a name="see-also"></a>Viz také  
 [Příručka pro projektového manažera](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]