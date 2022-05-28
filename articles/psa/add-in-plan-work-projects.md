---
title: Plánování práce v Microsoft Project s doplňkem Project Service
description: Toto téma obsahuje informace o způsobu použití doplňku Microsoft project pro Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 1b1c9861f2a3fbb62b29ccad272dab28dc766439
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727996"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Plánování práce v Microsoft Project s doplňkem Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vám usnadňuje plánování projektů, a to včetně odhadů. Můžete definovat práci tak, aby náklady, úsilí a hodnota prodeje byly jasné již při odesílání konečného návrhu.  

Můžete nainstalovat [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] a plánovat práci ve známém prostředí aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Využívejte výkonné možnosti plánování a správy aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a aktualizujte plán projektu v nástroji Project Service Automation.  

> [!IMPORTANT]
> - Chcete-li použít funkci správy dokumentů SharePoint pro uložení souborů [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] projektů [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], musí váš správce aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] zapnout správu dokumentů. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] je kompatibilní pouze s aplikací [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Stažení a instalace doplňku  
 Připravte si přihlašovací informace pro [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Tyto informace budete potřebovat pro připojení z aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] k [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Z webu Download Center si můžete stáhnout doplněk pro podporovanou verzi Project Service, a to buď [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) nebo [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Vyberte odkaz ke stažení.  

3.  Po dokončení stahování vybráním tlačítka **Ano** nainstalujte doplněk.  

## <a name="configure-the-add-in"></a>Konfigurace doplňku  

1. Otevřete aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a vyberte kartu **Project Service**.  

2. Vyberte **Připojit**.  

3. Zadejte své přihlašovací informace a poté vyberte tlačítko **Přihlásit**.  

   Nyní můžete doplněk začít používat.  

## <a name="read-from-a-template"></a>Čtení ze šablony  
 Plánování projektu zahájíte tím, že budete číst ze šablony vytvořené v nástroji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a zkopírované do aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Vytvoření šablony projektu (Project Service Automation)](../psa/create-project-template.md)  

1.  Z karty **Project Service** vyberte tlačítko **Číst** > **Šablona projektu nástroje Project Service Automation**.  

2.  Ze seznamu zvolte šablonu projektu a potom vyberte tlačítko **Otevřít**.  

    > [!NOTE]
    >  Ve výchozím nastavení jsou úkoly, které jsou zkopírovány ze šablony do projektu, nastaveny jako ručně naplánované.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Přiřazení rolí [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ke zdrojům projektu  

1.  Otevřete projekt a vyberte pás karet **Úkol**.  

2. Vyberte nabídku **Ganttův diagram** a pak zvolte **Seznam zdrojů**.  

3. V zobrazení Seznam zdrojů vyberte na rozevírací nabídku **Role zdroje Project Service** a zvolte roli Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Poskytnutí zdrojů projektu  

1.  Na kartě Project Service vyberte řádek a vyberte tlačítko **Najít zdroje**.  

2.  Na obrazovce **Rezervovat zdroj** vyberte zdroj, který chcete použít pro projekt.  

3.  Zvolte **Rezervovat** a pak vyberte **OK**.  

## <a name="publish-your-project"></a>Publikování projektu  
Po dokončení plánování projektu je dalším krokem import a publikování projektu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekt se importuje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Použijí se procesy tvorby cen a generování týmu. Otevřením projektu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ověřte, že byl vygenerován tým, odhad projektu a strukturovaný rozpis prací. Následující tabulka uvádí, kde lze nalézt výsledky.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ganttův diagram**   | Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Strukturovaný rozpis prací**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Tabulka zdrojů** |   Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Členové týmu projektu**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Pomocí využití**    |    Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Odhady projektů**.     |

**Chcete-li importovat a publikovat projekt**  
1. Na kartě **Project Service** přejděte na **Publikovat** > **Nový projekt nástroje Project Service Automation**.  

2. V dialogovém okně  **Publikovat do nového projektu v aplikaci Project Service** zadejte **Název projektu** a vyberte položku **Zákazník**.  

3. Volitelně můžete vybráním položky **Propojit projektový plán s řešením Project Service Automation** propojit soubor aplikace Project plánu s nástrojem Project Service Automation.  

4. Vyberte **Publikovat**.  

   Propojení souboru aplikace Project s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] učiní soubor aplikace Project hlavním souborem a nastaví strukturovaný rozpis prací v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] jen pro čtení.  Aby bylo možné provádět změny v plánu projektu, je nutné změny provést v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a publikovat je jako aktualizace do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Úpravy projektu, který byl importován  
 Chcete-li provést změny v plánu projektu, který byl importován do nástroje [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], máte dvě možnosti:  

- Otevření hlavního souboru a jeho úprava v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Zrušte propojení souboru a upravte jej přímo v aplikaci Project Service. Ve výchozím nastavení je projekt, který je odeslán z aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], uzamčen a lze jej upravovat pouze v aplikaci Project. Chcete-li upravit soubor v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], je třeba u souboru zrušit propojení.  

### <a name="edit-in-pn_microsoft_project"></a>Upravit v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. V hlavní nabídce přejděte na **Project Service** > **Projekty**.  

2. Ze seznamu projektů otevřete ten, který jste vytvořili v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Na pásu karet vyberte **Otevřít v MS Projectu**. Tím se propojený hlavní soubor otevře v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Zrušení propojení souboru a jeho úprava v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. V hlavní nabídce přejděte na **Project Service** > **Projekty**.  

2. Ze seznamu projektů otevřete ten, který jste vytvořili v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Na pásu karet vyberte **Odpojit od MS Projectu**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Odeslání souboru aplikace Project do služby SharePoint nebo do Skupin Office  
 Soubor aplikace Project můžete odeslat do služby SharePoint a najít jej v seznamu Přidružené dokumenty pro váš projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Váš správce vám musí nakonfigurovat správu dokumentů SharePoint a zapnout ji pro entitu aplikace Project. 

 Pokud máte nastaveny Skupiny Office, lze soubor aplikace Project uložit také do služby [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)].

### <a name="upload-a-file-for-sharepoint"></a>Nahrát soubor pro SharePoint  

1. V hlavní nabídce přejděte na **Project Service** > **Nahrát**.  

2. Vyberte položku **Do projektových dokumentů aplikace Project Service Automation**.  

3. V dialogovém okně **Povolit otevření v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** vyberte **Ano** nebo **Ne**.  

   - Po kliknutí na tlačítko **Ano** budete moci vybrat tlačítko **Otevřít v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v aplikaci Project Service Automation a spustit aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a načíst soubor aplikace Project z knihovny dokumentů systému SharePoint.  

   - Pokud vyberete **Ne**, odkaz na **Otevřít v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nebude fungovat.  

4. Soubor aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] naleznete v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v části **Dokumenty** pro konkrétní projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Odeslání souboru pro Skupiny Office  

1. V hlavní nabídce přejděte na **Project Service** > **Nahrát**.  

2. Vyberte položku **Do projektových dokumentů aplikace Project Service Automation**.  

3. V dialogovém okně **Povolit otevření v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** vyberte **Ano** nebo **Ne**.  

   - Po kliknutí na tlačítko **Ano** budete moci vybrat tlačítko **Otevřít v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v aplikaci Project Service Automation a spustit aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a načíst soubor aplikace Project z knihovny dokumentů systému SharePoint.  

   - Pokud vyberete **Ne**, odkaz na **Otevřít v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nebude fungovat.  

4. Soubor aplikace [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] naleznete v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v části **Dokumenty** pro konkrétní projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publikování projektu jako šablony  
 Projekt můžete uložit a znovu použít pomocí jeho uložení jako šablony projektu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Šablony projektu jsou znovu použitelné plány projektů v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Další informace naleznete v části [Vytvořit šablonu projektu (Project Service Automation)](../psa/create-project-template.md). 

1. Na kartě **Project Service** přejděte na **Publikovat** > **Nová šablona projektu nástroje Project Service Automation**.  

2. V dialogovém okně  **Publikovat do nové šablony projektu v aplikaci Project Service** zadejte **Název šablony projektu**.  

3. Volitelně můžete zaškrtnutím položky **Propojit projektový plán s řešením Project Service Automation** vybrat soubor aplikace Project plánu s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Vyberte **Publikovat**.  

Propojení souboru aplikace Project s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] učiní soubor aplikace Project hlavním souborem a nastaví strukturovaný rozpis prací v šabloně [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] jen pro čtení.  Aby bylo možné provádět změny v plánu projektu, je nutné změny provést v aplikaci [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a publikovat je jako aktualizace do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Přečtěte si plán načtených zfrojů

Při čtení projektu z Project Service Automation se kalendář prostředku nesynchronizuje s klientem plochy. Pokud existují rozdíly v dobách trvání, úsilí nebo konci úkolu, je to pravděpodobně proto, že prostředky a klient pro stolní počítače nemají pro projekt stejný kalendář šablon pracovní doby.


## <a name="data-synchronization"></a>Synchronizace dat
Tabulky v této části poskytují informace o synchronizaci dat entit mezi Project Service Automation a doplňkem Microsoft Project pro počítače.

### <a name="project-task-entity-table"></a>Tabulka entit úkolu projektu
Následující tabulka popisuje, jak se synchronizují data entity úkolu projektu mezi Project Service Automation a doplňkem Microsoft Project pro stolní počítače.

| **Entita** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Projektový úkol | Termín | Synchronizováno | Nesynchronizováno |
| Projektový úkol | Odhadované úsilí | Synchronizováno | Nesynchronizováno |
| Projektový úkol | ID klienta MS Project | Synchronizováno | Nesynchronizováno |
| Projektový úkol | Nadřazený úkol | Synchronizováno | Nesynchronizováno |
| Projektový úkol | Project | Synchronizováno | Nesynchronizováno |
| Projektový úkol | Projektový úkol | Synchronizováno | Nesynchronizováno |
| Projektový úkol | Název projektového úkolu | Synchronizováno | Nesynchronizováno |
| Projektový úkol | Jednotka zdroje (vyřazeno ve verzi 3.0) | Synchronizováno | Nesynchronizováno |
| Projektový úkol | Plánovaná doba trvání | Synchronizováno | Nesynchronizováno |
| Projektový úkol | Počáteční datum | Synchronizováno | Nesynchronizováno |
| Projektový úkol | ID strukturovaného rozpisu prací | Synchronizováno | Nesynchronizováno |

### <a name="team-member-entity-table"></a>Tabulka entit člena týmu
Následující tabulka popisuje, jak se synchronizují data entity člena týmu mezi Project Service Automation a doplňkem Micros

| **Entita** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Člen týmu | ID klienta MS Project | Synchronizováno | Nesynchronizováno |
| Člen týmu | Název pozice | Synchronizováno | Nesynchronizováno |
| Člen týmu | projekt | Synchronizováno | Synchronizováno |
| Člen týmu | Projektový tým | Synchronizováno | Synchronizováno |
| Člen týmu | Jednotka zdroje | Nesynchronizováno | Synchronizováno |
| Člen týmu | Role | Nesynchronizováno | Synchronizováno |
| Člen týmu | Pracovní doba | Nesynchronizováno | Nesynchronizováno |

### <a name="resource-assignment-entity-table"></a>Tabulka entit přiřazení zdrojů
Následující tabulka popisuje, jak se synchronizují data entity přiřazení zdrojů mezi Project Service Automation a doplňkem Micros

| **Entita** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Přiřazení zdroje | Od data | Synchronizováno | Nesynchronizováno |
| Přiřazení zdroje | hod | Synchronizováno | Nesynchronizováno |
| Přiřazení zdroje | ID klienta MS Project | Synchronizováno | Nesynchronizováno |
| Přiřazení zdroje | Naplánovaná práce | Synchronizováno | Nesynchronizováno |
| Přiřazení zdroje | Project | Synchronizováno | Nesynchronizováno |
| Přiřazení zdroje | Projektový tým | Synchronizováno | Nesynchronizováno |
| Přiřazení zdroje | Přiřazení zdroje | Synchronizováno | Nesynchronizováno |
| Přiřazení zdroje | Úkol | Synchronizováno | Nesynchronizováno |
| Přiřazení zdroje | K aktuálnímu datu | Synchronizováno | Nesynchronizováno |

### <a name="project-task-dependencies-entity-table"></a>Tabulka entit závislostí úkolu projektu
Následující tabulka popisuje, jak se synchronizují data entity závislostí úkolů projektu mezi Project Service Automation a doplňkem Micros

| **Entita** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Závislosti projektových úkolů | Závislost projektového úkolu | Synchronizováno | Nesynchronizováno |
| Závislosti projektových úkolů | Typ propojení | Synchronizováno | Nesynchronizováno |
| Závislosti projektových úkolů | Předchozí úkol | Synchronizováno | Nesynchronizováno |
| Závislosti projektových úkolů | Project | Synchronizováno | Nesynchronizováno |
| Závislosti projektových úkolů | Následný úkol | Synchronizováno | Nesynchronizováno |

### <a name="additional-resources"></a>Další materiály
 [Příručka pro projektového manažera](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
