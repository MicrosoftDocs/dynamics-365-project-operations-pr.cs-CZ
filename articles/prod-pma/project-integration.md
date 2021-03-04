---
title: Integrace aplikace Microsoft Project Client
description: Plánování a údržba projektového harmonogramu mohou být složité, a proto projektoví manažeři musí používat nástroje, které jim pomohou tento úkol zvládnout. Integrace s klientem Microsoft Project Client poskytuje podporu pro otevření a správu strukturovaného rozpisu prací na projektu.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073841"
---
# <a name="microsoft-project-client-integration"></a>Integrace aplikace Microsoft Project Client

[!include [banner](../includes/banner.md)]

Plánování a údržba projektového harmonogramu mohou být složité, a proto projektoví manažeři musí používat nástroje, které jim pomohou tento úkol zvládnout. Integrace s klientem Microsoft Project Client poskytuje podporu pro otevření a správu strukturovaného rozpisu prací na projektu. Manažer projektu může publikovat jakékoli změny zpět do strukturovaného rozpisu prací na projektu v Dynamics 365 Finance.

> [!NOTE]
> Pokud používáte červencovou aktualizaci (verze 10.0.4), musíte nainstalovat aktualizace KB 4054797 a 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurace doplňku Microsoft Project Client
Chcete-li povolit integraci s doplňkem Microsoft Project Client, je nutné nainstalovat doplněk Microsoft Dynamics 365 do aplikace Microsoft Project klienta uživatele. To se provádí otevřením **pracovního prostoru pro správu projektů**.

•   Klikněte na příkaz **Konfigurace doplňku klienta projektu** v části **Odkazy** > **Nastavení** pracovního prostoru.

•   Klikněte na položku **Otevřít** a po výzvě klikněte na možnost **Spustit**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Otevření a úprava stávajícího konceptu strukturovaného rozpisu prací v doplňku Microsoft Project Client
Pokud má projekt v Dynamics 365 Finance již vytvořený strukturovaný rozpis prací, lze strukturovaný rozpis prací otevřít v aplikaci Microsoft Project Client, pokud je ve stavu konceptu. Chcete-li otevření provést ze stránky **Projekt** , klikněte na odkaz **Otevřít v Microsoft Project** na kartě **Plán**. Tuto stránku lze otevřít také z aplikace Microsoft Project Client kliknutím na možnost **Otevřít** na kartě **Microsoft Dynamics 365**. V seznamu vyberte **Právnická osoba** a **Projekt**.

> [!NOTE]
> Pokud jako prohlížeč používáte Internet Explorer, budete muset kliknout na **Uložit** a ručně otevřít soubor z umístění, do kterého je stažen. Nebo klikněte **Uložit a otevřít** a otevřete soubor v aplikaci Microsoft Project Client. Při ukládání neměňte název souboru.

Před provedením jakýchkoli úprav souboru pomocí aplikace Microsoft Project Client je nutné jej rezervovat. Klikněte na příkaz **Rezervovat** na kartě **Microsoft Dynamics 365**. Rezervace nedovolí ostatním uživatelům upravovat současně strukturovaný rozpis prací v rámci aplikace Finance. Chcete-li po dokončení všech úprav strukturovaný rozpis prací publikovat, klikněte na **Vrátit se změnami** na kartě **Microsoft Dynamics 365**.

Pokud již byl projektový tým přidán do projektu v aplikaci Finance, seznam zdrojů se naplní členy týmu. Pokud projektový tým ještě nebyl do projektu přidán, můžete vybrat zdroje a vytvořit tým uvnitř aplikace Microsoft Project Client kliknutím na tlačítko **Zdroje** na kartě **Microsoft Dynamics 365**. 

Následující data budou synchronizována zpět do Finance jako součást procesu vrácení se změnami:

•   Název úkolu

•   Počáteční datum

•   Datum dokončení

•   Předchůdci

•   Názvy zdrojů

•   Kategorie

•   Kategorie zdroje

•   Pracovní doba

•   Poznámky

•   Priorita

> [!NOTE]
> Pokud do souboru aplikace Microsoft Project Client přidáte jakékoli další sloupce, nebudou do souboru uloženy a po opětovném otevření souboru se nezobrazí.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Vytvoření strukturovaného rozpisu prací pro existující projekt v aplikaci Microsoft Project Client
Chcete-li vytvořit nový strukturovaný rozpis prací v aplikaci Microsoft Project Client, postupujte takto:


1.  Otevřete aplikaci Microsoft Project Client.

2.  Na kartě **Microsoft Dynamics 365** klikněte na položku **Otevřít**.

3.  Vyberte hodnotu **Právnická osoba** pro projekt.

4.  Vyberte **Projekt**.

5.  Klikněte na příkaz **Rezervovat** na kartě **Microsoft Dynamics 365**.

6.  Až budete připraveni publikovat do aplikace Finance, klikněte na **Vrátit se změnami** na kartě **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Nahrazení stávajícího strukturovaného rozpisu prací pro existující projekt v aplikaci Microsoft Project Client
Chcete-li vytvořit nový strukturovaný rozpis prací pomocí aplikace Microsoft Project Client a nahradit stávající strukturovaný rozpis prací pro existující projekt, postupujte takto:

1.  Otevřete aplikaci Microsoft Project Client.

2.  Vytvořte plán v aplikaci Microsoft Project Client.

3.  Na kartě **Microsoft Dynamics 365** klikněte na příkaz **Uložit změny** > **Nahradit stávající projekt**.

4.  Vyberte hodnotu **Právnická osoba** pro projekt.

5.  Vyberte **Projekt**.

6.  Klikněte na **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Vytvoření nového projektu v aplikaci Microsoft Project Client


1.  Otevřete aplikaci Microsoft Project Client.

2.  Vytvořte plán v aplikaci Microsoft Project Client.

3.  Na kartě **Microsoft Dynamics 365** klikněte na příkaz **Uložit změny** > **Uložit do nového projektu**.

4.  Vyberte hodnotu **Právnická osoba** pro projekt.

5.  Zadejte **ID projektu** , pokud je třeba.

6.  Zadejte **Název projektu**.

7.  Zvolte hodnoty **Typ projektu** , **Projektová skupina** a **ID smlouvy o projektu**. Alternativně můžete vytvořit novou projektovou smlouvu kliknutím na možnost **Nový**.

8.  Vyberte **Kalendář** , který bude použit pro zajišťování zdrojů.

11. Klikněte na **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]