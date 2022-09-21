---
title: Vytváření faktur dodavatele
description: Tento článek popisuje koncept dodavatelských faktur a způsob jejich vytváření v Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475409"
---
# <a name="create-vendor-invoices"></a>Vytváření faktur dodavatele

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Chcete-li používat funkce popsané v tomto článku, musíte aktivovat funkci **Aktivovat zpracování skutečného stavu subdodávek pomocí Project Operations pro scénáře založené na zdrojích** v pracovním prostoru **Správa funkcí**.

Fakturace dodavatele v Microsoft Dynamics 365 Project Operations lze použít k evidenci nákladů na dodávky služeb a materiálů na projektu vykonávaných dodavateli.

Když jsou služby a/nebo materiály zadány dodavateli subdodávkou, představuje subdodávka smluvní dohodu s tímto dodavatelem. Jak dodavatel dodává služby nebo jsou materiály přijímány a používány na projektových úkolech, náklady jsou zaznamenány v projektu. Dodavatel pak pravidelně zasílá faktury. Ty jsou ověřeny a spárovány s náklady zaznamenanými v projektu. Po dokončení procesu ověření je faktura dodavatele potvrzena a uvolněna k platbě.

## <a name="scenarios-for-use"></a>Scénáře použití

Faktury dodavatele v Project Operations lze použít k podpoře dvou odlišných scénářů:

- Zákazníci využívají plné možnosti subdodávek.
- Zákazníci nevyužívají plné subdodavatelské zkušenosti, ale chtějí mít jednotný pohled na náklady na projekty v Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Zákazníci využívají plné možnosti subdodávek

Prostředí s fakturami dodavatele poskytuje způsob, jak ověřit položky času, spotřeby materiálu a položek výdajů, které odkazují na subdodavatelské komponenty, a spárovat je s řádky faktur dodavatele. Tento proces lze použít k ověření správnosti řádků faktury dodavatele. Po dokončení ověřovacího procesu a potvrzení faktury dodavatele systém vrátí skutečné hodnoty, které byly zaznamenány schválenými protokoly využití času, výdajů a materiálu, a poté vytvoří nové skutečné náklady pomocí řádků faktury dodavatele.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Zákazníci nevyužívají plné subdodavatelské zkušenosti, ale chtějí mít jednotný pohled na náklady na projekty v Project Operations

Pokud sledujete proces subdodávek v systému třetí strany, můžete zaznamenat náklady z tohoto systému třetí strany do Project Operations vytvořením faktur dodavatele, které neodkazují na subdodávky. Vaši projektoví manažeři tak mohou mít jednotný pohled na všechny náklady na daný projekt.

## <a name="create-vendor-invoices-in-project-operations"></a>Vytváření dodavatelských faktur v Project Operations

Faktury dodavatele se vytvářejí v Dynamics 365 Finance pomocí modulu **Závazky**. Nemůžete vytvářet faktury dodavatele přímo v Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Nastavení ověřování faktur dodavatele

Pokud je faktura dodavatele určena pro subdodávku v Dataverse, musíte aktivovat parametr **Je vyžadováno ruční ověření projektovým manažerem**. Nastavení volby určuje, zda má být faktura dodavatele automaticky potvrzena v Dataverse, nebo zda vyžaduje ruční potvrzení. Záhlaví každé faktury dodavatele projektu obsahuje stejnojmennou možnost. Ve výchozím nastavení je možnost v záhlaví všech faktur dodavatelů projektu nastavena na hodnotu, kterou zde nastavíte. Hodnotu však můžete podle potřeby aktualizovat v záhlaví faktur jednotlivých dodavatelů.

Pokud je možnost nastavena na **Ano**, faktura dodavatele, která je vytvořena ve Finance a synchronizována s Dataverse, má stav **Koncept**. Faktura pak musí být validována a ověřena projektovým manažerem a potvrzena před jejím zpracováním a zaúčtováním na konkrétní projekt a účty hlavní knihy ve Finance.

Pokud je možnost nastavena na **Ne**, faktura dodavatele je automaticky potvrzena. Nevyžadují se žádné další akce.

Chcete-li nastavit ověřování faktury dodavatele, postupujte takto.

1. Ve Finance přejděte do nabídky **Řízení projektů a účetnictví** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.
1. Na kartě **Finanční údaje** nastavte možnost **Je vyžadováno ruční ověření projektovým manažerem** na **Ano**, pokud zásady společnosti vyžadují ověření faktur dodavatelů subdodavatelů. Pokud není vyžadováno ověření projektovým manažerem v Dataverse, ponechte sadu možností na **Ne**. Ve výchozím nastavení bude toto nastavení použito na stránce **Nevyřízená faktura dodavatele**.

> [!NOTE]
> Faktury dodavatele, které jsou vytvořeny pro subdodávky v Dataverse, mohou být správně zpracovány pouze v případě, že je možnost **Je vyžadováno ruční ověření projektovým manažerem** nastavena na **Ano**. Skutečné náklady na čas, materiál a náklady, které vytvoří subdodavatelé, může projektový manažer ručně přiřadit k řádkům faktury dodavatele, pouze pokud je tato možnost nastavena na **Ano**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Nastavení účtu integrace nákupu pro faktury dodavatele

Když je faktura dodavatele zaúčtována v části Finance pro Project Operations – integrované prostředí (neskladové), finanční údaje se zaúčtují na účet integrace nákupu. Systém generuje skutečné hodnoty v Dataverse za zaúčtovanou fakturu. Tyto skutečné hodnoty jsou zaúčtovány ve Finance pomocí deníku integrace projektu. Zaúčtováním deníku integrace projektu se zaúčtuje skutečný náklad a vrátí účet integrace nákupu.

Pro nastavení účtu integrace nákupu pro faktury dodavatele postupujte následovně.

1. Ve Finance přejděte do nabídky **Řízení projektů a účetnictví** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.
1. Na kartě **Project Operations na Dynamics 365 Customer Engagement** vyberte **Materiály** \> **Účet integrace nákupu**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Vytváření a účtování faktur dodavatelů subdodávek

Když fakturant závazků obdrží fakturu od subdodavatele, vytvoří se ve Finance nová faktura.

1. Ve Finance přejděte na **Závazky** \> **Faktury** \> **Nevyřízené faktury dodavatele**.
1. V **podokně akcí** vyberte **Nový** pro vytvoření faktury dodavatele.
1. Na hlavičce faktury v poli **Účet faktury** vyberte **Subdodavatel**.
1. Vyberte datum faktury.
1. Na kartě **Záhlaví** nastavte možnost **Je vyžadováno ruční ověření projektovým manažerem** na **Ano**. Výchozí nastavení této možnosti pochází ze stránky **Parametry projektového řízení a účetnictví**. Lze jej však změnit na úrovni faktury dodavatele.
1. Na pevné záložce **Řádek faktury** vyberte **Přidat řádek** k vytvoření řádku faktury dodavatele.
1. Vyberte kategorii nákupu, která byla vytvořena pro řádky subdodávek, a zadejte jednotkovou cenu, měrnou jednotku a množství.
1. V sekci řádky faktur dodavatele na kartě **Projekt** vyberte projekt, proti kterému subdodavatel sdílí fakturu za subdodávku.
1. Vyberte kategorii projektu. Může být jakéhokoli typu: **Položka**, **Výdaj**, **Materiály** nebo **Hodiny**.
1. Vyberte roli pouze v případě, že vybraná kategorie projektu je typu **Hodina**.
1. Vyberte **Zaúčtovat** pro zaúčtování faktury dodavatele.

Případně můžete vytvořit fakturu dodavatele tak, že přejdete na **Závazky** \> **Faktury** \> **Otevřené faktury dodavatele** a vyberete **Nová**.

Když je faktura dodavatele zaúčtována, bude dostupná v Dataverse pro ověření a zpracování projektovým manažerem.

## <a name="vendor-invoice-processing-in-dataverse"></a>Zpracování faktur dodavatele v Dataverse

Ve faktuře dodavatele, která je vytvořena v Dataverse, některé hodnoty polí pocházejí z faktury dodavatele, která je zaznamenána ve Finance. Ostatní hodnoty jsou výchozí hodnoty, které pocházejí ze subdodávky.

Následující pole a související záznamy budou zkopírovány ze subdodávky do záhlaví faktury dodavatele:

- Měna
- Smluvní jednotka
- Platební podmínky

Na řádcích faktury dodavatele používá Project Operations k zadání výchozího odkazu na řádek subdodávky a subdodávky následující hodnoty pole:

- Třída transakce
- Role
- Kategorie transakce
- Pole produktu
- Project
- Úloha

> [!NOTE]
> Řádky subdodávek s pevnou cenou nejsou v Project Operations podporovány.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
