---
title: Opravené faktury
description: Toto téma poskytuje informace o opravených fakturách.
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
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898073"
---
# <a name="corrected-invoices"></a>Opravené faktury

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Potvrzené faktury lze upravovat. Když upravíte potvrzenou fakturu, vytvoří se koncept opravené faktury. Protože se předpokládá, že chcete zrušit všechny transakce a množství z původní faktury, obsahuje tato opravená faktura všechny transakce z původní faktury a všechna množství na ní jsou nula (0).

Pokud transakce nevyžadují opravu, můžete je odebrat z konceptu opravné faktury. Pokud chcete stornovat nebo vrátit pouze částečné množství, můžete upravit pole Množství v podrobnostech řádku. Pokud otevřete podrobnosti řádku faktury, uvidíte původní množství faktury. Potom můžete upravit aktuální množství faktury tak, aby bylo menší nebo větší než původní množství faktury.

Po potvrzení opravné faktury se původní skutečná hodnota fakturovaného prodeje stornuje a vytvoří se nová skutečná hodnota fakturovaného prodeje. Pokud bylo množství sníženo, rozdíl způsobí, že bude vytvořena i nová skutečná hodnota nefakturovaného prodeje. Pokud byl například původní fakturovaný prodej na 8 hodin a opravené podrobnosti řádku faktury obsahují snížené množství 6 hodin, stornují se původní vyfakturované prodejní řádky a vytvoří dvě nové skutečné hodnoty:

- Fakturovaná skutečná hodnota prodeje pro 6 hodin.
- Skutečná hodnota nefakturovaného prodeje pro zbývající dvě hodiny. Tato transakce může být buď fakturována později, nebo označena jako neúčtovatelná, v závislosti na jednáních se zákazníkem.
