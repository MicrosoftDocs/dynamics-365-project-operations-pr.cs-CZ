---
title: Přehled využití zdroje
description: Tohle téma obsahuje informace o využití zdrojů v Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401368"
---
# <a name="resource-utilization-overview"></a>Přehled využití zdroje

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Zdroje mohou mít cílové fakturovatelné využití. Toto cílové využití je definováno jako atribut výchozí role zdroje, nebo je nastaveno v záznamu konkrétního rezervovatelného zdroje. Výpočty využití vycházejí ze skutečných hodin, které zdroje vykázaly pomocí schválených časových záznamů.

K výpočtu využití se používají následující vzorce:

  - Fakturovatelné využití = skutečné fakturovatelné hodiny ÷ kapacita zdroje
  - Nefakturovatelné využití = skutečný čas s ID typu fakturace = neúčtovatelné, komplementární nebo nedostupné ÷ kapacita zdroje
  - Interní = skutečný čas bez prodejní smlouvy ÷ kapacita zdroje
  - Kapacita zdroje = pracovní doba zdroje – mimo kancelář – nepracovní dny

Zobrazení **Využití zdroje** naleznete v podokně **Zdroje**.

Každá buňka v tabulce představuje procentuální hodnotu fakturovatelného využití zdroje v určitém období, například den, týden nebo měsíc. K obarvení buněk se používají následující vzorce:

  - **Zelená**: Fakturovatelné využití > = Cílové využití zdroje
  - **Žlutá**: Cílové využití – 20 < = Fakturovatelné využití < Cílové využití
  - **Červená**: Fakturovatelné využití < Cílové využití – 20.

Vzhledem k tomu, že je zobrazení **Využití zdroje** založeno na Plánovací vývěsce, můžete k filtrování výsledků využít funkce filtrování Plánovací vývěsky.

Mřížka vyžaduje, abyste nastavili cílové využití buď u role, nebo u konkrétního zdroje. Pro toto nastavení přejděte na **Zdroje** > **Role zdrojů**.

Navíc musí být ke každému rezervovatelnému zdroji přiřazena výchozí role. Přejděte na **Zdroje** > **Zdroje**. Na kartě **Project Service** ověřte, zda je definována role zdroje a zda pole **Je výchozí** je nastaveno na **Ano**. Můžete přidat další role, kde **Je výchozí** = **Ne**. Role, ve které **Je výchozí** = **Ano**, slouží k vyhodnocení využití prostředku vůči cíli pro danou roli.

Na kartě **Project Service** můžete také nastavit individuální cílové využití zdroje. Výpočet využití pak používá toto cílové využití k vyhodnocení cíle zdroje namísto cíle výchozí role zdroje.

Využití je pro zdroj zobrazeno pouze v případě, že tento zdroj má schválenou fakturovatelnou dobu během období zobrazeného v mřížce.
