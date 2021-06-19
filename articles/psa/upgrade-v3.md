---
title: Zvažování upgradu - Microsoft Dynamics 365 Project Service Automation verze 2.x nebo 1.x na verzi 3
description: Toto téma obsahuje důležité informace, které je třeba zvážit při upgradu aplikace Project Service Automation verze 2.x nebo 1.x na verzi 3.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 04ae6aa3ef6a14a6f85dce3eaa5af01e0adce9ba
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014873"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Důležité informace o upgradu – PSA verze 2.x nebo 1.x na verzi 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation a Field Service
Obě aplikace Dynamics 365 Project Service Automation a Dynamics 365 Field Service používají pro plánování zdrojů řešení Universal Resourcing Scheduling (URS). Pokud máte v instanci řešení Project Service Automation i Field Service, aktualizujte je obě na nejnovější verzi. U Project Service Automation je to verze 3.x. U Field Service je to verze 8.x. Upgrade Project Service Automation nebo Field Service nainstaluje nejnovější verzi URS. Pokud řešení Project Service Automation i Field Service ve stejné instanci nejsou upgradována na nejnovější verzi, může dojít k nekonzistentnímu chování.

## <a name="resource-assignments"></a>Přiřazení zdrojů
Ve verzích 2 a 1 aplikace Project Service Automation byla přiřazení úkolů uložena jako podřízené úlohy (nazývané také jako řádkové úkoly) v **entitě Úkol** a nepřímo související s entitou **Přiřazení zdroje**. Úkol na řádku byl viditelný v automaticky otevřeném okně přiřazení ve strukturovaném rozpisu prací (WBS).

![Úkoly na řádku pro WBS v aplikaci Project Service Automation verze 2 a 1](media/upgrade-line-task-01.png)

V aplikaci Project Service Automation verze 3 se změnilo základní schéma přiřazení rezervovatelných zdrojů k úkolům. Úkol na řádku byl zastaralý a mezi úlohou v **entitě Úkol** a členem týmu v entitě **Přiřazení zdroje** existuje přímá relace 1:1. Úkoly, které jsou přiřazeny členovi projektového týmu, jsou nyní uloženy přímo v entitě Přiřazení zdroje.  

Tyto změny ovlivňují upgrade všech existujících projektů, které mají přiřazení zdrojů pro pojmenované rezervovatelné zdroje a obecné zdroje v projektovém týmu. Toto téma obsahuje důležité informace, které je třeba zohlednit u projektů při upgradu na verzi 3. 

### <a name="tasks-assigned-to-named-resources"></a>Úkoly přiřazené k pojmenovaným zdrojům
Pomocí základní entity úkolu umožňovaly úkoly ve verzích 2 a 1 členům týmu ztvárnit jinou roli, než je jejich výchozí definovaná role. Například Ivaně Kočvářové, které je ve výchozím nastavení přiřazena role Programový manažer, může být přiřazena Vývojář. Ve verzi 3 je role pojmenovaného člena týmu vždy výchozí, takže všechny úkoly, ke kterým je přiřazena Ivana Kočvářová, používají její výchozí roli Programový manažer.

Pokud jste přiřadili zdroj k úkolu mimo jeho výchozí roli ve verzi 2 a 1, při upgradu bude pojmenovanému zdroji přiřazena výchozí role pro všechna přiřazení úkolů, bez ohledu na přiřazení role ve verzi 2. Výsledkem tohoto přiřazení budou rozdíly ve vypočtených odhadech ve verzích 2 nebo 1 a ve verzi 3, protože odhady se počítají na základě role zdroje, nikoli na základě přiřazení úkolu na řádku. Například ve verzi 2 byly Dagmar Stejskalové přiřazeny dva úkoly. Role v úkolu 1 na řádku je Vývojář a pro úkol 2 Programový manažer. Dagmar Stejskalová má výchozí roli Programový manažer.

![Více rolí přiřazených jednomu zdroji](media/upgrade-multiple-roles-02.png)

Vzhledem k tomu, že role Vývojář a Programový manažer se liší, jsou odhady nákladů a prodeje následující:

![Odhady nákladů pro role zdroje](media/upggrade-cost-estimates-03.png)

![Odhady prodeje pro role zdroje](media/upgrade-sales-estimates-04.png)

Při upgradu na verzi 3 jsou úkoly na řádku nahrazeny přiřazeními zdroje v úkolu rezervovatelného člena týmu zdroje. Přiřazení bude používat výchozí roli rezervovatelného zdroje. V následující grafice je zdrojem Dagmar Stejskalová, která má roli Programový manažer.

![Přiřazení zdrojů](media/resource-assignment-v2-05.png)

Vzhledem k tomu, že odhady jsou založeny na výchozí roli zdroje, mohou se odhady prodeje a nákladů změnit. V následující grafice již není zobrazena role **Vývojář**, protože tato role je nyní převzata z výchozí role rezervovatelného zdroje.

![Odhady nákladů pro výchozí role](media/resource-assignment-cost-estimate-06.png)
![Odhad prodeje pro výchozí role](media/resource-assignment-sales-estimate-07.png)

Po dokončení upgradu můžete upravit roli člena týmu tak, aby byla jiná než přiřazená výchozí hodnota. Pokud však změníte roli členů týmu, bude změněna u všech jim přiřazených úkolů, protože členům týmu nelze přiřazovat více rolí ve verzi 3.

![Aktualizace role zdroje](media/resource-role-assignment-08.png)

To platí také pro úkoly na řádku, které byly přiřazeny pojmenovaným zdrojům v případě, že změníte organizační jednotku zdroje z výchozí na jinou organizační jednotku. Po dokončení upgradu verze 3 bude přiřazení používat výchozí organizační jednotku zdroje namísto jednotky nastavené v úkolu na řádku.

### <a name="tasks-assigned-to-generic-resources"></a>Úkoly přiřazené k obecným zdrojům
Ve verzi 2 a verzi 1 můžete nastavit roli a organizační jednotku v úkolu a potom pomocí funkce **Vygenerovat tým** vygenerovat obecné zdroje na základě atributů nastavených v úkolu. Ve verzi 3 vytvoříte obecné členy týmu s rolí a organizační jednotkou a potom přiřadíte k úkolům členy týmu.

Ve verzích 2 a 1 mohou být projekty s obecnými zdroji ve dvou stavech nebo v jejich kombinaci na úrovni úkolu. Vezměte si například následující situace:

- Úkoly s rolemi a organizačními jednotkami jsou nastaveny, ale nebyly vygenerovány žádná přidružená přiřazení zdrojů.
- Úkoly s přiřazeními zdrojů obecných členů týmů, které byly přiřazeny vytvořením obecného zdroje pomocí funkce **Vygenerovat tým**.

Než zahájíte upgrade, doporučujeme znovu vygenerovat tým pro každý projekt, který má úkoly přiřazené k obecným zdrojům nebo u kterého je ještě třeba spustit proces generování týmu.

U úkolů, které jsou přiřazeny obecným členům týmu vygenerovaným pomocí funkce **Vygenerovat tým**, bude při upgradu tento obecný zdroj v týmu ponechán a toto přiřazení zůstane tomuto obecnému členovi týmu. Požadavek na zdroj pro obecného člena týmu doporučujeme vygenerovat po upgradu, ale dříve, než rezervujete nebo odešlete žádost o zdroj. Tím zůstanou zachována jakákoli přiřazení organizační jednotky pro obecné členy týmu, která se liší od smluvní organizační jednotky projektu.

Například v projektu Project Z je smluvní organizační jednotkou Contoso US. V plánu projektu byla k testování úkolů v rámci fáze implementace přiřazena role Technický poradce a přiřazenou organizační jednotkou je Contoso India.

![Přiřazení organizace v rámci fáze implementace](media/org-unit-assignment-09.png)

Po fázi implementace bude úkol testu integrace přiřazen k roli Technický poradce, ale organizace bude nastavena na Contoso US.  

![Přiřazení organizace v úkolu testování integrace](media/org-unit-generate-team-10.png)

Při generování týmu pro projekt budou z důvodu různých organizačních jednotek v úkolech vytvořeni dva obecní členové týmu. Technický poradce 1 bude přiřazen k úkolům Contoso India a Technický poradce 2 bude mít úkoly Contoso US.  

![Vygenerovaní obecní členové týmu](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> V aplikaci Project Service Automation verze 2 a 1 nedrží člen týmu organizační jednotku, která je spravována v úkolu na řádku.

![Úkoly na řádku verze 2 a 1 v aplikaci Project Service Automation](media/line-tasks-12.png)

Organizační jednotku můžete zobrazit v zobrazení odhadů. 

![Odhady organizační jednotky](media/org-unit-estimates-view-13.png)
 
Po dokončení upgradu bude organizační jednotka v úkolu na řádku, který odpovídá obecnému členovi týmu, přidána k obecnému členovi týmu a úkol na řádku bude odebrán. Proto doporučujeme před upgradem vygenerovat nebo znovu vygenerovat tým pro každý projekt, který obsahuje obecné zdroje.

Pro úkoly, které jsou přiřazeny k roli s organizační jednotkou, která se liší od organizační jednotky smluvního projektu, a ve kterých nebyl vygenerován tým, bude při upgradu vytvořen obecný člen týmu pro roli, ale použije se smluvní jednotka projektu pro organizační jednotku člena týmu. S ohledem na příklad Project Z smluvní organizační jednotce Contoso US a úkolům testování plánu projektu v rámci fáze implementace byla přiřazena role Technický poradce s organizační jednotkou přiřazenou společnosti Contoso India. Úkol testování integrace bude dokončen poté, co bude fáze implementace přiřazena k roli Technický poradce. Organizační jednotka je Contoso US a tým nebyl vygenerován. Upgrade vytvoří jednoho obecného člena týmu, technického poradce, který má přiřazené hodiny všech tří úkolů, a organizační jednotku Contoso US, což je smluvní organizační jednotka projektu.   
 
Změna výchozího nastavení různých organizačních jednotek zdroje u nevygenerovaných členů týmu je důvodem, proč doporučujeme vygenerovat nebo znovu vygenerovat tým pro každý projekt, který obsahuje obecné zdroje, ještě před upgradem, aby nedošlo ke ztrátě přiřazení organizační jednotky.



[!INCLUDE[footer-include](../includes/footer-banner.md)]