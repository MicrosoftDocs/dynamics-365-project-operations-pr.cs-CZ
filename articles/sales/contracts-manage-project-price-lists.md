---
title: Správa projektových ceníků ve smlouvách projektů
description: Tohle téma poskytuje informace o správě projektových ceníků u projektových smluv.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 030684576e1f53d27921907b07c9e5e0c5efe612
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133305"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Správa projektových ceníků ve smlouvách projektů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Projektové smlouvy v Dynamics 365 Project Operations jsou navrženy tak, aby podporovaly vícedenní efektivní prodejní ceníky pro smlouvy. V Project Operations existuje nová přidružená entita s názvem **Projektové ceníky**. Tato entita má vztah 1:N k projektové smlouvě.

Projektové ceníky se používají k oceňování časových a výdajových transakcí na projektu. Pokud má smlouva jeden nebo více projektových ceníků, tyto ceníky se používají k ocenění odhadů času a výdajů a skutečných hodnot u projektů, které jsou přidruženy ke smlouvě prostřednictvím řádku smlouvy.

Pokud v projektové smlouvě nejsou žádné projektové ceníky, zobrazí se varovná zpráva, že neexistují žádné projektové ceníky a vaše odhady, skutečná práce na projektu a výdaje nebudou oceněny. Za prodejní hodnoty nebude žádná cena.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Přidružení nebo zrušení přidružení projektového ceníku k projektové smlouvě

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Vytvoření nebo přidružení konkrétního ceníku pro odhad projektové práce a výdajů

1. Na projektové smlouvě vyberte kartu **Projektové ceníky**.
2. V podmřížce vyberte **+ Přidat nový projektový ceník**.
3. Na posuvníku **Rychlé vytvoření** vyberte ceník. 

  Rozevírací seznam zobrazuje všechny ceníky, které mají nastaven kontext na **Prodej**, kde se měna ceníku shoduje s měnou smlouvy.
  
4. Zadejte popis přidružení projektového ceníku, vyberte **Uložit** a poté zavřete posuvník **Rychlé vytvoření**.

   Vytvoří se přidružení projektového ceníku.
   
5. Opakováním kroků 1–4 přiřaďte k projektové smlouvě více než jeden projektový ceník. Více projektových ceníků vytvářejte, pouze pokud máte u každého z přidružených projektových ceníků jiné datum platnosti.

> [!NOTE]
> Project Operations nepodporuje překrývající se data platnosti projektových ceníků. Pokud existuje více projektových ceníků pro transakci s daným datem, cena této transakce bude implicitně nastavena na nulu.

### <a name="remove-a-project-price-list-association"></a>Odebrání přidružení projektového ceníku

- Vyberte projektový ceník a poté vyberte **Odstranit projektový ceník smlouvy** v podmřížce. 

  Ceník je odstraněn z projektových ceníků smlouvy. Samotný ceník nebude smazán. Bude odstraněno pouze přidružení ke smlouvě.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Nastavení automatických výchozích projektových ceníků smlouvy

Projektový ceník lze nastavit jako výchozí seznam v projektové smlouvě. Toto nastavení může pomoci zajistit, aby všechny smlouvy ve vaší organizaci vždy začínaly standardním ceníkem pro dané cenové období.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Nastavení výchozí organizace pro projektové ceníky

1. Přejděte na **Nastavení** > **Obecné** a poté vyberte **Parametry**.
2. V seznamu **Aktivní parametry** vyberte záznam a poklepáním jej otevřete. Při poklepání se ujistěte, že neklikáte na hodnotu pole, které je hypertextovým odkazem. 
3. Na stránce **Aktivní parametry** vyberte kartu **Ceník**. Podmřížka zobrazuje seznam výchozích ceníků. Toto je seznam standardních nákladových a prodejních ceníků. Pokud zde máte ceník **Prodej** přidružen ke každé měně, ve které prodáváte, máte zajištěno, že prodejní ceník je výchozí u jakékoli smlouvy, kterou vytvoříte pro zákazníky, kteří obchodují v této měně.

### <a name="set-up-a-customer-specific-project-price-list"></a>Nastavení projektového ceníku pro konkrétního zákazníka

Pokud jste se svými zákazníky sjednali hlavní cenovou smlouvu, můžete také nastavit projektové ceníky pro konkrétního zákazníka.

1. Přejděte na **Prodej** > **Zákazníci**.
2. Ze seznamu aktivních obchodních vztahů vyberte zákazníka, pro kterého máte speciální ceník.
3. Výběrem záznamu zákazníka jej otevřete a vyberte kartu **Projektové ceníky**. Podmřížka obsahuje seznam projektových ceníků pro tohoto konkrétního zákazníka. 
4. Vytvořte zde nové přidružení ceníku, abyste měli projektový ceník pro tohoto konkrétního zákazníka.

## <a name="custom-pricing-on-a-project-contract"></a>Vlastní ceny v projektové smlouvě

Poté, co vytvoříte výchozí projektové ceníky pro konkrétního zákazníka, budou projektové smlouvy automaticky vytvořeny s těmito přidruženými projektovými ceníky. Projektové ceníky se však vždy kopírují s připojeným datem a názvem smlouvy. Manažeři obchodních vztahů a projektoví manažeři pak mohou na těchto kopiích začít provádět úpravy cen. Tyto změněné ceny se budou vztahovat pouze na tuto projektovou smlouvu.
