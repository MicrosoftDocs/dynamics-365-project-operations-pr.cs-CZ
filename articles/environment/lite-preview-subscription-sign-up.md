---
title: Registrace k odběru verze Preview – omezené
description: Toto téma obsahuje informace o tom, jak se přihlásit k odběru a nasadit omezené nasazení Project Operations - od obchodu po pro forma fakturaci.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334774"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrace k odběru verze Preview - omezené 

Tento téma vysvětluje, jak se přihlásit k odběru zkušební nabídky a nasadit Dynamics 365 Project Operations omezené nasazení – od obchodu po pro forma fakturaci

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


1. Přejděte do [Centra pro správu Microsoft 365](https://portal.office.com/), kde přiřadíte licence vašim uživatelům.
2. Na stránce **Aktivní uživatelé** vyberte uživatele, kterým chcete přiřadit licenci.
3. Ověřte, že je vybrána licence **Dynamics 365 Project Operations**. 
4. Vyberte volbu **Uložit změny**.

## <a name="create-a-new-dataverse-environment"></a>Vytvořte nové prostředí Dataverse

1. Nové prostředí pro nasazení Project Operations Dataverse zřiďte podle pokynů v tématu [Model nasazení Dataverse](lite-deployment.md). Když vyberete typ prostředí, ujistěte se, že používáte **Zkušební verze (na základě předplatného)**.

  ![Nové prostředí](./media/19CreateEnvironment.png)

2. Vyberte nastavení **Povolit aplikace Dynamics 365** a nechte možnost **Automaticky nasadit tyto aplikace** prázdnou.  
3. Výběrem možnosti **Uložit** vytvořte prostředí.

  ![Přidat databázi](./media/20CreateEnvironment1.png)

4. Po vytvoření prostředí nainstalujte řešení **Microsoft Dynamics 365 Project Operations**. 

![Instalace řešení](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Nainstalujte konfiguraci CDS a nastavte ukázková data

Nainstalujte konfiguraci CDS a nastavte ukázková data podle pokynů v tématu [Použití ukázkového nastavení a konfiguračních dat](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
