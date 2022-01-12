---
title: Možnosti subdodávek pro členy projektového týmu
description: Toto téma vysvětluje možnosti subdodávek pro členy projektového týmu v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903368"
---
# <a name="subcontracting-options-for-project-team-members"></a>Možnosti subdodávek pro členy projektového týmu

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V aplikaci Microsoft Dynamics 365 Project Operations můžete vyhodnotit možnosti subdodávek dostupné pro jednoho nebo více členů projektového týmu. Dostupné možnosti subdodávky vám umožňují:

- Vytvořit novou subdodávku a/nebo nové řádky na existující subdodávce pro vybrané členy projektového týmu. 
- Vytvořit rezervaci pro stávající subdodávku a řádek subdodávky. 

Můžete si vybrat z dostupných možností subdodávek pro obecné členy projektového týmu nebo si vybrat z členů projektového týmu, kteří byli personálně obsazeni pojmenovaným zdrojem, kterým je smluvní pracovník. 

Pro následující položky nejsou k dispozici žádné možnosti subdodávky:

- Členové projektového týmu, kteří byli obsazeni zaměstnancem. 
- Členové projektového týmu, kteří jsou již přidruženi k subdodávce či řádku subdodávky. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Přidělení neobsazeného člena projektového týmu k subdodávce

Chcete-li zkontrolovat a vybrat z dostupných možností subdodávek pro obecného nebo neobsazeného člena projektového týmu, postupujte takto:

1. Vyberte jeden nebo více záznamů členů projektového týmu, kde je zdrojem obecný zdroj.
2. Ujistěte se, že žádný z vybraných záznamů členů projektového týmu již není přiřazen k subdodávce. 
3. Vyberte **Možnosti subdodávek** na podmřížce členů projektového týmu. Otevře se dialogové okno **Možnosti subdodávek**: 
4. Pokud jste v kroku 1 vybrali pouze jeden záznam člena projektového týmu, budou k dispozici následující možnosti:
    - Vytvořte nové řádky subdodávky. 
    - Rezervace proti existující subdodávce – pokud jste v kroku 1 vybrali více záznamů členů projektového týmu, pak jedinou dostupnou možností je vytvoření nových řádků subdodávky.
5. Možnost rezervace proti existujícímu řádku subdodávky vám umožňuje vybrat subdodávku a řádek subdodávky, pro kterou chcete provést rezervaci. Při výběru řádku subdodávky k rezervaci kapacity byste se měli ujistit, že vybraný řádek je časový a že role požadovaná u člena projektového týmu odpovídá roli, která byla zakoupena na řádku subdodávky.
6. Když se rozhodnete vytvořit nové řádky subdodávek pro členy projektového týmu, systém vám umožní vybrat subdodávku, pro kterou chcete tyto řádky vytvořit. Subdodávka, kterou vyberete pro vytvoření nových řádků, by měla být ve stavu **Koncept**. U této možnosti pro vytvoření nových řádků subdodávky pro vybrané členy projektového týmu systém vytvoří jeden řádek subdodávky pro čas každého člena projektového týmu. Role, hodiny a data budou zkopírovány z člena projektového týmu do každého vytvořeného řádku subdodávky. 
7. Když je obecný člen týmu přidružen k subdodávce a řádku subdodávky, pole **Typ pracovníka** na řádku obecného člena týmu bude aktualizováno na **Smluvní pracovník** a **Platnost subdodávky** bude nastavena na **Platná**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Přidělení obsazeného člena projektového týmu k subdodávce

Stejně jako u obecných nebo neobsazených členů týmu můžete možnosti subdodávek také zobrazit u obsazených členů projektového týmu, pokud je obsazený člen týmu smluvním pracovníkem. Chcete-li zkontrolovat a vybrat z dostupných možností subdodávek pro obsazeného nebo pojmenovaného člena projektového týmu, postupujte takto:

1. Vyberte jeden nebo více záznamů členů projektového týmu, kde je zdrojem pojmenovaný smluvní pracovník.
2. Ujistěte se, že žádný z vybraných záznamů členů projektového týmu již není přiřazen k subdodávce. 
3. Vyberte **Možnosti subdodávek** na podmřížce členů projektového týmu. Otevře se dialogové okno **Možnosti subdodávek**: 
4. Pokud jste v kroku 1 vybrali pouze jeden záznam člena projektového týmu, budou k dispozici následující možnosti:
      - Vytvořte nové řádky subdodávky.
      - Rezervujte proti stávající subdodávce.
  Pokud jste v kroku 1 vybrali více záznamů členů projektového týmu, pak jedinou dostupnou možností je vytvoření nových řádků subdodávky.
5. Možnost rezervace proti existujícímu řádku subdodávky vám umožňuje vybrat subdodávku a řádek subdodávky, pro kterou chcete provést rezervaci. Při výběru řádku subdodávky pro rezervaci kapacity byste měli zajistit následující:
      - Vybraný řádek subdodávky je časový. 
      - Role požadovaná u člena projektového týmu odpovídá roli, která byla zakoupena na řádku subdodávky. 
      - Dodavatel, ke kterému je smluvní pracovník přidružen, je stejný jako dodavatel na subdodávce.
6. Když se rozhodnete vytvořit nové řádky subdodávek pro členy projektového týmu, systém vám umožní vybrat subdodávku, pro kterou chcete tyto řádky vytvořit. U této možnosti byste měli zajistit, aby dodavatel, ke kterému smluvní pracovník patří, byl stejný jako dodavatel na subdodávce. 
7. Subdodávka, kterou vyberete pro vytvoření nových řádků, by měla být ve stavu **Koncept**. U této možnosti pro vytvoření nových řádků subdodávky pro vybrané členy projektového týmu systém vytvoří jeden řádek subdodávky pro čas každého člena projektového týmu. Role, hodiny a data budou zkopírovány z člena projektového týmu do každého vytvořeného řádku subdodávky.  
8. Když je pojmenovaný člen týmu přidružen k subdodávce a řádku subdodávky, pole **Typ pracovníka** na řádku pojmenovaného člena týmu bude aktualizováno na **Smluvní pracovník** a **Platnost subdodávky** bude nastavena na **Platná**.

## <a name="re-costing-subcontractor-assignments"></a>Přecenění přiřazení subdodavatelů

Když je člen projektového týmu (obecný nebo pojmenovaný) připojen k řádkům subdodávky pomocí dialogu **Možnosti subdodávek**, budou všechna přiřazení k úkolům, které člen týmu má, přeceněna na základě nákupního ceníku připojeného k subdodávce. Na kartě **Odhady** na stránce **Podrobnosti projektu** vyberte příkaz **Aktualizovat ceny** a zobrazte tak aktualizované ceny a/nebo ocenění vyplývající z rozhodnutí uzavřít subdodávku.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
