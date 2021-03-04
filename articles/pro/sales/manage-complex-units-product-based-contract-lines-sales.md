---
title: Správa komplexních jednotek pro řádky smlouvy založené na produktu – omezené
description: Tohle téma poskytuje informace o podpoře prodeje produktů založených na předplatném.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177368"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Správa komplexních jednotek pro řádky smlouvy založené na produktu – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Dynamics 365 Project Operations používá množstevní faktory pro podporu prodeje produktů založených na předplatném. U produktů založených na předplatném je množství ve smlouvě nebo na řádku projektové smlouvy vyjádřeno jako počet uživatelských měsíců.

Cena předplaceného softwaru je v katalogu uložena jako cena za uživatele za měsíc. Během prodejního procesu je cena na řádku smlouvy obvykle cena za uživatele za měsíc, která byla sjednána prodejním agentem a po uplatnění slevy. Každá dohoda má různý počet uživatelů a různý počet měsíců předplatného. Množství, které se používá k výpočtu částky řádku smlouvy, je součin počtu uživatelů a počtu měsíců předplatného.

Za účelem podpory tohoto typu prodeje podporuje Project Operations koncept *množstevních faktorů*. Množstevní faktory závisí na atributech produktu. Při konfiguraci určitých vlastností produktu můžete označit podmnožinu těchto vlastností nebo všechny vlastnosti jako množstevní faktory.

Project Operations ověřuje, zda jsou jako množstevní faktory označeny pouze numerické vlastnosti nebo vlastnosti produktu, které mají číselný datový typ. Když je produkt s konfigurovanými množstevními faktory přidán do řádku smlouvy, pole **Množství** se stane jen pro čtení. Po zadání hodnot vlastností produktu, které jsou množstevními faktory, Project Operations vypočítá množství řádku smlouvy.

Dynamics 365 Sales může mít například následující vlastnosti:

- **Počet uživatelů**: počet uživatelů.
- **Poč. měsíců**: počet měsíců předplatného.
- **SKU produktu**: skladová jednotka (SKU) pro produkt.

Vlastnosti **Počet uživatelů** a **Počet měsíců** lze pomocí úpravy vlastností řádku produktu označit jako množstevní faktory.

Chcete-li z vlastností produktu vytvořit množstevní faktory, proveďte následující kroky.

1. Na stránce **Project Operations** vyberte **Prodej – produkty**.
2. Otevřete produkt, pro který potřebujete nastavit množstevní faktory. Ujistěte se, že produkt má již nastavené vlastnosti.
3. Na stránce **Informace o projektu** vyberte stránku kartu **Množstevní faktory**.
4. V podřízené mřížce vyberte položku **+ Nový výpočet pole**.
5. Zadejte název **množstevního faktoru** a vyberte hodnotu vlastnosti, která se mapuje na výpočet pole.
6. Uložte a zavřete formulář.
7. Opakujte kroky 2–6 pro všechny vlastnosti, které společně tvoří množství pro řádek smlouvy na základě produktu.

S nastavenými množstevními faktory, když uživatel vytvoří pro tento produkt řádek kontraktu, je množství řádku smlouvy uzamčeno. Množství se poté vypočítá jako produkt hodnot vlastností pro daný řádek smlouvy.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]