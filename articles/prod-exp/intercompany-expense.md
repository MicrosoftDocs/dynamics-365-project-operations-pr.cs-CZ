---
title: Mezipodnikové výdaje
description: Tento článek poskytuje informace o tom, jak použít mezipodnikové výdaje k přiřazení výdajů pracovníka k právnické osobě, pro kterou byla práce provedena.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c58fb1510c9ba75bc81a4dc07b91f1b6a60355d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932380"
---
# <a name="intercompany-expenses"></a>Mezipodnikové výdaje

Pracovník, který je zaměstnán u jedné právnické osoby v organizaci, může vykonávat práci pro jinou právnickou osobu ve stejné organizaci. Pomocí mezipodnikových výdajů můžete přiřadit výdaje pracovníka entitě, pro kterou byla práce provedena. Právnická osoba, která zaměstnává pracovníka, se nazývá půjčující právnická osoba. Právní osoba, za kterou vznikají náklady na pracovníka, se nazývá vypůjčující právnická osoba. 

Než bude pracovník moci vytvářet a odesílat mezipodnikové výdaje, musíte povolit mezipodnikové výdajové řádky. V půjčující entitě na stránce **Parametry řízení výdajů** vyberte **Povolit mezipodnikové výdajové řádky**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Daňové účtování mezipodnikových nákladů

[!include [banner](../includes/banner.md)]

Než budete moci v sestavě výdajů použít daňové skupiny, které jsou přidruženy k zapůjčující (zdroj) entitě místo půjčující si (cílové) entity, musíte povolit funkci v nastavení daně z prodeje hlavního registru. Když je parametr **Právní entita pro účtování mezipodnikových daní** nastaven na **Zdroj** a **Použít pravidla pro zdanění daně z prodeje** je nastaveno na **Ne**, je použita daňová kombinace pro zapůjčující právnickou osobu. Když je stejný parametr nastaven na **Cílová**, použije se daňová kombinace pro vypůjčující právnickou osobu. U právnických osob ve Spojených státech, když je parametr nastaven na **Zdrojová**, pole **Pohledávka z prodejní dáně** musí být také nakonfigurováno na nové stránce **Skupiny účtování hlavní knihy**. Účetní nástroj použije informace z tohoto pole pro daňový účetní záznam.   
Chování je konzistentní pro výdajové řádky zaúčtované s projektem nebo bez něj.  

## <a name="new-expense-expression-builder"></a>Nový nástroj pro tvorbu výrazů výdajů

Nový tvůrce výrazů výdajů řeší problémy se scénáři mezipodnikových výdajů, které používají projekty. Tato funkce zajišťuje, že když vytvoříte mezipodnikové výdaje, budou zásady výdajů správně ověřeny proti projektu, který je vybrán na řádku výdajů, a že lze úspěšně odeslat sestavu výdajů.

Aby funkce tvůrce výrazů výdajů fungovala, musí být zapnutá. Kromě toho by měly být nastaveny zásady výdajů, které mají ID projektu.

Pokud jste již nakonfigurovali zásady, které ověřují ID projektu na řádku výdajů, musí být tyto zásady vyřazeny. Poté můžete funkci zapnout a překonfigurovat zásady.

Chcete-li tuto funkci zapnout, postupujte podle následujících kroků.

1. Přejděte na **Pracovní prostory** \> **Správa funkcí**.
2. V seznamu vyberte **Nový tvůrce výrazů výdajů řeší problémy se scénáři mezipodnikových výdajů, které používají projekty**. Poté vyberte **Povolit hned**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
