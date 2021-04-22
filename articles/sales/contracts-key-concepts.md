---
title: Projektové smlouvy – klíčové koncepty
description: Toto téma poskytuje informace o klíčových konceptech projektových smluv v Dynamics 365 Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0e0280cb94e6f0186f59024c233e8fcb9e86abf
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663696"
---
# <a name="concepts-unique-to-project-based-contracts"></a>Koncepty jedinečné pro smlouvy na základě projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tento téma poskytuje klíčové koncepty, které musíte znát, než začnete používat projektové smlouvy v Dynamics 365 Project Operations:

## <a name="owning-company"></a>Vlastnící společnost

Vlastnící společnost je právnická osoba v modulu **Řízení a účetnictví projektů** pro Project Operations z Dynamics 365 Finance. Vlastnící společnost zastupuje právní subjekt, který bude účtovat náklady a výnosy plynoucí z obchodu.

## <a name="contracting-unit"></a>Smluvní jednotka

Smluvní jednotka představuje divizi nebo postup, které vlastní dodávku projektu. Náklady na zdroje můžete nastavit pro každou smluvní jednotku. Když zadáte cenu prostředku pro prostředek, budete také moci nastavit různé sazby nákladů pro prostředky. Tato smluvní jednotka si tyto zdroje půjčuje od jiných divizí nebo týmů v rámci podniku. Nákladové sazby se označují jako vnitropodnikové ceny, výpůjčky zdrojů nebo ceny za směnu. Když nastavujete nákladové sazby na půjčování zdrojů od jiných divizí, použijte měnu půjčující divize.

## <a name="cost-currency"></a>Měna nákladů

Měna nákladů je měna, ve které se vykazují náklady na obrazovce. Tato měna je odvozena od měny připojené k poli **Smluvní jednotka** smlouvy a projektu. Náklady projektu lze zapsat v jakékoli měně. Při zobrazení na displeji však dochází k převodu z měny zaznamenaných nákladů na měnu nákladů projektu.

Vzhledem k tomu, že směnné kurzy v platformě Common Data Service (CDS) nemohou být účinné od data, mohou se součty nákladů na obrazovce v průběhu času změnit, pokud aktualizujete směnné kurzy měn. Náklady zaznamenané v databázi však zůstanou nezměněny, protože částky jsou uloženy v měně, ve které vznikly.

## <a name="sales-currency"></a>Měna prodeje

Měna prodeje v aplikaci Project Operations je měna, ve které jsou zaznamenávány a zobrazovány odhadované a skutečné částky prodeje. Prodejní měna je také měna, ve které je zákazníkovi fakturován obchod. U projektové smlouvy je výchozí měna prodeje převzata ze záznamu zákazníka nebo účtu a lze ji změnit při vytvoření smlouvy. Když je smlouva vytvořena uzavřením nabídky tak, jak byla vyhrána, měna ve smlouvě je výchozí z měny v nabídce.

Když vytvoříte projektovou smlouvu od nuly, pole **Měna prodeje** nelze upravit. Výchozí hodnoty ceníků produktů a projektů jsou založeny na měně na smlouvě.

Na rozdíl od nákladů lze hodnoty prodejů zaznamenat pouze v měně prodeje.

## <a name="billing-method"></a>Způsob fakturace

Projekty mají obvykle dva typy smluvních modelů, s pevným poplatkem a založené na spotřebě. Tyto modely jsou v Project Operations zastoupeny jako způsoby fakturace se dvěma možnými hodnotami:

- Čas a materiál: Smluvní model založený na spotřebě, kde jsou všechny vzniklé náklady kryty odpovídajícími výnosy. S novým odhadem nebo při vzniku dalších nákladů se také zvýší odpovídající odhadovaný a skutečný prodej. Určete nepřekročitelné limity u řádků smlouvy, které mají tuto metodu fakturace, která omezuje skutečné výnosy. Odhadované výnosy nejsou nepřekročitelnými limity ovlivněny.
- Pevná cena: Jedná se o smluvní model s pevným poplatkem, který označuje, že hodnoty prodejů budou nezávislé na vzniklých nákladech. Hodnota prodeje je pevná a nemění se, když dále odhadujete náklady nebo když další náklady.

## <a name="project-price-lists"></a>Projektové ceníky

Ceníky projektu se používají ke stanovení výchozích cen (nikoli nákladových sazeb) za čas, výdaje a další součásti související s projektem. Ceníků může být více. Každý ceník má svoji vlastní datovou účinnost pro každou projektovou smlouvu. V aplikaci Project Operations není podporováno překrývání dat účinnosti u projektových ceníků.

Když je vytvořena smlouva o projektu získáním nabídky projektu, zkopírují se ceníky projektu s uvedením názvu a data smlouvy. Kopírování těchto informací představuje vlastní určení ceny pro komponenty projektu v této smlouvě projektu.

## <a name="transaction-classes"></a>Třídy transakcí

Aplikace Project Operations podporuje čtyři typy tříd transakcí:

- Čas
- Výdaje
- Materiál
- Poplatek

Hodnoty nákladů a prodejů lze odhadnout a vytvořit ve třídách transakcí Čas, Výdaje a Materiál. Poplatek je pouze příjmovou třídou transakcí.

## <a name="work-entities-and-billing-entities"></a>Pracovní entity a fakturační entity

Entity, které představují práci, jsou projekty a úkoly. Entity, které představují aspekty fakturace, jsou řádky smlouvy. Různé pracovní entity můžete propojit s možnostmi fakturace jejich přidružením k řádkům smlouvy.

## <a name="multi-customer-deals"></a>Obchody s více zákazníky

Obchody s více zákazníky fakturují více než jednomu zákazníkovi u obchodu. Běžné příklady tohoto typu zahrnují:

- Podniky OEM a jejich partneři: Partneři a prodejci prodávají produkt s některými službami s přidanou hodnotou, obvykle zahrnující konkrétní dohodu se zákazníkem. Výrobce OEM nabízí financování části projektu. 

- Projekty veřejného sektoru: Několik oddělení místní samosprávy souhlasí s financováním projektu a fakturuje se jim podle předem dohodnutého rozdělení. Například školní obvod a místní úřad souhlasí s financováním stavby bazénu.

## <a name="invoice-schedules"></a>Rozpisy faktur

Rozpisy faktur jsou specifické pro každý řádek smlouvy a jsou vyžadovány pro fungování automatické fakturace. Rozpisy faktur jsou vytvářeny na základě určitých dat zahájení a ukončení a četnosti faktur. Rozpisy se používají ve fázi smlouvy, když je konfigurován proces automatického vytváření faktur. Když je projektová smlouva vytvořena z projektové nabídky, rozpis faktur se zkopíruje do projektové smlouvy z nabídky.

## <a name="changes-from-dynamics-365-sales-orders"></a>Změny oproti objednávce aplikace Dynamics 365 Sales

Smlouvy v Project Operations jsou postaveny na objednávkách v Dynamics 365 Sales. Existují však důležité odchylky a rozdíly ve funkčnosti. Smlouvy mají svůj vlastní formulář a prvky uživatelského rozhraní, obchodní pravidla, obchodní logiku v modulech plug-in, a skripty na straně klienta, díky nimž se liší od smluv. Z těchto důvodů nepoužívejte prodejní objednávku a smlouvu Project Operations záměnně.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
