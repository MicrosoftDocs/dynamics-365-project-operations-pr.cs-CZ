---
title: Zdroje řádku subdodávky
description: Tento téma vysvětluje, jak určit vyhrazené zdroje, které poskytuje dodavatel pro konkrétní řádek subdodávky na čas.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4a929b985a51ab49d3e34ce4a5c277af4c05c216
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558449"
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
4. Na stránce **Nový zdroj řádku subdodávky** zadejte požadované informace a poté vyberte **Uložit a zavřít**.

V následující tabulce jsou vysvětlena pole zdroje řádku subdodávky.

| Pole | Popis | Funkční dopad |
| ----- | ----------- | ----------------- |
| Rezervovatelný zdroj | Vyberte rezervovatelný zdroj typu **Smluvní pracovník**, který chcete použít jako zdroj na řádku subdodávky.| Pokud jste pro smluvního pracovníka nevytvořili rezervovatelný zdroj, ponechte toto pole prázdné. Při uložení záznamu bude vytvořen rezervovatelný zdroj.  |
| Kontakt | Zdroj řádku subdodávky můžete vytvořit z existujícího kontaktu. Pomocí vyhledávání zobrazíte seznam aktivních kontaktů v systému. Vyberte kontakt pro dodavatele této subdodávky. Pokud kontakt, který jste vybrali, není platným kontaktem pro dodavatele na subdodávce, záznam zdroje řádku subdodávky nebude uložen.| Pokud pro vybraný kontakt neexistuje žádný rezervovatelný zdroj, systém vytvoří rezervovatelný zdroj pro vybraný kontakt před vytvořením zdroje řádku subdodávky. |
| Uživatelská | Zdroj řádku subdodávky můžete vytvořit výběrem aktivního uživatele. Pomocí vyhledávání zobrazíte seznam aktivních uživatelů v systému.| Pokud pro vybraný kontakt neexistuje žádný rezervovatelný zdroj, systém vytvoří rezervovatelný zdroj pro vybraného uživatele před vytvořením zdroje řádku subdodávky. |
| Počáteční datum | Datum, kdy začne přiřazení pracovníka subdodávky.| Pokud je tento zdroj rezervován na období, které patří před toto časové období, dojde k varování. |
| Koncové datum | Datum, kdy je dokončeno přiřazení pracovníka subdodávky.| Pokud je tento zdroj rezervován na období, které patří do období po tomto rozsahu, dojde k varování. |
| Úsilí | Celkový počet hodin úsilí, které smluvní pracovník stráví na tomto řádku subdodávky.| Pokud je tento zdroj rezervován nad rámec úsilí, které je přiděleno této subdodávce, dojde k varování. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]