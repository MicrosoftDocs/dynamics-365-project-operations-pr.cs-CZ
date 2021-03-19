---
title: Přidat nové vlastní formuláře entit (Project Service Automation 2.x)
description: Toto téma obsahuje informace o způsobu přidávání vlastních formulářů entit pro příležitosti, nabídky, objednávky nebo faktury v Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c9e31dc6d4d5a8ad5cc568f2d7d673c8703936d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284845"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="f12bc-103">Přidat nové vlastní formuláře entit (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="f12bc-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="f12bc-104">Typ pole</span><span class="sxs-lookup"><span data-stu-id="f12bc-104">Type field</span></span> 

<span data-ttu-id="f12bc-105">Dynamics 365 Project Service Automation spoléhá na pole **Typ** (**msdyn\_ordertype**) entit Příležitost, Nabídka, Objednávka a Faktura, aby rozlišil verze těchto entit **založené na práci** od verzí **založených na položce** a **založených na službě**.</span><span class="sxs-lookup"><span data-stu-id="f12bc-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="f12bc-106">Verze těchto entit založené na práci jsou zpracovávány pomocí PSA.</span><span class="sxs-lookup"><span data-stu-id="f12bc-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="f12bc-107">Mnoho obchodní logiky na straně klienta a na straně serveru daného řešení závisí na poli **Typ**.</span><span class="sxs-lookup"><span data-stu-id="f12bc-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="f12bc-108">Proto je důležité, aby při vytváření entit bylo toto pole inicializováno se správnou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="f12bc-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="f12bc-109">Nesprávná hodnota může způsobit nesprávné chování a některá obchodní logika nemusí fungovat správně.</span><span class="sxs-lookup"><span data-stu-id="f12bc-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="f12bc-110">Automatické přepínání formulářů</span><span class="sxs-lookup"><span data-stu-id="f12bc-110">Automatic form switching</span></span>

<span data-ttu-id="f12bc-111">Chcete-li předejít možnému poškození dat a nečekanému chování způsobenému nesprávnou inicializací a úpravou záznamů entit prodeje, bude funkce PSA nyní obsahovat logiku pro automatické přepínání formulářů v připravených formulářích.</span><span class="sxs-lookup"><span data-stu-id="f12bc-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="f12bc-112">Tato logika vrátí uživatele do správného formuláře pro práci s verzí založenou na práci nebo s jakýmkoli jiným typem entity Příležitost, Nabídka, Objednávka nebo Faktura.</span><span class="sxs-lookup"><span data-stu-id="f12bc-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="f12bc-113">Když uživatel otevře verzi entity Příležitost, Nabídka, Objednávka nebo Faktura založené na práci, bude formulář přepnut do **Informací o projektu**.</span><span class="sxs-lookup"><span data-stu-id="f12bc-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="f12bc-114">Logika automatického přepínání formulářů se opírá o mapování mezi hodnotou **formId** a polem **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="f12bc-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="f12bc-115">K tomuto mapování byly přidány všechny připravené formuláře.</span><span class="sxs-lookup"><span data-stu-id="f12bc-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="f12bc-116">Vlastní formuláře však musí být přidány ručně, aby bylo možné určit, kterou verzi entity mají zpracovávat.</span><span class="sxs-lookup"><span data-stu-id="f12bc-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="f12bc-117">To vychází z pole **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="f12bc-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="f12bc-118">Pokud v mapování chybí přepínání formuláře, přepne logika do připraveného formuláře na základě hodnoty uložené v poli **msdyn\_ordertype** entity.</span><span class="sxs-lookup"><span data-stu-id="f12bc-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="f12bc-119">Přidání vlastních formulářů a zapnutí logiky přepínání formulářů</span><span class="sxs-lookup"><span data-stu-id="f12bc-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="f12bc-120">Následující příklad ukazuje, jak přidat vlastní formulář **Mé informace o projektu**, aby fungoval s příležitostmi založenými na práci.</span><span class="sxs-lookup"><span data-stu-id="f12bc-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="f12bc-121">Stejný proces se používá k přidání vlastních formulářů tak, aby fungovaly s nabídkami, objednávkami a fakturami.</span><span class="sxs-lookup"><span data-stu-id="f12bc-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="f12bc-122">Chcete-li vytvořit vlastní verzi formuláře **Informace o projektu**, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="f12bc-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="f12bc-123">V entitě Příležitost otevřete formulář **Informace o projektu** a uložte kopii s názvem **Mé informace o projektu**.</span><span class="sxs-lookup"><span data-stu-id="f12bc-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="f12bc-124">Otevřete nový formulář a potom ve vlastnostech zkontrolujte, zda jsou k dispozici inicializační skripty z formuláře **Informace o projektu**.</span><span class="sxs-lookup"><span data-stu-id="f12bc-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="f12bc-125">Neodstraňujte skripty.</span><span class="sxs-lookup"><span data-stu-id="f12bc-125">Don't remove the scripts.</span></span> <span data-ttu-id="f12bc-126">V opačném případě může dojít k nesprávné inicializaci některých dat.</span><span class="sxs-lookup"><span data-stu-id="f12bc-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="f12bc-127">Ověřte, zda je pole **Typ** (**msdyn\_ordertype**) ve formuláři k dispozici.</span><span class="sxs-lookup"><span data-stu-id="f12bc-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="f12bc-128">Toto pole neodstraňujte.</span><span class="sxs-lookup"><span data-stu-id="f12bc-128">Don't remove this field.</span></span> <span data-ttu-id="f12bc-129">V opačném případě dojde k selhání inicializačních skriptů.</span><span class="sxs-lookup"><span data-stu-id="f12bc-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="f12bc-130">Najděte hodnotu **formId** nového formuláře.</span><span class="sxs-lookup"><span data-stu-id="f12bc-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="f12bc-131">Tento krok můžete provést dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="f12bc-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="f12bc-132">Exportujte formulář **Mé informace o projektu** jako součást nespravovaného řešení a potom vyhledejte v souboru customization.xml exportovaného řešení hodnotu **formId**.</span><span class="sxs-lookup"><span data-stu-id="f12bc-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="f12bc-133">Otevřete formulář **Mé informace o projektu** v editoru formulářů a potom vyhledejte globálně jedinečný identifikátor (GUID) vedle parametru **fromId** v adrese URL, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="f12bc-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Hodnota formId nového formuláře v adrese URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="f12bc-135">Vytvořte mapování **msdyn\_ordertype** pro hodnotu **formId** pomocí úprav webového prostředku msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="f12bc-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="f12bc-136">Odeberte kód ze zdroje a nahraďte jej následujícím kódem.</span><span class="sxs-lookup"><span data-stu-id="f12bc-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="f12bc-137">Uložte a poté publikujte vlastní nastavení.</span><span class="sxs-lookup"><span data-stu-id="f12bc-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]