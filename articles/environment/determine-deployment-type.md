---
title: Určení typu nasazení
description: Tento téma poskytuje informace, které vám pomůžou určit hlavní typ nasazení Project Operations pro vaši společnost.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401210"
---
# <a name="determine-your-deployment-type"></a>Určení typu nasazení

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

> [!IMPORTANT]
> Po zakoupení licence začněte zde a určete nejlepší model nasazení Dynamics 365 Project Operations pomocí [Řízený průběh instalace](https://aka.ms/provisionprojectoperations).
> Poté, co dokončíte postup instalace s průvodcem, budete přesměrováni na správný portál pro správu, abyste dokončili instalaci. Dokončete instalaci podle informací o nasazení.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Stávající zákazníci Dynamics pomocí Dynamics 365 Project Service Automation
Project Operations zahrnuje funkce dodávané s Project Service Automation. Pro tyto zákazníky bude v 1. vlně vydání v roce 2021 uvolněna cesta k upgradu.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Stávající zákazníci Dynamics 365 Finance pomocí Projektového řízení a účetnictví 

Stávající zákazníci řešení Finance, kteří používají funkce správy projektů a účetnictví, je mohou i nadále používat tak, jak jsou. Viz [Project Operations pro scénáře se skladovým materiálem a výrobními příkazy](#pma)


## <a name="deployment-types"></a>Typy nasazení
Project Operations podporuje více možností nasazení, aby odpovídaly vašim požadavkům. Ať už jste novým nebo stávajícím zákazníkem Dynamics 365, Project Operations může podpořit vaše potřeby.

Náš [Dotazník o nasazení](https://aka.ms/provisionprojectoperations) vám pomůže určit správné nasazení. Výsledky vás povedou k jednomu z následujících typů nasazení:

- [Omezené nasazení – od obchodu po pro forma fakturaci](#lite)
- [Project Operations pro scénáře se zdroji bez skladových materiálů](#integrated)
- [Project Operations pro scénáře se skladovým materiálem a výrobními příkazy](#pma)

Project Operation podporují scénáře zásob / výrobní zakázky a scénáře bez zásob / zdrojů ve stejném prostředí prostřednictvím konfigurací na úrovni právnických osob. Například společnost Contoso může využívat možnosti skladového materiálu / výrobní objednávky ve svém výrobním závodě v USA (právnická osoba = Contoso Manufacturing United States). Společnost Contoso může ve svém servisním zařízení Contoso Robotics Arms ve Velké Británii využívat funkce, které nejsou skladové / založené na zdrojích (právnická osoba = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Omezené nasazení – od obchodu po pro forma fakturaci

Omezené nasazení zahrnuje následující funkce:

- Proces prodeje pro projekty, které rozšiřují možnosti aplikace Dynamics 365 Sales
- Plánování projektu pomocí Microsoft Project pro web
- Multidimenzionální ceny
- Sjednocené řízení zdrojů
- Sledování času
- Základní výdaje
- Proforma a fakturace zaměřená na zákazníka 

#### <a name="deployment-steps"></a>Postup nasazení
Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).

Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](lite-preview-subscription-sign-up.md) a [Zřídit nové prostředí](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations pro scénáře se zdroji bez skladových materiálů
Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě:
 
- Proces prodeje pro projekty, které rozšiřují aplikaci Dynamics 365 Sales
- Plánování projektu pomocí Microsoft Project pro web
- Multidimenzionální ceny
- Sjednocené řízení zdrojů
- Sledování času
- Základní výdaje
- Plné výdaje
- OCR účtenky
- Proforma a fakturace zaměřená na zákazníka 
- Vykazování výnosů z projektů

#### <a name="deployment-steps"></a>Postup nasazení
Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).

Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](resource-sign-up-preview-subscription.md) a [Zřídit nové prostředí](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations pro scénáře se skladovým materiálem a výrobními příkazy

- Plánování projektu pomocí strukturovaného rozpisu prací
- Správa zdrojů
- Doba sledování
- Plné výdaje
- OCR účtenky
- Plná fakturace
- Uznání výnosů
- Výrobní zakázky
- Podpora materiálů

#### <a name="deployment-steps"></a>Postup nasazení
Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).

Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) a [Zřídit nové prostředí](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

