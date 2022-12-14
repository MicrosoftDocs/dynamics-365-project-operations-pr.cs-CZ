---
title: Koncepty jedinečné pro nabídky na základě projektu
description: Tento článek poskytuje informace o cenových nabídkách projektu v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824319"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Koncepty jedinečné pro nabídky na základě projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Než začnete používat projektové nabídky v Microsoft Dynamics 365 Project Operations, musíte znát následující klíčové koncepty.

## <a name="owning-company"></a>Vlastnící společnost

Vlastnící společnost představuje právnickou osobu, která vlastní doručování projektu. Zákazník na cenové nabídce musí být platným zákazníkem v této právnické osobě ve finančních a provozních aplikacích. Měna vlastnící společnosti a měna smluvní jednotky, která je vybrána na základě projektové nabídky, se musí shodovat.

## <a name="contracting-unit"></a>Smluvní jednotka

Smluvní jednotka představuje divizi nebo postup, které vlastní dodávku projektu. Náklady na zdroje můžete nastavit pro každou smluvní jednotku. Když zadáte náklady na zdroj u zdroje ve smluvní jednotce, můžete nastavit různé nákladové sazby pro zdroje, které si tato smluvní jednotka vypůjčí, nebo jiné divize či postupy v rámci podniku. Tyto nákladové sazby se označují jako vnitropodnikové ceny, výpůjčky zdrojů nebo ceny za směnu. Když nastavujete náklady na půjčování zdrojů od jiných divizí, můžete nastavit tyto nákladové sazby v měně půjčující divize.

## <a name="cost-currency"></a>Měna nákladů

Měna nákladů v aplikaci Project Operations je měna, ve které se vykazují náklady. Tato měna je odvozena od měny připojené k poli **Smluvní jednotka** nabídky, smlouvy a projektu. Náklady projektu lze zaznamenat v jakékoli měně. Existuje však převod měny z měny zaznamenaných nákladů na měnu nákladů projektu.

Vzhledem k tomu, že směnné kurzy v platformě Dataverse nemohou být účinné od data, mohou se součty nákladů na obrazovce v průběhu času změnit, pokud aktualizujete směnné kurzy měn. Náklady zaznamenané v databázi však zůstanou nezměněny, protože částky jsou uloženy v měně, ve které vznikly.

## <a name="sales-currency"></a>Měna prodeje

Měna prodeje v aplikaci Project Operations je měna, ve které jsou zaznamenávány a zobrazovány odhadované a skutečné částky prodeje. Je to také měna, ve které je zákazníkovi fakturován obchod. U projektové nabídky je výchozí měna prodeje převzata ze záznamu zákazníka nebo účtu a lze ji změnit při vytvoření nabídky. Po uložení nabídky nelze však měnu prodeje změnit. Výchozí hodnoty ceníků produktů a projektů jsou založeny na měně prodeje nabídky.

Na rozdíl od nákladů lze hodnoty prodejů zaznamenat **pouze** v měně prodeje.

## <a name="billing-method"></a>Způsob fakturace

Projekty mají obvykle smluvní modely s pevným poplatkem a založené na spotřebě. V Project Operations je smluvní model projektu reprezentován metodou účtování. Metoda účtování má dvě hodnoty: čas a materiál a pevná cena.

- **Čas a materiál** – Smluvní model založený na spotřebě, kde jsou všechny vzniklé náklady kryty odpovídajícími výnosy. S novým odhadem nebo při vzniku dalších nákladů se také zvýší odpovídající odhadovaný a skutečný prodej. Na řádcích nabídek, které mají tuto metodu fakturace, můžete určit nepřekročitelné limity. Tímto způsobem můžete zastropovat skutečné výnosy. Odhadované výnosy nejsou nepřekročitelnými limity ovlivněny.
- **Pevná cena** – Jedná se o smluvní model s pevným poplatkem, kde hodnoty prodejů budou nezávislé na vzniklých nákladech. Hodnota prodeje je pevná a nemění se, když dále odhadujete náklady nebo když další náklady.

## <a name="project-price-lists"></a>Projektové ceníky

Ceníky projektu jsou ceníky, které se používají k zadání výchozích cen (nikoli nákladových sazeb) za čas, výdaje a další součásti související s projektem. Může existovat více ceníků a každý ceník může mít své vlastní datum platnosti pro každou nabídku projektu. Project Operations nepodporuje překrývající se data platnosti projektových ceníků.

## <a name="product-price-lists"></a>Produktové ceníky

Ceníky produktů jsou ceníky, které se používají k zadání výchozích cen (nikoli nákladových sazeb) za řádky založené na produktech v nabídce. Existuje pouze jeden produktový ceník na nabídku.

## <a name="transaction-classes"></a>Třídy transakcí

Aplikace Project Operations podporuje čtyři typy tříd transakcí:

- Čas
- Výdaje
- Materiál
- Poplatek

Hodnoty nákladů a prodejů lze odhadnout a vytvořit ve třídách transakcí **Čas**, **Výdaje** a **Materiál**. **Poplatek** je pouze příjmovou třídou transakcí.

## <a name="work-entities-and-billing-entities"></a>Pracovní entity a fakturační entity

Projekty a Úkoly jsou entity, které představují práci. Řádky nabídky a Řádky smlouvy jsou entity, které představují fakturaci. Různé pracovní entity můžete propojit s možnostmi fakturace jejich přidružením k řádkům nabídky nebo smlouvy.

## <a name="multi-customer-deals"></a>Obchody s více zákazníky

K obchodům s více zákazníky dochází, když se má fakturovat více než jednomu zákazníkovi. Zde je uvedeno několik typických příkladů:

- **Podniky výrobce originálního vybavení (OEM) a jejich partneři** – Partneři a prodejci prodávají produkt obsahující služby s přidanou hodnotou. OEM během obchodu se zákazníkem obvykle nabízí financování části projektu.
- **Projekty veřejného sektoru** – Několik oddělení místní samosprávy souhlasí s financováním projektu a fakturuje se jim podle předem dohodnutého rozdělení. Například školní obvod a oddělení městského úřadu nebo místní vlády souhlasí s financováním stavby bazénu.

## <a name="invoice-schedules"></a>Rozpisy faktur

Rozpisy faktur jsou specifické pro každý řádek nabídky a jsou volitelné. Rozpisy faktur jsou vytvářeny na základě určitých dat zahájení a ukončení a četnosti faktur. Používají se ve fázi smlouvy, když je konfigurován proces automatického vytváření faktur. Ve fázi nabídky jsou rozpisy faktur volitelné. Když se vytvářejí během fáze nabídky, jsou zkopírovány do projektové smlouvy, která je vytvořena při získání projektové nabídky.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Rozdíly oproti nabídce aplikace Dynamics 365 Sales

Nabídky Project Operations vycházejí z nabídek Dynamics 365 Sales. Existují však některé důležité rozdíly ve funkčnosti, které byste měli znát:

- Nabídky Project Operations mají dva různé typy řádků, jedny pro projekty a druhé pro produkty.
- Nabídky Project Operations mají svou vlastní stránku a prvky uživatelského rozhraní, obchodní pravidla, obchodní logiku v modulech plug-in, a skripty na straně klienta, díky nimž se liší od nabídek aplikace Sales.
- V Sales můžete k prodejní nabídce můžete připojit jednu objednávku. V Project Operations můžete k projektové nabídce připojit pouze jednu projektovou smlouvu.
- Když získáte prodejní nabídku, související příležitost může zůstat otevřená. Po získání projektové nabídky je související příležitost uzavřena.
- Prodejní nabídka neobsahuje některá pole a koncepty, které jsou součástí projektové nabídky. Mezi tato pole patří **Smluvní jednotka**, **Manažer obchodních vztahů** a **Fakturační adresa – jméno kontaktu**.
- Prodejní nabídky a projektové nabídky jsou také identifikovány pomocí pole **Typ** založeného na sadě možností. U prodejní nabídky má toto pole hodnotu **Na základě zboží**. U projektové nabídky má hodnotu **Na základě práce**.

Z důvodu těchto rozdílů nedoporučujeme používat zaměnitelně faktury v Sales a Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
