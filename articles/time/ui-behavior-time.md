---
title: Chování uživatelského rozhraní při zadávání času
description: Toto téma obsahuje informace o chování uživatelského rozhraní při zadávání času.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961693"
---
# <a name="time-entry-ui-behavior"></a>Chování uživatelského rozhraní při zadávání času

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_


Nová mřížka pro **týdenní zadávání času** je vlastní ovládací prvek, který obsahuje panel nástrojů a dvě hlavní části **Dimenze** a **Doba trvání**.

## <a name="dimensions"></a>Dimenze
Část **Dimenze** znázorňuje dimenze, pro které lze zadat čas. Následující dimenze jsou podporovány ve výchozím nastavení:

  - Project
  - Projektový úkol
  - Role
  - Typ
  - Stav záznamu

Část **Dimenze** neumožňuje úpravy na řádku. Tato část je podložena zobrazením, které umožňuje přidat vlastní pole do mřížky pro týdenní zadávání času.

## <a name="duration"></a>Trvání
Část Doba trvání zobrazuje dny v týdnu jako záhlaví sloupců. Tato část umožňuje úpravy na řádku. Po vytvoření časového záznamu, který má odpovídající dimenze, mohou uživatelé rychle zadat množství času stráveného v těchto dimenzích.

## <a name="create-a-new-time-entry"></a>Vytvoření nového časového záznamu

1. V Mřížce zadání času vyberte **Nový**. 
2. V dialogovém okně **Rychlé zadání času** vyberte datum zadání času.
3. Zadejte data pro dimenze **Projekt**, **Projektový úkol**, **Role** a **Doba trvání**. Tyto informace by měly být přidány během několika minut, hodin nebo dnů zadáním hodnot **h**, **m** nebo **d** spolu s číslicí. 
4. Zadejte popis záznamu a jakékoli komentáře, které lze sdílet ohledně časového záznamu externě. 

Když záznam uložíte, zadané hodnoty se zobrazí v části **Rozměry**. Informace zadané do pole **Doba trvání** se zobrazí k datu, pro které byl časový záznam vytvořen.

Vyhledávací pole jsou zálohována systémovými zobrazeními. Například poté, co uživatel zadá projekt, bude pole **Projektový úkol** ve výchozím nastavení nastaveno na zobrazení **Kopie**. Chcete-li vytvořit časové záznamy pro úkoly, které nejsou přiřazeny uživateli, vyberte možnost **Změnit zobrazení** v dialogovém okně vyhledávání a pak vyberte zobrazení **Všechny aktivní projektové úkoly**.

## <a name="edit-a-time-entry"></a>Úprava časového záznamu 
Podrobnosti z některých polí na stránce zadávání času, například **Popis** a **Externí komentáře**, nejsou zobrazeny v mřížce týdenního zadávání času. Místo toho se v buňkách **Doba trvání**, které mají tyto další podrobnosti, zobrazí malý trojúhelníkový ukazatel. 

1. Chcete-li upravit záznam času, vyberte v záznamu času buňku, kterou chcete aktualizovat.
2. Vyberte **Upravit podrobnosti** k aktualizaci dat v podokně **Hlavní formulář zadání času**. 

## <a name="copy-a-time-entry-row"></a>Kopírování řádku časového záznamu
Po vytvoření řádku pro zadání času můžete vybrat možnost **Kopírovat řádek** a zkopírovat celý řádek do nového řádku. Po zkopírování řádku tímto způsobem budou zkopírovány také dimenze a doby trvání. Můžete také vybrat možnost **Upravit řádek** a aktualizovat hodnoty dimenzí a dob trvání na řádku v části **Doba trvání**.

## <a name="open-a-time-entry-behavior"></a>Chování při otevření časového záznamu
Pro podporu optimálního a rychlého zadávání do nejvýraznějších polí se v mřížce týdenního zadávání času zobrazuje podmnožina vybraných dimenzí a dob trvání. Chcete-li zobrazit všechny podrobnosti o jednom časovém záznamu, v části **Upravit záznam** vyberte možnost **Otevřít**.

## <a name="submit-a-time-entry"></a>Odeslání časového záznamu
Můžete odeslat jeden časový záznam nebo skupinu časových záznamů výběrem bloku buněk nebo celého řádku časového záznamu a následným výběrem příkazu **Odeslat**. Odeslané časové záznamy se zobrazí jako položky čekající na schválení na stránce **Schválení** schvalovatelů. Po úspěšném odeslání časových záznamů je nelze upravit.

## <a name="recall-a-time-entry"></a>Odvolání časového záznamu
Časové záznamy, které jste odeslali, můžete odvolat. Můžete odvolat jeden časový záznam, blok časových záznamů nebo celý řádek časových záznamů. Odvolané časové záznamy lze editovat.

## <a name="time-entry-status"></a>Stav časového záznamu

- **Koncept**: Novým časovým záznamům je automaticky přiřazen stav **Koncept**. Odstranit lze pouze časové záznamy, které mají stav **Koncept**.
- **Odesláno**: Po odeslání časového záznamu je stav aktualizován na **Odesláno**. 
- **Schváleno**: Po schválení časového záznamu je stav aktualizován na **Schváleno**. 
- **Vráceno**: Pokud je časový záznam zamítnut, bude jeho stav aktualizován na **Vráceno** a záznam bude dostupný pro opravu a opětovné odeslání. 

## <a name="view-rejection-comments"></a>Zobrazení komentářů k zamítnutí
Pokud je časový záznam zamítnut schvalovatelem, může schvalovatel přidat komentáře, které pomohou zdroji porozumět důvodu zamítnutí. Chcete-li zobrazit komentáře k zamítnutí časového záznamu, vyberte možnost **Otevřít záznam**. Komentáře k zamítnutí budou zobrazeny na časové ose. Uživatel může reagovat na komentáře o odmítnutí před opětovným odesláním záznamu.

## <a name="copy-week"></a>Kopírovat týden
Po vytvoření několika časových záznamů mohou uživatelé vytvářet více časových záznamů současně.

1. Ve formuláři **Časové záznamy** vyberte **Kopírovat týden** k hromadnému vytváření dalších časových záznamů. 
2. V dialogovém okně **Kopírovat** v části **Od období** použijte pole **Počáteční datum** a **Koncové datum** k definování rozsahu dat, ze kterého budou zkopírovány časové záznamy. 
3. V části **Do období** v poli **Počáteční datum** zadejte datum, pro které chcete vytvořit časové záznamy. 
4. Vyberte **Kopírovat**. Pro zadané datum v poli **Do období** se vytvoří kopie časových záznamů pro odpovídající den v týdnu v poli **Od období**. Například pondělní časový záznam z minulého týdne bude zkopírován do pondělí týdne, který je zadán jako **Do období**.

## <a name="import"></a>Import
Stejný základní postup se používá k importu z rezervací, přiřazení a výměn. Můžete určit rozsah kalendářních dat, odkdy jsou rezervace importovány, a pak explicitně vybrat rezervace, které mají být zkopírovány do konceptu časových záznamů. 
