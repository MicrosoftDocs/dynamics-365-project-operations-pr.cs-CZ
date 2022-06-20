---
title: Řádky příležitosti založené na projektu
description: Tento článek poskytuje informace o práci s řádky příležitostí založených na projektu.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f4b8d80a7e3ec06c4089d7c5c32fdb41ac86fb76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918258"
---
# <a name="project-based-opportunity-lines"></a>Řádky příležitosti založené na projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_


Řádky příležitosti založené na projektu jsou k dispozici pouze u příležitostí založených na projektu. Záznamy příležitosti založené na projektu mají nastaveno pole **Typ** na hodnotu **Na základě práce**.

Řádky příležitosti založené na projektu jsou řádkové položky, které budou zákazníkovi doručeny pomocí projektu. Projekt však nelze vázat na řádek příležitosti založené na projektu. Projekty lze přiřadit k řádkovým položkám od fáze **Nabídka** dále, protože příležitost se obvykle objevuje v rané fázi obchodu. Rozhodnutí, kolik projektů bude použito k doručení práce pro zákazníka, je rozhodnutím, které se provede později ve fázi prodeje. Využijte fázi příležitosti k identifikaci jednotlivých komponent dodávek pro zákazníka. Rozhodnutí týkající se skutečného počtu projektů použitých k dodání těchto komponent lze odložit na později, až budou známy další informace o samotné práci.

Níže jsou vyjmenována pole v řádku příležitosti založené na projektu:

| **Pole** | **Umístění** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- | --- |
| Typ produktu | Karta Obecné (skrytá) | Toto je pole sady možností. Pokud máte nainstalovanou aplikaci Dynamics 365 Operations, jednou z dostupných možností je **Služba založená na projektu**.  | Hodnota tohoto pole se nastaví na **Služba založená na projektu**, když vytvoříte řádek příležitosti založené na projektu z mřížky řádků založených na projektu v příležitosti. <br> Pokud tuto hodnotu změníte nebo přepíšete, nebude u vašich řádkových položek založených na projektu povolena funkce projektu. |
| Příležitost | Karta Obecné | Toto pole je pouze ke čtení a odkazuje na nadřazený záznam příležitosti, ke kterému tato řádková položka patří. | Toto pole nemá žádný následný dopad. |
| Jméno | Karta Obecné | Toto je upravitelné textové pole, ve kterém lze této řádkové položce zadat krátkou identitu | Tato hodnota se přenese do řádku nabídky, když vytvoříte nabídku z této příležitosti |
| Rozpočet zákazníka | Karta Obecné | Toto upravitelné pole měny lze použít ke sledování částky, kterou je zákazník ochoten za tuto řádkovou položku utratit. | Tato hodnota se přenese do odpovídajícího pole v řádku nabídky, když vytvoříte nabídku z této příležitosti |
| Způsob fakturace | Karta Obecné | Toto upravitelné pole může obsahovat následující hodnoty:</br>- Čas a materiál</br>- Pevná cena | Tato hodnota se přenese do odpovídajícího pole v řádku nabídky, když vytvoříte nabídku z této příležitosti. Po vytvoření řádku nabídky je pole uzamčeno a nelze jej změnit. Přiřaďte tuto hodnotu pole co nejpřesněji. Pokud potřebujete změnit hodnotu tohoto pole v řádku nabídky, odstraňte a znovu vytvořte řádek nabídky. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]