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
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Přidat nové vlastní formuláře entit (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Typ pole 

Dynamics 365 Project Service Automation spoléhá na pole **Typ** (**msdyn\_ordertype**) entit Příležitost, Nabídka, Objednávka a Faktura, aby rozlišil verze těchto entit **založené na práci** od verzí **založených na položce** a **založených na službě**. Verze těchto entit založené na práci jsou zpracovávány pomocí PSA. Mnoho obchodní logiky na straně klienta a na straně serveru daného řešení závisí na poli **Typ**. Proto je důležité, aby při vytváření entit bylo toto pole inicializováno se správnou hodnotou. Nesprávná hodnota může způsobit nesprávné chování a některá obchodní logika nemusí fungovat správně.

## <a name="automatic-form-switching"></a>Automatické přepínání formulářů

Chcete-li předejít možnému poškození dat a nečekanému chování způsobenému nesprávnou inicializací a úpravou záznamů entit prodeje, bude funkce PSA nyní obsahovat logiku pro automatické přepínání formulářů v připravených formulářích. Tato logika vrátí uživatele do správného formuláře pro práci s verzí založenou na práci nebo s jakýmkoli jiným typem entity Příležitost, Nabídka, Objednávka nebo Faktura. Když uživatel otevře verzi entity Příležitost, Nabídka, Objednávka nebo Faktura založené na práci, bude formulář přepnut do **Informací o projektu**.

Logika automatického přepínání formulářů se opírá o mapování mezi hodnotou **formId** a polem **msdyn\_ordertype**. K tomuto mapování byly přidány všechny připravené formuláře. Vlastní formuláře však musí být přidány ručně, aby bylo možné určit, kterou verzi entity mají zpracovávat. To vychází z pole **msdyn\_ordertype**. Pokud v mapování chybí přepínání formuláře, přepne logika do připraveného formuláře na základě hodnoty uložené v poli **msdyn\_ordertype** entity.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Přidání vlastních formulářů a zapnutí logiky přepínání formulářů

Následující příklad ukazuje, jak přidat vlastní formulář **Mé informace o projektu**, aby fungoval s příležitostmi založenými na práci. Stejný proces se používá k přidání vlastních formulářů tak, aby fungovaly s nabídkami, objednávkami a fakturami.

Chcete-li vytvořit vlastní verzi formuláře **Informace o projektu**, postupujte následovně.

1. V entitě Příležitost otevřete formulář **Informace o projektu** a uložte kopii s názvem **Mé informace o projektu**.
2. Otevřete nový formulář a potom ve vlastnostech zkontrolujte, zda jsou k dispozici inicializační skripty z formuláře **Informace o projektu**. 

    > [!IMPORTANT]
    > Neodstraňujte skripty. V opačném případě může dojít k nesprávné inicializaci některých dat.

3. Ověřte, zda je pole **Typ** (**msdyn\_ordertype**) ve formuláři k dispozici. 

    > [!IMPORTANT]
    > Toto pole neodstraňujte. V opačném případě dojde k selhání inicializačních skriptů.

4. Najděte hodnotu **formId** nového formuláře. Tento krok můžete provést dvěma způsoby:

    - Exportujte formulář **Mé informace o projektu** jako součást nespravovaného řešení a potom vyhledejte v souboru customization.xml exportovaného řešení hodnotu **formId**.
    - Otevřete formulář **Mé informace o projektu** v editoru formulářů a potom vyhledejte globálně jedinečný identifikátor (GUID) vedle parametru **fromId** v adrese URL, jak je znázorněno na následujícím obrázku.

    ![Hodnota formId nového formuláře v adrese URL](media/how-to-add-custom-forms-in-v2.0.png)

5. Vytvořte mapování **msdyn\_ordertype** pro hodnotu **formId** pomocí úprav webového prostředku msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Odeberte kód ze zdroje a nahraďte jej následujícím kódem.

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

6. Uložte a poté publikujte vlastní nastavení.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]