---
title: Deaktivace ceníků
description: Tento téma vysvětluje, jak deaktivovat nebo odstranit nepoužívané nebo staré ceníky.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001328"
---
# <a name="deactivate-price-lists"></a>Deaktivace ceníků 

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

K odebráních starých nebo nepoužívaných ceníků z Dynamics 365 Project Operations musíte provést dva kroky. 

1. Odeberte nebo odstraňte ceník z konkrétních stránek.
2. Deaktivujte nebo odstraňte ceník z aktivních ceníků na stránce **Ceníky**.

>[!IMPORTANT]
> K úplnému odstranění ceníku musíte provést oba kroky. Nestačí pouze provedení kroku 2, kterým je přímé odstranění nebo deaktivace ceníku z pohledu Aktivní ceníky. Také musíte odstranit přidružení tohoto ceníku ze všech míst uvedených v kroku 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Odstranění ceníku z konkrétních stránek
1. Chcete-li odstranit ceník z Project Operations, přejděte na následující stránky:  

      - Karta **Parametry projektu** > karta **Ceníky**
      - Stránka **Organizační jednotka** > mřížka **Ceníky**
      - Stránka **Účet** > mřížka **Ceníky projektu**
      - Stránka **Cenové nabídky projektu** > mřížka **Ceníky projektu**: To platí pro všechny aktivní nabídky projektu.
      - Stránka **Smlouvy projektu** > mřížka **Ceníky projektu**: To platí pro všechny aktivní smlouvy projektu.

 2. U každé stránky musíte vybrat ceník, který chcete odstranit, a poté vybrat **Odstranit**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Odstranění nebo deaktivace ceníku z aktivních ceníků na stránce Ceníky
 
1. Chcete-li odstranit ceník z aktivních ceníků, přejděte na **Prodej** > **Zákazníci** > **Ceníky**. 
2. Vyberte ceník, který chcete odstranit, a vyberte **Odstranit**. Pokud se na ceník odkazuje na jakékoli existující transakce, nebudete jej moci odstranit. Pokud k tomu dojde, můžete deaktivovat ceník, aby se nezobrazil v žádném zobrazení. 
3. Chcete-li deaktivovat ceník, vyberte znovu ceník a poté vyberte **Deaktivovat**.   
