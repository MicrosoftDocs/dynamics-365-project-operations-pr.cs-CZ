---
title: Přehled prodejních procesů
description: Toto téma poskytuje informace o základních prodejních procesech.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app: ''
ms.openlocfilehash: c70760748c5faa87f6738ab7e2ab593e2df49e41
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073979"
---
# <a name="sales-processes-overview"></a>Přehled prodejních procesů

Prodejní procesy používané v organizaci založené na projektech se liší od prodejních procesů používaných v organizaci založené na produktech. K tomuto rozdílu dochází proto, že prodejní cykly pro organizace založené na projektech jsou delší a vyžadují pro analýzu a vytváření nabídek pro jednotlivé obchody přizpůsobené techniky odhadu. Dynamics 365 Project Operations používá některé z následujících funkcí, které se používají v prodejním procesu:

- Záznam zájemce slouží ke sledování prodejního procesu.
- Zařazování zájemců je sledováno jako příležitosti.
- K dispozici jsou všechny související artefakty pro příležitost. Mezi tyto artefakty patří prodejní tým, účastníci, pravděpodobnost, hodnocení, fáze prodeje a obchodní procesy.
- Pro příležitost je vytvořeno více nabídek.
- Nabídce je přiřazen stav **Uzavřena jako získaná** pro vytvoření prodejní objednávky. V Project Operations je prodejní objednávka přizpůsobena a nazývá se projektová smlouva.

## <a name="estimate-a-sale"></a>Odhad prodeje
Hodnotu prodeje lze odhadnout na základě dříve dodaných projektů a složitosti projektů. U projektů, které zahrnují rozšíření do předchozích projektů, nebo projektů, u kterých je odbornost dodavatele vysoká a jsou používány dobře známé šablony práce, můžete použít jednodušší proces odhadu. Složitější projekty obvykle mají delší proces nákupu. Proto je v procesu odhadu prodeje více fází. Na začátku procesu používá prodejní tým k vytváření odhadu na vysoké úrovni pro každou jednotlivou komponentu práce, která je nabízena, vstup manažerů zákaznických účtů a odborníků na konkrétní problematiku (SMEs). Tyto komponenty práce jsou reprezentovány řádky nabídky. 

Můžete vytvořit odhad nabídky na vysoké úrovni. Nakonec bude tento odhad na vysoké úrovni nahrazen detailnějším odhadem založeným na projektovém plánu, který vytvoříte pomocí standardizovaných projektových šablon. Tyto šablony vám pomohou vytvořit plán a určit peněžní hodnoty v nabídce a jejích komponentách (řádcích nabídek). 

Můžete vytvořit více nabídek pro projekt a seskupit je pod jedním záznamem příležitosti. Nakonec je jedna z nabídek označena jako **Uzavřena jako získaná** a je vytvořena projektová smlouva nebo popis práce (SOW). Projektová smlouva obsahuje nasmlouvanou hodnotu pro každou komponentu (řádek smlouvy), kterou zákazník přijme k dodání. Popis práce je obvykle vytvořen jako dokument aplikace Microsoft Word. Všechny faktury, které jsou odeslány zákazníkovi v průběhu dodávky projektu, odkazují na projektovou smlouvu nebo popis práce.

Pod jedním záznamem příležitosti můžete také vytvořit alternativní nabídky nebo nastavit systém tak, aby se při získání nabídky vytvořila projektová smlouva. V tomto případě můžete k záznamu projektové smlouvy připojit dokument aplikace Word, který představuje popis práce.

## <a name="configure-the-sales-process"></a>Konfigurace prodejního procesu
Můžete použít toky obchodních procesů pro konfiguraci vašeho prodejního procesu. Tyto toky poskytují asistované vizuální rozhraní, které posouvá obchody vpřed fázemi prodejního procesu.

Vaše společnost může mít například v prodejním procesu následujících šest fází:

1. Zařadit
2. Odhad
3. Interní revize
4. Smlouva
5. Dodat
6. Uzavřeno
 
Vaše organizace může v průběhu vývoje používat k reprezentaci stejného obchodu různé entity. Počátkem prodejního procesu je obchod reprezentován entitou Příležitost. Jak plyne čas a objeví se další podrobnosti, můžete k vytvoření jedné nebo více nabídek použít odhady na vysoké úrovni. Pokud je jedna z těchto nabídek zkontrolována interními a zákaznickými zúčastněnými stranami, představuje entita Nabídka obchod. Poté, co zákazník nabídku přijme, představuje projektová smlouva nebo SOW obchod. Pro podporu tohoto chování jsou toky obchodních procesů strukturovány tak, aby každá fáze procesu byla propojena s jinou databázovou tabulkou.

Fázi **Zařadit** lze v prodejním procesu podpořit pomocí entity Příležitost. Fáze **Odhad** a **Interní revize** lze podpořit pomocí entity Nabídka. Fáze **Smlouva** , **Dodávka** a **Uzavření** lze podpořit pomocí entity Projektová smlouva.

Při přesouvání obchodů napříč fázemi se zobrazí výzva k vytvoření příslušného záznamu entity, který vám pomůže a provede vás procesem. Fáze mohou být podmíněné. Pokud například požadujete interní revizi nabídky pouze v případě, že nabídka používá vlastní ceník, můžete tuto podmínku nakonfigurovat v příslušné fázi obchodního procesu. Fáze **Interní revize** se pak zobrazí pouze pro nabídky, které používají vlastní ceník. U všech ostatních obchodů a nabídek následuje po fázi **Odhad** fáze **Smlouva**.

> [!NOTE]
> Project Operations má konkrétní stránky pro záznamy entit Příležitost, Nabídka, Objednávka a Faktura. Tyto záznamy musíte vytvořit pomocí informačních stránek projektu pro tyto entity. Jinak nebudete moci otevřít záznamy ze stránky **Informace o projektu**. Pokud chcete otevřít záznam ze stránky **Informace o projektu** , musíte záznam odstranit a znovu ho vytvořit pomocí stránky **Informace o projektu** , kde obchodní logika pro každý z těchto typů entit zajišťuje, že pole **Typ** záznamu je nastaveno správně a všechny povinné koncepty jsou správně inicializovány.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Sledování revizí nabídek a projektových plánů v prodejním cyklu
V Project Operations nelze sledovat revize provedené v nabídce. Místo toho musíte označit existující nabídku jako **Uzavřenou jako ztracenou** a pak vytvořit novou nabídku. Můžete kopírovat nabídku nebo klonovat nabídku založenou na projektu.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Sledování komentářů a schvalování nabídek a projektových smluv
Revizi a schvalování nabídek a projektových smluv můžete spravovat pomocí zdi záznamu a příspěvků. Vaše organizace může vytvořit vlastní pracovní postupy a moduly plug-in pro přiřazení, přesměrování, eskalaci a správu upozornění na revize a schválení pracovních položek.
