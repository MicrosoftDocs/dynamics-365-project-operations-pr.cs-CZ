---
title: Správa prodejců a nákupních ceníků v Project Operations
description: Tento téma poskytuje informace, které vám pomohou vytvářet a udržovat údaje o prodejcích a nákupní ceníky pro subdodávky.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9c76d5ca45e03167f0ccfd2c1c7013f91fef0f86
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576722"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Správa prodejců a nákupních ceníků v Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

## <a name="vendors-in-project-operations"></a>Prodejci v Project Operations

V Microsoft Dynamics 365 Project Operations mají účty dodavatele typ vztahu **Prodejce** nebo **Dodavatel**. Můžete vybrat pouze záznam účtu, který má jeden z těchto typů vztahů, jako dodavatele subdodávky.

K záznamu dodavatele můžete přiřadit jeden nebo více nákupních ceníků. Každý nákupní ceník, který je přidružen k záznamu dodavatele, by však měl mít odlišné účinnost platnosti. Project Operations nepodporuje překrývající se data platnosti nákupních ceníků.

Ve výchozím nastavení se pro libovolnou subdodávku, která je pro dodavatele vytvořena, používají následující pole a koncepty v záznamu dodavatele:

- Platební podmínky
- Fakturační adresa kontaktu
- Primární kontakt

    > [!NOTE]
    > Ve výchozím nastavení se jako správce účtu dodavatele subdodávky použije primární kontakt dodavatele.

- Měna
- Aktuální nákupní ceníky

## <a name="purchase-price-lists-in-project-operations"></a>Nákupní ceníky v Project Operations

Ceník, kde je pole **Kontext** nastaveno na **Nákup**, je považován za nákupní ceník. Nákupní ceníky lze definovat tak, aby představovaly katalog nákupních sazeb za čas, výdaje a materiál. Nákupní ceníky se podobají ceníkům nákladů a prodejů v Project Operations. Následující koncepty platí pro nákupní ceníky stejným způsobem jako pro ceníky nákladů a prodejů:

- **Datum účinnosti** - Nákupní ceníky mají datum účinnosti. Datum účinnosti je reprezentováno poli počátečního data a koncového data v každém ceníku. Doba mezi počátečním datem a datem ukončení je datem účinného období.
- **Měna** - Měna v záhlaví ceníku se používá jako měna, v níž jsou nákupní ceny vyjádřeny pro práci, kategorie nákladů a produkty v katalogu.
- **Výchozí časová jednotka** - Výchozí časová jednotka vyjadřuje ceny práce za nákupy. Pole časové jednotky v ceníku slouží pouze k zadání výchozí hodnoty. Tuto hodnotu lze změnit v jednotlivých řádcích cen rolí.

Ceníky nákupů lze připojit k záznamům dodavatelů jako přidružení, která jsou známá jako ceníky projektů. Tyto ceníky slouží k zadávání výchozích cen na řádcích subdodávek. Ve výchozím nastavení, když je k záznamu dodavatele připojeno více nákupních ceníků, se pro subdodávky, které jsou vytvořeny pro dodavatele, použije nejaktuálnější ceník. Pouze ceníky, kde je pole **Kontext** nastaveno na **Nákup**, lze připojit k záznamům dodavatelů.

### <a name="subcontract-specific-purchase-price-lists"></a>Nákupní ceníky specifické pro subdodávky

Nákupní ceníky nákupů lze také připojit k subdodávkám jako přidružení, která jsou známá jako ceníky projektů. Tyto ceníky slouží k zadávání výchozích cen na řádcích subdodávek. Ve výchozím nastavení, když je k subdodávce připojeno více nákupních ceníků, musí mít každý z nich odlišné datum účinnosti. Project Operations nepodporuje nákupní ceníky, které mají překrývající se data účinnosti. Pouze ceníky, kde je pole **Kontext** nastaveno na **Nákup**, lze připojit k subdodávkám.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
