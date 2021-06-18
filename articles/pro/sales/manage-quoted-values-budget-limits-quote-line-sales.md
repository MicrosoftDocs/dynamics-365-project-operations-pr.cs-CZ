---
title: Přehled řádků nabídky založené na projektu
description: Toto téma poskytuje informace o používání řádků nabídek založených na projektu pro práci na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994848"
---
# <a name="project-based-quote-lines-overview"></a>Přehled řádků nabídky založené na projektu 

_**Platí pro:** omezené nasazení – dohoda o pro forma fakturaci, Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Řádky nabídek založených na projektu jsou navrženy tak, aby pomohly odhadnout projektovou práci na zakázce. Struktura řádku nabídky založené na projektu se rozšiřuje u odhadů projektu o následující koncepty:

- Způsob fakturace
- Projekt a mapování úkolů
- Zahrnuté třídy transakcí
- Nepřekročitelný limit
- Nastavení účtovatelnosti
- Odhad pomocí podrobností řádku nabídky
- Zákazníci řádku nabídky

Následující tabulka poskytuje informace o polích na karrtě **Všeobecné** řádku nabídky založené na projektu. Tato pole pomáhají připravit základ pro podrobný počáteční odhad projektové práce.

| **Pole** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- |
| Jméno | Název řádku nabídky, který vám pomůže identifikovat diskrétní složku nabídky, která se odhaduje. | Zkopírováno do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Způsob fakturace | U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z příslušného pole na řádku příležitosti. Toto pole zahrnuje dva hlavní smluvní modely podporované Dynamics 365 Project Operations:</br>- Pevná cena</br>- Čas a materiál.| Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |
| Project | Pomocí tohoto volitelného pole můžete identifikovat projekt, který bude použit k provedení práce na této zakázce. Když je projekt mapován na řádek nabídky, pomáhá to při nastavení zpoplatněných úkolů a také při stanovení odhadu založeného na projektu do řádku nabídky jako podrobnosti řádku nabídky. Pokud projekt není mapován na řádek nabídky založené na projektu, odhad by měl být vytvořen ručně – vytvořením každé podrobnosti řádku nabídky. | Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána.|
| Zahrnuté úkoly | Udává, zda je tento řádek nabídky použit pro všechny nebo jen některé úkoly vybraného projektu. Toto pole může obsahovat následující hodnoty:</br>- Všechny projektové úkoly</br>- Pouze vybrané úkoly projektu</br>Prázdná hodnota v tomto poli odpovídá možnosti **Všechny úkoly projektu**. | Když je na stránce projektu vybráno **Pouze vybrané úkoly projektu**, karta **Nastavení fakturace úkolu** umožňuje vybrat konkrétní úkoly a přidružit je k tomuto řádku nabídky. Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |
| Zahrnout čas | Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty časové transakce nebo náklady práce na vybraném projektu. Hodnota **Ne** určuje, že časové transakce nebo náklady práce nebudou zahrnuty do odhadu na tomto řádku nabídky. Hodnota **Ano** určuje, že časové transakce nebo náklady práce budou zahrnuty do odhadu na tomto řádku nabídky. | Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |
| Zahrnout výdaj | Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty náklady výdajů na vybraném projektu. Hodnota **Ne** určuje, že výdajové náklady nebudou zahrnuty do odhadu na tomto řádku nabídky. Hodnota **Ano** určuje, že výdajové náklady budou zahrnuty do odhadu na tomto řádku nabídky. | Tato hodnota je překopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |
| Zahrnout materiál | Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty náklady na materiál na vybraném projektu. Hodnota **Ne** označuje, že nebudou do odhadu na tomto řádku nabídky zahrnuty náklady na materiál. Hodnota **Ano** označuje, že budou do odhadu na tomto řádku nabídky zahrnuty náklady na materiál. | Tato hodnota je překopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |
| Zahrnout poplatek | Hodnota **Ano**/**Ne** označuje, zda budou do odhadu na tomto řádku nabídky zahrnuty poplatky na vybraném projektu. Hodnota **Ne** určuje, že poplatky nebudou zahrnuty do odhadu na tomto řádku nabídky. Hodnota **Ano** určuje, že poplatky budou zahrnuty do odhadu na tomto řádku nabídky. | Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |
| Nabízená částka | Jedná se o částku, která bude zákazníkovi nabídnuta za veškerou práci předpovídanou v tomto řádku nabídky projektu. U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z pole **Rozpočet zákazníka** na řádku příležitosti. Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky na podrobnostech řádku nabídky. | Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |
| Odhad daně | Toto je upravitelné pole, kde může uživatel přidat odhadovanou částku daně do řádku nabídky. Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky daně na podrobnostech řádku nabídky. | Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |
| Nabízená částka včetně daně | Toto pole představuje částku nabídky po zdanění a je pouze ke čtení. Částka v tomto poli se počítá jako *Nabízená částka + daň*. | Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |
| Nepřekročitelný limit | Toto pole je upravitelné a je k dispozici pouze na řádcích nabídek založených na projektu, které mají nastaven způsob fakturace **Čas a materiál**. | Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |
| Rozpočet zákazníka | Toto pole je upravitelné a jeho hodnota se zkopíruje z příslušného pole na řádku příležitosti, když je nabídka vytvořena z příležitosti. | Tato hodnota je zkopírována do řádku smlouvy projektu, který je vytvořen z tohoto řádku nabídky, když je nabídka vyhrána. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Pravidla ověření pro pole na kartě Všeobecné řádků nabídek založených na projektu

**Pravidlo 1** : Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Všechny úkoly projektu**, je projekt zahrnut do řádku nabídky.

**Pravidlo 2** : Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Všechny úkoly projektu**, lze projekt a určitou třídu transakcí zahrnout pouze na jeden řádek nabídky založené na projektu.

**Pravidlo 3**: Pokud je pole **Zahrnuté úkoly** prázdné nebo je-li nastaveno na hodnotu **Pouze vybrané úkoly projektu**, lze projekt a určitou třídu transakcí zahrnout do více řádků nabídky založené na projektu.

**Pravidlo 4** : Pokud má příležitost více nabídek, mohou existovat řádky nabídky z různých nabídek, které všechny odkazují na stejný projekt a zahrnují stejnou třídu transakcí.

**Pravidlo 5** : Pokud nabídky nepatří ke stejné příležitosti, nemohou zahrnovat stejný projekt a třídu transakcí.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Příležitost</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Nabídka</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Řádek nabídky</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Zahrnuté úkoly</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Zahrnout čas</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Zahrnout výdaj</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Zahrnout materiál</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Zahrnout</strong>
                </p>
                <p>
                    <strong>Poplatek</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Platné / Neplatné</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Důvod</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Porušení pravidla č. 2. Čas, náklady a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 a ŘN2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Porušení pravidla č. 2. Čas, materiál a poplatky za projekt P1 jsou zahrnuty v řádcích nabídky ŘN1 a ŘN2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Platné </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Čas, materiál a poplatky za projekt P1 jsou zahrnuty na ŘN1 <br>
Výdaje na projekt P1 jsou zahrnuty do ŘN2 <br>
Žádné překrývání toho, co je zahrnuto na každém řádku nabídky, a proto je zadání platné.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Porušení pravidla č. 2 </p>
                <p>
S1 zahrnuje čas, materiál, výdaje a poplatky za podmnožinu úkolů v projektu P1 </p>
                <p>
ŘN2 zahrnuje čas, výdaje a poplatky za celý projekt P1, a proto se překrývá s tím, co je zahrnuto v S1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
prázdnou </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Platné </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Podle pravidla č. 3 </p>
                <p>
Č1 zahrnuje čas, materiál, výdaje a poplatky za podmnožinu úkolů v projektu P1.
                </p>
                <p>
ŘN2 zahrnuje čas, materiál, výdaje a poplatky za podmnožinu úkolů v projektu P1.
                </p>
                <p>
Jediná další validace je kolem podmnožiny úkolů na ŘN1, která se liší od podmnožiny úkolů na ŘN2, aby se zajistilo, že nedojde k překrývání. Toto provádí systém, když jsou přidruženy úkoly.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Pouze vybrané úkoly projektu </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Všechny úkoly projektu nebo prázdné </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Platné </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Podle pravidla č. 5 jsou Č1 a Č2 dvě nabídky u stejné příležitosti, takže mohou obě odhadovat na stejných komponentech projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č2 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Všechny úkoly projektu nebo prázdné </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Všechny úkoly projektu nebo prázdné </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Podle pravidla č. 4 jsou Č1 a Č2 dvě nabídky na různé příležitosti, takže mohou obě odhadovat na stejných komponentech stejného projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
P2 </p>
            </td>
            <td width="39" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="40" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Všechny úkoly projektu nebo prázdné </p>
            </td>
            <td width="45" valign="top">
                <p>
Ano </p>
            </td>
            <td width="46" valign="top">
                <p>
Ano </p>
            </td>
            <td width="43" valign="top">
                <p>
Ano </p>
            </td>
            <td width="41" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
