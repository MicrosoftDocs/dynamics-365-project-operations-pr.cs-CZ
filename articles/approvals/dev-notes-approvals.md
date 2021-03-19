---
title: Poznámky pro vývojáře ohledně schvalování
description: Tohle téma poskytuje další informace pro vývojáře o práci se schváleními.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290261"
---
# <a name="developer-notes-for-approvals"></a>Poznámky pro vývojáře ohledně schvalování

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Řešení Dynamics 365 Project Operations obsahuje logiku ověřování, která zajišťuje správný průchod záznamů fázemi schvalování. Správný průchod záznamu zajistí: 

  - Všechny podpůrné řádky jsou vytvořeny v souvisejících tabulkách, jako jsou deníky a aktuální údaje.
  - Před pokračování je schvalovatel v projektu označen jako **Schvalovatel projektu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]