---
title: Nastavení a použití dat konfigurace ve službě Common Data Service pro Project Operations
description: Toto téma poskytuje informace o tom, jak nastavit a použít konfigurační data v aplikaci Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948800"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a>Nastavení a použití dat konfigurace ve službě Common Data Service pro Project Operations

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

## <a name="install-setup-and-configuration-data"></a>Instalace nastavení a dat konfigurace

1. Stáhněte, odblokujte a rozbalte soubor [Balíček údajů o nastavení a konfiguraci](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Přejděte do rozbalené složky a spusťte soubor *DataMigrationUtility*.
3. Na straně 1 Průvodce konfigurací migrace (CMT) Common Data Service, vyberte **Importovat data** a poté vyberte **Pokračovat**.

![Migrace konfigurace](./media/1ConfigurationMigration.png)

4. Na stránce 2 průvodce CMT vyberte **Office 365** jako **Typ nasazení**.
5. Zaškrtněte políčka **Zobrazit seznam dostupných organizací** a **Zobrazit pokročilé**.
6. Vyberte oblast vašeho klienta, zadejte své přihlašovací údaje a vyberte příkaz **Přihlásit se**.

![Přihlášení do konfigurace](./media/2ConfigurationSignin.png)

7. Na stránce 3 vyberte ze seznamu organizací v klientovi organizaci, do které chcete importovat ukázková data, a vyberte příkaz **Přihlásit se**.
8. Na stránce 4 vyberte soubor zip *SampleSetupAndConfigData* z rozbalené složky.

![Výběr souboru ZIP](./media/3ZipFile.png)

![Vyberte soubor.](./media/4SelectAFile.png)

9. Po výběru souboru zip vyberte **Importovat data**.

![Importovat data](./media/5ImportData.png)

10. Import bude probíhat přibližně dvě až deset minut v závislosti na rychlosti vaší sítě. Po dokončení importu ukončete průvodce CMT. 
11. Zkontrolujte ve své organizaci data v následujících 19 entitách:

  - Měna
  - Organizační jednotka
  - Kontakt
  - Daňová skupina
  - Skupina zákazníků
  - Jednotka
  - Skupina jednotek
  - Ceník
  - Ceník projektových parametrů
  - Frekvence faktur
  - Kategorie rezervovatelného zdroje
  - Kategorie transakce
  - Kategorie výdaje
  - Cena role
  - Cena kategorie transakce
  - Charakteristika
  - Rezervovatelný zdroj
  - Přidružení kategorie rezervovatelného zdroje
  - Charakteristika rezervovatelného zdroje

![Dokončit import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Aktualizace konfigurací Project Operations

1. Přejděte do prostředí CE. Najdete jej otevřením [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com/environments), kde vyberete prostředí a poté **Otevřené prostředí**. 

![Otevření prostředí](./media/7OpenEnvironment.png)

2. Přejděte do nabídky **Projekty** > **Zdroje** a poté vyberte příkaz **Nový** k vytvoření rezervovatelného zdroje pro vašeho uživatele.

![Rezervovatelné zdroje](./media/8BookableResources.png)

3. Na kartě **Obecné** vyberte uživatele správce. Ověřte, zda se časové pásmo shoduje s časovým pásmem, ve kterém se nacházíte. 

![Nový rezervovatelný zdroj](./media/9NewBookableResource.png)

4. Na kartě **Plánování** v poli **Společnost** vyberte společnost **USPM** a poté vyberte příkaz **Uložit**. 

![Karta Plánování](./media/10SchedulingTab.png)

5. Vyberte kartu **Pracovní doba**.  

![Pracovní doba](./media/11WorkHours.png)

6. Poklepejte na libovolnou hodnotu v kalendáři a vyberte příkaz **Upravit** > **Všechny události v řadě**. 

![Pracovní kalendář](./media/12WorkCalendar.png)

7. Změňte pracovní dobu na osmi (8) hodinový pracovní den, označte víkendy jako dny pracovního klidu a ujistěte se, že časové pásmo odpovídá vašemu. 
8. Zvolte **Uložit a zavřít**.

![Aktualizace kalendáře](./media/13UpdateCalendar.png)

9. Přejděte do nabídky **Nastavení** > **Šablony kalendáře** a vyberte položku **Nová**.
 
 ![Šablony kalendářů](./media/14CalendarTemplates.png)
 
 10. Zadejte název, vyberte zdroj šablony, který jste vytvořili, a pak vyberte příkaz **Uložit**. 
 
 ![Uložení šablony kalendáře](./media/15SaveCalendarTemplate.png)
 
 11. Přejděte do části **Parametry** a dvakrát klikněte na záznam. 
 
 ![Projektové parametry](./media/16ProjectParameters.png)
 
12. Aktualizujte následující pole:

 - **Výchozí společnost**: USPM
 - **Výchozí organizační jednotka**: Contoso Robotics Global
 - **Četnost faktur**: Sedmý a poslední den
 - **Šablona pracovní doby**: Změňte na šablonu, kterou jste vytvořili.

13. Zvolte **Uložit**. 

![Aktualizované projektové parametry](./media/17UpdatedProjectParameters.png)
