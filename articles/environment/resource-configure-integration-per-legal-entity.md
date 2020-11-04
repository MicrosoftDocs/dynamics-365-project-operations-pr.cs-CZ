---
title: Konfigurace integrace Project Operations podle právnické osoby
description: Toto téma poskytuje informace o tom, jak nastavit integraci podle právnické osoby v aplikaci Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096744"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurace integrace Project Operations podle právnické osoby 

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma vás provede kroky potřebnými ke konfiguraci Dynamics 365 Project Operations podle právnické osoby.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Povolení klíče oprávnění v Dynamics 365 Finance

Chcete-li povolit požadované funkce, proveďte následující kroky.

1. V aplikaci Dynamics 365 Finance přejděte do pracovního prostoru **Správa funkcí**.
2. V poli **Seznam funkcí** vyhledejte a povolte následující funkce:
  
    - **Povolit více řádků smlouvy pro projekt**
    - **Povolit Project Operations v Dynamics 365 Customer Engagement**

> [!NOTE]
> Pokud nevidíte uvedené **Klíče oprávnění** , ověřte, zda vaše verze Finance splňuje požadavek na minimální verzi (verze aplikace 10.0.13 se všemi použitými aktualizacemi kvality nebo vyšší). Výběrem položky **Kontrola aktualizací** aktualizujte seznam funkcí.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definování scénáře nasazení Project Operations pro právnickou osobu

Aplikaci Project Operations můžete v Dynamics 365 Customer Engagement povolit na úrovni právnických osob. Můžete mít jednu právnickou osobu, která používá Project Operations v Dynamics 365 Customer Engagement pro scénáře založené na zdrojích / položkách, které nejsou na skladě. Ve stejném prostředí můžete mít jinou právnickou osobu, která používá Project Operations pro scénáře se skladovým materiálem a výrobními příkazy.

1. V Dynamics 365 Finance přejděte do nabídky **Řízení projektů a účetnictví** > **Nastavení** > **Globální parametry modulu Řízení a účetnictví projektu**.
2. V seznamu dostupných právnických osob vyberte entity, u kterých budou povoleny smlouvy s více řádky a Project Operations v Dynamics 365 Customer Engagement. Nevybírejte právnické osoby, které budou používat Project Operations pro scénáře se skladovým materiálem a výrobními příkazy.

> [!NOTE]
> Právnickou osobu lze vybrat, pouze pokud nemá žádné stávající projekty.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurace parametrů modulu Řízení projektu a účetnictví

Každá právnická osoba využívající Project Operations v Dynamics 365 Customer Engagement potřebuje sadu výchozích parametrů. Tyto parametry se konfigurují na kartě **Project Operations** ve stránce **Parametry řízení projektu a účetnictví**. K dispozici jsou tyto parametry:

  - **Výchozí hodnoty typu účtování** : Project Operations používá pevnou sadu výchozích typů účtování, které musejí být mapovány na vlastnosti řádku ve Finance. Vytvořte záznam pro každý typ účtování: **Nezadáno** , **Účtovatelné** , **Neúčtovatelné** , **Doplňkové** a **Není dostupné**.
  - **Výchozí nastavení kategorie projektu** : Vyberte výchozí kategorie projektu, které se mají použít pro každý typ transakce. Tyto výchozí hodnoty budou použity v **Deníku integrace Project Operations** a v odhadech, kde není pro skutečný projekt zadána žádná kategorie transakcí.
  - **Prognózy** : Vyberte model prognózy, který se použije pro odhady času a výdajů.
