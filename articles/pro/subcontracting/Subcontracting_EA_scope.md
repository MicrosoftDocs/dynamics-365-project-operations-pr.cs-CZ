---
title: Subdodávky vydané verze brzkého přístupu v říjnu 2021
description: Toto téma poskytuje přehled možností subdodavatelů v Project Operations, které jsou součástí vydání brzkého přístupu v říjnu 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383687"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Subdodávky vydané verze brzkého přístupu v říjnu 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma poskytuje přehled možností subdodavatelů v Dynamics 365 Project Operations, které jsou součástí vydání brzkého přístupu v říjnu 2021. Tato sada funkcí není připravena pro produkční ani živá prostředí, takže tyto funkce zůstanou ve vydání brzkého přístupu, dokud nebude vydána celá sada funkcí. Důrazně doporučujeme, abyste nepoužívali sadu funkcí subdodavatelů pro scénáře živé produkce, dokud není odstraněn transparent náhledu. 

Následující seznam poskytuje přehled toho, co je aktuálně k dispozici ve vydání brzkého přístupu v říjnu 2021:

1. Projektový manažer vytvoří subdodávku s dodavatelem. Pro subdodávku se standardně používají ceníky, které jsou připojeny k záznamu dodavatele. Účet dodavatele má typ vztahu **Prodejce** nebo **Dodavatel**.

2. Projektový manažer může všechny nákupy rozdělit do řádkových položek na subdodávku. Řádky subdodávky mohou být na čas, výdaje nebo produkty. Třída transakce každého řádku subdodávky určuje, k čemu daný řádek slouží.

3. Správce obchodního vztahu prodejce a správce projektu mohou iterovat subdodávku. Cenu lze upravit v nákupních cenících, které jsou přiřazeny k subdodávce.

4. Pokud je v tomto okamžiku nebo později v procesu řádek subdodávky na čas, správce účtu dodavatele přidruží kontakty dodavatele ke každému řádku subdodávky. Toto sdružení poskytuje informace projektovému manažerovi, který pracuje na subdodávce. Když je dodavatelský kontakt spojen s řádkem subdodávky, systém automaticky vytvoří rezervovatelný zdroj z kontaktu, pokud rezervovatelný zdroj již neexistuje.

5. Způsob účtování na každém řádku subdodávky může být **Pevná cena** nebo **Čas a materiál**. U řádků subdodávek s pevnou cenou můžete nastavit plán faktur na základě milníků.

Zbývající kroky v toku obchodního procesu pro subdodávky, které jsou popsány v Přehledu, aktuálně nejsou k dispozici. Až budou přidány nové funkce, bude toto téma aktualizováno. 

Následující obrázek představuje vydání subdodavatelského brzkého přístupu v kontrastu s komplexním obchodním procesem typu.

![Tok subdodavatelských procesů](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Množstevní řádky subdodávky a pracovní řádky vydání brzkého přístupu
Ve vydání brzkého přístupu v říjnu 2021 budou podporovány pouze množstevní řádky subdodávky. To znamená, že řádek subdodávky lze použít pro nákupní čas, výdaje nebo materiály dodavatele, avšak nikoliv celé práce. To také znamená, že nakupované množství (jednotky času, výdaje nebo množství materiálu) na řádku subdodávky lze použít na jakýkoli projekt v systému.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
