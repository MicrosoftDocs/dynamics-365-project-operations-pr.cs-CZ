---
title: Správa proforma faktury založené na projektu
description: Tento téma poskytuje informace o tom, jak spravovat projektové proforma faktury a pracovat s nimi.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cba74c14f6d039dce0650f25ee04cbe35ec8f668b774cdaaa3bbf1aab99cb44d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989318"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Správa proforma faktury založené na projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

V Dynamics 365 Project Operations jsou proforma faktury vytvářeny rozšířením faktur v Dynamics 365 Sales. Pokud však jde o fakturaci, existuje mnoho rozdílů mezi Sales a Project Operations. Například není možné vytvořit novou fakturu ze stránky **Seznam faktur** v Project Operations, ale je to možné v Sales. Tyto rozdíly a rozšíření jsou zavedeny, aby podporovaly procesy fakturace u projektů, které se liší od typické fakturace za prodejní objednávku.

> [!IMPORTANT]
> Z důvodu rozdílů nepoužívejte zaměnitelně faktury v Sales a Project Operations.

## <a name="invoice-header"></a>Záhlaví faktury

Následující informace jsou k dispozici v záhlaví proforma faktury v Project Operations.

| Pole | Místo | Popis |
| --- | --- | --- | 
| **ID faktury** | Karta **Souhrn** | ID, které je automaticky generováno při vytvoření proforma faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. Toto pole se používá jako odkaz na každou proforma fakturu. |
| **Jméno** | Karta **Souhrn** | Ve výchozím nastavení má pole název projektové smlouvy. Toto pole lze upravovat. | 
| **Měna** | Karta **Souhrn** | Ve výchozím nastavení má pole měnu projektové smlouvy. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Ceník** | Karta **Souhrn** | Ve výchozím nastavení má pole ceník projektové smlouvy. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Příležitost** | Karta **Souhrn** | Odkaz na propojenou příležitost. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Smlouva** | Karta **Souhrn** | Odkaz na propojenou projektovou smlouvu. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Zákazník** | Karta **Souhrn** | Odkaz na propojenou projektovou smlouvu. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Popis** | Karta **Souhrn** | Textové pole, které popisuje fakturu. Toto pole lze upravovat. | 
| **Fakturační adresa** a související pole | **Karta Souhrn** | Výchozí hodnoty jsou nastaveny od zákazníka projektové smlouvy. Toto pole lze upravovat.  | 
| **Stav** | Karta **Souhrn** | Nastavuje následující možnosti: **Aktivní**, **Zavřeno**, **Zaplaceno** a **Zrušeno** a lze ho upravovat. Mezi nepodporované stavy v Project Operations patří **Uzavřeno** a **Zrušeno**. </br> Stav je nastaven na **Aktivní** při vytvoření faktury. </br>Stav by měl být nastaven na **Zaplaceno** až po potvrzení faktury.  | 
| **Stav projektové faktury** | Karta **Souhrn** | Nastavuje následující možnosti: **Koncept**, **Probíhá kontrola** a **Potvrzeno** a lze ho upravovat. V obou stavech **Koncept** a **Kontroluje se** lze fakturu upravit. Fakturu nelze po potvrzení upravit. | 
| **Výchozí částka** | Karta **Souhrn** | Součet částek na všech řádcích faktury po zálohách a odpočtech. Pole jen pro čtení, když je uzamčeno pro úpravy.  Toto pole se používá k výpočtu konečné částky. | 
| **Sleva (%)** | Karta **Souhrn** | Toto pole lze upravit a zadat procento slevy. Toto pole není podporováno funkcí Project Operations. Toto pole není podporováno.|  
| **Částka slevy** | Karta **Souhrn** | Toto pole lze upravit a zadat částku slevy. Toto pole není podporováno funkcí Project Operations. Toto pole není podporováno. |  
| **Částka bez přepravného** | **Karta Souhrn** | Celková částka faktury po uplatnění slev. Pole jen pro čtení, když je uzamčeno pro úpravy. Toto pole se používá k výpočtu konečné částky.  | 
| **Přepravné** | Karta **Souhrn** | Toto pole lze upravit a zadat částku bez přepravného. Toto pole není podporováno funkcí Project Operations. Toto pole není podporováno. |
| **Celková daň** | Karta **Souhrn** | Celková daň ze všech řádků faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Celková částka** | Karta **Souhrn** | Součet částky po uplatnění slev a daní. Součet je částka, kterou zákazník musí zaplatit. | 

## <a name="project-based-invoice-lines"></a>Řádky faktury založené na projektu

V Project Operations je vždy jeden řádek faktury pro každý řádek projektové smlouvy. Řádek faktury je vytvořen, i když neexistují žádné skutečné hodnoty. Následující informace jsou k dispozici na řádku proforma faktury.

| Pole | Místo | Popis | 
| --- | --- | --- |
| **ID faktury** | Karta **Obecné** | Odkaz na ID faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. Odkaz na ID faktury lze použít k přechodu zpět do záhlaví faktury. | 
| **Jméno** | Karta **Obecné** | Název řádku faktury nastavený ve výchozím nastavení z názvu řádku smlouvy. Toto pole lze upravovat. |
| **Project** | Karta **Obecné** | Projekt na souvisejícím řádku projektové smlouvy. Pole jen pro čtení, když je uzamčeno pro úpravy. Odkaz na projekt lze použít k přechodu k projektu. | 
| **Způsob fakturace** | Karta **Obecné** | Způsob fakturace na souvisejícím řádku projektové smlouvy. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Částka řádku smlouvy** | Karta **Obecné** | Částka smlouvy na souvisejícím řádku projektové smlouvy. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Fakturováno do data** | Karta **Obecné** | Součet částek ze všech podrobností řádku této faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Množství** | Karta **Obecné** | Součet částek ze všech podrobností účtovatelného řádku této faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. Toto pole se používá k výpočtu konečné částky v záhlaví faktury. | 
| **Daň** | Karta **Obecné** | Součet částek daně ze všech podrobností tohoto řádku faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. Toto pole se používá k výpočtu konečné částky daně v záhlaví faktury. | 
| **Rozšířená částka** | Karta **Obecné** | Součet celkových částek (**Daň + částky**) ze všech podrobností tohoto účtovatelného řádku faktury. Pole jen pro čtení, když je uzamčeno pro úpravy. Toto pole se používá k výpočtu konečné částky v záhlaví faktury. |

## <a name="invoice-line-details"></a>Podrobnosti řádku faktury

Každý řádek faktury projektu zahrnuje podrobnosti daného řádku. Tyto podrobnosti řádku souvisejí s nefakturovanými skutečnými hodnotami a milníky prodeje, které se vztahují k řádku smlouvy, na který odkazuje řádek faktury. Všechny tyto transakce jsou označeny jako **Připraveno k fakturaci**.

Pro řádek **Faktura za čas a materiál** jsou údaje řádku faktury seskupeny do skupin **Účtovatelné**, **Neúčtovatelné** a **Zdarma** na stránce **Řádek faktury**. Podrobnosti **účtovaného řádku faktury** se přičítají k celkovému součtu řádku faktury. **Neplacené** a **Neúčtovatelné skutečné hodnoty** se nepřičítají k celkovému součtu řádku faktury.

Pro řádek **Faktura s pevnou cenou** jsou údaje řádku faktury vytvořeny z milníků, které jsou označeny jako **Připraveno k fakturaci** na souvisejícím řádku smlouvy. Po vytvoření podrobnosti řádku faktury z milníku se stav fakturace u milníku aktualizuje na **Faktura zákazníka vytvořena**.

### <a name="edit-invoice-line-details"></a>Úprava podrobností řádku faktury

Následující pole jsou k dispozici v podrobnostech řádku faktury, které jsou podloženy nefakturovanou skutečnou hodnotou prodeje.

| Pole | Popis |
| --- | --- | 
| **Řádek faktury** | Odkaz na **ID řádku faktury**. Toto pole je pouze pro čtení a uzamčeno pro úpravy. Tento odkaz lze použít k přechodu zpět do záhlaví faktury. | 
| **Popis** | Popis podrobnosti řádku faktury. Hodnota je standardně nastavena z pole **Interní komentáře** v **Časový záznam** a z pole **Popis** v **Výdajová položka**. Pole lze upravovat.| 
| **Externí popis** | Popis podrobnosti řádku faktury. Hodnota je standardně nastavena z pole **Externí komentáře** v **Časový záznam** a z pole **Popis** v **Výdajová položka**. Pole lze upravovat. Tento popis lze použít k určení, co by mělo být na vytištěné faktuře, která bude zaslána zákazníkovi. V Project Operations nemá proforma faktura všechny požadované funkce pro konfiguraci nastavení tisku faktury. | 
| **Počáteční datum** | Toto pole je pouze ke čtení a je nastaveno ve výchozím nastavení ze zdrojové skutečné hodnoty. |
| **Project** | Toto je pole jen pro čtení, které je ve výchozím nastavení nastaveno ze zdrojové skutečné hodnoty na projekt na souvisejícím řádku smlouvy. |  
| **Úkol** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Kategorie transakce** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Role** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |  
| **Rezervovatelný zdroj** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Společnost poskytující zdroje** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Jednotka zdroje** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Množství** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |  
| **Rozpis jednotky** | V případě podrobnosti řádku faktury pro čas je hodnota vždy nastavena na čas a nelze ji upravovat. V případě výdajů je hodnota standardně nastavena podle skutečné hodnoty výdaje zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Jednotka** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |  
| **Cena** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Měna** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Množství** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Daň** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole lze upravovat.| 
| **Rozšířená částka** | Počítané pole, počítáno jako **Částka + daň**. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Typ fakturace** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole lze upravovat. Volba **Účtovatelné** připočítá řádek k součtu řádku faktury. **Neplacené** a **Neúčtovatelné** jej vyloučí ze součtu řádku faktury.| 
| **Vybrat produkt** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Produkt** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Název produktu** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |  
| **Popis produktu nezahrnutého do katalogu** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Typ transakce** | Toto pole je pouze ke čtení a je nastaveno ve výchozím nastavení ze zdrojové skutečné hodnoty na **Fakturovaný prodej**. |  
| **Třída transakce** | Hodnota je standardně nastavena podle skutečné hodnoty zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 

Následující pole jsou k dispozici v údaji řádku faktury, která vychází z milníku.

| Pole | Popis |
| --- | --- | 
| **Řádek faktury** | Odkaz na **ID řádku faktury**. Pole jen pro čtení, když je uzamčeno pro úpravy. Tento odkaz lze použít k přechodu zpět do záhlaví faktury.  | 
| **Popis** | Popis podrobnosti řádku faktury. Hodnota je standardně nastavena podle popisu milníku zdroje. | 
|**Externí popis** | Popis podrobnosti řádku faktury, která je standardně nastavena z popisu milníku zdroje. Tohle pole lze použít k určení, co by mělo být na vytištěné faktuře, která bude zaslána zákazníkovi. Proforma faktura v Project Operations nemá všechny požadované funkce pro konfiguraci nastavení tisku faktury. | 
| **Počáteční datum** | Hodnota je standardně nastavena podle data **milníku** zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Project** | Hodnota je standardně nastavena podle milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Úkol** | Hodnota je standardně nastavena podle milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Kategorie transakce** | Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Role** | Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Rezervovatelný zdroj** | Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Jednotka zdroje** | Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Rozpis jednotky** | Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Jednotka** | Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Cena** | Hodnota je standardně nastavena podle částky milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Měna** | Hodnota je standardně nastavena podle milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Množství** | Hodnota je standardně nastavena podle částky milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Daň** | Hodnota je standardně nastavena podle částky daně milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Rozšířená částka** | Hodnota je standardně nastavena podle rozšířené částky milníku zdroje. Pole lze upravovat. | 
| **Typ fakturace** | Hodnota je vždy standardně nastavena jako **Účtovatelné**. Pole jen pro čtení, když je uzamčeno pro úpravy. |
| **Typ transakce** | Hodnota je standardně nastavena podle milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 
| **Třída transakce** | Hodnota je standardně nastavena podle milníku zdroje. Pole jen pro čtení, když je uzamčeno pro úpravy. | 

## <a name="refresh-invoice-transactions"></a>Aktualizace transakcí faktury

Pokud máte skutečné hodnoty, které vznikly až po vytvoření faktury, můžete je zahrnout do faktury.

1. V **Zobrazení nedokončené fakturace** označte data jako **Připraveno k fakturaci**.   
2. Otevřete koncept proforma faktury a na pásu **Akce** vyberte **Obnovit transakce na řádku faktury**.

  Podrobnosti faktury se vytvářejí pro všechny skutečné údaje, jejichž datum a čas jsou označeny jako **Připraveno k fakturaci**, ale nejsou uvedeny na faktuře.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
