---
title: Scénáře s více měnami (verze 3.x)
description: Toto téma poskytuje informace o scénářích s více měnami.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4b589142-952d-4121-ab5c-3aa7a85690e2
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9dbd7755e2dc4bd33f264feb7d8bf9f2a4a0787
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750297"
---
# <a name="multiple-currency-scenarios"></a>Scénáře s více měnami

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 má dva koncepty měn:

- **Měna transakce** – měna, v níž transakce probíhá. 
- **Základní měna** – měna instance Dynamics 365. Tato měna se nastavuje při zřizování instance Dynamics 365. Nelze ji změnit.

Společnost Contoso US například prodala zákazníkům ve Spojeném království 100 triček, každé za 15 liber šterlinků (GBP). Následující tabulka ukazuje, jak je tato transakce zaznamenána v entitě Produkt objednávky.

| Produkt | Množství | Cena za jednotku | Měna | Částka | Směnný kurz | Cena za jednotku (základní)| Částka (základní)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Tričko | 100      | 15             | GBP      | 1500   | 0.94          | 17,25 $               | 1 725 $       |

Sloupec **Měna** zobrazuje měnu transakce, která je měnou, ve které došlo k prodeji. Sloupec **Směnný kurz** je směnný kurz mezi měnou transakce a základní měnou. Základní měnou je americký dolar (USD). Tato základní měna byla nastavena při zřizování instance Dynamics 365.
Jak ukazuje tabulka, každá transakce je zaznamenána jak v měně transakce, tak v základní měně. Dynamics 365 používá k výpočtu částek základní měny směnný kurz.

## <a name="project-service-automation-extensions"></a>Rozšíření Project Service Automation

Dynamics 365 Project Service Automation ovlivňuje měnu transakce, protože obchodní transakce mají obvykle dva aspekty: náklady a prodej.

Následující entity jsou považovány za obchodní transakce:

- Podrobnosti řádku nabídky
- Podrobnosti řádku projektové smlouvy
- Řádek odhadu
- Řádek deníku
- Podrobnosti řádku faktury
- Skutečnost

V každé z těchto entit existuje záznam, který představuje částku nákladů nebo částku prodeje. Stejně jako u každé entity Dynamics 365, která obsahuje pole **Částka**, obsahuje každý záznam částky v měně transakce i v základní měně. 

PSA rozšiřuje koncept měny transakce pro náklady a prodej následujícími způsoby:

- Měna nákladové transakce pro časové transakce vždy pochází z měny organizační jednotky, která projekt vlastní nebo spravuje. Tato organizační jednotka je známa jako smluvní jednotka.
- Měna prodejní transakce pro časové a výdajové transakce vždy pochází z měny projektové smlouvy.
- Měna nákladové transakce pro výdaje pochází z měny, ve které byla výdajová položka vytvořena.

## <a name="multiple-currency-scenario"></a>Scénář s více měnami

Tato část popisuje příklad projektu, který společnost Contoso UK dodává pro zákazníka s názvem Fabrikam, Japonsko. Zde je způsob nastavení scénáře:

1. V části **Nastavení** \> **Správa podniku** \> **Měny** je nastaveno GBP a japonský jen. 
2. Je vytvořen zákaznický obchodní vztah s názvem **Fabrikam – Japonsko** a jako měna je vybráno JPY.
3. Je vytvořena organizační jednotka nazvaná **Contoso UK** a jako měna je zvoleno GBP.
4. Je vytvořena projektová smlouva, kde **Contoso UK** je určena jako smluvní jednotka a **Fabrikam – Japonsko** je specifikována jako zákazník.
5. Řádky projektové smlouvy se vytvářejí na základě řešení fakturace pro různé třídy transakcí projektu, jako je například fakturace za čas versus fakturace za výdaje.
6. Je vytvořen projekt, kde **Contoso UK** je specifikována jako smluvní jednotka. Tento projekt je vytvořen a namapován na řádky projektové smlouvy.


Během odhadu, který používá podrobnosti řádku nabídky, podrobnosti řádku projektové smlouvy nebo na řádku odhadu plánu, jsou v entitě vždy vytvořeny dva záznamy. Jeden záznam je pro náklady a druhý záznam je pro prodej.

- Ve výchozím nastavení je měna transakce v záznamu nákladů nastavena na měnu smluvní jednotky projektu. V tomto příkladu je měnou GBP.
- Ve výchozím nastavení je měna transakce v záznamu prodeje nastavena na měnu projektové smlouvy. V tomto příkladu je měnou JPY.

Při vytváření skutečných hodnot pro čas pomocí časového záznamu nebo řádku deníku, dojde k následujícímu chování:

- Ve výchozím nastavení je měna transakce v záznamu nákladů nastavena na měnu smluvní jednotky projektu.
- Ve výchozím nastavení je měna transakce v záznamu prodeje nastavena na měnu projektové smlouvy.

Při vytváření skutečných hodnot pro výdaje pomocí výdajové položky nebo řádku deníku, dojde k následujícímu chování:

- Částku výdajů můžete zaznamenat v libovolné měně. Vyberte měnu pomocí výběru měny na stránce **Výdajová položka** nebo na stránce **Řádek deníku**. Ve výchozím nastavení je měna transakce pro záznam nákladů nastavena na měnu na výdajové položce. 
- Ve výchozím nastavení je měna transakce pro záznam prodeje měna projektové smlouvy. Chcete-li nastavit tuto měnu, systém nejprve převede částku transakce v měně, kterou uživatel zadal do základní měny. Poté převede částku na měnu projektové smlouvy. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Výpočet souhrnů při zaznamenávání skutečných hodnot projektu ve více měnách transakcí

Dynamics 365 automaticky zpracovává souhrny částek v různých měnách. Zde je příklad:

| Třída transakce | Typ transakce| Date   | Zdroj | Kategorie transakce | Množství | Cena za jednotku | Částka      | Směnný kurz | Částka v základní měně |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Nefakturovaný prodej   | 14. VI. | Kamil  |                      | 8 hod    | 20 000 JPY    | 160 000 JPY | 123           | 1 300,81 USD    |
| Time              | Nefakturovaný prodej   | 15. VI. | Kamil  |                      | 8 hod    | 20 000 JPY    | 160 000 JPY | 123           | 1 300,81 USD    |
| Výdaj           | Nefakturovaný prodej   | 16. VI. | Kamil  | Hotel                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Výdaj           | Nefakturovaný prodej   | 17. VI. | Kamil  | Pronájem auta           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

K výpočtu celkové nefakturované hodnoty prodeje projektu můžete vytvořit souhrnné pole pro pole **Částka** na všech souvisejících nefakturovaných skutečných hodnotách prodeje. Toto souhrnné pole je konstruktem aplikace Dynamics 365, která u souvisejících záznamů umožňuje rychlé vzorce.
