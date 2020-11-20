---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 19, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126826"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="63256-103">Project Service Automation, vydání aktualizace 19, V3</span><span class="sxs-lookup"><span data-stu-id="63256-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="63256-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="63256-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="63256-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="63256-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="63256-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="63256-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="63256-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="63256-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="63256-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="63256-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="63256-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 19 pro aplikaci PSA V3.</span><span class="sxs-lookup"><span data-stu-id="63256-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="63256-110">Tato verze má číslo sestavení V3.10.30.41 a je obvykle k dispozici prostřednictvím automatické aktualizace v květnu 2020.</span><span class="sxs-lookup"><span data-stu-id="63256-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="63256-111">Aktualizace verze 19</span><span class="sxs-lookup"><span data-stu-id="63256-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="63256-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="63256-112">Bug fixes</span></span>

<span data-ttu-id="63256-113">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="63256-113">**Time and Expense**</span></span>

<span data-ttu-id="63256-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="63256-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="63256-115">Chyby odvozené z importu časových vstupů nejsou správně zviditelněny.</span><span class="sxs-lookup"><span data-stu-id="63256-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="63256-116">Mřížka pro zadání času nepodporuje chování v terénu **Pouze datum**.</span><span class="sxs-lookup"><span data-stu-id="63256-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="63256-117">Zdroje projektu nemohou vytvořit náklady s projektem.</span><span class="sxs-lookup"><span data-stu-id="63256-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="63256-118">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="63256-118">**Project Management**</span></span>

<span data-ttu-id="63256-119">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="63256-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="63256-120">Úloha na nižším stupni podřízenosti způsobuje nesprávný odhad úsilí během výpočtu dokončení (EAC).</span><span class="sxs-lookup"><span data-stu-id="63256-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="63256-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="63256-121">**Sales**</span></span>

<span data-ttu-id="63256-122">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="63256-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="63256-123">Akce **Přepočítat** nefunguje s podrobnostmi o nákladech na smlouvu nebo s podrobnostmi o nabídce.</span><span class="sxs-lookup"><span data-stu-id="63256-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="63256-124">V odhadech nákladů chybí **aktualizované ceny**.</span><span class="sxs-lookup"><span data-stu-id="63256-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="63256-125">Zákazníci si nemohou vybrat vlastní důvody stavu smlouvy ze stránky **Projektová smlouva**.</span><span class="sxs-lookup"><span data-stu-id="63256-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="63256-126">Při vytváření vlastního ceníku z nabídky dochází u zákazníků k poklesu výkonu.</span><span class="sxs-lookup"><span data-stu-id="63256-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="63256-127">Zákazníci narážejí na nekonzistenci s výchozími hodnotami **jednotka** na stránkách **Podrobnosti řádku nabídky** a **Podrobnosti řádku smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="63256-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="63256-128">Přidání položek z kategorie nefakturovatelné transakce do fakturovatelného řádku smlouvy nebude respektovat typ fakturace **Nefakturovatelné** v kategorii transakce.</span><span class="sxs-lookup"><span data-stu-id="63256-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="63256-129">Zákazníci nemohou používat nově přidané role a kategorie u dříve vytvořených smluv.</span><span class="sxs-lookup"><span data-stu-id="63256-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="63256-130">Zákazníci zažívají snížený výkon Zbytečné načítání v souboru PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="63256-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="63256-131">Role nastavené jako nefakturovatelné v seznamu **Kategorie zdrojů** by měly být přidány na kartu **Fakturovatelné role** jako **Nefakturovatelné** na řádku smlouvy pro projekt.</span><span class="sxs-lookup"><span data-stu-id="63256-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="63256-132">Zákazníci se mohou při vytváření projektu setkat se sníženým výkonem, protože **GetBookableResourceIdFromUser** načte všechny sloupce rezervovatelných zdrojů namísto pouze primárního ID.</span><span class="sxs-lookup"><span data-stu-id="63256-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="63256-133">Entita **Typ transakce** postrádá plug-in aktualizace před ověřením, aby uživatelům zabránila v zadání vlastností **Units** a **UnitGroups**, které nejsou platné pro typy transakcí.</span><span class="sxs-lookup"><span data-stu-id="63256-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="63256-134">Krok **Odebrat** krok nefunguje při importu zadání času.</span><span class="sxs-lookup"><span data-stu-id="63256-134">The **Remove** step does not work for time entry import.</span></span>
