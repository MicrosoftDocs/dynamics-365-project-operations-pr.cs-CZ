---
title: Přepsání prodejních ceníků projektu
description: Tohle téma poskytuje informace o vytváření vlastních prodejních ceníků.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: db2ff6acaad6ab4cbcc98d3d5b06b36ed23b758f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995073"
---
# <a name="override-project-sales-price-lists"></a>Přepsání prodejních ceníků projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

## <a name="customer-specific-project-price-lists"></a>Projektový ceník konkrétního zákazníka

Cenové smlouvy konkrétních zákazníků lze nastavit jako projektové ceníky v záznamu obchodního vztahu v Dynamics 365 Project Operations.

Chcete-li nastavit projektový ceník konkrétního zákazníka, v oblasti **Prodej** přejděte k záznamu obchodního vztahu.

1. Otevřete stránku seznamu **Obchodní vztahy**.
2. Vyhledejte a poklepejte na záznam zákazníka a otevřete stránku s podrobnostmi **Obchodní vztah**.
3. Na kartě **Projektové ceníky** vyberte **+ Nový projektový ceník**.
4. Na stránce **Nový projektový ceník** vyberte z rozevíracího seznamu ceník. Jsou zde pouze ceníky, jejichž kontext je nastaven na **Prodej** a jejichž měna odpovídá měně obchodního vztahu.
5. Pojmenujte přidružení a poté vyberte **Uložit**. Vytvoří se projektový ceník konkrétního zákazníka. Tento ceník bude určovat výchozí projektové ceny u projektových nabídek nebo smluv vytvořených pro tohoto zákazníka, kde datum vytvoření projektové nabídky nebo smlouvy spadá do data účinnosti ceníku.

## <a name="custom-pricing-on-project-quotes"></a>Vlastní ceny projektových nabídek

V případě projektových nabídek můžete mít ceny projektu, které začínají s výchozím standardním ceníkem vycházejícím z parametrů zákazníka nebo projektu.

Když potřebujete vlastní ceny za práci související s projektem pro konkrétní nabídku, můžete ji získat z přidružené entity projektových ceníků.

Provedením následujících kroků nastavíte ceny projektu pro konkrétní nabídku.

1. Otevřete projektovou nabídku a vyberte kartu **Projektové ceníky**.
2. V podmřížce vyberte **Vytvořit vlastní ceny**.

Všechny projektové ceníky, které jsou připojeny k nabídce, jsou zkopírovány do nových ceníků. Názvy nových ceníků odrážejí název nabídky s razítkem data a času, kdy byly tyto ceníky vytvořeny.

Můžete použít každý z těchto ceníků a aktualizovat ceny práce (cena role) a nákladů (cena kategorie). Tyto ceny se budou vztahovat pouze na tuto projektovou nabídku.

## <a name="price-lists-on-a-project-contract"></a>Projektové ceníky na projektové smlouvě

Na projektové smlouvě je cena projektu vždy výchozí jako vlastní ceník s názvem smlouvy a vytvořeným razítkem data a času připojeným k názvu. To platí, ať už byla smlouva vytvořena při získání nabídky, nebo pokud byla smlouva vytvořena úplně od začátku. V případě potřeby můžete toto přidružení k vlastnímu ceníku odebrat a místo toho přidružit standardní ceník k projektové smlouvě.

Když přidružíte standardní ceník k projektovým ceníkům nabídky nebo smlouvy, jakékoli změny provedené v cenách v ceníku ovlivní všechny nabídky a smlouvy, které používají ceník.


[!INCLUDE[footer-include](../includes/footer-banner.md)]