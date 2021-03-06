---
title: Řádky příležitosti založené na projektu (Pro)
description: Toto téma poskytuje informace o řádcích příležitosti založené na projektu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896363"
---
# <a name="project-based-opportunity-lines-pro"></a>Řádky příležitosti založené na projektu (Pro)

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Řádky příležitosti založené na projektu jsou k dispozici pouze u příležitostí založených na projektu. Záznamy příležitosti založené na projektu mají nastaveno pole **Typ** na hodnotu **Na základě práce**.

Řádky příležitosti založené na projektu jsou řádkové položky, které budou zákazníkovi doručeny pomocí projektu. Projekt však nelze vázat na řádek příležitosti založené na projektu. Projekty lze vázat k řádkovým položkám od fáze **Nabídka** dále, protože příležitost se obvykle objevuje v rané fázi životního cyklu obchodu. Rozhodnutí, kolik projektů bude použito k doručení práce pro zákazníka, je rozhodnutím, které se provede později ve fázi prodeje. Fázi příležitosti používejte k identifikaci jednotlivých komponent dodávek pro zákazníka. Rozhodnutí týkající se skutečného počtu projektů použitých k dodání těchto komponent lze odložit na později, až budou známy další informace o samotné práci.

Níže jsou vyjmenována pole v řádku příležitosti založené na projektu:

| **Pole** | **Umístění** | **Relevance, účel a vedení** | **Dopad na následné složky** |
| --- | --- | --- | --- |
| Typ produktu | Karta Obecné (skrytá) | Můžete vybrat některou z následujících možností:</br>- Služba založená na projektu (k dispozici pouze v případě, že máte nainstalovanou aplikaci Dynamics 365 Project Operations)</br>- Produkt (k dispozici pouze v případě, že jsou nainstalovány aplikace Project Operations a Dynamics 365 Sales) | Hodnota tohoto pole se nastaví na **Služba založená na projektu**, když vytvoříte řádek příležitosti založené na projektu z mřížky řádků založených na projektu v příležitosti. <br> Pokud tuto hodnotu změníte nebo přepíšete, nebude u vašich řádkových položek založených na projektu povolena funkce projektu. |
| Příležitost | Karta Obecné | Toto pole je pouze ke čtení a odkazuje na nadřazený záznam příležitosti, ke kterému tato řádková položka patří. | Toto pole nemá žádný následný dopad. |
| Jméno | Karta Obecné | Toto upravitelné textové pole lze použít k zadání krátké identity pro řádkovou položku. | Tato hodnota se přenese do řádku nabídky, když vytvoříte nabídku z této příležitosti. |
| Rozpočet zákazníka | Karta Obecné | Toto upravitelné pole měny lze použít ke sledování částky, kterou je zákazník ochoten za tuto řádkovou položku utratit. | Tato hodnota se přenese do odpovídajícího pole v řádku nabídky, když vytvoříte nabídku z této příležitosti. |
| Způsob fakturace | Karta Obecné | Toto upravitelné pole může obsahovat následující hodnoty:</br>- Čas a materiál</br>- Pevná cena | Tato hodnota se přenese do odpovídajícího pole v řádku nabídky, když vytvoříte nabídku z této příležitosti. Po vytvoření řádku nabídky je pole uzamčeno a nelze jej změnit. Přiřaďte tuto hodnotu pole co nejpřesněji. Pokud potřebujete změnit hodnotu tohoto pole v řádku nabídky, odstraňte a znovu vytvořte řádek nabídky. |
