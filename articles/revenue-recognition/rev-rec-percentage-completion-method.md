---
title: Projekty odhadu výnosů pevné ceny
description: Tento článek obsahuje informace o výnosech s pevnou cenou v projektech.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928378"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projekty odhadu výnosů pevné ceny 

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Když vytvoříte řádek smlouvy projektu s následujícími atributy v Dynamics 365 Project Operations v Microsoft Dataverse, systém automaticky vytvoří projekt odhadu výnosů s fixní cenou. Informace v tomto projektu jsou založeny na následujícím:

  - Metoda fakturace za pevnou cenu.
  - Přidružený projekt
  - Alespoň jeden milník definovaný na kartě **Harmonogram faktur** na stránce **Řádek projektové smlouvy**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Kontrola projektů odhadu výnosů s fixní cenou
Chcete-li zkontrolovat projekty odhadů výnosů s pevnou cenou, proveďte následující kroky:

1. V prostředí Dynamics 365 Finance přejděte na **Řízení projektů a účetnictví** > **Projekty** > **Projekty odhadu příjmů s pevnou cenou**.
2. Vyberte projekt, který chcete zobrazit, a dvakrát klikněte na ikonu **ID projektu odhadu**, chcete-li otevřít záznam a zkontrolovat podrobnosti projektu.
3. Rozbalte kartu **Projekt**. Jeden projekt uvidíte v mřížce **Vybrané projekty**. Systém toto používá jako výchozí projekt, protože se jedná o projekt přidružený k řádku smlouvy projektu. 
4. Chcete-li změnit přidružení, vyberte další projekty a přidejte je do mřížky **Vybrané projekty**. Pokud je v této mřížce vybráno více projektů, vypočítá se procento dokončení projektu a odhady výnosů společně pro všechny vybrané projekty.

  Náklady na projekt, profil výnosů, šablonu nákladů a kód období lze nastavit ručně. Pokud nejsou nastaveny ručně, výchozí hodnoty jsou během prvního výpočtu odhadu pro projekt pomocí pravidel nakonfigurovaných pro profily nákladů a výnosů projektu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]