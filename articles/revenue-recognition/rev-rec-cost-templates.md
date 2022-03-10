---
title: Nastavení šablon nákladů
description: Toto téma poskytuje informace, jak vytvářet a používat šablony nákladů v Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b3a9f1e4f5ea0abe34dc860db87ef349daa46c487b03d271bfe207868c521f39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993548"
---
# <a name="set-up-cost-templates"></a>Nastavení šablon nákladů

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_


Toto téma poskytuje informace, jak vytvářet a používat šablony nákladů v Project Operations. Šablona nákladů určuje:

- Kategorie projektu pro prognózy a skutečné transakce, které mají být zahrnuty do procenta z výpočtu dokončení projektu. Hodnota procenta dokončení se pak použije k výpočtu, kolik výnosů je uznáno.
- Zda lze upravit procento dokončení, pokud se automaticky počítá.
- Zda se procento dokončení vypočítá na základě množství nebo jednotek.

## <a name="cost-template-example"></a>Příklad šablony nákladů

Pracujete na projektu webového designu pro zákazníka, ve kterém si účtujete paušální poplatek ve výši USD 10 000. Předpovídáte, že dokončení projektu bude trvat 100 hodin (5 000 USD). Předpovídáte také dvě letenky a čtyři noci v hotelu na cesty k zákazníkovi (1 800 USD). Výsledkem jsou celkové předpokládané náklady USD 6 800.

Když spustíte proces rozpoznávání výnosů s pevnou cenou a vytvoříte odhad na konci měsíce, zjistíte, že jste na projektu pracovali 35 hodin. To zatím nezahrnuje lety ani náklady na hotel. Také jste nechali asistenta provést pět hodin výzkumu projektu za cenu USD 100, kterou jste neplánovali.

Při výpočtu hodnoty procenta dokončení pro tento projekt je třeba provést následující volby:

- Chcete zahrnout všechny náklady (hodiny a výdaje) nebo jen hodiny?
- Chcete zahrnout všechny hodiny nebo jen plánované hodiny?
- Chcete vypočítat úplné procento na základě dolarových nákladů plánovaných hodin (5 000 USD) nebo jen podle počtu hodin (100)?

Vaše odpovědi na tyto otázky určují možnosti, které nastavíte na šabloně nákladů, a kategorie, které vyberete na řádcích šablony nákladů.

V následující tabulce jsou uvedeny výsledky různých metod výpočtu hodnoty procenta dokončení pro tento scénář.

| Dokončení na základě | Dolarové náklady nebo jednotky | Procento dokončení | Výpočet |
| --- | --- | --- | --- |
| Všechny hodiny, žádné výdaje | Dolarové náklady | 37% 35 x USD 50 + USD 100 = USD 1 850 USD 1 850/USD 5 000 |
| Všechny hodiny, žádné výdaje | Jednotky | 40% | 40 hodin / 100 hodin (včetně pěti neplánovaných hodin) |
| Plánované hodiny, žádné výdaje | Dolarové náklady nebo jednotka | 35% | 35/100 hodin nebo 35 x USD 50 / 5 000 |
| Všechny hodiny a výdaje | Dolarové náklady | 27,2% | USD 1 850 / 6 800 USD |

Rozhodování o tom, jaký zvolit přístup k vytvoření šablony nákladů, může záviset na několika ohledech:

- Pokud do šablony nákladů zahrnete neplánované hodiny, riskujete dosažení 100 procent dokončení před dokončením projektu. Je to proto, že skutečné hodiny budou větší než plánované hodiny. Pokud použijete některou z prvních dvou metod uvedených v tabulce, měli byste změnit plán (předpokládané jednotky), jakmile zjistíte odchylky. V tomto případě byste přidali nebo odečetli hodiny na základě vašich znalostí toho, co je nutné k dokončení projektu. Pokud bude dokončení projektu trvat dalších 65 hodin, přidali byste k plánu pět hodin, celkem tedy 105. Pokud víte, že váš asistent provede dalších pět hodin výzkumu, celková částka bude 110 hodin.
- Pokud použijete třetí metodu uvedenou v tabulce, aktualizujete pouze plánované hodiny pro svůj vlastní čas, aby byl výpočet procenta úplnosti přesný. Vaše ziskovost se změní, když se zaznamenají neplánované hodiny, ale zůstanete na známé trajektorii procentuálního dokončení.
- Pokud použijete čtvrtou metodu uvedenou v tabulce, existuje riziko, že výdaje nastanou v nepravidelných časech a nemusí se promítnout do postupu dokončení. Pokud jsou tedy zahrnuty výdaje, mohou způsobit, že vaše procentní dokončení bude kolísat více, než je žádoucí. Například proto, že jste ještě neletěli, bylo vaše procento dokončení 27 procent namísto 35 procent nebo 37 procent, pokud jste měli výpočet založit pouze na čase. Pokud jste podnikli jednu cestu na dvě noci a předpovídali své letové a hotelové náklady přesně, procento dokončení by bylo 40,4 procenta (1 850 USD za práci a USD 900 za výdaje = USD 2 750 / 6 800 USD = 40,4 procenta). Proto by vznik nákladů pouze na jednu cestu letadlem změnil procento dokončení z 27 procent na 40 procent.

## <a name="create-cost-templates"></a>Vytvořit šablony nákladů
Při vytváření šablony nákladů postupujte takto:

1. Pro přístup k šablonám nákladů v prostředí Dynamics 365 Finance přejděte na **Řízení projektů a účetnictví** > **Založit** > **Odhady** > **Šablona nákladů**.
2. Výběrem možnosti **Nová** vytvořte novou šablonu nákladů. Zadejte jméno a popis.
3. U každého typu transakce uveďte ID řádku nákladů.
4. Vyberte výchozí metodu dokončení:

  - **Automaticky**: Procento dokončení se u projektu vypočítá automaticky. Výslednou hodnotu nelze změnit.
  - **Ručně**: Procento dokončení se u projektu vypočítá automaticky. Výslednou hodnotu lze změnit.

  > [!NOTE]
  > Pro ruční výpočty je procento dokončení udržováno v **Ručním výpočtu** na kartě **Všeobecné** na stránce **Odhad**.

5. V možnosti **Dokončení na základě** vyberte jednu z následujících hodnot:

  - **Množství**: Částka v účetní měně vypočítává procento dokončení.
  - **Jednotka**: Množství vypočítá procento dokončení.
  - **Přímka**: Systém vypočítá procento dokončení na poměrném základě pomocí dat zahájení a ukončení projektu k určení délky projektu.

6. Vyberte **Řádky nákladů** pro kontrolu řádků nákladů šablony nákladů. Pro každý typ transakce je vyžadován alespoň jeden nákladový řádek. Můžete však vytvořit více nákladových řádků pro stejné typy transakcí a nastavit požadované atributy pro tyto řádky.
7. Na kartě **Kategorie** vyberte kategorie projektů, které mají být zahrnuty do řádku šablony nákladů.
8. Na kartě **Všeobecné** vyberte, zda bude tento řádek zahrnut do procenta výpočtu dokončení.
9. Vyberte metodu nákladů na dokončení, která se použije při výpočtu procenta dokončení.


[!INCLUDE[footer-include](../includes/footer-banner.md)]