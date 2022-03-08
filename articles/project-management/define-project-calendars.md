---
title: Definování kalendářů projektů
description: Tento téma poskytuje informace o tom, jak použít šablonu kalendáře na projekt ke sledování harmonogramu projektu.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9c2ea49e008d6cde40f152320face073c7e5f548
ms.sourcegitcommit: bbe484e58a77efe77d28b34709fb6661d5da00f9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487632"
---
# <a name="define-project-calendars"></a>Definování kalendářů projektů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Chcete-li vytvořit a spravovat projekt, musíte na projekt použít šablonu kalendáře. Šablona kalendáře definuje následující atributy projektu:

- Pracovní doba, včetně času zahájení a ukončení
- Pracovní dny
- Výjimky v kalendáři, například nepracovní dny

Šablona kalendáře, která se použije na projekt, je kopií šablony kalendáře definované v nastavení vaší organizace.

> [!NOTE]
> Pokud změníte šablonu kalendáře, tyto změny se nebudou šířit do pracovní doby projektu. Chcete-li změnit pracovní dobu projektu, je nutné použít novou šablonu.

K vytvoření šablony kalendáře pro vaši organizaci existují dva klíčové požadavky:

- Definujte požadovanou pracovní dobu šablony pomocí nového nebo existujícího rezervovatelného zdroje.
- Vytvořte novou šablonu kalendáře a přidružte ji k rezervovatelnému prostředku.

**Definujte pracovní dobu šablony**

1. Přejděte na **Zdroje** \> **Zdroje**.
2. Vytvořte nový prostředek, který bude odkazovat v šabloně kalendáře, nebo vyberte existující prostředek.
3. Vyberte kartu **Pracovní doba** zdroje a postupujte podle pokynů v části [Nastavení pracovní doby zdroje](/dynamics365/field-service/set-work-hours-resource) ke konfiguraci pravidel kalendáře.

**Vytvořit novou šablonu kalendáře**

1. Přejděte na **Nastavení** \> **Šablona kalendáře**.
2. Vyberte **Nový** a zadejte název, popis a prostředek šablony.

> [!NOTE]
> Když je prostředek odkazován v šabloně kalendáře, je kopie kalendáře prostředku přidružena k šabloně kalendáře. Pokud se změní pracovní doba kopírované šablony, tyto změny se nebudou šířit do šablony kalendáře.

Nyní můžete šablonu práce přidružit k šabloně kalendáře projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

