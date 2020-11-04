---
title: Výchozí ceníky
description: Tento téma poskytuje informace o výchozích prodejních a nákladových cenících ve službě Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 275ef9b9706d212a6da0dc7c060081c3226572f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073659"
---
# <a name="default-price-lists"></a>Výchozí ceníky

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

## <a name="sales-price-lists"></a>Prodejní ceníky

Každá nabídka a smlouva o projektu v Dynamics 365 Project Operations obsahuje výchozí prodejní ceník. 

### <a name="price-list-default-on-project-quotes"></a>Ceník je výchozí pro nabídky projektu
Systém provede následující proces, aby určil, který ceník má být v nabídce projektu nastaven jako výchozí:

1. Systém zkoumá ceníky, které jsou připojeny k ceníkům projektů účtu. 
2. Pokud jsou k záznamu účtu připojeny ceníky projektu, systém prohlédne prodejní ceníky připojené k parametrům projektu, které odpovídají měně nabídky projektu.
3. Dále systém zkontroluje datovou platnost ceníků, které odpovídají časovému období nabídky projektu. Konkrétně datum vytvoření nabídky.
4. Pokud existuje více ceníků, které jsou platné pro datum nabídky projektu, všechny ceníky jsou výchozí pro nabídku projektu.
5. Pokud k datu nabídky projektu nejsou platné žádné ceníky, není v nabídce projektu žádný výchozí ceník projektu. V nabídce projektu se zobrazí varovná zpráva. Zpráva uvádí, že kvůli neexistenci projektových ceníků nebudou vaše skutečné a odhadované práce a výdaje na projekt oceněny.

### <a name="price-list-default-on-project-contracts"></a>Ceník je výchozí pro projektové smlouvy 
Systém provede následující proces, aby určil, který ceník má být v projektové smlouvy nastaven jako výchozí:

1. Pokud je smlouva vytvořena z nabídky, projektové ceníky v nabídce jsou zkopírovány samostatně a připojeny ke smlouvě o projektu.
2. Pokud je smlouva vytvořena úplně od začátku, systém se podívá na ceníky, které jsou připojeny k projektovým ceníkům účtu. Pokud jsou k záznamu účtu připojeny ceníky projektu, systém prohlédne prodejní ceníky připojené k parametrům projektu, které odpovídají měně projektové smlouvy.
4. Dále systém zkontroluje datovou platnost ceníků, které odpovídají časovému období projektové smlouvy. Konkrétně datum vytvoření smlouvy.
5. Pokud existuje více ceníků, které jsou platné pro datum smlouvy, všechny ceníky jsou výchozí pro smlouvy.
6. Pokud k datu smlouvy nejsou platné žádné ceníky, není ve smlouvě žádný výchozí ceník projektu. V projektové smlouvě se zobrazí varovná zpráva. Zpráva uvádí, že kvůli neexistenci projektových ceníků nebudou vaše skutečné a odhadované práce a výdaje na projekt oceněny.

## <a name="cost-price-lists"></a>Nákladové ceníky

Ceníky nákladů nemají výchozí žádnou entitu v Project Operations. Stanovení nákladového ceníku, který se má použít pro náklady projektu, se vždy provádí v daném okamžiku. Systém provede následující proces, aby určil, který ceník se má na projektové náklady použít.

1. Systém nejprve prozkoumá ceníky, které jsou připojeny ke smluvní organizační jednotce projektu.
2. Systém poté zkoumá datovou platnost ceníků, které odpovídají datu příchozího odhadu nebo skutečného řádku. V této situaci, *odhadový řádek* odkazuje na všechny tři kontexty odhadu v Project Operations:

    - Řádek odhadu projektu
    - Podrobnosti řádku nabídky
    - Podrobnosti řádku smlouvy
  
3. Pokud existuje více ceníků, které jsou platné pro datum v příchozím odhadu nebo skutečné hodnotě, je vybrán naposledy vytvořený ceník.
4. Pokud nejsou ke smluvní organizační jednotce připojeny žádné ceníky, systém prohlédne nákladové ceníky připojené k parametrům projektu, které odpovídají měně projektu.
5. Dále systém zkoumá datovou platnost ceníků, které odpovídají datu příchozího odhadu nebo skutečného řádku. 
6. Pokud existuje více ceníků, které jsou platné pro datum v příchozím odhadu nebo skutečné hodnotě, je vybrán naposledy vytvořený ceník.
7. Pokud k parametrům projektu nejsou připojeny žádné nákladové ceníky, které odpovídají měně a datu platnosti, systém nastaví výchozí hodnotu nákladové sazby na nulu (0) na příchozím odhadu nebo skutečném řádku.
