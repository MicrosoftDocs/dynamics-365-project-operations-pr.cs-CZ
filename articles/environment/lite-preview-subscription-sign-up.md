---
title: Registrace k odběru verze Preview - omezené
description: Tento článek poskytuje informace o tom, jak přihlásit odběr a nasadit omezené nasazení Project Operations - od obchodu po pro forma fakturaci.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410003"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrace k odběru verze Preview - omezené 

Tento článek vysvětluje, jak si zaregistrovat zkušební nabídku a nasadit omezené nasazení Dynamics 365 Project Operations - od obchodu po pro forma fakturaci.

> [!NOTE]
> Tento proces se v nadcházejících verzích Project Operations změní.

## <a name="prerequisites"></a>Požadavky
- Uživatel, který nasadí preview, musí mít práva globálního správce klienta Azure. Během prvního uplatnění nabídky můžete vytvořit nájemce.

> [!IMPORTANT]
> Tuto úlohu musí v organizaci provést pouze jedna osoba, správce tenanta. Pokud nejste předplatitelem tohoto vydání, počkejte, dokud nebude vaše organizace zaregistrována a neobdržíte přihlašovací údaje uživatele.
> 
> Zkušební verze jsou na jedno použití v klientovi. Zkušební verzi můžete spustit pouze jednou. Pro účely zkušebního období vám doporučujeme vytvořit nového klienta.

### <a name="dynamics-365-project-operations-trial"></a>Zkušební verze Dynamics 365 Project Operations 

Než začnete, ujistěte se, že jste přihlášeni do prohlížeče s pracovním účtem uživatele v klientu, kde chcete Project Operations Preview mít.

1. Přejděte na [Zkušební verze Project Operations](https://aka.ms/try-po), chcete-li uplatnit první nabídkový kód **Dynamics 365 Project Operations**.
2. Objednávku potvrďte.

  Uvidíte, že nabídka potvrzení byla úspěšně uplatněna.

## <a name="assign-licenses"></a>Přiřazení licencí

> [!IMPORTANT]
> Budete potřebovat přístup správce k portálu Microsoft 365 vaší organizace, abyste mohli dokončit následující kroky.


1. Přejděte do [centra pro správu Microsoft 365](https://portal.office.com/) a přiřaďte licence vašim uživatelům.
2. Na stránce **Aktivní uživatelé** vyberte uživatele, kterým chcete přiřadit licenci.
3. Ověřte, že je vybrána licence **Dynamics 365 Project Operations**. 
4. Vyberte volbu **Uložit změny**.

## <a name="create-a-new-dataverse-environment"></a>Vytvořte nové prostředí Dataverse

1. Nové prostředí nasazení Project Operations Dataverse zřiďte podle pokynů v článku [Model nasazení Dataverse](lite-deployment.md). Když vyberete typ prostředí, ujistěte se, že používáte **Zkušební verze (na základě předplatného)**.

  ![Nové prostředí.](./media/19CreateEnvironment.png)

2. Vyberte nastavení **Povolit aplikace Dynamics 365** a nechte možnost **Automaticky nasadit tyto aplikace** prázdnou.  
3. Výběrem možnosti **Uložit** vytvořte prostředí.

  ![Přidat databázi.](./media/20CreateEnvironment1.png)

4. Po vytvoření prostředí nainstalujte řešení **Microsoft Dynamics 365 Project Operations**. 

![Instalace řešení.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Nastavení ukázkových dat

Nastavte ukázková data podle pokynů v článku [Použití ukázkového nastavení a dat konfigurace](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
