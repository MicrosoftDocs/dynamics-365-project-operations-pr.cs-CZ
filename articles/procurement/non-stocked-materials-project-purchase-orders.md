---
title: Objednávka neskladových materiálů projektu pomocí nákupních objednávek projektu
description: Toto téma popisuje, jak můžete objednat neskladové materiály projektu pomocí nákupních objednávek projektu.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2aa8fb94e2f9cbf91182f3f169339284d3eb9f44
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612695"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Objednávka kategorií zásobování nebo neskladových materiálů u projektů používajících projektové nákupní objednávky

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Oddělení zásobování vaší organizace může použít [nákupní objednávky](/dynamics365/supply-chain/procurement/purchase-order-overview) pro sledování objednávek zboží a služeb. Nákupní objednávky pro kategorie zásobování nebo jiné než skladové materiály lze přiřadit projektu. Fakturace těchto nákupních objednávek zaznamenává náklady projektu.

## <a name="prerequisites"></a>Předpoklady
Chcete-li povolit funkci nákupních objednávek projektu, proveďte následující kroky.

1. V Dynamics 365 Finance přejděte do pracovního prostoru **Správa funkcí**.
2. V seznamu funkcí vyhledejte a vyberte funkci **Povolit nákupní objednávky projektu v Project Operations pro scénáře založené na zdrojích / neskladových položkách**.
3. Vyberte **Povolit**.
4. Nakonfigurujte neskladové materiály a nevyřízené faktury dodavatele, jak je popsáno v části [Konfigurace neskladovaných materiálů a nevyřízené faktury dodavatele](configure-materials-nonstocked.md).
5. Konfigurujte kategorie zásobování podle popisu v článku [Používání kategorií zásobování s projektovými nákupními objednávkami a nevyřízenými fakturami dodavatele](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Vytvoření nákupní objednávky projektu ze seznamu nákupních objednávek projektu

1. V modulu Finance přejděte na **Řízení projektů a účetnictví** > **Projekty** > **Všechny projekty** a vyberte projekt.
2. V podokně Akce na kartě **Správa** ve skupině **Nová** vyberte **Úloha položky** > **Nákupní objednávka**.
3. Na stránce **Vytvoření nákupní objednávky** vyberte dodavatele, pro kterého chcete vytvořit nákupní objednávku, podle potřeby zadejte další informace a poté vyberte **OK**.
4. Na stránce **Nákupní objednávka** v mřížce **Řádky nákupní objednávky** vyberte **Přidat řádek**.
5. Podle potřeby zadejte číslo položky nebo kategorii zásobování, množství, jednotku, jednotkovou cenu a další informace.

    > [!NOTE]
    > V projektových nákupních objednávkách lze použít pouze kategorie zásobování, zboží, které není skladem, a služby. Skladové položky nejsou podporovány.

6. Pokračujte v přidávání položek nebo kategorií zásobování podle potřeby a potvrďte nákupní objednávku.

    Účtenky za zboží a služby lze zaznamenat vytvořením a zaúčtováním příjemky produktu.

    > [!NOTE]
    > Příjemky produktů se nezaznamenávají do skutečných hodnot projektu v Microsoft Dataverse a nemají vliv na dílčí hlavní knihu projektu.

    Poté, co dodavatel odešle fakturu za položky a služby v nákupní objednávce, může oddělení zásobování vygenerovat fakturu pro nákupní objednávku v části **Faktura** > **Generovat** > **Faktura** v podokně akcí. Další informace o nevyřízených fakturách dodavatele viz [Nákup neskladových materiálů pomocí nevyřízené faktury dodavatele](pending-vendor-invoices.md).
