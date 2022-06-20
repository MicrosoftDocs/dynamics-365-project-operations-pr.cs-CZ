---
title: Záznam využití materiálu na projektech a projektových úkolech
description: Tento článek poskytuje informace o tom, jak protokolovat využití materiálu u projektů a projektových úkolů.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eeb8303821bc4c246e37333ddbcb77ca798d2e8f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920052"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Záznam využití materiálu na projektech a projektových úkolech

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Jak projektový tým pracuje na úkolech na projektu, spotřebovává nebo používá materiály. Protokol použití materiálu poskytuje způsob, jak toto využití zaznamenat, aby jej mohl schválit vedoucí projektu a případně fakturovat zákazníkovi. 

Chcete-li zaznamenat použití katalogových nebo zapisovaných materiálů a odeslat je schvalovateli, postupujte takto: 

1. V navigačním podokně vyberte **Využití materiálu** a potom vyberte **Nový**.
2. Na stránce **Nové využití materiálu** zadejte požadované informace o využití materiálu a poté vyberte **Uložit**.

Následující tabulka poskytuje informace o polích na stránce **Protokol použití materiálu**. 

| **Pole** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- |
| Popis | Popis konkrétního použití materiálu. | Neexistuje žádný následný dopad na toto pole. |
| Datum | Datum, kdy se předpokládá použití materiálu. | Neexistuje žádný následný dopad na toto pole. |
| Project | Seznam projektů, které jsou aktivní. | Výběr projektu pro protokol využití materiálu ovlivní pole **Úkol** pro zobrazení pouze těch úkolů, které jsou na projektu. |
| Úkol | Seznam úkolů pro projekt včetně souhrnných úkolů a úkolů v uzlech typu list. | Výběr úlohy pro protokol využití materiálu ovlivní skutečné náklady na materiál a skutečný prodej materiálu pro daný úkol. Pokud je toto pole prázdné, jsou odpovídající náklady na využití materiálu a tržby sledovány a shrnuty pouze na úrovni projektu. |
| Vybrat produkt | Určete, zda je toto použití materiálu pro **Existující** (katalogový) produkt nebo a **Zapsaný** produkt. | Toto pole určuje typ produktu. |
| Produkt | ID produktu z katalogu produktů. Když vyberete ID produktu, pole **Vybrat produkt** se automaticky aktualizuje na **Stávající produkt**. ID se používá k načtení nákladů a prodejních cen z ceníku. | Neexistuje žádný následný dopad na toto pole. |
| Popis produktu nezahrnutého do katalogu | Textové pole pro zadání názvu produktu. Toto pole je k dispozici, když vyberete produkt **nezahrnutý do katalogu** v poli **Vybrat produkt**.| Neexistuje žádný následný dopad na toto pole. |
| Rezervovatelný zdroj| Prostředek, který použil tento materiál na projekt. Výchozí hodnota pro toto pole je rezervovatelný prostředek přihlášeného uživatele, ale lze jej změnit tak, aby zaznamenával využití jménem ostatních členů projektového týmu. | Neexistuje žádný následný dopad na toto pole. |
| Skupina jednotek | Výchozí hodnota v tomto poli pochází ze skupiny jednotek, která je nastavena jako výchozí na katalogovém produktu. Toto pole můžete aktualizovat a vybrat jinou skupinu jednotek. | Neexistuje žádný následný dopad na toto pole. |
| Jednotka | Výchozí hodnota v tomto poli je výchozí jednotka vybraného produktu. Toto pole můžete aktualizovat a vybrat jinou jednotku. | Změna jednotky má za následek jinou výchozí jednotkovou cenu a náklad. |
| Množství | Množství produktu, které bylo použito na projektu nebo úkolu projektu. | Neexistuje žádný následný dopad na toto pole. |
| Jednotkové náklady | Jednotkové náklady na vybraný produkt a kombinace jednotek stanovené v příslušném ceníku nákladů. | Jednotkové náklady se vždy zobrazují v měně nákladů projektu. Pokud v ceníku neexistují jednotkové náklady pro kombinovaný produkt a jednotku, jednotkové náklady se standardně nastaví na 0,00. |
| Celkové náklady | Částka nákladů, která se počítá jako množství \* jednotková cena.| Částka nákladů se vždy zobrazuje v měně nákladů projektu. |


## <a name="submit-material-usage-for-review-and-approval"></a>Odešlete použití materiálu ke kontrole a schválení 
Jakmile zachytíte veškeré využití materiálu a jste připraveni jej schválit, musíte odeslat informace o použití ke kontrole.

1. Přejděte na **Protokol použití materiálu** a vyberte jednu nebo více položek. Nebo vyberte všechny záznamy o využití materiálu pomocí zaškrtávacího políčka v záhlaví.
2. Vyberte položku **Odeslat**. Systém zpracuje vybrané položky a poté vytvoří žádosti o schválení použití materiálu.

## <a name="recall-a-material-usage-log"></a>Protokol odvolání použití materiálu

V případě potřeby můžete odvolat odeslané využití materiálu. Čas potřebný k odvolání záznamu o použití materiálu závisí na fázi schválení.  Pokud schvalovatel dosud neschválil záznam, může k odvolání dojít okamžitě. Pokud však již byl záznam schválen, je schvalovatel požádán o schválení odvolání a zrušení transakcí.

1. Přejděte do nabídky **Využití materiálu** a v seznamu protokolů využití materiálu vyberte využití materiálu, které chcete odvolat.
2. Vyberte **Odvolat**. Pokud položka využití materiálu ještě nebyla schválena, systém ji okamžitě odvolá. Pokud již byla položka materiálu schválena, vytvoří se žádost o odvolání, která informuje schvalovatele, že chcete odvolat použití materiálu. Schvalovatel poté potvrdí, že lze provést zrušení, a záznam bude vrácen.

## <a name="delete-a-material-usage-log"></a>Protokol odstranění použití materiálu

Můžete odstranit protokoly o použití materiálu, které nebyly odeslány. Chcete-li odstranit již odeslaný protokol o použití materiálu, musíte jej nejprve odvolat.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
