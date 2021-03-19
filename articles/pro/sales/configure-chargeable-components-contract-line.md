---
title: Konfigurace účtovatelných součásti řádku smlouvy na základě projektu – omezená
description: Tento téma poskytuje informace o tom, jak přidat účtovatelné komponenty do řádků smlouvy v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf3f2a28fc992d6444b35d6ffa0c3f6cadcf16ea
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273910"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Konfigurace účtovatelných součásti řádku smlouvy na základě projektu – omezená

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Řádek smlouvy na základě projektu má *zahrnuté* komponenty a *účtovatelné* komponenty.

Zahrnuté komponenty jsou komponenty, které podléhají:

  - Způsob fakturace a rozdělení zákazníků
  - Nepřekročitelné limity 
  - Nastavení frekvence faktur definované na řádku smlouvy na základě projektu

Podskupinu zahrnutých komponent lze označit jako účtovatelnou pomocí pole **Typ fakturace**. Pole **Typ fakturace** je sada možností, která umožňuje následující hodnoty v kontextu řádku smlouvy:

  - Účtovatelné
  - Neúčtovatelné

Účtovatelné komponenty lze definovat na úkolech, rolích a kategoriích transakcí.

Účtovatelnost je definována na úkolech pro řádek smlouvy projektu a platí pro všechny třídy transakcí zahrnutých na řádku. Pokud je pole **Zahrnout úkoly** na řádku smlouvy prázdné nebo je nastaveno na **Celý projekt**, karta **Účtovatelné úlohy** nebude k dispozici.

Účtovatelnost definovaná pro role pro řádek smlouvy projektu se vztahuje pouze na třídu transakcí **Čas**. Pokud je pole **Zahrnout čas** na řádku smlouvy nastaveno na **Ne**, karta **Účtovatelné role** nebude k dispozici.

Účtovatelnost definovaná na kategoriích transakcí pro řádek smlouvy projektu se vztahuje pouze na třídu transakcí **Výdaj**. Pokud je pole **Zahrnout výdaje** na řádku smlouvy nastaveno na **Ne**, karta **Účtovatelné kategorie** nebude k dispozici.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Nastavení úkolu projektu jako účtovatelného nebo neúčtovatelného

Úkol projektu může být účtovatelný nebo neúčtovatelný na konkrétním řádku smlouvy, což umožňuje následující nastavení:

Pokud řádek smlouvy na základě projektu zahrnuje **Čas** a určitý úkol, **T1** je k němu přidruženo jako účtovatelné. Pokud existuje druhý řádek smlouvy, který zahrnuje **Výdaje**, můžete úkol T1 na řádku smlouvy asociovat jako neúčtovatelný. Výsledkem je, že veškerý čas zaznamenaný na úkolu je účtovatelný a všechny náklady jsou neúčtovatelné.

Typ fakturace úkolu lze nakonfigurovat na kartě **Účtovatelné úkoly** řádku smlouvy aktualizací pole **Typ fakturace** v podmřížce Úkoly řádku smlouvy. Alternativně můžete aktualizovat pole **Typ fakturace** v nastavení fakturace úkolu projektu, které zobrazuje řádky smluv přidružené k úkolu.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Nastavení role jako účtovatelné nebo neúčtovatelné

Role může být účtovatelná nebo neúčtovatelná na konkrétním řádku smlouvy.

Typ fakturace role lze nakonfigurovat na kartě **Účtovatelné role** řádku smlouvy. Chcete-li to provést, aktualizujte pole **Typ fakturace** v podmřížce **Účtovatelné role**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Nastavení kategorie transakcí jako účtovatelné nebo neúčtovatelné

Kategorie transakcí může být účtovatelná nebo neúčtovatelná na konkrétním řádku smlouvy.

Typ fakturace transakce lze nakonfigurovat na kartě **Účtovatelné kategorie** řádku smlouvy na základě projektu. Chcete-li to provést, aktualizujte pole **Typ fakturace** v podmřížce **Účtovatelné kategorie**.

### <a name="resolve-chargeability"></a>Vyřešení účtovatelnosti

Odhadovaní nebo skutečně vytvořené na čas budou považovány za účtovatelné, pouze pokud je **Čas** uveden na řádku smlouvy a pokud **Úkol** a **Role** jsou nakonfigurovány jako účtovatelné na řádku smlouvy.

Odhadované nebo skutečně vytvořené na výdaj budou považovány za účtovatelné, pouze pokud je **Výdaj** uveden na řádku smlouvy a pokud **Úloha** a **Transakce** jsou nakonfigurovány jako účtovatelné na řádku smlouvy.


| Zahrnuje čas | Zahrnuje výdaj | Zahrnuje úkoly | Role           | Kategorie       | Úloha                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Ano           | Ano              | Celý projekt | Účtovatelné     | Účtovatelné     | Skutečná fakturace na čas: **Účtovatelné** </br> Typ fakturace při skutečných výdajích: **Účtovatelné**           |
| Ano           | Ano              | Vybrané úkoly | Účtovatelné     | Účtovatelné     | Skutečná fakturace na čas: **Účtovatelné** </br> Typ fakturace při skutečných výdajích: **Účtovatelné**           |
| Ano           | Ano              | Vybrané úkoly | Neúčtovatelné | Účtovatelné     | Skutečná fakturace na čas: **Neúčtovatelné** </br> Typ fakturace při skutečných výdajích: **Účtovatelné**       |
| Ano           | Ano              | Vybrané úkoly | Účtovatelné     | Účtovatelné     | Skutečná fakturace na čas: **Neúčtovatelné** </br> Typ fakturace při skutečných výdajích: **Neúčtovatelné** |
| Ano           | Ano              | Vybrané úkoly | Neúčtovatelné | Účtovatelné     | Skutečná fakturace na čas: **Neúčtovatelné** </br> Typ fakturace při skutečných výdajích: **Neúčtovatelné** |
| Ano           | Ano              | Vybrané úkoly | Neúčtovatelné | Neúčtovatelné | Skutečná fakturace na čas: **Neúčtovatelné** </br> Typ fakturace při skutečných výdajích: **Neúčtovatelné** |
| No            | Ano              | Celý projekt | Nelze nastavit   | Účtovatelné     | Skutečná fakturace na čas: **Není k dispozici**</br>Typ fakturace při skutečných výdajích: **Účtovatelné**          |
| No            | Ano              | Celý projekt | Nelze nastavit   | Neúčtovatelné | Skutečná fakturace na čas: **Není k dispozici**</br> Typ fakturace při skutečných výdajích: **Neúčtovatelné**     |
| Ano           | No               | Celý projekt | Účtovatelné     | Nelze nastavit   | Skutečná fakturace na čas: **Účtovatelné** </br> Typ fakturace při skutečných výdajích: **Není k dispozici**        |
| Ano           | No               | Celý projekt | Neúčtovatelné | Nelze nastavit   | Skutečná fakturace na čas: **Neúčtovatelné** </br>Typ fakturace při skutečných výdajích: **Není k dispozici**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]