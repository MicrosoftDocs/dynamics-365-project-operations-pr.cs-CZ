---
title: Projekty odhadu výnosů pevné ceny
description: Toto téma obsahuje informace o výnosech s fixní cenou v projektech.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278905"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projekty odhadu výnosů pevné ceny 

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Když vytvoříte řádek smlouvy projektu s následujícími atributy v Dynamics 365 Project Operations v Microsoft Dataverse, systém automaticky vytvoří projekt odhadu výnosů s fixní cenou. Informace v tomto projektu jsou založeny na následujícím:

  - Metoda fakturace za pevnou cenu.
  - Přidružený projekt
  - Alespoň jeden milník definovaný na kartě **Harmonogram faktur** na stránce **Řádek projektové smlouvy**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Kontrola projektů odhadu výnosů s fixní cenou
Chcete-li zkontrolovat projekty odhadů výnosů s pevnou cenou, proveďte následující kroky:

1. V prostředí Dynamics 365 Finance přejděte na **Řízení projektů a účetnictví** > **Projekty** > **Projekty odhadu výnosů s fixní cenou**.
2. Vyberte projekt, který chcete zobrazit, a dvakrát klikněte na ikonu **ID projektu odhadu**, chcete-li otevřít záznam a zkontrolovat podrobnosti projektu.
3. Rozbalte kartu **Projekt**. Jeden projekt uvidíte v mřížce **Vybrané projekty**. Systém toto používá jako výchozí projekt, protože se jedná o projekt přidružený k řádku smlouvy projektu. 
4. Chcete-li změnit přidružení, vyberte další projekty a přidejte je do mřížky **Vybrané projekty**. Pokud je v této mřížce vybráno více projektů, vypočítá se procento dokončení projektu a odhady výnosů společně pro všechny vybrané projekty.

  Náklady na projekt, profil výnosů, šablonu nákladů a kód období lze nastavit ručně. Pokud nejsou nastaveny ručně, výchozí hodnoty jsou během prvního výpočtu odhadu pro projekt pomocí pravidel nakonfigurovaných pro profily nákladů a výnosů projektu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]