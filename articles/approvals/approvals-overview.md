---
title: Přehled schválení
description: Toto téma poskytuje informace o práci se schváleními ve službě Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961158"
---
# <a name="approvals-overview"></a>Přehled schválení

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Odeslání času a výdajů prochází schvalovacím pracovním postupem. Po schválení položek jsou transakce zaznamenány ve skutečných hodnotách nebo je čas zaúčtován v rozvrhu.

## <a name="approvals-workflow"></a>Pracovní postup schválení
Když vytvoříte a odešlete položku času nebo výdajů, vytvoří se položka schválení. Schvalovatel projektu nebo váš nadřízený váš vstup zkontroluje a schválí. Pokud položka souvisí s projektem, po schválení budou vytvořeny skutečné údaje. To umožňuje sledování nákladů a fakturace. 

## <a name="approve-an-entry"></a>Schválit záznam
Formulář **Schválení** umožňuje přepínat mezi různými pohledy, takže můžete prohlížet různé typy schválení.
  
1. Přejděte na formulář **Schválení** a vyberte **Výdaje**, **Čas** nebo **Odvolání**.
2. Zkontrolujte každé schválení a vyberte ty, které chcete schválit.
3. Vyberte **Schvalovat**, chcete-li schválit vybrané položky.
Systém tyto záznamy zpracuje a vytvoří skutečné hodnoty nebo rezervaci.

## <a name="reject-an-entry"></a>Odmítnout záznam
Jako schvalovatel projektu možná budete muset zaslat záznam zpět uživateli k opravě.
  
1. Přejděte na formulář **Schválení** a vyberte záznam, který chcete odmítnout. 
2. Vyberte **Odmítnout**.
3. Volitelné - Přidejte komentář do dialogového okna **Komentáře k odmítnutí** informující uživatele, proč je záznam odmítnut.
4. Vyberte **OK**. Záznam bude vrácen uživateli.
  
## <a name="recall-entries"></a>Odvolání záznamů
V určitém okamžiku možná budete muset odeslaný záznam odvolat. Pokud záznam nebyl schválen, bude okamžitě vrácen. Schválená položka však může mít podstatný dopad. Schvalovatel projektu je povinen schválit odvolání, aby se transakce dále nepromítala do skutečných hodnot.

## <a name="specify-project-approvers"></a>Zadejte schvalovatele projektu
Každý projekt má několik členů projektového týmu. Můžete určit, kteří členové týmu jsou také schvalovateli projektu.

1. Přejděte na formulář **Projekty** a otevřete projekt ze seznamu.
2. Na kartě **Tým** vyberte člena týmu, který bude schvalovatelem projektu, a poté vyberte **Upravit**.
3. Nastavte pole **Schvalovatel projektu** na **Ano**.
4. Zvolte **Uložit**.
5. Opakováním kroků 2 a 4 přidejte další schvalovatele projektu.

## <a name="configure-the-users-manager"></a>Nakonfigurujte správce uživatele

1. Přejděte na **Nastavení** > **Zabezpečení** > **Uživatelé**.
2. Vyberte uživatele, kterému přiřazujete manažera, a v oblasti **Informace o organizaci** vyberte správce ze seznamu. 
3. Zvolte **Uložit**.


