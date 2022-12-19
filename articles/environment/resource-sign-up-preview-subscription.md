---
title: Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě
description: Tento článek poskytuje informace o registraci a nasazení Project Operations u scénářů založených na zdrojích/položkách, které nejsou na skladě.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842007"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Přihlášení k odběru preview Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_



Tento článek vysvětluje, jak si registrovat zkušební nabídku a nasadit prostředí Project Operations u scénářů založených na zdrojích/položkách, které nejsou na skladě.

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

Vytvořte nový projekt LCS, jak je popsáno v článku [Zahájení nového projektu v LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Přidání předplatného Azure do projektu LCS

Chcete-li tento úkol dokončit, postupujte podle kroků v článku [Přidání předplatného Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Nasazení ukázkového prostředí Finance spolu s Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě

Nasazení dokončete podle pokynů v článku [Zřízení nového prostředí](resource-provision-new-environment.md). Pro preview použijte typ nasazení [demo prostředí](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment). 

## <a name="install-cds-setup-and-configuration-data"></a>Instalace nastavení CDS a dat konfigurace

Nainstalujte data nastavení a konfigurace CDS, jak je popsáno v článku [Nastavení a použití konfiguračních dat v Common Data Service](resource-apply-pro-setup-config-data.md).
Tento krok dokončete až po nasazení demo prostředí Finance a připravě demo dat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
