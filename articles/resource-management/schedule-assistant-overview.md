---
title: Přehled pomocníka plánování
description: Toto téma poskytuje informace o práci s Pomocníkem plánování při rezervaci zdrojů.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125620"
---
# <a name="schedule-assistant-overview"></a>Přehled pomocníka plánování

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Pomocník plánování se používá k rezervaci zdrojů na základě požadavků definovaných projektovým manažerem. Pomocník plánování se při hledání zdrojů spoléhá na parametry uvedené v požadavku na zdroj. Pomocník plánování doporučuje zdroje, které odpovídají relevantním požadavkům, jako jsou časová okna nebo potřebné dovednosti.

Poté, co jsou identifikovány vhodné zdroje, může manažer zdrojů nebo projektu rezervovat zdroj pro práci.

## <a name="prerequisites"></a>Požadavky

Pomocník plánování je součástí řešení Universal Resource Scheduling. Toto řešení je součástí a instalováno spolu s Dynamics 365 Project Operations, Dynamics 365 Field Service a Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Odpovídající požadavky a zdroje

Vygenerovaný požadavek na zdroj je založen na podrobnostech, jako jsou:

-   Charakteristiky
-   Role
-   Organizační jednotky
-   Preference zdroje
-   Průběhové křivky úsilí
-   Časové pásmo

Pomocník plánování používá tyto podrobnosti k filtrování zdrojů.

## <a name="launch-the-schedule-assistant"></a>Spuštění Pomocníka plánování

Existují dva způsoby, jak spustit Pomocníka plánování. Pokud používáte hybridní režim, můžete v mřížce členů týmu vybrat libovolného člena týmu s nesplněným požadavkem na zdroj a poté vybrat příkaz **Rezervovat**. Pokud používáte centrální režim, správce prostředků vyhledá a vybere zdroj.

## <a name="schedule-assistant-filters"></a>Filtry pomocníka plánování

Po spuštění Pomocníka plánování se podrobnosti z požadavku na zdroj zobrazí v levém podokně jako filtrované hodnoty. Správce zdrojů nebo projektový manažer může doladit výsledky úpravou filtrů podle potřeb plánování.

Podokno filtru zobrazuje možnosti související s prací, včetně:

-   Zahájení a konec práce
-   Charakteristiky
-   Role
-   Organizační jednotky
-   Společnost poskytující zdroje
-   Typy zdrojů
-   Preferované zdroje


[!INCLUDE[footer-include](../includes/footer-banner.md)]