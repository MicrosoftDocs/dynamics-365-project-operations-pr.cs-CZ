---
title: Přehled cenových dimenzí
description: Toto téma obsahuje informace o nastavení cenových dimenzí v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 33f55976eafedd046fba952ab6381c297ab4e271
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650177"
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

![Snímek obrazovky parametrů Project Service se zvýrazněním „Použitelné na prodej”](media/PS-OOB-parameters.png)

Potřebujete-li své zdroje ocenit nebo vyjádřit náklady na ně pomocí dalších atributů, můžete vytvořit přizpůsobená pole, entity a dimenze. Další informace naleznete v následujících tématech: 
  
  > [!NOTE]
  > Postupy musí být dokončeny v pořadí, v jakém jsou uvedeny.

1. [Vytvoření řešení pro vlastní cenové dimenze](../sales/create-solution-custompd.md)
2. [Vytvoření vlastních polí a entit](create-custom-fields-entities-pricing-dimensions.md)
3. [Přidání vlastních polí do nastavení ceny a transakčních entit ](add-custom-fields-price-setup-transactional-entities.md)
4. [Nastavení vlastních polí jako cenových dimenzí ](set-up-custom-fields-pricing-dimensions.md)
5. [Aktualizace atributů modulů plug-in tak, aby zahrnovaly nové cenové dimenze](update-plugin-attributes-pd.md)


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


[!INCLUDE[footer-include](../includes/footer-banner.md)]