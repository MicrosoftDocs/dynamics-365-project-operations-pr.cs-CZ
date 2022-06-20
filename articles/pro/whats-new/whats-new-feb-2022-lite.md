---
title: Co je nového, únor 2022 - omezené nasazení Project Operations
description: Tento článek poskytuje informace o aktualizacích kvality, které jsou k dispozici ve verzi Project Operations z února 2022 pro omezené nasazení.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922812"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Co je nového, únor 2022 - omezené nasazení Project Operations

_Platí pro: Omezené nasazení – od obchodu po pro forma fakturaci_

Tento článek se vztahuje na následující součásti a verze aplikace Microsoft Dynamics 365 Project Operations:

- Project Operations v prostředí Dataverse verze 4.28.0.120

## <a name="features-included-in-this-release"></a>Funkce v této vydané verzi

Od této verze můžete do jednoho projektu přidat až 300 členů týmu. Dříve byl limit na počet členů týmu 150. Další informace naleznete v části [Projektové lilmity](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Aktualizace pro zvýšení kvality

| Oblast funkcí | Referenční číslo | Aktualizace pro zvýšení kvality |
| --- | --- | --- |
| Fakturace a ceny | 2497369 | Oprava materiálu musí sledovat hodnotu data v parametrech **Oprava**. |
| Fakturace a ceny | 2498697 | Vylepšena konfigurace zabezpečení pro **Odvolání časového záznamu**. |
| Fakturace a ceny | 2517455 | Akce **Aktualizované transakce řádku faktury** nesmí být spuštěna vícekrát současně pro stejnou fakturu. |
| Fakturace a ceny | 2517465 | Akce **Deaktivujte podrobnosti řádku faktury** je zablokována, protože není podporována. |
| Fakturace a ceny | 2556660 | Opraveny kontroly účinnosti data, které se provádějí v ceníku připojeném k záznamu parametrů projektu. |
| Správa příležitostí | 2369202 | Opravena obchodní logika, která ověřuje, že ceníky, které mají překrývající se data účinnosti, mohou být připojeny ke stejné projektové smlouvě. |
| Správa příležitostí | 2385965 | Opraveno chování na kartě **Zákazníci** na stránce **Projektová smlouva**, když vyberete **Uložit a zavřít**. |
