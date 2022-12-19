---
title: Zabezpečení a schválení
description: Tento článek poskytuje informace o nastavení zabezpečení pro práci se schváleními v Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841915"
---
# <a name="security-and-approvals"></a>Zabezpečení a schválení

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Microsoft Dynamics 365 Project Operations používá dvě role zabezpečení, které umožňují schvalování položek času, výdajů a materiálu:

- Schvalovatel projektu
- Schvalovatel projektu – správce

## <a name="project-approver"></a>Schvalovatel projektu

Musíte mít roli zabezpečení **Schvalovatel projektu**, abyste schválili položky času projektu, výdajů a materiálu. Musíte mít také přístup k příslušným souvisejícím entitám, jako je například **Projekt**. Tento přístup může přidělit někdo, kdo má roli **Projektový manažer**. Navíc musíte být členem týmu projektu a označeni jako schvalovatel.

Chcete-li schvalovat neprojektové položky, musíte být manažerem zadavatele.

## <a name="project-approver-admin"></a>Schvalovatel projektu – správce

> [!NOTE]
> Funkce [Schvalovací sady](approval-sets.md) musí být povolena před použitím funkce Schvalovatel projektu – správce.

Role zabezpečení **Schvalovatel projektu – správce** umožňuje uživatelům obejít zásady a umožňuje schvalování položek ve všech projektech. Přiřazení této role vynechá logiku ověřování, která vyžaduje členství v týmu a označení jako schvalovatel. Musíte mít přístup k příslušným souvisejícím tabulkám, například **Projekt**, prostřednictvím rolí zabezpečení, které vám byly přiděleny.

Uživatelský kontext SYSTEM vynechá ověřování stejným způsobem jako role zabezpečení Schvalovatel projektu – správce.
