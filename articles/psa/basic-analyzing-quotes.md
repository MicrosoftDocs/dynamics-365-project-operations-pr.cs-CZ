---
title: Analýza projektových nabídek
description: Toto téma poskytuje informace o analýze projektových nabídek.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291251"
---
# <a name="analysis-of-project-quotes"></a>Analýza projektových nabídek

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analyzuje nabídky projektů za účelem odhadu ziskovosti. Analyzuje také, v jaké míře je nabídka v souladu s očekáváními zákazníka o datu dodání nebo datu dokončení a o rozpočtu.

## <a name="profitability-analysis"></a>Analýza ziskovosti

Project Service Automation analyzuje ziskovost pomocí hrubého marže a upravené hrubé marže.

- Hrubé marže se vypočítají pomocí následujícího vzorce:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Upravená hrubá marže se vypočítá pomocí následujícího vzorce:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Je-li rozdíl hrubé marže a upravené hrubé marže obrovský, je velká část práce v nabídce klasifikována jako nefakturovatelná.

## <a name="analysis-of-customer-expectations"></a>Analýza očekávání zákazníka

Pokud zadáte hodnoty do následujících polí, můžete analyzovat nabídky a generovat grafy pro očekávání zákazníka týkající se plánu a rozpočtu:

- Pole **Požadované datum dodávky** v záhlaví nabídky.
- Pole **Rozpočet zákazníka** pro každý řádek nabídky (pro řádky založené na projektu a řádky založené na produktu).

Analýza očekávání zákazníka týkající se plánu je provedena porovnáním nejpozdějšího koncového data podrobnosti řádku nabídky s požadovaným datem dodání na všech řádcích nabídky v nabídce.

Analýza očekávání zákazníka týkající se rozpočtu je provedena porovnáním součtu celkového rozpočtu zákazníka s nabízenou částkou na všech řádcích nabídky.


[!INCLUDE[footer-include](../includes/footer-banner.md)]