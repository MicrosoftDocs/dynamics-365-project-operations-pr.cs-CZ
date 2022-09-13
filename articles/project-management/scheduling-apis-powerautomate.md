---
title: Použití rozhraní API projektového plánu s Power Automate
description: Tento článek poskytuje ukázkový tok, který používá rozhraní API (Project schedule application programming interface).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404393"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Použití rozhraní API projektového plánu s Power Automate

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Tento článek popisuje ukázkový tok, který ukazuje, jak vytvořit úplný plán projektu pomocí Microsoft Power Automate, jak vytvořit sadu operací a jak aktualizovat entitu. Příklad ukazuje, jak vytvořit projekt, člena projektového týmu, sady operací, projektové úkoly a přiřazení zdrojů. Tento článek také vysvětluje, jak aktualizovat entitu a provést sadu operací.

Následuje úplný seznam kroků, které jsou zdokumentovány ve vzorovém toku v tomto článku:

1. [Vytvoření spouštěče PowerApps](#1)
2. [Vytvoření projektu](#2)
3. [Inicializujte proměnnou pro člena týmu](#3)
4. [Vytvoření obecného člena týmu](#4)
5. [Vytvoření sady operacíí](#5)
6. [Vytvoření kbelíku projektu](#6)
7. [Inicializujte proměnnou pro stav odkazu](#7)
8. [Inicializujte proměnnou počtu úkolů](#8)
9. [Inicializujte proměnnou pro ID projektového úkolu](#9)
10. [Dělat dokud](#10)
11. [Nastavit projektový úkol](#11)
12. [Vytvořit projektový úkol](#12)
13. [Vytvoření přiřazení zdroje](#13)
14. [Snížit proměnnou](#14)
15. [Přejmenovat projektový úkol](#15)
16. [Spustit sadu operacíí](#16)

## <a name="assumptions"></a>Předpoklady

Tento článek předpokládá, že máte základní znalosti o platformě Dataverse, cloudových tocích a Project Schedule Application Programming Interface (API). Více informací naleznete v části [Reference](#references) v dále v tomto článku.

## <a name="create-a-flow"></a>Vytvoření toku

### <a name="select-an-environment"></a>Vyberte prostředí.

Ve svém prostředí můžete vytvářet tok Power Automate.

1. Přejděte na <https://flow.microsoft.com> a přihlaste se pomocí přihlašovacích údajů správce.
2. V pravém horním rohu vyberte **Prostředí**.
3. V seznamu vyberte prostředí, kde je nainstalována aplikace Dynamics 365 Project Operations.

### <a name="create-a-solution"></a>Vytvoření řešení

Pokud chcete vytvořit [tok s podporou řešení](/power-automate/overview-solution-flows), postupujte podle těchto kroků. Vytvořením toku s podporou řešení můžete tok snadněji exportovat a použít jej později.

1. V levém navigačním podokně vyberte **Řešení**.
2. Na stránce **Řešení** vyberte **Nové řešení**.
3. V dialogovém okně **Nové řešení** nastavte požadovaná pole a poté vyberte **Vytvořit**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Krok 1: Vytvoření spouštěče PowerApps

1. Na stránce **Řešení** vyberte řešení, které jste vytvořili, a poté vyberte **Nový**.
2. V levém podokně vyberte **Cloudové toky** \> **Automatizace** \> **Cloudový tok** \> **Okamžitý**.
3. Do pole **Název toku** zadejte **Naplánovat ukázkový tok API**.
4. V seznamu **Vyberte, jak tento tok spustit** vyberte **Power Apps**. Když vytvoříte trigger Power Apps, logika je na vás jako autorovi. V tomto článku ponechte vstupní parametry prázdné pro účely testování.
5. Vyberte **Vytvořit**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Krok 2: Vytvoření projektu

Při vytváření vzorového projektu postupujte takto.

1. V toku, který jste vytvořili, vyberte **Nový krok**.

    ![Přidat nový krok.](media/newstep.png)

2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **provedení nevázané akce**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.

    ![Výběr operace.](media/chooseactiontab.png)

3. V novém kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.

![Přejmenování kroku](media/renamestep.png)

4. Přejmenujte krok **Vytvořit projekt**.
5. Do pole **Název akce** vyberte **msdyn\_CreateProjectV1**.
6. V poli **msdyn\_subject** vyberte **Přidat dynamický obsah**.
7. Na kartě **Výraz**, do pole funkce zadejte **Název projektu - utcNow()**.
8. Vyberte položku **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Krok 3: Inicializujte proměnnou pro člena týmu

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **inicializace proměnné**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V novém kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Init člen týmu**.
5. Do pole **Název** vložte **TeamMemberAction**.
6. V poli **Typ** vyberte **Řetězec**.
7. V poli **Hodnota** zadejte **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Krok 4: Vytvořte obecného člena projektového týmu

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **provedení nevázané akce**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V novém kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Vytvořit člena týmu**.
5. V poli **Název akce** vyberte **TeamMemberAction** v dialogovém okně **Dynamický obsah**.
6. V poli **Parametry akce** zadejte následující informace o parametrech.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Následuje vysvětlení parametrů:

    - **\@\@odata.type** – Název typu entity. Například zadejte **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projektteamid** – Primární klíč ID projektového týmu. Hodnota je výraz globálně jedinečný identifikátor (GUID).   ID se generuje z karty výraz.

    - **msdyn\_project\@odata.bind** – ID projektu úkolu vlastnícího úkolu. Hodnota bude dynamický obsah, který pochází z odezvy kroku „Vytvořit projekt“. Ujistěte se, že jste zadali úplnou cestu a přidali dynamický obsah do závorek. Uvozovky jsou povinné. Například zadejte **"/msdyn\_projekty (PŘIDAT DYNAMICKÝ OBSAH)“**.
    - **msdyn\_name** – Jméno člena týmu. Například zadejte **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Krok 5: Vytvoření sady operacíí

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **provedení nevázané akce**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V novém kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Vytvořit sadu operací**.
5. V poli **Název akce** vyberte **msdyn\_CreateOperationSetV1**, což je vlastní akce Dataverse.
6. V poli **Popis** zadejte **ScheduleAPIDemoOperationSet**.
7. Do pole **Projekt** zadejte **/msdyn\_projects(**.
8. V dialogovém okně **Dynamický obsah** vyberte **msdyn\_CreateProjectV1Response ProjectId**.
9. Do pole **Projekt** zadejte **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Krok 6: Vytvoření kbelíku projektu

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **přidat nový řádek**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V novém kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Vytvořit kbelík**.
5. Do pole **Název tabulky** vyberte **Kbelíky projektu**.
6. Do pole **Název** vložte **ScheduleAPIDemoBucket1**.
7. Do pole **Projekt** vyberte **msdyn\_CreateProjectV1Response ProjectId** v dialogovém okně **Dynamický obsah**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Krok 7: Inicializujte proměnnou pro stav odkazu

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **inicializace proměnné**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V novém kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Init linkstatus**.
5. Do pole **Název** vložte **linkstatus**.
6. V poli **Typ** vyberte **Integer**.
7. Do pole **Hodnota** zadejte **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Krok 8: Inicializujte proměnnou počtu úkolů

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **inicializace proměnné**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V novém kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Init Počet úkolů**.
5. Do pole **Název** vložte **počet úkolů**.
6. V poli **Typ** vyberte **Integer**.
7. Do pole **Hodnota** zadejte **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Krok 9: Inicializujte proměnnou pro ID projektového úkolu

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **inicializace proměnné**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V novém kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Init ProjectTaskID**.
5. Do pole **Název** vložte **počet úkolů**.
6. V poli **Typ** vyberte **Řetězec**.
7. Do pole **Hodnota** zadejte **guid()** v nástroji pro tvorbu výrazů.

## <a name="step-10-do-until"></a><a id="10"></a>Krok 10: Provádět dokud

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **provádět dokud**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. Nastavte první hodnotu v podmíněném příkazu na proměnnou **počet úkolů** z dialogového okna **Dynamický obsah**.
4. Nastavte podmínku na **menší než nebo rovno**.
5. Nastavte druhou hodnotu v podmíněném příkazu na **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Krok 11: Nastavit projektový úkol

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **nastavit proměnnou**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V novém kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Nastavit projektový úkol**.
5. Do pole **Název** vyberte **msdyn\_projecttaskid**.
6. Do pole **Hodnota** zadejte **guid()** v nástroji pro tvorbu výrazů.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Krok 12: Vytvoření projektového úkolu

Chcete-li vytvořit projektový úkol, který má jedinečné ID, které náleží aktuálnímu projektu a vámi vytvořenému segmentu projektu, postupujte podle těchto kroků.

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **provedení nevázané akce**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V tomto kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Vytvořit projektový úkol**.
5. Do pole **Název akce** vyberte **msdyn\_PssCreateV1**.
6. V poli **Entita** zadejte následující informace o parametrech.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Následuje vysvětlení parametrů:

    - **\@\@odata.type** – Název typu entity. Například zadejte **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – Jedinečné ID úkolu. Hodnota by měla být nastavena na dynamickou proměnnou z **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – ID projektu úkolu vlastnícího úkolu. Hodnota bude dynamický obsah, který pochází z odezvy kroku „Vytvořit projekt“. Ujistěte se, že jste zadali úplnou cestu a přidali dynamický obsah do závorek. Uvozovky jsou povinné. Například zadejte **"/msdyn\_projekty (PŘIDAT DYNAMICKÝ OBSAH)“**.
    - **msdyn\_subject** – Libovolný název úkolu.
    - **msdyn\_projectbucket\@odata.bind** – Kbelík projektu, který obsahuje úkoly. Hodnota bude dynamický obsah, který pochází z odezvy kroku „Vytvořit kbelík“. Ujistěte se, že jste zadali úplnou cestu a přidali dynamický obsah do závorek. Uvozovky jsou povinné. Například zadejte **"/msdyn\_projectbuckets(PŘIDAT DYNAMICKÝ OBSAH)“**.
    - **msdyn\_start** – Dynamický obsah pro datum zahájení. Například zítřek bude reprezentován jako **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Plánované datum zahájení operace. Například zítřek bude reprezentován jako **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Plánované datum ukončení. Vyberte datum v budoucnosti. Například zadejte **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Stav odkazu. Například zadejte **"192350000"**.

7. Do pole **OperationSetId** vyberte **msdyn\_CreateOperationSetV1Response** v dialogovém okně **Dynamický obsah**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Krok 13: Vytvoření přiřazení zdrojů

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **provedení nevázané akce**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V tomto kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Vytvořit přiřazení**.
5. Do pole **Název akce** vyberte **msdyn\_PssCreateV1**.
6. V poli **Entita** zadejte následující informace o parametrech.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Do pole **OperationSetId** vyberte **msdyn\_CreateOperationSetV1Response** v dialogovém okně **Dynamický obsah**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Krok 14: Snížit proměnnou

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **snížení proměnné**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V poli **Název** vyberte **počet úkolů**.
4. Do pole **Hodnota** zadejte **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Krok 15: Přejmenujte projektový úkol

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **provedení nevázané akce**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V tomto kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Přejmenovat projektový úkol**.
5. Do pole **Název akce** vyberte **msdyn\_PssUpdateV1**.
6. V poli **Entita** zadejte následující informace o parametrech.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Do pole **OperationSetId** vyberte **msdyn\_CreateOperationSetV1Response** v dialogovém okně **Dynamický obsah**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Krok 16: Spuštění sady operacíí

1. V toku vyberte **Nový krok**.
2. V dialogovém okně **Vybrat operaci** zadejte do vyhledávacího pole **provedení nevázané akce**. Poté na kartě **Akce** vyberte operaci v seznamu výsledků.
3. V tomto kroku vyberte tři tečky (**...**) a potom vyberte **Přejmenovat**.
4. Přejmenujte krok **Provést sadu operací**.
5. Do pole **Název akce** vyberte **msdyn\_ExecuteOperationSetV1**.
6. Do pole **OperationSetId** vyberte **msdyn\_CreateOperationSetV1Response OperationSetId** v dialogovém okně **Dynamický obsah**.

## <a name="references"></a>Odkazy

- [Přehled způsobu integrace toků s Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [K provádění operací s entitami plánování použijte rozhraní API pro plánování projektu](schedule-api-preview.md)
- [Přehled cloudových toků - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Přehled toků s podporou řešení - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
