---
title: Fakturace dodavatele - koncept a tvorba
description: Tento téma popisuje koncept dodavatelských faktur, scénáře použití a způsob vytváření dodavatelských faktur v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580540"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Fakturace dodavatele - koncept a tvorba

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Fakturace dodavatele v Microsoft Dynamics 365 Project Operations lze použít k evidenci nákladů na dodávky služeb a/nebo materiálů na projektu od dodavatelů.

Když jsou služby a/nebo materiály zadány dodavateli subdodávkou, představuje subdodávka smluvní dohodu s tímto dodavatelem. Jak dodavatel dodává služby nebo jsou materiály přijímány a používány na projektových úkolech, náklady jsou zaznamenány v projektu. Dodavatel pravidelně zasílá faktury, které jsou ověřeny a spárovány s náklady zaznamenanými v projektu. Po dokončení procesu ověření je faktura dodavatele potvrzena a uvolněna k platbě.

## <a name="scenarios-for-use"></a>Scénáře použití

Faktury dodavatele v Project Operations lze použít k podpoře dvou odlišných scénářů.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Zákazníci využívají plné možnosti subdodávek

Zkušenosti s fakturami dodavatele poskytují způsob, jak ověřit a spárovat položky času, spotřeby materiálu a položek výdajů, které odkazují na subdodavatelské komponenty s řádky faktur dodavatele. Tento proces lze použít k ověření správnosti řádků faktury dodavatele. Po dokončení ověřovacího procesu a potvrzení faktury dodavatele aplikace stornuje skutečné skutečnosti, které byly zaznamenány schválenými protokoly využití času, výdajů a materiálu, a vytvoří nové skutečné náklady pomocí řádků faktury dodavatele.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Zákazníci nevyužívají plné subdodavatelské zkušenosti, ale chtějí mít jednotný pohled na náklady na projekty v Project Operations

Pokud sledujete proces subdodávek v systému třetí strany, můžete zaznamenat náklady z tohoto systému třetí strany do Project Operations vytvořením faktur dodavatele, které neodkazují na subdodávky. Vaši projektoví manažeři tak mohou mít jednotný pohled na všechny náklady na daný projekt.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Vytváření dodavatelských faktur v Project Operations

Faktury dodavatele lze vytvořit dvěma způsoby:

- Na stránce se seznamem faktur dodavatele nebo na stránce podrobností pro jednu fakturu dodavatele
- Ze stránky se seznamem subdodávek nebo ze stránky s podrobnostmi pro jednu subdodávku

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Vytvoření ze stránky seznamu faktur dodavatele nebo stránky podrobností

1. Přejděte na **Nákup** \> **Faktury dodavatele**.
2. Na stránce se seznamem faktur dodavatele nebo na stránce podrobností pro jednu fakturu dodavatele vyberte **Nová** k vytvoření nové faktury dodavatele.

Faktury dodavatele, které jsou vytvořeny tímto způsobem, mohou také odkazovat na subdodávku.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Vytvoření ze stránky seznamu subdodávak nebo stránky podrobností

1. Přejděte na **Nákup** \> **Subdodávky**.
2. Vyberte jednu nebo více subdodávek.
3. Na stránce se seznamem subdodávek nebo na stránce podrobností pro jednu subdodávku vyberte **Vytvořit fakturu dodavatele** k vytvoření nové faktury dodavatele.

Nová faktura dodavatele ve stavu **Koncept** je vytvořena pro každou subdodávku, kterou jste vybrali.

Faktury dodavatele, které vytvoříte tímto způsobem, vždy odkazují na subdodávku v záhlaví faktury dodavatele. Každý řádek v subdodávce, který má metodu účtování podle času a materiálu, způsobí vytvoření řádku na faktuře dodavatele. Každý řádek v subdodávce, který má metodu fakturace s pevnou cenou, způsobí vytvoření řádku na faktuře dodavatele pro každý milník řádku subdodávky, který má stav **Připraveno k fakturaci**.

Následující pole a související záznamy budou zkopírovány ze subdodávky do záhlaví faktury dodavatele:

- Dodavatel.
- Související ceníky budou zkopírovány na fakturu dodavatele jako ceníky.
- Měna:
- Smluvní jednotka.
- Platební podmínky.

Pro řádky subdodávek Čas a materiál budou následující pole a související záznamy zkopírovány z řádku subdodávky do řádku faktury dodavatele:

- Subdodávka a odkazy na řádky subdodávky
- Třída transakce
- Role
- Kategorie transakce
- Pole produktu
- Project
- Úloha
- Rezervovatelný zdroj

Pro řádky subdodávek Pevná cena budou následující pole zkopírovány z řádku subdodávky milníku řádků subdodávky do řádku faktury dodavatele:

- Subdodávka a odkazy na řádky subdodávky.
- Třída transakce. Ve výchozím nastavení bude hodnota **Milník**.
- Název a částka milníku budou zkopírovány ze souvisejícího milníku řádku subdodávky.
- Uživatel bude moci vybrat projekt a úkol na řádku faktury dodavatele.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
