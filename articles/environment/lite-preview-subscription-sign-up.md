---
title: Registrace k odběru verze Preview – omezené
description: Toto téma obsahuje informace o tom, jak se přihlásit k odběru a nasadit omezené nasazení Project Operations - od obchodu po pro forma fakturaci.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997413"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrace k odběru verze Preview – omezené 

Toto téma vysvětluje, jak se přihlásit k odběru nabídky a nasazení partnerské nabídky a nasazení Dynamics 365 Project Operations Lite - dohoda o proforma fakturaci.

> [!NOTE]
> Tento proces se v nadcházejících verzích Project Operations změní.

## <a name="prerequisites"></a>Požadavky

- Obdržíte e-mail s výzvou k účasti v programu Preview. O preview můžete požádat na [webu Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Uživatel, který nasadí preview, musí mít práva globálního správce klienta Azure.
- Přečtěte si všechny smluvní podmínky.

## <a name="subscribe"></a>Odebírat

Když obdržíte schválení [požadavku na preview](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), dostanete od společnosti Microsoft e-mailem dvě nabídky. Tyto nabídky vám umožňují nasadit Project Operations Preview:

- Zkušební verze Preview Dynamics 365 Project Operations (CRM)
- Office 365 Project Operations – zkušební verze Preview

> [!IMPORTANT]
> Tuto úlohu musí v organizaci provést pouze jedna osoba, správce tenanta. Pokud nejste předplatitelem tohoto vydání, počkejte, dokud nebude vaše organizace zaregistrována a neobdržíte přihlašovací údaje uživatele.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Zkušební verze Preview Dynamics 365 Project Operations (CRM) 

Než začnete, ujistěte se, že jste přihlášeni do prohlížeče s pracovním účtem uživatele v klientu, kde chcete Project Operations Preview mít.

1. Uplatněte první kód nabídky **Dynamics 365 Project Operations (CRM) - zkušební verze náhledu** vložením do adresy URL prohlížeče.

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

3. Ověřte, že jsou vybrány licence **Dynamics 365 Project Operations (CRM) Preview** a **Office 365 Project Operations - Preview**. 
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]