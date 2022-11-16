---
title: Upgrade z Project Service Automation na Project Operations
description: Tento článek obsahuje přehled funkce procesu upgradu z Microsoft Dynamics 365 Project Service Automation na Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736658"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Upgrade z Project Service Automation na Project Operations

S potěšením oznamujeme první ze dvou fází upgradu z Microsoft Dynamics 365 Project Service Automation na Microsoft Dynamics 365 Project Operations. Tento článek poskytuje přehled pro zákazníky, kteří se vydávají na tuto vzrušující cestu. 

Program doručení upgradu bude rozdělen do tří fází.

| Doručení upgradu | Fáze 1 (leden 2022) | Fáze 2 (listopad 2022) | Fáze 3 (vlna duben 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Žádná závislost na strukturovaném rozpisu prací (WBS) u projektů | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Strukturovaný rozpis prací v rámci aktuálně podporovaných limitů Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| Strukturovaný rozpis prací mimo aktuálně podporované limity Project Operations, včetně podpory pro aplikaci Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funkce procesu upgradu 

V rámci procesu upgradu jsme do mapy webu přidali protokoly upgradu, aby správci mohli snadněji diagnostikovat selhání. Kromě nového rozhraní budou přidána nová ověřovací pravidla, která zajistí integritu dat po upgradu. Do procesu upgradu budou přidána následující ověření.

| Ověření | Fáze 1 (leden 2022) | Fáze 2 (listopad 2022) | Fáze 3  |
|-------------|------------------------|---------------------------|---------------------------|
| Strukturovaný rozpis prací bude ověřen vůči běžným narušením integrity dat (například přiřazení zdrojů, které jsou spojeny se stejným nadřazeným úkolem, ale mají různé nadřazené projekty). | | :heavy_check_mark: | :heavy_check_mark: |
| Strukturovaný rozpis prací bude ověřen vůči [známým limitům aplikace Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| Strukturovaný rozpis prací bude ověřen vůči známým limitům aplikace Project Desktop Client. | |  | :heavy_check_mark: |
| Rezervovatelné zdroje a projektové kalendáře budou vyhodnoceny vůči běžným výjimkám nekompatibilních pravidel kalendáře. | | :heavy_check_mark: | :heavy_check_mark: |

Ve fázi 2 budou zákazníkům, kteří upgradují na Project Operations, upgradovány jejich stávající projekty na prostředí pouze ke čtení pro plánování projektů. V tomto prostředí určeném pouze ke čtení bude v mřížce sledování viditelný úplný strukturovaný rozpis prací. Pokud budou projektoví manažeři chtít upravit strukturovaný rozpis prací, mohou vybrat příkaz [**Převést**](/PSA-Upgrade-Project-Conversion.md) na hlavní stránce projektu. Proces na pozadí pak aktualizuje projekt tak, aby podporoval nové prostředí plánování projektu z aplikace Project for the Web. Tato fáze je vhodná pro zákazníky, kteří mají projekty, které vyhovují [známým limitům aplikace Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Ve fázi 3 bude přidána podpora pro aplikaci Project Desktop Client ve prospěch zákazníků, kteří chtějí nadále upravovat své projekty z této aplikace. Pokud jsou však existující projekty převedeny do nového prostředí Project for the Web, přístup k doplňku bude pro každý převedený projekt zakázán.

## <a name="prerequisites"></a>Předpoklady

Abyste byli způsobilí pro upgrade fáze 1, musíte splňovat následující kritéria:

- Cílové prostředí nesmí obsahovat žádné záznamy v entitě **msdyn_projecttask**.
- Všem aktivním uživatelům musejí být přiřazeny platné licence Project Operations. 
- Musíte ověřit proces upgradu alespoň v jednom neprovozním prostředí obsahujícím reprezentativní datovou sadu, která je v souladu s provozním prostředím.
- Cílové prostředí musí být aktualizováno na verzi Project Service Automation Update Release 37 (V3.10.58.120) nebo novější.

Abyste byli způsobilí pro upgrade fáze 2, musíte splňovat následující kritéria:

- Všem aktivním uživatelům musejí být přiřazeny platné licence Project Operations. 
- Musíte ověřit proces upgradu alespoň v jednom neprovozním prostředí obsahujícím reprezentativní datovou sadu, která je v souladu s provozním prostředím.
- Cílové prostředí musí být aktualizováno na verzi Project Service Automation Update Release 37 (V3.10.58.120) nebo novější.
- Prostředí obsahující úkoly (msdyn_projecttask) jsou podporována pouze v případě, že celkový počet úkolů na projekt je 500 nebo méně.

Předpoklady pro fázi 3 budou aktualizovány, jakmile se blíží datum obecné dostupnosti.

## <a name="licensing"></a>Licencování

Pokud máte aktivní licence Project Service Automation, můžete nainstalovat a používat aplikaci Project Operations, která zahrnuje všechny funkce Project Service Automation a další. Tímto způsobem můžete otestovat schopnosti Project Operations, zatímco budete pokračovat v produkčním používání Project Service Automation. Po vypršení platnosti licencí Project Service Automation budete muset přejít na Project Operations. Při plánování tohoto přechodu musíte počítat se skutečností, že licence Project Operations nezahrnuje licenci Project Service Automation. Zákazníci, kteří mají scénáře, kdy nasadili Project Service Automation a potřebují nadále používat nebo zvyšovat své licence pro PSA, zatímco plánují přejít na Project Operations, mohou požádat o dočasné licence PSA na základě zakoupených licencí Project Operations. Jedna licence Project Service Automation bude vydána pro jednu licenci Project Operations. O dočasné licence PSA lze požádat pomocí tohoto odkazu: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Testování a refaktorování přizpůsobení

Jako výchozí bod importujte všechna přizpůsobení do čistého prostředí Project Operations (Lite), abyste potvrdili, že import je úspěšný a že obchodní operace se chovají podle očekávání.

Dávejte si pozor na několik věcí:

- Import může selhat kvůli chybějícím závislostem. Jinými slovy, přizpůsobení se odkazují na pole nebo jiné součásti, které byly z Project Operations odstraněny. V takovém případě odeberte tyto závislosti z vývojového prostředí.
- Pokud vaše nespravovaná a spravovaná řešení obsahují součásti, které nejsou přizpůsobené, odeberte tyto součásti z řešení. Například když přizpůsobíte entitu **Projekt**, přidejte do svého řešení pouze hlavičku entity. Nepřidávejte všechna pole. Pokud jste předtím přidali všechny dílčí součásti, možná budete muset ručně vytvořit nové řešení a přidat do něj relevantní součásti.
- Formuláře a zobrazení se nemusí jevit jako očekávané. Za určitých okolností, pokud jste přizpůsobili některý z předem připravených formulářů nebo zobrazení, mohou přizpůsobení zabránit novým aktualizacím v Project Operations. Chcete-li tyto problémy identifikovat, doporučujeme provést souběžnou kontrolu čisté instalace Project Operations a instalace Project Operations, která zahrnuje vaše přizpůsobení. Porovnejte nejčastěji používané formuláře ve vaší firmě, abyste se ujistili, že vaše verze formuláře stále dává smysl a nechybí jí něco z čisté verze formuláře. Proveďte stejný typ souběžné kontroly u všech zobrazení, která jste si přizpůsobili.
- Obchodní logika může za běhu selhat. Protože odkazy na pole ve vašich modulech plug-in nejsou v době importu ověřeny, obchodní logika může selhat kvůli odkazům na pole, která již neexistují, a můžete obdržet chybovou zprávu, vypadající jako následující příklad: "Entita 'Project' neobsahuje atribut s Name = 'msdyn_plannedhours' a NameMapping = 'Logical'." V takovém případě upravte svá přizpůsobení tak, aby používala nová pole. Pokud v logice modulu plug-in používáte automaticky generované třídy proxy a odkazy na silné typy, zvažte opětovné vytvoření těchto proxy z čisté instalace. Tímto způsobem můžete snadno identifikovat všechna místa, kde vaše moduly plug-in závisejí na zastaralých polích.

Po aktualizaci vašich přizpůsobení tak, aby čistě importovaly údaje z Project Operations, přejděte k dalším krokům.

## <a name="end-to-end-testing-in-development-environments"></a>Komplexní testování ve vývojových prostředích

### <a name="initiate-upgrade"></a>Spusťte upgrade 

1. V centru pro správu Power Platform vyhledejte a vyberte prostředí. Poté v aplikacích vyhledejte a vyberte **Dynamics 365 Project Operations**.
2. Výběrem možnosti **Instalovat** spusťte upgrade. Centrum pro správu Power Platform označí tuto instalaci jako novou. Bude však zjištěna přítomnost dřívější verze Project Service Automation a stávající instalace bude upgradována.

    Po dokončení upgradu by mělo prostředí ukazovat, že je nainstalován Project Operations a že není nainstalován Project Service Automation.

    V závislosti na množství dat v prostředí může upgrade trvat několik hodin. Základní tým, který spravuje upgrade, by ho měl podle toho plánovat a provádět mimo pracovní dobu. V některých případech, pokud je objem dat velký, by měl být upgrade spuštěn přes víkend. Rozhodnutí o plánování by mělo být založeno na výsledcích testování v nižších prostředích.

3. Podle potřeby upgradujte vlastní řešení. V tomto okamžiku nasaďte všechny změny, které jste provedli ve svých přizpůsobeních v sekci [Testování a refaktorování přizpůsobení](#testing-and-refactoring-customizations) tohoto článku.
4. Jděte na stránku **make.powerapps.com**, vyberte své prostředí z rozevíracího seznamu v pravém horním rohu portálu, vyberte **Řešení** z nabídky vlevo, vyberte řešení **Zastaralé součásti Project Operations** a **Odinstalovat**.

    Toto řešení je dočasné řešení, které uchovává stávající datový model a součásti, které jsou přítomny během upgradu. Odebráním tohoto řešení odeberete všechna pole a součásti, které se již nepoužívají. Tímto způsobem zjednodušíte rozhraní a usnadníte integraci a rozšíření.
    
### <a name="upgrade-to-project-operations-lite"></a>Upgrade na Project Operations Lite

Následující kroky popisují proces upgradu a související protokolování chyb:

1. **Kontrola verze PSA:** Chcete-li nainstalovat Project Operations, musíte mít verzi V3.10.58.120 nebo vyšší.
1. **Předběžné ověření:** Když správce zahájí upgrade, systém spustí operaci předběžného ověření u každé entity, která je jádrem řešení Project Operations. Tento krok ověří, že jsou všechny odkazy na entity platné, a zajistí, že data související s WBS jsou v rámci publikovaných omezení Project for the Web.
1. **Upgrade metadat:** Po úspěšném předběžném ověření systém zahájí změny schématu a vytvoří řešení zastaralých komponent. Toto zastaralé řešení můžete odebrat poté, co dokončíte všechny požadované úpravy vlastních nastavení. Tento krok je nejdelší částí procesu upgradu a jeho dokončení může trvat až čtyři hodiny.
1. **Upgrade dat:** Po dokončení všech požadovaných změn schématu v kroku upgradu metadat se vaše data migrují do nového schématu a provedou se všechna požadovaná výchozí nastavení a přepočet.
1. **Aktualizace modulu harmonogramu projektu:** Po úspěšném upgradu dat se karta **Plán** na hlavní stránce přejmenuje na **Úkoly**. Když uživatel po upgradu vybere tuto kartu, bude přesměrován na sledovací mřížku, kde je zobrazena verze WBS pouze pro čtení. Chce-li upravit WBS, musí spustit plán [zpracování převodu](/PSA-Upgrade-Project-Conversion.md). Všechny projekty bez předem existujícího WBS mohou používat nové prostředí plánování přímo bez převodu.
 
### <a name="validate-common-scenarios"></a>Ověřte běžné scénáře

Když ověřujete svá konkrétní přizpůsobení, doporučujeme vám také zkontrolovat obchodní procesy, které jsou podporovány napříč aplikacemi. Tyto obchodní procesy zahrnují, ale nejsou omezeny na vytváření prodejních subjektů, jako jsou nabídky a smlouvy, a vytváření projektů, které zahrnují WBS a schvalování skutečností.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Hlavní změny mezi Project Service Automation a Project Operations

Tato sekce obsahuje souhrn hlavních změn, které můžete očekávat při přechodu mezi Project Service Automation a Project Operations.

### <a name="project-planning"></a>Plánování projektu

Možnosti plánování projektu v Project Operations se již nespoléhají na kombinaci logiky na straně klienta a logiky na straně serveru. Namísto toho používá Project Operations jako svůj primární plánovací modul aplikaci Project for the Web. Tato změna ve schopnostech plánování aktivuje několik nových funkcí, jako jsou plánovací vývěska a Ganttova zobrazení, plánování řízené zdroji, [položky kontrolního seznamu úkolu](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) a režimy plánování projektů. Nové schopnosti plánování jsou také podporovány bohatou sadou nových [rozhraní pro programování aplikací (API)](../project-management/schedule-api-preview.md). Tato rozhraní API mají pomoci zajistit, aby žádná programová operace pro vytváření, aktualizaci nebo odstraňování entity ve WBS nepoškodila vypočítaná pole v plánu.

### <a name="billing-and-pricing"></a>Fakturace a ceny

V rámci pokračujících investic do Project Operations je k dispozici několik nových funkcí v oblasti fakturace a stanovení cen. Zde je uvedeno několik příkladů:

- [Záznam využití materiálu na projektech a projektových úkolech](../material/material-usage-log.md)
- [Řízení subdodávek](../pro/subcontracting/managing-subcontracts-overview.md)
- [Zálohy a smlouvy na základě záloh](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Nepřekročitelné stavy smlouvy a ověření](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Fakturace na základě úkolů

### <a name="resource-management"></a>Řízení zdrojů

Project Operations poskytuje volitelnou podporu plánovací vývěsky Universal Resource Scheduling (URS) a pomocníka plánování. Toto nové prostředí bude povinné ve vlně v dubnu 2023.

## <a name="frequently-asked-questions"></a>Nejčastější dotazy

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Které typy nasazení jsou aktuálně podporovány u upgradu?

| Source                                                 | Cíl                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Nasazení Project Operations Lite                        | Podporováno               |
| Řízení projektů a účetnictví v Dynamics 365 Finance | Nasazení Project Operations Lite                        | V současnosti není podporováno |
| Finance pro řízení projektů a účetnictví              | Project Operations pro scénáře se zdroji bez skladových materiálů     | V současnosti není podporováno |
| Project Service Automation 3.x                         | Project Operations pro scénáře se zdroji bez skladových materiálů     | V současnosti není podporováno |
| Project for the web (vyhrazené prostředí)            | Nasazení Project Operations Lite                        | V současnosti není podporováno |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Jak mohu nainstalovat Project Operations předtím, než budou k dispozici nástroje pro upgrade?

Existují dvě možnosti instalace Project Operations před tím, než budou k dispozici nástroje pro upgrade:

- Zřízení nového prostředí.
- Nasaďte Project Operations samostatně v jakékoli prodejní organizaci, kde není k dispozici Project Service Automation.

Pokud je aplikace Project Service Automation nainstalována v organizaci, ale nebyla použita, lze ji odinstalovat. Po úplném odebrání Project Service Automation lze Project Operations nainstalovat do stejné organizace.
