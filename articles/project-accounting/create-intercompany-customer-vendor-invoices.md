---
title: Vytvářejte mezipodnikové faktury zákazníků a dodavatelů
description: Toto téma obsahuje informace, jak vytvářet mezipodnikové faktury zákazníků a dodavatel.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595444"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Vytvářejte mezipodnikové faktury zákazníků a dodavatelů

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Účetní projektu v právnické osobě poskytující půjčku vytvoří mezipodnikovou fakturu zákazníka za náklady projektu, které se převádějí na výpůjčující entitu. Po schválení a zaúčtování mezipodnikové faktury odběratele odešle půjčující právnická osoba mezipodnikovou fakturu vypůjčující právnické osobě.

Účetní projektu pro právnickou osobu poskytující půjčky může nastavit dávkový proces pro opakované generování mezipodnikových faktur. Účetní projektu určuje kritéria, například konkrétní projekty, pro vytvoření mezipodnikových faktur v dávce.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Ručně vytvořte mezipodnikovou fakturu zákazníka za transakce projektu 

Použijte tento proces pro řuční vytvoření mezipodnikové faktury zákazníka za transakce projektu. Vyhledejte hodiny, které pracovníci vyúčtovali za projekty ve vypůjčujících právnických osobách, a výdaje, které vaší právnické osobě vznikly jménem vypůjčujících právnických osob. Můžete vyhledávat podle názvu právnické osoby, čísla projektové smlouvy, čísla projektu, rozsah kalendářních dat nebo libovolné kombinace těchto možností. Ve výsledcích hledání vyberte transakce, které chcete přidat do mezipodnikové faktury.

1. v Dynamics 365 Finance přejděte na **Řízení projektů a účetnictví** > **Faktury projektu** > **Mezipodnikové faktury zákazníků**. Na stránce seznamu **Mezipodnikové faktury zákazníků** v podokně akcí vyberte **Nový.**
2. Na stránce **Vytvořte mezipodnikovou fakturu** v poli **Právnická osoba** vyberte vypůjčující právnickou osobu.
3. Volitelné: Zadejte konkrétní smlouvu o projektu a číslo projektu.
4. Vyhledávání můžete zúžit výběrem časového období. Zadejte konkrétní data do pole **Počáteční datum** a **Koncové datum**. Ve výsledcích hledání se zobrazí pouze mezipodnikové transakce, které jsou zaúčtovány v tomto období.
5. Nastavte **Parametr rozšířeného řádku deníku projektu** na **Ano** a vyberte **Vyhledávání**.
6. Ve výsledcích hledání vyberte transakce, které chcete zahrnout do návrhu mezipodnikové faktury, a poté vyberte **OK**.
7. Na stránce **Mezipodniková faktura zákazníka** se zobrazí transakce mezipodnikového projektu, které jste vybrali z výsledků vyhledávání. Chcete-li upravit transakce před odesláním faktury vypůjčující právnické osobě, postupujte takto:
  
    1. Otevři stránku **Vytvořit návrh faktury**. Vyberte další mezipodnikové transakce pro aktuální fakturu a poté vyberte **Přidat řádek**.
    2. Řádek můžete odebrat, pokud jej vyberete **Odebrat** .
    3. Zobrazit komentáře, důvody, finanční dimenze a další informace o vybraném řádku na pevné záložce **Řádky faktur**.
    
8. Chcete-li zaúčtovat mezipodnikovou fakturu zákazníků v podokně akcí vyberte **Zaúčtovat**.

> [!NOTE]
> Pokud vaše organizace vyžaduje, aby byly mezipodnikové faktury zkontrolovány před jejich zaúčtováním, může správce systému nastavit pracovní postup pro mezipodnikové faktury. Pokud u mezipodnikových faktur není nastaven pracovní postup, můžete mezipodnikovou fakturu zaúčtovat.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Vytvořte dávkovou úlohu pro mezipodnikové faktury

Můžete vytvořit více mezipodnikových faktur současně pro všechny vypůjčené právnické osoby. Pomocí funkce vyhledávání můžete například vyhledávat všechny transakce, které jsou zaúčtovány vypůjčenými pracovníky a souvisejí s projekty, které jsou spravovány jinými právnickými osobami. Poté můžete pro každou vypůjčující právnickou osobu vytvořit mezipodnikovou fakturu za transakce uvedené ve výsledcích vyhledávání.

1. Přejděte na **Řízení projektů a účetnictví** > **Periodické** > **Projektové faktury** > **Vytvořit mezipodnikové faktury zákazníků**.
2. Na stránce **Vytvořit mezipodnikové faktury zákazníků** v poli **Společnost** vyberte právnickou osobu k fakturaci. Pokud nevyberete společnost, všechny transakce, které splňují kritéria vyhledávání, se zobrazí u všech vypůjčujících právnických osob.
3. Ve **Vytvořit jednu fakturu za** vyberte, zda chcete vytvořit fakturu za mezipodnikové transakce na základě projektu nebo na základě vypůjčené právnické osoby.
4. Volitelné: Chcete-li vybrat konkrétní projekt a projektovou smlouvu, pro kterou chcete vytvořit mezipodnikové faktury, klikněte na **Vybrat**. Na stránce **DOtaz** v poli **Kritéria** vyberte projektovou smlouvu, číslo projektu nebo obojí a poté vyberte **OK**.
5. Na kartě **Dávka** nastavte dávkový proces pro opakované vytváření mezipodnikových faktur. Další informace viz [Odeslat úlohu dávkového zpracování z formuláře](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Chcete-li zaúčtovat mezipodnikové faktury, v podokně akcí vyberte **Zaúčtovat**.

> [!NOTE]
> Pokud vaše organizace vyžaduje, aby byly mezipodnikové faktury zkontrolovány před jejich zaúčtováním, může správce systému nastavit pracovní postup pro mezipodnikové faktury. Pokud u mezipodnikových faktur není nastaven pracovní postup, můžete mezipodnikové faktury zaúčtovat.

## <a name="post-the-intercompany-vendor-invoice"></a>Zaúčtujte fakturu mezipodnikového dodavatele

Účetní projektu ve vypůjčující právnické osobě může zkontrolovat mezipodnikové nevyřízené faktury dodavatele, když je zaúčtována příslušná mezipodniková faktura zákazníka. Ve Finance přejděte ve vypůjčující právnické osobě na **Závazky** > **Faktury** > **Nevyřízená faktura dodavatele**. Číslo nevyřízené faktury se bude shodovat s číslem faktury mezipodnikového zákazníka. Ověřte správnost faktury a poté fakturu zaúčtujte. Zaúčtováním faktury mezipodnikového dodavatele se vytvoří podřízená kniha projektu a transakce hlavní knihy, která odráží transakční náklady ve vypůjčující právnické osobě.


[!INCLUDE[footer-include](../includes/footer-banner.md)]