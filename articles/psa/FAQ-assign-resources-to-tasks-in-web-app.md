---
title: Jak přiřadit rezervovatelný zdroj k úkolu ve webové aplikaci
description: Přehled způsobů, kterými můžete přiřadit rezervovatelné zdroje.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
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
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146565"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Jak přiřadit rezervovatelný zdroj k úkolu ve webové aplikaci (aplikace Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Existují dva způsoby, jak přiřadit zdroj k úkolu v aplikaci Project Service. Můžete rezervovat zdroj jako člena týmu a pak ho přiřadit k úkolu. Nebo můžete vytvořit obecného člena týmu prostřednictvím přiřazení role na úkoly, generovat tým a poté splnit podpůrné požadavky s pojmenovaným zdrojem.

Všimněte si, že pokud chcete přiřadit rezervovatelný zdroj k úkolu, rezervovatelný člen týmu zdrojů musí mít dostatek dostupných rezervací. Stav rezervace musí být Typ potvrzení Závazně rezervovat a Stav potvrzeno. Pokud není k dispozici dostatek rezervací pro zdroj, Project Service odebere přiřazení a zobrazí následující chybovou zprávu:

*Nelze přiřadit zdroj k úkolu - Následující zdroje nemají dostatek hodin rezervovaných proti projektu*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervace zdroje jako člena týmu a následné přiřazení zdroje k úkolu

Při použití této metody přidáte zdroj do projektového týmu a poté přiřadíte zdroje k úkolům v plánu projektu. Zde je postup:
1.  V mřížce člena týmu přidejte nového člena týmu výběrem možnosti **Nový**.
2.  Na obrazovce rychlého vytvoření člena týmu zvolte název rezervovatelného zdroje a nastavte roli.
3.  Zvolte data **Od** a **Do**.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot znázorňující přidání člena týmu](media/FAQ-Resources-to-Tasks2-1.png "Screenshot znázorňující přidání člena týmu")
 
4.  Vyberte jednu z následujících metod přidělení pro rezervaci zdroje:
    - **Plná kapacita** rezervuje plnou kapacitu zdroje pro zadaná počáteční a koncová data.
    - **Procentuální kapacita** rezervuje zdroj pro procento kapacity zdroje pro daná počáteční a koncová data.
    - **Rovnoměrně rozdělit podle hodin** rezervuje zdroj pro určený počet hodin a distribuuje ho rovnoměrně každý den v období od počátečního do koncového data.
    - **Vytížení na začátku podle hodin** rezervuje zdroj pro určený počet hodin s vytížením na začátku každý den v období od počátečního do koncového data.

    Nevybírejte **Žádné**, protože to přidá zdroj k týmu, ale nevytvoří žádné rezervace, které absorbují kapacitu zdroje.
5.  Vyberte **Uložit**.

    Všimněte si, že hodiny rezervace musí být dostatečné k pokrytí hodin úsilí a datového rozsahu úkolů, ke kterým přiřazujete tento zdroj. Pokud nejsou ve shodě, nelze přiřadit zdroj k úkolu.

6.  Na strukturovaném rozpisu prací pro daný úkol klikněte na rozevírací seznam buňky zdroje. A poté: 

    1. Vyberte **Přidat**.
    2. Vyberte rozevírací seznamu pod možností **Zdroje** a vyberte člena týmu, kterého jste přidali výše.
    3. Vyberte **OK**. Člen týmu je nyní přiřazen k úkolu.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot znázorňující přidání zdrojů pomocí WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot znázorňující přidání zdrojů pomocí WBS")
 
V mřížce člena týmu uvidíte agregaci přiřazených hodin zdroje pod položkou Přiřazené hodiny. Bude menší nebo rovna rezervovaným hodinám pro daný zdroj. 

> [!div class="mx-imgBorder"] 
> ![Screenshot znázorňující přiřazené hodiny zdroje](media/FAQ-Resources-to-Tasks2-3.png "Screenshot znázorňující přiřazené hodiny zdroje")
 
Pokud úloha, kterou se pokoušíte přiřadit zdroji, začíná po datu ukončení rezervace zdrojů, nebude zdroj v rozevíracím seznamu zobrazen.

Všimněte si, že můžete přiřadit zdroj více hodinám než jsou jeho rezervované hodiny, pokud má zdroj nějakou zbývající nepřiřazenou kapacitu. V takovém případě bude zdroj pouze částečně přiřazen ke svým rezervacím. Tyto zbývající nepřiřazené hodiny úloh můžete vidět přidáním sloupce Nevykryté hodiny do strukturovaného rozpisu prací.

Pokud jsou zdroje přiřazeny ke svým rezervovaným hodinám (jejich rezervované hodiny se shodují s přiřazenými hodinami), při pokusu o přiřazení dalších úkolů se zobrazí následující chybová zpráva:

*Nelze přiřadit zdroj k úkolu - Následující zdroje nemají dostatek hodin rezervovaných proti projektu.*

Navíc je při tvorbě projektu přidán výchozí člen týmu projektového manažera, který je přidán do týmu bez jakýchkoli rezervací a nemůže být přiřazen žádnému úkolu. Nezobrazí se v rozevíracím seznamu zdrojů pro úkoly.

Chcete-li tento zdroj přiřadit, musíte ho odebrat z týmu a potom ho přidat znovu jinou metodou přidělení než Žádná. Důvod, proč jsou přidáni do týmu při vytváření projektu, je ten, aby projekt měl ve výchozím nastavení alespoň jednoho schvalujícího projektu.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Vytvoření obecného člena týmu prostřednictvím přiřazení role na úkoly

Tato metoda zajišťuje, že zdroje mají dostatek rezervací pro úkoly. Nejprve je třeba vytvořit zástupce nebo obecný zdroj, který popisuje vlastnosti pojmenovaného zdroje, u kterého chcete, aby pracoval na úkolech, vygenerováním týmu po přiřazení rolí k úkolům. Zde je postup:

1. Na strukturovaném rozpisu prací vyberte požadovaný úkol.
2. Vyberte ikonu rozevíracího seznamu **Přiřazená role** v buňce zdroje.
3. Vyberte rozevírací seznam **Role** a vyberte roli pro obecný zdroj.
4. Vyberte **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot znázorňující přidání zdroje pomocí WBS](media/FAQ-Resources-to-Tasks2-4.png "Screenshot znázorňující přidání zdroje pomocí WBS")
 
Po dokončení přiřazování rolí k úkolům ve strukturovaném rozpisu prací vyberte **Vygenerovat projektový tým**. Project Service vytvoří minimální počet obecných členů týmu založený na rolích, organizačních jednotkách zdrojů a kalendáři projektu pomocí agregace přiřazení úkolů.

> [!div class="mx-imgBorder"] 
> ![Screenshot znázorňující generování projektového týmu](media/FAQ-Resources-to-Tasks2-5.png "Screenshot znázorňující generování projektového týmu")
 
Na mřížce Člen týmu se zobrazí zdroje typu Obecný zdroj s názvem role a pozice. Pokud jsou potřebné dva zdroje pro roli k dokončení práce, funkce Vygenerovat tým vytvoří dva členy týmu a použije název pozice, aby je nastavila odděleně.

> [!div class="mx-imgBorder"] 
> ![Screenshot znázorňující přidání dvou obecných zdrojů](media/FAQ-Resources-to-Tasks2-6.png "Screenshot znázorňující přidání dvou obecných zdrojů")
 
Požadavek na podpůrný zdroj pro obecného člena týmu můžete otevřít výběrem odkazu v části Požadavek na zdroj.

> [!div class="mx-imgBorder"] 
> ![Screenshot znázorňující požadavek na podpůrný zdroj](media/FAQ-Resources-to-Tasks2-7.png "Screenshot znázorňující požadavek na podpůrný zdroj")

Vyberte možnost **Rezervovat** pro obecný zdroj a pak můžete použít plánovací vývěsku pro nalezení a rezervaci skutečného zdroje. Je také možné odeslat požadavek na splnění manažerem zdrojů volbou **Odeslat požadavek**.

Když je obecný zdroj naplněn pojmenovaným zdrojem, obecný zdroj je odebrán z týmu a přiřazení úkolů pro obecný zdroj jsou přiřazena k pojmenovanému zdroji, který splnil požadavek na zdroj obecného zdroje.
 

