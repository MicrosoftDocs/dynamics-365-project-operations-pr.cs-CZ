---
title: Zdroje řádku subdodávky
description: Tento téma vysvětluje, jak určit vyhrazené zdroje, které poskytuje dodavatel pro konkrétní řádek subdodávky na čas.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323363"
---
# <a name="subcontract-line-resources"></a>Zdroje řádku subdodávky

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V Dynamics 365 Project Operations, dodavatel může určit zdroje, které budou použity k zásobování kapacity zdrojů zakoupených na řádku subdodávky na čas.

## <a name="create-subcontract-line-resources"></a>Vytvořit zdroje řádku subdodávky

Chcete-li vytvořit řádek subdodávky postupujte podle následujících kroků.

1. V navigačním podokně vyberte **Subdodávky** a otevřete subdodávku, na které chcete pracovat.
2. Otevřete řádek subdodávky pro čas, pro který chcete zadat zdroje dodavatele.
3. Na kartě **Milníky řádku subdodávky** na dílčí mřížce vyberte **+ nový milník řádku subdodávky**.
4. Na stránce **Nový milník řádku subdodávky** zadejte požadované informace a vyberte **Uložit a zavřít**.

V následující tabulce jsou vysvětlena pole zdroje řádku subdodávky.

| Pole |  Popis |
| ----- | ------------ |
| Rezervovatelný zdroj | Vyberte rezervovatelný zdroj typu „Smluvní pracovník“, který chcete použít jako zdroj na řádku subdodávky. Pokud jste pro smluvního pracovníka ještě nevytvořili rezervovatelný zdroj, ponechte toto pole prázdné. Rezervovatelný zdroj se vytvoří při uložení záznamu.  |
| Kontakt | Pokud je pole **Rezervovatelný zdroj** prázdné, můžete vytvořit zdroj řádku subdodávky z existujícího kontaktu. Pomocí vyhledávání zobrazíte seznam aktivních kontaktů v systému. Vyberte kontakt pro dodavatele této subdodávky. Vybraný kontakt se ověří při uložení záznamu. Pokud vybraný kontakt není platným kontaktem, záznam se neuloží. Pokud pro vybraný kontakt neexistuje žádný rezervovatelný zdroj, systém vytvoří rezervovatelný zdroj pro vybraný kontakt před vytvořením zdroje řádku subdodávky. |
| Uživatelská | Pokud je pole **Rezervovatelný zdroj** prázdné, můžete vytvořit zdroj řádku subdodávky výběrem aktivního uživatele. Pomocí vyhledávání zobrazíte seznam aktivních uživatelů v systému. Pokud pro vybraný kontakt neexistuje žádný rezervovatelný zdroj, systém vytvoří rezervovatelný zdroj pro vybraného uživatele před vytvořením zdroje řádku subdodávky. |
| Počáteční datum | Datum, kdy začne přiřazení pracovníka subdodávky. Pokud je tento zdroj rezervován na období, které patří před toto časové období, dojde k varování. |
| Koncové datum | Datum, kdy je dokončeno přiřazení pracovníka subdodávky. Pokud je tento zdroj rezervován na období, které patří do období po tomto rozsahu, dojde k varování. |
| Úsilí | Celkový počet hodin úsilí, které pracovník subdodávky stráví na tomto řádku subdodávky. Pokud je tento zdroj rezervován nad rámec úsilí, které je této subdodávce přiděleno, dojde k varování. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
