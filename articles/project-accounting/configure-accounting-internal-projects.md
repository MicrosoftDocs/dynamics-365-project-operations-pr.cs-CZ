---
title: Konfigurace účetnictví pro interní projekty
description: Toto téma poskytuje informace o tom, jak nastavit účetní postupy za interní projekty v aplikaci Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073714"
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


