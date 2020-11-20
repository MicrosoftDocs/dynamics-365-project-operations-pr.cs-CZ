---
title: Poznámky pro vývojáře ohledně schvalování
description: Tohle téma poskytuje další informace pro vývojáře o práci se schváleními.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483940"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="762b2-103">Poznámky pro vývojáře ohledně schvalování</span><span class="sxs-lookup"><span data-stu-id="762b2-103">Developer notes for Approvals</span></span>

<span data-ttu-id="762b2-104">_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_</span><span class="sxs-lookup"><span data-stu-id="762b2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="762b2-105">Řešení Dynamics 365 Project Operations obsahuje logiku ověřování, která zajišťuje správný průchod záznamů fázemi schvalování.</span><span class="sxs-lookup"><span data-stu-id="762b2-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="762b2-106">Správný průchod záznamu zajistí:</span><span class="sxs-lookup"><span data-stu-id="762b2-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="762b2-107">Všechny podpůrné řádky jsou vytvořeny v souvisejících tabulkách, jako jsou deníky a aktuální údaje.</span><span class="sxs-lookup"><span data-stu-id="762b2-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="762b2-108">Před pokračování je schvalovatel v projektu označen jako **Schvalovatel projektu**.</span><span class="sxs-lookup"><span data-stu-id="762b2-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
