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
ms.openlocfilehash: 6e4b80b9c4b1b0f57d04079c9d2f84051b451d29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281830"
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