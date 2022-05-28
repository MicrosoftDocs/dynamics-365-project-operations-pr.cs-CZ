---
title: Používání kategorií zásobování s projektovými nákupními objednávkami a nevyřízenými fakturami dodavatele
description: Tento téma popisuje, jak konfigurovat kategorie zásobování, které lze použít s projektovými nákupními objednávkami a nevyřízenými fakturami dodavatele.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613264"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Používání kategorií zásobování s projektovými nákupními objednávkami a nevyřízenými fakturami dodavatele

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Nákupčí mohou vytvářet a udržovat katalogy položek a služeb, které lze použít v projektových nákupních objednávkách a nevyřízených fakturách dodavatele. [Katalogy zásobování](/dynamics365/supply-chain/procurement/procurement-catalogs) vám nabízejí snadný způsob, jak kategorizovat nákupy, aniž byste museli konfigurovat a používat katalog vydaných produktů. Každou kategorii zásobování lze namapovat na kategorii projektu pro transakce času, výdajů nebo položek. Po zaúčtování čekající faktury dodavatele, která používá kategorii zásobování, vytvoří systém skutečné časové, výdajové nebo materiálové projektové hodnoty, transakce projektu a položky dílčí hlavní knihy.

## <a name="minimum-version-requirements"></a>Minimální požadovaná verze

K použití kategorií zásobování s projektovými nákupními objednávkami pro scénáře založené na zdrojích/položkách, které nejsou na skladě aplikace Microsoft Dynamics 365 Project Operations jsou vyžadovány následující verze:

- Řešení Project Operations Dataverse verze 4.41.0.45 nebo novější
- Prostředí finančních a provozních aplikací verze 10.0.26 nebo novější

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Spuštění map duálního zápisu pro podporu kategorií zásobování

Ujistěte se, že mapování pro **entitu exportu řádku dodavatelské faktury projektu integrace Project Operations msdyn\_projectvendorinvoicelines** používá verzi 1.0.0.4 nebo novější.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Povolní klíče funkce pro kategorie nákupu

Chcete-li povolit funkce pro použití kategorií zásobování s nákupními objednávkami projektu, postupujte podle těchto kroků.

1. V Dynamics 365 Finance otevřete pracovní prostor **Správa funkcí**.
1. V seznamu funkcí vyhledejte funkci **Používat kategorie zásobování v Project Operations pro scénáře založené na zdrojích / neskladových položkách** a poté vyberte položku **Povolit**.

> [!IMPORTANT]
> Zapnout musíte také funkci **Povolit nevyřízené faktury dodavatelů v Project Operations u scénářů založených na zdrojích/položkách, které nejsou na skladě**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapování projektových kategorií v hierarchii kategorií Zásobování

Chcete-li namapovat kategorie projektů na kategorie zásobování v hierarchii **Kategorie zásobování**, postupujte podle těchto kroků:

1. Přejděte do nabídky **Zásobování a zdroje \> Kategorie zásobování**.
1. Vyberte **Upravit hierarchii kategorií**.
1. Vyberte požadovaný uzel hierarchie kategorií a poté na kartě **Přiřadit kategorie projektů** asociujte uzel s kategorií projektu z kategorie **Čas**, Výdaj, popř. **Položka projektu** (tj. kategorie **Výchozí čas** nebo **Výchozí výdaje**).
1. Vyberte **Uložit**.
1. Zavřete stránku.

> [!NOTE]
> Mapování kategorie zásobování na kategorii projektu je volitelné. Pokud kategorie nákupu není mapována, systém použije hodnotu nastavenou v poli **Položka** v sekci **Výchozí kategorie projektu** na kartě **Project Operations v Dynamics 365 Customer engagement** ve stránce **Parametry modulu Řízení a účetnictví projektu**.
