---
title: Nastavení fakturačních sazeb za práci – omezené
description: Tento článek poskytuje informace o nastavení fakturačních sazeb za práci v Project Operations.
author: rumant
ms.date: 10/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 443132797f20c961b42ed20340e74f420965526f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917430"
---
# <a name="set-up-labor-bill-rates---lite"></a>Nastavení fakturačních sazeb za práci – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Každý ceník obsahuje sadu cen rolí nebo pracovních sazeb, které jsou účinné pro kontext a datum účinnosti uvedené v záhlaví ceníku. Sazby faktur za čas v Dynamics 365 Project Operations lze nastavit pouze v jedné měně, což je měna v záhlaví ceníku.

1. Chcete-li nastavit fakturační sazby za práci za prodejní ceník, vytvořte ceník na základě záhlaví ceníku. 
2. Na kartě **Ceny rolí** vyberte v podmřížce položku **+ Nová cena role**. 
3. V podokně **Vytvořit** zadejte kombinaci role a organizační jednotky, pro které potřebujete nastavit fakturační sazbu.

  V následující tabulce je uveden seznam polí na kartě **Všeobecné** a v podokně **Vytvořit** řádku ceny role, na které byste měli pamatovat při vytváření cen rolí v prodejním ceníku:

  | Pole | Místo | Popis | Dopad na následné složky |
  | --- | --- | --- | --- |
  | Role | Karta **Všeobecné** a podokno **Vytvořit** | Vyberte roli, pro kterou nastavujete fakturační sazbu. | Role u příchozího odhadu nebo skutečné hodnoty bude porovnána s tímto řádkem za účelem určení výchozí fakturační sazby role. |
  | Jednotka zdroje | Karta **Všeobecné** a podokno **Vytvořit** | Vyberte organizační jednotku nebo divizi společnosti, ze které role pochází. Například vývojář z divize Robotics společnosti Fabrikam Indie nebo vývojář z divize Software společnosti Fabrikam USA. | Jednotka zdroje u příchozího odhadu nebo skutečné hodnoty bude porovnána s tímto řádkem za účelem určení výchozí fakturační sazby role. |
  | Cena | Karta **Všeobecné** a podokno **Vytvořit** | Nastavte fakturační sazbu pro kombinaci role, společnosti zajišťující zdroje a jednotky zdrojů. Například vývojář ze společnosti Fabrikam Indie má fakturační sazbu 100 USD, vývojář ze společnosti Fabrikam USA má fakturační sazbu 150 USD. | Tato cena je výchozí fakturační sazba pro jednotkovou cenu řádku příchozího odhadu nebo skutečné hodnoty pro třídu transakcí Čas. |
  | Měna | Karta **Všeobecné** a podokno **Vytvořit**| Ve výchozím nastavení hodnota měny pochází z měny v záhlaví prodejního ceníku. V prodejním ceníku nelze měnu přepsat. | Tato měna je výchozí měnou pro jednotkovou cenu řádku příchozího skutečného prodeje pro třídu transakcí Čas. |
  | Rozpis jednotky | Karta **Všeobecné** a podokno **Vytvořit** | Tento rozpis jednotky má jako výchozí nastaven Čas a toto nelze u entity ceny role změnit, protože se používá k vyjádření sazeb podle časových jednotek. | Neexistuje žádný následný dopad na toto pole. |
  | Jednotka | Karta **Všeobecné** a podokno **Vytvořit** | Hodnota jednotky pochází z pole **Časová jednotka** v záhlaví prodejního ceníku. Ale tato hodnota nemůže být přepsána. Například vývojář ze společnosti Fabrikam Indie má fakturační sazbu 1000 USD za **Den v Indii**. Vývojář ze společnosti Fabrikam USA má fakturační sazbu 1500 USD za **Den v USA**. | Když je výchozí cena za jednotku založena na řádku příchozího odhadu nebo skutečné hodnoty, systém používá k výpočtu ceny za jednotku systém jednotek a převod v základních jednotkách. Například odhad je 10 **dnů v Indii** práce pro vývojáře z Indie, a jednotka Den v Indii je definována jako 10 hodin. Při ocenění tohoto řádku odhadu aplikace vypočítá jednotkovou cenu v odhadu jako 1000 USD / 10 hodin = 100 USD za hodinu. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Přenos ocenění nebo nastavení fakturačních sazeb pro zdroje z jiných organizačních jednotek nebo divizí 

Projektové společnosti využívají k práci na projektech zaměstnance z různých divizí společnosti. Projekty lze provádět z jedné divize, zatímco zaměstnanci nebo konzultanti pocházejí ze stejné nebo odlišné divize společnosti. Projekt by také mohl být tvořen kombinací lidí z různých divizí. V aplikaci Project Operations se společnost, která vlastní dodávku projektu, nazývá **Smluvní jednotka**. Všechny ostatní divize, které poskytují zdroje, se nazývají **Jednotky zdrojů**. Kvůli rozdílům v nákladech na pracovní sílu v různých zeměpisných oblastech a na trzích práce po celém světě jsou fakturační sazby za práci také nastaveny odlišně pro různé zeměpisné oblasti.

Například vývojáři ze společnosti Fabrikam Indie pracující na americkém projektu je účtována sazba 100 USD za hodinu. Vývojáři ze společnosti Fabrikam USA pracujícímu na americkém projektu je účtována sazba 150 USD za hodinu.

### <a name="example-set-up-a-bill-rate"></a>Příklad: Nastavení fakturační sazby

1. Vytvořte prodejní ceník s názvem *Fakturační sazby společnosti Fabrikam USA* a nastavte datum jeho účinnosti.
2. V prodejním ceníku zadejte následující sazby:

    | Role | Organizační jednotka | Fakturační sazba |
    | --- | --- | --- |
    | Developer | Fabrikam Indie | 100 dolarů |
    | Developer | Fabrikam Filipíny | 90 USD |
    | Developer | Fabrikam USA | 150 USD |

3. Připojte prodejní ceník **Fakturační sazby společnosti Fabrikam USA** k projektovému ceníku projektové smlouvy nebo k určitému účtu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]