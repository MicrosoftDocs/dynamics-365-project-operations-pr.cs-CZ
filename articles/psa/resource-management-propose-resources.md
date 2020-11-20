---
title: Navrhování projektových zdrojů
description: Toto téma obsahuje informace o navrhování projektových zdrojů.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 1fcb8d1d40286cf5cbb23338f93b072ae5bed70d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120175"
---
# <a name="propose-project-resources"></a>Navrhování projektových zdrojů

Správci zdrojů mohou navrhnout zdroj projektovému manažerovi pomocí žádosti o zdroj.

1. Z mřížky žádosti nebo ze samotné žádosti vyberte **Najít zdroje**.
2. Na stránce **Pomocník plánování** vyberte zdroj a potom v podokně **Vytvořit rezervaci zdroje** v poli **Stav rezervace** vyberte **Rezervovat**.

    ![Vybraný navržený zdroj](media/Resource-Management-image62.png)

Dojde k následujícím aktualizacím stavu:

- Na stránce **Pomocník plánování** jsou ukazatele stavu aktualizovány tak, aby označovaly, že rezervace je navržena, že není závazně rezervována.

    ![Ukazatele stavu pro navrženou rezervaci na stránce Pomocník plánování](media/Resource-Management-image63.png)

- U žádosti o zdroj se stav změní na **Potřebuje kontrolu**.

    ![Stav žádosti o zdroj změněný na Potřebuje kontrolu](media/Resource-Management-image64.png)

- Na kartě **Tým** projektu je změněna hodnota **Stav žádosti** obecného člena týmu na **Potřebuje kontrolu**.

    ![Stav žádosti obecného člena týmu změněný na Potřebuje kontrolu na kartě Tým](media/Resource-Management-image48.png)

Projektový manažer může návrh buď přijmout, nebo zamítnout.

Správci zdrojů mohou při zpracování žádostí o zdroje použít kterýkoli z následujících přístupů:

- Navrhnout více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro splnění požadovaných hodin. Navržené hodiny jsou pak rozděleny mezi více zdrojů, které mohou uspokojit požadované hodiny. V tomto scénáři se hodiny nemohou překrývat.
- Navrhnout méně zdrojů, než je vyžadováno. V tomto scénáři je navrhovaná kapacita zdroje menší než požadovaná doba, kterou žadatel specifikoval. Proto, když žadatel přijme navržené prostředky, je vytvořen nesplněný požadavek na zdroj k zachycení zbývající poptávky.
- Rezervovat více zdrojů pro uspokojení poptávky, pokud není k dispozici žádný zdroj pro dokončení práce.
- Rezervovat méně zdrojů, než je vyžadováno. V tomto scénáři je počet rezervovaných hodin menší než počet požadovaných hodin. Systém vás provede návrhy zdrojů místo rezervací, aby mohl žadatel ověřit a sledovat zbývající poptávku.

## <a name="billable-utilization"></a>Fakturovatelné využití

Zdroje mohou mít cílové fakturovatelné využití. Toto cílové využití je buď definováno jako atribut výchozí role zdroje, nebo je nastaveno v záznamu konkrétního rezervovatelného zdroje. Výpočty využití vycházejí ze skutečných hodin, které zdroje vykázaly pomocí schválených časových záznamů.

K výpočtu využití se používají následující vzorce:

- Fakturovatelné využití = skutečné fakturovatelné hodiny ÷ kapacita zdroje
- Nefakturovatelné využití = skutečný čas s ID typu fakturace = neúčtovatelné, komplementární nebo nedostupné ÷ kapacita zdroje
- Interní = skutečný čas bez prodejní smlouvy ÷ kapacita zdroje
- Kapacita zdroje = pracovní doba zdroje – mimo kancelář – nepracovní dny

Zobrazení **Využití zdroje** naleznete v podokně **Zdroje**.

![Zobrazení Využití zdroje](media/Resource-Management-image65.png)

Každá buňka v tabulce představuje procentuální hodnotu fakturovatelného využití zdroje v určitém období, například den, týden nebo měsíc. K obarvení buněk se používají následující vzorce:

- **Zelená:** fakturovatelné využití \>= cílové využití zdroje
- **Žlutá:** cílové využití – 20 \<= fakturovatelné využití \< cílové využití
- **Červená:** fakturovatelné využití \< cílové využití – 20

Vzhledem k tomu, že je zobrazení **Využití zdroje** založeno na Plánovací vývěsce, můžete k filtrování výsledků využít funkce filtrování Plánovací vývěsky.

Mřížka vyžaduje, abyste nastavili cílové využití buď u role, nebo u konkrétního zdroje. Pro toto nastavení přejděte na **Zdroje** \> **Role zdrojů**.

Navíc musí být ke každému rezervovatelnému zdroji přiřazena výchozí role. Přejděte na **Zdroje** \> **Zdroje**. Na kartě **Project Service** ověřte, zda je definována role zdroje a zda pole **Je výchozí** je pro ni nastaveno na **Ano**. Můžete přidat další role, kde **Je výchozí = Ne**. Role, ve které **Je výchozí = Ano**, slouží k vyhodnocení využití prostředku vůči cíli pro danou roli.

![Nastavení výchozí role](media/Resource-Management-image67.png)

Na kartě **Project Service** můžete také nastavit individuální cílové využití zdroje. Výpočet využití pak používá toto cílové využití k vyhodnocení cíle zdroje namísto cíle výchozí role zdroje.

Využití je pro zdroj zobrazeno pouze v případě, že tento zdroj má schválenou fakturovatelnou dobu během období zobrazeného v mřížce.

## <a name="resource-availability"></a>Dostupnost zdroje

Je důležité, aby správci zdrojů mohli zobrazit dostupnost zdrojů a aktualizovat rezervace. V některých případech neexistuje formální poptávka (žádost o zdroj), ale správce zdrojů musí odpovědět na neplánovanou poptávku, která přichází prostřednictvím kanálů, jako je e-mail, telefonní hovor nebo rychlá zpráva. Správci zdrojů používají k aktualizaci zdrojů a rezervací Plánovací vývěsku.

Jako základ pro výpočet dostupnosti zdroje slouží pracovní doba zdroje. Rezervace zdrojů spotřebovávají kapacitu zdrojů.

![Plánovací vývěska](media/Resource-Management-image68.png)

Plánovací vývěska používá barvy a stínování k zobrazení rezervací, dostupnosti a přerezervace a také stavu rezervací. Nastavení v Plánovací vývěsce umožňuje zobrazit legendu.

Pokud se vedle konkrétního rezervovatelného zdroje v plánovací vývěsce zobrazí šipka vpravo, lze zdroj rozbalit, aby se zobrazily podrobnosti o práci, pro kterou je zdroj rezervovaný.

![Rozbalený rezervovatelný zdroj v Plánovací vývěsce](media/Resource-Management-image69.png)

Protože Dynamics 365 Project Service Automation používá modul Universal Resource Scheduling, tak pokud máte nainstalovanou aplikaci Dynamics 365 Field Service můžete také zobrazit podrobnosti o rezervacích zdrojů pro projekty, pracovní objednávky a všechny další entity, na které jste rozšířili plánování.

![Podrobnosti rezervací zdrojů pro projekty a pracovní objednávky](media/Resource-Management-image70.png)

Chcete-li zobrazit další podrobnosti o konkrétním zdroji, klepněte na něj pravým tlačítkem myši a otevřete kartu zdroje.

![Karta zdroje](media/Resource-Management-image71.png)
