---
title: Výkon návrhů projektové faktury
description: Tento článek poskytuje informace o vylepšeních výkonu u návrhů projektových faktur.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 70069778b7d4326cb23d6bb36e2c78a33da12573
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927182"
---
# <a name="project-invoice-proposal-performance"></a>Výkon návrhů projektové faktury

[!include [banner](../includes/banner.md)]

Když vytvoříte nový návrh faktury, můžete narazit na problémy s výkonem, když výrazně naroste celkový počet projektů a dílčích projektů. Ke zlepšení výkonu je k dispozici funkce, která zkracuje čas potřebný k vytvoření nového návrhu faktury za zaúčtované projektové transakce.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Povolení vylepšení výkonu návrhů projektových faktur
Chcete-li povolit funkci vylepšení výkonu návrhu projektové faktury, proveďte následující kroky.

1.  Přejděte do nabídky **Správa funkcí** > **Vše**. V seznamu funkcí vyhledejte **Vylepšení výkonu návrhu projektové faktury**.
2.  Vyberte **Povolit nyní**.
3.  Obnovte stránku prohlížeče a vytvořte nový návrh faktury.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Vypnutí vylepšení výkonu návrhů projektových faktur
Chcete-li vypnout funkci vylepšení výkonu návrhu projektové faktury, dokončete následující kroky.

1.  Přejděte do nabídky **Správa funkcí** > **Vše**. V seznamu funkcí vyhledejte **Vylepšení výkonu návrhu projektové faktury**.
2.  Vyberte **Zakázat**.
3.  Aktualizujte okno prohlížeče.

> [!NOTE]
> Jsou-li povolena pravidla fakturace, nelze použít výkon návrhu faktury.
> 
> Během dávkového procesu vytváření návrhů faktur počet dílčích úkolů rozdělí úkoly na maximální počet na základě počtu smluv s fakturovatelnými transakcemi, bez ohledu na to, co jste zadali. Například pokud zadáte **3** pro počet dílčích úkolů pro hromadné vytvoření návrhu faktury a existují pouze dvě smlouvy s fakturovatelnými transakcemi, jsou vytvořeny pouze dva dílčí úkoly.
