---
title: Vývoj šablon projektů pomocí kopírování projektu
description: Tento článek poskytuje informace o tom, jak vytvořit šablony projektu pomocí vlastní akce Kopírovat projekt.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923824"
---
# <a name="develop-project-templates-with-copy-project"></a>Vývoj šablon projektů pomocí kopírování projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations podporuje schopnost kopírovat projekt a vrátit jakékoli přiřazení zpět k obecným prostředkům, které představují roli. Zákazníci mohou pomocí této funkce vytvářet základní šablony projektů.

Když vyberete **Kopírovat projekt**, je aktualizován stav cílového projektu. Použijte **Důvod stavu** k určení, kdy je akce kopírování dokončena. Výběr možnosti **Kopírovat projekt** také aktualizuje počáteční datum projektu na aktuální počáteční datum, pokud v entitě cílového projektu není zjištěno žádné cílové datum.

## <a name="copy-project-custom-action"></a>Vlastní akce Kopírovat projekt

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Vstupní parametry

Jsou tři vstupní parametry:

- **ReplaceNamedResources** nebo **ClearTeamsAndAssignments** – Nastavte pouze jednu z možností. Nenastavujte obojí.

    - **\{"ReplaceNamedResources":true\}** – Výchozí chování pro Project Operations. Jakýkoli pojmenovaný zdroj je nahrazen obecnými zdroji.
    - **\{"ClearTeamsAndAssignments":true\}** – Výchozí chování pro Project for the Web. Všechny úkoly a členové týmu jsou odebráni.

- **SourceProject** – Reference entity zdrojového projektu, ze kterého se má kopírovat. Tento parametr nemůže mít hodnotu null.
- **Target** – Reference entity cílového projektu, do kterého se má kopírovat. Tento parametr nemůže mít hodnotu null.

Následující tabulka obsahuje souhrn třech parametrů.

| Parametr                | Type             | Hodnota                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Logický          | **Pravda** nebo **Nepravda** |
| ClearTeamsAndAssignments | Logický          | **Pravda** nebo **Nepravda** |
| SourceProject            | Odkaz na entitu | Zdrojový projekt    |
| Cíl                   | Odkaz na entitu | Cílový projekt    |

Další informace o výchozích hodnotách akcí naleznete v článku [Použití akcí webového rozhraní API](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

### <a name="validations"></a>Ověření

Provedena jsou následující ověření.

1. Kontrola hodnot null a načtení zdrojových a cílových projektů, aby se potvrdila existence obou projektů v organizaci.
2. Systém ověří platnost cílového projektu pro kopírování ověřením následujících podmínek:

    - Na projektu neprobíhá žádná předchozí aktivita (včetně výběru karty **Úkoly**) a projekt je nově vytvořen.
    - Neexistuje žádná předchozí kopie, v tomto projektu nebyl požadován žádný import a projekt není ve stavu **Selhání**.

3. Operace není volána pomocí protokolu HTTP.

## <a name="specify-fields-to-copy"></a>Zadejte pole ke kopírování

Po zavolání se akce **Kopírovat projekt** podívá na pohled projektu **Kopírovat sloupce projektu** k určení, která pole se mají kopírovat při kopírování projektu.

### <a name="example"></a>Příklad

Následující příklad ukazuje, jak zavolat vlastní akci **CopyProjectV3** se sadou parametrů **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
