---
title: Správa komplexních jednotek, jako jsou na uživatele nebo za měsíc pro řádky nabídek založené na produktu
description: Tento článek poskytuje informace o správě složitých jednotek pro řádky nabídek založené na produktech.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50151e9a34e8608c98e406a30131c1efc4bf2f11
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825463"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Správa komplexních jednotek, jako jsou na uživatele nebo za měsíc pro řádky nabídek založené na produktu

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Dynamics 365 Project Operations používá množstevní faktory pro podporu prodeje produktů založených na předplatném. U produktů založených na předplatném je množství v nabídce nebo na řádku projektové smlouvy vyjádřeno jako počet uživatelských měsíců.

Cena předplaceného softwaru je v katalogu obvykle uložena jako cena za uživatele za měsíc. Během prodejního procesu je cena na řádku nabídky obvykle cena za uživatele za měsíc, která byla sjednána prodejním agentem IT a po uplatnění slevy. Každá dohoda má různý počet uživatelů a různý počet měsíců předplatného. Množství použité k výpočtu řádku nabídky je součin počtu uživatelů a počtu měsíců předplatného.

Za účelem podpory tohoto typu prodeje byl v Project Operations zaveden koncept množstevních faktorů. Množstevní faktory závisí na atributech produktu v Dynamics 365. Při konfiguraci určitých vlastností produktu umožňuje Project Operations označit podmnožinu těchto vlastností nebo všechny vlastnosti jako množstevní faktory.

Project Operations ověřuje, zda jsou jako množstevní faktory označeny pouze numerické vlastnosti nebo vlastnosti produktu, které mají číselný datový typ. Když do řádku nabídky přidáte produkt s množstevními faktory, pole **Množství** se zamkne pouze ke čtení. Po zadání hodnot vlastností produktu, které jsou množstevními faktory, Project Operations vypočítá množství řádku nabídky.

Dynamics 365 Sales může mít například následující vlastnosti:

- **Počet uživatelů**: počet uživatelů
- **Poč. měsíců**: počet měsíců předplatného
- **Jednotka SKU produktu**

Vlastnosti **Počet uživatelů** a **Počet měsíců** můžete označit příznakem množstevní faktoru pomocí úpravy vlastností řádku produktu.

Chcete-li vytvořit kvantitativní faktory z vlastností produktu, postupujte takto:

1. V levém navigačním podokně Project Operations přejděte na nabídku **Prodej** > **Produkty**.
2. Otevřete produkt, pro který potřebujete konfigurovat množstevní faktory. Ujistěte se, že produkt má již nakonfigurované vlastnosti.
3. Na stránce **Informace o projektu** pro produkt vyberte kartu **Množstevní faktory**.
4. V podřízené mřížce vyberte položku **+ Nový výpočet pole**.
5. Zadejte název množstevního faktoru a vyberte hodnotu vlastnosti, která se mapuje na výpočet pole.
6. Uložte a zavřete formulář. Opakujte tyto kroky pro všechny vlastnosti, které se mají použít pro výpočet množství pro řádek nabídky založené na produktu.

Když pro produkt vytvoříte řádek nabídky založené na produktu, množství řádku nabídky se uzamkne. Množství bude vypočítáno jako součin hodnot vlastností, které zadáte pro daný řádek nabídky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
