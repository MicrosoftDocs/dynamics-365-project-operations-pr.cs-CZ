---
title: Nastavit subdodavatele jako rezervovatelné zdroje
description: Tento téma vysvětluje, jak nastavit a udržovat prostředky subdodavatelů, které jsou vytvořeny od uživatelů a kontaktů v systému, aby je bylo možné spojovat se subdodávkami v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994178"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Nastavit subdodavatele jako rezervovatelné zdroje

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Chcete-li nastavit subdodavatele jako rezervovatelné zdroje v Microsoft Dynamics 365 Project Operations, postupujte takto.

1. Přejděte na **Projekt** \> **Zdroje** a vyberte **Nový**.
2. Na stránce **Nový rezervovatelný zdroj** v poli **Typ zdroje** vyberte jednu z následujících možností:

    - **Uživatel** - Tento typ zdroje vyberte, pokud má subdodavatel přístup k Project Operations, aby zadal čas nebo výdaje. Pokud zvolíte **Uživatel**, subdodavatel vyžaduje pro přístup do systému platnou licenci.
    - **Kontakt** nebo **Obchodní vztah** - Vyberte jeden z těchto typů zdrojů, pokud subdodavatel nevyžaduje přístup k Project Operations, ale musí být k dispozici pro přiřazování úkolů nebo rezervace projektů. Žádný z těchto typů prostředků neposkytuje přístup k systému. Vyberte **Obchodní vztah**, chcete-li reprezentovat společnost dodavatele jako rezervovatelný zdroj. Vyberte **Kontakt**, chcete-li zastupovat jednotlivé zaměstnance dodavatele.

3. V závislosti na typu zdroje, který jste vybrali, budete vyzváni k výběru příslušného záznamu uživatele, obchodního vztahu nebo kontaktu.
4. V poli **Typ pracovníka** vyberte „Smluvní pracovník“ a nastavte subdodavatele jako rezervovatelný zdroj.

    > [!NOTE]
    > Pokud necháte pole **Typ pracovníka** prázdné, rezervovatelný zdroj bude považován za zaměstnance.

5. Pokud jste vybrali **Smluvní pracovník** jako typ pracovníka, vyberte dodavatele, pro kterého prostředek pracuje.
6. Vyberte časové pásmo prostředku a poté vyberte **Uložit**. Chcete-li přiřadit šablonu pracovní doby rezervovatelnému zdroji, můžete vybrat **Nastavit kalendář** na stránce seznamu **Rezervovatelný zdroj**.

Aby mohl být rezervovatelný zdroj přidružený k řádku subdodávky, musí splnit následující podmínky:

- Rezervovatelný zdroj musí být smluvní pracovník.
- Rezervovatelný zdroj typu zdroje **Kontakt** musí být spojen s účtem dodavatele jako kontakt. Rezervovatelný zdroj typu zdroje **Uživatel** nemusí být spojen s účtem dodavatele jako kontakt.
- Hodnota pole **Prodejce** pro rezervovatelný zdroj se musí shodovat s hodnotou pole **Prodejce** pro subdodávku.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Aktualizujte typ mapování pracovníků a dodavatelů pro rezervovatelné zdroje

Pole **Typ pracovníka** pro rezervovatelný zdroj určuje, zda je rezervovatelným zdrojem smluvní pracovník nebo zaměstnanec. Pole **Prodejce** definuje účet dodavatele, ke kterému je rezervovatelný zdroj přidružen. Přiřazením rezervovatelného zdroje k prodejci jako kontaktu označujete, že kontakt je zaměstnancem společnosti prodejce.

Pokud se pole **Typ pracovníka** a **Prodejce** pro rezervovatelný zdroj změní, změny ovlivní veškerá budoucí ověření nových záznamů, která rezervovatelný zdroj vytvoří, například časové záznamy. Změny však nezruší platnost stávajících záznamů.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
