---
title: Proč je výchozí cena skutečných časových prodejů nastavena na nulu?
description: Odstranění problému, kdy je výchozí cena skutečných časových prodejů nastavena na nulu.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 202ee371-2863-4bcf-918c-212d7293faa8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 04ab519955b55088d85bdf36c3a90835f70ea501
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750356"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Proč je výchozí cena skutečných časových prodejů nastavena na nulu?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tyto často kladené dotazy se týkají skutečných výdajů, kde je třída transakce nastavena na Čas a typ transakce na Nefakturované prodeje. Následující tři kontroly vám pomohou vyřešit, proč je cena (fakturační sazba) skutečných časových prodejů nastavena na nulu.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Kontrola 1: Určete prodejní ceník pro daný projekt

Najděte projekt z oblasti aktuálních nákladu a přejděte na stránku projektu. Následně přejděte na kartu Prodej a v mřížce řádků smlouvy projektu klikněte na odkaz v poli Projektová smlouva. Otevře se stránka Smlouva projektu. Na stránce Projektová smlouva přejděte na kartu Ceníky projektu. Zkontrolujte, zda je zde připojený alespoň jeden ceník. Pokud v mřížce Ceníky projektu Projektové smlouvy není připojen žádný ceník, odhalili jste problém. Připojte ceník k mřížce Ceníky projektu. Ceníky, které je zde povoleno připojit, by měly mít kontextové pole nastaveno na Prodej a pole měny v ceníku by mělo odpovídat poli měny v položce Projektová smlouva. Po provedení požadovaných oprav znovu vytvořte časovou položku, schvalte ji a ověřte, že nefakturované prodeje ukazují platnou cenu. 

Pokud máte v mřížce Ceníky projektu Projektové smlouvy připojen jeden nebo více ceníků, přejděte k následující kontrole v dokumentu.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Kontrola 2: Jsou všechny ceníky určené výše platné pro konkrétní datum skutečných časových prodejů?

Aby bylo možné považovat daný ceník projektových služeb za ceník definující výchozí cenu, ceník by měl být platný pro datum aktuálních časových prodejů. Zkontrolujte následující položky, pokud si přejete zjistit, zda jsou výše uvedené ceníky platné:
- Zkontrolujte, zda není počáteční a koncové datum na kartě Obecné pro přiložené ceníky prázdné. Pokud je počáteční a koncové datum ve výše uvedených cenících prázdné, odhalili jste problém. 
- Poznamenejte si pole Počáteční datum vašich skutečných časových prodejů a zkontrolujte, zda jsou všechny uvedené ceníky pro toto datum platné. Například datum skutečných časových prodejů by měl spadat mezi počáteční datum a koncové datum v ceníku. 
    - Pokud pro datum skutečných časových prodejů neexistuje žádný ceník, odhalili jste problém. Upravte počáteční a koncové datum ceníku pro zajištění, že ceník zahrnuje datum skutečných časových prodejů. 
    - Pokud pro datum skutečných časových prodejů existuje více ceníků, odhalili jste problém. Můžete to vyřešit úpravou počátečních a koncových dat ceníků tak, aby pouze jeden ceník pokrýval datum skutečných časových prodejů. 
    - Pokud existuje pouze jeden ceník, který se vztahuje k tomuto datu skutečných časových prodejů, přesuňte se na kontrolu 3.
Po provedení požadovaných oprav znovu vytvořte položku času, schvalte ji a ověřte, že skutečné časové prodeje ukazují platnou cenu.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Kontrola 3: Je v ceníku cena pro ocenění skutečných časových prodejů?

Pokud jste úspěšně dokončili kontrolu 1 a 2, nyní byste měli mít pouze jeden ceník, který platí pro datum skutečných časových prodejů. Otevřete tento ceník a přejděte na kartu Ceny rolí. Ujistěte se, že je pro konkrétní cenové dimenze u skutečných Časových prodejů řádek v mřížce.

Pokud pro konkrétní cenové dimenze u skutečných časových prodejů řádek v mřížce chybí, odhalili jste problém. Vytvořte řádek v mřížce Ceny rolí pro konkrétní cenové dimenze vašich skutečných časových prodejů. Jakmile to provedete, znovu vytvořte položku času, schvalte ji a ověřte, že skutečné časové prodeje ukazují platnou cenu.

Pokud i přesto nevidíte platnou cenu vašich skutečných časových prodejů po provedení tří výše uvedených kontrol, odešlete prosím lístek podpory. 

