---
title: Zřízení nového prostředí
description: Toto téma poskytuje informace o zřízení nového prostředí Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 044a942a068b33318b98041cc94944d90c1d63c3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121165"
---
# <a name="provision-a-new-environment"></a>Zřízení nového prostředí

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Toto téma poskytuje informace o tom, jak zřídit nové prostředí Dynamics 365 Project Operations pro scénáře založené na zdrojích / neuskladněných zásobách.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Povolení automatického zřizování Project Operations v projektu LCS

Pomocí následujících kroků povolíte tok automatického zřizování Project Operations pro váš projekt LCS.

1. Přejděte do [LCS](https://lcs.dynamics.com/v2) a vyberte dlaždici **Správa funkce náhledu**.
2. V seznamu **Funkce Preview** vyberte **Funkce Project Operations** a poté výběrem možnosti **Povolit funkci verze Preview** povolte aplikaci Project Operations.

> [!NOTE]
> Tento krok se provádí pouze jednou za projekt LCS.

## <a name="provision-a-project-operations-environment"></a>Zřízení prostředí Project Operations

1. Otevřete nové [demo prostředí Dynamics 365 Finance](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) nebo nasazení [sandboxu / produkčního prostředí](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Projděte jednotlivé obrazovky průvodce **Zřízení prostředí**. 

> [!IMPORTANT]
> Zkontrolujte, zda je vybrána verze aplikace 10.0.13 nebo vyšší.

3. Chcete-li zřídit Project Operations, vyberte v části **Pokročilé nastavení** položku **Common Data Service**. 
4. Povolte **Nastavení Common Data Service** výběrem **Ano** a poté zadejte informace do požadovaných polí:

  - Jméno
  - Oblast
  - Jazyk
  - Měna
 
5. V poli **Šablona Common Data Service** vyberte **Project Operations** 

6. Vyberte typ prostředí pro vaše nasazení. Zkušební verze založená na předplatném vám umožní nasadit prostředí CDS po dobu 30 dnů. 

![Nastavení nasazení](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Výběrem možnosti **Souhlasím** potvrďte podmínky služby a poté se výběrem možnosti **Hotovo** vraťte do nastavení nasazení.

![Souhlas s nasazením](./media/2DeploymentConsent.png)

7. Vyplňte zbývající požadovaná pole v průvodci a potvrďte nasazení. Čas zřízení prostředí se liší podle typu prostředí. Zřizování může trvat až šest hodin.

  Po úspěšném dokončení nasazení se prostředí zobrazí jako **Nasazeno**.

8. Chcete-li potvrdit úspěšné nasazení prostředí, vyberte možnost **Přihlásit se** a potvrďte dokončení přihlášením do prostředí.

![Podrobnosti prostředí ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Použití ukázkových dat Project Operations Finance (volitelný krok)

Ukázková data Project Operations Finance se použijí na prostředí hostované v cloudu s verzí služby 10.0.13 podle popisu v [tomto článku](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Použití aktualizací v prostředí Finance

Project Operations vyžaduje prostředí Finance s verzí aplikace **10.0.13 (10.0.569.20009)** nebo vyšší.

K získání této verze možná budete muset na svém prostředí Finance použít aktualizace kvality.

1. V LCS, na stránce **Podrobnosti o prostředí** v sekci **Dostupné aktualizace** vyberte možnost **Zobrazit aktualizaci**.

![Zobrazení aktualizací](./media/5ViewUpdates.png)

2. Na stránce **Binární aktualizace** vyberte možnost **Uložit balíček.**

![Uložení balíčku](./media/6SavePackage.png)

3. Klikněte na položku **Vybrat vše** a pak vyberte příkaz **Uložit balíček**.

![Kontrola a ukládání aktualizací](./media/7ReviewAndSaveUpdates.png)

4. Zadejte název a popis balíčku a poté vyberte příkaz **Uložit**. Tento proces může nějakou dobu trvat (v závislosti na rychlosti připojení k internetu).

![Nahrání balíčku do knihovny prostředků](./media/8UploadPackageToAssetsLibrary.png)

5. Po uložení balíčku vyberte možnost **Hotovo** a uložte tento balíček do knihovny prostředků ve vašem projektu LCS.

Uložení a ověření balíčku může trvat až 15 minut.

6. Chcete-li použít aktualizaci, přejděte na stránku **Podrobnosti o prostředí** v LCS a vyberte příkaz **Údržba** > **Použít aktualizace**.

![Údržba prostředí](./media/9MaintainEnvironment.png)

7. V seznamu aktualizací vyberte balíček, který jste vytvořili, a vyberte příkaz **Použít**.

![Instalace aktualizací](./media/10ApplyUpdates.png)

Údržba prostředí bude nějakou dobu trvat. Po dokončení se prostředí vrátí do nasazeného stavu.

![Nasazené prostředí](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Vytvoření připojení s duálním zápisem 

1. V projektu LCS přejděte na stránku **Podrobnosti o prostředí**.
2. V části **Informace o prostředí Common Data Service** vyberte možnost **Odkaz na CDS pro aplikace**.
3. Po vytvoření odkazu vyberte znovu možnost **Odkaz na CDS pro aplikace**. Budete přesměrováni na duální zápis ve Finance.

![Odkaz na CDS](./media/12LinktoCDS.png)

4. Výběrem položky **Použít řešení** získáte přístup k entitám, které budou mapovány v integraci.

![Použít řešení](./media/13ApplySolutions.png)

5. Vyberte obě řešení **Mapa entit duálního zápisu Dynamics 365 Finance and Operations** a **Mapa entit duálního zápisu Dynamics 365 Project Operations** a potom vyberte příkaz **Použít**.

![Potvrzení řešení](./media/14ConfirmSolutions.png)

Poté, co je řešení použito, se na prostředí použijí entity duálního zápisu.

![Použití řešení](./media/15ApplyingSolutions.png)

Po použití entit se v prostředí zobrazí všechna dostupná mapování.

![Mapy duálního zápisu](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Po aktualizaci aktualizujte datové entity

1. Ve Finance přejděte do pracovního prostoru **Správa dat**.

![Pracovní prostor správy dat](./media/16DataManagement.png)

2. Vyberte dlaždici **Parametry architektury**.

![Parametry architektury](./media/17FrameworkParameters.png)

3. Na stránce **Nastavení entity** vyberte možnost **Aktualizovat seznam entit**.

![Aktualizovat seznam entit](./media/18RefreshEntityList.png)

Aktualizace bude trvat přibližně 20 minut. Po dokončení obdržíte upozornění.

![Potvrzení aktualizace](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Spuštění mapování duálního zápisu Project Operations

1. V projektu LCS přejděte na stránku **Podrobnosti o prostředí**.
2. V části **Informace o prostředí Common Data Service** vyberte možnost **Odkaz na CDS pro aplikace**. Poté, co vyberete odkaz, budete přesměrováni na seznam entit v mapováních.
3. Spusťte mapování podle popisu v následující tabulce. Postupujte podle níže uvedené sekvence.

| **Mapování entity** | **Aktualizovat entity** | **Počáteční synchronizace** | **Předloha pro počáteční synchronizaci** | **Spustit požadavky** | **Počáteční synchronizace požadavků** |
| --- | --- | --- | --- | --- | --- |
| **Role zdrojů projektu pro všechny společnosti (bookableresourcecategories)** | No | Ano | Common Data Service | No | Neuvedeno |
| **Právnické osoby (cdm\_companies)** | No | Ano | Aplikace Finance and Operations | No | Neuvedeno |
| **Skutečné hodnoty integrace Project Operations (msdyn\_actuals)** | No | No | Neuvedeno | Ano | No |
| **Řádky smlouvy založené na projektu (salesorderdetails)** | No | No | Neuvedeno | No | No |
| **Entita integrace pro vztahy projektových transakcí (msdyn\_transactionconnections)** | No | No | Neuvedeno | No | Neuvedeno |
| **Milníky řádku smlouvy integrace Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | Neuvedeno | No | Neuvedeno |
| **Entita integrace Project Operations pro odhady výdajů (msdyn\_estimateslines)** | No | No | Neuvedeno | No | Neuvedeno |
| **Entita exportu kategorie výdajů projektu integrace Project Operations (msdyn\_expensecategories)** | No | No | Neuvedeno | No | Neuvedeno |
| **Entita exportu výdajů projektu integrace Project Operations (msdyn\_expenses)** | Ano | No | Neuvedeno | No | Neuvedeno |
| **Entita integrace Project Operations pro odhady hodin (msdyn\_resourceassignments)** | Ano | No | Neuvedeno | No | Neuvedeno |


4. Chcete-li entitu aktualizovat, vyberte název mapy a poté vyberte příkaz **Aktualizovat entity**. 


![Aktualizovat mapu](./media/20RefreshMapping.png)

5. Po dokončení aktualizace spusťte mapu. Před povolením další mapy ověřte, zda je mapa v tabulce ve stavu **Běh**. Spuštění map s větším počtem předpokladů může trvat delší dobu.

Chcete-li spustit mapu s předpoklady, zapněte přepínač **Zobrazit související mapy entit**. Pokud je v tabulce **Počáteční synchronizace požadavků** nastavena na **Ne**, ověřte, zda příznak **Počáteční synchronizace** má hodnotu **Vypnuto** ve všech mapách požadavků, než ji spustíte.

![Spuštění mapy](./media/21RunMap.png)

6. Ověřte, zda jsou všechny mapy související s projektem v běžícím stavu.

![Všechny mapy běží](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Použití dat konfigurace v prostředí CDS pro Project Operations (volitelně)

Pokud jste použili ukázková data v prostředí Finance, viz [Nastavení a použití konfiguračních dat v Common Data Service pro Project Operations](resource-apply-pro-setup-config-data.md) pro použití ukázkových dat v prostředí CDS.


Vaše prostředí Project Operations je nyní zřízeno a nakonfigurováno. 
