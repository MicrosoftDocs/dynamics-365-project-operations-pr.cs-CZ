---
title: Prodejní procesy
description: Toto téma poskytuje informace o základních prodejních procesech.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 2561a54af6bdb9764a318f012fdc53f7b3298893
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145170"
---
# <a name="sales-processes"></a>Prodejní procesy

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Prodejní procesy používané v organizaci založené na projektech se liší od prodejních procesů používaných v organizaci založené na produktech. K tomuto rozdílu dochází proto, že prodejní cykly pro organizace založené na projektech jsou delší a vyžadují pro analýzu a vytváření nabídek pro jednotlivé obchody přizpůsobené techniky odhadu. Dynamics 365 Project Service Automation používá některé ze stejných funkcí, které se používají v prodejním procesu pro Dynamics 365 Sales. Zde je uvedeno několik příkladů:

- Entita Zájemce slouží ke sledování prodejního procesu.
- Zařazování zájemců je sledováno jako příležitosti. Prodejní proces může také začínat příležitostí.
- K dispozici jsou všechny související artefakty pro příležitost. Mezi tyto artefakty patří prodejní tým, účastníci, pravděpodobnost, hodnocení, fáze prodeje a obchodní procesy.
- Pro příležitost je vytvořeno více nabídek.
- Poptávka je pro vytvoření prodejní objednávky označena jako **Uzavřena jako získaná**. V PSA je prodejní objednávka přizpůsobena a nazývá se projektová smlouva.

Následující ilustrace znázorňuje typický prodejní proces v organizaci založené na projektech.

> ![Prodejní proces v organizaci založené na projektech](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Odhad prodeje
Hodnotu prodeje lze odhadnout na základě dříve dodaných projektů a složitosti projektů. U projektů, které zahrnují rozšíření do předchozích projektů, nebo projektů, u kterých je odbornost dodavatele vysoká a jsou používány dobře známé šablony práce, můžete použít jednodušší proces odhadu. Složitější projekty obvykle mají delší proces nákupu. Proto je v procesu odhadu prodeje více fází. Na začátku procesu používá prodejní tým k zahájení vytváření odhadu na vysoké úrovni pro každou jednotlivou komponentu práce, která je nabízena, vstup manažerů zákaznických účtů a odborníků na konkrétní problematiku (SMEs). Tyto komponenty práce jsou reprezentovány řádky nabídky. 

Můžete vytvořit odhad nabídky na vysoké úrovni. Nakonec bude tento odhad na vysoké úrovni nahrazen detailnějším odhadem založeným na projektovém plánu, který vytvoříte pomocí standardizovaných projektových šablon. Tyto šablony vám pomohou vytvořit plán a určit peněžní hodnoty v nabídce a jejích komponentách (řádcích nabídek). 

Můžete vytvořit více nabídek pro projekt a seskupit je pod jedním typem entity příležitosti. Nakonec je jedna z těchto nabídek označena jako **Uzavřena jako získaná** a je vytvořena projektová smlouva nebo popis práce (SOW). Projektová smlouva obsahuje nasmlouvanou hodnotu pro každou komponentu (řádek smlouvy), kterou zákazník přijme k dodání. Popis práce je obvykle vytvořen jako dokument aplikace Microsoft Word. Všechny faktury, které jsou odeslány zákazníkovi v průběhu dodávky projektu, odkazují na projektovou smlouvu nebo popis práce.

Pod jedním typem entity příležitosti můžete také vytvořit alternativní nabídky nebo nastavit systém tak, aby se při získání nabídky vytvořila projektová smlouva. V tomto případě můžete k záznamu projektové smlouvy připojit dokument aplikace Word, který představuje popis práce.

![Uzavření nabídky za účelem vytvoření projektové smlouvy](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Konfigurace prodejního procesu
V Microsoft Dynamics 365 můžete použít toky obchodních procesů (BPFs) pro konfiguraci vašeho prodejního procesu. BPFs poskytuje vašim prodejcům vizuální rozhraní s průvodcem, které mohou použít k přesunu obchodů v rámci fází, které jsou pro vaši firmu typické.

Vaše společnost může mít například v prodejním procesu následujících šest fází:

1. Zařadit
2. Odhad
3. Interní revize
4. Contract
5. Dodat
6. Close (Zavřít)

Těchto šest fází je reprezentováno dvojitými šipkami (\>), které vyberete pro rozbalení v každém typu entity příležitosti, který vytvoříte.

![Konfigurace obchodního procesu v Dynamics 365](media/basic-guide-3.png)
 
Vaše organizace může v průběhu vývoje používat k reprezentaci stejného obchodu různé entity. Počátkem prodejního procesu je obchod reprezentován entitou Příležitost. Jak plyne čas a objeví se další podrobnosti, můžete k vytvoření jedné nebo více nabídek použít odhady na vysoké úrovni. Pokud je jedna z těchto nabídek zkontrolována interními a zákaznickými zúčastněnými stranami, představuje entita Nabídka obchod. Poté, co zákazník nabídku přijme, představuje projektová smlouva nebo SOW obchod. Pro podporu tohoto chování jsou toky obchodních procesů strukturovány tak, aby každá fáze procesu byla propojena s jinou databázovou tabulkou.

Fázi **Zařadit** lze v prodejním procesu podpořit pomocí entity Příležitost. Fáze **Odhad** a **Interní revize** lze podpořit pomocí entity Nabídka. Fáze **Smlouva**, **Dodávka** a **Uzavření** lze podpořit pomocí entity Projektová smlouva.

Při přesouvání obchodů napříč fázemi se zobrazí výzva k vytvoření příslušného záznamu entity, který vám pomůže a provede vás procesem. Fáze mohou být podmíněné. Pokud například požadujete interní revizi nabídky pouze v případě, že nabídka používá vlastní ceník, můžete tuto podmínku nakonfigurovat v příslušné fázi obchodního procesu. Fáze **Interní revize** se pak zobrazí pouze pro nabídky, které používají vlastní ceník. U všech ostatních obchodů a nabídek následuje po fázi **Odhad** fáze **Smlouva**.

> [!NOTE]
> PSA obsahuje pro entity Příležitost, Nabídka, Objednávka a Faktura specifické stránky. Pro tyto entity musíte pomocí stránek informací o projektu vytvořit příležitosti, nabídky, objednávky a faktury služby Project Service. Pokud k vytvoření záznamu použijete jinou stránku, nebudete tento záznam moci otevřít ze stránky **Informace o projektu**. Chcete-li otevřít záznam ze stránky **Informace o projektu**, je nutné záznam odstranit a znovu jej vytvořit pomocí stránky **Informacemi o projektu**. Obchodní logika na stránce **Informace o projektu** pro každý z těchto typů entit zaručuje, že pole **Typ** záznamu je správně nastaveno, a že jsou správně inicializovány všechny povinné koncepty.

> ![Informace o projektu pro novou objednávku](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Rozdíly mezi Project Service Automation a Sales
Ačkoli prodejní proces v PSA používá základní funkce prodejního procesu v Sales, obsahuje kvůli variantám v obchodních praktikách organizací založených na projektech několik klíčových rozdílů. Zde je uvedeno několik příkladů:

- **Projektové nabídky** – v Project Service Automation je nabídka uzavřena po vytvoření projektové smlouvy z nabídky. V prodeji můžete nechat nabídku otevřenou poté, co jste ji vyhráli. Důvodem tohoto rozdílu je, že shoda mezi nabídkou a projektovou smlouvou je lepší pro organizace založené na projektech. 
- **Aktivace a revize** – v PSA nejsou aktivace a revize podporovány pro nabídky projektů. V prodeji může být nabídka uzamčena, aby se zabránilo dalším úpravám.
- **Uzavření nabídky jako ztracené nebo získané** – v případě, že je v PSA projektová nabídka uzavřena jako získaná nebo ztracená, zůstane příležitost otevřená. Všechny ostatní nabídky příležitosti jsou uzavřeny jako ztracené. Pokud je nabídka v Prodeji uzavřena jako získaná nebo ztracená, je uživatel vyzván k provedení akce v příležitosti. V závislosti na vstupu uživatele může být zdrojová příležitost zavřena nebo ponechána otevřená.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Sledování revizí nabídek a projektových plánů v prodejním cyklu
V PSA nelze sledovat revize provedené v nabídce. Místo toho musíte označit existující nabídku jako **Uzavřenou jako ztracenou** a pak vytvořit novou nabídku. Pomocí PSA můžete kopírovat nabídku nebo klonovat nabídku založenou na projektu.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Sledování komentářů a schvalování nabídek a projektových smluv
Revizi a schvalování nabídek a projektových smluv můžete spravovat pomocí zdi záznamu a příspěvků. Vaše organizace může vytvořit vlastní pracovní postupy a moduly plug-in pro přiřazení, přesměrování, eskalaci a správu upozornění na pracovní položky revize a schválení.
