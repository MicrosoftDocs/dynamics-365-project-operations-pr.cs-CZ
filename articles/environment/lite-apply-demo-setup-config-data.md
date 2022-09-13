---
title: Použití ukázkového nastavení a data konfigurace – omezené
description: Tento článek poskytuje informace o tom, jak použít demonstrační nastavení a konfigurační data v Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2022
ms.locfileid: "9409969"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Použití ukázkového nastavení a data konfigurace pro Project Operations – omezené 

_**Omezené nasazení - dohoda o pro forma fakturaci_



## <a name="prerequisites"></a>Předpoklady

Před zahájením konfigurace musíte mít mít zřízeno prostředí Dataverse pro Dynamics 365 Project Operations.


## <a name="instructions"></a>Pokyny

1. Stáhněte si [Balíček kmenových dat](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Přejděte do složky *ProjOpsSampleSetupData – pouze CMT CE* a spusťte spustitelný soubor *DataMigrationUtility*.
3. Na straně 1 Průvodce konfigurací migrace (CMT) Common Data Service, vyberte **Importovat data** a poté vyberte **Pokračovat**.

    ![Migrace konfigurace.](./media/1ConfigurationMigration.png)

4. Na stránce 2 průvodce CMT vyberte **Microsoft 365** jako **Typ nasazení**.
5. Zaškrtněte políčka **Zobrazit seznam dostupných organizací** a **Zobrazit pokročilé**.
6. Vyberte oblast vašeho klienta, zadejte své přihlašovací údaje a pak vyberte **Přihlásit se**.

   ![Přihlášení do konfigurace.](./media/2ConfigurationSignin.png)

7. Na stránce 3 ze seznamu organizací v klientovi vyberte, do které organizace chcete importovat ukázková data, a poté vyberte **Přihlásit se**.
8. Na stránce 4 vyberte soubor zip *SampleSetupAndConfigData* z rozbalené složky *ProjOpsSampleSetupData – CE pouze CMT*.

   ![Soubor ZIP.](./media/3ZipFile.png)

   ![Vyberte soubor.](./media/4SelectAFile.png)

9. Po výběru souboru zip vyberte **Importovat data**.

   ![Importovat data.](./media/5ImportData.png)

10. Import bude probíhat přibližně dvě až deset minut v závislosti na rychlosti vaší sítě. Po dokončení ukončete průvodce CMT. 
11. Zkontrolujte ve své organizaci data v následujících 18 entitách:

    -   Měna
    -   Účet
    -   Organizační jednotka
    -   Kontakt
    -   Jednotka
    -   Skupina jednotek
    -   Ceník
    -   Ceník projektových parametrů 
    -   Frekvence faktur
    -   Kategorie rezervovatelného zdroje
    -   Kategorie transakce
    -   Kategorie výdaje
    -   Cena role
    -   Cena kategorie transakce
    -   Charakteristika
    -   Rezervovatelný zdroj
    -   Přidružení kategorie rezervovatelného zdroje
    -   Charakteristika rezervovatelného zdroje

    ![Dokončit import.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
