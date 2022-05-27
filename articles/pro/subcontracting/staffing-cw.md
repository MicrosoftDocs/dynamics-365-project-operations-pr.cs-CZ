---
title: Personální zajištění projektu smluvními pracovníky a subdodavatelskou kapacitou
description: Toto téma vysvětluje, jak lze v Microsoft Dynamics 365 Project Operations personálně zajistit projektové požadavky pomocí smluvních pracovníků nebo subdodavatelské kapacity .
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a0efea80484dfca0a9dae8404837c3376dfecaed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574634"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Personální zajištění projektu smluvními pracovníky a subdodavatelskou kapacitou

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Členové obecného projektového týmu mohou být obsazeni zaměstnanci nebo smluvními pracovníky. Při obsazení projektu smluvními pracovníky můžete omezit své personální možnosti na konkrétní smluvní pracovníky, kteří jsou přiřazeni k řádku subdodávky. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Hledejte požadavky na personální obsazení u smluvních pracovníků, kteří patří ke konkrétnímu řádku subdodávky

Při hledání požadavků na personální obsazení u smluvních pracovníků, kteří patří ke konkrétnímu řádku subdodávky, postupujte takto:

1. Vytvořte obecného člena projektového týmu, který odkazuje na subdodávku a řádek subdodávky.
2. Vygenerujte požadavek na zdroj pro tohoto obecného člena projektového týmu pomocí tlačítka **Generovat požadavek** na podmřížce členů projektového týmu.
3. Vyberte řádek člena týmu a poté vyberte tlačítko **Rezervovat** na podmřížce. 
4. Tím otevřete plánovací vývěsku s kontextem požadavku. Spolu s dalšími atributy, jako jsou data, role a pole organizační jednotky, jsou filtry plánovací vývěsky také automaticky vyplněny poli dodavatele, subdodávky a řádku subdodávky z požadavku na zdroj.
5. Systém vyhledává zdroje, které splňují kritéria filtru, a uvede je v seznamu. 
6. Vyberte jeden z filtrovaných zdrojů a rezervujte zdroj pro daný požadavek. 
7. Vytvoří se člen projektového týmu, který je aktualizován odkazy na subdodávku a řádek subdodávky. Přejděte do **Odhadů projektu** a vyberte **Aktualizovat ceny**, abyste uviděli aktualizované náklady přiřazení zdrojů. 

> [!NOTE]
> Aktualizace člena projektového týmu pomocí odkazů na subdodávku a řádek subdodávky nemusí být během rezervace vždy možná, pokud je zdroj přiřazen k více řádkům subdodávky. Pokud systém není schopen aktualizovat člena projektového týmu údaji o subdodávce a řádku subdodávky, otevřete záznam člena projektového týmu a ručně aktualizujte tato pole, aby odhad finančních nákladů přesně odrážel náklady subdodavatele.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Hledání a zajištění požadavků na personální obsazení u jakéhokoli smluvního pracovníka

Při hledání a zajištění požadavků na personální obsazení u jakéhokoli smluvního pracovníka postupujte takto:

1. Vytvořte obecného člena projektového týmu.
2. Vygenerujte požadavek na zdroj pro tohoto obecného člena projektového týmu pomocí tlačítka **Generovat požadavek** na podmřížce členů projektového týmu.
3. Vyberte řádek člena týmu a poté vyberte tlačítko **Rezervovat** na podmřížce. 
4. Tím otevřete plánovací vývěsku s kontextem požadavku. Spolu s dalšími atributy, jako jsou data, role a pole organizační jednotky, jsou filtry plánovací vývěsky také automaticky vyplněny poli dodavatele, subdodávky a řádku subdodávky z požadavku na zdroj. Protože požadavek neměl vyplněné žádné hodnoty subdodávky nebo řádku subdodávky, budou tyto atributy v podokně filtru prázdné.
5. Systém vyhledává zdroje, které splňují kritéria filtru, a uvede je v seznamu.
6. Aktualizujte pole **Typ pracovníka** v podokně filtru na **Smluvní pracovník** a omezte tak hledání na smluvní pracovníky. Aktualizujte **Dodavatele** v podokně filtru a vyberte dodavatele, abyste omezili hledání pouze na smluvní pracovníky, kteří patří ke konkrétní dodavatelské společnosti.
7. Vyberte smluvního pracovníka ze seznamu a rezervujte zdroj pro daný požadavek.
8. Vytvoří se člen projektového týmu. Člen projektového týmu však není aktualizován subdodávkou ani řádkem subdodávky, a proto přiřazení zdrojů nebude účtováno pomocí cen subdodávek. Ručně aktualizujte člena projektového týmu údajem řádku subdodávky, přejděte na **Odhady projektu** a vyberte příkaz **Aktualizovat ceny**, abyste viděli aktualizované náklady přiřazení zdrojů.

> [!NOTE]
> Členové projektového týmu, kteří mají **Typ pracovníka** nastaven na **Smluvní pracovník**, ale nemají odkaz na subdodávku, jsou označeni jako **Neplatný** v mřížce **Členové projektového týmu**. Pokud existují členové projektového týmu s tímto stavem, otevřete záznam člena projektového týmu a ručně aktualizujte pole subdodávky a řádku subdodávky, aby odhad finančních nákladů přesně odrážel náklady subdodavatele na kartě **Odhady**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
