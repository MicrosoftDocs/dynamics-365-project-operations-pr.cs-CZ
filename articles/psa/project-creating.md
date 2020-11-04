---
title: Plány projektu
description: Toto téma obsahuje informace o způsobu vytvoření plánu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073815"
---
# <a name="project-schedules"></a>Plány projektu 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Plán projektu uvádí, jaká práce se musí dokončit, které zdroje práci vykonají a časový rámec, ve kterém se musí práce dokončit. Odráží všechny práce související s dodáním projektu včas. V Dynamics 365 Project Service Automation vytvoříte plán projektu rozdělením práce do zvládnutelných úkolů, odhadem doby potřebné k provedení jednotlivých úkolů, nastavením závislostí úkolů, nastavení doby trvání úkolů a odhadem obecných zdrojů, které budou úkoly provádět. Plán projektu je vytvořen na kartě **Plán** na stránce projektu.
 
## <a name="tasks"></a>Úkoly

Prvním krokem při vytváření plánu projektu je rozdělení práce do zvládnutelných částí. Plán v PSA podporuje následující funkce:

- Kořenový uzel projektu.
- Souhrnné úkoly nebo úkoly kontejneru
- Úkoly uzlu typu list

### <a name="project-root-node"></a>Kořenový uzel projektu.

Kořenový uzel projektu je souhrnný úkol nejvyšší úrovně pro projekt. Všechny ostatní úkoly projektu jsou vytvořeny pod ním. Název kořenového uzlu je vždy nastaven na název projektu. Úsilí, data a doba trvání kořenového uzlu jsou shrnuty na základě hodnot v hierarchii pod ním. Vlastnosti kořenového uzlu nelze upravovat. Kořenový uzel také nelze odstranit.

### <a name="summary-or-container-tasks"></a>Souhrnné úkoly nebo úkoly kontejneru 

Souhrnné úkoly mají pod sebou dílčí úkoly nebo úkoly kontejneru. Neobsahují žádné vlastní pracovní úsilí nebo náklady. Jejich pracovní úsilí a náklady jsou spíše shrnutím pracovního úsilí a nákladů jejich úkolů kontejneru. Počátečním datem souhrnného úkolu je datum zahájení úkolů kontejneru a koncovým datem je datum ukončení úkolů kontejneru. Název souhrnného úkolu lze upravit, ale vlastnosti plánování (úsilí, data a dobu trvání) nelze upravit. Odstraníte-li souhrnný úkol, odstraníte také všechny jeho úkoly kontejneru.

### <a name="leaf-node-tasks"></a>Úkoly uzlu typu list

Úkoly uzlu typu list představují nejpodrobnější práci na projektu. Obsahují odhadnuté úsilí, zdroje, plánované datum zahájení a ukončení a dobu trvání.
 
## <a name="creating-a-task-hierarchy"></a>Vytvoření hierarchie úkolů

Hierarchii úkolů můžete vytvořit pomocí následujících možností:

- Tlačítko **Přidat úkol**
- Tlačítko **Zvětšit odsazení úkolu**
- Tlačítko **Zmenšit odsazení úkolu**
- Tlačítka **Posunout nahoru** a **Posunout dolů**
- Usnadnění a klávesové zkratky

### <a name="add-task"></a>Přidat úkol

Tlačítko **Přidat úkol** umožňuje vytvořit nový úkol v hierarchii. Pokud nevyberete umístění, tak se nový úkol vloží na konec. 

Každému úkolu je přiřazeno ID plánu. ID plánu představuje hloubku a umístění úkolu v hierarchii. Používá číslování osnovy. U úkolů na první úrovni pod kořenovým uzlem projektu se používá schéma číslování 1, 2, 3 atd. U úkolů pod první úrovní se používá schéma číslování 1.1, 1.2, 1.3 atd.

### <a name="indent-task"></a>Zvětšit odsazení úkolu

Pokud je úkol odsazen, stává se podřízeným úkolem úkolu, který je přímo nad ním. ID plánu úkolu je pak přepočítáno tak, že je založeno na ID plánu jeho nového nadřazeného úkolu a následuje schéma číslování osnovy. Nadřazeným úkolem je nyní souhrnný úkol nebo úkol kontejneru. Proto se stane souhrnem svých podřízených úkolů.

### <a name="outdent-task"></a>Zmenšit odsazení úkolu 

Je-li úkol předsazen, tak už není podřízeným úkolem úkolu, který mu byl nadřazen. ID plánu je pak přepočítáno tak, aby odráželo aktualizovanou hloubku a umístění úkolu v hierarchii. Úsilí, náklady a data předchozího nadřazeného úkolu jsou přepočítány tak, aby nezahrnovaly tento úkol.

### <a name="move-up-and-move-down"></a>Posunout nahoru a Posunout dolů 

Tlačítka **Posunout nahoru** a **Posunout dolů** změní pozici úkolu v jeho nadřazené hierarchii. Změny tohoto typu neovlivňují úsilí, náklady, data ani dobu trvání úkolu. Ovlivňují pouze ID plánu úkolu. ID plánu je pak přepočítáno tak, aby odráželo novou pozici úkolu v seznamu podřízených úkolů nadřízeného úkolu.

### <a name="accessibility-and-keyboard-shortcuts"></a>Usnadnění a klávesové zkratky

Mřížka **Plán** je plně přístupná a lze ji použít se čtečkami obrazovky, jako jsou např. Narrator, JAWS nebo NVDA. Oblast mřížky můžete procházet pomocí kláves se šipkami (jako v aplikaci Microsoft Excel), pomocí klávesy Tab můžete procházet interaktivní prvky uživatelského rozhraní a pomocí klávesy se šipkou dolů, klávesy Enter nebo mezerníku vybrat a vyvolat rozevírací nabídky. Záhlaví sloupců jsou také interaktivní. Sloupce můžete skrýt nebo zobrazit, pomocí klávesy Tab a kláves se šipkami se pohybovat záhlavími sloupců a používat tlačítka akcí na panelu nástrojů. Kromě toho můžete použít následující klávesové zkratky:

- **Aktualizovat** : ALT+SHIFT+F5
- **Přidat** : ALT+SHIFT+Insert
- **Odstranit** : ALT+SHIFT+Delete
- **Přesunout nahoru/dolů** : ALT+SHIFT+šipky nahoru/dolů
- **Zvětšit/zmenšit odsazení** : ALT_SHIFT+šipky vlevo/vpravo
- **Rozbalit/sbalit hierarchie** : ALT+SHIFT+klávesy plus/minus

## <a name="task-attributes"></a>Atributy úkolu

Název úkolu popisuje práci, která musí být provedena. V PSA popisují atributy přidružené k úkolu plán úkolu a požadavky na personální obsazení.

> ![Atributy úkolu](media/project-2.png)
 
### <a name="schedule-attributes"></a>Plánování atributů

Atributy **Úsilí** , **Počáteční datum** , **Koncové datum** a **Doba trvání** definují plán úkolu.

Mezi další atributy plánu patří:

- **Úsilí v hodinách** : zadejte odhad hodin potřebných k dokončení úkolu. 
- **Doba trvání** : zadejte počet pracovních dnů potřebných k dokončení úkolu.
- **ID plánu** : toto automaticky generované ID se používá k řazení úkolů v hierarchii. Závislosti mezi úkoly řídí aktuální pořadí, ve kterém jsou úkoly zpracovávány.
 
### <a name="staffing-attributes"></a>Personální atributy

K atributům personálního obsazení se přistupuje prostřednictvím pole **Zdroje** v plánu. Můžete buď vyhledat existující zdroj, nebo kliknout na **Vytvořit** a v podokně **Vytvořit** přidat člena projektového týmu jako nový zdroj.

Pole **Role** , **Jednotka zdroje** a **Název pozice** slouží k popisu požadavků na personální obsazení úkolu. Tyto atributy personálního obsazení se společně s plánem úkolů používají k nalezení dostupných zdrojů pro vykonání tohoto úkolu.

**Role** – určete typ prostředku, který je vyžadován k provádění úkolu.

**Jednotka zdroje** – určete jednotku, ze které mají být přiřazeny zdroje pro daný úkol. Tento atribut ovlivňuje odhad nákladů a prodeje pro daný úkol, pokud jsou sazby nákladů a fakturační sazby pro daný zdroj nastaveny na základě jednotek zdroje.

**Název pozice** – zadejte popisný název obecného zdroje, který slouží jako zástupný název zdroje, který bude tuto práci nakonec provádět.

Pole **Zdroje** obsahuje název pozice obecného zdroje nebo pojmenovaného zdroje, pokud existují.

Pole **Kategorie** obsahuje hodnoty, které označují širší typ práce, do kterého lze úkol seskupit. Toto pole nemá vliv na plánování nebo personálního obsazení. Používá se pouze pro vykazování.

### <a name="task-dependencies"></a>Závislosti úkolu 

Pomocí plánu můžete v PSA mezi úkoly vytvořit vztahy předchůdců. Pole **Předchůdce** v části **Úkoly** přebírá jednu nebo více hodnot, které označují úkoly, na kterých úkol závisí. Když k úkolu přiřadíte hodnoty předchůdců, lze úkol zahájit pouze v případě, že byly dokončeny všechny úkoly typu předchůdce. Vzhledem k závislosti je plánované datum zahájení úkolu znovu nastaveno na datum, kdy byly dokončeny předchozí úkoly.

Režim úkolu nemá žádný vliv na aktualizace dat zahájení a ukončení předchozích/závislých úkolů.

## <a name="task-mode"></a>Režim úkolu 

Režim úkolu určuje plánování úkolů uzlů typu list. PSA podporuje pro každý úkol dva režimy úkolů: automatické plánování a ruční plánování.

### <a name="auto-scheduling"></a>Automatické plánování 
 
Při nastavení režimu úkolu na **Automaticky naplánováno** používá modul plánování úkolu pravidla plánování na tributy úkolu k určení plánu úkolu:

#### <a name="scheduling-rules"></a>Pravidla plánování

Nemá-li úkol uzlu typu list předchůdce, nastaví se počáteční datum ve výchozím nastavení na plánované datum zahájení projektu. Doba trvání úkolu uzlu typu list se vždy počítá jako počet pracovních dnů mezi jeho počátečním a koncovým datem. Když je úkol naplánován automaticky, plánovací modul postupujte podle následujících pravidel:

- Datum zahájení a ukončení úkolu musí být podle plánovacího kalendáře projektu pracovní dny 
- Datum zahájení libovolného úkolu, který má předchůdce, se automaticky nastaví na nejpozdější datum ukončení jeho předchůdců.
- Úsilí se vypočte pomocí tohoto vzorce: počet osob × doba trvání × hodiny ve standardní pracovní den v kalendáři projektu.

### <a name="manual-scheduling"></a>Ruční plánování

Pokud pravidla automatického plánování nesplňují vaše požadavky, můžete nastavit režim úkolu pro úkol na **Ručně naplánováno**. Toto nastavení zabrání plánovacímu modulu ve výpočtu hodnot dalších atributů plánování. Nastavíte-li u úkolů předchůdce, bude bez ohledu na režim úkolu vždy ovlivněno počáteční datum závislého úkolu.
