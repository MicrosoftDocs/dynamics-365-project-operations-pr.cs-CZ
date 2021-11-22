---
title: Odinstalace produktu Dynamics 365 Project Operations
description: Toto téma obsahuje informace o odebrání instalace Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783635"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Odinstalace produktu Dynamics 365 Project Operations 

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Chcete-li odinstalovat aplikaci Dynamics 365 Project Operations, musíte mít přidělenou roli administrátora.

1. Přejděte na **Nastavení** > **Řešení**.

    ![Stránka Nastavení.](./media/uninstall-proj-ops-solutions.png)
  
2. Odeberte řešení v přesném pořadí, v jakém jsou uvedena v následující tabulce. 

    | krok | Název   řešení                                    | Poznámka                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 0 | msdyn_ProjectServiceUpgrade_managed.cab            | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 2 | ProjectOperations_Anchor                           | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 5 | ProjectService                                     | Žádné další poznámky.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Žádné další poznámky.                                                                         |
    | 7 | ProjectServiceCore                                 | Žádné další poznámky.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 9 | FieldServiceCommon                                 | Vyžadováno pro duální zápis v Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Vyžadováno pro duální zápis v Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Požadováno pro Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Požadováno pro Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Požadováno pro Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Požadováno pro Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Požadováno pro Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Požadováno pro Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Požadováno pro Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 19 | Dynamics365Notes                                   | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 21 | DualWriteCore                                      | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 23 | Dynamics365AssetManagement                         | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 26 | HCMCommon                                          | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 28 | Strana                                              | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 29 | Dynamics365Company                                 | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 30 | CurrencyExchangeRates                              | Pokud není nalezeno, toto řešení přeskočte.                                                            |
    | 31 | AssetCommon                                        | Pokud není nalezeno, toto řešení přeskočte.                                                            |