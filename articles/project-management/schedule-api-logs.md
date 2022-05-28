---
title: Protokoly plánování projektu
description: Toto téma poskytuje informace a ukázky, které vám pomohou používat protokoly plánování projektu ke sledování selhání souvisejících se službou Plánování projektu a rozhraními API plánování projektu.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589510"
---
# <a name="project-scheduling-logs"></a>Protokoly plánování projektu

_**Platí pro**: Project Operations pro scénáře založené na zdrojích / neskladových položkách, nasazení Lite – řeší proforma fakturaci_, _Project for the Web_

Microsoft Dynamics 365 Project Operations používá [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) jako svůj primární plánovací modul. Namísto použití standardního webového aplikačního programovacího rozhraní Microsoft Dataverse (API) Project Operations používá nová rozhraní API Plánování projektu k vytváření, aktualizaci a odstraňování projektových úkolů, přiřazení zdrojů, závislostí úkolů, skupin projektů a členů projektových týmů. Když jsou však operace vytvoření, aktualizace nebo odstranění programově spuštěny na entitách strukturovaného rozpisu prací (WBS), může dojít k chybám. Pro sledování těchto chyb a vytvoření historie operací byly implementovány dva nové administrativní protokoly: **Sada operací** a **Služba plánování projektů (PSS)**. Pro přístup k těmto protokolům přejděte na **Nastavení** \> **Plán integrace**.

Následující ilustrace znázorňuje datový model protokolů plánování projektu.

![Datový model protokolů plánování projektu.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Protokol sady operací

Protokol sady operací sleduje provádění sady operací, která se používá ke spuštění jedné nebo mnoha operací vytvoření, aktualizace nebo odstranění v dávce u projektů, projektových úkolů, přiřazení zdrojů, závislostí úkolů, skupin projektů nebo členů projektového týmu. Pole **Operace ve stavu** zobrazuje celkový stav sady operací. Podrobnosti o datové části sady operací jsou zachyceny v souvisejících záznamech podrobností sady operací.

### <a name="operation-set"></a>Sada operací

Následující tabulka obsahuje pole, která souvisejí s entitou **Sada operací**.

| Název schématu            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datum a čas, kdy byla sada operací dokončena nebo selhala.                                                | CompletedOn            |
| msdyn_correlationid   | Hodnota **correlationId** požadavku.                                                                  | CorrelationId          |
| msdyn_description     | Popis sady operací.                                                                        | Description            |
| msdyn_executedon      | Datum a čas, kdy byl záznam spuštěn.                                                                       | Provedeno dne            |
| msdyn_operationsetId  | Jedinečný identifikátor instancí entity.                                                                   | OperationSet           |
| msdyn_Project         | Projekt související se sadou operací.                                                            | Project                |
| msdyn_projectid       | Hodnota **projectId** požadavku.                                                                      | ProjectId (zastaralé) |
| msdyn_projectName     | Nevztahuje se.                                                                                              | Nelze použít         |
| msdyn_PSSErrorLog     | Jedinečný identifikátor protokolu chyb služby Plánování projektu, který je přidružen k sadě operací. | Protokol chyb PSS          |
| msdyn_PSSErrorLogName | Nevztahuje se.                                                                                              | Nelze použít         |
| msdyn_status          | Stav sady operací.                                                                             | Status                 |
| msdyn_statusName      | Nevztahuje se.                                                                                              | Nelze použít         |
| msdyn_useraadid       | ID objektu Azure Active Directory (Azure AD) uživatele, kterému tento požadavek patří.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detail operační sady

Následující tabulka obsahuje pole, která souvisejí s entitou **Detail sady operací**.

| Název schématu                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serializovaná pole Dataverse pro požadavek.                                            | CdsPayload            |
| msdyn_entityname           | Název entity pro požadavek.                                                     | EntityName            |
| msdyn_httpverb             | Metoda požadavku.                                                                         | HTTPVerb (zastaralé) |
| msdyn_httpverbName         | Nevztahuje se.                                                                             | Nelze použít        |
| msdyn_operationset         | Jedinečný identifikátor sady operací, do které tento záznam patří.                      | OperationSet          |
| msdyn_operationsetdetailId | Jedinečný identifikátor instancí entity.                                                  | Podrobnosti OperationSet   |
| msdyn_operationsetName     | Nevztahuje se.                                                                             | Nelze použít        |
| msdyn_operationtype        | Typ operace detailu sady operací.                                             | OperationType         |
| msdyn_operationtypeName    | Nevztahuje se.                                                                             | Nelze použít        |
| msdyn_psspayload           | Serializovaná pole služby Plánování projektu pro požadavek.                           | PssPayload            |
| msdyn_recordid             | Identifikátor záznamu požadavku.                                                       | ID záznamu             |
| msdyn_requestnumber        | Automaticky generované číslo sloužící k identifikaci pořadí, ve kterém byly požadavky přijaty. | Číslo požadavku        |

## <a name="project-scheduling-service-error-logs"></a>Protokoly chyb služby Plánování projektu

Protokoly chyb služby Plánování projektu zachycují selhání, ke kterým dojde, když se služba pokusí o operaci **Uložit** nebo **Otevřít**. Existují tři podporované scénáře, kde jsou tyto protokoly generovány:

- Akce iniciované uživatelem kriticky selžou (například nelze vytvořit přiřazení kvůli chybějícím oprávněním).
- Služba Plánování projektu nemůže programově vytvářet, aktualizovat, odstraňovat ani provádět žádné jiné kaskádové operace na entitě.
- Uživatel zaznamená chyby, když se záznam neotevře (například při otevření projektu nebo aktualizaci informací o členu týmu).

### <a name="project-scheduling-service-log"></a>Protokol služby Plánování projektu

Následující tabulka obsahuje pole, která jsou součástí protokolu služby Plánování projektu.

| Název schématu          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Zásobník volání výjimky.                                               | Zásobník volání     |
| msdyn_correlationid | ID korelace chyby.                                               | CorrelationId  |
| msdyn_errorcode     | Pole, které se používá k uložení chybového kódu Dataverse nebo chybového kódu HTTP. | Kód chyby     |
| msdyn_HelpLink      | Odkaz na veřejnou dokumentaci nápovědy.                                       | Odkaz na nápovědu      |
| msdyn_log           | Protokol ze služby Plánování projektu.                                   | Protokol            |
| msdyn_project       | Projekt přidružený k protokolu chyb.                             | Project        |
| msdyn_projectName   | Název projektu, pokud bude zachována datová část sady operací. | Nelze použít |
| msdyn_psserrorlogId | Jedinečný identifikátor instancí entity.                                     | Protokol chyb PSS  |
| msdyn_SessionId     | ID relace projektu.                                                        | ID relace     |

## <a name="error-log-cleanup"></a>Vyčištění protokolu chyb

Ve výchozím nastavení lze protokoly chyb služby Plánování projektu i protokol sady operací vyčistit každých 90 dní. Všechny záznamy starší než 90 dnů se odstraní. Změnou pole **msdyn_StateOperationSetAge** na stránce **Parametry projektu** však správci mohou upravit frekvenci čištění tak, aby byla mezi 1 a 120 dny. Pro změnu této hodnoty je k dispozici několik metod:

- Přizpůsobte si entitu **Parametr projektu** vytvořením vlastní stránky a přidáním pole **Stáří zastaralé sady operací**.
- Použijte klientský kód, který využívá [Sadu pro vývoj softwaru WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Použijte kód Service SDK, který využívá metodu Xrm SDK **updateRecord** (referenční kleintské API) v modelem řízených aplikacích. Power Apps obsahuje popis a podporované parametry metody **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
