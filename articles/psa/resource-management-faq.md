---
title: Nejčastější dotazy ke správě zdrojů
description: Toto téma poskytuje odpovědi na časté otázky týkající se správy zdrojů.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f80e65e7ff423c362fd1a86676a84ab67afabc88115c99b582c5eefa6c725a46
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002368"
---
# <a name="resource-management-faq"></a>Nejčastější dotazy ke správě zdrojů

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Jaký je rozdíl mezi členem týmu a požadavkem na zdroj?

Člena projektového týmu lze přiřadit k úkolům, rezervovat nebo přerezervovat a nastavit jako schvalovatele. Požadavek na zdroj může existovat bez člena projektového týmu jako koncept poznámky k poptávce. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Jaký je rozdíl mezi navrženými a předběžně rezervovanými hodinami?

Navržené hodiny a předběžně rezervované hodiny se liší viditelností. Navržené hodiny jsou viditelné pouze správcům zdrojů a projektovému manažerovi, který poptávku inicioval pomocí žádosti o zdroj. Předběžně rezervované hodiny jsou viditelné všem uživatelům, kteří mají přístup k Plánovací vývěsce.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Jak lze zobrazit předběžně rezervované hodiny pro zdroje v týmu?

Předběžné rezervace lze provést při rezervaci požadavku na zdroj. Zdroje, které jsou v projektovém týmu předběžně rezervované, se zobrazí jako členové týmu, kteří mají předběžně rezervované hodiny. Zobrazí se také v Plánovací vývěsce.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Jak změnit požadované hodiny a počáteční a koncová data pro zdroj (obecný nebo pojmenovaný), který jsem rezervoval?

Chcete-li provést libovolné požadované změny vyberte po rezervaci zdrojů vyberte **Spravovat rezervace**.

## <a name="what-resources-types-does-project-service-automation-support"></a>Jaké typy zdrojů podporuje Project Service Automation?

**Uživatel** a **Kontakt** jsou jediné typy zdrojů podporované v Dynamics 365 Project Service Automation. I když můžete vytvářet další typy zdrojů (například **Vybavení** a **Skupina**), není pro ně podporován žádný případ komplexního použití.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Jaký je rozdíl mezi přiřazením a rezervací?

Přiřazení jsou přiřazení zdrojů k úkolům projektu v plánu projektu. Zdroje mohou být buď skutečné, nebo obecné. Rezervace jsou závazné nebo předběžné přidělení zdrojů k projektu. Závazné rezervace spotřebovávají kapacitu zdroje. V ideálním případě by se pro reálné zdroje měly dohodnout rezervace a přiřazení, protože se neliší. PSA však tuto dohodu nevynucuje. Zobrazení Vyrovnání ukazuje projektovému manažerovi místa, kde se neshodují rezervace a přiřazení zdroje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]