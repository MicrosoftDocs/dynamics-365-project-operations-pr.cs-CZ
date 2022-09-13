---
title: Aktivace a úprava nabídky projektu
description: Tento článek poskytuje informace o tom, jak aktivovat a revidovat nabídky v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410317"
---
# <a name="activate-and-revise-a-project-quote"></a>Aktivace a úprava nabídky projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Funkce aktivace a revize vám pomohou sledovat správu verzí pro projektové nabídky během fází odhadu a vyjednávání. Když je koncept nabídky aktivován, bude pouze pro čtení.

Funkce aktivace a revize vám umožňují provádět následující úlohy:

- Nabídky vyhráváte a prohráváte pouze po aktivaci.
- Upravte nabídku, abyste provedli změny ve stávající nabídce nebo vytvořili novou verzi.

> [!NOTE]
> Po aktivaci funkce pro aktivaci a revizi nabídek ji nelze deaktivovat.

Chcete-li zapnout možnost aktivovat a revidovat nabídky na základě projektu, postupujte takto.

1. Přejděte na **Nastavení** \> **Parametry**.
1. Otevřete záznam **Parametry**.
1. V podokně akcí na kartě **Ovládání funkcí** vyberte **Povolit aktivaci a revizi nabídek**.
1. V dialogovém okně pro potvrzení vyberte **OK**.
1. Po chvíli obnovte prohlížeč. Nyní by měly být k dispozici možnosti aktivace a revize. Budete vědět, že tyto funkce byly povoleny, pokud se tlačítko **Povolit aktivaci a revizi nabídek** již nezobrazuje v podokně akcí.

## <a name="activating-a-quote"></a>Aktivace nabídky

Po aktivaci funkce pro aktivaci a revizi nabídek, tlačítka **Zavřít nabídku jako získanou** a **Zavřít nabídku jako ztracenou** v podokně akcí nejsou k dispozici pro návrhy nabídek projektu. Jsou dostupné pouze po aktivaci nabídky.

Aktivace představuje fázi v procesu nabídky, kdy chcete zabránit dalším změnám nabídky. V této fázi je nabídka odeslána k interní kontrole nebo zákazníkovi.

Tlačítka **Zavřít nabídku jako získanou** a **Zavřít nabídku jako ztracenou** v podokně akcí jsou k dispozici pro aktivované nabídky. V závislosti na výsledku interního nebo zákaznického hodnocení můžete použít jedno z těchto tlačítek k uzavření aktivované nabídky. Výběrem **Revidovat nabídku** můžete provádět vyjednávání a změny aktivovaných nabídek.

## <a name="revising-a-quote"></a>Revize nabídky

Pokud musíte provést změny v aktivované nabídce, vyberte **Revidovat nabídku**. Nabídka je uzavřena a použije se kód důvodu **revidováno**. Poté se vytvoří nová nabídka, která má stejné ID a zvýšené číslo revize. Všechny údaje z původní nabídky se zkopírují do nové nabídky. Nová nabídka je ve stavu konceptu a lze ji podle potřeby upravit.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
