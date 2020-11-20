---
title: Ocenění projektů
description: Toto téma obsahuje informace o fungování ocenění v Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 88b791a1eb90d2aad67adba69169eab2c49c1318
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120760"
---
# <a name="project-pricing"></a>Ocenění projektů 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation rozšiřuje entitu Ceník v Dynamics 365 Sales. 

## <a name="key-entities"></a>Klíčové entity

Ceník obsahuje informace poskytované čtyřmi různými entitami:

- **Ceník** – tato entita uchovává informace o kontextu, měně, datu účinnosti a časové jednotce pro dobu ocenění. Kontext ukazuje, zda ceník vyjadřuje nákladové sazby nebo prodejní sazby. 
- **Měna** – tato entita uchovává měnu cen v ceníku. 
- **Datum** – tato entita se používá v případě, že se systém pokouší zadat výchozí cenu pro transakci. Ocenění PSA vybírá ceník, který má datum účinnosti, které zahrnuje datum transakce. Pokud ocenění PSA nalezne více než jeden ceník, který je platný pro datum transakce připojené k související nabídce, smlouvě nebo organizační jednotce, pak nebude použita žádná výchozí cena. 
- **Čas** – tato entita uchovává jednotku času, pro kterou jsou vyjádřeny ceny, například denní nebo hodinové sazby. 

Entita Ceník obsahuje tři související tabulky, ve kterých jsou uloženy ceny:

  - **Cena role** – v této tabulce jsou uloženy sazby pro kombinaci hodnot role a organizační jednotky a slouží k nastavení cen lidských zdrojů založených na rolích.
  - **Cena kategorie transakce** – tato tabulka uchovává ceny podle kategorie transakcí a používá se k nastavení cen kategorií výdajů.
  - **Položky ceníku** – tato tabulka uchovává ceny pro katalogové produkty.

> ![Konfigurace cen pomocí ceníku](media/basic-guide-12.png)
 
Ceník je karta se sazbami. Karta se sazbami je kombinací entity Ceník a souvisejících řádků v tabulkách Cena role, Cena kategorie transakce a Položky ceníku.

## <a name="resource-roles"></a>Role zdrojů

Termín *Role zdroje* odkazuje na sadu dovedností, kompetencí a certifikací, které musí osoba mít k provedení specifické sady úkolů na projektu.

Čas lidských zdrojů je obvykle uváděn na základě role, kterou zdroj plní v určitém projektu. PSA pro čas lidských zdrojů podporuje oceňování a fakturaci, které jsou založeny na roli zdroje. Čas lze ocenit v libovolné jednotce ve skupině jednotek **Čas**.

Skupina jednotek **Čas** se vytvoří při instalaci PSA. Obsahuje výchozí jednotku **Hodina**. Atributy skupiny jednotek **Čas** nebo jednotky **Hodina** nelze odstranit, přejmenovat ani upravit. Do skupiny jednotek **Čas** však můžete přidat další jednotky. Pokud se pokusíte odstranit skupinu jednotek **Čas** nebo jednotku **Hodina**, můžete způsobit selhání v obchodní logice PSA.

> ![Konfigurace cen podle role](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Kategorie transakcí a kategorie výdajů

Cestovné a další výdaje, které vzniknou projektovým konzultantům, jsou obvykle fakturovány zákazníkovi. PSA podporuje oceňování kategorií výdajů pomocí ceníků. Příklady kategorií výdajů jsou letenky, hotel a pronájem aut. Každý řádek ceníku pro výdaje určuje ceny pro specifickou kategorii výdajů. PSA podporuje pro ocenění kategorií výdajů následující tři způsoby ocenění:

- **Podle nákladů** – výdajové náklady jsou fakturovány zákazníkovi a není použita žádná přirážka.
- **Procento přirážky** – procentní podíl nad skutečné náklady je fakturován zákazníkovi. 
- **Cena za jednotku** – fakturační cena je nastavena pro každou jednotku kategorie výdajů. Částka, která je fakturována zákazníkovi, je vypočtena na základě počtu výdajových jednotek, které konzultant hlásí. Mílovné používá metodu ocenění cena za jednotku. Kategorie výdajů na mílovné může být nakonfigurována pro 30 amerických dolarů (USD) za den nebo 2 USD na míli. Když konzultant ohlásí mílovné na projekt, fakturovaná částka se vypočte na základě počtu mil, které konzultant ohlásil.

> ![Konfigurace oceňování kategorií výdajů](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Oceňování a přepisy projektových prodejů

U projektových nabídek a smluv má projektový ceník odlišný způsob přepsání ceny než produktový ceník. Na řádku nabídky založeném na katalogu produktů můžete přepsat cenu rolí a kategorií přímo na řádku nabídky, protože každý řádek nabídky odkazuje přesně na jednu položku katalogu. Na řádku nabídky založeném na projektu však nemůžete přepsat cenu rolí a kategorií přímo na řádku nabídky. Za účelem podpory dvou odlišných způsobů přepsání zavedl PSA nové přidružení ceníku, což je projektový ceník.

> [!NOTE]
> Doporučujeme, abyste pro zdroje projektu a položky katalogu měli samostatný ceník, a to z důvodu rozdílů v chování mezi těmito dvěma položkami při přepsání ceny.

Každá z následujících entit může obsahovat jeden nebo více přidružených ceníků pro ocenění projektu:

- Zákazník (účet) 
- Příležitost 
- Nabídka 
- Projektová smlouva

Přidružení těchto entit k ceníku je označeno pomocí projektových ceníků. K entitám Zákazník, Příležitost, Nabídka a Projektová smlouva můžete přidružit jeden nebo více ceníků.

Výchozí projektový ceník není automaticky zadán do záznamu zákazníka. K záznamu zákazníka však můžete ručně připojit Ceník projektu. Přesto byste měli projektový ceník přiložit ručně pouze v případě, že máte se zákazníkem vlastní cenovou dohodu. 

Pokud je projektový ceník připojen k prodejní entitě, PSA ověřuje následující informace:

- Ceník jako kontext **Prodeje**. 
- Měna ceníku se musí shodovat s měnou zákazníka. 

PSA používá u projektové smlouvy následující pořadí priorit pro automatické nastavení souvisejících projektových ceníků:

1. Nabídka
2. Příležitost
3. Zákazník 
4. Globální nastavení pro PSA

Je-li ve výchozím nastavení zadán projektový ceník, PSA ověří, že měna odpovídá měně zákazníka, a že zadané výchozí ceníky obsahují kontext **Prodeje**.

K entitám Zákazník, Příležitost, Nabídka a Projektová smlouva můžete přidružit několik projektových ceníků. Tato funkce podporuje výchozí ceny specifické pro datum pro dlouhotrvající projektovou smlouvu, kde můžete vyžadovat více než jeden ceník na obchodní vztah pro aktualizace cen, ke kterým dochází z důvodu inflace. Pokud však ceníky, které přidružíte k entitě Zákazník, Příležitost, Nabídka nebo Projektová smlouva, mají překrývající se datum účinnosti, mohou být výchozí ceny nesprávné. Proto byste se měli ujistit, že projektové ceníky s překrývajícími se daty účinnosti nejsou přidruženy k těmto entitám.

### <a name="deal-specific-price-overrides"></a>Přepisy cen specifické pro obchod

V PSA můžete v projektových cenících vytvořit pro vybrané ceny přepisy specifické pro obchod, které jsou ve výchozím nastavení zadány v nabídce nebo projektové smlouvě.

Projektová smlouva dostane ve výchozím nastavení vždy kopii hlavního prodejního ceníku namísto přímého odkazu na něj. Toto chování pomáhá zaručit, že se cenové dohody, které jsou se zákazníkem učiněny pro popisy práce (SOW), při změně hlavního ceníku nezmění.

V nabídce je však možné použít hlavní ceník. Můžete také zkopírovat hlavní ceník a upravit jej za účelem vytvoření vlastního ceníku, který se vztahuje pouze k dané nabídce. Chcete-li vytvořit nový ceník, který je specifický pro určitou nabídku, vyberte na stránce **Nabídka** možnost **Vytvořit vlastní ceny**. K projektovému ceníku specifickému pro obchod můžete přistupovat pouze z nabídky. 

Při vytváření vlastního projektového ceníku se zkopírují pouze projektové komponenty ceníku. Jinými slovy, nový ceník vytvořený jako kopie existujícího projektového ceníku, který je připojen k nabídce, a tento nový ceník obsahuje pouze související ceny rolí a ceny kategorií transakcí.

> ![Zobrazení a konfigurace vlastních cen pro projektovou smlouvu](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Sledování nákladů

PSA sleduje u projektů náklady na použití času lidských zdrojů. Sleduje také náklady na další výdaje, které během projektu vzniknou, například cestovní výdaje.

Nákladové sazby pro lidské zdroje se stejně jako fakturační sazby také nastavují pomocí ceníků. Zde jsou hlavní rozdíly v chování nákladového ceníku a prodejního ceníku:

- Nákladovou sazbu zdroje nelze u specifického projektu, smlouvy nebo nabídky přepsat. Pokud však dojde k provedení změn, které jsou specifické pro podstatu obchodu, lze na základě jednotlivých obchodů přepsat fakturační sazby. 

- K vyřešení nákladového ceníku se používá následující pořadí:

    1. Nákladový ceník, který je připojen k organizační jednotce.
    2. Nákladový ceník, který je připojen k parametrům služby Project Service. Protože k parametrům služby Project service připojit nákladové ceníky v mnoha různých měnách, jsou měna smluvní organizační jednotky projektu, smlouvy nebo nabídky a měna nákladového ceníku stejné.
    3. U výdajů se metody ocenění podle nákladů a podle přirážky k nákladům na nákladové ceníky nepoužijí. I když se tyto metody ocenění používají v řádcích nákladových ceníků pro nastavení nákladů kategorie transakce, systém je ignoruje a nebude zadána výchozí nákladová cena.
