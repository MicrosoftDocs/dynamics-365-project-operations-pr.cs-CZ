---
title: Přepsání cen s datem platnosti
description: Tento článek vysvětluje, jak nastavit přepsání cen pro konkrétní ceny v ceníku.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445963"
---
# <a name="date-effective-price-overrides"></a>Přepsání cen s datem platnosti 

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

*Přepisy cen platné k datu* poskytují způsob, jak přepsat nebo změnit konkrétní ceny v ceníku. Máte například standardní ceník platný od 1. ledna 2022 do 31. prosince 2022. Tento ceník obsahuje ceny pro mnoho rolí. Cena, která je nastavena pro roli **Síťový technik**, je 100 amerických dolarů (USD) za hodinu. Když síťový technik zaznamená čas mezi 1. lednem 2022 a 31. prosincem 2022, čas je oceněn na 100 USD. 1. října 2022 musíte upravit cenu *pouze* pro roli **Síťový technik**, z 100 USD za hodinu na 110 USD za hodinu. Funkce **Datum platnosti přepsání cen** umožňuje nastavit tuto změnu jako přepsání řádku pro konkrétní cenu role. Nemusíte tedy kopírovat celý ceník a měnit cenu jen toho jednoho řádku.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Přepis ceny platný k datu pro cenu práce

Proces nastavení přepisů ceny s datem platnosti pro pracovní dobu na projektu se skládá ze dvou základních kroků.

1. Aktivujte funkci **Přepsání cen s datem platnosti**.
1. Nastavte přepsání ceny s datem platnosti.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Aktivace funkce přepsání ceny s datem platnosti

> [!NOTE]
> Po aktivaci funkce **Přepsání cen s datem platnosti** ji nelze deaktivovat.

Chcete-li funkci **Přepsání cen s datem platnosti** aktivovat, postupujte podle těchto kroků.

1. Přejděte na **Nastavení** \> **Parametry**.
1. Otevřete záznam **Parametry**.
1. V podokně akcí na kartě **Ovládání funkcí** kartu, vyberte **Aktivovat přepsání cen s datem platnosti**.
1. V dialogovém okně pro potvrzení vyberte **OK**.
1. Po chvíli obnovte prohlížeč. Nyní by měly být k dispozici možnosti přepisu ceny platné k datu. Budete vědět, že tyto funkce byly aktivovány, pokud se tlačítko **Aktivovat přepisy cen s datem platnosti** již nezobrazuje v podokně akcí.

### <a name="set-up-a-date-effective-price-override"></a>Nastavení přepsání ceny s datem platnosti

Přepsání ceny s datem platnosti lze nastavit u ceníků **Náklady**, **Prodej** nebo **Nákup**.

> [!NOTE]
>Chování funkce **Přepsání cen s datem platnosti** má aktuálně následující omezení:
>
> - Pouze ceny rolí a přirážky cen rolí podporují funkci **Přepsání cen s datem platnosti** v Project Operations.
> - Když zkopírujete ceník pomocí akce **Kopírovat** na stránce **Údaje ceníku** a když během vytváření smlouvy vytvoříte ceník projektu ze standardního nebo vlastního ceníku, přepisy cen platné k datu **nejsou** zkopírovány ze zdrojového ceníku.

Chcete-li pro cenu role nebo přirážku ceny role nastavit přepsání ceny platné pro datum, postupujte takto.

1. Otevřete stránku pro ceník, pro který chcete nastavit přepsání ceny platné pro datum.
1. Vyberte kartu **Ceny rolí**. Tato karta obsahuje seznam všech záznamů **Cena role** v ceníku.
1. Vyberte záznam **Cena role** záznam, pro který chcete nastavit novou přepsanou cenu platnou pro datum, a poté dvakrát klepněte (nebo dvakrát klikněte) na možnost **Cena role** k otevření stránky **Údaje o ceně role**.
1. Vyberte kartu **Přepsání s datem platnosti**. V mřížce na této záložce jsou uvedeny všechny přepisy cen platné pro datum pro vybraný záznam **Cena role**.
1. Na panelu nástrojů nad mřížkou vyberte **Nové přepsání ceny role**. Otevře se posuvník **Nové přepsání ceny role**.
1. Zadejte datum účinnosti, jednotku a novou cenu pro přepsání ceny. Potom vyberte **Uložit** a zavřete formulář.

> [!NOTE]
> - Přepsání ceny role nebo přirážky ceny role platné k datu platí pro stejnou kombinaci hodnot cenové dimenze, která existuje na nadřazeném řádku **Cena role** nebo **Přirážka k ceně role**.
> - Datum, které je vybráno v polo **Účinné od** musí být v rámci data účinnosti nadřazeného ceníku. Přepsání ceny vstoupí v platnost v den, který je vybráno v poli **Účinné od** a bude platit do konce data ukončení nadřazeného ceníku. Pokud pro stejnou cenu role nastavíte jiné přepsání ceny platné pro datum, první přepsání ceny vstoupí v platnost v den, který je vybráno v poli **Účinné od** a bude platit až do začátku druhého přepsání.

## <a name="examples"></a>Příklady

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Příklad 1: Určení účinnosti data pro cenu role, která má přepsání ceny role

Následující příklad ukazuje, jak se určuje účinnost data pro konkrétní cenu role, pro kterou jsou nastaveny přepisy ceny role.

**Ceník A: od 1. ledna do 30. června**

*Cena role*

| Cena role | Jednotka | Cena | Vliv na ceny za příchozí transakce |
|---|---|---|---|
| Síťový technik | Hodina | 100 | Tato cena bude použita u všech transakcí, jejichž datum transakce je mezi 1. lednem a 14. březnem. |

*Přepsání ceny role*

| Platnost od | Jednotka | Cena | Vliv na ceny za příchozí transakce |
|---|---|---|---|
| Březen 15 | Hodina | 110 | Tato cena bude použita u všech transakcí, jejichž datum transakce je mezi 15. březnem a 30. březnem. |
| Duben 1 | Hodina | 120 | Tato cena bude použita u všech transakcí, jejichž datum transakce je mezi 1. dubnem a 30. červnem. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Příklad 2: Určení účinnosti data pro přirážku k ceně role, která má přepsání přirážky k ceně role

Následující příklad ukazuje, jak se určuje účinnost data pro konkrétní přirážku k ceně role, pro kterou jsou nastaveny přepisy přirážky k ceně role.

**Ceník A: od 1. ledna do 30. června**

*Cena role*

| Cena role | Pracovní doba | Jednotka | Cena | Vliv na ceny za příchozí transakce |
|---|---|---|---|---|
| Síťový technik | Regulární | Hodina | 100 | Tato cena bude použita u všech transakcí, jejichž datum transakce je mezi 1. lednem a 14. březnem. |

*Přirážka ceny role*

| Organizační jednotka | Pracovní doba | % přirážky |
|---|---|---|
| Contoso US | Přesčas | 10 % |

*Přepsání přirážky ceny role*

| Platnost od | Cena | Vliv na ceny za příchozí transakce |
|---|---|---|
| Březen 15 | 20 % | Toto procento přirážky bude použito u všech transakcí, jejichž datum transakce je mezi 15. březnem a 30. březnem. |
| Duben 1 | 25 % | Tato přirážka bude použita u všech transakcí, jejichž datum transakce je mezi 1. dubnem a 30. červnem. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
