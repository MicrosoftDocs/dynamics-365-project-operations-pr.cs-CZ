---
title: Hromadné opravy skutečných hodnot vytvořených schválenými položkami času a výdajů
description: Toto téma vysvětluje, jak může správce provést jednorázové nebo hromadné opravy dříve schválených položek času nebo výdajů, pokud není fakturace dokončena.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 88706946e5c5c59be996640f4c7b37e958c1cf1d9fd14c72c0c6dc854a77dab4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995393"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Hromadné opravy skutečných hodnot vytvořených schválenými položkami času a výdajů

[!include [banner](../includes/psa-now-project-operations.md)]

Někdy může být nesprávně zadán údaj o čase nebo výdaji. Poradce může například při vytváření časového záznamu vybrat nesprávné datum nebo při zadávání výdaje může transponovat čísla. Pokud konzultant nemůže provést aktualizace odeslaných zadání, může správce přímo opravit záznam pro projekt.

K dokončení postupů v tomto tématu budete potřebovat oprávnění správce.

## <a name="correct-approved-time-entries"></a>Oprava schválených časových údajů     

Chcete-li opravit jeden nebo více časových záznamů pro projekt, proveďte následující kroky.

1. V oblasti **Prodej** vyberte **Transakce** a poté vyberte **Schválený čas**. 

2. V seznamu **Schválený čas** vyhledejte a vyberte jeden nebo více schválených časových záznamů, které chcete opravit. Pomocí filtru můžete vyhledat související položky. Můžete například filtrovat ID projektu a vybrat všechny schválené časové záznamy s tímto ID projektu.

3. Zvolte **Opravit položky**. Automaticky se vytvoří nový deník oprav s přiřazeným typem **Oprava času**. Vybrané položky se přidají do deníku. 

4. Na stránce **Nový deník** zadejte **Popis** pro svůj deník oprav a poté vyberte kartu **Opravy časových záznamů**.  
5. V části **Nové hodnoty pro časové záznamy** aktualizujte pole správnými informacemi podle potřeby. Například můžete změnit přiřazený projekt nebo rezervovatelný zdroj.

6. Vyberte **Náhled**. V dialogovém okně vyberte **OK**. Na kartě **Řádky deníku** můžete zobrazit seznam původních skutečných hodnot, které se vztahují k vybraným časovým záznamům, které byly stornovány, a opraveným odpovídajícím řádkům, které byly vytvořeny. Pokud je třeba provést další opravy, opakujte kroky 5 a 6. 

> [!NOTE]
> Všechny opravené skutečné hodnoty budou mít stejné hodnoty, jaké jste vybrali v části **Nové hodnoty pro časové záznamy**.

7. Pokud se opravy objeví podle očekávání, vyberte **Potvrdit**. V dialogovém okně vyberte **OK**.

8. Vraťte se do části **Prodej**, vyberte **Projekty** a poté otevřete projekt, pro který jste právě aktualizovali časové záznamy. 

9. Na stránce **Projekty** na kartě **Skutečné hodnoty** zobrazte provedené změny. 

> [!NOTE]
> Pokud není karta **Skutečné hodnoty** viditelná, vyberte **Související** > **Skutečné hodnoty**.  

10. V seznamu **Přidružené zobrazení skutečností** můžete vidět, že původní časové záznamy, které byly stornovány, jsou stále uvedeny, stejně jako odpovídající opravené časové záznamy. 

Například v následující grafice jsou dvě položky řádku s množstvím 8,00, jejichž debety jsou uvedeny ve sloupci Částka. Navíc jsou ve sloupci Částka dvě položky řádku s množstvím -8,00, které zobrazují připsané částky. Tyto korekce uvádějí množství na nulu.

![Seznam přidružených zobrazení skutečností.](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Oprava schválených záznamů výdajů

Chcete-li opravit jeden nebo více záznamů výdajů, proveďte následující kroky. 

1. V části **Prodej** v levém navigačním podokně pod možností **Transakce** vyberte **Schválené výdaje**.

2. V seznamu **Schválené výdaje** vyberte projekt, který chcete opravit, a poté vyberte **Opravit položky**. Automaticky se vytvoří nový deník oprav s přiřazeným typem **Oprava výdajů**. 

3. Na stránce **Nový deník** zadejte **Popis** pro opravu a na kartě **Oprava výdajů** v části **Nové hodnoty nákladů** vyberte datová pole, která chcete opravit pro vybrané řádky výdajů. Například můžete přiřadit výdaje jinému **projektu**, nebo opravit **Kategorie výdajů**, **Datum výdaje**, nebo **Rezervovatelný zdroj**.

4. Vyberte **Náhled**. V dialogovém okně vyberte **OK**. 

5. Na kartě **Řádky deníku** ověřte opravy. Můžete zobrazit seznam původních skutečných hodnot, které se vztahují k vybraným záznamům výdajů, které byly stornovány, a opraveným odpovídajícím řádkům, které byly vytvořeny.

6. Pokud opravené hodnoty odpovídají očekávání, vyberte **Potvrdit**. V dialogovém okně vyberte **OK**. Pokud se hodnoty nezobrazují podle očekávání, vyberte **Zrušit** a vraťte se do seznamu **Schválené výdaje**. Opakujte kroky 2 až 5. 

> [!NOTE]
> Opravené skutečné hodnoty budou mít stejné hodnoty, jaké jste vybrali v části **Nové hodnoty pro výdaje**.

7. Po potvrzení deníku oprav přejděte zpět k projektu nebo projektům, které jste aktualizovali, a zobrazte své změny.  

8. Na stránce projektu na kartě **Skutečné hodnoty** zkontrolujte **Přidružené zobrazení skutečností**. Jsou uvedeny původní záznamy a opravené záznamy. Následující obrázek ukazuje původní částky záznamu výdajů a odpovídající opravené položky částek zadaných výdajů. 

![Skutečné hodnoty nákladů.](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]