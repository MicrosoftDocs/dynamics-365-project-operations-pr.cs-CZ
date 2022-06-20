---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 22, V3
description: Tento článek uvádí funkce a opravy, které jsou k dispozici v Project Service Automation, vydání Update 22, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 733ee6e0d3583f21d0f58f9651920be3e3fd8cb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930632"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation, vydání aktualizace 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](/power-platform/admin/install-remove-preferred-solution).

Tento článek uvádí funkce a opravy, které jsou nové nebo se změnily v Project Service Automation V3, vydání Update 22. Tato verze má číslo sestaveníV 3.10.33.48 a je obvykle k dispozici prostřednictvím automatické aktualizace v červnu 2020.

## <a name="update-release-22"></a>Aktualizace verze 22

### <a name="bug-fixes"></a>Opravy chyb



**Čas a výdaje**

Byly vyřešeny následující problémy:

- **Časové záznamy** se po importu automaticky nepřidávají do plánu zadání času.
- Výběr data mřížky **Zadání času** nerozpozná místní nastavení uživatele.

**Správa zdrojů**

Byly vyřešeny následující problémy:

- V ručním režimu nejsou změny kontur **Přiřazení zdrojů** při generování **Požadavků na zdroje** rozpoznány.
- **Požadavky na zdroje** nepodporují vlastní stavy požadavků.

**Správa projektů**

Byly vyřešeny následující problémy:

- Dvojí kliknutí na EstimateGridControl nebude správně analyzovat čísla v holandském formátu.
- Přiřazené hodiny se neaktualizují správně, když se přiřazení změní pomocí doplňku počítačového klienta Microsoft Project.
- Mřížky sledování projektů a odhadů zobrazují nesprávný kód měny prodeje, pokud je měna smlouvy jiná než měna zákazníka a organizace je nakonfigurována tak, aby místo symbolů měny zobrazovala kódy měny.
- Datum ukončení členství týmu přidá jeden den, pokud je plán pracovní doby 24 hodin denně.
- V plánu projektu nespustí přidání kategorie transakce k úkolu automatické uložení.
- Při přidávání člena týmu do šablony projektu se zobrazí následující chyba: "Požadavky na zdroje nelze přidružit k šablonám projektu". 
- Skript pravidla pásu karet "msdyn.Approval.CanApproveOrReject" zobrazuje chybu časového limitu.

**Sales**

Byly vyřešeny následující problémy:

- Chybová zpráva o ověření se nezobrazí, když je ve vyhledávání ceníku ve formuláři / entitě Ceník projektu nové nabídky vybraný Ceník nákladové ceny.
- Uzavření nabídky tak, jak byla vyhrána, se nevztahuje na vytvořenou smlouvu, pokud je BPF připojená k nabídce v konečné fázi.
- Stornování položky **Nevyfakturovaný prodej** je spojeno s původními náklady při vyvolání časového záznamu.
- Po výběru tlačítka **Potvrdit** se stav faktury nezmění na **Potvrzeno**, pokud není faktura obnovena.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
