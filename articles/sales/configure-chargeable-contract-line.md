---
title: Konfigurace účtovatelných součásti řádku smlouvy na základě projektu
description: Tento téma poskytuje informace o zahrnutých, účtovatelných a neúčtovatelných komponent na řádcích nabídky.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d6f67d5dc6b94148d437b3399229c1235c702c6a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128680"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurace účtovatelných součásti řádku smlouvy na základě projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Řádek smlouvy na základě projektu má koncept zahrnutých, účtovatelných a neúčtovatelných komponent.

Zahrnuté komponenty podléhají metodě fakturace, rozdělení zákazníků, nepřekročitelným limitům a nastavení frekvence fakturace definované na řádku smlouvy na základě projektu.

Podskupinu zahrnutých komponent lze označit jako účtovatelnou úpravou pole **Typ fakturace**.

Účtovatelné komponenty lze definovat na rolích a kategoriích transakcí.

Účtovatelnost definovaná pro role pro řádek smlouvy projektu se vztahuje pouze na třídu transakcí **Čas**. Pokud je pole **Zahrnout čas** na řádku smlouvy projektu nastaveno na **Ne**, karta **Účtovatelné role** není k dispozici.

Účtovatelnost definovaná na kategoriích transakcí pro řádek smlouvy projektu se vztahuje pouze na třídu transakcí **Výdaj**. Pokud je pole **Zahrnout výdaje** na řádku smlouvy projektu nastaveno na **Ne**, karta **Účtovatelné kategorie** není k dispozici.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Nastavení role jako účtovatelné nebo neúčtovatelné

Role může být účtovatelná nebo neúčtovatelná na konkrétním řádku smlouvy na základě projektu.

Na kartě **Účtovatelné role** řádku smlouvy založené na projektu v podmřížce **Účtovatelné role** v poli **Typ fakturace** aktualizujte typ fakturace role.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Nastavení kategorie transakcí jako účtovatelné nebo neúčtovatelné

Kategorie transakcí může být účtovatelná nebo neúčtovatelná na konkrétním řádku smlouvy na základě projektu.

Na kartě **Účtovatelné kategorie** řádku smlouvy založené na projektu v podmřížce **Účtovatelné role** v poli **Typ fakturace** aktualizujte typ fakturace transakce.

### <a name="resolve-chargeability"></a>Vyřešení účtovatelnosti

Odhadovaní nebo skutečně vytvořené na čas budou považovány za účtovatelné, pouze pokud je čas uveden na řádku smlouvy a pokud je role nakonfigurována jako účtovatelná na řádku smlouvy.

Odhadované nebo skutečně vytvořené na výdaj budou považovány za účtovatelné, pouze pokud je výdaj uveden na řádku smlouvy a pokud kategorie transakce je nakonfigurována jako účtovatelná na řádku smlouvy.

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