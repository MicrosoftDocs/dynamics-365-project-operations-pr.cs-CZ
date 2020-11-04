---
title: Správa zájemců (Pro)
description: Toto téma obsahuje informace o správě zájemců na základě projektu (Pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073709"
---
# <a name="manage-leads-pro"></a>Správa zájemců (Pro)

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Zájemce na základě projektu lze spravovat a kvalifikovat v aplikaci Project Operations. Proces správy zájemců zahrnuje vytváření pracovních zájemců na základě práce a jejich kvalifikaci. 

## <a name="list-of-project-sales-leads"></a>Seznam potenciálních zákazníků projektu

V části **Prodej** v levém navigačním podokně otevřete stránku seznamu **Zájemci** a zobrazte tak seznam všech záznamů potenciálních zákazníků v systému. Zobrazený seznam zájemců obsahuje zájemce založené na práci a další typy zájemců, které lze vytvořit, pokud máte také aplikace Dynamics 365 Sales nebo Dynamics 365 Field Service.

Vytvořením filtru podle hodnoty **Typ** můžete vytvořit filtrované zobrazení a ukázat pouze zájemce na základě projektu. Můžete například vybrat, aby se zobrazovali pouze zájemci na základě práce.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Vytvoření nového zájemce pro obchod založený na projektu

Když je zájemce na základě projektu kvalifikován, vytvoří se příležitost a účet. Příležitost založená na projektu je výchozím bodem pro aktivity zaměřené na prodej ve fázi Příležitost. Příležitosti založené na projektu mají jedinečné schopnosti, které jsou vyžadovány k prodeji projektové práce. Mezi tyto schopnosti patří:

- Metody fakturace času, materiálu a pevné ceny
- Ceníky s více daty účinnosti pro lidské zdroje, náklady a materiál vynaložené na projekty.

Chcete-li, aby kvalifikovaný zájemce automaticky vytvořil příležitost, nastavte při vytvoření zájemce atribut **Typ** na hodnotu **Na základě práce**. Pokud zvolíte jiný typ, zájemce nevytvoří příležitost založenou na projektu, pokud bude kvalifikován. Pokud není vytvořena příležitost založená na projektu, funkce specifické pro projekt nebudou k dispozici v procesech následného prodeje.

Následující tabulka obsahuje důležité informace o poli pro zájemce a důsledky těchto polí v následných činnostech.

| **Pole** | **Umístění** | **Relevance, účel a vedení** | **Dopad na následné složky** |
| --- | --- | --- | --- |
| Téma | Karta Obecné | Toto textové pole by mělo obsahovat krátký popis obchodu. | Téma zájemce bude mít výchozí obsah podle tématu příležitosti, a název nabídky a projektové smlouvy. |
| Typ | Karta Obecné | Toto pole sady možností obsahuje následující možnosti:</br>- Na základě práce (k dispozici pouze v případě, že je nainstalována aplikace Project Operations)</br>- Na základě zboží (k dispozici pouze v případě, že jsou nainstalovány aplikace Project Operations a Sales)</br>- Na základě servisní údržby (k dispozici, když je nainstalována služba Field Service) | Když je toto pole nastaveno na hodnotu **Na základě práce** u zájemce, je zájemce kvalifikován k vytvoření příležitosti založené na projektu. Příležitost založená na projektu je nutná k povolení všech rozšíření a funkcí specifických pro projekt v procesu následného prodeje pro tento obchod. |
| Jméno | Karta Obecné | Křestní jméno kontaktní osoby potencionálního zákazníka | Když je zájemce kvalifikován, vytvoří se účet, kontaktní osoba a příležitost. Křestní jméno kontaktní osoby je zde nastavená hodnota. |
| Příjmení | Karta Obecné | Příjmení kontaktní osoby potencionálního zákazníka | Když je zájemce kvalifikován, vytvoří se účet, kontaktní osoba a příležitost. Příjmení kontaktní osoby je zde nastavená hodnota. |
| Společnost | Karta Obecné | Název společnosti potenciálního zákazníka | Když je zájemce kvalifikován, vytvoří se účet, kontaktní osoba a příležitost. Název vytvořeného účtu je zde nastavená hodnota. |
| Měna | Karta Podrobnosti | Měna potenciálního zákazníka | Když je zájemce kvalifikován, vytvoří se účet, kontaktní osoba a příležitost. Měna vytvořeného účtu je zde nastavená hodnota. |

## <a name="qualify-a-new-project-based-lead"></a>Kvalifikace nového zájemce na základě projektu

Zájemci, kteří mají **Typ** nastaven na hodnotu **Na základě práce** , se nazývají zájemci na základě projektu. Když je zájemce na základě projektu kvalifikován, vytvoří se následující položky:

- Účet, který používá pole **Společnost** ze zájemce.
- Záznam kontaktní osoby přidružený k účtu na základě hodnot v polích **Křestní jméno** a **Příjmení** zájemce.
- Příležitost založená na projektu, která má pole **Typ** nastaveno na **Na základě práce**.

Podrobnější informace o zařazení zájemců najdete v tématu[Zařazení nebo převod zájemců](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

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
