---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Project Operations
description: Tento článek popisuje funkce, které byly odebrány nebo u nichž se plánuje odebrání z aplikace Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921478"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Project Operations

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení – od obchodu po proforma fakturaci a Project Operations pro scénáře založené na skladovém materiálu / výrobě_

Tento článek popisuje funkce, které byly odebrány nebo u nichž se plánuje odebrání z aplikace Dynamics 365 Project Operations.

- *Odebraná* funkce již v produktu není k dispozici.
- *Zastaralá* funkce není v aktivním vývoji a může být v budoucí aktualizaci odebrána.

Tento seznam vám pomůže zvážit tato odebrání a zastarání pro vaše vlastní plánování.

> [!NOTE]
> Podrobné informace o objektech v finančních a provozních aplikacích lze nalézt v části [**Sestavy technických informací**](/dynamics/s-e/global/axtechrefrep_61). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí finančních a provozních aplikací.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funkce odstraněné nebo zastaralé ve verzi Project Operations z března 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Řízení projektu a účetnictví - Parametr "Vždy vytvořit transakci úpravy"

| &nbsp; | &nbsp; |
|--------|--------|
| **Důvod zastarání/odebrání** | Pro účely auditu jsou vyžadovány opravné transakce. Po ukončení podpory bude tento parametr skrytý. Systém vždy vytvoří transakce úprav, stejně jako v současnosti, když je parametr nastaven na **Ano**. |
| **Nahrazeno jinou funkcí?** | No |
| **Dotčené oblasti produktu** | Aplikace |
| **Možnost nasazení** | Project Operations pro scénáře se skladovým materiálem a výrobními příkazy |
| **Stav** | Zastaralé: Do 1. března 2023 skryjeme parametr a změníme chování systému tak, aby byly vždy vytvářeny transakce úprav. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Řízení a účetnictví projektu – Parametr "Použít datum úpravy jako nové datum projektu"

| &nbsp; | &nbsp; |
|--------|--------|
| **Důvod zastarání/odebrání** | Tento parametr byl původně použit k umožnění úprav při uzavření fiskálního období. Již však není nutný, protože účetní datum transakce lze změnit na první datum otevřeného období, pokud je konfigurováno. Datum projektu se nesmí měnit, protože představuje datum, kdy k transakci došlo. |
| **Nahrazeno jinou funkcí?** | No |
| **Dotčené oblasti produktu** | Aplikace |
| **Možnost nasazení** | Project Operations pro scénáře se skladovým materiálem a výrobními příkazy |
| **Stav** | Zastaralé: Do 1. března 2023 skryjeme parametr a změníme chování systému tak, aby se datum projektu při úpravách nikdy nezměnilo. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Pracovní postup žádosti o zdroj v Project Operations pro scénáře založené na skladovém materiálu / výrobě

| &nbsp; | &nbsp; |
|--------|--------|
| **Důvod zastarání/odebrání** | Zastaralé kvůli nízkému využití a omezení objemu transakcí. |
| **Nahrazeno jinou funkcí?** | No |
| **Dotčené oblasti produktu** | Aplikace |
| **Možnost nasazení** | Project Operations pro scénáře se skladovým materiálem a výrobními příkazy |
| **Stav** | Zastaralé: Do 1. března 2023 deaktivujeme možnost žádat o zdroje pro projekt pomocí pracovního postupu. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Stránka návrhu faktury projektu bez zobrazení záhlaví a řádků

| &nbsp; | &nbsp; |
|--------|--------|
| **Důvod zastarání/odebrání** | Zastaralé kvůli vylepšením stránky, která byla představena společně s funkcí **Použít návrh projektové faktury a formuláře deníku faktur se zobrazením Záhlaví a řádky**. |
| **Nahrazeno jinou funkcí?** | Ano |
| **Dotčené oblasti produktu** | Aplikace |
| **Možnost nasazení** | Project Operations pro scénáře založené na skladovém materiálu / výrobě; Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě |
| **Stav** | Zastaralé: Do 1. března 2023 vypneme dřívější (starší) stránku a zapneme ve výchozím nastavení funkci **Použít návrh projektové faktury a formuláře deníku faktur se zobrazením Záhlaví a řádky**. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funkce odstraněné nebo zastaralé ve verzi Project Operations z prosince 2021

### <a name="collaboration-workspaces"></a>Pracovní prostory pro spolupráci

[Vytvoření nebo propojení pracovního prostoru pro spolupráci (Project)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Důvod zastarání/odebrání** | Zastaralé kvůli nízkému využití. Zákazníci využívající Project Operations pro scénáře se zdroji bez skladových materiálů mohou využít [Spolupráci se Skupinami Office](../project-management/collaboration-groups.md). |
| **Nahrazeno jinou funkcí?** | No |
| **Dotčené oblasti produktu** | Aplikace  |
| **Možnost nasazení** | Project Operations pro scénáře se skladovým materiálem a výrobními příkazy |
| **Stav** | Zastaralé: Od 1. prosince 2022 plánujeme ukončit podporu pracovních prostorů pro spolupráci. |
