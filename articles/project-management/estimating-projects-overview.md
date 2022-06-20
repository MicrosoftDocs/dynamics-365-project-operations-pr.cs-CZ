---
title: Koncepty finančního odhadu
description: Tento článek poskytuje informace o finančních odhadech projektů v Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f8a4c3dd31cf5612c352331891178ac0ab852921
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931000"
---
# <a name="financial-estimation-concepts"></a>Koncepty finančního odhadu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V Dynamics 365 Project Operations můžete své projekty finančně odhadnout ve dvou fázích: 
1. Během předprodejní fáze, než dojde k získání dohody. 
2. Během fáze provádění po vytvoření smlouvy o projektu. 

Finanční odhad pro projektovou práci můžete vytvořit na kterékoli z následujících 3 stránek:
- Stránka **Řádek nabídky** pomocí údajů řádku nabídky.  
- Stránka **Řádek smlouvy o projektu** pomocí údajů řádku smlouvy. 
- Stránka **Projekt** pomocí stránek karty **Úkoly** nebo **Odhady výdajů**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Pomocí nabídky projektu vytvořte odhad
U nabídky založené na projektu můžete pomocí entity **Podrobnosti řádku nabídky** odhadnout práci, která je požadována pro dodání projektu. Tento odhad pak můžete sdílet se zákazníkem.

Řádky nabídky založené na projektu mohou mít nula až mnoho podrobností řádku nabídky. Podrobnosti řádku nabídky se používají k odhadu času, výdajů nebo poplatků. Microsoft Dynamics 365 Project Operations neumožňuje u podrobností řádku nabídky materiálové odhady. Ty se nazývají třídy transakcí. Odhadované částky daně lze zadat také do třídy transakcí.

Kromě tříd transakcí, obsahují podrobnosti řádku nabídky mají typ transakce. Jsou podporovány dva typy transakcí pro podrobnosti řádku nabídky: **Náklady** a **Projektová smlouva**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Pomocí smlouvy o projektu vytvořte odhad

Pokud jste při vytváření smlouvy založené na projektu použili nabídku, bude odhad, který jste udělali pro každý řádek nabídky v nabídce, zkopírován do projektové smlouvy. Struktura projektové smlouvy se podobá struktuře projektové nabídky, která obsahuje řádky, podrobnosti řádků a rozpisy faktur.

Odhady lze provádět přímo v projektové smlouvě, jako v projektové nabídce. U projektové nabídky se odhad provádí pomocí řádků smlouvy a podrobností řádku smlouvy. Podrobnosti řádku smlouvy lze také vygenerovat z projektového plánu, který byl vytvořen pomocí metody odhadu zdola nahoru.

Podrobnosti řádku smlouvy lze použít k odhadu času, výdajů nebo poplatků. Odhadované částky daně lze zadat také do podrobností řádku smlouvy.

Na podrobnostech řádku smlouvy nejsou materiálové odhady povoleny.

## <a name="use-a-project-to-create-an-estimate"></a>Pomocí projektu vytvořte odhad 

Můžete odhadnout čas a výdaje na projekty. Project Operations nepodporuje odhady materiálů ani poplatků za projekty.

Odhady času se generují při vytvoření úkolu a určení atributů obecného zdroje, který je vyžadován k provedení úkolu. Odhady času jsou generovány z plánování úkolů. Odhady času nejsou vytvářeny, pokud vytváříte obecné členy týmu mimo kontext plánu.

Odhady výdajů se zapisují do mřížky na stránce **Odhady výdajů**.

Vytvoření odhadu pro projekt je považováno za osvědčený postup, protože u každého úkolu v plánu projektu můžete sestavit podrobné odhady pracovní síly nebo času a výdajů zdola nahoru. Tento podrobný odhad pak můžete použít k vytvoření odhadů pro každý řádek nabídky a vytvoření důvěryhodnější nabídky pro zákazníka. Když importujete nebo vytvoříte podrobný odhad na řádku nabídky pomocí plánu projektu, Project Operations importuje hodnoty prodeje a hodnoty nákladů těchto odhadů. Po importu si můžete zobrazit ziskovost, marže a metriky proveditelnosti v nabídce projektu.

## <a name="understanding-estimates"></a>Princip odhadování

Následující tabulku použijte jako vodítko pro pochopení obchodní logiky ve fázi odhadu.

| Scénář                                                                                                                                                                                                                                                                                                                                          | Záznam entity                                                                                                                                                                                                       | Typ transakce | Třída transakce | Další informace                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Potřebujete-li odhadnout prodejní hodnotu času v nabídce                                                                                                                                                                                                                                                                                    | Je vytvořen záznam Podrobnosti řádku nabídky (PŘN).                                                                                                                                                                               | Projektová smlouva | Time        | Pole Původ transakce na řádku PŘN strany prodeje odkazuje na PŘN strany nákladů |
|                                                                                                                                                                                                                                                                                     | Systém vytvoří druhý záznam PŘN, který bude uchovávat odpovídající hodnoty nákladů. Systém zkopíruje všechna nepeněžní pole z PŘN prodeje do PŘN nákladů.                                                                                                                                                                               | Náklady | Time        | Pole Původ transakce na řádku PŘN strany prodeje odkazuje na PŘN strany nákladů |
| Potřebujete-li odhadnout prodejní hodnotu času ve smlouvě                                                                                                                                                                                                                                                                                 | Je vytvořen záznam Podrobnosti řádku projektové smlouvy (PŘS).                                                                                                                                                                    | Projektová smlouva | Time        | Pole Původ transakce na řádku PŘS strany prodeje odkazuje na PŘS nákladů      |
|                                                                                                                                                                                                                                                                                  | Systém vytvoří druhý záznam PŘS, který bude uchovávat odpovídající hodnoty nákladů. Systém zkopíruje všechna nepeněžní pole z PŘS prodeje do PŘS nákladů.                                                                                                                                                                    | Náklady | Time        | Pole Původ transakce na řádku PŘS strany prodeje odkazuje na PŘS nákladů      |
| Pokud uživatel popisuje zdroj v úkolu projektu                                                                                                                                                                                                                                                                                            | Záznam řádku odhadu pro zobrazení hodnoty prodeje úkolu je vytvořen při vytvoření úkolu se všemi požadovanými cenovými dimenzemi. Role a organizační jednotky jsou cenovými dimenzemi | Projektová smlouva | Čas        |                                                                                   |
|     | Záznam řádku odhadu pro zobrazení hodnoty nákladů úkolu je vytvořen při vytvoření úkolu se všemi požadovanými cenovými dimenzemi. Systém zkopíruje všechna nepeněžní pole z řádku odhadu prodeje do řádku odhadu nákladů. Role a organizační jednotka jsou cenovými dimenzemi pro nákladové a fakturační sazby.                                                                                                                                                                                                                | Náklady             | Čas           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Přizpůsobení entit Podrobnosti řádku nabídky a Podrobnosti řádku smlouvy

Pokud jste na řádku podrobností nabídky přidali vlastní pole a chcete, aby systém zadal hodnotu pole jako výchozí hodnotu na souvisejícím řádku nákladů, který vytvoří, použijte nástroje pro registraci modulů plug-in **PreOperationContractLineDetailUpdate** a **PreOperationQuoteLineDetailUpdate**. Tyto moduly plug-in je nutné znovu zaregistrovat po změně podrobností řádku nabídky nebo řádku smlouvy. Postup pro dokončení tohoto procesu:

1. Otevřete PluginRegistrationTool a připojte se k vaší online instanci.
2. Vyberte **Hledat** a vyhledejte modul plug-in, který chcete aktualizovat.
3. Vyberte modul plug-in a poté na hlavní stránce klikněte na **Vybrat**.
4. Vyberte krok modulu plug-in, který chcete aktualizovat, klikněte pravým tlačítkem myši a vyberte **Aktualizovat**.
5. V dialogovém okně **Aktualizovat existující krok** vyberte v poli **Atributy filtrování** tlačítko se třemi tečkami (**…**):
6. V dialogovém **Vybrat atributy** zaškrtněte zaškrtávací políčka u vlastních atributů.
7. Klepnutím na **OK** zavřete dialogové okno a pak vyberte **Aktualizovat krok**.
8. Opakujte kroky 1 až 7 pro druhý modul plug-in.
9. Zavřete **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
