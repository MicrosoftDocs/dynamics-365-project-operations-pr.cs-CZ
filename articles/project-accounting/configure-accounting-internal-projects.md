---
title: Konfigurace účetnictví pro interní projekty
description: Toto téma poskytuje informace o tom, jak nastavit účetní postupy za interní projekty v aplikaci Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857970"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurace účetnictví pro interní projekty

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Interní projekty umožňují společnostem sledovat náklady spojené s aktivitami, které nejsou fakturovány zákazníkovi. Mezi příklady interních projektů patří:

- Vývoj produktu, například mobilní aplikace, a sledování nákladů spojených s vývojem.
- Správa času a výdajů před prodejem. Tento interní projekt před prodejem lze později převést na zúčtovatelný projekt, pokud bude získána nabídka.

Jakýkoli projekt, který není spojen se smlouvou v Dynamics 365 Project Operations, je považováno za interní. Náklady projektu a profily výnosů se nepoužívají k určení pravidel zúčtování pro projekt. Náklady na interní projekt se vždy zaúčtují pomocí zásad zisku a ztráty. Účty hlavní knihy pro účtování jsou definovány na stránce **Nastavení účtování hlavní knihy**.

- Časové transakce se účtují odečtením z účtu **Náklady** a připsáním na účet **Přidělení mezd**.
- Výdajové transakce se účtují odečtením z účtu **Náklady** a připsáním na účet **Offsetový účet pro výdaje**.
- Transakce s položkami se zaúčtují na vrub účtu **Náklady** a odepíšou z účtu **Cena – položka**.

Pokud je projekt spojen se smlouvou o projektu, po zaúčtování transakcí do projektu, systém vrátí všechny akumulované transakce a vytvoří nové zúčtovatelné transakce. Fakturovatelné transakce se řídí účetními pravidly definovanými v příslušném profilu nákladů a výnosů projektu.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
