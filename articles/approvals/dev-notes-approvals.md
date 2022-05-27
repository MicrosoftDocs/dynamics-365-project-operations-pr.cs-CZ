---
title: Poznámky pro vývojáře ohledně schvalování
description: Tohle téma poskytuje další informace pro vývojáře o práci se schváleními.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579712"
---
# <a name="developer-notes-for-approvals"></a>Poznámky pro vývojáře ohledně schvalování

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Řešení Dynamics 365 Project Operations obsahuje logiku ověřování, která zajišťuje správný průchod záznamů fázemi schvalování. Správný průchod záznamu zajistí: 

  - Všechny podpůrné řádky jsou vytvořeny v souvisejících tabulkách, jako jsou deníky a aktuální údaje.
  - Před pokračování je schvalovatel v projektu označen jako **Schvalovatel projektu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]