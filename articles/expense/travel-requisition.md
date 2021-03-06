---
title: Cestovní žádanky
description: Toto téma poskytuje informace o cestovních žádankách.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906112"
---
# <a name="travel-requisitions"></a>Cestovní žádanky

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Cestovní žádanka uvádí výdaje, které vzniknou za účelem cesty. Cestovní žádanka je předložena ke kontrole a lze ji použít k autorizaci výdajů.

Předtím, než vám vzniknou jakékoli náklady, které jsou účtovány organizaci, může být nutné předložit cestovní žádanku. Tento požadavek platí bez ohledu na to, zda účtujete výdaje na podnikovou kreditní kartu, utrácíte hotovost, kterou jste obdrželi z hotovostní zálohy, nebo vám vzniknou hotové výdaje, které vám organizace uhradí.

Cestovní žádanky a zásady lze použít ke správě výdajů organizace. Například pokud vaše organizace pracuje na projektu s pevnou cenou, který vyžaduje cestování, musí cestovní náklady členů týmu projektu odpovídat rozpočtu projektu. Vyžadováním schválení cestovních výdajů před jejich vznikem může organizace pomoci zajistit, aby projekt zůstal v rámci rozpočtu.

## <a name="configuration"></a>Konfigurace 

Cestovní požadavky lze nakonfigurovat jako „povinné“ povolením parametru „Předběžná autorizace cesty je povinná“ v parametrech správy výdajů. 

## <a name="create-and-submit-a-travel-requisition"></a>Vytvoření a odeslání cestovní žádanky

1. Přejděte na **Moje výdaje: Cestovní žádanka** a vyberte **Nová cestovní žádanka**.
2. Zadejte účel a cíl žádanky.
3. Do pole **Popis cesty** zadejte jakékoli další informace. 
4. Pro každý z očekávaných výdajů, například za letenku, stravu nebo pronájem auta, vytvořte řádkovou položku výdajů. Uveďte předpokládané datum, odhadovanou částku a měnu pro každý výdaj. 
5. Po dokončení přidávání očekávaných výdajů vyberte **Uložit**.
6. Až budete připravení odeslat cestovní žádanku, vyberte **Pracovní postup** > **Odeslat**.

Schválené cestovní žádanky si můžete prohlédnout v okně **Moje výdaje: Cestovní žádanka**. 

## <a name="view-available-travel-requisitions"></a>Zobrazení dostupných cestovních žádanek

Všechny své cestovní žádanky si můžete prohlédnout v okně **Moje výdaje: Cestovní žádanky**.

## <a name="approve-travel-requisitions"></a>Schválení cestovních žádanek

Vyberte cestovní žádanku, kterou chcete schválit, a poté vyberte **Pracovní postup** > **Schválit**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Odeslání zprávy o výdajích pomocí schválené cestovní žádanky

1. Vytvořte nové vyúčtování výdajů a v záhlaví vyúčtování výdajů vyberte ze seznamu schválených cestovních žádanek **Mapa k cestovní žádance**.
2. Pole **Částka na cestovní žádance** se automaticky aktualizuje v záhlaví vyúčtování výdajů.
3. Přidejte jednotlivé výdaje vynaložené na cestu. Pokud je povoleno pole **Schváleno předem**, bude aktualizována sesouhlasená částka a autorizovaná částka pro konkrétní kategorii výdajů.

> [!NOTE]
> Když mapujete vyúčtování výdajů na schválenou žádost o cestování, částka transakce nemůže být větší než autorizovaná částka. 
