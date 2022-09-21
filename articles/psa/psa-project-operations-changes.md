---
title: Změny funkcí mezi Project Service Automation a Project Operations
description: Tento článek poskytuje přehled změn funkcí mezi Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459918"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Změny funkcí mezi Project Service Automation a Project Operations

Upgrade z Dynamics 365 Project Service Automation na omezenou verzi Dynamics 365 Project Operations bude dodáván ve třech fázích. Tento článek poskytuje informace o hlavních změnách, které můžete očekávat po dokončení upgradu.

| Doručení upgradu | Fáze 1 <br>(leden 2022) | Fáze 2 <br>(listopad 2022) | Fáze 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Žádná závislost na strukturovaném rozpisu prací (WBS) u projektů. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Strukturovaný rozpis prací je součástí aktuálně podporovaných limitů Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| Strukturovaný rozpis prací mimo aktuálně podporované limity Project Operations, včetně podpory pro aplikaci Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Správa projektů

Nejvýraznější změny v uživatelském prostředí budou v oblasti plánování projektů. Project Operations je vybaven novým moderním prostředím pro správu strukturovaného rozpisu prací (WBS) využitím možností plánování, které poskytuje [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Rozdíly v prostředí plánování

Následující tabulka shrnuje rozdíly v plánování mezi Project Service Automation a Project Operations.

|  Plánování     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Šablony projektů – Schopnost definovat a aplikovat šablony projektů při vytváření projektu  |  &nbsp;    | :heavy_check_mark: |
| Integrace projektového strukturovaného rozpisu prací (WBS) s klientem pro stolní počítače   |    &nbsp;  | :heavy_check_mark: |
| Omezení – Začít ne dříve než, skončit nejpozději  | :heavy_check_mark: |   &nbsp;  |
| Milníky – Úkoly s nulovým trváním   | :heavy_check_mark:  |  &nbsp;  |
| Úkoly řízené zdroji budou respektovat dostupnost přidělených zdrojů   | :heavy_check_mark: |  &nbsp;    |
| Časově uspořádané úpravy – Upravujte plány a pracujte každý den   |   &nbsp;  | :heavy_check_mark: |
| Automatické/ruční plánování – Pomocí modulu plánování projektu můžete automaticky nebo ručně plánovat úlohy |  &nbsp; | :heavy_check_mark:  |
| Úpravy rozsáhlých projektů přímo v uživatelském rozhraní: Velikost plánů, které lze upravovat, není omezena  | Limit 500 úkolů  | :heavy_check_mark:       |
| Procento dokončení – Označte průběh úkolu   | :heavy_check_mark:  |  &nbsp;  |
| [Režimy plánování projektu](../project-management/scheduling-modes.md) - Definujte projekt jako pevné jednotky, pevné úsilí nebo pevnou dobu trvání | :heavy_check_mark: | &nbsp; |
| Časová osa – Sestavte a přizpůsobte zobrazení časové osy pro vizualizaci podrobností plánu a komunikaci se zúčastněnými stranami. | :heavy_check_mark:  | &nbsp; |
| Úkoly řízené úsilím – Podpora plánovacího nástroje pro plánování úkolu na základě úsilí  | :heavy_check_mark:  | &nbsp; |
| Dialogové okno **Informace o úkolu** – Uložte podrobnosti úlohy pomocí dialogového okna | :heavy_check_mark:  |  &nbsp;  |
| Přetažení myší – Vyberte více úloh najednou a upravte jejich pozici na rozpisu WBS | :heavy_check_mark: | &nbsp;  |
| Flexibilní trvalé pohledy – Definujte podrobnější pohledy na atributy úkolů   | :heavy_check_mark:  | &nbsp; |
| Řazení a filtrování rozpisu WBS  | :heavy_check_mark:  | &nbsp; |
| Zobrazení vývěsek pro nekaskádové dodání projektu  | :heavy_check_mark:   | &nbsp; |
| Zobrazení časové osy – Interaktivní Ganttův diagram používaný k vizualizaci a úpravě rozpisu WBS   | :heavy_check_mark:  | &nbsp; |
| Klávesové zkratky – Klávesové zkratky používejte pro běžné operace, jako je odsazení nebo vložení  | :heavy_check_mark:  |  &nbsp; |
| Víceúrovňové vrácení zpět – Proveďte analýzu typu „co kdyby“, abyste plně porozuměli dopadu změn tím, že zrušíte a znovu použijete celou sadu operací | :heavy_check_mark: | &nbsp; |
| Vyjmout/Kopírovat/Vložit – Spolupracujte na vývoji plánu kopírováním a vkládáním podrobností plánu mezi aplikacemi  | :heavy_check_mark: | &nbsp; |
| Kontrolní seznamy úkolů – Přidejte k úkolu až 20 položek kontrolního seznamu   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Plánování projektu

Stránka **Projekt** v Project Operations se od stránky **Projekt** v Project Service Automation v mnoha ohledech liší.

Následující akce byly ze stránky **Projekty** odstraněny v rámci aktualizace fáze 1:

  - **Otevřít v MS Projectu**
  - **Vytvořit šablonu**
  - **Odpojit od MS Projectu**

Stránka **Projekt** v Project Operations obsahuje následující nové karty.

- **Odhady materiálu**
- **Nastavení účtování úkolů**

Karta **Stav** byla odebrána a pole **Stav** pole je nyní na kartě **Souhrn** s režimem plánování projektu.

   ![Aktualizace stránky Projekt.](media/projectform.png)

Karta **Plán** byla přejmenována na **Úkol** a nabízí nové možnosti plánování projektů v aplikaci Project for the Web.

   ![Nová karta Projektové úkoly.](media/tasktab.png)

## <a name="scheduling-modes"></a>Režimy plánování

Project Operations zavádí novou funkci [Režimy plánování](../project-management/scheduling-modes.md). Všechny existující projekty Project Service Automation budou mít v Project Operations implicitně nastavenu **Pevnou dobu trvání**. Výchozí nastavení pro nové projekty však lze spravovat v nabídce **Nastavení** > **Parametry** > **Parametr** > **Režim plánu**.

   ![Nastavení parametrů projektu pro režim Plán.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Omezení plánování projektu

Project Operations provádí všechny operace plánování projektu prostřednictvím aplikace Project for the Web. Project for the Web spravuje strukturovaný rozpis prací pomocí limitů v následující tabulce.

| **Pole**                                          | **Omezení**             |
|----------------------------------------------------|-----------------------|
| Maximální celkový počet úkolů v projektu                  | 500                   |
| Maximální celková doba trvání projektu               | 3650 dní (10 let)  |
| Maximální celkový počet zdrojů v projektu              | 300                   |
| Maximální celkový počet odkazů (pouze následovník) v projektu | 600                   |
| Maximální celkový počet vlastních polí v projektu          | 10                    |
| Maximální úroveň hierarchie                            | 10 úrovní             |
| Maximální počet odkazů (následovník + předchůdce)            | 20                    |
| Maximální doba trvání koncového úkolu                      | 1250 dní             |
| Maximální doba trvání souhrnného úkolu                 | 3650 dní (10 let)  |
| Maximální počet zdrojů přiřazených k úkolu               | 20 zdrojů          |
| Podporované časové období pro úkol                    | 1. 1. 2000 - 31. 12. 2149 |
| Položky kontrolního seznamu                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Rozšiřitelnost a rozvoj projektového plánování

Po upgradu na Project Operations musíte u následujících entit použít k provádění operací vytváření, aktualizace a odstraňování rozhraní Project Scheduling API:

|   Název entity           |   Logický název entity       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektový úkol            | msdyn_projecttask           |
| Závislost projektového úkolu | msdyn_projecttaskdependency |
| Přiřazení zdroje     | msdyn_resourceassignment    |
| Kbelík projektu          | msdyn_projectbucket         |
| Člen projektového týmu     | msdyn_projectteam           |

Pokud aktuálně máte přizpůsobení, která zahrnují tyto entity, přečtěte si návod k implementaci v článku [Používání rozhraní API Plánu projektu k provádění operací s entitami plánování](../project-management/schedule-api-preview.md).

## <a name="data-model-changes"></a>Změny datového modelu

V rámci fáze 1 upgradu dochází ke změnám datového modelu. Tyto změny jsou primárně změnami polí stávajících entit. Ve fázi 1 dochází k předělání entit **msydn_project** a **msdyn_projectteam**. 

> [!IMPORTANT]
> Po dokončení budoucích fází upgradu bude tato část aktualizována o další entity.

Následující pole byla nahrazena novými poli.

|   Entity          |   Starý logický název   |   Nový logický název    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Následující pole byla přidána.

|   Entity          |   Logický název                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Zobrazuje celkovou hodnotu skutečného prodeje poplatků na projektu. K použití pouze v Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Zobrazuje úhrn skutečných materiálových nákladů na projektu. K použití pouze v Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Zobrazuje celkovou hodnotu skutečného prodeje materiálu na projektu. K použití pouze v Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Řádek smlouvy přidružený k tomuto projektu. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Toto je interní systémové pole, které se používá pro **kopírování projektu** související s identifikátorem korelace. K použití pouze v Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Toto je interní systémové pole, které se používá pro **kopírování projektu** související s identifikátorem relace. K použití pouze v Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Token globální revize xRM z poslední synchronizace ze služby plánování projektu. |
| msdyn_project     | msdyn_msprojectdocument                      | Dokument Microsoft Project náležící k projektu. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Úhrn plánovaných materiálových nákladů na projektu. K použití pouze v Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Úhrn plánovaných materiálových prodejů na projektu. K použití pouze v Project Service Automation. |
| msdyn_project     | msdyn_program                                | Program, se kterým tento projekt souvisí. |
| msdyn_project     | msdyn_quotelineproject                       | Řádek nabídky přidružený k tomuto projektu. |
| msdyn_project     | msdyn_replaylogheader                        | Záhlaví protokolů opětovného přehrání. |
| msdyn_project     | msdyn_schedulemode                           | Výchozí režim plánování používaný pro všechny úkoly na projektu.  |
| msdyn_project     | msdyn_taskearlieststart                      | Nejčasnější počáteční datum libovolného úkolu projektu.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Člen projektového týmu, ze kterého byl tento člen projektového týmu zkopírován. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Uvádí, zda vytvořit požadavek na zdroje pro nově vytvořeného obecného člena týmu.  |
| msdyn_projectteam | msdyn_deletestatus                           | Stav odstranění člena týmu pro sledování, zda je do služby plánování projektu odeslán požadavek na odstranění a zda služba úspěšně odešle zpět odpověď v očekávaném časovém intervalu. |
| msdyn_projectteam | msdyn_effortcompleted                        | Sleduje úsilí člena týmu, které vynaložil na svá přiřazení. |
| msdyn_projectteam | msdyn_effortremaining                        | Sleduje nedokončené úsilí člena týmu na svá přiřazení. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Doba čekání od okamžiku, kdy člen týmu odešle požadavek na odstranění do služby plánování projektu, až do skutečného odstranění člena týmu v Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Časové razítko k zaznamenání, kdy je žádost o odstranění člena týmu odeslána do služby plánování projektu. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Ukazuje člena projektového týmu, ze kterého byl tento člen projektového týmu zkopírován.  |

## <a name="project-templates"></a>Šablony projektů

Project Operations neposkytuje podporu pro projektové šablony. Většinu základních funkcí však můžete replikovat pomocí rozhraní [Project Copy API](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Podpora doplňků pro stolní počítače

Podpora pro doplněk Microsoft Project Desktop nebude k dispozici v prvních 2 fázích upgradu. Ve fázi 3 budou moci zákazníci, kteří mají projekty větší než aktuálně podporované limity Project for the Web, používat doplněk pro stolní počítače.

## <a name="editing-resource-assignment-contours"></a>Úprava křivek přiřazení zdrojů

Možnost upravovat křivky přiřazení zdrojů bude k dispozici, až bude k dispozici fáze 2 upgradu.

## <a name="billing-and-pricing"></a>Fakturace a ceny

Do Project Operations byly přidány následující nové funkce. Tyto funkce jsou aditivní povahy a nemají vliv na datový model Project Service Automation.

- [Záznam využití materiálu na projektech a projektových úkolech](../material/material-usage-log.md)
- [Řízení subdodávek](../pro/subcontracting/managing-subcontracts-overview.md)
- [Zálohy a smlouvy na základě záloh](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Nepřekročitelné stavy smlouvy a ověření](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Fakturace na základě úkolů](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Zastaralé komponenty

Následující tabulky dokumentují všechna zastaralá pole, která se po upgradu přesunou do řešení zastaralých komponent. Další informace a odkaz na řešení viz [Komponenty zastaralé při upgradu z Dynamics 365 Project Service Automation 3x na Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Pole                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

