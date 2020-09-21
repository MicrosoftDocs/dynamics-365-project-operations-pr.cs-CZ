---
title: Co je nového v aktualizaci verze 13 pro aplikaci Project Service Automation V3
description: Tohle téma poskytuje informace o tom, co je nového v aktualizaci verze 13 pro aplikaci Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750334"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="144ef-103">Project Service Automation V3, aktualizace verze 13</span><span class="sxs-lookup"><span data-stu-id="144ef-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="144ef-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="144ef-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="144ef-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="144ef-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="144ef-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="144ef-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="144ef-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 a na stránce řešení nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="144ef-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="144ef-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="144ef-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="144ef-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 13 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="144ef-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="144ef-110">Tato verze má číslo sestavení V3.10.3.18 a je k dispozici v následujícím plánu:</span><span class="sxs-lookup"><span data-stu-id="144ef-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="144ef-111">**Obecná dostupnost (automatická aktualizace):** Listopad 2019</span><span class="sxs-lookup"><span data-stu-id="144ef-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="144ef-112">**Automatická aktualizace:** Prosinec 2019</span><span class="sxs-lookup"><span data-stu-id="144ef-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="144ef-113">Aktualizace verze 13</span><span class="sxs-lookup"><span data-stu-id="144ef-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="144ef-114">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="144ef-114">Bug fixes</span></span>

- <span data-ttu-id="144ef-115">Čas a výdaje</span><span class="sxs-lookup"><span data-stu-id="144ef-115">Time and Expense</span></span>

     - <span data-ttu-id="144ef-116">Opraveno: Funkce vyhledávání na stránce **Schválení výdajů** nefunguje při vyhledávání podle účelu výdajů.</span><span class="sxs-lookup"><span data-stu-id="144ef-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="144ef-117">Správa zdrojů</span><span class="sxs-lookup"><span data-stu-id="144ef-117">Resource Management</span></span>

     - <span data-ttu-id="144ef-118">Opraveno: Čísla odsouhlasení byla aktualizována, aby byla správně odůvodněna.</span><span class="sxs-lookup"><span data-stu-id="144ef-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="144ef-119">Opraveno: Pojmenované zdroje nelze k úkolům přiřadit pomocí karty **Plán**.</span><span class="sxs-lookup"><span data-stu-id="144ef-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="144ef-120">Správa projektů</span><span class="sxs-lookup"><span data-stu-id="144ef-120">Project Management</span></span>

     - <span data-ttu-id="144ef-121">Opraveno: Nulová referenční výjimka při přiřazování člena týmu, když pro **Typ transakce** chybí informace o nastavení pro **Jednotka** a **Výchozí skupina**.</span><span class="sxs-lookup"><span data-stu-id="144ef-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="144ef-122">Sales</span><span class="sxs-lookup"><span data-stu-id="144ef-122">Sales</span></span>

     - <span data-ttu-id="144ef-123">Opraveno: Duplicitní záznamy typu transakce vrátí chybu při vytváření záznamů cen rolí.</span><span class="sxs-lookup"><span data-stu-id="144ef-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="144ef-124">Oprava: Extra tlačítka pro **Nová příležitost**, **Nabídka**, **Řádek objednávky** a **Přidat produkt** jsou viditelné v příkazech pro Příležitosti, Nabídky, Produkty v objednávkách a dílčí mřížku Řádky na bázi projektu.</span><span class="sxs-lookup"><span data-stu-id="144ef-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


