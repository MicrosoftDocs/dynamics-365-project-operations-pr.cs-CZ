---
title: Synchronizace projektových smluv a projektů přímo z Project Service Automation do Finance
description: Toto téma popisuje šablonu a základní úkoly, které se používají k synchronizaci projektových smluv a projektů přímo z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 1a470fd86ceccd7b6058da6972399a6d6be2a991
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764811"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Synchronizace projektových smluv a projektů přímo z Project Service Automation do Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje šablonu a základní úkoly, které se používají k synchronizaci projektových smluv a projektů přímo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.

> [!NOTE] 
> Pokud používáte Enterprise Edition 7.3.0, musíte si nainstalovat aktualizaci KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datový tok pro Project Service Automation do Finance

> [!NOTE]
> Než budete moci použít řešení integrace Project Service Automation do Finance, měli byste být obeznámeni s funkcí integrace dat Dynamics 365.

Řešení integrace aplikací Project Service Automation do Finance využívá funkci integrace dat k synchronizaci dat napříč instancemi aplikací Project Service Automation a Finance. Šablona integrace, která je k dispozici s funkcí integrace dat, umožňuje tok dat o projektových smlouvách, projektech, řádcích projektových smluv a milníků řádků projektových smluv z Project Service Automation do Finance.

Následující obrázek ukazuje, jak jsou data synchronizována mezi Project Service Automation a Finance.

[![Datový tok pro integraci Project Service Automation s Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Pro přístup k dostupným šablonám v centru pro správu Microsoft Power Apps vyberte **Projekty** a poté v pravém horním rohu vyberte **Nový projekt**, aby se vybraly veřejné šablony.

Následující šablony a základní úlohy se používají k synchronizaci projektových smluv a projektů z Project Service Automation do Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrace s Dynamics 365 Project Service Automation v2.x
- **Název šablony v Integraci dat:** Projekty a smlouvy (Project Service Automation do Finance)
- **Název úloh v projektu:**

    - Projektové smlouvy Project Service Automation do Finance
    - Projekty Project Service Automation do Finance
    - Řádky projektové smlouvy Project Service Automation do Finance
    - Milníky řádku projektové smlouvy Project Service Automation do Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrace s Dynamics 365 Project Service Automation v3.x
V Project Service Automation dochází ke změně schématu, která má dopad na šablonu milníku řádků projektové smlouvy. Použití verze v2 šablony je nutné pro integraci Project Service Automation v3.x s Dynamics 365.

- **Název šablony v Integraci dat:** Projekty a smlouvy (Project Service Automation 3.x do Finance) – v2
- **Název úloh v projektu:**

    - Projektové smlouvy Project Service Automation do Finance
    - Projekty Project Service Automation do Finance
    - Řádky projektové smlouvy Project Service Automation do Finance
    - Milníky řádku projektové smlouvy Project Service Automation do Finance

Než může dojít k synchronizaci projektových smluv a projektů, musíte synchronizovat účty.

## <a name="entity-set"></a>Sada entit

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| Objednávky                           | Entita integrace pro projektovou smlouvu                |
| Projekty                         | Entita integrace pro projekt                         |
| Řádky objednávek                      | Entita integrace pro řádek projektové smlouvy           |
| Milníky řádku projektových smluv | Entita integrace pro milník řádku projektové smlouvy |

## <a name="entity-flow"></a>Tok entity

Projektové smlouvy jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány do Finance jako projektové smlouvy. Jako součást šablony integrace můžete nastavit zdroj integrace ve Finance pro projektovou smlouvu.

Časové a materiálové projekty a projekty s pevnou cenou jsou spravovány v Project Service Automation a synchronizovány s Finance jako projekty. Jako součást integrace šablony můžete nastavit zdroj integrace pro projekt v aplikaci Finance. V současné době jsou podporovány pouze časové a materiálové projekty a projekty s pevnou cenou.


Řádky projektové smlouvy jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány do Finance jako pravidla fakturace smlouvy. Pokud se metoda fakturace liší od výchozího typu projektu, synchronizace aktualizuje typ projektu pro řádek projektové smlouvy a skupinu projektů.

Milníky řádků projektové smlouvy jsou spravovány v aplikaci Project Service Automation a jsou synchronizovány do Finance jako milníky pravidla fakturace smlouvy.

## <a name="project-service-automation-to-finance-integration-solution"></a>Řešení integrace Project Service Automation do Finance

Pole **ID projektové smlouvy** je dostupné na stránce **Projektové smlouvy**. Toto pole se stalo přirozeným a jedinečným klíčem pro podporu integrace.

Když je vytvořena nová projektová smlouva a **ID projektové smlouvy** hodnota ještě neexistuje, je automaticky generován pomocí číselné řady. Hodnota se skládá z řetězce **ORD**, za kterým následuje automaticky se zvyšující číslo a přípona šesti znaků. Zde je příklad: **ORD-01022-Z4M9Q0**.

Pole **Číslo projektu** je dostupné na stránce **Projekty**. Toto pole se stalo přirozeným a jedinečným klíčem pro podporu integrace.

Když je vytvořen nový projekt a hodnota **Číslo projektu** ještě neexistuje, je automaticky generována pomocí číselné řady. Hodnota se skládá z řetězce **PRJ**, za kterým následuje automaticky se zvyšující číslo a přípona šesti znaků. Zde je příklad: **PRJ-01049-CCNID0**.

Když je použito řešení integrace Project Service Automation do Finance, nastaví skript upgradu pole **ID projektové smlouvy** pro stávající projektové smlouvy a pole **Číslo projektu** pro stávající projekty v Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Předpoklady a nastavení mapování

- Než může dojít k synchronizaci projektových smluv a projektů, musíte synchronizovat účty.
- V sadě připojení přidejte mapování pole integračního klíče pro **msdyn\_organizationalunits** na **msdyn\_name \[Název\]**. Možná budete muset nejprve přidat projekt do sady připojení. Další informace viz článek [Integrace dat do Common Data Service pro aplikace](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- V sadě připojení přidejte mapování pole integračního klíče pro **msdyn\_projects** na **msdynce\_projectnumber \[Číslo projektu\]**. Možná budete muset nejprve přidat projekt do sady připojení. Další informace viz článek [Integrace dat do Common Data Service pro aplikace](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Pole **SourceDataID** u projektových smluv a projektů lze aktualizovat na jinou hodnotu nebo odebrat z mapování. Výchozí hodnota šablony je **Project Service Automation**.
- Mapování **Platební podmínky** musí být aktualizováno tak, aby odráželo platné platební podmínky ve Finance. Můžete také odebrat mapování z projektové úlohy. Mapa výchozích hodnot má výchozí hodnoty pro ukázková data. V následující tabulce jsou uvedeny hodnoty v Project Service Automation.

    | Hodnota | Popis   |
    |-------|---------------|
    | 0     | Netto 30        |
    | 2     | 2 % 10, Netto 30 |
    | 3     | Netto 45        |
    | 4     | Netto 60        |

## <a name="power-query"></a>Power Query

K filtrování dat použijte Microsoft Power Query pro Excel, pokud jsou splněny následující podmínky:

- Máte prodejní objednávky v Dynamics 365 Sales.
- Máte více organizačních jednotek v Project Service Automation a tyto organizační jednotky budou mapovány na více právnických osob ve Finance.

Pokud musíte použít Power Query, postupujte podle těchto pokynů:

- Šablona Projekty a smlouvy (PSA do Fin a Ops) má výchozí filtr, který zahrnuje pouze prodejní objednávky typu **Pracovní položka (msdyn\_ordertype = 192350001)**. Tento filtr pomáhá zaručit, že projektové smlouvy nejsou vytvořeny pro prodejní objednávky ve Finance. Pokud vytvoříte vlastní šablonu, musíte přidat tento filtr.
- Vytvořte filtr Power Query, který zahrnuje pouze smluvní organizace, které by se měly synchronizovat s právní entitou sady integračních připojení. Například projektové smlouvy uzavřené se smluvní organizační jednotkou společnosti Contoso USA by měly být synchronizovány s právním subjektem USSI, ale projektové smlouvy se smluvní organizační jednotkou společnosti Contoso Global by měly být synchronizovány s právním subjektem USMF. Pokud tento filtr nepřidáte do svého mapování úkolů, budou všechny projektové smlouvy synchronizovány s právním subjektem, který je definován pro sadu připojení, bez ohledu na smluvní organizační jednotku.

## <a name="template-mapping-in-data-integration"></a>Mapování šablon v integraci dat

> [!NOTE] 
> Pole **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** a **AdresssZipCode** nejsou zahrnuta do výchozího mapování pro projektové smlouvy. Můžete přidat mapování, pokud požadujete synchronizaci těchto dat u projektových smluv.
>
> Pole **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** a **ProjectType** nejsou zahrnuta do výchozího mapování pro projekty. Můžete přidat mapování, pokud požadujete synchronizaci těchto dat u projektů.

Následující obrázky ukazují příklady mapování úlohy šablony v Integraci dat. Mapování zobrazuje informace pole, které budou synchronizovány z Project Service Automation do Finance.

[![Mapování šablony projektové smlouvy](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mapování šablony projektu](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mapování šablony řádků projektové smlouvy](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mapování šablony milníku řádku projektové smlouvy](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Mapování milníku řádků projektových smluv v projektech a smlouvách (PSA 3.x do Dynamics) - šablona v2:

[![Mapování šablony milníku řádku projektové smlouvy se šablonou druhé verze](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]