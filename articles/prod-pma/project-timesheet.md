---
title: Mobilní aplikace Časový výkaz projektu
description: Tento článek obsahuje informace o mobilní aplikaci Microsoft Dynamics 365 Project Timesheet. Mobilní aplikace Časový výkaz projektu umožňuje uživatelům odesílat a schvalovat časové rozvrhy projektů na jejich mobilním zařízení.
author: abruer
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 6f4be64f595371334e4065b60ca1a81232b333f7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923962"
---
# <a name="project-timesheet-mobile-application"></a>Mobilní aplikace Časový výkaz projektu

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Přehled

Mobilní aplikace Microsoft Dynamics 365 Project Timesheet umožňuje uživatelům odesílat a schvalovat časové rozvrhy projektů na jejich mobilním zařízení. (iPhone nebo Android). Tato mobilní aplikace je vybavena funkcí časového rozvrhu, která je umístěna v Řízení projektů a účetnictví aplikace Dynamics 365 Finance a zlepšuje produktivitu a efektivitu uživatelů a umožňuje včasné zadávání a schvalování časového rozvrhu projektu.

## <a name="download-and-install-the-mobile-app"></a>Stažení a instalace mobilní aplikace

Stáhněte a nainstalujte mobilní aplikaci Microsoft Dynamics 365 Project Timesheet pro Android nebo iPhone z mobilního obchodu pro vaše zařízení.

## <a name="enable-the-app"></a>Povolte aplikaci 

Ve Financích musí být mobilní aplikace Časový výkaz projektu povolena. Chcete-li tuto funkci povolit, přejděte na **Parametry řízení projektu a účetnictví \> Rozvrh hodin** a vyberte **Povolit Microsoft Dynamics 365 Project Timesheet** parametr.

## <a name="sign-in-to-the-app"></a>Přihlaste se do aplikace

1.  Otevřete mobilní aplikaci na svém mobilním zařízení.

2.  Zadejte své Finance URL.

3.  Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte vaše pověření.

4.  Budete přihlášeni do své výchozí společnosti.

## <a name="submit-a-project-timesheet"></a>Odešlete časový rozvrh projektu

V aplikaci můžete vytvořit a odeslat časový rozvrh projektu. Nový časový rozvrh můžete založit na informacích z předchozího časového rozvrhu, uložených řádcích nebo přiřazení projektu. Pokud jste určeni jako delegát, můžete také zadat časový výkaz pro jiného pracovníka. Chcete-li vytvořit časový rozvrh jako delegáta, vyberte tlačítko **Nabídka** a poté vyberte název prostředku.

Stránka časového rozvrhu vytvoří nový časový rozvrh pro časové období na základě aktuálního data. Tento pracovní týden bude zobrazen . Pokud časové období pokrývá několik týdnů, můžete si na kartách pracovního týdne vybrat jiný pracovní týden.
Pokud existuje časový rozvrh pro aktuální datum, zobrazí se. Pokud potřebujete vytvořit nový časový rozvrh v jiném časovém období, vyberte tlačítko **Nabídka** a poté vyberte **Nový časový rozvrh**.

Informace o projektu můžete zadat kliknutím na akci **Přidat čas** nebo **Zkopírovat čas z**. Akce **Zkopírovat čas z** zkopíruje informace o řádku projektu, ale ne hodiny. Nabídka **Zkopírujte čas z** obsahuje následující možnosti:

- **Kopírovat z existujícího časového rozvrhu** - Zkopírujte řádky časového rozvrhu z existujícího časového rozvrhu.

- **Kopírovat z oblíbených** - Vytvoří nové řádky časového rozvrhu pomocí nastavení časového rozvrhu, které jste vybrali jako oblíbené.

- **Kopie z úkolu** - Vytvoří nové řádky časového rozvrhu z přiřazených projektů.

Zobrazené informace o projektu závisí na mobilních parametrech, které jste definovali na stránce **Parametry řízení projektu a účetnictví**.

V poli **Právnická osoba** vyberte právnickou osobu, pro kterou jste prováděli projektovou práci. Pole **Právnická osoba** je k dispozici, pouze pokud byla u vaší právnické osoby povolena podpora mezipodnikového časového rozvrhu.

Vyberte zákazníka, který je přidružen k projektu pro časový rozvrh. Pro první vydání na Android, vstup od zákazníka není podporován, protože musíte nejprve vybrat projekt. Pokud jste nejprve vybrali projekt, pole **Zákazník** se vyplňuje automaticky.

V poli **Projekt** vyberte projekt, pro který zadáváte čas. pole **Zákazník** se vyplňuje automaticky.

Vyhledávání zákazníků a projektů umožňuje vyhledávání napříč zákazníky i projekty.

Informace v polích **Kategorie**, **Aktivita**, **Vlastnost řádku**, **Skupina DPH**, a **Skupina daně z prodeje zboží** jsou povinné. Tato pole lze přepsat.

Pole **Vlastnost řádku** bude nastaveno na výchozí hodnotu na základě parametrů řízení projektu a účetnictví. Když jsou povoleny parametry projektu / kategorie a kategorie / zdroje, hodnota **Vlastnost řádku** bude nastavena na výchozí hodnotu, kterou jste definovali pro toto ověření. Pokud nejsou povoleny parametry projektu / kategorie a kategorie / zdroje, hodnota **Vlastnost řádku** bude nastavena podle pole **Povolit výchozí vlastnost řádku** na stránce **Parametry řízení projektu a účetnictví**. Hodnotu **Vlastnost řádku** lze přepsat.

Vyberte den a přidejte čas. Zadejte počet hodin, které jste každý den odpracovali.

Chcete-li přidat komentáře k otevírací době, klikněte na **Přidejte komentáře**, a poté zadejte komentáře pro interní cílovou skupinu, zákazníka cílová skupiny nebo obojí.
Interní komentáře mohou zobrazit projektoví manažeři. Komentáře zákazníků jsou zahrnuty na fakturách.

Chcete-li řádek uložit jako oblíbený, zaškrtněte políčko a poté klikněte **Uložit jako oblíbené**.

Finanční dimenze a podpora příloh nejsou v mobilní aplikaci poskytovány.

Podle potřeby pokračujte v přidávání řádků projektu a vyplňte svůj časový rozvrh.

Klepněte na **Předložit** k odeslání časového rozvrhu do pracovního postupu schválení.

## <a name="review-timesheets"></a>Zkontrolujte časové rozvrhy

Seznam časových výkazů, které je třeba zkontrolovat, je k dispozici v nabídce. Tato možnost je k dispozici, pouze pokud jste byli označeni jako schvalovatel pracovního postupu. Je podporováno schválení záhlaví i řádku. Schválení na úrovni řádků nabízí možnost označit jeden nebo více řádků ke schválení. Po kontrole informací časového rozvrhu klikněte na **Schválit**, **Delegovat** nebo **Vrátit se** k pokračování pracovního postupu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]