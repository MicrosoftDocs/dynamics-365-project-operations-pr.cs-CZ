---
title: Vytvoření šablony pracovní doby
description: Toto téma popisuje postup vytvoření šablony pracovní doby v Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 5788378c7e015c4b11182aaf427aca7d1da48b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598940"
---
# <a name="create-a-work-hours-template-project-service"></a>Vytvoření šablony pracovní doby (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

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


### <a name="see-also"></a>Viz také  
 [Nastavení zdrojů](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
