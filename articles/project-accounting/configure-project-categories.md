---
title: Konfigurace kategorií projektu
description: Toto téma obsahuje informace o nastavení kategorií projektu.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131920"
---
# <a name="configure-project-categories"></a>Konfigurace kategorií projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Project Operations nabízí robustní funkce pro kategorizaci výnosů a nákladů na projekty. Kategorie poskytují možnost reportovat a analyzovat transakce projektu a řídit účtování do hlavní knihy.

Následující diagram ilustruje korelaci mezi kategoriemi transakcí, sdílenými kategoriemi a kategoriemi projektů. 

Kategorie transakcí jsou základním seskupením transakcí projektu. V rámci tohoto seskupení existuje sada sdílených kategorií, které lze sdílet mezi aplikacemi a moduly. Když se dostaneme ještě dále ke konkrétnostem, kategorie projektů jsou nejpodrobnější úrovní kategorií. Kategorie projektů jsou specifické pro právnické osoby, moduly a aplikace.

![Korelace mezi kategoriemi transakcí, sdílenými kategoriemi a kategoriemi projektů.](media/project-categories.png)

## <a name="transaction-categories"></a>Kategorie transakcí

Kategorie transakcí představují základní seskupení pro projektové transakce a nejsou specifické pro společnost nebo typ transakce. Společnost Contoso Robotics například používá ke seskupení transakcí projektu kategorie Design, Travel, Installation a Service Transaction.

Kategorie transakcí jsou definovány v modulu Project Operations. 
1. Chcete-li otevřít formulář, přejděte na **Nastavení** \> **Kategorie transakcí**. 
2. Vytvořte novou kategorii transakcí výběrem **Nový** nebo výběrem **Import z aplikace Excel**.

## <a name="shared-categories"></a>Sdílené kategorie

Dynamics 365 používá koncept Sdílené kategorie ke kategorizaci výdajů v různých aplikacích, například Dynamics 365 Finance, Dynamics 365 Supply Chain a Dynamics 365 Project Operations. Pro každou vytvořenou kategorii transakcí projektové operace automaticky vytvoří čtyři související sdílené kategorie: hodiny, výdaje, poplatky a položka. Sdílené kategorie můžete zkontrolovat a upravit na **Řízení projektů a účetnictví** \> **Nastavit** \> **Kategorie** \> **Sdílené kategorie**.

## <a name="project-categories"></a>Kategorie projektů

Kategorie projektu představují nejpodrobnější úroveň konfigurace kategorií a musí být nakonfigurovány samostatně a pro každou společnost účetním projektu.

1. Přejděte na **Řízení projektů a účetnictví** \> **Nastavit** \> **Kategorie** \> **Kategorie projektu**.
2. Vyberte **Nové**.
3. Vyberte **ID kategorie** sdílené kategorie, kterou jste vytvořili v předchozí části. Project Operations umožňuje používat pouze ty sdílené kategorie, které jsou spojeny s kategoriemi transakcí.
4. Vyberte skupinu kategorií.

## <a name="category-groups"></a>Skupiny kategorií

Skupiny kategorií se používají ke sdílení vlastností, zejména zveřejňování profilů, mezi souvisejícími kategoriemi projektu. Pro každý typ transakce musí existovat alespoň jedna skupina kategorií a každé kategorii projektu je přiřazena skupina.

Specifikace účtování v Project Operations jsou definovány pravidly profilu nákladů a výnosů profilu projektu, kategoriemi projektů a skupinami kategorií. Skupiny kategorií můžete nastavit přechodem na **Řízení projektů a účetnictví** \> **Nastavit** \> **Kategorie** \> **Skupiny kategorií**.
