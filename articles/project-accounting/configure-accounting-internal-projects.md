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
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="87163-103">Konfigurace účetnictví pro interní projekty</span><span class="sxs-lookup"><span data-stu-id="87163-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="87163-104">_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_</span><span class="sxs-lookup"><span data-stu-id="87163-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="87163-105">Interní projekty umožňují společnostem sledovat náklady spojené s aktivitami, které nejsou fakturovány zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="87163-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="87163-106">Mezi příklady interních projektů patří:</span><span class="sxs-lookup"><span data-stu-id="87163-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="87163-107">Vývoj produktu, například mobilní aplikace, a sledování nákladů spojených s vývojem.</span><span class="sxs-lookup"><span data-stu-id="87163-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="87163-108">Správa času a výdajů před prodejem.</span><span class="sxs-lookup"><span data-stu-id="87163-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="87163-109">Tento interní projekt před prodejem lze později převést na zúčtovatelný projekt, pokud bude získána nabídka.</span><span class="sxs-lookup"><span data-stu-id="87163-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="87163-110">Jakýkoli projekt, který není spojen se smlouvou v Dynamics 365 Project Operations, je považováno za interní.</span><span class="sxs-lookup"><span data-stu-id="87163-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="87163-111">Náklady projektu a profily výnosů se nepoužívají k určení pravidel zúčtování pro projekt.</span><span class="sxs-lookup"><span data-stu-id="87163-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="87163-112">Náklady na interní projekt se vždy zaúčtují pomocí zásad zisku a ztráty.</span><span class="sxs-lookup"><span data-stu-id="87163-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="87163-113">Účty hlavní knihy pro účtování jsou definovány na stránce **Nastavení účtování hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="87163-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="87163-114">Časové transakce se účtují odečtením z účtu **Náklady** a připsáním na účet **Přidělení mezd**.</span><span class="sxs-lookup"><span data-stu-id="87163-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="87163-115">Výdajové transakce se účtují odečtením z účtu **Náklady** a připsáním na účet **Offsetový účet pro výdaje**.</span><span class="sxs-lookup"><span data-stu-id="87163-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="87163-116">Transakce s položkami se zaúčtují na vrub účtu **Náklady** a odepíšou z účtu **Cena – položka**.</span><span class="sxs-lookup"><span data-stu-id="87163-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="87163-117">Pokud je projekt spojen se smlouvou o projektu, po zaúčtování transakcí do projektu, systém vrátí všechny akumulované transakce a vytvoří nové zúčtovatelné transakce.</span><span class="sxs-lookup"><span data-stu-id="87163-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="87163-118">Fakturovatelné transakce se řídí účetními pravidly definovanými v příslušném profilu nákladů a výnosů projektu.</span><span class="sxs-lookup"><span data-stu-id="87163-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
