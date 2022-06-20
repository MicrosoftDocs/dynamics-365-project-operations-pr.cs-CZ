---
title: Konfigurace účtovatelných součásti řádku nabídky na základě projektu
description: Tento článek poskytuje informace o nastavení zahrnutých, účtovatelných a neúčtovatelných komponent na řádcích projektové nabídky.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff409132ef9103641578f9c94f8ea1ff56738a71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915544"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Konfigurace účtovatelných součásti řádku nabídky na základě projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Řádek nabídky založený na projektu může obsahovat komponenty a zpoplatněné komponenty.

Zahrnuté komponenty podléhají metodě fakturace, rozdělení zákazníků, nepřekračovatelným limitům a nastavení frekvence fakturace definované na řádku nabídky na základě projektu.
Podmnožinu zahrnutých komponent lze označit jako zpoplatněnou pomocí **Typu fakturace**. V poli **Typ fakturace** můžete vybrat jednu z následujících možností pole v kontextu nabídky:

   - Účtovatelné
   - Neúčtovatelné

Účtovatelné komponenty lze definovat na rolích a kategoriích transakcí.

Účtovatelnost, která je definována na rolích pro řádek nabídky projektu, se vztahuje pouze na třídu transakcí **Čas**. Pokud má řádek nabídky projektu **Zahrnout čas** = **Ne**, karta **Účtovatelné role** není k dispozici.

Účtovatelnost, která je definována v kategoriích transakcí pro řádek nabídky projektu, se vztahuje pouze na třídu transakcí **Výdaj**. Pokud má řádek nabídky projektu **Zahrnout výdaje** = **Ne**, karta **Účtovatelné kategorie** není k dispozici.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Nastavení role jako účtovatelné nebo neúčtovatelné
Role může být účtovatelná nebo neúčtovatelna na řádku nabídky na základě projektu. Typ fakturace pro roli lze nakonfigurovat na kartě **Účtovatelné role** řádku nabídky na základě projektu. Chcete-li to provést, aktualizujte **Typ fakturace** v podmřížce **Účtovatelné role**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Nastavení kategorie transakcí jako účtovatelné nebo neúčtovatelné
Kategorie transakcí může být účtovatelná nebo neúčtovatelna na řádku nabídky na základě projektu. Typ fakturace pro transakci lze nakonfigurovat na kartě **Účtovatelné kategorie** řádku nabídky na základě projektu. Chcete-li to provést, aktualizujte pole **Typ fakturace** v podmřížce **Účtovatelné kategorie**. 

## <a name="resolve-chargeability"></a>Vyřešení účtovatelnosti

Odhad nebo skutečný čas vytvořený bude považován za účtovatelný, pouze pokud je čas uveden na řádku nabídky a pokud je role nakonfigurována jako účtovatelná.
Odhad nebo skutečná hodnota vytvořená pro výdaj bude považován za účtovatelnou, pouze pokud je výdaj uveden na řádku nabídky a pokud je kategorie transakcí nakonfigurována jako účtovatelná na řádku nabídky. Následující tabulka ukazuje, jak je výchozí hodnota zúčtování u každé skutečné hodnoty. Výchozí hodnoty jsou založeny na zahrnutých součástech a typu fakturace, který je nastaven na řádku nabídky.

| Zahrnuje čas | Zahrnuje výdaj | Role | Kategorie | Úloha |
| --- | --- | --- | --- | --- |
| Ano | Ano | Účtovatelné | Účtovatelné | Skutečná fakturace na čas: Účtovatelné </br>Typ fakturace při skutečných výdajích: Účtovatelné |
| Ano | Ano | Neúčtovatelné | Účtovatelné | Skutečná fakturace na čas: Neúčtovatelné </br>Typ fakturace při skutečných výdajích: Účtovatelné |
| Ano | Ano | Neúčtovatelné | Neúčtovatelné | Skutečná fakturace na čas: Neúčtovatelné </br>Typ fakturace při skutečných výdajích: Neúčtovatelné |
| No | Ano | Nelze nastavit | Účtovatelné | Skutečná fakturace na čas: Není k dispozici </br>Typ fakturace při skutečných výdajích: Účtovatelné |
| No | Ano | Nelze nastavit | Neúčtovatelné | Skutečná fakturace na čas: Není k dispozici </br>Typ fakturace při skutečných výdajích: Neúčtovatelné |
| Ano | No | Účtovatelné | Nelze nastavit | Skutečná fakturace na čas: Účtovatelné </br>Typ fakturace při skutečných výdajích: Není k dispozici |
| Ano | No | Neúčtovatelné | Nelze nastavit | Skutečná fakturace na čas: Neúčtovatelné </br> Typ fakturace při skutečných výdajích: Není k dispozici |


[!INCLUDE[footer-include](../includes/footer-banner.md)]