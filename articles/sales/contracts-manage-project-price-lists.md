---
title: Správa projektových ceníků ve smlouvách projektů
description: Tohle téma poskytuje informace o správě projektových ceníků u projektových smluv.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ad0e260fde65cf3eb32539fbcdb7101796cb53b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600504"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Správa projektových ceníků ve smlouvách projektů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Projektové smlouvy v Dynamics 365 Project Operations jsou navrženy tak, aby podporovaly vícedenní efektivní prodejní ceníky pro smlouvy. V Project Operations existuje nová přidružená entita s názvem **Projektové ceníky**. Tato entita má vztah 1:N k projektové smlouvě.

Ceníky projektu se používají k oceňování časových, materiálových a výdajových transakcí na projektu. Pokud má smlouva jeden nebo více ceníků projektu, tyto ceníky se používají k ocenění ceny za čas, materiálu, odhadů výdajů a skutečné hodnoty u projektů, které jsou spojeny se smlouvou prostřednictvím řádku smlouvy.

Pokud ve smlouvě o projektu nejsou žádné ceníky projektu, zobrazí se varovná zpráva, že neexistují žádné ceníky projektu a vaše odhady, skutečná práce na projektu, materiál a zaznamenané náklady nebudou oceněny. Za prodejní hodnoty nebude žádná cena.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Přidružení nebo zrušení přidružení projektového ceníku k projektové smlouvě

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Vytvořte nebo přiřaďte konkrétní ceník pro odhad projektové práce, materiálu a nákladů

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

Ceník projektu lze nastavit jako výchozí ceník projektu. Toto nastavení zajišťuje, že všechny smlouvy ve vaší organizaci vždy začínají standardním ceníkem projektu pro dané cenové období.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
