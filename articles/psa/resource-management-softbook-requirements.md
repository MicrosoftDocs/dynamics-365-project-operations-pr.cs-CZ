---
title: Požadavky na předběžnou rezervaci
description: Toto téma obsahuje informace o požadavcích na předběžnou rezervaci.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 95f064e0f83d2052ac4ae9673b4fcdcd16a2574246d3320e1ed3798cd6ff062b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007003"
---
# <a name="soft-book-requirements"></a>Požadavky na předběžnou rezervaci

[!include [banner](../includes/psa-now-project-operations.md)]

Požadavek na zdroj může být rezervovaný závazně. Závazná rezervace vytvoří návrh, který spotřebovává kapacitu zdroje. Návrh je poté odeslán zpět žadateli ke schválení. Předběžná rezervace předběžně přidá zdroj do projektového týmu a má jiný stav v Plánovací vývěsce, ale nespotřebovává kapacitu zdroje. Chcete-li předběžně rezervovat zdroj z Plánovací vývěsky, nastavte pole **Stav rezervace** na **Předběžná**.

![Stav rezervace nastavený na Předběžná.](media/Resource-Management-image77.png)

Pokud je karta **Tým** v zobrazení **Pojmenovaní členové týmu**, zdroj se zde zobrazí. Předběžně rezervované hodiny jsou hlášeny ve sloupci **Předběžně rezervované hodiny**.

![Předběžně rezervované hodiny v zobrazení Pojmenovaní členové týmu.](media/Resource-Management-image78.png)

Předběžně rezervované členy týmu lze přiřadit k úkolům.

![Předběžně rezervovaný člen týmu přiřazený k úkolu.](media/Resource-Management-image79.png)

Na kartě **Vyrovnání** se u předběžně rezervovaného zdroje nezobrazují žádné rezervace, protože karta **Vyrovnání** zohledňuje pouze závazné rezervace.

![Předběžně rezervovaný zdroj bez rezervací na kartě Vyrovnání.](media/Resource-Management-image80.png)

> [!NOTE]
> Z požadavku, který vygeneroval obecný člen týmu, nelze provést předběžnou rezervaci zdroje.

V Plánovací vývěsce se pro předběžné rezervace zdrojů používá odlišné zbarvení.

![Předběžné rezervace v Plánovací vývěsce.](media/Resource-Management-image81.png)

Chcete-li změnit předběžnou rezervaci na závaznou rezervaci, klikněte v Plánovací vývěsce na předběžnou rezervaci pravým tlačítkem myši a pak vyberte **Změnit stav** \> **Závazně rezervovat** \> **Závazná**.

![Změna stavu rezervace na Závazná.](media/Resource-Management-image82.png)

Rezervace se změní a změní se stav v Plánovací vývěsce. Vzhledem k tomu, že stav je nyní **Závazná**, zdroj je zobrazen jako rezervovaný a je upravena jeho kapacita a dostupnost.

Stejný postup můžete použít ke zrušení závazné rezervace nebo předběžné rezervace z Plánovací vývěsky.

Chcete-li změnit zdroj, který je na kartě **Tým** předběžně rezervovaný na závazně rezervovaný, vyberte zdroj a pak vyberte **Potvrdit**.

![Příkaz Potvrdit.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]