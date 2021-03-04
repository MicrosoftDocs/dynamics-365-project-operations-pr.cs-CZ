---
title: Správa příležitostí založených na projektech
description: Toto téma poskytuje informace o tom, jak pracovat s příležitostmi, které souvisejí s projekty.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5a8bfea5540432a62d7075443cf237571bfa4de
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118465"
---
# <a name="manage-project-based-opportunities"></a>Správa příležitostí založených na projektech

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Projektové společnosti mají své doručovací činnosti obvykle rozložené do více zemí a geografických oblastí. Náklady na realizaci a dodání projektu se mohou lišit v závislosti na tom, která geografická oblast nebo divize řídí dodávku. To pak může mít dopad na obchodní marže. Poskytování služeb založených na projektu obvykle zahrnuje velké množství času vynaloženého lidskými zdroji, značné výdaje na cestování, náklady na materiál a další výdaje.

Příležitosti založené na projektu v aplikaci Dynamics 365 Project Operations jsou rozšířením příležitostí vyskytujících se v Dynamics 365 Sales. Téma poskytuje podrobnosti o různých polích a obchodní logice obsažené v dalších funkcích, které jsou vyžadovány projektovými společnostmi ke správě příležitostí založených na projektu.

## <a name="view-all-project-based-opportunities"></a>Zobrazení všech příležitostí založených na projektech

Seznam všech příležitostí založených na projektech je uveden na stránce seznamu **Příležitost**. 

1. Přejděte na **Prodej** > **Příležitosti**.
2. K výběru jiných filtrovaných pohledů na příležitosti použijte **Přepínač zobrazení** . Můžete si vytvořit vlastní pohledy s vlastními kritérii filtru ke konfiguraci těchto zobrazení a možností navigace.

Na této stránce se seznamem nebo na stránce s podrobnostmi lze vytvářet nebo odstranit projektové příležitosti.

## <a name="business-process-flow-for-project-based-deals"></a>Tok obchodního procesu u obchodů založených na projektu

Následující toky obchodního procesu jsou podporovány u obchodů založených na projektu v aplikaci Project Operations:

- Obchodní proces od zájemce po příležitost
- Prodejní proces příležitosti

### <a name="lead-to-opportunity-business-process"></a>Obchodní proces od zájemce po příležitost 
Obchodní proces od zájemce po příležitost podporuje následující fáze:

| Fáze | Mapovaná entita | Funkce |
| --- | --- | --- |
| Zařadit | Potenciální zákazník | Zařazením zájemce vytvoříte účet, kontaktní osobu nebo příležitost. |
| Vytvořit | Příležitost | Vypracováním příležitosti přidáte další informace o provedené práci, klíčových účastnících a konkurenci. |
| Navrhnout | Příležitost | Vypracujte návrh a získejte souhlas od interního kontrolního týmu. |
| Uzavřeno | Příležitost | Vyhrajte příležitost uzavřít obchod. |

### <a name="opportunity-sales-process"></a>Prodejní proces příležitosti
Prodejní proces příležitosti v Project Operations je rozšířením obchodního toku prodejního procesu příležitosti v aplikaci Sales. Tento obchodní proces je navržen tak, aby podporoval následující fáze v příležitosti založené na projektu.

| Fáze | Mapovaná entita | Funkce |
| --- | --- | --- |
| Zařadit | Příležitost | Zařazením zájemce vytvoříte účet, kontaktní osobu nebo příležitost. |
| Navrhnout | Nabídka | Vypracujte návrh pomocí projektových nabídek a získejte souhlas od interního kontrolního týmu. |
| Smlouva | Projektová smlouva | Vyhrajte nabídku, vytvořte smlouvu a začněte s realizací a dodávkou projektu. |
| Uzavřeno | Projektová smlouva | Úspěšně dokončete práci a uzavřete projektovou smlouvu. |

> [!NOTE]
> Pokud vaše projektová dohoda začala zájemcem, má přednost obchodní proces od zájemce po příležitost.
>
> Pokud vaše projektová dohoda začala příležitostí, má přednost prodejní proces příležitosti.

Můžete upravit tok obchodního procesu produktu nebo vytvořit vlastní toky obchodního procesu a podle potřeby sledovat prodejní proces. Další informace o toku obchodního procesu naleznete v tématu [Přehled toků obchodního procesu](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]