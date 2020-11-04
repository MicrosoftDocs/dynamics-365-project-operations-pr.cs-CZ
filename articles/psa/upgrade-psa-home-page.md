---
title: Upgrade domovské stránky
description: Toto téma ukazuje, kde naleznete důležité informace o nových a změněných funkcích aplikace Dynamics 365 Project Service Automation a o procesu upgradu na nejnovější verzi.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 29e7b519b61e8709c025e9906d04aed0156f65eb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073861"
---
# <a name="upgrade-home-page"></a>Upgrade domovské stránky

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Upgrade PSA z verze 2.x nebo 1.x na verzi 3.x

### <a name="new-instances"></a>Nové instance

Od 17. května 2019 platí, že pokud je při zřizování nové instance vybrána služba Project Service Automation, bude ve výchozím nastavení nainstalována verze 3.x.

### <a name="existing-instances"></a>Existují instance

Dříve museli zákazníci, kteří měli instanci PSA verze 2.x a potřebovali upgradovat na verzi 3.x, což je verze PSA založená na sjednoceném rozhraní klienta (UCI), kontaktovat podporu Microsoft a poskytnout podrobnosti o jejich instanci, aby podpora mohla povolit instanci pro upgrade na verzi 3.x. Od 1. března 2020 budou zákazníci, kteří mají instanci PSA verze 2.x a potřebují upgradovat na verzi 3.x, moci upgradovat své instance přímo z portálu pro správu, aniž by museli kontaktovat podporu společnosti Microsoft.  

> [!NOTE]
> PSA verze 3.x zahrnuje významné změny. Byla postavena na architektuře Sjednoceného rozhraní, aby pomohla zajistit lepší uživatelské prostředí. Nově přepracovaná aplikace poskytuje konzistentní, jednotné uživatelské rozhraní (UI) a řídí se zásadami přizpůsobivého návrhu pro optimální zobrazení libovolné velikosti obrazovky nebo zařízení. V aplikaci byly provedeny další změny. Mezi oblasti, které byly změněny, patří tvorba cen, rezervace a přiřazování zdrojů, čas, výdaje a schválení.

Před spuštěním upgradu doporučujeme dokončit následující úkoly:

- Ověřte, zda jsou v identifikované instanci nainstalovány aplikace Dynamics 365 Field Service a Project Service Automation. Pokud jsou nainstalována obě řešení, měli byste naplánovat upgrade obou před obnovením běžného používání dané instance.
- Pečlivě si prostudujte následující témata. Znalost a pochopení změn mezi verzemi vám pomůže při procesu upgradu. Tato témata obsahují informace o hlavních změnách v programu PSA, včetně důležitých informací a doporučení pro plánování upgradu na verzi 3.x.

    - [Novinky a změny v aplikaci Project Service Automation verze 3](whats-new-changed-v3.md)
    - [Důležité informace o upgradu – Project Service Automation verze 2.x nebo 1.x na verzi 3](upgrade-v3.md)

- Upgradujte sandboxovou instanci, chcete-li zhodnotit změny v implementaci před upgradem produkční instance.

Po zkontrolování dříve zmíněných témat a jakmile budete připraveni na upgrade na verzi PSA 3.x nebo na verzi založenou na UCI, odešlete požadavek oddělení podpory Microsoftu, aby byl upgrade k dispozici z centra pro správu. V požadavku zadejte podrobnosti o vaší instanci.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Starší verze programu PSA (PSA verze 2.x) v nově vytvořené instanci

Od 17. května 2019 budou mít všechny nové instance UCI jako výchozího klienta. Pro zajištění souladu s touto změnou bude ve výchozím nastavení zřízena verze PSA 3.x a Field Service 8.x, protože tyto verze jsou navrženy tak, aby fungovaly s klientem UCI.

Od 1. března 2020 již zákazníci Dynamics PSA nebudou moci vytvářet nová prostředí se staršími verzemi PSA, například PSA verze 2.x nebo nižší. Jakékoli nové prostředí bude pouze verze 3.x aplikace PSA.

> [!NOTE]
> Chcete-li dosáhnout nejlepších výsledků, pokud používáte starší verze aplikací Field Service a PSA, přejděte na stránku **Nastavení systému** a pro pole **Používat jen nové Sjednocené rozhraní (doporučeno)** vyberte možnost **Ne** , protože tyto verze nejsou navrženy tak, aby byly v UCI správně načteny. Po vypnutí UCI můžete tyto verze aplikací Field Service a PSA otevřít a spustit pomocí starého webového klienta. 
