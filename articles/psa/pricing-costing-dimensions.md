---
title: Domovská stránka cenových a nákladových dimenzí
description: Toto téma obsahuje přehled cenových dimenzí.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9a2e2f7ed394229bbc553af9e616a6f322857195
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009248"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Domovská stránka cenových a nákladových dimenzí

[!include [banner](../includes/psa-now-project-operations.md)]

Dimenze používané k nastavení cen práce a nákladů v projektových organizacích jsou ovlivněny následujícími atributy:

- Lidé dělají práci dle svých zkušeností, rolí nebo geografie.
- Práce, která má být provedena dle složitosti nebo denní doby

Vzhledem k typické povaze těchto atributů práce a osob vyžadovaných k provedení práce jsou v Project Service Automation k dispozici dva typy hodnot dimenzí cen: 

- **Sady možností**: atributy, které jsou pevnými výčty pro sadu hodnot.
- **Hodnoty založené na entitách** - Atributy, které mohou mít různou sadu hodnot, které jsou konečné, ale mohou se časem měnit.

## <a name="pricing-dimensions"></a>Cenové dimenze

PSA se dodává s výchozí sadou cenových dimenzí. Můžete je zobrazit pomocí **Project Service** > **Parametry**. V záznamu parametru na kartě **Cenové dimenze založené na částce** ověřte, že role **msdyn_resourcecategory** a organizační jednotka zdroje **msdyn_organizationalunit** mají pole **Použitelné pro prodej** a **Použitelné pro náklady** nastavená na **Ano**. To vám umožní nastavit cenu a náklady pro každou kombinaci role a organizační jednotky.

![Snímek obrazovky parametrů Project Service se zvýrazněním „Použitelné na prodej”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Pokud jste před verzí 3 PSA jako cenové dimenze používali připravená pole role a organizační jednotky, nezaznamenáte žádné zjistitelné změny. Službu Project Service můžete nadále používat obvyklým způsobem. 

Potřebujete-li své zdroje ocenit nebo vyjádřit náklady na ně pomocí dalších atributů, můžete vytvořit přizpůsobená pole, entity a dimenze. Další informace naleznete v následujících tématech, ale mějte na vědomí, že je nutné dokončit postupy v uvedeném pořadí:

- [Vytvoření vlastních polí a entit](create-custom-fields-entities.md)
- [Přidání vlastních polí do nastavení ceny a transakčních entit](field-references.md)
- [Nastavení vlastních polí jako cenových dimenzí ](set-up-pricing-dimensions.md)
- [Aktualizace atributů modulů plug-in tak, aby zahrnovaly nové cenové dimenze](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Ocenění času lidského zdroje
Způsob, jakým organizace oceňuje čas lidského zdroje, je často důležitým strategickým aspektem, který přímo ovlivňuje ziskovost organizace. V případě, že vaše organizace je připravena určit, jakým způsobem chce vytvořit sazby fakturace a nákladové sazby pro čas lidského zdroje, pracujte s finančními týmy a vedoucími praxe.

Další úvahy týkající se tvorby cen zahrnují to, zda se mají znovu použít pole nebo entity, které aktuálně nejsou cenovými dimenzemi, ale které se použijí jako cenové dimenze pro vaši organizaci. Pole jako **Kategorie transakce** (**msdyn_transactioncategory**) a **Rezervovatelný zdroj** (**bookableresource**) jsou příklady kandidátských dimenzí. 

Zvažte, zda by vaší cenovou dimenzí měla být tabulka nebo sada možností. Pokud předvídáte změny hodnot dimenze, které budou vyšší než 10 nebo 12, a potřebujete pro tyto hodnoty další atributy, vytvořte spíše entitu než sadu možností. Správa sada možností, jako např. přidání nebo odebrání hodnot, vyžaduje správce nebo vývojáře, zatímco přidání nových řádků do tabulky může provádět většina obchodních uživatelů.

Následující příklad zobrazuje sazby fakturace, nastavené na základě role a organizační jednotce zdroje, ke které zdroj patří. Nákladové sazby jsou obvykle založeny na mzdovém pásmu zaměstnance a organizační jednotky, do které patří. V tomto příkladu budou tabulky fakturačnícch sazeb a nákladových sazeb vypadat následovně.

**Ukázkové fakturační sazby**

| Role        | Organizační jednotka    |Jednotka      |Cena      |Měna  |
| ------------|-------------|----------|----------:|----------|
| Vývojář   | Contoso (USA)  |hod | 200|USD     |
| Vývojář   | Contoso India |hod|   112|USD     |


**Příklad nákladových sazeb**

| Mzdové pásmo     | Organizační jednotka    |Jednotka      |Cena      |Měna  |
| ----------------|-------------|----------|----------:|----------|
| Moje company_Band1 | Contoso (USA)  |hod | 145|USD     |
| Moje company_Band2 | Contoso India |hod|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]