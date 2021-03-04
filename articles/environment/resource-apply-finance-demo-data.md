---
title: Použití ukázkových dat na prostředí aplikace Finance hostované v cloudu
description: Toto téma vysvětluje, jak použít ukázková data z Project Operations na prostředí Dynamics 365 Finance hostované v cloudu.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365230"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Použití ukázkových dat na prostředí aplikace Finance hostované v cloudu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

> [!IMPORTANT]
> Toto téma je použitelné pouze pro Microsoft Dynamics 365 Finance ve verzi 10.0.13 a lze ho provést pouze v prostředí hostovaném v cloudu. Kroky v tomto tématu dokončete **PŘED** použitím aktualizací kvality na prostředí.

1. Ve svém projektu LCS otevřete stránku **Podrobnosti o prostředí**. Všimněte si, že obsahuje podrobnosti potřebné pro připojení k prostředí pomocí protokolu RDP (Remote Desktop Protocol).

![Podrobnosti prostředí ](./media/1EnvironmentDetails.png)

První sada zvýrazněných přihlašovacích údajů jsou přihlašovací údaje místního účtu a obsahují hypertextový odkaz na připojení ke vzdálené ploše. Přihlašovací údaje zahrnují uživatelské jméno a heslo správce prostředí. Druhá sada přihlašovacích údajů se používá pro přihlášení k serveru SQL v tomto prostředí.

2. Připojte se vzdáleně k prostředí pomocí hypertextového odkazu v části **Místní účty** a k ověření použijte **Přihlašovací údaje místního účtu**.
3. Přejděte na části **Internetová informační služba** > **Fondy aplikací** > **AOSService** a zastavte službu. V tomto okamžiku zastavujete službu, abyste mohli pokračovat v nahrazování databáze SQL.

![Zastavit AOS](./media/2StopAOS.png)

4. Přejděte do části **Služby** a zastavte následující dvě položky:

- Microsoft Dynamics 365 Unified Operations: Služba správy dávek
- Microsoft Dynamics 365 Unified Operations: Platforma importu a exportu dat

![Zastavit služby](./media/3StopServices.png)

5. Otevřete aplikaci Microsoft SQL Server Management Studio. Přihlaste se pomocí přihlašovacích údajů serveru SQL a použijte uživatele axdbadmin a jeho heslo, uvedené na stránce LCS **Podrobnosti o prostředí**.

![SQL Server Management Studio](./media/4SSMS.png)

6. V Průzkumníku objektů zvolte **Databáze** a vyhledejte **AXDB**. Databázi nahradíte novou databází, která se nachází v [Centru stahování](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Zkopírujte soubor zip na virtuální počítač, ke kterému jste vzdáleně připojeni, a rozbalte obsah archivu.
8. V aplikaci SQL Server Management Studio pravým tlačítkem klikněte na položku **AxDB** a potom vyberte postupně **Úkoly** > **Obnovit** > **Databáze**.

![Obnova databáze](./media/5RestoreDatabase.png)

9. Vyberte **Zdrojové zařízení** a přejděte na soubor extrahovaný z archivu, který jste zkopírovali.

![Zdrojová zařízení](./media/6SourceDevice.png)

10. Vyberte položku **Možnosti** a potom vyberte možnosti **Přepsat existující databázi** a **Zavřít stávající připojení k cílové databázi**. 
11. Vyberte **OK**.

![Obnovit nastavení](./media/7RestoreSetting.png)

Obdržíte potvrzení, že obnovení AXDB proběhlo úspěšně. Po obdržení tohoto potvrzení můžete zavřít aplikaci SQL Services Management Studio.

12. Přejděte zpět na nabídku **Internetová informační služba** > **Fondy aplikací** > **AOSService** a spusťte službu AOSService.
13. Přejděte do části **Služby** a spusťte dvě služby, které jste dříve zastavili.

14. Vyhledejte nástroj AdminUserProvisioning na tomto virtuálním počítači. Hledejte soubor K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Spusťte soubor .ext pomocí své uživatelské adresy v poli **E-mailová adresa**. 
16. Vyberte položku **Odeslat**.

![Admin User Provisioning](./media/8AdminUserProvisioning.png)

Tato akce může trvat několik minut. Měla by se zobrazit potvrzovací zpráva, že uživatel správce byl úspěšně aktualizován.

17. Nakonec spusťte příkazový řádek jako správce a proveďte příkaz iisreset

![Obnova IIS](./media/9IISReset.png)

18. Ukončete relaci vzdálené plochy a na stránce LCS **Podrobnosti o prostředí** se přihlaste do prostředí a zkontrolujte, že funguje podle očekávání.

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]