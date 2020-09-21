---
title: Vytvoření ceníku
description: Postup vytvoření ceníku v Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750424"
---
# <a name="create-a-price-list-project-service"></a>Vytvoření ceníku (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ceníky poskytují šablonu, kterou mohou vaši manažeři použít ke tvorbě nabídek a projektů a pro stanovení nákladů projektu. Poskytují seznam položek řádku rolí a nákladů, stejně jako ceny, které za ně budete účtovat. Můžete vytvořit několik ceníků, abyste mohli udržovat samostatné struktury cen pro různé regiony, v nichž prodáváte své produkty, nebo pro různé prodejní kanály. Je vhodné vytvořit alespoň jeden ceník pro každou měnu, kterou budete chtít používat k fakturaci zákazníků.  
  
Chcete-li vytvořit finanční odhady pro dodávané práce, zkontrolujte, zda má každý projekt seznam pomocných nákladů a prodejních cen. Nastavte výchozí nákladový a prodejní ceník, který platí pro všechny projekty vytvořené v organizaci.  
  
Ceníky jsou závislé na rolích a kategoriích výdajů, proto se před vytvořením ceníku přesvědčte, zda jste již nakonfigurovali role a výdajové kategorie, které chcete použít při vytváření ceníku.  
  
1.  Přejděte do části **Project Service > Ceníky**.  
  
2.  Klikněte na tlačítko **Nový**.  
  
3.  V části **Kontext** vyberte, zda je tento ceník pro **Náklady**, **Nákup** nebo **Prodej**.  
  
4.  Do pole **Název** zadejte název pro tento ceník.  
  
5.  V poli **Měna** vyberte měnu, kterou chcete použít pro účtování a oceňování.  
  
6.  V poli **Časová jednotka** určete dobu, k níž se cena vztahuje, například den nebo hodinu.  
  
7.  Podle potřeby vyplňte pole  **Počáteční datum**, **Koncové datum** a **Popis**.  
  
8.  Kliknutím na tlačítko **Uložit** vytvořte záznam, abyste mohli pokračovat v jeho úpravách.  
  
9. Chcete-li přidat cenu role do ceníku, klikněte na tlačítko **+** pod polem **Ceny rolí.**.  
  
10. V podokně **Cena role** vyplňte údaje a poté klikněte na položku **Uložit**. Pokračujte podle potřeby v přidávání cen rolí. Když jste hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.  
  
11. Chcete-li přidat cenu kategorie výdajů do ceníku, klikněte na tlačítko **+** pod polem **Ceny kategorií**.  
  
12. V podokně **Cena kategorie transakce** vyplňte údaje a poté klikněte na položku **Uložit**. Pokračujte podle potřeby v přidávání cen kategorií. Když jste hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.  
  
13. Chcete-li přidat položky ceníku do ceníku, klikněte na tlačítko **+** pod částí **Položky ceníku**.  
  
14. V podokně **Položka ceníku** vyplňte údaje a poté klikněte na položku **Uložit**. Pokračujte podle potřeby v přidávání položek ceníku. Když jste hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.  
  
15. Chcete-li přidat vztahy mezi oblastmi do ceníku, klikněte na tlačítko **+** pod částí **Vztahy mezi oblastmi**.  
  
16. V okně **Nové připojení** vyplňte údaje a poté klikněte na položku **Uložit**. Pokračujte podle potřeby v přidávání vztahů mezi oblastmi. Když jste hotovi, klikněte na tlačítko **Uložit** v pravém dolním rohu obrazovky.  
  
### <a name="see-also"></a>Viz také  
 [Konfigurace Project Service Automation](../project-service/configure.md)
