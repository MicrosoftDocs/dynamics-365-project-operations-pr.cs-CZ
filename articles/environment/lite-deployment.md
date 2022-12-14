---
title: Nasazení Project Operations Lite
description: Tento článek poskytuje informace o tom, jak nainstalovat omezené nasazení Project Operations - od obchodu po pro forma fakturaci.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810970"
---
# <a name="deploy-project-operations-lite"></a>Nasazení Project Operations Lite

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_



Project Operations podporuje více modelů nasazení. Chcete-li zjistit nejlepší model nasazení, podívejte se na [Typy nasazení](determine-deployment-type.md).


> [!IMPORTANT]
> Toto nasazení, omezené nasazení - od obchodu po pro forma fakturaci, má za následek pouze nasazení **Dataverse Project Operations**.

- [Instalace Project Operations do nového prostředí Dataverse](#new)
- [Instalace do existujícího prostředí Dataverse](#existing)
- [Nainstalujte do stávajícího prostředí Dataverse, které obsahuje komponenty pro duální zápis](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Instalace Project Operations Lite do nového prostředí Dataverse

1. Jako [Globální správce nebo správce Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencí Project Operations vytvořte nové prostředí Dataverse v [Centru pro správu PowerPlatform](https://admin.powerplatform.com). Zkontrolujte, že jsou zapnuty funkce **Vytvořit databázi pro toto prostředí** a **Aplikace Dynamics 365**. Další informace naleznete v [Vytvoření a správa prostředí v centru pro správu Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Vyberte **Microsoft Dynamics 365 Project Operations** ze seznamu nasazení aplikací Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instalace Project Operations Lite do stávajícího prostředí Dataverse 
1. Jako [Globální správce nebo správce Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencí Project Operations vyhledejte prostředí v [Centru pro správu PowerPlatform](https://admin.powerplatform.com), kam chcete nainstalovat Project Operations.
1. Nainstalujte **Microsoft Dynamics 365 Project Operations** ze seznamu nasazení aplikací Dynamics 365. Další informace najdete v části [Správa aplikací Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Instalace Project Operations Lite do stávajícího prostředí Dataverse, kde již existují řešení pro duální zápis

Pokud chcete pokračovat v používání Project Operations v režimu nasazení Lite, měli byste postupovat takto:

1. Jako [Globální správce nebo správce Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licencí Project Operations vyhledejte prostředí v [Centru pro správu PowerPlatform](https://admin.powerplatform.com), kam chcete nainstalovat Project Operations.
1. Nainstalujte **Microsoft Dynamics 365 Project Operations** ze seznamu nasazení aplikací Dynamics 365. Další informace najdete v části [Správa aplikací Dynamics 365](/power-platform/admin/manage-apps).
1. Protože vaše prostředí má nainstalované komponenty pro duální zápis, které pomáhají s integrací do finančních a provozních aplikací, instalace Project Operations také nainstaluje možnosti a rozšíření potřebná k integraci dat souvisejících s projektem do finančních a provozních aplikací. Protože chcete provozovat Project Operations v nasazení Lite, měly by být tyto integrační komponenty odstraněny, protože budou vytvářet omezení a režii pro scénáře nasazení Lite. Chcete-li tyto součásti odebrat, ručně odinstalujte řešení **Duální zápis Dynamics 365 Project Operations** a **Mapy entity duálního zápisu Dynamics 365 Project Operations**.
1. Přejděte do **Project Operations -> Nastavení -> Parametry**. Otevřete stránku s údaji **Parametr projektu** a nastavte pole **Chování při upgradu řešení** na **Pouze Lite**. To zajišťuje, že žádné následné upgrady Project Operations nevrátí integrační komponenty zpět do Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
