---
title: Správa návrhů faktury projektu
description: Toto téma obsahuje informace o zpracování faktur pro zákazníky se systémem Project Operations pro scénáře se zdroji bez skladových materiálů.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089221"
---
# <a name="manage-project-invoice-proposals"></a>Správa návrhů faktury projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Vaše fakturační oddělení může zpracovat návrhy faktury za projekt, pokud jsou splněny následující dvě podmínky:

  - Manažer projektu potvrdí proforma fakturu v Microsoft Dataverse.
  - Všechny časově a materiálně nevyfakturované prodejní transakce, které jsou zahrnuty do pro forma faktury, se zaúčtují pomocí deníku integrace Dynamics 365 **Project Operations**.

Pomocí následujících kroků dokončete návrh faktury projektu v Dynamics 365 Finance.

1. Zkontrolujte fakturační údaje týkající se časových a věcných materiálových transakcí a zaúčtujte deník **integrace Project Operations**.
2. Zkontrolujte fakturační údaje pro milníky fakturace s pevnou cenou.
3. Zkontrolujte a naformátujte návrh faktury projektu.
4. Zveřejněte a vytiskněte projektové faktury.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Správa fakturačních údajů v deníku Project Operations Integration

Skutečné hodnoty projektu vytvořené v Dataverse jsou zkontrolovány a zaúčtovány v účetním financí podle projektu. Další informace o práci s deníkem integrace [viz Deník integrace v Project Operations](../project-accounting/project-operations-integration-journal.md).

Skutečné náklady a nevyfakturované skutečné tržby se přidají do deníku integrace jako samostatné řádky:

  - Jednotková nákladová cena a částka nákladů ve výchozím nastavení skutečných nákladů z transakce skutečných nákladů projektu v Dataverse.
  - Jednotková prodejní cena a částka prodeje u nevyfakturované prodejní transakce má výchozí hodnotu ze skutečné nevyfakturované prodejní transakce v Dataverse.

### <a name="billing-sales-tax"></a>Účtování daně z prodeje

Výpočet daně z prodeje pro fakturaci je určen kombinací polí **Skupina fakturace daně** a **Skupina daně z prodeje fakturační položky** na záznamu nevyfakturovaného prodeje na řádku deiníku **Integrace Project Operations**. Systém nastaví výchozí hodnoty těchto polí na základě nastavení na kartě **Finance** na stránce **Parametry řízení projektu a účetnictví**.

- **Metoda skupiny daně z prodeje** určuje výchozí logiku skupiny fakturace daně z prodeje:
  
  - **Projekt**: Bude vždy mít vždy výchozí hodnotu skupinu fakturace daně z prodeje z projektu. Můžete zkontrolovat nebo změnit výchozí skupinu fakturace daně z prodeje v projektu výběrem **Zobrazit výchozí účetnictví** na stránce **Všechny projekty**.
  - **Smlouva projektu**: Bude vždy mít vždy výchozí hodnotu skupinu fakturace daně z prodeje ze smlouvy projektu. Můžete zkontrolovat nebo změnit výchozí skupinu fakturace daně z prodeje ve smlouvě projektu výběrem **Zobrazit výchozí účetnictví** na stránce **Smlouvy projektu**.
  - **Zákazník**: Bude vždy mít vždy výchozí hodnotu skupinu fakturace daně z prodeje ze zákazníka.
  - **Vyhledávání**: Prohledá všechny výše uvedené entity a vybere první dostupnou hodnotu. Hledání začíná na entitě **Projekt**, pak na entitě **Smlouva projektu** a nakonec entitě **Zákazník**.

- **Metoda skupiny daně z prodeje položky** určuje výchozí logiku skupiny fakturace daně z prodeje položky:
  
  - U typů časových, výdajových a poplatkových transakcí bude mít skupina daně z prodeje fakturační položky vždy výchozí hodnotu z entity **Kategorie projektu**.
  - U typů materiálových transakcí je výchozí skupina daně z prodeje fakturační položky na základě nastavení **Metoda skupiny daně z prodeje položky** v části **Parametry řízení projektu a účetnictví**. Číslo položky má výchozí hodnotu skupiny daně z prodeje položky z entity **Vydaný produkt**. Kategorie má výchozí hodnotu skupiny daně z prodeje položky z entity **Kategorie produktu**.

### <a name="financial-dimensions"></a>Finanční dimenze

Finanční dimenze nevyfakturovaných záznamů o prodeji v deníku **integrace Project Operations** má výchozí hodnotu z entity **Projekt**. Finanční dimenze lze zkontrolovat a upravit výběrem **Rozdělit částky**. Pokud potřebujete změnit finanční dimenze nevyfakturovaného záznamu prodeje po zaúčtování deníku integrace, ale před potvrzením pro forma faktury, přejděte na **Všechny projekty** > **Spravovat** > **Zaúčtované transakce**, vyberte transakci a poté vyberte **Proces** > **Upravit účtování**.

### <a name="exchange-rates"></a>Směnné kurzy

Měna nevyfakturované transakce v Dataverse se používá jako měna transakce ve Finance a převádí se na zúčtovací měnu společnosti pomocí směnných kurzů definovaných ve Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Správa finančních atributů milníků fakturace 

Řádky projektové smlouvy využívající metodu fakturace s pevnou cenou jsou fakturovány prostřednictvím [Milníky pevné ceny](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Účetní projektu může zkontrolovat milníky fakturace ve Finance v nabídce **Řízení projektů a účetnictví** > **Všechny projekty** > **Spravovat** > **Transakce na účet**.

### <a name="billing-sales-tax"></a>Účtování daně z prodeje

Hodnoty **Skupina daně z prodeje** a **Skupina daně z prodeje položek** mají výchozí hodnoty z nastavení při vytváření nového milníku fakturace v Dataverse. Systém nastaví výchozí hodnoty těchto polí na základě nastavení na kartě **Finance** na stránce **Parametry řízení projektu a účetnictví**.

- **Metoda skupiny daně z prodeje** určuje výchozí logiku **skupiny fakturace daně z prodeje**:

    - **Projekt** bude vždy mít vždy výchozí hodnotu skupinu fakturace daně z prodeje z projektu. Můžete zkontrolovat nebo změnit výchozí skupinu daně z prodeje v projektu výběrem **Zobrazit výchozí účetnictví** na stránce **Všechny projekty**.
    - **Smlouva projektu** bude vždy mít vždy výchozí hodnotu skupinu fakturace daně z prodeje ze smlouvy projektu. Můžete zkontrolovat nebo změnit výchozí skupinu fakturace daně z prodeje ve smlouvě projektu výběrem **Zobrazit výchozí účetnictví** na stránce **Smlouvy projektu**.
    - **Zákazník** bude vždy mít vždy výchozí hodnotu skupinu fakturace daně z prodeje ze zákazníka.
    - **Vyhledávání** prohledá všechny výše uvedené entity v tomto seznamu a vybere první dostupnou hodnotu. Hledání začíná na entitě **Projekt**, pak na entitě **Smlouva projektu** a nakonec entitě **Zákazník**.

- **Skupina daně z prodeje položky s pevnou cenou** se používá jako výchozí hodnota pole **Skupina daně z prodeje položky**.

### <a name="financial-dimensions"></a>Finanční dimenze

Výchozí finanční dimenze pro milník fakturace s pevnou cenou jsou nastaveny na řádcích smlouvy projektu. Přejděte do **Smlouvy projektu** > **Zobrazit výchozí účetnictví** a na kartě **Řádky smlouvy** vyberte **řádek smlouvy ceny**, poté nastavte hodnoty finanční dimenze, které chcete použít jako výchozí.

Účetní projektu může upravovat informace o dani z obratu a finanční dimenzi na milnících faktur, dokud nebude vytvořen návrh faktury projektu.


## <a name="create-project-invoice-proposals"></a>Vytvoření návrhů faktury projektu

Návrhy faktury za projekt lze zkontrolovat v modulu **Řízení projektů a účetnictví** přejitím na **Faktury projektu** > **Návrhy faktury projektu**.

Záhlaví návrhu faktury projektu se vytvoří v aplikaci Finance, když je pro forma faktura potvrzena v Dataverse. Pro snazší odsouhlasení systém nastaví číslo návrhu faktury projektu ve Finance na stejné číslo jako ID pro forma faktury v Dataverse. Vzhledem k tomu, že pro forma faktury nemusí být nutně potvrzeny ve stejném pořadí, v jakém jsou vytvářeny, musí sekvence čísel návrhů faktury projektu v Finance umožňovat změny na nižší a vyšší čísla. Nakonfigurujte číselné řady pomocí následujících kroků:

1. Ve Finance přejděte na **Správa organizace** > **Číselné řady** > **Číselné řady**.
2. Ve filtru **Oblast** vyberte **Projekty**.
3. Ve filtru **Odkaz** vyberte **Návrh faktury**.
4. Použijte pole **Společnost** k filtrování jednotlivých právnických osob s aktivní integrací Project Operations Dataverse.
5. Otevřete **Podrobnosti o číselné posloupnosti** a na kartě **Všeobecné** nastavte:

    - **Povolit uživatelské změny: na nižší číslo** = **Ano**
    - **Povolit uživatelské změny: na vyšší číslo** = **Ano**

Řádky návrhu faktury projektu jsou přidávány systémem pomocí periodického procesu **Import z pracovní tabulky** (**Řízení projektů a účetnictví** > **Periodické** > **Integrace Project Operations** > **Import z pracovní tabulky**). Tento proces lze spustit ručně nebo pomocí pravidelného plánu. Systém nepřidá řádky do dokumentu návrhu faktury, dokud nejsou všechny řádky připraveny k fakturaci. Časové a materiálové transakce jsou připraveny k fakturaci, pouze pokud jsou zaúčtovány pomocí deníku **Integrace Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Formátování a tisk návrhů faktur projektu

Účetní projektu může přizpůsobit výtisk faktury projektu pomocí stránky **Formátovat návrh faktury** možností správy tisku.

### <a name="format-invoice-proposals"></a>Formátování návrhů faktur

Stránka **Formátovat návrhy faktur** umožňuje zobrazení vlastních seskupovacích transakcí na faktuře projektu zákazníka.

1. Na stránce **Návrh faktury projektu** vyberte **Vytisknout** > **Formátovat návrh faktury**.
2. Vyberte možnost **Nový** k vytvoření nového seskupení pro výtisk faktury projektu.
3. V poli **Detail/shrnutí** pole vyberte možnosti pro toto seskupení:

    - Vyberte možnost **Detail** k vytištění podrobností transakce na faktuře zákazníka.
    - Vyberte možnost **Souhrn** k vytištění souhrnu transakce na faktuře zákazníka.

> [!NOTE]
> Výběr v poli **Detail/Shrnutí** na stránce **Formátovat návrh faktury** přepíše volbu vybranou v poli **Formát faktury** na stránce **Návrhy fakturace** pro tisk podrobné faktury nebo souhrnné faktury.

- Vyberte řádky transakcí, které chcete zahrnout do této části na kartě **Dostupné transakce** a vyberte **Zahrnout transakce**, abyste je přesunuli na kartu **Vybrané transakce**.
- Vyberte **Posunout nahoru** a **Posunout dolů** ke změně pořadí sekcí.
- Vyberte **Náhled před tiskem** k zobrazení náhledu formátované faktury.

### <a name="print-management"></a>Správa tisku

Správa tisku používá různé soubory se sestavami k tisku, určení cílů a přizpůsobení textu zápatí pro fakturu. Správa tisku může být nastavena na úrovni modulu, ale tato nastavení lze přepsat pro konkrétního zákazníka, smlouvu nebo návrh faktury. Pro přístup k této funkci na stránce **Návrh faktury projektu** vyberte možnost **Vytisknout** > **Správa tisku**.

Nastavení správy tisku se zobrazuje jako stromové zobrazení, kde každá úroveň uzlu zobrazuje dostupné dokumenty, které lze upravit. Můžete přiřadit vlastní výtisky na úrovni modulu, zákazníka, smlouvy nebo faktury. Chcete-li upravit výtisk původního dokumentu, rozbalte požadovaný uzel a vyberte **Originální položka**. V poli **Formát zprávy** vyberte formát zprávy, který se má použít pro tisk. Můžete použít vlastní formáty zpráv pomocí [Rámec správy obchodních dokumentů](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Zaúčtování návrhů faktur

Poté, co bude faktura zkontrolována a upravena a řádky návrhu faktury budou uspokojivé, zkontrolujte součty faktur a daň z prodeje. Ve skupině **Detaily** vyberte **Součty** a poté vyberte **Zaúčtovat** k zaúčtování faktury.

Chcete-li před zaúčtováním zobrazit fakturu, zrušte zaškrtnutí políčka **Zaúčtování**. **Pro forma** bude vytištěno na faktuře, což znamená, že se jedná o vzorovou fakturu. Chcete-li fakturu vytisknout, vyberte zaškrtávací políčko **Tisk faktury**.

Kromě stránky **Návrh faktury** lze také návrhy faktur zveřejnit spuštěním periodické úlohy **Zaúčtovat návrhy faktur**. Chcete-li najít tuto úlohu, přejděte na **Řízení projektů a účetnictví** > **Periodické** > **Faktury projektu** > **Zaúčtovat návrhy faktur**.

Tato stránka zobrazuje všechny návrhy faktur, které jsou připraveny k zaúčtování. Můžete naplánovat odesílání návrhů faktur výběrem možnosti **Dávka**. Nastavte **Parametr dávkového zpracování** na **Ano** a nastavte opakování dávkového zpracování výběrem **Opakování**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]