---
title: Rezervace a přiřazení
description: Toto téma poskytuje informace o rozdílech mezi rezervacemi zdrojů a přiřazeními zdrojů.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841164"
---
# <a name="bookings-vs-assignments"></a>Rezervace a přiřazení

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Rezervace jsou závazné nebo předběžné přidělení zdrojů k projektu. Závazné rezervace spotřebovávají kapacitu zdroje. Rezervace představují organizační koncepty pro týmy, aby mohly pochopit, jak budou zdroje zapojeny do různých projektů. Dynamics 365 Project Operations považuje rezervace za koncept na úrovni projektu. 

Na rozdíl od rezervací představuje přiřazení závazek zdrojů k úkolům projektu v plánu projektu. Zdroje mohou být pojmenované nebo obecné.  Když je požadavek na zdroj odvozen z přiřazení úkolů projektu, používá Project Operations obrysy přiřazení prostředků k vytvoření obrysů detailů požadavku na prostředek. Odkaz na přiřazení zdrojů se však neudržuje. Aktualizace rezervací odvozených z požadavku na zdroje neaktualizují žádné přiřazení zdrojů.

Součet rezervací pro zdroj se obvykle bude rovnat součtu přiřazení zdroje napříč jedním nebo více úkoly. Project Operations však tuto dohodu nevynucuje. Zobrazení **Vyrovnání** ukazuje projektovému manažerovi místa, kde se neshodují rezervace a přiřazení zdroje.




[!INCLUDE[footer-include](../includes/footer-banner.md)]