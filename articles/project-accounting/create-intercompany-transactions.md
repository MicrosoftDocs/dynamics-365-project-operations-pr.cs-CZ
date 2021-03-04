---
title: Vytváření mezipodnikových transakcí
description: Toto téma obsahuje informace, jak vytvářet mezipodnikové transakce.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a9d34d69ff59f0cb470bb852d8a80ecaedf6544
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595445"
---
# <a name="create-intercompany-transactions"></a>Vytváření mezipodnikových transakcí

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Mezipodnikové transakce jsou časové a výdajové transakce ze smlouvy o projektu, které patří jedné společnosti nebo organizační jednotce, zatímco prostředky ve smlouvě o projektu jsou součástí jiné společnosti nebo organizační jednotky.

Po schválení mezipodnikové transakce se vytvoří následující skutečné transakce

| **Typ transakce** | **Použitý ceník** | **Měna transakce** |
| --- | --- | --- |
| Náklady | Ceník smluvní jednotkové ceny | Měna na řádku měny |
| Nefakturovaný prodej Ty jsou vytvořeny pouze pro skutečné údaje, které jsou spojeny s řádkem smlouvy s typem fakturace, časem a materiálem. | Prodejní ceník smluvního projektu | Měna smlouvy |
| Jednotkové náklady zdroje | Ceník nákladů jednotky zdroje | Měna na řádku měny |
| Prodeje meziorganizační jednotky | Ceník smluvní jednotkové ceny | Měna na řádku měny |

Náklady, jednotkové náklady na zdroje, ceník transakcí mezi organizacemi a měna se řídí **organizační jednotkou**. To je důležité mít na paměti při rozhodování o tom, jak strukturovat společnosti a organizační jednotky ve vaší implementaci.

Když vytvoříte příležitost, nabídku, smlouvu o projektu a záznamy o projektu, systém ověří, zda se měna smluvní jednotky shoduje s účetní měnou smluvní společnosti. Pokud nejsou stejné, nelze tyto záznamy vytvořit. Měna organizační jednotky je definována v Dynamics 365 Project Operations tím, že přejdete na **Dataverse** > **Nastavení** > **Organizační jednotky**. Účetní měna společnosti je definována v Dynamics 365 Finance tím, že přejdete na **Hlavní kniha** > **Nastavení hlavní knihy** > **Účetní kniha**. Měna je synchronizována s vaším prostředím Dataverse pomocí mapy dvojího zápisu účetních knih.

Systém vytváří jednotkové náklady na zdroje a skutečné prodeje mezi organizačními jednotkami v následujících situacích:

  - Když se zdrojová jednotka liší od kontraktační jednotky
  - Když se zdrojová společnost liší od smluvní jednotky

Avšak pouze transakce, které mají odlišnou zdrojovou společnost od smluvní společnosti, budou převedeny do prostředí Dynamics 365 Finance pro další účtování.

Účtování skutečných hodnot projektu se zaznamenává v deníku integrace Project Operations v Finance. Systém vytvoří následující řádky deníku.

| **Typ transakce** | **Právnická osoba** | **Vytvoří transakci projektu při zaúčtování** | **Výchozí hodnoty finanční dimenze z** | **Výchozí fakturační skupina DPH a fakturační skupina DPH položky** |
| --- | --- | --- | --- | --- |
| Náklady | Nepřidá se do integračního deníku | Neuvedeno | Neuvedeno | Neuvedeno |
| Nefakturovaný prodej | Deník pro integraci vypůjčující právnických osob | Ano | Project | **Skupina fakturace DPH**: Založeno na **smluvním zákazníkovi** <br/> **Skupina DPH fakturační položky**: Z aktuální kategorie projektu právnické osoby na řádku deníku |
| Jednotkové náklady zdroje | Deník pro integraci půjčující právnické osoby | No | Mezipodnikový zákazník | **Skupina fakturace DPH**: Založeno na **mezipodnikovém zákazníkovi** <br/> **Skupina DPH fakturační položky**: Z aktuální kategorie projektu právnické osoby na řádku deníku |
| Meziorganizační prodej | Deník pro integraci půjčující právnické osoby | No | Mezipodnikový zákazník | **Skupina fakturace DPH**: Založeno na **mezipodnikovém zákazníkovi** <br/> **Skupina DPH fakturační položky**: Z aktuální kategorie projektu právnické osoby na řádku deníku |

### <a name="example-intercompany-transactions"></a>Příklad: mezipodnikové transakce

Molly Clarková, vývojářka zaměstnaná v GBPM, zaznamenává 10 hodin práce proti projektu USPM Adventure Works, který je schválen vedoucím projektu. Náklad vývojáře v GBPM je 88 GBP za hodinu. GBPM bude účtovat USPM 120 USD za hodinu vývojáře. USPM bude účtovat zákazníkovi Adventure Works, 200 USD za práci odvedenou prostředkem GBPM. Další informace naleznete v tématu [Konfigurace mezipodnikové fakturace](configure-intercompany-invoicing.md).

1. V Project Operations přejděte na **Zdroje** a vyberte **Molly Clarková** ze seznamu. Na kartě **Plánování** v poli **Společnost** zvolte **GBPM**.
2. Přejděte na **Prodej** > **Zákazníci** a vyberte **Nový** k vytvoření nového zákaznického záznamu pro Adventure Works.
    1. Nastavte společnost na **USPM**.
    2. Nastavte **Typ vztahu** na **Zákazník**.
    3. Vyberte **Skupina zákazníků 10 - domácí**.
    4. Nastavte měnu na **USD**.
    5. Uložte záznam.
3. Přejděte na **Prodej** > **Smlouvy o projektu** a vytvořte novou projektovou smlouvu pro Adventure Works.
    1. Nastavte vlastnickou společnost na **USPM** a smluvní jednotku na **Contoso Robotics USA**.
    2. Jako zákazníka vyberte Adventure Works.
    3. Vyberte ceník produktu a uložte záznam.
    4. Na kartě **Řádky smlouvy** vytvořte nový řádek smlouvy. Nastavte libovolný název a vyberte **Čas a materiály** jako způsob fakturace.
    5. Vytvořte nový projekt a přidružte jej k tomuto řádku smlouvy.
4. Přihláste se jako zdroj **Molly Clarková**. Přejděte na **Projekty** > **Časové údaje** a vytvořte časový údaj pro projekt Adventure Works.
5. Přihlaste se jako projektový manažer. Přejděte na **Projekty** > **Schválování** a schvalte transakci časového údaje zaprotokolovanou Molly Clarkovou.
6. Přejděte na projekt Adventure Works a vyberte **Související** > **Skutečné hodnoty**. Budou vytvořeny následující skutečné transakce.

| **Typ transakce** | **Cena** | **Měna transakce** | **Množství** |
| --- | --- | --- | --- |
| Náklady | 120 | USD | 1200 |
| Nefakturovaný prodej | 200 | USD | 2000 |
| Jednotkové náklady zdroje | 88 | GBP | 880 |
| Prodeje meziorganizační jednotky | 120 | USD | 1200 |

7. Přihlaste se jako účetní USPM. Otevřete instanci Finance Project Operations a vyberte společnost **USPM**. 
8. Přejděte na **Řízení projektů a účetnictví** > **Periodické** > **Project Operations v Customer Engagement** > **Import z fáze** a vyberte spuštění periodického procesu. Tento pravidelný proces vyplní deník integrace Project Operations.
9. Přejděte na **Řízení projektů a účetnictví** > **Deníky** > **Integrační deník Project Operations** a zkontrolujte řádky deníku. Systém vytvoří následující řádek.

    | **Typ transakce** | **Cena** | **Měna transakce** | **Množství** |
    | --- | --- | --- | --- |
    | Nefakturovaný prodej | 200 | USD | 2000 |

    Pokud je systém nastaven tak, aby časově rozlišoval výnosy z tohoto projektu, zaúčtuje se následující:

    - Debet: Projekt - hodnota prodeje probíhající práce (WIP) 200 USD
    - Kredit: Projekt - časově rozlišený výnos 200 USD

    Tento nevyfakturovaný prodej je nyní připraven k fakturaci. Fakturu pro zákazníka Adventure Works lze v případě potřeby finančně zaúčtovat.

10. Přihlaste se jako účetní **GBPM**. Otevřete instanci Finance Project Operations a otevřete společnost **GBPM**. 
11. Přejděte na **Řízení projektů a účetnictví** > **Periodické** > **Project Operations v Customer Engagement** > **Import z fáze** a spusťte periodický proces pro vyplnění deníku integrace Project Operations.
12. Přejděte na **Řízení projektů a účetnictví** > **Deníky** > **Integrační deník Project Operations** a zkontrolujte řádky. Systém vytvoří následující řádky.

    | **Typ transakce** | **Cena** | **Měna transakce** | **Množství** |
    | --- | --- | --- | --- |
    | Jednotkové náklady zdroje | 88 | GBP | 880 |
    | Prodeje meziorganizační jednotky | 120 | USD | 1200 |

    Výsledkem zaúčtování těchto záznamů jsou následující poukazové transakce:

    - Debet: Náklady na projekt 88 GBP
    - Kredit: přidělení mezd 88 GBP

    Pokud je systém nastaven tak, aby časově rozlišoval mezipodnikové výnosy, zaúčtuje se následující:

    - Debet: Projekt - hodnota prodeje probíhající práce (WIP) 120 USD
    - Kredit: Projekt - časově rozlišený výnos 120 USD

    Systém je nyní připraven k vytvoření mezipodnikové faktury zákazníka.


[!INCLUDE[footer-include](../includes/footer-banner.md)]