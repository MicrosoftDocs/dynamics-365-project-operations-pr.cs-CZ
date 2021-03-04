---
title: Rezervujte pro projektový tým pojmenované rezervovatelné zdroje a přiřaďte úkoly
description: Toto téma obsahuje informace o rezervaci pojmenovaných zdrojů pro projektové týmy a jejich přiřazování k úkolům.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145350"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Rezervujte pro projektový tým pojmenované rezervovatelné zdroje a přiřaďte úkoly 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pojmenovaný zdroj můžete do vašeho projektového týmu přidat pomocí přímé rezervace pro tým. Postup je uveden níže.

1. V Project Service Automation přejděte na **Projekty** a vyberte otevření projektu, pro který provádíte rezervaci.
2. Na stránce **Projekt** klikněte na kartě **Tým** na **Nový**. 

![Přidání člena týmu z karty týmu](media/RM-how-to-1.png)

3. V dialogovém okně **Vytvořit: Člen projektového týmu** vyberte rezervovatelný zdroj. Pole **Role** se vyplní výchozí rolí zdroje, pokud je přiřazena. V případě potřeby můžete roli změnit. 
4. Vyberte data od a do, kdy bude zdroj vyžadován, a vyberte metodu přidělení kapacity zdroje. 
5. Pokud chcete, aby byl člen týmu schvalovatelem projektu, vyberte **Ano** v poli **Schvalovatel projektu**. To bude znamenat, že tento člen týmu může schválit odeslané časové a výdajové záznamy pro tento projekt. 
6. Klikněte na **Uložit**.

![Přidání člena týmu na stručný formulář pro vytvoření](media/RM-how-to-2.png)


Nyní můžete rezervovaný zdroj přiřadit k úkolům v projektu. Chcete-li přiřadit úkoly k novému zdroji, klikněte na stránce **Projekt** na kartu **Plán**. Výběr zdroje, který se spouští z pole **Zdroje** v mřížce úkolu, zobrazí členy týmu, které můžete vybrat.

![Přiřazení člena týmu k úkolu na kartě plánu](media/RM-how-to-3.png)

Ve verzi 3 pro Project Service Automation (PSA) nejsou rezervace zdrojů a přiřazení úkolů úzce spojeny. To znamená, že pokud použijete výběr zdroje v plánu, můžete členům týmu přiřadit úkoly na více hodin, než jejich rezervace pokrývají projekt.
Rozdíly mezi rezervacemi a přiřazeními členů týmu lze zobrazit na kartě **Tým** nebo na kartě **Vyrovnání zdrojů**. Můžete také vyrovnat rozdíly mezi rezervacemi a přiřazeními zdrojů na podrobnější úrovni.

![Karta Vyrovnání zdrojů](media/RM-how-to-4.png)

Pomocí výběru zdroje na kartě **Plán** můžete také vyhledat a vybrat rezervovatelné zdroje, které ještě nejsou součástí projektového týmu. Tyto jsou ve výběru zdroje zobrazeny jako **Další zdroje**.

![Přiřazení zdroje, který není členem týmu, k úkolu](media/RM-how-to-5.png)

Pokud to uděláte, bude zdroj přidán do projektového týmu a přiřazen k úkolu, ale nebudou generovány žádné rezervace.

![Člen týmu s přiřazeními a bez rezervací](media/RM-how-to-6.png)

K rezervaci kapacity zdroje pro projekt můžete použít funkci prodloužení rezervace na kartě **Vyrovnání** nebo **Plánovací vývěska**.

![Rozšíření rezervací pro člena týmu na kartě vyrovnání prostředků](media/RM-how-to-7.png)

Po rezervaci člena týmu ve vašem projektu můžete použít správu rezervací nebo pomocí Plánovací vývěsky přímo spravovat jejich rezervace.
