---
title: Novinky a změny v aplikaci Project Service Automation, aktualizace verze 30, V3
description: Tohle téma uvádí seznam funkcí a oprav, které jsou k dispozici v Project Service Automation, aktualizace verze 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852839"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Novinky a změny v aplikaci Project Service Automation, aktualizace verze 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potěšením oznamujeme nejnovější aktualizaci aplikace Project Service Automation pro Dynamics 365. Tato verze obsahuje některá důležitá vylepšení kvality, výkonu a použitelnosti. Tato verze je kompatibilní s Dynamics 365 9.x. Chcete-li aktualizovat tuto verzi, navštivte Centrum pro správu Dynamics 365 online, stránku řešení a nainstalujte danou aktualizaci. Další informace viz [Instalace, aktualizace nebo odebrání preferovaného řešení](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Tohle téma uvádí seznam funkcí a oprav, které jsou nové nebo změněné v aktualizaci verze 30 pro aplikaci Project Service Automation V3. Tato verze má číslo sestavení V3.10.51.61 a je obvykle k dispozici prostřednictvím automatické aktualizace v dubnu 2021.

## <a name="update-release-30"></a>Aktualizace verze 30

### <a name="bug-fixes"></a>Opravy chyb

**Čas a výdaje**

Byly vyřešeny následující problémy:

- Při vytváření a ukládání časového záznamu dojde k chybě na stránce **Rychlé vytvoření**, pokud je odstraněno pole **Role**.
- Filtr Časový vstup použije nesprávný operátor filtru.
- Zkopírované časové rozvrhy se po výběru možnosti **Kopírovat týden** na ovládacím prvku zadávání času automaticky nezobrazí.

**Správa zdrojů**

Byly vyřešeny následující problémy:

- Při prodloužení rezervace je stav rezervace přiřazený závazné rezervaci nesprávný. Prodloužení rezervace respektuje stav rezervace definovaný jako **Potvrzený** v metadatech nastavení rezervace.
- Pokud není zadán platný stav rezervace, chybová zpráva není správně lokalizována.

**Správa projektů**

Byly vyřešeny následující problémy:

- Projekty nelze vytvořit v jedné měně, když zahrnují související úkoly v jiné měně.

**Prodej**

Byly vyřešeny následující problémy:

- Při kopírování ceníku se ceny neaktualizují.
- Uzavření nabídky jako vyhrané selže, když má detail nákladů hodnotu původu.
- U entity **Projektový úkol** byly **Odhadované náklady** přejmenovány **Plánované náklady (základ)**.
- Při vytváření nebo odstraňování faktur se generuje výjimka null reference.