---
title: Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o tom, jak přihlásit odběr a nasadit Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4c2cd4c5d4dfbb95398932d432864cf0d4d5d54d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276835"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma vysvětluje, jak se přihlásit k odběru preview / nabídky partnera a nasadit prostředí Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.

## <a name="prerequisites"></a>Požadavky

- Obdržíte e-mail s výzvou k účasti v programu Preview. O preview můžete požádat na [webu Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Uživatel, který nasadí preview, musí mít práva globálního správce klienta Azure.
- Nasazení prostředí Finance vyžaduje platné předplatné Azure, kterému bude účtováno každé prostředí zvlášť. V začátcích můžete použít stávající předplatné vaší organizace nebo [zkušební verzi Azure](https://azure.microsoft.com/en-us/free/). Prostředí CDS bude poskytováno zdarma po omezenou dobu 30 dnů.

## <a name="subscribe"></a>Odebírat

Až bude váš [požadavek na preview](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) schválen, dostanete od společnosti Microsoft e-mailem tři nabídky. Tyto nabídky vám umožňují nasadit Project Operations Preview:

- Zkušební verze Preview Dynamics 365 Project Operations (CRM)
- Office 365 Project Operations – zkušební verze Preview
- Dynamics 365 Finance - Zkušební verze Preview

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

### <a name="dynamics-365-finance-preview-trial"></a>Zkušební verze Preview Dynamics 365 Finance

Stejné kroky opakujte s poslední nabídkou z uvítacího e-mailu.

## <a name="assign-licenses"></a>Přiřazení licencí

> [!IMPORTANT]
> Budete potřebovat přístup správce k portálu Microsoft 365 vaší organizace, abyste mohli dokončit následující kroky.

1. Přejděte do [Centra pro správu Microsoft 365](https://portal.office.com/), kde přiřadíte licence vašim uživatelům.

![Domovská stránka centra pro správu](./media/14AdminPortal.png)

2. Na stránce **Aktivní uživatelé** vyberte uživatele, kterým chcete přiřadit licenci.

![Přiřazení licencí](./media/15AssignLicenses.png)

3. Ověřte, že byla vybrána licence **Náhled Dynamics 365 Project Operations (CRM)** a **Office 365 Project Operations - náhled** a vyberte **Uložit změny**.

> [!NOTE]
> Nabídku zkušební verze Finance není nutné přiřadit uživateli.

## <a name="start-a-new-project-in-lcs"></a>Zahájení nového projektu v LCS

Vytvořte nový projekt LCS podle popisu v tématu [Spuštění nového projektu v LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Přidání předplatného Azure do projektu LCS

Chcete-li dokončit tento úkol, postupujte podle pokynů v tématu [Přidání předplatného Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Nasazení ukázkového prostředí Finance spolu s Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

Postupujte podle pokynů v tématu [Zřízení nového prostředí](resource-provision-new-environment.md) a dokončete nasazení. Pro preview použijte typ nasazení [demo prostředí](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment). 

## <a name="install-cds-setup-and-configuration-data"></a>Instalace nastavení CDS a dat konfigurace

Nainstalujte instalační a konfigurační data CDS podle popisu v tématu [Nastavení a použití dat konfigurace ve službě Common Data Service](resource-apply-pro-setup-config-data.md).
Tento krok dokončete až poté, co se nasadí ukázkové prostředí Finance a budou připravena ukázková data ve FO.


[!INCLUDE[footer-include](../includes/footer-banner.md)]