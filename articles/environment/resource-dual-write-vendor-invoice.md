---
title: Integrace faktury dodavatele
description: Tento téma poskytuje informace o integraci faktury dodavatele v Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8650eed2230b99b821c1635fdc88252bb65c5583
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591167"
---
# <a name="vendor-invoice-integration"></a>Integrace faktury dodavatele

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Zásobování související s projektem v Dynamics 365 Project Operations lze zaznamenat přechodem na **Závazky** > **Faktury** > **Nevyřízené faktury dodavatele** a pomocí dokladu nevyřízené faktury dodavatele. Další informace viz [Zakoupení neskladovaných materiálů pomocí nevyřízené faktury dodavatele](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Než použijete funkce popsané v tomto tématu, zkontrolujte a použijte požadované konfigurace. Další informace viz [Povolené neskladovaných materiálů a nevyřízených faktury dodavatele](../procurement/configure-materials-nonstocked.md).

V Project Operations se řádky faktury dodavatele související s projektem zaúčtují pomocí zvláštních pravidel účtování:

- Náklady související s projektem (včetně nevratné daně) nejsou okamžitě zaúčtovány na účet nákladů projektu v hlavní knize. Místo toho se náklady zaúčtují na **Účet integrace zásobování**. Tento účet se konfiguruje v nastavení **Řízení projektů a účetnictví** > **Nastavit** > **Parametry řízení projektu a účetnictví** na kartě **Project Operations na Dynamics 365 Customer engagement**.
- Duální zápis synchronizuje údaje faktury dodavatele s Microsoft Dataverse pomocí následujících map tabulek:

     - **Entita exportu faktury dodavatele projektu integrace Project Operations (msdyn_projectvendorinvoices)**: Tato mapa tabulky synchronizuje informace v záhlaví faktury dodavatele. Synchronizovány jsou pouze faktury dodavatele s alespoň jedním řádkem, který obsahuje ID projektu Dataverse.
     - **Entita exportu řádku faktury dodavatele projektu integrace Project Operations (msdyn_projectvendorinvoices)**: Tato mapa tabulky synchronizuje informace v řádku faktury dodavatele. Do Dataverse jsou synchronizovány pouze řádky, které obsahují ID projektu.

     > [!NOTE]
     > Údaje faktury dodavatele v Dataverse nelze upravovat.

Dílčí účetní kniha daní, dílčí kniha dodavatele a další finanční účtování se zaznamenávají podle potřeby v Dynamics 365 Finance při zaúčtování faktury dodavatele.

![Integrace faktury dodavatele.](media/DW7VendorInvoice.png)

Když jsou záznamy zapsány do a entity **Faktura dodavatele** v Dataverse, začíná automatizovaný schvalovací proces záznamů. V případě potřeby lze stav automatizovaného schvalovacího procesu zkontrolovat v Dataverse tím, že půjdete do **Pokročilé nastavení** > **Systém** > **Systémové úlohy**. Po dokončení schválení se v systému vytvoří záznamy třídy transakcí materiálu v entitě **Skutečné hodnoty**.

Skutečné hodnoty související s materiálem jsou poté zpracovány pomocí mapy tabulky s duálním zápisem **Skutečné hodnoty integrace Project Operations (msdynactuals)**. Další informace viz [Odhady a skutečné hodnoty projektu](resource-dual-write-estimates-actuals.md).

Periodický proces **Import z předvádění** vytvoří v řádky deníku integrace Project Operations související s fakturou dodavatele. Výchozí účet offsetu je účet integrace zásobování. Když je integrační deník zaúčtován, vymaže se zůstatek účtu pro transakci faktury dodavatele a částka řádku se přesune na účet nákladů projektu. Jsou také vytvořeny transakce podřízené knihy projektu pro účely následné fakturace a uznání výnosů.
