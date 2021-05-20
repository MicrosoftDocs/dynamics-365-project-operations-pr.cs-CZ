---
title: Konfigurace mezipodnikové fakturace
description: Tento téma poskytuje informace a příklady o konfiguraci mezipodnikové fakturace pro projekty.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bb39e212d00f8874254d4255f310217cdf46eb5a
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949671"
---
# <a name="configure-intercompany-invoicing"></a>Konfigurace mezipodnikové fakturace

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Chcete-li v projektu nastavit mezipodnikovou fakturaci, proveďte následující kroky v Dynamics 365 Project Operations. Mezipodnikové transakce jsou časové a výdajové transakce ze smlouvy o projektu, které patří jedné společnosti nebo organizační jednotce, zatímco prostředky ve smlouvě o projektu jsou součástí jiné společnosti nebo organizační jednotky.

## <a name="example-configure-intercompany-invoicing"></a>Příklad: Konfigurace mezipodnikové fakturace

V následujícím příkladu Contoso Robotics USA (USPM) je půjčující si právnická osoba a Contoso Robotics UK (GBPM) je půjčující právnická osoba. 

1. **Nakonfigurujte mezipodnikové účetnictví mezi právnickými osobami**. Každá dvojice výpůjčujících a půjčujících právnických osob musí být nakonfigurována v hlavní knize na stránce [Mezipodnikové účetnictví](/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. v Dynamics 365 Finance přejděte na **Hlavní kniha** > **Nastavení účtování** > **Mezipodnikové účetnictví**. Vytvořte záznam obsahující následující údaje:

        - **Původní společnost** = **GBPM**
        - **Cílová společnost** = **USPM**

2. **Nakonfigurujte obchodní vztah mezi právnickými osobami**. Záznam o zákazníkovi představující vypůjčující právnickou osobu musí být vytvořen v půjčující právnické osobě. Záznam o dodavateli představující půjčující právnickou osobu musí být vytvořen ve vypůjčující právnické osobě.

     1. V části Finance vyberte právnickou osobu **GBPM**.
     2. Přejděte na **Pohledávky** > **Zákazníci** > **Všichni zákazníci**. Vytvořte nový záznam pro právnickou osobu **USPM**.
     3. Rozbalte **Název** filtrujte záznamy podle **Typu** a vyberte **Právnické osoby**. 
     4. Najděte a vyberte záznam zákazníka pro **Contoso Robotics USA (USPM)**.
     5. Vybrerte **Použít shodu**. 
     6. Vyberte skupinu zákazníků **50 - Mezipodnikoví zákazníci** a poté záznam uložte.
     7. Vyberte právnickou osobu **USPM**.
     8. Přejděte na **Závazky** > **Dodavatelé** > **Všichni dodavatelé**. Vytvořte nový záznam pro právnickou osobu **GBPM**.
     9. Rozbalte **Název** filtrujte záznamy podle **Typu** a vyberte **Právnické osoby**. 
     10. Najděte a vyberte záznam zákazníka pro **Contoso Robotics UK (GBPM)**.
     11. Vyberte **Použijte shodu**, vyberte skupinu dodavatelů a poté záznam uložte.
     12. V záznamu dodavatele vyberte **Všeobecné** > **Založit** > **Mezipodniková**.
     13. Na kartě **Obchodní vztah** nastavte **Aktivní** na **Ano**.
     14. Nastavte pole **Společnost zákazníka** na **GBPM** a v **Záznam mého účtu** vyberte záznam zákazníka, který jste vytvořili dříve v postupu.

3. **Nakonfigurujte nastavení mezi společnostmi v Správa projektů a parametry účetnictví**. 

    1. Vyberte právnickou osobu **USPM** a přejděte do **Řízení projektů a účetnictví** > **Založit** > **Správa projektů a parametry účetnictví**.
    2. Na kartě **Mezipodniková** vyberte kategorii nákupu, aby odpovídala automaticky generovaným fakturám dodavatele.
    3. Ve **Výchozí kategorie** vyberte **Mezipodnikové zdroje**.
    4. Vyberte právnickou osobu **GBPM** a přejděte do **Řízení projektů a účetnictví** > **Založit** > **Správa projektů a parametry účetnictví**.
    5. Na kartě **Mezipodniková** vyberte pro každý typ transakce výchozí kategorii projektu. Kategorie projektu se používají pro konfiguraci daně, když fakturovaná kategorie v mezipodnikových transakcích existuje pouze v právnické osobě přijímající půjčku. Můžete si vybrat, zda časově rozložit výnosy z mezipodnikových transakcí. Časové rozlišení nastane, když jsou transakce zaúčtovány prostřednictvím deníku Project Operations Integration v půjčující právnické osobě. Deník je stornován, když je zaúčtována mezipodniková faktura.
    6. Ve skupině **Při půjčování zdrojů** vyberte **...** > **Nový**. 
    7. V mřížce vyberte následující informace:

          - **Výpůjčující právnická osoba** = **USPM**
          - **Časově rorozlišení příjmů** = **Ano**
          - **Výchozí kategorie časového rozvrhu** = **Výchozí - hodina**
          - **Výchozí kategorie výdajů** = **Výchozí - výdaj**

4. **Nastavte mezipodnikové účty nákladů a výnosů v nastavení účtování v účetní knize**. Účet mezipodnikových výnosů je kreditován při zaúčtování faktury mezipodnikového zákazníka u půjčující právnické osoby. Účet mezipodnikových nákladů je zatížen při párování nezaúčtované faktury dodavatele ve vypůjčující právnické osobě. Tyto účty jsou zřízeny v příslušných právnických osobách. 
      
     1. V části Finance vyberte vypůjčující právnickou osobu **USPM**. 
     2. Přejděte na **Řízení projektů a účetnictví** > **Nastavit** > **Účtování** > **Nastavení účtování hlavní knihy**. 
     3. Na kartě **Nákladové účty** v **Typu účtu hlavní knihy** vyberte **Mezipodnikové náklady**. Vytvořte nový záznam obsahující následující údaje:
      
        - **Půjčující právnická osoba** = **GBPM**
        - **Hlavní účet** = Vyberte hlavní účet pro mezipodnikové náklady. Toto nastavení je povinné. Nastavení se používá pro mezipodnikové toky ve Finance, ale ne v mezipodnikových tocích souvisejících s projektem. Tento výběr nemá žádný následný dopad. 
        
     4. Vyberte půjčující právnickou osobu **GBPM**. 
     5. Přejděte na **Řízení projektů a účetnictví** > **Nastavit** > **Účtování** > **Nastavení účtování hlavní knihy**. 
     6. Na kartě **Výnosové účty** v **Typu účtu hlavní knihy** vyberte **Mezipodnikové náklady**. Vytvořte nový záznam obsahující následující údaje:

        - **Výpůjčující právnická osoba** = **USPM**
        - **Hlavní účet** = Vyberte hlavní účet pro mezipodnikové výnosy. Toto nastavení je povinné. Nastavení se používá pro mezipodnikové toky ve Finance, ale ne v mezipodnikových tocích souvisejících s projektem. Tento výběr nemá žádný následný dopad. 

5. **Nastavte převodní ceny pro práci**. Mezipodnikové převodové ceny jsou konfigurovány v části Project Operations v Dataverse. Konfigurovat [nákladové sazby za práci](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) a [sazby účtů za práci](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) pro mezipodnikovou fakturaci. Transferové ceny nejsou podporovány u transakcí mezi společnostmi. Cena za prodej mezi jednotkami mezi organizacemi bude vždy nastavena na stejnou hodnotu jako cena nákladů na jednotku zajišťující zdroje.

      Cena prostředku vývojáře v Contoso Robotics UK je 88 GBP za hodinu. Contoso Robotics UK bude fakturovat společnosti Contoso Robotics USA 120 USD za každou hodinu, kdy tento zdroj pracoval na projektech v USA. Contoso Robotics USA bude fakturovat zákazníkovi Adventure Works 200 USD za práci prostředkem vývojáře Contoso Robotics UK.

      1. V Project Operations v Dataverse přejděte na **Prodej** > **Ceníky**. Vytvořte nový ceník nákladů s názvem **Sazby nákladů Contoso Robotics UK**. 
      2. V ceníku nákladů vytvořte záznam s následujícími informacemi:
         - **Role** = **Vývojář**
         - **Náklady** = **88 GBP**
      3. Přejděte do **Nastavení** > **Organizační jednotky** a připojte tento ceník nákladů k organizační jednotce **Contoso Robotics UK**.
      4. Přejděte na **Prodej** > **Ceníky**. Vytvořte ceník nákladů s názvem **Sazby nákladů Contoso Robotics USA**. 
      5. V ceníku nákladů vytvořte záznam s následujícími informacemi:
          - **Role** = **Vývojář**
          - **Zdrojová společnost** = **Contoso Robotics UK**
          - **Náklady** = **120 USD**
      6. Přejděte do **Nastavení** > **Organizační jednotky** a připojte ceník nákladů **Sazba nákladů Contoso Robotics USA** k organizační jednotce **Contoso Robotics USA**.
      7. Přejděte na **Prodej** > **Ceníky**. Vytvořte prodejní ceník s názvem **Fakturační sazby Adventure Works**. 
      8. V prodejním ceníku vytvořte záznam s následujícími informacemi:
          - **Role** = **Vývojář**
          - **Zdrojová společnost** = **Contoso Robotics UK**
          - **Fakturační sazba** = **200 USD**
      9. Přejděte na **Prodej** > **Projektové smlouvy** a připojte ceník **Fakturační sazby Adventure Works** do ceníku projektu Adventure Works projektové smlouvy.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
