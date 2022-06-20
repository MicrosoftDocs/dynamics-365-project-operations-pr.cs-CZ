---
title: Nabídky – klíčové koncepty – omezené
description: Tento článek poskytuje informace o tom, jak používat projektové nabídky v Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8c2f009b7a0bebbf6a49bf942dd19f97205072e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916970"
---
# <a name="concepts-unique-to-project-quotes"></a>Koncepty jedinečné pro projektové nabídky

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_


Toto téma poskytuje klíčové koncepty, které musíte znát, než začnete používat projektové nabídky v Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Smluvní jednotka

Smluvní jednotka představuje divizi nebo postup, které vlastní dodávku projektu. Náklady na zdroje můžete nastavit pro každou smluvní jednotku. Když zadáte náklady na zdroj u zdroje ve smluvní jednotce, budete také moci nastavit různé nákladové sazby pro zdroje, které si tato smluvní jednotka vypůjčí, nebo jiné divize či postupy v rámci podniku. Ty se označují jako vnitropodnikové ceny, výpůjčky zdrojů nebo ceny za směnu. Když nastavujete náklady na půjčování zdrojů od jiných divizí, můžete si také zvolit nastavení těchto nákladových sazeb v měně půjčující divize.

## <a name="cost-currency"></a>Měna nákladů

Měna nákladů v aplikaci Project Operations je měna, ve které se vykazují náklady. Tato měna je odvozena od měny připojené k poli **Smluvní jednotka** nabídky, smlouvy a projektu. Náklady projektu lze zapsat v jakékoli měně. Existuje však převod měny z měny zaznamenaných nákladů na měnu nákladů projektu.

Vzhledem k tomu, že směnné kurzy v platformě CDS nemohou být účinné od data, mohou se součty nákladů na obrazovce v průběhu času změnit, pokud aktualizujete směnné kurzy měn. Náklady zaznamenané v databázi však zůstanou nezměněny, protože částky jsou uloženy v měně, ve které vznikly.

## <a name="sales-currency"></a>Měna prodeje

Měna prodeje v aplikaci Project Operations je měna, ve které jsou zaznamenávány a zobrazovány odhadované a skutečné částky prodeje. Je to také měna, ve které je zákazníkovi fakturován obchod. U projektové nabídky je výchozí měna prodeje převzata ze záznamu zákazníka nebo účtu a lze ji změnit při vytvoření nabídky. Po uložení nabídky nelze měnu prodeje změnit. Výchozí hodnoty ceníků produktů a projektů jsou založeny na měně prodeje nabídky.

Na rozdíl od nákladů lze hodnoty prodejů zaznamenat pouze v měně prodeje.

## <a name="billing-method"></a>Způsob fakturace

Projekty mají obvykle smluvní modely s pevným poplatkem a založené na spotřebě. To je v aplikaci Project Operations vyjádřeno jako pole **Způsob fakturace**, které má dvě hodnoty, čas a materiál a pevnou cenu.

- **Čas a materiál:** Jedná se o smluvní model založený na spotřebě, kde jsou všechny vzniklé náklady kryty odpovídajícími výnosy. S novým odhadem nebo při vzniku dalších nákladů se také zvýší odpovídající odhadovaný a skutečný prodej. Na řádcích nabídek, které mají tuto metodu fakturace, můžete určit nepřekročitelné limity. Tím se omezí skutečný příjem. Odhadované výnosy nejsou nepřekročitelnými limity ovlivněny.
- **Pevná cena:** Jedná se o smluvní model s pevným poplatkem, který naznačuje, že hodnoty prodejů budou nezávislé na vzniklých nákladech. Hodnota prodeje je pevná a nemění se, když dále odhadujete náklady nebo když další náklady.

## <a name="project-price-lists"></a>Projektové ceníky

Ceníky projektu jsou ceníky, které se používají ke stanovení výchozích cen (nikoli nákladových sazeb) za čas, výdaje a další součásti související s projektem. Může existovat více ceníků a každý ceník může mít své vlastní datum platnosti pro každou nabídku projektu. V aplikaci Project Operations není podporováno překrývání datumů účinnosti u projektových ceníků.

## <a name="product-price-lists"></a>Produktové ceníky

Ceníky produktů jsou ceníky, které se používají ke stanovení výchozích cen (nikoli nákladových sazeb) za řádky založené na produktech v nabídce. Existuje pouze jeden produktový ceník na nabídku.

## <a name="transaction-classes"></a>Třídy transakcí

Aplikace Project Operations podporuje čtyři typy tříd transakcí:

- Čas
- Výdaje
- Materiál
- Poplatek

Hodnoty nákladů a prodejů lze odhadnout a vytvořit ve třídách transakcí Čas, Výdaje a Materiál. Poplatek je pouze příjmovou třídou transakcí.

## <a name="work-entities-and-billing-entities"></a>Pracovní entity a fakturační entity

Entity, které představují práci, jsou projekty a úkoly. Entity, které představují fakturaci, jsou řádky nabídky a řádky smlouvy. Různé pracovní entity můžete propojit s možnostmi fakturace jejich přidružením k řádkům nabídky nebo smlouvy.

## <a name="multi-customer-deals"></a>Obchody s více zákazníky

K obchodům s více zákazníky dochází, když se má fakturovat více než jednomu zákazníkovi. Běžné příklady tohoto typu zahrnují:

- **OEM podniky a jejich partneři:** Partneři a prodejci prodávají produkt obsahující služby s přidanou hodnotou. Obvykle se jedná o scénář, kdy OEM během konkrétního obchodu se zákazníkem nabízí financování části projektu. 

- **Projekty veřejného sektoru:** Několik oddělení místní samosprávy souhlasí s financováním projektu a fakturuje se jim podle předem dohodnutého rozdělení. Například školní obvod a oddělení městského úřadu nebo místní vlády souhlasí s financováním stavby bazénu.

## <a name="invoice-schedules"></a>Rozpisy faktur

Rozpisy faktur jsou specifické pro každý řádek nabídky a jsou také volitelné. Rozpisy faktur jsou vytvářeny na základě určitých dat zahájení a ukončení a četnosti faktur. Rozpisy faktur se používají ve fázi smlouvy, když je konfigurován proces automatického vytváření faktur. Ve fázi nabídky jsou rozpisy volitelné. Když se vytvářejí rozpisy faktur ve fázi **Nabídka**, jsou zkopírovány do projektové smlouvy, která je vytvořena při získání projektové nabídky.

## <a name="changes-from-dynamics-365-sales-quote"></a>Změny oproti nabídce aplikace Dynamics 365 Sales:

Nabídky Project Operations vycházejí z nabídek Dynamics 365 Sales. Existují však některé důležité rozdíly ve funkčnosti, které byste měli znát:

- Akce **Opravit** a **Aktivovat** nejsou podporovány.
- Nabídky Project Operations mají dva různé typy řádků. Jeden typ je určen pro projekty a druhý pro produkty.
- Nabídky Project Operations mají svůj vlastní formulář a prvky uživatelského rozhraní, obchodní pravidla, obchodní logiku v modulech plug-in, a skripty na straně klienta, díky nimž se liší od nabídek aplikace Sales.

Z těchto důvodů se nedoporučuje zaměňovat nabídky aplikace Sales a nabídky Project Operations.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
