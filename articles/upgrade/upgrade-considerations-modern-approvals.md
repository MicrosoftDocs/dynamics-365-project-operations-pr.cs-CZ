---
title: Poznánky o upgradu pro moderní schválení
description: Téma pokrývá body, které by správci měli zvážit, když povolují funkci moderního schválení.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578378"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Poznánky o upgradu pro moderní schválení 

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

V rámci vydání 1. vlny z dubna 2022 bude ve výchozím nastavení povolena funkce Moderní schválení. Tato funkce zlepšuje spolehlivost schvalovací logiky a zajišťuje, že můžete určit důvod, pokud logika schvalování selže.

V rámci této změny jsou aktualizovány změny stavu schvalování projektů. Stav nyní jde přímo z **Odesláno** na **Schváleno**. **Čekající** již není stavem pro schválení. Chcete-li zjistit, zda čeká na schválení, ověřte, zda je schválení součástí sady schválení, a zkontrolujte stav připojené sady schválení.

## <a name="before-you-upgrade"></a>Před upgradem

Před upgradem na moderní schválení se ujistěte, že nemáte žádná nevyřízená schválení. Moderní schválení nepoužívá stav **Čekající**. Proto všechna schválení, která jsou ještě označena jako **Čekající** po aktualizaci, nebudou zpracována.

## <a name="after-you-upgrade"></a>Po upgradu

Po upgradu na moderní schválení musí správce ověřit, že byl povolen cloudový tok, který zpracovává schválení.

1. Přihlaste se k [flow.microsoft.com](https://flow.microsoft.com)
2. V pravém horním rohu stránky přepněte své prostředí na prostředí, které jste upgradovali.
3. Výběrem položky **Řešení** vypište seznam řešení, která jsou nainstalována v prostředí.
4. V seznamu řešení vyberte **Project Operations** nebo **Project Service**.
5. Změňte filtr z **Vše** na **Cloudové toky**.
6. Zkontrolujte, že je možnost **Project Service - Souběžně naplánovat sady schválení projektu** nastavena na **Zapnuto**. Pokud tomu tak není, vyberte tok a poté vyberte **Zapnout**.
7. Ověřte, že zpracování probíhá každých pět minut kontrolou seznamu **Systémové úlohy** v oblasti **Nastavení**.

## <a name="short-term-rollback"></a>Krátkodobé vrácení zpět

Pokud nemůžete přijmout změny nebo pokud narazíte na závažný problém s touto funkcí, můžete se dočasně vrátit k původnímu postupu schvalování provedením následujících kroků:
1. Přihlaste se do svého prostředí a ověřte, že neexistují žádná nevyřízená schválení.
2. Přejděte do **Nastavení** > **Parametry projektu**.
3. Vyberte **Ovládání funkcí** a poté vyberte **Moderní schválení** pro vypnutí funkce.

## <a name="removing-the-feature-flag"></a>Odstranění příznaku funkce

V aktualizaci Wave 2 z října 2022 bude možnost vypnout tuto funkci odstraněna.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
