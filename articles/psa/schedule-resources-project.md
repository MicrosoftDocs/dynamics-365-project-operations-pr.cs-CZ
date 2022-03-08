---
title: Plánování zdrojů pro projekt
description: Postup plánování zdrojů pro projekt v Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 7beb1f86795a909a1266b2a2c97421e1f04ef3c4cf2f9b49413cd1382b0f2011
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998138"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Plánování zdrojů pro projekt (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Můžete zkontrolovat dostupnost zdrojů, chcete-li získat celkový přehled o tom, jak jsou zdroje rezervovány, nebo můžete filtrovat zobrazení podle dovedností, týmu, umístění a dalších možností.  
  
Plánovací vývěska zobrazuje seznam zdrojů a jejich dostupnost. Vyberte režim zobrazení pro zobrazení dostupnosti podle **Hodin**, **Dne**, **Týdne** nebo **Měsíce**.  
  
Před použitím plánovací vývěsky je třeba ji nastavit. Další informace naleznete v tématu [Konfigurace plánovací vývěsky (Field Service nebo Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Pokud používáte starší verzi, naleznete informace o dostupnosti zdrojů v části [Zobrazení dostupnosti zdrojů](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Abyste mohli používat funkci rezervace plánovací vývěsky, geografické kódování a služby zjišťování polohy, je třeba zapnout mapy.  
> 
> 1. V hlavní nabídce vyberte **Plánování zdrojů** > **Správa**.  
> 2. Klikněte na **Parametry plánování**.  
> 3. Otevřete záznam a přejděte dolů do části **Resource Scheduling Optimization**.  
> 4. V poli **Připojit k mapám** vyberte **Ano**.  
> 5. Přijměte podmínky a uložte záznam.  
> 6. V hlavní nabídce vyberte **Project Service** > **Plánovací vývěska**. Požadavek na rezervaci odsud lze ručně naplánovat několika způsoby. Zvolte metodu, která u vás funguje.
  
## <a name="find-available-resources"></a>Nalezení dostupných zdrojů

1.  V seznamu **Požadavek na rezervaci** klikněte pravým tlačítkem myši na nenaplánovanou rezervaci a vyberte některou z následujících možností:  
  
- Zvolte **Najít dostupnost – aktuální zdroje** pro vyhledání dostupného zdroje ze seznamu na plánovací vývěsce.  
- Zvolte **Najít dostupnost – všechny zdroje** pro vyhledání dostupného zdroje ze zdrojů v systému.  
   > [!NOTE]
   >  Následně filtry zobrazí možnosti pro vybraný požadavek na rezervaci.  
  
2. Pokud vidíte volnou pozici, klikněte pravým tlačítkem myši na časový úsek na plánovací vývěsce a zvolte **Rezervovat zde**. Nebo přetáhněte požadavek na rezervaci na dostupný časový úsek.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Rezervování zdroje pomocí denního zobrazení a vyhledání málo rezervovaných zdrojů
  
1.  Na plánovací vývěsce zvolte **Režim zobrazení** a vyberte **Dny**.  
  
    Bude k dispozici zobrazení mřížky uvádějící, kolik hodin denně je zdroj rezervován a které dny je volný.  
  
2.  Klikněte na jméno zdroje, který chcete rezervovat, a potom zvolte **Rezervovat**.  
  
3.  V dialogovém okně **Rezervace zdrojů (vytvoření)** zvolte projekt, pro který chcete daný zdroj rezervovat, a také způsob rezervace a počáteční a koncový čas.  
  
4.  Až budete hotovi, vyberte **Rezervovat**.  
  
## <a name="view-to-the-schedule-board"></a>Zobrazit na plánovací vývěsce
  
1.  Vyberte neplánovaný požadavek na rezervaci ze seznamu ve spodní části.  
  
2.  Přetáhněte požadavek na rezervaci na dostupnou pozici zdroje/času na plánovací vývěsce.  
  
3.  Až budete hotovi, vyberte **Rezervovat**.  
  
### <a name="additional-resources"></a>Další materiály  
 [Příručka pro manažera zdrojů](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]