---
title: Jak přizpůsobit tok obchodního procesu týkající se fází projektu?
description: Přehled přizpůsobení toku obchodního procesu týkajícího se fází projektu.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7efbb19161878e13a1b0d33bc1bc4e06521445c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596962"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Jak přizpůsobit tok obchodního procesu týkající se fází projektu?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Existuje známé omezení v dřívějších verzích aplikace Project Service spočívající v tom, že názvy fází v toku obchodního procesu týkajícího se fází projektu musí přesně odpovídat očekávaným anglickým názvům (**Quote**, **Plan**, **Close**). V opačném případě obchodní logika, která závisí na anglických názvech fází, nefunguje podle očekávání. Proto nevidíte známé akce, jako je **Přepnout proces** nebo **Upravit proces** dostupné ve formuláři projektu, a přizpůsobení toku obchodního procesu není doporučeno. 

Toto omezení bylo adresováno ve verzi 2.4.5.48 a vyšší. Tento článek obsahuje zástupná řešení, pokud potřebujete přizpůsobit výchozí tok obchodního procesu pro starší verze.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Obchodní logika vyžaduje přesnou shodu s anglickými názvy fází

Tok obchodního procesu týkající se fází projektu zahrnuje obchodní logiku, která řídí následující chování v aplikaci:
- Když je přiřazen projekt k nabídce, kód nastaví tok obchodního procesu do fáze **Quote**.
- Když je přiřazen projekt ke smlouvě, kód nastaví tok obchodního procesu do fáze **Plan**.
- Když se tok obchodního procesu posune do fáze **Close**, záznam projektu je deaktivovaný. Když je projekt deaktivován, formulář projektu a strukturovaný rozpis prací jsou nastaveny pouze na čtení, rezervace pojmenovaných zdrojů se uvolní a všechny přidružené ceníky se deaktivují.

Tato obchodní logika spoléhá na anglické názvy fází projektu. Tato závislost na anglických názvech fází je hlavním důvodem, proč není doporučeno přizpůsobení toku obchodního procesu týkajícího se fází projektu, stejně jako příčinou, proč nevidíte běžné akce toku obchodního procesu, jako je **Přepnout proces** nebo **Upravit proces** na entitě projektu.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Co se stane, pokud se neshodují názvy fáze s anglickými názvy?

V aplikaci Project Service verze 1.x na platformě 8.2, když názvy fáze v procesu obchodního toku neodpovídají přesně anglickým názvům fází, obchodní logika, která nastavuje správnou fázi pro nabídky nebo smlouvy, nebo která uzavírá projekt, bude vynechána. Nejsou zobrazeny žádné chybové zprávy. Proto se zobrazí, že jste schopni přizpůsobit tok obchodního procesu týkajícího se fází projektu. Neuvidíte ale žádné automatické procesy fungující pro nabídky, smlouvy a uzavření projektu.

V aplikaci Project Service verze 2.4.4.30 nebo dřívější na platformě 9.0 došlo k významné změně architektury toků obchodních procesů, což vyžaduje přepsání obchodní logiky toku obchodního procesu. Důsledkem je, že pokud se názvy fází procesu neshodují s očekávanými anglickými názvy, zobrazí se chybová zpráva. 

Proto, pokud chcete přizpůsobit tok obchodního procesu týkajícího se fází projektu pro entitu projektu, můžete přidat pouze zcela nové fáze k výchozímu toku obchodního procesu pro entitu projektu, zatímco fáze **Quote**, **Plan** a **Close** zůstanou beze změny. Toto omezení zajišťuje, že neobdržíte chyby z obchodní logiky, která očekává anglické názvy fází v toku obchodního procesu.

Ve verzi 2.4.5.48 nebo novější byla obchodní logika popsaná v tomto článku odebrána z výchozího toku obchodního procesu pro entitu projektu. Upgrade na tuto verzi nebo novější vám umožní přizpůsobit nebo nahradit výchozí tok obchodního procesu jedním ze svých vlastních. 

## <a name="workarounds-for-earlier-versions"></a>Zástupná řešení pro starší verze

Pokud upgrade není možností, můžete přizpůsobit tok obchodního procesu týkajícího se fází projektu pro entitu projektu pomocí jednoho z těchto dvou způsobů:

1. Přidejte další fáze k výchozí konfiguraci při současném zachování anglických názvů fází pro možnosti **Quote**, **Plan** a **Close**.


![Snímek obrazovky přidání fází k výchozí konfiguraci.](media/FAQ-Customize-BPF-1.png)
 
2. Vytvořte svůj vlastní tok obchodního procesu a učiňte ho primárním tokem obchodního procesu pro entitu projektu, který umožňuje mít názvy fáze, které chcete. Pokud však chcete použít stejné standardní fáze projektu **Quote**, **Plan** a **Close**, je nutné provést některá přizpůsobení, která jsou vyvozena z vašich vlastních názvů fází. Složitější logika je v uzavření projektu, kterou můžete stále spustit pouze deaktivací záznamu projektu.

![Vlastní nastavení BPF.](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Další skutečnosti ke zvážení pro aplikaci Project Service verze 2.4.4.30 nebo starší na platformě 9.0

V aplikaci Project Service verze 2.4.4.30 nebo starší na platformě 9.0 s vlastním tokem obchodního procesu, se pole **Název fáze** na entitě projektu použité v grafu **Projektu podle fáze** a zobrazeních seznamů projektu nebude aktualizovat, protože je kombinované s výchozím tokem obchodního procesu týkajícího se fází projektu. Můžete vyřešit tento problém pomocí následujících kroků:

- Přidejte vlastní pole pro zachycení aktuální fáze toku obchodního procesu, která se aktualizuje, jakmile uživatel přejde přes vlastní tok obchodního procesu.

- Upravte graf **Projekt podle fáze** tak, aby pracoval s vaším vlastním polem, namísto s výchozí konfigurací.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Kroky k vytvoření vlastního toku obchodního procesu pro entitu projektu

K vytvoření vlastního toku obchodního procesu pro entitu projektu proveďte následující:

1. Přejděte na **Nastavení** > **Centrum zpracování**. Nekopírujte tok obchodního procesu týkajícího se fází projektu, protože ten rovněž kopíruje obchodní logiku aplikace Project Service.

  ![Vytvořit proces.](media/FAQ-Customize-BPF-3.png)

2. Pomocí návrháře procesu vytvořte názvy fází, které chcete. Chcete-li stejnou funkci jako výchozí fáze pro **Quote**, **Plan** a **Close**, budete ji muset vytvořit na základě vlastních názvů fází toku obchodního procesu.

   ![Snímek obrazovky návrháře procesu použitého k přizpůsobení BPF.](media/FAQ-Customize-BPF-4.png) 

3. V návrháři procesu klikněte na **Seřadit tok procesu** a učiňte vlastní tok obchodního procesu primárním tokem obchodního procesu pro entitu projektu přesunutím nad tok obchodního procesu týkajícího se fází projektu do horní části seznamu.


   [Snímek obrazovky použití možnosti Seřadit tok procesu](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Následující kroky platí pro aplikaci Project Service verze 2.4.4.30 nebo starší na platformě 9.0

4. Přidejte nové vlastní pole k entitě projektu pro zachycení vlastních fází ve svém vlastním toku obchodního procesu. Budete muset přidat obchodní logiku (modul plug-in/workflow) pro aktualizaci tohoto, když je fáze na vlastním toku obchodního procesu aktualizována.

   ![Snímek obrazovky přizpůsobení entity projektu.](media/FAQ-Customize-BPF-6-720.png)

5. Upravte graf **Projekt podle fáze** pro použití vašeho nového vlastního pole pro fáze.

   ![Snímek obrazovky použití grafu Projekt podle fáze.](media/FAQ-Customize-BPF-7-720.png)

6. Upravte jakékoliv zobrazení pro entitu projektu, aby zahrnovalo vaše nové vlastní pole pro fáze.

   ![Snímek obrazovky úprav zobrazení na entitě projektu.](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
