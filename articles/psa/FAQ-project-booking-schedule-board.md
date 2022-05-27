---
title: Vytvoření rezervace projektu z Plánovací vývěsky
description: Toto téma obsahuje informace o způsobu vytvoření rezervace projektu z plánovací vývěsky.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 693f4c4be1371bae232f636a5e168e889e81b09c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578010"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Vytvoření rezervace projektu z Plánovací vývěsky

[!include [banner](../includes/psa-now-project-operations.md)]

Zdroj na projekt můžete rezervovat buď přímo z karty **Tým** projektu nebo generováním požadavku na zdroj z přiřazení obecného člena týmu a poté naplněním generovaného požadavku členem projektového týmu.

Můžete také rezervovat zdroj na projektu přímo z Plánovací vývěsky. To lze vyřešit třemi způsoby:

- **Rezervace z vygenerovaného požadavku na zdroj:** po vytvoření obecného zdroje a přiřazení úkolů v rámci projektu můžete vygenerovat požadavek na zdroj.

- **Rezervace z primárního požadavku:** primární požadavky se zobrazují na kartě **Projekt** na plánovací vývěsce. 

- **Rezervace z nového požadavku na zdroj:** můžete vytvořit úplně nový požadavek na zdroj a přidružit ho k projektu. Na plánovací vývěsce se tento požadavek na zdroj zobrazuje na kartě **Otevřené požadavky**.

## <a name="book-from-a-generated-resource-requirement"></a>Rezervace z generovaného požadavku na zdroj

Můžete vytvořit obecný zdroj a přiřadit k němu jeden nebo více úkolů v rámci projektu. Poté můžete vygenerovat požadavek na zdroj z obecného člena týmu. 

1.  Na Plánovací vývěsce se tento zdroj zobrazí na kartě **Otevřené požadavky**. Můžete chtít použít filtry sloupců na mřížce, pokud máte mnoho otevřených požadavků. 

    ![Otevření karty Požadavky na plánovací vývěsce.](media/FAQ-Project-Booking-Schedule-Board-1.png "Snímek obrazovky tabulky rezervací a přiřazení")

2. Vyberte požadavek. Karta **Najít dostupnost** se zobrazí v horní části vybraného řádku.
 
3. Pokud vyberete tuto kartu, otevře se režim Pomocníka plánování plánovací vývěsky a poté vyfiltruje dostupné zdroje, které splňují požadavek na zdroj. Potom můžete rezervovat zdroj.

4. Také můžete přetáhnout a umístit vybraný řádek z dolní části Plánovací vývěsky do buňky zdroje v mřížce výše. Po přetažení se otevře panel **Vytvořit rezervaci zdroje** na pravé straně.

    Výběr **Rezervace** zarezervuje zdroj na projektový tým.

![Panel Vytvořit rezervaci zdroje.](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Rezervace z primárního požadavku

Vytvoření projektu v aplikaci Project Service automaticky vytvoří požadavek na zdroj nazvaný Primární požadavek. Jedná se o prázdný požadavek, umožňující rychle rezervovat zdroj pomocí Plánovací vývěsky bez generování požadavku nebo vytvoření požadavku od samého začátku. Vzhledem k tomu, že požadavek je prázdný, bude nutné zadat data, stejně jako metodu přidělení a popřípadě hodiny. 

1. Chcete-li rezervovat zdroj s Primárním požadavkem, zvolte na Plánovací vývěsce kartu **Projekt**. Možná budete chtít použít filtr sloupce ve sloupci **Projekt**, pokud máte příliš mnoho projektů.

   ![Filtry sloupců na plánovací vývěsce.](media/FAQ-Project-Booking-Schedule-Board-2.png "Snímek obrazovky tabulky rezervací a přiřazení")

2. Vyberte požadavek, který má pouze název projektu jako svůj název a má nulovou dobu trvání (0).

3. Zvolte kartu **Najít dostupnost**, která se zobrazí na řádku. To převede Plánovací vývěsku do režimu Pomocníka plánování a zobrazí dostupné prostředky, které lze rezervovat na projekt.

4. Protože **Primární požadavek** je prázdným požadavkem s nulovou dobou trvání (0), budete muset nastavit dobu trvání na panelu **Vytvořit rezervaci zdrojů** při výběru a rezervaci zdroje.

5. Můžete také vybrat **Primární požadavek projektu** v dolní části Plánovací vývěsky a přetáhnout a umístit ho na zdroj za účelem jeho rezervace.
 
    Protože **Primární požadavek** je prázdným požadavkem s nulovou dobou trvání (0), budete muset nastavit dobu trvání na panelu **Vytvořit rezervaci zdrojů** při výběru a rezervaci zdroje.
 
    Když rezervujete zdroj prostřednictvím **Primary Requirement** na Plánovací vývěsce, přidáte ho do projektového týmu bez jakýchkoli přiřazení.
 
## <a name="book-from-a-new-resource-requirement"></a>Rezervace z nového požadavku na zdroj
Chcete-li provést rezervaci z nového požadavku na zdroj, postupujte následujícím způsobem. 

1. Přejděte na **Požadavky na zdroj** a poté vyberte **Nový**, chcete-li vytvořit nový požadavek na zdroj.

2. Na kartě **Projekt** vyberte projekt, ke kterému chcete požadavek na projekt přidružit.
 
    Tento nově vytvořený požadavek se na Plánovací vývěsce zobrazuje jako **Otevřený požadavek**, který můžete splnit.

3. Rezervace zdroje za účelem jeho přidání do projektového týmu.

4. Nyní, když je zdroj rezervován, musíte ručně přiřadit úkoly.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
