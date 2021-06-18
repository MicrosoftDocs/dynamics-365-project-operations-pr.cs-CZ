---
title: Nákupní objednávky pro projekt
description: Tento článek popisuje různé metody, které můžete použít k vytvoření nákupních objednávek pro projekt. Metoda, kterou použijete, závisí na účelu nákupní objednávky a na tom, kdy jsou zakoupené položky spotřebovány a účtovány projektu.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999348"
---
# <a name="purchase-orders-for-a-project"></a>Nákupní objednávky pro projekt

[!include [banner](../includes/banner.md)]

Tento článek popisuje různé metody, které můžete použít k vytvoření nákupních objednávek pro projekt. Metoda, kterou použijete, závisí na účelu nákupní objednávky a na tom, kdy jsou zakoupené položky spotřebovány a účtovány projektu.

### <a name="methods-for-creating-a-purchase-order"></a>Metody pro vytvoření nákupní objednávky

K vytvoření nákupní objednávky ve Správě projektů a účetnictví můžete použít jednu z následujících metod. Účel nákupní objednávky určuje, kdy bude tato spotřebována a tedy i to, kdy budou její položky účtovány projektu.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Způsob</th>
<th>Účel</th>
<th>Spotřeba položek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vytvořte nákupní objednávku přímo z projektu.</td>
<td>Tuto metodu použijte k nákupu položek od externího dodavatele, určených ke spotřebě v projektu. Nákupní objednávku můžete vytvořit dvěma způsoby:
<ul>
<li>Přímo z projektu. V tomto případě je projekt již pro nákupní objednávku definován.</li>
<li>Přechodem k nákupní objednávce projektu. Chcete-li vytvořit nákupní objednávku, musíte vybrat dodavatele i projekt.</li>
</ul></td>
<td>Položky se spotřebovávají při aktualizaci faktury dodavatele.</td>
</tr>
<tr class="even">
<td>Vytvořte nákupní objednávku z prodejní objednávky.</td>
<td>Tuto metodu použijte k nákupu položek při vytváření prodejní objednávky z projektu.</td>
<td>Položky jsou spotřebovány, když je prodejní objednávka fakturována zákazníkovi.</td>
</tr>
<tr class="odd">
<td>Vytvořte nákupní objednávku z požadavku na položku.</td>
<td>Tuto metodu použijte k nákupu položek při vytváření požadavku na položku z projektu.</td>
<td>Položky se spotřebovávají, když se aktualizuje dodací list s požadavkem na položku.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Když aktualizujete fakturu dodavatele nebo dodací list, budete vyzváni k aktualizaci dodacího listu v požadavku na položku.

Další informace viz téma [Příjem položek na nákupní objednávce z požadavku na položku](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]