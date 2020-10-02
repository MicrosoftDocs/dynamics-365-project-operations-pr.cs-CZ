---
title: Nastavení prodejního ceníku
description: Tento téma poskytuje informace o prodejních cenících pro ceny projektů.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896453"
---
# <a name="sales-price-list-setup"></a>Nastavení prodejního ceníku

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

U projektových nabídek a smluv má projektový ceník odlišný způsob přepsání ceny než produktový ceník. Na řádku nabídky založeném na katalogu produktů můžete přepsat cenu rolí a kategorií přímo na řádku nabídky, protože každý řádek nabídky odkazuje přesně na jednu položku katalogu. Na řádku nabídky založeném na projektu však nemůžete přepsat cenu rolí a kategorií přímo na řádku nabídky. Ceník projektu můžete použít pro práci se dvěma odlišnými vzory přepsání.

> [!NOTE]
> Doporučujeme, abyste pro zdroje projektu a položky katalogu měli samostatný ceník, a to z důvodu rozdílů v chování mezi těmito dvěma položkami při přepsání ceny.

Každá z následujících entit může obsahovat jeden nebo více přidružených ceníků pro ocenění projektu:

- Zákazník (účet) 
- Příležitost 
- Nabídka 
- Projektová smlouva

Přidružení těchto entit k ceníku je označeno pomocí projektových ceníků. K entitám Zákazník, Příležitost, Nabídka a Projektová smlouva můžete přidružit jeden nebo více ceníků.

Výchozí projektový ceník není automaticky zadán do záznamu zákazníka. K záznamu zákazníka však můžete ručně připojit Ceník projektu. Přesto byste měli projektový ceník přiložit ručně pouze v případě, že máte se zákazníkem vlastní cenovou dohodu. 

Pokud je projektový ceník připojen k prodejní entitě, ověřují se následující informace:

- Ceník má kontext **Prodej**. 
- Měna ceníku se musí shodovat s měnou zákazníka. 

U projektové smlouvy se používá následující pořadí priorit pro automatické nastavení souvisejících projektových ceníků:

1. Nabídka
2. Příležitost
3. Zákazník 
4. Globální nastavení 

Je-li ve výchozím nastavení zadán projektový ceník, systém ověří, že měna odpovídá měně zákazníka, a že zadané výchozí ceníky obsahují kontext **Prodeje**.

K entitám Zákazník, Příležitost, Nabídka a Projektová smlouva můžete přidružit několik projektových ceníků. Tato funkce podporuje výchozí ceny specifické pro datum pro dlouhotrvající projektovou smlouvu, kde můžete vyžadovat více než jeden ceník na obchodní vztah pro aktualizace cen, ke kterým dochází z důvodu inflace. Pokud však ceníky, které přidružíte k entitě Zákazník, Příležitost, Nabídka nebo Projektová smlouva, mají překrývající se datum účinnosti, mohou být výchozí ceny nesprávné. Proto byste se měli ujistit, že projektové ceníky s překrývajícími se daty účinnosti nejsou přidruženy k těmto entitám.
