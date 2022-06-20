---
title: Nastavení projektových zdrojů
description: Tento článek poskytuje informace o nastavení nebo požadování prostředků projektu.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a4e6fe829d6b39aed9eb6aaea42f245fc997593
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933760"
---
# <a name="set-up-project-resources"></a>Nastavení projektových zdrojů

[!include [banner](../includes/banner.md)]

Musíte nastavit kalendář a přidružit jej k zaměstnanci nebo pracovníkovi. Kalendář se používá k naplánování projektu a pracovní doby zdrojů, které jsou pro projekt rezervovány. Během přípravy kalendáře mohou projektoví manažeři provádět vyrovnávání zdrojů jako součást jejich optimalizace. Na základě harmonogramu kalendáře lze zdroje omezit. Kalendář můžete nastavit na straně **Kalendáře**.

Když nastavujete pracovníka jako zdroj projektu, můžete vybírat z pracovníků, kteří pracují ve společnosti, pro kterou nastavujete prostředky. Případně můžete vybrat pracovníky z jiných společností ve vaší organizaci. Tito pracovníci jsou označování jako mezipodnikové zdroje.

Následující postupy vysvětlují, jak nastavit pracovníka jako projektový zdroj ve vaší společnosti a jak nastavit mezipodnikový projektový zdroj.

## <a name="set-up-a-worker-as-a-project-resource"></a>Nastavení pracovníka jako projektový zdroj

1. Na stránce **Pracovníci** vyberte v seznamu **Pracovníci** toho pracovníka, kterého přidáváte jako projektový zdroj, a otevřete záznam pracovníka.
2. V podokně akcí vyberte **Projekt** &gt; **Nastavení** &gt; **Nastavení projektu**.
3. Vyberte kalendář a poté stránku zavřete.

Můžete také určit výchozí projekty pro zdroj jako typ předběžného přiřazení. Předběžné přiřazení lze použít, pokud manažer prostředků nebo projektový manažer předem ví, na kterých projektech bude prostředek pracovat. Předběžná přiřazení mohou být také založena na požadavku sponzora projektu nebo zákazníka. Chcete-li předem přiřadit projekt, vyberte příslušný projekt na stránce **Přiřadit projekty** na kartě **Projekty** v seznamu **Zbývající projekty**.

## <a name="set-up-an-intercompany-resource"></a>Nastavení mezipodnikového zdroje

Když nastavíte pracovníka jako mezipodnikový zdroj, musíte dokončit nastavení jak ve společnosti poskytující půjčku, tak ve společnosti, která si zdroj půjčuje.

### <a name="in-the-lending-company"></a>Ve společnosti poskytující půjčku

1. V aplikace Finance ověřte, zda je vybrána společnost poskytující půjčku, a poté dokončete postup v předchozí části „Nastavení pracovníka jako projektový zdroj“.
2. Na stránce **Mezipodnikové účetnictví** vyberte možnost **Nový**.
3. V poli **ID právnické osoby** vyberte společnost poskytující půjčku. Vyplňte zbývající pole podle potřeby a poté vyberte příkaz **Uložit**.
4. Na stránce **Cena za převod** vyberte možnost **Nová**.
5. V poli **Půjčující si subjekt** vyberte příslušnou společnost.
6. Chcete-li půjčující si společnosti zapůjčit pouze zdroj, který jste vytvořili na začátku této části, vyberte v poli **Zdroj** název zdroje, který jste vytvořili. Chcete-li půjčující si společnosti zpřístupnit všechny zdroje společnosti poskytující půjčku, ponechte pole **Zdroj** prázdné.
7. Na stránce **Parametry správy projektu a účetnictví** nastavte na kartě **Mezipodnikové** možnost **Povolit mezipodnikové plánování zdrojů a časové rozvrhy** na **Ano**.

### <a name="in-the-borrowing-company"></a>V půjčující si společnosti

- Na stránce **Seznam zdrojů** ve filtru vyhledávání zadejte název zdroje, který jste vytvořili pro společnost poskytující půjčku, abyste ověřili, zda je název zahrnut do seznamu prostředků pro půjčující si společnost.

## <a name="request-project-resources"></a>Žádosti o projektové zdroje
Funkce pro plánování projektových zdrojů slouží pouze k tomu, aby manažeři zdrojů distribuovali personální zdroje na zakázkách nebo projektech. Chcete-li povolit tuto funkci, proveďte následující úkoly nebo ověřte, že byly dokončeny:

- Nastavte číselné řady.
- Nastavte pracovní postupy pro správu projektů a účetnictví.
- Povolte pracovní postupy žádostí o zdroje.

Po dokončení předchozích úkolů můžete podle potřeby dokončit následující úkoly:

- Vytvořte požadavek na zdroj z předběžně rezervovaného personálního zdroje.
- Monitorujte žádosti o zdroje.
- Vyřizujte žádosti o zdroje.
- Požádejte o personální zdroj ze strukturovaného rozpisu prací.
- Rezervujte si zdroje do projektu bez požadavku na personální zdroj.


[!INCLUDE[footer-include](../includes/footer-banner.md)]