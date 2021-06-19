---
title: Aktualizace Project Operations v prostředí Finance
description: Tohle téma poskytuje informace, jak aktualizovat Project Operations v prostředí Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011048"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Aktualizace Project Operations v prostředí Finance

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_


Tohle téma poskytuje informace, jak aktualizovat Dynamics 365 Project Operations v prostředí Dynamics 365 Finance. K aktualizaci Project Operations na Update 5 (UR5) jsou vyžadovány tři postupy:

- [Importujte balíček do projektu náhledu](#import)
- [Nainstaluje aktualizaci](#apply)
- [Aktualizujte prostředí Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importujte balíček do projektu LCS

1. Přihlaste se do [Lifecycle Services (LCS)](https://lcs.dynamics.com/) jako vlastník projektu nebo manažer prostředí.
2. Ze seznamu projektů vyberte svůj projekt LCS.
3. Na stránce **Projekt** ve skupině **Prostředí** otevřete prostředí, které chcete aktualizovat.
4. Ověřte, že prostředí běží. Pokud není spuštěno, spusťte prostředí.
5. V části **Nová verze** pod **Dostupné aktualizace** vyberte **Zobrazit aktualizaci** u 10.0.15.

![Tlačítko Zobrazit aktualizaci](media/view-update.png)

6. Na stránce **Binární aktualizace** vyberte možnost **Uložit balíček**.
7. Na stránce **Zkontrolovat a uložit aktualizace** vyberte možnost **Uložit balíček**.
8. V podokně **Uložit balíček do knihovny prostředků**, které se otevře, zadejte název balíčku a poté vyberte **Uložit balíček**.
9. Když LCS dokončí ukládání balíčku, aktivuje se tlačítko **Hotovo**. Vyberte **Hotovo**. LCS ověří balíček. Ověření může trvat několik minut nebo až hodinu.


## <a name="apply-the-package-update"></a><a name="apply"></a>Nainstalujte aktualizaci balíčku

1. V LCS na stránce **Podrobnosti o prostředí** vyberte **Udržovat** > **Použít aktualizace**.
2. Ze seznamu vyberte balíček, který jste dříve uložili, a poté vyberte **Použít**.
3. Vyberte **Ano** k potvrzení, že chcete balíček nasadit.

![Dialogové okno Potvrdit nasazení balíčku](media/confirm-package-deployment.png)

4. Vyberte **Ano** k potvrzení, že chcete aplikaci aktualizovat.

![Dialogové okno Potvrdit aktualizaci aplikace](media/confirm-application-update.png)

Spustí se nasazení a aktualizace aplikace. 

Na stránce **Podrobnosti o prostředí** se v pravém horním rohu aktualizuje stav prostředí **Servis**. Aktualizace bude dokončena přibližně za dvě hodiny. Informace o vydání aplikace se aktualizují na **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** a stav prostředí se aktualizuje na **Nasazeno**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Aktualizace prostředí Dataverse

1. Přihlaste se k [centru pro správu Power Platform](https://admin.powerplatform.com/).
2. V seznamu vyhledejte a otevřete prostředí, které jste použili k instalaci Project Operations.
3. Na stránce **Prostředí** vyberte **Zdroj** > **Aplikace Dynamics 365**.
4. V seznamu vyhledejte **Microsoft Dynamics 365 Project Operations** a ve sloupci **Stav** vyberte **Aktualizace je k dispozici**.
5. Zaškrtněte **Souhlasím s podmínkami služby** a poté vyberte **Aktualizace**. Bude nainstalována nejnovější verze řešení.

Po dokončení instalace budete mít nainstalovanou verzi 4.5.0.134.

## <a name="configure-new-features"></a>Konfigurace nových funkcí

### <a name="enable-dual-write-mapping"></a>Aktivace mapování duálního zápisu

Po dokončení aktualizace v prostředí Finance a Dataverse prostředí můžete povolit požadovaná mapování duálního zápisu. K povolení mapování duálního zápisu proveďte následující postupy.

- [Aktualizujte nastavení zabezpečení v prostředí Customer Engagement](#security)
- [Aktualizace datových entit](#refresh)
- [Aktualizujte a spusťte mapování duálního zápisu](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Aktualizujte nastavení zabezpečení v prostředí Dataverse

Následující aktualizace bezpečnostních oprávnění pro entity jsou vyžadovány jako součást aktualizace UR5.

1. V prostředí Dataverse přejděte do **Nastavení** a ve skupině **Systém** vyberte **Zabezpečení**.

![Nastavení prostředí Dataverse](media/Picture21.png)

2. Vyberte **Role zabezpečení**.
3. Ze seznamu rolí vyberte **uživatel aplikace duálního zápisu** a vyberte kartu **Vlastní entity**. 
4. Ověřte, zda role má oprávnění **Číst** a **Připojit k** pro:

      - **Typ směnného kurzu měny**
      - **Účtová osnova** 
      - **Fiskální kalendář** 
      - **Registr**

5. Po aktualizaci role zabezpečení přejděte na **Nastavení** > **Zabezpečení** > **Týmy**. Ověřte, že role **uživatel aplikace dvojitého zápisu** byla na tým aplikována. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Aktualizujte datové entity z aktualizace

1. Ve prostředí Finance otevřete pracovní prostor **Správa dat** a poté otevřete stránku **Parametry rámce**.
2. Na kartě **Nastavení entity** kartu vyberte **Obnovit seznam entit**.
3. Vyberte **Zavřít** pro potvrzení aktualizace entity.

 > [!NOTE]
 > Tento proces zabere přibližně 20 minut. Až bude aktualizace dokončena, budete upozorněni.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Aktualizace mapování duálního zápisu

1. V pracovním prostoru **Správa dat** vyberte **Duální zápis**.
2. Vyberte **Použít řešení**, vyberte obě řešení v seznamu a poté vyberte **Použít**.
3. Na stránce **Duální zápis** vyberte následující mapové tabulky a poté vyberte **Stop**.

    - **Skutečné hodnoty integrace Project Operations (msdyn_actuals)**
    - **Kategorie výdajů projektu integrace Project Operations (msdyn_expensecategories)**
    - **Entita exportu skutečných hodnot výdajů projektu integrace Project Operations (msdyn_expenses)**

4. Na stránce **Verze tabulky mapy** použijte novou verzi mapy na každou ze tří entit.
5. Na stránce **Duální zápis** vyberte příkaz Spustit a restartujte mapy.
6. Ze seznamu map vyberte mapu **Registr (msdyn_ledgers)** se všemi předpoklady a zaškrtněte **Počáteční synchronizace**. 
7. V poli **Předloha pro počáteční synchronizaci** vyberte **Aplikace Finance and Operations** a poté vyberte **Spustit**.
 
 ![Synchronizace mapy registru](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]