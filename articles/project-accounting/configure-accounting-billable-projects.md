---
title: Konfigurace účetnictví pro fakturovatelné projekty
description: Toto téma poskytuje informace o možnostech účtování pro fakturovatelné projekty.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1159a31ba4f30f09734bf9c5a9e594b5c77a831e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596456"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfigurace účetnictví pro fakturovatelné projekty

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Dynamics 365 Project Operations podporuje různé možnosti účtování pro fakturovatelné projekty, které zahrnují časové a věcné transakce a transakce s pevnou cenou.

- **Časové a materiálové transakce**: Tyto transakce jsou fakturovány podle postupu práce na základě spotřeby hodin, výdajů, položek nebo poplatků na projektu. Tyto transakční náklady lze porovnat s výnosy z každé transakce a projekt je fakturován podle postupu práce. Výnosy z projektu lze také akumulovat v době, kdy k transakci dojde. Během fakturace jsou výnosy uznány a časově rozlišené výnosy jsou případně stornovány.
- **Transakce s pevnou cenou**: tyto transakce fakturovány podle plánu fakturace, který je založen na smlouvě o projektu. Výnosy z transakcí s pevnou cenou lze uznat při fakturaci nebo vypočítat a zaúčtovat pravidelně podle metody **Dokončená smlouva** nebo **Dokončené procento**.

Projekt je považován za fakturovatelný, pokud je spojen s jedním nebo více řádků smlouvy. Řádek smlouvy projektu sám definuje, které způsoby fakturace a typy transakcí jsou povoleny.

Například společnost Fabrikam Robotics získala projektovou smlouvu se společností Adatum pro optimalizaci zařízení. Adatum zaplatí pevnou částku $10000 USD na pokrytí vzniklých výdajů na projekt. Toto je metoda fakturace za pevnou cenu. Čas projektu a poplatky budou účtovány za použití. Jedná se o metodu fakturace času a materiálu. Celá práce bude sledována v rámci jediného projektu s názvem Optimalizace zařízení Adatum.

Člen projektového týmu předloží osm hodin práce na projektu optimalizace zařízení Adatum. Když projektový manažer tuto dobu schválí, systém použije metodu fakturace času a materiálu k vytvoření skutečných transakcí, faktury a účtu. Tato transakce nebude zahrnuta do výpočtu odhadu výnosů z pevné ceny.

Další člen projektového týmu předkládá cestovní náklady za $2000,00 USD oproti projektu optimalizace zařízení Adatum. Když projektový manažer jeho náklady schválí, systém použije metodu fakturace za pevnou cenu k vytvoření skutečných transakcí a účtu k zaúčtování výdajů ná tento projekt. Zákazníkov neobdrží fakturu na základě této transakce. Místo toho mu bude fakturováno pomocí samostatně nakonfigurovaných milníků fakturace. Tato transakce výdajů spolu s odhady výdajů bude zahrnuta do výpočtu odhadu výnosů z pevné ceny.

Účetní zásady pro transakce projektu jsou definovány v nákladových a výnosových profilech projektu. Pro každou transakci projektu systém určí příslušný profil nákladů a výnosů projektu pomocí pravidel projektu a profilů výnosů, které byly nakonfigurovány.

## <a name="define-project-cost-and-revenue-profiles"></a>Definice nákladů projektu a profilů výnosů 

Náklady projektu a profily výnosů určují pravidla zúčtování projektových transakcí. Tyto profily jsou konfigurovány v části Správa projektů a účetnictví. 

Pomocí následujících kroků vytvořte nový profil nákladů a výnosů projektu. 

1. Přejděte na **Řízení projektů a účetnictví** > **Nastavení** > **Zaúčtovat** > **Profily nákladů a výnosů projektu**. 
2. Vyberte **Nový** k vytvoření nového profilu nákladů a výnosů projektu.
3. V poli **Název** zadejte název a krátký popis profilu.
4. V poli **Způsob účtování** vyberte **Čas a materiál** nebo **Pevná cena**.
5. Rozbalte pevnou záložku **Účetní kniha**. Pole na této kartě definují účetní zásady, které se používají, když jsou transakce projektu zapsány do deníku pomocí deníku integrace Project Operations a poté fakturovány prostřednictvím návrhu faktury projektu.
6. Vyberte příslušné informace v následujících polích na pevné záložce **Hlavní kniha**:

    - **Zaúčtovat náklady - hodiny**:

       - *Žádná hlavní kniha*: Cena za časové transakce nebude zaúčtována do hlavní knihy, když bude zaúčtován deník integrace Project Operations. Účetní však může zaúčtovat náklady pomocí funkce Zaúčtovat náklady později.
       - **Zůstatek**: Náklady za časové transakce budou odečteny z účtu hlavní knihy typem *Nedokončená práce - hodnota nákladů* a připsány na *Účet přidělování mezd* v nastavení účtování v hlavní knize. Účetní bude pomocí funkce Zaúčtovat náklady pravidelně přesouvat tyto náklady z účtu zůstatku na účet zisků a ztrát.
       - **Zisk a ztráta**: Při zaúčtování deníku integrace Project Operations budou náklady za časovou transakci odečteny z účtu hlavní knihy typu *Náklady* a připsány na *Účet přidělování mezd* definovaný na kartě **Náklady** na stránce **Nastavení účtování hlavní knihy** (**Řízení projektů a účetnictví** \> **Nastavení** \> **Účtování** \> **Nastavení účtování hlavní knihy**). Toto je nejběžnější nastavení pro časové a materiálové transakce.
        - *Nikdy hlavní kniha*: Cena za časové transakce nebude nikdy zaúčtována do hlavní knihy.

    - **Zaúčtování nákladů - výdaje**:

         - **Zůstatek** : Při zaúčtování deníku integrace Project Operations budou náklady výdajových transakcí odečteny z účtu hlavní knihy typem *Nedokončená práce - hodnota nákladů*, jak je definováno na kartě **Náklady** na stránce **Nastavení účtování hlavní knihy** a připsány na offsetový účet na řádku deníku. Výchozí offsetové účty pro výdaj jsou definovány v **Řízení projektů a účetnictví** > **Nastavení** \> **Účtování** \> **Výchozí offsetový účet pro výdaje**. Účetní bude pomocí funkce **Zaúčtovat náklady** pravidelně přesouvat tyto náklady z účtu zůstatku na účet zisků a ztrát.
        - **Zisk a ztráta**: Při zaúčtování deníku integrace Project Operations budou náklady výdajových transakcí odečteny z účtu hlavní knihy typem *Náklady*, jak je definováno na kartě **Náklady** na stránce **Nastavení účtování hlavní knihy** a připsány na offsetový účet na řádku deníku. Výchozí offsetové účty pro výdaj jsou definovány v **Řízení projektů a účetnictví** \> **Nastavení** \> **Účtování** \> **Výchozí offsetový účet pro výdaje**.
      
    - **Zaúčtovat náklady – položka**:

         - **Zůstatek**: Při zaúčtování deníku Project Operations Integration budou náklady transakce položky odečteny z typu účtu hlavní knihy *WIP – hodnota nákladů – položka*, jak je definováno na kartě **Náklady** na stránce **Nastavení účtování hlavní knihy** a připsány na následující:
    
              - Při typu dokumentu použití: Účet **Náklad – položka** účet na **Nastavení účtování hlavní knihy**.  
              - Při typu dokumentu nákup: **Účet integrace nákupu** na **Parametry projektového řízení a účetnictví**.
           Účetní bude pomocí funkce **Zaúčtovat náklady** pravidelně přesouvat tyto náklady z účtu zůstatku na účet zisků a ztrát.
        - **Zisk a ztráta**: Při zaúčtování deníku Project Operations Integration budou náklady transakce položky odečteny z typu účtu hlavní knihy *Náklad*, jak je definováno na kartě **Náklady** na stránce **Nastavení účtování hlavní knihy** a připsány na následující:
         
             - Při typu dokumentu použití: Účet **Náklad – položka** účet na **Nastavení účtování hlavní knihy**.  
             - Při typu dokumentu nákup: **Účet integrace nákupu** na **Parametry projektového řízení a účetnictví**.
       
    - **Fakturace na účet**:

        - **Zůstatek** : Při zaúčtování návrhu faktury projektu bude transakce na účtu (milník fakturace) připsána na typ účtu hlavní knihy *Fakturovaná nedokončená práce - na účet*, jak je definováno na kartě **Výnosy** na stránce **Nastavení účtování hlavní knihy** a odečtena z účtu zůstatku zákazníka.
         - **Zisk a ztráta**: Při zaúčtování návrhu faktury projektu bude transakce na účtu (milník fakturace) připsána na typ účtu hlavní knihy *Fakturované výnosy - na účet*, jak je definováno na kartě **Výnosy** na stránce **Nastavení účtování hlavní knihy** a odečtena z účtu zůstatku zákazníka. Účty zůstatku zákazníka jsou definovány v **Pohledávky** \> **Nastavení** \> **Profily účtování zákazníků**.

   Když definujete profily účtování pro metody účtování času a materiálu, máte možnost seskupit výnosy podle typu transakce (hodina, výdaj, položka a poplatek). Pokud je možnost **Časové rozložzit výnosy** nastavena na **Ano**, nevyfakturované prodejní transakce v deníku integrace Project Operations budou zaznamenány do hlavní knihy. Hodnota prodeje je odepsána z **Nedokončené práce - účet hodnoty prodeje** a připsána na účet **Časově rozložené příjmy - hodnota prodeje**, který byl zřízen na stránce **Nastavení účtování hlavní knihy** na kartě **Výnosy**. 
  
  > [!NOTE]
  > Možnost **Časově rozložit příjmy** je k dispozici pouze v případě, že příslušný typ transakce **Náklady** se zaúčtuje na účet zisků a ztrát.
    
7. Rozbalte pevnou záložku **Odhad**. Pole na této kartě definují nastavení výpočtu pro odhady výnosů z pevné ceny. Pole na této kartě se vztahují pouze na profily nákladů a výnosů projektu s metodou fakturace **Pevná cena**.
8. Vyberte příslušné informace v následujících polích na pevné záložce **Odhad**:

    - **Zásada použitá pro výpočty dokončení projektu**:

        - **Dokončená smlouva**: K porovnávání nákladů a rozpoznávání výnosů dojde až na konci projektu. Náklady se odrážejí jako Nedokončená práce v zůstatku, dokud není projekt dokončen.
        - **Dokončené procento**: Časově rozlišené výnosy se počítají a zaúčtují do účetní knihy každé období na základě procenta dokončení projektu. Existuje několik metod pro výpočet procentního dokončení. Tyto metody mohou být na základě konfigurace automatické nebo ruční.
        - **Žádné nedokončené práce**: Toto nastavení se používá pro projekty s pevnou cenou s krátkým časovým rozpětím a kde se faktura a náklady vyskytují ve stejném období. V tomto případě je hodnota pole **Fakturace na účet** na pevné záložce **Účetní kniha** automaticky nastavena na **Zisk a ztráta**, aby se zajistilo, že jsou výnosy uznány při fakturaci. Proces odhadu výnosů nebude použit pro tento profil nákladů a výnosů projektu.

    - **Zásada přiřazení**: Toto pole určuje, jak bude vypočítaná hodnota prodeje (časově rozložený výnos) zaúčtována do hlavní knihy.

        - Při použití zásady **Hodnota prodeje** systém vypočítá hodnotu prodeje přiřazením nákladů a výnosů a poté je zaúčtuje jako jednu částku.
        - Při použití zásady **Výroba a zisk** systém rozdělí hodnotu prodeje na realizované náklady a vypočítaný zisk. Ty jsou zaúčtovány samostatně.

    - **Šablony nákladů**: Povolit seskupování transakcí projektu na základě typu transakce a kategorie projektu a definovat pravidla výpočtu procentního dokončení pro tyto skupiny.
    - **Kódy období**: Definujte frekvenci, s jakou se počítají odhady výnosů pro daný profil nákladů a výnosů projektu.
    - **Kategorie pro odhad**: Používá se pro prodejní hodnotu (časově rozložený výnos) zaúčtování do transakcí projektu. Nejprve nakonfigurujte kategorii vyhrazeného projektu pro typ transakce **Poplatek** a poté nastavte příznak **Odhad** pro tuto kategorii projektu. Dále v závislosti na vybraném principu párování vyberte tuto kategorii projektu v hodnotě **Prodej** nebo poli **Zisk** v profilu nákladů a výnosů projektu.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Ukázkové konfigurace pro profily nákladů a výnosů projektu

Čas a materiál - bez nedokončené práce

![Profil nákladů a výnosů: čas a materiály - bez nedokončené práce.](media/time-material-no-wip.png)

Čas a materiál - nedokončené práce (výnos)

![Profil nákladů a výnosů: čas a materiály - nedokončené práce.](media/time-material-with-wip.png)

Pevná cena - bez nedokončené práce

![Profil nákladů a výnosů: pevná cena - bez nedokončené práce.](media/fixed-price-no-wip.png)

Fixní cena - dokončená smlouva

![Profil nákladů a výnosů: pevná cena - dokončená smlouva.](media/fixed-price-completed-contract.png)

Fixní cena - dokončení v procentech

![Profil nákladů a výnosů: pevná cena - dokončení v procentech.](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Příklady účetních událostí pro ukázkové profily nákladů a výnosů projektu.

| Účetní událost                  | Čas a materiál - bez nedokončené práce                       | Čas a materiál - nedokončená práce                                                                                           | Pevná cena - bez nedokončené práce                                            | Pevná cena - dokončená smlouva                                                                            | Pevná cena - dokončení v procentech                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Zápis časových transakcí do deníku    | Debet - náklady <br>Kredit - přidělení mezd          | Debet - náklady <br>Kredit - přidělení mezd <br>Debet - hodnota prodeje nedokončené práce <br>Kredit - Hodnota prodeje časově rozložených výdajů                | Debet - náklady <br>Kredit - přidělení mezd                         | Debet - náklady <br>Kredit - přidělení mezd                                                                    | Debet - náklady <br>Kredit - přidělení mezd                       |
| Zápis výdajových transakcí do deníku | Debet - náklady <br>Kredit - offsetový účet pro výdaje | Debet - náklady <br>Kredit - offsetový účet pro výdaje <br>Debet - hodnota prodeje nedokončené práce <br>Kredit - Hodnota prodeje časově rozložených výdajů      | Debet - náklady <br>Kredit - offsetový účet pro výdaje                 | Debet - náklady<br> Kredit - offsetový účet pro výdaje                                                            | Debet - náklady <br>Kredit - offsetový účet pro výdaje               |
| Fakturace zákazníla                | Debet - zůstatek zákazníka <br>Kredit - Fakturované výnosy | Debet - zůstatek zákazníka <br>Kredit - Fakturované výnosy <br>Kredit - debet hodnota prodeje nedokončené práce - hodnota prodeje časově rozložených výnosů | Debet - zůstatek zákazníka <br>Kredit - Fakturovaný výnos - na účet | Debet - zůstatek zákazníka <br>Kredit - nedokončená práce - fakturováno na účet                                                  | Debet - zůstatek zákazníka <br>Kredit - nedokončená práce - fakturováno na účet    |
| Zaúčtovat odhadované výnosy             | Nelze použít                                   | Nelze použít                                                                                                    | Nevztahuje se                                                  | Debet - hodnota nákladů nedokončené práce <br>Kredit - náklady                                                                         | Debet - nedokončená práce - hodnota prodeje <br>Kredit - Hodnota prodeje časově rozložených výdajů |
| Eliminovat                         | Nelze použít                                   | Nelze použít                                                                                                    | Nevztahuje se                                                  | Kredit - hodnota nákladů nedokončené práce <br>Debet - náklady <br>Kredit - časově rozložené výnosy - hodnota prodeje <br>Debet - nedokončená práce - fakturováno na účet | Debet - nedokončená práce - fakturováno na účet <br>Kredit - nedokončená práce - hodnota prodeje     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfigurace nákladů projektu a pravidel profilů výnosů

Pravidla profilu nákladů a výnosů projektu určují profil nákladů a výnosů projektu, které je nutné použít při zpracování fakturovatelných transakcí projektu. Definujte pravidla přechodem na **Řízení projektů a účetnictví** \> **Nastavení** \> **Účtování** \> **Pravidla profilu nákladů a výnosů projektu**.

Pravidla mohou být definována smlouvou projektu, skupinou projektů nebo konkrétním projektem. Systém vždy nejprve vybere pravidlo nejvyšší podrobnosti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
