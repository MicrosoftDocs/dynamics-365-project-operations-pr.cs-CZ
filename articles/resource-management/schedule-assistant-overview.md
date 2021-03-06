---
title: Přehled pomocníka plánování
description: Toto téma poskytuje informace o práci s Pomocníkem plánování při rezervaci zdrojů.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907980"
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
