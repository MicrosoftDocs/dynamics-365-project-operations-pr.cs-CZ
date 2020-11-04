---
title: Registrace Preview předplatného
description: Toto téma obsahuje informace o tom, jak se přihlásit k odběru a nasadit omezené nasazení Project Operations - od obchodu po pro forma fakturaci.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073643"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Přihlaste se k odběru Preview pro omezené nasazení - od obchodu po pro forma fakturaci

Toto téma vysvětluje, jak se přihlásit k odběru preview nabídky partnera a nasadit omezené nasazení Dynamics 365 Project Operations - od obchodu po pro forma fakturaci.

> [!NOTE]
> Tento proces se v nadcházejících verzích Project Operations změní.

## <a name="prerequisites"></a>Požadavky

- Obdržíte e-mail s výzvou k účasti v programu Preview. O preview můžete požádat na [webu Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Uživatel, který nasadí preview, musí mít práva globálního správce klienta Azure.
- Přečtěte si všechny smluvní podmínky.

## <a name="subscribe"></a>Odebírat

Když obdržíte schválení [požadavku na preview](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), dostanete od společnosti Microsoft e-mailem dvě nabídky. Tyto nabídky vám umožňují nasadit Project Operations Preview:

- Dynamics 365 Project Operations (CRM) – zkušební verze Preview
- Office 365 Project Operations – zkušební verze Preview

> [!IMPORTANT]
> Tuto úlohu musí v organizaci provést pouze jedna osoba, správce tenanta. Pokud nejste předplatitelem tohoto vydání, počkejte, dokud nebude vaše organizace zaregistrována a neobdržíte přihlašovací údaje uživatele.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – zkušební verze Preview 

Než začnete, ujistěte se, že jste přihlášeni do prohlížeče s pracovním účtem uživatele v klientu, kde chcete Project Operations Preview mít.

1. Uplatněte první kód nabídky, **Dynamics 365 Project Operations (CRM) – zkušební verze Preview** , vložením do adresy URL prohlížeče.

![Uplatnění nabídky](./media/16RedeemFirstOfferNew.png)

2. Objednávku potvrďte.
![Potvrďte objednávku](./media/17ConfirmOrderNew.png)

Uvidíte, že nabídka potvrzení byla úspěšně uplatněna.

![Potvrzení](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – zkušební verze Preview

Opakujte stejné kroky jako u prvního nabídkového kódu. Přidejte druhý kód nabídky pomocí stejného uživatelského účtu, který byl použit s prvním kódem nabídky.

## <a name="assign-licenses"></a>Přiřazení licencí

> [!IMPORTANT]
> Budete potřebovat přístup správce k portálu Microsoft 365 vaší organizace, abyste mohli dokončit následující kroky.


1. Přejděte do [Centra pro správu Microsoft 365](https://portal.office.com/), kde přiřadíte licence vašim uživatelům.

![Domovská stránka centra pro správu](./media/14AdminPortal.png)

2. Na stránce **Aktivní uživatelé** vyberte uživatele, kterým chcete přiřadit licenci.

![Přiřazení licencí](./media/15AssignLicenses.png)

3. Ověřte, že je vybrána položka **Dynamics 365 Project Operations (CRM) – Preview** a licence **Office 365 Project Operations – Preview**. 
4. Vyberte volbu **Uložit změny**.

## <a name="create-a-new-cds-environment"></a>Vytvoření nového prostředí CDS

1. Nové prostředí pro nasazení Project Operations CDS zřiďte podle pokynů v tématu [Model nasazení CDS](lite-deployment.md). Když vyberete typ prostředí, ujistěte se, že používáte **Zkušební verze (na základě předplatného)**.
![Nové prostředí](./media/19CreateEnvironment.png)

2. Vyberte nastavení **Povolit aplikace Dynamics 365** a nechte možnost **Automaticky nasadit tyto aplikace** prázdnou.  
3. Výběrem možnosti **Uložit** vytvořte prostředí.

![Přidat databázi](./media/20CreateEnvironment1.png)

4. Po vytvoření prostředí nainstalujte řešení **Microsoft Dynamics 365 Project Operations**. 

![Instalace řešení](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Nainstalujte konfiguraci CDS a nastavte ukázková data

Nainstalujte konfiguraci CDS a nastavte ukázková data podle pokynů v tématu [Použití ukázkového nastavení a konfiguračních dat](lite-apply-demo-setup-config-data.md).
