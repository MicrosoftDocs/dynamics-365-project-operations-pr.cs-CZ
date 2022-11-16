---
title: Externí plánování
description: Tento článek obsahuje informace o externím plánování.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736957"
---
# <a name="external-scheduling"></a>Externí plánování

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Režim externího plánování umožňuje nativně vytvářet, aktualizovat a odstraňovat entity, které souvisejí se strukturovaným rozpisem prací, ale bez aktuálních omezení, která jsou vynucována aplikací Microsoft Project for the Web. Poskytuje také omezené ověřování. Tento režim by měli používat pouze tito zákazníci:

- Zákazníci, kteří mají nástroje potřebné k definování strukturovaného rozpisu prací mimo plánovací logiku, kterou poskytuje Project Operations
- Zákazníci, kteří musí spravovat hierarchii plánů, závislosti nebo dobu trvání úkolů

> [!IMPORTANT]
> Data, která nejsou správně zadána v entitách souvisejících se strukturovaným rozpisem prací, nemusí být vykreslena v mřížce sesouhlasení zdrojů, mřížce odhadů, mřížce sledování nebo mřížce přiřazení zdrojů.

## <a name="configuration"></a>Configuration

Tato funkce je ve výchozím nastavení povolena. Na předdefinované hlavní stránce projektů se však související pole standardně nezobrazuje. Chcete-li pole povolit, v portálu Maker Portal otevřete hlavní stránku entity projektu a vyberte položku **Plánovací modul** a potom pole změňte na **Při výchozím nastavení viditelné**. Pokud nepoužíváte přednastavenou hlavní stránku projektu, upravte stávající stránku a na ni přidejte pole **Plánovací modul**.

## <a name="settings"></a>Nastavení

Chcete-li použít režim externího plánování, musíte nejprve vytvořit nový projekt a vybrat plánovací modul **Externě naplánováno** v rozevíracím seznamu na hlavní stránce projektu. Po nastavení tohoto režimu pro projekt jej nelze změnit.

## <a name="viewing-the-wbs"></a>Zobrazení strukturovaného rozpisu prací

Pokud je projekt naplánován externě, přístup aplikace Project for the Web je pro tento projekt omezen. Chcete-li zobrazit strukturovaný rozpis prací, musíte přejít na sledovací mřížku, kde je zobrazen celý strukturovaný rozpis prací.

## <a name="creating-and-editing-the-wbs"></a>Vytváření a úprava strukturovaného rozpisu prací

Pokud je pro projekt povoleno externí plánování, musíte definovat data pro všechny entity související se strukturovaným rozpisem prací, včetně úkolů, členů týmu, přiřazení zdrojů a závislostí.

Následující ilustrace znázorňuje datový model plánování projektu.

![Datový model plánování projektu.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funkční omezení

Následující operace nejsou povoleny pro externě naplánované projekty.

### <a name="project-planning"></a>Plánování projektu

- **Kopírovat projekt** – Tato operace není podporována u externě naplánovaných projektů.
- **Přesunout projekt** – Změny počátečního data projektu neposunou začátek úkolů nebo přiřazení zdrojů ve strukturovaném rozpisu prací.
- **Aktualizace projektového manažera** – Změny projektového manažera na hlavní stránce projektu automaticky nevytvoří nového člena projektového týmu, dokud nebude projekt převeden.
- **Aktualizace šablony pracovní doby projektu** – Změny v šabloně pracovní doby projektu nepřepočítají plán projektu.
- **Průběhové křivky přiřazení zdrojů** – Vytvoření přiřazení zdrojů automaticky neaktualizuje pole **mdyn\_PlannedWork**. Toto pole se používá k uchování průběhových křivek úsilí o přiřazení zdrojů. Pokud v mřížce přiřazení zdrojů nebo v mřížce sesouhlasení zdrojů zobrazíte časově rozložené úsilí, musíte definovat platné průběhové křivky přiřazení zdrojů. Tyto průběhové křivky musí být správně naformátovány, aby aktivovaly výpočet průběhových křivek nákladů i průběhových křivek prodejní ceny. Doporučujeme vytvořit testovací projekt, který je naplánován aplikací Project for the Web, a poté zkontrolovat přidružená data, abyste ověřili správnost požadavků a formátování.

### <a name="resource-management"></a>Řízení zdrojů

- **Splnění obecného zdroje** – U externě naplánovaných projektů není podporováno splnění obecného zdroje. Pokusy o splnění aktivních otevřených požadavků vytvoří nové členy projektového týmu, ale neodstraní obecného člena týmu ani nenahradí obecného člena týmu v žádném existujícím přiřazení zdrojů.
- **Odstranění členů týmu** – Odstraněním člena týmu se automaticky neodstraní přiřazení zdrojů.

### <a name="quoting-and-contracting"></a>Nabídky a uzavírání smluv

- **Import podrobností o řádku nabídky a řádku smlouvy** – Když jsou z projektu importovány podrobnosti o řádku nabídky nebo smlouvy, aplikace byla otestována tak, aby podporovala maximálně 500 úkolů ve struktuře rozpisu prací, což vychází z omezení 20 přiřazení na úkol.

### <a name="actuals-and-invoicing"></a>Skutečné hodnoty a fakturace

- I když nedochází k žádným změnám stávajících ověření mezi strukturovaným rozpisem prací a finančními transakcemi, je důležité, abyste se řídili předpřipraveným datovým modelem, abyste zajistili, že všechny následné transakce proběhnou podle očekávání.
