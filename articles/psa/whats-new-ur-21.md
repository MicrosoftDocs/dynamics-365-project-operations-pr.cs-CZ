---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 21, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 21, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073731"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="cc7d7-103">Project Service Automation, vydání aktualizace 21, V3</span><span class="sxs-lookup"><span data-stu-id="cc7d7-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="cc7d7-104">S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cc7d7-105">Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cc7d7-106">Tato verze je kompatibilní s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cc7d7-107">Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cc7d7-108">Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cc7d7-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cc7d7-109">Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 21 pro aplikaci Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="cc7d7-110">Tato verze má číslo sestaveníV 3.10.32.50 a je obvykle k dispozici prostřednictvím automatické aktualizace v červnu 2020.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="cc7d7-111">Aktualizace verze 21</span><span class="sxs-lookup"><span data-stu-id="cc7d7-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cc7d7-112">Opravy chyb</span><span class="sxs-lookup"><span data-stu-id="cc7d7-112">Bug fixes</span></span>

<span data-ttu-id="cc7d7-113">**Čas a výdaje**</span><span class="sxs-lookup"><span data-stu-id="cc7d7-113">**Time and Expense**</span></span>

<span data-ttu-id="cc7d7-114">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cc7d7-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc7d7-115">Při hostování **ovládacího prvku mřížky pro zadání času** v řídicích panelech mřížka nevyužívá celou šířku kontejneru mřížky řídicího panelu.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="cc7d7-116">Pro konkrétní časová pásma ovládací prvek mřížky **Zadání času** nezobrazuje záznamy.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="cc7d7-117">Časové záznamy, které jsou po 21:00, se zobrazují ve špatný den.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="cc7d7-118">Uživatelé nemohou odesílat výdaje, pokud kategorie výdajů **Je vyžadován příjem výdajů** nemá žádnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="cc7d7-119">**Správa zdrojů**</span><span class="sxs-lookup"><span data-stu-id="cc7d7-119">**Resource Management**</span></span>

<span data-ttu-id="cc7d7-120">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cc7d7-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc7d7-121">Neaktivní rezervace jsou zobrazeny v zobrazení **Párování**.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="cc7d7-122">Při plnění obecných prostředků chybělo ověření, aby bylo zajištěno, že existuje platný stav rezervace.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="cc7d7-123">**Správa projektů**</span><span class="sxs-lookup"><span data-stu-id="cc7d7-123">**Project Management**</span></span>

<span data-ttu-id="cc7d7-124">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cc7d7-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc7d7-125">Mřížky formuláře **Projekt** (zobrazení **Přiřazení zdroje** , **Úkol** , **Párování** , **Odhady výdajů** ) zůstávají upravitelné, i když projekt není aktivní.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-125">The **Project** form grids ( **Resource Assignment** , **Task** , **Reconciliation** view, **Expense Estimates** ) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="cc7d7-126">Duplicitní zákazníky nelze sloučit se zákazníky, kteří jsou spojeni s potvrzenými smlouvami o projektu.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="cc7d7-127">Když je přidán prostředek, který nemá platný kalendář, systém nevrací uživatelsky přehlednou chybovou zprávu.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="cc7d7-128">Tlačítko **Přidat úkol** v mřížce úlohy je povoleno, když je projekt propojen s **doplňkem aplikace Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="cc7d7-129">Úsilí nekontrolovatelně roste, když je úkol s kategorií přiřazen ke zdroji s rolí, pro niž je definována nákladová cena.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="cc7d7-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cc7d7-130">**Sales**</span></span>

<span data-ttu-id="cc7d7-131">Byla provedena následující vylepšení:</span><span class="sxs-lookup"><span data-stu-id="cc7d7-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="cc7d7-132">**Frekvence faktury** a **začátek fakturace** byly přesunuty na kartu **Plán faktur**.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="cc7d7-133">Byly vyřešeny následující problémy:</span><span class="sxs-lookup"><span data-stu-id="cc7d7-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc7d7-134">**Celková prodejní cena** je nula (0) pro **Kategorii** , přestože **Role** má celkovou prodejní cenu, která není nula.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="cc7d7-135">Zákazníci nemohou změnit hodnotu pole **Stav faktury** na **Připraveno k fakturaci** , když jiný přizpůsobený proces aktualizuje další pole.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="cc7d7-136">Tlačítko **Aktualizovat řádky faktury** může vytvořit více duplikovaných řádků, pokud je opakovaně vybráno.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="cc7d7-137">Tlačítko **Aktualizace cen** nefunguje v podmřížce **Ceny role** ve formuláři **Rychlé zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-137">The **Update Prices** button doesn't work on the **Role Prices** sub-grid in the **Quick View** form.</span></span>
- <span data-ttu-id="cc7d7-138">Logika **Řešení seznamu prodejních cen** nesprávně zpracovává časová pásma, což má za následek nesprávný výběr ceníků.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="cc7d7-139">**Celkové skutečné náklady** na projekt mohou být po schválení jednoho časového záznamu posunuty o zlomkovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="cc7d7-140">Logika **Rozlišení cen** neposkytuje uživatelsky přehlednou chybovou zprávu, pokud **Načtená RolePrice** nemá hodnoty v polích **'Primární jednotka'** a **'Cena v primární jednotce'**.</span><span class="sxs-lookup"><span data-stu-id="cc7d7-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
