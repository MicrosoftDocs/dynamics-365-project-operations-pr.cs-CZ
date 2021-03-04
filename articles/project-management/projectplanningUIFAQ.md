---
title: Řešení potíží s prací v mřížce úloh
description: Tento téma poskytuje potřebné informace o odstraňování potíží při práci v mřížce úloh.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031529"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Řešení potíží s prací v mřížce úloh 

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Tento téma popisuje, jak opravit problémy, se kterými se můžete setkat při práci se správou nákladů.

## <a name="enable-cookies"></a>Povolení souborů cookie

Aby bylo možné vykreslit strukturu rozpisu práce, vyžaduje Project Operations povolení souborů cookie třetích stran. Pokud nejsou povoleny soubory cookie třetích stran, místo zobrazení úkolů se zobrazí prázdná stránka po výběru karty **Úkoly** na stránce **Projekt**.

![Prázdná karta, pokud nejsou povoleny soubory cookie třetích stran](media/blankschedule.png)


### <a name="workaround"></a>Zástupné řešení
U prohlížečů Microsoft Edge a Google Chrome následující postupy popisují, jak aktualizovat nastavení prohlížeče tak, aby povolil soubory cookie třetích stran.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Spusťte prohlížeč Edge.
2. V pravém horním rohu vyberte **tři tečky** (…). Potom vyberte **Nastavení**.
3. V části **Soubory cookie a oprávnění stránek** vyberte **Cookies a data stránek**.
4. Vypněte **Blokovat soubory cookie třetích stran**.

#### <a name="google-chrome"></a>Google Chrome

1. Spusťte prohlížeč Chrome.
2. V pravém horním rohu vyberte tři svislé tečky a potom **Nastavení**.
3. V části **Ochrana osobních údajů a zabezpečení** vyberte **Cookies a další data stránek**.
4. Vyberte **Povolit všechny soubory cookie**.

> [!IMPORTANT]
> Pokud zablokujete soubory cookie třetích stran, budou blokovány všechny soubory cookie a data webů z jiných webů, i když je web povolen ve vašem seznamu výjimek.

## <a name="pex-endpoint"></a>Koncový bod PEX

Project Operations vyžaduje, aby parametr projektu odkazoval na PEX koncový bod. Tento koncový bod je vyžadován pro komunikaci se službou používanou k vykreslování strukturovaného rozpisu prací. Pokud parametr není povolen, zobrazí se chyba „Parametr projektu není platný“. 

### <a name="workaround"></a>Zástupné řešení
 ![Pole PEX koncového bodu v parametru projektu](media/projectparameter.png)

1. Přidejte pole **Koncový bod PEX** na stránku **Parametry projektu**.
2. Aktualizujte pole následující hodnotou: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Odeberte pole ze stránky **Parametry projektu**.

## <a name="privileges-for-project-for-the-web"></a>Oprávnění pro Projekt pro web

Project Operations spoléhá na externí plánovací službu. Služba vyžaduje, aby měl uživatel několik rolí přiřazených ke čtení a zápisu do entit souvisejících se strukturou rozpisu práce. Mezi tyto entity patří projektové úkoly, přiřazení prostředků a závislosti úkolů. Pokud uživatel nemůže vykreslit strukturu rozpisu práce, když přejde na kartu **Úkoly**, je to pravděpodobně proto, že projekt pro Project Operations nebyl povolen. Uživatel může obdržet buď chybu role zabezpečení, nebo chybu související s odepřením přístupu.


## <a name="workaround"></a>Zástupné řešení

1. Přejděte na **Nastavení > Zabezpečení > >Uživatelé aplikace**.  

   ![Čtečka aplikace](media/applicationuser.jpg)
   
2. Dvojitým kliknutím na záznam uživatele aplikace ověřte následující:

 - Uživatel má přístup k projektu. Toto ověření se obvykle provádí zajištěním, že uživatel má roli zabezpečení **Projektový manažer**.
 - Uživatel aplikace Microsoft Project existuje a je správně nakonfigurován.
 
3. Pokud tento uživatel neexistuje, můžete vytvořit nový záznam uživatele. Vyberte možnost **Noví uživatelé**. Změňte formulář zadání na **Uživatel aplikace** a poté přidejte **ID aplikace**.

   ![Uživatelské údaje aplikace](media/applicationuserdetails.jpg)

4. Ověřte, že uživateli byla přiřazena správná licence a že je služba povolena v podrobnostech servisních plánů licence.
5. Ověřte, že uživatel může otevřít project.microsoft.com.
6. Prostřednictvím parametrů projektu ověřte, že systém ukazuje na správný koncový bod projektu.
7. Ověřte, že je vytvořen uživatel aplikace projektu.
8. Aplikujte na uživatele následující role zabezpečení:

  - Uživatel služby Dataverse
  - Systém Project Operations
  - Systém projektu

## <a name="error-when-updating-the-work-breakdown-structure"></a>Chyba při aktualizaci strukturovaného rozpisu práce

Když se provede jedna nebo více aktualizací struktury rozpisu práce, změny nakonec selžou a neuloží se. V mřížce plánu se vyskytla chyba s informací, že „poslední provedenou změnu nelze uložit“.

### <a name="workaround"></a>Zástupné řešení

1. Ověřte, že uživateli byla přiřazena správná licence a že je služba povolena v podrobnostech servisních plánů licence.
2. Ověřte, že uživatel může otevřít project.microsoft.com.
3. Ověřte, že systém ukazuje na správný koncový bod projektu.
4. Ověřte, že uživatel aplikace projektu byl vytvořen.
5. Aplikujte na uživatele následující role zabezpečení:
  
  - Uživatel Dataverse nebo základní uživatel
  - Systém Project Operations
  - Systém projektu
  - Systém duálního zápisu Project Operations (Tato role je vyžadována, pokud nasazujete scénář Project Operations, který není založen na zdroji / není skladem.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]