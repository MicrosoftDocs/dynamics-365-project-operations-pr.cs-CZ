---
title: Mapování projektů a úkolů na řádky nabídky založené na projektu
description: Toto téma poskytuje informace o mapování projektů a úkolů na řádku nabídky založené na projektu.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073672"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Mapování projektů a úkolů na řádky nabídky založené na projektu

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Na řádcích nabídek založených na projektu můžete mapovat konkrétní úkoly projektu, který je již přidružen k řádku nabídky.

Když mapujete úkoly na řádek nabídky, následující položky, které jste definovali na řádku nabídky, se vztahují pouze na tyto úkoly:

- Způsob fakturace
- Možnosti účtovatelnosti
- Nepřekročitelné limity
- Zákazníci

Například můžete mít projekt, kde jedna fáze je pevná cena a všechny ostatní fáze jsou čas a materiály. V tomto případě můžete první fázi a všechny její podřízené úkoly přidružit k řádku nabídky pro tuto fázi s metodou fakturace za pevnou cenu. Poté můžete všechny ostatní fáze přidružit k řádku nabídky založeném na čase a materiálů.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Přidružení úkolů k řádkům nabídky založené na projektu

Úkoly můžete přidružit k řádkům nabídek z následujících umístění:

- Stránka **Projekt** > karta **Účtování úkolů** (optimální)
- Stránka **Řádek nabídky** > karta **Účtovatelné úkoly** 

### <a name="from-the-project-page"></a>Ze stránky Projekt

Stránka **Projekt** poskytuje optimální prostředí pro přidružení úkolů k řádkům nabídky. Na této stránce můžete vybrat více úkolů a všechny z nich – včetně jejich podřízených úkolů – přiřadit k vybranému řádku nabídky.

1. Na kartě **Všeobecné** řádku nabídky založené na projektu si ověřte, že je vyplněno pole **Projekt**.
2. V poli **Zahrnuté úkoly** vyberte možnost **Pouze vybrané úkoly**.
3. Uložte řádek nabídky založené na projektu. Když se formulář aktualizuje, zobrazí se karta **Účtovatelné úkoly**.
4. Na kartě **Všeobecné** vyberte odkaz na projekt v poli **Projekt**.
5. Na stránce **Projekt** vyberte kartu **Účtování úkolů**.
6. Ve druhé mřížce, která se vztahuje na nastavení fakturace pro konkrétní úkol, vyberte jeden nebo více úkolů a poté vyberte možnost **Přidružit řádky nabídek**.
7. V zobrazené stránce dialogu vyberte řádek nabídky, který v nabídce zobrazí řádky nabídky založené na projektu.
8. V poli **Typ fakturace** uveďte, zda jsou tyto úkoly účtovatelné nebo neúčtovatelné.
9. Zaškrtnutím políčka určíte, zda má přidružení zahrnovat podřízené úkoly vybraných úkolů. Zaškrtnutí políčka přidruží podřízené úkoly vybraných úkolů k řádku nabídky.
10. Výběrem možnosti **OK** zavřete dialogové okno.

### <a name="from-the-quote-line-page"></a>Ze stránky řádku nabídky

K řádkům nabídky můžete přidružit projektové úkoly na kartě **Účtovatelné úkoly** umístěné ve stránce **Řádek nabídky**.

>[!NOTE]
>Optimálním místem pro přidružení projektových úkolů k řádkům nabídky je karta **Účtování úkolů** na stránce **Projekt**. Pokud přidružení úkolů provádíte na kartě **Účtovatelné úkoly** umístěné na stránce **Řádek nabídky** , musíte ručně přidružit každý projekt.

1. Na kartě **Všeobecné** řádku nabídky založené na projektu si ověřte, že je v poli **Projekt** vybrán projekt.
2. V poli **Zahrnuté úkoly** vyberte možnost **Pouze vybrané úkoly**.
3. Uložte řádek nabídky založené na projektu. Když se formulář aktualizuje, zobrazí se karta **Účtovatelné úkoly**.
4. Na kartě **Účtovatelné úkoly** vyberte možnost **Přidat úkol řádku nabídky**.
5. Na stránce **Úkol řádku nabídky** vyberte úkol v poli **Úkoly** a v poli **Typ fakturace** vyberte příkaz **Uložit**. 
6. Zavřete stránku. Vybraný úkol je nyní přidružen k řádku nabídky.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Zrušení přidružení úkolů k řádkům nabídky založené na projektu

### <a name="from-the-project-page"></a>Ze stránky Projekt

Tato metoda poskytuje optimální prostředí pro zrušení přidružení úkolů k řádkům nabídky. Na této stránce můžete vybrat více úkolů a zrušit jejich přiřazení – včetně jejich podřízených úkolů – k vybranému řádku nabídky.

1. Na kartě **Všeobecné** řádku nabídky založené na projektu vyberte v poli **Projekt** odkaz na projekt.
2. Na stránce **Projekt** vyberte kartu **Účtování úkolů**.
3. Ve druhé mřížce, která se vztahuje na nastavení fakturace pro konkrétní úkol, vyberte jeden nebo více úkolů a poté vyberte možnost **Zrušit přidružení řádků nabídek**.
4. Na zobrazené stránce dialogu vyberte řádek nabídky.
5. Zaškrtnutím políčka určíte, zda má být přidružení odebráno také u podřízených úkolů vybraných úkolů. Zaškrtnutí políčka zruší také přidružení podřízených úkolů vybraných úkolů k řádku nabídky.
6. Vyberte **OK**. Varovná zpráva vás informuje, že pokud toto přidružení odeberete, všechny skutečné údaje dříve zaznamenané v úkolu lze stornovat. 
7. Výběrem možnosti **OK** pokračujte a odeberte přidružení mezi úkolem a řádkem nabídky založené na projektu.

### <a name="from-the-quote-line-page"></a>Ze stránky řádku nabídky

Přidružení projektových úkolů k řádkům nabídky lze zrušit také na kartě **Účtovatelné úkoly** umístěné ve stránce **Řádek nabídky**.

1. Na kartě **Účtovatelné úkoly** vyberte možnost **Odstranit úkol řádku nabídky**.
2. Vyberte **OK**. Varovná zpráva vás informuje, že pokud toto přidružení odeberete, všechny skutečné údaje dříve zaznamenané v úkolu lze stornovat. 
3. Výběrem možnosti **OK** pokračujte a odeberte přidružení mezi úkolem a řádkem nabídky založené na projektu.

>[!NOTE]
> Tento postup neodstraní úkol z projektu. Odstraní pouze přidružení úkolu k řádku nabídky založené na projektu.
