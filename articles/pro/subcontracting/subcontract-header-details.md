---
title: Podrobnosti záhlaví pro subdodávky
description: Toto téma vysvětluje funkce poskytované v záhlaví subdodávky v Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323633"
---
# <a name="header-details-for-subcontracts"></a>Podrobnosti záhlaví pro subdodávky

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma vysvětluje funkce poskytované v záhlaví subdodávky v Dynamics 365 Project Operations.

Když projektový manažer plánuje a provádí projekty, může zaměstnávat subdodavatele a nakupovat produkty a služby od prodejců. Když správce projektu potřebuje zakoupit produkty nebo služby, může vytvořit subdodávku v Project Operations.

Chcete-li vytvořit subdodávku postupujte podle následujících kroků.

1. V navigačním podokně vyberte **Subdodávky**, a na stránce **Subdodávka** vyberte **Nový**.
2. Zadejte požadované informace a zvolte **Uložit**.

    Následující tabulka obsahuje informace o polích na stránce záhlaví subdodávky.

    | **Pole** | **Popis** |
    | --- | --- | 
    | Jméno | Název subdodávky |
    | Popis | Stručný popis služeb a produktů, které jsou nakupovány na základě subdodávky. |
    | Dodavatel | Název společnosti, od které jsou produkty a služby nakupovány. Tento účet dodavatele má typ vztahu **Prodejce** nebo **Dodavatel**. |
    | Datum subdodávky | Datum vytvoření subdodávky je vytvořeno. |
    | Důvod stavu | Stav řádku subdodávky |
    | Měna | Měna, ve které se nakupují produkty a služby. Hodnota v tomto poli je výchozí z účtu dodavatele, ale lze ji změnit. Ceníky projektů, které se používají pro oceňování produktů a služeb na subdodávce, by měly být v této měně. K subdodávce nelze přiřadit ceníky v žádné jiné měně. Náklady na produkty a služby vzniklé na základě této subdodávky budou zaznamenány do projektu v této měně. |
    | Smluvní jednotka | Divize společnosti, která uzavírá kupní smlouvu nebo subdodávku s prodejcem. |
    | Platební podmínky | Platební podmínky pro faktury dodavatele vystavené na základě této subdodávky. Hodnota v tomto poli je výchozí z účtu dodavatele, ale lze ji změnit. |
    | Adresa platby | Adresa, na kterou jsou zasílány platby faktur dodavatele. Hodnota v tomto poli je výchozí z účtu dodavatele, ale lze ji změnit. |
    | Fakturační adresa – jméno | Jméno osoby nebo divize ve společnosti dodavatele, která bude zasílat fakturu. Výchozí hodnota v tomto poli je ze záznamu účtu dodavatele a bude použita jako název primárního kontaktu na fakturách dodavatele vytvořených pro tuto subdodávku. |
    | Fakturační adresa | Adresa použitá na fakturách od tohoto dodavatele. Hodnota v tomto poli je výchozí z účtu dodavatele, ale lze ji změnit. Tato adresa se také používá jako faktura z adresy na fakturách dodavatele vytvořených pro tuto subdodávku. |
    | Dílčí součet | Pokud subdodávka nemá řádky, zadejte do tohoto pole hodnotu, která označuje mezisoučet objednávky před zdaněním. Pokud má subdodávka řádky, je toto pole pouze pro čtení. Zobrazená částka je mezisoučet všech řádků na subdodávce. |
    | Celková daň | Pokud subdodávka nemá řádky, zadejte do tohoto pole hodnotu určující zdanění objednávky. Pokud má subdodávka řádky, je toto pole pouze pro čtení. Zobrazená částka je zdaněný součet všech zdaněných řádků na subdodávce. |
    | Celková částka |  Tato počítané pole ukazuje celkovou částku subdodávky po zahrnutí daní.  |
    | Datum potvrzení | Datum, kdy byla subdodávka potvrzena  |
    | Vyžádal/a | Výchozí hodnota v tomto poli je jméno uživatele, který vytváří subdodávku. Tuto hodnotu může změnit tvůrce subdodávky, aby označil osobu, pro kterou subdodávku vytváří.  |
    | Manažer účtu dodavatele | Název primárního kontaktu účtu dodavatele. Hodnota v tomto poli je výchozí z účtu dodavatele, ale lze ji změnit. Tuto hodnotu pole může uživatel změnit, aby jako správce účtu dodavatele subdodávky vybral jiný kontakt. Tímto kontaktem lze konfigurovat a odesílat e-mailová upozornění a vyjednávání o ceně. |


