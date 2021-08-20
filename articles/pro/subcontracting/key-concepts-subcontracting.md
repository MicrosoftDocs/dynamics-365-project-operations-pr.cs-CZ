---
title: Klíčové pojmy v subdodávkách
description: Tento téma vysvětluje některé klíčové koncepty, které platí pro subdodávky v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01d2e57b99015c346be15e3504440c14cb9a54e24215c0b1c052c5112f4b940a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994268"
---
# <a name="key-concepts-in-subcontracting"></a>Klíčové pojmy v subdodávkách

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Téma vysvětluje některé klíčové koncepty, kterých byste si měli být vědomi, než začnete používat funkce subdodávek v Microsoft Dynamics 365 Project Operations.

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
