---
title: Mapování projektů a úkolů na řádek smlouvy na základě projektu – omezené
description: Tohle téma poskytuje informace, jak přidávat a odebírat projekty a úkoly na řádek smlouvy.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 30a74f683a032d5bd6caed347f4d0a948376d267
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177638"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line---lite"></a>Mapování projektů a úkolů na řádek smlouvy na základě projektu – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Na řádcích smlouvy založené na projektu můžete namapovat konkrétní úkoly v projektu na řádek smlouvy.

Když mapujete konkrétní úkoly na řádek smlouvy, způsob fakturace, možnosti účtovatelnosti, nepřekročitelné limity a zákazníci definovaní na řádku smlouvy budou platit pouze pro tyto konkrétní úkoly.

Pokud máte situaci, ve kterém je jedna fáze projektu, například fáze prototypu, pevná cena a všechny ostatní fáze jsou čas a materiál, budete moci přidružit fázi prototypu a všechny podřízené úkoly přidružené k řádku smlouvy pro tuto fázi ke způsobu fakturace s pevnou cenou.

Všechny ostatní fáze ve strukturovaném rozpisu prací projektu (WBS) lze přidružit k řádce smlouvy na základě času a materiálu.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Přidružení úkolů k řádkům smlouvy na základě projektu

Úkoly lze přidružit k řádkům smlouvy z karty **Účtovatelné úkoly** na stránce **Řádek smlouvy** nebo z karty **Účtování úkolů** na stránce **Projekt**.

### <a name="from-the-contract-line-page"></a>Ze stránky Řádek smlouvy

Chcete-li přidružit projektové úkoly k řádku smlouvy z karty **Účtovatelné úkoly** na stránce **Řádek smlouvy**, proveďte následující kroky.

1. Na kartě **Obecné** pro řádek smlouvy na základě projektu ověřte, že je vyplněno pole **Projekt**.
2. V poli **Zahrnuté úkoly** vyberte **Pouze vybrané úkoly**.
3. Uloží vaše změny. Formulář se aktualizuje a kartě **Účtovatelné úkoly** bude viditelná.
4. Vyberte kartu **Účtovatelné úkoly** a v podmřížce vyberte **Přidat úkol řádku smlouvy**.
5. Na stránce **Úkoly řádku smlouvy** v rozevíracím seznamu **Úkoly** vyberte úkol. 
6. Zadejte informace do pole **Typ fakturace** a poté vyberte **Uložit a zavřít**. Vybraný úkol je přidružen k řádku smlouvy.

> [!NOTE]
> To není nejoptimálnější způsob přidružení projektových úkolů k řádkům smluv. Každý projekt bude muset být v tomto prostředí ručně přidružen. Preferovaný způsob je z karty **Účtování úkolů** na stránce **Projekt**.

### <a name="from-the-project-page"></a>Ze stránky Projekt

Toto je optimální metoda přidružení úkolů k řádkům smlouvy. Můžete vybrat více úkolů a přidružit všechny z nich a jejich podřízené úkoly k vybranému řádku smlouvy. Chcete-li přidružit úkoly k řádku smlouvy ze stránky **Projekt**, proveďte následující kroky.

1. Na kartě **Obecné** pro řádek smlouvy na základě projektu ověřte, že je vyplněno pole **Projekt**.
2. V poli **Zahrnuté úkoly** vyberte **Pouze vybrané úkoly**.
3. Uložte řádek smlouvy založené na projektu. Formulář se aktualizuje a kartě **Účtovatelné úkoly** bude viditelná. Toto slouží pouze pro účely ověření.
4. Na kartě **Obecné** pro řádek smlouvy na základě projektu v poli **Projekt** vyberte odkaz na projekt.
5. Na stránce **Projekt** vyberte kartu **Nastavení účtování úkolů**.
6. K dispozici jsou dvě mřížky. Jedna mřížka je pro řádky smlouvy, která platí pro celý projekt. Druhá mřížka platí pro nastavení fakturace konkrétních úkolů. Ve druhé mřížce vyberte jeden nebo více úkolů a poté vyberte **Přidružit řádky smlouvy**.
7. Na otevřené stránce dialogového okna vyberte v rozevíracím seznamu řádek smlouvy.
8. Pomocí rozevíracího seznamu **Typ fakturace** označte úkoly jako účtovatelné nebo neúčtovatelné.
9. Zaškrtnutím políčka označte, zda by přidružení mělo zahrnovat i podřízené úkoly vybraných úkolů. Zaškrtnutí políčka také přidruží podřízené úkoly vybraných úkolů k řádku smlouvy.
10. Výběrem možnosti **OK** zavřete dialogové okno.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Zrušení přidružení úkolů k řádkům smlouvy na základě projektu

### <a name="from-the-contract-line-page"></a>Ze stránky Řádek smlouvy

Chcete-li zrušit přidružení projektových úkolů k řádku smlouvy z karty **Účtovatelné úkoly** na stránce **Řádek smlouvy**, proveďte následující kroky.

1. Na kartě **Účtovatelné úkoly** vyberte **Odstranit úkol řádku smlouvy**.
2. Zobrazí se varovná zpráva s upozorněním, že odebrání tohoto přidružení může mít za následek obrácení všech skutečných hodnot dříve zaznamenaných v úkolu. Vyberte **OK** v dialogovém okně, čímž odeberete přidružení mezi úkolem a řádkem smlouvy na základě projektu. 

> [!NOTE]
> Tímto úkonem neodstraníte úkol z projektu. Místo toho odebere přidružení úkolu k řádku smlouvy na základě projektu.

### <a name="from-the-project-page"></a>Ze stránky Projekt

To je optimálnější způsob zrušení přidružení úkolů k řádkům smluv. Můžete vybrat více úkolů a zrušit přidružení všech a jejich podřízených úkolů k vybranému řádku smlouvy. Chcete-li zrušit přidružení úkolů k řádku smlouvy, proveďte následující kroky.

1. Na kartě **Obecné** pro řádek smlouvy na základě projektu v poli **Projekt** klikněte na odkaz na projekt.
2. Na stránce **Projekt** vyberte kartu **Nastavení účtování úkolů**.
3. Na stránce jsou dvě mřížky. Jedna mřížka je pro řádky smlouvy, které platí pro celý projekt, a druhá platí pro nastavení fakturace pro konkrétní úkol. Ve druhé mřížce vyberte jeden nebo více úkolů a poté vyberte **Zrušit přidružení řádků smlouvy**.
4. Na otevřené stránce dialogového okna vyberte v rozevíracím seznamu řádek smlouvy.
5. Zaškrtnutím políčka označte, zda by přidružení mělo být odebráno i od podřízených úkolů vybraných úkolů. Zaškrtnutí políčka také zruší přidružení podřízených úkolů vybraných úkolů k řádku smlouvy.
6. Vyberte **OK**. Zobrazí se varovná zpráva s upozorněním, že odebrání tohoto přidružení může mít za následek obrácení všech skutečných hodnot dříve zaznamenaných v úkolu. Vyberte **OK** v dialogovém okně s upozorněním, čímž odeberete přidružení mezi úkolem a řádkem smlouvy na základě projektu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]