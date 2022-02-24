---
title: Vytvořit nový projekt
description: Toto téma obsahuje informace o způsobu vytvoření nového projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270715"
---
# <a name="create-a-new-project"></a>Vytvořit nový projekt

[!include [banner](../includes/banner.md)]

Pomocí následujících kroků vytvořte nový projekt.

1. Na stránce **Správa projektu** vyberte **Nový projekt** a zadejte následující hodnoty:

    - **Typ projektu:** Čas a materiál
    - **Název projektu:** Fáze 2 upgradu XYZ
    - **Projektová skupina:** TM\_WIP
    - **ID projektové smlouvy:** 00000002

2. Vyberte příkaz **Vytvořit projekt**.

## <a name="assign-a-resource-to-a-project"></a>Přiřazení zdroje k projektu

1. Na stránce **Pracovníci** vyberte v seznamu **Pracovníci** záznam pro toho pracovníka, kterému jste předtím přiřadili kompetence, a otevřete záznam pracovníka.
2. V podokně akcí na kartě **Projekt** vyberte ve skupině **Nastavení** příkaz **Přiřadit projekty**.
3. Na stránce **Přiřazení projektů ověření prostředku** na kartě **Projekty** v poli **Přidat projekt k vybraným projektům** filtrujte podle projektu **Fáze 2 upgradu XYZ**.
4. V podokně **Zbývající projekty** vyberte projekt a poté jej kliknutím na tlačítko se šipkou přidejte do podokna **Vybrané projekty**.

Můžete také podle potřeby přiřadit kategorie ke zdroji. Typ kategorie je buď **Náklady** nebo **Výnosy**. Typ kategorie určuje vaše organizace. Pokud zdroji nejsou přiřazeny žádné kategorie, vyhledá Finance výchozí kategorii na základě hodinových cen nákladů a výnosů.

## <a name="set-up-project-resource-and-role-characteristics"></a>Nastavení charakteristik projektového zdroje a role

Manažer projektu může použít funkci projektového zajišťování zdrojů k vytvoření rolí, které jsou pro projekt vyžadovány. Role lze použít, pokud jsou potvrzené zdroje stále neznámé, když probíhá rezervace zdrojů. Role lze dočasně rezervovat jako plánované zdroje, abyste mohli pokračovat ve fázích plánování projektu.

[![Příklad role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scénář:** Společnost Contoso byla najata, aby dokončila projekt Čas a materiál, který má schválenou chartu projektu. Nižší projektový manažer stále dokončuje rozsah projektu. Správce prostředků aktuálně identifikuje konkrétní zdroje, které budou vyhrazeny pro práci na novém projektu. Vzhledem ke kritické povaze projektu si sponzor projektu požádal o přidělení role vyššího projektového manažera. Správce zdrojů musí získat nový zdroj a definovat roli v systému v případě, že nižší projektový manažer vyžaduje během plánování projektu informace o zdroji.

Následující kroky ukazují, jak může správce zdrojů nastavit roli vyššího projektového manažera a asociovat s ním charakteristiky zdrojů. Později lze roli použít k vyhledání dostupných zdrojů, které odpovídají požadovaným kompetencím zdrojů.

1. Na stránce **Nastavení rolí** vyberte **Nová** a zadejte následující hodnoty:

    - **ID role:** Vyšší projektový manažer
    - **ID role:** Vyšší projektový manažer

2. Vyberte **Vytvořit**.
3. Vyberte roli **Vyšší projektový manažer** a poté vyberte **Konfigurovat charakteristiky**.
4. V poli **Typ charakteristiky** vyberte **Dovednost**.
5. V poli **Dostupné charakteristiky** zadejte hledanou dovednost.
6. V poli **Typ charakteristiky** vyberte **Certifikát**.
7. V poli **Dostupné charakteristiky** zadejte hledaný typ certifikátu.

## <a name="assign-a-project-resource-to-a-project"></a>Přiřazení projektového zdroje k projektu

1. Na stránce **Všechny projekty** vyberte projekt **Fáze 2 upgradu XYZ**.
2. Na kartě **Projektový tým a plánování** vyberte možnost **Přidat**.
3. V poli **Role** vyberte **Člen týmu**.
4. Vyberte **Rezervovat z kalendáře**.
5. Na stránce **Dostupnost zdrojů** vyberte možnost **Nastavení zobrazení**.
6. Na stránce **Upravit nastavení zobrazení** zadejte následující hodnoty:

    - **Formát pro zobrazení rozsahu dat:** Den
    - **Zobrazit popisy dostupnosti:** Ano
    - **Zobrazit zbývající kapacitu:** Ano

7. V seznamu zdrojů vyberte zdroj.
8. Vyberte **Závazná rezervace** a **Plná kapacita**.

## <a name="assign-a-resource-to-a-default-role"></a>Přiřazení zdroje k výchozí roli

Chcete-li pomoci správcům projektů nebo zdrojů s procházením hierarchie zdrojů, které lze pro projekt rezervovat. Můžete přiřadit výchozí roli k existujícímu zdroji nebo nově získanému zdroji. Například když byl Daniel najat, měl zkušenosti a dovednosti, aby mohl plnit roli obchodního analytika. Správce zdrojů přidělil tuto Danielovi jako výchozí. Proto správce zdrojů přidal Daniela do fondu obchodních analytiků, kteří jsou k dispozici pro práci na projektech.

Během rezervace zdrojů mohou projektoví manažeři filtrovat zdroje rolí, které jsou k dispozici pro práci na projektech. Tuto informaci mohou použít jako jedno z kritérií při provádění multikriteriální rozhodovací analýzy během plnění zdrojů. Mohou také přidat do filtru další charakteristiky zdrojů, aby vyhledali zdroje, které mají specifické dovednosti, vzdělání a zkušenosti pro daný projekt.

**Scénář:** Byl zahájen schválený projekt a role vyššího projektového manažera byla rezervována jako plánovaný zdroj během fáze plánování projektu. Správce prostředků nyní získal zdroj ke splnění role vyššího projektového manažera.

1. Na stránce **Seznam zdrojů** vyberte položku **Daniel Goldschmidt**.
2. Na stránce **Role zdroje** vyberte **Nová** a zadejte následující hodnoty:

    - **Platí od:** Zadejte aktuální datum.
    - **Vypršení platnosti:** Zadejte **Nikdy**.
    - **Role:** Zadejte **Vyšší projektový manažer**.

3. Vyberte tlačítko **Uložit** a potom zavřete stránku.
4. Na kartě **Kompetence** přidejte dovednost **Správa projektu** a certifikát **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]