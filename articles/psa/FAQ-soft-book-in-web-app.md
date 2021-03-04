---
title: Jak předběžně rezervovat zdroje v aplikaci verze 2.x?
description: Tento článek popisuje, jak předběžně rezervovat členy týmu projektu s pomocí Project Service.
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
ms.openlocfilehash: 6bd13c448f4ce16fb93843df54f26cdd9bb884f4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146475"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Jak předběžně rezervuji zdroje ve webové aplikaci (Project Service app v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Nezávazně můžete naplánovat nebo předběžně rezervovat zdroj do projektového týmu pro zobrazení toho, že plánujete přiřazení zdroje k projektu. Předběžné rezervace nespotřebovávají dostupné kapacity zdroje. Předběžně rezervované členy týmu nelze přiřadit k úkolům projektu. Pouze závazně rezervované zdroje a s typem potvrzení Potvrzeno lze přiřadit k úkolům (za předpokladu, že mají dostatek rezervačních hodin k pokrytí úsilí přiřazení).

Předběžně rezervovaní členové týmu projektu se zobrazí v mřížce Člen týmu s předběžně rezervovanými hodinami zobrazenými ve sloupci předběžné rezervace. Zobrazí se také na plánovací vývěsce. Neoznačují jakoukoli spotřebu kapacity, protože předběžně rezervované zdroje nespotřebovávají kapacitu zdroje.

Existují tři způsoby předběžné rezervace člena týmu na projekt s verzí služby Project Service 2.x. Můžete provést předběžnou rezervaci pomocí plánovací vývěsky, použít funkci Správa rezervace nebo vytvořit obecný zdroj. Tyto metody jsou popsány níže.

## <a name="soft-book-with-the-schedule-board"></a>Předběžná rezervace pomocí plánovací vývěsky

Chcete-li vytvořit předběžnou rezervaci pomocí plánovací vývěsky, postupujte takto: 
1. Otevřete plánovací vývěsku.
2. Zvolte kartu Projekt na spodním panelu Požadavky na rezervace v plánovací vývěsce.
3. Najděte projekt, na který chcete předběžně rezervovat zdroj. Pokud máte mnoho projektů, klikněte na záhlaví sloupce Projekt a pak použijte filtr k vyhledání projektu.
4. Klikněte na projekt a potom ho přetáhněte na časovou mřížku zdroje.
5. Otevře se panel Vytvořit rezervaci zdroje na pravé straně. Upravte počáteční a koncové datum, vyberte Stav rezervace jako Předběžná a nastavte hodiny. 
6. Klikněte na Rezervovat.
7. Zpět na projektu se nyní zobrazí zdroj jako člen týmu s předběžně rezervovanými hodinami ve sloupci Předběžná rezervace.

Všimněte si, že je nelze přiřadit k úkolům ve strukturovaném rozpisu práce, protože prostředky musí být závazně rezervovány na týmu, aby je bylo možné přiřadit.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Předběžná rezervace pomocí funkce Správa rezervací

Chcete-li vytvořit předběžnou rezervaci pomocí správy rezervace, postupujte takto:
1. V mřížce člena týmu klikněte na Nový.
2. Vyberte rezervovatelný zdroj, roli, od/do.
3. Vyberte metodu přidělení jinou než Žádná:
- Plná kapacita
- Procentuální kapacita
- Rovnoměrně rozdělit podle hodin
- Vytížení na začátku podle hodin
4. Klikněte na tlačítko Uložit. Zdroje uvidíte na mřížce týmu a jejich hodiny budou označené jako Závazné.
5. Kliknutím na Správa rezervací spravujte rezervace zdroje.
6. Při otevření plánovací vývěsky rozbalte zdroje pro zobrazení jejich rezervací. Uvidíte rezervaci označenou jako Závazná.
7. Klikněte pravým tlačítkem myši na rezervaci a u možnosti Změnit stav vyberte Předběžná rezervace a potom Předběžná. Stav rezervace je nyní Předběžná.
8. Po uzavření plánovací vývěsky uvidíte, že se hodiny pro zdroj změnily ze závazných na předběžné na mřížce člena týmu.
Mějte na paměti, že pokud závazně rezervujete zdroj pro tým a poté mu přiřadíte úkoly ve strukturovaném rozpisu prací, když používáte správu rezervací pro změnu stavu ze závazné na předběžnou, odeberou se z úkolů přiřazení pro tento zdroj, protože pouze závazně rezervované zdroje lze přiřadit k úkolům.

## <a name="soft-book-by-creating-a-generic-resource"></a>Předběžná rezervace vytvořením obecného zdroje

Předběžnou rezervaci můžete vytvořit pomocí vygenerování obecného člena týmu zdrojů podle plánovací vývěsky nebo žádosti o zdroj a změnou typu během rezervace.
Pro vykonání této akce použijte tento postup:

1. Ve strukturovaném rozpisu prací projektu přiřaďte role k úkolům, pro které chcete vygenerovat obecné členy týmu.
2. Klikněte na Vygenerovat projektový tým.
3. V mřížce člena týmu projektu vyberte obecný zdroj a klikněte na Rezervovat.
4. Na plánovací vývěsce vyberte zdroj, který chcete rezervovat.
5. Na panelu Vytvořit rezervaci zdroje plánovací vývěsky změňte stav rezervace na Předběžná.
6. Klikněte na Rezervovat nebo Rezervovat a Ukončit.

Po zavření plánovací vývěsky uvidíte vybraný zdroj přidaný do týmu s předběžně rezervovanými hodinami a přiřazenými hodinami. Uvidíte také, že obecný zdroj zůstane v týmu jako ukazatel, že úkoly jsou přiřazeny předběžně rezervovanému členu týmu.

Pokud budete chtít změnit předběžně rezervovaný zdroj člena týmu na závazně rezervovaného člena týmu, abyste mu mohli přiřadit úkoly, proveďte následující kroky:

1. Vyberte zdroj a klikněte na tlačítko Správa rezervací.
2. Při otevření plánovací vývěsky rozbalte zdroje pro zobrazení jejich rezervací. Uvidíte rezervaci označenou jako Předběžná.
3. Klikněte pravým tlačítkem myši na rezervaci a u možnosti Změnit stav vyberte Závazná rezervace a potom Závazná. Stav rezervace je nyní Závazná.
4. Po uzavření plánovací vývěsky uvidíte, že se hodiny pro zdroj změnily ze předběžných na závazné na mřížce člena týmu. Nyní můžete přiřadit zdroj k úkolům (za předpokladu, že existuje shoda mezi závazně rezervovanými hodinami a hodinami úsilí úkolu pro přiřazení). Všimněte si, že pokud jste postupovali podle kroků plnění obecného zdroje ve výše uvedeném bodu 3, při změně stavu předběžně rezervovaného zdroje na závazně rezervovaný, obecný člen týmu se z týmu odstraní.
