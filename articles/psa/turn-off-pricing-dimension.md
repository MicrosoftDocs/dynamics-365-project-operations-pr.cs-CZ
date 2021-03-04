---
title: Vypnutí cenové dimenze
description: Toto téma ukazuje, jak nastavit cenové dimenze v řešení Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da0ac942579ba8d9b2258a011b8eeef8e64ba9c9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147285"
---
# <a name="turn-off-a-pricing-dimension"></a>Vypnutí cenové dimenze

[!include [banner](../includes/psa-now-project-operations.md)]

Možná budete muset každých několik let zkontrolovat a aktualizovat cenovou strategii. Jakékoli aktualizace, které provedete, mohou vyžadovat, abyste vypnuli existující cenovou dimenzi a vytvořili novou. Například jste mohli dříve oceňovat podle **Role**, ale nyní jste se rozhodli oceňovat podle **Pracovních zkušeností**. To může vyžadovat vypnutí **Role** jako cenové dimenze a vytvoření **Pracovní zkušenosti** jako nové cenové dimenze. 

Vypnutí cenové dimenze bez ohledu na to, zda je pole předem připravené nebo vlastní, lze provést nastavením polí **Použitelné na náklady** a **Použitelné na prodej** cenové dimenze na **Ne**.

Pokud to však uděláte, může se zobrazit následující chybová zpráva.

![Chyba obchodního procesu při vypnutí cenové dimenze](media/Business-Process-Error.png)


Tato chybová zpráva značí, že existují cenové záznamy, které byly dříve nastaveny pro dimenzi, která je vypnuta. Všechny záznamy **Cena role** a **Přirážka ceny role**, které odkazují na dimenzi, musí být odstraněny dříve, než bude možné použitelnost dimenze nastavit na **Ne.** Toto pravidlo platí pro předem připravené i vlastní cenové dimenze, které jste vytvořili. Důvodem tohoto ověření je, že služba Project Service má omezení, podle kterého každý záznam **Cena role** musí mít jedinečnou kombinaci dimenzí. Například v ceníku s názvem **Nákladové sazby USA 2018** máte následující řádky **Cena role**. 

| Standardní název         | Organizační jednotka    |Jednotka   |Cena  |Měna  |
| -----------------------|-------------|-------|-------|----------|
| Systémový inženýr|Contoso US|Hour| 100|USD|
| Senior systémový inženýr|Contoso US|Hour| 150| USD|


Pokud jako cenovou dimenzi vypnete **Standardní název** a modul ocenění služeb Project Service vyhledává cenu, použije pouze hodnotu **Organizační jednotka** ze zadání. Pokud je **Organizační jednotka** v zadání „Contoso US“, výsledek bude nedeterministický, protože oba řádky budou shodné. Chcete-li se vyhnout tomuto scénáři, při vytváření záznamů **Cena role** služba Project Service ověří, zda je kombinace dimenzí jedinečná. Pokud je dimenze po vytvoření záznamů **Cena role** vypnutá, může být toto omezení porušeno. Proto je nutné, aby před vypnutím dimenze byly odstraněny všechny řádky **Cena role** a **Přirážka ceny role**, které mají tuto hodnotu dimenze vyplněnou.



[!INCLUDE[footer-include](../includes/footer-banner.md)]