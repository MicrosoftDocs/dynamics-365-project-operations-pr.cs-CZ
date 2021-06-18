---
title: Nastavení projektu
description: Toto téma obsahuje informace o nastavení řízení projektu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 24032a77834005c444972f8d234d3acb33d19135
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998313"
---
# <a name="project-settings"></a>Nastavení projektu

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pro přístup k funkcím plánování projektu použijte následující nastavení.

## <a name="work-template"></a>Šablona práce

Chcete-li vytvořit plán projektu, vytvořte šablonu projektového kalendáře, který definuje počet pracovních hodin denně a všechny zavírací dny. Chcete-li vytvořit šablonu kalendáře projektu, přidružte šablonu práce k poli **Šablona kalendáře** pro projekt. Při vytváření šablony práce postupujte takto.

1. V PSA klikněte v levém navigačním podokně na **Zdroje**. 
2. Na stránce se seznamem **Zdroje** otevřete záznam uživatele a pak vyberte **Zobrazit pracovní dobu**.

  > [!NOTE]
  > Ujistěte se, že na stránce prohlížeče povolíte automaticky otevíraná okna. To vám umožní zobrazit pracovní hodiny nastavené pro daný zdroj.
  
3. Na kartě **Měsíční zobrazení** klikněte na tlačítko **Nastavit**. Zobrazí se seznam se třemi možnostmi: 

  - Nový týdenní plán
  - Pracovní plán na jeden den
  - Volno

> ![Možnosti nastavení](media/project-13.png)

4. Vyberte **Nový týdenní plán** a pak nastavte možnosti pro tento plán zdrojů. Můžete nastavit opakovaný týdenní plán, parametry denní hodiny, zavírací dny a další.
5. Nastavte rozsah kalendářních dat, vyberte **Uložit** a klikněte na tlačítko **Zavřít**. 
6. Vraťte se zpět na se seznamem **Zdroje** a vyberte zdroj, pro který jste nastavili pracovní dobu. 
7. Chcete-li nastavit šablonu práce vyberte **Nastavit kalendář jako**. 
8. V dialogovém **Šablona práce** zadejte název šablony práce a pak vyberte **Použít**. 

Nyní můžete šablonu práce přidružit k šabloně kalendáře projektu.

## <a name="resource-roles"></a>Role zdrojů

Termín *Role zdroje* odkazuje na sadu dovedností, kompetencí a certifikací, které musí osoba mít k provedení specifické sady úkolů na projektu. PSA vám umožní použít nákladovou a fakturační sazbu za čas zdroje na základě role, ke které je zdroj přidružen. Každá organizace musí tyto role nastavit pomocí navigace vlevo v nabídce **Project Service**.

Každá organizace musí tyto role nastavit na stránce **Aktivní kategorie zdrojů**. Chcete-li tuto stránku otevřít, vyberte v levém navigačním podokně **Role zdrojů**.

## <a name="price-lists"></a>Ceníky

Ceníky vám umožní nastavit nákladové a prodejní ceny pro role zdrojů, kategorie výdajů, produkty a další položky v organizaci. Před nastavením finančních odhadů pro práci, která musí být dodána pro projekt, byste měli vytvořit pomocný nákladový a prodejní ceník. V sekci parametry byste měli také nastavit výchozí nákladový a prodejní ceník, který se vztahuje na všechny projekty vytvořené v organizaci. Na stránce **Aktivní projektové parametry** se ujistěte, že jste nastavili výchozí nákladový a prodejní ceník.


[!INCLUDE[footer-include](../includes/footer-banner.md)]