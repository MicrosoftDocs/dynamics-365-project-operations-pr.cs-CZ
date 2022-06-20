---
title: Přidání předplatného Azure do projektu LCS
description: Tento článek poskytuje informace o tom, jak připojit předplatné Azure k projektu LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64ee8cfa7394a08c3d588c0e8f4a73185d9496cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912140"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Přidání předplatného Azure do projektu LCS

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Prostředí hostovaná v cloudu musí být nasazena pomocí existujícího předplatného Azure. Tento článek vysvětluje, jak připojit stávající předplatné Azure k projektu LCS. 

## <a name="grant-admin-consent"></a>Udělit souhlas správce

1. Ve vašem projektu LCS v sekci **Prostředí** vyberte nastavení **Microsoft Azure**.

![Nastavení Microsoft Azure.](./media/1MicrosoftAzureSettings.png)

2. Na stránce **Nastavení projektu** na kartě **Konektory Azure** vyberte položku **Autorizovat**. Tato akce umožňuje nasazení prostředí do tohoto projektu.

![Konektory Azure.](./media/2AzureConnectors.png)

3. Znovu vyberte položku **Autorizovat** a poskytněte tak souhlas správce.

![Udělit souhlas správce.](./media/3GrantAdminConsent.png)

4. Přijměte žádost o oprávnění.

![Schválení žádosti o oprávnění.](./media/4AcceptPermissionRequest.png)

Autorizace je nyní dokončena. 

![Autorizace byla úspěšná.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Poskytnutí přístupu k předplatnému Azure službám Dynamics Deployment Services

1. Přejděte do části [Fakturace Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) a vyberte své předplatné. Aby bylo možné nasadit prostředí, služby Dynamics Deployment Services vyžadují přístup k tomuto předplatnému.

![Podrobnosti předplatného Azure.](./media/6AzureSubscription.png)

2. V navigačním podokně vyberte položku **Řízení přístupu (IAM)** a poté vyberte možnost **Přidat přiřazení role**.
3. V posuvníku na pravé straně vyberte možnost **Role přispěvatele** a v zobrazeném seznamu najděte a vyberte položku **Dynamics Deployment Services**. 
4. Zvolte **Uložit**.

![Přístup k předplatnému.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Přidání konektoru předplatného do projektu LCS

1. Ve vašem projektu LCS na stránce **nastavení Microsoft Azure** vyberte příkaz **Přidat** a přidejte nový konektor.
2. Zadejte ID vašeho předplatného Azure. ID předplatného Azure najdete na [portálu Azure](https://ms.portal.azure.com/) v části **Nastavení** v levém dolním rohu obrazovky.
3. V poli **Konfigurovat pro použití technologie ARM (Azure Resource Manager)** vyberte **Ano**.
4. Ujistěte se, že se doména klienta AAD předplatného Azure shoduje s předplatným Azure vlastnícím vámi používanou doménu, a vyberte položku **Další**.
5. Na obrazovce **Nastavení Microsoft Azure** potvrďte výběr tlačítkem **Další**. Pokud se na této obrazovce zobrazí chyba, vraťte se do sekce [Poskytnutí přístupu k předplatnému Azure službám Dynamics Deployment Services](#provide) v tomto článku a ujistěte se, že jste provedli všechny kroky.
6. Stáhněte si certifikát pro správu Azure do místní složky ve vašem počítači. Požádejte svého správce předplatného Azure o nahrání certifikátu na portál Azure Management Portal výběrem předplatného a přechodem na **Nastavení** > **Certifikáty pro správu**. Tento certifikát umožňuje LCS komunikovat s Azure vaším jménem. Tento krok můžete přeskočit, pokud má váš uživatel přístup k předplatnému.
7. Vyberte tlačítko **Další**.
8. Vyberte oblast Azure, do které chcete provést nasazení, a vyberte datové centrum, které je blízko místa, kde plánujete tento systém používat.
9.  Vyberte příkaz **Připojit**.

Úspěšně jste připojili své předplatné Azure. Nyní můžete nasadit cloudová prostředí Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
