---
title: Nastavení fakturačních sazeb za práci
description: Toto téma poskytuje informace o tom, jak nastavit fakturační sazby za práci v aplikaci Project Operations.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7d2dd7b6001ddb475d381d35a4863dcc4b322214
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004658"
---
# <a name="set-up-labor-bill-rates"></a>Nastavení fakturačních sazeb za práci

_ **Platí pro:** Project Operations u scénářů založených na zdrojích / položkách, které nejsou na skladě

Každý ceník obsahuje sadu cen rolí nebo pracovních sazeb, které jsou účinné pro kontext a datum účinnosti uvedené v záhlaví ceníku. Sazby faktur za čas v Dynamics 365 Project Operations lze nastavit pouze v jedné měně, což je měna v záhlaví ceníku.

1. Chcete-li nastavit fakturační sazby za práci v prodejním ceníku, přejděte na **Prodeje** > **Zákazníci** > **Ceníky** a výběrem položky **Nový** vytvořte nový ceník. 
2. Na kartě **Ceny rolí** vyberte v podmřížce položku **Nová cena role**. 
3. V podokně **Vytvořit** zadejte kombinaci role a organizační jednotky, pro které potřebujete nastavit fakturační sazbu.

   V následující tabulce je uveden seznam polí na kartě **Všeobecné** a v podokně **Vytvořit** řádku ceny role, na které byste měli pamatovat při vytváření cen rolí v prodejním ceníku:

    | Pole | Místo | Popis | Dopad na následné složky |
    | --- | --- | --- | --- |
    | Role | Karta **Všeobecné** a podokno **Vytvořit** | Vyberte roli, pro kterou nastavujete fakturační sazbu. | Role u příchozího odhadu nebo skutečné hodnoty bude porovnána s tímto řádkem za účelem určení výchozí fakturační sazby role. |
    | Společnost poskytující zdroje | Karta **Všeobecné** a podokno **Vytvořit** | Vyberte společnost nebo právnickou osobu, ze které role pochází. Například vývojář ze společnosti Fabrikam Indie nebo vývojář z Fabrikam USA. | Společnost poskytující zdroje u příchozího odhadu nebo skutečné hodnoty bude porovnána s tímto řádkem za účelem určení výchozí fakturační sazby role. |
    | Jednotka zdroje | Karta **Všeobecné** a podokno **Vytvořit** | Vyberte organizační jednotku nebo divizi společnosti, ze které role pochází. Například vývojář z divize Robotics společnosti Fabrikam Indie nebo vývojář z divize Software společnosti Fabrikam USA. | Jednotka zdroje u příchozího odhadu nebo skutečné hodnoty bude porovnána s tímto řádkem za účelem určení výchozí fakturační sazby role. |
    | Cena | Karta **Všeobecné** a podokno **Vytvořit** | Nastavte fakturační sazbu pro kombinaci role, společnosti zajišťující zdroje a jednotky zdrojů. Například vývojář ze společnosti Fabrikam Indie má fakturační sazbu 100 USD, vývojář ze společnosti Fabrikam USA má fakturační sazbu 150 USD. | Tato cena je výchozí fakturační sazba pro jednotkovou cenu řádku příchozího odhadu nebo skutečné hodnoty pro třídu transakcí Čas. |
    | Měna | Karta **Všeobecné** a podokno **Vytvořit**| Ve výchozím nastavení hodnota měny pochází z měny v záhlaví prodejního ceníku. V prodejním ceníku nelze měnu přepsat. | Tato měna je výchozí měnou pro jednotkovou cenu řádku příchozího skutečného prodeje pro třídu transakcí Čas. |
    | Rozpis jednotky | Karta **Všeobecné** a podokno **Vytvořit** | Tento rozpis jednotky má jako výchozí nastaven Čas a toto nelze u entity ceny role změnit, protože se používá k vyjádření sazeb podle časových jednotek. | Neexistuje žádný následný dopad na toto pole. |
    | Jednotka | Karta **Všeobecné** a podokno **Vytvořit** | Hodnota jednotky pochází z pole **Časová jednotka** v záhlaví prodejního ceníku. Ale tato hodnota nemůže být přepsána. Například vývojář ze společnosti Fabrikam Indie má fakturační sazbu 1000 USD za **Den v Indii**. Vývojář ze společnosti Fabrikam USA má fakturační sazbu 1500 USD za **Den v USA**. | Když je výchozí cena za jednotku založena na řádku příchozího odhadu nebo skutečné hodnoty, systém používá k výpočtu ceny za jednotku systém jednotek a převod v základních jednotkách. Například odhad je 10 **dnů v Indii** práce pro vývojáře z Indie, a jednotka Den v Indii je definována jako 10 hodin. Při ocenění tohoto řádku odhadu aplikace vypočítá jednotkovou cenu v odhadu jako 1000 USD / 10 hodin = 100 USD za hodinu. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Přenos ocenění nebo nastavení fakturačních sazeb pro zdroje z jiných organizačních jednotek nebo divizí 

Projektové společnosti k práci na projektech často využívají zaměstnance z různých právnických osob a různých divizí v rámci právnické osoby. Projekty lze provádět z určité právnické osoby a divize, zatímco zaměstnanci nebo konzultanti, kteří na projektech pracují, mohou pocházet ze stejné právnické osoby a divize nebo z jiné. Projekt by také mohl být tvořen kombinací lidí z různých právnických osob a divizí. V rámci Project Operations se právnická osoba, která vlastní dodávku projektu, nazývá **Vlastnická společnost** a divize, která vlastní dodávku, se nazývá **Smluvní jednotka**. Všechny ostatní právnické osoby, které dodávají zdroje, se označují jako **Společnosti poskytující zdroje** a divize, které dodávají zdroje, se nazývají **Jednotky zdrojů**. Kvůli rozdílům v nákladech na pracovní sílu v různých zeměpisných oblastech a na trzích práce po celém světě jsou fakturační sazby za práci také nastaveny odlišně pro různé zeměpisné oblasti.

Například vývojáři z divize Robotics společnosti Fabrikam Indie pracujícímu na americkém projektu je účtována sazba 100 USD za hodinu. Vývojáři z divize Robotics společnosti Fabrikam USA pracujícímu na americkém projektu je účtována sazba 150 USD za hodinu. 

### <a name="example-set-up-a-bill-rate"></a>Příklad: Nastavení fakturační sazby 

1. Vytvořte prodejní ceník s názvem *Fakturační sazby společnosti Fabrikam USA* a nastavte datum jeho účinnosti.
2. V prodejním ceníku zadejte následující sazby:

    | Role | Společnost poskytující zdroje | Jednotka zdroje | Fakturační sazba |
    | --- | --- | --- | --- |
    | Developer | Fabrikam Indie | Fabrikam Indie - Robotics | 100 dolarů |
    | Developer | Fabrikam Filipíny | Fabrikam Filipíny - Robotics | 90 USD |
    | Developer | Fabrikam USA | Fabrikam USA - Robotics | 150 USD |

3. Připojte prodejní ceník **Fakturační sazby společnosti Fabrikam USA** k projektovému ceníku projektové smlouvy nebo k určitému účtu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
