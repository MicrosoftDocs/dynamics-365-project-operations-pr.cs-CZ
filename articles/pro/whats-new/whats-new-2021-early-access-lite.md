---
title: Co je nového v druhé vlně brzkého přístupu pro rok 2021 - omezené nasazení Project Operations
description: Tento článek poskytuje informace o funkcích, které jsou k dispozici ve vydání předběžného přístupu k 2. vlně 2021 Project Operations pro omezené nasazení.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924100"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Co je nového v druhé vlně brzkého přístupu pro rok 2021 - omezené nasazení Project Operations

_Platí pro: Omezené nasazení – od obchodu po pro forma fakturaci_

Tento článek se vztahuje na následující součásti a verze aplikace Dynamics 365 Project Operations:

  - Project Operations v prostředí Dataverse verze 4.23.0.4

Vydání lze použít pouze v případě, že je prostředí [přihláseno k brzkému přístupu](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

[Řízení subdodávek](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - Tato funkce poskytuje lepší viditelnost a kontrolu nad všemi aspekty práce na projektu. Náhled řízení subdodávek obsahuje následující možnosti:

  - Projektový manažer vytvoří subdodávku s dodavatelem. Pro subdodávku se standardně používají ceníky, které jsou připojeny k záznamu dodavatele. Účet dodavatele má typ vztahu **Prodejce** nebo **Dodavatel**.
  - Projektový manažer může všechny nákupy rozdělit do řádkových položek subdodávky. Řádky subdodávky mohou být na čas, výdaje nebo produkty. Třída transakce každého řádku subdodávky určuje, k čemu daný řádek slouží.
  - Správce obchodního vztahu prodejce a správce projektu mohou iterovat subdodávku. Cenu lze upravit v nákupních cenících, které jsou přiřazeny k subdodávce.
  - Pokud je řádek subdodávky během procesu pro čas, správce zákaznického dodavatele přidruží kontakty ke každému řádku subdodávky. Toto sdružení poskytuje informace projektovému manažerovi, který pracuje na subdodávce. Když je dodavatelský kontakt spojen s řádkem subdodávky, systém automaticky vytvoří rezervovatelný zdroj z kontaktu, pokud rezervovatelný zdroj již neexistuje.
  - Fakturační metoda na každém řádku subdodávky může být pevná cena nebo čas a materiál. U řádků subdodávek s pevnou cenou můžete nastavit plán faktur na základě milníků.
