---
title: Změny správy zdrojů (Project Service Automation 3.x)
description: Tento článek poskytuje informace o změnách v oblasti správy zdrojů.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cac11606811632bdc48f462eb3a09a163ba1620d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916004"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Změny správy zdrojů (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Části tohoto článku poskytují informace o změnách, které byly provedeny v oblasti správy zdrojů Dynamics 365 Project Service Automation verze 3.x.

## <a name="project-estimates"></a>Odhady projektů

Místo toho, aby byly odhady projektu založeny na entitě **msdyn\_** projecttask **(Projektový úkol)**, jsou založeny na entitě **msdyn\_resourceassignment** (**Přiřazení zdroje**). Přiřazení zdrojů se stala „zdrojem pravdy” pro plánování úkolů a tvorbu cen.

## <a name="line-tasks"></a>Úkoly na řádku

V PSA 3.x jsou úkoly na řádku zastaralé (vyřazené). Přiřazení nyní odkazují na celý úkol, nikoli na úkoly na řádku.

Následující příklad ukazuje, jak je úkol nazvaný „testovací úkol” přidělen členům týmu A a B v dřívějších verzích PSA a v PSA 3.x.

- **Před PSA 3.x:**

    - Testovací úkol

        - Testovací úkol – úkol na řádku 1

            - Přiřazení k A

        - Testovací úkol – úkol na řádku 2

            - Přiřazení k B

- **PSA 3.x:**

    - Testovací úkol

        - Přiřazení k A
        - Přiřazení k B

## <a name="unassigned-assignment"></a>Nepřiřazené přiřazení

V PSA 3.x je nepřiřazené přiřazení přiřazení, které je přiřazeno členu týmu **NULL** a prostředku **NULL** . Nepřiřazená přiřazení se mohou vyskytnout v několika scénářích:

- Pokud byl úkol vytvořen, ale dosud nebyl přiřazen žádné členovi týmu, je vždy vytvořeno nepřiřazené přiřazení. 
- Pokud jsou všechny přiřazené osoby v úkolu odebrány, bude pro tento úkol znovu vytvořeno nepřiřazené přiřazení.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Pole plánování entity Projektový úkol

Pole v entitě **\_msdyn projecttask** byla vyřazena nebo přesunuta do entity **msdyn\_resourceassignment** nebo je na ně nyní odkazováno z entity **msdyn\_projectteam** (**Člen projektového týmu**).

| Vyřazené pole v msdyn\_projecttask (Projektový úkol) | Nové pole v msdyn\_resourceassignment (Přiřazení zdroje) | Komentář |
|---|---|---|
| msdyn\_assignedresources | Žádný | |
| msdyn\_assignedteammembers | Žádný | |
| msdyn\_numberofresources | Žádný | |
| msdyn\_scheduledhours | Žádný | |
| msdyn\_effortcontour | msdyn\_plannedwork | Formát datové struktury JavaScript Object Notation (JSON), který je uložen v poli, byl změněn. |

## <a name="schedule-contour"></a>Průběhová křivka plánu

Průběhová křivka plánu je uložena v poli **Naplánovaná práce** (**msdyn\_plannedwork**) jednotlivých entit **Přiřazení zdroje** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struktura

Nová struktura průběhové křivky plánu se skládá z pružných časových úseků, které jsou definovány pro každý den plánu. Každý časový úsek má následující vlastnosti:

- **Začátek** – začátek pracovní doby pro daný den podle kalendáře projektu.
- **Konec** – konec pracovní doby pro daný den podle kalendáře projektu.
- **Hodiny** – počet hodin přiřazených k danému dnu.

**Příklad**

V tomto příkladu je použit kalendář projektu, kde pracovní den je od 9:00 do 17:00 v časovém pásmu UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatické plánování a ruční plánování

Pokud je úkol automaticky naplánován, jsou hodiny předem načteny a doba trvání úkolu může být snížena.

**Příklad**

Následující úkol je automaticky naplánován na 18 hodin během tří dnů (od 3. prosince 2018 do 5. prosince 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Pokud je úkol naplánován ručně, jsou hodiny rovnoměrně rozděleny do všech dat.

**Příklad**

Následující úkol je ručně naplánován na 18 hodin během tří dnů (od 3. prosince 2018 do 5. prosince 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Jednotka přiřazení

Jednotka přiřazení byla v PSA 3.x vyřazena. Hodiny úsilí úkolu jsou nyní rovnoměrně rozděleny na každý den, mezi všechny přiřazené zdroje.

**Příklad**

V tomto příkladu je úkol přiřazen dvěma zdrojům a je automaticky naplánován na 36 hodin během tří dnů (od 3. prosince 2018 do 5. prosince 2018).

- Přiřazení 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Přiřazení 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Cenové dimenze

V PSA 3.x byla z entity **msdyn\_projecttask** odebrána pole cenových dimenzí specifická pro konkrétní zdroj (jako např. **Role** a **Organizační jednotka**). Tato pole lze nyní načíst z odpovídajícího člena projektového týmu (**msdyn\_projectteam**) přiřazení zdroje (**msdyn\_resourceassignment**) při generování odhadů projektu. Nové pole **msdyn\_organizationalunit** bylo přidáno do entity **msdyn\_projectteam**.

| Vyřazené pole v msdyn\_projecttask (Projektový úkol) | Pole z modulu msdyn\_projectteam (Člen projektového týmu), které je použito místo |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Průběhové křivky

Pole průběhové křivky ocenění a odhadu byla v entitě **msdyn\_projecttask** vyřazena. Byla přesunuta do entity **msdyn\_resourceassignment**.

| Vyřazené pole v msdyn\_projecttask (Projektový úkol) | Nové pole v msdyn\_resourceassignment (Přiřazení zdroje) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Do entity **msdyn\_resourceassignment** byla přidána následující pole.

* msdyn\_plannedcost
* msdyn\_plannedsales

Následující pole pro plánované, skutečné a zbývající náklady a prodej zůstávají v entitě **msdyn\_projecttask** beze změny:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
