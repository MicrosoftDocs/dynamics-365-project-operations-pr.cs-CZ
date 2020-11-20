---
title: Správa zájemců
description: Toto téma obsahuje informace o správě potenciálních zákazníků na základě projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4c99485a1d0c54ae848e5fbed4c4590e96cba9fd
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181759"
---
# <a name="manage-leads"></a>Správa zájemců

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Zájemce na základě projektu lze spravovat a kvalifikovat v aplikaci Project Operations. Proces správy zájemců zahrnuje vytváření pracovních zájemců na základě práce a jejich kvalifikaci. 

## <a name="project-sales-leads"></a>Potenciální zákazníci projektu

V části **Prodej** v levém navigačním podokně otevřete stránku seznamu **Zájemci** a zobrazte tak seznam všech záznamů potenciálních zákazníků v systému. Zobrazený seznam zájemců obsahuje zájemce založené na práci a další typy zájemců, které lze vytvořit, pokud máte také aplikace Dynamics 365 Sales nebo Dynamics 365 Field Service.

Vytvořením filtru podle hodnoty **Typ** můžete vytvořit filtrované zobrazení a ukázat pouze zájemce na základě projektu. Můžete například vybrat, aby se zobrazovali pouze zájemci na základě práce.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Vytvoření nového potenciálního zákazníka pro obchod založený na projektu

Když je zájemce na základě projektu kvalifikován, vytvoří se příležitost a účet. Příležitost založená na projektu je výchozím bodem pro aktivity zaměřené na prodej ve fázi Příležitost. Příležitosti založené na projektu mají jedinečné schopnosti, které jsou vyžadovány k prodeji projektové práce. Mezi tyto schopnosti patří:

- Metody fakturace času, materiálu a pevné ceny
- Ceníky s více daty účinnosti pro lidské zdroje, náklady a materiálu vynaložené na projekty

Chcete-li, aby kvalifikovaný zájemce automaticky vytvořil příležitost, nastavte při vytvoření zájemce atribut **Typ** na hodnotu **Na základě práce**. Pokud zvolíte jiný typ, zájemce nevytvoří příležitost založenou na projektu, pokud bude kvalifikován. Pokud není vytvořena příležitost založená na projektu, funkce specifické pro projekt nebudou k dispozici v procesech následného prodeje.

Následující tabulka obsahuje důležité informace o poli pro zájemce a důsledky těchto polí v následných činnostech.
 
| **Pole** | **Umístění** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- | --- |
| Téma | Karta Obecné | Toto textové pole by mělo obsahovat krátký popis obchodu. | Téma zájemce bude mít výchozí obsah podle tématu příležitosti, a název nabídky a projektové smlouvy. |
| Typ | Karta Obecné | Toto pole sady možností obsahuje následující možnosti:</br>- Na základě práce (k dispozici pouze v případě, že je nainstalována aplikace Project Operations)</br>- Na základě zboží (k dispozici pouze v případě, že jsou nainstalovány aplikace Project Operations a Sales)</br>- Na základě servisní údržby (k dispozici, když je nainstalována služba Field Service) | Když je toto pole nastaveno na hodnotu **Na základě práce** u zájemce, je zájemce kvalifikován k vytvoření příležitosti založené na projektu. Příležitost založená na projektu je nutná k povolení všech rozšíření a funkcí specifických pro projekt v procesu následného prodeje pro tento obchod. |
| Jméno | Karta Obecné | Křestní jméno kontaktní osoby potencionálního zákazníka | Když je zájemce kvalifikován, vytvoří se účet, kontaktní osoba a příležitost. Křestní jméno kontaktní osoby je zde nastavená hodnota. |
| Příjmení | Karta Obecné | Příjmení kontaktní osoby potencionálního zákazníka | Když je zájemce kvalifikován, vytvoří se účet, kontaktní osoba a příležitost. Příjmení kontaktu – zde nastavená hodnota. |
| Společnost | Karta Obecné | Název společnosti potenciálního zákazníka | Když je zájemce kvalifikován, vytvoří se účet, kontaktní osoba a příležitost. Název vytvořeného účtu – zde nastavená hodnota. |
| Měna | Karta Podrobnosti | Měna potenciálního zákazníka | Když je zájemce kvalifikován, vytvoří se účet, kontaktní osoba a příležitost. Měna vytvořeného účtu je zde nastavená hodnota. |

## <a name="qualify-a-new-project-based-lead"></a>Kvalifikace nového zájemce na základě projektu

Zájemci, kteří mají **Typ** nastaven na hodnotu **Na základě práce**, se nazývají zájemci na základě projektu. Když je zájemce na základě projektu kvalifikován, vytvoří se následující položky:

- Účet, který používá pole **Společnost** ze zájemce.
- Záznam kontaktní osoby přidružený k účtu na základě hodnot v polích **Křestní jméno** a **Příjmení** zájemce.
- Příležitost založená na projektu, která má pole **Typ** nastaveno na **Na základě práce**.

Podrobnější informace o zařazení zájemců najdete v tématu[Zařazení nebo převod zájemců](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Zařazení zájemce a informace o právnické osobě 

Když spustíte aplikaci Project Operations v režimu nasazení, Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě, každý zákazník a příležitost bude vyžadovat, aby měla nastaveno pole **Vlastnická společnost**. Vlastnická společnost je právnická osoba ve vaší organizaci, která vlastní dodávku projektu. Každý zákazník nebo účet s typem vztahu „zákazník“ musí mít pole **Vlastnická společnost** nastavené na právnickou osobu, která uzavírá smlouvy a vyjednává s tímto zákazníkem. Zákazník může být pouze v jedné právnické osobě.

Když je zájemce kvalifikován, budou mít vytvořené záznamy o zákaznících a příležitostech nastaveno pole **Vlastnická společnost** na společnost záznamu rezervovatelného zdroje aktuálního uživatele.

Pokud je záznam rezervovatelného zdroje aktuálního uživatele prázdný, pak se hodnota pole **Vlastnická společnost** v záznamu uživatele používá jako výchozí v záznamech zákazníka a příležitosti.

## <a name="business-process-flow-for-project-based-deals"></a>Tok obchodního procesu u obchodů založených na projektu

Následující toky obchodního procesu jsou podporovány u obchodů založených na projektu v aplikaci Project Operations:

- Obchodní proces od zájemce po příležitost
- Prodejní proces příležitosti

Obchodní proces od zájemce po příležitost podporuje následující fáze:

| Název fáze | Mapovaná entita | Funkce |
| --- | --- | --- |
| Zařadit | Potenciální zákazník | Zařazením zájemce vytvoříte účet, kontaktní osobu nebo příležitost. |
| Vytvořit | Příležitost | Vypracováním příležitosti přidáte další informace o provedené práci, klíčových účastnících a konkurenci. |
| Navrhnout | Příležitost | Vypracujte návrh a získejte souhlas od interního kontrolního týmu. |
| Uzavřeno | Příležitost | Vyhrajte příležitost uzavřít obchod. |
