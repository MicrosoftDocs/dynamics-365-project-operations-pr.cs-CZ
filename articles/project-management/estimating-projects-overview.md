---
title: Přehled odhadů projektů
description: Toto téma poskytuje informace o odhadech v Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d35be82563515adbba2c22402a751ed3daca8f83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131560"
---
# <a name="estimate-projects-overview"></a>Přehled odhadů projektů

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

U nabídky založené na projektu můžete pomocí entity **Podrobnosti řádku nabídky** odhadnout práci, která je požadována pro dodání projektu. Tento odhad pak můžete sdílet se zákazníkem.

Řádky nabídky založené na projektu mohou mít nula až mnoho podrobností řádku nabídky. Podrobnosti řádku nabídky se používají k odhadu času, výdajů nebo poplatků. Microsoft Dynamics 365 Project Operations neumožňuje u podrobností řádku nabídky materiálové odhady. Ty se nazývají třídy transakcí. Odhadované částky daně lze zadat také do třídy transakcí.

Kromě tříd transakcí, obsahují podrobnosti řádku nabídky mají typ transakce. Jsou podporovány dva typy transakcí pro podrobnosti řádku nabídky: **Náklady** a **Projektová smlouva**.

## <a name="estimate-by-using-a-contract"></a>Odhad pomocí smlouvy

Pokud jste při vytváření smlouvy založené na projektu použili nabídku, bude odhad, který jste udělali pro každý řádek nabídky v nabídce, zkopírován do projektové smlouvy. Struktura projektové smlouvy se podobá struktuře projektové nabídky, která obsahuje řádky, podrobnosti řádků a rozpisy faktur.

Odhady lze provádět přímo v projektové smlouvě, jako v projektové nabídce. U projektové nabídky se odhad provádí pomocí řádků smlouvy a podrobností řádku smlouvy. Podrobnosti řádku smlouvy lze také vygenerovat z projektového plánu, který byl vytvořen pomocí metody odhadu zdola nahoru.

Podrobnosti řádku smlouvy lze použít k odhadu času, výdajů nebo poplatků. Odhadované částky daně lze zadat také do podrobností řádku smlouvy.

Na podrobnostech řádku smlouvy nejsou materiálové odhady povoleny.

Procesy, které jsou podporovány ve smlouvě o projektu, jsou vytvoření a potvrzení faktury. Vytvoření faktury vytvoří koncept faktury založené na projektu, který zahrnuje všechny skutečné hodnoty nefakturovaného prodeje do aktuálního data.

Po potvrzení je smlouva jen pro čtení a její stav se změní z **Koncept** na **Potvrzeno**. Jakmile tuto akci provedete, nelze ji vrátit zpět. Vzhledem k tomu, že tato akce je trvalá, je vhodné udržovat smlouvu ve stavu **Koncept**.

Jedinými rozdíly mezi koncepty smluv a potvrzenými smlouvami je jejich stav a skutečnost, že koncept smluv lze upravit, zatímco potvrzené smlouvy nelze. Vytváření faktur a sledování skutečných hodnot lze provádět u konceptů smluv i u potvrzených smluv.

Project Operations nepodporuje u smluv nebo projektů změnové příkazy.

## <a name="estimating-projects"></a>Odhady projektů

Můžete odhadnout čas a výdaje na projekty. Project Operations neumožňuje odhady materiálů nebo poplatků na projekty.

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
