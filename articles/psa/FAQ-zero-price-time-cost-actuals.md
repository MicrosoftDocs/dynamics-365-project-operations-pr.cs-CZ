---
title: Proč je výchozí cena skutečných časových nákladů nastavena na nulu?
description: Odstranění problému, kdy je výchozí cena skutečných časových nákladů nastavena na nulu.
author: rumant
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 1421f83458cf0aee4e70858e83d4c54179ff87e3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588222"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Proč je výchozí cena skutečných časových nákladů nastavena na nulu?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tyto často kladené dotazy se týkají skutečných položek, kdy je třída transakce nastavena na Čas a typ transakce na Náklady. Následující tři kontroly vám pomohou vyřešit, proč je cena skutečných časových nákladů nastavena na nulu.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Kontrola 1: Určete nákladový ceník pro daný projekt

Najděte projekt z oblasti aktuálních nákladu a následně přejděte na stránku projektu. Klepněte na odkaz smluvní jednotky v poli. Na stránce Smluvní jednotka zkontrolujte, zda smluvní jednotka má ceník v mřížce Nákladové ceníky.

Pokud existuje více než jeden ceník, odhalili jste problém Projektové služby podporují pouze jeden ceník na organizační jednotku. Odstraňte všechny seznamy cen z této entity, dokud nebude v mřížce Nákladové ceníky Organizační jednotky připojen pouze jeden ceník.

Pokud neexistují žádné ceníky připojené k organizační jednotce, poznamenejte si měnu organizační jednotky. Přejděte na Projektové služby, následně na Parametry a otevřete kartu Ceníky. Zkontrolujte, zda existují ceníky s kontextem nastaveným na Náklady a měnou, která se shoduje s měnou Organizační jednotky.
 
Pokud neexistují žádné ceníky, které splňují tato kritéria, odhalili jste problém. Přesvědčte se, zda máte alespoň jeden ceník, jehož kontext je nastaven na Náklady a jehož měna odpovídá měně Organizační jednotky.

Pokud existuje více ceníků, které splňují tato kritéria, pokračujte ve čtení tohoto dokumentu a proveďte další kontroly.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Kontrola 2: Jsou všechny ceníky určené výše platné pro konkrétní datum skutečného časového nákladu?

Aby bylo možné považovat daný ceník projektových služeb za ceník definující výchozí cenu, ceník by měl být platný pro datum aktuálních časových nákladů. Zkontrolujte následující položky, pokud si přejete zjistit, zda jsou výše uvedené ceníky platné:

- Zkontrolujte, zda není počáteční a koncové datum na kartě Obecné pro přiložené ceníky prázdné. Pokud je počáteční a koncové datum ve výše uvedených cenících prázdné, odhalili jste problém. 
- Poznamenejte si pole Počáteční datum vašich skutečných časových nákladů a zkontrolujte, zda jsou všechny uvedené ceníky pro toto datum platné. Například datum skutečných časových nákladů by měl spadat mezi počáteční datum a koncové datum v ceníku. 
    - Pokud pro datum skutečných časových nákladů neexistuje žádný ceník, odhalili jste problém. Upravte počáteční a koncové datum ceníku pro zajištění, že ceník zahrnuje datum skutečných časových nákladů. 
    - Pokud pro datum skutečných časových nákladů existuje více ceníků, odhalili jste problém. Můžete to vyřešit úpravou počátečních a koncových dat ceníků tak, aby pouze jeden ceník pokrýval datum skutečných časových nákladů. 
    - Pokud existuje pouze jeden ceník, který je platný pro tyto skutečné časové náklady, přesuňte se na další kontrolu v dokumentu.
Po provedení požadovaných oprav znovu vytvořte položku času, schvalte ji a ověřte, že skutečné časové náklady ukazují platnou cenu.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Kontrola 3: Je v ceníku cena pro ocenění skutečných časových nákladů?

Pokud jste úspěšně dokončili kontrolu 1 a 2, nyní byste měli mít pouze jeden ceník, který platí pro datum skutečných časových nákladů. Otevřete tento ceník a přejděte na kartu Ceny rolí. Ujistěte se, že je pro konkrétní cenové dimenze u skutečných časových nákladů řádek v mřížce.

Pokud pro konkrétní cenové dimenze u skutečných časových nákladů řádek v mřížce chybí, odhalili jste problém. Vytvořte řádek v mřížce Ceny rolí pro konkrétní cenové dimenze vašich skutečných časových nákladů. Jakmile to provedete, znovu vytvořte položku času, schvalte ji a ověřte, že skutečné časové náklady ukazují platnou cenu.
 
Pokud i přesto nevidíte platnou cenu vašich skutečných časových nákladů po provedení tří výše uvedených kontrol, odešlete prosím lístek podpory.





[!INCLUDE[footer-include](../includes/footer-banner.md)]
