---
title: Správa subdodávek ve službě Project Operations
description: Toto téma poskytuje přehled procesu správy komplexních subdodávek v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994223"
---
# <a name="subcontract-management-in-project-operations"></a>Správa subdodávek ve službě Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Subdodávky v Microsoft Dynamics 365 Project Operations podporují následující tok obchodního procesu.

![Tok subdodavatelských procesů](../media/SubcontractingProcessFlow.png)

Zde je podrobný popis procesu subdodávky.

1. Projektový manažer vytvoří subdodávku s dodavatelem. Pro subdodávku se standardně používají ceníky, které jsou připojeny k záznamu dodavatele. Účet dodavatele má typ vztahu **Prodejce** nebo **Dodavatel**.
2. Projektový manažer může všechny nákupy rozdělit do řádkových položek na subdodávku. Řádky subdodávky mohou být na čas, výdaje nebo produkty. Třída transakce, která je vybrána na každém řádku subdodávky, určuje, k čemu daný řádek slouží.
3. Správce obchodního vztahu prodejce a správce projektu mohou iterovat subdodávku. Cenu lze upravit v nákupních cenících, které jsou přiřazeny k subdodávce.
4. V tomto okamžiku nebo později v procesu, pokud je řádek subdodávky na čas, správce účtu dodavatele přidruží kontakty ke každému řádku subdodávky. Toto sdružení poskytuje informace projektovému manažerovi, který pracuje na subdodávce. Když je kontakt spojen s řádkem subdodávky, systém automaticky vytvoří rezervovatelný zdroj z kontaktu, pokud rezervovatelný zdroj již neexistuje.
5. Způsob účtování na každém řádku subdodávky může být **Pevná cena** nebo **Čas a materiál**. U řádků subdodávek s pevnou cenou můžete nastavit plán faktur na základě milníků.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
