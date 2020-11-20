---
title: Udržování členů týmu
description: Toto téma obsahuje informace o rezervaci pojmenovaných zdrojů pro projektové týmy a jejich přiřazování k úkolům.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131515"
---
# <a name="maintain-team-members"></a>Udržování členů týmu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Pojmenovaný zdroj můžete do vašeho projektového týmu přidat pomocí jejich přímé rezervace pro tým.

1. V aplikaci Dynamics 365 Project Operations přejděte na **Projekty** a vyberte otevření projektu, pro který provádíte rezervaci.
2. Na stránce **Projekt** vyberte na kartě **Tým** položku **Nový**. 
3. V dialogovém okně **Vytvořit: Člen projektového týmu** vyberte rezervovatelný zdroj. Pole **Role** se vyplní výchozí rolí zdroje, pokud je přiřazena. Roli je možné změnit. 
4. Vyberte datumy začátku a konce období, kdy bude zdroj vyžadován, a vyberte metodu přidělení kapacity zdroje. 
5. Pokud chcete, aby byl člen týmu schvalovatelem projektu, vyberte v poli **Schvalovatel projektu** hodnotu **Ano**. Člen týmu může schválit odeslané časové a výdajové záznamy pro tento projekt. 
6. Zvolte **Uložit**.

Nyní můžete rezervovaný zdroj přiřadit k úkolům v projektu. Na stránce **Projekt** na kartě **Plán** přiřaďte úkoly k novému zdroji,. Výběr zdroje, který se spouští z pole **Zdroje** v mřížce úkolu, zobrazí členy týmu, které můžete vybrat.


V aplikaci Project Operations nejsou rezervace zdrojů a přiřazení úkolů pevně spojeny. Když použijete výběr zdroje v plánu, můžete členům týmu přiřadit úkoly na více hodin, než jejich rezervace pokrývají projekt.

Rozdíly mezi rezervacemi a přiřazením člena týmu jsou uvedeny na kartách **Tým** a **Odsouhlasení zdrojů**. Můžete také odsouhlasit rozdíly mezi rezervacemi a přiřazeními zdrojů na podrobnější úrovni.

Pomocí výběru zdroje na kartě **Plán** vyhledejte a vyberte rezervovatelné zdroje, které ještě nejsou součástí projektového týmu. Tyto zdroje jsou ve výběru zdroje zobrazeny jako **Další zdroje**.

Po provedení výběru bude zdroj přidán do projektového týmu a přiřazen k úkolu, ale nebudou generovány žádné rezervace.

K rezervaci kapacity zdroje pro projekt můžete použít funkci prodloužení rezervace na kartě **Vyrovnání** nebo **Plánovací vývěska**.

Po rezervaci člena týmu ve vašem projektu můžete přímo spravovat jejich rezervace pomocí funkcí **Správa rezervací** **Plánovací vývěska**.
