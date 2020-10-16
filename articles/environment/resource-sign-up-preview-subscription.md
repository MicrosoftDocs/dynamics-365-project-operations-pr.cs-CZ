---
title: Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o tom, jak přihlásit odběr a nasadit Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948802"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma vysvětluje, jak se přihlásit k odběru preview / nabídky partnera a nasadit prostředí Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.

## <a name="prerequisites"></a>Požadavky

- Obdržíte e-mail s výzvou k účasti v programu Preview. O preview můžete požádat na [webu Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Uživatel, který nasadí preview, musí mít práva globálního správce klienta Azure.
- Nasazení prostředí Finance vyžaduje platné předplatné Azure, kterému bude účtováno každé prostředí zvlášť. V začátcích můžete použít stávající předplatné vaší organizace nebo [zkušební verzi Azure](https://azure.microsoft.com/en-us/free/). Prostředí CDS bude poskytováno zdarma po omezenou dobu 30 dnů.

## <a name="subscribe"></a>Odebírat

Až bude váš [požadavek na preview](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) schválen, dostanete od společnosti Microsoft e-mailem dvě nabídky. Tyto nabídky vám umožňují nasadit Project Operations Preview:

- Dynamics 365 Project Operations – zkušební verze Preview
- Zkušební verze Preview Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Tuto úlohu musí v organizaci provést pouze jedna osoba, správce tenanta. Pokud nejste předplatitelem tohoto vydání, počkejte, dokud nebude vaše organizace zaregistrována a neobdržíte přihlašovací údaje uživatele.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – zkušební verze Preview

1. První nabídku na **zkušební verzi aplikace Dynamics 365 Project Operations** uplatněte pomocí adresy URL uvedené v uvítacím e-mailu.

![První nabídka](./media/1FirstOffer.png)

2. Ověřte, že jste přihlášeni jako uživatel patřící do organizace, která si bude předplácet službu.
3. Pokračujte v uplatnění nabídky. 
4. Vyberte položku **Ano, přidat do mého účtu**.

![Uplatnění nabídky](./media/2RedeemFirstOffer.png)

![Potvrďte nabídku](./media/3ConfirmFirstOffer.png)

![Nabídka uplatněna](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Zkušební verze Preview Dynamics 365 Finance

Stejné kroky opakujte s druhou nabídkou z uvítacího e-mailu.

## <a name="assign-licenses"></a>Přiřazení licencí

> [!IMPORTANT]
> Budete potřebovat přístup správce k portálu Office 365 vaší organizace, abyste mohli dokončit následující kroky.

1. Přejděte do [Centra pro správu Microsoft 365](https://portal.office.com/), kde přiřadíte licence vašim uživatelům.

![Portál pro správu služeb Office](./media/5OfficeAdminPortal.png)

2. Na stránce **Aktivní uživatelé** vyberte uživatele, kterým chcete přiřadit licenci.

![Přiřazení licencí](./media/6AssignLicenses.png)

3. Ověřte, že byla vybrána licence Project Operations, a vyberte příkaz **Uložit změny**. 

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

