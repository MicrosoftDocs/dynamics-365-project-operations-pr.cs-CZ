---
title: Správa proforma faktury projektu
description: Tento článek poskytuje informace o práci s pro forma projektovými fakturami.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7253b2f8beefb970c573279b1873070219edce08
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922996"
---
# <a name="manage-a-proforma-project-invoice"></a>Správa proforma faktury projektu 

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

V Dynamics 365 Project Operations jsou proforma faktury vytvářeny rozšířením faktur v Dynamics 365 Sales. Pokud však jde o fakturaci, existuje mnoho rozdílů mezi Sales a Project Operations. Například není možné vytvořit novou fakturu ze stránky **Seznam faktur** v Project Operations, ale je to možné v Sales. Tyto rozdíly a rozšíření jsou zavedeny, aby podporovaly procesy fakturace u projektů, které se liší od typické fakturace za prodejní objednávku.

> [!IMPORTANT]
> Z důvodu rozdílů nepoužívejte zaměnitelně faktury v Sales a Project Operations.

## <a name="invoice-header"></a>Záhlaví faktury

Následující informace jsou k dispozici v záhlaví proforma faktury v Project Operations.

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| **ID faktury** | Karta **Souhrn** | ID, které je automaticky generováno při vytvoření proforma faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole se používá jako odkaz na každou proforma fakturu. |
| **Jméno** | Karta **Souhrn** | Ve výchozím nastavení má pole název projektové smlouvy. Toto pole může uživatel upravit. | &nbsp;  |
| **Měna** | Karta **Souhrn** | Ve výchozím nastavení má pole měnu projektové smlouvy. Pole jen pro čtení, když je uzamčeno pro úpravy. |&nbsp; |
| **Ceník** | Karta **Souhrn** | Ve výchozím nastavení má pole ceník projektové smlouvy. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Příležitost** | Karta **Souhrn** | Odkaz na propojenou příležitost. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp;  |
| **Smlouva** | Karta **Souhrn** | Odkaz na propojenou projektovou smlouvu. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Zákazník** | Karta **Souhrn** | Odkaz na propojenou projektovou smlouvu. Pole jen pro čtení, když je uzamčeno pro úpravy. |&nbsp;  |
| **Popis** | Karta **Souhrn** | Textové pole, které popisuje fakturu. Toto pole může uživatel upravit. | &nbsp; |
| **Fakturační adresa** a související pole | **Karta Souhrn** | Výchozí hodnoty jsou nastaveny od zákazníka projektové smlouvy. Toto pole může uživatel upravit.  | &nbsp; |
| **Stav** | Karta **Souhrn** | Nastavuje následující možnosti: **Aktivní**, **Uzavřeno**, **Zaplaceno** a **Zrušeno**, a uživatel jej může upravit. | Mezi nepodporované stavy v Project Operations patří **Uzavřeno** a **Zrušeno**. </br> Stav je nastaven na **Aktivní** při vytvoření faktury. </br>Stav by měl být nastaven na **Zaplaceno** až po potvrzení faktury. |
| **Stav projektové faktury** | Karta **Souhrn** | Nastavuje následující možnosti: **Koncept**, **Kontroluje se** a **Potvrzeno**, a uživatel jej může upravit. | V obou stavech **Koncept** a **Kontroluje se** lze fakturu upravit. Fakturu nelze po potvrzení upravit. |
| **Výchozí částka** | Karta **Souhrn** | Součet částek na všech řádcích faktury po zálohách a odpočtech. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole se používá k výpočtu konečné částky. |
| **Sleva (%)** | Karta **Souhrn** | Toto pole lze upravit a zadat procento slevy. Toto pole není podporováno funkcí Project Operations. | Toto pole není podporováno. |
| **Částka slevy** | Karta **Souhrn** | Toto pole lze upravit a zadat částku slevy. Toto pole není podporováno funkcí Project Operations. | Toto pole není podporováno. |
| **Částka bez přepravného** | **Karta Souhrn** | Celková částka faktury po uplatnění slev. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole se používá k výpočtu konečné částky. |
| **Přepravné** | Karta **Souhrn** | Toto pole lze upravit a zadat částku bez přepravného. Toto pole není podporováno funkcí Project Operations. | Toto pole není podporováno. |
| **Celková daň** | Karta **Souhrn** | Celková daň ze všech řádků faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. | Žádné |
| **Celková částka** | Karta **Souhrn** | Součet částky po uplatnění slev a daní. | Součet je částka, kterou zákazník musí zaplatit. |
## <a name="project-based-invoice-lines"></a>Řádky faktury založené na projektu

V Project Operations je vždy jeden řádek faktury pro každý řádek projektové smlouvy. Řádek faktury je vytvořen, i když neexistují žádné skutečné hodnoty. Následující informace jsou k dispozici na řádku proforma faktury.

| Pole | Místo | Popis | Dopad na následné složky |
| --- | --- | --- | --- |
| **ID faktury** | Karta **Obecné** | Odkaz na ID faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. | Odkaz na ID faktury lze použít k přechodu zpět do záhlaví faktury. |
| **Jméno** | Karta **Obecné** | Název řádku faktury nastavený ve výchozím nastavení z názvu řádku smlouvy. Toto pole může uživatel upravit. | &nbsp; |
| **Project** | Karta **Obecné** | Projekt na souvisejícím řádku projektové smlouvy. Pole jen pro čtení, když je uzamčeno pro úpravy. | Odkaz na projekt lze použít k přechodu k projektu. |
| **Způsob fakturace** | Karta **Obecné** | Způsob fakturace na souvisejícím řádku projektové smlouvy. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Částka řádku smlouvy** | Karta **Obecné** | Částka smlouvy na souvisejícím řádku projektové smlouvy. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Fakturováno do data** | Karta **Obecné** | Součet částek ze všech podrobností řádku této faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Množství** | Karta **Obecné** | Součet částek ze všech podrobností účtovatelného řádku této faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole se používá k výpočtu konečné částky v záhlaví faktury. |
| **Daň** | Karta **Obecné** | Součet částek daně ze všech podrobností tohoto řádku faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole se používá k výpočtu konečné částky daně v záhlaví faktury. |
| **Rozšířená částka** | Karta **Obecné** | Součet celkových částek (**Daň + částky**) ze všech podrobností tohoto účtovatelného řádku faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole se používá k výpočtu konečné částky v záhlaví faktury. |


## <a name="invoice-line-details"></a>Podrobnosti řádku faktury

Každý řádek faktury projektu zahrnuje podrobnosti daného řádku. Tyto podrobnosti řádku souvisejí s nefakturovanými skutečnými hodnotami a milníky prodeje, které se vztahují k řádku smlouvy, na který odkazuje řádek faktury. Všechny tyto transakce jsou označeny jako **Připraveno k fakturaci**.

Pro řádek **Faktura za čas a materiál** jsou údaje řádku faktury seskupeny do skupin **Účtovatelné**, **Neúčtovatelné** a **Zdarma** na stránce **Řádek faktury**. Podrobnosti **účtovaného řádku faktury** se přičítají k celkovému součtu řádku faktury. **Zdarma** a **Neúčtovatelné skutečné hodnoty** se nepřičítají k součtovému řádku faktury.

Pro řádek **Faktura s pevnou cenou** jsou údaje řádku faktury vytvořeny z milníků, které jsou označeny jako **Připraveno k fakturaci** na souvisejícím řádku smlouvy. Po vytvoření podrobnosti řádku faktury z milníku se stav fakturace u milníku aktualizuje na **Faktura zákazníka vytvořena**.

### <a name="edit-invoice-line-details"></a>Úprava podrobností řádku faktury

Následující pole jsou k dispozici v podrobnostech řádku faktury, které vychází z nefakturované skutečné hodnoty prodeje:

| Pole | Popis | Dopad na následné složky |
| --- | --- | --- |
| **Řádek faktury** | Odkaz na **ID řádku faktury**. Pole jen pro čtení, uzamčeno pro úpravy. | Tento odkaz lze použít k přechodu zpět do záhlaví faktury. |
| **Popis** | Popis podrobnosti řádku faktury. Hodnota je standardně nastavena z pole **Interní komentáře** v **Časový záznam** a z pole **Popis** v **Výdajová položka**. Toto pole může uživatel upravit.| &nbsp; |
| **Externí popis** | Popis podrobnosti řádku faktury. Hodnota je standardně nastavena z pole **Externí komentáře** v **Časový záznam** a z pole **Popis** v **Výdajová položka**. Toto pole může uživatel upravit. | Tento popis lze použít k určení, co by mělo být na vytištěné faktuře, která bude zaslána zákazníkovi. V Project Operations nemá proforma faktura všechny požadované funkce pro konfiguraci nastavení tisku faktury. |
| **Počáteční datum** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole lze upravit v nové podrobnosti řádku faktury, která nevychází ze skutečné hodnoty zdroje. |
| **Project** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Standardně nastaveno na projekt na souvisejícím řádku smlouvy. |
| **Úkol** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole lze upravit v nové podrobnosti řádku faktury, která nevychází ze skutečné hodnoty zdroje. Rozevírací seznam zobrazuje všechny úkoly, které jsou přidruženy k příslušnému řádku projektové smlouvy.  |
| **Kategorie transakce** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole lze upravit v nové podrobnosti řádku faktury, která nevychází ze skutečného zdroje. |
| **Role** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole lze upravit v nové podrobnosti řádku faktury, která nevychází ze skutečné hodnoty zdroje. |
| **Rezervovatelný zdroj** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole lze upravit v nové podrobnosti řádku faktury, která nevychází ze skutečného zdroje. |
| **Jednotka zdroje** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole lze upravit v nové podrobnosti řádku faktury, která nevychází ze skutečné hodnoty zdroje. |
| **Množství** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole lze upravit v nové podrobnosti řádku faktury, která nevychází ze skutečné hodnoty zdroje. |
| **Rozpis jednotky** | V případě podrobnosti řádku faktury pro čas je hodnota vždy nastavena na čas a nelze ji upravovat. V případě výdajů je hodnota standardně nastavena podle skutečné hodnoty výdaje zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Hodnota je standardně nastavena na **Čas** v nové podrobnosti řádku faktury, která nevychází ze skutečné hodnoty. |
| **Jednotka** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole lze upravit v nové podrobnosti řádku faktury, která nevychází ze skutečné hodnoty zdroje. |
| **Cena** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Toto pole lze upravit v nové podrobnosti řádku faktury, která nevychází ze skutečné hodnoty zdroje. Pokud není zadána žádná hodnota, standardně se nastaví po stisknutí tlačítka **Uložit**. |
| **Měna** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Hodnota je standardně nastavena ze záhlaví faktury při vytvoření nové podrobnosti řádku faktury, která nevychází ze skutečné hodnoty.  Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Množství** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Vypočítáno jako **Množství \* Cena** při vytváření nové podrobnosti faktury, která nevychází ze skutečné hodnoty. Vypočítá se po stisknutí **Uložit**. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Daň** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Toto pole může uživatel upravit. | Toto pole může uživatel upravit při vytvoření nové podrobnosti řádku faktury, která nevychází ze skutečné hodnoty. |
| **Rozšířená částka** | Počítané pole, počítáno jako **Částka + daň**. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Typ fakturace** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Toto pole může uživatel upravit. | Volba **Účtovatelné** připočítá řádek k součtu řádku faktury. **Neplacené** a **Neúčtovatelné** jej vyloučí ze součtu řádku faktury. |
| **Vybrat produkt** | Toto pole je nastaveno ve výchozím nastavení ze zdrojové skutečné hodnoty a je jen pro čtení. | Když vytvoříte nový údaj řádku faktury bez podkladové skutečné hodnoty, lze toto pole upravit. |
| **Produkt** | Toto pole je nastaveno ve výchozím nastavení ze zdrojové skutečné hodnoty a je jen pro čtení. | Když vytvoříte nový údaj řádku faktury bez podkladové skutečné hodnoty, lze toto pole upravit, pokud je pole **Vybrat produkt** nastaveno na **Stávající produkt**. |
| **Název produktu** | Toto pole je nastaveno ve výchozím nastavení ze zdrojové skutečné hodnoty a je jen pro čtení. | V novém detailu řádku faktury, kde je ID produktu vybráno z katalogu, je toto pole nastaveno na název produktu. U produktu, který je není v katalogu, je pole nastaveno na název pro zápis. |
| **Popis produktu nezahrnutého do katalogu** | Toto pole je nastaveno ve výchozím nastavení ze zdrojové skutečné hodnoty a je jen pro čtení. | Když vytvoříte nový údaj řádku faktury bez podkladové skutečné hodnoty, můžete k produktu přidat popis. |
| **Typ transakce** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Hodnota je standardně nastavena na **Fakturovaný prodej** a uzamčena při vytváření nové **podrobnosti řádku faktury**, která nevychází ze skutečné hodnoty.  |
| **Třída transakce** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | Nastaveno ve výchozím nastavení podle toho, zda se uživatel rozhodne vytvořit údaj řádku faktury **Čas**, **Výdaje**, **Materiál** nebo **Poplatek** a zároveň vytvořit nový **Údaj řádku faktury** bez skutečné podkladové hodnoty. Uzamčeno pro úpravy. |

Následující pole jsou k dispozici v podrobnosti řádku faktury, která vychází z milníku.

| Pole | Popis | Dopad na následné složky |
| --- | --- | --- |
| **Řádek faktury** | Odkaz na **ID řádku faktury**. Pole jen pro čtení, když je uzamčeno pro úpravy. | Tento odkaz lze použít k přechodu zpět do záhlaví faktury. |
| **Popis** | Popis podrobnosti řádku faktury. Hodnota je standardně nastavena podle popisu milníku zdroje. | &nbsp; |
|**Externí popis** | Popis podrobnosti řádku faktury, která je standardně nastavena z popisu milníku zdroje. | Tohle pole lze použít k určení, co by mělo být na vytištěné faktuře, která bude zaslána zákazníkovi. Proforma faktura v Project Operations nemá všechny požadované funkce pro konfiguraci nastavení tisku faktury. |
| **Počáteční datum** | Hodnota je standardně nastavena podle data **milníku** zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Project** | Hodnota je standardně nastavena podle milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Úkol** | Hodnota je standardně nastavena podle milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Kategorie transakce** | Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Role** | Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Rezervovatelný zdroj** | Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Jednotka zdroje** | Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Rozpis jednotky** | Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Jednotka** | Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Cena** | Hodnota je standardně nastavena podle částky milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Měna** | Hodnota je standardně nastavena podle milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |&nbsp; |
| **Množství** | Hodnota je standardně nastavena podle částky milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Daň** | Hodnota je standardně nastavena podle částky daně milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Rozšířená částka** | Hodnota je standardně nastavena podle rozšířené částky milníku zdroje. Toto pole může uživatel upravit. | &nbsp; |
| **Typ fakturace** | Hodnota je vždy standardně nastavena jako **Účtovatelné**. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Typ transakce** | Hodnota je standardně nastavena podle milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |
| **Třída transakce** | Hodnota je standardně nastavena podle milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Vytvoření nových podrobností řádku faktury

Na řádcích faktury času a materiálu můžete vytvořit nové podrobnosti řádku faktury. Tyto podrobnosti řádku faktury nevychází ze skutečné hodnoty. Na řádku faktury času a materiálu můžete volbou **Nový** vytvořit novou podrobnost řádku faktury pro třídy transakcí, které jsou zahrnuty na řádku smlouvy.

## <a name="refresh-invoice-transactions"></a>Aktualizace transakcí faktury

Pokud máte skutečné hodnoty, které vznikly až po vytvoření faktury, můžete je zahrnout do faktury.

1. V **Zobrazení nedokončené fakturace** označte data jako **Připraveno k fakturaci**.   
2. Otevřete koncept proforma faktury a na pásu karet **Akce** klikněte na **Aktualizovat transakce řádku faktury**.

  Tím se vytvoří podrobnosti řádku faktury pro všechny skutečné hodnoty, jejichž datum a čas jsou označeny jako **Připraveno k fakturaci**; ale nejsou součástí faktury.

## <a name="product-based-invoice-lines"></a>Řádky faktury založené na produktu

V Project Operations můžete vytvořit řádky faktury pro produkty, které se nevztahují na žádný projekt, nebo pro všechny projekty společně s řádky faktury založené na projektu. Tyto řádky faktury jsou vytvořeny jako řádky smlouvy na základě produktu a poté, co jsou označeny jako připravené k fakturaci, jsou přidány jako řádky faktury na základě produktu.

Jakmile přidáte řádky faktury na základě produktu, nelze je změnit. Mohou však být z konceptu proforma faktury odstraněny.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
