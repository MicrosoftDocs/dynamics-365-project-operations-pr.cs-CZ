---
title: Určení typu nasazení
description: Tento téma poskytuje informace, které vám pomůžou určit hlavní typ nasazení Project Operations pro vaši společnost.
author: stsporen
manager: Annbe
ms.date: 03/15/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1aae04230104d27db2f62db8e674697fd83460ac
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948096"
---
# <a name="determine-your-deployment-type"></a>Určení typu nasazení

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

> [!IMPORTANT]
> Po zakoupení licence začněte zde a určete nejlepší model nasazení Dynamics 365 Project Operations za použití [Řízeného toku instalace](https://aka.ms/provisionprojectoperations).
> Poté, co dokončíte postup instalace s průvodcem, budete přesměrováni na správný portál pro správu, abyste dokončili instalaci. Dokončete instalaci podle informací o nasazení.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Stávající zákazníci Dynamics pomocí Dynamics 365 Project Service Automation
Project Operations zahrnuje funkce dodávané s Project Service Automation. Pro tyto zákazníky bude v 1. vlně vydání v roce 2021 uvolněna cesta k upgradu.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Stávající zákazníci Dynamics 365 Finance pomocí Projektového řízení a účetnictví 

Stávající zákazníci řešení Finance, kteří používají funkce správy projektů a účetnictví, je mohou i nadále používat tak, jak jsou. Viz [Project Operations pro scénáře se skladovým materiálem a výrobními příkazy](#pma)


## <a name="deployment-regions"></a>Oblasti nasazení
Chcete-li zjistit, které regiony podporují nasazení Project Operations, přečtěte si sestavu [ Geografická dostupnost pro Dynamics 365 a Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Vyberte **Zobrazit sestavu** a rozbalte **Dynamics 365> Provozní aplikace> Dynamics 365 Project Operations** k zobrazení podporovaných regionů.

## <a name="deployment-types"></a>Typy nasazení
Project Operations podporuje více možností nasazení, aby odpovídaly vašim požadavkům. Ať už jste novým nebo stávajícím zákazníkem Dynamics 365, Project Operations může podpořit vaše potřeby.

Náš [Dotazník o nasazení](https://aka.ms/provisionprojectoperations) vám pomůže určit správné nasazení. Výsledky vás povedou k jednomu z následujících typů nasazení:

- [Omezené nasazení – od obchodu po pro forma fakturaci](#lite)
- [Project Operations pro scénáře se zdroji bez skladových materiálů](#integrated)
- [Project Operations pro scénáře se skladovým materiálem a výrobními příkazy](#pma)

Project Operation podporují scénáře zásob / výrobní zakázky a scénáře bez zásob / zdrojů ve stejném prostředí prostřednictvím konfigurací na úrovni právnických osob. Například Contoso mohou využívat možnosti skladové/výrobní zakázky ve svém výrobním závodě v USA (právnická osoba =Contoso Manufacturing United States). Contoso může využívat možnosti, které nejsou na základě skladu/prostředků, ve svém servisním závodě Contoso Robotics Arms ve Velké Británii (právnická osoba = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Omezené nasazení – od obchodu po pro forma fakturaci

Omezené nasazení zahrnuje následující funkce:

- Proces prodeje pro projekty, které rozšiřují možnosti aplikace Dynamics 365 Sales
- Plánování projektu pomocí Microsoft Project pro web
- Multidimenzionální ceny
- Sjednocené řízení zdrojů
- Sledování času
- Základní výdaje
- Proforma faktura pro kontrolu a úpravy projektového manažera 

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
- Řízení zdrojů
- Sledování času
- Plné výdaje
- OCR účtenky
- Úplná fakturace
- Uznání výnosů
- Výrobní zakázky
- Podpora skladovaných materiálů s inventářem

#### <a name="deployment-steps"></a>Postup nasazení
Určete nejlepší model nasazení Project Operations pomocí [Dotazník o nasazení](https://aka.ms/provisionprojectoperations).

Pro toto nasazení viz [Zaregistrujte se k odběru náhledu](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) a [Zřídit nové prostředí](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]