---
title: Proč je výchozí cena skutečných prodejních výdajů nastavena na nulu?
description: Následující tři kontroly vám pomohou vyřešit, proč je cena skutečných prodejních výdajů nastavena na nulu.
author: rumant
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d4910d3727085a45036f3b438ecd69abc3e99836
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146295"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Proč je výchozí cena skutečných prodejních výdajů nastavena na nulu?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tyto často kladené dotazy se týkají skutečných výdajů, kde je třída transakce nastavena na Výdaje a typ transakce na Nefakturované prodeje. Následující tři kontroly vám pomohou vyřešit, proč je cena (fakturační sazba) skutečných prodejních výdajů nastavena na nulu.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Kontrola 1: Určete prodejní ceník pro daný projekt

Najděte projekt z oblasti aktuálních nákladu a přejděte na stránku projektu. Následně přejděte na kartu Prodej. V mřížce řádků smlouvy projektu klikněte na odkaz v poli Projektová smlouva. Otevře se stránka Projektová smlouva. Na stránce Projektová smlouva přejděte na kartu Ceníky projektu. Zkontrolujte, zda je zde připojený alespoň jeden ceník.

Pokud v mřížce Ceníky projektu Projektové smlouvy není připojen žádný ceník:

- Připojte ceník k mřížce Ceníky projektu. Ceníky, které je zde povoleno připojit, by měly mít kontextové pole nastaveno na Prodej a pole měny v ceníku by mělo odpovídat poli měny v položce Projektová smlouva. Po provedení požadovaných oprav znovu vytvořte položku výdajů, schvalte ji a ověřte, že nefakturované prodeje ukazují platnou cenu.
- Pokud máte v mřížce Ceníky projektu Projektové smlouvy připojen jeden nebo více ceníků, přejděte ke kontrole 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Kontrola 2: Jsou všechny ceníky výše určené platné pro konkrétní datum skutečného výdaje?

Aby bylo možné považovat daný ceník projektových služeb za ceník definující výchozí cenu, ceník by měl být platný pro datum aktuálních prodejních výdajů. Zkontrolujte následující položky, pokud si přejete zjistit, zda jsou výše uvedené ceníky platné:

- Začněte kontrolou, zda není počáteční a koncové datum na kartě Obecné pro přiložené ceníky prázdné. Pokud je počáteční a koncové datum ve výše uvedených cenících prázdné, odhalili jste problém. 
- Poznamenejte si pole Počáteční datum vašich skutečných prodejních výdajích a zkontrolujte, zda jsou všechny uvedené ceníky pro toto datum platné. Například datum skutečného výdaje by měl spadat mezi počáteční datum a koncové datum v ceníku. 
    - Pokud pro datum skutečného prodejního výdaje neexistuje žádný ceník, odhalili jste problém. Upravte počáteční a koncové datum ceníku pro zajištění, že ceník zahrnuje datum skutečného výdaje. 
    - Pokud pro datum skutečného prodejního výdaje existuje více ceníků, odhalili jste problém. Upravte počáteční a koncová data ceníků tak, aby pouze jeden ceník pokrýval datum skutečného výdaje. 
    - Pokud existuje pouze jeden ceník, který se vztahuje k tomuto datu skutečného výdaje, přesuňte se na kontrolu 3.
Po provedení požadovaných oprav znovu vytvořte položku výdajů, schvalte ji a ověřte, že nefakturované prodeje ukazují platnou cenu.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Kontrola 3: Je v platném ceníku příslušného projektu platná cena pro danou kategorii výdajů? 

Pokud jste úspěšně dokončili kontrolu 1 a 2, nyní byste měli mít pouze jeden ceník pro příslušný projekt, který platí pro datum skutečných prodejních nákladů. Otevřete ceník tohoto projektu a přejděte na kartu Kategorie cen. Ujistěte se, že je pro konkrétní kategorii výdajů u skutečného výdaje řádek v mřížce .
 
- Pokud řádek neexistuje, odhalili jste problém. Vytvořte řádek v mřížce Kategorie cen pro kategorii svého skutečného nákladu. Poté znovu vytvořte položku výdajů, schvalte ji a ověřte, že nefakturované prodeje ukazují platnou cenu. 
- Pokud pro konkrétní kategorii výdajů skutečného výdaje řádek v mřížce Kategorie cen existuje, zkontrolujte, zda obsahuje platnou cenu.

Chcete-li pochopit, co je platná cena, použijte tyto metody:

- Pokud je pole Metoda ocenění na řádku Kategorie cen nastavena na Náklady, bude jednotková sazba vašich skutečných nákladů prodeje ve výchozím nastavení brána z položky Výdaje.
- Pokud je pole Metoda ocenění v řádku Kategorie cen nastavena na Procento přirážky, zkontrolujte, zda je pole Procento nastaveno na platnou hodnotu. Jednotková sazba vašich skutečných nákladů prodeje ve výchozím nastavením používá toto procento přirážky k ceně v položce Výdaje.
- Pokud je pole Metoda ocenění v řádku Kategorie cen nastavena na Cenu za jednotku, zkontrolujte, zda je pole Cena nastaveno na platnou hodnotu. Jednotková sazba vašich skutečných nákladů prodeje bude ve výchozím nastavení přestavovat částku uvedenou v poli Cena.

Pokud není nastavení ceny pro kategorii výdajů platné, odhalili jste problém. Řešením je úprava řádku kategorie cen na platnou cenu pro kategorii výdajů podle výše uvedených pravidel. Jakmile to provedete, znovu vytvořte položku výdajů, schvalte ji a následně zkontrolujte, zda nefakturované prodeje získávají platnou cenu.

Pokud i přesto nevidíte platnou cenu vašich skutečných výdajů prodeje po provedení tří výše uvedených kontrol, odešlete lístek podpory.




[!INCLUDE[footer-include](../includes/footer-banner.md)]