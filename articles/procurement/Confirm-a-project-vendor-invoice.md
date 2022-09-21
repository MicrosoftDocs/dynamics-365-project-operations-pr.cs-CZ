---
title: Potvrzení faktur dodavatele projektu
description: Tento článek vysvětluje, jak potvrdit fakturu dodavatele projektu v Microsoft Dynamics 365 Project Operations, a popisuje finanční dopad potvrzení faktury dodavatele projektu.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475414"
---
# <a name="confirm-project-vendor-invoices"></a>Potvrzení faktur dodavatele projektu

_ **Platí pro:** Project Operations u scénářů založených na zdrojích / položkách, které nejsou na skladě

Když je parametr **Je vyžadováno ruční potvrzení projektovým manažerem** zapnutý, faktury dodavatele, které jsou vytvořeny v Microsoft Dataverse, mají stav **Koncept**. Faktury dodavatele, které jsou vytvořeny tímto způsobem, musí být zkontrolovány a ručně potvrzeny. Když je parametr **Je vyžadováno ruční potvrzení projektovým manažerem** neaktivní, faktury dodavatele, které jsou vytvořeny v Dataverse, jsou automaticky potvrzeny. Nevyžadují se žádné další akce. 

Po ověření všech řádků na faktuře dodavatele v Dynamics 365 Project Operations vyberte **Potvrdit** k potvrzení faktury dodavatele.

Když vyberete **Potvrdit** na faktuře dodavatele, dojde k následujícím akcím:

1. Stav faktury dodavatele je aktualizován na **Potvrzeno**.
1. Potvrzená faktura dodavatele a související záznamy jsou nadále pouze ke čtení a nelze je upravovat ani odstranit.
1. Pokud některé skutečné náklady odkazují na řádek faktury dodavatele jako součást procesu párování, všechny skutečné náklady, které jsou přidruženy k řádku faktury dodavatele odkazu, jsou stornovány.
1. Nové skutečné náklady se vytvářejí pomocí informací na řádku faktury dodavatele.
1. Již nemůžete vytvářet deníky oprav, zpracovávat odvolání časových záznamů ani rušit schválení původních skutečných časů, výdajů nebo materiálu, které byly stornovány.
1. V Dynamics 365 Finance je hodnota **Náklady na projekt** aktualizována pomocí deníku integrace projektu a účet integrace nákupu je *vrácen* po zaúčtování deníku integrace projektu.

> [!NOTE]
> Pokud má některý řádek na faktuře dodavatele stav ověření jiný než **Dokončeno**, fakturu dodavatele nelze potvrdit.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
