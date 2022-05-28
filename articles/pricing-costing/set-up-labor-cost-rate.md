---
title: Nastavení nákladových sazeb za práci
description: Toto téma poskytuje informace o tom, jak nastavit sazby za náklady na práci v aplikaci Project Operations
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 96c74195209641f31e84af9159241123559fab17
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588498"
---
# <a name="set-up-labor-cost-rates"></a>Nastavení nákladových sazeb za práci

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_


Každý ceník obsahuje sadu sazeb za práci (cen rolí), které jsou spojeny s kontextem a datem účinnosti ceníku.

1. Vytvořte ceník a na kartě **Cena role** v podmřížce vyberte **Nová role**.
2. Na stránce **Vytvořit** vyberte roli a organizační jednotku.
3. Zadejte informace do všech dalších povinných polí.

Následující tabulka obsahuje některá pole, která jsou důležitá při vytváření sazeb práce v ceníku nákladů.

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| Role | Karta **Všeobecné** a stránky **Vytvořit** | Vyberte roli, na kterou se nákladová sazba vztahuje. | Role u příchozího odhadu nebo skutečné hodnoty bude porovnána s tímto řádkem za účelem určení výchozího nákladu role. |
| Společnost poskytující zdroje | Karta **Všeobecné** a stránky **Vytvořit** | Vyberte právnickou osobu, které je role přiřazena. Například vývojář ze společnosti Fabrikam Indie nebo vývojář z Fabrikam USA. | Společnost poskytující zdroje u příchozího odhadu nebo skutečné hodnoty bude porovnána s tímto řádkem za účelem určení výchozí nákladové sazby role. |
| Jednotka zdroje | Karta **Všeobecné** a stránky **Vytvořit** | Vyberte organizační jednotku nebo divizi společnosti, ze které bude tato role použita. Například vývojář z divize Robotics společnosti Fabrikam Indie nebo vývojář z divize Software společnosti Fabrikam USA. | Jednotka zdroje u příchozího odhadu nebo skutečné hodnoty bude porovnána s tímto řádkem za účelem určení výchozího nákladu role. |
| Cena | Karta **Všeobecné** a stránky **Vytvořit** | Nastavte nákladovou sazbu pro kombinaci role, společnosti zajišťující zdroje a jednotku zdrojů. Například vývojář ze společnosti Fabrikam Indie stojí 1000 INR nebo vývojář z Fabrikam USA stojí 150 USD. | Cena je nákladová sazba, jejíž výchozí hodnotou je jednotková cena řádku příchozího odhadu nebo skutečné hodnoty pro třídu transakcí **Čas**. |
| Měna | Karta **Všeobecné** a stránky **Vytvořit** | Ve výchozím nastavení hodnota měny pochází z měny v záhlaví nákladového ceníku, ale může být přepsána. Například vývojář z Fabrikam Indie stojí 1 000 INR. Vývojář z Fabrikam USA stojí 150 USD. | Tato měna je výchozí pro jednotkový náklad řádku příchozího skutečného nákladu pro třídu transakcí **Čas**. U odhadu projektu se hodnota měny převede na projektovou měnu a zobrazí se v časově odstupňovaném zobrazení odhadu. |
| Rozpis jednotky | Karta **Všeobecné** a stránky **Vytvořit** | Rozpis jednotky má jako výchozí nastaven Čas a toto nelze u entity ceny role změnit, protože se používá k vyjádření sazeb podle časových jednotek. | Nemá to žádný následný dopad. |
| Jednotka | Karta **Všeobecné** a stránky **Vytvořit** | Hodnota jednotky implicitně pochází z pole **Časová jednotka** v záhlaví nákladového ceníku. Hodnota může být přepsána. Například vývojář ze společnosti Fabrikam Indie stojí 1000 INR za **Den v Indii**. Vývojář z Fabrikam USA stojí 150 USD za **Den v USA**. | Systém používá systém jednotek a převod v základních jednotkách k výpočtu nákladů za jednotku určené k výpočtu výchozí ceny za jednotku v řádku příchozího odhadu nebo skutečné hodnoty, . Například odhad je 10 **dnů v Indii** práce pro vývojáře z Indie, a jednotka **Den v Indii** je definována jako 10 hodin. Při výpočtu tohoto řádku odhadu aplikace vypočítá jednotkové náklady u odhadu jako: 1 000 INR / 10 hodin = 100 INR za hodinu. Výsledek je převeden na USD a zobrazen jako jednotkové náklady na stránce **Odhady projektu**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Přenos cen a nákladů u zdrojů mimo vaši divizi nebo právnickou osobu

Projektové společnosti běžně využívají k práci na projektech zaměstnance z jiných právnických osob nebo divizí. Projekty lze provádět jednou právnickou osobou, ale zaměstnanci nebo konzultanti, kteří na projektu pracují, mohou pocházet ze stejné nebo z jiné právnické osoby, případně může jít o kombinaci obou možností. V Dynamics 365 Project Operations je právnickou osobou, která vlastní dodávku projektu, **Vlastnická společnost** a divize, která vlastní dodávku, je **Smluvní jednotka**. Ostatní právnické osoby, které dodávají zdroje, se označují jako **Společnosti poskytující zdroje** a divize, které dodávají zdroje, se nazývají **Jednotky zdrojů**. Ve většině zemí jsou společnosti povinny zajistit, aby právnická osoba nebo divize zajišťující zdroje účtovala za použití zdrojů vlastnické společnosti a smluvní jednotce.

Například společnost Fabrikam musí zajistit, aby společnost Fabrikam Indie - Robotics měla sjednaný nákladový tarif se společností Fabrikam USA - Robotics nebo Fabrikam UK - Robotics.

Vývojář ze společnosti Fabrikam Indie - Robotics účtuje 100 USD při zapůjčení do společnosti Fabrikam USA - Robotics a 150 USD při zapůjčení společnosti Fabrikam UK - Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Nastavení nákladů na externí zdroje

1. Vytvořte nákladový ceník s názvem *Sazby nákladů společnosti Fabrikam USA - Robotics* a nastavte rozsah jeho platnosti.
2. V nákladovém ceníku nastavte sazby pomocí informací z následující tabulky. 

| Role | Společnost poskytující zdroje | Jednotka zdroje | Nákladová sazba |
| --- | --- | --- | --- |
| Developer | Fabrikam Indie | Fabrikam Indie - Robotics | 100 dolarů |
| Developer | Fabrikam Filipíny | Fabrikam Filipíny - Robotics | 90 USD |
| Developer | Fabrikam USA | Fabrikam USA - Robotics | 150 USD |

3. Připojte tento nákladový ceník k organizační jednotce Fabrikam USA - Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Nastavte cenu za převod pro zdroj v příslušné měně 

V Project Operations lze nastavit ceny zdrojů v jakékoli měně. Výchozí měna je převzata ze záhlaví ceníku, lze ji však změnit.

Pomocí příkladu pro nastavení ceny za převod lze informace změnit na:

Společnost Fabrikam musí zajistit, aby společnost Fabrikam Indie - Robotics měla sjednanou nákladovou sazbu se společností Fabrikam USA - Robotics nebo Fabrikam UK - Robotics.

Vývojář ze společnosti Fabrikam Indie - Robotic stojí 5000 INR při zapůjčení do společnosti Fabrikam USA - Robotics a 5500 INR při zapůjčení společnosti Fabrikam UK - Robotics.

V nákladovém ceníku pro společnost Fabrikam USA - Robotics lze sazby nákladů vyjádřit jako:

| Role | Společnost poskytující zdroje | Náklady |
| --- | --- | --- |
| Developer | Fabrikam Indie | 5000 INR |
| Developer | Fabrikam USA | 115 USD |

V nákladovém ceníku pro společnost Fabrikam UK - Robotics lze sazby nákladů vyjádřit takto:

| Role | Společnost poskytující zdroje | Náklady |
| --- | --- | --- |
| Developer | Fabrikam Indie | 5500 INR |
| Developer | Fabrikam UK | 115 GBP |

Nákladový ceník může poskytovat sazby práce ve více měnách. Při generování odhadu nákladů na projekt převede Project Operations tyto nákladové sazby na projektovou měnu a zobrazí ji uživateli. Když je časová položka schválena a je vytvořena skutečná cena, bude skutečná cena oceněna v měně tohoto odpovídajícího řádku ceny role v nákladovém ceníku. Skutečné náklady za čas na jednom projektu lze zaznamenat ve více měnách. Při shrnutí nebo sečtení skutečných pracovních nákladů na úrovni projektu však aplikace Project Operations převede všechny částky pracovních nákladů do měny projektu, kterou může uživatel zobrazit.


[!INCLUDE[footer-include](../includes/footer-banner.md)]