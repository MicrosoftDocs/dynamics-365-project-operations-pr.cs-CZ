---
title: Mezipodnikové výdaje
description: Pracovník, který je zaměstnán u jedné právnické osoby v organizaci, může vykonávat práci pro jinou právnickou osobu ve stejné organizaci. V této situaci můžete pomocí funkce mezipodnikových výdajů přiřadit výdaje pracovníka právnické osobě, pro kterou byla práce provedena.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073931"
---
# <a name="intercompany-expenses"></a>Mezipodnikové výdaje

[!include [banner](../includes/banner.md)]

Pracovník, který je zaměstnán u jedné právnické osoby v organizaci, může vykonávat práci pro jinou právnickou osobu ve stejné organizaci. V této situaci můžete pomocí funkce mezipodnikových výdajů přiřadit výdaje pracovníka právnické osobě, pro kterou byla práce provedena. Právnická osoba, která zaměstnává pracovníka, se nazývá půjčující právnická osoba. Právní osoba, za kterou vznikají náklady na pracovníka, se nazývá vypůjčující právnická osoba. 

Než může pracovník vytvořit a odeslat výdaje za práci, která je prováděna pro jinou právnickou osobu, v půjčující právnické osobě na stránce **Parametry řízení výdajů** vyberte možnost **Povolit mezipodnikové výdajové řádky**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Daňové účtování mezipodnikových nákladů

[!include [banner](../includes/banner.md)]

Pokud chcete ve své zprávě o výdajích použít daňové skupiny, které jsou přidruženy k půjčující právnické osobě (zdrojové) místo právnické osoby vypůjčující (cílové), budete to muset nakonfigurovat v nastavení daně z obratu hlavní knihy. Když je parametr hlavní knihy **Právní subjekt pro účtování mezipodnikových daní** je nastaven na **Zdrojový** a možnost **Použít pravidla pro zdanění daně z obratu** je nastavena na **Ne** , použije se daňová kombinace pro půjčující právnickou osobu. Když je stejný parametr nastaven na **Cílová** , použije se daňová kombinace pro vypůjčující právnickou osobu. U právnických osob ve Spojených státech, když je parametr nastaven na **Zdrojová** , pole **Pohledávka z prodejní dáně** musí být také nakonfigurováno na nové stránce **Skupiny účtování hlavní knihy**. Účetní nástroj použije informace z tohoto pole pro daňový účetní záznam.   
Chování je konzistentní pro výdajové řádky zaúčtované s projektem nebo bez něj.  
