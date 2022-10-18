---
title: Proces konverze plánování projektu Project Service Automation na Project Operations
description: Tento článek poskytuje přehled změn funkcí pro Microsoft Dynamics 365 Project Service Automation na Dynamics 365 Project Operations
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642560"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Proces konverze plánování projektu Project Service Automation na Project Operations

Po úspěšném upgradu projektu z Microsoft Dynamics 365 Project Service Automation 3.X na Dynamics 365 Project Operations Lite není editace projektových úkolů ve struktuře rozpisu úkolů mřížky (WBS) možná. Zákazníci si budou moci prohlédnout WBS ve sledovací mřížce, kde byla přidána nová pole, která poskytují všechny podrobnosti, které souvisejí s úkolem. U projektů, kde jsou vyžadovány úpravy WBS, můžete selektivně převést způsobilé projekty do nového prostředí plánování Project for the web.

## <a name="project-conversion-process"></a>Postup převodu projektu

Při převodu projektu postupujte takto.

1. Otevřete hlavní stránku projektu a vyberte **Převést** na podokně akcí.
1. V potvrzovacím okně vyberte **OK** pro spuštění převodu projektu. Proběhnou následující akce:

    1. Panel zpráv, který se objeví na hlavní stránce projektu, uvádí: „Plán projektu se převádí. Dokud nebude převod dokončen, nemůžete v projektu provádět změny.“
    1. Budete přesměrováni na seznam projektů.

    Po dokončení převodu projektu proběhnou následující akce:

    1. Přiřazený projektový manažer obdrží upozornění na pravé straně aplikace.
    1. Panel zpráv oznamující, že probíhá převod, je odstraněn.
    1. Karta **Plán** zobrazuje nové prostředí plánování s Project for the web. Každý uživatel, který má příslušné licence a role zabezpečení, může upravovat WBS.
    1. Pole **Modul plánování** je aktualizováno na **Project for the web**.
    1. Tlačítko **Převést** je odstraněno z podokna akcí.

> [!IMPORTANT]
> Hromadný převod projektů není povolen. Jakýkoli pokus o aktualizaci velkého množství projektů současně bude omezen. Toto omezení pomáhá zajistit vysoký výkon pro všechny zákazníky.

## <a name="manual-tasks-vs-automatic-tasks"></a>Ruční úlohy a automatické úlohy

Když je prostředí upgradováno z Project Service Automation na Project Operations, jsou všechny úlohy ve WBS považovány za automaticky naplánované. Koncept ručně naplánovaných úloh není v Project for the web k dispozici. Můžete však definovat preferované chování plánování pro své projekty pomocí nastavení [režim plánování](/project-management/scheduling-modes.md) při vytváření nových projektů.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Omezené operace pro projekty před konverzí

Tato část popisuje funkční rozdíly, které můžete očekávat, když projekty nebyly převedeny.

### <a name="copy-project"></a>Kopírování projektu

Operace **Kopírovat** je podporována pouze u převedených projektů. Upgradované projekty nelze před převodem zkopírovat.

### <a name="move-project"></a>Přesunutí projektu

Změna data zahájení projektu úměrně neposune začátek úkolů, pokud nebyl projekt převeden.

## <a name="frequently-asked-questions"></a>Nejčastější dotazy

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Jaké jsou rozdíly mezi převedenými projekty a novými projekty, které se vytvoří po dokončení upgradu?

U projektů, které jsou převedeny po upgradu prostředí, bude nastaven příznak, který dá pokyn, aby plán respektoval pouze kalendář projektu. Toto chování odpovídá chování v Project Service Automation. Příznak však nebude nastaven pro nové projekty vytvořené po upgradu. Proto bude plán respektovat pracovní dobu zdrojů, když jsou přiřazeny k úkolu.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Co mám dělat, když se můj projekt nepodaří převést?

Pokud se váš projekt nezdaří převést, prvním krokem je zkontrolovat protokoly chyb a identifikovat všechny běžné problémy související s vaším WBS. Pokud protokoly neoznačují konkrétní chybu, kterou byste mohli podniknout, kontaktujte zákaznickou podporu, aby mohl být váš případ dále přezkoumán.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Jak se v Project for the web řeší uzavření podniků?

Project for the web nerespektuje uzavření podniku, které podnik definuje na úrovni organizace. Bude však respektovat jiné typy dnů volna, které jsou definovány v dané šabloně pracovní doby.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Jaká jsou omezení funkce Project for the web?

Viz [Vytvoření strukturovaného rozpisu prací: omezení projektu](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Mohu očekávat změny v odhadech nákladů a prodeje?

Ve vzácných případech, kdy jsou obrysy přiřazení zdrojů přepočítány nebo kdy spadají do jiné časové hranice než zdrojový projekt, můžete zaznamenat rozdíly v odhadech prodejů a nákladů. V rámci procesu upgradu se očekává, že zákazníci otestují reprezentativní vzorovou sadu projektů, aby porozuměli případným změnám harmonogramu.
