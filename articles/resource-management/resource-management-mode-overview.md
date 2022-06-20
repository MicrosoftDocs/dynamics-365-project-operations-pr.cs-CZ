---
title: Přehled režimů správy zdrojů
description: Tento článek poskytuje informace o funkčnosti správy zdrojů v Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928424"
---
# <a name="resource-management-modes-overview"></a>Přehled režimů správy zdrojů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


Dynamics 365 Project Operations podporuje dva režimy, abyste mohli provést celkový tok rezervací. Režim správy je definován jako parametr projektu a lze jej upravit, pokud se změní vaše obchodní potřeby.    

## <a name="central-mode"></a>Centrální režim
Organizacím, které centralizují přidělení zdrojů k projektům, poskytuje centrální režim způsob, jak zajistit, aby projektoví manažeři mohli definovat požadavky na zdroje na úrovni projektu. Splnění požadavků na zdroje je delegováno na správce zdrojů. Manažeři projektů mohou přijímat nebo odmítat zdroje, které navrhuje správce zdrojů.

![Centrální režim.](./media/resource-management-central.png)

Chcete-li spravovat zdroje v centrálním režimu, přečtěte si:

- [Přiřazení obecných rezervovatelných zdrojů k úkolu a vygenerování požadavků na zdroj](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervace pojmenovaných zdrojů z požadavků na zdroje](/dynamics365/project-service/book-named-resource)
- [Odeslání žádosti o zdroj](/dynamics365/project-service/submit-resource-request)
- [Splnění požadavku na zdroj](/dynamics365/project-service/resource-management-fulfill-requests)
- [Přijetí nebo zamítnutí navrženého zdroje projektu z žádosti o zdroj](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybridní režim
U organizací, které vyžadují při přidělování zdrojů flexibilitu, umožňuje hybridní režim projektovým manažerům i správcům zdrojů rezervovat prostředky.

![Hybridní režim.](./media/resource-management-hybrid.png)

Kromě podporovaného procesu centrálního režimu si přečtěte následující články, které vám pomohou spravovat všechny ostatní podporované toky rezervace v hybridním režimu:

Rezervace zdroje přímo k projektu:
- [Rezervujte pro projektový tým pojmenované rezervovatelné zdroje a přiřaďte úkoly](/dynamics365/project-service/assign-named-bookable-resource)

Rezervace zdroje z požadavku na zdroj:
- [Přiřazení obecných rezervovatelných zdrojů k úkolu a vygenerování požadavků na zdroj](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervace pojmenovaných zdrojů z požadavků na zdroje](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]