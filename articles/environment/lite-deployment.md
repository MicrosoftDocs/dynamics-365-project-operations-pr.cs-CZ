---
title: Nasazení Project Operations – omezené
description: Toto téma obsahuje informace o tom, jak nainstalovat omezené nasazení Project Operations - od obchodu po pro forma fakturaci.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580724"
---
# <a name="deploy-project-operations---lite"></a>Nasazení Project Operations – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_



Project Operations podporuje více modelů nasazení. Chcete-li zjistit nejlepší model nasazení, podívejte se na [Typy nasazení](determine-deployment-type.md).


> [!IMPORTANT]
> Toto nasazení, omezené nasazení - od obchodu po pro forma fakturaci, má za následek pouze nasazení **Dataverse Project Operations**.

- [Instalace Project Operations do nového prostředí Dataverse](#new)
- [Instalace do existujícího prostředí Dataverse](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Instalace Project Operations do nového prostředí Dataverse

1. Jako [Globální správce nebo správce Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencí Project Operations vytvořte nové prostředí Dataverse v [Centru pro správu PowerPlatform](https://admin.powerplatform.com). Zkontrolujte, že jsou zapnuty funkce **Vytvořit databázi pro toto prostředí** a **Aplikace Dynamics 365**. Další informace naleznete v [Vytvoření a správa prostředí v centru pro správu Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Vyberte **Microsoft Dynamics 365 Project Operations** ze seznamu nasazení aplikací Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instalace Project Operations do stávajícího prostředí Dataverse
1. Ujistěte se, že prostředí nemá konfigurováno [duální zápis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), protože instalace poté nainstaluje schopnosti [Project Operations pro scénáře založené na zdrojích/položkách, které nejsou na skladě](project-operations-integrated-deployment-overview.md).
2. Jako [Globální správce nebo správce Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencí Project Operations vyhledejte prostředí v [Centru pro správu PowerPlatform](https://admin.powerplatform.com), kam chcete nainstalovat Project Operations.
3. Nainstalujte **Microsoft Dynamics 365 Project Operations** ze seznamu nasazení aplikací Dynamics 365. Další informace najdete v části [Správa aplikací Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
