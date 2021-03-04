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
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132370"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurace účetnictví pro interní projekty

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Interní projekty umožňují společnostem sledovat náklady spojené s aktivitami, které nejsou fakturovány zákazníkovi. Mezi příklady interních projektů patří:

- Vývoj produktu, například mobilní aplikace, a sledování nákladů spojených s vývojem.
- Správa času a výdajů před prodejem. Tento interní projekt před prodejem lze později převést na zúčtovatelný projekt, pokud bude získána nabídka.

S jakýmkoli projektem, který není spojen se smlouvou v aplikaci Dynamics 365 Project Operations, se zachází jako s interním. Náklady projektu a profily výnosů se nepoužívají k určení pravidel zúčtování pro projekt. Náklady na interní projekt se vždy zaúčtují pomocí zásad zisku a ztráty. Účty hlavní knihy pro účtování jsou definovány na stránce **Nastavení účtování hlavní knihy**.

- Časové transakce se účtují odečtením z účtu **Náklady** a připsáním na účet **Přidělení mezd**.
- Výdajové transakce se účtují odečtením z účtu **Náklady** a připsáním na účet **Offsetový účet pro výdaje**.

Pokud je projekt spojen se smlouvou o projektu, po zaúčtování transakcí do projektu, systém vrátí všechny akumulované transakce a vytvoří nové zúčtovatelné transakce. Fakturovatelné transakce se řídí účetními pravidly definovanými v příslušném profilu nákladů a výnosů projektu.




[!INCLUDE[footer-include](../includes/footer-banner.md)]