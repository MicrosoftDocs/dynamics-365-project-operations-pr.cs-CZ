---
title: Použití ukázkového nastavení a data konfigurace
description: Toto téma poskytuje informace o tom, jak použít ukázková nastavení a konfigurační data pro Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073645"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Použít ukázkové nastavení a konfigurační data pro omezené nasazení Project Operations - od obchodu po pro forma fakturaci

_**Omezené nasazení - dohoda o pro forma fakturaci_

1. Stáhněte si [Balíček kmenových dat](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Přejděte do složky *ProjOpsDemoDataSetupAndMaster - integrovaný CMT* a spusťte soubor *DataMigrationUtility*.
3. Na straně 1 Průvodce konfigurací migrace (CMT) Common Data Service, vyberte **Importovat data** a poté vyberte **Pokračovat**.

![Migrace konfigurace](./media/1ConfigurationMigration.png)

4. Na stránce 2 průvodce CMT vyberte **Microsoft 365** jako **Typ nasazení**.
5. Zaškrtněte políčka **Zobrazit seznam dostupných organizací** a **Zobrazit pokročilé**.
6. Vyberte oblast vašeho klienta, zadejte své přihlašovací údaje a pak vyberte **Přihlásit se**.

![Přihlášení do konfigurace](./media/2ConfigurationSignin.png)

7. Na stránce 3 ze seznamu organizací v klientovi vyberte, do které organizace chcete importovat ukázková data, a poté vyberte **Přihlásit se**.
8. Na stránce 4 vyberte soubor zip *MasterAndSetupData* z rozbalené složky *ProjOpsDemoDataSetupAndMaster - integrovaný CMT*.

![Soubor ZIP](./media/3ZipFile.png)

![Vyberte soubor.](./media/4SelectAFile.png)

9. Po výběru souboru zip vyberte **Importovat data**.

![Import dat](./media/5ImportData.png)

10. Import bude probíhat přibližně dvě až deset minut v závislosti na rychlosti vaší sítě. Po dokončení ukončete průvodce CMT. 
11. Zkontrolujte ve své organizaci data v následujících 20 entitách:

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
- Podrobnosti četnosti faktury
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
