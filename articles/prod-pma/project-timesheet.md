---
title: Mobilní aplikace Časový výkaz projektu
description: Tento článek obsahuje informace o mobilní aplikaci Microsoft Dynamics 365 Project Timesheet. Mobilní aplikace Časový výkaz projektu umožňuje uživatelům odesílat a schvalovat časové rozvrhy projektů na jejich mobilním zařízení.
author: abruer
ms.date: 06/29/2022
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
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110967"
---
# <a name="project-timesheet-mobile-application"></a>Mobilní aplikace Časový výkaz projektu

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Přehled

Mobilní aplikace Microsoft Dynamics 365 Project Timesheet umožňuje uživatelům odesílat a schvalovat časové rozvrhy projektů na jejich mobilním zařízení. (iPhone nebo Android). Tato mobilní aplikace se týká funkce časových rozvrhů v oblasti Řízení projektů a účetnictví v aplikaci Dynamics 365 Finance. Pomáhá zlepšit produktivitu a efektivitu uživatelů a také umožňuje včasné zadávání a schvalování časových výkazů projektu.

## <a name="download-and-install-the-mobile-app"></a>Stažení a instalace mobilní aplikace

Stáhněte a nainstalujte mobilní aplikaci Microsoft Dynamics 365 Project Timesheet pro Android nebo iPhone z mobilního obchodu pro vaše zařízení.

## <a name="enable-the-app"></a>Povolte aplikaci 

Ve Financích musí být mobilní aplikace Časový výkaz projektu povolena. Chcete-li tuto funkci povolit, přejděte na **Parametry řízení projektu a účetnictví \> Rozvrh hodin** a vyberte **Povolit Microsoft Dynamics 365 Project Timesheet** parametr.

### <a name="resolve-sign-in-issues"></a>Řešení potíží s přihlášením

**Problém:** Během přihlašování do mobilní aplikace Project Timesheet se uživatelům zobrazí chybová zpráva, že „nemají přístup k aplikaci“ '2bc50526-cdc3-4e36-a970-c284c34cbd6e' v daném klientovi."

**Problém:** Během přihlašování do mobilní aplikace Project Timesheet se uživatelům zobrazí chyba podobná jednomu z následujících příkladů:

- "AADSTS50020: Uživatelský účet '[jméno uživatele]' od poskytovatele identity 'https://sts.windows.net/[app id]“ neexistuje v klientovi '[tenant id]' a nemá přístup k aplikaci '[app id]' v tomto klientovi."
- "Vybraný uživatelský účet neexistuje v klientovi '[tenant id]' a nemůže získat přístup k aplikaci '[app id]' v tomto klientovi."

**Vysvětlení:** Tyto problémy jsou způsobeny změnou, která byla provedena v Azure Active Directory (Azure AD) v květnu 2022 a týká se externích uživatelů. Protože tato změna nebyla provedena ve finančních a provozních aplikacích, může ovlivnit zákazníky na jakékoli verzi platformy nebo aplikace.

**Řešení:** Všichni externí uživatelé musí být pozváni do klienta prostřednictvím Azure AD. Více informací viz [Pozvěte uživatele pomocí Azure Active Directory B2B collaboration](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Přihlaste se do aplikace

1.  Otevřete mobilní aplikaci na svém mobilním zařízení.

2.  Zadejte své Finance URL.

3.  Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte vaše pověření.

4. Budete přihlášeni do své výchozí společnosti.

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
