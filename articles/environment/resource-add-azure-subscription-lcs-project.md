---
title: Přidání předplatného Azure do projektu LCS
description: Toto téma poskytuje informace o tom, jak připojit vaše předplatné Azure k projektu LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073651"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>Přidání předplatného Azure do projektu LCS

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Prostředí hostovaná v cloudu musí být nasazena pomocí existujícího předplatného Azure. Toto téma vysvětluje, jak připojit vaše stávající předplatné Azure k projektu LCS. 

## <a name="grant-admin-consent"></a>Udělit souhlas správce

1. Ve vašem projektu LCS v sekci **Prostředí** vyberte nastavení **Microsoft Azure**.

![Nastavení aplikace Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Na stránce **Nastavení projektu** na kartě **Konektory Azure** vyberte položku **Autorizovat**. Tato akce umožňuje nasazení prostředí do tohoto projektu.

![Konektory Azure](./media/2AzureConnectors.png)

3. Znovu vyberte položku **Autorizovat** a poskytněte tak souhlas správce.

![Udělit souhlas správce](./media/3GrantAdminConsent.png)

4. Přijměte žádost o oprávnění.

![Schválení žádosti o oprávnění](./media/4AcceptPermissionRequest.png)

Autorizace je nyní dokončena. 

![Autorizace byla úspěšná](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Poskytnutí přístupu k předplatnému Azure službám Dynamics Deployment Services

1. Přejděte do části [Fakturace Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) a vyberte své předplatné. Aby bylo možné nasadit prostředí, služby Dynamics Deployment Services vyžadují přístup k tomuto předplatnému.

![Podrobnosti předplatného Azure](./media/6AzureSubscription.png)

2. V navigačním podokně vyberte položku **Řízení přístupu (IAM)** a poté vyberte možnost **Přidat přiřazení role**.
3. V posuvníku na pravé straně vyberte možnost **Role přispěvatele** a v zobrazeném seznamu najděte a vyberte položku **Dynamics Deployment Services**. 
4. Zvolte **Uložit**.

![Přístup k předplatnému](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Přidání konektoru předplatného do projektu LCS

1. Ve vašem projektu LCS na stránce **nastavení Microsoft Azure** vyberte příkaz **Přidat** a přidejte nový konektor.
2. Zadejte ID vašeho předplatného Azure. ID předplatného Azure najdete na [portálu Azure](https://ms.portal.azure.com/) v části **Nastavení** v levém dolním rohu obrazovky.
3. V poli **Konfigurovat pro použití technologie ARM (Azure Resource Manager)** vyberte **Ano**.
4. Ujistěte se, že se doména klienta AAD předplatného Azure shoduje s předplatným Azure vlastnícím vámi používanou doménu, a vyberte položku **Další**.
5. Na obrazovce **Nastavení Microsoft Azure** potvrďte výběr tlačítkem **Další**. Pokud se na této obrazovce zobrazí chyba, vraťte se do sekce [Poskytnutí přístupu k předplatnému Azure službám Dynamics Deployment Services](#provide) v tomto tématu a ujistěte se, že jste dokončili všechny kroky.
6. Stáhněte si certifikát správy Azure do místní složky ve vašem počítači a poté jej nahrajte na Portál pro správu Azure z nabídky **Nastavení** > **Certifikáty pro správu**. Tento certifikát umožní systému LCS komunikovat s Azure vaším jménem. Tento krok můžete přeskočit, pokud má váš uživatel přístup k předplatnému.
7. Vyberte tlačítko **Další**.
8. Vyberte oblast Azure, do které chcete provést nasazení, a vyberte datové centrum, které je blízko místa, kde plánujete tento systém používat.
9.  Vyberte příkaz **Připojit**.

Úspěšně jste připojili své předplatné Azure. Nyní můžete nasadit prostředí Dynamics 365 Finance hostovaná v cloudu.


