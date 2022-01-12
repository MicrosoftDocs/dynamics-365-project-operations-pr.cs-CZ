---
title: Co je nového, prosinec 2021 – omezené nasazení Project Operations
description: Toto téma poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z prosince 2021 pro omezené nasazení.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942969"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Co je nového, prosinec 2021 – omezené nasazení Project Operations

_Platí pro: Omezené nasazení – od obchodu po pro forma fakturaci_

Toto téma se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

### <a name="subcontract-management"></a>Řízení subdodávek 

- [Přidělování členů projektového týmu k subdodávkám](../subcontracting/subcontracting-project-team-members.md): Projektový manažer může vytvářet pojmenované nebo obecné členy týmu se subdodávkami a řádky subdodávek, aby ovlivnil personální obsazení a odhady.
- [Možnosti subdodávek pro členy projektového týmu](../subcontracting/subcon-options.md): Při výběru pracovníků pro jmenované nebo obecné členy projektového týmu může projektový manažer zkontrolovat stávající subdodávky nebo vytvořit nové subdodávky pro jednoho nebo více členů projektového týmu. 
- [Odhad nákladů na přidělení zdrojů subdodávky](../subcontracting/costing-subcon-ra.md): Odhad nákladů na projekt bude brát do úvahy přidělení zdrojů k subdodávkám a bude je účtovat podle nákupních ceníků přidružených k subdodávkám. 
- [Konfigurace plánovací vývěsky pro zobrazení smluvních pracovníků a kapacity subdodávky](../subcontracting/configure-sb-subcon.md): Plánovací vývěsku v Project Operations lze nyní konfigurovat tak, aby vyhledávala a navrhovala typ smluvních pracovníků rezervovatelných zdrojů a kapacity pro subdodávky spolu se zaměstnanci. Tuto konfiguraci lze použít při hledání zdrojů v kontextu personálního zajištění konkrétního projektového požadavku nebo při hledání mimo kontext projektového požadavku.
- [Personální zajištění projektu smluvními pracovníky a kapacitou pro subdodávky](../subcontracting/staffing-cw.md): Smluvní pracovníci mohou být nyní rezervováni na projektech využívajících prostředí plánovací vývěsky.
- [Evidence času, výdajů a spotřeby materiálu u projektů pro součásti subdodávky](../subcontracting/recording-subcon-actuals.md): Smluvní pracovníci mohou zaznamenávat čas a výdaje a členové projektového týmu mohou také zaznamenávat spotřebu materiálů zakoupených pomocí subdodávky na projekt. To povede k zaznamenávání přesných nákladů na projekty, které využívají nakoupenou kapacitu nebo materiály.
- [Přechody stavů u subdodávky](../subcontracting/subcon-states.md): Subdodávky mohou být potvrzeny za účelem dokončení jednání s prodejcem, uzavřeny, aby bylo oznámeno dokončení dodávky, nebo zrušeny, aby bylo oznámeno ukončení smlouvy s prodejcem před dokončením dodávky.

### <a name="task-planning"></a>Plánování úkolů
- Vylepšené řešení potíží pro správce systému. Když uživatel nemůže otevřít projekt, správce může zkontrolovat chyby, které se netýkají licence, generované z aplikace Project for the web, v [protokolech plánování projektu](../../project-management/schedule-api-logs.md).
- [Použití kontrolních seznamů úkolů v aplikaci Microsoft Project for the web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). V aplikaci Microsoft Project for the web můžete k úkolu přidat kontrolní seznam, abyste měli přehled o konkrétních položkách.

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

| **Oblast funkcí** | **Referenční číslo** | **Aktualizace pro zvýšení kvality** |
| --- | --- | --- |
| Plánování a sledování | 2392596 | Rozhraní API pro plánování nyní umožňují aktualizaci polí **Zbývající úsilí**, **Dokončené úsilí** a **Dokončeno %**. |
| Plánování a sledování | 2478497 | Pole rozhraní API plánování **Číslo aktivity** a **ID úkolu** mohou být při zadávání prázdná, protože systém je vyplní pomocí automatického číslování.|
| Čas a výdaje | 2468135 | Počet pokusů o schválení je snížen z pěti na tři. |
| Čas a výdaje | 2468188 | Opraven problém s textem protokolu překračujícím maximální délku v atributu **notetext** entity **annotation**. |
