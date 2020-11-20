---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 13, V3
description: Tohle téma poskytuje informace o tom, co je nového v aktualizaci verze 13 pro aplikaci Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bcb05b640966e760a7a74a306a3f0a39594baed8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121615"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="5dbc0-103">Project Service Automation, vydání aktualizace 13, V3</span><span class="sxs-lookup"><span data-stu-id="5dbc0-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="5dbc0-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="5dbc0-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="5dbc0-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="5dbc0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5dbc0-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5dbc0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5dbc0-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="5dbc0-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="5dbc0-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5dbc0-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5dbc0-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 13 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="5dbc0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="5dbc0-110">Tato verze má číslo sestavení V3.10.3.18 a je k dispozici v následujícím plánu:</span><span class="sxs-lookup"><span data-stu-id="5dbc0-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="5dbc0-111">**Obecná dostupnost (automatická aktualizace):** Listopad 2019</span><span class="sxs-lookup"><span data-stu-id="5dbc0-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="5dbc0-112">**Automatická aktualizace:** Prosinec 2019</span><span class="sxs-lookup"><span data-stu-id="5dbc0-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="5dbc0-113">Aktualizace verze 13</span><span class="sxs-lookup"><span data-stu-id="5dbc0-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="5dbc0-114">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="5dbc0-114">Bug fixes</span></span>

- <span data-ttu-id="5dbc0-115">Čas a výdaje</span><span class="sxs-lookup"><span data-stu-id="5dbc0-115">Time and Expense</span></span>

     - <span data-ttu-id="5dbc0-116">Opraveno: Funkce vyhledávání na stránce **Schválení výdajů** nefunguje při vyhledávání podle účelu výdajů.</span><span class="sxs-lookup"><span data-stu-id="5dbc0-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="5dbc0-117">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="5dbc0-117">Resource Management</span></span>

     - <span data-ttu-id="5dbc0-118">Opraveno: Čísla odsouhlasení byla aktualizována, aby byla správně odůvodněna.</span><span class="sxs-lookup"><span data-stu-id="5dbc0-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="5dbc0-119">Opraveno: Pojmenované zdroje nelze k úkolům přiřadit pomocí karty **Plán**.</span><span class="sxs-lookup"><span data-stu-id="5dbc0-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="5dbc0-120">Správa projektů</span><span class="sxs-lookup"><span data-stu-id="5dbc0-120">Project Management</span></span>

     - <span data-ttu-id="5dbc0-121">Opraveno: Nulová referenční výjimka při přiřazování člena týmu, když pro **Typ transakce** chybí informace o nastavení pro **Jednotka** a **Výchozí skupina**.</span><span class="sxs-lookup"><span data-stu-id="5dbc0-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="5dbc0-122">Sales</span><span class="sxs-lookup"><span data-stu-id="5dbc0-122">Sales</span></span>

     - <span data-ttu-id="5dbc0-123">Opraveno: Duplicitní záznamy typu transakce vrátí chybu při vytváření záznamů cen rolí.</span><span class="sxs-lookup"><span data-stu-id="5dbc0-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="5dbc0-124">Opraveno: Dodatečná tlačítka pro **Nová příležitost**, **Nabídka**, **Řádek objednávky** a **Přidat produkt** jsou viditelné v příkazech pro Příležitosti, Nabídky, Produkty v objednávkách a podmřížku Řádky na základě projektu.</span><span class="sxs-lookup"><span data-stu-id="5dbc0-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


