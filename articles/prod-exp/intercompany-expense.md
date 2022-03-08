---
title: Mezipodnikové výdaje
description: Tento téma poskytuje informace o tom, jak pomocí mezipodnikových výdajů přiřadit výdaje pracovníka entitě, pro kterou byla práce provedena.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005063"
---
# <a name="intercompany-expenses"></a>Mezipodnikové výdaje

Pracovník, který je zaměstnán u jedné právnické osoby v organizaci, může vykonávat práci pro jinou právnickou osobu ve stejné organizaci. Pomocí mezipodnikových výdajů můžete přiřadit výdaje pracovníka entitě, pro kterou byla práce provedena. Právnická osoba, která zaměstnává pracovníka, se nazývá půjčující právnická osoba. Právní osoba, za kterou vznikají náklady na pracovníka, se nazývá vypůjčující právnická osoba. 

Než bude pracovník moci vytvářet a odesílat mezipodnikové výdaje, musíte povolit mezipodnikové výdajové řádky. V půjčující entitě na stránce **Parametry řízení výdajů** vyberte **Povolit mezipodnikové výdajové řádky**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Daňové účtování mezipodnikových nákladů

[!include [banner](../includes/banner.md)]

Než budete moci v sestavě výdajů použít daňové skupiny, které jsou přidruženy k zapůjčující (zdroj) entitě místo půjčující si (cílové) entity, musíte povolit funkci v nastavení daně z prodeje hlavního registru. Když je parametr **Právní entita pro účtování mezipodnikových daní** nastaven na **Zdroj** a **Použít pravidla pro zdanění daně z prodeje** je nastaveno na **Ne**, je použita daňová kombinace pro zapůjčující právnickou osobu. Když je stejný parametr nastaven na **Cílová**, použije se daňová kombinace pro vypůjčující právnickou osobu. U právnických osob ve Spojených státech, když je parametr nastaven na **Zdrojová**, pole **Pohledávka z prodejní dáně** musí být také nakonfigurováno na nové stránce **Skupiny účtování hlavní knihy**. Účetní nástroj použije informace z tohoto pole pro daňový účetní záznam.   
Chování je konzistentní pro výdajové řádky zaúčtované s projektem nebo bez něj.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]