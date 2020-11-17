---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 20, V3
description: Toto téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 20, V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073729"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="6bdb2-103">Project Service Automation, vydání aktualizace 20, V3</span><span class="sxs-lookup"><span data-stu-id="6bdb2-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="6bdb2-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6bdb2-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6bdb2-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6bdb2-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6bdb2-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6bdb2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6bdb2-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 20 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="6bdb2-110">Tato verze má číslo sestaveníV 3.10.31.37 a je obvykle k dispozici prostřednictvím automatické aktualizace v červnu 2020.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="6bdb2-111">Aktualizace verze 20</span><span class="sxs-lookup"><span data-stu-id="6bdb2-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6bdb2-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="6bdb2-112">Bug fixes</span></span>

<span data-ttu-id="6bdb2-113">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="6bdb2-113">**Project Management**</span></span>

<span data-ttu-id="6bdb2-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="6bdb2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="6bdb2-115">Import členů projektového týmu s metodou alokace, která vyžaduje hodiny, vede k nejasné chybové zprávě, když jsou zadané hodiny nula.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="6bdb2-116">Uživatelům se zobrazí nesprávná chyba při zadání maximálního počtu znaků do pole **Popis** pro projektovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="6bdb2-117">Stránka **Stažení doplňku Microsoft Dynamics 365 Project Service Automation** přesměrovává na stránku ke stažení v angličtině, když je jazyk uživatele nastavený na japonštinu.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="6bdb2-118">Pokud nastane chyba serveru, popisek synchronizace na kartě **Plán** formuláře **Projekty** někdy zůstává.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="6bdb2-119">Při změně úlohy jsou na server odesílány redundantní aktualizace úkolů.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="6bdb2-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="6bdb2-120">**Sales**</span></span>

<span data-ttu-id="6bdb2-121">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="6bdb2-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="6bdb2-122">Ve formuláři **Smlouva** dojde při dvojím kliknutí na **Vytvořit fakturu** k vytvoření dvou faktur pro jeden záznam skutečných hodnot.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="6bdb2-123">V aplikaci Internet Explorer 11 nemohou uživatelé vytvářet položky výdajů.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="6bdb2-124">Stornování nákladů a nefakturovaných prodejních skutečných hodnot není propojené.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="6bdb2-125">Tlačítko **Aktualizovat skutečné hodnoty** ve formuláři **Projekt** neaktualizuje **Skutečné hodiny úkolu**.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="6bdb2-126">Modul plug-in **PreValidateProjectTeamMemberCreate** může vytvářet duplicitní obecné rezervovatelné zdroje, když je atribut **msdyn_isgenericresourceprojectscoped** nastaven na **False**.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="6bdb2-127">Hodnota **Přepočítat** vymaže fakturovatelné náklady položek řádku založených na produktu a podrobnosti řádku smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="6bdb2-128">V konkrétních scénářích zobrazuje modul plug-in **PostEstimateLineUpdate** chybu výjimky nulového odkazu.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="6bdb2-129">Trvání časové fáze v **Grafu analýzy ziskovosti** neodpovídá době trvání nákladů v podrobnostech pevné cenové nabídky v nabídce.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="6bdb2-130">Hodnoty jednotek a skupin jednotek nejsou správně nastaveny pro kategorie výdajů ve formulářích **Detaily řádku smlouvy** a **Detaily řádku nabídky**.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="6bdb2-131">Seznamy **Nákladová cena organizační jednotky** umožňují překrývání účinnosti data.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="6bdb2-132">Uživatelé nemají dovoleno měnit hodnotu **OrgUnit** , když typ objednávky není založený na práci, protože to povede k chybě výjimky nulového odkazu.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="6bdb2-133">Když se uživatel pokusí přejít z formuláře **Detaily řádku nabídky** zpět na kartu **Nabídka** formulář se aktualizuje a zobrazí kartu **Souhrn**.</span><span class="sxs-lookup"><span data-stu-id="6bdb2-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>