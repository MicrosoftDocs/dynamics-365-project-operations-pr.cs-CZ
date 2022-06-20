---
title: Projektové smlouvy – klíčové koncepty – omezené
description: Tento článek poskytuje informace o klíčových konceptech projektových smluv.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e92edadc49469ad5f541be8bce7b7a8043b981e2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932656"
---
# <a name="concepts-unique-to-project-contracts"></a>Koncepty jedinečné pro projektové smlouvy

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_



Tento článek poskytuje klíčové koncepty, které je třeba znát, než začnete používat projektové smlouvy v Dynamics 365 Project Operations:

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

## <a name="product-price-lists"></a>Produktové ceníky

Ceníky produktů se používají ke stanovení výchozích cen (nikoli nákladových sazeb) za řádky založené na produktech ve smlouvě. Existuje pouze jeden produktový ceník na smlouvu.

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

Obchody s více zákazníky fakturují více než jednomu zákazníkovi u obchodu. K běžným příkladům patří:

- Podniky OEM a jejich partneři: Partneři a prodejci prodávají produkt s některými službami s přidanou hodnotou, obvykle zahrnující konkrétní dohodu se zákazníkem. Výrobce OEM nabízí financování části projektu. 

- Projekty veřejného sektoru: Několik oddělení místní samosprávy souhlasí s financováním projektu a fakturuje se jim podle předem dohodnutého rozdělení. Například školní obvod a místní úřad souhlasí s financováním stavby bazénu.

## <a name="invoice-schedules"></a>Rozpisy faktur

Rozpisy faktur jsou specifické pro každý řádek smlouvy a jsou vyžadovány pro fungování automatické fakturace. Rozpisy faktur jsou vytvářeny na základě určitých dat zahájení a ukončení a četnosti faktur. Rozpisy se používají ve fázi smlouvy, když je konfigurován proces automatického vytváření faktur. Když je projektová smlouva vytvořena z projektové nabídky, rozpis faktur se zkopíruje do projektové smlouvy z nabídky.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Změny oproti smlouvě Dynamics 365 Sales

Smlouvy v Project Operations jsou postaveny na smlouvách v Dynamics 365 Sales. Existují však některé důležité odchylky a rozdíly ve funkčnosti, které byste měli znát:

- Smlouvy Project Operations mají dva různé typy řádků, jedny pro projekty a druhé pro produkty.
- Smlouvy Project Operations mají svůj vlastní formulář a prvky uživatelského rozhraní, obchodní pravidla, obchodní logiku v modulech plug-in, a skripty na straně klienta, díky nimž se liší od smluv aplikace Sales.

Z těchto důvodů nepoužívejte smlouvu Sales a projektovou smlouvu záměnně.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
