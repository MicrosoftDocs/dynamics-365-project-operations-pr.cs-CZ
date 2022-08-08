---
title: Migrace plně fakturovaných fakturačních milníků při přechodu
description: Tento článek vysvětluje, jak migrovat fakturační milníky s pevnou cenou, které byly zákazníkovi fakturovány za otevřené projektové smlouvy před datem uvedení do provozu.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028694"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrace plně fakturovaných fakturačních milníků při přechodu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

## <a name="scenario"></a>Scénář

Contoso přejde do ostrého provozu se scénáři Microsoft Dynamics 365 Project Operations založenými na zdrojích/položkách, které nejsou na skladě. V rámci aktivit přechodu musí realizační tým migrovat otevřené projektové smlouvy ze starého systému. Některé z projektových smluv zahrnují řádky smlouvy, které využívají metodu účtování s pevnou cenou a již byly částečně fakturovány koncovému zákazníkovi. Realizační tým musí tyto fakturační milníky migrovat jako typ **Faktura zákazníka zaúčtována**, protože musejí být zahrnuty do celkové hodnoty smlouvy pro účely účtování výnosů. Zůstatky zákazníků v pohledávkách a hlavní knize však nesmí být ovlivněny.

## <a name="solution"></a>Řešení

### <a name="prerequisites"></a>Předpoklady

- Musí být nainstalována aplikace Dynamics 365 Finance 10.0.24 nebo novější.
- Prostředí, kde budou dokončeny kroky migrace, musí být v režimu údržby. Během migrace milníků by neměly být prováděny žádné další činnosti.
- Kroky migrace musí být provedeny přesně tak, jak je zde popsáno, a lze je použít pouze pro činnost přechodu. Společnost Microsoft nepodporuje žádné jiné použití této schopnosti.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Vytvořte přechodovou verzi mapy s duálním zápisem milníků řádku smlouvy o integraci Project Operations 

1. Ujistěte se, že cílové mapování pro entitu **Milníky řádku smlouvy integrace Project Operations** je aktuální. 

    1. Ve Finance přejděte na **Správa dat** \> **Datové entity** a vyberte entitu **Milníky řádku smlouvy integrace Project Operations**. 
    2. Vyberte položku **Změnit mapování cíle**. 
    3. Na stránce **Mapovat fázování na cíl** vyberte **Generovat mapování** a poté potvrďte, že chcete vygenerovat mapování.

2. Zastavte a obnovte mapování s duálním zápisem **Milníky řádku smlouvy integrace Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Přejděte do nabídky **Správa dat** \> **Duální zápis**, vyberte mapu a otevřete její podrobnosti. 
    2. Vyberte příkaz **Zastavit** a počkejte, dokud systém nezastaví mapování. 
    3. Vyberte položku **Aktualizovat tabulky**.

3. Přidejte mapování pro stav transakce.

    1. Vyberte **Přidat mapování**.
    2. Na novém řádku vyberte ve sloupci **Finanční a provozní aplikace** pole **TRANSSTATUS\[TRANSSTATUS\]**.
    3. Ve sloupci **Microsoft Dataverse** vyberte **msdyn\_invoicestatus \[Stav faktury\]**.
    4. Ve sloupci **Typ mapy** vyberte šipku vpravo (**\>**).
    5. V dialogovém okně, které se objeví, vyberte v poli **Směr synchronizace** hodnotu **Dataverse do finančních a provozních aplikací**.
    6. Vyberte **Přidat transformaci**.
    7. V poli **Typ transformace** vyberte **ValueMap**.
    8. Vyberte položku **Přidat mapování hodnot**.
    9. V levém poli zadejte hodnotu **4**. V pravém poli zadejte hodnotu **192350001**. 
    10. Vyberte **Uložit** a zavřete dialogové okno.

4. Vyberte příkaz **Uložit jako** a uložte verzi mapy s duálním zápisem. 
5. V podokně **Přidat tabulku** v poli **Vydavatel** vyberte **Výchozí vydavatel**.
6. V poli **Verze** zapište verzi.
7. V poli **Popis** zadejte poznámku o této verzi přechodu mapy. 
8. Vyberte **Uložit**.
9. Spusťte mapu.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrace fakturovaných milníků do prostředí Dataverse

1. V prostředí Project Operations Dataverse vytvořte milníky, které mají stav faktury **Připraveno k fakturaci**. V tuto chvíli nemigrujte žádné milníky, které nebyly fakturovány.

    > [!NOTE]
    > Před migrací fakturačních milníků se ujistěte, že finanční dimenze související s řádkem projektové smlouvy jsou nastaveny podle očekávání. Po dokončení migrace nelze finanční dimenze upravit.

2. Po migraci všech milníků zastavte následující mapy s duálním zápisem:

    - Milníky řádku smlouvy integrace Project Operations (msdyn\_contractlinescheduleofvalues)
    - Skutečné hodnoty integrace Project Operations (ms\_dynactuals)
    - Návrh faktury projektu V2 (faktury)

    Mapu zastavíte tímto způsobem:

    1. Ve Finance přejděte do nabídky **Správa dat** \> **Duální zápis**, vyberte mapu a otevřete její podrobnosti.
    2. Vyberte příkaz **Zastavit** a počkejte, dokud systém nezastaví mapování.

3. V prostředí Project Operations Dataverse vytvářejte a potvrzujte proforma faktury za fakturační milníky. 

    1. Na mapě webu přejděte na projektové smlouvy, vyberte je a poté vyberte **Vytvořit faktury**.
    2. Po vytvoření faktur je otevřete z nabídky **Faktury** v mapě webu a poté vyberte **Potvrdit**.

    Tento krok vytvoří požadované záznamy v prostředí Dataverse. Nemá to však vliv na finance a pohledávky, protože dříve uvedené mapy s duálním zápisem byly zastaveny.

4. Po potvrzení všech proforma faktur vraťte všechny mapy s duálním zápisem do původního stavu.

    1. Aktualizujte verzi mapování s duálním zápisem **Milníky řádku smlouvy integrace Project Operations** (**msdyn\_contractlinescheduleofvalues**) zpět na původní. 
    2. Vyberte mapu s duálním zápisem v seznamu map, vyberte **Verze mapování tabulky** a poté vyberte původní verzi mapování tabulky.
    3. Vyberte **Uložit**.
    4. Restartujte následující mapy s duálním zápisem:

        - Milníky řádku smlouvy integrace Project Operations (msdyn\_contractlinescheduleofvalues)
        - Skutečné hodnoty integrace Project Operations (ms\_dynactuals)
        - Návrh faktury projektu V2 (faktury)

Milníky jsou nyní migrovány a systém je připraven na další kroky v aktivitě přechodu.
