---
title: Odhady
description: Toto téma poskytuje informace o odhadech v Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 978af25fb89feb61e3c6fcfeafa212db034ff5cb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590660"
---
# <a name="estimates"></a>Odhady

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U nabídky založené na projektu můžete pomocí entity Podrobnosti řádku nabídky odhadnout práci, která je požadována pro dodání projektu. Tento odhad pak můžete sdílet se zákazníkem.

Řádky nabídky založené na projektu nebudou muset obsahovat žádné podrobnosti řádku nabídky. Alternativně mohou obsahovat mnoho podrobností řádku nabídky. Podrobnosti řádku nabídky se používají k odhadu času, výdajů nebo poplatků. PSA neumožňuje u podrobností řádku nabídky materiálové odhady. Ty se nazývají třídy transakcí. Odhadované částky daně lze zadat také do třídy transakcí.

Kromě tříd transakcí, obsahují podrobnosti řádku nabídky mají typ transakce. PSA podporuje dva typy transakcí pro podrobnosti řádku nabídky: **Náklady** a **Projektová smlouva**.

## <a name="estimate-by-using-a-contract"></a>Odhad pomocí smlouvy

Pokud jste při vytváření smlouvy založené na projektu použili nabídku PSA, bude odhad, který jste udělali pro každý řádek nabídky v nabídce, zkopírován do projektové smlouvy. Struktura projektové smlouvy se podobá struktuře projektové nabídky, která obsahuje řádky, podrobnosti řádků a rozpisy faktur.

Odhady lze provádět přímo v projektové smlouvě, jako v projektové nabídce. U projektové nabídky se odhad provádí pomocí řádků smlouvy a podrobností řádku smlouvy. Podrobnosti řádku smlouvy lze také vygenerovat z projektového plánu, který byl vytvořen pomocí metody odhadu zdola nahoru.

Podrobnosti řádku smlouvy lze použít k odhadu času, výdajů nebo poplatků. Odhadované částky daně lze zadat také do podrobností řádku smlouvy.

PSA neumožňuje u podrobností řádku smlouvy materiálové odhady.

Procesy, které jsou podporovány ve smlouvě o projektu, jsou vytvoření a potvrzení faktury. Vytvoření faktury vytvoří koncept faktury založené na projektu, který zahrnuje všechny skutečné hodnoty nefakturovaného prodeje do aktuálního data.

Po potvrzení je smlouva jen pro čtení a její stav se změní z **Koncept** na **Potvrzeno**. Jakmile tuto akci provedete, nelze ji vrátit zpět. Vzhledem k tomu, že tato akce je trvalá, je vhodné udržovat smlouvu ve stavu **Koncept**.

Jedinými rozdíly mezi koncepty smluv a potvrzenými smlouvami je jejich stav a skutečnost, že koncept smluv lze upravit, zatímco potvrzené smlouvy nelze. Vytváření faktur a sledování skutečných hodnot lze provádět u konceptů smluv i u potvrzených smluv.

PSA nepodporuje u smluv nebo projektů změnové příkazy.

## <a name="estimating-projects"></a>Odhady projektů

Můžete odhadnout čas a výdaje na projekty. PSA neumožňuje odhady materiálů nebo poplatků na projekty.

Odhady času se generují při vytvoření úkolu a určení atributů obecného zdroje, který je vyžadován k provedení úkolu. Odhady času jsou generovány z plánování úkolů. Odhady času nejsou vytvářeny, pokud vytváříte obecné členy týmu mimo kontext plánu.

Odhady výdajů se zapisují do mřížky na stránce **Odhady**.

## <a name="understanding-estimation"></a>Princip odhadování

Následující tabulku použijte jako vodítko pro pochopení obchodní logiky ve fázi odhadu.

| Situace                                                                                                                                                                                                                                                                                                                                          | Záznam entity                                                                                                                                                                                                       | Typ transakce | Třída transakce | Další informace                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Potřebujete-li odhadnout prodejní hodnotu času v nabídce                                                                                                                                                                                                                                                                                    | Je vytvořen záznam Podrobnosti řádku nabídky (PŘN).                                                                                                                                                                               | Projektová smlouva | Time        | Pole Původ transakce na řádku PŘN strany prodeje odkazuje na PŘN strany nákladů |
|                                                                                                                                                                                                                                                                                     | Systém vytvoří druhý záznam PŘN, který bude uchovávat odpovídající hodnoty nákladů. Systém zkopíruje všechna nepeněžní pole z PŘN prodeje do PŘN nákladů.                                                                                                                                                                               | Náklady | Time        | Pole Původ transakce na řádku PŘN strany prodeje odkazuje na PŘN strany nákladů |
| Potřebujete-li odhadnout prodejní hodnotu času ve smlouvě                                                                                                                                                                                                                                                                                 | Je vytvořen záznam Podrobnosti řádku projektové smlouvy (PŘS).                                                                                                                                                                    | Projektová smlouva | Time        | Pole Původ transakce na řádku PŘS strany prodeje odkazuje na PŘS nákladů      |
|                                                                                                                                                                                                                                                                                  | Systém vytvoří druhý záznam PŘS, který bude uchovávat odpovídající hodnoty nákladů. Systém zkopíruje všechna nepeněžní pole z PŘS prodeje do PŘS nákladů.                                                                                                                                                                    | Náklady | Time        | Pole Původ transakce na řádku PŘS strany prodeje odkazuje na PŘS nákladů      |
| Pokud uživatel popisuje zdroj v úkolu projektu                                                                                                                                                                                                                                                                                            | Záznam řádku odhadu pro zobrazení hodnoty prodeje úkolu je vytvořen při vytvoření úkolu se všemi požadovanými cenovými dimenzemi. Role a organizační jednotky jsou předdefinovanými cenovými dimenzemi Project Service | Projektová smlouva | Time        |                                                                                   |
|     | Záznam řádku odhadu pro zobrazení hodnoty nákladů úkolu je vytvořen při vytvoření úkolu se všemi požadovanými cenovými dimenzemi. Systém zkopíruje všechna nepeněžní pole z řádku odhadu prodeje do řádku odhadu nákladů. Role a organizační jednotka jsou předdefinovanými cenovými dimenzemi PSA pro nákladové a fakturační sazby.                                                                                                                                                                                                                | Náklady             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Přizpůsobení entit Podrobnosti řádku nabídky a Podrobnosti řádku smlouvy

Pokud jste na řádku podrobností nabídky přidali vlastní pole a chcete, aby systém zadal hodnotu pole jako výchozí hodnotu na souvisejícím řádku nákladů, který vytvoří, použijte nástroje pro registraci modulů plug-in PreOperationContractLineDetailUpdate a PreOperationQuoteLineDetailUpdate. Tyto moduly plug-in je nutné znovu zaregistrovat po změně podrobností řádku nabídky nebo řádku smlouvy. Postup pro dokončení tohoto procesu:

1. Otevřete PluginRegistrationTool a připojte se k vaší online instanci.
2. Vyberte **Hledat** a vyhledejte modul plug-in, který chcete aktualizovat.

    ![Dialogové okno stromu vyhledávání.](media/basic-guide-19.png)

3. Vyberte modul plug-in a poté na hlavní stránce vyberte **Vybrat**.
4. Vyberte krok modulu plug-in, který chcete aktualizovat, klikněte pravým tlačítkem myši a vyberte **Aktualizovat**.

    ![Výběr kroku v modulu plug-in.](media/basic-guide-20.png)

5. V dialogovém okně **Aktualizovat existující krok** vyberte v poli **Atributy filtrování** tlačítko se třemi tečkami (**…**):
 
    ![Dialogové okno Aktualizovat existující krok.](media/basic-guide-21.png)

6. V dialogovém **Vybrat atributy** zaškrtněte zaškrtávací políčka u vlastních atributů.

    ![Vyberte dialogové okno Atributy.](media/basic-guide-22.png)

7. Klepnutím na **OK** zavřete dialogové okno a pak vyberte **Aktualizovat krok**.
 
    ![Tlačítko Aktualizovat krok.](media/basic-guide-23.png)

8. Opakujte kroky 1 až 7 pro druhý modul plug-in.
9. Zavřete PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
