---
title: Instalace ukázkových dat
description: Tento článek obsahuje informace o instalaci ukázkových dat v aplikaci Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: johnmichalak
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 8fb3854c139125abbf499622d048e2ff0791516a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926768"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instalace ukázkových dat pro aplikaci Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Abyste mohli vytvářet vlastní ukázková prostředí, společnost Microsoft nabízí ukázkové balíčky dat ke stažení, které prezentují funkce vašich aplikací. Existují dva typy balíčků ukázkových dat:
- referenční data a data nastavení
- ukázková data (referenční data a data nastavení, a transakční data, jako například pracovní příkazy a projekty)

Ukázkové balíčky **referenčních** dat lze stáhnout ve třech samostatných balíčcích, takže můžete nainstalovat data pouze pro služby Project Service nebo jen pro Field Service nebo můžete nainstalovat ukázková data pro obě aplikace najednou.

Balíčky ukázkových referenčních dat a dat nastavení jsou:

- [**V902PSMasterData** - pouze Project Service verze 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - pouze Project Service verze 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x a Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Nejnovější balíček **ukázkových** dat je:

 - [**FPSDemoData** - Field Service 8.x a Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Pokyny k instalaci se pro uživatele mírně liší při vytváření a konfiguraci částí, ale zbytek je stejný jako předchozí [**příspěvky blogu**](https://aka.ms/fpsdemodatablog). Tento balíček obsahuje omezenou sadu ukázkových dat a jeho instalace trvá asi 3 hodiny.

Tyto balíčky ukázkových dat jsou k dispozici pouze v angličtině.

> [!IMPORTANT]
> **Neexistuje žádný způsob odinstalace ukázkových dat.** Proto byste měli tyto balíčky instalovat pouze pro účely ukázky, hodnocení, školení nebo testování systémů. Všimněte si také, že instalace samostatného balíčku a následná instalace dalších jednotlivých balíčků není podporována. (Jinými slovy, nelze nainstalovat **FSMasterData** a potom **PSMasterData**, nebo naopak.) Pokud máte pocit, že v budoucnu budete potřebovat ukázková data pro obě aplikace, měli byste nainstalovat balíček **v902FPSMasterData**.

Při instalaci kteréhokoli z balíčků ukázkových dat proces instalace provede následující akce:

- Vytvoří nebo nastaví výchozí parametry pro použití aplikace Project Service, Field Service nebo obou (pokud existuje).

- Importuje ukázková data pro aplikace, například rezervovatelné prostředky, role specifické pro aplikaci, prodej a ceníky nákladů, organizační jednotky, záznamy prodejního procesu a jiných subjektů k prokázání klíčových schopností.  

S balíčkem **ukázkových dat** získáte výše uvedená a další transakční data, jako jsou pracovní příkazy a projekty.

Ptáte se, jaké schopnosti můžete pomocí ukázkových dat předvést? Viz fiktivní scénář na společnosti Fabrikam Robotics níže, v části [technické poznámky](#technical-notes).

Pokud máte dotazy týkající se instalace těchto balíčků ukázkových dat, [pošlete nám e-mail na adresu fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Požadavky

Protokol instalace předpokládá následující skutečnosti týkající se vaší cílové instance (org):

- Základním jazykem je angličtina a základní měna je americký dolar (USD, $)

- Organizace ještě nemá žádná data služeb Project Service nebo Field Service nebo má pouze nejzákladnější výchozí data, která jsou součástí jakékoli nové organizace

- Je již nainstalována správná verze kancelářské aplikace:
       
    - **Pro FPSDemoData nebo v902FPSMasterData:** Organizace má nainstalovanou aplikaci Field Service verze 8.x a Project Service verze 3.x.

    - **Pro v902PSMasterData:** Organizace má instalovanou aplikaci Project Service 3.x.

    - **Pro v902FSMasterData:** Organizace má nainstalovanou aplikaci Field Service verze 8.x.

> [!NOTE]
> Pokud potřebujete instalovat ukázková data ke stávající zkušební verzi aplikace Project Service a Field Service nebo jejich ukázkovému prostředí, které již obsahuje data (není doporučeno), bude nutné pozastavit předběžné kontroly bezpečnosti, které provádí instalační program. Další informace naleznete v následujících technických poznámkách:

## <a name="prepare-for-installation"></a>Příprava na instalaci

Je nutné spustit instalační program v počítači s nejnovější verzí systému Windows (ideálně Windows 10).

Měli byste naplánovat, aby počítač zůstal připojený k síti, a počítat s tím, že instalace může trvat až **1 hodinu** pro **data nastavení a referenční data**. (Obvykle instalace trvá přibližně 30 minut u **FPSMasterData**, který obsahuje ukázková data pro obě aplikace.) U **FPSDemoData** bude instalace trvat kolem **3 hodin**.

Na počítači by měla být vypnuta funkce spořiče obrazovky. Jinak se můžou při aktivaci spořiče obrazovky ztratit přihlašovací údaje pro instalaci (pokud nezachováte relaci po celou dobu aktivní).

> [!div class="mx-imgBorder"]
> ![Snímek obrazovky nastavení spořiče obrazovky s vypnutým spořičem obrazovky.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Stažení a vybalení

Instalační program ukázkových dat aplikací Project Service a Field Service je distribuován jako samorozbalovací spustitelný soubor. Názvy souborů se mohou lišit podle balíčku ukázkových dat, ale jinak jsou kroky stejné bez ohledu na to, který balíček nainstalujete.

Po stažení balíčku spusťte soubor EXE a poté přijměte podmínky pro rozbalení komprimovaného souboru ZIP. Pak bude nutné extrahovat obsah tohoto souboru do složky v počítači.

V závislosti na operačním systému a nastavení zabezpečení je třeba po rozbalení souboru zip provést následující kroky:

1. Vyhledejte soubor **FPSDemoData.dll** ve složce **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Zvolte **Odblokovat**.

3. Vyberte **Použít**.

4. Vyberte **OK**.


## <a name="create-or-configure-users"></a>Vytvoření nebo konfigurace uživatelů

Balíček **FPSDemoData** vyžaduje šest uživatelů, zatímco balíček **FPSMasterData** vyžaduje jednoho uživatele. Vyberte si ten správný balíček ukázkových dat pro vás.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Vytvoření nebo konfigurace uživatelů - balíčky dat nastavení nebo referenčních dat

Balíček **FPSMasterData** je navržen pro instalaci s jedním uživatelem pojmenovaným Spencer Low s nastavením popsaným zde. Aby instalace balíčku proběhla správně, musíte vytvořit (nebo dočasně přejmenovat) uživatele ve vašem prostředí aby odpovídali konfiguraci příchozích ukázkových dat.

Chcete-li vytvořit nebo konfigurovat uživatele, přejděte na **Nastavení** > **Zabezpečení** > **Uživatelé** a proveďte následující kroky:

1. Nastavte UserFullname="Spencer Low" s uživatelským jménem "spencerl" (**malými písmeny**) na role Project Manager a Practice Manager.

2. Vyberte uživatele **Spencer Low** a pak vyberte **Spravovat role**. Vyhledejte a vyberte roli **Správce systému** a pak vyberte **OK** k udělení úplných oprávnění pro správu uživateli Spencer Low. Tento krok je nezbytný pro zajištění, že ukázkové záznamy jsou vytvořeny se správným uživatelským vlastnictvím a tedy správně naplňují zobrazení.

3. Ze staženého balíčku musíte aktualizovat soubor mapování dat pomocí e-mailových adres výchozího kontextu uživatele. Postupujte tak, že otevřete složku **PkgFolder** a potom vyhledáte a otevřete soubor **ImportUserMapFile.xml** v programu Poznámkový blok (nebo Visual Studio nebo v jiném editoru XML). Nastavte v poli **DefaultUserToMapTo =** e-mailovou adresu uživatele Spencer Low.

4. Pokud nevystupujete jako uživatel Spencer Low s uživatelským jménem **spencerl**, je třeba aktualizovat další soubor. Otevřete soubor **DemoDataPreImportConfig.xml** a potom vyhledejte značku **userstocreateandconfigure**. Aktualizujte značku **\<login\>** uživatelským jménem uživatele Spencer Low. Další podrobnosti naleznete v [technických poznámkách](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Vytvoření nebo konfigurace uživatelů - balíček ukázkových dat

Balíček ukázkových dat vyžaduje šest uživatelů. Pro správnou instalaci balíčku proveďte následující kroky:

 1. Vytvořte nebo dočasně přejmenujte existující uživatele, aby odpovídaly konfiguraci příchozích ukázkových dat, přechodem na **Nastavení** > **Zabezpečení** > **Uživatelé**.
 
    Tyto role jsou potřebné pouze pro ukázky na základě persona.  
    - Celé jméno uživatele = David So jako technik v terénu   
    - Celé jméno uživatele = Jamie Reding jako dispečer služeb Customer Service a Field Service   
    - Celé jméno uživatele = Molly Clark jako manažerka obchodních vztahů   
    - Celé jméno uživatele = Spencer Low jako projektový manažer  
    - Celé jméno uživatele = Veronica Quek jako členka týmu   
    - Celé jméno uživatele = William Contoso
  
2. Pro účely importu ukázkových dat přiřaďte výše uvedeným šesti uživatelům roli správce, aby se záznamy importovaly správně. 

3. Otevřete **PkgFolder** a potom vyhledejte a otevřete **ImportUserMapFile.xml**. Aktualizujte pole **Nová =** pro e-mailové adresy odpovídajících uživatelů ve vašem systému.

   > [!div class="mx-imgBorder"]
   > ![Snímek obrazovky UserMapFile.](media/sample-data-7.png)

4. Pokud má celé jméno uživatele Spencer Low jiné ID uživatele než **"spencerl"**, je třeba aktualizovat další soubor. Otevřete **DemoDataPreImportConfig.xml** a potom vyhledejte značku **userstocreateandconfigure**. Aktualizujte značku **\<login\>** s loginId (rozlišuje velká a malá písmena). 

5. Kalendář prvního uživatele (ve značce **userstocreateandconfigure**) slouží k naplnění pracovní doby pro všechny rezervovatelné prostředky při importu ukázkových dat. Přejděte do **Nastavení** > **Zabezpečení** > **Uživatelé**, vyhledeje uživatele Spencer Low a otevřete možnost Pracovní doba. Upravte existující pracovní dobu výběrem možnosti **Celý opakovaný týdenní plán od začátku do konce**. Ujistěte se, že **pracovní doba je nastavena na 8:00 - 17:00 (9 hodin), od pondělí do pátku a v časovém pásmu Tichomoří (USA a Kanada)**. To je nutné proto, aby se , aby se Projekt a Plánovací vývěska zobrazovaly podle očekávání.

**Doporučení:** Nyní zvažte vytvoření zálohy organizace pro případ, že budete potřebovat obnovit počáteční bod, pokud dojde k chybě při instalaci ukázkových dat. Další informace získáte v části [Instance zálohování a obnovení](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Spusťte Package Deployer

1. Najděte a spusťte **PackageDeployer.exe** ve složce **v902FPSMasterData** NEBO **PackageDeployer_FPSDemoData**

2. Přijměte smluvní podmínky.

3. V dalším okně:

   a. Jako typ nasazení zvolte **Office 365**.

   b. Použijte uživatelské jméno a heslo správce systému nakonfigurovaného ve složce "Vytvořit nebo konfigurovat uživatele" ("Spencer Low" s uživatelským jménem "spencerl").

   c. Ujistěte se, že je vybrána položka **Zobrazit seznam dostupných organizací**.

      > [!div class="mx-imgBorder"]
      > ![Snímek obrazovky okna Package Deployer s vybranou možností „Zobrazit seznam dostupných organizací”](media/sample-data-2.png)

4. Vyberte organizaci, ve které chcete nainstalovat ukázková data.

5. Klikejte na **Další**, dokud se nezobrazí dialogové okno **Nastavení ukázkových dat**.

   > [!div class="mx-imgBorder"]
   > ![Screenshot stavového okna instalačního programu ukázkových dat.](media/sample-data-3.png)

6. Než budete pokračovat, všimněte si, že instalace ukázkových dat může trvat až jednu hodinu (obvykle ~ 10 minut). Bude nutné ujistit se, že počítač zůstává zapnutý a připojený k síti během procesu instalace a že vaše relace zůstane aktivní.   

7. Jakmile budete připraveni, kliknutím na tlačítko **Další** spusťte proces instalace ukázkových dat. Po načtení ukázkových dat klikněte na tlačítko **Dokončit**.

## <a name="verify-the-sample-data-installation"></a>Ověřte instalaci ukázkových dat

Z důvodu kontroly vhodnosti ověřte, že počet záznamů a typy entit uvedené ve fiktivním scénáři Fabrikam Robotics se chovají podle očekávání.

Poté, co se ukázková data zcela načtou, přihlaste se jako uživatel Spencer Low a potvrďte následující:

- Pokud je nainstalována aplikace Project Service, přejděte na **Project Service** > **Nastavení** > **Ceníky**. Potvrďte, že v datové sadě existují fakturované sazby a sazby nákladů, v příslušné měně pro každou zemi/oblast.

- Pokud je nainstalována aplikace Project Service, přejděte k **Universal Resource Scheduling** > **Nastavení** > **Organizační jednotky**. Ověřte, že byla ceníková cena v příslušné měně spojena s každou organizační jednotku (kromě záznamů města). Pokud některá chybí, najděte a přidružte seznam správné ceníkové ceny.

- Pokud je nainstalována aplikace Field Service, přejděte na **Project Service** > **Nastavení** > **Ceníky**. Ověřte, zda existují sazby fakturace a sazby nákladů. Přejděte na **Field Service** > **Nastavení** > **Ceníky** a zkontrolujte, že v datové sadě existují fakturované sazby a sazby nákladů, v příslušné měně pro každou zemi/oblast.

  > [!div class="mx-imgBorder"]
  > ![Screenshot aktivních ceníků.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Screenshot aktivních organizačních jednotek.](media/sample-data-5.png)

## <a name="technical-notes"></a>Technické poznámky

Níže naleznete bližší technické podrobnosti o instalaci těchto dat.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Instalace ukázkových dat nad rámec existujících dat (nedoporučeno)

Poznámka: Pokud potřebujete instalovat ukázková data ke stávající zkušební verzi aplikace Field Service nebo Project Service nebo jejich ukázkovému prostředí, které již obsahuje data (není doporučeno), bude nutné pozastavit předběžné kontroly bezpečnosti, které provádí instalační program.

Chcete-li to provést, přejděte do složky **PkgFolder** a vyhledejte a otevřete soubor **DemoDataPreImportConfig.xml** v programu Poznámkový blok (nebo v jiném editoru XML).

Najděte následující hodnotu a potom změňte nastavení z true na false:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Tato změna způsobí, že instalační program obejde některé důležité bezpečnostní kontroly, včetně:

- Potvrzení, že neexistuje více než jeden aktivní záznam **organizační jednotky** a jeho přejmenování na **Fabrikam US**.

- Potvrzení, že neexistuje více než jeden aktivní záznam **šablony práce**.

- Potvrzení, že neexistuje více než jeden aktivní záznam **parametru projektu** a následné přejmenování tohoto záznamu na **Parametry**.

### <a name="configuration-components"></a>Součásti konfigurace

V tomto konfiguračním souboru před importem existuje několik dalších součástí konfigurace. Pro technické uživatele, k některým z nich patří:

- **\<RequiredSolutions\>** určuje požadované instalace řešení a jejich čísla verzí.

- **\<InstallSampleData\>** řídí, zda jsou nainstalována přednastavená ukázková data pro aplikace.

    - nepravda - přeskočí instalace těchto integrovaných dat (které jsou vyměnitelné)

    - pravda - nainstaluje předdefinovaná data souběžně s instalací ukázkových dat FS a PSA

- **\<PreImportDataCollection\>** určuje soubor mapování dat a přidružené záznamy, které mají být importovány před instalaci hlavních ukázkových dat.

- **\<EntitiesToEnableScheduling\>** určuje, které entity by měly být povoleny pro rezervaci v aplikaci Microsoft Dynamics Scheduling (neboli Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** určuje rezervovatelné zdroje, které budou vytvořeny (pokud zatím neexistují). Všimněte si, že rezervovatelný zdroj ukázkových dat zdrojového systému odpovídá záznamům rezervovatelných zdrojů cílového systému u celého jména a přihlašovacích údajů každého ze zdrojů. Proto NENÍ možné změnit názvy v tomto souboru předběžné konfigurace, pokud nejprve neimportujete ukázková data do cílového systému pomocí těchto názvů, a potom nepřejmenujte rezervovatelné zdroje na požadovanou sadu názvů spolu s povolenými záznamy uživatele a potom znovu neexportujete data pro import do konečného cílového systému (aktualizace starých a nových položek **ImportUserMapFile.xml** odpovídajícím způsobem).

- **\<PluginsToDisable\>** určuje velmi samostatné pluginy položky řádku, které musí být zakázány během importu ukázkových dat a následně znovu povoleny.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fiktivní scénář společnosti Fabrikam Robotics

Balíčky referenčních ukázkových dat Field Service a Project Service instalují řešení **Fabrikam Manufacturing Master Data (v3.0.0.0)**, spolu s přibližně 4 000 záznamy a 40 různými entitami. Samostatné balíčky ukázkových dat pro aplikaci Field Service nebo Project Service obsahují dílčí sadu ukázkových dat **v902FPSMasterData** pro tuto aplikaci. Balíček **Ukázková Data** instaluje **řešení Fabrikam Manufacturing Demo Data (v3.0.0.7)** s přibližně 22 000 záznamů napříč 148 subjekty.

Fiktivní společnost Fabrikam Robotics je výrobce robotů montážní linky elektronických zařízení a je známá díky kvalitě svých výrobků, inovacím a solidním službám zákazníkům, včetně instalace, plánování, implementace a průběžných služeb údržby. Společnost Fabrikam sídlí ve Spojených státech (Fabrikam USA) a má operace služeb založené na projektu ve Francii, Indii, Spojeném království a Švýcarsku.

Provozy Field Service jsou ve Spojených státech, především v oblasti Seattlu. Společnost se zaměřuje na využití připojení k Internetu věcí (IoT) ke sledování výkonu majetku zákazníků a poskytování stále aktivnějších místních služeb.

Podrobný přehled ukázkových dat je následující:

- Společné prvky dat vzorku (zahrnuty pro obě aplikace)

    - 1 uživatel

    - 71 obchodních vztahů

    - 137 kontaktů

    - Různé typy transakcí a kategorií

    - 50 produktů s 1 ceníkem produktů

    - 14 ceníků/nákladových cen

    - 31 vlastností (dovedností zdrojů) v 2 modelech hodnocení se 3 úrovněmi (hodnoty hodnocení)

- Project Service

    - 8 organizačních jednotek

    - 6 úrovní využití specifických pro role

    - 2,8k a více specifikací role-cena

- Field Service

    - 4 území

    - 5 typů pracovních příkazů

    - 22 aktiv zákazníka

    - 9 typů incidentů s řadou přidružených vlastností zdroje (9), služby (13) a servisní úlohy (13)
   
Balíček **Ukázková Data** nainstaluje přibližně 179 pracovních příkazů, 12 projektů a přidružená transakční data. 

### <a name="change-the-work-hours-for-sample-resources"></a>Změna pracovní doby pro zdroje ukázek

Ve výchozím nastavení mají všechny rezervovatelné zdroje kalendář na 24 pracovních hodin.

Pokud potřebujete změnit pracovní dobu pro ukázkové rezervovatelné zdroje zdroje, přejděte k **Universal Resource Scheduling** > **Plánování** > **Zdroje**.

Vyberte uživatele (například Spencer Low) a změňte pracovní dobu Spencera na hodiny, které chcete použít u více uživatelů. Přejděte na **Universal Resource Scheduling** > **Nastavení** > **Šablony pracovní doby** a upravte záznam **Výchozí šablona práce**. V poli **Šablona zdroje** vyberte uživatele s pracovní dobou, kterou chcete použít pro jiné zdroje. Přejděte k **Universal Resource Scheduling** > **Plánování** > **Zdroje** > **Aktivní rezervovatelné zdroje**. Vyberte zdroje, které chcete změnit, a potom vyberte **Nastavit kalendář**. V rozevíracím seznamu **Šablona práce** vyberte šablonu **výchozí pracovní doba** nebo jinou šablonu se správným zdrojem šablon. Při přechodu na plánovací vývěsku byste si měli všimnout, že zdroje teď mají aktualizovanou pracovní dobu.

> [!div class="mx-imgBorder"]
> ![Screenshot aktivních rezervovatelných zdrojů.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]