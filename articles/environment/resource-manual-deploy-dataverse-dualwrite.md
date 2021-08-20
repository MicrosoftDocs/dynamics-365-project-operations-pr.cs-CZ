---
title: Ruční nasazení aplikace Project Operations Dataverse s podporou duálního zápisu
description: Toto téma vysvětluje, jak ručně nasadit aplikaci Project Operations Dataverse tak, aby podporovala duální zápis.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986438"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Ruční nasazení aplikace Project Operations Dataverse s podporou duálního zápisu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma vysvětluje, jak ručně nasadit Microsoft Dynamics 365 Project Operations v Microsoft Dataverse tak, aby podporovala duální zápis. Project Operations detekuje konfiguraci prostředí a přidá další podporu pro duální zápis, pokud jsou splněny předpoklady.

Během nasazení do Microsoft Dynamics Lifecycle Services (LCS), pokud jste postupovali podle pokynů v tomto tématu, můžete přeskočit nasazení integrace Microsoft Power Platform (dříve známá jako prostředí Common Data Service).

Proces nasazení Project Operations v Dataverse podporující dvojitý zápis má čtyři hlavní kroky:

1. [Vytvořte nové prostředí v Dataverse, který podporuje duální zápis](#create).
2. [Přidejte do prostředí předpoklady pro duální zápis](#prerequisites).
3. [Přidejte aplikaci Project Operations Dataverse](#dataverse).
4. [Propojte svá prostředí](#link)

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Vytvořte nové prostředí v Dataverse, které podporuje duální zápis.

Chcete-li tento postup dokončit, musíte se přihlásit jako správce.

1. Otevřete [Centrum pro správu Power Platform](https://admin.powerplatform.com) a přihlaste se jako správce.
2. Vytvořit nové prostředí a pojmenujte jej.
3. Vyberte typ prostředí. Pokud jste se zaregistrovali k nabídce zkušební verze, vyberte **Zkušební verze (na základě předplatného)**.
4. Potvrďte oblast nasazení.
5. Povolte možnost **Vytvořit databázi pro toto prostředí**. 
6. Potvrďte jazyk a poté potvrďte, že měna odpovídá měně vaší aplikace Finance and Operations.
7. Povolte možnost **Aplikace Dynamics 365** a potvrďte, že je pole **Automaticky nasadit tyto aplikace** nastaveno na **Žádné**.
8. Přidejte skupinu zabezpečení, pokud je požadována.
9. Výběrem možnosti **Uložit** vytvořte prostředí.
10. Počkejte, až se nasazení dokončí a prostředí dosáhne stavu **Připraveno**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Přidejte do prostředí předpoklady pro duální zápis.

Podpora duálního zápisu zahrnuje další pole, která se přidávají ke klíčovým entitám, jako je například entita **Společnost**. Pokud přidáváte podporu duálního zápisu do existujícího prostředí, možná budete muset aktualizovat data, abyste podporu povolili. Informace o tom, jak provést bootstrap daa, viz [Bootstrap dat společnosti](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Další informace o duálním zápisu najdete v části [Systémové požadavky pro duální zápis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Dokončením tohoto postupu přidáte do svého prostředí předpoklady pro duální zápis.

1. Otevřete prostředí, které jste právě vytvořili, a přejděte na **Zdroj** \> **Aplikace Dynamics 365**.
2. Vyberte **Základní řešení pro duální zápis** v seznamu aplikací a nainstalujte jej.
3. Počkejte, až bude instalace dokončena. Potom vyberte **Řešení orchestrace aplikace pro duální zápis** v seznamu aplikací a nainstalujte jej.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Přidejte aplikaci Project Operations Dataverse.

Tento postup můžete dokončit, pouze pokud jste před instalací Project Operations dokončili předchozí postupy. Během instalace systém analyzuje konfiguraci prostředí a v případě potřeby přidává podporu pro duální zápis.

1. Otevřete prostředí, které jste vytvořili dříve, a přejděte na **Zdroj** \> **Aplikace Dynamics 365**.
2. Vyberte **Microsoft Dynamics 365 Project Operations** v seznamu aplikací a nainstalujte jej.

## <a name="link-your-environments"></a><a name="link"></a>Propojte svá prostředí

Po nasazení prostředí Dataverse můžete nastavit odkaz ve vašich aplikacích Finance and Operations. Postupujte podle pokynů v [Propojte prostředí pomocí průvodce duálním zápisem](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
