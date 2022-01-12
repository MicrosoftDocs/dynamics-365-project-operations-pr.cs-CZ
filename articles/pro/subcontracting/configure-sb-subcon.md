---
title: Konfigurace plánovací vývěsky pro zobrazení smluvních pracovníků a kapacity subdodávky
description: Toto téma popisuje, jak konfigurovat plánovací vývěsku v Microsoft Dynamics 365 Project Operations tak, aby zobrazovala kapacitu zdrojů subdodávky při personálním zajištění požadavků na zdroje projektu.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903363"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurace plánovací vývěsky pro zobrazení smluvních pracovníků a kapacity subdodávky 

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Plánovací vývěsku v Microsoft Dynamics 365 Project Operations lze použít k vyhledávání zdrojů dvěma způsoby:

- Obecné vyhledávání zdrojů bez kontextu jakéhokoli konkrétního požadavku na zdroje založeného na projektu.
- Vyhledávání zdrojů na základě požadavku, kde požadavek projektu poskytne kontext pro navrhované zdroje.

Chcete-li upozornit plánovací vývěsku na kapacitu zdrojů subdodávky a smluvní pracovníky, musíte provést aktualizace nastavení plánovací vývěsky. Mezi tyto aktualizace patří: 
- Aktualizace nastavení plánovací vývěsky pro obecné vyhledávání zdrojů.
- Aktualizace nastavení plánovací vývěsky pro vyhledávání zdrojů na základě požadavku.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Aktualizace nastavení plánovací vývěsky pro obecné vyhledávání zdrojů
### <a name="update-filters-for-general-resource-search"></a>Aktualizace filtrů pro obecné vyhledávání zdrojů
Když hledáte zdroj, filtry dostupné na plánovací vývěsce by se měly aktualizovat, abyste mohli hledat také externí zdroje zadáním některého nebo všech z následujících údajů:
  - Typ pracovníka, zda zobrazené zdroje mají být smluvními pracovníky nebo zaměstnanci.
  - Společnost dodavatele, ke které zdroj patří.
  - Zdroje, které patří ke konkrétní subdodávce nebo řádku subdodávky.
    
### <a name="update-retrieve-resource-query"></a>Aktualizace dotazu načítajícího zdroje
Dotaz používaný k vyhledávání by měl být také aktualizován, aby používal tyto další atributy filtru. Chcete-li aktualizovat konfiguraci plánovací vývěsky pro obecné vyhledávání zdrojů, použijte následující postup:  
1. Otevřete **Nastavení plánovací vývěsky** pro konkrétní vývěsku.
2. Otevřete kartu **Obecné nastavení** a přejděte na **Další nastavení**.
3. V seznamu nastavení v této části aktualizujte **Rozložení filtru** na **Výchozí rozložení filtru pro Project Operations Lite**.
4. Aktualizujte **Dotaz na načtení zdrojů** na **Výchozí dotaz na načtení zdrojů pro Project Operations Lite**.

![Aktualizace nastavení plánovací vývěsky pro obecné vyhledávání zdrojů](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Aktualizace nastavení plánovací vývěsky pro vyhledávání zdrojů na základě požadavku
### <a name="update-filters-for-requirement-specific-resource-search"></a>Aktualizace filtrů pro vyhledávání zdrojů na základě požadavku 
Když hledáte zdroj, filtry dostupné na plánovací vývěsce by se měly aktualizovat, abyste mohli hledat také externí zdroje zadáním některého nebo všech z následujících údajů:
 - Typ pracovníka, zda zobrazené zdroje mají být smluvními pracovníky nebo zaměstnanci.
 - Společnost dodavatele, ke které zdroj patří.
 - Zdroje, které patří ke konkrétní subdodávce nebo řádku subdodávky.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Aktualizace dotazu na načtení zdroje pro vyhledávání zdrojů na základě požadavku 
Dotaz používaný k vyhledávání by měl být také aktualizován, aby používal tyto další atributy filtru. Chcete-li aktualizovat konfiguraci plánovací vývěsky pro vyhledávání zdrojů na základě požadavku, použijte následující postup:

1. Otevřete **Nastavení plánovací vývěsky** pro konkrétní vývěsku a poté výběrem položky **Otevřít výchozí nastavení** otevřete nastavení pro vyhledávání na základě požadavku.
2. Otevřete kartu **Obecné nastavení** a přejděte na **Další nastavení**.
3. V seznamu nastavení v této části aktualizujte **Rozložení filtru** na **Výchozí rozložení filtru pro Project Operations Lite**.
4. Aktualizujte **Dotaz na načtení zdrojů** na **Výchozí dotaz na načtení zdrojů pro Project Operations Lite**.
5. Otevřete kartu **Typy plánu** a přejděte na **Projekt**.
6. V nastavení **Projektu** aktualizujte **Dotaz na načtení zdrojů pomocníka plánování** na **Výchozí dotaz na načtení zdrojů pro Project Operations Lite** a aktualizujte **Dotaz na načtení omezení pomocníka plánování** na **Výchozí dotaz na načtení omezení pro Project Operations Lite**.

![Aktualizace nastavení plánovací vývěsky pro vyhledávání zdrojů na základě požadavku](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
