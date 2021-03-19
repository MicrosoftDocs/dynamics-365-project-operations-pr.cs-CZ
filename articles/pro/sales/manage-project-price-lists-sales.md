---
title: Správa ceníků projektů v nabídkách projektů – omezené
description: Toto téma poskytuje informace o práci s projektovými ceníky v nabídkách. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d48da44f382e329a978a8ceee59c354d009f2114
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273010"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a>Správa ceníků projektů v nabídkách projektů – omezené

_**Platí pro:** Omezené nasazení – od obchodu po pro forma fakturaci_

Projektové nabídky projektu jsou navrženy tak, aby podporovaly prodejní ceníky s více daty účinnosti. S Dynamics 365 Project Operations je přidána nová přidružená entita s názvem **Ceníky projektu**. Tato entita má vztah 1:N k projektové nabídce.

Projektové ceníky se používají k oceňování časových a výdajových transakcí na projektu. Pokud má nabídka jeden nebo více projektových ceníků, používají se tyto ceníky ke stanovení odhadů času a výdajů a skutečných hodnot u projektů, které jsou přidruženy k nabídce prostřednictvím řádku nabídky.

Pokud v projektové nabídce nejsou žádné projektové ceníky, zobrazí se varovná zpráva. Zpráva uvádí, že kvůli neexistenci projektových ceníků nebudou vaše odhadované a skutečné práce a výdaje na projekt oceněny. Místo toho budou mít prodejní hodnoty nulovou (0) cenu.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Přidružení nebo zrušení přidružení projektového ceníku v projektové nabídce

Chcete-li vytvořit nebo vybrat konkrétní ceník pro odhad projektové práce a výdajů, proveďte následující kroky.

1. V nabídce vyberte kartu **Cena projektu** a v podřízené mřížce vyberte příkaz **+ Přidat nový projektový ceník**.
2. Na stránce Vytvořit vyberte ceník. Rozevírací seznam zobrazuje všechny ceníky, které mají kontext nastaven na **Prodej** a jejich měna odpovídá měně v nabídce.
4. Zadejte popis přidružení projektového ceníku a vyberte příkaz **Uložit a zavřít**.

Vytvoří se přidružení projektového ceníku.

Tento proces můžete opakovat, pokud potřebujete k projektové nabídce přidružit více než jeden projektový ceník. Více projektových ceníků vytvářejte, pouze pokud máte na každém z přidružených projektových ceníků různá data účinnosti.

> [!NOTE]
> Project Operations nepodporuje překrývající se datumy účinnosti u projektových ceníků. Pokud existuje více projektových ceníků pro transakci s daným datem, cena této transakce bude implicitně nastavena na nulu (0).
Chcete-li odebrat přidružení projektového ceníku, vyberte projektový ceník a poté vyberte příkaz **Odstranit projektový ceník nabídky**. Ceník je odebrán z projektových ceníků nabídky, ale samotný ceník není odstraněn. Odstraní se pouze přidružení k nabídce.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Nastavení výchozích projektových ceníků v nabídce

Projektové ceníky lze nastavit jako výchozí pro projektovou nabídku. Toto nastavení zajišťuje, aby všechny nabídky ve vaší organizaci vždy začínaly standardním ceníkem pro toto cenové období.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Nastavení výchozích organizačních hodnot pro projektové ceníky

1. Přejděte do nabídky **Nastavení** > **Všeobecné** > **Parametry**.
2. Na stránce seznamu **Aktivní parametry** vyhledejte záznam a poklepáním jej otevřete. 
3. Na stránce **Parametry** vyberte kartu **Ceník**. Zobrazí se seznam výchozích ceníků. Toto je seznam standardních nákladových a prodejních ceníků. Budete-li zde mít přidružený prodejní ceník pro každou měnu, ve které prodáváte, zajistí si tak, aby tento prodejní ceník byl výchozí u jakékoli nabídky, kterou vytvoříte pro zákazníky obchodující v této měně.

### <a name="set-up-customer-specific-project-price-lists"></a>Nastavení projektových ceníků pro konkrétního zákazníka

Projektové ceníky pro konkrétního zákazníka lze také nastavit po vyjednání hlavní cenové dohody se zákazníky.

Chcete-li nastavit projektový ceník pro konkrétního zákazníka, proveďte následující kroky.

1. V oblasti **Prodej** vyberte položku **Zákazníci**.
2. V seznamu aktivních účtů vyberte a otevřete záznam zákazníka, pro kterého máte speciální ceník.
3. Na kartě **Projektové ceníky** můžete vytvořit nové přidružení ceníku, abyste měli projektový ceník pro tohoto konkrétního zákazníka.

## <a name="create-custom-pricing-on-a-project-quote"></a>Vytvoření vlastních cen v projektové nabídce

Až budete mít nastaveny výchozí projektové ceníky pro organizaci a konkrétní zákazníky, budou vaše projektové nabídky automaticky vytvářeny s přidruženými projektovými ceníky. V určitých případech však možná budete muset vytvořit vlastní cenu pro určitou projektovou nabídku. 

1. V **Projektové nabídce** na kartě **Projektový ceník** si ověřte v podřízené mřížce, že není vybrán žádný konkrétní záznam ceníku.
2. Vyberte položku **Vytvořit vlastní ceny**. Tímto způsobem vytvoříte kopie všech standardních ceníků aktuálně přidružených k nabídce a přidružíte tyto kopie k nabídce. Stávající přidružení ke standardním ceníkům budou odstraněna. Prodejce pak může v těchto kopiích začít provádět úpravy cen. Tyto změněné ceny se budou vztahovat pouze na tuto projektovou nabídku.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]