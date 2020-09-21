---
title: Metody přidělení rezervace
description: Toto téma obsahuje informace o různých způsobech, kterými můžete rezervovat přidělení.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
ms.assetid: 5bb0fdbc-88fe-43eb-8abf-4af9c2352a57
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 030d4fc3bb64fcc67b4a5e51016a8b3a028f3ca8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750284"
---
# <a name="booking-allocation-methods"></a>Metody přidělení rezervace

Ať už přidáváte člena týmu přímo do projektu na kartě **Tým** nebo rezervujete zdroj pro projekt nebo požadavek z Plánovací vývěsky, existuje několik různých metod přidělení rezervace, které můžete použít. Toto téma vysvětluje, jak funguje každá metoda, a jaké metody by mohly vést k přerezervaci zdrojů.

## <a name="booking-allocation-methods"></a>Metody přidělení rezervace

### <a name="full-capacity"></a>Plná kapacita 
Metoda plné kapacity rezervuje pro určená data od a do plnou kapacitu zdroje. Například pokud má zdroj kalendář nastavený na osm hodin práce denně, pět dnů týdně, nastavení dat zahájení a ukončení, která zahrnují pět pracovních dnů, zarezervuje zdroj na 40 hodin. Rezervace se provádí bez ohledu na zbývající kapacitu zdrojů. Pokud je zdroj již rezervován v tomto období na jiné projekty, 40 hodin je rezervováno jako další hodiny, což by mohlo vést k přerezervaci.

### <a name="remaining-capacity"></a>Zbývající kapacita
Metoda zbývající kapacity je dostupná pouze tehdy, když rezervujete přímo na projekt pomocí plánovací vývěsky. Tato metoda rezervuje dostupnou kapacitu zdroje v rámci určeného datového rozsahu. Například pokud má zdroj kapacitu 40 hodin týdně a byl již rezervován na 10 hodin, rezervace pro tentýž týden bude mít za následek rezervaci zbývajících 30 hodin kapacity pro daný týden.

### <a name="percentage-capacity"></a>Procentuální kapacita
Metoda procentuální kapacity rezervuje zdroj pro procento kapacity zdroje pro daná počáteční a koncová data. Například pokud je kalendář zdroje nastavený na osm hodin práce denně, pět dnů týdně, tak nastavení dat zahájení a ukončení, která zahrnují pět pracovních dnů při 50% kapacitě, zarezervuje zdroj na 20 hodin. Jednotlivé rezervace denně jsou rovnoměrně rozmístěny přes období, 4 hodiny denně v tomto příkladu. Rezervace se provádí bez ohledu na zbývající kapacitu zdrojů. Pokud je zdroj již rezervován v tomto období na jiné projekty, 20 hodin je rezervováno jako další hodiny, což by mohlo vést k přerezervaci.

### <a name="evenly-distribute-hours"></a>Rovnoměrné rozdělení hodin
Metoda rovnoměrného rozdělení hodin rezervuje zdroj pro určený počet hodin a distribuuje čas rovnoměrně každý den v období od počátečního do koncového data. Například pokud rezervujete zdroj na dobu 20 hodin během pěti dnů, tato metoda rozděluje 20 hodin rovnoměrně na čtyři hodiny denně. Rezervace se provádí bez ohledu na zbývající kapacitu zdrojů. Pokud je zdroj již rezervován v tomto období na jiné projekty, 20 hodin je rezervováno jako další hodiny, což by mohlo vést k přerezervaci.

### <a name="front-load-hours"></a>Více hodin na začátku
Metoda více hodin na začátku rezervuje zdroj pro určený počet hodin s vytížením na začátku každý den v období od počátečního do koncového data. Vytížení na začátku spotřebovává dostupnou kapacitu v pořadí „první v prvně spotřebovaných“. Například pokud je pracovní plán zdroje osm hodin denně, pět dní v týdnu a nemá žádné aktuální rezervace, rezervace zdroje na 20 hodin během pěti pracovních dnů vede k následujícímu vzorci denní rezervace: 

|                           |    Den 1    |    Den 2    |    Den 3    |    Den 4    |    Den 5    |    Celkem    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Existující rezervace    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Nová rezervace          |    8        |    8        |    4        |    0        |    0        |    20       |

Metoda vytížení na začátku bere v úvahu existující rezervace a dostupnou kapacitu. Například pokud stejný zdroj již má v týdnu 20 hodin rezervací, nové rezervace spotřebovávají zbývající kapacitu takto:

|                     | Den 1 | Den 2 | Den 3 | Den 4 | Den 5 | Celkem |
|---------------------|-------|-------|-------|-------|-------|-------|
| Existující rezervace | 8     | 8     | 4     | 0     | 0     | 20    |
| Nová rezervace       | 0     | 0     | 4     | 8     | 8     | 20    |

Protože je zvážena dostupná kapacita, může se zobrazit chybová zpráva, pokud nemá zdroj žádnou zbývající kapacitu, která může být absorbována rezervací. S touto metodou nelze dosáhnout přerezervace.

### <a name="none"></a>Žádný
Možnost nepoužít žádnou metodu je k dispozici pouze tehdy, když rezervujete z karty **Tým** v rámci projektu. Tato metoda přidá zdroj jako člena týmu na projekt, ale nevytvoří žádné rezervace, které absorbují kapacitu zdroje. Tato metoda se používá při přidání výchozího člena týmu projektového manažera u vytvoření projektu. Uživatel projektového manažera, který vytvořil projekt, bude automaticky přidán do projektu tak, aby záznam entity projektu měl vlastníka a v projektu byl jeden schvalovatel. Vzhledem k tomu, že tento uživatel nemá žádné rezervace, tak chcete-li rezervovat zdroj, můžete ho buď vymazat a poté ho znovu přidat pomocí jiné metody přidělování, nebo přidat zdroj k úkolům a potom použít **Prodloužit rezervace** na kartě **Vyrovnání** pro vytvoření rezervace pro přiřazení.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Metod přidělení, které vedou k přerezervaci
Stručně řečeno, následující metody přidělování vedou k přerezervování, pokud je zdroj již vázán v jiných projektech (nebo u jiných pracovních příkazů nebo plánovatelných entit):

- Plná kapacita
- Procentuální kapacita
- Rovnoměrné rozdělení hodin

Používáte-li jednu z těchto tří metod přidělení, nebudete upozorněni, že je zdroj přerezervován. Chcete-li opravit přerezervaci, musíte použít Plánovací vývěsku.
