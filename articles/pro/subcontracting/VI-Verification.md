---
title: Ověřování faktur dodavatele se schválenými skutečnými hodnotami
description: Tento článek vysvětluje, jak Microsoft Dynamics 365 Project Operations dovoluje projektovým manažerům ověřovat faktury dodavatelů se skutečnými údaji, které byly schváleny, když dodavatelé provedli práci a zaznamenali čas, a náklady a materiály, které členové projektového týmu použili.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 43f47a44260d1a47437846f2764b56f680d4b682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914210"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Ověřování faktur dodavatele se schválenými skutečnými hodnotami

[!include [banner](../../includes/dataverse-preview.md)]

**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci

Microsoft Dynamics 365 Project Operations nechává projektové manažery ověřit řádky dodavatelské faktury následujícími způsoby:

- Použití pole **Stav ověření** na řádcích faktury dodavatele.
- Pokud řádky faktury dodavatele odkazují na řádek subdodávky, propojte skutečné náklady z činnosti subdodavatele s těmito řádky faktury dodavatele. Propojení se vytvoří spárováním skutečných nákladů s řádky faktury dodavatele.

    > [!NOTE]
    > Přestože lze stav ověření sledovat u řádků faktur dodavatele, které neodkazují na subdodávku, skutečné náklady nelze propojit s těmito řádky faktur dodavatele.

## <a name="verification-status"></a>Stav ověření

Pole **Stav ověření** na řádku faktury dodavatele označuje tento stav ověření. Podporovány jsou následující stavy:

1. Nezahájeno
2. Probíhající
3. Dokončit

Upravit lze řádky faktur dodavatele, které mají stav ověření **Nespuštěno**.

Řádky faktur dodavatele, které mají stav ověření **Probíhá**, již upravit nelze. U řádku faktury dodavatele, který odkazuje na subdodávku, je stav ověření automaticky nastaven na **Probíhá**, jakmile se první skutečné náklady přiřadí k řádku faktury dodavatele.

Řádky faktur dodavatele, které mají stav ověření **Dokončeno**, již upravit nelze. Jakmile mají všechny řádky na faktuře dodavatele tento stav ověření, fakturu dodavatele lze potvrdit.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Spárujte skutečné hodnoty nákladů s řádky faktury dodavatele

Párování skutečných nákladů pomáhá s procesem ověřování na řádku faktury dodavatele. Chcete-li přiřadit skutečné náklady k řádku faktury dodavatele, postupujte takto.

1. Otevřete řádek faktury dodavatele a vyberte kartu **Nespárované skutečné náklady**. Mřížka zobrazuje seznam skutečných nákladů, které odkazují na stejný řádek subdodávky jako řádek faktury dodavatele.
2. Vyberte jednu nebo více skutečných nákladů a poté vyberte **Párovat** na panelu nástrojů nad mřížkou. Systém ověří, že vybrané skutečné náklady lze spárovat. Po provedení ověření se skutečné náklady propojí s řádkem faktury dodavatele.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Ověřovací kritéria, která se používají k propojení skutečných nákladů s řádky faktury dodavatele

Během procesu párování lze vytvořit vazbu mezi skutečnými náklady a řádkem faktury dodavatele, pouze pokud jsou splněny obě následující podmínky:

- Pole **Stav úpravy** pro každou vybraný skutečný náklad musí být prázdné. Jinými slovy, skutečné náklady nesmí být nahrazeny jinými skutečnými náklady během procesu stahování, zrušení schválení nebo opravného deníku.
- Hodnoty následujících polí jsou spárovány mezi řádkem faktury dodavatele a vybranými skutečnými náklady. Není-li na řádku faktury dodavatele nastaveno žádné pole, není bráno v úvahu pro párování.

    - Projektová smlouva
    - Řádek projektové smlouvy
    - Třída transakce
    - Project
    - Úloha
    - Kategorie zdroje
    - Kategorie transakce
    - Produkt
    - Řádek subdodávky
    - Rezervovatelný zdroj

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Zrušit párování skutečných nákladů z řádku faktury dodavatele

Odstranění spárování skutečných nákladů může také pomoci s procesem ověření na faktuře dodavatele tím, že umožní odstranit dříve vytvořené odkazy. Pro skutečné náklady lze zrušit párování pouze z řádků faktur dodavatele, které mají stav ověření **Probíhá**. Chcete-li zrušit párování skutečných nákladů z řádku faktury dodavatele, postupujte takto.

1. Otevřete řádek faktury dodavatele a vyberte kartu **Spárované skutečné náklady**. Mřížka zobrazuje seznam skutečných nákladů, které odkazují na řádek faktury dodavatele.
2. Vyberte jednu nebo více skutečných nákladů a poté vyberte **Zrušení párování** na panelu nástrojů nad mřížkou.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
