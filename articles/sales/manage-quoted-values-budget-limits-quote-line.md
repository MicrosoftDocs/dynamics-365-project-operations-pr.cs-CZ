---
title: Přehled řádků nabídky založené na projektu
description: Toto téma poskytuje informace o používání řádků nabídek založených na projektu pro práci na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea54d83b1e26d1ee3520dbfab9ba56ffd1191dc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181849"
---
# <a name="project-based-quote-lines-overview"></a>Přehled řádků nabídky založené na projektu

_**Platí pro:** Project Operations pro scénáře založené na zdrojích / položkách, které nejsou na skladě_

Řádky nabídek založených na projektu jsou navrženy tak, aby pomohly odhadnout projektovou práci na zakázce. Struktura řádku nabídky založené na projektu se rozšiřuje u odhadů projektu o následující koncepty:

- Způsob fakturace
- Mapování projektu
- Zahrnuté třídy transakcí
- Nepřekročitelný limit
- Nastavení účtovatelnosti
- Odhad pomocí podrobností řádku nabídky
- Zákazníci řádku nabídky

Následující tabulka poskytuje informace o polích na karrtě **Všeobecné** řádku nabídky založené na projektu. Tato pole pomáhají připravit základ pro podrobný počáteční odhad projektové práce.

| **Pole** | **Popis** | **Dopad na příjem dat** |
| --- | --- | --- |
| Jméno | Název řádku nabídky, který by vám měl pomoci identifikovat diskrétní součást nabídky, která se odhaduje. | Zkopírováno do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Způsob fakturace | U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z příslušného pole na řádku příležitosti. Toto pole zahrnuje dva hlavní smluvní modely podporované aplikací Dynamics 365 Project Operations:</br>- Pevná cena</br>- Čas a materiál.| Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Project | Pomocí tohoto volitelného pole můžete identifikovat projekt, který bude použit k provedení práce na této zakázce. Když je projekt mapován na řádek nabídky, pomáhá to při nastavení zpoplatněných úkolů a také při stanovení odhadu založeného na projektu do řádku nabídky jako podrobnosti řádku nabídky. Pokud projekt není mapován na řádek nabídky založené na projektu, odhad by měl být vytvořen ručně – vytvořením každé podrobnosti řádku nabídky. | Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Zahrnout čas | Příznak **Ano**/**Ne** určuje, zda budou časové transakce nebo náklady práce ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky. Hodnota **Ne** určuje, že časové transakce nebo náklady práce nebudou zahrnuty do odhadu na tomto řádku nabídky. Hodnota **Ano** určuje, že časové transakce nebo náklady práce budou zahrnuty do odhadu na tomto řádku nabídky. | Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Zahrnout výdaj | Příznak **Ano**/**Ne** určuje, zda budou výdajové náklady ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky. Hodnota **Ne** určuje, že výdajové náklady nebudou zahrnuty do odhadu na tomto řádku nabídky. Hodnota **Ano** určuje, že výdajové náklady budou zahrnuty do odhadu na tomto řádku nabídky. | Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Zahrnout poplatek | Příznak **Ano**/**Ne** určuje, zda budou poplatky ve vybraném projektu zahrnuty do odhadu na tomto řádku nabídky. Hodnota **Ne** určuje, že poplatky nebudou zahrnuty do odhadu na tomto řádku nabídky. Hodnota **Ano** určuje, že poplatky budou zahrnuty do odhadu na tomto řádku nabídky. | Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Nabízená částka | Jedná se o částku, která bude zákazníkovi nabídnuta za veškerou práci předpovídanou v tomto řádku projektové nabídky. U nabídky vytvořené z příležitosti se tato hodnota zkopíruje z pole **Rozpočet zákazníka** na řádku příležitosti. Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky na podrobnostech řádku nabídky. | Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Odhad daně | Toto je upravitelné pole, kde může uživatel přidat odhadovanou částku daně do řádku nabídky. Pokud má řádek nabídky založené na projektu podrobnosti řádku, je toto pole uzamčeno pro úpravy a je vytvořen jeho souhrn z částky daně na podrobnostech řádku nabídky. | Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Nabízená částka včetně daně | Toto pole představuje částku nabídky po zdanění a je pouze ke čtení. Částka v tomto poli se počítá jako *Nabízená částka + daň*. | Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Nepřekročitelný limit | Toto pole je upravitelné a je k dispozici pouze na řádcích nabídek založených na projektu, které mají nastaven způsob fakturace **Čas a materiál**. | Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |
| Rozpočet zákazníka | Toto pole je upravitelné a jeho hodnota se zkopíruje z příslušného pole na řádku příležitosti, když je nabídka vytvořena z příležitosti. | Hodnota tohoto pole je zkopírována do řádku projektové smlouvy, který je vytvořen z tohoto řádku nabídky, když je nabídka získána. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Pravidla ověření pro pole na kartě Všeobecné řádků nabídek založených na projektu

**Pravidlo 1** : Určitou třídu transakcí ve vybraném projektu lze zahrnout pouze do jednoho řádku nabídky založené na projektu.

**Pravidlo 2** : Pokud má příležitost více nabídek, mohou existovat řádky nabídky z různých nabídek, které všechny odkazují na stejný projekt a zahrnují stejnou třídu transakcí.

**Pravidlo 3** : Pokud nabídky nepatří ke stejné příležitosti, nemohou zahrnovat stejný projekt a třídu transakcí.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Příležitost</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Nabídka</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Řádek nabídky</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Zahrnout čas</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Zahrnout výdaj</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Zahrnout</strong>
                </p>
                <p>
                    <strong>poplatek</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Platné / Neplatné</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Důvod</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Porušení pravidla č. 1. Čas, náklady a poplatky za projekt P1 jsou zahrnuty v obou řádcích nabídky ŘN1 a ŘN2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Porušení pravidla č. 1. Čas a poplatky za projekt P1 jsou zahrnuty v obou řádcích nabídky ŘN1 a ŘN2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Platná </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Čas a poplatky za projekt P1 jsou zahrnuty v ŘN1.
Výdaje na projekt P1 jsou zahrnuty do ŘN2.
Neexistuje žádné překrývání položek zahrnutých v každém řádku nabídky, takže je platná.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Neplatný </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Porušení výše uvedeného pravidla č. 1. </p>
                <p>
Nabídka N1 zahrnuje čas, výdaje a poplatky za celý projekt P1.
                </p>
                <p>
ŘN2 zahrnuje čas, výdaje a poplatky za celý projekt P1 a překrývá se s tím, co je zahrnuto v N1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="54" valign="top">
                <p>
Platná </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Na základě pravidla č. 2 jsou N1 a N2 dvě nabídky u stejné příležitosti, takže mohou obě odhadovat položky pro stejné součásti projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č2 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN1 v N2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="54" valign="top">
                <p>
Platná </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Na základě pravidla č. 3 jsou N1 a N2 dvě nabídky u různých příležitostí, takže nemohou odhadovat položky pro stejné součásti stejného projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
P2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Č1 </p>
            </td>
            <td width="42" valign="top">
                <p>
ŘN1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="48" valign="top">
                <p>
Ano </p>
            </td>
            <td width="42" valign="top">
                <p>
Ano </p>
            </td>
            <td width="54" valign="top">
                <p>
Neplatný </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]