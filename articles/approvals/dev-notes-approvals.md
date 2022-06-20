---
title: Poznámky pro vývojáře ohledně schvalování
description: Tento článek poskytuje další informace pro vývojáře o práci se schváleními.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924744"
---
# <a name="developer-notes-for-approvals"></a>Poznámky pro vývojáře ohledně schvalování

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Řešení Dynamics 365 Project Operations obsahuje logiku ověřování, která zajišťuje správný průchod záznamů fázemi schvalování. Správný průchod záznamu zajistí: 

  - Všechny podpůrné řádky jsou vytvořeny v souvisejících tabulkách, jako jsou deníky a aktuální údaje.
  - Před pokračování je schvalovatel v projektu označen jako **Schvalovatel projektu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]