---
title: Dotaz Plán výdajů z federálních grantů
description: Toto téma poskytuje informace o dotazu Plán výdajů z federálních grantů.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073764"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Dotaz Plán výdajů z federálních grantů

[!include [banner](../includes/banner.md)]

Podle oběžníku A-133 Úřadu pro správu a rozpočet (Office of Management and Budget) se na agentury, které dostávají federální fondy, vztahují požadavky na audit, které se označují také jako jednotné audity. Proces auditu se používá k pravidelnému podávání zpráv o příjmech a výdajích plynoucích z federálních grantů. Součástí zprávy o jednotném auditu je Plán výdajů z federálních grantů (Schedule of Expenditures of Federal Awards, SEFA).

Dotaz Plán výdajů z federálních grantů zahrnuje název a číslo katalogu federální domácí pomoci (CFDA), číslo grantu, rok poskytnutí grantu, název federální agentury, která poskytuje finanční prostředky, a název předávací entity. Dotaz je určen pro konkrétní období. Toto období je obvykle stejné jako období finančního výkazu, což je fiskální rok.

Dotaz zahrnuje granty, které mají projekční data ve vybraném časovém období. Sloupec **Grantor agency** (Grantová agentura) v dotazu uvádí zákazníka grantu nebo – u předávacího grantu – agenturu poskytující granty. U předávacího grantu je ve sloupci **Pass-through agency** (Předávací agentura) uveden zákazník grantu. Jestliže grant není předávací, je sloupec **Pass-through agency** (Předávací agentura) ponechán prázdný.

## <a name="set-up-the-cfda-clusters"></a>Nastavení clusterů CFDA

Musíte nastavit clustery CFDA, které lze přidružit k číslům CFDA v dotazu Plán výdajů z federálních grantů.

1. Přejděte do nabídky **Řízení projektů a účetnictví \> Nastavení \> Granty \> Katalog clusterů federální domácí pomoci**.
2. Výběrem položky **Nový** vytvoříte cluster CFDA.
3. Zadejte název clusteru.
4. Výběrem možnosti **Uložit** uložte změny.

## <a name="set-up-cfda-numbers"></a>Nastavení čísel CFDA

Musíte nastavit čísla CFDA, které lze přidat ke grantům a zahrnout do dotazu Plán výdajů z federálních grantů.

1. Přejděte do nabídky **Řízení projektů a účetnictví \> Nastavení \> Granty \> Katalog čísel federální domácí pomoci**.
2. Výběrem položky **Nové** vytvoříte číslo CFDA.
3. Do sloupce **Číslo** zadejte číslo CFDA.
4. Stiskněte **tabulátor**.
5. Do sloupce **Popis** zadejte název CFDA.
6. Stiskněte **tabulátor**.
7. Volitelné: V poli **Programový cluster** přidejte příslušný cluster CFDA.
8. Výběrem možnosti **Uložit** uložte změny.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Nastavení grantů, které budou vykazovány v dotazu Plán výdajů z federálních grantů

1. Přejděte do nabídky **Řízení projektů a účetnictví \> Granty \> Granty** a vyberte existující grant.
2. Na pevné záložce **Nastavení** přiřaďte číslo CFDA v poli **Katalog federální domácí pomoci**. Číslo CFDA na grantu určuje cluster CFDA pro podávání zpráv.
3. Na pevné záložce **Kontaktní informace** zadejte informace o poskytovateli grantů pomocí následujícího postupu:

    1. V poli **Zákazník grantu** zadejte zákazníka, který je odpovědný za grant. U stávajícího grantu mohou být tyto informace již zadány.
    2. Uveďte, zda je zákazník grantu sám plátcem. Pokud je zákazník grantu plátcem, nechte zaškrtávací políčko **Předávací** vypnuté. Pokud je plátcem jiný zákazník a za utrácení a sledování peněz je odpovědný zákazník grantu, zapněte zaškrtávací políčko **Předávací**.

4. Pokud jste v předchozím kroku zapnuli zaškrtávací políčko **Předávací**, zadejte v poli **Grantová agentura** zákazníka, který poskytl grant. Agentura poskytující granty a zákazník grantu nemohou být stejní zákazníci.

Zde je příklad předávacího grantu:

Federální vláda financovala projekt infrastruktury pro stát. Federální vláda dala státu peníze na útratu. V tomto případě je federální vláda agenturou poskytující granty a stát je zákazníkem grantu.

> [!NOTE] 
> Při prvním zapnutí této funkce budou počáteční čísla CFDA zadána pomocí stávajících čísel v grantech.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Vyloučení grantů z vykazování SEFA na základě typu grantu

1. Přejděte do nabídky **Řízení projektů a účetnictví \> Nastavení \> Granty \> Typy grantů**.
2. Na pevné záložce **Výchozí informace** zapněte zaškrtávací políčko **Vyloučit z plánu výdajů z federálních grantů**.
3. Výběrem možnosti **Uložit** uložte změny.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Spuštění dotazu Plán výdajů z federálních grantů

1. Přejděte do nabídky **Řízení projektů a účetnictví \> Dotazy a sestavy \> Dotaz na grant \> Plán výdajů z federálních grantů**.
2. V části **Parametry** postupujte takto:

    1. V poli **Interval dat** vyberte kód pro časový interval. Případně definujte časový interval v polích **Od data** a **Do data**.
    2. Volitelné: Chcete-li do dotazu zahrnout jako výnos pouze fakturované transakce, nastavte možnost **Zahrnout pouze fakturované výnosy** na **Ano**.

## <a name="columns"></a>Sloupce

Dotaz Plán výdajů z federálních grantů zahrnuje následující sloupce:

- Katalog názvů clusterů federální domácí pomoci
- Grantová agentura
- Předávací agentura
- Název grantu
- ID grantu
- ID aplikace grantu
- Katalog federální domácí pomoci
- Potvrzení
- Výdaje
