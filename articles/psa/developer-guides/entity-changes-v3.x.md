---
title: Změny entit, ovládacích prvků a uživatelského rozhraní (Project Service Automation 3.x)
description: Tento článek popisuje změny řešení pro Microsoft Dynamics Project Service Automation 3.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
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
ms.openlocfilehash: 8f54d263666c4fb999464f98c0138fc008dbbbd2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926860"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Změny entit, ovládacích prvků a uživatelského rozhraní (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Ve vydání Microsoft Dynamics Project Service Automation (PSA) 3.x bylo provedeno mnoho změn entit, ovládacích prvků, zobrazení a uživatelského rozhraní. Tento článek obsahuje informace o těchto důležitých změnách.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Vztahy nadřízenosti a podřízenosti pro entity prodejní dokument, řádek prodejního dokumentu, podrobnosti řádku prodejního dokumentu
Ve verzích Dynamics 365 Project Service Automation (PSA), které byly vydány před verzí 3.0, byly některé vztahy mezi entitami prodejní dokument, řádky prodejního dokumentu, podrobnosti řádku prodejního dokumentu implementovány pomocí řetězcových polí, která by obsahovala řetězcovou reprezentaci GUID související entity. To bylo způsobeno omezeními platformy, která na straně serveru a klienta tohoto řešení vyžadovala množství vlastního kódu, aby tyto vztahy fungovaly podobně jako u typické vztahy entity Dynamics CRM a aby pole řetězců fungovala jako vyhledávací pole.

Aplikace PSA 3.0 byla aktualizován za účelem využití nových vztahů entit mezi entitami prodejní dokument a řádek prodejního dokumentu.

Vzhledem k tomu, že vyhledávací pole lze nyní použít k označení odkazů na entity, nejsou už potřebná pole, která v předchozích verzích obsahovala řetězcovou hodnotu GUID související entity, a byla proto vyřazena. Vlastní kód na straně klienta a serveru, který zpracovává vztahy definované starými řetězcovými poli, byl také vyřazen.

### <a name="entity-schema-changes"></a>Změny schématu entit
V následující tabulce je uveden seznam vyřazených řetězcových polí typu 1:1 a nová vyhledávací pole entit. 

 Entita |   Vyřazené pole (řetězcové) | Nové pole (vyhledávací)
--- | --- | ---
invoicedetail (Řádek faktury) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (skutečná hodnota) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Rozpis faktury řádku projektové smlouvy) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Milník řádku projektové smlouvy) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Fakt) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Podrobnosti řádku faktury) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Řádek deníku) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Kategorie zdroje řádku projektové smlouvy) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Podrobnosti řádku projektové smlouvy) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Kategorie transakce řádku projektové smlouvy) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Klasifikace transakce řádku projektové smlouvy) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Rozpis faktury řádku nabídky) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Kategorie zdroje řádku nabídky) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Milník řádku nabídky) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Podrobnosti řádku nabídky) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Kategorie transakce řádku nabídky) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Klasifikace transakce řádku nabídky) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Řádek objednávky) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Vyřazená vlastní zobrazení a ovládací prvky
Následující vlastní zobrazení a ovládací prvky a jejich související artefakty byly vyřazeny.

- Zobrazení účtovatelnosti.
- Vlastní ovládací prvky mřížky pro zobrazení podrobností řádku nabídky na stránce **Informace o projektu** pro řádek nabídky.
- Vlastní ovládací prvky mřížky pro zobrazení podrobností řádku projektové smlouvy na stránce **Informace o projektu** pro řádek prodejní objednávky.

> [!NOTE]
> Úplný seznam vyřazených zdrojů viz [Vyřazené webové prostředky v Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Modul aplikace Sjednocené rozhraní klienta
Po zavedení modulů aplikace Sjednocené rozhraní klienta (UCI) byly položky mapy webu PSA ze systému odebrány.  
Funkce související s přepínáním formulářů pro Příležitost, Nabídku, Objednávku, Fakturu byla vyřazena, neboť již není vyžadována, protože modul aplikace UCI obsahuje pouze verze PSA těchto formulářů.  

Následující webové prostředky byly vyřazeny:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Úplný seznam vyřazených zdrojů viz [Vyřazené webové prostředky v Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
