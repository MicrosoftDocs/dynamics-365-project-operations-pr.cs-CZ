---
title: Výchozí ceníky
description: Tento článek poskytuje informace o výchozích prodejních a nákladových cenících v Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410254"
---
# <a name="default-price-lists"></a>Výchozí ceníky

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

## <a name="sales-price-lists"></a>Prodejní ceníky

Každá nabídka projektu a smlouva v Dynamics 365 Project Operations obsahuje výchozí prodejní ceník. 

### <a name="price-list-default-on-project-quotes"></a>Ceník je výchozí pro nabídky projektu
Systém provede následující proces, aby určil, který ceník má být v nabídce projektu nastaven jako výchozí:

1. Systém zkoumá ceníky, které jsou připojeny k ceníkům projektů účtu. 
1. Pokud nejsou k záznamu účtu připojeny ceníky projektu, systém prohlédne prodejní ceníky připojené k parametrům projektu, které odpovídají měně nabídky projektu.
1. Dále systém zkontroluje datovou platnost ceníků, které odpovídají časovému období nabídky projektu. Konkrétně datum vytvoření nabídky.
1. Pokud existuje více ceníků, které jsou platné pro datum nabídky projektu, všechny ceníky jsou výchozí pro nabídku projektu.
1. Pokud k datu nabídky projektu nejsou platné žádné ceníky, není v nabídce projektu žádný výchozí ceník projektu. V nabídce projektu se zobrazí varovná zpráva. Zpráva uvádí, že kvůli neexistenci projektových ceníků nebudou vaše skutečné a odhadované práce a výdaje na projekt oceněny.

### <a name="price-list-default-on-project-contracts"></a>Ceník je výchozí pro projektové smlouvy 
Systém provede následující proces, aby určil, který ceník má být v projektové smlouvy nastaven jako výchozí:

1. Pokud je smlouva vytvořena z nabídky, projektové ceníky v nabídce jsou zkopírovány samostatně a připojeny ke smlouvě o projektu.
1. Pokud je smlouva vytvořena úplně od začátku, systém se podívá na ceníky, které jsou připojeny k projektovým ceníkům účtu. Pokud jsou k záznamu účtu připojeny ceníky projektu, systém prohlédne prodejní ceníky připojené k parametrům projektu, které odpovídají měně projektové smlouvy.
1. Dále systém zkontroluje datovou platnost ceníků, které odpovídají časovému období projektové smlouvy. Konkrétně datum vytvoření smlouvy.
1. Pokud existuje více ceníků, které jsou platné pro datum smlouvy, všechny ceníky jsou výchozí pro smlouvy.
1. Pokud k datu smlouvy nejsou platné žádné ceníky, není ve smlouvě žádný výchozí ceník projektu. V projektové smlouvě se zobrazí varovná zpráva. Zpráva uvádí, že kvůli neexistenci projektových ceníků nebudou vaše skutečné a odhadované práce a výdaje na projekt oceněny.

## <a name="cost-price-lists"></a>Nákladové ceníky

Ceníky nákladů nemají výchozí žádnou entitu v Project Operations. Stanovení nákladového ceníku, který se má použít pro náklady projektu, se vždy provádí pro danou transakci. Systém provede následující proces, aby určil, který ceník se má na projektové náklady použít.

1. Systém prozkoumá ceníky, které jsou připojeny ke smluvní organizační jednotce projektu.
1. Dále systém zkoumá datovou platnost ceníků, které odpovídají datu příchozího kontextu odhadu nebo skutečného kontextu.

    - *Kontext odhadu* odkazuje na libovolný ze tří kontextů odhadu v Project Operations:

        - Řádek odhadu projektu
        - Podrobnosti řádku nabídky
        - Podrobnosti řádku smlouvy

    - *Skutečný kontext* odkazuje na libovolný ze tří zdrojů skutečných hodnot v Project Operations:

       - Řádky deníku zápisu, které jsou ručně vytvořeny, nebo řádky deníku oprav, které jsou vytvořeny v deníku oprav
       - Řádky deníku, které se vytvářejí během odesílání protokolů času, výdajů nebo použití materiálu
       - Podrobnosti řádku faktury

    Když Project Operations páruje datum účinnosti řádku příchozího deníku nebo detailu řádku faktury ve *skutečném kontextu*, používá pole **Datum transakce**.

    - Pokud existuje více ceníků, které jsou platné pro datum v příchozím kontextu odhadu nebo skutečném kontextu, je vybrán naposledy vytvořený ceník.
    - Pokud nejsou ke smluvní organizační jednotce připojeny žádné ceníky, systém prohlédne nákladové ceníky připojené k parametrům projektu, které odpovídají měně projektu.

## <a name="enable-multi-currency-cost-price-list"></a>Povolit nákladový ceník ve více měnách

Toto nastavení lze nalézt na **Nastavení** \> **Parametry**. Výchozí hodnota je **Ne**.

Když je toto nastavení povoleno (to znamená, že hodnota je nastavena na **Ano**), systém se chová následovně:

- Umožňuje přidružení nákladových ceníků v libovolné měně k organizační jednotce. Například nákladový ceník v měně EUR lze připojit k organizační jednotce v měně USD. Systém bude nadále ověřovat, že ceníky nákladů, které jsou připojeny k organizační jednotce, nemají překrývající se datum účinnosti.
- Ověřuje, že ceníky nákladů, které jsou připojeny k parametrům projektu, nemají překrývající se datum účinnosti, i když mají různé měny. Toto chování se liší od výchozího chování (to znamená chování, když je hodnota nastavena na **Ne**). Ve výchozím chování jsou validovány pouze nákladové ceníky, které mají **stejnou**, pro nepřekrývající se datum účinnosti.
- Pro kontext příchozí transakce to určuje nákladový ceník pouze na základě účinnosti data. Toto chování se liší od výchozího chování, kdy systém vybere nákladový ceník, který odpovídá jak měně projektu, tak účinnosti data.

Díky těmto změnám v chování budou zákazníci Project Operations schopni udržovat globální ceník nákladů, který bude relevantní pro celou společnost. Nebudou muset mít ceníky v každé měně operací. Globální ceník bude mít platnost podle data a umožní nastavit nákladové sazby v jakékoli měně pro konkrétní kombinaci hodnot cenové dimenze. Měna ceníku nákladů se používá pouze pro zadání výchozích hodnot, když jsou vytvořeny záznamy položek **Ceny rolí**, **Ceny kategorií** a **Ceník**. Nebude použita pro stanovení ceníku.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
