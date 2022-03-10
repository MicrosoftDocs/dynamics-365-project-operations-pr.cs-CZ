---
title: Řešení potíží s prací v mřížce úloh
description: Tento téma poskytuje potřebné informace o odstraňování potíží při práci v mřížce úloh.
author: ruhercul
ms.date: 09/22/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 67136229d84a09886fffe9677b10f671aea3c393
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547191"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Řešení potíží s prací v mřížce úloh 


_**Platí pro:** Project Operations pro scénáře založené na zdrojích / neskladových položkých, nasazení Lite – řeší proforma fakturaci, Project for the Web_

Mřížka úkolů využívaná řešením Dynamics 365 Project Operations je hostovaný prvek iframe uvnitř Microsoft Dataverse. V důsledku tohoto použití musí být splněny specifické požadavky, aby bylo zajištěno správné fungování ověřování a autorizace. Toto téma popisuje časté problémy, které mohou mít dopad na vykreslení mřížky nebo správu úkolů ve strukturovaném rozpisu praccí (WBS).

Časté problémy zahrnují:

- Karta **Úkol** na mřížce úkolu je prázdná.
- Při otevírání projektu se projekt nenačte a uživatelské rozhraní (UI) se zasekne na indikátoru průběhu.
- Správa oprávnění pro **Project for the Web**.
- Změny se neuloží, když vytvoříte, aktualizujete nebo odstraníte úkol.

## <a name="issue-the-task-tab-is-empty"></a>Problém: Karta Úkol je prázdná

### <a name="mitigation-1-enable-cookies"></a>Řešení 1: Povolte soubory cookie

Project Operations vyžaduje, aby byly k vykreslení strukturovaného rozpisu prací povoleny soubory cookie třetích stran. Pokud nejsou povoleny soubory cookie třetích stran, místo zobrazení úkolů se zobrazí prázdná stránka po výběru karty **Úkoly** na stránce **Projekt**.

U prohlížečů Microsoft Edge a Google Chrome následující postupy popisují, jak aktualizovat nastavení prohlížeče tak, aby povolil soubory cookie třetích stran.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Spusťte prohlížeč Edge.
2. V pravém horním rohu vyberte **tři tečky** (…). Potom vyberte **Nastavení**.
3. V části **Soubory cookie a oprávnění stránek** vyberte **Cookies a data stránek**.
4. Vypněte **Blokovat soubory cookie třetích stran**.
5. Aktualizujte okno prohlížeče. 

#### <a name="google-chrome"></a>Google Chrome

1. Spusťte prohlížeč Chrome.
2. V pravém horním rohu vyberte tři svislé tečky a potom **Nastavení**.
3. V části **Ochrana osobních údajů a zabezpečení** vyberte **Cookies a další data stránek**.
4. Vyberte **Povolit všechny soubory cookie**.
5. Aktualizujte okno prohlížeče. 

> [!NOTE]
> Pokud zablokujete soubory cookie třetích stran, budou blokovány všechny soubory cookie a data webů z jiných webů, i když je web povolen ve vašem seznamu výjimek.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Řešení 2: Ověřte, že je správně nakonfigurován koncový bod PEX

Project Operations vyžaduje, aby parametr projektu odkazoval na PEX koncový bod. Tento koncový bod je vyžadován ke komunikaci se službou, která slouží k vykreslení strukturovaného rozpisu prací. Pokud parametr není povolen, zobrazí se chyba „Parametr projektu není platný“. Chcete-li aktualizovat koncový bod PEX, proveďte následující kroky.

1. Přidejte pole **Koncový bod PEX** na stránku **Parametry projektu**.
2. Identifikujte typ produktu, který používáte. Tato hodnota se používá, když je nastaven PEX koncový bod. Po načtení je typ produktu již definován v PEX koncovém bodě. Hodnotu uchovejte.
3. Aktualizujte pole následující hodnotou: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Následující tabulka uvádí parametr typu, který se má použít v závislosti na typu produktu.

      | **Typ produktu**                     | **Typ parametru** |
      |--------------------------------------|--------------------|
      | Project for the Web ve výchozí oganizaci   | type=0             |
      | Project for the Web ve oganizaci pojmenovanou CDS | type=1             |
      | Project Operations                   | type=2             |

4. Odeberte pole ze stránky **Parametry projektu**.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problém: Projekt se nenačte a uživatelské rozhraní je zaseknuto na indikátoru průběhu

Pro účely ověřování musí být povolena automaticky otevíraná okna, aby se mřížka Úkol mohla načíst. Pokud nejsou povolena automaticky otevíraná okna, obrazovka se zasekne na indikátoru průběhu načítání. Následující obrázek znázorňuje adresu URL s blokovaným automaticky otevíraným popiskem v adresním řádku, což má za následek zaseknutí indikátoru průběhu při pokusu o načtení stránky. 

   ![Zaseknutý indikátor průběhu a automaticky otevíraný blok.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Řešení 1: Povolte automaticky otevíraná okna

Když se zasekne indikátor průběhu načítání projektu, je možné, že nejsou povolena automaticky otevíraná okna.

#### <a name="microsoft-edge"></a>Microsoft Edge

V prohlížeči Edge existují dva způsoby, jak povolit automaticky otevíraná okna.

1. V prohlížeči Edge vyberte oznámení v pravém horním rohu prohlížeče.
2. Vyberte **Vždy povolit automaticky otevíraná okna a přesměrování z** pro konkrétní prostředí Dataverse.
 
     ![Automaticky otevíraná okna zablokovala okno.](media/enablepopups.png)

Případně můžete také provést některý z následujících kroků:

1. Spusťte prohlížeč Edge.
2. V pravém horním rohu vyberte **tři tečky** (...) a potom vyberte **Nastavení** > **Oprávnění webu** > **Automaticky otevíraná okna a přesměrování**.
3. Přepněte **Automaticky otevíraná okna a přesměrování** do polohy vypnuto, čímž zablokujete automaticky otevíraná okna, nebo do polohy zapnuto, čímž povolíte automaticky otevíraná okna na vašem zařízení.
4. Po povolení automaticky otevíraných oken aktualizujte prohlížeč. 

#### <a name="google-chrome"></a>Google Chrome
1. Spusťte prohlížeč Chrome.
2. Přejděte na stránku, kde jsou automaticky otevíraná okna blokována.
3. V adresním řádku vyberte **Automaticky otevírané okno blokováno**.
4. Vyberte odkaz na automaticky otevírané okno, které chcete vidět.
5. Po povolení automaticky otevíraných oken aktualizujte prohlížeč. 

> [!NOTE]
> Chcete-li pro web vždy zobrazit automaticky otevíraná okna, vyberte **Vždy povolit automaticky otevíraná okna a přesměrování z [web]** a poté vyberte **Hotovo**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problém 3: Správa oprávnění pro Project for the Web

Project Operations spoléhá na externí plánovací službu. Služba vyžaduje, aby měl uživatel přiřazeno několik rolí, které mu umožňují číst a zapisovat entity související s WBS. Mezi tyto entity patří projektové úkoly, přiřazení prostředků a závislosti úkolů. Pokud uživatel nemůže vykreslit WBS, když přejde na kartu **Úkoly**, je to pravděpodobně proto, že **Projekt** pro **Project Operations** není povolen. Uživatel může obdržet buď chybu role zabezpečení, nebo chybu související s odepřením přístupu.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Řešení 1: Ověřte role zabezpečení uživatele aplikace a koncového uživatele

1. Přejděte na **Nastavení** > **Zabezpečení** > **Uživatelé** > **Uživatelé aplikace**.  

   ![Čtečka aplikace.](media/applicationuser.jpg)
   
2. Poklepáním na záznam uživatele aplikace ověřte:

     - Uživatel má přístup k projektu. To lze provést ověřením, že uživatel má roli zabezpečení **Projektový manažer**.
     - Uživatel aplikace Microsoft Project existuje a je správně nakonfigurován.
 
3. Pokud tento uživatel neexistuje, vytvořte nový záznam uživatele. 
4. Vyberte **Noví uživatelé**, změňte vstupní formulář na **Uživatel aplikace** a poté přidejte **ID aplikace**.

   ![Uživatelské údaje aplikace.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problém 4: Změny se neuloží, když vytvoříte, aktualizujete nebo odstraníte úkol

Když provedete jednu nebo více aktualizací WBS, změny selžou a nejsou uloženy. V mřížce plánu se zobrazí chyba se zprávou „Nedávno provedenou změnu nelze uložit“.

### <a name="mitigation-1-validate-the-license-assignment"></a>Řešení 1: Ověřte přiřazení licence

1. Ověřte, že uživateli byla přiřazena správná licence a že je služba povolena v podrobnostech servisních plánů licence.  
2. Ověřte, že uživatel může otevřít **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Řešení 2: Ověřte konfiguraci uživatele aplikace Project
1. Ověřte, že uživatel aplikace Project byl vytvořen.
2. Aplikujte na uživatele následující role zabezpečení:
  
  - Uživatel nebo základní uživatel Dataverse
  - Systém Project Operations
  - Systém projektu
  - Systém duálního zápisu Project Operations. Tato role je vyžadována pro scénáře Project Operations založené na zdrojích / neskladových položkách.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
