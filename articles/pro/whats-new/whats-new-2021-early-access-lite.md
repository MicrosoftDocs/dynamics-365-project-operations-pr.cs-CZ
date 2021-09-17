---
title: Co je nového v druhé vlně brzkého přístupu pro rok 2021 - omezené nasazení Project Operations
description: Toto téma obsahuje informace o funkcích dostupných ve vydání brzkého přístupu druhé vlny v roce 2021 omezeného nasazení Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323903"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Co je nového v druhé vlně brzkého přístupu pro rok 2021 - omezené nasazení Project Operations

_Platí pro: Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

  - Project Operations v prostředí Dataverse verze 4.23.0.4

Vydání lze použít pouze v případě, že je prostředí [přihláseno k brzkému přístupu](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

[Řízení subdodávek](../subcontracting/subcontracting_EA_scope.md) - Tato funkce poskytuje lepší viditelnost a kontrolu nad všemi aspekty práce na projektu. Náhled řízení subdodávek obsahuje následující možnosti:

  - Projektový manažer vytvoří subdodávku s dodavatelem. Pro subdodávku se standardně používají ceníky, které jsou připojeny k záznamu dodavatele. Účet dodavatele má typ vztahu **Prodejce** nebo **Dodavatel**.
  - Projektový manažer může všechny nákupy rozdělit do řádkových položek subdodávky. Řádky subdodávky mohou být na čas, výdaje nebo produkty. Třída transakce každého řádku subdodávky určuje, k čemu daný řádek slouží.
  - Správce obchodního vztahu prodejce a správce projektu mohou iterovat subdodávku. Cenu lze upravit v nákupních cenících, které jsou přiřazeny k subdodávce.
  - Pokud je řádek subdodávky během procesu pro čas, správce zákaznického dodavatele přidruží kontakty ke každému řádku subdodávky. Toto sdružení poskytuje informace projektovému manažerovi, který pracuje na subdodávce. Když je dodavatelský kontakt spojen s řádkem subdodávky, systém automaticky vytvoří rezervovatelný zdroj z kontaktu, pokud rezervovatelný zdroj již neexistuje.
  - Fakturační metoda na každém řádku subdodávky může být pevná cena nebo čas a materiál. U řádků subdodávek s pevnou cenou můžete nastavit plán faktur na základě milníků.
