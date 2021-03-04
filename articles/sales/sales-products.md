---
title: Produkty
description: Toto téma poskytuje informace o katalogu produktů, který můžete použít k poskytování informací zákazníkům o produktech a cenách, které nabízí vaše organizace.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 30633a7445baaf99af5be5c88e35b24824022b93
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121255"
---
# <a name="products"></a>Produkty

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Produkty jsou páteří vašeho podnikání. Katalog produktů v Dynamics 365 Sales Professional je sada produktů a informací o jejich cenách. Usnadněte svým prodejcům zvýšit prodeje pomocí rychlého vytvoření katalogu produktů.

## <a name="add-a-product"></a>Přidání produktu

1.  Ujistěte se, že máte roli Manažer specialisty prodeje nebo roli Správce systému, abyste mohli přidávat produkty do Dynamics 365 Sales Professional.
2.  V mapě webu v části **Nastavení** vyberte **Produkty**.
3.  Vyberte **Přidat produkt** a vyplňte následující informace:

    -  **Jméno**
    -  **ID produktu**
    -  **Nadřazený**: Zvolte nadřazenou produktovou řadu pro produkt. Pokud vytváříte podřízený produkt v produktové řadě, je zde naplněn název nadřazené produktové řady. Toto nelze změnit po uložení záznamu.
    -  **Platnost od**/**Platnost do**: Definujte dobu trvání, po kterou je balíček produktů platný, volbou data **Platné od** a **Platnost do**.
    -  **Skupina jednotek**: Vyberte skupinu jednotek. Skupina jednotek je kolekce různých jednotek, ve kterých se produkt prodává, a definuje, jak jsou jednotlivé položky seskupeny do větších množství. Pokud například přidáváte jako produkt semena, můžete mít vytvořenou skupinu jednotek s názvem „Semena“ a definovat její primární jednotku jako „sáček“.
    -  **Výchozí jednotka**: Vyberte nejčastější jednotku, ve které se produkt prodává. Jednotky jsou množství nebo míry, ve kterých své produkty prodáváte. Pokud například přidáváte jako produkt semena, můžete je prodávat v sáčcích, krabičkách nebo paletách. Každá z těchto možností se stane jednotku produktu. Semena se nejčastěji prodávají v baleních, proto zvolte jako jednotku tuto možnost.
    -  **Výchozí ceník**: Pokud se jedná o nový produkt, je toto pole určeno jen pro čtení. Před výběrem výchozího ceníku je třeba zadat hodnoty do všech povinných polí a poté záznam uložit. Ačkoli výchozí ceník není požadován, po uložení záznamu produktu je vhodné nastavit výchozí ceník pro jednotlivé produkty. V případě, že záznam zákazníka neobsahuje žádný ceník, aplikace Prodej bude moci použít výchozí Ceník pro generování nabídek, objednávek a faktur.
    -  **Podporovaná desetinná místa**: Musíte zadat celé číslo mezi 0 a 5. Pokud produkt nelze rozdělit na zlomkové množství, zadejte hodnotu 0. Pokud k tomuto produktu není přidružen ceník, přesnost pole **Množství** v záznamu produktu na nabídce, objednávce nebo faktuře se ověří vůči hodnotě v tomto poli.
    -  **Předmět**: Tento produkt můžete přidružit k předmětu. Pomocí předmětů můžete produkty zařazovat do kategorií a filtrovat sestavy.

4.  Zvolte **Uložit**.
5.  Na kartě **Další podrobnosti** v sekci **Položky ceníku** vyberte možnost **Další příkazy** a poté zvolte **Přidat novou položku ceníku**.
7.  Na kartě **Další podrobnosti** v sekci **Vztah produktu** vyberte ikonu **Další příkazy** a poté zvolte **Přidat nový produktový vztah.**
8.  Ve formuláři **Nový produktový vztah** vložte následující údaje a na panelu příkazů vyberte položku **Uložit a zavřít**:

    -   **Související produkt**: Vyberte produkt, který chcete přidat jako související produkt do stávajícího záznamu produktu, na němž právě pracujete.
    -   **Typ prodejního vztahu**: Vyberte, zda chcete přidat produkt jako následný prodej, prodej souvisejících produktů, příslušenství nebo jako náhradní produkt.
    -   **Směr**: Vyberte, zda bude vztah mezi produkty jednosměrný nebo obousměrný. Pokud vyberete jednosměrný, produkt vybraný v části **Související produkt** se zobrazí jako doporučení pro existující produkt, ale nikoli naopak.

9.  Ve formuláři Produkt vyberte **Uložit**.

## <a name="import-products"></a>Import produktů

Pomocí importu šablon můžete přenést hromadná data produktu do Dynamics 365 Sales.

## <a name="revise-a-product"></a>Oprava produktu

Udržujte skladové zásoby produktů aktualizované pomocí rychlé kontroly vlastností produktů podle potřeby a publikování informací, aby vaši prodejci viděli nejnovější změny v zásobách.

1.  Zkontrolujte, jestli máte některou z následujících rolí zabezpečení nebo ekvivalentní oprávnění: Správce systému, Úpravce systému, Obchodní manažer, Obchodní náměstek, Marketingový náměstek nebo Výkonný/obchodní ředitel
2.  V mapě webu vyberte **Produkty**.
3.  Otevřete aktivní produkt, který chcete změnit, a na panelu příkazů zvolte **Revidovat**.
4.  V dialogovém okně **Potvrdit revizi** vyberte **Potvrdit**. To změní stav produktu na **Revidováno**.
5.  Po provedení změn na panelu příkazů vyberte možnost **Publikovat**.

    > [!TIP]
    > Chcete-li změny vrátit a pokračovat s poslední aktivní verzí produktu, vyberte možnost **Vrátit**. To změní stav produktu zpět na **Aktivní**.

## <a name="clone-a-product"></a>Klonování produktu 

Při vytváření nového produktu můžete ušetřit čas pomocí klonování existujícího produktu. Tím dojde k vytvoření kopie původního záznamu se všemi podrobnostmi kromě názvu a ID.

1.  Zkontrolujte, jestli máte některou z následujících rolí zabezpečení nebo ekvivalentní oprávnění: Správce systému, Úpravce systému, Obchodní manažer, Obchodní náměstek, Marketingový náměstek nebo Výkonný/obchodní ředitel
2.  V mapě webu vyberte **Produkty**.
3.  Vyberte záznam produktu, který chcete klonovat, a na panelu příkazů klikněte na položku **Klonovat**. Zobrazí se dialogové okno s potvrzením
4.  Vyberte **Potvrdit**.

Otevře se záznam nového produktu se stejnými údaji, jako měl záznam původního produktu, s výjimkou názvu a ID.

## <a name="retire-a-product"></a>Vyřazení produktu 

Pokud vaše organizace již nebude produkt prodávat, vyřaďte jej, aby produkt již nebyl obchodním zástupcům k dispozici.

1.  Zkontrolujte, jestli máte roli zabezpečení Správce systému nebo Manažera Sales Professional nebo ekvivalentní oprávnění.
2.  V mapě webu vyberte **Produkty**.
3.  Otevřete aktivní produkt, který chcete vyřadit, a na panelu příkazů zvolte **Vyřadit**.
4.  V dialogovém okně **Potvrdit vyřazení** vyberte **Potvrdit**.


## <a name="delete-a-product"></a>Odstranit produkt

Prodej produktu zastavíte tím, že jej odstraníte.

> [!IMPORTANT]
> Odstraněný záznam nelze obnovit.

1.  Zkontrolujte, jestli máte roli zabezpečení Správce systému nebo Manažera Sales Professional nebo ekvivalentní oprávnění.
2.  V mapě webu vyberte **Produkty**.
3.  Vyberte záznam produktu, který chcete odstranit, a na panelu příkazů klikněte na položku **Odstranit**.
4.  V dialogovém okně **Potvrzení odstranění** vyberte tlačítko **Pokračovat**.
 
 ## <a name="quantity-factors-for-products"></a>Množstevní faktory pro výrobky

Faktory množství podporují prodeje produktů založených na předplatném. U produktů založených na předplatném je množství v nabídce nebo na řádku projektové smlouvy vyjádřeno jako počet uživatelských měsíců.

Cena předplaceného softwaru je v katalogu obvykle uložena jako cena za uživatele za měsíc. Místo toho však můžete použít jiné popisy času. Během prodejního procesu je cena na řádku nabídky obvykle cena za uživatele za měsíc, která byla sjednána prodejním agentem IT a po uplatnění slevy. Každá dohoda má různý počet uživatelů a různý počet měsíců předplatného. Množství, které se používá k výpočtu částky řádku nabídky, je součin počtu uživatelů a počtu měsíců předplatného.

Množstevní faktory závisí na atributech produktu. Při konfiguraci určitých vlastností produktu můžete označit podmnožinu těchto vlastností nebo všechny vlastnosti jako množstevní faktory.

Systém ověřuje, zda jsou jako množstevní faktory označeny pouze numerické vlastnosti nebo vlastnosti produktu, které mají číselný datový typ. Pokud je produkt, pro nějž jsou nakonfigurovány množstevní faktory, přidán k řádku nabídky, pole **Množství** na řádku nabídky se stane polem jen pro čtení. Po zadání hodnot vlastností produktu, které jsou množstevními faktory, se vypočítá množství řádku nabídky.

Například pokud existují následující vlastnosti: 

- **Počet uživatelů**: počet uživatelů 
- **Poč. měsíců**: počet měsíců předplatného
- **Jednotka SKU produktu** 

Vlastnosti **Počet uživatelů** a **Počet měsíců** lze pomocí úpravy vlastností řádku produktu označit jako množstevní faktory. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]