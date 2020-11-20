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
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="1ed5b-103">Konfigurace účetnictví pro interní projekty</span><span class="sxs-lookup"><span data-stu-id="1ed5b-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="1ed5b-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="1ed5b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1ed5b-105">Interní projekty umožňují společnostem sledovat náklady spojené s aktivitami, které nejsou fakturovány zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="1ed5b-106">Mezi příklady interních projektů patří:</span><span class="sxs-lookup"><span data-stu-id="1ed5b-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="1ed5b-107">Vývoj produktu, například mobilní aplikace, a sledování nákladů spojených s vývojem.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="1ed5b-108">Správa času a výdajů před prodejem.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="1ed5b-109">Tento interní projekt před prodejem lze později převést na zúčtovatelný projekt, pokud bude získána nabídka.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="1ed5b-110">S jakýmkoli projektem, který není spojen se smlouvou v aplikaci Dynamics 365 Project Operations, se zachází jako s interním.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="1ed5b-111">Náklady projektu a profily výnosů se nepoužívají k určení pravidel zúčtování pro projekt.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="1ed5b-112">Náklady na interní projekt se vždy zaúčtují pomocí zásad zisku a ztráty.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="1ed5b-113">Účty hlavní knihy pro účtování jsou definovány na stránce **Nastavení účtování hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="1ed5b-114">Časové transakce se účtují odečtením z účtu **Náklady** a připsáním na účet **Přidělení mezd**.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="1ed5b-115">Výdajové transakce se účtují odečtením z účtu **Náklady** a připsáním na účet **Offsetový účet pro výdaje**.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="1ed5b-116">Pokud je projekt spojen se smlouvou o projektu, po zaúčtování transakcí do projektu, systém vrátí všechny akumulované transakce a vytvoří nové zúčtovatelné transakce.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="1ed5b-117">Fakturovatelné transakce se řídí účetními pravidly definovanými v příslušném profilu nákladů a výnosů projektu.</span><span class="sxs-lookup"><span data-stu-id="1ed5b-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


