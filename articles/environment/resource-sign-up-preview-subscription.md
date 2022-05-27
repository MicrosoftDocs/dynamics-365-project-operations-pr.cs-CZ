---
title: Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Toto téma poskytuje informace o tom, jak přihlásit odběr a nasadit Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9094b6928c5c276a40166ef5d8cb0facb539685b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575802"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_



Tento téma vysvětluje, jak se přihlásit k nabídce zkušební verze a nasadit prostředí Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě.

## <a name="prerequisites"></a>Požadavky
- Uživatel, který nasadí preview, musí mít práva globálního správce klienta Azure. Během prvního uplatnění nabídky můžete vytvořit nájemce. 
- Nasazení prostředí Finance vyžaduje platné předplatné Azure, kterému bude účtováno každé prostředí zvlášť. V začátcích můžete použít stávající předplatné vaší organizace nebo [zkušební verzi Azure](https://azure.microsoft.com/free/). Prostředí CDS bude poskytováno zdarma po omezenou dobu 30 dnů.

> [!IMPORTANT]
> Tuto úlohu musí v organizaci provést pouze jedna osoba, správce tenanta. Pokud nejste předplatitelem tohoto vydání, počkejte, dokud nebude vaše organizace zaregistrována a neobdržíte přihlašovací údaje uživatele.
> 
> Zkušební verze jsou na jedno použití v klientovi. Zkušební verzi můžete spustit pouze jednou. Pro účely zkušebního období vám doporučujeme vytvořit nového klienta.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations(CE) - zkušební verze 

Než začnete, ujistěte se, že jste přihlášeni do prohlížeče s pracovním účtem uživatele v klientu, kde chcete Project Operations Preview mít.

1. Uplatněte první nabídkový kód **Dynamics 365 Project Operations** zde [Zkušební verze Project Operations](https://aka.ms/try-po)
2. Objednávku potvrďte.

  Uvidíte, že nabídka potvrzení byla úspěšně uplatněna.

### <a name="dynamics-365-finance-preview-trial"></a>Zkušební verze Dynamics 365 Finance

Přejděte na [Zkušební verze Dynamics 365 for Finance](https://aka.ms/trypoche) a zopakujte kroky z předchozí části s nabídkou, zaregistrujte se v prostředí hostovaném v cloudu.  

## <a name="assign-licenses"></a>Přiřazení licencí

> [!IMPORTANT]
> Budete potřebovat přístup správce k portálu Microsoft 365 vaší organizace, abyste mohli dokončit následující kroky.

1. Přejděte do [centra pro správu Microsoft 365](https://portal.office.com/) a přiřaďte licence vašim uživatelům.

2. Na stránce **Aktivní uživatelé** vyberte uživatele, kterým chcete přiřadit licenci.

3. Ověřte, že byla vybrána licence **Dynamics 365 Project Operations** a vyberte **Uložit změny**.

> [!NOTE]
> Nabídku zkušební verze Finance není nutné přiřadit uživateli.

## <a name="start-a-new-project-in-lcs"></a>Zahájení nového projektu v LCS

Vytvořte nový projekt LCS podle popisu v tématu [Spuštění nového projektu v LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Přidání předplatného Azure do projektu LCS

Chcete-li dokončit tento úkol, postupujte podle pokynů v tématu [Přidání předplatného Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Nasazení ukázkového prostředí Finance spolu s Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

Postupujte podle pokynů v tématu [Zřízení nového prostředí](resource-provision-new-environment.md) a dokončete nasazení. Pro preview použijte typ nasazení [demo prostředí](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment). 

## <a name="install-cds-setup-and-configuration-data"></a>Instalace nastavení CDS a dat konfigurace

Nainstalujte instalační a konfigurační data CDS podle popisu v tématu [Nastavení a použití dat konfigurace ve službě Common Data Service](resource-apply-pro-setup-config-data.md).
Tento krok dokončete až po nasazení demo prostředí Finance a připravě demo dat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
