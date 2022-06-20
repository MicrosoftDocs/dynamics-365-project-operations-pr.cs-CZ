---
title: Integrace parametrů Project Service Automation
description: Tento článek vysvětluje, jak konfigurovat výchozí data zadávaná při integraci Microsoft Dynamics 365 for Project Service Automation s Microsoft Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a4abeb2960981196ed1d7c453e7daa0558e326ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932288"
---
# <a name="project-service-automation-integration-parameters"></a>Integrace parametrů Project Service Automation

[!include[banner](../includes/banner.md)]

Na stránce **Parametry integrace Project Service Automation** můžete konfigurovat způsob zadávání výchozích dat při integraci aplikací Dynamics 365 Project Service Automation a Dynamics 365 Finance. Aby se projekty úspěšně synchronizovaly z Project Service Automation do Finance, musíte nastavit následující pole.

Chcete-li otevřít **Parametry integrace Project Service Automation** přejděte na **Řízení projektů a účetnictví** \> **Založit** \> **Integrační parametry Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - Integrace projektových úkolů, kategorie transakcí výdajů, odhady hodin, odhady výdajů a zamykání funkcí jsou k dispozici ve verzi 8.0.
> - Integrace skutečných hodnot je k dispozici ve verzi 8.0.1 nebo novější.


| Tabulátor                    | Pole                | Popis |
|------------------------|----------------------|-------------|
| OBECNÉ                | Výchozí typ projektu | Vyberte výchozí typ projektu. Když se projekty synchronizují z Project Service Automation, tato hodnota se použije, pokud jste v integrační šabloně nezadali výchozí hodnotu. Během synchronizace se pole **Typ projektu** nových projektů nastaví na tuto hodnotu. Hodnota však může být aktualizována, když jsou řádky kontraktu projektu synchronizovány z Project Service Automation. |
|                        | Časová kategorie        | Vyberte výchozí kategorii času. Tato hodnota se používá, když jsou hodinové odhady synchronizovány z Project Service Automation. Když jsou odhady hodin a skutečné hodiny synchronizovány z Project Service Automation, pole **Kategorie** nových prognóz hodin projektu v Finance je nastaveno na tuto hodnotu. |
|                        | Kategorie poplatku         | Vyberte výchozí kategorii poplatku. Tato hodnota se používá, když jsou skutečné údaje o poplatcích synchronizovány z Project Service Automation. Když jsou skutečné poplatky synchronizovány z Project Service Automation, pole **Kategorie** nových poplatkových transakcí v Finance je nastaveno na tuto hodnotu. |
| Výchozí nastavení skupiny projektů | Typ projektu         | Klikněte na **Nový** k přidání řádku, ve kterém můžete vybrat typ projektu a nastavit výchozí skupinu pro. Konkrétní typ projektu lze v konfiguraci vybrat pouze jednou. |
|                        | Projektová skupina        | Vyberte výchozí skupinu projektů pro vybraný typ projektu. Když jsou nové projekty synchronizovány z Project Service Automation, pole **Projektová skupina** je nastaveno na výchozí hodnotu pro typ projektu pokud jste v integrační šabloně nezadali výchozí hodnotu. |
| Výchozí nastavení typu fakturace  | Typ fakturace         | Klikněte na **Nový** k přidání řádku, ve kterém můžete vybrat typ fakturace a nastavit výchozí vlastnost řádku pro. Konkrétní typ fakturace lze v konfiguraci vybrat pouze jednou. |
|                        | Vlastnost řádku        | Vyberte výchozí vlastnost řádku pro vybraný typ fakturace. Když jsou nové odhady hodin, nové odhady výdajů nebo nové skutečné údaje synchronizovány z Project Service Automation, je pole **Vlastnost čáry** nastaveno na výchozí hodnotu pro typ fakturace. |
| Uzamčení funkce  | Nelze použít       | Vyberte funkci, kterou chcete zakázat v Finance pro projekty a smlouvy, které pocházejí z Project Service Automation. Můžete například vypnout schopnost upravovat smlouvy a projekty, vytvářet struktury rozpisu prací a zadávat časové rozvrhy v aplikaci Finance. Pole související s účetnictvím budou i nadále povolena, i když jsou v nastavení parametrů zpřístupněna. Ve výchozím nastavení jsou povoleny všechny funkce. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]