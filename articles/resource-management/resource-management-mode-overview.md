---
title: Přehled režimů správy zdrojů
description: Toto téma poskytuje informace o funkci Správa zdrojů v Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118510"
---
# <a name="resource-management-modes-overview"></a>Přehled režimů správy zdrojů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


Dynamics 365 Project Operations podporuje dva režimy provádění celkového toku rezervací. Režim správy je definován jako parametr projektu a lze jej upravit, pokud se změní vaše obchodní potřeby.    

## <a name="central-mode"></a>Centrální režim
Organizacím, které centralizují přidělení zdrojů k projektům, poskytuje centrální režim způsob, jak zajistit, aby projektoví manažeři mohli definovat požadavky na zdroje na úrovni projektu. Splnění požadavků na zdroje je delegováno na správce zdrojů. Manažeři projektů mohou přijímat nebo odmítat zdroje, které navrhuje správce zdrojů.

![Centrální režim](./media/resource-management-central.png)

Chcete-li spravovat zdroje v centrálním režimu, přečtěte si:

- [Přiřazení obecných rezervovatelných zdrojů k úkolu a vygenerování požadavků na zdroj](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervace pojmenovaných zdrojů z požadavků na zdroje](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Odeslání žádosti o zdroj](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Splnění požadavku na zdroj](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Přijetí nebo zamítnutí navrženého zdroje projektu z žádosti o zdroj](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybridní režim
U organizací, které vyžadují při přidělování zdrojů flexibilitu, umožňuje hybridní režim projektovým manažerům i správcům zdrojů rezervovat prostředky.

![Hybridní režim](./media/resource-management-hybrid.png)

Kromě podporovaného procesu v centrálním režimu najdete v následujících tématech přehled správy všech ostatních podporovaných toků rezervací v hybridním režimu:

Rezervace zdroje přímo k projektu:
- [Rezervujte pro projektový tým pojmenované rezervovatelné zdroje a přiřaďte úkoly](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Rezervace zdroje z požadavku na zdroj:
- [Přiřazení obecných rezervovatelných zdrojů k úkolu a vygenerování požadavků na zdroj](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervace pojmenovaných zdrojů z požadavků na zdroje](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]