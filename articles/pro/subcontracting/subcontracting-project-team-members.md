---
title: Přidělování členů projektového týmu k subdodávkám
description: Tento článek vysvětluje, jak přidělit členy projektového týmu v Microsoft Dynamics 365 Project Operations k subdodávkám.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522787"
---
# <a name="subcontracting-project-team-members"></a>Přidělování členů projektového týmu k subdodávkám

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V Microsoft Dynamics 365 Project Operations můžete přidělit personálně obsazené či neobsazené členy projektového týmu k subdodávkám.

- Neobsazení členové projektového týmu mají přiřazený obecný zdroj.
- Obsazení členové týmu mají přiřazený pojmenovaný zdroj.

Když propojíte člena projektového týmu s řádkem subdodávky, všechna přiřazení k úkolům, které člen týmu má, budou přeúčtována na základě nákupního ceníku připojeného k subdodávce.  Na kartě **Odhady** na stránce **Podrobnosti projektu** vyberte příkaz **Aktualizovat ceny** a zobrazte tak aktualizované ceny a/nebo ocenění vyplývající z rozhodnutí uzavřít subdodávku. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Přidělení neobsazeného člena projektového týmu k subdodávce
Stránka **Podrobnosti člena týmu** obsahuje pole subdodávky a řádku subdodávky, která umožňují projektovému manažerovi vyjádřit, jak by chtěl čerpat požadovanou kapacitu ze subdodávky. Chcete-li přidělit člena projektového týmu k subdodávce jako obecný zdroj, postupujte takto:

1.  Vyberte subdodávku na stránce **Podrobnosti člena týmu**.

2.  Můžete vybrat pouze subdodávky se stavem **Koncept** nebo **Potvrzeno**. **Zavřené** nebo **Zrušené** subdodávky nelze vybrat. 

3.  Pole **Řádek subdodávky** se zobrazí po výběru subdodávky.

4.  V poli **Řádek subdodávky** můžete vybrat pouze časové řádky subdodávek. Nemůžete vybrat řádky subdodávek pro výdaje nebo materiál.

5.  Role pro záznam člena projektového týmu musí odpovídat roli na řádku subdodávky. Tím je zajištěno, že čas pro roli, která se odhaduje na projektu, je stejný jako u role, která je zakoupena na řádku subdodávky. 

Když je obecný člen týmu přidružen k subdodávce a řádku subdodávky, pole **Typ pracovníka** na řádku obecného člena týmu bude aktualizováno na **Smluvní pracovník** a **Platnost subdodávky** bude nastavena na **Platná**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Přidělení obsazeného člena projektového týmu k subdodávce
Stejně jako u obecných nebo neobsazených členů týmu může být kapacita obsazeného člena týmu potřebná pro projekt také propojena se subdodávkou. Chcete-li přidělit pojmenovaného člena projektového týmu k subdodávce, postupujte takto:

1.  Ujistěte se, že je pojmenovaný zdroj nastaven jako typ smluvního pracovníka rezervovatelného zdroje. Také se ujistěte, že pole **Dodavatel** u rezervovatelného zdroje odpovídá dodavateli na subdodávce, kterou vybíráte. 

2.  Můžete vybrat pouze subdodávky se stavem **Koncept** nebo **Potvrzeno**. **Zavřené** nebo **Zrušené** subdodávky nelze vybrat. 

3.  Pole **Řádek subdodávky** se zobrazí po výběru subdodávky.

4.  V poli **Řádek subdodávky** můžete vybrat pouze časové řádky subdodávek. Nemůžete vybrat řádky subdodávek pro výdaje nebo materiál.

5.  Role pro záznam člena projektového týmu musí odpovídat roli na řádku subdodávky. Tím je zajištěno, že čas pro roli, která se odhaduje na projektu, je stejný jako u role, která je zakoupena na řádku subdodávky. 

Pojmenovaní členové projektového týmu, kteří jsou nastaveni jako typ smluvního pracovníka v poli **Rezervovatelný zdroj**, se zobrazí se stavem platnosti subdodávky **Neplatná** pokud nejsou propojeni se subdodávkou. Když je pojmenovaný člen projektového týmu přidružen k subdodávce a řádku subdodávky, pole **Typ pracovníka** na řádku obecného člena týmu bude aktualizováno na **Smluvní pracovník** a **Platnost subdodávky** bude nastavena na **Platná**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
