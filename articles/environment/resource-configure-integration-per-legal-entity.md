---
title: Konfigurace integrace Project Operations podle právnické osoby
description: Tento článek poskytuje informace o nastavení integrace právním subjektem v Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914670"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurace integrace Project Operations podle právnické osoby 

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Tento článek vás provede kroky potřebnými ke konfiguraci Dynamics 365 Project Operations podle právnické osoby.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Povolte klíče funkcí v Dynamics 365 Finance

Chcete-li povolit požadované funkce, proveďte následující kroky.

1. V Dynamics 365 Finance přejděte do pracovního prostoru **Správa funkcí**.
2. V poli **Seznam funkcí** vyhledejte a povolte následující funkce:
  
    - **Povolit více řádků smlouvy pro projekt**
    - **Povolte Project Operations v Dynamics 365 Customer Engagement**

> [!NOTE]
> Pokud nevidíte uvedené **Klíče oprávnění**, ověřte, zda vaše verze Finance splňuje požadavek na minimální verzi (verze aplikace 10.0.13 se všemi použitými aktualizacemi kvality nebo vyšší). Výběrem položky **Kontrola aktualizací** aktualizujte seznam funkcí.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definování scénáře nasazení Project Operations pro právnickou osobu

Můžete povolit Project Operations v Dynamics 365 Customer Engagement na úrovni právního subjektu. Můžete mít jednu právnickou osobu používající Project Operations na Dynamics 365 Customer Engagement pro cénáře založené na zdrojích/položkách, které nejsou na skladě. Ve stejném prostředí můžete mít jinou právnickou osobu, která používá Project Operations pro scénáře se skladovým materiálem a výrobními příkazy.

1. V Dynamics 365 Finance přejděte na **Projektové řízení a účetnictví** > **Založit** > **Globální řízení projektů a účetní parametry**.
2. V seznamu dostupných právnických osob vyberte subjekty, pro které bude povoleno více řádků smlouvy a funkce Project Operations on Dynamics 365 Customer Engagement. Nevybírejte právnické osoby, které budou používat Project Operations pro scénáře se skladovým materiálem a výrobními příkazy.

> [!NOTE]
> Právnickou osobu lze vybrat, pouze pokud nemá žádné stávající projekty.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurace parametrů modulu Řízení projektu a účetnictví

Každá právnická osoba používající Project Operations v Dynamics 365 Customer Engagement potřebuje sadu výchozích parametrů. Tyto parametry se konfigurují na kartě **Project Operations** ve stránce **Parametry řízení projektu a účetnictví**. K dispozici jsou tyto parametry:

  - **Výchozí hodnoty typu účtování**: Project Operations používá pevnou sadu výchozích typů účtování, které musejí být mapovány na vlastnosti řádku ve Finance. Vytvořte záznam pro každý typ účtování: **Nezadáno**, **Účtovatelné**, **Neúčtovatelné**, **Doplňkové** a **Není dostupné**.
  - **Výchozí nastavení kategorie projektu**: Vyberte výchozí kategorie projektu, které se mají použít pro každý typ transakce. Tyto výchozí hodnoty budou použity v **Deníku integrace Project Operations** a v odhadech, kde není pro skutečný projekt zadána žádná kategorie transakcí.
  - **Prognózy** : Vyberte model prognózy, který se použije pro odhady času a výdajů.


[!INCLUDE[footer-include](../includes/footer-banner.md)]