---
title: Konfigurace účtovatelných součásti řádku nabídky
description: Tento téma poskytuje informace o nastavení účtovatelných a neúčtovatelných komponent na řádku nabídky založeného na projektu.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073901"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurace účtovatelných součásti řádku nabídky

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Řádek nabídky na základě projektu má koncept *zahrnutých* komponent a  *účtovatelných* komponent.

Zahrnuté součásti podléhají:

  - Způsob fakturace a rozdělení zákazníků
  - Nepřekročitelné limity 
  - Nastavení frekvence faktur definované na řádku nabídky na základě projektu

Podskupinu zahrnutých komponent lze označit jako účtovatelnou pomocí pole **Typ fakturace**. Pole **Typ fakturace** je sada možností, která umožňuje následující hodnoty v kontextu řádku nabídky:

  - Účtovatelné
  - Neúčtovatelné

Účtovatelné komponenty lze definovat na úkolech, rolích a kategoriích transakcí.

Účtovatelnost je definována na úkolech pro řádek nabídky a platí pro všechny třídy transakcí zahrnutých na řádku. Pokud je pole **Zahrnout úkoly** nastaveno na **Celý projekt** nebo ponecháno prázdné, karta **Účtovatelné úlohy** není k dispozici.

Účtovatelnost definovaná pro role pro řádek nabídky se vztahuje pouze na třídu transakcí **Čas**. Pokud je pole **Zahrnout čas** na řádku nabídky projektu nastaveno na **Ne** , karta **Účtovatelné role** není k dispozici.

Účtovatelnost definovaná na kategoriích transakcí pro řádek nabídky se vztahuje pouze na třídu transakcí **Výdaj**. Pokud je pole **Zahrnout výdaje** na řádku nabídky projektu nastaveno na **Ne** , karta **Účtovatelné kategorie** není k dispozici.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Nastavení úkolu projektu jako účtovatelného nebo neúčtovatelného

Úkol projektu může být účtovatelný nebo neúčtovatelný v kontextu konkrétního řádku nabídky podle projektu, což umožňuje následující nastavení:

Pokud řádek nabídky na základě projektu zahrnuje **Čas** a úkol **T1** , úkol je přidružen k řádku nabídky jako účtovatelný. Pokud existuje druhý řádek nabídky , který zahrnuje **Výdaje** , můžete úkol **T1** na řádku nabídky asociovat jako neúčtovatelný. Výsledkem je, že veškerý čas zaznamenaný na úkolu je účtovatelný a všechny náklady zaznamenané na úkolu jsou neúčtovatelné.

Typ fakturace úkolu lze nakonfigurovat na kartě **Účtovatelné úkoly** řádku nabídky na základě projektu aktualizací pole **Typ fakturace** v podmřížce **Úkoly řádku nabídky**. Případně můžete aktualizovat typ faktura pro úlohu projektu v poli **Typ fakturace** v podmřížce úkolu Nastavení fakturace úlohy, která zobrazuje řádky nabídky spojené s úkolem.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Nastavení role jako účtovatelné nebo neúčtovatelné

Role může být účtovatelná nebo neúčtovatelná v kontextu konkrétního řádku nabídky založeného na projektu.

Typ fakturace role lze nakonfigurovat na kartě **Účtovatelné role** řádku nabídky na základě projektu aktualizací pole **Typ fakturace** v podmřížce **Účtovatelné role**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Nastavení kategorie transakcí jako účtovatelné nebo neúčtovatelné

Kategorie transakcí může být účtovatelná nebo neúčtovatelná na konkrétním řádku nabídky.

Typ fakturace transakce lze nakonfigurovat na kartě **Účtovatelné kategorie** řádku nabídky na základě projektu aktualizací pole **Typ fakturace** v podmřížce **Účtovatelné kategorie**.

### <a name="resolve-chargeability"></a>Vyřešení účtovatelnosti
Odhadovaní nebo skutečně vytvořené na čas budou považovány za účtovatelné, pouze pokud je **Čas** uveden na řádku nabídky a pokud **Úkol** a **Role** jsou nakonfigurovány jako účtovatelné na řádku nabídky.

Odhadovaní nebo skutečně vytvořené na výdaj budou považovány za účtovatelné, pouze pokud je **Výdaj** uveden na řádku nabídky a pokud **Úloha** a **Kategorie transakce** jsou nakonfigurovány jako účtovatelné na řádku nabídky.

| Zahrnuje čas | Zahrnuje výdaj | Zahrnuté úkoly | Role | Kategorie | Úloha | Fakturace |
| --- | --- | --- | --- | --- | --- | --- |
| Ano | Ano | Celý projekt | Účtovatelné | Účtovatelné | Nelze nastavit | Skutečná fakturace na čas: Účtovatelné </br>Typ fakturace při skutečných výdajích: Účtovatelné |
| Ano | Ano | Pouze vybrané úkoly projektu | Účtovatelné | Účtovatelné | Účtovatelné | Skutečná fakturace na čas: Účtovatelné</br>Typ fakturace při skutečných výdajích: Účtovatelné |
| Ano | Ano | Pouze vybrané úkoly projektu | Neúčtovatelné | Účtovatelné | Účtovatelné | Skutečná fakturace na čas: Neúčtovatelné</br>Typ fakturace při skutečných výdajích: Účtovatelné |
| Ano | Ano | Pouze vybrané úkoly projektu | Účtovatelné | Účtovatelné | Neúčtovatelné | Skutečná fakturace na čas: Neúčtovatelné</br> Typ fakturace při skutečných výdajích: Neúčtovatelné |
| Ano | Ano | Pouze vybrané úkoly projektu | Neúčtovatelné | Účtovatelné | Neúčtovatelné | Skutečná fakturace na čas: Neúčtovatelné</br> Typ fakturace při skutečných výdajích: Neúčtovatelné |
| Ano | Ano | Pouze vybrané úkoly projektu | Neúčtovatelné | Neúčtovatelné | Účtovatelné | Skutečná fakturace na čas: Neúčtovatelné</br> Typ fakturace při skutečných výdajích: Neúčtovatelné |
| No | Ano | Celý projekt | Nelze nastavit | Účtovatelné | Nelze nastavit | Skutečná fakturace na čas: Není k dispozici </br>Typ fakturace při skutečných výdajích: Účtovatelné |
| No | Ano | Celý projekt | Nelze nastavit | Neúčtovatelné | Nelze nastavit | Skutečná fakturace na čas: Není k dispozici </br>Typ fakturace při skutečných výdajích: Neúčtovatelné |
| Ano | No | Celý projekt | Účtovatelné | Nelze nastavit | Nelze nastavit | Skutečná fakturace na čas: Účtovatelné</br>Typ fakturace při skutečných výdajích: Není k dispozici |
| Ano | No | Celý projekt | Neúčtovatelné | Nelze nastavit | Nelze nastavit | Skutečná fakturace na čas: Neúčtovatelné </br>Typ fakturace při skutečných výdajích: Není k dispozici |
