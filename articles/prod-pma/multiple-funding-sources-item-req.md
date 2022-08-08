---
title: Požadavky na položky u projektových smluv s více zdroji financování
description: Tento článek poskytuje informace o tom, jak konfigurovat a používat požadavky na položky s více zdroji financování.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028465"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Požadavky na položky u projektových smluv s více zdroji financování

_**Platí pro:** Project Operations pro scénáře založené na skladovém materiálu / výrobě_

Některé smluvní dohody u dodávek založených na projektech mohou vyžadovat více zdrojů financování. Tento článek vysvětluje, jak vybrat a konfigurovat požadované zdroje financování, když projekt nebo projektová smlouva vyžaduje více zdrojů.

## <a name="terminology"></a>Terminologie

- **Zdroj financování** – Entita, která financuje práci na projektové smlouvě. Touto entitou může být interní organizace nebo externí fakturační účet (zákazník nebo grant).
- **Zákazník projektu** – Entita, které je projektová práce dodána.
- **Fakturační účet** – Externí entita, která platí za projektové práce.

## <a name="example"></a>Příklad

Společnost Contoso získala smlouvu na obnovu zařízení u dvou zákazníků: Adatum US a Adatum Corporate. Smlouva zahrnuje hardware a instalační služby, které budou dodány společnosti Adatum US (zákazník projektu). Hardware bude financován společností Adatum Corporate (fakturační účet 1) a instalační práce budou financovány společností Adatum US (fakturační účet 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Nastavení výchozích pravidel fakturačního účtu pro požadavky na položky

### <a name="prerequisites"></a>Předpoklady

- U požadavků na položky, které mají více fakturačních účtů, je nutné použít Microsoft Dynamics 365 Finance **verze 10.0.27 nebo novější**.
- Váš správce systému musí povolit funkci **Povolit požadavky na položky s více zdroji financování u scénářů Project Operations založených na skladovém materiálu / výrobě** v pracovním prostoru **Správa funkcí**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Nastavení výchozích pravidel fakturačního účtu

Chcete-li nastavit výchozí pravidla pro fakturační účet, postupujte takto.

1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.
1. Na kartě **Všeobecné** v sekci **Prodejní objednávky a požadavky na položky** nastavte možnost **Povolit projekty s více zdroji financování** na **Ano**.
1. V poli **Výchozí zákazník** zadejte, odkud ve výchozím nastavení pochází zákazník projektové dodávky u požadavku na položku:

    - **Ze zdroje financování** – Výchozí zákazník dodávky projektu pochází ze zdroje financování. Pokud je s projektovou smlouvou spojeno více zdrojů financování, použije se první zdroj financování v seznamu.
    - **Z projektu** – Výchozí zákazník dodávky projektu pochází ze zákazníka, který je vybrán v poli **Evidenční účet projektu**.

1. Volitelné: Nastavte nebo změňte výchozí fakturační účet v záznamech projektu:

    1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty** a otevřete podrobnosti záznamu projektu.
    2. Na kartě **Všeobecné** nastavte nebo aktualizujte pole **Výchozí fakturační účet**. Účet, který určíte, bude použit jako výchozí fakturační účet u nových požadavků na položky vytvořených pro projekt. Pokud necháte pole prázdné, bude standardně použit účet faktury prvního zdroje financování projektové smlouvy. Uživatelé však budou moci účet změnit při uložení záznamu.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Výběr účtu faktury, který chcete použít při vytváření požadavku na položku

Při výběru účtu faktury, který chcete použít při vytváření požadavku na položku, postupujte takto.

1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty** a vyberte záznam projektu.
1. Na kartě **Plán** vyberte **Požadavky na položku**.
1. Vytvořte nový záznam požadavku na položku.

    - Ve výchozím nastavení je pole **Fakturační účet** v záznamu nastaveno na účet faktury nastavený pro projekt. Hodnotu pole **Fakturační účet** můžete změnit a poté záznam uložte. Po uložení záznamu již nelze hodnotu **Fakturační účet** aktualizovat. Pokud musíte u požadavku na položku aktualizovat **Fakturační účet**, odstraňte stávající požadavek na položku a poté vytvořte nový, který má požadovanou hodnotu.
    - Ve výchozím nastavení je pole **Zákazník** pro požadavek položky nastaveno na základě hodnoty **Výchozí zákazník**, která je nastavena na stránce **Parametry modulu Řízení a účetnictví projektu**.

    Když je záznam požadavku položky uložen, systém jej přiřadí k záznamu záhlaví **Prodejní objednávka požadavku na položku**. Pokud žádné záhlaví otevřené prodejní objednávky neobsahuje vybraný fakturační účet, systém jej vytvoří a přiřadí k němu řádek požadavku na položku.

> [!NOTE]
> Požadavky na položky jsou vždy plně fakturovány na fakturační účet, který je nastaven v záznamu. Systém aktuálně nepodporuje pravidla pro přidělování finančních prostředků, která mají požadavky na položky, a nerozdělí zaúčtování na základě nastavení pravidel přidělování finančních prostředků.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Vytvoření požadavku na položku ze záznamu prognózy položky

Při vytvoření požadavku na položku ze záznamu prognózy položky postupujte takto.

1. Přejděte do nabídky **Řízení projektů a účetnictví** \> **Projekty** \> **Všechny projekty** a vyberte záznam projektu.
1. Na kartě **Plán** vyberte **Prognózy položek**.
1. Vytvořte nový záznam prognózy položky.
1. Volitelné: Na kartě **Projekt** v poli **Zdroj financování** vyberte požadovaný fakturační účet.
1. Vyberte položku **Vytvořit požadavek na položku** a potvrďte přijatou zprávu.

    > [!NOTE]
    > Systém zkopíruje hodnotu **Zdroj financování** ze záznamu prognózy položky do nově vytvořeného záznamu požadavku na položku.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Výchozí fakturační účet, když systém automaticky vytvoří požadavek na položku z řádku nákupní objednávky

Pokud je možnost **Vytvořit požadavek na položku** nastavena na **Ano** na stránce **Parametry modulu Řízení a účetnictví projektu**, systém automaticky vytvoří požadavek na položku, když je uložen nový řádek nákupní objednávky projektu. Ve výchozím nastavení jsou pole **Fakturační účet** a **Požadavek na položku** nastavena na hodnotu **Výchozí fakturační účet** v záznamu projektu. Systém aktuálně nepodporuje aktualizaci nebo změnu fakturačního účtu u záznamů tohoto typu.
