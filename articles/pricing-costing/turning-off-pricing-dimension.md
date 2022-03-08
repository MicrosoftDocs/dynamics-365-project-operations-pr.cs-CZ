---
title: Vypnutí cenové dimenze
description: Toto téma obsahuje informace o tom, jak vypnout cenové dimenze.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d9f0cb2a054941b07809b61ca14a3145c6d6d06acd6ca40255d5ec9de92be22
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994493"
---
# <a name="turning-off-a-pricing-dimension"></a>Vypnutí cenové dimenze

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Možná budete muset každých několik let zkontrolovat a aktualizovat cenovou strategii. Jakékoli aktualizace, které provedete, mohou vyžadovat, abyste vypnuli existující cenovou dimenzi a vytvořili novou. Například jste mohli dříve oceňovat podle **Role**, ale nyní jste se rozhodli oceňovat podle **Pracovních zkušeností**. To může vyžadovat vypnutí **Role** jako cenové dimenze a vytvoření **Pracovní zkušenosti** jako nové cenové dimenze. 

Vypnutí cenové dimenze bez ohledu na to, zda je pole předem připravené nebo vlastní, lze provést nastavením polí **Použitelné na náklady** a **Použitelné na prodej** cenové dimenze na **Ne**.

Když to však uděláte, může se zobrazit chybová zpráva **Cenovou dimenzi nelze aktualizovat ani odstranit, pokud existují přidružené cenové záznamy.**

![Chyba obchodního procesu při vypnutí cenové dimenze.](media/Business-Process-Error.png)

Tato chybová zpráva značí, že existují cenové záznamy, které byly dříve nastaveny pro dimenzi, která je vypnuta. Všechny záznamy **Cena role** a **Přirážka ceny role**, které odkazují na dimenzi, musí být odstraněny dříve, než bude možné použitelnost dimenze nastavit na **Ne.** Toto pravidlo platí pro předem připravené i vlastní cenové dimenze, které jste vytvořili. Důvodem tohoto ověření je, že záznam **Cena role** musí mít jedinečnou kombinaci dimenzí. Například v ceníku s názvem **Nákladové sazby USA 2018** máte následující řádky **Cena role**. 

| Standardní funkce         | Organizační jednotka    |Jednotka   |Cena  |Měna  |
| -----------------------|-------------|-------|-------|----------|
| Systémový inženýr|Contoso (USA)|hod| 100|USD|
| Senior systémový inženýr|Contoso (USA)|hod| 150| USD|


Pokud jako cenovou dimenzi vypnete **Standardní název** a modul ocenění vyhledává cenu, použije pouze hodnotu **Organizační jednotka** ze zadání. Pokud je **Organizační jednotka** v zadání „Contoso US“, výsledek bude nedeterministický, protože oba řádky budou shodné. Chcete-li se vyhnout tomuto scénáři, při vytváření záznamů **Cena role** systém ověří, zda je kombinace dimenzí jedinečná. Pokud je dimenze po vytvoření záznamů **Cena role** vypnutá, může být toto omezení porušeno. Proto je nutné, aby před vypnutím dimenze byly odstraněny všechny řádky **Cena role** a **Přirážka ceny role**, které mají tuto hodnotu dimenze vyplněnou.


[!INCLUDE[footer-include](../includes/footer-banner.md)]