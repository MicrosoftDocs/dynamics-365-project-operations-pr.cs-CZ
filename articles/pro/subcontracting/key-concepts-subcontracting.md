---
title: Klíčové pojmy v subdodávkách
description: Tento článek vysvětluje některé klíčové koncepty, které se vztahují na subdodávky v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9577169f12198222e647ed07ae8a1b6c55da4323
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522740"
---
# <a name="key-concepts-in-subcontracting"></a>Klíčové pojmy v subdodávkách


_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Tento článek vysvětluje některé klíčové pojmy, které byste měli znát, než začnete používat funkci subdodávek v aplikaci Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Smluvní jednotka na subdodávce

Smluvní jednotka představuje divizi nebo praxi, která vlastní dodávku případného projektu. Smluvní jednotkou je také divize, která vstupuje do smluvního vztahu s prodejcem.

## <a name="purchase-currency"></a>Měna nákupu

V Project Operations je nákupní měnou měna, ve které je subdodávka vytvořena. Je to také měna, ve které jsou zaznamenány náklady na subdodavatele projektu. Měna nákupu se může lišit od měny projektu a měna projektu se zase může lišit od měny prodeje.

## <a name="billing-methods-on-subcontract-lines"></a>Metody účtování na subdodavatelských linkách

Pro projekty obvykle existují smluvní modely založené na pevných poplatcích a spotřebě. Project Operations podporuje tyto způsoby účtování v kontextech prodeje a nákupu. U nákupu fungují způsoby fakturace následujícím způsobem:

- **Čas a materiál** - Pokud řádek subdodávky používá způsob fakturace **Čas a materiál**, náklady na čas jsou zaznamenány na projektu, protože subdodavatelé na tomto projektu pracují a zaznamenávají čas. Tyto transakce nákladů od subdodavatelů jsou poté spárovány s řádkovými položkami na fakturách dodavatele. V tomto modelu mohou projektoví manažeři, kteří používají Project Operations, přiřadit a ověřit řádky faktury dodavatele se zaznamenaným a schváleným časem subdodavatele. Po dokončení ověřování se obrátí předchozí skutečná cena, která byla zaznamenána po schválení, a v projektu se vytvoří nové skutečné náklady, které jsou založeny na faktuře dodavatele.
- **Pevná cena** - V tomto modelu smlouvy s fixními poplatky jsou faktury dodavatele založeny na pevných milnících. Zdroje subdodavatele však mohou také vykazovat čas. Čas je poté zkontrolován a schválen projektovým manažerem. Po jeho schválení vytvoří Project Operations dočasné skutečné náklady na projekt. Poté, co dodavatel odešle fakturu za milník, může projektový manažer porovnat dříve zaznamenané skutečné náklady s milníkem. Po dokončení ověření se skutečné náklady obrátí a zaznamenají se náklady na základě milníků.

## <a name="project-price-lists-on-subcontracts"></a>Projektové ceníky v subdodávkách

Ceníky projektu jsou ceníky, které slouží k nastavení nákupních cen pro čas, výdaje a další komponenty související s projektem. Může existovat více ceníků, z nichž každý může mít svou vlastní subdodávku platnou podle data v Project Operations. Project Operations nepodporuje překrývající se data platnosti v cenících projektu pro subdodávku.

## <a name="transaction-classes-on-subcontracts"></a>Třídy transakcí u subdodávek

Aplikace Project Operations podporuje čtyři typy tříd transakcí:

- Čas
- Výdaje
- Materiál
- Poplatek

Náklady na nákup lze odhadnout a vzniknout pouze v transakčních třídách **Čas**, **Výdaje** a **Materiál**. **Poplatek** je transakční třída pouze pro příjmy a není k dispozici v obsahu nákupu.

## <a name="purchase-pricing-dimensions"></a>Nákupní cenové dimenze

Cenové dimenze vám umožňují rozhodnout, jaké atributy se použijí pro nastavení nákupní ceny a výchozí nastavení pro časové transakce. Pokud jde o nákup, Project Operations podporuje pouze nastavení pevných dimenzí pro nastavení a výchozí nastavení nákupní ceny. Pro nastavení nákupní ceny a výchozí nastavení na subdodavatelských linkách a subdodavatelských časových transakcích jsou atributy **Role** a **Rezervovatelný zdroj**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
