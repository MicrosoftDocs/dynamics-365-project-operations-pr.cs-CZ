---
title: Domovská stránka cenových a nákladových dimenzí
description: Toto téma obsahuje přehled cenových dimenzí.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750316"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Domovská stránka cenových a nákladových dimenzí

Dimenze používané v lidských zdrojích k nastavení cen a nákladů spadají do dvou kategorií:

- Lidé
- Naplánovaná práce

Z tohoto důvodu jsou v Project Service Automation (PSA) k dispozici dva typy hodnot cenové dimenze: 

- **Sady možností** – dimenze, které jsou pevnými výčty pro sadu hodnot.
- **Hodnoty založené na entitě** – dimenze, které mohou být různé sady hodnot.

## <a name="pricing-dimensions"></a>Cenové dimenze

PSA se dodává s výchozí sadou cenových dimenzí. Můžete je zobrazit pomocí **Project Service** > **Parametry**. V záznamu parametru na kartě **Cenové dimenze založené na částce** ověřte, že role **msdyn_resourcecategory** a organizační jednotka zdroje **msdyn_organizationalunit** mají pole **Použitelné pro prodej** a **Použitelné pro náklady** nastavená na **Ano**. To vám umožní nastavit cenu a náklady pro každou kombinaci role a organizační jednotky.

![Snímek obrazovky parametrů Project Service se zvýrazněním „Použitelné na prodej”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Pokud jste před verzí 3 PSA jako cenové dimenze používali připravená pole role a organizační jednotky, nezaznamenáte žádné zjistitelné změny. Službu Project Service můžete nadále používat obvyklým způsobem. 

Potřebujete-li své zdroje ocenit nebo vyjádřit náklady na ně pomocí dalších atributů, můžete vytvořit přizpůsobená pole, entity a dimenze. Další informace naleznete v následujících tématech, ale mějte na vědomí, že je nutné dokončit postupy v uvedeném pořadí:

- [Vytvoření vlastních polí a entit](create-custom-fields-entities.md)
- [Přidání vlastních polí do nastavení ceny a transakčních entit](field-references.md)
- [Nastavení vlastních polí jako cenových dimenzí](set-up-pricing-dimensions.md)
- [Aktualizace atributů modulů plug-in tak, aby zahrnovaly nové cenové dimenze](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Ocenění času lidského zdroje
Způsob, jakým organizace oceňuje čas lidského zdroje, je často důležitým strategickým aspektem, který přímo ovlivňuje ziskovost organizace. V případě, že vaše organizace je připravena určit, jakým způsobem chce vytvořit sazby fakturace a nákladové sazby pro čas lidského zdroje, pracujte s finančními týmy a vedoucími praxe.

Další úvahy týkající se tvorby cen zahrnují to, zda se mají znovu použít pole nebo entity, které aktuálně nejsou cenovými dimenzemi, ale které se použijí jako cenové dimenze pro vaši organizaci. Pole jako **Kategorie transakce** (**msdyn_transactioncategory**) a **Rezervovatelný zdroj** (**bookableresource**) jsou příklady kandidátských dimenzí. 

Měli byste také zvážit, zda by vaší cenovou dimenzí měla být tabulka nebo sada možností. Pokud předvídáte změny hodnot dimenze, které budou vyšší než 10 nebo 12, a potřebujete pro tyto hodnoty další atributy, mohli byste vytvořit spíše entitu než sadu možností. Správa sada možností, jako např. přidání nebo odebrání hodnot, vyžaduje správce nebo vývojáře, zatímco přidání nových řádků do tabulky může provádět většina uživatelů.

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
