---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 24, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 24, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073732"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation, vydání aktualizace 24, V3

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 24 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V 3.10.42.43 a je obvykle k dispozici prostřednictvím automatické aktualizace v říjnu 2020.

## <a name="update-release-24"></a>Aktualizace verze 24

### <a name="bug-fixes"></a>Opravy chyb

**Sales**

Byly vyřešeny následující problémy:

- Problém při nastavování výchozího ceníku produktů.
- Výkon získávání nabídek je pomalý kvůli kopii záznamů ceníku a ceny role.
- **Projektová smlouva / Centrum prodeje** > **Množství položky produktové řady / řádku objednávky** je automaticky zaokrouhleno na nejbližší celé číslo.
- Při čtení ceníků zvýšit na systémová oprávnění.
- Zkopírujte pole adresy zákazníka **address1_freighttermscode** a **address1_shippingmethodcode** do nabídky / objednávky. 


**Čas a výdaje**

Byly vyřešeny následující problémy:

- **Mřížka časových záznamů** nepodporuje chování času **Pouze datum**.
- **Časový záznam** se automaticky neobnovuje. Je vyžadována ruční aktualizace.
- Nelze importovat časové záznamy z přiřazení, když je v přiřazení prostředku přestávka (0 hodin).
- Při vytváření časového záznamu nastavte začátek na stejný jako **msdyn_date**.
- Znovu povolte hromadné úpravy pro časový záznam.

**Správa zdrojů**

Byly vyřešeny následující problémy:

- Pokus o aktualizaci stavu mezidenní rezervace bez požadavku vyvolá výjimku null-ref.
- Chyba při načítání souboru **Zobrazení vyrovnání**.


**Správa projektů**

Byly vyřešeny následující problémy:

- V **Časovém plánu projektu** , když přecházíte z **Manual** na **Auto** , automatické ukládání se nedokončí.
- Náklady by se neměly počítat směrem k odchylce v **Mřížce pro sledování projektů**.
- Nekonzistentní chování pro sloupce **Značka odhadů** během načítání versus změna typu **Časová fáze**.
- Skutečné náklady na projekt nemusí odrážet součty ze **Skutečných hodnot**.
- **Předpokládané datum dokončení** na kartě **Souhrn** neodpovídá **Plánu strukturovaného rozpisu prací**.
- **Aktualizave skutečných hodin** při zmenšení odsazení nefunguje správně.
- Projektový manažer mimo kořenovou **BU** nemůže vytvořit projekt.
- Změny úkolu nebo kategorie v **Odhadech výdajů** nejsou zachovány.
- **Kopie smlouvy** zkopíruje plány faktur a stav běhu.
- Tlačítko **Obnovit skutečné údaje** nesprávně vypočítá souhrnné úkoly.
- Doplněk Microsoft Project: Oprava chyby s nulovou referencí, pokud má kterýkoli člen týmu prázdnou zdrojovou jednotku.

