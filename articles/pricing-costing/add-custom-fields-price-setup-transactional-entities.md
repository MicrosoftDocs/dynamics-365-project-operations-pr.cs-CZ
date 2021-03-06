---
title: Přidání požadovaných vlastních polí do nastavení ceny a transakčních entit
description: Toto téma poskytuje informace o tom, jak přidat požadované odkazy na vlastní pole do entit a do formulářů a zobrazení.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: a27bfe881fdb6431941fa860d279e3e7b526f623
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898298"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Přidání požadovaných vlastních polí do nastavení ceny a transakčních entit

_**Platí pro:** Project Operations scénáře založené na zdrojích / položkách, které nejsou na skladě, omezené nasazení - dohoda o pro forma fakturaci_

Toto téma předpokládá, že jste dokončili postupy v tématu [Vytvoření vlastních polí a entit k použití jako cenových dimenzí](create-custom-fields-entities-pricing-dimensions.md). Pokud jste tyto postupy nedokončili, vraťte se zpět, dokončete je a vraťte se k tomuto tématu. 

Postupy v tomto tématu vám ukážou, jak přidat požadované odkazy na vlastní pole do entit a do prvků uživatelského rozhraní (UI), jako jsou formuláře a zobrazení.

## <a name="add-custom-pricing-dimension-fields"></a>Přidání polí vlastních cenových dimenzí 
Po vytvoření vlastních polí a entit je dalším krokem pomocí vytvoření referenčních polí informovat nastavení ceny a transakční entity o všech vlastních entitách nebo sadách možností. V závislosti na tom, zda váš seznam cenových dimenzí zahrnuje dimenze sady možností nebo dimenze entit nebo obojí, proveďte pouze příslušné kroky v **Vlastní cenové dimenze založené na sadě možností** nebo **Vlastní cenové dimenze založené na entitě** nebo obojí.

### <a name="option-set-based-custom-pricing-dimensions"></a>Vlastní cenové dimenze založené na sadě možností
Pokud je vlastní cenová dimenze založena na sadě možností, přidejte ji jako pole do klíčových entit. V následujícím postupu jsou jako cenové dimenze založené na sadě možností použity **Místo výkonu práce zdroje** a **Pracovní doba zdroje**. Tyto je třeba nejprve přidat jako pole do cenových entit **Cena role** a **Přirážka ceny**.

1. V Project Operations zvolte **Nastavení** > **Řešení** a dvakrát klikněte na **\<your organization name> cenové dimenze**. 
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Entity > Cena role**.
3. Rozbalte entitu **Cena role** a vyberte **Pole**.
4. Zvolte **Nové** vytvořte nové pole nazvané **Místo výkonu práce zdroje** a jako typ pole vyberte **Sada možností**. 
5. Vyberte **Použít existující sadu možností**, vyberte sadu možností **Místo výkonu práce zdroje** a poté zvolte **Uložit**.
6. Opakováním kroků 1–5 přidejte toto pole do entity **Přirážka ceny role**. 
7. Opakujte kroky 1–5 pro sadu možností **Pracovní doba zdroje**.

> [!IMPORTANT]
> Přidáte-li pole do více než jedné entity, použijte stejný název pole ve všech entitách. 

Ve fázích prodeje a odhadu projektu se k odhadu hodnoty Nabídky/Projektu používají odhady pracovního úsilí, které je nutné k dokončení práce **Místní** a **U zákazníka**, v **Běžné pracovní době** a **Přesčasové pracovní době**. Pole **Místo výkonu práce zdroje** a **Pracovní doba zdroje** budou přidány do entit odhadu **Podrobnosti řádku nabídky**, **Podrobnosti řádku smlouvy**, **Člen projektového týmu** a **Řádek odhadu**.

1. V Project Operations zvolte **Nastavení** > **Řešení** a pak dvakrát klikněte na **\<your organization name> cenové dimenze**. 
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Entity > Podrobnosti řádku nabídky**.
3. Rozbalte entitu **Podrobnosti řádku nabídky** a vyberte **Pole**.
4. Zvolte **Nové** vytvořte nové pole nazvané **Místo výkonu práce zdroje** a vyberte typ pole **Sada možností**. 
5. Vyberte **Použít existující sadu možností** a **Místo výkonu práce zdroje** a poté zvolte **Uložit**.
6. Opakováním kroků 1–5 přidejte toto pole do entit **Podrobnosti řádku projektové smlouvy**, **Člen projektového týmu** a **Řádek odhadu**.
7. Opakujte kroky 1–6 pro sadu možností **Pracovní doba zdroje**. 

Pro dodání a fakturaci musí být dokončená práce přesně oceněna, aby bylo možné ve Skutečnostech projektu vybrat, zda byla provedena **Místně** nebo **U zákazníka**, a zda byla dokončena v **Běžné pracovní době** nebo **Přesčasové pracovní době**. Pole **Místo výkonu práce zdroje** a **Pracovní doba zdroje** by měla být přidána do entit **Časový záznam**, **Skutečnost**, **Podrobnosti řádku faktury** a **Řádek deníku**.

1. Zvolte **Nastavení** > **Řešení** a pak dvakrát klikněte na **\<your organization name> cenové dimenze**.
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Entity > Časový záznam**.
3. Rozbalte entitu **Podrobnosti řádku nabídky** a poté vyberte **Pole**.
4. Zvolte **Nové** vytvořte nové pole nazvané **Místo výkonu práce zdroje** a jako typ pole vyberte **Sada možností**. 
5. Vyberte **Použít existující sadu možností**, vyberte sadu možností **Místo výkonu práce zdroje** a poté zvolte **Uložit**.
6. Opakováním kroků 1–5 přidejte toto pole k entitám **Skutečnost**, **Podrobnosti řádku faktury** a **Řádek deníku**.
7. Opakujte kroky 1–6 pro sadu možností **Pracovní doba zdroje**. 

Tím dokončíte změny schématu vyžadované pro vlastní dimenze založené na sadě možností.

## <a name="entity-based-custom-pricing-dimensions"></a>Vlastní cenové dimenze založené na entitě

Pokud je vlastní cenová dimenze entitou, přidáte mezi entitu dimenze a klíčové entity vztahy 1:N. Při použití výše uvedeného příkladu Standardní funkce lze očekávat, že každému zaměstnanci bude přiřazena standardní funkce. V důsledku toho budete potřebovat vztah 1:N ze Standardní funkce do Rezervovatelného zdroje nebo vztah N:1, pokud byl vytvořen z Rezervovatelného zdroje do Standardní funkce.

1. V Project Operations zvolte **Nastavení** > **Řešení** a pak dvakrát klikněte na **\<your organization name> cenové dimenze**. 
2. V Průzkumníku řešení vyberte v levém navigačním podokně **Entity > Standardní funkce**.
3. Rozbalte entitu **Standardní funkce** a vyberte **Vztahy 1:N**.
4. Zvolte **Nový** vytvoříte nový vztah 1:N nazvaný **Standardní funkce do Rezervovatelného zdroje**. Zadejte požadované informace a zvolte **Uložit**.

Standardní funkci bude také nutné přidat k cenovým entitám **Cena role** a **Přirážka ceny role**. Toto se také provede pomocí vztahů 1:N mezi entitami **Standardní funkce** a **Cena role** a entitami **Standardní funkce** a **Přirážka ceny role**.

1. V Průzkumníku řešení vyberte v levém navigačním podokně **Entity > Standardní funkce**.
2. Rozbalte entitu **Standardní funkce** a vyberte **Vztahy 1:N**.
3. Zvolte **Nový** vytvoříte nový vztah 1:N nazvaný **Standardní funkce do Ceny role**. Zadejte požadované informace a zvolte **Uložit**.
4. Opakováním kroků 1–4 vytvořte vztahy 1:N mezi entitami **Standardní funkce** a **Přirážka ceny role**.

Ve fázích prodeje a odhadu projektu jsou pro ocenění Nabídky/Projektu vyžadovány odhady pracovního úsilí pro každou standardní funkci. To znamená, že jsou nutné vztahy 1:N ze Standardní funkce ke každé z těchto entit odhadu: 

- **Podrobnosti řádku nabídky**
- **Podrobnosti řádku projektové smlouvy**
- **Člen projektového týmu**
- **Řádek odhadu**

5. Opakujte kroky 1–5 pro vytvoření vztahů 1:N ze **Standardní funkce** do **Podrobnosti řádku nabídky**, **Podrobnosti řádku projektové smlouvy**, **Člen projektového týmu** a **Řádek odhadu**.

  Ve fázích Dodání a Fakturace musí být práce dokončená každou Standardní funkcí přesně oceněna ve Skutečnostech projektu. To znamená, že zde musí být vztahy 1:N ze **Standardní funkce** do **Časový záznam**, **Skutečnost**, **Podrobnosti řádku faktury** a **Entity řádku deníku**.

6. Opakováním kroků 1–6 vytvořte vztahy 1:N ze **Standardní funkce** do **Časový záznam**, **Skutečnost**, **Podrobnosti řádku faktury** a **Entity řádku deníku**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Nastavení výchozí hodnoty Dimenze pomocí funkcí mapování platformy
V případě Časového záznamu by bylo užitečné mít systémovou výchozí hodnotou standardní funkci u Časového záznamu z Rezervovatelného zdroje, který časový záznam zaznamenává. Chcete-li přidat mapování polí u vztahu 1:N z **Rezervovatelný zdroj** do **Časový záznam**, použijte následující postup.

1. V Průzkumníku řešení vyberte v levém navigačním podokně **Entity > Standardní funkce**.
2. Rozbalte entitu **Standardní funkce** a vyberte **Vztahy 1:N**.
3. Dvakrát klikněte na **Rezervovatelný zdroj do Časového záznamu**. Na stránce **Vztah** zvolte **Použít mapování polí**. 
4. Zvolením **Nové** vytvoříte nové mapování pole mezi polem **Standardní funkce** u entity **Rezervovatelný prostředek** do odkazovaného pole **Standardní funkce** u entity **Časový záznam**. 

Tím dokončíte změny schématu vyžadované pro vlastní dimenze založené na entitě.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Přidání vlastních polí do formulářů, zobrazení a obchodních pravidel

Po provedení všech požadovaných změn schématu je dalším krokem zobrazení polí v uživatelském rozhraní přidáním polí do formulářů a zobrazení.

1. Otevřete formulář nebo zobrazení. V pravém navigačním podokně vyberte pole a přetáhněte ho na plátno formuláře. 
2. Pokud upravujete zobrazení, použijte pravé navigační podokno, zvolte **Přidat pole** a v dialogovém okně **Výpis polí** vyberte pole, která potřebujete, a zvolte **OK**.

Následující tabulka obsahuje úplný seznam připravených formulářů a zobrazení, uvedených podle entity, kterou bude nutné pomocí těchto nových polí aktualizovat. Pokud vaše vlastní nastavení těchto entit obsahují další zobrazení nebo formuláře, přidejte do nich tato nová pole také.

| Entity        | Formuláře, které potřebují nové pole   |Zobrazení, která potřebují nové pole      |
| ------------------------------|---------------------------------|----------------------------------|
|  Cena role|• Informace |• Aktivní ceny kategorií zdrojů<br> • Přidružené zobrazení cen kategorií zdrojů|
|  Přirážka ceny role|• Informace|• Aktivní přirážky ceny role<br>• Přidružené zobrazení přirážek ceny role|
|  Podrobnosti řádku nabídky|• Informace o projektu<br>• Vytvořit projekt|• Aktivní podrobnosti řádků nabídek<br>• Sloučené podrobnosti řádků objednávek<br>• Přidružené zobrazení podrobností řádků nabídek|
|  Podrobnosti řádku projektové smlouvy|• Informace o projektu<br>• Vytvořit projekt|• Sloučené podrobnosti řádků smluv<br>• Aktivní podrobnosti řádků smluv<br>• Přidružené zobrazení podrobností řádků smluv|
|  Člen projektového týmu|• Informace<br>• Nový formulář|• Aktivní členové projektových týmů<br>• Členové projektových týmů<br>• Přidružené zobrazení členů projektových týmů|
|  Časový záznam|• Informace<br>• Vytvořit časový záznam|• Moje časové záznamy podle data<br>• Moje časové záznamy za tento týden<br>• Časové záznamy ke schválení|
|  Řádek deníku|• Informace<br>• Vytvořit|• Aktivní řádky deníků<br>• Přidružené zobrazení řádků deníků|
|  Podrobnosti řádku faktury|• Informace<br>• Vytvořit|• Aktivní podrobnosti řádků faktur<br>• Účtovatelné fakturační transakce<br>• Neplacené fakturační transakce<br>• Přidružené zobrazení podrobností řádků faktur<br>• Neúčtovatelné fakturační transakce|
|  Skutečnost|• Informace<br>• Aktivní skutečnosti|• Přidružené zobrazení skutečností|

V závislosti na tom, co jste definovali, může být také nutné přidat vlastní pole do obchodních pravidel. Jeden z těchto připravených příkladů je pro obchodní pravidlo **Upravitelnost časového záznamu na základě stavu**. Toto pravidlo definuje, která pole je třeba uzamknout, pokud je Časový záznam v neupravitelném stavu, jako je např. **Schválen**. Přidejte pole do tohoto obchodního pravidla tak, aby byla tato pole uzamčena pro úpravy, pokud je Časový záznam v jiném stavu než **Koncept** nebo **Vrácen**.
