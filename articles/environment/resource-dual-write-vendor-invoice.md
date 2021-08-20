---
title: Integrace faktury dodavatele
description: Tento téma poskytuje informace o integraci faktury dodavatele v Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 538a2694591f1d0d368ee0ffeed9bdf12cb47420c3d0571f75185fe433f23436
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986483"
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

Daňová podřízená kniha, podřízená kniha dodavatele a další finanční zaúčtování se zaznamenávají podle potřeby v Dynamics 365 Finance v době zaúčtování faktury dodavatele.

![Integrace faktury dodavatele.](media/DW7VendorInvoice.png)

Když jsou záznamy zapsány do a entity **Faktura dodavatele** v Dataverse, začíná automatizovaný schvalovací proces záznamů. V případě potřeby lze stav automatizovaného schvalovacího procesu zkontrolovat v Dataverse tím, že půjdete do **Pokročilé nastavení** > **Systém** > **Systémové úlohy**. Po dokončení schválení se v systému vytvoří záznamy třídy transakcí materiálu v entitě **Skutečné hodnoty**.

Skutečné hodnoty související s materiálem jsou poté zpracovány pomocí mapy tabulky s duálním zápisem **Skutečné hodnoty integrace Project Operations (msdynactuals)**. Další informace viz [Odhady a skutečné hodnoty projektu](resource-dual-write-estimates-actuals.md).

Periodický proces **Import z předvádění** vytvoří v řádky deníku integrace Project Operations související s fakturou dodavatele. Výchozí účet offsetu je účet integrace zásobování. Když je integrační deník zaúčtován, vymaže se zůstatek účtu pro transakci faktury dodavatele a částka řádku se přesune na účet nákladů projektu. Jsou také vytvořeny transakce podřízené knihy projektu pro účely následné fakturace a uznání výnosů.
