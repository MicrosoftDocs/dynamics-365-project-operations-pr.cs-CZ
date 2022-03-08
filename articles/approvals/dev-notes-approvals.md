---
title: Poznámky pro vývojáře ohledně schvalování
description: Tohle téma poskytuje další informace pro vývojáře o práci se schváleními.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991658"
---
# <a name="developer-notes-for-approvals"></a>Poznámky pro vývojáře ohledně schvalování

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Řešení Dynamics 365 Project Operations obsahuje logiku ověřování, která zajišťuje správný průchod záznamů fázemi schvalování. Správný průchod záznamu zajistí: 

  - Všechny podpůrné řádky jsou vytvořeny v souvisejících tabulkách, jako jsou deníky a aktuální údaje.
  - Před pokračování je schvalovatel v projektu označen jako **Schvalovatel projektu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]