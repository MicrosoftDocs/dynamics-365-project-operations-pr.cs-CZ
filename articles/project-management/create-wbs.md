---
title: Vytvoření strukturovaného rozpisu prací
description: Tento téma vysvětluje, jak vytvořit strukturovaný rozpis práce (WBS) včetně základních ovládacích prvků v novém plánovacím rozhraní.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d7fa645e78d2206e333d9f85fcec0f7a9c213c23
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841319"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Vytvoření strukturovaného rozpisu prací (WBS)

Plán projektu uvádí, jaká práce se musí dokončit, které zdroje práci vykonají a časový rámec, ve kterém se musí práce dokončit. Plán odráží všechny práce související s dodáním projektu včas. V Dynamics 365 Project Operations vytvoříte harmonogram projektu takto:

  - Rozdělení práce na zvládnutelné úkoly.
  - Odhad času potřebného k provedení každého úkolu.
  - Nastavení závislostí úkolů.
  - Nastavení doby trvání úkolu.
  - Odhad obecných zdrojů, které budou dělat úkoly. 

Plán projektu je vytvořen na kartě **Plán** na stránce **Projekt**.

## <a name="tasks"></a>Úkoly

Prvním krokem při vytváření plánu projektu je rozdělení práce do zvládnutelných částí. Plán v Project Operations podporuje následující funkce:

- Souhrnné úkoly nebo úkoly kontejneru
- Úkoly uzlu typu list

### <a name="summary-tasks"></a>Souhrnné úlohy

Souhrnné úkoly mohou ukládat další souhrnné úkoly nebo úkoly v uzlech. Neobsahují žádné vlastní pracovní úsilí nebo náklady. Jejich pracovní úsilí a náklady jsou spíše shrnutím pracovního úsilí a nákladů jejich úkolů kontejneru. Počátečním datem souhrnného úkolu je datum zahájení úkolů kontejneru a koncovým datem je datum ukončení úkolů kontejneru. Název souhrnného úkolu lze upravit, ale vlastnosti plánování, včetně práce, data a doby trvání, nelze upravit. Odstraníte-li souhrnný úkol, odstraníte také všechny jeho úkoly kontejneru.

### <a name="leaf-node-tasks"></a>Úkoly uzlu typu list

Úkoly uzlu typu list představují nejpodrobnější práci na projektu. Obsahují odhadnuté úsilí, zdroje, plánované datum zahájení a ukončení a dobu trvání.

## <a name="create-a-task-hierarchy"></a>Vytvoření hierarchie úkolů

### <a name="add-a-task"></a>Přidání úkolu

Chcete-li přidat jeden nebo více úkolů, postupujte dle následujících instrukcí.

1. Přejděte na **Projekty** a vyberte a otevřete záznam projektu, pro který chcete vytvořit plán. 
2. Vyberte kartu **Úkoly**. 
3. Vyberte **Přidat nový úkol**, zadejte název úkolu a stiskněte klávesu Enter.
2. Zadejte jiný název úkolu a znovu stiskněte klávesu Enter, dokud nebudete mít úplný seznam úkolů.

### <a name="manage-hierarchy-of-a-task"></a>Správa hierarchie úkolu

Pokud je úkol odsazen, stává se podřízeným úkolem úkolu, který je přímo nad ním. ID plánu úkolu je pak přepočítáno tak, že je založeno na ID plánu jeho nového nadřazeného úkolu a následuje schéma číslování osnovy. Nadřazený úkol je nyní souhrnný úkol. Proto se stane souhrnem svých podřízených úkolů. Je-li zvýšena úroveň úkolu, tak už není podřízeným úkolem úkolu, který mu byl nadřazen. ID plánu je pak přepočítáno tak, aby odráželo aktualizovanou hloubku a umístění úkolu v hierarchii. Úsilí, náklady a data předchozího nadřazeného úkolu jsou přepočítány tak, aby nezahrnovaly tento úkol.

Chcete-li odsadit nebo zvýšit úroveň úkolu, postupujte dle následujících instrukcí.

1. Na stránce **Projekt** na kartě **Úkoly** pod **Souhrnné úkoly** vyberte tři svislé tečky podle názvu úkolu a poté vyberte **Vytvořit dílčí úkol**. 
2. Vyberte úkol, který chcete odsadit nebo jehož úroveň chcete zvýšit. Chcete-li vybrat více než jeden úkol, vyberte úkol, stiskněte a podržte Ctrl a poté vyberte další úkol.
2. Vyberte **Odsadit** nebo **Zvýšit úroveň dílčího úkolu**, chcete-li přesunout úkoly pod nebo mimo souhrnné úkoly.

### <a name="move-tasks-up-and-down"></a>Posun úkolů nahoru a dolů

Úkoly lze přesunout na libovolnou úroveň ve strukturovaném rozpisu prací jedním ze dvou způsobů:

- Vyberte ještě jeden úkol a přetáhněte je na požadované místo.
- Vyberte jeden nebo více úkolů, klikněte pravým tlačítkem a vyberte **Vyjmout**, vyberte cílovou buňku v plánu a poté klikněte pravým tlačítkem a vyberte **Vložit**.

## <a name="task-attributes"></a>Atributy úkolu

Název úkolu popisuje práci, která musí být provedena. V Project Operations popisují atributy přidružené k úkolu plán úkolu a požadavky na personální obsazení.

## <a name="schedule-attributes"></a>Plánování atributů

Atributy **Úsilí**, **Počáteční datum**, **Koncové datum** a **Doba trvání** definují plán úkolu.

V následující tabulce jsou uvedeny další atributy plánu.

| **Konečný zobrazovaný název** | **Konečný popis** |
| --- | --- |
| Vynaložené úsilí (hodiny) | Dokončená práce na úkolu v hodinách |
| Doba trvání | Zobrazuje dobu trvání úkolu ve dnech. |
| Celková práce | Celkový objem práce na úkolu v hodinách |
| Dokončení | Datum a čas dokončení. |
| Dokončeno % | Procento dokončení úkolu. |
| Kbelík projektu | Panel úkolů lze seskupit podle kbelíku, takže má každý kbelík svůj vlastní sloupec. |
| Zbývající úsilí (hodiny) | Zbývající práce na úkolu v hodinách. |
| Začátek | Datum a čas zahájení. |
| Jméno | Název úkolu. |
| ID | Identifikátor úkolu ve strukturovaném rozpisu prací. |

## <a name="staffing-attributes"></a>Personální atributy

K atributům personálního obsazení se přistupuje prostřednictvím pole **Zdroje** v plánu. Můžete buď vyhledat existující zdroj, nebo vybrat **Vytvořit** a v podokně **Vytvořit** přidat člena projektového týmu jako nový zdroj.

Pole **Role**, **Jednotka zdroje** a **Název pozice** slouží k popisu požadavků na personální obsazení úkolu. Tyto atributy personálního obsazení se společně s plánem úkolů používají k nalezení dostupných zdrojů pro vykonání tohoto úkolu.

   - **Role**: určete typ prostředku, který je vyžadován k provádění úkolu.
   - **Jednotka zdroje**: určete jednotku, ze které mají být přiřazeny zdroje pro daný úkol. Tento atribut ovlivňuje odhad nákladů a prodeje pro daný úkol, pokud jsou sazby nákladů a fakturační sazby pro daný zdroj nastaveny na základě jednotek zdroje.
   - **Název pozice**: zadejte název obecného zdroje, který slouží jako zástupný název zdroje, který bude tuto práci nakonec provádět.

Pole **Zdroje** obsahuje název pozice obecného zdroje nebo pojmenovaného zdroje, pokud existují.

Pole **Kategorie** obsahuje hodnoty, které označují širší typ práce, do kterého lze úkol seskupit. Toto pole nemá vliv na plánování nebo personálního obsazení. Místo toho se pole používá pouze pro vykazování.

## <a name="task-dependencies"></a>Závislosti úkolu

Pomocí plánu můžete v Project Operations mezi úkoly vytvořit vztahy předchůdců. Pole **Předchůdce** v používá jednu nebo více hodnot, které označují úkoly, na kterých úkol závisí. Když k úkolu přiřadíte hodnoty předchůdců, lze úkol zahájit pouze v případě, že byly dokončeny všechny úkoly typu předchůdce. Vzhledem k závislosti je plánované datum zahájení úkolu znovu nastaveno na datum, kdy byly dokončeny předchozí úkoly.

Režim úkolu nemá žádný vliv na aktualizace dat zahájení a ukončení předchozích/závislých úkolů.

## <a name="accessibility-and-keyboard-shortcuts"></a>Usnadnění a klávesové zkratky

Mřížka **Plán** je plně přístupná a lze ji použít se čtečkami obrazovky, jako jsou např. Narrator, JAWS nebo NVDA. Oblast mřížky můžete procházet pomocí kláves se šipkami (jako v aplikaci Microsoft Excel), pomocí klávesy Tab můžete procházet interaktivní prvky uživatelského rozhraní a pomocí klávesy se šipkou dolů, klávesy Enter nebo mezerníku vybrat a otevřít rozevírací nabídky.
