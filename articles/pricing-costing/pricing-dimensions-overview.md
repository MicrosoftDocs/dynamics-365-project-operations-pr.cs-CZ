---
title: Přehled cenových dimenzí
description: Toto téma obsahuje informace o cenových dimenzích v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898208"
---
# <a name="pricing-dimensions-overview"></a>Přehled cenových dimenzí

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dimenze používané v lidských zdrojích k nastavení cen a nákladů spadají do dvou kategorií:

- Lidé
- Naplánovaná práce

Z tohoto důvodu jsou k dispozici dva typy hodnot cenové dimenze:

- **Sady možností**: Dimenze, které jsou pevnými výčty pro sadu hodnot.
- **Hodnoty založené na entitě**: Dimenze, které mohou být různé sady hodnot.

## <a name="pricing-dimensions"></a>Cenové dimenze

Dynamics 365 Project Operations se dodává s výchozí sadou cenových dimenzí. Tyto cenové dimenze můžete zobrazit přechodem na **Project Operations** > **Parametry**. V záznamu parametru na kartě **Cenové dimenze založené na částce** ověřte, že role **msdyn_resourcecategory** a organizační jednotka zdroje **msdyn_organizationalunit** mají pole **Použitelné pro prodej** a **Použitelné pro náklady** nastavená na **Ano**. Když jsou tato pole povolena, můžete nastavit cenu a náklady pro každou kombinaci role a organizační jednotky.

Potřebujete-li své zdroje ocenit nebo vyjádřit náklady na ně pomocí dalších atributů, můžete vytvořit přizpůsobená pole, entity a dimenze.

## <a name="pricing-human-resource-time"></a>Ocenění času lidského zdroje
Způsob, jakým organizace oceňuje čas lidského zdroje, je často důležitým strategickým aspektem, který přímo ovlivňuje ziskovost organizace. V případě, že vaše organizace je připravena určit, jakým způsobem chce vytvořit sazby fakturace a nákladové sazby pro čas lidského zdroje, pracujte s finančními týmy a vedoucími praxe.

Další úvahy týkající se tvorby cen zahrnují to, zda se mají znovu použít pole nebo entity, které aktuálně nejsou cenovými dimenzemi, ale které se použijí jako cenové dimenze pro vaši organizaci. Pole jako **Kategorie transakce** (**msdyn_transactioncategory**) a **Rezervovatelný zdroj** (**bookableresource**) jsou příklady kandidátských dimenzí. 

Zvažte, zda by vaší cenovou dimenzí měla být tabulka nebo sada možností. Pokud předvídáte změny hodnot dimenze, které budou vyšší než 10 nebo 12, a potřebujete pro tyto hodnoty další atributy, mohli byste vytvořit spíše entitu než sadu možností. Správa sada možností, jako např. přidání nebo odebrání hodnot, vyžaduje správce nebo vývojáře, zatímco přidání nových řádků do tabulky může provádět většina uživatelů.

Následující příklad zobrazuje sazby fakturace, nastavené na základě role a organizační jednotce zdroje, ke které zdroj patří. Nákladové sazby jsou obvykle založeny na mzdovém pásmu zaměstnance a organizační jednotky, do které patří. V tomto příkladu budou tabulky fakturačnícch sazeb a nákladových sazeb vypadat následovně.

**Ukázkové fakturační sazby**

| Role        | Organizační jednotka    |Jednotka      |Cena      |Měna  |
| ------------|-------------|----------|----------:|----------|
| Vývojář   | Contoso US  |Hour | 200|USD     |
| Vývojář   | Contoso India |Hour|   112|USD     |


**Příklad nákladových sazeb**

| Mzdové pásmo     | Organizační jednotka    |Jednotka      |Cena      |Měna  |
| ----------------|-------------|----------|----------:|----------|
| Moje company_Band1 | Contoso US  |Hour | 145|USD     |
| Moje company_Band2 | Contoso India |Hour|   67|USD     |
