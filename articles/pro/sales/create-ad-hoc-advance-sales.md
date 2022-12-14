---
title: Vytvoření ad hoc zálohy na projektové smlouvě
description: Tento článek poskytuje informace o vytvoření zálohy na smlouvu podle potřeby.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 62e41e5faeb5e40143e26e2cdf48c1279941a6b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824836"
---
# <a name="create-an-ad-hoc-advance-on-a-project-contract"></a>Vytvoření ad hoc zálohy na projektové smlouvě

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Microsoft Dynamics 365 Project Operations podporuje scénáře fakturace, které zahrnují platby předem a zálohy. Proces používání **Záloh** v **Project Operations** je podobný smlouvám **Záloha**. 

Chcete-li zákazníkovi fakturovat zálohu, proveďte následující kroky.

1. Přejděte na stránku **Projektová smlouva** a poté vyberte kartu **Zálohy**.
2. V podmřížce, která obsahuje seznam všech dříve zaznamenaných záloh, vyberte **+ Nová záloha projektové smlouvy**. 

    Otevře se formulář **Rychlé vytvoření** pro zaznamenání zálohy.
    
3. V tabulce níže jsou uvedena pole záznamu zálohy, které je třeba mít na paměti při vytváření nových:

    | Pole | Popis | Dopad na následné složky |
    | --- | --- | --- |
    | **Zákazník projektové smlouvy** | Toto pole označuje, kterému zákazníkovi na smlouvě bude tato záloha fakturována. | Pokud máte na smlouvě více zákazníků a chcete každému z nich fakturovat konkrétní zálohu nebo částku zálohy, vytvořte zálohu pro každého zákazníka zvlášť. |
    | **Popis** | Popis účelu nebo načasování zálohy, který pomůže tuto zálohu identifikovat. | Tento popis se zobrazuje na řádku faktury pro tuto zálohu. |
    | **Částka** | Částka zálohy. | Tato částka se zobrazuje na řádku faktury pro tuto zálohu. |
    | **Datum faktury** | Datum, kdy je tato záloha fakturována zákazníkovi. | Toto je datum, kdy má proces automatického vytváření faktur vytvořit řádek faktury pro tuto zálohu. |
    | **Stav faktury** | Toto je nastavení možnosti, které označuje, zda je tato záloha přidána do konceptu faktury pro tohoto zákazníka. Možné hodnoty jsou:</br>- **Nepřipraveno k fakturaci**</br>- **Připraveno k fakturaci** | Když je záloha označena jako **Připraveno k fakturaci**, je přidána jako čas na řádku v konceptu faktury. K vyrovnání vůči nákladům projektu na další fakturační období lze použít pouze plně fakturovanou zálohu. |

4. Vyberte **Uložit a zavřít** v dialogovém okně pro rychlé vytvoření, čímž zálohu zaznamenáte.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
